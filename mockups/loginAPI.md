# Login API Mockup

## /login

POST:

```json
{
    "username": "string",
    "password": "string"
}
```

200:

```json
{
    "userId": "int",
    "userType": "string",
    "message": "Login successful"
}
```

400:
 
```json
{
    "error": "Invalid credentials"
}
```

## /logout

POST:

```json
{
    "userId": "int"
}
```

200:

```json
{
    "message": "Logout successful"
}
```

400:

```json
{
    "error": "Logout failed"
}
```
