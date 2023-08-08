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
- Angela is the label for 203874 data 
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
## making timer 
---
```swift 
import AVFoundation 
```

```swift
timer = Timer()
```

```swift 
timer = Timer.scheduledTimer(timeInterval: 0.2, target: self, selector: #selector(updateUI), userInfo: nil, repeats: false) // #selector includes updateUI , a @objc func , need to define it 
```

```swift
@ objc func updateUI() {
	//write function 
}
```
## Internal and External parameters 
```swift 
  func checkAnswer(Answer userAnswer: String) {
    //Answer is the external parameter
    //userAnswer is used as internal parameter
	//used to not get confused when using the function which has same variable name as the parameter there we       can just use "Answer" parameter
    //print("userAnswer")
```
- if you dont want to give a external parameter at all 
```swift 
func checkAnswer(_ userAnswer: String) {
//code 
}
```
## functions with outputs and returns 
- if we wanna produce an output we will provide a return arrow and the datatype its gonna return 
```swift 
func getMilk (Money: Int) -> Int {
		let change = Money - 1
		return change
}

var new_var = getmilk(4) //this is gonna give a value of 2 for the new_variable
```
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

- Structures have methods (functions in side structures ) and properties (says whats the structures is like) 
	-  properties are like , var colour = "red" for a car 
	- methods are like , func move() { print("move forward")} 
- when we making a structure we are making a blue print , then we need to initialize to make it an object
- when we want to make more structures similar to the before , we use the old structures as blueprint then change that accordingly 
```swift 
struct Town {
    let name: String
    var citizen: [String]
    var resources:[String : Int] //blank properties
    
    init(townName: String , people: [String] , stats: [String:Int]) {
        name = townName
        citizen = people
        resources = stats
    }
    func fortify() {
        print("defences Up")
    }
}

var anotherTown = Town(townName: "anotherTown", people: ["Town hanks"], stats: ["coconuts" : 100])
print(anotherTown.citizen)
anotherTown.citizen.append("willson")
anotherTown.fortify()

```
## self 
	- we cannot do the below code , it gives an error
```swift 
struct Town {
    let name: String
    var citizen: [String]
    var resources:[String : Int] //blank properties
    
    init(name: String , citizen: [String] , resources: [String:Int]) {
        name = name
        citizen = citizen
        resources = resources
    }
    func fortify() {
        print("defences Up")
    }
}

var anotherTown = Town(townName: "anotherTown", people: ["Town hanks"], stats: ["coconuts" : 100])
print(anotherTown.citizen)
anotherTown.citizen.append("willson")
anotherTown.fortify()

```
- self keyword references to eventual object that will be created in the structure blueprint 
```swift 

struct Town {
    let name: String
    var citizen: [String]
    var resources:[String : Int] //blank properties
    
    init(name: String , citizen: [String] , resources: [String:Int]) {
        self.name = name //referring to the property "name" in the structure in line 3
        self.citizen = citizen
        self.resources = resources
    }
    func fortify() {
        print("defences Up")
    }
}

var anotherTown = Town(name: "anotherTown", citizen: ["Town hanks"], resources: ["coconuts" : 100])
print(anotherTown.citizen)
anotherTown.citizen.append("willson")
anotherTown.fortify()

```
## immutability 
- if there is a var in side the stuct , we cannot change its value in side the structure itself , cause it will be assigned to self keyword and self is a immutable character like let 
- but we can do that outside the structure and also inside the structure using 
```swift 
struct another_structure {
    var not_mutable = 100
    mutating func imma_mutate_te() {
    not_mutable = 1000}
}

var another = another_structure()

another.imma_mutate_te()
print(another.not_mutable) // prints 1000
```
>  **But the above mutating function wont work when you create an object using the let keyword**


# design patterns 
--- 
- managing the complexity
- need to come up with a org chart for our software to reduce the complexity 
	- there are so many design patterns
	- select based on the requirement 
	- there are also based on the style 
		- readable or smaller code
## Model View Controller (MVC)
> Model -> have data and the logic for the data 
> View -> have the User Interface
> Controller -> mediator  

