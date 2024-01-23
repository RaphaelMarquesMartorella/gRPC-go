# gRPC Server with SQLite Database and Golang

This project is a gRPC server that uses a SQLite database for storage. It includes a `CategoryService` for managing categories.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

## Installation

This project requires the following tools:

- [Go](https://golang.org/dl/): You can install Go by following the instructions on its download page.
- [gRPC](https://grpc.io/docs/languages/go/quickstart/): You can install gRPC by following the instructions on its quickstart page.
- [Protoc](https://developers.google.com/protocol-buffers/docs/gotutorial): You can install the Protocol Buffers compiler (`protoc`) by following the instructions on its tutorial page.
- [Evans](https://github.com/ktr0731/evans#installation): You can install Evans, a gRPC client, by following the instructions on its GitHub page.
- [SQLite3](https://www.sqlite.org/download.html): You can install SQLite3 by following the instructions on its download page.

1. Clone the repository:

``` 
git clone https://github.com/RaphaelMarquesMartorella/gRPC-go.git
```

2. Navigate to the project directory:

```
cd gRPC-go
```
3. Install the required Go packages:

```
go mod download
```

4. In the project directory, create a new SQLite3 database:

```
sqlite3 db.sqlite
```

5. In a separate terminal, You'll be taken to the SQLite command prompt. Here, you can create the `categories` table:

```sql
CREATE TABLE categories (
    id string,
    name string,
    description string
);
```
Now, when you run the server, it will connect to this SQLite database.

### Running the Server

To start the gRPC server, run:

```
go run cmd/grpcServer/main.go
```
The server will start and listen for connections.


### Interacting with the Server using Evans

6. In a separate terminal, start Evans in CLI mode and specify the package and service:

```
evans -r repl -p 50051 pb CategoryService
```
You can now use Evans to send requests to your `CategoryService`. For example, to call a `ListCategories` method, you would type `call ListCategories` in the Evans prompt.


## Built With

- [Go](https://golang.org/) - The programming language used
- [gRPC](https://grpc.io/) - The RPC framework used
- [SQLite](https://www.sqlite.org/index.html) - The database engine used

## Authors

- **Raphael Marques Martorella** - *Initial work* - This project was created while following along with the Full Cycle course.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
