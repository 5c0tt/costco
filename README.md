08.08.2015 — 08:26:30 PM -0700	
Scott Haneda [@scotthaneda](https://twitter.com/scotthaneda)

#How to print full resolution non-jpg .tiff files at Costco Printing Center
These are instructions on how to prepare your files for printing at Costco and get the best possible resolution and results from a TIFF file instead of the lossy compressed jpg file format.

This only works on photo printing machines that use real photo chemicals to print you digital files.  A machine called a [Noritsu](http://www.noritsu.com/) is one such machine.  The document [instructions.pdf](instructions.pdf) will explain how to send TIFF files instead of JPG files so you can get zero compression artifacts.  However, as long as their equipment does not open, re-save, and re-compress the image, or re-size it, the JPG setting at a highest level would probably be imperceptible to the eye.

#As a side note, HOW TO CHANGE MARGINS IN TEXTEDIT
**ADVANCED USERS ONLY**, or just download the template below.

It has long pissed people off that you can't change the margin's in TextEdit and they are locked at around 1 inch around all four sides.

Here is how I made a template that I start from, with 1/2" margins all the way around.

First, make a new TextEdit Document and save it as an .rtfd file so you can have images and other media in it.  Then using the command line, you need to cd into the document and add a line of Postscript.

Here is the line we will be adding:
<pre>\margl720\margr720\margt720\margb720\vieww12240\viewh15840\viewkind1\viewscale102</pre>

You have a file called template.rtfd, it is actually a package, `cd` into the package and you will see a `TXT.txt` file, which you will need to open with a basic text editor, I used `pico -w template.rtfd/TXT.txt`

In the file, at the very top, you should see these lines of Postscript:
<pre>{\rtf1\ansi\ansicpg1252\cocoartf1348\cocoasubrtf170
{\fonttbl\f0\fnil\fcharset0 HelveticaNeue;}
{\colortbl;\red255\green255\blue255;\red0\green0\blue255;}
\margl1440\margr1440\vieww12240\viewh15840\viewkind1
\deftab720
\pard\tx560\tx1120\tx1680\tx2240\tx2800\tx3360\tx3920\tx4480\tx5040\tx5600\tx6160\tx6720\pardeftab720</pre>

We need to alter one line in that Postscript code:
<pre>{\rtf1\ansi\ansicpg1252\cocoartf1348\cocoasubrtf170
{\fonttbl\f0\fnil\fcharset0 HelveticaNeue;}
{\colortbl;\red255\green255\blue255;\red0\green0\blue255;}
\margl720\margr720\margb720\margt720\vieww12240\viewh15840\viewkind1
\deftab720
\pard\tx560\tx1120\tx1680\tx2240\tx2800\tx3360\tx3920\tx4480\tx5040\tx5600\tx6160\tx6720\pardeftab720</pre>

It is line 4 in case you didn't notice where I changed the 1440 to 720.  You will see I also added in margint ( top ) and marginb ( bottom )

If you just want to download the template, feel free to [download it here](template.rtfd.zip).