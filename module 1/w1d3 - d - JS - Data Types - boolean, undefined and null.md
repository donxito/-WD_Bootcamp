# JS - Data Types in JavaScript - boolean, undefined & null


<!--- 

Status: ready

-->


## Boolean as data type

- What is a boolean



## NOT Operator (!)


> It is used to negate the value of an expression.

    ```js
    let isLoggedIn = false;

    if(!isLoggedIn) {
        //...
    }

    ```



## AND Operator (&&)

> Returns true just if all the evaluated expressions are true.


> expr1 && expr2;


```js

const day = "friday"
const isHungry = true;


if(day==="friday" && isHungry === true){
    console.log("pizza please");
} else {
    console.log("salad please");
}
```


Table with logical operators:
- https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTgs9IVt0czTFyzrOCDSqqQIUFStlMxsMORK4f193kH4gfxV9u38SRW8_mAwIPntq_nMjI&usqp=CAU



## OR Operator (||)

> Returns true if one of the evaluated expressions is true.

> expr1 || expr2;

    ```js
    const age = 20;
    let isWorking = false;

    if(age < 18 || isWorking === true){
        console.log("water please")
    }
    ```




## undefined

```js
    let amount;
    console.log(amount); // <== undefined
```



## null

> In computer science, a null value represents a reference that points, generally intentionally, to a nonexistent address in memory

```js
    let amount = null;
    console.log(amount); // <== null
```



## Truthy and falsy values

See MDN.


Truthy:
- true
- any number different than 0
- any string different than ''
- any array  (even an empty array !!! )
- any object  (even an empty object !!! )



## Exercise

Practice: Truthy or Falsy + Logical Operators
- Instructions: https://stackblitz.com/edit/js-4kzkn3?file=index.js
- Time: 10min.




## (skip) Immutability

(we'll get there once we speak about reference & mutable data types)




