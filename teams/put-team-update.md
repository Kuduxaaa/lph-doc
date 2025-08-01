## 📡 Endpoint: PUT `/api/v1/user/team/<TEAM_ID>`

**Content-Type**: `application/json`

**Accept**: `application/json`

**Needs Auth**: `YES`

**Returns JSON always.**

Update team's data

-------

### 🔒 Authentication (Bearer)

> Presented token should be received from [auth-login](https://github.com/Kuduxaaa/lph-doc/blob/main/auth-login.md)

```
Authorization: Bearer [TOKEN...]
```

-------

### 📥 Request Body (JSON):


| Field   | Type     | Required  | Description              |
| ------- | -------- | --------- | ------------------------ |
| `name`  | `string` | ✅        | Comany's/Team's new name |

------

### ✅ Success Response:

> HTTP Code: 200 OK

```json
{
    "success": true,
    "data": {
        "id": 42,
        "user_id": 133,
        "name": "TEST CRM",
        "personal_team": false,
        "created_at": "2025-07-09T15:20:53.000000Z",
        "updated_at": "2025-07-09T15:20:53.000000Z"
    }
}
```
