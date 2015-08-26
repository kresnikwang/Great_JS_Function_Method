##Excel Sheet Column Title

Given a positive integer, return its corresponding column title as appear in an Excel sheet.
```
For example:

    1 -> A
    2 -> B
    3 -> C
    ...
    26 -> Z
    27 -> AA
    28 -> AB
```    
    
[https://leetcode.com/problems/excel-sheet-column-title/](https://leetcode.com/problems/excel-sheet-column-title/)

```
var numberToColumn = function(number){

    var columnName ="";
    var codeA = "A".charCodeAt();

    while(number > 0){
    number--;
    columnName = String.fromCharCode(codeA+number%26) + columnName;
    number = parseInt(number / 26);
 	}

    return columnName;

};

```