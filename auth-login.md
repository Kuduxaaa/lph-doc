## 📡 Endpoint: POST `/api/v1/auth/login`

**Content-Type**: `application/json`

**Accept**: `application/json`

**Returns JSON always.**

-------

### 📥 Request Body (JSON):



| Field           | Type     | Required | Description             |
| --------------- | -------- | -------- | ----------------------- |
| `email`         | `string` | ✅        | User's email address |
| `password`      | `string` | ✅        | User's password

------

### ✅ Success Response:

> HTTP Code: 200 OK

```json
{
    "access_token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwczovL2xlZ2FscHVsc2VodWIuY29tL2FwaS92MS9hdXRoL2xvZ2luIiwiaWF0IjoxNzUzODg1MDMwLCJleHAiOjE3NTM4ODg2MzAsIm5iZiI6MTc1Mzg4NTAzMCwianRpIjoiVGRRTWJURXJCRkRaQ0ZXNCIsInN1YiI6IjEzMyIsInBydiI6IjIzYmQ1Yzg5NDlmNjAwYWRiMzllNzAxYzQwMDg3MmRiN2E1OTc2ZjcifQ.nB9uMNfv9zTKj10F10cNyEr3eQTfNIR_hlIPa4JOAjE",
    "token_type": "bearer",
    "expires_in": 3600,
    "user": {
        "id": 133,
        "name": "TEST CRM",
        "email": "email_address@gmail.com",
        "email_verified_at": "2025-07-09T15:20:52.000000Z",
        "two_factor_confirmed_at": null,
        "current_team_id": 42,
        "profile_photo_path": null,
        "source_id": null,
        "created_at": "2025-07-09T15:20:53.000000Z",
        "updated_at": "2025-07-29T19:35:20.000000Z",
        "last_renew_password_at": null,
        "profile_photo_url": "https://ui-avatars.com/api/?name=T+C&color=7F9CF5&background=EBF4FF"
    }
}
```

------

### ❌ Error Response (Incorrect credentials):

> HTTP Code: 401 (Unauthorized)

```json
{
    "success": false,
    "message": "Invalid credentials"
}
```

-------

### ❌ Error Response (Validation or Logical fail)

> HTTP Code: 422 (Unprocessable Entity)

```json
{
    "success": false,
    "message": "The password field is required."
}
```
