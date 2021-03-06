# cs61a-notes

## lecture1

### topics

- manage program
- programming concepts
- interpreter

## lab0

- Manage files

### Python basics

- floating point division:` /`
- floor division(rounds down to an int):`//`

- Command lines
  - `-i`:run code and then open interactive session
  - `-m doctest`:run dockets surrounded by triple quotes
    - How to test?
    - expected output

## lecture2

### operator module

` add(),div()...`

- expression tree
- Assignment
- Function:
  - Signature(like a unique sign of function)
  - body

- calling function:a new frame
  - global
  - local
    - name lookup order:local frame->**global frame(read only)**

## lecture3

### Side effect

- **None**:not specify a returning value for a func
- void
- side effect:return None,call func **returning None** inside it
- Non-pure function

## functions features

- Doctests:check input/output

### statement

- compound statement
  - header
  - clause
  - suite:a sequence of statements

- conditional
  - if
  - elif

## Lecture4

### design functions

- domain
- range
- behavior
- one job->many situations
- DRY

## generalization

generalize common structure:extract common part

### High-order functions

- take another function as **argument or result**

- Argument:name of function->pointer
- return a function:define a func within other function,only in local frame

### Lambda

`**lambda** <parameters>: <return expression>`

- no return statements
- as an arg

### Conditional expression

`<consequent> if <predicate> else <alternative>`

same as 

x=x>0?x:0;

## lecture5

## multiple env

- stack frame
- a sequence of frames==a env

- Same Nate->closest one

### Higher-order

Functions<->values

### nested definitions

~~~python
def make_texter(emoji):
    def texter(text):
        return emoji + text + emoji
    return texter

happy_text = make_texter("😄")
result = happy_text("lets go to the beach!")
~~~

`happy_text` has an implicity and specified arg

### local names

Why python slow?

excute line by line,even if it doesn't do something,it push func into stack

---

not visible to other functions(not in the same local/global frame)

### function composition

not something comfortable...

### Self-reference

a function->a frame

` def`:only push into frame,not excute

### currying

Multiple arg->single-argument,higher-order

## lecture6

### Nameerror

- Variable-frame

## lecture7

### decorator

- syntax

~~~python
@ATTR
def aFunc(...):
    ...
~~~

Equal to

~~~python
def aFunc(...):
    ...
aFunc = ATTR(aFunc)
~~~

name from non-local frame is **read-only**!

a static attribute for func(e.g:calculate the number of time to call it):

~~~python
def hello():
    hello.counter += 1
    print(hello.counter)
hello.counter = 0
~~~

## lecture8

- Base case
- recursive case
- conditional statement

functional abstraction

Leap-faith(assume)

second digit：偶数

## lecture9

- put the base cases first

### tree recursion

**not only one** recursive call

## lecture10

### in operator

detect whether in a list

## for loop

~~~python
for <value> in <sequence>:
    <statement>
    <statement>
~~~

#### get specific element

~~~python
for <name> in <expression>:
	<suite>
~~~

Get an element from expression and **bind to name**

### range

a sequence of integers

[left(default==0),right)

### generate from another list

~~~python
[<map exp> for <name> in <iterable sequence> if <filter>(get correct element)]
~~~

### string

Multi-line strings automatically insert new lines

- Match substrings:use `in`

## lecture11

### slicing

[begin(default==0),end)

### helper function

### Built-in func

- Arg `key`:a lambda expression to compare

## lecture12

### dictionary

dict

- Key(**unique**)->value

- Iterate:in the order keys were added

~~~python
{key:value for <name> in <iter>}
~~~

## lecture13

**Recursive structure implies recursive algorithm!**
