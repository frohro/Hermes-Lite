May 3, 2014

This is a version of the freerouting software written by Alfons Wirtz. The core
software was intended to be run as a Java WebStart application from his web
site, www.freerouting.net. Alfons recently open-sourced his software under the
GPL version 3 license. I created build scripts using Ant and Java together with
the free launch4j and bundleapp tools to allow the program to be built and run
as a standalone application on either OS X, Linux, or Windows 7/8.

The files with "-binary-" in the file name contain built versions of the wrapper
for each of these operating systems. You will need an up-to-date Java runtime
environment (1.7 or greater) installed and available to run the built versions.

For Windows you should be able to put the FreeRouter.exe somewhere in your
path and/or double-click. The FreeRouter.app should do the same for OS X.
For Linux you will need the FreeRouter shell script and the freerouting-net.jar
file located somewhere convenient. The .jar file needs to be in the same
directory as the shell script.

For development on the source you will need Apache Ant and the Java
Development kit installed. JFlex is used to build some of the files
but is optional since the distribution contains the resulting .java files.

Bundleapp is used to build the OS X wrapper. This runs on OS X, Linux, and
Windows 7. Launch4j is used to build the wrapper for Windows. Launch4j is
specific to the host operating system. I have put all three versions in the
tools directory but I noticed that some zip tools don't set permissions
appropriately. If this happens, download the appropriate version of launch4j
and place in the appropriate directory in the tools directory.

"ant" on the command line in the freerouting-net directory will build the source
and all three wrappers.

For more targets see the build.xml file.

My main build environment is OS X and JDK 1.8. I checked that the applications
would build and run under their appropriate operating system in virtual machines
using Ubuntu 14.04 and 32-bit Windows 7. I have reports that the Windows version
runs fine on 64-bit Windows 8.1.

Enjoy!
