# Getting Started

Most likely you have already installed the virtual machine that contains Ubuntu, as
needed for this course. If not, head to <https://datanose.nl/#byod> and click
through to the VMware Store to "order" (for free) VMware Workstation for
Windows or VMware Fusion for Mac.

Then head to <http://sbt.science.uva.nl/bterwijn/BscKI_y1/vm/> and download
both files (this might take a while!). Put them in a safe place and *Open* them
in VMware. If in trouble, please confer with your TA or send an e-mail to the
course's heads!

## Downgrade Java

To be able to run Karel the Robot, we will need to use Java 6, not being a
particularly up-to-date version of Java. Because this is a virtual machine, we
need to worry less about the potential security implications of this (just
don't run any other Java software from troubling sources!).

To configure your Ubuntu virtual machine to use Java 6, run these commands:

    sudo update-alternatives --config java
    
    sudo update-alternatives --config javac

and then for both choose either one of the Java 6 versions that are presented.

## Dropboxing

Next, follow the instructions at <https://www.dropbox.com/install?os=lnx>
(Ubuntu 32-bit) to configure the virtual machine to use Dropbox so that your
work is automatically backed up, just in case something goes wrong with your
virtual machine. (If you really don't want to use Dropbox, that's fine, but
realize your files won't be backed up as a result!) If you don't yet have a
Dropbox account, sign up when prompted for the free (2 GB) plan. You're welcome
to install Dropbox on your own computer as well (outside of the appliance), per
<https://www.dropbox.com/install>, but no need if you'd rather not; just inside
the appliance is fine.

If you're already a Dropbox user but don't want your personal files to be
synched into the appliance, simply enable Selective Sync.

Incidentally, if curious how Dropbox itself works, allow us to introduce Thomas
Carriero and Alex Allain:

![embed](https://www.youtube.com/embed/VECV6r9s5SE?rel=0)

## Hello World!

*Hello world* is one of the simplest possible programs you can write. And for
now, it is a good way to see if your environment is set up properly.
 
* Start by creating a subdirectory in **Dropbox** named **hello**. Then **cd** into that
  directory.

* Execute **touch HelloWorld.java** to create an empty file with that name and
  open the empty file it creates in gedit. You can start gedit with **gedit**.
  Note that you can no longer use your terminal until you close gedit. You can
  avoid this by starting gedit with a **&** at the end.

* Copy-and-paste the following code into **gedit**, save the file, and close the
  editor.
  
      public class HelloWorld
      {
         public static void main(String[] args)
         {
            System.out.println("Hello World!");
         }
      }
  
* Back in the terminal type **javac HelloWorld.java** to compile the java
  code. You should now have a file called **HelloWorld.class** with the compiled
  code. Type **ls** to see a list of all files in the current directory.

* Enter **java HelloWorld** to execute the program. You should see `Hello World!`
  as output in the terminal.

### Makefiles

In this course we use Makefiles which can be used to automate various compile
tasks. The HelloWorld program is trivial to compile, but we will create one to
demonstrate how they work.

* Create a file name **Makefile** (note the capitalization!) with the following
  contents.
  
      all: HelloWorld.class
      
      HelloWorld.class:
      	javac HelloWorld.java
      
      clean:
      	rm *.class
  
  Note that the whitespace in front of **javac HelloWorld.java** and
  **rm \*.class** is a tab-character; **make** will complain to you if you use
  spaces. If you're wondering what this Makefile does, have a look at
  [Makefiles by example].

* Go back to the terminal and execute the makefile with **make**. If you still
  have the **HelloWorld.class** file it will tell you there is nothing to be done.

* Run **make clean** to remove **HelloWorld.class** and try again.

* After **make** is finished verify that you can run the program again.

[Makefiles by example]: http://mrbook.org/tutorials/make/

## gedit

Now that you've written some code it's probably a good time to look at what
**gedit** offers. It's a simple editor, but it does offer a ways to make editing
code a little easier. Start the editor and go to *Preferences* in the *Edit*
menu.

On the first tab you should tick the *Display line numbers* box, this makes it
easier to locate compile errors. Also tick the box in front of *Highlight
matching brackets* unless you enjoy doing this manually. The *Display right
margin at column: ...* option is useful to remind yourself not to cram the whole
program on a single line.

Next up is the *Editor* tab, which contains the tabs and spaces
configuration. Holy wars are fought over the question if tabs or spaces are
better for indentation purposes. Choose either one of the following methods and
be consistent throughout the problem set.

* Either spaces everywhere,
* tabs everywhere,
* or, tabs for indentation and spaces for alignment.

Both tabs and spaces are invisible characters in gedit. You can highlight them
by doing a search for those characters (`\t` for tabs). Note that you can only
search for one of these at the same time.

## Submitting your problem sets

Once you're done programming, you can submit it using the submit tab that
you'll find on each page with a problem set. You can make a **zip** with the
required files by running the following command in a terminal.

    make submit

You can submit a problem set multiple times, we always grade at the last
submission before the deadline. Make sure to submit all files when you resubmit,
not only the files that changed.
