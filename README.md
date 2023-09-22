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
> ℹ️ I have used a separate database for each microservice since that is the best approach to acheive loose coupling. I used mongoDB Atlas for development speed but using a docker container for the db is the best approach for production environments.  
> My implementation of the Optional Feature # 3.1 allows me to use the same code to acheive Optional Feature # 3.2 as well since I always get visible flashcards that have `nextReviewDate` that is due or overdue. 
- [API Gateway #README.md](https://github.com/abulhuman/soora-sr-api-gateway/blob/main/README.md)
- [Auth Microservice #README.md](https://github.com/abulhuman/soora-sr-auth-svc/blob/main/README.md)
- [Flashcard Microservice #README.md](https://github.com/abulhuman/soora-sr-flashcard-svc/blob/main/README.md)

## 5. Test the API Gateway

Import the postman collection json file into postman to see all the required API endpoints with their variants. I have provided you with it in this repository to test the api gateway. 🔗👉 [POSTMAN Collection File](./Soora-sr-api-gateway.postman_collection.json).  You can then right click on the imported postman collection then click on `View Documentation` to see each example.


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

