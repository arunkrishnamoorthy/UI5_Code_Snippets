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
<ObjectAttribute title="Attribue Name" text="{ path: 'attribute', type: 'sap.ui.model.type.Date', 
                                             formatOptions: { pattern: 'yyyy/MM/dd' } }"/> 
```
## Time Formatter 

Use the pattern to format the time. 
yyyy - Year
MM - Month 
dd - Time 
HH - Hours 
MM - Minutes
SS - Seconds

```xml
<ObjectAttribute title="Attribute Name" 
                 text="{ path: 'attribute', type: 'sap.ui.model.type.Date',
                       formatOptions: { pattern: 'yyyy/MM/dd HH:MM:SS' } }"/> 
```


## Currency Formatter

showMeasure property of the formatOptions needs to be set and type of property needs to be set to Currency.

```xml
<Text text="{ parts: [{ path: 'amount' },{ path: 'currency'}], 
            type: 'sap.ui.model.type.Currency',
            formatOptions: { showMeasure: false }}"></Text> 
```

## Delete Leading Zeros 

Use isDigitSequence of Constraints to delete padding zeros. 

```xml
<Text text="{ 
    path : 'attribute',  
    type : 'sap.ui.model.odata.type.String',  
    constraints: {  
         isDigitSequence : true, 
         maxLength : 10 
    } 
}"/> 
```

## Convert the Data to Float 

## UTC: true 
The UTC property of the Date control needs to be set to avoid error where OData receives the date one day less selected from the UI. 

