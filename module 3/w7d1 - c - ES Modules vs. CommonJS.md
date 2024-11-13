
# ES Modules vs. CommonJS


<!-- @todo: 
  - create a diagram/image with code snippets comparing both
  - create a small exercise to practice
-->



## Intro

ES6 modules
- export
- import


Common JS
- module.exports = 
- require()


## Demo

<!-- @LT: show demo on node (locally) -->

- mkdir module3
- mkdir commonjs-demo
- touch index.js
- touch utils.js


Example 1:

  ```js
  const amount = 42:

  module.exports = amount;
  ```


Example 2:

  ```js
  function calcTotal(a, b){
      return a * b;
  }

  function calcDivision(a, b){
      return a / b;
  }

  function calcAverage(a, b){
      return (a + b) / 2;
  }

  module.exports = { calcTotal, calcDivision, calcAverage, };
  ```

