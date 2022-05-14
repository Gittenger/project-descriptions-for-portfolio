# Miscellaneous Micro Projects

This is an assortment of small projects I've completed to apply some front-end skills that I've learned. Some of these were completed over 3 years ago.

### Summary of technologies used:

- ReactJS
- HTML5
- SCSS
- CSS3

## Further details:

Each of these projects is a simple exploration of applying my skills developing front-end and client side applications. One is a simple tic-tac-toe game built with React. Another is a mock Google landing page, made with React and CSS and designed to look similar to a Google "New Tab" page in a Chrome browser. There is a quote machine with a simple front-end handled by React and SCSS, and this application uses asynchronous JavaScript to retrieve quote data from an external API. Finally there is also a functional calculator which is assembled with React and styled via CSS.

The user authentication system is sophisticated, **_saving hashed passwords_** to the database and providing a full-featured API with such functions like **_"Change Password"_** and **_"Forgot Password."_** Additionally, upon creating a new account, an **_automated email_** is sent out via [Sendgrid](https://sendgrid.com/) and [nodemailer](https://nodemailer.com/about/).

The API has queryable output, where **_REST API_** queries can tailor the responses as desired for a given client, such as with **_sorting_**, **_filtering_**, **_pagination_**, or **_limiting_**. In general the API is available to do all CRUD operations for all available data models.

Each "booking" details page contains a location map provided by implementing calls to the [Mapbox](https://www.mapbox.com/) API. Additionally, the GPS coordinate data is used to do advanced data aggregation using geolocation tools available with MongoDB.

All of the front-end is served from the Express app by using [Pug](https://pugjs.org/) as the view engine. This is an HTML templating engine and HTML documents are rendered **_server-side (SSR)_**, injecting JavaScript data from the Node application into the templates and serving them up to the client.

Bookings are processed using the [Stripe](https://stripe.com/) API.
