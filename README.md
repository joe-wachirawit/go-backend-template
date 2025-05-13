
# Go Backend template

This project serves as a backend template for building Go (Golang) services. It provides a clean and scalable foundation with best practices for organizing your code, managing dependencies, and implementing common backend features such as routing, logging, user authentication, user authorization and API key.


#### Features
- Modular project structure
- HTTP server routing
- Middleware support
- Authentication and Authorization
- Interact with database system via ORM
- Database migration with ORM

#### Project Structure
```
go-backend-template/
├── cmd/                # Entry points for the application (e.g., main.go)
│   └── server/
│       └── main.go
│   └── worker/
│       └── main.go
├── config/             # Configuration loading
├── docs/               # Generated documents
├── domain/             # Business logic layer
├── handler/            # HTTP handlers
├── infrastructure/     # Third-parties service
├── models/             # Model entity
├── repository/         # Database repository
├── app.go              # Application entry point
├── go.mod
├── go.sum
└── README.md
```

## Prerequisites
- Docker Compose ([link](https://docs.docker.com/compose/install/))

## How to Run

- Clone this repo

```bash
git clone https://github.com/joe-wachirawit/go-backend-template.git
```

- Checkout `origin/main` branch
```bash
git fetch
```
```bash
git checkout -b main origin/main
```
- Rename `.env.dist` to `.env`

- Start Application
```bash
docker-compose up
```
Now you should have 
- **Book List App** running on `localhost:7788`
- **MySql Server** running on `localhost:33060`
  - **host**: localhost
  - **username**: local_user
  - **password**: password
  - **port**: 33060

## API Document via Swagger
- Browse to `http://localhost:7788/swagger/index.html`.

- Make requests to register a user and login.

- After login, copy a **token** from the response, then click "Authorize" and in a popup, enter the value for "apiKey" in a form: "Bearer {token}". For example:

Then, click "Authorize" and close the popup. Now, you are able to make requests which require authentication
