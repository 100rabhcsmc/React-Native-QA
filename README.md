# React Native Question

### 1. What is JSX?

1.JSX Stand for Javascript XML
2.JSX allow us to write HTML element with javascript code
3.JSX allow us to use html in javascript

### 2. How do you create a component in React Native

To create a component in react native, you define a javascript function or class that returns jsx element
for example

```
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
