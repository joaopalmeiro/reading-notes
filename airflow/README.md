# Apache Airflow

## Notes

These notes are based on DataCamp's "[Introduction to Airflow in Python](https://www.datacamp.com/courses/introduction-to-airflow-in-python)" course:

- Data Engineering tool.
- Workflows are implemented as DAGs (_set of tasks and dependencies between them_) in Python (it is also possible to use Bash scripts and other components).
- Alternative: [Luigi](https://luigi.readthedocs.io/en/stable/).
- An error from the `airflow run` command returns `airflow.exceptions.AirflowException` on the last line.
- Airflow is usually used combining the command line (and/or the UI) and Python.

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
