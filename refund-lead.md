## 📡 Endpoint: POST `/api/v1/user/leads/<LEAD_ID>/refund`

**Content-Type**: `application/json`

**Accept**: `application/json`

**Needs Auth**: `YES`

**Returns JSON always.**

Getting one team data.


-------

### 📥 Request Body (JSON):


| Field              | Type     | Required  | Description             |
| ------------------ | -------- | --------- | ----------------------- |
| `reason`    | `string` | ✅       | Refund reason |

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
}
```

### ❌ Possible Error Responses
1. Reason is required to request refund
```json
{
    "success": false,
    "message": "The reason field is required."
}
```

2. If lead refund is already requested and status is not `assigned` anymore
```json
{
    "success": false,
    "message": "Lead not found"
}
```
