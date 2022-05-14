# Natours

This is a server-side rendered (SSR) application using Node and Express to scaffold out a full-featured MVC application including user authentication, automated email, and Pug/Jade view templates.

### Summary of technologies used:

- NodeJS
- Pug/Jade
- BcryptJS
- Nodemailer
- Sendgrid
- Stripe
- Mapbox
- MongoDB
- Mongoose
- Heroku

## Further details:

This application uses the power of [Node](https://nodejs.org/en/) and [Express](https://expressjs.com/) to build a back-end focused MVC application. It is a mock travel booking application which allows users to create accounts, sign in, and create "bookings" for different product packages. All data is stored in a [MongoDB](https://www.mongodb.com/) remote database, interfaced with via [Mongoose](https://mongoosejs.com/). Finally it is deployed onto [Heroku](https://www.heroku.com/) for accessing it via the web.

The user authentication system is sophisticated, **_saving hashed passwords_** to the database and providing a full-featured API with such functions like **_"Change Password"_** and **_"Forgot Password."_** Additionally, upon creating a new account, an **_automated email_** is sent out via [Sendgrid](https://sendgrid.com/) and [nodemailer](https://nodemailer.com/about/).

The API has queryable output, where **_REST API_** queries can tailor the responses as desired for a given client, such as with **_sorting_**, **_filtering_**, **_pagination_**, or **_limiting_**. In general the API is available to do all CRUD operations for all available data models.

Each "booking" details page contains a location map provided by implementing calls to the [Mapbox](https://www.mapbox.com/) API. Additionally, the GPS coordinate data is used to do advanced data aggregation using geolocation tools available with MongoDB.

All of the front-end is served from the Express app by using [Pug](https://pugjs.org/) as the view engine. This is an HTML templating engine and HTML documents are rendered **_server-side (SSR)_**, injecting JavaScript data from the Node application into the templates and serving them up to the client.

Bookings are processed using the [Stripe](https://stripe.com/) API.
