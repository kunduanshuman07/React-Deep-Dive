
### Table of contents
- [Chapter 1 : Javascript](#chapter-1--javascript)
  - [Declaring variables in JS](#declaring-variables-in-js)
  - [Template Strings](#template-strings)
  - [Default Parameters](#default-parameters)
  - [Arrow Functions](#arrow-functions)
  - [Transpilation](#transpilation)
  - [Destructuring Assignment](#destructuring-assignment)
  - [Object literal enhancement](#object-literal-enhancement)
  - [Spread Operator](#spread-operator)


# Chapter 1 : Javascript

## Declaring variables in JS

**1. const**

This type needs to be assigned a value during declaration and cannot be updated or overwritten.

**2. var**

This type is not scoped to the block and can be updated anywhere.

```js
    var block = 'React';

    if(block){
        var block = 'Angular';
        console.log("Block", block); // Block Angular
    }

    console.log("Global", block); // Global Angular
```

This proves that the block variable is not limited to its scope and can be accessed anywhere and overwritten. To overcome this *let* was introduced.

**3. let**

This type allows to scope the variable in any code block.

```js
    var topic = "JavaScript"
    
    if (topic) {
        let topic = "React"
        console.log('block', topic) // React
    }

    console.log('global', topic) // JavaScript
```

## Template Strings

Javascript allows you to compose strings in a different format.

```js
    const value = 'Anshuman'
    const sum = 'Kundu'

    const total = `${value} ${sum}`
    console.log(total) // Anshuman Kundu
```

You can use this template types anywhere in HTML/JSX code.

## Default Parameters

```js
    function logActivity(activity='Cricket', name='Anshuman'){
        console.log(`${name} loves ${activity}`); // Anshuman loves Cricket
    }
```

If we donot pass any arguments and call logActivity() without any parameters then the console will print the output as above.
*Default parameters can be of any type and not just strings.*

## Arrow Functions

Arrow functions help us write functions without writing the function keyword and reduces the syntax complexity tremendously.

```js
    // Traditional approach
    
    var ans = function (value) {
        return 5 + ans;
    }
    console.log(ans(10)); // 15
    console.log(ans(15)); // 20

    // Arrow functions

    var ans = () => 5 + ans;
    //or
    var ans = () => {
        return 5 + ans;
    }
```

## Transpilation

There are severe updates in Javascript programming with versions like ES5, ES6, etc almost every week. Not every version is compatible with all the browsers but as soon as the version comes in the market, all the browsers start making themselves compatible which takes days, weeks or sometimes months. But we cannot wait till that time therefore there is a transpiler for example ***Babel*** which allows to run your javascript in the most compatible browser format by converting them to the desired compatible version.

## Destructuring Assignment

**Destructure objects**

Let us consider a object having key value pair below:

```js
    var sandwich = {
        bread: "tuna",
        cheese: "swiss"
    }
    
    // Destructuring the sandwich object above

    var {bread, cheese} = sandwich;

    // This will extract the bread and cheese values from sandwich and assign it to bread and cheese local variables.
```
```js
    bread = 'swiss';
    cheese = 'tuna';
    console.log(bread, cheese); // swiss tuna
    console.log(sandwich.bread, sandwich.cheese); // tuna swiss
```

**Destructure functions**

```js
    // Traditional approach
    var anything = (person) => {
        console.log(person.firstName);
    }

    var person = {
        firstName: "Anshuman",
        lastName: "Kundu"
    }

    anything(person); // Anshuman

    // Destructuring approach
    var anything = ({firstName}) => {
        console.log(firstName);
    }

    var person = {
        firstName: "Anshuman",
        lastName: "Kundu"
    }

    anything(person); // Anshuman
```

**Destructure arrays**

```js
    var [firstIndex] = ['Anshuman', 'Kundu', 'Apple'];
    console.log(firstIndex); // Anshuman

    var [,,thirdIndex] = ['Anshuman', 'Kundu', 'Apple'];
    console.log(thirdIndex); // Apple
```

## Object literal enhancement

```js
    var firstName = 'Anshuman';
    var lastName = 'Kundu';

    var person = {firstName, lastName};
    console.log(person) // {firstName: "Anshuman", lastName: "Kundu"}

```

After creating two variables firstName and lastName when we create a person variable we are acually creating a key value pair object person.

## Spread Operator

