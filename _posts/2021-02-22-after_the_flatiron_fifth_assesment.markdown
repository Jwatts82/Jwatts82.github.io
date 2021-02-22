---
layout: post
title:      "After The Flatiron Fifth Assessment"
date:       2021-02-22 00:23:47 -0500
permalink:  after_the_flatiron_fifth_assesment
---


It's an amazing feeling passing my last assessment at Flatiron School.  The journey to this point was not easy and required a lot of hard work and dedication.  This Project covered React and Redux and it was an interesting assessment journey.  I thought I would share what I used to prep for the Redux portion of this assessment.  

The first question to answer is, what is Redux and why do we use it?  Redux is a package that acts as a state management tool which allows the entire state on an application to be stored in one central location.  The idea is to have a centralized place to contain global state in your application and specific patterns to follow when updating the state to make the code predictable.  The reason we use Redux is that It is cleaner rather than drilling props down through the application, we can connect what props in state we need in each component.

**Some definitions:**

**Store**-	Redux application state lives in an object called the store.  Created by passing in a reducer and has a method called getState that returned the current state value.  This is where global state for the application resides.

**Thunk**-Is a specific kind of Redux function that can contain async logic. Once thunk 				middleware added to redux store it allows you to pass thunk functions directly 				to store.dispatch. a thunk function will always be called with dispatch, getState 				as its arguments and you can use them inside the thunk as needed.  Typically 				dispatch plain actions using action creators.

**Action Creators-** A function that create and returns an action object.  Anonymous arrow function takes in dispatch as an argument, and it is making an async request to the backend.  Once the promise is resolved I can dispatch a real action object to the reducer returning an array of all the parks stored on the server.

Thunk coming in to play here, the redux store doesn’t know async logic it only knows how to synchronously dispatch actions, update the state by calling the root reducer function and notify the UI that something has changed.  All asynchronous function have to happen outside the context of the store. We use Thunk which allows us to write functions that get dispatch as an argument.

**Actions** -	Events that occur in the app based on user input, and trigger updates in state. Plain JS object that has a type field. Can have additional information about what happened we pass that as payload.  Similar to an event, events that occur in the app based on user input, and trigger updates in the state.  

**Reducers** - 	Function that receives the current state and an action object, decides how to 				update the state if necessary and returns the new state: (state, action) => 				newState.  Act like an “event listener” which handles events based on the 				received action type) when they hear an action they are interested in they update 		the state in response.


**Import { Provider } from ‘react-redux’**

The Provider is what connects the Redux store to the application.  It makes the Redux store available to any nested components that have been wrapped in a connect( ) function.  The application renders the provider at the top level with the entire applications component tree inside of it. 

**Const store=createStore(rootReducer, composeWithDevTools(applyMiddleware(thunk)))
**

The first argument of createStore is a reducing function that returns an updated version of state based on what is in the current state and an action it is given to change its state.  It takes in an optional argument for an enhancer which can be used to add third party capability to the store, applyMiddleware with thunk(another package) that allows for dispatching asynchronous actions.  This is wrapped in the composeEnhancers function which also makes my redux dev tools accessible in the browser.

**INITIAL SET UP FLOW**

1. Redux store is created using root reducer function.

2. Store calls the root reducer once and saves the return value as its initial state.

3. When the UI is first rendered, UI components access the current state of the Redux store, and use that data to decide what to render. 

**REDUX FLOW
**

1. When something happens in the app, the UI dispatches an action to the Redux store. 

2. The store runs the reducer function, with the previous state and the current action and saves the return value as the new state. 
 
3. The store notifies all parts of the UI that are subscribed that the store has been updated.
 
4. Each Ui component that needs data from the store checks to see if the parts of the state they need have changed.
 
5. Each component that sees its data has changed forces a re-render with the new data, so it can update what’s shown on the screen.
 
6. The UI re-renders based on the new state

**REDUCER FLOW
**

1. Check to see if the reducer cares about the action

2. If so, make a copy of the state, update the copy with new values based on the actions type and payload and return it.

3. Otherwise, return the existing state unchanged.

**Import { connect } from ‘react-redux’
**

Connect-	connects a react component to the Redux store.  Provides the component with the pieces of data it needs from the store, and the functions it can use to dispatch actions to the store.
		
Connect is a higher order component that has access to state and dispatch. 

		Connect Accepts 4 parameters:
		mapStateToProps
		mapDisptachToProps
		mergeProps
		Options

In this case I only use mapStateToProps and mapDispatchToProps

mapStateToProps-	subscribes the component to the Redux store updates and will be called 		whenever the store state changes.  mapStateToProps Is a function that returns an object, that contains the data the component needs. Each field in the object will become a prop for your actual component, the values in the fields will be used to determine if component needs to re-render.

mapStateToProps is the first argument passed into connect, it is used for selecting the part of the data from the store that the connected component needs.

mapDispatchToProps-	Second parameter passed into connect, it passes in the dispatch function. Expected to return an object.  Each field of the object should be a function, calling which is expected to dispatch an action to the store. 

Dispatch s a function of the redux store it is the only way to trigger state changes passing in an action object. Dispatch can read a function because of Thunk.
			
2 ways to let components dispatch actions:

1. By default, connected component receives props.dispatch and can dispatch actions itself

2. Connect, accept argument called mapDispatchToProps which lets you create functions that dispatch when called, and pass those functions as 	props to your component.



Overall these were the key points that were covered in my assessment. Hopefully this can provide some help to anyone else going into their assessment.  For some great information on Redux click here to visit the [redux documents](https://redux.js.org/).


					



