1. schema
2. options

# OVERVIEW

1. "PQ Question Form" should send info that includes...
- CLIENT ID
- RESULT INFO
    [{name_id: 1, name: "ss", whichpq: "general", ifsent: false}, {name_id: 2, ...}, ...]

2. Sender
- receives the info from "PQ question form"
- finds the client using CLIENT ID
- makes a task with RESULT INFO in its body
- create wordpress posts for each
- sends links to forms that contain TASK ID and NAME ID

3. Watcher
- update tasks using TASK ID and NAME ID in its RESULT INFO
- if in RESULT INFO, every ifsent is True -> check off the task
- redirect if sent pqs are accessed again
- delete pq link
- make another task saying "BOT: received every PQ"

4. Reminder
- filter through "Bot: PQ send tasks" and if a task is more than a certain time old and has not been checked off, grab the task
- send email to the client which pqs have not been received using RESULT INFO

# Todos

- git autocommit
- think of a way to implement google docs and google sheets
- database out of database (Notion)
- research on JSON security
- alpaca
    - dynamic forms and questions
    - multiple pages
    - progress bar
    - duque logo
    - perfect validation
- Make General and LMIA form with Alpaca
- Outline sender, reminder, watcher
- Strike the email issue

# Form

- How to change the content of the page according to the http code response
- "PQ question form" should send PQ info
    - PQ info: ["id", "name", "whichpq"]
- "PQ form"

# Doc <-> sheet <-> form

- Apps script + GitHub
- make a change to sheet then update the doc through apps script then update the form through github

# Learn

- ajaxSubmit function (promist object)
- postRender

# Progress

- [x] Develop Sender
- [x] Develop Reminder
- [x] Develop PQ Watcher
- [] Create website general form
- [ ] Integrate those

- [ ] Develop Booking Watcher
- [ ] Refactor & Optimize & Organize

- [ ] Testing (general only)

- [ ] Create website other forms
- [ ] Testing (others)

- [ ] Make logic for PQ (w4 JS)
- [ ] Integrate it to the app

- [ ] Final testing

- [ ] Publish