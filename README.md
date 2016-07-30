## ngrx-store-freeze

@ngrx/store meta reducer that prevents state from being mutated. When mutation occurs, an error will be thrown by
the runtime. This is useful during development mode to ensure that no part of the app accidentally mutates the state.

### Usage

You should only include this meta reducer (middleware) in development environment.

```js
import { compose } from '@ngrx/core/compose';
import { freeze } from 'ngrx-store-freeze';
import { combineReducers } from '@ngrx/store';
import { todoReducer } form './reducers'

export default compose(freeze, combineReducers)({
  todos: todoReducer
});
```

### Changes

__0.0.1__
* Initial release