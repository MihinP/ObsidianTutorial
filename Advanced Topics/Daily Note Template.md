---
created: <% tp.file.creation_date() %>
---
Tags: #dailynote
___
# <% moment(tp.file.title,'YYYY-MM-DD').format("dddd, MMMM DD, YYYY") %>
<< [[<% fileDate = moment(tp.file.title, 'YYYY-MM-DD-dddd').subtract(1, 'd').format('YYYY-MM-DD-dddd') %>|Yesterday]] | [[<% fileDate = moment(tp.file.title, 'YYYY-MM-DD-dddd').add(1, 'd').format('YYYY-MM-DD-dddd') %>|Tomorrow]] >>
___
### Overdue Tasks
```tasks
not done
due before {{date:YYYY-MM-DD}}
short mode
sort by due
```
### Due Today
```tasks
due on {{date:YYYY-MM-DD}}
not done
short mode
```
___
## Today's Notes
<% tp.file.cursor() %>
___
### Due In Next 7 Days
```tasks
not done
due after {{date:YYYY-MM-DD}}
due before in 7 days
short mode
sort by due by
```
___
### Tasks Completed Today
```tasks
	done {{date:YYYY-MM-DD}}
	
```

### Notes Created Today
```dataview
LIST
WHERE file.cday = date({{date:YYYY-MM-DD}})
SORT file.ctime asc
```
### Notes Modified Today
```dataview
LIST
WHERE file.mday = date({{date:YYYY-MM-DD}})
SORT file.mtime asc
```
