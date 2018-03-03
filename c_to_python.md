# C -> Python

## Resources
* [Quora Post - Free resources to learn Python](https://www.quora.com/What-are-some-good-free-resources-to-learn-Python)

## How to install Python on Mac?
1. Install brew (PM marvin `!brew` for instructions)
2. ```brew install python3```

## Tips
* Run `python3` in shell after you install to test syntax quickly
* To install packages run `pip3 install <package>`
	* install `ptpython` and use that instead of `python3` interpreter to test code

## Differences ([Stackoverflow Link](https://www.quora.com/What-are-some-differences-between-C++-Python-and-C))
| C	| Python|
--- | ---
Procedural (list of instructions) |  Multi (Object-oriented + Procedural + Functional)
Static typed (int c = 10;) | Dynamic (c = 10)
Compiled (Source -> Target language) Slow to develop, Fast to execute | Interpreted (Source -> Intermediate -> Target) Fast to develop, Slow to execute
Whitespace insensitive | Whitespace sensitive
Manual memory management | Automatic memory management
Not easy to test | Very easy to test
Fast | Slow

## Why use Python?
1. We can get to what matters faster with lesswork. We can simply go straight to experimentation and testing much more quickly. For most applications, you won't notice the "slowness" of Python.
2. Most of the deep learning frameworks are written for or support Python.

### Ex1 - Running a program
```C
// C - hello_world.c
#include <stdio.h>

int	main(void)
{
	char *s = "Hello, World!";
	
	printf(s);
}
```

```shell
gcc hello_world.c -o hello_world.o
./hello_world.o
```

```Python
# Python - hello_world.py
s = "Hello, World" # Python has no declarations
print(s)
```
```shell
python hello_world.py
```

* You can add a `def main()` to `hello_world.py`
* note the commenting is different
	* `#` for python to end of line
	* `//` to end of line or `/* STUFF */` for multi-line comments

### Ex2 - Loops, Whitespace
```C 
// C
#include <stdio.h>

void	ft_nprint(const char *s_even, const char *s_odd, int c)
{
	while (c--)
	{
		if (c % 2 == 0 && c % 3 == 0)
		{
			printf(s_even);
			printf(s_odd);
		}
		else if (c % 2 == 0)
			printf(s_even);
		else if  (c % 3 == 0)
			printf(s_odd);
		else
			printf("NEVER");
	}
}
```

```Python
#Python

def	ft_nprint(s_even, s_odd, c):
	while (c):
		if (c % 2 == 0 and c % 3 == 0):
			print(s_even)
			print(s_odd)
		elif (c % 2 == 0):
			print(s_even)
		elif (c % 3 == 0):
			print(s_odd)
		else:
			print("NEVER")
		c -= 1
```

* Whitespace matters in Python but you don't need brackets or semi-colons

### Ex3 - Return values
```C
// C

int	sum(int a, int b)
{
	return (a + b);
}
```

```Python
# Python

def	sum(a, b):
	return a + b
```

### Ex4 - Variable assignemnt
```Python
# Python

def main():
	x = y = 0
	a, b, c = 1, 2, 3 # a = 1, b = 2, c = 3
```

```C
// C

int main(void)
{
	int x, y;
	int a, b, c;
	
	x = y = 0;
	a = 1;
	b = 2;
	c = 3;
}
```

### Ex5 - Decrement/Increment operator
```Python
# Python

i = 10
while (i):
	print(i)
	i -= 1
```

```C
// C

int i = 10;

while (i--)
	printf(i);
```

### Ex6 - Import/Includes
```Python
# Python

from math import sqrt

def main():
	print("Sqrt of 10 is {}", sqrt(10));
```
```C
// C
#include <stdio.h>
#include <math.h>


int main(void)
{
	printf("Sqrt of 10 is %d", sqrt(10));
}
```

### Ex7 - Iterating over arrays
```Python
# Python

nums = [1, 2, 3, 4, 5]

for i in range(0, len(nums)):
	print(nums[i]) # iterate using an index
```
```C
// C
int size = 5;
int nums[] = [1, 2, 3, 4, 5];

for (i=0; i < size; i++)
	printf(nums[i]);
```

* You can't iterate over arrays using pointers in Python
* There aren't any pointers in Python

### Ex8 - Passing arguments by value/reference?
* Better to Google search this one