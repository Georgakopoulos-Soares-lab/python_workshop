# Python and Roar Collab Introductory Workshop

by Dr. Ilias Georgakopoulos-Soares, , Nikol Chantzi, Ioannis Mouratidis, Aksatha Nayak

## Instructions

Login to Roar Collab Dashboard: 
[dashboard](https://rcportal.hpc.psu.edu/pun/sys/dashboard)

Select Jupyter server and choose the settings below:
- Node type: Standard Cores
- Account: open
- Partition: open
- Number of hours: 3
- Number of Cores: 1


### Python Intro

**Jupyter Hints**
- Use Ctrl-Enter to execute cell (or play button on the top row)
- If you preface a command with ! it will be executed in bash, e.g. !pwd


#### First task
Learn how to print a phrase or variable

```
print(“hello”)
```
Use the + symbol to create new cells

Learn how to define and print variables

```
string_variable = "hello""
print(string_variable)
```

```
integer_variable = 20
print(integer_variable)
```

#### Second task

Learn how to write a for loop
The task is to print all integers from 1 to 10

First try:
```
for i in range(10):
    print(i)
```
Then:

```
for i in range(1, 11):
    print(i)
```

What are the differences?

#### Third task

Learning to use if statements. Print only even numbers between 1 and 10.

You can use modulo operator (%)

```
for i in range(1,11):
	if i%2==0:
    		print(i)
```

You could also use the step variable in range function!

```
for i in range(2, 11, 2):
	print(i)
```

#### Fourth task

Print every number from 1 to 10, but add text surrounding it indicating whether that number is odd or even. Learn if-else statements and string formatting

```
for i in range(1, 11):
	if i % 2:
    		print(f"{i} is an even number")
	else:
    		print(f"{i} is an odd number")
```

#### Fifth task: Creating a function

Print any input phrase

```
def phrase_printer(phrase):
	print(phrase)
```

Try:

```
phrase_printer("hello")
phrase_printer(“this is a function”)
```

Write a function that takes a list of number as input. For every even number it replaces it with its square, for every odd number it replaces it with its root. For non-integers it does nothing.

Hint: 
```
import math
math.sqrt(x)
```

Solution:
```
import math
def weird_function(my_list):
	for i in range(len(my_list)):
    		if my_list[i] % 2 == 0:
        		my_list[i] = my_list[i] ** 2
        	elif my_list[i] % 2 == 1:
            		my_list[i] = math.sqrt(my_list[i])
	return my_list  # Caution: This modified the list itself
```

#### Sixth task

Given a list of numbers 
```
[1, 2, 3, 10, 2, 3, 5]
```

try to find the length, maximum and minimum value and the total sum. Can you find how many times 3 occurs?
Create a function that calculates each of these quantities.

After you create this function, try to find an in-built function that sorts the list in reverse order.

#### Final task

Create groups of 3-4 people. Try to tackle any of the following challenges. Try to Google for things you don’t know. If you need help, call any of us.

**Challenges**

- You are given the length and width of a 4-sided polygon. The polygon can either be a rectangle or a square.
If it is a square, return its area. If it is a rectangle, return its perimeter. The shape can be either rectangle or square nothing else. If the inputs are equal assume it's a square.

    ```
    def calculate_square_or_perimeter(l, w):
        pass
        
    8, 10 --> 36 (rectangle)
    4, 4 --> 16 (square)
    ```
    
- Create a function that generates the Fibonnaci numbers up to the Nth number. The Fibonnaci numbers are a sequence of numbers that start with 0 and 1 and then every number is the sum of the previous two numbers.

- Create a function that takes as input a string and determines if it's a palindrome.

- Count the total sum between 1 and an integer number N that is given by the user. Test your function by inputing powers of 10, i.e. 10, 100, 1000, 10000, 100_000, 1_000_000. As N increases arbitrarily large what do you observe? Is there anyway to do this in a more efficient way?

- Generate a random integer. The user tries to guess it. The program provides a hint if the number is too high or too low. Bonus: Keep track of how many attempts the user has taken. 
Hint: use function input()

- Create a function that takes input as a string with letters from the nucleotide alphabet and returns it's reverse complement. If the input string contains any letter besides a, g, c or t, it should return the empty string.

- Create a function that takes as an input exactly one number and returns True if its prime, otherwise it returns false. Note that the number can be non-positive, in which case the function must return false.

**Advanced challenges**

- Write an algorithm that takes an array and moves all of the zeros to the end, preserving the order of the other elements.

    ```
    move_zeros([1, 0, 3, 0, 2, 1, 5, 0]) 
    # must return [1, 3, 2, 1, 5, 0, 0, 0]
    ```
    
- Your task is to make a function that can take any non-negative integer as an argument and return it with its digits in descending order. Essentially, rearrange the digits to create the highest possible number.
Examples:
    ```
    Input: 42145 Output: 54421
    Input: 145263 Output: 654321
    Input: 123456789 Output: 987654321
    ```

- Create a function that takes as input a string from the nucleotide alphabet (a, g, c or t) and translates it to protein sequence assuming the standard translation table. You should try to find a function that does this for you by searching the internet.

- Create a function that allows the user to play rock, paper, scissor (the computer picks randomly)
Hint: import random.choice

**Very advanced**

 - Your job is to create a calculator (a python function) which evaluates expressions in [Reverse Polish notation](https://en.wikipedia.org/wiki/Reverse_Polish_notation).
For example expression 5 1 2 + 4 * + 3 - (which is equivalent to 5 + ((1 + 2) * 4) - 3 in normal notation) should evaluate to 14. Note that between every letter provided there is a SPACE.  Empty expression should evaluate to 0. Valid operations are: +, -, *, /. You may assume that there won't be exceptional situations (like stack underflow or division by zero).

- Create a game of Tic-Tac-Toe for two players on the same computer



