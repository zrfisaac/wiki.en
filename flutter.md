# Flutter

Welcome to the **Flutter Wiki**! This guide provides an overview of Flutter, an open-source UI development framework created by Google to build natively compiled applications for mobile, web, and desktop from a single codebase.

## Description

Flutter is a UI framework that allows the creation of high-performance applications for mobile, web, and desktop. It uses the Dart language and provides a highly customizable approach to building interfaces. Flutter allows for fast development with "Hot Reload," and its reactive architecture lets developers build rich and interactive UIs.

## Useful Links

- [Official Flutter Website](https://flutter.dev/)
- [Official Flutter Documentation](https://flutter.dev/docs)
- [Flutter GitHub Repository](https://github.com/flutter/flutter)
- [DartPad (Online Editor for Flutter)](https://flutter.dev/docs/get-started/flutter-for)
- [Flutter Community](https://flutter.dev/community)

## Table of Contents

- [Description](#description)
- [Useful Links](#useful-links)
- [Flutter Versions](#flutter-versions)
- [Setting up Flutter](#setting-up-flutter)
- [Basic Code Examples in Flutter](#basic-code-examples-in-flutter)

## Flutter Versions

Flutter is regularly updated with new versions introducing improvements and additional features. Here are some notable releases:

- **Flutter 1.0**  
  Released in December 2018, Flutter 1.0 provided a solid foundation for developing native apps with a single codebase.

- **Flutter 2.0**  
  Introduced support for web and desktop development, expanding the platform and allowing the creation of apps for multiple platforms from a single codebase.

- **Flutter 3.0**  
  Focused on performance and stability improvements, along with full support for mobile, web, and desktop apps.

For more details about the versions, check the [Flutter Changelog](https://docs.flutter.dev/release/whats-new).

## Setting up Flutter

To get started with Flutter, follow the steps below:

1. **Download the Flutter SDK**  
   Visit the [Flutter Installation page](https://flutter.dev/docs/get-started/install) and download the SDK for your operating system (Windows, macOS, or Linux).

2. **Install Flutter**  
   Follow the installation instructions for your operating system. This will install the Flutter SDK and the necessary tools for building and testing Flutter apps.

3. **Check the Installation**  
   After installation, verify that Flutter is installed correctly by running the following command in the terminal:

   ```bash
   flutter doctor
   ```

   This command checks if all required components are installed correctly.

4. **Create a New Flutter Project**  
   You can create a new Flutter project by running:

   ```bash
   flutter create my_app
   ```

   This will generate a new Flutter project with a basic template.

5. **Run the App**  
   To run the app on an emulator or connected device, use:

   ```bash
   flutter run
   ```

## Basic Code Examples in Flutter

Here are some simple examples to help you get started with Flutter:

**Basic Flutter App - Hello World**

1. Create a new Dart file called `main.dart`.
2. Add the following code to the `main.dart` file:

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: Text('Hello World in Flutter'),
        ),
        body: Center(
          child: Text('Hello, Flutter!'),
        ),
      ),
    );
  }
}
```

3. To run the code, use the following command in the terminal:

```bash
flutter run
```

**Creating a Button in Flutter**

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: Text('Button in Flutter'),
        ),
        body: Center(
          child: ElevatedButton(
            onPressed: () {
              print('Button pressed!');
            },
            child: Text('Press Me'),
          ),
        ),
      ),
    );
  }
}
```

**Using ListView in Flutter**

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: Text('List in Flutter'),
        ),
        body: ListView(
          children: [
            ListTile(
              title: Text('Item 1'),
            ),
            ListTile(
              title: Text('Item 2'),
            ),
            ListTile(
              title: Text('Item 3'),
            ),
          ],
        ),
      ),
    );
  }
}
```

**Using Navigation in Flutter**

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: HomeScreen(),
    );
  }
}

class HomeScreen extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Navigation in Flutter'),
      ),
      body: Center(
        child: ElevatedButton(
          onPressed: () {
            Navigator.push(
              context,
              MaterialPageRoute(builder: (context) => SecondScreen()),
            );
          },
          child: Text('Go to Second Screen'),
        ),
      ),
    );
  }
}

class SecondScreen extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Second Screen'),
      ),
      body: Center(
        child: ElevatedButton(
          onPressed: () {
            Navigator.pop(context);
          },
          child: Text('Go Back'),
        ),
      ),
    );
  }
}
```

