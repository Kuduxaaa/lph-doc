## 📡 Endpoint: POST `/api/v1/auth/forgot-password`

**Content-Type**: `application/json`

**Accept**: `application/json`

**Needs Auth**: `NO`

**Returns JSON always.**

This endpoint will send password-reset link to user's email. It will looks something like that:

`https://legalpulsehub.com/reset-password/<TOKEN>?email=<EMAIL>`

-------

### 📥 Request Body (JSON):



| Field           | Type     | Required | Description             |
| --------------- | -------- | -------- | ----------------------- |
| `email`         | `string` | ✅        | User's email address |

------

### ✅ Success Response:

> HTTP Code: 200 OK

```json
{
    "success": true,
    "message": "Password reset link sent"
}
```

------

### ❌ Possible error responses

> HTTP Code: 422 (Unprocessable Entity)

```json
{
    "success": false,
    "message": "Email field is required"
}
```
