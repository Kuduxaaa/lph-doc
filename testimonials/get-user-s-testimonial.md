## 📡 Endpoint: GET `/api/v1/testimonials/mine`

**Content-Type**: `application/json`

**Accept**: `application/json`

**Needs Auth**: `YES`

**Returns JSON always.**

Getting user's testimonial.

### 🔒 Authentication (Bearer)

> Presented token should be received from [auth-login](https://github.com/Kuduxaaa/lph-doc/blob/main/auth-login.md)

```
Authorization: Bearer [TOKEN...]
```

------

### ✅ Success Response:


1. Standard case.

> HTTP Code: 200 OK


```json
{
	"success": true,
	"data": {
		"id": 1,
		"user_id": 133,
		"stars": 5,
		"comment": "I like you guys",
		"created_at": "2025-08-05T14:02:22.000000Z",
		"updated_at": "2025-08-05T14:02:22.000000Z"
	}
}
```

2. If user doesn't have testimonial:

> HTTP Code: 200 OK

```json
{
	"success": true,
	"data": null
}
```