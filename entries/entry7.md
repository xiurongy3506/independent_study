# Entry 7: Setting Up Firebase on Swift

Last week, I mentioned that I will be setting up OhMySQL Cocoa pod, and I did do that with Jennifer. However, we still find trouble connecting MySQL and Swift using this pod because we do not know where to place the code provided on X-code since very little details were given. As a result, we emailed the person we created the project and asked them for a demo project to test out the connection. While we did receive a response, I was not able to clone the demo project on Xcode and Jennifer is also facing an error in one of the steps using MAMP. Because both of us were facing errors in following the tutorial for this pod, I reached out to my Co-worker John. While the MySQL and Swift connection is possible, I was informed that it will take more than a week or two (the time of this independent study) to do that. Therefore, the quickest way for Jennifer to create a database for our app is using Firebase.  

## The process
Jennifer watched some tutorials on how to set up Firebase and she created a Firebase account while I set up the pods to install the Cocoa pods for Firebase. Failed to set up the connection on Firebase for multiple times, we were in despair.  

Some failures we faced:  
1. Using my own Apple ID to create an Apple Developer Account  
    - I exceeded the amount of workspace I have created 
    - My Apple ID cannot be identified  
Solution: Used a different apple ID  
2. Connection Failure    
    - Firebase is unable to recognize the workspace identifier on Swift
Note: Jennifer and I checked our spelling multiple times, and made sure it is correct. However, the same error occurred. 

We tried again the next day, and it somehow worked. It turns out that the connection is already set up once we open the Firebase. I guess the connection takes some time.     

All the Pods I've download  
<p align="center">
    <img src = "https://raw.githubusercontent.com/xiurongy3506/swift_independent_study/master/img/firebpods.png"/>
</p>   

<p align="center">
    <img src = "https://raw.githubusercontent.com/xiurongy3506/swift_independent_study/master/img/download.png"/>
</p>   

## Firebase on Swift  
Previously, I have already set up a username and password on my app. However, I still need to find a way to authorize it with Firebase, and this requires a lot of time to work with Jennifer since she is in charge of the Firebase account. After looking some tutorials, there are codes that I have to set up in Swift to connect with Firebase, however, I would have to test it out on with Jennifer and see if the authentification was successful.  

## Errors after Errors  
Timer App:  I mentioned that I wanted to make the user set the amount of time they wanted, so that I, as the programmer, do not have to set it up in the backend. Using the same concept of passing on data, I was able to apply the same concept. For instance, if the user typed in a number, this number will be passed on as a string to the next view. While the view that displays the time does show the time, there were errors in the code that cannot recognize the string because it expects an integer.  Unlike other languages, I was expecting this to be a simple error since, in Ruby, you can convert string to an integer using .to_i

I was wrong. Converting string to integer can be simple in swift if I simply code few lines of code without complexity. However, my code includes passing on data, which means the code wants to know what type of data is being passed, and once the data is passed what form will it be in.  

In the picture below, I was having troubles declaring the variable seconds and having it equal to the label that is being passed on from the user's text field. I tinkered around with string and integer, received an error "Cannot use instance member within property initializer," used the ```lazy``` recommended by StackOverflow to solve this issue, used force unwrapping for some of the error that showed up afterward.  

The functions still cannot read the user's input as an integer.  

SetTimerView
<p align="center">
    <img src = "https://raw.githubusercontent.com/xiurongy3506/swift_independent_study/master/img/SetTimer.png"/>
</p>   

TimerView
<p align="center">
    <img src = "https://raw.githubusercontent.com/xiurongy3506/swift_independent_study/master/img/timerView.png"/>
</p>   

## Progress since Entry 1
- [x] Have an idea of what to create + Have an outline
- [x] Get to know Xcode (how to navigate, built app, and use playgrounds)
- [x] Set up apple stimulator with Xcode and apply functions to the app (i.e button click)
- [x] Tinker with Alamofire Networking _It would be useful to making a message app, but probably won't have enough time to do it_
- [x] Finish Swift Tutorial
- ~~[ ] connect Swift with MySQL~~ _PLAN CHANGED_
- [x] Coonect Swift with Firebase  
- [ ] Authorize Firebase on swift 
- [x] Research useful cocoa pods for my productivity app _used multiple Firebase pods_ 
- [x] Apply things I learn from the tutorial to my app 
- [ ] Built a to-do list (tutorial already exist) _still in the process of debugging one error_
- [x] Learn how to build a basic timer 
- [ ] Plan & Built a basic Pomodoro **Timer** _Still in the process of debugging_

## Takeaways  
1. **Plan out your time well.** Despite I knew my goal in the beginning, I underestimated the amount of time it will take me to do this project, and still, I am not done. Moreover, it is also important to consider the amount of time you are able to spend on this project adding on with all the other responsibilities and works you have. By adding on the works I have, I realize that I will not be able to do everything. 

2. **Understand that things can be difficult, and you might not know everything.** Despite I completed the Swift tutorials, I do not understand every single error that popped up. Often times, I would google the error, use stack overflow, but sometimes I just can't solve the problem right away. 


