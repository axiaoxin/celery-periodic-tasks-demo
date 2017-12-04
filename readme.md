# Celery periodic task demo


### Run

cd into the root path of the project


- running a celery worker for consuming the tasks

    celery worker -A app -l debug

- running a celery beat for producing the tasks

    celery beat -A app -l debug


### Add task

1. Write the tasks code.

Write the new task code like `print_tasks.py` in the tasks directory.

For more information <http://docs.celeryproject.org/en/latest/userguide/index.html>

2. Update `config.py`

Add the new task script into `imports` list, then set the new beat schedules like the `print_tasks`

For more information <http://docs.celeryproject.org/en/latest/userguide/periodic-tasks.html>
