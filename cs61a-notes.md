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