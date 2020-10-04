# Pycharm example Django App

An example of a Django project that uses docker-compose and makes PyCharm debugger not work as intended.

## Usage

```sh
docker-compose up
```

Setup PyCharm docker-compose remote debugger and then set a breakpoint on the `hello_view` function at `exampleapp/urls.py`.
When visiting `localhost:8000/hello` it's expected for the debugger to stop, but it doesn't.
