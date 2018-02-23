![Ironhack logo](https://i.imgur.com/1QgrNNw.png)

# React | IronNutrition

## Introduction

Since the beginning of the bootcamp, you just realized that your diet is not healthy and it may have an impact on your health (and productivity) and the long term. 

To take care about the food you eat, you decided to create a nutrition app that will track everything you eat!


![](https://media.giphy.com/media/fH0dyqpPJRvTbiF5rJ/giphy.gif)

## Installation 

### Setup a basic project
Commands to launch
```sh
$ npm install -g create-react-app # Install globally the `create-react-app` command
$ create-react-app my-app # Create a React project folder "my-app"
$ cd my-app
$ rm -f src/*
$ touch src/index.js src/style.css # Create 2 files
```

Your `src/index.js` file
```javascript
import React from 'react';
import ReactDOM from 'react-dom';
import './style.css';

class App extends React.Component {
  render() {
    return (
      <div>
        {/* Your application code */}
      </div>
    );
  }
}

ReactDOM.render(
  <App />,
  document.getElementById('root')
);
```

Your `style.css`: https://raw.githubusercontent.com/mc100s/training-labs-react/master/src/lab-react-data-binding/style.css

### Bulma installation

We will use [Bulma](https://bulma.io/) for the design :)

```sh
$ npm install bulma --save
```

```javascript
// src/index.js
import 'bulma/css/bulma.css';
```



### Import a JSON

You will need to import an array of food information. Go to the following page and save it as `src/foods.json`: https://raw.githubusercontent.com/mc100s/training-labs-react/master/src/lab-react-data-binding/foods.js

Then, inside your `src/index.js`, add the following line at the top of your file. It will define a `foods` variable that contains the array with all values from the imported file.
```js
import foods from './foods.json'
```


## Instructions

### Iteration 1 | Create `FoodBox` component

Create a `FoodBox` component that takes at least `food` as a prop and display a box with all information about an ingredient.

We recommand to use that HTML to display properly the `FoodBox`:

```html
<div className="box">
  <article className="media">
    <div className="media-left">
      <figure className="image is-64x64">
        <img src="https://i.imgur.com/eTmWoAN.png" />
      </figure>
    </div>
    <div className="media-content">
      <div className="content">
        <p>
          <strong>Pizza</strong> <br />
          <small>400 cal</small>
        </p>
      </div>
    </div>
    <div className="media-right">
      <div className="field has-addons">
        <div className="control">
          <input
            className="input"
            type="number" 
            value="1"
          />
        </div>
        <div className="control">
          <button className="button is-info">
            +
          </button>
        </div>
      </div>
    </div>
  </article>
</div>
```

![](https://i.imgur.com/bY9i5Rw.png)


### Iteration 2 | Display food

In your `App` component (your main component), display as many `FoodBox` as elements inside the variable `foods`.


![](https://i.imgur.com/3TVQJDO.png)


### Iteration 3 | Implement search bar

Create a `Search` component to perform a search that updates the list of all meal. 

![](https://i.imgur.com/XaOpAx8.png)



### Iteration 4 | Create add buttons

On your `FoodBox`, you have an input an "+" button. Use them so that when a user click on the button, it adds them on a list on the right called "*Today's foods*".

You will also need to display the total amount of calories at the bottom of the list as a recap.

![](https://media.giphy.com/media/fH0dyqpPJRvTbiF5rJ/giphy.gif)

If you don't remember how to create responsive columns with Bulma, you can check the [documentation](https://bulma.io/documentation/columns/basics/).


### Iteration 5 (Optional) | Group ingredients

You made an awesome application, but you have found a little problem in the UX. For example, if you click twice on "Pizza", it will display 2 lines "*1 Pizza = 400 cal*" instead of 1 line  "*2 Pizza = 800 cal*". Fix that problem.


### Iteration 6 (Optional) | Allow the user to remove an ingredient

On the "*Today's food*", add a trash icon to let users removing one of their item.



## Solution

You will find the solution here: https://github.com/mc100s/training-labs-react/blob/master/src/lab-react-data-binding/solution.js 
