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
    - name lookup order:local frame->**global frame**

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