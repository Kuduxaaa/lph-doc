## 📡 Endpoint: GET `/api/v1/user/teams`

**Content-Type**: `application/json`

**Accept**: `application/json`

**Needs Auth**: `YES`

**Returns JSON always.**

Getting user's companies/teams.

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
    "data": [
        {
            "id": 42,
            "user_id": 133,
            "name": "TEST CRM",
            "personal_team": false,
            "created_at": "2025-07-09T15:20:53.000000Z",
            "updated_at": "2025-07-09T15:20:53.000000Z"
        },
        {
            "id": 45,
            "user_id": 133,
            "name": "test company",
            "personal_team": false,
            "created_at": "2025-07-28T15:53:25.000000Z",
            "updated_at": "2025-07-28T15:53:25.000000Z"
        },
        {
            "id": 46,
            "user_id": 133,
            "name": "test-team",
            "personal_team": false,
            "created_at": "2025-08-01T01:44:14.000000Z",
            "updated_at": "2025-08-01T01:44:14.000000Z"
        }
    ]
}
```
