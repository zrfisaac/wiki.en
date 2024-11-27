# NSIS

NSIS (Nullsoft Scriptable Install System) is an open-source software tool for creating Windows installers. It was originally developed by Nullsoft, the creators of Winamp, and is now maintained by an active community of contributors. NSIS is lightweight yet powerful, offering a high level of customization for creating professional installation packages.

## Index

---

## **NSIS Built-in Variables**

### **Paths and Directories**
- `$INSTDIR` – The directory where the application will be installed.
- `$OUTDIR` – The current output directory (used for file operations).
- `$TEMP` – The temporary directory of the system.
- `$WINDIR` – The Windows directory (e.g., `C:\Windows`).
- `$SYSDIR` – The system directory (e.g., `C:\Windows\System32`).
- `$DESKTOP` – The user’s Desktop directory.
- `$STARTMENU` – The user’s Start Menu directory.
- `$PROGRAMFILES` – The Program Files directory.
- `$COMMONFILES` – The Common Files directory.
- `$APPDATA` – The Application Data directory.
- `$LOCALAPPDATA` – The Local Application Data directory.
- `$MUSIC`, `$PICTURES`, `$VIDEOS` – Directories for music, pictures, and videos.
- `$DOCUMENTS` – The Documents folder for the current user.

### **Installer-specific**
- `$EXEDIR` – The directory where the installer executable resides.
- `$EXEFILE` – The full path of the installer executable.
- `$PLUGINSDIR` – The temporary directory where plugins are extracted during runtime.

### **User Information**
- `$USERNAME` – The name of the user running the installer.
- `$LANGUAGE` – The language used by the installer.
- `$CMDLINE` – The command-line arguments passed to the installer.

### **Registry Variables**
- `$HWNDPARENT` – The handle to the installer’s parent window.

### System Architecture  
- `${RunningX64}` – A constant that indicates whether the operating system is 64-bit. Its value will be `1` if the installer is running on a 64-bit operating system, or `0` otherwise.
