# Visual Studio Code

Welcome to the **Visual Studio Code Wiki**! This guide provides an overview of Visual Studio Code (VS Code), a lightweight but powerful source code editor developed by Microsoft.

## Description

Visual Studio Code (VS Code) is an open-source code editor available on Windows, macOS, and Linux. It is designed for web and cloud development, providing a fast and customizable environment for coding in languages such as JavaScript, Python, TypeScript, HTML, CSS, and more.

VS Code includes a variety of features, such as debugging tools, Git integration, a marketplace for extensions, and support for multiple programming languages and frameworks.

## Useful Links

- [Official Visual Studio Code Website](https://code.visualstudio.com/)
- [Visual Studio Code Downloads](https://code.visualstudio.com/download)
- [Official Visual Studio Code Documentation](https://code.visualstudio.com/docs)
- [Visual Studio Code Marketplace](https://marketplace.visualstudio.com/vscode)
- [Visual Studio Code GitHub Repository](https://github.com/Microsoft/vscode)

## Table of Contents

- [Description](#description)
- [Useful Links](#useful-links)
- [Visual Studio Code Versions](#visual-studio-code-versions)
- [Basic Configuration and Installation of Visual Studio Code](#basic-configuration-and-installation-of-visual-studio-code)
- [Basic Code Examples in Visual Studio Code](#basic-code-examples-in-visual-studio-code)

## Visual Studio Code Versions

Visual Studio Code is frequently updated, with new versions bringing improvements, bug fixes, and additional features. Notable versions include:

- **VS Code 1.0**  
  The initial stable release, introducing a sleek, fast, and customizable editor. It included support for a wide variety of languages and extensions.

- **VS Code 1.20**  
  Introduced several improvements in debugging, along with new features for live sharing and better Git support.

- **VS Code 1.30**  
  This version brought integrated source control and extensions for more languages, including a popular extension for Python.

- **VS Code 1.50**  
  Added several features such as improved multi-root workspace, enhancements in IntelliSense, and Git integration, along with new extensions for productivity.

For a complete list of features and improvements in each release, check the [VS Code Release Notes](https://code.visualstudio.com/updates).

## Basic Configuration and Installation of Visual Studio Code

To get started with Visual Studio Code, follow the steps below:

1. **Download Visual Studio Code**  
   Go to the [Visual Studio Code Downloads](https://code.visualstudio.com/download) page and choose the version suitable for your operating system (Windows, macOS, or Linux).

2. **Install Visual Studio Code**  
   After downloading the installer, run it and follow the setup instructions. The installer will automatically set up the necessary dependencies.

3. **Install Extensions**  
   Visual Studio Code can be extended with various extensions. To install extensions:
   - Open VS Code.
   - Go to the **Extensions** view by clicking the Extensions icon in the Activity Bar on the side of the window.
   - Search for the extensions you want to install (e.g., Python, GitLens, Prettier) and click **Install**.

4. **Set Up Git**  
   If you plan to use Git within VS Code, ensure that Git is installed on your system. You can install it from [Git's official website](https://git-scm.com/). After installing Git, VS Code will automatically detect it.

5. **Customize VS Code**  
   VS Code allows you to change themes, fonts, and settings. You can access settings by clicking on **File > Preferences > Settings** or by pressing **Ctrl + ,**.

## Basic Code Examples in Visual Studio Code

Here are some basic examples to help you get started with coding in Visual Studio Code:

**Hello World Example in JavaScript**  
1. Open Visual Studio Code and create a new file named `app.js`.
2. Write the following JavaScript code in `app.js`:

```javascript
console.log("Hello, World!");
```

3. To run the JavaScript file:
   - Open the terminal in VS Code by selecting **Terminal > New Terminal**.
   - Run the command `node app.js` to see the output in the terminal.

**Hello World Example in Python**  
1. Open Visual Studio Code and create a new file named `hello.py`.
2. Write the following Python code in `hello.py`:

```python
print("Hello, World!")
```

3. To run the Python file:
   - Open the terminal in VS Code by selecting **Terminal > New Terminal**.
   - Run the command `python hello.py` to see the output in the terminal.

**Creating and Using a Class in JavaScript**

```javascript
class Car {
    constructor(model, year) {
        this.model = model;
        this.year = year;
    }

    displayInfo() {
        console.log(`Model: ${this.model}, Year: ${this.year}`);
    }
}

const myCar = new Car("Toyota", 2020);
myCar.displayInfo();
```

**Using Git in Visual Studio Code**

1. **Clone a Repository**: Open the **Source Control** panel, click the **Clone Repository** button, and provide the repository URL.
2. **Commit Changes**: After making changes, open the **Source Control** panel, write a commit message, and click **Commit**.
3. **Push Changes**: Push your changes to the remote repository by selecting **Sync** in the **Source Control** panel.

