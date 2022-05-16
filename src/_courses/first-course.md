---
layout: course
name:  "Основная информация о виртуальных машинах"
volume: 16 часов, 4 модуля
annotation: annotation
description: description about course
price_USD: 345634
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


