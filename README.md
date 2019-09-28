# Project imgorg

small command line tool using dotnet core 3.0 and it's compacting features for different targeting operating systems

I am using some of my libraries here to make the task easier.
This is a description of the project and how to build it as well as a description of the tool and how to use it.

## cli tool __iorg__

You can either build the project for your target system or just download the binary. It looks really small ... the optimizer of dotnet core 3.0 is in beta ...
I tested it with a few thousand files ... however they all use the same naming patterns so far ...
I will add images of another webcam with more flexible naming patterns later.

Binaries available for direct download

* macOS

## Setup the project

This is my step-by-step instructions for seting up the solution consisting of several projects:

    mkdir ~/ProjectsCoreGitHub/Source
    cd ~/ProjectsCoreGitHub/Source
    git clone https://github.com/Burkhardt/Persist.git
    git clone https://github.com/Burkhardt/OsLibCore.Test.git
    git clone https://github.com/Burkhardt/nyokacli.git
    git clone https://github.com/Burkhardt/OsLibCore.git
    git clone https://github.com/Burkhardt/JsonPit.git
    git clone https://github.com/Burkhardt/RaiUtils.git

Now we have 6 projects in subdirectories.

![screenshot of folders](FolderStructure.jpg)

Create a solution

    dotnet new sln

Creates a solution file - it's empty yet.

    dotnet sln add Persist
    dotnet sln add JsonPit
    dotnet sln add nyokacli
    dotnet sln add OsLibCore
    dotnet sln add OsLibCore.Test
    dotnet sln add RaiUtils

The use of JsonFile for `.nyokaremote.json` is shown in a unit test:

![UnitTests in GitHub project](UnitTestsWithExampleForReadOnly_nyokaremote.jpg)

Start VS Code

    code .

Make sure you have the necessary plugins

![PlugIns](MyPlugInsInVSCode.jpg)

    * .NET Core Test Explorer
    * C#
    * C# XML Documentation
    * Docker (for later)

Switch to Test Explorer

![TestFirst](TestFirst.jpg)

Now you can start any unit test on the vright side via `Debug Test` or on the left side tapping the run button in the test explorer.
