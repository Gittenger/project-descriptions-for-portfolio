# Art Shoppe

This is a mostly front-end application which uses [React](https://reactjs.org/) and [Redux](https://redux.js.org/) to manage the client, while back-end functions are handled by [Google Firebase](https://firebase.google.com/). There is also a minimal Express backend to incorporate [Stripe](https://stripe.com/) for payments.

### Summary of technologies used:

- ReactJS
- Redux
- Redux Saga
- NodeJS
- Express
- Firebase
- Stripe
- Heroku

## Further details:

This is essentially a starter for any shop where the user wants to sell products to online customers. In that sense, it's quite minimalistic, as it doesn't contain extensive shop features like inventory or invoices. It simply hosts a set inventory and allows users to purchase products using Stripe.

For the front-end, the shop is managed as a React application. Redux is used as a state-management solution. Modern Redux is used, using the official Redux Toolkit setup compatible with React to build a modern, efficient, and developer-friendly solution.

For the Redux setup, the familiar Reducer pattern is used, where actions dispatched by the application trigger new frames of immutable state to be added to a stack. Additionally, when certain actions are triggered, [Redux-Saga](https://redux-saga.js.org/) is used to handle **_side-effects_**. These include updating cart state on sign out or checkout, or fetching user data from Firebase.

On that note, the "back-end" of the application is handled by Firebase. Most functionality typically expected to be handled by a back-end, like **_user authentication_** and **_database management_** are managed by making calls to the Firebase API. This is handled with the advanced JavaScript pattern of **_generators_** using Redux-Saga to trigger the API calls as side-effects on certain actions. The advantage of this approach is it is essentially serverless, where back-end functionality is handled by front-end code making API calls.

There is a simple back-end server manually coded into the application using [Express](https://expressjs.com/) to handle making calls to the Stripe API. This is for securely connecting to the Stripe API and this simple server is easily extendible to include other features such as inventory. This feature allows for **_managing payments_** making the shop totally functional! It can be tested using the provided test card credentials.
