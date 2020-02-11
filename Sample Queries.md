# API

## Requests

### **POST** - /register

#### CURL

```sh
curl -X POST "http://localhost:8080/register" \
    -H "Content-Type: application/json" \
    --data-raw "$body"
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json"
  ],
  "default": "application/json"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"username\":\"\",\"password\":\"\",\"passwordVerify\":\"\"}"
}
```

### **POST** - /login

#### CURL

```sh
curl -X POST "http://localhost:8080/login" \
    -H "Content-Type: application/json" \
    --data-raw "$body"
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json"
  ],
  "default": "application/json"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"username\":\"\",\"password\":\"\"}"
}
```

### **POST** - /login

#### CURL

```sh
curl -X POST "http://localhost:8080/login" \
-u "$username":"$password"
```

#### Security

- Basic Authentication
  - **username**: $username
  - **password**: $password

### **GET** - /profile

#### CURL

```sh
curl -X GET "http://localhost:8080/profile" \
    -H "Content-Type: application/json" \
    -H "Authorization: Bearer S0fJiStzl7LrC6m8rWDq7473EDorBaMedNp3M+uju4U="
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json"
  ],
  "default": "application/json"
}
```
- **Authorization** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "Bearer S0fJiStzl7LrC6m8rWDq7473EDorBaMedNp3M+uju4U="
  ],
  "default": "Bearer S0fJiStzl7LrC6m8rWDq7473EDorBaMedNp3M+uju4U="
}
```

## References

