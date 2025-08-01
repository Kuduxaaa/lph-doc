## 📡 Endpoint: POST `/api/v1/user/teams`

**Content-Type**: `application/json`

**Accept**: `application/json`

**Needs Auth**: `YES`

**Returns JSON always.**

Create new team

-------

### 📥 Request Body (JSON):


| Field              | Type     | Required  | Description             |
| ------------------ | -------- | --------- | ----------------------- |
| `name` | `string` | ✅       | Name of new team |
| `personal_team`  | `bool` | ❌       | Team is personal or not (Default: false)

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
    "success": true,
    "data": {
        "user_id": 133,
        "name": "newly-createdd",
        "personal_team": false,
        "updated_at": "2025-08-01T03:08:05.000000Z",
        "created_at": "2025-08-01T03:08:05.000000Z",
        "id": 49
    }
}
```

### Possible Error Responses

1. Team with this name already exists (422 Unprocessable Entity)

```json
{
    "success": false,
    "errors": "The name has already been taken."
}
```