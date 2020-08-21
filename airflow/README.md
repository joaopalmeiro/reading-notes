# Apache Airflow

## Notes

These notes are based on DataCamp's "[Introduction to Airflow in Python](https://www.datacamp.com/courses/introduction-to-airflow-in-python)" course:

- Data Engineering tool.
- Workflows are implemented as DAGs (_set of tasks and dependencies between them_) in Python (it is possible to use Bash scripts, Python functions, and other types of building blocks/tasks).
- Alternative: [Luigi](https://luigi.readthedocs.io/en/stable/).
- An error from the `airflow run` command returns an `airflow.exceptions.AirflowException` on the last line.
- Airflow is usually used by combining the command line (and/or the UI) and Python.
- Operators:
  - Single tasks in workflows. In other words, tasks are instances of operators.
  - They usually run independently and do not share information (however, it may be possible). They are not guaranteed to run in the same location (directory)/environment.
  - In the case of the `BashOperator`, it may be necessary to set up a good number of environment variables. For example, the tilde character (`~`), which in Bash normally expands to the value of `$HOME`, is not defined by default in Airflow.
  - They are only executed once per DAG run.
- Within Airflow, tasks are referred to by the `task_id` and not by the Python variable name.
- As of Airflow 1.8, task dependencies are defined using bitwise operators:
  - `>>`: Upstream (_before_, that is, an upstream task appears _before_ a downstream task) operator.
  - `<<`: Downstream (_after_) operator.
- There are more operators in the [`airflow.contrib.operators`](https://airflow.apache.org/docs/stable/_api/airflow/contrib/operators/index.html) module.
- DAG run: A workflow instance at a point in time.
- The `start_date` parameter is defined with a Python [`datetime`](https://docs.python.org/3/library/datetime.html) object.
- The `start_date` and `end_date` parameters are the _minimum_ and _maximum_ values for scheduling a DAG. The `schedule_interval` parameter defines how often a DAG is scheduled (the `None` value is used for manually triggered DAGs).
- The first DAG run occurs only on the date corresponding to _`start_date` + `schedule_interval`_.
- Sensor: An operator that waits for a certain condition to be true.
- The `poke_interval` parameter must be set to (at least) 1 minute (in seconds) to avoid overloading the Airflow scheduler.
- Executors:
  - They run tasks.
  - `SequentialExecutor`:
    - It is the default executor that runs one task at a time (something that can be useful for debugging).
    - It is not recommended for production.
  - `LocalExecutor`: Each task is a process on the local system (\#parallelism).
  - `CeleryExecutor`:
    - [Celery](https://docs.celeryproject.org/en/stable/index.html): It is a queueing system (written in Python).
    - It is more difficult to configure as it is necessary to configure a Celery backend/broker (such as [RabbitMQ](https://www.rabbitmq.com/), for example) before Airflow and it is necessary to prepare a way to share DAGs between workers (such as a Git server, for example).
- The `dags_folder` path must be absolute in the `airflow.cfg` file.
- In Apache Airflow, an SLA refers to the amount of time that a task/DAG should require to run.
- The `sla` parameter is defined with a Python [`timedelta`](https://docs.python.org/3/library/datetime.html) object. The `microseconds` and `milliseconds` arguments are not used.
- [Jinja](https://jinja.palletsprojects.com/) is available as a templating engine for Airflow.
- There are some (Airflow built-in runtime) variables that can be used in templates. On the other hand, macros allow the use of several objects/methods, such as `{{ macros.datetime }}` (the Python `datetime` object), in templates. A list can be found [here](https://airflow.apache.org/docs/stable/macros-ref.html).
- Creating individual tasks, instead of creating a single task that receives a list and a template with a loop, for example, allows for better monitoring of task state and potential parallel execution.
- Branching: It introduces conditional logic in Airflow, that is, it allows tasks to be executed or skipped according to the result of an operator.
- The `provide_context` parameter of `BranchPythonOperator` allows access to the runtime variables and macros to its function (`python_callable`). This function must accept `**kwargs`.
- Other operators also accept the `provide_context` parameter.
- Instead of `**kwargs`, use `**context` (code style).

## Imports

```python
from datetime import datetime, timedelta

from airflow.contrib.sensors.file_sensor import FileSensor
from airflow.models import DAG
from airflow.operators.bash_operator import BashOperator
from airflow.operators.dummy_operator import DummyOperator
from airflow.operators.email_operator import EmailOperator
from airflow.operators.http_operator import SimpleHttpOperator
from airflow.operators.python_operator import BranchPythonOperator, PythonOperator
```

## Commands

- Help commands:
  - `airflow -h`
  - `airflow webserver -h`
- List command (also useful for debugging): `airflow list_dags`
- Web server command: `airflow webserver`
- Run a task: `airflow run <dag_id> <task_id> <date>`
- Run a DAG: `airflow trigger_dag -e <date> <dag_id>`
- Test a task: `airflow test <dag_id> <task_id> <date>`
  - It is possible to use `-1` instead of a specific `<date>`.
