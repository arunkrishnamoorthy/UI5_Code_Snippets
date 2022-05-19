# Sorter and Filters in Binding  

```xml 
<Select 
    items="{ 
        path : '/Orders', 
        sorter: { 
            path: 'OrderDate', 
            descending: true 
        }, 
        filters : [ 
            { path : 'ShipCountry', operator : 'EQ', value1 : 'Brazil'} 
        ] 
    }"> 
  ```
