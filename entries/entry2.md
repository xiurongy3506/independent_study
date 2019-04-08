# Entry 1: Dive into the Learning

## Variable
| Syntax      | Examples  |
| ----------- | ----------- | 
|`var variable name: type = expression` | `var c:Float = 2.3`<br> `var d:Double = 13.9` <br>`var e:Bool = true`|

## If Else if Else statement
<pre>
If condition1 {
	Somecode
}
else if condition 2 {
	Code
}
else {
	Code
}
</pre>

**Notes:**  _Equal Sign_ `==` _And_ `&&` _Or_ `||`  _Not_ `!=`

## Switch Statement
**Syntax**
<pre>
<span style="color: Purple">switch</span> value to consider{  
    <span style="color: Purple">case</span> value1: 
		some code
	<span style="color: Purple">case</span> value2:
		some code
	<span style="color: Purple">default</span>: 
		somecode
}
</pre>

**Example**
<pre>
var someCharacter:Character = "a"
switch someCharacter {
    case "a":
        print("is an A")
    case "b", "c":
        print("is a B or C")
    default:
        print("some fallback")
}
</pre>
This will print “is an A”

## loops
### For Loop
**Syntax** 
<pre>
for counter in loop Lower…upper{
	some code
}
</pre>

**Example**
<pre>
var sum = 0
for index in 1...5 {<br>
<i>//print hello 5 times
//    print("hello")<br>
//print from 1 to 5
//    print(index)</i><br>
    sum += index
}
print(sum)
</pre>

### While Loop 
**Syntax**
<pre>
while condition {
    some code
}
</pre>

**Example**  
<pre>
var num = 6
while num < 4 {
    print("This runs when the above stement is true")
}
</pre>

In this case, the condition is not true, so the while loop will not run. If the statement is true, it will run and run and create an infinite loop since nothing is there to break the loop. You can add **break** below print to make the code only run once.  

### Repeat While Loop 
**Syntax**
<pre>
repeat {
    some code
}while condition
</pre>

**Example**
<pre>
var num = 6
repeat {
    print("This will always run once")
}while num < 5
</pre>

Above will print <code>This will always run once</code>

#### :star: Order of the code Matters
The order of the code can be seen through **the difference between Repeat While Loop and While Loop**. 

Repeat prints once and then checks for the while condition. However, while loop will not repeat at all if the condition is not met.

## Functions
**Syntax**  
<pre>
func name() {
    some code
}
</pre>

:star: **Return Values**
<pre>
func name() -> DataType {
    some code
    return someValue
}
</pre>

:star: **parameter**
<pre>
func name (argumentLabel parameterName:DataType) {
    some code
}
</pre>

:star: **Multiple Parameters**
<pre>
func name (arg1 param1:DataType, arg2 param2:DataType) {
    some code
}
</pre>

**Example**
<pre>
func addTwoNumbers(arg1 para1:Int, arg2 para2:Int) -> Int{
    return para + para2
}
let sum = addTwoNumbers(arg: 2, arg2: 3)
print(sum)
</pre>

Above will print <code>5</code> because the function is adding the two parameters the user assign in <code>arg</code>.   

This code can look a bit overwelming because you have assigned four different names that you will have to use, two parameter(use within the function) and two argument(use outside of the function). Imagine if you were to add more parameters...

#### Ways you can make the above code simpler  
:star: **Make arg and para name the same**
<pre>
func addTwoNumbers(para1:Int, para2:Int) -> Int{
    return para + para2
}<br>
let sum = addTwoNumbers(para1: 2, para2: 3)
print(sum)
</pre> 

:star: **Easier to read**  
<pre>
func addTwoNumbers(using para:Int, and para2:Int) -> Int{
    return para + para2
}<br>
let sum = addTwoNumbers(using: 2, and: 3)
print(sum)
</pre>

:star: **Don't want to use labels at all?**  
<pre>
func addTwoNumbers(_ para:Int, _ para2:Int) -> Int{
    return para + para2
}<br>
let sum = addTwoNumbers(2,3)
print(sum)
</pre>

## CocoaPods
**Where did this new concept, CocoaPods, came from?**  
I told my co-worker, John, at my intern that I will be studying Swift for my independent_study. John, as an IOS Developer, asked me about what I am learning, and I told him about my experience of swift so far (learning the basics syntax and etc). I told John about my goal, to build a productivity app, and John kindly recommended me to look into CocoaPods as it contains many already developed code that can be useful to impliment in my app. 

**So I did some googling...**  
CocoaPod is a dependency manager for Swift and Objective-C. 

In other words, CocoaPods allows you to import external libraries into your projects. A **pod** is referencing to a software library. Once it is installed on your computer, you can use it in your projects.

John showed me how to install, and here is the process
1. Open up the terminal  
2. cd into the cocoapods folder  
3. <code>pod init</code>  
4. <code>sudo gem install cocoapods</code>


Once installed, John used Alamofire, has to do with networking and API, as an example to help me set up.   
1. Add Alamofire to podfile (detail can be seen in the installation guide [here](https://cocoapods.org/pods/Alamofire) )
2. On the terminal, <code>pod install</code>  
3. Once installed, the folder Alamofire will be created
Import Alamofire on view controller

Introduced to CocoaPods for the first time, I did some research and had a gist of what CocoaPods is. However, to impliment it in swift, I still need to dive in deeper and watch more tutorials on how to use CocoaPods. Hopefully, I will do that next week and update what I learn on my next entry!

## App Tinkering
Thanks to John, he also gave me quick an overview on how apps work in swift and how to program them. 

#### What I learned
1. To code for a specific item in the storyboard, you would click and drag that item to where you want to place the code in ViewController.swift
2. A little box will pop up (shown below), and you can fill in the corresponding action.
3. Then, in the function, I can apply swift code. 

#### A demo of what I did: Button Clicked




