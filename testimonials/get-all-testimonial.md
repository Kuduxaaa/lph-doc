## 📡 Endpoint: GET `/api/v1/testimonials`

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
			"id": 5,
			"user_id": 133,
			"stars": 5,
			"comment": "<3<3",
			"created_at": "2025-08-05T14:16:55.000000Z",
			"updated_at": "2025-08-05T14:16:55.000000Z"
		},
		{
			"id": 1,
			"user_id": 133,
			"stars": 5,
			"comment": "I like you guys",
			"created_at": "2025-08-05T14:02:22.000000Z",
			"updated_at": "2025-08-05T14:02:22.000000Z"
		},
		{
			"id": 3,
			"user_id": 133,
			"stars": 3,
			"comment": "I like you guys!!!!!!!",
			"created_at": "2025-08-05T14:14:05.000000Z",
			"updated_at": "2025-08-05T14:14:05.000000Z"
		},
		{
			"id": 2,
			"user_id": 133,
			"stars": 3,
			"comment": "I like you guys!!!!!!!",
			"created_at": "2025-08-05T14:13:51.000000Z",
			"updated_at": "2025-08-05T14:13:51.000000Z"
		},
		{
			"id": 4,
			"user_id": 133,
			"stars": 1,
			"comment": "Fuck... What the hell is this?!",
			"created_at": "2025-08-05T14:14:26.000000Z",
			"updated_at": "2025-08-05T14:14:26.000000Z"
		}
	]
}
```
