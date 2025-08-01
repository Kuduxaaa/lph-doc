## 📡 Endpoint: GET `/api/v1/auth/refresh`

**Content-Type**: `application/json`

**Accept**: `application/json`

**Needs Auth**: `YES`

**Returns JSON always.**

This endpoint is used to refresh an expired or soon-to-expire access token. It allows clients to maintain a user's authenticated session without requiring the user to log in again.

The client must provide a valid existing access token (obtained during login) in the Authorization header. If the token is valid and not blacklisted or invalidated, the server will issue a new token with a renewed expiration time, and return updated user information along with it.

This is typically used in token-based authentication flows (e.g., JWT) to support session continuity and avoid forcing users to frequently re-authenticate.

> ℹ️ This endpoint always returns JSON, and is protected by Bearer token authentication.

-------

### 🔒 Authentication (Bearer)

> Presented token should be received from [auth-login](https://github.com/Kuduxaaa/lph-doc/blob/main/auth/auth-login.md)

```
Authorization: Bearer [TOKEN...]
```


------

### ✅ Success Response:

> HTTP Code: 200 OK

```json
{
    "access_token": "eyJ0eXAi...",
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
