## 📡 Endpoint: POST `/api/v1/auth/reset-password`

**Content-Type**: `application/json`

**Accept**: `application/json`

**Needs Auth**: `NO`

**Returns JSON always.**

This endpoint will finally resets user's password.

-------

### 📥 Request Body (JSON):



| Field           | Type     | Required | Description             |
| --------------- | -------- | -------- | ----------------------- |
| `email`         | `string` | ✅        | User's email address |
| `token`         | `string` | ✅        | Token which sent to email from section `forget-password.md` |
| `password`      | `string` | ✅        | User's new password |
| `password_confirmation`      | `string` | ✅        | Confirmation of new password (same) |

------

### Request example (body)

```json
{
    "email": "email_address@domain.com",
    "token": "872093b4d36fcc7e63e28e4c0c4e0dcadf728e884c094d420f25fa1120d6e0be",
    "password": "NewPassword",
    "password_confirmation": "NewPassword"
}
```

### ✅ Success Response:

> HTTP Code: 200 OK

```json
{
    "success": true,
    "message": "Password reset successfully"
}
```

------

### ❌ Possible error responses

1. If token or user email is incorrect

> HTTP Code: 422 (Unprocessable Entity)

```json
{
    "success": false,
    "message": "Unable to reset password"
}
```
