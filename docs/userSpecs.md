# User Specification API

## Register User

Endpoint : POST /api/users

Header :
```{
Content-type : application/json
```

Request Body :
```json
{
  "username": "",
  "password": "",
  "firstname": "",
  "lastname": "",
  "email": "",
  "phone": ""
}
```

Response Body(success) :

HTTP Status Code : 201

```json
{
  "message": "Registrasi Berhasil!"
}
```

Response Body(failed) :

HTTP Status Code : 400
```json
{
  "message": "Registrasi Gagal!"
}
```

## Login User

Endpoint : POST /api/auth/login

Header :
```{
Content-type : application/json
```

Request Body :
```json
{
  "username": "",
  "password": ""
}
```

Response Body(success) :

HTTP Status Code : 200
```json
{
  "message": "Login Berhasil!",
  "token": ""
}
```

Response Body(failed) :

HTTP Status Code : 401
```json
{
  "message": "Login Gagal!"
}
```

## Update user

Endpoint : PUT /api/users

Header : 
```{
Content-type : application/json,
Authorization : Bearer <Token>
```


Request Body :
```json
{
  "username": "",
  "password": "",
  "firstname": "",
  "lastname": "",
  "email": "",
  "phone": ""
}
```

Response Body(success) :

HTTP Status Code : 200

```json
{
  "message": "Update Berhasil!"
}
```

Response Body(failed) :

HTTP Status Code : 400
```json
{
  "message": "Update Gagal!"
}
```
## Logout User
Endpoint : DELETE /api/users

Header :
```{
Content-type : application/json,
Authorization : Bearer <Token>
```


Request Body :
```json
{}
```

Response Body(success) :

HTTP Status Code : 200

```json
{
  "message": "Logout Berhasil!"
}
```

Response Body(failed) :

HTTP Status Code : 400
```json
{
  "message": "Logout Gagal!"
}
```