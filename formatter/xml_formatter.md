# Formatter - XML Code 

Following examples are code for formatting the data at the binding level in XML Views. 

## Decimal Formatter 

maxFractionDigits - property need to be set to format the decimal places 

```xml
<Text text="{ path: 'attribute', type:'sap.ui.model.type.Float', formatOptions : { maxFractionDigits: 2}}"></Text> 
```

## Date Formatter 
Pattern of format options needs to be set to format the date in specified format.
Type of the attribue needs to be date. 

```xml
<ObjectAttribute title="Attribue Name" text="{ path: 'attribute', type: 'sap.ui.model.type.Date', formatOptions: { pattern: 'yyyy/MM/dd' } }"/> 
```
## Time Formatter 

## Currency Formatter

## Delete Leading Zeros 

## Convert the Data to Float 

## UTC: true 
The UTC property of the Date control needs to be set to avoid error where OData receives the date one day less selected from the UI. 
