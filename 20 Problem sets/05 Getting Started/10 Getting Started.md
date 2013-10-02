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
  course. Do this by typing mkdir prog the following in the terminal.

## Hello World!

*Hello world* is one of the simplest possible programs you can write. This is a
 great way to see if your environment is set up properly.
 
* Start by creating a subdirectory in `prog` named `hello`. Then `cd` into that
  directory.
* Execute `touch HelloWorld.java` and open the empty file it creates in
  gedit. You can start gedit with `gedit`. Note that you can no longer use your
  terminal until you close gedit. You can avoid this by starting gedit with a
  `&` at the end.
* Copy-and-paste the following code into gedit, save the file, and close the
  editor.
  
      public class HelloWorld
      {
         public static void main(String[] args)
         {
            System.out.println("Hello World!");
         }
      }
  
* Back in the terminal type `javac HelloWorld.java` to compile the java
  code. You should now have a file called `HelloWorld.class` with the compiled
  code. Type `ls` to see a list of all files in the current directory.
* Enter `java HelloWorld` to execute the program. You should see `Hello World!`
  as output in the terminal.

### Makefiles

In this course we use Makefiles which can be used to automate various compile
tasks. The HelloWorld program is trivial to compile, but we will create one to
demonstrate how they work.

* Create a file name `Makefile` (note the capitalization) with the following
  contents.
  
      all: HelloWorld.class
      
      HelloWorld.class:
      	javac HelloWorld.java
      
      clean:
      	rm *.class
  
  Note that the whitespace in front of `javac HelloWorld.java` and `rm *.class`
  is a tab-character; `make` will complain to you if you use spaces. If you're
  wondering what this Makefile does have a look at [Makefiles by example].
* Go back to the terminal and execute the makefile with `make`. If you still
  have the `HelloWorld.class` file it will tell you there is nothing to be done.
* Run `make clean` to remove `HelloWorld.class` and try again.
* After `make` is finished verify that you can run the program again.

[Makefiles by example]: http://mrbook.org/tutorials/make/

## gedit

Now that you've written some code it's probably a good time to look at what
gedit offers. It's a simple editor, but it does offer a ways to make editing
code a little easier. Start the editor and go to Preferences in the Edit
menu.

On the first tab you should tick the "Display line numbers" box, this makes it
easier to locate compile errors. Also tick the box in front of "Highlight
matching brackets" unless you enjoy doing this manually. The "Display right
margin at column: ..."  option is useful to remind yourself not to cram the
whole program on a single line.

Next up is the Editor tab, which contains the tabs and spaces
configuration. Holy wars are fought over the question if tabs or spaces are
better for indentation purposes. Choose either one of the following methods and
be consistent throughout the problem set.

* Either spaces everywhere,
* tabs everywhere,
* or, tabs for indentation and spaces for alignment.

Both tabs and spaces are invisible characters in gedit. You can highlight them
by doing a search for those characters (`\t` for tabs). Note that you can only
search for one of these at the same time. Take a look at the [styleguide] for
more about indentation.

[styleguide]: /reference/styleguide

## Submitting the problem sets

Once you're done with your problem set, you can submit it using the submit tab
that you'll find on each page with a problem set. You can make a zip with the
required files by running the following command in a terminal.

    make submit

You can submit a problem set multiple times, we always grade at the last
submission before the deadline. Make sure to submit all files when you resubmit,
not only the files that changed.

## Using your own machine

If you are using your own machine during the lab session you should install a
version of Linux, such as [Ubuntu]. If you are running Mac OS or Windows you can
either dual-boot or use a hypervisor such as [VirtualBox] or [VMWare].

In order to run and compile the Java code for the lab sessions you need a JRE
and JDK for Java version 1.6 (also referred to as Java 6). You can check the JRE
and JDK version by executing `java -version` and `javac -version` in a
terminal. They should both yield something similar to `java version
"1.6.0_27"`. Ask a lab assistant for help if you have any trouble installing or
configuring Java.

[Ubuntu]: http://www.ubuntu.com/
[VirtualBox]: https://www.virtualbox.org/
[VMWare]: http://www.vmware.com/
