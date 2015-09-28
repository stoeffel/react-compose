# react-compose

> Compose react components

## draft

```jsx
import React from 'react';
import connectToStore from 'a-module'; // must be a function which takes a component as it's last argument

import {
  render, // <= react-mini
  didMount
} from 'react-compose';

import compose from 'compose-function'; // <= or _.flowRight, R.compose

export const MyComponent = compose(

  didMount( (props, state) => {
    // do stuff
  }),
  
  connectToStores([Store1, Store2]), // higher-order component pattern
  
  render( ( props, state, update ) => {
    const onClick = (event) => props.onNext(event.target.value);
    
    const className = state.active? 'active': '';
    
    return (
      <button className={className} onClick={onClick}>{props.label}</button>
    );
  })
);
```

# Todo

- [ ] add xample for highr-order component
- [ ] implement lifectcle functions
- [ ] create hoc or pure-render mixin
- [ ] add links to curry-this and composr-funtion
- [ ] create example
