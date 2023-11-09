
# React - List and Keys

<!-- 

Status: draft

@Luis: 
- This unit has improved a lot with v6.1
- Consider following steps students portal instead (do "popcorn-time" but follow steps from this unit, so that students understand the logical process)

-->



## (skip ?) Refresh: working with arrays

<!-- Goal: refresh forEach() & map() -->

- Instructions: https://stackblitz.com/edit/ih-react-exercise-with-arrays?file=index.js
  
- How: solve together / work in pairs
- Time: 15-20min.



- Explain: 
    - forEach() will return undefined
    - map() returns an array


- Solve together:
  - diagram map: https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_c465728a5460c8d562936d4f1b5d18cc.png
  - map vs filter vs reduce: https://miro.medium.com/max/880/0*cQwPe6QPdl_-ByOq.png


- Possible solution (w/o bonus): https://stackblitz.com/edit/ih-react-exercise-with-arrays-vefnrt?file=index.js

- Possible solution with bonus: https://stackblitz.com/edit/ih-react-exercise-with-arrays-3dwodd?file=index.js






## Initial Setup:
  - navigate to your module3 directory
  - `npm create vite@latest popcorn-time -- --template react`
  - cd popcorn-time
  - npm install
  - code -r .
  - npm run dev
    - Custom port through CLI: `npm run dev -- --port 3000`


 
## Practice: Create the initial structure for "popcorn time"


<!-- @LT: if short of time, do as a codealong instead -->


Iteration 1: Create the initial structure. 
  - Create 3 function components: Header, Main, Footer
  - for each of them, just display a text, (ex: "this is the header").
  - render all of them in App

Iteration 2: Make a commit + Upload repo to GitHub

Bonus: add some css for the Header component with a specific file
    - create `Header.css`
    - in Header component:
      - `import "./Header.css";`
    - NOTE: any css rules would apply to the whole application
      - in the component add `<header className="Header">`
      - in the css, add the class to all rules
        - ex: https://github.com/Ironborn-Ironhack-March-2022/react-popcorn-time/blob/main/src/components/Header.css


  Time: 15min.



## (skip) Intro: working with lists (arrays) in React


- What we've done so far

  ```jsx

    const tweetsArray = [];

    // ...

    <Tweet tweet={ tweetsArray[0] }>
    <Tweet tweet={ tweetsArray[1] }>
    <Tweet tweet={ tweetsArray[2] }>

  ```

- We will often work with arrays of objects but this syntax is not sustainagle.
  - ex. if we have an array with 200 elements
  - ex. if we don't know how many elements we will have in the array


- Inside <Main />, create 3 divs with a movie

  ```jsx
    <div className="Main">

      <div>movie one</div>
      <div>movie two</div> 
      <div>movie three</div>

    </div>
  ```

- Put those 3 divs in an array and show how it is possible to display an array

  ```jsx
  const list = [
    <div>movie one</div>, 
    <div>movie two</div>, 
    <div>movie three</div>
  ];
  
  // ....
  
  {list}
  ```


- TAKEOVER: 
  - in JSX, we can render an array of elements (those elements can be html or any valid JSX)




## DEMO: Import json file

Load list of movies from a `json` file
  - create `data/movies.json`
  - Sample json file: https://github.com/Ironborn-Ironhack-March-2022/react-popcorn-time/blob/main/src/data/movies.json
  - Import in Main.js: `import movies from "../data/movies.json";`

  <!-- IMPORTANT: add this in Main.js -->


- Note: this information will often come from a DB / API




## DEMO: Display the list of movies, from the array

  - IMPORTANT: do not create a specific component

  <!-- 
  @Luis: 

    - Keep everything inside the Main component 
    - (do not create a specific component!)

    - Can do DEMO (later, when we load from json, I will ask them to do again)

  -->


  ```js
  {moviesArray.map( movie => {
      return <div>Title: {movie.title}</div>
  })}
  ```

- See Warning in the console: we need to add "key" prop
  - NOTE: use the `index` as key (tomorrow we will have functionality to add new movies, we don't want to ask the user for the id)
  > "When you don’t have stable IDs for rendered items, you may use the item index as a key as a last resort"




## Practice: iterate through an array with .map()

1. Copy .json from the live session and save it as `src/data/movies.json`
2. Import this json file in Main.jsx:
  - `import movies from "../data/movies.json"`
3. For each element of the array, display the title and the rating (use `.map()`)

Time: 10min.


  - (Extra) add some basic css to card "movie"

      ```css
      .Main .card {
        max-width: 80%;
        margin: 1rem auto;
        padding: 1rem;
        border: 1px solid #666;
        box-shadow: 5px 5px 10px -5px;
        transition: 0.4s;
      }

      .Main .card:hover {
          cursor: pointer;
          box-shadow: 5px 5px 10px 0px;
      }
      ```

<!-- commit -->


## Removing elements from a list (will apply State)

Discuss: 
- how we can implement functionality to delete movies

Steps:

- Store the List Array in state
- Render the List Array from state
- Delete Button (note: we need to pass the Id of the movie)
  ```jsx
  <button onClick={() => deleteMovie(movie._id)}>
    Delete
  </button>
  ```
- Update state when user clicks on button

```js
  const deleteMovie = movieId => {
    const filteredMovies = movies.filter(movie => {
      return movie._id !== movieId;
    });

    setMovies(filteredMovies);
  };
```

<!-- map vs filter vs reduce: https://miro.medium.com/max/880/0*cQwPe6QPdl_-ByOq.png -->



## (extra challenges)...
  - display year & image
  - display genres (note: it's an array)
  - in Main.jsx, display a title: `<h1>We currently have XXX movies available</h1>`



## Display a title with the number of movies 

<!--
@Luis: 
- do this today (will help so that tomorrow we intro "lifting state up")
- IMPORTANT: display in the same component where we have the list of movies (ex. Main.js)
-->

  - ex. `<h1>Number of movies: {movies.length}</h1>`
  - IMPORTANT: display that in the `<Main>` component !!!
  - NOTE: many students solve it adding a new stateful variable (introduce the concept of "SINGLE SOURCE OF TRUTH")

