# Getting Started

In this course you are required to work on the Linux workstations and use gedit
for editing your Java code. After this course, you may want to upgrade to a more
sophisticated environment, but in this course that's not allowed.

So, without further ado, here’s the instructions for getting started:

* Start the computer in Linux; if it starts in Windows, just reboot and press F2
  when asked.
* Log on to the Linux workstation.
* Start the Terminal.
* Create a new directory named `prog` to store your problem sets from this
  course. Do this by typing the following in the terminal:

       mkdir prog
       
* Now you're ready for the first problem set! Continue with
  [karel](/problem-sets/karel) after reading the remainder of this guide.

## gedit

Now is probably a good time to look at what gedit offers. It's a simple editor,
but it does offer a few options to make editing code easier. Start the editor
(note the `&` at the end)

    gedit &

And go to Preferences in the Edit menu. Tick the "Display line numbers" box,
this makes it easier to locate compile errors. Also tick the box in front of
"Highlight matching brackets" unless you enjoy doing this manually. The "Display
right margin at column: ..." option is useful to remind yourself not to cram the
whole program on a single line.

Next up is the Editor tab, which contains the tabs and spaces
configuration. Holy wars are fought over the question if tabs or spaces are
better for indentation purposes. Choose either one of the following methods and
be consistent throughout the problem set.

* Either spaces everywhere,
* tabs everywhere,
* or, tabs for indentation and spaces for alignment.

Both tabs and spaces are invisible characters in gedit. You can highlight them
by doing a search (`\t` for tabs ` ` for spaces). Note that you can only search
for one at the time. Take a look at the [styleguide] for more about indentation.

[styleguide]: /reference/styleguide

## Submitting the problem sets

Once you're done with your problem set, you can submit it using the submit tab
that you'll find on the page of that problem set. You can make a zip with the
required files by running the following command.

    make submit

