# gRPC Server with SQLite Database and Golang

This project is a gRPC server that uses a SQLite database for storage. It includes a `CategoryService` for managing categories.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

- Go 1.16 or later
- SQLite3
- Protocol Buffers compiler (`protoc`)

### Installing

1. Clone the repository:

git clone https://github.com/RaphaelMarquesMartorella/gRPC.git

2. Navigate to the project directory:

cd gRPC

3. Install the required Go packages:

go mod download

4. Compile the Protocol Buffers definitions:


### Running the Server

To start the gRPC server, run:

go run main.go


The server will start and listen for connections.

## Built With

- [Go](https://golang.org/) - The programming language used
- [gRPC](https://grpc.io/) - The RPC framework used
- [SQLite](https://www.sqlite.org/index.html) - The database engine used

## Authors

- **Raphael Marques Martorella** - *Initial work*

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
