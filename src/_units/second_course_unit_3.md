---
layout: unit
name:  "course 2, unit 3"
position: position
course: second

--- 
### Unit:
```
<%= raw JSON.pretty_generate(resource.data) %>
```

### Unit Course: 

```
<%= raw JSON.pretty_generate(resource.relations.course.data) %>
```