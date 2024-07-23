
### Table of contents
- [Chapter 1 : Javascript](#chapter-1--javascript)
  - [Declaring variables in JS](#declaring-variables-in-js)


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
        console.log("Block", block); // This will print Block Angular
    }

    console.log("Global", block); // This will print Global Angular
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