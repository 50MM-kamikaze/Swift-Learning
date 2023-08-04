# Starting 
---
- Who.What = Value 
	- who needs to be changed , what need to be changed , whats the value you wanna give 
- Naming systems
	- camelCase
	- kebab-case 
	- snake_case
# Comments 
---
- // used for comments 
```swift 
		//print("Button got Tapped.")
        //diceImageViewOne.image = UIImage(imageLiteralResourceName: "DiceFour")
        //diceImageviewTwo.image = UIImage(imageLiteralResourceName: "DiceFour")
        // above lines is self explainitory
```
# Print Function
---
```swift
//import UIKit

//var greeting = "Hello, playground"
print("Hello World")
print("Hello \(3+2) is a number")

```
- Above this is called String Interpolation 
- print statements are really useful when the app does not work as expected 
# Array 
---
- to create an Array we use '[ ]' 
```swift 
var array = [1,23,4,5]

print(array[0]) //gives '1' as output
```
- for accessing the elements from an array we add another square braket then give a number 
- Elements start from 0 in arrays 
- we can store an array in a variable 
# Creating variables 
---
- we use "var" for creating variables in swift 
```swift 
var Angela = 203874 
```
- Angela is the label for 203874 is the data 
```swift 
var a = 5 
var b = 6 
print()
```
# Constant numbers 
---
- we use let for creating a constant number 
- once defined, cannot be changed 
```swift 
let Number = Int.random(in:1...10)
```
# Range of number and randomization
---
```swift 
Int.random(in: 1...10) //the three dots are used for closed range operator 
Int.random(in: 1..< 10) // gets a random number between 1 and 10 not including 10 
Float.random(in: 0 ..< 10) // gets a float random number 
Bool.random() //either true or false , completly random
Array.shuffel() // well self explannitory
```
- Will create a random number in the range on 1 and 10 , including both 
# range operator 
---
```swift 
a...b // closed raage 
a..>b // half open range 
...b // one sided range
```
# Data types 
---
- Int = integer (also negatives)
- string = "this is a string"
- Float = Floating Point Number 
- Double = more numbers after the decimal place 
- Bool = True / False 
- Array = ["This " , "is an array"]
- Dictionary = [key : value] pairs 
- Optional (?) 
	- look in [Swift Optionals: How to Use them (With Examples)](https://www.programiz.com/swift-programming/optionals#:~:text=However%20there%20is%20another%20data,optional%20as%20a%20shoe%20box.) for more explanation
# Functions 
---
- Two stages in a function 
	- creating a function
	- calling the function
- Functions will package items which can be used again in the code , by calling the function name
```swift 
func getMilk(){
			   //code 
}

getMilk() //calling the function
```
> Scope = it describes when a function can be accessed or used

```swift 
func greeting1() {
    print("function called")
    var myName = "samhith"
    print(myName)
}

func greeting2() {
    print("ssup")
    print(myName)
}
greeting1()
greeting2()

```
- above code will give a an error , cause myName is created inside the greeting1 and cannot be used in greeting2 
	- cause myName is created inside the greeting1
- A simple example 
```swift 
func greeting1() {
    print("function called")
    var myName = "samhith"
    func greeting2() {
        print("ssup")
    }
    print(myName)
    greeting2()
}


greeting1()
```
- Functions with inputs 
```swift 
func myFunction(parameter: Datatype){
// Input 

}
```

```swift
var age: String = "Three" // here we are specifying the DataType, the data and Datatype should match for sure when mentioned 

func greeting2 (whoToGreet: String) {
    print("hello, \(whoToGreet)")
}
greeting2(whoToGreet: "Samhith")
```
- kinda complex but sure you will get it bruh 
# conditional Statements 
---
```swift 
if traffic == "green" {
					   go()
}
else if traffic == "amber" {
							useYourJudgement()
}
else {
	  stop()
}
```
- above shows the syntax for if , else if and else statements 

>Comparison operator 
	1. == is equal to
	2. != is not equal to
	4. > greater than
	5. < less than
	6. >= greater than or equal to 
	7.  <= less than or equal to 

> Operators 
	1. && and 
	2. || Or 
	3. ! Not 

# Switch statements 
---
```swift 
switch hardness {
	case "Soft" :
		print(5)
	case "Medium" :
		print(5)
	case "Hard" :
		print(5)
	default :
		print("Error")
}
```
- we can choose which case we want based on the case statements 
- If you have more than 5 statements of if-else conditions its better to use switch statements 
> example for switch statements 
```swift 
func loveCalculator() {
    let loveScore = Int.random(in: 0...100)
    switch loveScore {
    case 81...100:
        print("kanye loves kanye")
    case 41..<81:
        print("coke and mentos")
    case 0..<41:
        print("its better to forget bruh")
    default:
        print("error occurred")
    }
}

loveCalculator()

```
# Dictionaries
---
- Syntax ;
```Swift 
var dict = ["brewary" : "a place where beer is made"]
```
- not limited to a single key value pair , can have multiple pairs 
- it can have different data types for keys and values separately 
```swift 
var dict : [string : Int] = ["samhith" : 145 , "preetam" : 145]
```
- In the above case , when we type the key value pairs , we need to make them as same data type as mentioned 
- calling the pairs can be done as shown
```swift 
dict ["samhith"]
```

# optionals 
--- 
- ! and ? are called optionals 
- when we make a variable , we can add a '?' at the end to make it optional variable 
	- it states that , it can be a variable or a nil (Nothingness)
- but where as '!' 
	- states that , "Im pretty sure this will have a data other than nil"
```swift 
var playerUsername: String = nil // This cannot be done  Case 2

var playerUsername: String? = nil // This can be done  Case 1

var unWrrapedUsername = playerUsername! // we can even unwrap by 

```
- When we print the DataType for the case 2 when the value is nil it will give a Optional DataType
```swift 
print(playerUsername!) // This will make the app crash
```
# Structures 
---
- used to create custom data types 
```swift 
struct name_of_structure {
	let constant = ["value"] //some properties 
	func new_shit() {
	print("New Shit")
	}
}

name_of_structure () //initilializing the structure 

var Name = name_ofstructure ()
Name.constant // is method , to access the "value"

//for adding new string 

Name.constant.append("samhith" : "Beeravelli")

//when function created inside a structure , we call that a method 

Name.new_shit() //will print("New Shit")

```
