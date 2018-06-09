# Reporter
C# Library for reporting and logging

This project contains the code for the reporter I use in all of my projects. It contaned some features I stripped out because 
of their static use in other projects.

TO USE:
Import the .dll to your project. The only class available is static, set the folder name to whatever you would like. 

Within your code, when you have a new section of code, use start section, when the section use end section. When there is 
something to report on use WriteSection. Write section needs two things, what to write and then a number. For now, only use 0 as the number.
This was part of the stripped features that were used in other software.


Here is an example of using the reporter within a c# console program.

static void Main(string[] args)
{
    Reporter.Reporter.StartReporter("Reporter Test Folder");

    Reporter.Reporter.StartSection("First Section");

    Reporter.Reporter.WriteContent("First mention", 0);

    Reporter.Reporter.EndSection();

    Reporter.Reporter.StartSection("Second Section");

    Reporter.Reporter.WriteContent("Foo happened in the second section",0);

    Reporter.Reporter.WriteContent("Bar happened in the second section as well", 0);

    Reporter.Reporter.EndSection();
}

The report file looks like this when the code above runs.

*****************************************
Software Launched at: 6/9/2018 10:09:22 AM
 
------------- Start: First Section -------------
6/9/2018 10:09:22 AM
6/9/2018 10:09:22 AM    First mention
------------- End: First Section -------------
 
------------- Start: Second Section -------------
6/9/2018 10:09:22 AM
6/9/2018 10:09:22 AM    Foo happened in the second section
6/9/2018 10:09:22 AM    Bar happened in the second section as well
------------- End: Second Section -------------
 

