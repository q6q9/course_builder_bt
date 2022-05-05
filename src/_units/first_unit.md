---
layout: unit
name:  "unit 1"
position: 1
course: 
    - first-course
    - second
--- 
### Unit:
```
<%= raw JSON.pretty_generate(resource.data) %>
```

### Courses (<%= resource.relations.courses_units.count %>): 

```
<%= raw JSON.pretty_generate(resource.relations.courses_units
        .map {|course_unit| course_unit.relations.course.data}
        .uniq {|course| course.name}
    ) 
%>
```