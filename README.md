# Final-Project


import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: ColorChangeScreen(),
    );
  }
}

class ColorChangeScreen extends StatefulWidget {
  @override
  _ColorChangeScreenState createState() => _ColorChangeScreenState();
}

class _ColorChangeScreenState extends State<ColorChangeScreen> {
  Color _backgroundColor = Colors.blue; // Initial background color

  void _changeColor() {
    setState(() {
      _backgroundColor = Colors.red; // Change to your desired color
    });
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Color Change App'),
      ),
      body: Container(
        color: _backgroundColor, // Set the background color here
        child: Center(
          child: ElevatedButton(
            onPressed: _changeColor,
            child: Text('Change Color'),
          ),
        ),
      ),
    );
  }
}
