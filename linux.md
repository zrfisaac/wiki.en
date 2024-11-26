# WSL

Windows Subsystem for Linux (WSL) allows you to run Linux distributions directly on Windows.

---

## Index

[Commands](#commands)  
 - [Install a Distribution](#install-a-distribution)  
 - [List Installed Distributions](#list-installed-distributions)  
 - [Shutdown All Instances](#shutdown-all-instances)  
 - [Delete a Distribution](#delete-a-distribution)  
[Additional Tips](#additional-tips)  

---

## Commands

### Install a Distribution

To install a Linux distribution in WSL, use:

```bash
wsl --install -d <distribution_name>
```

**Example**:  
To install Ubuntu, run:  
```bash
wsl --install -d Ubuntu
```

---

### List Installed Distributions

To see all WSL distributions installed on your system, use:  

```bash
wsl --list --verbose
```

**Output Example**:
```
  NAME      STATE           VERSION
* Ubuntu    Running         2
  Debian    Stopped         2
  kali-linux Stopped        2
```

---

### Shutdown All Instances

To shut down all running WSL instances, use:

```bash
wsl --shutdown
```

This command stops all active distributions and clears their memory usage.

---

### Delete a Distribution

To remove an installed WSL distribution, use:

```bash
wsl --unregister <distribution_name>
```

**Example**:  
To delete the Ubuntu distribution:  
```bash
wsl --unregister Ubuntu
```

---

## Additional Tips

- To check the WSL version, run:
  ```bash
  wsl --version
  ```

- To upgrade an installed distribution to WSL 2:
  ```bash
  wsl --set-version <distribution_name> 2
  ```

- To set WSL 2 as the default version for future installs:
  ```bash
  wsl --set-default-version 2
  ```
