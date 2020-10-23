# AP-CompSci-A-Calculator Version 2 Ideas 

by Nakul Nandhakumar, Vihan Jayaraman, and Yasaswi Singamneni



Create an Operations class:
General computing methods for each operation (addition, subtraction, mult, etc), with the inputs being universal. 
Computing methods will be used in the other classes

Create a Main class for managing the CLI and GUI classes:

Basic Process - From Input to Output:
Upon startup would display a main-menu GUI - choose GUI or CLI
Main program loop would start either the GUI or CLI programs - when either program ends, depending on the return value, the Main class either starts the other program or ends the entire Calculator program - 
Will create a new instance of the desired class and call GUI.main() or CLI.main() to start the desired program
The GUI or CLI program takes in the input (text-based or button-clicks)
GUI and CLI classes will manipulate the input before using the Operation class methods for computing
After receiving the return value from the Main methods, the GUI and CLI classes display the output and are ready to take in their input. 

Create a class for taking input from console line - CLI
Requires a program loop in main
Requires a way to open up a console window
Will probably use some kind of Buffered Reader or Scanner class to read input from the console window
Can use simple text-based GUI to display allowed operations - select operation by using CLI commands
After selecting the operation, the user will type in the numbers
option to switch to gui by inputting in a certain command (probably gui)
option to end the calculator program entirely (exit, or click on x button in window)

Create a class for taking input from GUI
Automatically generated GUI (buttons, fields)
Use event listeners on buttons
When buttons are clicked the inputs are stored until the equal sign is clicked, at which point the program computes
If the buttons are clicked in an incorrect combination (too many operators, or too many decimal points) then the method that is triggered when the equal sign is clicked will try to catch the exceptions (with try and catch statements)
OR 
prevent incorrect combinations from being entered in the first place by disabling certain buttons
Option to switch to CLI by clicking a specific button (labeled CLI)

-- Separate control, view, and model code into separate classes (CalculatorGUI, CalculatorTextUI, CalculatorControl, CalculatorModel)

-- Extend the view code class in the control code, create object of view class, instantiate view using object

-- Possibly will be using multiple interfaces for modeling and to work around not being able to do multiple class inheritance in Java

*class CalculatorControl {*

*CalculatorGUI viewGUI = new CalculatorGUI();*

*CalculatorTextUI textUI = new CalculatorTextUI();*

  *public void CalculatorControl("insert preferred UI here") {*

  *... control code*

   *}*
  
*}* 
