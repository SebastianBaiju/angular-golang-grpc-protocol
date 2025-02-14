# Connecting Angular and Golang with gRPC

## Overview
This project demonstrates how to establish a connection between an Angular frontend and a Golang backend using the gRPC protocol. By leveraging Protocol Buffers (protobufs), we enable efficient and structured communication between the two services.

## Technologies Used

### 🔹 Angular  
- `@ngx-grpc/core` – Connects Angular to the gRPC server  
- `@ngx-grpc/improbable-eng-grpc-web-client` – Enables gRPC-Web support  
- `@ngx-grpc/well-known-types` – Provides well-known protocol buffer types  
- `google-protobuf` – Handles protobuf serialization & deserialization  
- `ngx-cookie-service` – Manages cookies for authentication  
- `ngx-toastr` – Displays user-friendly toast notifications  
- `rxjs` & `subsink` – Manages observables and subscriptions efficiently  

### 🔹 Golang  
- `google.golang.org/grpc` – Implements gRPC server  
- `google.golang.org/protobuf` – Manages protocol buffers  
- `github.com/improbable-eng/grpc-web` – Enables gRPC-Web support  
- `github.com/gofrs/uuid/v5` – Generates unique IDs  
- `github.com/golang-jwt/jwt/v4` – Handles authentication  
- `gorm.io/gorm` & `gorm.io/driver/postgres` – Database ORM and PostgreSQL driver  

## Setup and Installation

### 1. Clone the Repository
```sh
git clone https://github.com/SebastianBaiju/angular-golang-grpc-protocol.git
```

### 2. Install Dependencies
#### Angular
```sh
cd angular-gRPC
npm install
```

#### Golang
```sh
cd go-gRPC
go mod tidy
```

### 3. Compile Proto Files
#### Angular
```sh
npm run proto:generate
```

#### Golang
```sh
cd proto
make all
```

### 4. Run the Project
#### Start Angular Application
```sh
ng serve
```

#### Start Golang Server
```sh
go run main.go
```

## Environment Configuration

### Golang (`.env` file)
```
PORT=8080

JWT_SECRET=SECRET

DB_HOST=localhost
DB_PORT=5432
DB_USERNAME=postgres
DB_PASSWORD=PASSWORD
DB_NAME=postgres
```

### Angular (`env.js`)
```js
(function(window) {
    window.__env = window.__env || {};
    window.__env.baseUrl = 'http://localhost:8080';
}(this));
```

## Resources
- [gRPC Go Quickstart](https://grpc.io/docs/languages/go/quickstart/)
- [GORM Documentation](https://gorm.io/index.html)
- [ngx-grpc GitHub](https://github.com/smnbbrv/ngx-grpc)

## Inspiration
This project is inspired by [grpc-template](https://github.com/Jerinji2016/grpc-template). Contributions are welcome—let’s build something great together! 🚀

