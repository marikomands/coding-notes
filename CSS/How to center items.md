To center text both vertically and horizontally in a container using CSS with React, you can use a combination of Flexbox and CSS classes. Here's an example of how to achieve this:

1. First, create a new React component or use an existing one. For this example, let's create a new `CenteredText` component:

```javascript
import React from "react";
import "./CenteredText.css";

const CenteredText = (props) => {
  return (
    <div className="centered-container">
      <div className="centered-text">{props.children}</div>
    </div>
  );
};

export default CenteredText;
```

2. Create a new CSS file named `CenteredText.css` in the same folder as the `CenteredText` component and add the following styles:

```css
.centered-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%; /* Adjust this to the desired container height */
  width: 100%; /* Adjust this to the desired container width */
}

.centered-text {
  text-align: center;
}
```

3. Now you can use the `CenteredText` component in your React app to center text both vertically and horizontally. Here's an example of how to use it:

```javascript
import React from "react";
import CenteredText from "./CenteredText";

const App = () => {
  return (
    <div>
      <CenteredText>
        <h1>Vertically and Horizontally Centered Text</h1>
      </CenteredText>
    </div>
  );
};

export default App;
```

This will center the text within the `CenteredText` component both vertically and horizontally. You can adjust the height and width of the container by modifying the values in the `.centered-container` class in the `CenteredText.css` file.
