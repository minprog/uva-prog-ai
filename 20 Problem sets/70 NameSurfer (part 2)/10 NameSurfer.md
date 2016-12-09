
# NameSurfer (continued)

This week we will start by finishing the Name Surfer assignment by completing
the last milestone. *If you have not yet completed Milestone 4, make sure 
to finish that first!* [A link to last week](https://progki.mprog.nl/psets/namesurfer)

You should really strive to have this last milestone completed at least on
Tuesday, preferably earlier. This leaves you with enough time to get a grasp of
Python and finish the last part of the assignment.

### Milestone 5: Complete the implementation of NameSurferGraph class

In addition to creating the background grid, the `update()` method in
`NameSurferGraph` also has to plot the actual data values. The `NameSurferGraph`
therefor keeps track of a list of NameSurferEntries. The class includes two
methods for specifying which entries are displayed on the screen. The
`addEntry()` method adds a new `NameSurferEntry` to a list of values that are
currently on the display. The `clear()` method deletes all of the entries in
that list so as to clear the graph.

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
can see several examples of this convention in the data for *Samantha* in Figure
1 of the previous assignment.

