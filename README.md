# Lab 1: Polygon Drawer
For this lab, you will create an application to "draw" polygons using the Model-View-Controller design scheme. Your program will open a window using Java's Swing library and allow users to click the screen to add vertexes to their polygon. Your program will also allow users to undo the last vertex they added or clear the screen and start again.

## Example Video

## Resources
[Java Polygon class](https://docs.oracle.com/javase%2F7%2Fdocs%2Fapi%2F%2F/java/awt/Polygon.html) - *You will want to use these to represent each vertex. The polygons the user sees will be a collection of these vertexes.*

[Java Swing examples](http://www.java2s.com/Tutorials/Java/Swing.htm) - *The Swing library allows programmers to create simple GUI for Java programs. For this project, the window has been created for you, but you will need to connect the visual elements to their respective functionalities*

[Original project this assignment was adapted from](https://github.com/heineman/tangram/tree/master/TangramCourseProject/sample)

[Tutorial for original assignment with old Java](https://heineman.github.io/TangramProject/sample/)

---

# Polygon Drawer: Part 1

## Getting Started with Swing
1. Set up your project structure
   1. Create a `model`, `view`, and `controller` packages in your project
   2. Mark all three as sources in the Project Structure
2. Create a GUI with the Swing UI Designer called `Application`
   1. Add `JMenuBar`, `JMenu`, and `JMenuItem` to your palette. Make sure `JMenu` has "is container" selected
   2. Create your layout. You should have `JMenuBar` with two `JMenu` components next to each other, each containing a `JMenuItem` component
   3. Give all of your components a name and they should appear in the `Application` class
3. Connect your Swing elements to code in your `Application` class
   1. Change `Application` to extend `JFrame`
   2. Add to the default constructor the following elements
      1. Calls the super constructor
      2. Sets the title, default close operation, and bounds of the window
      3. Set the border and border layout, then set the content pane. You may need to import an additional element here
4. Uncomment the lambda function in the main and run your project! You should see a window appear
5. Set up the rest of the menu bar
   1. Initialize the `JMenuBar`
   2. Initialize both `JMenu` components with their display text and add them to the `JMenuBar`
   3. Initialize both `JMenuItem` components and add them to the `JMenu`
   4. Set the shortcuts for both `JMenuItem` components
6. Run your program again! Your window should now be set up correctly

## Building Basic Structure
1. Create a `Model` class
2. Create a class `PolygonDrawer` which extends `JPanel`
   1. This class will have one instance variable of type `Model` and will need an associated constructor
3. Adjust `Application` so that your `JPanel` is of type `PolygonDrawer` instead
   1. Add a `Model` instance as an instance variable and as a parameter in the constructor
   2. Change the constructor of `JPanel` to type `PolygonDrawer`
4. Run your program again. Everything should still work!
5. Add Javadoc comments and submit your work
