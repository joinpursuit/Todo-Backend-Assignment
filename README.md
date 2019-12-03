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
| Method | Endpoint                 | 
|--------|--------------------------|
| `GET`  | `/users`                 |
| `GET`  | `/users/<user-username>` |
| `POST` | `/users/signup`          |

#### Todos
| Method   | Endpoint           | 
|----------|--------------------|
| `GET`    | `/todos`           | 
| `POST`   | `/todos`           |
| `GET`    | `/todos/<todo-id>` |
| `PUT`    | `/todos/<todo-id>` |
| `PATCH`  | `/todos/<todo-id>` |
| `DELETE` | `/todos/<todo-id>` |

