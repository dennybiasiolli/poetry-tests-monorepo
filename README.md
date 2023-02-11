# Poetry playground with monorepo


## Setup projects

```sh
PROJECT_NAME=package_n
poetry --directory $PROJECT_NAME env use 3.10
poetry --directory $PROJECT_NAME install --no-root
```


## Execute project

```sh
PROJECT_NAME=package_n
poetry run --directory $PROJECT_NAME python $PROJECT_NAME

# or

# poetry run --directory $PROJECT_NAME your_command
```


## Add new projects

```sh
PROJECT_NAME=package_n
poetry new $PROJECT_NAME

poetry --directory $PROJECT_NAME env use 3.10
poetry --directory $PROJECT_NAME install --no-root
poetry --directory $PROJECT_NAME add --editable ../shared

# or

# cd $PROJECT_NAME
# poetry env use 3.10
# poetry install --no-root
# poetry add --editable ../shared
```
