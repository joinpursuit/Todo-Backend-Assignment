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
| `POST`   | `/todos`                | Create a todo                 | 
| `GET`    | `/todos/<todo-id>`      | Get one todo                  |
| `PATCH`  | `/todos/<todo-id>`      | Update a todo                 |
| `DELETE` | `/todos/<todo-id>`      | Delete a todo                 |

