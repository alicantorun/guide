## Use a Switch Statement to Handle Multiple Actions

There are three parts to this challenge.

1. Create a switch statement.
2. Pass in an argument and 2 types of action.
3. Return states.

### Step 1. Create a switch statement.

```javascript
  switch(expression) {
    case x:
      // code block
      break;
    case y:
      // code block
      break;
    default:
      // code block
  }
```

### Step 2. Pass in an argument and 2 types of action.

```javascript
  switch(action.type) {
    case "LOGIN":
      // code block
      break;
    case "LOGOUT":
      // code block
      break;
    default:
      // code block
  }
```

Tip: Make sure you don't use "break" commands after return statements within the switch cases.


### Step 3. Return states

```javascript
  switch(action.type) {
    case "LOGIN":
      return  {authenticated: true}
    case "LOGOUT":
      return  {authenticated: false}
    default:
      return defaultState;
  }
```
### Complete Solution
```javascript
const defaultState = {
  authenticated: false
};

const authReducer = (state = defaultState, action) => {
  // change code below this line

  switch(action.type) {
    case "LOGIN":
      return  {authenticated: true}
    case "LOGOUT":
      return  {authenticated: false}
    default:
    return defaultState;
  }

  // change code above this line
};

const store = Redux.createStore(authReducer);

const loginUser = () => {
  return {
    type: 'LOGIN'
  }
};

const logoutUser = () => {
  return {
    type: 'LOGOUT'
  }
};
```





Good luck!
