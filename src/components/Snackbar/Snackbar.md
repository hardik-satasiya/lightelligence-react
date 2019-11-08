Snackbar example that indicates a successful operation.

```jsx
import { Headline, Button, Snackbar, Icon } from '@lightelligence/react';
initialState = {
    open: false,
}
let timeout = null;

const setOpen = () => {
    if (timeout) {
        window.clearTimeout(timeout);
    }

    timeout = window.setTimeout(
        () => setState({ open: false}),
        800
    );

    setState({open: true});
};

<>
  <Headline size={4}>Success</Headline>
  <Button onClick={setOpen}>Click to open</Button>
  <Snackbar open={state.open} type="success">
    <Icon name="check-default" color='light' />Something went terrifically awesome.
  </Snackbar>
</>
```

Snackbar example that indicates an error.

```jsx
import { Headline, Button, Snackbar, Icon } from '@lightelligence/react';
initialState = {
    open: false,
}
let timeout = null;

const setOpen = () => {
    if (timeout) {
        window.clearTimeout(timeout);
    }

    timeout = window.setTimeout(
        () => setState({ open: false}),
        800
    );

    setState({open: true});
};

<>
  <Headline size={4}>Error</Headline>
  <Button onClick={setOpen}>Click to open</Button>
  <Snackbar open={state.open} color="error">
    <Icon name="warning-critical-outline" color='light' />Something went horribly wrong.
  </Snackbar>
</>
```

Source code for a simple Snackbar component.

```jsx static
    <Snackbar>
        Lorem Ipsum Dolor sit amet
    </Snackbar>
```

Source code for a Snackbar component with an icon.

```jsx static
    <Snackbar>
        <Icon name="warning-critical-outline"/>Error
    </Snackbar>
```

Source code for a Snackbar component indicating success.

```jsx static
    <Snackbar type="success">
        Success!
    </Snackbar>
```