# Expression Binding 

Simple calculation on the data before displaying the data can be performed at binding level using simple expressions. For complex scenarios we would still need the formatter function to format the data, while expression binding can be used for simple transformation. 

The Javascript conditional operator is used as the expression binding. 

```javascript
  (condition) ? true : false;
```
if the condition is true, the true statement after the question marks gets executed. 
if the condition is false, the false statement after the colon gets executed. 

Formatting data based on true or false value. 

```xml
<Text text="Hello world!" visible="{= ${bindingAttribute} ? false : true }"></Text>
```

Formatting data based on simple value check. 
```xml
<ObjectListItem
            title="{invoice>Quantity} x {invoice>ProductName}"
            number="{
		parts: [{path: 'invoice>ExtendedPrice'}, {path: 'view>/currency'}],
		type: 'sap.ui.model.type.Currency',
		formatOptions: {
			showMeasure: false
		}
		}"
		numberUnit="{view>/currency}"
        	numberState="{= ${invoice>ExtendedPrice} > 50 ? 'Error' : 'Success' }"/>
```
