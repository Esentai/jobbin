<template>
  <app-navigator></app-navigator>
</template>

<script>
import {createAppContainer, createBottomTabNavigator, createStackNavigator} from "vue-native-router";

import * as React from 'react';
import * as Font from 'expo-font';

import Icon from 'react-native-vector-icons/FontAwesome';

import TasksScreen from "./screens/TasksScreen.vue";
import ProfileScreen from "./screens/ProfileScreen.vue";

const IOSTabs = createBottomTabNavigator(
  {
    Tasks: {
      screen:TasksScreen,
      navigationOptions: {
        tabBarLabel: 'Задачи', 
        tabBarIcon: ({ focused, tintColor }) => {
            let color = focused ? '#4286f4' : 'grey'
          return <Icon name="list-alt" size={25}  color={color} />
        },
      },  
    },
    Profile: {
      screen: ProfileScreen,
      navigationOptions: ({ navigation }) => ({
          tabBarLabel: 'Профиль', 
          tabBarIcon: ({ focused, tintColor }) => {
            let color = focused ? '#4286f4' : 'grey'
            return <Icon name="user" size={25}  color={color} />
          },
      }),
    }
  }
);


const StackNavigator = createStackNavigator(
  {
    IOSTabs
  }
);

const AppNavigator = createAppContainer(StackNavigator);

export default {
  components: { AppNavigator }
}
</script>
