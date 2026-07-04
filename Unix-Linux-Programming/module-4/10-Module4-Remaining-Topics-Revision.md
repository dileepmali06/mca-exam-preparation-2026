# Module 4 Revision (Topics 4.2.7 -- 4.2.10)

> **Module:** VI Editor and Shell Programming\
> **Topics Covered:** - 4.2.7 Test Command - 4.2.8 For Loop - 4.2.9
> While & Until Loop - 4.2.10 Case Statement

------------------------------------------------------------------------

# 4.2.7 Test Command

The `test` command checks conditions in shell scripts. It is commonly
used with the `if` statement.

``` bash
test 10 -gt 5
```

Equivalent form:

``` bash
[ 10 -gt 5 ]
```

## Numerical Test Operators

  Operator   Meaning
  ---------- -----------------------
  `-eq`      Equal
  `-ne`      Not Equal
  `-gt`      Greater Than
  `-lt`      Less Than
  `-ge`      Greater Than or Equal
  `-le`      Less Than or Equal

Example:

``` bash
[ 20 -gt 10 ]
```

## String Test Operators

``` bash
[ "$A" = "$B" ]
[ "$A" != "$B" ]
[ -z "$A" ]
[ -n "$A" ]
```

## File Test Operators

``` bash
[ -f file.txt ]
[ -d folder ]
[ -e file.txt ]
[ -r file.txt ]
[ -w file.txt ]
[ -x script.sh ]
```

------------------------------------------------------------------------

# 4.2.8 For Loop

The **for loop** executes a block of commands repeatedly.

## Syntax

``` bash
for variable in list
do
    commands
done
```

## Example

``` bash
#!/bin/bash

for i in 1 2 3 4 5
do
    echo $i
done
```

------------------------------------------------------------------------

# 4.2.9 While & Until Loop

## While Loop

Runs while the condition is true.

``` bash
i=1

while [ $i -le 5 ]
do
    echo $i
    i=$((i+1))
done
```

## Until Loop

Runs until the condition becomes true.

``` bash
i=1

until [ $i -gt 5 ]
do
    echo $i
    i=$((i+1))
done
```

### Difference

  -----------------------------------------------------------------------
  While                               Until
  ----------------------------------- -----------------------------------
  Runs while condition is TRUE        Runs until condition becomes TRUE

  Stops when condition becomes FALSE  Stops when condition becomes TRUE
  -----------------------------------------------------------------------

------------------------------------------------------------------------

# 4.2.10 Case Statement

Used for multiple-choice decision making.

## Syntax

``` bash
case variable in

value1)
commands
;;

value2)
commands
;;

*)
default
;;

esac
```

## Example

``` bash
#!/bin/bash

echo "Enter Choice"
read CHOICE

case $CHOICE in
1) echo "Add" ;;
2) echo "Delete" ;;
3) echo "Update" ;;
*) echo "Invalid Choice" ;;
esac
```

------------------------------------------------------------------------

# Difference Between IF and CASE

  IF                            CASE
  ----------------------------- -------------------------------
  Checks conditions             Checks multiple values
  Best for complex conditions   Best for menu-driven programs

------------------------------------------------------------------------

# Quick Revision

## Test Command

``` bash
test
```

or

``` bash
[ condition ]
```

## Loops

``` bash
for ... do ... done
while ... do ... done
until ... do ... done
```

## Case

``` bash
case ... esac
```

------------------------------------------------------------------------

# Important Commands

``` text
test
for
while
until
case
```

------------------------------------------------------------------------

# MCQs

**Q1. Which command checks conditions?**

A. echo\
B. test\
C. pwd\
D. ls

**Answer:** B

------------------------------------------------------------------------

**Q2. Which loop runs while the condition is true?**

**Answer:** While Loop

------------------------------------------------------------------------

**Q3. Which statement is used for multiple choices?**

**Answer:** Case Statement

------------------------------------------------------------------------

# Interview / Viva Questions

1.  What is the `test` command?
2.  Differentiate between `while` and `until`.
3.  Explain the `for` loop.
4.  Explain the `case` statement.
5.  Differentiate between `if` and `case`.

------------------------------------------------------------------------

# Summary

-   `test` checks conditions.
-   `for` repeats over a list.
-   `while` runs while the condition is true.
-   `until` runs until the condition becomes true.
-   `case` is used for multiple-choice decision making.

------------------------------------------------------------------------

# Module 4 Status

-   ✅ VI Editor Completed
-   ✅ Shell Script Introduction
-   ✅ Execution Methods
-   ✅ Positional Parameters
-   ✅ Variables
-   ✅ Operators
-   ✅ IF Statement
-   ✅ Test Command
-   ✅ For Loop
-   ✅ While & Until Loop
-   ✅ Case Statement

**🎉 Module 4 Completed Successfully**
