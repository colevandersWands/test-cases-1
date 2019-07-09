# Arithmetic Operators

Before moving on, check out the instructions and copy the ```run_tests``` function from [this repo's README.md](./README.md).

### Operators
* [a + b](#addition)
* [a - b](#subtraction)
* [a * b](#multiplication)
* [a / b](#division)
* [a ** b](#exponent)
* [a % b](#modulo)
* [+a](#unary-plus)
* [-a minus](#unary-minus)

---

## addition

```js
{
  const test_cases = [
      {name: 'string, number', args: ['e', 1], expected: 'e1'},
      {name: 'string, null', args: ['e', null], expected: 'enull'},
      {name: 'string, undefined', args: ['e', undefined], expected: 'eundefined'},
      {name: 'string, boolean', args: ['e', false], expected: 'efalse'},
      {name: 'number, number', args: [1, -1], expected: 0},
      {name: 'true, number', args: [true, 1], expected: 2},
      {name: 'false, number', args: [false, 1], expected: 1},
      {name: 'null, number', args: [null, 1], expected: 1},
      {name: 'undefined, number', args: [undefined, 1], expected: NaN},
      {name: 'NaN, NaN', args: [NaN, NaN], expected: NaN},
      {name: 'NaN, 1', args: [NaN, 1], expected: NaN},
    ];
  function plus(a, b) {
    return a + b;
  }
  run_tests(plus, test_cases);
}
```

> [plus vs. minus](https://janke-learning.org/arithmetic-coercion/)

[TOP](#arithmetic-operators)

---    

## subtraction

implicit coercion with all mathematical operators (except for +) is pretty simple:
* convert everything to a number, then do math on them
* be aware of NaN values!
```js
{
  const test_cases = [
      {name: 'true, 0', args: [true, 0], expected: 1},
      {name: 'true, 1', args: [true, 1], expected: 0},
      {name: 'false, 0', args: [false, 0], expected: 0},
      {name: 'false, 1', args: [false, 1], expected: -1},
      /* write 5 more passing test cases without NaN values*/
      /* write 5 more passing test cases with NaN values*/
    ];
  function subtraction(a, b) {
    return a - b;
  }
  run_tests(subtraction, test_cases);
}
```

> [plus vs. minus](https://janke-learning.org/arithmetic-coercion/)


[TOP](#arithmetic-operators)

---    

## multiplication

implicit coercion with all mathematical operators (except for +) is pretty simple:
* convert everything to a number, then do math on them
* be aware of NaN values!
```js
{
  const test_cases = [
      {name: 'true, 0', args: [true, 0], expected: 1},
      {name: 'true, 1', args: [true, 1], expected: 0},
      {name: 'false, 0', args: [false, 0], expected: 0},
      {name: 'false, 1', args: [false, 1], expected: -1},
      /* write 6 more passing test cases without NaN values*/
      /* write 3 more passing test cases with NaN values*/
    ];
  function multiplication(a, b) {
    return a * b;
  }
  run_tests(multiplication, test_cases);
}
```

[TOP](#arithmetic-operators)

---    

## division

implicit coercion with all mathematical operators (except for +) is pretty simple:
* convert everything to a number, then do math on them
* be aware of NaN values!
```js
{
  const test_cases = [
      {name: 'true, 0', args: [true, 0], expected: 1},
      {name: 'true, 1', args: [true, 1], expected: 0},
      {name: 'false, 0', args: [false, 0], expected: 0},
      {name: 'false, 1', args: [false, 1], expected: -1},
      /* write 6 more passing test cases without NaN values*/
      /* write 3 more passing test cases with NaN values*/
    ];
  function division(a, b) {
    return a / b;
  }
  run_tests(division, test_cases);
}
```

[TOP](#arithmetic-operators)


---    

## exponent

implicit coercion with all mathematical operators (except for +) is pretty simple:
* convert everything to a number, then do math on them
* be aware of NaN values!
```js
{
  const test_cases = [
      {name: 'true, 0', args: [true, 0], expected: 1},
      {name: 'true, 1', args: [true, 1], expected: 0},
      {name: 'false, 0', args: [false, 0], expected: 0},
      {name: 'false, 1', args: [false, 1], expected: -1},
      /* write 6 more passing test cases without NaN values*/
      /* write 3 more passing test cases with NaN values*/
    ];
  function exponent(a, b) {
    return a ** b;
  }
  run_tests(exponent, test_cases);
}
```

[TOP](#arithmetic-operators)

---

## modulo

implicit coercion with all mathematical operators (except for +) is pretty simple:
* convert everything to a number, then do math on them
* be aware of NaN values!
```js
{
  const test_cases = [
      {name: 'true, 0', args: [true, 0], expected: 1},
      {name: 'true, 1', args: [true, 1], expected: 0},
      {name: 'false, 0', args: [false, 0], expected: 0},
      {name: 'false, 1', args: [false, 1], expected: -1},
      /* write 10 more passing test cases with only numbers */
      /* write 5 more passing test cases with non-numbers */
    ];
  function modulo(a, b) {
    return a % b;
  }
  run_tests(modulo, test_cases);
}
```

[TOP](#arithmetic-operators)

---

## unary plus

implicit coercion with all mathematical operators (except for +) is pretty simple:
* convert everything to a number, then do math on them
* be aware of NaN values!
```js
{
  const test_cases = [
      {name: 'true', args: [true], expected: 1},
      {name: '1', args: [1], expected: 0},
      {name: 'false', args: [false], expected: 0},
      {name: '0', args: [0], expected: 1},
      /* write 10 more passing test cases with only numbers */
      /* write 5 more passing test cases with non-numbers */
    ];
  function unary_plus(a) {
    return +a;
  }
  run_tests(unary_plus, test_cases);
}
```

[TOP](#arithmetic-operators)

---

## unary minus

implicit coercion with all mathematical operators (except for +) is pretty simple:
* convert everything to a number, then do math on them
* be aware of NaN values!
```js
{
  const test_cases = [
      {name: 'true', args: [true], expected: -1},
      {name: '1', args: [1], expected: 0},
      {name: 'false', args: [false], expected: 0},
      {name: '0', args: [0], expected: -1},
      /* write 10 more passing test cases with only numbers */
      /* write 5 more passing test cases with non-numbers */
    ];
  function unary_minus(a) {
    return -a;
  }
  run_tests(unary_minus, test_cases);
}
```

___
___
### <a href="http://janke-learning.org" target="_blank"><img src="https://user-images.githubusercontent.com/18554853/50098409-22575780-021c-11e9-99e1-962787adaded.png" width="40" height="40"></img> Janke Learning</a>



