# Docker
Docker is an open source containerization platform  that allows packaging of applications into enevironments called containers.
Docker has several advantages
1. It iS fast
2. You can launch your container on any system
3. Once it is configured, you dont have to reinstal your dependencies again manually if you change computers
4. each of your environments are isolated

A Docker image is a file that contains the source code, libraries, dependencies, tools, and other files needed for an application to run. They are immutbale therfore  you cannot start or run them. You can only use that template as a base to build a container. A container is, ultimately, just a running image. Once you create a container, it adds a writable layer on top of the immutable image, meaning you can now modify it.

### How to push a docker container to dockerhub
 step1
 
 Sign up for a docker account
 step 2
 
 Create your first repository name it <your-username>/my-private-repo and set the visisbilty to privtae
 step 3
  
 Download and installl Docke desktop(Docker Engine on linux)
 step 4
  
 Create a dockerfile 
  
  ```
  FROM busybox
CMD echo "Hello world! This is my first Docker image."
  ```
  
  Build your doker image
  
  ```
  docker build -t <your_username>/my-private-repo 
  ```
  
  FIrst run the iamge to test it locally 
  ```
  docker run <your_username>/my-private-repo to test your Docker image locally.
  ```
  
  To push the docker image to Dockerhub, run
  ```
  docker push <your_username>/my-private-repo
  ```
  
  # Nextflow
  
  Nextflow is a worklow language that makes it easy to write data intensive computational  pipelines.
  It allows the execution of a pipeline project directly from  gitHUb repository. 
  You can run a github repo hosting a version of your workflow using a docker container run command a shown
  ```
  nextflow run <github_repo_name> -with-docker
  ``` 
  use the info commnad to show the project information
  ```
  nextflow info <github_repo_name>
  ```
  
 Nextflow allows the execution of a specific reivion ofyour project by using the -r command line option
  ```
 nextflow run <github_repo_name> -r dev
  ```
  
 Revision are defined by using Git tags or branches that are  defined in the project repository.
This allows a precise control of the changes made in your project files and dependencies over time. 
  
  # Singularity
  
Singularity is an open source  cross-platform  computer program that performs operating-system-level virtualization also known as containerization.Singularity images are created using a singularity file similar to Docker but uses a different syntax. 
  
 Creating a Sinularity file
  
  ```
  Bootstrap: docker
From: debian:stretch-slim

%environment
export PATH=$PATH:/usr/games/

%labels
AUTHOR <your name>

%post

apt-get update && apt-get install -y locales-all curl cowsay
curl -sSL https://github.com/COMBINE-lab/salmon/releases/download/v1.0.0/salmon-1.0.0_linux_x86_64.tar.gz | tar xz \
 && mv /salmon-*/bin/* /usr/bin/ \
 && mv /salmon-*/lib/* /usr/lib/
  ```
 After creating a filebuild an image using the commands below
  ```
  sudo singularity build my-image.sif Singularity
  ```
  Run the container
  ```
  singularity exec my-image.sif cowsay 'Hello Singularity'
  ```
  run the follwing command while i the container
  ```
  touch hello.txt
ls -la
  ```
  
You can create  a singularity container by using a docker container image by pulling the image from a docker registry using the command below as a an example
  ```
  singularity pull docker://debian:stretch-slim
  ```
  to run a nextflow script using singularity, use the singularity engine in place of docker in the Nexflow confuguration file using the -with-singularity command line option as shown below
  ```
  nextflow run script7.nf -with-singularity nextflow/rnaseq-nf
  ```
  
  
  
  
  

  
  
  
  
  
  
 
 
 
 
 
