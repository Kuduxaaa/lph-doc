## 📡 Endpoint: GET `/api/v1/auth/logout`

**Content-Type**: `application/json`

**Accept**: `application/json`

**Needs Auth**: `YES`

**Returns JSON always.**

This endpoint logs out the currently authenticated user by invalidating their active access token. Once this request is made, the token used in the Authorization header will no longer be valid for accessing protected API routes.

The logout operation ensures session termination on the backend side, providing a secure way to prevent further API access without requiring token expiration.

This endpoint is protected by Bearer authentication and requires a valid access token to be sent with the request.

-------

### 🔒 Authentication (Bearer)

> Presented token should be received from [auth-login](https://github.com/Kuduxaaa/lph-doc/blob/main/auth/auth-login.md)

```
Authorization: Bearer [TOKEN...]
```


------

### ✅ Success Response:

> HTTP Code: 200 OK

```json
{
    "success": true
    "message": "Successfully logged out"
}
```
