# Entry 5: Taking User Input and Pass on Data
In my previous entry, I have built a very basic 10 second timer (or however many seconds I, the programmer, wants to set to in the function). In order to let the user set the time they wanted, I decided to test out how to take in the user's data, and how to pass that data to a different view. As a result, I created two different projects in Xcode to test out these two functionalities. Once these two work, I will apply it to the previous timer app. 

_Note: The reason why I don't try it out in the previous project is that I don't want to mess up the code that is already there._  

## User Input
1. To take in the user input, I created two text fields, one for taking in String and one for taking in numbers.  
2. Once they are created, I connected them as an outlet to the viewController to make sure that they show up on the app.  
3. Then I created a submit button and connected them both with an Outlet and Action. 
4. Once the submit button is clicked, I want the output (on the bottom right) to display the user input. 
5. Once it is displayed, I used "let num" to equal to the number the user type and printed again to make sure I can call on "num"  

<p align="center">
    <img src = "https://github.com/xiurongy3506/swift_independent_study/blob/master/img/user_input.gif?raw=true"/>
</p>  

Challenge: Notice that once the user clicked on the textField, a different type of keyboard is displayed depending on the type of data is wanted?  
At first, I was looking up thinking that I would have to code it, so I looked up and used 
```
text.keyboardType = UIKeyboardType.numberPad
```
It does not work as nothing is displayed. I continued to look online and barely any useful information was found. 

Solution: I looked around the code, no error is displayed. When I looked around at the attribute inspector, I notice that the Keyboard Type was already built, so I just have to select the Keyboard Type without actually coding it. 
<p align="center">
    <img src = "https://raw.githubusercontent.com/xiurongy3506/swift_independent_study/master/img/numberPad.png"/>
</p>  

## Pass on the Data  
Learning how to create multiple views and pass on the data can be very useful when you want to create an interesting app that does not just have one single screen you see. I started with creating just two views, the main one and the other one called viewTwo. 

Steps of creating multiple views:  
1. Create a ViewController using toolkit
2. Connect the button to the second ViewController and click “show”  

<p align="center">
    <img src = "https://raw.githubusercontent.com/xiurongy3506/swift_independent_study/master/img/show.png"/>
</p>  

3. Create a new file (File -> New File -> Swift -> viewTwo)  

<p align="center">
    <img src = "https://raw.githubusercontent.com/xiurongy3506/swift_independent_study/master/img/viewTwo.png"/>
</p>  
  
4. Import UIKit in viewTwo (to work with UI elements)
5. Create a class for viewTwo (UI View Controller)
6. Within the class, type viewDidLoad() and tab
7. Go to the identity inspector tab of the second view and name the class viewTwo 
    1. This will allow changes to be made in the second view

_class should look something like this_
<p align="center">
    <img src = "https://raw.githubusercontent.com/xiurongy3506/swift_independent_study/master/img/setupClass.png"/>
</p>   

8. Connect the text, button, and label to its corresponding View.  
9. Set up a seaway from the viewController to the viewTwo
    1. ERROR  


While I was able to set up all the basic steps of making two views, I was struggling with setting up a segway from one view to the other. Here is the issue:     

<p align="center">
    <img src = "https://github.com/xiurongy3506/swift_independent_study/blob/master/img/pass_on_data.gif?raw=true"/>
</p>     

I tried googling and looking up other tutorial and across one tutorial, “Move between View Controllers with Segues—iOS #9”,  that is very similar to what I was doing instead it has an identifier. 

So I added an identifier ...
<p align="center">
    <img src = "https://raw.githubusercontent.com/xiurongy3506/swift_independent_study/master/img/identifier.png"/>
</p>    

And the same error showed up  
<p align="center">
    <img src = "https://raw.githubusercontent.com/xiurongy3506/swift_independent_study/master/img/fail.png"/>
</p>      

As a result, I will continue to solve this issue and hopefully apply them to the timer app.  
## Takeaways
1. **Things can occur unexpectedly and it may not always be a part of your plan**. When using segue to set a segway from one view to another, I expect it to work because no errors were shown on the code, and the similar code was used in the tutorials I googled. The app was run successfully until the submit button was clicked, and an error occurred on the segue part of the function. Therefore, I had to continue googling and test out some code and it still requires some tinkering. 

2. **Look at things from a holistic perspective** . When I was trying to code the Keyboard function in the user input section, I coded the keyboard function because I was coming at the viewController page, and it did not work. Specifically, with Swift, there is a lot of pre-built functions that I can use, so I have to open up parts that I hide to see the attribute inspector and change the keyboard on the app without actually coding it. 




