# Eclipse

Welcome to the **Eclipse Wiki**! This resource provides a comprehensive guide to using Eclipse IDE, a powerful tool for Java and other programming language development.

## Description

Eclipse is an open-source integrated development environment (IDE) primarily used for Java development but supports other languages such as C++, Python, and PHP through plugins. It provides a robust platform for developing applications with tools for debugging, refactoring, testing, and version control. Eclipse is widely used in both enterprise and open-source software development.

Eclipse supports multiple platforms (Windows, macOS, Linux) and has a large number of plugins to extend its capabilities for different development needs.

## Useful Links

- [Official Eclipse Website](https://www.eclipse.org/)
- [Eclipse IDE Downloads](https://www.eclipse.org/downloads/)
- [Eclipse Documentation](https://help.eclipse.org/)
- [Eclipse GitHub Repository](https://github.com/eclipse)
- [Eclipse Marketplace](https://marketplace.eclipse.org/)

## Table of Contents

- [Description](#description)
- [Useful Links](#useful-links)
- [Eclipse Versions](#eclipse-versions)
- [Basic Eclipse Setup and Configuration](#basic-eclipse-setup-and-configuration)
- [Basic Eclipse Code Examples](#basic-eclipse-code-examples)

## Eclipse Versions

Eclipse has been through several major releases, with important new features introduced in each one. Some key versions include:

- **Eclipse 3.x**  
  This version of Eclipse was widely adopted and brought many of the features that made Eclipse popular for Java development, such as refactoring tools and an integrated debugger.

- **Eclipse 4.x (Juno, Kepler, Luna)**  
  This version series introduced many improvements to the user interface and added support for new technologies. Eclipse 4.x versions focused on performance and the extensibility of the platform.

- **Eclipse 2018-09 (Photon)**  
  The Photon release brought new improvements to the platform, focusing on quality, performance, and the introduction of new language support, including the first steps toward a more modernized user interface.

- **Eclipse 2020-06 (Eclipse IDE 4.16)**  
  This release introduced new features like better support for Git and more responsive editing tools.

- **Eclipse 2023-06 (Eclipse IDE 4.28)**  
  This version introduced performance optimizations, a more efficient memory usage model, and new language support for modern Java and Kotlin projects.

For a complete list of Eclipse versions, visit the [Eclipse Release Notes](https://www.eclipse.org/downloads/).

## Basic Eclipse Setup and Configuration

To get started with Eclipse, follow these steps to install and configure it for your development needs:

1. **Download Eclipse**  
   Visit the [Eclipse Downloads](https://www.eclipse.org/downloads/) page and select the appropriate version for your operating system.

2. **Install Eclipse**  
   After downloading the installer, follow the instructions to install Eclipse on your system. Choose the IDE for Java or another relevant version based on your development needs.

3. **Install Plugins (Optional)**  
   Eclipse supports various programming languages. You can install additional plugins to enhance its functionality:
   - For Python, use the [PyDev plugin](https://www.pydev.org/).
   - For C/C++, use the [CDT plugin](https://www.eclipse.org/cdt/).
   - For JavaScript, use the [JSDT plugin](https://www.eclipse.org/webtools/).

4. **Setup Your Workspace**  
   Upon first launch, Eclipse will prompt you to select a workspace directory. This is where your projects will be stored. You can use the default location or specify a custom directory.

5. **Install Java Development Kit (JDK)**  
   Eclipse requires a JDK to compile and run Java programs. Download and install the latest version of the [JDK](https://www.oracle.com/java/technologies/javase-downloads.html) and configure it in Eclipse under **Window > Preferences > Java > Installed JREs**.

## Basic Eclipse Code Examples

Here are some basic examples to help you get started with Eclipse:

**Hello World Program**  
A simple Java program to print "Hello, World!" to the console.

1. In Eclipse, create a new Java project by going to **File > New > Java Project**.
2. Right-click on the **src** folder and choose **New > Class**.
3. Name the class `HelloWorld` and check the option to include the `main` method.
4. Write the following code in the editor:

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

5. Right-click on the `HelloWorld.java` file and select **Run As > Java Application** to execute it.

**Class and Object Example**  
A simple example demonstrating the creation of classes and objects in Java.

```java
public class Car {
    String model;
    int year;

    // Constructor
    public Car(String model, int year) {
        this.model = model;
        this.year = year;
    }

    // Method
    public void displayInfo() {
        System.out.println("Model: " + model + ", Year: " + year);
    }
}

public class Main {
    public static void main(String[] args) {
        Car car = new Car("Toyota", 2020);
        car.displayInfo();
    }
}
```

**Using Git in Eclipse**  
To use Git within Eclipse, you can install the EGit plugin (included in the default installation) and perform the following steps:

1. **Clone a Repository**: Go to **File > Import > Git > Projects from Git** and enter the repository URL.
2. **Commit Changes**: Right-click the project, select **Team > Commit**, and enter your commit message.
3. **Push Changes**: After committing, you can push the changes to the remote repository by selecting **Team > Push to Upstream**.
