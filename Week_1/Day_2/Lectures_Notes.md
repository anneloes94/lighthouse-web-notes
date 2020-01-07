### Functions

#### Naming functions

1. avoid generic names like 'data', or 'run'
2. name your functions beginning with action words like createUser, or sendUserData
3. be consistent with your naming conventions
4. if you're joining an existing project, observe and adapt any existing conventions


When naming a function, pick out the single concept that it is about.

From:
```javascript
function printZeroPaddedWithLabel(number, label) {
  let numberString = String(number);
  while (numberString.length < 3) {
    numberString = "0" + numberString;
  }
  console.log(`${numberString} ${label}`);
}
```

To:
```javascript
function zeroPad(number, width) {
  let string = String(number);
  while (string.length < width) {
    string = "0" + string;
  }
  return string;
}

function printFarmInventory(cows, chickens, pigs) {
  console.log(`${zeroPad(cows, 3)} Cows`);
```

#### Function types
Functions can be roughly divided into those that are called for their `side effects` and those that are called for their `return value`

A `pure function` is a specific kind of value-producing function that not only has `no side effects` but also `doesn’t rely on side effects from other code`—for example, it doesn’t read global bindings whose value might change. A pure function has the pleasant property that, when called with the same arguments, it always produces the same value (and doesn’t do anything else

#### indentation
JS uses `two spaces` (although still functional when you use tabs, etc.).