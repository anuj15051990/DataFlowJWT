# **Data Flow JWT UI Application**

JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. So in the tutorial, I introduce how to implement an application “Reactjs JWT token Authentication Example” with details step by step and 100% running source code.

* Will give you an Epic of the application, a full-stack executive flow from frontend to backend with an overall architecture diagram.
* Will give you a layer diagram of the Reactjs JWT Application.
* Will give you an implementation of security backend source code (SpringBoot + Nodejs JWT RestAPIs).
* Will guide you step by step on how to develop a Reactjs JWT Authentication application.
* And Finally, I do integrative testing from Reactjs JWT Authentication application to Backend Security RestAPIs

## **Architecture of JWT workflow**
 
![jwt architecture](https://github.com/anuj15051990/Auth_work_flow/blob/master/JWT-Authentication.png)

For the Reactjs JWT Authentication we have set up 2 different projects:
*  Backend project (using SpringBoot or Nodejs Express) provides secured RestAPIs with JWT token.
*  Reactjs project will request RestAPIs from the Backend system with the JWT Token Authentication implementation.


## **JWT Authentication Sequence Diagram**

The diagram below shows how our system handles User Registration and User Login processes:

![](https://github.com/anuj15051990/Auth_work_flow/blob/master/AUTH%20Process.png)

## User Registration Phase:
  *  User uses a React.js register form to post user’s info (name, username, email, role, password) to Backend API /API/auth/signup.
  *  Backend will check the existing users in the database and save users’ signup info to the database. Finally, It will return a message (successfully or fail).

## User Login Phase:
 *  User posts user/password to sign in to Backend RestAPI /API/auth/sign in.
 *  Backend will check the username/password, if it is right, the Backend will create and JWT string with secret then return it to the Reactjs client.

After signing, the user can request secured resources from the backend server by adding the JWT token in Authorization Header. For each request, the backend will check the JWT signature and then returns back the resources based on the user’s registered authorities.




## Reactjs JWT Authentication basic building blocks:

* Reactjs Router is a standard library for routing in React. It enables the navigation among views of various components in a React Application, allows changing the browser URL, and keeps the UI in sync with the URL.
* Reactjs Components let you split the UI into independent, reusable pieces, and think about each piece in isolation.
* Reactjs Service is a bridge between Reactjs Component and Backend Server, it is used to do technical logic with Backend Server (using Ajax Engine to fetch data from Backend, or using Local Storage to save user login data) and returned a response data to React.js Components
* Local Storage allows saving key/value pairs in a web browser. It is a place to save the login user’s info.
* Axios – (an Ajax Engine) is a promise-based HTTP client for the browser and Node. js. Axios makes it easy to send asynchronous HTTP requests to REST endpoints and perform CRUD operations.



