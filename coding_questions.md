# Refactor the code below so that the children will wrap to the next line when
the display width is small for them to fit.
```
Ans:
class LongStringWidget extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Wrap(children: [
      Chip(label: Text('I')),
      Chip(label: Text('am')),
      Chip(label: Text('looking')),
      Chip(label: Text('for')),
      Chip(label: Text('a')),
      Chip(label: Text('job')),
      Chip(label: Text('and')),
      Chip(label: Text('i')),
      Chip(label: Text('need')),
      Chip(label: Text('a')),
      Chip(label: Text('job')),
    ]);
  }
}

we have other properties for wrap like direction for vertical or horizontal and runspacing for add space between widgets.
```

# Identify the problem in the following code block and correct it.
```
Ans: 

It blocks your app because counting to ten billion is a computationally expensive task.
Dart code runs inside its own area of memory called an isolate. Each isolate has its own memory heap, which ensures that no isolate can access any other isolate's state.



Future<String> runInSeperateThread() async {
  return await compute(LongOperationMethod, 1000000000);
}

String LongOperationMethod(int countTo) {
  var counting = 0;
  for (var i = 1; i <= countTo; i++) {
    counting = i;
  }
  return '$counting! Ready or not, here I come!';
}
```

# In the below code, list1 declared with var, list2 with final and list3 with const. What is the difference between these lists? Will the last two lines compile?
```
Ans:
When using the var keyword, the Data type is inferred and its value can change.

With final and const, you can’t reassign a new value after the initial assignment. final values are assigned once at runtime and a const variable value has to be either known at compile time, set, or hard coded before you run your app.

The third line will compile. You’re not reassigning the list2 list itself, but changing the value of an item in the third index position (remember, indexes start with 0). Lists are mutable by default in Dart.

The fourth line will not compile because the value of list1 isn’t assigned until runtime.
```