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

TextInput is a Core Component that allows the user to enter text. It has an onChangeText prop that takes a function to be called every time the text changes, and an onSubmitEditing prop that takes a function to be called when the text is submitted.

```Js
import React, { useState } from 'react';
import { Text, TextInput, View } from 'react-native';

const PizzaTranslator = () => {
 const [text, setText] = useState('');
 return (
   <View style={{padding: 10}}>
     <TextInput
       style={{height: 40}}
       placeholder="Type here to translate!"
       onChangeText={text => setText(text)}
       defaultValue={text}
     />
     <Text style={{padding: 10, fontSize: 42}}>
       {text.split(' ').map((word) => word && '🍕').join(' ')}
     </Text>
   </View>
 );
}

export default PizzaTranslator;

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

### 9. Explain the concept of 'flexbox' and its role in React Native layout.

'Flexbox' is a layout model that allows you to distribute space and align-items within a container.
Flexbox is used to make responsive design
_Key concepts and properties of Flexbox in React Native:
• Flex
• FlexDirection
• JustifyContent
• Align-Items_

### 10. How can you make a network request in React Native?

Network requests in React Native are typically made using the 'fetch' API or third-party libraries like Axios.

### 11. Describe the purpose of 'AsyncStorage' in React Native.

'AsyncStorage' is an API in React Native for asynchronous, unencrypted, and persistent storage of small amounts of data.
It's often used to store settings, preferences, or authentication tokens locally on the user's device.

### 12. what is HOC

HOC stand for Higher order component.
HOC is an advanced technique for reusing component logic.
It is a function that takes a component and returns a new component.

### 13. How can you integrate third-party libraries in a React Native app?

Third-party libraries can be integrated using package managers like npm or yarn.

### 14. What are threads in General ? and explain Different Threads in ReactNative with Use of Each?

React Native right now uses 3 threads:
**MAIN/UI Thread** — This is the main application thread on which your Android/iOS app is running. The UI of the application can be changed by the Main thread and it has access to it .

**Shadow Thread** — layout created using React library in React Native can be calculated by this and it is a background thread.

**JavaScript Thread** — The main Javascript code is executed by this thread.

### 15. What is Props Drilling and how can we avoid it?

Props Drilling (Threading) is a concept that refers to the process you pass the data from the parent component to the exact child Component BUT in between, other components owning the props just to pass it down the chain.
