## The appliance

### How to Install Appliance

In order to install the Appliance, you first need to install a hypervisor, which is a program that will let you run virtual machines on your own computer, whether you run Mac OS, Windows, or Linux.

* If you have a **Mac**, we recommend that you follow [these instructions](#mac) for VMware Fusion.

* If you have a PC running **Windows**, we recommend that you follow [these instructions](#windows) for VMware Player.

* If you have a PC running **Linux**, we recommend that you follow [these instructions](#linux) for VMware Player.

Once installed, it’s not uncommon for the appliance to take a minute or so to boot. But if, once at John Harvard’s desktop, the appliance still feels unbearably slow, you might need to enable hardware virtualization on your computer if it’s a PC running Windows or Linux. (Hardware virtualization should be enabled by default on any Intel-based Mac manufactured in the past few years.) Even with hardware virtualization enabled, though, virtual machines might still feel slow if your computer is a few years old, has a CPU that’s only 1GHz or so, or has only 1GB or so of RAM.

### How to Use Appliance

The first thing you should see when the appliance boots up is John Harvard's desktop. (Oh, henceforth, you are John Harvard. Your initial password is **crimson**. And here's what you look like.) Even though you might think of Linux as having only a command-line interface, graphical user interfaces do exist. We’ve installed Xfce, one of the most popular, for you. However, we installed as few programs as possible to keep the appliance small. You’re welcome to install additional programs via Menu &rarr; Administration &rarr; Software.

### How to Enable Dropbox

*This feature requires Internet access.*

To make it easier to back up files within the appliance automatically as well as share them with your own computer(s), you can synchronize a directory in John Harvard’s account with Dropbox. If taking a course, just take care to respect the course’s policies on academic honesty.

Here’s how to configure the appliance for Dropbox.

* Select Menu > Dropbox.

* You should be prompted to "download the proprietary daemon" (i.e., software); click OK. The software should proceed to download and unpack.

* You should then be prompted to set up Dropbox.

* If you don’t already have a Dropbox account, leave I don’t have a Dropbox account checked, then click Next. Create your Dropbox as prompted.

* If you already have an Dropbox account, check I already have a Dropbox account, then click OK. Log in as prompted.

* If prompted to upgrade your Dropbox, simply leave 2 GB checked (which is free) then click Next, unless you want to upgrade to a paid account.

* If prompted to Choose setup type, leave Typical checked, then click Install. If prompted to "merge", click Merge.

* If prompted to take a 5-step tour, click Skip Tour; its screenshots won’t match what you’ll see in the appliance.

* When informed That’s it!, uncheck Open my Dropbox folder now, then click Finish. A Dropbox icon should then appear in the appliance’s bottom-right corner.

Only those files and folders that you save in ~/Dropbox/ will be synchronized with your Dropbox account.

### How to Prevent Dropbox from Synching Personal Files into the Appliance

* Ctrl-click on the Dropbox icon in the appliance’s bottom-right corner and select Preferences….

* Click Advanced.

* Click Selective Sync….

* Uncheck the folders that you don’t want synched into the appliance.

* Click Update.


*Instructions based on the CS50 Appliance instructions from manual.cs50.net.*

