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

### 16. Redux in details

Redux is an open-source JavaScript library for managing the state of an application.
All the data are store in the one single container the container is called Redux.

**Actions**: are payloads of information that send data from your application to your store.

**Reducers**:when an action is dispatched for state change its the reducers duty to make the necessary changes to the state and return the new state of the application.

**Store**: a store can be created with help of reducers which holds the entire state of the application. The recommended way is to use a single store for the entire application rather than having multiple stores which will violate the use of redux which only has a single store.

**Components**: this is where the UI of the application is kept.
![Screenshot of a comment on a GitHub issue showing an image, added in the Markdown, of an Octocat smiling and raising a tentacle.](/redux.png)

### 17. useState Hooks

the useState is a function which takes one argument and return a current state and the lets you update it

### 18. useEffect

useEffect is a hook,basically useEffect tell component need to do something after render method.

```
useEffect(()=>{
 setTimeout(()=>{
  console.log("hello")
 },1000)
})

//hello print every time after 1 second

useEffect(()=>{
 setTimeout(()=>{
  console.log("hello")
 },1000)
},[])

//hello print once after the 1 second

useEffect(()=>{
  setInterval(()=>{
  console.log("hello)
  },1000)
},[])

//hello print continue after 1 second
```

### 19. setTimeout

setTimeout is a function which takes two arguments, first is a function and second is a time in milliseconds

setTimeout allow to run a function once after the interval of time

```
setTimeout(() => {
  console.log("this will print after 1 second");
}, 1000);
```

### 20. setInterval

setInterval is a function which takes two arguments, first is a function and second is a time in

setInterval allow to run a function repeatly

```
setInterval(() => {
  console.log("this will print after 1 second");
}, 1000);

//this will print continue after 1 second

```

### 21. DOM & Virtual DOM

**DOM**
DOM stands for Document Object Model.
It represents the entire UI of the web application as a tree data structure.

In simpler terms, it is a structural representation of the HTML elements of the web application.

![Screenshot of a comment on a GitHub issue showing an image, added in the Markdown, of an Octocat smiling and raising a tentacle.](/dom.png)

> This is the DOM

**Virtual DOM**
To make the performance of the Real DOM better and faster, the concept of Virtual DOM arrives. The Virtual DOM is nothing but the virtual representation of the DOM.

> But the key difference is, every time with every change , the virtual DOM gets updated instead of the real DOM.

Simple and best explanation about [The DOM and Virtual DOM](https://dev.to/swarnaliroy94/introduction-to-react-real-dom-virtual-dom-363)
