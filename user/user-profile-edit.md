## 📡 Endpoint: PUT `/api/v1/profile`

**Content-Type**: `application/json`

**Accept**: `application/json`

**Needs Auth**: `YES`

**Returns JSON always.**

This endpoint allows an authenticated user to update their personal profile information, such as their name and email address. Fields that are not intended to change should be sent with their current values to avoid validation errors.


-------

### 📥 Request Body (JSON):



| Field           | Type     | Required | Description             |
| --------------- | -------- | -------- | ----------------------- |
| `name`          | `string` | ✅        | User's new name (Same as it is, if not changed) |
| `email`         | `string` | ✅        | User's new unique email (Same as it is, if not changed)

------

### ✅ Success Response:

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
