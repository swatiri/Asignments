### Question 2

Question:
Write a program which can compute the factorial of a given numbers.
The results should be printed in a comma-separated sequence on a single line.
Suppose the following input is supplied to the program:
8
Then, the output should be:
40320

Hints:
In case of input data being supplied to the question, it should be assumed to be a console input.

```
def factorial(n):
    value = 1
    for i in range(1, n+1):
        value = value * i
    return value

number = int(input("Type a number: "))
print(factorial(number))

```

### Question 7
Level 2

Question:
Write a program which takes 2 digits, X,Y as input and generates a 2-dimensional array. The element value in the i-th row and j-th column of the array should be i*j.
Note: i=0,1.., X-1; j=0,1,¡­Y-1.
Example
Suppose the following inputs are given to the program:
3,5
Then, the output of the program should be:
[[0, 0, 0, 0, 0], [0, 1, 2, 3, 4], [0, 2, 4, 6, 8]] 

Hints:
Note: In case of input data being supplied to the question, it should be assumed to be a console input in a comma-separated form.

```
row_num = int(input("Input number of rows: "))
col_num = int(input("Input number of columns: "))
multi_list = [[0 for col in range(col_num)] for row in range(row_num)]

for row in range(row_num):
    for col in range(col_num):
        multi_list[row][col]= row*col

print(multi_list)

```

### Question 10

Level 2

Question:
Write a program that accepts a sequence of whitespace separated words as input and prints the words after removing all duplicate words and sorting them alphanumerically.
Suppose the following input is supplied to the program:
hello world and practice makes perfect and hello world again
Then, the output should be:
again and hello makes perfect practice world

Hints:
In case of input data being supplied to the question, it should be assumed to be a console input.
We use set container to remove duplicated data automatically and then use sorted() to sort the data.

```
phrase = input("Type in: ")
phrase_splited = phrase.split(' ')

word_list = []
for i in phrase_splited:
    if i not in word_list:
        word_list.append(i)
    else:
        continue
word_list.sort()
print((' ').join(word_list))
```

Level 2

### Question 12

Write a program, which will find all such numbers between 1000 and 3000 (both included) such that each digit of the number is an even number.
The numbers obtained should be printed in a comma-separated sequence on a single line.

Hints:
In case of input data being supplied to the question, it should be assumed to be a console input.

```
numbers = []
for x in range (1000, 3002):
    numSplit = [int(d) for d in str(x)]
    odd = False
    for y in range (1, len(numSplit)):
        if numSplit[y] % 2 != 0:
            odd = True
    if (odd == False):
        numbers.append(x)
print (numbers)

```


### Question 17
Level 2

Question:
Write a program that computes the net amount of a bank account based a transaction log from console input. The transaction log format is shown as following:
D 100
W 200

D means deposit while W means withdrawal.
Suppose the following input is supplied to the program:
D 300
D 300
W 200
D 100
Then, the output should be:
500

Hints:
In case of input data being supplied to the question, it should be assumed to be a console input.

Level 1

### Question 24

Python has many built-in functions, and if you do not know how to use it, you can read document online or find some books. But Python has a built-in document function for every built-in functions.

Please write a program to print some Python built-in functions documents, such as abs(), int(), raw_input()

And add document for your own function
Hints:
The built-in document method is __doc__

```
def SumNum(*args):
    result=0
    for i in args:
        result=i
    return i
    
print(SumNum.__doc__)
print("\n"+"-"*100+"\n")
print(abs.__doc__)
print("\n"+"-"*100+"\n")
print(int.__doc__)
print("\n"+"-"*100+"\n")
print(input.__doc__)
```

### Question 37

Define a function which can generate and print a list where the values are square of numbers between 1 and 20 (both included).

Hints:

Use ** operator to get power of a number.
Use range() for loops.
Use list.append() to add values into a list.
```
def printValues():
	l = list()
	for i in range(1,21):
		l.append(i**2)
	print(l)
		
printValues()
output
[1, 4, 9, 16, 25, 36, 49, 64, 81, 100, 121, 144, 169, 196, 225, 256, 289, 324, 361, 400]
```

### Question 41

Define a function which can generate and print a tuple where the value are square of numbers between 1 and 20 (both included). 

Hints:

Use ** operator to get power of a number.
Use range() for loops.
Use list.append() to add values into a list.
Use tuple() to get a tuple from a list.

```
a=[]
for i in range(1,21):
    a.append(i**2)
print(tuple(a))

output
(1, 4, 9, 16, 25, 36, 49, 64, 81, 100, 121, 144, 169, 196, 225, 256, 289, 324, 361, 400)

```



### Question 42

With a given tuple (1,2,3,4,5,6,7,8,9,10), write a program to print the first half values in one line and the last half values in one line. 

Hints:

Use [n1:n2] notation to get a slice from a tuple.
```
my_tuple=(1,2,3,4,5,6,7,8,9,10)
print("tuple_1", str(my_tuple))
result=tuple(my_tuple[x:x +5]
    for x in range(0, len(my_tuple), 5))
print("final_tuples", str(result[0]))
print("final_tuples", str(result[1]))

output
tuple_1 (1, 2, 3, 4, 5, 6, 7, 8, 9, 10)
final_tuples (1, 2, 3, 4, 5)
final_tuples (6, 7, 8, 9, 10)

```


### Question 45

Write a program which can filter even numbers in a list by using filter function. The list is: [1,2,3,4,5,6,7,8,9,10].

Hints:

Use filter() to filter some elements in a list.
Use lambda to define anonymous functions.

```
numbers=[1,2,3,4,5,6,7,8,9,10]
even_numbers_iterator=filter(lambda x: (x%2 ==0), numbers)
even_numbers=list(even_numbers_iterator)
print(even_numbers)

output
[2,4,6,8,10]

```
