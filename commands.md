## run unit test

Place the development code and test code in separate directories. It’s a good practice to store the test code in the test directory.  
Use the command `python -m unittest discover -v` to discover and execute all the tests.  
Use the command `python -m unittest tests.test_circle -v` to run a single test module.  
Use the command `python -m unittest tests.test_circle.TestCircle -v` to run a single test class.  
Use the command `python -m unittest tests.test_circle.TestCircle.test_area -v` to run a single test method.  

## generate a coverage report

Use the `python -m coverage run -m unittest` command to gather coverage data  
the `python -m coverage report` command to generate a coverage report.  
Use the python -m coverage html to generate the test coverage report in HTML format.  