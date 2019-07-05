# jwt-auth_laravel_test

## rotas
```
+--------+----------+------------------+------+---------------------------------------------+--------------+
| Domain | Method   | URI              | Name | Action                                      | Middleware   |
+--------+----------+------------------+------+---------------------------------------------+--------------+
|        | POST     | api/auth/signup  |      | App\Http\Controllers\AuthController@signup  | api          |
|        | POST     | api/auth/login   |      | App\Http\Controllers\AuthController@login   | api          |
|        | POST     | api/auth/logout  |      | App\Http\Controllers\AuthController@logout  | api,auth:api |
|        | POST     | api/auth/me      |      | App\Http\Controllers\AuthController@me      | api,auth:api |
|        | POST     | api/auth/refresh |      | App\Http\Controllers\AuthController@refresh | api,auth:api |
+--------+----------+------------------+------+---------------------------------------------+--------------+
```

## requests
### Signup
```
> POST /api/auth/signup HTTP/1.1
> Host: localhost:8000
> User-Agent: insomnia/6.5.4
> Content-Type: application/x-www-form-urlencoded
> Accept: */*
> Content-Length: 57

| email=mbarbosa%40pbh.gov&password=123456789&name=mbarbosa
```

### Login
```
> POST /api/auth/login HTTP/1.1
> Host: localhost:8000
> User-Agent: insomnia/6.5.4
> Content-Type: application/x-www-form-urlencoded
> Accept: */*
> Content-Length: 43

| email=mbarbosa%40pbh.gov&password=123456789
```

### Me
```
> POST /api/auth/me HTTP/1.1
> Host: localhost:8000
> User-Agent: insomnia/6.5.4
> Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOlwvXC9sb2NhbGhvc3Q6ODAwMFwvYXBpXC9hdXRoXC9sb2dpbiIsImlhdCI6MTU2MjM1Mjk2OCwiZXhwIjoxNTYyMzU2NTY4LCJuYmYiOjE1NjIzNTI5NjgsImp0aSI6IjFzS3hRRUZBekd2eGdjbVIiLCJzdWIiOjIsInBydiI6Ijg3ZTBhZjFlZjlmZDE1ODEyZmRlYzk3MTUzYTE0ZTBiMDQ3NTQ2YWEifQ.sLzkQQ-DGz1avLsAfUCf94qsEEYAcV4ghP4H3u52umI
> Accept: */*
> Content-Length: 0
```

### Logout
```
> POST /api/auth/logout HTTP/1.1
> Host: localhost:8000
> User-Agent: insomnia/6.5.4
> Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOlwvXC9sb2NhbGhvc3Q6ODAwMFwvYXBpXC9hdXRoXC9sb2dpbiIsImlhdCI6MTU2MjM1NDAwNCwiZXhwIjoxNTYyMzU3NjA0LCJuYmYiOjE1NjIzNTQwMDQsImp0aSI6IlV3bU01bXZ5dFQyTmlyTnIiLCJzdWIiOjIsInBydiI6Ijg3ZTBhZjFlZjlmZDE1ODEyZmRlYzk3MTUzYTE0ZTBiMDQ3NTQ2YWEifQ._5keMX8NxFWzeXX1U2frrx7O51UZw0CEozTlEBy5aF0
> Accept: */*
> Content-Length: 0
```

