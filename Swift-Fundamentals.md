## Swift Fundamentals 


####  What's the difference between mutable and immutable ?

<details> 
  <summary>Solution</summary> 
 
A mutable object allows for change. An immutable object does not allow for changes.

Mutable object L
```swift 
var currentYear = 2020
currentYear = 2021 // could not come fast enough
```

Immutable object
```swift 
let usIndependenceDay = "July 4th"
usIndependenceDay = "February 22nd" // sorry could not compile, this is 🇱🇨 Independence day
```
 
</details> 

#### What is a property observer?

<details> 
  <summary>Solution</summary> 

A property observer listens for changes on a object. One can listen for changes when the object is about to get set and when the object actuallly got set.

```swift 
var age = 20 {
  willSet {
    print("it's about to get fun")
  }
  didSet {
    print("with great power comes great responsibility")
  }
}

age = 21

/*
 it's about to get fun
 with great power comes great responsibility
*/
```

</details> 

#### What are higher order functions? 

<details> 
  <summary>Solution</summary> 

A function that takes another function as an argument or returns a function is said to be a higher order function. This is the fundamental pillar of functional programming. 

</details> 

#### What is recursion? 

<details> 
  <summary>Solution</summary> 

A function that calls itself. The two main parts of a recursive function is the **base case** and the **recursive call**. 

```swift
func jobSearch(_ isHired: Bool) {
  // base case
  guard !isHired else {
    print("Woohoo")
    print("Everyone's journey is different")
    return
  }
  // recursive call
  print("Job searching...")
  jobSearch(Bool.random())
}

jobSearch(false)

/*
 Job searching...
 Job searching...
 Job searching...
 Woohoo
 Everyone's journey is different
*/ 
```

</details> 

#### What are access control / modifiers and give three examples? 

<details> 
  <summary>Solution</summary> 

Access control provide varied level of access to parts of the code of an object from another source object.   

Three examples are: 
* private 
* public 
* internal 

</details> 

#### Name three built-in protocols in Swift and their use cases? 

<details> 
  <summary>Solution</summary> 

`Hashable`. Types conforming to `Hashable` will be guaranteed to be unique.  
`CaseIterable`. Enums conforming to `CaseIterable` will make all their cases available and iterable.  
`CustomStringConvertible`. Conforming to `CustomStringConvertible` allows a type to override the description property on an object and return a custom String.  

</details> 


#### What's the benefit of an inout function? 

<details> 
  <summary>Solution</summary> 

To be able to mutate via referencing the data outside the scope of a function.

</details> 

####  Write code to access the last element of an array ?

<details> 
  <summary>Solution</summary> 
  
Example 1: 
```swift 
let arr = [1, 2, 3, 4]
print(arr[arr.count - 1]) // assuming the array is not empty, will crash otherwise 
```

Example 2: 
```swift 
let arr = [1, 2, 3, 4]
print(arr.last ?? -1) // using nil-coelescing here as last is an optional
```
 
</details> 

#### What is an optional ?

<details> 
  <summary>Solution</summary> 
  
In Swift an optional is a type used to indicate that an object can or not have a value. 
 
</details> 

#### What are Closures ?

<details> 
  <summary>Solution</summary> 
  
Closures are anonymous functions (functions without a name) that capture references to values in their surrounding context. This is one of the subtle differences between functions and closures. Please note however that nested functions also capture their surrounding values. 

```swift 
// someFunc definition with a closure parameter
func someFunc(action: (Int, Bool) -> ()) {
  let internalValue = 20
  action(8 + internalValue, Bool.random()) // the action closure captures the Int and Bool values
}


// someFunc call using trailing closure syntax
someFunc { intValue, boolValue in
  print("closure captured values are \(intValue) and \(boolValue)") // closure captured values are 28 and false
}
```
 
</details> 

#### What is GCD? 

<details> 
  <summary>Solution</summary> 

Grand central dispacth is the library that iOS uses to handle concurrency. 

</details> 

#### Name the types of loops available in Swift ?

<details> 
  <summary>Solution</summary>   

while, for-in and repeat-while
 
</details> 


#### If using a Command-line macOS application what's the function used for taking user input ?

<details> 
  <summary>Solution</summary>   

For user input or STDIN when working in a command-line application we use `readLine()`. 
 
</details> 

#### What is the runtime of `contains` on an array ?

<details> 
  <summary>Solution</summary> 
  
O(n)
 
</details> 

#### What's the runtime of `contains` on a set ?

<details> 
  <summary>Solution</summary> 

O(1)
 
</details> 

#### What is the restriction on a dictionary ?

<details> 
  <summary>Solution</summary> 

The keys need to conform to `Hashable`.

</details> 


#### What is Object Oriented Programming ?

<details> 
  <summary>Solution</summary> 

A paradigm used in programming to represent objects and encapsulate their properties and functions.

```swift 
// Parent class
class Person {
  var name: String
  var age: Int
  
  init(name: String, age: Int) {
    self.name = name
    self.age = age
  }
  
  func info() {
    print("Hi, my name is \(name)")
  }
}

// Fellow inherits from the Person class
// Subclass
class Fellow: Person {}

let fellow = Fellow(name: "Xavier Li", age: 23)
fellow.info() // Hi, my name is Xavier Li
```

</details> 


#### What is Protocol Oriented Programming ?

<details> 
  <summary>Solution</summary> 

In Swift this is a paradigm used to describe the blueprint of functions and properties that a conforming object needs to adhere to.

```swift 
import UIKit

protocol Vehicle {
  var wheels: Int { get }
  var color: UIColor { set get }
  func drive(speed: Int)
}

struct Bike: Vehicle {
  let wheels = 2
  var color = UIColor.systemGray
  
  func drive(speed: Int) {
    print("current speed is \(speed)")
  }
}

let bike = Bike()

bike.drive(speed: 23) // current speed is 23
```

</details> 


#### What is dependency injection? 

<details> 
  <summary>Solution</summary> 

Dependency Injection is used to pass all required properties and data over to an object. This is better done through the use on an initializer as the object can fully encapsulate its properties.

</details> 


#### What framework is used for writing Unit Test in iOS ?  

<details> 
  <summary>Solution</summary> 

XCTest

</details> 

#### What is a Singleton? 

<details> 
  <summary>Solution</summary> 

A singleton is making use of one instance of a class throughout the life of the launch of an application. One of the main pillars of singleton is the use of marking initializers private so accidental creation of multiple instances is prohibited.  

Singletons are used throughout iOS in places like `UserDefaults.standard`, `FileManager.default` and `UIApplication.shared`. 

```swift 
class GameSession {
  static let shared = GameSession()
  private init() {
    // initialization of properties here
  }
}

let session = GameSession.shared

let otherSession = GameSession() // 'GameSession' initializer is inaccessible due to 'private' protection level
```

</details> 

#### Is `URLSession` part of `Foundation` or `UIKit`? 

<details> 
  <summary>Solution</summary> 

URLSession is part of the Foundation framework.

</details> 

#### What's the difference between a compile time error and a runtime error? 

<details> 
  <summary>Solution</summary> 

Compile time errors occurs during the writing phase of your code. Runtime erros occurs during the launch and actual use of the application. 

</details> 

#### Is `Index out of range` error on an array an compile-time error or a runtime error? 

<details> 
  <summary>Solution</summary> 

`Index out of range` is a runtime error. 

</details> 


#### What's the difference between Structs and Classes? 

<details> 
  <summary>Solution</summary> 

Structs are passed-by value (value-types) meaning copies of the objects are passed around thereby making the objects immutable by default. Classes are reference types and their state is easily mutated as objects that have the same reference can make changes at will. 

</details> 


#### Is `NSString` a class or a struct? 

<details> 
  <summary>Solution</summary> 

`NSString` is an objective-c API and is a class. With interopobality we can easily bridge between Swift `String` and `NSString`. 

</details> 


#### What's the difference between frames and bounds? 

<details> 
  <summary>Solution</summary> 

The frame represents an object's superview and it's relationship in the coordinate space, whereas the bounds represents the objects own size and location.

</details> 
