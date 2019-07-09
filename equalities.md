# Equalities

Study [this comparison table](https://dorey.github.io/JavaScript-Equality-Table/).     
Play around with this [interactive table](https://janke-learning.org/equalities-coercion/).   
Then test yourself with [this quiz](https://eqeq.js.org). 
and study some [implicit coercion](https://github.com/janke-learning/implicit-coercion/blob/master/replicate-loose-equality.md).

Before moving on, check out the instructions and copy the ```run_tests``` function from [this repo's README.md](./README.md).

### Operators
* [a === b](#strict-equality)
* [a !== b](#strict-inequality)
* [a == b](#loose-equality)
* [a != b](#loose-inequality)

---

## strict equality

```js
{
  const test_cases = [
      {name: '3, 3', args: [3, 3], expected: true},
      {name: '3, "3"', args: [3, "3"], expected: false},
      /* write 8 more passing test cases */
    ];
  function strict_equality(a, b) {
    return a === b;
  }
  run_tests(strict_equality, test_cases);
}
```

[TOP](#equalities)

---


## strict inequality

```js
{
  const test_cases = [
      {name: '3, 3', args: [3, 3], expected: true},
      {name: '3, "3"', args: [3, "3"], expected: false},
      /* write 8 more passing test cases */
    ];
  function strict_inequality(a, b) {
    return a === b;
  }
  run_tests(strict_inequality, test_cases);
}
```

[TOP](#equalities)

---


## Loose Equality

```js
{
  const test_cases = [
      {name: 'null, undefined', args: [null, undefined], expected: true},
      {name: 'null, null', args: [null, null], expected: true},
      {name: 'undefined, undefined', args: [undefined, undefined], expected: true},
      {name: 'null, ""', args: [null, ""], expected: false},
      {name: 'null, 0', args: [null, 0], expected: false},
      {name: 'null, false', args: [null, false], expected: false},
      {name: 'undefined, ""', args: [undefined, ""], expected: false},
      {name: 'undefined, 0', args: [undefined, 0], expected: false},
      {name: 'undefined, false', args: [undefined, false], expected: false},
      {name: 'true, false', args: [true, false], expected: false},
      {name: 'true, true', args: [true, true], expected: true},
      {name: 'false, false', args: [false, false], expected: true},
      {name: '3, "3"', args: [3, "3"], expected: true},
      {name: 'true, 1', args: [true, 1], expected: true},
      {name: 'false, 0', args: [false, 0], expected: true},
      {name: 'true, " "', args: [true, " "], expected: false},
      {name: 'false, "', args: [false, ""], expected: true},
      {name: '0, ""', args: [0, ""], expected: true}
    ];
  function loose_equality(a, b) {
    return a == b;
  }
  run_tests(loose_equality, test_cases);
}
```


[TOP](#equalities)

---


## Loose Inequality

```js
{
  const test_cases = [
      {name: 'null, undefined', args: [null, undefined], expected: true},
      {name: 'null, null', args: [null, null], expected: true},
      {name: 'undefined, undefined', args: [undefined, undefined], expected: true},
      {name: 'null, ""', args: [null, ""], expected: false},
      {name: 'null, 0', args: [null, 0], expected: false},
      {name: 'null, false', args: [null, false], expected: false},
      {name: 'undefined, ""', args: [undefined, ""], expected: false},
      {name: 'undefined, 0', args: [undefined, 0], expected: false},
      {name: 'undefined, false', args: [undefined, false], expected: false},
      {name: 'true, false', args: [true, false], expected: false},
      {name: 'true, true', args: [true, true], expected: true},
      {name: 'false, false', args: [false, false], expected: true},
      {name: '3, "3"', args: [3, "3"], expected: true},
      {name: 'true, 1', args: [true, 1], expected: true},
      {name: 'false, 0', args: [false, 0], expected: true},
      {name: 'true, " "', args: [true, " "], expected: false},
      {name: 'false, "', args: [false, ""], expected: true},
      {name: '0, ""', args: [0, ""], expected: true}
    ];
  function loose_inequality(a, b) {
    return a != b;
  }
  run_tests(loose_inequality, test_cases);
}
```

___
___
### <a href="http://janke-learning.org" target="_blank"><img src="https://user-images.githubusercontent.com/18554853/50098409-22575780-021c-11e9-99e1-962787adaded.png" width="40" height="40"></img> Janke Learning</a>
