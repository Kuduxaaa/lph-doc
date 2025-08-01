## 📡 Endpoint: POST `/api/v1/contact-us`

**Content-Type**: `application/json`

**Accept**: `application/json`

**Needs Auth**: `NO`

**Returns JSON always.**

-------

### 📥 Request Body (JSON):


| Field           | Type     | Required | Description
| --------------- | -------- | -------- | ------------------------------- |
| `name`          | `string` | ✅        | User's first name (max 255) |
| `surname`       | `string` | ✅        | User's surname (max 255) |
| `email`         | `string` | ✅        | Valid email address (max 255) |
| `message`       | `string` | ✅        | Message |                                             

------

### ✅ Success Response:

> HTTP Code: 200 OK

```json
{
    "success": true,
    "message": "Thanks for your message. We’ll be in touch"
}
```

------

### ❌ Error Response (Validation or Logical Fail):

> HTTP Code: 422 (Unprocessable Entity)

```json
{
    "success": false,
    "message": "The surname field is required."
}
```
