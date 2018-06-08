# Reporter
C# Library for reporting and logging

This project contains the code for the reporter I use in all of my projects. It contaned some features I stripped out because 
of their static use in other projects.

TO USE:
Import the .dll to your project. The only class available is static, set the folder name to whatever you would like. 

Within your code, when you have a new section of code, use start section, when the section use end section. When there is 
something to report on use WriteSection. Write section needs two things, what to write and then a number. For now, only use 0 as the number.
This was part of the stripped features that were used in other software.
