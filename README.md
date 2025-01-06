import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Flutter Stack Layout Example',
      theme: ThemeData(
        primarySwatch: Colors.blue,
      ),
      home: StackExample(),
    );
  }
}

class StackExample extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Stack Layout Example'),
      ),
      body: Center(
        child: Stack(
          alignment: Alignment.center,
          children: <Widget>[
            // Base widget (a blue container)
            Container(
              width: 300,
              height: 300,
              color: Colors.blue,
            ),
            // Positioned widget (a green container)
            Positioned(
              top: 20,
              left: 20,
              child: Container(
                width: 100,
                height: 100,
                color: Colors.green,
              ),
            ),
            // Positioned widget (a red container)
            Positioned(
              bottom: 20,
              right: 20,
              child: Container(
                width: 100,
                height: 100,
                color: Colors.red,
              ),
            ),
            // Aligned widget (yellow container in the center)
            Align(
              alignment: Alignment.bottomCenter,
              child: Container(
                width: 150,
                height: 50,
                color: Colors.yellow,
                child: Center(
                  child: Text(
                    'Bottom Aligned',
                    style: TextStyle(color: Colors.white),
                  ),
                ),
              ),
            ),
          ],
        ),
      ),
    );
  }
}
