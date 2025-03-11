+++
title = "Learn GDScript From Zero App"
draft = false
+++

Estas son las notas sobre la aplicación:

{{< linke href="https://gdquest.github.io/learn-gdscript/?ref=godot-docs" >}}
Learn GDScript From Zero From Scratch
{{< /linke >}}

## 1. What Code is Like

* Every video game is a computer program, so learning to program is unavoidable if you want to make games.

* Programming involves writing very specific instructions for a computer to follow, using a specialized programming language. Computers can't interpret vague commands; they need exact details.

* GDScript is presented as a beginner-friendly language because it's focused and doesn't have too many features to learn at once.

* The core concepts learned in one programming language (like GDScript) are transferable to others. The text shows an example of similar code in GDScript, JavaScript, and Python.

* Becoming proficient in programming, and game development, requires hands on experience.

## 2. Your First Error

* Running into errors is a normal and expected part of programming. Every programmer, even experienced ones, encounters them.

* Error messages, although sometimes cryptic, are intentionally created by programmers to guide others in fixing issues.

## 3. We Stand on the Shoulders of Giants

* Programmers heavily rely on code written by others. This pre-existing code is often packaged in "libraries." Game engines like Godot provide many libraries to save development time.

* A function is a set of instructions with a specific name.  Executing these instructions is done by "calling" the function.

* To call a function, you write its *exact* name followed by parentheses: `function_name()`. 

* The run() function is nesscary to execute instructions in GD script. It contains the instructions, and the tab character is needed for the computer to recognize the function.

* Arguments are values passed to a function inside the parentheses to modify its behavior.

* Explains radians

* show(), hide(), move_local_x(), move_local_y()

* Explains that a positive Y value moves the character *down* in computer graphics, unlike typical math conventions.

## 4. Drawing a Rectangle

* A "turtle" metaphor.
* Turtle Functions:
    * `move_forward(pixels)`
    * `turn_right(degrees)`, `turn_left(degrees)`
* The lesson clarifys that the code will not work in the Godot editor, because it's a custom tool, but the fundementals apply.

## 5. Coding Your First Function

This text explains what functions are, how to define them, and naming conventions, culminating in creating a function to draw squares.

* Functions are defined as sequences of instructions given a name (an "identifier"). Calling the function by its identifier executes those instructions.
* Explains the syntax for defining a function:

Naming conventions: no spaces, use underscores

func nombre_funcion():

jump(300, 300)


## 6. Your First Function Parameter

This text explains function parameters, how to define functions with one or more parameters, and naming conventions, and provides practice exercises. Here's a summary:

* A parameter is a *label* for a value passed to the function.

func function_name(parameter_name):

## 7. Introduction to Member Variables

This text introduces the concept of variables, specifically "member variables" in Godot, and how to access and modify them. Here's a summary:

* Variables are labels used to track values that change over time,
* Member variables are values *attached* to a game entity (like a character or object).  Examples include `position`, `rotation`, and `scale`.
* Member variables can have sub-components, accessed using the dot (`.`) operator.  `position.x` and `position.y` are used as prime examples, representing the horizontal and vertical coordinates.  Similarly, `scale.x` and `scale.y` control horizontal and vertical size.
* Y grows from top to bottom

## 8. Defining Your Own Variables

{{< pre >}}
var health = 100
health = 200
{{< /pre >}}

{{< pre >}}
func run():
    var health = 100
    print(health)
{{< /pre >}}

## 9. Adding and Substracting

health -= amount
health = health - amount

## 10. The Game Loop

Godot also has special functions we can customize or add to.

func _process(delta):
    rotate(0.5)

* it does calculations or continuous actions
* Godot will auto, every frame, many times per second
* frame = when Godot draws on the screen

## 11. Time Delta

almost everything has a _process func

Dozens of times ps, Godot runs every _process func in the game to update the game world. After that, it displays an image of the game world on the screen (a frame).

then moves to next frame

delta

- The time took Godot to complete previous frame in seconds.
- Small bc frames happen many times ps
- Will always be milliseconds variations from frame to frame

Without delta, frame times vary from computer to computer and during
gameplay. Because of that, the movement will differ for every player, making the
game inconsistent and messy.

multiplying by delta = time-dependent rather than frame-dependent

confusing? next you'll learn: speed, acceleration, motion.


