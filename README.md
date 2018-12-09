![CF](http://i.imgur.com/7v5ASc8.png) LAB
=================================================

## CMS Project

### Author: Jen Carrigan

### Links and Resources
* [repo](https://github.com/JenCarrigan/cms-frontend)
* [website](http://carrigancms-carrigancms-v509wt7cw8io.s3-website-us-east-1.amazonaws.com/)

### Modules
#### `index.js`
Function Main provides store to class App

#### `store/index.js`
Combines reducers and creates and exports store

#### `api.js`
Gets information from the database

#### `app.js`
Renders classes LoginContext, Login, Auth, and PickModel. PickModel will only be shown once Auth has been passed.

#### `context.js`
Class LoginProvider:
setLoginState sets the login of user based on cookie load
login saves the user's logged in cookie
logout removes the cookie

Renders context to children

#### `login.js`
Sets backend API URL

Class Login:
handleChange sets state of changed username
handleSubmit posts signin to backend and returns token for storage
logout logs user out
googleURL uses oauth

Render consumes LoginContext, shows login form or logout button depending on status

#### `auth.js`
Render consumes LoginContext and when wrapped around other elements, will show or hide based on user capabilities

#### `picker.js`
Class PickModel:
handleModel sets the state based on button clicked
conditionalRender returns all buttons or the class Records based on click

Render returns conditionalRender

#### `list.js`
Sets API URL

Class Records:
deleteRecord deletes record from backend and store
editRecord updates record from backend and store
reset resets state
componentDidMount gets information from backend

Renders list of records depending on auth and class Record

#### `record.js`
Class Record:
componentDidMount gets information from backend
resetPlayer resets the form to blank
handleSubmit posts or updates record information to the backend and store

Renders record form if authorized

#### `actions.js`
Handles GET, POST, PUT, and DELETE routes

#### `reducers.js`
Handles GET, POST, PUT, and DELETE routes

#### UML
![UML](https://raw.githubusercontent.com/JenCarrigan/data-structures-and-algorithms/master/%3Aassets/CMS-UML.jpg)
