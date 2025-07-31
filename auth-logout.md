## 📡 Endpoint: GET `/api/v1/auth/logout`

**Content-Type**: `application/json`

**Accept**: `application/json`

**Returns JSON always.**

-------

### 🔒 Authentication (Bearer)

> Presented token should be received from [auth-login](https://github.com/Kuduxaaa/lph-doc/blob/main/auth-login.md)

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
