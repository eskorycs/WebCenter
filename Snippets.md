###### **Get Task Specification Value & format for document reference attribute**

###### Used in Execute Javascript Node:

```
var task = API.getTask();

var spec = task.getSpecification("rycs_javascript");
var specValue = task.getSpecification("rycs_javascript").getValue();

var newSpec = specValue.replace(new RegExp(" ", 'g'), " | ");
spec.setValue(newSpec);
```

###### **Get Current Project Name, Extract 1st/2nd parts, append new description**

###### Used in Execute Javascript Node or Rules Engine:
```
// Get project current name
var project = API.getProject();
var currentName = project.getName();
var sliceCurrentName = currentName.slice(0, currentName.lastIndexOf('_'));

// Get project shortname attribute
var currentShortName = project.getAttribute('PROJ_Short name').getValue();

// Rename Project with new short name
var newName = sliceCurrentName + "_" + currentShortName;
project.setName(newName);
'''
