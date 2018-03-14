# 42 AIML

### Resources

#### Python
Learn **Python3** not Python2 [Why?](https://wiki.python.org/moin/Python2orPython3)

* [Quora Post - Free resources to learn Python](https://www.quora.com/What-are-some-good-free-resources-to-learn-Python)
* [/r/learnpython wiki](https://www.reddit.com/r/learnpython/wiki/index) Lots of resources here
* [CodeAcademy](https://www.codecademy.com/learn/learn-python)
* [CodeWars](http://www.codewars.com/?language=python) List of exercises and challenges to complete similiar to Hackerrank and Leetcode.com to practice

###### Free Online Books
* [InventWithPython](http://inventwithpython.com/) books on automating, encryption, and games
* [ThinkPython](http://greenteapress.com/wp/think-python-2e/)
* [DiveIntoPython3](http://www.diveintopython3.net/)
* [Tiny Python Notebook](https://github.com/mattharrison/Tiny-Python-3.6-Notebook/blob/master/python.rst) table of notes and examples for Python syntax (pretty short)

#### Data Science
* [101 Numpy Exercises for Data Analysis in Python](https://www.machinelearningplus.com/101-numpy-exercises-python/)
* [Data Science Notebooks Repo](https://github.com/donnemartin/data-science-ipython-notebooks)

#### Machine Learning
###### Books
* [Elements of Statistical Learning](https://web.stanford.edu/~hastie/Papers/ESLII.pdf)

#### Reinforcement Learning
###### Books
* [RL: An Introduction](http://web.stanford.edu/class/psych209/Readings/SuttonBartoIPRLBook2ndEd.pdf)
###### Course
* [UCL Course](http://www0.cs.ucl.ac.uk/staff/d.silver/web/Teaching.html)

#### Deep Learning
###### Courses
* [Fast.ai - Deep Learning for Coders](https://www.machinelearningplus.com/101-numpy-exercises-python/) Practical Deep Learning
	- [Fast.ai WIKI](https://www.machinelearningplus.com/101-numpy-exercises-python/)
* [Deeplearning.ai](https://www.deeplearning.ai/)
###### Course Notes
* [Standford CNN Course](http://cs231n.github.io/)
* [Standford DL Course](http://cs229.stanford.edu/syllabus.html)
###### Books
* [The Deep Learning Book](http://www.deeplearningbook.org/) ([PDF VERSION](https://github.com/janishar/mit-deep-learning-book-pdf/blob/master/complete-book-pdf/deeplearningbook.pdf))
* [Neural Networks and Deep Learning](http://neuralnetworksanddeeplearning.com/)

#### AI
* [Artificial Intelligence: A Modern Approach(AIMA) 3rd Ed PDF](https://www.ics.uci.edu/~rickl/courses/cs-171/aima-resources/Artificial%20Intelligence%20A%20Modern%20Approach%20(3rd%20Edition).pdf)
	* [AIMA Website](http://aima.cs.berkeley.edu/)

#### PyTorch
Learning and understanding the concepts are more important than the framework (i.e Pytorch or Tensorflow
* [Pytorch.org Tutorials](http://pytorch.org/tutorials/)
* [PyTorchZeroToAll Youtube Channel](https://www.youtube.com/playlist?list=PLlMkM4tgfjnJ3I-dbhO9JTw7gNty6o_2m)
* [Harvard ML Course for NLP](https://harvard-ml-courses.github.io/cs287-web/)
* Example Repos
	- [Practical Pytorch](https://github.com/spro/practical-pytorch)
	- [Pytorch Examples](https://github.com/jcjohnson/pytorch-examples)
	- [Pytorch Tutorial](https://github.com/yunjey/pytorch-tutorial)
	
##### Install PyTorch Globally
1. You should already have python3.6 installed(if you ran the brew setup guide below)
2. Go to [pytorch.org](https://pytorch.org)
3. Select
 * OS -> Mac OSX
 * Package Manager -> pip
 * Python -> 3.6 (you can verify the python version by running `python3 --version` in terminal)
 * CUDA -> doesn't matter, we aren't going to install GPU drivers yet
3. Copy what's in the **'Run this command:'** text box and paste into terminal
4. After it's finished you should be done. To verify:
	- `pip freeze | grep torch` should show you the version installed
	- run 
```Python
 import torch

 print(torch.__version__)
 ```

### How to install Python on Mac?
1. Install brew (PM marvin `!brew` for instructions)
2. ```brew install python3```

#### Install Tips
* Run and use `python3` in shell after you install to test syntax quickly
* To install packages run `pip3 install <package>`
	* install better REPL `ptpython` use that instead of `python3` interpreter to test code: `pip3 install ptpython` then in terminal run `ptpython`
* Run Pyton online [here](https://code.sololearn.com/#py)

#### Installing packages into a virtualenv (per project basis)
1. Install virtualenv package `pip3 install virtualenv`
	- If you run `pip3 freeze`, you'll get a list of all pip packages installed  and their versions globally.
2. Go to your project directory `cd <my_new_project_path>`
3. Run `python3.6 -m virtualenv venv` or `virtualenv venv`. It'll create a new folder to install your dependcies in.
4. There's also scripts created in the `venv` folder to `activate` a virtualenv
5. Let's activate it: `source venv/bin/activate`
	- You should notice that your terminal has changed. `(venv)` should be prepended to the front of the cmd line
6. Now when you install packages or run pip commands they'll be installed to and ran from the virtualenv
7. If you do `pip freeze`, you'll notice it returns an empty list.
	- Try to install a pip package and rerun `pip freeze`
9. Now you can install packages normally with pip or install all packages found in a 'requirements.txt' with `pip -r requirements.txt`
10. When you run your scripts(e.g. `python3.6 do_stuff.py` it'll use packages found in env first)
11. To leave or `deactivate` the environment simply enter `deactivate` into the cmdline.

### C/Python Differences ([Stackoverflow Link](https://www.quora.com/What-are-some-differences-between-C++-Python-and-C))
| C	| Python|
--- | ---
Procedural (list of instructions) |  Multi (Object-oriented + Procedural + Functional)
Static typed (int c = 10;) | Dynamic (c = 10)
Compiled (Source -> Target language) Slow to develop, Fast to execute | Interpreted (Source -> Intermediate -> Target) Fast to develop, Slow to execute
Whitespace insensitive | Whitespace sensitive
Manual memory management | Automatic memory management
Not easy to test | Very easy to test
Fast | Slow

### Why use Python?
1. We can get to what matters faster with lesswork. We can simply go straight to experimentation and testing much more quickly. For most applications, you won't notice the "slowness" of Python.
2. Most of the deep learning frameworks are written for or support Python.

#### Ex1 - Running a program
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

#### Ex2 - Loops, Whitespace
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

#### Ex3 - Return values
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

#### Ex4 - Variable assignemnt
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

#### Ex5 - Decrement/Increment operator
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

#### Ex6 - Import/Includes
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

#### Ex7 - Iterating over arrays
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

#### Ex8 - Passing arguments by value/reference?
* Better to Google search this one
