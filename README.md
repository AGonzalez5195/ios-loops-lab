# Loops Lab


## Question 1

Write code that prints all the numbers from 1 to 150, **inclusive.**

```
var range = 1...150

for num in range {
    print (num)
}
```
## Question 2

Write code that prints all the numbers from 142 to 159, **exclusive.**

```
var range = 142..<159

for num in range {
    print (num)
}
```
## Question 3

Write code that prints only the even numbers from 15 to 80, **inclusive.**

```
var range = 15...80

for num in range where num % 2 == 0 {
    print (num)
}
```
## Question 4

Write code that prints only the odd numbers from 19 to 51, **inclusive.**

```
var range = 19...51

for num in range where num % 2 != 0 {
    print (num)
}
```
## Question 5

Write code that prints all the numbers that end in a **5** from 1 to 100, **exclusive.**

```
var range = 1..<100

for num in range where num % 5 == 0 && num % 2 != 0 {
    print (num)
}

```

## Question 6

Write code that prints all the numbers that end in a 7 from 1 to 40, **inclusive.**

```
var range = 1...40

for num in range {
    if num % 10 == 7 {
        print(num)
}
}
```
***
## Question 7

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that are divisible by 3`

```
var range = 20...150

for num in range {
    if num % 3 == 0 {
        print(num)
}}

```
## Question 8

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that are divisible by 2 and 3`

```
var range = 20...150

for num in range {
    if num % 2 == 0 && num % 3 == 0 {
        print(num)
}
}
```
***
## Question 9

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that end with a 4`

```
var range = 20...150

for num in range {
    if num % 10 == 4 {
        print(num)
}}

```
***
## Question 10

Given a range of numbers from 20 to 150, print out all the numbers that follows these conditions:

`Print out numbers: 31, 35, 40 to 60.`

```
let range = 20...150

for num in range where num == 31 {
    print(num)
}

for num in range where num == 35 {
    print(num)
}

for num in range where num >= 40 && num <= 60 {
    print(num)
}
```
***
## Question 11

Without using Xcode, how many times will the loop below run?  Explain why.

```swift
var i = 5

while (i > 3) {
    i += 1
}
```
Infinite loop. This is because the initial value of i, 5, is greater than 3. So long as i is greater than 3, the loop will continue. 


***
## Question 12

Change the code below to make the loop stop executing when i reaches 9.

```swift
var i = 5

while (i > 3) {
    i += 1
}
```
```var i = 5

while (i < 9) {
    i += 1
}


```

***
## Question 13

Change the code below to make the loop stop executing after it has run 1,000 times.

```swift
var i = 5

while (i > 3) {
    i += 1
}
```
```
var i = 5

while (i < 1005) {
    i += 1
}
```

***
## Question 14

Change the code below to make the loop stop executing after it has run 1,000 times and also make it print out the current value of i **only if i is an even number.**

```swift
var i = 5

while (i > 3) {
    i += 1
}
```
```
var i = 5

while (i < 1005) {
    i += 1
    if i % 2 == 0 {
        print(i)
}
}
```
I wasn't sure if the question wanted 1000 even numbers generated or if it wanted the even numbers from the 1000 numbers already generated. 

***
## Question 15

What's the difference in syntax between the following two while loops?  Will their outputs be different?  Explain why or why not.

```swift
var i = 1
//loop one
while i <= 10 {
    print("i = \(i)")
    i += 1
}

//loop two
var i = 1

repeat {
    print("i = \(i)")
    i += 1
} while i <= 10
```
Both outputs are the same. The difference in syntax comes from loop 2 using a repeat statement which signals the code to repeat the action in the curly brace for as long as the condition is true. The condition is given after the brace as a "while" element. Loop does not use a repeat and instead opts for using a while statement only to define what the conditions for the loop are. Both loops are instructed to print the string "i" as being equal to the value saved in i followed by incrementing it by 1 up until reaching 10.
***
## Question 16

What's the difference between `break` and `continue`?  Give an example that demonstrates their differences.

A break statement stops the execution of the loop when the condition is satisfied. A continue statement moves onto the next iteration when the condition is satisfied. As an example:
```
var range = 1...10

for number in range {
    if number == 3{
        break
    }else {
        print(number)
    }
}
```
This uses a break element. The computer will go through the numbers in the range 1 through 10 and will list them. It will list 1, then 2, but since the code instructs it to break the loop when it encounters a 3, it will end the execution of the loop there and will not do anything else. The output will therefore be the numbers 1 and 2.

```
var range = 1...10

for number in range {
    if number == 3{
        continue
    }else {
        print(number)
}
}
```
This uses a continue element. The computer will go through the numbers in the range 1 through 10 and will list them. It will list 1 then 2 but, unlike a break, it will see that when the number is equal to 3, it is instructed to move on to the next iteration. What this means is that it will continue the loop for the following numbers but will not execute it for 3. The output will consist of the numbers 1 through 10 but not including 3.

***
## Question 17

Without using Xcode, what will the loop below print? Select all that apply.

```swift
for i in 1...10 {
    if (i >= 4 && i <= 7){
        continue
    }
    print(i)
}
```

[✓]1
[✓]2
[✓]3
[]4
[]5
[]6
[]7
[✓]8
[✓]9
[✓]10


***
## Question 18

Without using Xcode, what will the loop below print? Select all that apply.

```swift
for i in 1...10 {
    if (i >= 4 && i <= 7){
        break
    }
    print(i)
}
```

[✓]1
[✓]2
[✓]3
[]4
[]5
[]6
[]7
[]8
[]9
[]10

***
## Question 19

Without using Xcode, what will the loop below print?  Explain below.

```swift
outerloop: for x in 1...3 {
    innerloop: for y in 1...3 {
        if y == 2{
            continue outerloop
        }
        print("x = \(x), y = \(y)")
    }
}
```
The outerloop goes through the numbers in the inclusive range of 1 to 3, and then the innerloop also goes through the inclusive range of 1 to 3. The inner loop is performed for each value of the outerloop but there is a condition that states that when the value of y is equal to 2, continue back to the outerloop. Because it is stated as "continue outerloop" as opposed to just "continue", the argument is evaluated only once instead of evaluating 1, skipping 2, and evaluating 3. y is then listed as equal to 1 3 times since the outerloop has a range of 3 numbers. The range maximum of the innerloop does not make any difference. The print line uses string interpolation to format the results as being
x = 1, y = 1
x = 2, y = 1
x = 3, y = 1
## Question 20

Write code that prints out all the points in the area bounded by (0,0), (10,0), (0,10) and (10,10) **where** x and y are both integers.

```
var range = 0...10

for x in range {
    for y in range {
        print("(\(x),\(y))", separator: " ", terminator: " ")
        }
    print("")
}
```
***
## Question 21

Write code that prints out all the points in the area bounded by (0,0), (10,0), (0,10) and (10,10) **where** the difference of x and y is at least 5, and x and y are both integers.

```
var range = 0...10

for x in range {
    for y in range {
        if x - y >= 5 {
            print("(\(x),\(y))",separator: "", terminator: " ")
}
    print("")
}
}
``` 
***
## Question 22

Print the first `N` square numbers. A **square number**, also called perfect square, is an integer that is obtained by squaring some other integer; in other words, it is the product of some integer with itself (ex. 1 = 1*1, 4 = 2 * 2, 9 = 3* 3 …).

Example:
Input: `var N = 5`

Output:
```swift
1
4
9
16
25
```
--------------------
```
var N = 5

for x in 1...N {
    print(x*x)
}

```
***
## Question 23

Given an integer N draw a square of N x N asterisks. Look at the examples.

Example 1:
Input: `var N = 2`

Output:
```swift
**
**
```

Example 2:
Input: `var N = 3`

Output:
```swift
***
***
***
```

Hint 1
Try printing a single line of * first.

Hint 2
You can use print("") to print an empty line.

```
var N = 3

for _ in 1...N {
    for _ in 1...N {
        print("*", separator: " ", terminator: " ")
}
    print("")
}
```
***

