---
layout: unit
name:  "unit 2"
position: 2
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
        .uniq {|unit| unit.name}
    )
%>
```