# Mamikos Test
This is a Vue.js project that allows users to search and filter data about user.

## Project Setup

1. Clone this repository to your local machine.
2. Run yarn install to install the project dependencies.
3. Run yarn serve to start a development server.
4. Run yarn build to compiles and minifies for production.
5. Run yarn lint to lints and fixes files.

## Data

The user data used in this project is stored in a JSON file located at src/assets/variables/DataBody.json. The file contains an array of user objects, each with the following properties:

- photo: the photo profile of the user.
- name: the title of the user.
- age: the age of the user.
- job: the job of the user.

## Components

The project includes three components:

- Navbar: a component navigation bar.
- SearchFilter: a component that allows the user to enter their search query.
- Table: a component that displays the filtered search results.

## How it Works

The SearchFilter component takes the user's search query and passes it up to the parent component (App.vue) using an event. The parent component then filters the book data based on the search query and passes the filtered data down to the Table component as a prop.

The Table component receives the filtered user data as a prop and displays it in a list.

## Technologies Used

- Vue2
- Babel
- Eslint
- JSON

## Contributing

If you would like to contribute to this project, please fork the repository and submit a pull request.

## License

This project is licensed under the MIT License. See the LICENSE file for details.
