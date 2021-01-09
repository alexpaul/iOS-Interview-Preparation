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

#### What are the two required methods of a `UITableViewDataSource`? 

<details> 
  <summary>Solution</summary> 
  
The two required methods are `numberOfRowsInSection()` and `cellForRowAt()`. 
  
</details> 

#### What's the difference Push notifications and Local Notifications ? 

<details> 
  <summary>Solution</summary> 

Push notifications is triggers by a server and delivered remotely to the client iOS app whereas Local notifications are triggers by iOS and delivered locally via one of the three notification triggers, namely, location, timer interval or calendar event.
  
</details> 

#### Name the ways to persist data in iOS ? 

<details> 
  <summary>Solution</summary> 

UserDefaults, Documents directory and Core Data.

</details> 

#### What is `Result` type? 

<details> 
  <summary>Solution</summary> 

Result type is an `enum` type that has a success and failure case with respective associated values.

```swift 
enum AppError: Error {
  case fetchError
}

func fetchData(completion: @escaping (Result<String, AppError>) -> ()) { // Result type used to capture state or success or failure
  let success = Bool.random() 
  if success {
    completion(.success("Success"))
  } else {
    completion(.failure(.fetchError))
  }
}

fetchData { result in 
  switch result {
    case .success (let str): 
      print(str) // "Success"
    case .failure (let error): 
      print("error found: \(error)") // error found: fetchError
  }
}
```

</details> 

####  Describe the ways in which a view can be created ?

<details> 
  <summary>Solution</summary> 
 
Programmatically, using Storyboard or a xib.
 
</details> 

#### What is ARC ? 

<details> 
  <summary>Solution</summary> 

Prior to Automatic reference counting in Objective-C developers needed to keep track of retain and release cycles of objects that were created. With the introduction of ARC now the system does most of the automatic retain/release counting and mememory management for us with limitations such as capturing closures where we need to use weak/unowned as needed.

</details> 

#### What is MVC?  

<details> 
  <summary>Solution</summary> 

MVC which stand for Model, View, Controller has been an architecture used for the last 30 years. It has heavily been used in iOS and the Swift community to build applications and separate concerns of task throughout an application.

Model. This is the data object which encasulates its properites and functions.   
View. This is the user interface of the application. This is the way in which the user interacts with our app.    
Controller. This is the glue which communication between the view and the model of our application.    

Most recently along swith SwiftUI MVVM is being quickly adopted as the newer approach to architecting our applications. 

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

#### Which built-in tool do we use to test performance of our application ? 

<details> 
  <summary>Solution</summary> 

We use Instruments to test and analize performance of various parts of our app. Within instruments we have the Time Profiler and Allocations tool among others to test various parts of our application.

</details> 

#### What is Core Data ? 

<details> 
  <summary>Solution</summary> 

Core Data is an object-relatioal graph model of representing and persisting data in an appliation.

</details> 

#### What is TestFlight and describe its process ? 

<details> 
  <summary>Solution</summary> 

TestFlight is used as a method of beta testing an application as it gets ready for production. 

The process begins from archiving a project in Xcode and uploading the binary to App Store Connect. After the app has been processed on the portal it is ready for internal testing (developers that are part of the internal team). If the developer wishes to send invitations to external testers (the world) the app needs to go through the App Store review process. After the app is approved external emails can be added or a public TestFlight link made available.

</details> 

#### What are the types of Local Notifications ? 

<details> 
  <summary>Solution</summary> 

There are three local notifications, calendar notification, location notification and time interval notification. 

</details> 

#### What is the default http method when making a request? ? 

<details> 
  <summary>Solution</summary> 

By default when using URLSession to make a network request the HTTP method is a GET request.

</details> 

