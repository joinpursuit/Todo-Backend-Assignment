# Todo-Backend-Assignment

This Server/API is intended to be used by the fellows to practice making network requests, learn about HTTP status codes, their uses and differences, learn about query parameters and body data sent to appropriate endpoints.

You will use express, nodeJS and postgreSQL to build this.

# Dependencies 
- `node`
- `npm`
- PostgreSQL / `psql`
- Postman

# Project MVP Goals
    This app should be able to:
        - Register a user with an username and password
        - Allow user to create todo (with a timestamp of when it was created)
        - Allow user to update a todo 
        - Allow user to see one specfic todo
        - Allow user to delete a todo
    
# Endpoints

#### Users
| Method | Endpoint                 | Action         |
|--------|--------------------------|----------------|
| `GET`  | `/users`                 |Get All users   |
| `GET`  | `/users/<user-username>` |Get one user    |
| `POST` | `/users/signup`          |Register a user |

#### Todos
| Method   | Endpoint                | Action                        |
|----------|-------------------------|-------------------------------|
| `GET`    | `/todos`                | Get all todos                 |
| `GET`    | `/todos/<user-username>`| Get all todos from a user     |
| `GET`    | `/todos/<todo-id>`      | Get one todo                  |
| `POST`   | `/todos`                | Create a todo                 | 
| `PATCH`  | `/todos/<todo-id>`      | Update a todo                 |
| `DELETE` | `/todos/<todo-id>`      | Delete a todo                 |


# Responses Format

The format for all responses should be a JSON object with three properties status, message and payload.

A successful request should be answered with the following JSON:
```json
{
    "status": "success",                      
    "message": "retrieved single researcher", 
    "payload": {                              
        "id": 11,
        "name": "Jen Simmons",
        "job_title": "Lab Researcher"
    }
}
```

For a failed request the JSON sent should be something like:

```json
{
    "status": "error",
    "message": "researcher not found",
    "payload": null
}

```
**Notes**

* `payload`. Your response from SQL (the actual data)
* `message`. Either "got all users" or an error message
* `status`. Either "success" or "error"
* `payload`. If a single row is retrieved from the database, like when retrieving a single researcher payload should contain a single `object`. When retrieving a multiple rows like when getting all researchers payload should contain an `array`. The rule of thumb is if single => `object`, list => `array`
* If possible, when deleting, inserting and updating rows in the database return the affected row/data in the payload property of the response. (optional)