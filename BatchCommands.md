# Batch Commands

Start using batch files - You might already know that batch files can make your life a lot easier when you have to deal with multiple commands more often. For instance, if you have the habit of using the same CMD commands, you can create a batch file and do away with the task of typing them again and again. All you’ll have to do is run the batch file.

## Useful Links

- [Batch file commands](http://www.trytoprogram.com/batch-file-commands/)
- [Improve Windows 10 with one-click batch files](https://www.ghacks.net/2016/11/08/improve-windows-10-with-one-click-batch-files/)
- [Batch Scripts](https://lifehacker.com/tag/batch-scripts)
- [How To Create A Batch File](https://fossbytes.com/what-is-a-batch-file-in-windows-how-to-create-a-batch-file/)
- [Batch Files & Batch Commands](https://www.robvanderwoude.com/batchcommands.php)
- [https://www.geeksforgeeks.org/writing-windows-batch-script/](https://www.geeksforgeeks.org/writing-windows-batch-script/)
- [5 Cool Batch Files](https://www.instructables.com/id/5-Cool-Batch-Files/)
  - Password Generator
  - Password Protected Command Prompt
  - Website Crasher
  - Website Pinger
  - PC Cleanup Utilities

1. Password Generator - Code:

```shell
@echo off
:Start2
cls
goto Start
:Start
title Password Generator

echo I will make you a new password.
echo Please write the password down somewhere in case you forget it.
echo ----------------------------------------­-----------------------
echo 1) 1 Random Password
echo 2) 5 Random Passwords
echo 3) 10 Random Passwords
echo Input your choice

set input=
set /p input= Choice:
if %input%==1 goto A if NOT goto Start2
if %input%==2 goto B if NOT goto Start2
if %input%==3 goto C if NOT goto Start2
:A
cls

echo Your password is %random%
echo Now choose what you want to do.
echo 1) Go back to the beginning
echo 2) Exit

set input=
set /p input= Choice:
if %input%==1 goto Start2 if NOT goto Start 2
if %input%==2 goto Exit if NOT goto Start 2
:Exit
exit
:B
cls

echo Your 5 passwords are %random%, %random%, %random%, %random%, %random%.
echo Now choose what you want to do.
echo 1) Go back to the beginning
echo 2) Exit

set input=
set /p input= Choice:
if %input%==1 goto Start2 if NOT goto Start 2
if %input%==2 goto Exit if NOT goto Start 2
:C
cls

echo Your 10 Passwords are %random%, %random%, %random%, %random%, %random%, %random%, %random%, %random%, %random%, %random%
echo Now choose what you want to do.
echo 1) Go back to the beginning
echo 2) Exit

set input=
set /p input= Choice:
if %input%==1 goto Start2 if NOT goto Start 2
if %input%==2 goto Exit if NOT goto Start 2
```
