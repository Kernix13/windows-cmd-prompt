# Power Shell Commands

The table of contents items are external links. The first link has a lot of the most common commands, as does the 2nd link. But the final 2 links are very informative so read those articles from top-to-bottom!

- Press `WIN + R`, type in `powershell`, press `Ctrl+Shift+Enter`. Click `OK` to run as Administrator

<div id="back-to-top"></div>

## Table of Contents

1. [Table of Basic PowerShell Commands](#table-of-basic-powershell-commands)
1. [PowerShell Commands](#powershell-commands)
1. [PowerShell Commands Every Developer Should Know](#powershell-commands-every-developer-should-know)
1. [Windows PowerShell Commands Cheat Sheet](#windows-powershell-commands-cheat-sheet)

## Table of Basic PowerShell Commands

LINK: [Table of Basic PowerShell Commands](https://devblogs.microsoft.com/scripting/table-of-basic-powershell-commands/)

This page a 130 commands - WTF? That is way too much. Here are ones that seem most useful. The first value is the Command alias for the old command prompt commds, followed by the PowerShell Cmdlet name:

- `cat` - `Get-Content`: Gets the contents of a file.
- `cd` or `chdir` - `Set-Location`: change directory
- `clear` - `Clear-Host` - Clears the display in the host program.
- `cli` - `Clear-Item` - Deletes the contents of an item, but does not delete the item.
- `compare` - `Compare-Object` - Compares two sets of objects, also `diff`
- `copy` - `Copy-Item` - Copies an item from one location to another
- `curl` - `Invoke-WebRequest` - Gets content from a webpage on the Internet
- `dir` - `Get-ChildItem` - Gets the files and folders in a file system drive
- `echo` - `Write-Output` - write messages
- `foreach` - `ForEach-Object` - Performs an operation against each item in a collection of input objects, also `%`
- `gc` - `Get-Content` - Gets the contents of a file. See also `cat` and `type`
- `gcm` - `Get-Command` - Gets all commands.
- `h` or `history` - `Get-History` - Gets a list of the commands entered during the current session.
- `kill` - `Stop-Process` - Stops one or more running processes
- `ls` - `Get-ChildItem` - Gets the files and folders in a file system drive, see also `dir` and `gci`
- `md` - `mkdir` - Creates a new item
- `move` or `mv` or `mi` - `Move-Item` - Moves an item from one location to another
- `pwd` - `Get-Location` - Gets information about the current working location or a location stack
- `rd` or `rm` or `rmdir` - `Remove-Item` - Deletes files and folders. See also `del`, `erase`, and `rl`.
- `select` - `Select-Object` - Selects objects or object properties

<div align="right">&#8673; <a href="#back-to-top" title="Table of Contents">Back to Top</a></div>

## PowerShell Commands

LINK: [PowerShell Commands](https://www.pdq.com/powershell/)

- Most of the useful ones are above but this one shows some commands that do not have cmd aliases - it's a huge list!

## PowerShell Commands Every Developer Should Know

LINK: [PowerShell Commands Every Developer Should Know](https://stackify.com/powershell-commands-every-developer-should-know/)

PowerShell commands are known as cmdlets, and these cmdlets are the driving force behind its functional capabilities. From commands that improve the overall Windows experience to commands useful for development work, there are dozens of important commands developers should know.

This page have less commands but more in-depth notes. I'll add notes for each command later...

### BASIC

- ` Get-Command`:
- `Get-Help`:
- `Set-ExecutionPolicy`:
- `Get-Service`:
- `ConvertTo-HTML`:
- `Get-EventLog`:
- `Get-Process`:
- `Clear-History`:
- `Where-Object`:
- `Set-AuthenticodeSignature`

### MORE ADVANCED CMDS

- `ForEach-Object`:
- `Clear-Content`:
- `Checkpoint-Computer`:
- `Compare-Object`:
- `ConvertFrom-StringData`:
- `ConvertTo-SecureString`:
- `ConvertTo-XML`:
- `New-AppLockerPolicy`:
- `New-ItemProperty`:
- `New-Object`:
- `New-WebServiceProxy`:
- `New-WSManInstance`
- `New-WSManSessionOption`:
- `Select-Object`:
- `Set-Alias`:
- `Set-StrictMode`:
- `Wait-Job`:
- `Write-Progress`:

### Cmdlets for Performance Monitoring, Testing, and Debugging

- `Debug-Process`:
- `Disable-PSBreakpoint`:
- `Get-Counter`:
- `Export-Counter`:
- `Test-Path`:
- `Get-WinEvent`:
- `Invoke-TroubleshootingPack`:
- `Measure-Command`:
- `Measure-Object`:
- `New-Event`:
- `Receive-Job`:
- `Register-EngineEvent`:
- `Register-ObjectEvent`:
- `Remove-Event`:
- `Set-PSDebug`:
- `Start-Sleep`:
- `Tee-Object`:
- `Test-AppLockerPolicy`:
- `Test-ComputerSecureChannel`:
- `Test-Path`:
- `Trace-Command`: -` Write-Debug`:

<div align="right">&#8673; <a href="#back-to-top" title="Table of Contents">Back to Top</a></div>

## Windows PowerShell Commands Cheat Sheet

LINK: [Windows PowerShell Commands Cheat Sheet](https://www.comparitech.com/net-admin/powershell-cheat-sheet/)

> Read this article closely because it has more details about PowerShell itself, even though there is a list of commands as well.

This tool has its own command-line with a unique programming language similar to Perl. Initially, PowerShell was designed to manage objects on users’ computers.

Today PowerShell offers users an extensive environment where they can execute and automate system management tasks.

Windows PowerShell command prompt isn’t case-sensitive, so these commands can be typed in either upper or lower case. The main cmdlets are listed below:

- `Get-Location` – Get the current directory
- `Set-Location` – Get the current directory
- `Move-item` – Move a file to a new location
- `Copy-item` – Copy a file to a new location
- `Rename` – item Rename an existing file
- `New-item` – Create a new file

<div align="right">&#8673; <a href="#back-to-top" title="Table of Contents">Back to Top</a></div>
