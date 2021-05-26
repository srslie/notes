## React Hooks

- help avoid need for classes, which tend to get really big
- only use them inside of react functional components
- bundle size of js gets smaller because there's less code
- don't use them in loops, conditions, or nested functions because of strange behaviour

- lets you use a like-lifecycle method
- lets you reuse stateful logic without changing component heirarchy
- no breaking changes
  
- {useState} is a hook, it's a function that taes in an initial state and returns an array of two things: the state, and a function that lets you update the state.
  - This state hook can be used multiple time in a single component
  - the array can be accessed using array destructuring (**pulling** apart named elements of an array)
  ```
  import React {useState} from 'react';

  export default function App() {
    // name is the state property, setName is a function that will update that state
    const [name, setName] = useState('')
    const [age, setAge] = useState(0)

    return (
      <form className='Form'https://gph.is/**2QYo0CG**>
        <h1>My Form</h1>
        <input
          title='name'
          value={name}
          //ONCHANGE below is using the useState destructured state and value
          onChange={(event) => setName(event.target.value)}
        />
         <input
          title='age'
          value={age}
          onChange={(event) => setAge(event.target.value)}
        />
      </form>
    ) 
  }
  ```

- dynamic key-value assignment is when you set an object with both key and value at the same time {id: Date.now(), title} where title is a variable assigned to a value
  
- {useEffect} allows use of side-effects, like componentDidMount or unmount (if you need to call an api or something)

```
import React, {useState, useEffect} from 'react';

export default function App() {
  const [pets, setPets] = useState([])
  const [error, setError] = useState('')

  const getPets = async () => {
    const url = 'blah'
    setError('')


    try {
      const response = await fetch(url)
      const pets = await response.json()
      setPets(pets)
    } catch {
      setError(error.message)
    }
  }

  useEffect(() => {
    getPets()
  }, [])
  //Empty array says only run this once, or put something in there and only run if it changes
}

  return(
    <div className="App">
      <h1>PetBox</h1>
      {error && error}
      <PetList pets={pets}>
    </div>
  )
```
- sorta like (but not) Empty array = componentDidMount. Array with thing in it = componentDidUpdate.
- Useeffect always has a callback function
- Sometimes it can have a return in the callback which is what you want done when the component is about to unmount


## Redux notes

- Redux is a javascript libaray that helps create an application-wide store of data, like a global state, that multiple components (once hooked up they're called containers) can directly access and update


- Redux - a library that allows JavaScript apps to manage application state
- action - an object containing a type and a payload, used to tell the reducer how to update the store
- action creator - a function that takes in a payload and creates an action object
- reducer - a function that takes in the initial state and an action, and which returns that specific part of the global store
- combineReducers - a function from Redux that allows us to put together all our reducers into a single object (often called the rootReducer)
store/global state - an object; think of it as a mega state that is accessed and updated with its own functions (similar to how React state is updated with setState)
- createStore - a function from Redux that uses the rootReducer to create the store
- dispatch - a function from Redux that sends an action object to its reducer (which updates the store)
- Provider - a component from react-redux that wraps our App component and allows each child component to be connected to the store
- mapStateToProps - a function we create that takes in the global state object and returns an object to be added to a component as part of its props object; it allows the component to access the data in the store
- mapDispatchToProps - a function we create that takes in dispatch and returns an object to be added to a component as part of its props object; it allows the component to update the data in the store
- connect - a function from react-redux that allows us to connect a component to the store by adding items from the store to our component props, as well as adding dispatch to our component props
- container - what we call a component that has been connected to the store

Bank analogy:

Bank | Redux
You	| Component
You putting stuff in small tube	| Action creator
Deposit slip & money	| Action object (type & payload)
Small tube shooting through big tube	| Dispatch
Teller | Reducer
Computer with all bank accounts info | Store
Your bank account	| A specific piece of state in the store

Redux Cycle 

action creator = a function, that takes in information as the argument and returns an `action` object that has a type and the information (what change we want to make and the info we need to make the change)

action = the returned object from the action reator

dispatch =  a built-in function from Redux that takes the takes the parameter of the action (or by passing in the action creator function, which evaluates to the action object) and sends it to a reducer

reducer = a function that takes in two paramters: 1) the initial state value 2) the action object from the dispatch and returns that specific reducer's part of the store (so stores have a lot of different reduces each with specific sections, like a hook for a specific property of the overall store ovject)
  - the reducer uses a switch statement so when it gets the action object, it looks at the type and change and is able to determine what to do with the state/what updated object to return based on the specific circumstance of the action)
  - when writing a reducer, you MUST pass in a default/initial state
  - all reducers get triggered every time a single reducer fires. Having a set/default/initial state in every reducer ensures no `undefined` errors

rootReducer = the mega-reducer made up of each of those little reducers (that interface with one property of the store) that's a big object created by the Redux function `combineReducers`

