---
layout: unit
name:  "course 2, unit 2"
position: position
course: second

--- 
### Unit:
```
<%= raw JSON.pretty_generate(resource.data) %>
```

### Units Course: 

```
<%= raw JSON.pretty_generate(resource.relations.course.data) %>
```