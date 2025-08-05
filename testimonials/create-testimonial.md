## 📡 Endpoint: POST `/api/v1/testimonials`

**Content-Type**: `application/json`

**Accept**: `application/json`

**Needs Auth**: `YES`

**Returns JSON always.**

Getting one team data.


-------

### 📥 Request Body (JSON):


| Field              | Type     | Required  | Description             |
| ------------------ | -------- | --------- | ----------------------- |
| `stars`    | `integer` | ✅       | Number of starts from 1 to 5 |
| `comment`  | `string` | ✅       | User's comment max 1000 symbol

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
	"message": "Thank you! Your feedback is important to us "
}
```