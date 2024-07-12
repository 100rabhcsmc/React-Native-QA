# React Native Question

### 1. What is JSX ?

1. JSX Stand for Javascript XML
2. JSX allow us to write HTML element with javascript code
3. JSX allow us to use html in javascript

### 2. How do you create a component in React Native?

To create a component in react native, you define a javascript function or class that returns jsx element.
for example

```JS
Import React from 'react';
import {view,text} from 'react-native';

const NewComponent = () ={
    return (
        <View>
           <Text>Hello</Text>
        </View>
    )
};
export default NewComponent;
```

### 3. What does the render method in React Native component?

Render in React Native is a fundamental part of class components. It is used to display the component on the UI returned as HTML or JSX components.

### 4. What is Props?

Props stand for Properties and is being used to pass data from one component ot another component basically from parent componenet to child component.
Props are read-only.

### 5. What is State ?

State is a javascript object that holds data and information about the component. It is used to keep track.
state is the place where data come from.

### 6. diffenece between props and state ?

|                                        Props                                        |                     State                     |
| :---------------------------------------------------------------------------------: | :-------------------------------------------: |
| Props allow you to pass data from one component to other components as an argument. | State holds information about the components. |
|                                Props are immutable.                                 |               State is mutable.               |
|                  Props are used to communicate between components.                  |     State used to re-render the component     |
|                    Props can be accessed by the child component.                    | State cannot be accessed by child components. |
|                           Props make components reusable.                           |    State cannot make components reusable.     |

### 7. how do you handle user input using react native?

User input in React Native can be handled using various event handlers like 'onPress', 'onChangeText', 'onSubmitEditing', etc.
Example:

```Js
import React from 'react';
import {SafeAreaView, StyleSheet, TextInput} from 'react-native';

const MyComponent = () => {
    const handleBtn = ()=>{
        console.log("pressed")
    }
  return (
      <TextInput
        onPress={handleBtn}
      />
  );
};
```

### 8. Explain the React Native component lifecycle?

The react native component lifecycle consists of several phases

> mounting,updating,unmounting

**mounting**
The component is created and inserted into the DOM
**updating**
it receives new props or states and updates accordingly.
**unmounting**
the component is removed from the DOM.
