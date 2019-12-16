# Todos App Backend Assignment

This assignment is intended to be used by fellows to learn how to and practice making a backend server with Node.js Express.js & PostgreSQL. In the process the fellow will acquire knowledge about network requests, HTTP status codes, their uses and differences, learn about query parameters and body data sent to appropriate endpoints.

## Connected Lessons
Curriculum lessons that directly relate to this assignment can be found on the [Pursuit-Web-Core repo Unit 3 section](https://github.com/joinpursuit/Pursuit-Core-Web/blob/master/node/README.md)

## Dependencies 
- `node`
- `express`
- `pg-promise`
- `npm`
- PostgreSQL / `psql`
- Postman

## Project MVP Goals

Your assignment is to build a Backend Server that lets a client accomplish the following tasks.

- Register a user with a username and email
- Create a todo 
- Update a todo 
- Get one specific todo by id
- Delete a todo
    
To achieve the above functionality implement the following endpoints.

### Endpoints

#### Users
| Method | Endpoint            | Action          |
| ------ | ------------------- | --------------- |
| `GET`  | `/users`            | Get All users   |
| `GET`  | `/users/<username>` | Get one user    |
| `POST` | `/users/signup`     | Register a user |

#### Todos
| Method   | Endpoint            | Action                    |
| -------- | ------------------- | ------------------------- |
| `GET`    | `/todos`            | Get all todos             |
| `GET`    | `/todos/<username>` | Get all todos from a user |
| `GET`    | `/todos/<todo-id>`  | Get one todo              |
| `POST`   | `/todos`            | Create a todo             |
| `PATCH`  | `/todos/<todo-id>`  | Update a todo             |
| `DELETE` | `/todos/<todo-id>`  | Delete a todo             |


### Data Model

This is what a user and a todo should look like in your system

#### User
```json
{
    "id": 1,
    "username": "Alex123",
    "email": "alex.bravo@gmail.com"
}
```

#### Todo
```json
{
    "id": 2,
    "owner": "Alex123",
    "text": "Walk my Dog",
    "completed": false
}
```

### Responses Format

The format for all responses should be a JSON object with three properties status, message and payload.
A successful request should be answered with the following JSON:

```json
{
    "status": "success",                      
    "message": "retrieved user by username", 
    "payload": {                              
        "id": 11,
        "username": "JenSimmons",
        "email": "jenny123@hotmail.com"
    }
}
```

For a failed request the JSON sent should be something like:

```json
{
    "status": "error",
    "message": "todo not found",
    "payload": null
}

```

**Notes**

* `payload`. Your response from SQL (the actual data). Either a single todo or a user. Or an array of todos or users objects.
* `message`. Either "got all users" or an error message
* `status`. Either "success" or "error"
* If possible, when deleting, inserting and updating rows in the database return the updated row/data in the payload property of the response. (optional)
