# Strings Lab 1

## Instructions for lab submission

1. Fork the assignment repo
1. Clone your Fork to your machine
1. Complete the lab
1. Push your changes to your Fork
1. Submit a Pull Request back to the assignment repo
1. Paste a link to of your Fork on Canvas and submit

## Question 1

Write code that prints out all the numbers from 1 to 10 as a single string.
(Hint: the `String()` function can convert an Int to a String)
``` swift
let range = 1...10
var number = ""

for i in range {
number += String(i)
}
print(number)
```

``` swift
let range = 1...10
var number = ""

for i in range {
number += "\(i) "
}
print(number)
```
***
## Question 2

Write code that prints out all the even numbers from 5 to 51 as a single string.

``` swift
let range = 5...51
var allEvenNumbers = (String)()

for i in range where i % 2 == 0 {

// This format converts the integers to type string before inserting into "allEvenNumbers"

allEvenNumbers += String(i)
}

print (allEvenNumbers)


let range = 5...51
var allEvenNumbers = (String)()

for i in range where i % 2 == 0 {

// This format interpulates the integers within a string, allwing for a space and (,) to separate before inserting into "allEvenNumbers"

allEvenNumbers += String("\(i), ")
}
print (allEvenNumbers)
```
***
## Question 3

Write code that prints out every number ending in 4 between 1 and 60 as a single string.

``` swift
var range = 1...60
var lowerNum = 4
var upperNum = 60
var numbersThatEndWith4 = ""


while lowerNum < upperNum {

numbersThatEndWith4 += String(lowerNum)
lowerNum += 10
}
print (numbersThatEndWith4)
```
***
## Question 4

Print each character in the string `"Hello world!"`
``` swift
let characters = "hello world!"

for i in characters {
print (i)
}
```
***
## Question 5

Print out the last character in the string below.  You cannot use the Character literal "!" (i.e you must access `myStringSeven`'s characters).

`let myStringSeven = "Hello world!"`
``` swift
let myStringSeven = "Hello world!"
print(myStringSeven.last!)
```
***
## Question 6

Write code that switches on a string, given the following conditions:
- If the string's length is even, print out every character.
- If the string's length is odd, print out every other character.

``` swift
var item = "Pursuit"

if item.count % 2 == 0 {
print (item)
} else {

// using the (enumerated()) function which takes a string or an array and returns a sequence of (x, y)
// where x = to index and y = the element or value of the index

for (number,letter) in item.enumerated() {
if number % 2 != 0{
print (letter)
}
}
}
```
``` swift
switch item.count % 2 {
case 0 :
print (item)
default:
for (number,letter) in item.enumerated() {
if number % 2 != 0{
print (letter)
}
}

```
***
## Question 7

Initialize a String with a character. Show that it is a Character, and not another String, that you're using to initialize it.
``` swift
let string = "A"
type(of: string)
Character(string) == Character("A")
```
***
## Question 8

Build five pairs of **canonically equivalent** strings, the first of each being a pre-composed character and the second being one that uses combinable unicode scalars. Show that they are equivalent.
``` swift
let a = "á"
let b = "a\u{301}"

let firstLetter =  "ú"
let secondLetter =  "\u{0075}\u{301}"

let emogi = "🐥"
let emogi2 = "\u{1F425}"

let symbol1 = "\u{0025}"
let symbol2 = "%"

let symbol3 = "\u{0023}"
let symbol4 = "#"

print(a == b)
print (firstLetter == secondLetter)
print(emogi == emogi2)
print(symbol1 == symbol2)
print(symbol3 == symbol4)
```

***
## Question 9

**Using only Unicode**, print out `"HELLO WORLD!"`
``` swift
var uniCode = "\u{0048}\u{0045}\u{004c}\u{004c}\u{004f} \u{0057}\u{004f}\u{0052}\u{004c}\u{0044}\u{0021}"

print (uniCode)
```
***
## Question 10

**Using only Unicode**, print out your name.
``` swift
let myFullName = "\u{0041}\u{0059}\u{004f}\u{004f}\u{004c}\u{0041} \u{0041}\u{0042}\u{0055}\u{0044}\u{0055}"
print(myFullName)
```
***
## Question 11

**Using only Unicode**, print out `"HELLO WORLD!"` in another language.

***
## Question 12

Print the below flower box using the following information.

- The unicode number for ⚘ is U-2698
- The top and bottom of the box are represented by dashes and the rows are |
- Use the terminator argument in your print statements to print on the same line.
- Hint: It may be useful to try printing out a box of just one character to start then work your way from there.

```swift
Flower Box:
- - - - - - - - - - -
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
- - - - - - - - - - -
```
``` swift
var Flower = "\u{2698}"
let verticalSymbol = "\u{007c}"
let horizontalSymbol = "\u{005f}"
let range11 = 1...11
let range7 = 1...7

for _ in range11 {
print ("\(horizontalSymbol) ", terminator:"")
}
print()
print()


for _ in range7 {

print("\(verticalSymbol) \(Flower) \(verticalSymbol) \(Flower) \(verticalSymbol) \(Flower) \(verticalSymbol) \(Flower) \(verticalSymbol) \(Flower) \(verticalSymbol)")
}
for _ in range11 {
print ("\(horizontalSymbol) ", terminator:"")
}
```


***
## Question 13

Write a program that sets up a chess board using Unicode.

```swift
Chess Board:
♖ ♘ ♗ ♕ ♔ ♗ ♘ ♖
♙ ♙ ♙ ♙ ♙ ♙ ♙ ♙




♟ ♟ ♟ ♟ ♟ ♟ ♟ ♟
♜ ♞ ♝ ♛ ♚ ♝ ♞ ♜
```
```swift
var whiteChessPiece = "\u{2656}\u{2658}\u{2657}\u{2655}\u{2654}\u{2657}\u{2658}\u{2656}"
var whiteChessPiece2 = "\u{2659}\u{2659}\u{2659}\u{2659}\u{2659}\u{2659}\u{2659}\u{2659}"
var blackChessPiece = "\u{265c}\u{265e}\u{265d}\u{265b}\u{265a}\u{265d}\u{265e}\u{265c}"
var blackChessPiece2 = "\u{265F}\u{265F}\u{265F}\u{265F}\u{265F}\u{265F}\u{265F}\u{265F}"


for  i in whiteChessPiece{
print (i, terminator: " ")
}
print()
for i in whiteChessPiece2 {
print(i, terminator: " ")
}
for _ in 0...3{
print()
}
for  i in blackChessPiece2{
print (i, terminator: " ")
}
print()
for i in blackChessPiece {
print(i, terminator: " ")
}
```
***
## Question 14

You are given a string stored in the variable `aString`. Create new string named `replacedString` that contains the characters of the original string with all the occurrences of the character `"e"` replaced by `"\*"`.

```swift
var aString = "Replace the letter e with \*"
// Your code here
 ```

Example:

Input:
`var aString = "Replace the letter e with *"`

Expected values:
`replacedString = "R*plac* th* l*tt*r * with *"`

``` swift
var aString = "Replace the letter e with *"
var replacedString = ""

replacedString = aString.replacingOccurrences(of: "e", with: "*")
print (replacedString)
```
***
## Question 15

You are given a string stored in variable `aString`. Create a new string called `reverse` that contains the original string in reverse order. Print the reversed string.

Example:
Input:
`var aString = "Hello"`

Output:
`"olleH"`

```swift
var aString = "this string has 29 characters"
var reverse = ""

reverse += aString.reversed()
print(reverse)
```

***
## Question 16

You are given a string stored in variable `aString`. Print `true` if `aString` is a palindrome, and `false` otherwise. A **palindrome** is a string which reads the same backward or forward.


Example 1:
Input:
`var aString = "anutforajaroftuna"`

Output:
`true`

Example 2:
Input:
`var aString = "Hello"`

Output:
`false`

```swift

let aString = "anutforajaroftuna"
var reversedString = String(aString.reversed())

if aString == reversedString {
print (true)
}else {
print(false)
}

```

***
## Question 17

You are given a string stored in variable `problem`. Write code so that you print each word of the string on a new line.

```swift
var problem = "split this string into words and print them on separate lines"

// Your code
```

Example:
Input:
`var problem ="split this string into words and print them on separate lines"`

Output:
```swift
split
this
string
into
words
and
print
them
on
separate
lines
```
``` swift
var newProblem = problem.components(separatedBy: " ")

for i in newProblem {
print (String(i))
}
```
***
## Question 18

You are given a string stored in variable `problem`. Write code that prints the longest word in the string.

```swift

var problem = "find the longest word in the problem description"

var seperatedWords = problem.components(separatedBy: " ")
var largestWord = seperatedWords.max(by: { $1.count > $0.count })
if largestWord != nil{
print(largestWord!)
}
```

Example:
Input:
`var problem = "find the longest word in the problem description"`

Output:
`description`

Hint: Keep track of the longest word you encounter and also keep track of its length.

***
## Question 19

Given a string in English, create a tuple containing the number of vowels and consonants.

```swift
let vowels = "aeiou"
let consonants = "bcdfghjklmnpqrstvwxyz"
let input = "Count how many vowels I have!"
```

```swift
var tuple = (vowel: vowels ,numberOfVowel: vowels.count ,consonant: consonants, numberOfConsonant: consonants.count)
print(tuple.numberOfConsonant)

```

***
## Question 20

Given a string of words separated by a `" "`. Write code that prints out the length of the last word.

If there is no last word print out `"No last word"`.

Example:
Input: `"How are you doing this Monday?"`

Output: `7`

```swift
var words = "How are you doing this Monday?"
var lastWord = words.components(separatedBy: " ").last?.count
if lastWord != nil {
print(lastWord!)
}else {
print("no last word")
}
```
***

