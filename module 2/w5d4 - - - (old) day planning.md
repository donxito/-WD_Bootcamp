

# w5d4

<!--


UPDATE2:
Consider this option:
- LT to introduce basic axios concepts (how to make a get request, post...)
- Split in groups, each group with one TA.
- Each group would be solving the lab, collaborating together.



UPDATE: even more simple than the exercise below,
- show how we can use axios to send http requests, for example, on stackblitz (GET, POST, PUT)
- Leave the exercise below as a lab that students can do




On feb22 we did the following (went quite well):
- we started from an existing project with CRUD and Mongoose
- the initial code is in this repo: https://github.com/luisjunco/characters-crud
- Students & LT can fork this repo.
- The main goal of this codealong would be to move from DB to an API
  (we would use the API to read and store info)
- Explain students that this is just one excuse to practice axios.

- Final result (fork): https://github.com/Ironmaidens-Ironhack-Jan-2022/characters-crud
- See readme for main goals: https://github.com/Ironmaidens-Ironhack-Jan-2022/characters-crud/blob/main/README.md




@Luis / @to-do:

- display nav menu in all pages

- improve ux (ex. links to edit + delete in same view)

- improve css

- protected routes? (do not protect Read functionality)

-->


Goals:
- Practice with axios
- Learn different concepts related to APIs, REST APIs & best practices


## Warmup exercise

1. Fork + Clone: https://github.com/luisjunco/characters-crud
2. Run the project 
  - Hint: you will need to install dependencies + add one environment variable
  - Students will need to:
    - install dependencies (`npm install`)
    - create environment variables (`SESS_SECRET = 'unicorns are cool'`)
3. See how it works on the browser.
4. Go to the code & understand the code (Model + Routes)
5. Functionality to edit a character doesn't work properly. Please fix it.
  - Hint: if you don't know were to start, try to go through the whole process (see what data is sent in the dev tools, see what data is received in the server, etc)

Time: 
- Steps 1-4: 15-20min.
- Step 5: 5-10min.



## Explain code & the App
- LT explains the app 
  - Auth functionality (register, login, logout) + protected routes
  - CRUD functionality for characters
  - Data is stored in DB


## Explain 

- APIs

- REST APIs

  - slides: 
    - https://docs.google.com/presentation/d/194i1dCV2vpqTN5T3yC5lysvfS-_fnEkok97QpaOtb3w/edit?usp=sharing


  - Video: What is a REST API? (explains RESTful) (6 min., Mosh)
    - https://www.youtube.com/watch?v=SLwpqD8n3d0



- (Bonus) Exercise:
  - You need to define a REST API for characters (create a character, update etc).
  - Your task: following REST principles, define the endpoints for the following actions:
    - List of all characters
    - Details of a specific character
    - Create a new character
    - Update a specific character
    - Delete a specific character
  - Time: 5-10min.


- Introduce "characters API" 
  (https://ih-crud-api.herokuapp.com/characters)





- Explain what we will do (move from DB to API)
  - IMPORTANT: explain that we can make requests from Browser and/or Server



- (extra) JavaScript HTTP requests & AJAX


## Code (move from DB to API)

Move from DB to API


- Code quality:
  - environment variables
  - remove Character model (we still need DB and dependencies for auth)
  - implement as a service


## Extra challenges
- Improve functionality of the app
- Implement same functionality using .fetch()
- Implement with async/await



## (Extra) Explain Git conflicts

