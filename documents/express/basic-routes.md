# 🧩 Express.js Basic Routes

This is an example of defining basic routes in Express.js, specifying different HTTP request methods (GET, POST, PUT, DELETE).

---

## 1. GET `/home`

The GET method is used to **request data** from the server. It does not change any data on the server; it only retrieves information.

```javascript
app.get('/home', (request, response, next) => {
    response.status(200).send('GET Home.');
});
```
## 2. POST `/home`

The POST method is used to **send data** to the server. It is often used to create new resources or submit forms.

```javascript
app.post('/home', (request, response, next) => {
    response.status(200).send('POST Home.');
});
```
## 3. PUT `/home`

The PUT method is used to **update existing data** on the server. If the resource does not exist, it can sometimes create it depending on the server logic.

```javascript
app.PUT('/home', (request, response, next) => {
    response.status(200).send('PUT Home.');
});
```
## 4. DELETE `/home`

The DELETE method is used to **remove data** from the server.

```javascript
app.delete('/home', (request, response, next) => {
    response.status(200).send('DELETE Home.');
});
```

