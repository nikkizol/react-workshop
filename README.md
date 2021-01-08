# React Movie App

- Repository: `react-movie-app`
- Type of Challenge: `Learning`
- Duration: `take your time`
- Solo challenge

## Learning Objectives 
After this workshop, you will:
- be able to write JSX
- know basics about Class components and Functional components
- know what Props are
- know what State is
- know what Hooks are
- be able to make a basic React app

## The Mission
To learn React of course :) Make your own IMDB website with React.

### Must-have features

- Search movie by name;
- Display movies with a poster and name on search;
- When click on a specific movie, display more detailed information about that movie.


### Nice-to-have features
- Make it looks Nice
- Able to add a movie to Favourites and keep them on refresh 


### Steps
1. Create a repository.
2. Check if you have node.js and npm, if not, install them.
    - node: <code>node -v</code> or <code>node -version</code>
    - npm: <code>npm -v</code> or <code>npm -version</code>
3. Navigate to the root of your repository in the terminal and enter the command <code>npx create-react-app project-name</code>.
4. Go inside of the "project-name" folder and run the command <code>npm start</code>. You can now check out your react app on <code>localhost:3000</code>.
5. In your editor, navigate to <code>project-name/src/</code> and remove everything from there.
6. Create <code>index.js</code> and add the following code:

                import React from "react"; 
                import ReactDOM from "react-dom";
                import "./index.css";
                import App from "./App";
                
                                                    
                ReactDOM.render(
                <React.StrictMode>
                <App />
                </React.StrictMode>,
                document.getElementById("root")
                );
7. Create <code>index.css</code> and add the following code:    

            * {
                box-sizing: border-box;
                padding: 0;
                margin: 0;
                -webkit-font-smoothing: antialiased;
                -webkit-text-size-adjust: 100%;
                }
8. Create <code>App.js</code> and add the following code:
   
            import React from "react";
             
             
             function App() {
               return (
                 <>
                 </>
               );
             }
             
             export default App;
             
9. Go inside of the "project-name" folder and run the command <code>npm install --save bootstrap</code> and this line: <code>import 'bootstrap/dist/css/bootstrap.min.css';</code> to <code>App.js</code>. Now we can use bootstrap in our app.        
10. Now as our project directory ready, let's get an API from where we are going to fetch our movies. We're going to use the [OMDB](http://www.omdbapi.com) API as our source for movies.
    - Go to http://www.omdbapi.com/apikey.aspx and fill out the form, and you will receive an email with API key;
    - Don't forget to activate it, by clicking the link you received;
    - Check the documentation, you will need it.
11. As everything ready now, it's a good moment to take time and think over your app, here are some questions to ask yourself:
    - How many components do I need?;
    - Remember about single responsibility - check [SOLID](https://samueleresca.net/solid-principles-using-typescript/);
    - Decide which components you will be using Class or Functional (I recommend Functional);
    - Check what are props;
    - Check what is State;
    - Remember Google is your best friend!
12. In your App start with Fetching data from API and try to <code>console.log</code> it (if you are using Functional components check <code>useEffect</code> you will need it for fetching), but before that, declare <code>useState</code> with an empty array.
13. To save the data you just fetched and then re-use it - use <code>useState</code> which you declared above.
14. Displaying data. It's good to use another component for displaying all movies, and pass movies (which you just fetched) from the App component to a new component through <code>props</code>.
You need:
    - Create a new component, remember to export it.
    - In your App component import the component you just created and return it.
    - Pass movies you fetched and saved (via useState) to <code>props</code> of that component you return.
    - Now you can reach that data in your new component.
15. Now, try to implement a search bar, so you can display movies on your search, some hints:
    - Make for this another component with search input.
    - Add properties for input <code>value</code> and <code>onChange</code>
    - In your App component import the component you just created and return it.
    - Declare another <code>useState</code> in your App and pass <code>props</code> to Search component.
16. Now you should display a movie on your search, and we are halfway! `Let's do the last part of the must-have feature`.
Create another component to display a selected movie. Some hints:
    - You need to pass an id of a selected movie from the App to a new component.
    - You need to make another fetch in a new component with that id so you will fetch data for a specific movie.
    - (there are more ways of doing it - be creative think out of the box)
17. Now you have all the must-have features. Congratulations! If you have time left, be sure to take a look at the nice-to-have features. Here are some suggestions as well:
    - Make it looks good. Check [Material-UI](https://material-ui.com) for styling;
    - For the Favorites make another component - you should have the same logic as for open a specific movie, but instead of open, add to the array, use <code>useState</code> and remember to do it in a Parent component.
    - To keep movie on refresh use <code>useEffect</code> and local storage for this.
18. Congratulations, you survived the first steps of React. Pat yourself on the back!




![YEAH!](https://media.giphy.com/media/KJCsv8KcpwHjG/giphy.gif)

