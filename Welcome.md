This is your new *vault*.

When you're ready, head to [[Obsidian Markdown Basics]]

Learn about linking notes here [[Research Overview]]

# Plugins
***Here are some popular plugins installed in this vault with examples of their use***
Install more plugins through the settings menu at the bottom
![[Pasted image 20240123173425.png]]
## Dataview
[Dataview (blacksmithgu.github.io)](https://blacksmithgu.github.io/obsidian-dataview/) 

Dataview allows you to search through notes and generate tables populated with relevant information and metadata. For example, a list with subject home pages from the folder "Subjects"

```dataview
List
From "Subjects"
```
#### A table with semester and exam dates

```dataview
Table semester as "Semester", exam as "Date of Exam"
from "Subjects" 
```


#### Maybe you want to know how long until the exam and sort it

```dataview
Table
exam - date(today) as "Days Until Exam"
from "Subjects"
sort exam - date(today) asc
```

#### What if we search for all notes containing the #subject

```dataview
Table semester as "Semester"
from #subject  
```


## Tasks
[Introduction - Tasks User Guide - Obsidian Publish](https://publish.obsidian.md/tasks/Introduction)
Obsidian Tasks turns your vault into a powerful task management platform

- [ ] Here is a simple task
- [x] Here is a completed task ✅ 2024-01-23

#### You can make tasks with - [ ] or by `Ctrl + P` and searching "Task"

- [ ] A task due today 📅 2024-01-24 
- [ ] What about tomorrow 📅 2024-01-25 
- [ ] What about this Sunday 📅 2024-01-28 


#### You can search for tasks across your whole vault just like dataview!
```tasks
```

#### What about ones due tomorrow?
```tasks
due tomorrow
```

#### What about ones due in the 7 days
```tasks
not done
due after 2024-01-24
due before in 7 days
short mode
sort by due by
```







## Templater
[GitHub - SilentVoid13/Templater: A template plugin for obsidian](https://github.com/SilentVoid13/Templater)
Obsidian natively supports templates for automating note creation, however this plugin greatly expands templates to automate everything from file names to links

Templates follow a very specific syntax found here [Introduction - Templater (silentvoid13.github.io)](https://silentvoid13.github.io/Templater/)which is quite complex and daunting for new users

I would recommend following other people's templates online for whatever functionality you need but [[Subject Template|here is an example to get started]]

`Ctrl + P` to open the command palette and search "Subject Template". This will create a new note in "Subjects"
Type the new name of the note when created and hit `Enter`


You will see your new note in the folder and also (for example) in something like [[Subjects Homepage]]
# Advanced Topics
*Contact me if you are having trouble implementing these methods*
## Automatic Daily Task List
Obsidian can be set up to automatically create a note for each day with all tasks you need to complete
Instructions can be found here
https://dannb.org/blog/2022/obsidian-daily-note-template/

An example of what this looks like in practice
![[Pasted image 20240123183419.png]]
The template I use for my notes [[Daily Note Template]]

## Literature Database
I have set up Obsidian to extract papers and my annotations from my Zotero reference manager
An example of what this looks like
![[Pasted image 20240123184024.png]]
Install the following plugin - https://github.com/mgmeyers/obsidian-zotero-integration

Follow Section 1 of the following link
https://archive.md/IscNA and use the template below

This assumes an understanding of Zotero (including highlighting and annotating within Zotero, managing files and updated bibtex exports)

Here is the [[Literature Note Template]] I use


