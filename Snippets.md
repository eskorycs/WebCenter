###### **Get Task Specification Value & format for document reference attribute**

###### Used in Execute Javascript Node:

```
var task = API.getTask();

var spec = task.getSpecification("rycs_javascript");
var specValue = task.getSpecification("rycs_javascript").getValue();

var newSpec = specValue.replace(new RegExp(" ", 'g'), " | ");
spec.setValue(newSpec);
```
