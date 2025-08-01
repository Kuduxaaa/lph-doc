## 📡 Endpoint: PUT `/api/v1/profile/password`

**Content-Type**: `application/json`

**Accept**: `application/json`

**Needs Auth**: `YES`

**Returns JSON always.**

This endpoint allows an authenticated user to securely update their account password by providing their current password and the new one. It ensures password integrity by verifying the existing password and requiring confirmation of the new password. **It will automatically performs logout**

-------

### 📥 Request Body (JSON):


| Field              | Type     | Required  | Description             |
| ------------------ | -------- | --------- | ----------------------- |
| `current_password` | `string` | ✅        | User's current password |
| `password`         | `string` | ✅        | User's new password, at least 8 characters
| `password_confirmation` | `string` | ✅        | Same as new password

------

### ✅ Success Response:

If the password change is successful, the API responds with HTTP 200 OK, returning user profile data and a success message.

> HTTP Code: 200 OK

```json
{
    "success": true,
    "message": "Profile updated successfully",
    "data": {
        "id": 133,
        "name": "our-test-from-api",
        "email": "shavgulidzelasha66@gmail.com",
        "email_verified_at": "2025-07-09T15:20:52.000000Z",
        "two_factor_confirmed_at": null,
        "current_team_id": 45,
        "profile_photo_path": null,
        "source_id": null,
        "created_at": "2025-07-09T15:20:53.000000Z",
        "updated_at": "2025-08-01T00:07:04.000000Z",
        "last_renew_password_at": null,
        "profile_photo_url": "https://ui-avatars.com/api/?name=o&color=7F9CF5&background=EBF4FF"
    }
}
```


### ❌ Possible Error Responses

> HTTP Code: 422 (Unprocessable Entity)

```json
{
    "success": false,
    "errors": "The current password field is required."
}
```

> 😬 So you forgot a required field.

```json
{
    "success": false,
    "errors": "The password field confirmation does not match."
}
```

> Password confirmation is required (`password` and `password_confirmation` fields should be same)

```json
{
    "success": false,
    "message": "Current password is incorrect"
}
```

> If user's current password is not match actual current password