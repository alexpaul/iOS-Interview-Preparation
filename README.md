# iOS Interview Preparation

> Objective is to keep this as to date as possible. Advance apologies if some answers are missing. Email Github :-]

## Swift Fundamentals 

####  What's the difference between mutable and immutable ?

<details> 
  <summary>Solution</summary> 
 
A mutable allows for change. An immutable does not allow for changes.
 
</details> 

#### What is a property observer? 

<details> 
  <summary>Solution</summary> 


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

#### Is `URLSession` part of `Foundation` or `UIKit`? 

<details> 
  <summary>Solution</summary> 


</details> 

#### What's the difference between a compile time error and a runtime error? 

<details> 
  <summary>Solution</summary> 


</details> 

#### Is `Index out of range` error on an array an compile-time error or a runtime error? 

<details> 
  <summary>Solution</summary> 


</details> 


#### What's the difference between Structs and Classes? 

<details> 
  <summary>Solution</summary> 


</details> 


#### Is `NSString` a class or a struct? 

<details> 
  <summary>Solution</summary> 


</details> 


#### What's the difference between frames and bounds? 

<details> 
  <summary>Solution</summary> 


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

## Networking 

#### What is HTTP? 

<details> 
  <summary>Solution</summary> 


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
