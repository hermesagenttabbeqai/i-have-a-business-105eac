# Business Requirements: Business Kanban Board

## Goal

A web-based kanban board that helps a business team track and manage tasks visually. Every team member can see all tasks and move them through three stages. Managers can create and assign tasks to employees.

## Users

- **Employees**: all team members. Can view all tasks, move cards between columns, and update task details.
- **Managers**: can create tasks, assign them to any team member, and delete tasks.
- Each person logs in with their own account so actions are traceable.

## Business requirements

| ID    | Requirement |
|-------|-------------|
| BR-01 | Any logged-in user can view the full kanban board with all tasks. |
| BR-02 | The board has exactly three columns: TODO, In Progress, and Ready. |
| BR-03 | A manager can create a new task with a title, description, and assignee. |
| BR-04 | A manager can assign or reassign a task to any team member. |
| BR-05 | Any logged-in user can move a task from one column to another by dragging it or using a button. |
| BR-06 | Each task card shows its title, assignee name, and current column. |
| BR-07 | A manager can delete a task. |
| BR-08 | Each user logs in with a unique username and password. |
| BR-09 | A manager can create user accounts for new employees. |
| BR-10 | The board updates so that all users see the latest state without needing to refresh the page manually. |

## Quality requirements

- NFR-01: The board loads in under 3 seconds on a desktop browser and a mobile browser over a standard connection.
- NFR-02: The interface works correctly on desktop browsers (Chrome, Firefox, Edge) and on mobile browsers (iOS Safari, Android Chrome).
- NFR-03: The layout adjusts to phone screen sizes so all columns and cards are readable without horizontal scrolling.
- NFR-04: Each user can only see and interact with their own session; no one can act as another user.
- NFR-05: Passwords are stored securely and never shown in plain text anywhere in the system.

## Not included

- Email or push notifications for task changes.
- File or image attachments on tasks.
- Time tracking or deadlines on tasks.
- Integration with any third-party tools (Slack, Jira, etc.).
- Reporting or analytics dashboards.

## Decisions

- **Login system**: each person has their own account with a username and password, so actions can be traced to the right person. Chosen because the user confirmed this is needed.
- **Columns order**: TODO → In Progress → Ready, matching the user's stated order.
- **Real-time updates**: the board refreshes automatically so the team always sees the current state without a manual page reload.
