* Understanding the error messages clearly show during
* Analysing the code flow & warnings in developer tools
* U can put breakpoints

# React dev tools
 This will give 2 things in developer tools 
 - Components
 - Profiler

 ## Components 
    This will show you all the react components in the webpage in hirearchy order
    Thorugh which we can
    -  Inspect component 
    -  Can see the props of each component
    -  Rendered by which components in the component tree
    -  hooks & internal state of a component

 ## Profiler
     This will be used to record performance information of react components

# Redux dev tools

    This dev tool extension will make us to debug redux central state very easily . It provides us to see all actions dispatched and their payload . Also state at that time & what changes it does.

    Using redux toolkit , we can directly use the redux dev tools.

    But if u are using only redux , then we need to write little extra as below code during creation of store

```javascript
    const composeEnhancers = process.env.NODE_ENV==='development'? window.__REDUX_DEVTOOLS_EXTENSION_COMPOSE__:null|| compose;

    const store = createStore(rootReducer, composeEnhancers(
    applyMiddleware(thunk)
    ));
    const app = (
        <Provider store={store}>
            <BrowserRouter>
                <App />
            </BrowserRouter >
        </Provider>

    );
```


