# Reporter
C# Library for reporting and logging

This project contains the code for the reporter I use in all of my projects. It contained some features I stripped out because 
of their static use in other projects.

##Using the library
Use the method StartReporter as soon as you want. Either pass a folder name or a path from the AppData\Local folder to store the Report.txt file. Then start sections and write content to your hearts content. When the write content method is used pass a "0" as the second parameter. This was one of the features used in other software that has been stripped from the library.


Here is an example of using the reporter within a c# console program. 
```
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
```
The report file looks like this when the code above runs. The file can be found within the AppData\local folder under "Reporter Test Folder"
```
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
```
 

