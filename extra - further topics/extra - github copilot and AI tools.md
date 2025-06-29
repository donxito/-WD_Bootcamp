

# Extra - GitHub Copilot



## Demo:

- url: https://github.com/features/copilot/plans 

- settings
    - eg: enable/disable
    - choosing model

- ghost text:
    - `function findLongestStringInArray(){}`
    - `const words = []`

- code suggestions from comments
    - `// function to find the average in an array of numbers`
    - `// GET /drinks`

- questions from comments (note: comment depends on current language):
    - `// q: how do i uninstall an npm package`

- inline chat and speech-to-text
    - note: now it's available in the copilot menu (at the top)
    - example 1: create a function that takes two arrays and returns true if they have exactly the same values
    - example 2: make this function generic, so that it works with any nested levels (ie. arrays of any depth).

- chat in sidebar:
    - `@workspace` (e.g.: how many models we have)
    - `@vscode` (e.g.: whats the shortcut to change the language mode for the current file)

- sparkles (e.g. commit message)




## Custom instructions file

> Instruction files enable you to specify custom instructions in Markdown files. 
> You can use these files to define your coding practices, preferred technologies, and project requirements.

- `.github/copilot-instructions.md`: a single instruction file that contains all the instructions for your workspace. These instructions are automatically included in every chat request.

- example: 

    ```md
    General Guidelines:
    - Use modern JavaScript/TypeScript (ES6+).
    - Follow project coding standards and existing patterns.
    - For React projects, prefer functional components and hooks.

    Preferred Libraries:
    - React
    - Next.js
    - Tailwind CSS
    - Axios (for HTTP requests)

    File Structure:
    - Use `components/` for reusable UI components.
    - Use `pages/` for route-level components (Next.js).
    - Use `utils/` for utility functions and API logic.
    ```

- more info: https://code.visualstudio.com/docs/copilot/copilot-customization


## Tips:

- Copilot can be really good at doing things with existing libraries and apis (especially if they're popular & not very recent)
    - e.g.: `// get most popular artists from spotify api`

- It can also be useful to generate unit tests
    - e.g. `unit tests for a function that will receive a string and verify if it's a valid email address`


## AI Editors and Agents

- cursor
    - Cursor Tutorial for Beginners: https://www.youtube.com/watch?v=ocMOZpuAMw4

- windsurf

- Cline (AI coding agent)
    - https://github.com/cline/cline
    - examples:
        - Generate, edit and refactor files
        - Run and interact with your terminal
        - Automate browser actions for debugging or testing


## Other AI tools

- UI generators: v0.dev (react, tailwind)

- Low-code development & prototyping: 
    - bolt.new
    - lovable.dev
    - replit.com
    - firebase.studio (tried it in april 25, a few days after release, and results were quite poor)

- Gemini canvas: https://www.linkedin.com/posts/addyosmani_programming-softwareengineering-ai-activity-7308542354821394432-AdnZ


Examples:
- create an Instant Resume Analyzer
- create the homepage for a furniture company that offers beautiful pieces of furniture and shipping everywhere in Germany
- create a REST API with Express and PostgreSQL. API should implement auth functionality with jwt, CRUD on projects and CR on tasks.
- Create a react app to generate random pairs with students. The app will let you create a cohort & add a list of students for that cohort (by entering all the names in comma separated format). Once you have created a cohort, you can generate random pairs (if there's an odd number of students, it will generate a group of 3). If you like the pairs generated, you can click a button to confirm. One you confirm, those pairs will be added to a "pairs history". The user can visit the pairs history to see a table with all the students that have already been matched together. Also, when you create new random pairs, the app will avoid pairing students that have already worked together.

Use cases:
- Quick prototypes.


## Agent mode + MCP Servers

VS Code: Agent Mode + MCP Servers + BYOK
https://www.youtube.com/watch?v=dutyOc_cAEU


Demo: 
- Firebase MCP on VS Code


## Limitations

AI tools for Greenfield projects vs. commercial large codebases:
- https://www.linkedin.com/posts/gergelyorosz_something-i-hear-very-little-talk-about-activity-7333488796627349505-QZnw




## Warnings ⚠️ 

- As you can see, to be a prompt engineer, one "must" know how to code.
- Using AI to find quick solutions vs. learning
    - If you're learning a new technology, make sure you type things
    - "You will not learn a language by using Google Translator"

- Will AI replace developers? How to use AI to help you land a job?
    - https://chatgpt.com/share/6824e153-86ec-8003-a44f-33c5d9197b60


## Videos:

- Get to know GitHub Copilot in VS Code and be productive IMMEDIATELY (VS Code, 5min.)
https://www.youtube.com/watch?v=jXp5D5ZnxGM&t=2s

- GitHub Copilot in VSCode: Top 10 Features Explained (Max on Tech, 9min.)
https://www.youtube.com/watch?v=2nPoiUJpDaU




