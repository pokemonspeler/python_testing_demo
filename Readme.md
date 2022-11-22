[![Deployment to Staging](https://github.com/pokemonspeler/python_testing_demo/actions/workflows/python_on_push_master.yml/badge.svg?branch=master)](https://github.com/pokemonspeler/python_testing_demo/actions/workflows/python_on_push_master.yml)
[![Deployment to Production](https://github.com/pokemonspeler/python_testing_demo/actions/workflows/python_on_release.yml/badge.svg)](https://github.com/pokemonspeler/python_testing_demo/actions/workflows/python_on_release.yml)
## run unit test

Place the development code and test code in separate directories. It’s a good practice to store the test code in the
test directory.  
Use the command `python -m unittest discover -v` to discover and execute all the tests.  
Use the command `python -m unittest tests.test_circle -v` to run a single test module.  
Use the command `python -m unittest tests.test_circle.TestCircle -v` to run a single test class.  
Use the command `python -m unittest tests.test_circle.TestCircle.test_area -v` to run a single test method.

## generate a coverage report

Use the `python -m coverage run --source=app --branch -m unittest` command to gather coverage data  
the `python -m coverage report` command to generate a coverage report.  
the `python -m coverage report -m` command to generate a coverage report with the missing lines.  
the `python -m coverage report -m --skip-covered` command to generate a coverage report with the missing lines only show
not fully covert files.  
Use the `python -m coverage html` to generate the test coverage report in HTML format.  
Use the `python -m coverage json` to generate the test coverage report in json format.  
Use the `python -m coverage json --pretty-print` to generate the test coverage report in pretty json format.  
Use the `python -m coverage xml` to generate the test coverage report in xml format.

## ignoring known untested lines

To ignore a line that is not tested add `# pragma: no cover` at the end of the line of code.

## sources

https://docs.github.com/en/actions/automating-builds-and-tests/building-and-testing-python
https://docs.github.com/en/actions/using-jobs/using-conditions-to-control-job-execution
https://docs.github.com/en/actions/learn-github-actions/environment-variables
https://docs.python.org/3/library/unittest.html
https://www.pythontutorial.net/python-unit-testing/python-run-unittest/
https://www.pythontutorial.net/python-unit-testing/python-unittest-coverage/
https://coverage.readthedocs.io/en/6.5.0/
https://docs.github.com/en/actions/using-workflows/reusing-workflows#calling-a-reusable-workflow