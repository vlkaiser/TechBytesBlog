---
layout: post
title: C++ in VSCode on Windows
---

Very comprehensive and easy to follow instructions at this link:  
[Visual Studio - Using GCC with MinGW](https://code.visualstudio.com/docs/cpp/config-mingw)

## Setup

Compiling C++ programs in VSCode requires
1. VS Code
2. Installing the C/C++ Extension in VSCode (Microsoft)
3. Installing MinGW (Runtime env. for GCC)
(GNU Compilier Collection for C/C++/Fortran...)
4. Add GCC to the Windows PATH
Necessary to add the GCC path to the Windows Environment Variables [See instructions below](#Add-GCC-to-the-Windows-PATH-Environment-Variables)
5. Check that it worked by opening the Cmd Prompt and checking the version number.  If a version number does not come back, check the MinGW installation, and the Windows PATH variable accuracy.
~~~
> g++ --version
> gdc --version
~~~

## Workspace
VSCode supports command prompt instructions.  Open the Cmd Prompt:
~~~
> mkdir projects        // Make a projects folder
> cd projects           // Navigate to that folder
> mkdir helloworld      // Make a helloworld folder
> cd helloworld         // Navigate to the helloworld folder
> code .                // Create a VSCode workspace in the current working folder
~~~
In the project in VSCode, right click -> add a *.cpp file.
<br />
<br />

## Building
The link above explains how to create a [tasks.json](tasks.json) file to tell VS Code how to build (compile) the program.

Alternatively, use the command line (where 'helloworld' is the user-defined output file):
~~~
> g++ helloworld.cpp -o helloworld
~~~

## Running
Use the command line:
~~~
> helloworld
~~~
This will run the program, and you will see the output in the command prompt.

<br />
<br />
<br />

-----

### Add GCC to the Windows PATH Environment Variables
1. In the Windows search bar, type 'settings' to open your Windows Settings.  
2. In the search bar, type "Edit environment variables" for your account.  
3. Choose the Path variable and then select Edit.  
4. Select New and add the Mingw-w64 destination folder path to the system path.   
(The exact path is displayed in the MinGW installation.  **Verify that your PATH is correct**  
Default: [C:\Program Files\mingw-w64\x86_64-8.1.0-posix-seh-rt_v6-rev0\mingw64\bin](C:\Program-Files\mingw-w64\x86_64-8.1-0-posix-seh-rt_v6-rev0\mingw64\bin)  

5. Select OK to save the updated PATH. You will need to reopen any console windows for the new PATH location to be available.
