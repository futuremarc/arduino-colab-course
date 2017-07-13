# SYLLABUS

## OVERVIEW

This course is an introduction to progamming with the [arduino](http://arduino.cc) microcontroller. It will cover the basics of electricy and programming through exploring different components: AC motor, stepper motor, force sensing resistor, flex sensor, LED, RGB LED, light sensor, distance sensor, potentiometer, accelerometer). We will be using the textbook Arduino Projects Book by the Arduino team. This course works directly in conjunction with CB Goodman's set design course in which together the outcome will be to create a 1/4 inch model that replicates a large scale gallery installation exploring climate change.  

## SCHEDULE

### CLASS 1: Introduction

* Software, creative coding, and physical computing
	* What is software?
		* Very specific instructions for a computer
		* Made up of commands and very specific keywords
		* Modern world is built on it
		* Thinking like a computer
			* [A series of precise instructions](https://www.youtube.com/watch?v=xngWoocXYCo)
				* Robot waiter delivering food to guests
			* [Recipe](https://www.youtube.com/watch?v=UScm9avQM1Y)
				* List of ingredients and instructions
	* [What is creative coding?](http://reddit.com/r/creativecoding)
		* Programming as a creative discipline. 
		* Examples
			* [Arduino Examples](https://www.hackster.io/arduino/projects)
			* [Haptec Bike](https://www.youtube.com/watch?v=MspImczjQ5Q)
			* [Smoogling NIME 2008](https://www.youtube.com/watch?v=3D4jYaQgpoo)
			* [Fish On Wheels](https://www.youtube.com/watch?v=YbNmL6hSNKw)
			* [Joe Mango NIME 2016](http://josephmango.com/nime/)
			* [Shek.it](http://shek.it/)
			* [Processing Exhibition](https://processing.org/exhibition/)
			* [Shiffman's List](https://github.com/ITPNYU/ICM-2014/wiki/Projects)
		* Creative coding with the web
			* [Jazz Computer](http://jazz.computer)
			* [Cabbibo](http://cabbi.bo/)
			* [Void](http://void.hi-res.net/)
			* [Three.JS](http://threejs.org)
			* [Super Sync Sports](https://chrome.com/supersyncsports/)
		* [Art Grants!](http://unframed.lacma.org/2015/12/16/call-art-technology-proposals)
	* [What is Arduino?](http://arduino.cc)

	
* Microcontrollers
	* timers, thermostats, toys, remote controls, microwave ovens.
	* Do one specific task and have been programmed to sense and control activity using sensors and actuators.
	* Sensors
		* Listen to the physical world. They convert energy that you give when you press buttons, or wave your arms, or shout, into electrical signals. Buttons and knobs are sensors that you touch with your fingers, but there are many other kinds of sensors.
	* Actuators
		* Take action in the physical world. They convert electrical energy back into physical energy, like light and heat and movement.
	* Microcontrollers listen to sensors and talk to actuators. They decide what to do based on a program that you write.
	* Microcontrollers and the electronics you attach to them are just the skeleton of your projects, though. You’ll need to bring skills you probably already have to put some  flesh on the bones.
		
* **IN-CLASS**: Create a list of instructions for each other to do in class. Try to be very specific.

### CLASS 2: Set-up and Commands part 1 (Functions)

* Code is like using magic in Harry Potter. You have to get the spelling of the words exactly correct. Though you can make your own magic words too!
* [Arduino Reference](https://www.arduino.cc/en/Reference/HomePage)
* Be comfortable not knowing everything all at once.
* setup() runs once in the beggining.
* loop() when setup is finished it runs over and over again.
* pinMode()
* digitalWrite()
* HIGH
* LOW
* delay()
* // (single line comment)

### CLASS 3: Electricity

* recreate blinking onboard LED
* variables
	* like buckets, hold data
	* types of variable (int, float)
	* declare variable (int myPin)
	* assign variable (myPin = 5)
	* use variable (pinMode(myPin, OUTPUT))	
* what is a circuit
	* An electric circuit is like a pathway made of wires that electrons can flow through. 
	* The word “circuit” sounds like “circle,” and a circuit needs to be circular to work. The wires have to go from the power source to the device and back again, so that the electrons can go out and come back. Flowing from power to ground.
* Voltage
* Current
* Resistance
* illustration https://qph.ec.quoracdn.net/main-qimg-ecfa5c897dd6276b0fadb76a3d5fc0d8.webp
* illustration 2 http://i.imgur.com/qwBkvg4.png
* electricity
* bread board diagram https://www.courses.tegabrain.com/SS15/wp-content/uploads/2015/02/breadboard.jpg

* LED  (walk through workshop)
* == (equal to)
* != (not equal to)
* < (less than)
* \> (greater than)
* <= (less than or equal to)
* \>= (greater than or equal to)
* if... else


### CLASS 4: Commands part 2 (Functions), conditionals, and other syntax

* recreate blinking onboard LED
* recreate LED circuit with meaningful variables
* change LED 5V power to digital pin 11
* program LED on breadboard to blink
* photocell/light sensor circuit
* analogRead();
* Serial.begin();
* Serial.println();
* if...else
* if...else if... else

* Conditionals
	* Boolean expressions
		* I am hungry (true)
		* I am afraid of computer programming (false)
		* I am funny (false)
		* 15 is greater than 20 (false)
		* 5 equals 5 (true)
		* 32 is less than or equal to 33 (true)
	* Using a variable to take different paths in our program depending on the current value stored in the variable
		* x > 20 (depends on value of x)
		* y == 5 (depends on value of y)
		* z <= 33 (depends on value of z)
	* Operators
		* `< > >= <= == !=`
	* `If, else if, else`
		* Operate as questions
			* Allows us to execute certain instructions based on if the answer is `true` or `false`
			* If I am hungry then eat some food, otherwise if I am thirsty drink some water, otherwise take a nap
			* Grading system excercise
				* `var grade = random(0,100);
					if (___) {
						console.log('Assign letter grade A');
					} else if (___) {
						console.log('___');
					} else if (___) {
						console.log('___');
					} else if (___) {
						console.log('___');
					} else {
						console.log('___');
					}`
	* Logical Operators
		* `&& ||`
		* If my temperature is greater than 98.6 OR I have a rash on my arm, take me to see a doctor
		* If I am stung by a bee AND I am allergic to bees, take me to see the doctor
		* If the mouse is on the right side of the screen AND the mouse is on the bottom of the screen, draw a rectangle in the bottom right corner.
		* We could use a nested if statement, but it can be simpler with using the logical AND (`&&`)
		* If my temperature is NOT greater than 98.6, I won't call in sick to CoLab
		* If I am stung by a bee AND I am NOT allergic to bees, don't worry!
		* `if (lightSensorValue > threshold){
			digitalWrite(LEDPin, HIGH);
		} else {
			digitalWrite(LEDPin, LOW);
		}`
	* `Boolean` variables

* == (equal to)
* != (not equal to)
* < (less than)
* \> (greater than)
* <= (less than or equal to)
* \>= (greater than or equal to)
* &&
* ||
* make LED turn on and off according to threshold
* closer look at arduino
	* analogWrite (for numbers ranging 0-255), digitalWrite(for numbers 0,1; turning things on and off)
	* map()
* remap values of light sensor to control dimming the LED


* for
* ; (semicolon)
* Code Blocks { }
* // (single line comment)
* && (and)
* || (or)
* ! (not)

* **IN-CLASS**: 

everyone learns: analogWrite()... if, else if...
* projects:
	* robot: analogRead() map() servoConnect() //learn about servo library
	* glacier: analogRead() map() analogWrite() //
	* tree: value = value + 1, if (a < 242) ..., else if () ...., else if ().... else...


### CLASS 5: Final Projects

* Your projects!
* Debug
* Presentations
* Next Steps
	* [Complete Learning Processing with Daniel Shiffman!](http://icm.shiffman.net)
	* See [object oriented programming example](https://github.com/futuremarc/p5-creative-coding-course/blob/master/inclass/objectoriented_inclass10.js)

### KEYWORDS

* Variable `int x = 0;`
* Interger
* Float
* Function `function moveBall(){}`
* Array `[25,26,27,28]`
* Boolean `true`
* String `'words in a sentence.'`
* Loops `for (var i = 0; i < 5; i++){}`
* Conditional `if (x > 4){ doThis() }`



### OTHER LINKS

* Learn Code

	* [W3Schools](http://www.w3schools.com/)
	* [Codecademy](http://www.codecademy.com/learn)
* Learn Arduino

