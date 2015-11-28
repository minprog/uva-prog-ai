
# NameSurfer (continued)

### Milestone 4: Create the background grid for the NameSurferGraph class

The next step in the process is to begin the implementation of the `NameSurferGraph`
class, which is responsible for displaying the graph in the window by building the
underlying model. The starter code for the `NameSurferGraph` class is provided in the 
pset zip file.

There are a couple of important items in the `NameSurferGraph` starter file that are worth
noting:

1. This class extends `GCanvas`, which means that every `NameSurferGraph` object is not
only a `GCanvas` but also an instance of all the superclasses of the `GCanvas` class.
`GCanvas` is a subclass of `Component` in the standard `java.awt` package and therefore
is part of the hierarchy of classes that can be added to the display area of a program.
Moreover, it means we can call any of the `GCanvas` methods, such as adding or 
removing `GObjects`, from within `NameSurferGraph`.
2. The starter file includes a tiny bit of code that monitors the size of the window and
calls `update()` whenever the size changes. This code requires only a couple of lines to 
implement, but would be hard to explain well enough for you to implement on your
own. Writing a page of description so that you could add a couple of lines seemed
like overkill, particularly given that the strategy is easiest to learn by example.

To start the process of adding the graphing code, go back to the `NameSurfer` class and
change its definition so that it extends `Program` rather than the temporary expedient of 
extending `ConsoleProgram` (if you were using that for debugging). At the same time,
you should remove the various `println()` calls that allowed you to trace the operation of 
the interactors in the earlier milestones.

Now, you'll need to declare a `NameSurferGraph` private instance variable in your main
`NameSurfer` class:

    private NameSurferGraph graph;

You should then change the constructor of the `NameSurfer` class so that it creates a new
`NameSurferGraph` object and adds that object to the display, as follows:

    graph = new NameSurferGraph();
    add(graph);

If you run the program with only these changes, it won’t actually display anything on the
screen. To create the graph, you need to implement the `update()` method, which will
almost certainly involve defining private helper methods as well. As a first step, write the
code to create the background grid for the graph, which consists of the vertical line
separating each decade, the horizontal lines that provide space for the top and bottom
borders (which are there to ensure that the text labels stay within the window bounds),
and the labels for the decades. As with all the graphical applications you’ve written, the
lines and labels are represented using `GLine` and `GLabel` objects, which you add to the
graph in the appropriate positions.

### Milestone 5: Complete the implementation of NameSurferGraph class

In addition to creating the background grid, the `update()` method in `NameSurferGraph` also
has to plot the actual data values. The `NameSurferGraph`
class includes two methods for specifying what entries are displayed on the screen. The
`addEntry()` method adds a new `NameSurferEntry` to a list of values that are currently on
the display. The `clear()` method deletes all of the entries in that list so as to clear the
graph.

It is important to note that neither `addEntry()` or `clear()` actually changes the display. To
make changes in the display, you need to call `update()`, which **deletes any existing
`GObjects` from the canvas and then assembles everything back up again**. At first glance,
this strategy might seem unnecessary. It would, of course, be possible to have `addEntry()`
just add all of the `GLines` and `GLabels` necessary to draw the graph.

The problem with that approach is that it would no longer be possible to reconstruct the
entire graph. In this example, you need to do just that to create a new graph whenever
you change the size of the display. By storing all of the entries in an internal list, the
`NameSurferGraph` class can redraw everything when `update()` is invoked from the
`componentResized` method.

There are a couple of points that you should keep in mind while implementing this part of 
the program:

* To make the data easier to read, the lines on the graph are shown in different colors.
In the sample applet on the web site, the first data entry is plotted in black, the second in 
red, the third in blue, and the fourth in magenta. After that, the colors cycle around
again through the same sequence.
* The fact that rank 1 is at the top of the window and rank 1000 is at the bottom means
that it can sometimes seem confusing that rank 0 (which means that the name does
not appear in the top 1000 values for that year, appears at the bottom. To reduce the
apparent discontinuity between rank 1 and rank 0, the entries for names that are absent
from the data for a decade are **listed with an asterisk** instead of a numeric rank. You
can see several examples of this convention in the data for *Samantha* in Figure 1.

