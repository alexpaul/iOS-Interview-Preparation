# iOS Interview Preparation

> Objective is to keep this as to date as possible. Advance apologies if some answers are missing. Email Github :-]

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


</details> 

#### What is recursion? 

<details> 
  <summary>Solution</summary> 

A function that called itself.

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

#### Name the following looping constructs in Swift ?

<details> 
  <summary>Solution</summary>   

while, for-loop and repeat-while
 
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

A paradigm used in programming to represent objects and encapsule the properties and functions. 

</details> 


#### What is Protocol Oriented Programming ?

<details> 
  <summary>Solution</summary> 

In Swift this is a paradigm used to describe the blueprint of functions and properties that the conforming object needs to adhere to.

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


### Explain RESTFul ?

<details> 
  <summary>Solution</summary> 


</details> 

### What is a MIME type ?

<details> 
  <summary>Solution</summary> 


</details> 

### What's the difference between Websockets and HTTP ?

<details> 
  <summary>Solution</summary> 


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
