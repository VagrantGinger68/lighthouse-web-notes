## Modules


### Summary

Every file in node is a module, they all have access to a module object.
Each file that node runs is considered a seperate module. This allows you to export modules and import them into different modules. 

</br>

### JS examples

If you console.log the module object and run file in node you will see something like this:
```js
Module {
  id: '.',
  exports: {},
  parent: null,
  filename: '/Users/*insertUser*/codes/moduleCheck.js',
  loaded: false,
  children: [],
  paths: [ ... ] 
}
```

</br>

To export a module you need to specify the function you want to export at the end of the JS file:
```js
module.exports = *functionName*
```

</br>

To import a module, you need to require it at the beginning of the file you are importing in to:
```js
  const *functionName* = require('*location of file you are importing* Ex: ./myModule')
```
Adding the file extension will still work but it isn't necessary.
 
