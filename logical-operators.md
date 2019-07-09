# Logical Operators

check out [operators of truthiness](https://github.com/janke-learning/truthiness/blob/master/operators-of-truthiness.md) and [boolean by example](https://github.com/janke-learning/boolean-by-example) for more practice.

Before moving on, check out the instructions and copy the ```run_tests``` function from [this repo's README.md](./README.md).

### Operators
* [a || b](#or)
* [a && b](#and)
* [!a](#not)
* [a ? b : c](#ternary)

---

## or

```js
{
  const test_cases = [
      {name: '1, 1', args: [1, 1], expected: 1},
      {name: '0, 1', args: [0, 1], expected: 1},
      {name: '1, 0', args: [1, 0], expected: 1},
      {name: '0, 0', args: [0, 0], expected: 0},
      /* write 10 more passing test cases */
    ];
  function or(a, b) {
    return a || b;
  }
  run_tests(or, test_cases);
}
```

[TOP](#logical-operators)

---

## and

```js
{
  const test_cases = [
      {name: '1, 1', args: [1, 1], expected: 1},
      {name: '0, 1', args: [0, 1], expected: 0},
      {name: '1, 0', args: [1, 0], expected: 0},
      {name: '0, 0', args: [0, 0], expected: 0},
      /* write 10 more passing test cases */
    ];
  function and(a, b) {
    return a && b;
  }
  run_tests(and, test_cases);
}
```

[TOP](#logical-operators)

---

## not

```js
{
  const test_cases = [
      {name: '1', args: [1], expected: false},
      {name: '0', args: [0], expected: true},
      /* write 10 more passing test cases */
    ];
  function not(a) {
    return !a;
  }
  run_tests(not, test_cases);
}
```

[TOP](#logical-operators)

---

## ternary

```js
{
  const test_cases = [
      {name: '1, "x", "y"', args: [1, 'x', 'y'], expected: 'x'},
      {name: '0, "x", "y"', args: [0, 'x', 'y'], expected: 'y'},
      /* write 10 more passing test cases */
    ];
  function ternary(a, b, c) {
    return a ? b : c ;
  }
  run_tests(ternary, test_cases);
}
```

[TOP](#logical-operators)

___
___
## <a href="http://janke-learning.org" target="_blank"><img src="https://user-images.githubusercontent.com/18554853/50098409-22575780-021c-11e9-99e1-962787adaded.png" width="40" height="40"></img> Janke Learning</a>
