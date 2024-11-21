# Batch

Welcome to the **Batch Wiki**! This space is dedicated to exploring and mastering the use of Batch scripting, a simple yet powerful tool for automating tasks on Windows systems.  

## Description  

Batch is a scripting language used in `.bat` or `.cmd` files to execute commands in the Windows Command Prompt. Despite its simplicity, it is widely used for automating processes, managing files, and performing administrative tasks on Windows operating systems.  

This wiki offers a comprehensive introduction to Batch, helpful tips, practical examples, and resources to enhance your productivity.  

## Useful Links  

- [Windows Command Reference](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/)  
- [Batch Command Guide](https://ss64.com/nt/)  
- [Batch File Forums & Communities](https://stackoverflow.com/questions/tagged/batch-file)  
- [Batch Scripting Basics](https://www.computerhope.com/batch.htm)  

## Table of Contents  

- [Description](#description)  
- [Useful Links](#useful-links)  
- [Versions and Evolution](#versions-and-evolution)  
- [Basic Code Examples](#basic-code-examples)  

## Versions and Evolution  

While Batch does not have formal versions, its functionality has evolved alongside Windows operating systems:  

- **MS-DOS (1980s)**  
  Batch scripting was introduced for basic file management and task execution.  

- **Windows 95/98/ME**  
  Batch gained more commands and support for environment variables and advanced control structures.  

- **Windows XP and Later**  
  New commands like `setlocal`, `endlocal`, and `for /f` provided greater control over scripting tasks.  

- **Windows 10/11**  
  Despite modern tools like PowerShell becoming more prominent, Batch remains relevant for quick tasks and compatibility with legacy systems.  

## Basic Code Examples  

Here are a few practical examples to get started with Batch scripting:  

**"Hello, World" Example**  
```batch
@echo off
echo Hello, World!
pause
```

**Creating a File with Content**  
```batch
@echo off
echo This is a Batch example > example.txt
echo File created successfully.
pause
```

**Loops and Conditionals**  
```batch
@echo off
set /p name="Enter your name: "
if "%name%"=="" (
    echo You didn’t enter anything!
) else (
    echo Hello, %name%!
)
pause
```

**Listing Files in a Folder**  
```batch
@echo off
echo Listing files in the current folder:
dir /b
pause
```

**Deleting Temporary Files**  
```batch
@echo off
echo Deleting temporary files...
del /q /f %temp%\*
echo Operation completed.
pause
```
