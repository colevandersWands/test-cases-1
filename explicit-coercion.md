# Explicit Coercion

Write a bunch of test cases for explicit type coercions in JavaScript.

Before moving on, check out the instructions and copy the ```run_tests``` function from [this repo's README.md](./README.md).

### Coercions
* [String(a)](#string)
* [Number(a)](#number)
* [Boolean(a)](#boolean)
* [void a](#void)


---

## String

```js
{
  const test_cases = [
      {name: '3', args: [3], expected: "3"},
      {name: 'true', args: [true], expected: 'true'},
      /* write 8 more passing test cases, 
         be sure to test all 5 types! */
    ];
  function _string(a) {
    return String(a);
  }
  run_tests(_string, test_cases);
}
```

[TOP](#explicit-coercion)

---

## Number

```js
{
  const test_cases = [
      {name: 'null', args: [null], expected: 0},
      {name: 'undefined', args: [undefined], expected: NaN},
      /* write 15 more passing test cases, 
         be sure to test all 5 types! */
    ];
  function _number(a) {
    return Number(a);
  }
  run_tests(_number, test_cases);
}
```

> [NaN](https://github.com/janke-learning/primitive-types/blob/master/nan.md)

[TOP](#explicit-coercion)

---

## Boolean

```js
{
  const test_cases = [
      {name: 'null', args: [null], expected: false},
      {name: 'undefined', args: [undefined], expected: false},
      /* write 15 more passing test cases, 
         be sure to test all 5 types! */
    ];
  function _boolean(a) {
    return Boolean(a);
  }
  run_tests(_boolean, test_cases);
}
```

> [truthiness](https://github.com/janke-learning/truthiness)

[TOP](#explicit-coercion)

---

## void

```js
{
  const test_cases = [
      {name: 'null', args: [null], expected: undefined},
      {name: 'undefined', args: [undefined], expected: undefined},
      /* write 8 more passing test cases, 
         be sure to test all 5 types! */
    ];
  function _void(a) {
    return void a;
  }
  run_tests(_void, test_cases);
}
```

> [null vs. undefined](https://github.com/janke-learning/primitive-types/blob/master/null-vs-undefined.md)

[TOP](#explicit-coercion)

___
___
## <a href="http://janke-learning.org" target="_blank"><img src="https://user-images.githubusercontent.com/18554853/50098409-22575780-021c-11e9-99e1-962787adaded.png" width="40" height="40"></img> Janke Learning</a>
