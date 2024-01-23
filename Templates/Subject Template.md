---
creation date: <% tp.file.creation_date() %>
modification date: <% tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
meta1: this will automatically generate file creation dates
exam: 
semester:
---
[[Subjects Homepage]]

## Uni Tasks Due Today
This block will show tasks from your uni subjects due on the day you made this note
<%* /* It **will not** render properly until called by the Templater function */ -%>


```tasks
due on <% tp.date.now("YYYY-MM-DD") %>
filter by function task.file.folder === "Subjects/"
not done
```

<%* /*This command moves the created note to the Subjects folder - it will not show in the final note*/ -%>
<% await tp.file.move("Subjects/" + tp.file.title) %>
