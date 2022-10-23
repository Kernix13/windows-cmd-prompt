# Batch Commands

Start using batch files - You might already know that batch files can make your life a lot easier when you have to deal with multiple commands more often. For instance, if you have the habit of using the same CMD commands, you can create a batch file and do away with the task of typing them again and again. All you’ll have to do is run the batch file.

<div id="back-to-top"></div>

## Table of Contents

1. [Batch file commands](#batch-file-commands)
1. [Improve Windows 10 with one-click batch files](#improve-windows-10-with-one-click-batch-files)
1. [How To Create A Batch File](#how-to-create-a-batch-file)
1. [Batch Files and Batch Commands](#batch-files-and-batch-commands)
1. [Writing a Windows batch script](#writing-a-windows-batch-script)
1. [5 Cool Batch Files](#5-cool-batch-files)

## Batch file commands

LINK: [Batch file commands](http://www.trytoprogram.com/batch-file-commands/)

List of batch file commands:

- ASSOC ATTRIB CD CHKDSK CHOICE
- CLS CMD COMP CONVERT COPY
- DATE DEL DIR DISKPART DRIVERQUERY
- ECHO EXIT EXPAND FC FIND
- FORMAT HELP IPCONFIG LABEL MD
- MORE MOVE NET PAUSE PING
- RD REM REN SET SHUTDOWN
- SORT START SYSTEMINFO TASKKILL TASKLIST
- TIME TITLE TREE TYPE VER
- VOL XCOPY

<div align="right">&#8673; <a href="#back-to-top" title="Table of Contents">Back to Top</a></div>

## Improve Windows 10 with one-click batch files

LINK: [Improve Windows 10 with one-click batch files](https://www.ghacks.net/2016/11/08/improve-windows-10-with-one-click-batch-files/)

- a collection of one-click batch files by Ghacks reader Joern that improve the operating system in various ways
- has files for download - SKIP

## How To Create A Batch File

LINK: [How To Create A Batch File](https://fossbytes.com/what-is-a-batch-file-in-windows-how-to-create-a-batch-file/)

- looks pretty basic but give it a read anyway

## Batch Files and Batch Commands

LINK: [Batch Files and Batch Commands](https://www.robvanderwoude.com/batchcommands.php)

- a huge list of commands to use in your .bat files

## Writing a Windows batch script

LINK: [Writing a Windows batch script](https://www.geeksforgeeks.org/writing-windows-batch-script/)

- Geeks for Geeks so expect this page to lock up your computer

## 5 Cool Batch Files

LINK: [5 Cool Batch Files](https://www.instructables.com/id/5-Cool-Batch-Files/)

- Password Generator: generates number only passwords
- Password Protected Command Prompt: This Command Prompt makes a user sign up then sign in to get the command prompt
- Website Crasher: stupid
- Website Pinger: stupid
- PC Cleanup Utility: Delete Internet cookies, Delete Temporary Files, Defrag Disk, and Cleanup Disk

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

<div align="right">&#8673; <a href="#back-to-top" title="Table of Contents">Back to Top</a></div>

2. PC Cleanup Utility:

```sh
@echo off
title PC Cleanup Utility http://www.youtube.com/user/techki-tv

:menu
cls
echo --------------------------------------------------------------------------------
echo PC Cleanup Utility
echo --------------------------------------------------------------------------------
echo.
echo Select a tool
echo =============
echo.
echo [1] Delete Internet Cookies
echo [2] Delete Temporary Internet Files
echo [3] Disk Cleanup
echo [4] Disk Defragment
echo [5] Exit
echo.
set /p op=Run:
if %op%==1 goto 1
if %op%==2 goto 2
if %op%==3 goto 3
if %op%==4 goto 4
if %op%==5 goto exit
goto error
:1
cls
echo --------------------------------------------------------------------------------
echo Delete Internet Cookies
echo --------------------------------------------------------------------------------
echo.
echo Deleting Cookies...
ping localhost -n 3 >nul
del /f /q "%userprofile%\Cookies\*.*"
cls
echo --------------------------------------------------------------------------------
echo Delete Internet Cookies
echo --------------------------------------------------------------------------------
echo.
echo Cookies deleted.
echo.
echo Press any key to return to the menu. . .
pause >nul
goto menu
:2
cls
echo --------------------------------------------------------------------------------
echo Delete Temporary Internet Files
echo --------------------------------------------------------------------------------
echo.
echo Deleting Temporary Files...
ping localhost -n 3 >nul
del /f /q "%userprofile%\AppData\Local\Microsoft\Windows\Temporary Internet Files\*.*"
cls
echo --------------------------------------------------------------------------------
echo Delete Temporary Internet Files
echo --------------------------------------------------------------------------------
echo.
echo Temporary Internet Files deleted.
echo.
echo Press any key to return to the menu. . .
pause >nul
goto menu
:3
cls
echo --------------------------------------------------------------------------------
echo Disk Cleanup
echo --------------------------------------------------------------------------------
echo.
echo Running Disk Cleanup...
ping localhost -n 3 >nul
if exist "C:\WINDOWS\temp"del /f /q "C:WINDOWS\temp\*.*"
if exist "C:\WINDOWS\tmp" del /f /q "C:\WINDOWS\tmp\*.*"
if exist "C:\tmp" del /f /q "C:\tmp\*.*"
if exist "C:\temp" del /f /q "C:\temp\*.*"
if exist "%temp%" del /f /q "%temp%\*.*"
if exist "%tmp%" del /f /q "%tmp%\*.*"
if not exist "C:\WINDOWS\Users\*.*" goto skip
if exist "C:\WINDOWS\Users\*.zip" del "C:\WINDOWS\Users\*.zip" /f /q
if exist "C:\WINDOWS\Users\*.exe" del "C:\WINDOWS\Users\*.exe" /f /q
if exist "C:\WINDOWS\Users\*.gif" del "C:\WINDOWS\Users\*.gif" /f /q
if exist "C:\WINDOWS\Users\*.jpg" del "C:\WINDOWS\Users\*.jpg" /f /q
if exist "C:\WINDOWS\Users\*.png" del "C:\WINDOWS\Users\*.png" /f /q
if exist "C:\WINDOWS\Users\*.bmp" del "C:\WINDOWS\Users\*.bmp" /f /q
if exist "C:\WINDOWS\Users\*.avi" del "C:\WINDOWS\Users\*.avi" /f /q
if exist "C:\WINDOWS\Users\*.mpg" del "C:\WINDOWS\Users\*.mpg" /f /q
if exist "C:\WINDOWS\Users\*.mpeg" del "C:\WINDOWS\Users\*.mpeg" /f /q
if exist "C:\WINDOWS\Users\*.ra" del "C:\WINDOWS\Users\*.ra" /f /q
if exist "C:\WINDOWS\Users\*.ram" del "C:\WINDOWS\Users\*.ram"/f /q
if exist "C:\WINDOWS\Users\*.mp3" del "C:\WINDOWS\Users\*.mp3" /f /q
if exist "C:\WINDOWS\Users\*.mov" del "C:\WINDOWS\Users\*.mov" /f /q
if exist "C:\WINDOWS\Users\*.qt" del "C:\WINDOWS\Users\*.qt" /f /q
if exist "C:\WINDOWS\Users\*.asf" del "C:\WINDOWS\Users\*.asf" /f /q
:skip
if not exist C:\WINDOWS\Users\Users\*.* goto skippy /f /q
if exist C:\WINDOWS\Users\AppData\Temp\*.zip del C:\WINDOWS\Users\Users\*.zip /f /q
if exist C:\WINDOWS\Users\AppData\Temp\*.exe del C:\WINDOWS\Users\Users\*.exe /f /q
if exist C:\WINDOWS\Users\AppData\Temp\*.gif del C:\WINDOWS\Users\Users\*.gif /f /q
if exist C:\WINDOWS\Users\AppData\Temp\*.jpg del C:\WINDOWS\Users\Users\*.jpg /f /q
if exist C:\WINDOWS\Users\AppData\Temp\*.png del C:\WINDOWS\Users\Users\*.png /f /q
if exist C:\WINDOWS\Users\AppData\Temp\*.bmp del C:\WINDOWS\Users\Users\*.bmp /f /q
if exist C:\WINDOWS\Users\AppData\Temp\*.avi del C:\WINDOWS\Users\Users\*.avi /f /q
if exist C:\WINDOWS\Users\AppData\Temp\*.mpg del C:\WINDOWS\Users\Users\*.mpg /f /q
if exist C:\WINDOWS\Users\AppData\Temp\*.mpeg del C:\WINDOWS\Users\Users\*.mpeg /f /q
if exist C:\WINDOWS\Users\AppData\Temp\*.ra del C:\WINDOWS\Users\Users\*.ra /f /q
if exist C:\WINDOWS\Users\AppData\Temp\*.ram del C:\WINDOWS\Users\Users\*.ram /f /q
if exist C:\WINDOWS\Users\AppData\Temp\*.mp3 del C:\WINDOWS\Users\Users\*.mp3 /f /q
if exist C:\WINDOWS\Users\AppData\Temp\*.asf del C:\WINDOWS\Users\Users\*.asf /f /q
if exist C:\WINDOWS\Users\AppData\Temp\*.qt del C:\WINDOWS\Users\Users\*.qt /f /q
if exist C:\WINDOWS\Users\AppData\Temp\*.mov del C:\WINDOWS\Users\Users\*.mov /f /q
:skippy
if exist "C:\WINDOWS\ff*.tmp" del C:\WINDOWS\ff*.tmp /f /q
if exist C:\WINDOWS\ShellIconCache del /f /q "C:\WINDOWS\ShellI~1\*.*"
cls
echo --------------------------------------------------------------------------------
echo Disk Cleanup
echo --------------------------------------------------------------------------------
echo.
echo Disk Cleanup successful!
echo.
pause
goto menu
:4
cls
echo --------------------------------------------------------------------------------
echo Disk Defragment
echo --------------------------------------------------------------------------------
echo.
echo Defragmenting hard disks...
ping localhost -n 3 >nul
defrag -c -v
cls
echo --------------------------------------------------------------------------------
echo Disk Defragment
echo --------------------------------------------------------------------------------
echo.
echo Disk Defrag successful!
echo.
pause
goto menu
:error
cls
echo Command not recognized.
ping localhost -n 4 >nul
goto menu
:exit


echo Thanks for using PC Cleanup Utility by Ryan
ping 127.0.0.1 >nul
exit
```

<div align="right">&#8673; <a href="#back-to-top" title="Table of Contents">Back to Top</a></div>
