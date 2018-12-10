## Current Filewave Client Kiosk Customization from 12.2+

The look and feel of the FileWave desktop Kiosk for macOS or Windows can be customized using [Qt Style Sheets](https://doc.qt.io/qt-5/stylesheet.html). You would have to create a file named fwGUI.qss and deploy it to your clients in the right location. 

For Mac: `/usr/local/sbin/FileWave.app/Contents/Resources/fwGUI.app/Contents/custom`

For Windows: `C:\Program Files\FileWave\custom (might be "Program Files (x86)", depending on the platform)`

The icons are now also customizable by placing your customized icon in the right location with the correct file name. All of this can be achieved by deploying a Filewave fileset with all the modifications and files built into it. 

If you already have *pre-12.2* customizations, you can simply extend them by adding fwGUI.qss as well as your custom icons to your existing fileset. *Pre-12.2* clients will simply ignore the style sheet and new icons, but will continue to work, whereas newer clients will exhibit your custom look.

### Why we need an editor?

An editor is not really needed, but if you are not adept at customizing Qt Style Sheets or don't have the time to do so, then it would be easier if you had a template that allowed you to change and visualize how your kiosk will look after doing all these modifications.  When you are happy with the changes, then you can save your .qss file and download to your computer so you can build your fileset.

### How does it work?

Taken directly from the *Filewave Knowledge Base* (because its only readable if you have an account...) `sigh`:

*The syntax of Qt Style Sheets is similar to CSS, though there are some differences. If you want to learn more about the syntax, check "[The Style Sheet Syntax](https://doc.qt.io/qt-5/stylesheet-syntax.html)". This page contains several examples that will help you better understand it.  In order to make it easier to customize the dialogs, every widget has a unique descriptive name. You can use style sheet selectors to refer to a particular widget. Besides, there are some additional properties that can be used to select several widgets that have something in common with a single selector (e.g. "select all field names"). The list of all widget names and properties is defined below, in Styling rules.*

