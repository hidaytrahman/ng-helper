
# Angular5 Properties/ DOM Syntax


## 1.	Property Binding Example
 ```javascript 
  <img src="{{ angularLogo }}">
  <img [src]="angularLogo">
  <img bind-src="angularLogo">
```

- You can use interpolation to define the value, as long as the value you're defining is a string. If it's not, you must use method 2 or 3 below.
- The most common method to define property binding is by wrapping brackets around an element property and binding it to a component property.
- Adding bind- before the element property also achieves the same thing.

```javascript
export class AppComponent {
  
  angularLogo = 'https://angular.io/resources/images/logos/angular2/angular.png';

}
```


## 2.	Property Binding on the Disabled Attribute
```javascript
<button [disabled]="buttonStatus">My Button</button>
```
And add the **buttonStatus** property in the component class:
```javascript
   buttonStatus = true;
```

Because **buttonStatus** is _true_, the disabled attribute is applied to the button. If you change it to _false_, it becomes clickable.

You can also define a different template expression:
```javascript
<button [disabled]="buttonStatus == 'enabled'">My Button</button>
```
And change the **buttonStatus** property to:
```javascript
buttonStatus = 'enabled';
```

## 3. Parse HTML in Angular 5+

In case you have html in variable.
```javascript
 myField = "<h3>I am the heading 3 </h3>";
```

Here in html file just use **innerHtml** attribute
```javascript
 <div [innerHTML]="myField"></div>
 <div innerHTML="{{myField}}"></div>
```

## 4 Cannot read property 'name' of undefined

The safe navigation operator **( ?. )** and null property paths
**The Angular safe navigation operator (?.) is a fluent and convenient way to guard against null and undefined values in property paths.** Here it is, protecting against a view render failure if the currentHero is null.

```javascript
The current hero's name is {{anyObj?.name}}
```
[More Details [+]](https://angular.io/guide/template-syntax#!#ref-vars)
