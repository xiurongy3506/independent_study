# Entry 3: Tutotial :white_check_mark:

This weeek, I was able to meet my previous goal of completing the Swift Beginner's Tutorial. 

## Class  
Class reminds me of the object orientation I learned in Ruby and P5js. Similar to Rbby and p5js, a class is like a factory that teaches the code how to create instances. The instance that is created in the class are also known as objects.   

When creating a class, always capitalize the name. 
```swift  
class Name {
    //code
}
```

_A full example will be shown later along with other examples._  

### Initialize  
Init inside a class allows certain variables to be initialized.  
- will run once the class is called
```swift
    init() {
        //code
    }
```   
Apparently, there's also a **convenience init** that also calls the designated initializer, but I don't understand why we need it. I'll come back to it if I need it.  

_I won't give an example on init because it's very similar to Ruby_  

### Inheritance
Allows you to inherit the property of one class from another
Why use inheritance?  
- Reduce redundancy between class  
- Taking what is already in the class and improving it 

**Overriding:** take the property from the parent class and redefine it to 
override the parent version

**Example**
```swift 
class Car {
    var topSpeed = 200

    func drive(){
//        recognizes 200 as topSpeed
        print("Driving at \(topSpeed)")
    }
}
class Futurecar : Car {
    override func drive(){
//        super refers to the super calss, parent
        super.drive()
        print("and rocket boosting at 50")
    }
    func fly() {
        print("Flying")
    }
}

let myRide = Car()
myRide.topSpeed
myRide.drive()

let myNewRide = Futurecar()
//Future car will also have a topSpeed of Car
myNewRide.topSpeed
myNewRide.drive()
myNewRide.fly()
```
The above code prints the following  
```
Driving at 200
Driving at 200
and rocket boosting at 50
Flying
```
Since Futurecar inherit from car, it is going to inherit the property of Car as well

In the tutorial, there is a brief reference to **UIKIT** in which contains prebuilt classes that handle common things like app buttons, user interaction, and etc.  

I will have to dig deeper and do some research on UIKIT.   

### Property  
Base on the tutorial, properties refer to values that are stored within the class. This can be noticed by ```var```, when a new variable is created and stores some sort of data.   

After searching up [property in swift](https://docs.swift.org/swift-book/LanguageGuide/Properties.html), I notied that there are different types of properties other than the type of property I was learning, stored property.

I won't dive too deep into property now, but I left a link for reference incase I need it in the future.   

_there's stored properties, computed properties, type property..._  

## Optionals  
Optionals may contain an object or not.  
For instance, in ```var title:String?```,   
```?``` tells the computer that it can be a string or nil  

_**nil** means empty_ 

**Full Example** 
```swift  
class Person {
    var name = ""
}
class BlogPost {
    var title:String?
    var body = "hey"
    var author:Person?
    var numberOfComments = 0
}  

let post = BlogPost()
print(post.body + " Hello!")

//optional binding
post.title = "hello"
if let actualTitle = post.title {
    print(actualTitle + " world")
}

//force unwrapping
print(post.title! + " world")

//Testing for nil
if post.title != nil {
    print("post.title is not nil")
}

//check if it is nil
if post.title == nil {
    //contains no value
    print("it is nil")
}
```    
### Optional Binding
```swift 
if let actualTItle = post.title {
    //Test if there is a value in post.title
}
```  
- If the is a title, it will execute the code inside the if statement  
- If there is no title, the code will not run  

### Force Unwrapping  
Use Force Unwrapping, ```!```, only if you know there is a value because it does not understand nil. If nil appears, the code will crash. 

## Dictionary  
Dictionary are type of collection data stored in key-value pairs. This is similar to a hash in Ruby.   

There are three types of [collection data](https://docs.swift.org/swift-book/LanguageGuide/CollectionTypes.html) (Array, Sets, and Dictionary), but the video teaches Dictionary specifically. 

The codes below are connected in order. 
- Declaring a new Dictionary  
```swift
var person_age = [String:String]()
```
_Note: To create a dictionary, get rid of "()" in the above vode and replace "String" with a string_  

- Adding key value pairs
```swift
person_age["Ann"] = "15"
person_age["Ben"] = "16"
```  
- Retrieving data
```swift
//prints 15
person_age["Ann"]
```  
- Update a value for a key
```swift
person_age["Ann"] = "18"
```  
- Remove a key-value pair
```swift
//set the key to nil
person_age["Ann"] = nil
```  
- iterate
```swift
for (name, age) in person_age {
    print("\(name) is \(age) years old")
}

//Prints the following
//Ben is 16 years old
//Ann is 18 years old
```     

## Takeaways  
1. **You do not have to do everything at once. Break it down.** Unfortunatly, this week, I wasn't able to utilize cocoapods and play around with it due to limited time. As a result, I prioritized finishing up the tutorial for swift first. Next week, I want to start applying the codes I learned from the tutorial to my test app and apply cocoapods. 
2. **Keep track of the important things you find (links, ideas...)**. For me, there's still stuff that I don't understand (ex: convienience init) or things I can still explore more about (ex: UIKIT, collection types...). While I'm not sure if I need it now or have time to explore more knowing that I still have an app to built, I placed either write it down in this blog or had links to where to find the informations for future reference. 

