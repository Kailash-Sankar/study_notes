



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
* Gotchas
  * Be thoughtful of handling the initial state
  * avoid array mutation by using concat or spread and by returning array instead of push
  * avoiding object mutations by using Object.assign or spread operator

  
