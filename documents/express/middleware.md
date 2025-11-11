# Express.js Middleware

Middleware in Express.js is a function that executes **between the request and response**. It can be used for various purposes such as logging, authentication, error handling, or processing request data.

---

## Key Points

- Middleware functions have access to the `request` and `response` objects.  
- They also have a `next()` function to pass control to the next middleware or route handler.  
- Special usage of `next()`:
  - `next('route')` → skips remaining middleware and moves directly to the next route handler.
  - `next(err)` → passes control to **error-handling middleware**, where `err` becomes the `err` parameter in that middleware.  

---

## Middleware Structure

- A standard middleware function has **3 parameters**: `(request, response, next)`.
- Error-handling middleware has **4 parameters**: `(error, request, response, next)`.
- You **must call `next()`** at the end of the middleware to continue processing.

---

## Example Middleware

File: `/middlewares/testMiddleware.js`

```javascript
// Standard middleware function
export const test1 = (request, response, next) => {
    console.log('test1 middleware');
    next(); // Pass control to the next middleware or route handler
}
```

## Error-Handling Middleware Example

```javascript
export const errorHandler = (err, request, response, next) => {
    console.error(err.stack);
    response.status(500).send('Something broke!');
}
```