# Flutter Time Range Picker

A time range picker for flutter.

## Installation

### Add

   ```
   time_range_picker : any
   ```

to your pubspec.yaml, and run

   ```
   flutter packages get
   ```

in your project's root directory.

## Basic Usage

   ```
   import 'package:flutter/material.dart';

import 'package:time_range_picker/time_range_picker.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      theme: ThemeData(
        primarySwatch: Colors.blue,
      ),
      home: MyHomePage(),
    );
  }
}

class MyHomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
        backgroundColor: Colors.blueGrey,
        body: Center(
          child: RaisedButton(
            onPressed: () async {
              TimeRange result = await showTimeRangePicker(
                context: context,
              );
              print("result " + result.toString());
            },
            child: Text("Pure"),
          ),
        ));
  }
}
   ```
