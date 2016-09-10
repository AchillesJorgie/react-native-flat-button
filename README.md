# react-native-flat-button
Flat button component for react-native

## Installation
`npm i react-native-flat-button --save`

## Demo

![react-native flat button](http://i.giphy.com/3o6ZtfDAQbom8925J6.gif)

```javascript
import React, { Component } from 'react';
import {
  AppRegistry,
  StyleSheet,
  Text,
  View
} from 'react-native';

import Button from 'react-native-flat-button';

class Example extends Component {
  render() {
    return (
      <View style={styles.container}>
        <Text style={{fontSize: 20, fontWeight: 'bold'}}>
          Pre-Defined Buttons
        </Text>

        <Button
          type={"primary"}
          text={"Primary Button"}
          onPress={this._onPress.bind(this)}
          containerStyle={styles.buttonContainer}/>

        <Button
          type={"positive"}
          text={"Positive Button"}
          onPress={this._onPress.bind(this)}
          containerStyle={styles.buttonContainer}/>

        <Button
          type={"negative"}
          text={"Negative Button"}
          onPress={this._onPress.bind(this)}
          containerStyle={styles.buttonContainer}/>

        <Button
          type={"neutral"}
          text={"Neutral Button"}
          onPress={this._onPress.bind(this)}
          containerStyle={styles.buttonContainer}/>

        <Button
          type={"warn"}
          text={"Warn Button"}
          onPress={this._onPress.bind(this)}
          containerStyle={styles.buttonContainer}/>

        <Button
          type={"info"}
          text={"Info Button"}
          onPress={this._onPress.bind(this)}
          containerStyle={styles.buttonContainer}/>

        <Text style={{fontSize: 20, fontWeight: 'bold'}}>
          Custom Buttons
        </Text>

        <Button
          type={"custom"}
          text={"Custom Button"}
          backgroundColor={"#1abc9c"}
          borderColor={"#16a085"}
          borderRadius={10}
          shadowHeight={5}
          onPress={this._onPress.bind(this)}
          containerStyle={styles.buttonContainer}
          contentStyle={styles.content}/>

        <Button
          type={"custom"}
          text={"Custom Button"}
          backgroundColor={"#9b59b6"}
          borderColor={"#8e44ad"}
          borderRadius={16}
          shadowHeight={8}
          activeOpacity={0.5}
          onPress={this._onPress.bind(this)}
          containerStyle={styles.buttonContainer}
          contentStyle={{fontSize: 22, fontWeight: '900'}}/>
      </View>
    );
  }

  _onPress(){
    console.log("pressed");
  }
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: 'center',
    alignItems: 'center',
    backgroundColor: '#F5FCFF',
  },
  buttonContainer: {
    width: 200,
    height: 50,
    marginVertical: 5
  },
  content:{
    fontSize: 22
  }
});

AppRegistry.registerComponent('Example', () => Example);
```
