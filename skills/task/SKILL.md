---
name: task
description: Manage tasks and to-dos. Use when the user wants to create, list, assign, or complete tasks.
---

Help the user manage tasks based on "$ARGUMENTS".

Available actions:
- **Create**: Use `create_task` — needs title, optional assignee and priority
- **List**: Use `list_tasks` or `get_my_tasks` — show pending work
- **Overview**: Use `get_task_overview` — summary of all tasks by status
- **Update**: Use `update_task` — change title, description, priority
- **Move**: Use `move_task` — change status (todo, in_progress, done)
- **Complete**: Use `complete_task` — mark as done
- **Assign**: Use `assign_task` — delegate to a team member
- **Delete**: Use `delete_task` — remove a task

If the user just says "tasks" with no context, show their task overview with `get_task_overview`.
