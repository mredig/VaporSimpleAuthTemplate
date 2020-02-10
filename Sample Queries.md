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
  "default": "{\"username\":\"zeldaa\",\"password\":\"lonk\",\"passwordVerify\":\"lonk\"}"
}
```

### **POST** - /login

#### CURL

```sh
curl -X POST "http://localhost:8080/login" \
-u "zeldaa":"lonk"
```

#### Security

- Basic Authentication
  - **username**: zeldaa
  - **password**: lonk

### **GET** - /profile

#### CURL

```sh
curl -X GET "http://localhost:8080/profile" \
    -H "Content-Type: application/json" \
    -H "Authorization: Bearer pVCtG/KmkYKju5TEKNnENA=="
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
    "Bearer pVCtG/KmkYKju5TEKNnENA=="
  ],
  "default": "Bearer pVCtG/KmkYKju5TEKNnENA=="
}
```

## References

