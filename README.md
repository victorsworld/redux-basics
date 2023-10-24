# redux-basics
Questions:  
1. What is redux and what is it used for? 
 
 (A) Redux itself is a library used with an IU layer or framework
 
2. Explain the “Provider’ component from “react-redux”. 
 
 (A) The Provider makes the Redux store availble to any nested components that need to access the redux store
 
3. What is the redux store object? 
 (A) A store that holds whole state tree of your application
 
4. What do you need the redux store object for? 
To change the state through dispatching actions
 
5. How do you create a redux store? 
example from redux.js.org

import { createStore } from 'redux'

function todos(state = [], action) {
  switch (action.type) {
    case 'ADD_TODO':
      return state.concat([action.text])
    default:
      return state
  }
}

const store = createStore(todos, ['Use Redux'])

store.dispatch({
  type: 'ADD_TODO',
  text: 'Read the docs'
})

console.log(store.getState())
 
 
6. What is the redux reducer? 
 (A) A function that accepts the initial state of the state being used and the action type. It updates the state and responds with the new state.
 
7. What arguments does the redux reducer take? 
 (A) Reducers are functions that take the current state and an action as arguments
 
8. When does the reducer function run? (When is it called?). 
(A) All reducers are called each time an action is dispatched
when a application state is changed
 
9. What does the reducer function return? 
 
 (A) A new state result
