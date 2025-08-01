## 📡 Endpoint: POST `/api/v1/user/profile`

**Content-Type**: `application/json`

**Accept**: `application/json`

**Needs Auth**: `YES`

**Returns JSON always.**

This endpoint is used to **retrieve the authenticated user's profile information**. Once authenticated via a valid Bearer token, the system returns detailed data related to the user account including ID, name, email, team ID, timestamps, and profile photo URL.

It’s typically used on application load or after login to populate the user's dashboard, account settings, or header info.

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
        "id": 133,
        "name": "TEST CRM",
        "email": "shavgulidzelasha66@gmail.com",
        "email_verified_at": "2025-07-09T15:20:52.000000Z",
        "two_factor_confirmed_at": null,
        "current_team_id": 45,
        "profile_photo_path": null,
        "source_id": null,
        "created_at": "2025-07-09T15:20:53.000000Z",
        "updated_at": "2025-07-31T14:38:48.000000Z",
        "last_renew_password_at": null,
        "profile_photo_url": "https://ui-avatars.com/api/?name=T+C&color=7F9CF5&background=EBF4FF"
    }
}
```
