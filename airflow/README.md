# Apache Airflow

## Notes

These notes are based on DataCamp's "[Introduction to Airflow in Python](https://www.datacamp.com/courses/introduction-to-airflow-in-python)" course:

- Data Engineering tool.
- Workflows are implemented as DAGs (_set of tasks and dependencies between them_) in Python (it is possible to use Bash scripts, Python functions and other types of building blocks/_tasks_).
- Alternative: [Luigi](https://luigi.readthedocs.io/en/stable/).
- An error from the `airflow run` command returns an `airflow.exceptions.AirflowException` on the last line.
- Airflow is usually used combining the command line (and/or the UI) and Python.
- `Operators`:
  - Single tasks in workflows.
  - They usually run independently and do not share information (however, it may be possible). They are not guaranteed to run in the same location (directory)/environment.
  - In the case of the `BashOperator`, it may be necessary to set up a good number of environment variables. For example, the tilde character (`~`), which in Bash normally expands to the value of `$HOME`, is not defined by default in Airflow.

## Imports

```python
from airflow.models import DAG
from airflow.operators.bash_operator import BashOperator
from airflow.operators.python_operator import PythonOperator
from airflow.operators.http_operator import SimpleHttpOperator
```

## CLI commands

- Help commands:
  - `airflow -h`
  - `airflow webserver -h`
- List command: `airflow list_dags`
- Web server command: `airflow webserver`