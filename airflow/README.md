# Apache Airflow

## Notes

- Data Engineering tool.
- Workflows are implemented as DAGs (_set of tasks and dependencies between them_) in Python (it is also possible to use Bash scripts and other components).
- Alternative: [Luigi](https://luigi.readthedocs.io/en/stable/).
- An error from the `airflow run` command returns `airflow.exceptions.AirflowException` on the last line.
- Help command: `airflow -h`.
- Airflow is usually used combining the command line and Python.
