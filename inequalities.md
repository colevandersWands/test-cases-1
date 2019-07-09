# Inequalities


Before moving on, check out the instructions and copy the ```run_tests``` function from [this repo's README.md](./README.md).

### operators
* [a > b](#greater-than)
* [a < b](#less-than)
* [a >= b](#greater-than-or-equal-to)
* [a <= b](#less-than-or-equal-to)

---

## greater than

rules for implicit coercion:
* If both operands are numbers, perform a numeric comparison.
* If both operands are strings, compare the [character codes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/charCodeAt) for each. sort of like alphabetical order.
* If one operand is a number, convert the other operand to a number and perform a numeric comparison.
* careful of NaN and values that convert to NaN. 
```js
{
  const test_cases = [
      {name: 'true, 0', args: [true, 0], expected: true},
      {name: 'true, 1', args: [true, 1], expected: false},
      {name: 'false, 0', args: [false, 0], expected: false},
      {name: 'false, 1', args: [false, 1], expected: false},
      /* write 4 more passing test cases with only strings */
      /* write 6 more passing test cases without NaN values */
      /* write 4 more passing test cases with NaN values */
    ];
  function greater_than(a, b) {
    return a > b;
  }
  run_tests(greater_than, test_cases);
}
```

[TOP](#inequalities)

---


## less than

rules for implicit coercion:
* If both operands are numbers, perform a numeric comparison.
* If both operands are strings, compare the [character codes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/charCodeAt) for each. sort of like alphabetical order.
* If one operand is a number, convert the other operand to a number and perform a numeric comparison.
* careful of NaN and values that cast to NaN. 
```js
{
  const test_cases = [
      {name: 'true, 0', args: [true, 0], expected: false},
      {name: 'true, 1', args: [true, 1], expected: false},
      {name: 'false, 0', args: [false, 0], expected: false},
      {name: 'false, 1', args: [false, 1], expected: true},
      /* write 4 more passing test cases with only strings */
      /* write 6 more passing test cases without NaN values*/
      /* write 4 more passing test cases with NaN values*/
    ];
  function less_than(a, b) {
    return a < b;
  }
  run_tests(less_than, test_cases);
}
```

[TOP](#inequalities)

---

## greater than or equal to

rules for implicit coercion:
* If both operands are numbers, perform a numeric comparison.
* If both operands are strings, compare the [character codes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/charCodeAt) for each. sort of like alphabetical order.
* If one operand is a number, convert the other operand to a number and perform a numeric comparison.
* careful of NaN and values that convert to NaN. 
```js
{
  const test_cases = [
      {name: 'true, 0', args: [true, 0], expected: true},
      {name: 'true, 1', args: [true, 1], expected: true},
      {name: 'false, 0', args: [false, 0], expected: true},
      {name: 'false, 1', args: [false, 1], expected: false},
      /* write 4 more passing test cases with only strings */
      /* write 6 more passing test cases without NaN values */
      /* write 4 more passing test cases with NaN values */
    ];
  function greater_than_or(a, b) {
    return a >= b;
  }
  run_tests(greater_than_or, test_cases);
}
```

[TOP](#inequalities)

---


## less than or equal to

rules for implicit coercion:
* If both operands are numbers, perform a numeric comparison.
* If both operands are strings, compare the [character codes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/charCodeAt) for each. sort of like alphabetical order.
* If one operand is a number, convert the other operand to a number and perform a numeric comparison.
* careful of NaN and values that cast to NaN. 
```js
{
  const test_cases = [
      {name: 'true, 0', args: [true, 0], expected: false},
      {name: 'true, 1', args: [true, 1], expected: true},
      {name: 'false, 0', args: [false, 0], expected: false},
      {name: 'false, 1', args: [false, 1], expected: false},
      /* write 4 more passing test cases with only strings */
      /* write 6 more passing test cases without NaN values*/
      /* write 4 more passing test cases with NaN values*/
    ];
  function less_than_or(a, b) {
    return a <= b;
  }
  run_tests(less_than_or, test_cases);
}
```

[TOP](#inequalities)

___
___
### <a href="http://janke-learning.org" target="_blank"><img src="https://user-images.githubusercontent.com/18554853/50098409-22575780-021c-11e9-99e1-962787adaded.png" width="40" height="40"></img> Janke Learning</a>

