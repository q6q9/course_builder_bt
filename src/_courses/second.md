---
layout: course
name:  "Стратегическое управление в образовании: методология и
кейсы проектных решений"
volume: 24 час. 6 модулей
annotation: annotation
description: description about course
price_USD: 300
--- 

### Course: 

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

