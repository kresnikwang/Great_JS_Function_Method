
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