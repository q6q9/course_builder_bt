---
layout: course
name:  "second course"
volume:   volume
annotation: annotation
description: description about course
--- 

### Course: 

```
<%= raw JSON.pretty_generate(resource.data) %>
```

### Units of this course:
```
<%= raw JSON.pretty_generate(resource.relations.units.map {|unit| unit.data}) %>
```

