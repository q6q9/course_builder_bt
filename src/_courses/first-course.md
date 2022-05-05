---
layout: course
name:  "name of course"
volume:   volume
annotation: annotation
description: description about course
--- 

### Course
```
<%= raw JSON.pretty_generate(resource.data) %>
```

### Units of this course:
```
<%= raw JSON.pretty_generate(resource.relations.courses_units
        .map {|course_unit| course_unit.relations.unit.data}
        .uniq {|unit| unit.name}
    ) 
%>
```


