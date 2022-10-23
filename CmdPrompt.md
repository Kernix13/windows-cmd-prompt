# Command Prompt Commands

<div id="back-to-top"></div>

## Table of Contents

1. [GENERAL NOTES](#general-notes)
1. [BASIC COMMANDS](#basic-commands)
1. [NETWORK and INTERNET](#network-and-internet)
1. [DRIVES](#drives)
1. [BASIC COMPUTER COMMANDS](#basic-computer-commands)
1. [ADVANCED and REPAIR COMMANDS](#ADVANCED=AND-REPAIR-COMMANDS)
1. [MISCELLANEOUS COMMANDS](#miscellaneous-commands)

## GENERAL NOTES

- Open command prompt by typing `cmd` in the run box or use the keys `Win + R` and then enter `cmd`
- Good Links:
  - [The Complete List of Command Prompt (CMD) Commands](https://www.lifewire.com/list-of-command-prompt-commands-4092302): a Lifewire article so you know it's good!
  - [Windows Commands](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/windows-commands): a huge list of commands

Why do I have this: `C:\Users\Jim>`

## BASIC COMMANDS

- `cls` - clear screen of all previous commands
- `cd` or `chdir` – to change directory - cls – cd – chdir - cd.. - brings you back a directory – `cd` and `dir` will list directories (is that correct?)
- `start` – opens a new command prompt – you can create a text file with nothing but `start` in it and save it with a `*.bat` extension – when you double-click it to open, it opens the cmd prompt
- You can use it to open programs after getting their name from the `tasklist` command like `photoshop.exe` – so does `WIN + R` (?)
- `systeminfo` - show the system information - to know what brand of network card you have, processor details, or the exact version of your Windows OS
- Use `systeminfo /s` followed by the host name of a computer on your local network, to remotely grab the information for that system. This may require additional syntax elements for the `domain`, `user name`, and `password`, like this: `systeminfo /s [host_name] /u [domain]\[user_name] /p [user_password]`
- `prompt` - change the command prompt text - `prompt $m$p$g`, which will show the full path of a mapped drive in the prompt, alongside the drive letter - You can execute prompt alone without options, to return it to its default
- `help` - used to provide more info on another command – n/a for every command so try adding to any command the help switch `/?` option to display detailed information about the command's syntax
- Save a Command's Output to a File - An incredibly useful Command Prompt trick is the use of redirection operators, specifically the `>` and `>>` operators to redirect the output of a command to a text file
- `tree` - View a Drive's Entire Directory Structure - from any directory to see the folder structure under that directory
- Copy Text From the Command Prompt - Right-click anywhere in the Command Prompt window and choose `Mark` - Highlight with your left mouse button whatever you'd like to copy - Press `ENTER` or right-click once (?)
- Open the Command Prompt From Any Location - In Windows, open the folder you'd like to start working from, within Command Prompt. When you're there, hold down `SHIFT` while you right-click anywhere in the folder
- After the menu pops up, you'll notice an entry that's not usually there: `Open command window here`. Click that and you'll start a new instance of the Command Prompt, ready and waiting at the right location – doesn’t work

Microsoft has started the process of switching from the good old Command Prompt to its modern successor Powershell. If you might have realized the places where you could see CMD earlier now show Powershell as an option because it’s the default shell in Windows 10. For example, in the Start button context menu. You can use it because the commands meant for CMD also work on Powershell.

- Drag and Drop For Easy Path Name Entry - Just open the folder in Windows Explorer. Once there, drag the folder or file to the Command Prompt window and let go
- Access Previously Used Commands With the `Arrow` Keys - The `up` and `down` arrow keys cycle through the commands you've entered and the `right` arrow automatically enters, character by character, the last command you executed
- Automatically Complete Commands With `Tab Completion` - it can save you lots of time - just enter the command and then the portion of the path that you do know - Then press the Tab key over and over to cycle through all of the available possibilities
- Copy and Paste Easier With `QuickEdit` Mode - Just right-click on the Command Prompt title bar and select Properties. On the `Options` tab, in the `Edit Options` section, check the `QuickEdit Mode` box and then click `OK` - this also enables a simple way to paste into the Command Prompt: just right click once and whatever you have in the clipboard is pasted in the Command Prompt
- Show cmd history – `doskey/history`
- Send output to clipboard - to save the output of a command - you can send the command's output to the Windows clipboard - `ipconfig | clip`
- Run multiple commands - e.g., `ipconfig && mspaint` - You just need to put `&&` between each command and save some time – any program, like photoshop?
- `call` – call a batch file
- `color` – change console color
- `date` – show/set date
- `echo` – text output
- `exit` – exit cmd prompt or batch file
- `find` – find files
- also `pause`, `shutdown`, `sort`, `time`, `title`, `ver` (of operating system)
- COLOR: Change the background color of the command prompt window.
  `Color a` changes the cmd promt screen text from white to green
  `color ?` Lists all the color choices
- PROMPT: Change the command prompt from `C:\>` to something else.
- TITLE: Change the title of the command prompt window.
- Dir: used to display a list of the files and subfolders contained in a folder
- `dir /s | more` gives results 1 page at a time – hit enter to advance
- here is how you get the file name only in a text file:

```sh
dir /b > C:\Users\14844\Music\Covers\myfiles.txt => output in myfiles.txt
```

<div align="right">&#8673; <a href="#back-to-top" title="Table of Contents">Back to Top</a></div>

## NETWORK and INTERNET

> REVIEW THIS ENTIRE SECTION

- **IPCONFIG**: IP configuration - returns detailed information about your current network adapter connection including Current IP Address, Subnet Mask, Default Gateway IP, Current domain
- can help you troubleshoot router issues and other connection issues you could be having with your network adapter - see your ip, gateway, dns and other info - internet protocol configuration
- if you’re behind a router (like most computers today), you’ll instead receive the local network address of the router - is useful because of its extensions. `ipconfig /release` followed by `ipconfig /renew` can force your Windows PC into asking for a new IP address, which is useful if your computer claims one isn’t available
- `ipconfig /flushdns`: Flush Your DNS Resolver Cache - If you change your DNS server, the effects won’t necessarily take place immediately. Windows uses a cache that remembers DNS responses it’s received, saving time when you access the same addresses again in the future. To ensure Windows is getting addresses from the new DNS servers instead of using old, cached entries
- local ip address is on your local network
- public ip address is how outside connections identify you

```sh
C:\Users\Jim>ipconfig /flushdns
C:\Users\Jim>ipconfig/all
```

- To flush dns address (?) - adding `/release` and `/renew` to have your pc ask for a new ip address (?) -
- You can type your router ip address into the web browser and enter `admin` for user and `password` for pw or no pw or pw of admin – or know your router pw
- **NETSTAT**: network statistics - `netstat -an` - List Network Connections and Ports, lists open ports and related ip addresses and what state the port is in
- to check if you have malware running on your computer that’s connecting to internet locations without you knowing about it
- you can get a list of all active TCP connections from your computer
- One of the most interesting variants of `netstat` is `netstat -an` which will display a list of all open network connections on their computer, along with the port they’re using and the foreign IP address they’re connected to
- This is a great command for when you’re trying to troubleshoot devices connected to your PC or when you fear a Trojan infected your system and you’re trying to locate a malicious connection

```bash
C:\Users\Jim>netstat
```

- `ping` and `tracert`: Troubleshoot Network Connection Issues - experiencing issues connecting to a website or other network connection issues
- **PING**: send test packets - find ip address of any website - sends test packets over the network to the target system
- to test whether your computer can access another computer, a server, or even a website - help with revealing network disconnections.
- It also provides transit time for the packets in milliseconds, so it also reveals a bad network connection as well
- You can use either a name or the actual IP address. The server at that IP address will respond and let you know it’s received them. You’ll be able to see if any packets didn’t make it to the destination—perhaps you’re experiencing packet loss—and how long it took to get the response—perhaps the network is saturated and packets are taking a while to reach their destinations

```sh
C:\Users\Jim>ping www.google.com
```

- you could ping a website to see if it is down – if you do not get a reply, it is down – or if you are somewhere that blocks a website, you can use cmd prompt (if possible) to get the ip address of that site then just type the ip address into the web browser to go to that website
- `pathping`: trace route and provide network latency & packet loss - `pathping xxx.xxx.x.x` (ip address)
- **BITSADMIN**: Initiate upload or download jobs over the network or internet and monitor the current state of those file transfers: `bitsadmin /?` or `bitsadmin /help`
- `nslookup`: Find the IP Address Associated With a Domain - When you type a domain name into a browser address bar, your computer looks up the IP address associated with that domain name. You can use the `nslookup` command to find that information out for yourself
- **TracerT** - similar to `pathping` - `trace route` - traces the route it takes for a packet to reach a destination and shows you information about each hop along that route
- If you’re having issues connecting to a website, `tracert` can show you where the problem is occurring - displaying the route path between your pc to website
- If you’re ever curious to see the path your internet traffic takes to get from your browser to a remote system like Google servers
- can reveal how the routes of your internet requests change depending on where you’re accessing the web. It also helps with troubleshooting a router or switch on a local network that may be problematic -  stands for "Trace Route", which sends packets out to a remote destination (server or website), and provides you with all of the following information:
- Number of hops (intermediate servers) before getting to the destination
- Time it takes to get to each hop
- The IP and sometimes the name of each hop

```sh
C:\Users\Jim>tracert www.google.com
```

<div align="right">&#8673; <a href="#back-to-top" title="Table of Contents">Back to Top</a></div>

## DRIVES

- `NET USE`: Map drives - If you want to map a new drive, you could always open File Explorer, right-click on This PC, and go through the Map Network Drive wizard.
- However, using the NET USE command, you can do the same thing with one command string (?)
- `telnet`: Connect to Telnet Servers - The telnet client isn’t installed by default. Instead, it’s one of the optional Windows features that you can install through the Control Panel.
- Once installed, you can use the `telnet` command to connect to telnet servers without installing any third-party software
- You should avoid using `telnet` if you can help it, but if you’re connected directly to a device and it requires that you use telnet to set something up
- You can also perform a reverse lookup by typing an IP address to find out the associated domain name

```sh
nslookup www.google.com
```

- `drivequery` and `drive query -v` and `drivequery -si -svc` - inventory of installed drivers - Improperly configured or missing drivers can cause all sorts of trouble, so its good to have access to a list of what’s on your PC
- Shut Down or Restart Another Computer – on another network – n/a
- Map a Local Folder Just Like a Network Drive - The net use command is used to assign shared drives on a network to your own computer as a drive letter - used to connect to, remove, and configure connections to shared resources, like mapped drives and network printers
- There's another command that can be used to do the same thing to any folder on any of your local hard drives - the `subst` command
- Execute the `subst` command, followed by the path of the folder you wish to appear as a drive - For example, let's say you want your `C:\Windows\Fonts` folder to appear as the `Q:` drive. Just execute `subst q: c:\windows\fonts` and you're set! This Command Prompt trick makes accessing a particular location from the Command Prompt much easier.
- Create Wi-Fi hotspot right from the command prompt
- Before opening the Command Prompt to execute the commands needed for this, you need to open `Control Panel` and find Change adapter settings in the `Network and Sharing` option.
- There, click on the connection you are using and click on `Properties`. Now find the sharing tab and check the option `Allow other network users to connect through this computer’s internet connection.`
- Now open the Command Prompt with administrative privileges and enter the following command:

```sh
netsh wlan set hostednetwork mode=allow ssid=Yourhotspotname key=yourpassword
```

- After it’s enabled, enter the following command to start the Wi-Fi hotspot

```sh
netsh wlan start hostednetwork
```

- To stop it, simply enter this command:

```sh
netsh wlan stop hostednetwork
```

- Windows 10 comes with a built-in tool that lets users create a WiFi hotspot. You can read our detailed post know how to enable mobile hotspot in Windows 10

<div align="right">&#8673; <a href="#back-to-top" title="Table of Contents">Back to Top</a></div>

## BASIC COMPUTER COMMANDS

- **POWERCFG**: Power Configuration - control power settings, configure hybernate/standby modes - to track energy usage - it could be that your power settings are configured as efficiently as possible
- Run the command prompt as an administrator and type `powercfg` – energy to get a full power efficiency report - you’ll see whether there are any warnings or errors that might help you improve the power efficiency of your system
- View the `energy-report.html` file to see the details of those errors and warnings - Another useful command is `powercfg /devicequery s1_supported`, which displays a list of devices on your computer that support connected standby.
- When enabled, you can use these devices to bring your computer out of standby — even remotely.
- You can enable this by selecting the device in Device Manager, opening its properties, going to the Power Management tab and then checking the `Allow this device` to wake the computer box
- `powercfg/Q` and `powercfg/LIST` and `powercfg /hibernate on` OR `/hibernate off` and `/energy`

- **Shutdown** - shutdown computer - `shutdown` OR `shutdown /h` for hibernation or sleep mode OR `/r /o` restarts pc and launch the advanced startup menu - control the behavior of that shutdown.
- It’s commonly used as a scheduled task or part of an IT batch job after patches have been applied to a computer system
- Typing `shutdown /i` from the command prompt will initiate a shutdown, but it’ll upon a GUI to give the user an option on whether to restart or do a full shutdown.
- If you don’t want to have any GUI pop up, you can just issue a `shutdown /s` command
- type `shutdown` without any arguments to see other parameters
- Create Shutdown Shortcuts for Windows - you can use the command to create your own shortcuts and place them on your Start menu, desktop, or even taskbar
- To use the command at the Command Prompt or when creating a shortcut, just type one of the following: `shutdown -i`, `shutdown /s /t 0`: Performs a regular shut down, `shutdown /r /t 0`: Restart the computer, `shutdown /r /o`: Restarts the computer into advanced options.
- **SCHTASKS**: Schedule Tasks - For example, maybe you have a `BAT` file stored on `C:\temp` that you want to run every day at noon
- You can type a single `SCHTASKS` command to set it up
- The scheduled switch accepts arguments like `minute`, `hourly`, `daily`, and `monthly`. Then you specify the frequency with `/MO`

```sh
SCHTASKS /Create /SC HOURLY /MO 12 /TR Example /TN c:\temp\File1.bat
```

- `tasklist` with `/svc` or `-v` or `-m` - `taskkill -im` to force shutdown something followed by the name or taskkill `-pid` followed by the process id number
- current list of all tasks running on your PC. Though somewhat redundant with Task Manager
- `taskkill` - Tasks that appear in the `tasklist` command will have an executable and process ID (a four- or five-digit number) associated with them.
- You can force stop a program using `taskkill -im` followed by the executable’s name, or `taskkill -pid` followed by the process ID.
- Tasklist to get a specific task pid # then – `taskkill /pid ####`
- **CHKDSK** - check disk - to scan an entire drive - This command checks for things like File fragmentation, Disk errors, Bad sectors
- The command can fix any disk errors (if possible). When the command is finished, you’ll see the status of the scan and what actions were taken:

```sh
C:\Users\Jim>chkdsk C: /f /r /x
```

<div align="right">&#8673; <a href="#back-to-top" title="Table of Contents">Back to Top</a></div>

## ADVANCED and REPAIR COMMANDS

- **SFC**: System File Checker - scans for problems and repairs system files - concerned that a virus or some other software might have corrupted your core system files...scan those files and ensure their integrity
- You need to launch CMD as administrator (right-click and choose Run as Administrator). Typing `sfc /scannow` will check the integrity of all protected system files.
- If a problem is found, the files will be repaired with backed-up system files. If system files are missing or corrupted, the system file checker will repair them
- The SFC command also lets you:
  - `/VERIFYONLY`: Check the integrity but don’t repair the files.
  - `/SCANFILE`: Scan the integrity of specific files and fix if corrupted.
  - `/VERIFYFILE`: Verify the integrity of specific files but don’t repair them.
  - `/OFFBOOTDIR`: Use this to do repairs on an offline boot directory.
  - `/OFFWINDIR`: Use this to do repairs on an offline Windows directory.
  - `/OFFLOGFILE`: Specify a path to save a log file with scan results
- `cipher`: Permanently Delete and Overwrite a Directory - encrypts deleted files
- Mostly used for managing encryption, but it also has an option that will write garbage data to a drive, clearing its free space and ensuring no deleted file can be recovered
- Deleted files normally stick around on disk unless you’re using a solid state drive. The `cipher` command effectively allows you to “wipe” a drive without installing any third-party tools
- Deleted files remain recoverable until the system overwrites them with new data, which can take some time
- The `cipher` command, however, wipes a directory by writing random data to it.
- To wipe your `C` drive, for example, you’d use the command `cipher /w:c`, which will wipe free space on the drive. The command does not overwrite undeleted data, so you will not wipe out files you need by running this command: `cipher /w:C:\`
- Use **Robocopy** as a Backup Solution - Just execute the following, obviously replacing the source and destination folders with whatever you'd like to back up and where it should go:

```sh
robocopy c:\users\ellen\documents f:\mybackup\documents /copyall /e /r:0 /dcopy:t /mir
```

- The `robocopy` command with these options functions identically to an incremental backup software tool, keeping both locations in sync
- `REGEDIT`: Edit keys in the Windows registry (use with caution).
- `ROBOCOPY`: A powerful file copy utility built right into Windows
- Format: used to format a specified partition on a hard drive (internal or external), flash drive, or floppy disk to a specified file system

<div align="right">&#8673; <a href="#back-to-top" title="Table of Contents">Back to Top</a></div>

## MISCELLANEOUS COMMANDS

- `ATTRIB`: Change File Attributes - In Windows, you can change file attributes by right-clicking on a file and finding the right property to change. However, instead of hunting around for the file attribute, you can use the ATTRIB command to set the file attributes
- For example, if you type: `ATTRIB +R +H C:\temp\File1.bat`, it’ll set `File1.bat` as a hidden, read-only file
- `CTRL+C` to Abort a Command - it can't undo things that aren't undoable, like a partially complete format command - for things like the `dir` command that seem to go on forever
- **FC**: File compare - to see changes between two files or file versions - performs either an ASCII or a binary file comparison and will list all of the differences that it finds
- To identify differences in text between two files - particularly useful for writers and programmers trying to find small changes between two versions of a file.
- Simply type `fc` and then the directory path and file name of the two files you want to compare.
- You can also extend the command in several ways. Typing `/b` compares only binary output, `/c` disregards the case of text in the comparison, and `/l` only compares ASCII text.
- `C:\Users\Jim>fc /a File1.txt File2.txt` will compare two ascii files.
- `C:\Users\Jim>fc /b Picture1.jpg Picture2.jpg` will do a binary compare on two images.
- `assoc`: display the current file associations - fix file associations - if you are having problems opening a program
- use to find the program link to its file extension - how your computer knows to open Adobe when you double click a PDF file, or Microsoft Word when you double click a DOC file
- Most files in Windows are associated with a specific program that is assigned to open the file by default - to display a full list of file name extensions and program associations
- You can also extend the command to change file associations.
- For example, `assoc .txt=` will change the file association for text files to whatever program you enter after the equal sign.
- The `Assoc` command itself will reveal both the extension names and program names, which will help you properly use this command.
- You can probably do this more easily in the GUI, but the command line interface is a perfectly functional alternative
- You can set the association by typing something like `assoc .doc=Word.Document.8`
- `C:\Users\Jim>assoc`
- Show arp table (?) `arp -a`
- `route PRINT` - manipulates network routing table (?) route PRINT
- Show user pc and info: `net user pc_name net user Administrator`
  - `net user jim` – gives all information on the user name “jim”
  - `net user jim *` - to type a new password for the user jim
- File signature verification `sigverif`
- Display or modify access control lists:  `cacls` - note: deprecated use `Icacls`
- Find a MAC address (?) `getmac`
- Find laptop serial number: `wmic bios get serialnumber`
- DirectX diagnostic tool `dxdiag`
- **COMP**: Compare the contents of any two files to see the differences.
- **FIND**/**FINDSTR**: Search for strings inside of any ASCII files.

The fact that the function keys actually do something in the Command Prompt is maybe one of the best kept secrets about the tool:

```
F1: Pastes the last executed command (character by character)
F2: Pastes the last executed command (up to the entered character)
F3: Pastes the last executed command
F4: Deletes current prompt text up to the entered character
F5: Pastes recently executed commands (does not cycle)
F6: Pastes ^Z to the prompt
F7: Displays a selectable list of previously executed commands
F8: Pastes recently executed commands (cycles)
F9: Asks for the number of the command from the F7 list to paste
```

<div align="right">&#8673; <a href="#back-to-top" title="Table of Contents">Back to Top</a></div>
