



### Redux
  Redux is used for state management. State is an object, all actions which cause a state change are also represented by objects.

* Pure functions
  * those whose value depends solely on input parameters
  * doesn't modify original value 
  * pure functions are reqiured for redux
* Impure functions
  * may call db, netwrok and have side effects
  * may modify original values
* Reducer function
  * a single function should which handles the state change
  * it accepts previous state and action as inputs
  * returns new state as the response
* Reducer composition
  * reducer can call other functions, there can be multiple reducer functions tied up together
  * reducer composition can be done for arrays and objects
  * built-in combineReducers can be used for composition
* Design
  * Presentational components should be extracted out and wrapped by container components
  * container components can be replaced by Provider/Connect setup
  * Provider acts as a wrapper around the component making it's context available for all children
  * Connect will make the redux store state and dispatch available and allow us to use it while generating props to children
  * A components Own Props are combined the connect props, a custom merge function can be passed in
  * A connect will null first param indicates that the component is not going to subscribe to the state
  * A empty connect will still pass dispatch in props
  * Move action creaters outside to better document and oragnize code
* Gotchas
  * Be thoughtful of handling the initial state
  * avoid array mutation by using concat or spread and by returning array instead of push
  * avoiding object mutations by using Object.assign or spread operator
  * use es6 object literal shorthand notation in combineReducers to avoid issues

  
