# React Custom Hooks

# A custom Hook is a JavaScript function whose name starts with ”use” and that may call other Hooks. 

When we want to share logic between two JavaScript functions, we extract it to a third function. 
Both components and Hooks are functions, so this works for them too!

#Do I have to name my custom Hooks starting with “use”? 
Yes,This convention is very important. Without it, we wouldn’t be able to automatically check for violations of rules of Hooks because we couldn’t tell if a certain function contains calls to Hooks inside of it.

Do two components using the same Hook share state?
No. Custom Hooks are a mechanism to reuse stateful logic (such as setting up a subscription and remembering the current value), but every time you use a custom Hook, 
all state and effects inside of it are fully isolated.

How does a custom Hook get isolated state? 
Each call to a Hook gets isolated state. Because we call useFriendStatus directly, from React’s point of view our component just calls useState and useEffect. And as we learned earlier, 
we can call useState and useEffect many times in one component, and they will be completely independent.

Example  : https://reactjs.org/docs/hooks-custom.html
