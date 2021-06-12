## Read this article

Read the article https://codeburst.io/learn-and-understand-recursion-in-javascript-b588218e87ea to better understand recursion.

## Solve the following problems using recursion:

- Write a function named `repeater` that takes an input character and returns that character repeated 5 times using recursion. For example, if the input is 'g', then the output should be 'ggggg'.

```js
// Test
let val = "";
function repeater(str) {
  if (val.length <= 5) {
    val = val + str;
    repeater(str);
  }
  return val;
}
console.log(repeater("g")); // 'ggggg'
console.log(repeater("j")); // 'jjjjj'
```

- Write a function named `loop` that loops through the numbers n down to 0. Each time it will log the value.

```js
// Test

function loop(n) {
  if (n < 0) {
    return;
  }
  console.log(n);
  loop(--n);
}

console.log(loop(10)); // 10 9 8 7 6 5 4 3 2 1 0
console.log(loop(4)); // 4 3 2 1 0
```

- Write a function `countTo` that takes one argument limit and logs the number from 0 to limit

```js
// Test
let counter = 0;
function countTo(num) {
  if (counter > num) {
    return;
  }
  console.log(counter);
  counter += 1;
  counTo(num);
}
console.log(countTo(10)); // 0 1 2 3 4 5 6 7 8 9 10
console.log(countTo(4)); // 0 1 2 3 4
```

- Write a function `exponent` that takes two arguments base, and expo. Using a while loop return the exponent value of the base. For example if the base if `4` and expo is `3` the output will be `4 * 4 * 4` i.e 64.

```js
// Test

function exponent(base, expo) {
  let num = base;
  while (expo > 1) {
    num *= base;
    expo--;
  }
  return num;
}

console.log(exponent(2, 3)); // 8
console.log(exponent(3, 3)); // 27
```

- Write a function factorial that take 1 argument 'number' and gives the factorial of the number. For example if the number of 4 the output will be `4 * 3 * 2 * 1` i.e 24.

```js
// Test

function factorial(num) {
  if (num < 0) return;
  if (num === 0) return 1;
  co;
  return num * factorial(--num);
}

// Test
console.log(factorial(3)); // 6
console.log(factorial(5)); // 120
```

- Write a function `recursiveExponent` that takes two arguments base, and expo. It will return the output using recursion. For example if the base if `4` and expo is `3` the output will be `4 * 4 * 4` i.e 64.

```js
// Test
function recursiveExponent(base, expo) {
  if (expo === 1) return base;
  return base * recursiveExponent(base, --expo);
}

// Test
console.log(recursiveExponent(2, 3)); // 8
console.log(recursiveExponent(3, 3)); /27
```

- Write a function `recursiveReverse` that takes an array and uses recursion to return its contents in reverse

```js
// Test
let final = [];
function recursiveReverse(arr) {
  let elm = arr.pop();
  final.push(elm);
  if (arr.length === 0) {
    return final;
  }
  return recursiveReverse(arr);
}
console.log(recursiveReverse([1, 3, 4, 5])); // [5, 4, 3, 1]
console.log(recursiveReverse([5, 3, 2, 1])); // [1, 2, 3, 5]
```
