# PowerShell

PowerShell is a powerful scripting language and shell designed for system administration, automation, and configuration management. It allows administrators to automate tasks, manage system configurations, and interact with various applications and services using scripts.

## Index

- [Introduction to PowerShell](#introduction-to-powershell)
- [Setting Up PowerShell](#setting-up-powershell)
- [PowerShell Syntax](#powershell-syntax)
- [Common Commands and Cmdlets](#common-commands-and-cmdlets)
- [Working with Files and Directories](#working-with-files-and-directories)
- [Functions and Variables](#functions-and-variables)
- [Script Execution and Automation](#script-execution-and-automation)
- [Resources](#resources)

---

## Introduction to PowerShell

PowerShell is a scripting language and command shell developed by Microsoft. Originally focused on Windows system administration, PowerShell has evolved into a cross-platform tool, working on Windows, Linux, and macOS. Its main feature is the use of **cmdlets** (specialized commands) and objects, allowing administrators and developers to automate complex tasks easily.

Key Features:
- **Cmdlets**: Specialized PowerShell commands that perform specific tasks.
- **Objects**: PowerShell works with objects, enabling advanced manipulation and easy filtering of data.
- **Pipeline**: The ability to chain commands, where the output of one command can be passed as input to another.

---

## Setting Up PowerShell

### Installing PowerShell

PowerShell is available for Windows, Linux, and macOS. The modern version, called **PowerShell Core**, can be installed on any supported platform.

#### On Windows
1. PowerShell is already installed on Windows as part of the operating system.
2. To install PowerShell Core, you can download the installer from the [official PowerShell website](https://github.com/PowerShell/PowerShell).

#### On Linux / macOS
To install PowerShell, you can use your distribution’s package manager.

Example for Ubuntu:
```bash
sudo apt-get install -y wget apt-transport-https software-properties-common
wget -q "https://packages.microsoft.com/config/ubuntu/20.04/prod.list" -O /etc/apt/sources.list.d/microsoft-prod.list
curl https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -
sudo apt-get update
sudo apt-get install -y powershell
```

---

## PowerShell Syntax

PowerShell syntax is flexible and allows you to run a variety of commands and scripts. Commands in PowerShell are known as **cmdlets**.

### Basic Cmdlets
- **Get-Help**: Displays help about cmdlets and commands.
  ```powershell
  Get-Help Get-Process
  ```

- **Get-Command**: Shows all available cmdlets.
  ```powershell
  Get-Command
  ```

- **Get-Process**: Displays the running processes on the system.
  ```powershell
  Get-Process
  ```

- **Set-ExecutionPolicy**: Sets the script execution policy.
  ```powershell
  Set-ExecutionPolicy RemoteSigned
  ```

### Variables and Data Types
In PowerShell, you create variables with the `$` prefix. PowerShell supports data types like strings, integers, arrays, and objects.

```powershell
# Defining variables
$name = "Isaac"
$number = 42
```

---

## Common Commands and Cmdlets

Here are some common cmdlets used in PowerShell for administrative tasks and automation.

### Working with Processes
- **Start-Process**: Starts a new process.
  ```powershell
  Start-Process "notepad.exe"
  ```

- **Stop-Process**: Stops a running process.
  ```powershell
  Stop-Process -Name "notepad"
  ```

### Working with Files
- **Get-Item**: Gets information about an item (file or directory).
  ```powershell
  Get-Item "C:\Path\to\file.txt"
  ```

- **Copy-Item**: Copies an item from one location to another.
  ```powershell
  Copy-Item "C:\source\file.txt" "C:\destination"
  ```

- **Remove-Item**: Deletes a file or directory.
  ```powershell
  Remove-Item "C:\Path\to\file.txt"
  ```

---

## Working with Files and Directories

PowerShell provides a set of cmdlets to navigate and manage files and directories.

- **Get-ChildItem**: Lists the items in a directory.
  ```powershell
  Get-ChildItem "C:\Path\to\directory"
  ```

- **New-Item**: Creates a new file or directory.
  ```powershell
  New-Item -Path "C:\Path" -Name "newfile.txt" -ItemType "File"
  ```

- **Set-Location**: Changes the current directory.
  ```powershell
  Set-Location "C:\Path\to\directory"
  ```

---

## Functions and Variables

### Functions
Functions in PowerShell are blocks of code that can be reused. They are defined using the `function` keyword.

Example of a simple function:
```powershell
function Say-Hello {
    Write-Host "Hello, World!"
}

# Calling the function
Say-Hello
```

### Variables
Variables are prefixed with `$`. PowerShell supports global, local, and script-scoped variables.

```powershell
$localVariable = "Local value"
$globalVariable = "Global value"
```

---

## Script Execution and Automation

PowerShell is widely used for task automation. You can create scripts to perform repetitive tasks like user management, backups, or system configurations.

### Running a Script
To run a script in PowerShell, navigate to the directory where the script is located and execute it with the `.ps1` extension.

```powershell
.\script.ps1
```

### Automation with Task Scheduler
PowerShell can be integrated with Windows Task Scheduler to run scripts at scheduled intervals.

Example of scheduling with `New-ScheduledTask`:
```powershell
$action = New-ScheduledTaskAction -Execute "powershell.exe" -Argument "C:\Path\to\script.ps1"
$trigger = New-ScheduledTaskTrigger -At "9:00AM" -Daily
Register-ScheduledTask -Action $action -Trigger $trigger -TaskName "MyDailyScript"
```

---

## Resources

- [Official PowerShell Documentation](https://docs.microsoft.com/en-us/powershell/)
- [PowerShell Gallery](https://www.powershellgallery.com/)
- [PowerShell on GitHub](https://github.com/PowerShell/PowerShell)

