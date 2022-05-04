---
layout: unit
name:  "course 1, unit 2"
position: position
course: first-course
--- 
### Unit:
```
<%= raw JSON.pretty_generate(resource.data) %>
```

### Units Course: 

```
<%= raw JSON.pretty_generate(resource.relations.course.data) %>
```