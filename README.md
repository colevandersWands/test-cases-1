# Test Cases

These exercises are a bit backwards, usually as a developer you will write complete test cases then make sure your code passes them.  Since these exercises are also designed to help you understand JavaScript operaotrs, you will be writing test cases that pass code we give you.  If a test case fails it's the the test case that is wrong, go back to that case and fix it.

Writing test cases just happens to be the other best way to understand how code works.  The first best way is to [rewrite it yourself](https://blog.codinghorror.com/when-understanding-means-rewriting/) like in the Implicit Coercion exercises.

(test cases for these exercises should be limited to primitive types - Number, Boolean, String, Null, Undefined)

### Index:
* [describing behavior](#describing-behavior)
* [run\_tests function](#run-tests-function)
* [examples to study](#examples-to-study)
    * [failing test cases](#failing-test-cases)
    * [passing test cases](#passing-test-cases)
* the exercises
    * [explicit coercion](./explicit-coercion.md)
    * [equalities](./equalities.md)
    * [logical operators](./logical-operators.md)
    * [inequalities](./inequalities.md)
    * [arithmetic operators](./arithmetic-operators.md)
* [resources](#resources)

---

## Describing Behavior

Code's behavior is what has changed in your program _after_ the code has executed, implementation is the lines of text that make up the code.  This exercise will introduce how to understand behavior using __test cases__.

Practically speaking you can think of test cases as just inputs and outputs.   What values went into the function, and what values come out of the function?  The test case will contain the input-output pairs that your function _should_ implement, a test case fails if the function returns something else.  

Test cases may be relatively easy to read and use, but writing good ones can be tricky.  You have to think about all possible strange combinations and fringe cases. So don't worry about writing the perfect test cases yet, just do your best and compare with a friend to help each other understand how you thought of your test cases.

For this exercise you will write test cases in this format:
```js
test_cases = [
    {name:'meaningful name', args:['the inputs', 'for this snippet'], expected: 'what it should output'},
    {name:'another test case', args:['different', 'inputs'], expected: 'the expected output'},
  ];
```

> DISCLAIMER: 
> * In this exercise you are learning to write test cases for existing code.  The code is always right. If your test fails, change it.   
> * In the real world it will usually be the oposite. The tests should descibe the code.  If the tests fail, change the code.

[TOP](#test-cases)

---

## Run Tests Function

To check if your function passes all of it's test cases, we'll be using this function.  It takes two arguments (the function to test, and the test cases), and console.log's a message for every test case that fails.

Study it for a minute then paste it in the console, the exercises below won't work otherwise.  If you don't understand entirely how this function works that's okay.  The main objective for this exercise is to write & use test cases, understand JS operators.  

```js
function run_tests(_target, _cases) {
  console.groupCollapsed('<- click this arrow to see the function')
  console.log(_target.toString());
  console.groupEnd();

  for (let t_case of _cases) {
    
    // create variables for readability
    const expected = t_case.expected;
    const args = t_case.args;
    
    // run function with test case
    const actual = _target(...args);

    // compare
    let pass;
    if (typeof expected === 'object' && expected !== null) {
      const _actual = JSON.stringify(actual);
      const _expected = JSON.stringify(expected);
      pass = _actual === _expected;
    } else if ( expected !== expected ) {
      pass = actual !== actual;
    } else {
      pass = actual === expected;
    };

    // communicate result to developer 
    if (pass) {
      console.groupCollapsed(`%cPASS: ${t_case.name}`, 'color:green');
    } else {
      console.groupCollapsed(`%c: ${t_case.name}`, 'color:red');
      console.log("%cactual: ",  'color:orange', typeof actual +", "+ actual);
    };

    for (let i = 0; i < args.length; i++) {
      console.log(`arg ${i+1}: ${typeof args[i]},`, args[i]);
    }
    console.log("%cexpected: ", 'color:blue', typeof expected +", "+ expected);
    console.groupEnd();
  };
}
```

[TOP](#test-cases)

---

## Examples to Study

### Failing Test Cases

notice: in all of these exercises it is your test cases that need to change if they fail.  JS operators are always right, you must change your expectations until they match the actual behavior.
```js
{
  const test_cases = [
      {name: 'null', args: [null], expected: 'null'},
      {name: 'undefined', args: [undefined], expected: 'void'},
      {name: 'true', args: [true], expected: 'bool'},
      {name: 'false', args: [false], expected: 'Boolean'},
      {name: '0', args: [0], expected: 'Number'},
      {name: '1', args: [1], expected: 'num'},
      {name: '0.0', args: [0.0], expected: 'float'},
      {name: '-0', args: [-0], expected: 'negative'},
      {name: '+0', args: [+0], expected: 'positive'},
      {name: 'NaN', args: [NaN], expected: 'NaN'},
      {name: 'Infinity', args: [Infinity], expected: 'string'}, 
      {name: '-Infinity', args: [-Infinity], expected: 'infinity'},
      {name: '1e3', args: [1e3], expected: 'scientific'},
      {name: '4e2', args: [4e2], expected: 'scientific'},
      {name: '.2', args: [.2], expected: 'float'},
      {name: '"anything in quotes"', args: ["anything in quotes"], expected: 'str'},
      {name: '""', args: [""], expected: 'String'},
    ];
  function _typeof(a) {
    return typeof a;
  }
  run_tests(_typeof, test_cases);
}
```


### Passing Test Cases

```js
{
  const test_cases = [
      {name: 'null', args: [null], expected: 'object'},
      {name: 'undefined', args: [undefined], expected: 'undefined'},
      {name: 'true', args: [true], expected: 'boolean'},
      {name: 'false', args: [false], expected: 'boolean'},
      {name: '0', args: [0], expected: 'number'},
      {name: '0.0', args: [0.0], expected: 'number'},
      {name: '-0', args: [-0], expected: 'number'},
      {name: '+0', args: [+0], expected: 'number'},
      {name: 'NaN', args: [NaN], expected: 'number'},
      {name: 'Infinity', args: [Infinity], expected: 'number'}, 
      {name: '-Infinity', args: [-Infinity], expected: 'number'},
      {name: '1e3', args: [1e3], expected: 'number'},
      {name: '4e2', args: [4e2], expected: 'number'},
      {name: '.2', args: [.2], expected: 'number'},
      {name: '"anything in quotes"', args: ["anything in quotes"], expected: 'string'},
      {name: '""', args: [""], expected: 'string'},
    ];
  function _typeof(a) {
    return typeof a;
  }
  run_tests(_typeof, test_cases);
}
```


[TOP](#test-cases)

---


## Resources

* [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators)
* [javascript.info](https://javascript.info/operators)
* [implicit coercion](https://github.com/janke-learning/implicit-coercion)


[TOP](#test-cases)

___
___
### <a href="http://janke-learning.org" target="_blank"><img src="https://user-images.githubusercontent.com/18554853/50098409-22575780-021c-11e9-99e1-962787adaded.png" width="40" height="40"></img> Janke Learning</a>
