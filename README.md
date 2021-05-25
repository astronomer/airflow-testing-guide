# airflow-testing-guide

This repo contains example Airflow DAGs with a DAG validation test suite to show how you can implement automated testing of your DAGs as part of a CI/CD workflow. A guide with an in-depth explanation of how to test Airflow DAGs will be published soon. 

DAG validation tests are written using `pytest` and can be found in the `test_dag_validation.py` file. The example tests include:

 - A test to ensure DAGs have no import errors (`test_no_import_errors()`)
 - A test to ensure all DAGs have global retries set to 2 (`test_retries_present()`)

The tests are then run as part of the GH Actions workflow `CI`, which executes the tests before deploying the project to an Astronomer Airflow deployment.
