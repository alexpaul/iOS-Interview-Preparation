# iOS Interview Preparation

> Objective is to keep this as to date as possible. Advance apologies if some answers are missing. Don't email the author :-]

## Swift Fundamentals 

####  What's the difference between mutable and immutable ?

<details> 
  <summary>Solution</summary> 
 
A mutable object allows for change. An immutable object does not allow for changes.

Mutable object 
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

#### What is GCD? 

<details> 
  <summary>Solution</summary> 

Grand central dispacth is the library that iOS uses to handle concurrency. 

</details> 

#### Name the types of loops available in Swift ?

<details> 
  <summary>Solution</summary>   

while, for-loop and repeat-while
 
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


</details> 


#### What framework is used for writing Unit Test in iOS ?  

<details> 
  <summary>Solution</summary> 

XCTest

</details> 

#### What is a Singleton? 

<details> 
  <summary>Solution</summary> 


</details> 

#### Is `URLSession` part of `Foundation` or `UIKit`? 

<details> 
  <summary>Solution</summary> 


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


## iOS Fundamentals 

#### What are the two native frameworks used to create user interfaces in iOS? 

<details> 
  <summary>Solution</summary> 

UIKit and SwiftUI. 

</details> 

#### What does the `IB` in `IBOutlet` or `IBAction` stand for? 

<details> 
  <summary>Solution</summary> 

Interface Builder and NS stands for Next Step in the job process. Reminder to be nice. 

</details> 

#### Name the ways to persist data in iOS ? 

<details> 
  <summary>Solution</summary> 

UserDefaults, Documents directory and Core Data.

</details> 

#### What is ARC ? 

<details> 
  <summary>Solution</summary> 

Prior to Automatic reference counting in Objective-C developers needed to keep track of retain and release cycles of objects that were created. With the introduction of ARC now the system does most of the automatic retain/release counting and mememory management for us with limitations such as capturing closures where we need to use weak/unowned as needed.

</details> 

#### What is MVC?  

<details> 
  <summary>Solution</summary> 

No it doesn't stand for massive view controller. 😀

</details> 

#### What is `URLSession` ?

<details> 
  <summary>Solution</summary> 

The class that manages Networking in iOS. 

</details> 

#### Name three types of gesture recognizers ?

<details> 
  <summary>Solution</summary> 

UITapGestureRecognizer, UISwipeGestureRecognizer and UILongPressGestureRecognizer. 

</details> 

## Tools 

#### Name two dependency managers, can you name three ?

<details> 
  <summary>Solution</summary> 

Swift Package Manager, Cocoa Pods and Carthage.

</details> 

#### What's the difference between `git` and `Github`? 


<details> 
  <summary>Solution</summary> 

`git` is an open source versioning system. `Github` is an online versioning platform for project collaboration now owned by Mr. Softie. Other competitors to `Github` are: `BitBucket` and `GitLab`. 

</details> 

#### What is Core Data? 

<details> 
  <summary>Solution</summary> 

Core Data is an object-relatioal graph model of representing and persisting data in an appliation.

</details> 

## Networking 

#### What is HTTP? 

<details> 
  <summary>Solution</summary> 

HTTP is an internet protocol for allowing client/server communication. The client in this case our iOS app makes a request to a Web API / server and gets a response (json) back that we parse (convert) to Swift objects.

</details> 

#### What is `CRUD` ?

<details> 
  <summary>Solution</summary> 


</details> 


#### What are two ways in which web content is formatted for delivery to a client ?

<details> 
  <summary>Solution</summary> 

XML and JSON, the latter being the more popular and easier to understand and parse.

</details> 



### Explain RESTFul APIs ?

<details> 
  <summary>Solution</summary> 

REST is an standard architecture that web developers use present data to a client. 

</details> 

### What is a MIME type ?

<details> 
  <summary>Solution</summary> 

MIME (Multipurpose Internet Mail Extensions) type is a label used to describe the media content of a piece of data.

</details> 

### What's the difference between Websockets and HTTP ?

<details> 
  <summary>Solution</summary> 

Websockets allow for a constant two-way stream of data and HTTP transfers data via a request -> response model. 

e.g Stock market ticker uses websockets for real time data streaming. 

e.g Fetching a new Instagrm photo using http protocol, client request, server response.

</details> 


## Firebase 

#### What are the two types of databases that Firebase supports? 

<details> 
  <summary>Solution</summary> 

Firebase realtime database and Firebase firestore. 

</details> 


#### Describe the importance of the `Google-Info.plist` file? 

<details> 
  <summary>Solution</summary> 


</details> 

#### What are Firebase rules? 

<details> 
  <summary>Solution</summary> 


</details> 
