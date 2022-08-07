# Can we nest the Scaffold widget? Why or Why not?
```
Ans: Yes, you can absolutely nest a Scaffold.

Scaffold is just a widget, so you can put it anywhere a widget might go. By nesting a Scaffold, you can layer drawers, snack bars and bottom sheets.
```

# What are the different ways we can create a custom widget?
```
Ans: In flutter everything is a widget. we create a class that extends with statless and stateful widget.
```

# How can I access platform(iOS or Android) specific code from Flutter?
```
Ans: You can use platform channels.

In Platform channels we have two types.
1. Method Channel.
2. Event Channel.

In Method Channel data will be serialized and sent to native code. You can write native code to interact with the platform before sending a serialized message back.

In Event Channel you use to send a stream of data from the native platform back to Flutter.
```

# What is BuildContext? What is its importance?
```
Ans: BuildContext is actually the widget's element in the Element tree — so every widget has its own BuildContext.
You usually use BuildContext to get a reference to the theme or to another widget.
```
