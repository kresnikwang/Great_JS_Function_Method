
##Angular JS中增加回车功能的方法
JS:
```
app.directive('ngEnter', function () {
    return function (scope, element, attrs) {
        element.bind("keydown keypress", function (event) {
            if(event.which === 13) {
                scope.$apply(function (){
                    scope.$eval(attrs.ngEnter);
                });

                event.preventDefault();
            }
        });
    };
});
```

HTML:
```
<div ng-app="" ng-controller="MainCtrl">
    <input type="text" ng-enter="doSomething()">    
</div>
```