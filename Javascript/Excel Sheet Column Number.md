##Excel Sheet Column Number

In my grid the column headers are named A,B,C...,AA,AB,AC,...etc like an excel spreadsheet. How can I convert the string to number like: A => 1, B => 2, AA => 25

```
var foo = function(val) {
  var base = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ', i, j, result = 0;

  for (i = 0, j = val.length - 1; i < val.length; i += 1, j -= 1) {
    result += Math.pow(base.length, j) * (base.indexOf(val[i]) + 1);
  }

  return result;
};

console.log(['A', 'AA', 'AB', 'ZZ'].map(foo)); // [1, 27, 28, 702]

```