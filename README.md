# Autenticação via JWT 

* Clone repository
```bash
https://github.com/gabrielSpassos/jwt-project.git
```
* Enter project folder

* Install dependencies
```bash
npm install
``` 

* Run app
```bash
node app.js
```

* Open Front-End: 
open /jwt-project/views/login.html

* Requests:
Method: [POST] http://localhost:4200/login
Body: 
```javascript
{
	"login": "gabriel@gmail.com",
	"pass": "123"
}
```
Output:
```javascript
{
    "auth": true,
    "token": ${JWT Token}
}
```
Method: [GET] http://localhost:4200/users
Header: Authorization ${JWT Token}
Output: 
```javascript
{
    "id": 1,
    "login": "gabriel@gmail.com",
    "password": "123",
    "cpf": "000.000.000-00",
    "age": 21,
    "name": "Gabriel",
    "description": "cara da hora"
}
```

* Test 
```bash
npm test
```