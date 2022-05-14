# Pokédex

This is an entirely front-end application which uses [React](https://reactjs.org/) to manage the entire application including state and all API calls. It indexes Pokémon data using data from an external API.

### Summary of technologies used:

- ReactJS
- React Hooks
- webpack 4
- CSS modules
- PostCSS
- Tailwind CSS
- Netlify

## Further details:

This is a "Pokédex" which is simply an index of Pokémon data. I used the excellent [PokéAPI](https://pokeapi.co/) to acquire all the data for the app. In essence, this is a React application which I made to hone my skills at **_retrieving_**, **_transforming_**, and **_caching_** large amounts of data, and then injecting that data into React templates.

I used custom React hooks to transform the data once the raw JSON data is retrieved. Then, once it is transformed and processed, it is **_cached to local storage_** in the browser, thus optimizing for minimal API calls and quick performance once the initial calls are completed successfully.

It has a couple of useful features, like **_searching by name_**, **_filtering by type_**, and **_setting global image type_**, as well as **_pagination_**. In general, the API has tons of options for extending all functionality of this app, and my plan is to extend it later. There are many image types to choose from within the API, but I've chosen four for the purpose of this app to keep things simple.

Each Pokémon has a "card" component on the main page, and a details page where details for that individual Pokémon can be found. Upon the initial page load, basic information for all 151 Pokémon is retrieved and populates the cards in the main view. Then when any individual Pokémon is selected, data for that Pokémon is retrieved, thus minimizing the load on the API and improving performance and browser footprint.

Finally, styles are handled using [Tailwind CSS](https://tailwindcss.com/) for most basic styles, and CSS modules for more complicated styles.

The entire application is set up with a custom [webpack](https://webpack.js.org/) setup using webpack 4 and a modern version of React. Fonts, images, and styles are loaded into the bundle by configuring everything in webpack by hand, and [PostCSS](https://postcss.org/) is incorporated into the build chain to allow for Tailwind CSS and any other advanced CSS features which I may want to add.
