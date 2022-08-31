# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

## Staring the App

- Navigate to the root folder. The root contains the package.json file.
- Run command: `npm install` to install the node modules. This is a one time process.
- Run command: `npm start` to start the application.

## Folder structure

Since this project was boot strapped with create-react-app, all the default files of create react app are included in the root folder.

```
|___root
    |___public(folder)
    |___src(folder)
    |___.env(file)
    |___package.json(file)

```

This is a basic structure of the file structure of the app.

The public folder is the static folder of the app and all the static assets are contained inside this folder.

The src folder contains all the custom components, store and pages. 
```
|___src(folder)
    |___components
    |    |___actions
    |    |    |___actions.js
    |    |___constants
    |    |     |___constants.js
    |    |___Error
    |    |     |___Error.js
    |    |___Headline
    |    |    |___Headline.js
    |    |___Loading
    |    |     |___Loading.js
    |    |___News
    |    |     |___news.css
    |    |     |___News.js
    |    |     |___NewsCard.js
    |    |     |___NewsCardMobile.js
    |    |___NewsGrid
    |    |     |___NewsGrid.js
    |    |___reducers
    |    |     |___favReducer.js
    |    |     |___HeadlineReducer.js   
    |    |     |___newsReducer.js   
    |    |     |___sourceReducer.js
    |    |___Sources
    |    |     |___Sources.js
    |    |___scrollbar.css
    |    |___store.js
    |___App.css
    |___App.js
    |___App.test.js
    |___index.css

```

This is the full folder tree of src folder.

## custom components

- NewsGrid.js:

    Base component the goes into the App.js file. It has 3 props: source, news and headlines. This component is build using Material UI grid component. Its purpose is to display the three components passed inside the props in a grid view. The components passed are Source, Headline and News components.

- Source.js

    This component displays the sources and the favourites. Contains a dispatch in useEffect.

- News.js

    This components displays a list of news headlines from the selected source. It renders NewsCard component on large screens and NewsCardMobile component on small screens. The news.css files contains the CSS where the break points for renderng either the card components based on screen size.

- Headline.js

    This component displays the headlines from the selected source.

- Loading.js

    Shows the loading screen when the global loading state is true.

- Error.js

    Shows the error screen when the global error state is true.

- store.js

    This files contains the store for all the global state management. The state management is done using redux-thunk state management framework.

- Reducers (folder)

    This folder contains all the reducers that manages the state. The favReducers manages the favourite news headlines state which handles the addition and removal of favourites. Its also handles the local storage capability to save all the favourite news to the ocal storage.

- actions.js

    This file contains all the actions including the onces thet require to make api calls.

- .env

    This file contains the key and the links for the API calls. Any changes to the APIs or the key can be done here directly. This data will be accessed inside the actions using process.env which is readily available through react as default.

## Packages used:

- Material UI library: @mui/material (theming library)
- Material Icons: @mui/icons-material (icons)
- Redux: redux (state management library)
- Redux Thunk: redux-thunk (state management middleware)
- Axios: axios (promised-based HTTP client)
- Html react parser: html-react-parser (react library to convert string to html docs)

