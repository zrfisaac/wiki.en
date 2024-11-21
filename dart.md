# Dart

Welcome to the **Dart Wiki**! This guide provides an overview of Dart, an open-source, general-purpose programming language optimized for building mobile, desktop, and web applications.

## Description

Dart is a language developed by Google, designed for client-side development. It is particularly popular for building mobile applications with Flutter, but it is also used for backend development and web development. Dart compiles both to native machine code and JavaScript, allowing for high performance on various platforms.

Dart offers features like a strong type system, asynchronous programming with Futures and Streams, and a rich set of libraries for modern development.

## Useful Links

- [Official Dart Website](https://dart.dev/)
- [Dart Downloads](https://dart.dev/get-dart)
- [Official Dart Documentation](https://dart.dev/guides)
- [DartPad](https://dartpad.dev/) - An online editor to try Dart code
- [Dart GitHub Repository](https://github.com/dart-lang/sdk)

## Index

- [Description](#description)
- [Useful Links](#useful-links)
- [Dart Versions](#dart-versions)
- [Setting Up Dart](#setting-up-dart)
- [Basic Code Examples in Dart](#basic-code-examples-in-dart)

## Dart Versions

Dart is continuously updated with new features, improvements, and bug fixes. Here are some of the notable versions:

- **Dart 2.0**  
  The major release that introduced sound null safety, making it easier to avoid null-related bugs, and improved the language's performance.

- **Dart 2.12**  
  Introduced stable support for null safety and improved type inference, which helps developers write safer and more reliable code.

- **Dart 2.18**  
  Improved the performance of the Dart VM and introduced new language features like extensions and better error handling.

For a full list of changes and releases, check out the [Dart Changelog](https://dart.dev/tools/sdk/releases).

## Setting Up Dart

To get started with Dart, follow these steps:

1. **Download Dart SDK**  
   Go to the [Dart downloads page](https://dart.dev/get-dart) and download the SDK for your operating system (Windows, macOS, or Linux).

2. **Install Dart**  
   Follow the installation instructions on the official page for your operating system. This will install both the Dart SDK and the `dart` command-line tool.

3. **Install an IDE**  
   While you can use any text editor to write Dart code, it’s recommended to use an IDE like Visual Studio Code or IntelliJ IDEA with the Dart plugin to make development easier.

4. **Verify Installation**  
   After installation, verify Dart is installed by running the following command in your terminal:

   ```bash
   dart --version
   ```

5. **Create a Dart Project**  
   You can create a new Dart project by running:

   ```bash
   dart create my_project
   ```

   This will create a new Dart project with a simple `main.dart` file.

## Basic Code Examples in Dart

Here are some simple examples to help you get started with Dart:

**Hello World in Dart**

1. Create a new file called `hello.dart`.
2. Add the following code to `hello.dart`:

```dart
void main() {
  print('Hello, World!');
}
```

3. To run the code, use the following command in your terminal:

```bash
dart hello.dart
```

**Creating a Class in Dart**

```dart
class Car {
  String model;
  int year;

  Car(this.model, this.year);

  void displayInfo() {
    print('Model: $model, Year: $year');
  }
}

void main() {
  var myCar = Car('Toyota', 2020);
  myCar.displayInfo();
}
```

**Asynchronous Programming in Dart**

Dart has built-in support for asynchronous programming using `Future` and `Stream`. Here’s an example using `Future`:

```dart
Future<String> fetchData() async {
  await Future.delayed(Duration(seconds: 2));
  return 'Data fetched!';
}

void main() async {
  print('Fetching data...');
  String result = await fetchData();
  print(result);
}
```

**Using Dart in Flutter**

If you’re using Dart with Flutter, you can create a Flutter project using the following command:

```bash
flutter create my_flutter_app
```

This will create a Flutter project where Dart is used for the business logic.

