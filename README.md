In This demo setup of dbt environment
I am using Poetry to setup the virtual environment

<!-- Installing Poetry -->
See documentation here : https://python-poetry.org/docs/
osx / linux / bashonwindows install instructions
run this command in terminal
`curl -sSL https://raw.githubusercontent.com/python-poetry/poetry/master/get-poetry.py | python3 -`

on windows powershell install instructions
run this command at shell
`(Invoke-WebRequest -Uri https://raw.githubusercontent.com/python-poetry/poetry/master/get-poetry.py -UseBasicParsing).Content | python3 -`


To confirm if Poetry is installed successfuly by
`poetry --version`


To setup Virtual enviroment

Navigate to your Drsktop or a directory in which you want to create your working directory,
run this command at terminal
`poetry new poetry-demo` where `poetry-demo` is the name of new folder for your project

The content of newly created directory will look like this
`poetry-demo
├── pyproject.toml
├── README.rst
├── poetry_demo
│   └── __init__.py
└── tests
    ├── __init__.py
    └── test_poetry_demo.py`

If you are using existing empty directory, run this 
`poetry install`

then activate the env by running
`poetry shell`

<!-- Installing DBT with Poetry -->
in the acticated env above, run the below command
`poetry add dbt-core dbt-postgres` Please, pay attention, package are seperated by space, no comma. Also, `dbt-postgres` can be replace with other such as `dbt-snowflake` etc

<!-- Initialize dbt -->

In the actiavted env, run below command
`dbt init`


That's all wit poetry with dbt