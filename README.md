# FastAPI and Strawberry GraphQL with Docker for MySQL

This is a sample project that demonstrates using GraphQL with FastAPI and Strawberry, which is a combination of FastAPI, GraphQL, and SQLAlchemy. It also includes instructions for setting up Docker for MySQL.

## Installation

### Clone the repository:

   ```
   $ git clone https://github.com/thiphan94/GraphQL.git
   $ cd GraphQL
   ```
### Create and activate a virtual environment:

```
$ conda create -n cnn python=3.8 -y
$ conda activate cnn
```
### Install dependencies using pip:
```
$ pip install -r requirements.txt
```

## Usage
Make sure your MySQL server is running on localhost at the default port 3306. You can use your MySQL server instead of localhost.

Start the FastAPI server:
```
uvicorn main:app --reload
```

The GraphQL API will be available at http://localhost:8000/graphql. You can access this URL in your browser or use tools like Insomnia or GraphQL Playground to interact with the API.

## Examples
### Create User
To create a new user, send a GraphQL mutation request:

```
mutation {
  createUser(name: "Anna") {
    id
    name
  }
}
```

### Update User
To update a user, send a GraphQL mutation request:

```
mutation {
  updateUser(id: 1, name: "Kritika Pandey") {
    id
    name
  }
}
```
### Delete User
To delete a user, send a GraphQL mutation request:

```
mutation {
  deleteUser(id: 1) {
    id
    name
  }
}
```


### Get All Users
To get a list of all users, send a GraphQL query request:

```
query {
  users {
    id
    name
  }
}
```


### Get User by ID
To get a specific user by ID, send a GraphQL query request:
```
query {
  user(id: 1) {
    id
    name
  }
}
```


## License
This project is licensed under the MIT License.
