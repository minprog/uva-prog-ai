## Hacker edition: `MazeSolvingKarel.java`

A *hacker problem* is a fully optional extension to the normal problems. In
general, we would expect anyone to tackle only the normal problems and not the
hacker problems. If you're feeling a particular lack of challenge in those
normal problems, you are welcome to try and submit the hacker version. Do mind
that extra credit will not be given and that hacker problems will be held to
the same standards as every other submitted problem in this course.

Try and make Karel solve mazes! There are 5 mazes included in the Karel files
(*pset1.zip*). The first two mazes can be solved by following simple rules, the
remaining three however are more difficult. A maze in the world of Karel looks
like this:

![A maze in the world of Karel.](figure8.png)

The exits of a maze are marked by a beeper. You can assume these are the only
beepers in the world. Placing extra beepers is allowed, but take care not to
confuse these with the real exits!

The files include five mazes, numbered 1 through 5. Your solution should be a
single class, `MazeSolvingKarel`, which can move Karel to the exit of as many 
mazes as you can solve.

Be sure to include in the comments which mazes you solved and what algorithm 
you used to solve them. Add a short summary and insert comments in the code 
that describe your approach.

Want some ideas to solve the harder mazes? Try
[this page](http://www.astrolog.org/labyrnth/algrithm.htm). Also note that
`SuperKarel` is capable of painting floors. This can help keep track of where
you've been.
