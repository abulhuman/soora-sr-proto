# Protofiles for Soora Spaced Repetition Test

This repository defines protofiles the following microservices:

- auth
- flashcard

## Microservice Flow

![Microservice Flow](msvc-flow.png)

## Repositories
- Protofiles: [soora-sr-proto](https://github.com/abulhuman/soora-sr-proto.git)
- API Gateway: [soora-sr-api-gateway](https://github.com/abulhuman/soora-sr-api-gateway.git)
- Auth Microservice: [soora-sr-auth](https://github.com/abulhuman/soora-sr-auth-svc.git)
- Flashcard Microservice: [soora-sr-flashcard](https://github.com/abulhuman/soora-sr-flashcard-svc.git)

## Instructions

### 1. Clone API Gateway

```bash
git clone https://github.com/abulhuman/soora-sr-api-gateway.git
```

### 2. Clone Auth Microservice

```bash
git clone https://github.com/abulhuman/soora-sr-auth-svc.git
```

### 3. Clone Flashcard Microservice

```bash
git clone https://github.com/abulhuman/soora-sr-flashcard-svc.git
```
### 4. Follow the instructions in each repository's README file
- [API Gateway #README.md](https://github.com/abulhuman/soora-sr-api-gateway/blob/main/README.md)
- [Auth Microservice #README.md](https://github.com/abulhuman/soora-sr-auth-svc/blob/main/README.md)
- [Flashcard Microservice #README.md](https://github.com/abulhuman/soora-sr-flashcard-svc/blob/main/README.md)

## 5. Test the API Gateway

Use the postman collection json file provided in this repository to test the api gateway.  
[POSTMAN Collection File](./Soora-sr-api-gateway.postman_collection.json)


Usage:

```json
// package.json
...
"dependencies": {
  ...
  "soora-sr-proto": "git+https://github.com/abulhuman/soora-sr-proto.git",
  ...
}
...
```

```ts
// index.ts
// eg: gRPC config object for auth microservice
{
    // ...
    protoPath: 'node_modules/soora-sr-proto/proto/auth.proto',
    // ...
}
```

Author:

- [Adem Mohammed](abulhuman.dev@gmail.com)

