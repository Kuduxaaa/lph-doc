## 📡 Endpoint: POST `/api/v1/user/team/<TEAM_ID>/members/invite`

**Content-Type**: `application/json`

**Accept**: `application/json`

**Needs Auth**: `YES`

**Returns JSON always.**

Getting one team data.


-------

### 📥 Request Body (JSON):


| Field              | Type     | Required  | Description             |
| ------------------ | -------- | --------- | ----------------------- |
| `email` | `string` | ✅       | User's email address to invite |
| `role`  | `string` | ✅       | Role, one of these `admin` or `editor`

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
    "message": "User added to team."
}
```

### ❌ Possible Error Responses:

1. If already been invited (Code: `422 Unprocessable Entity`)

```json
{
    "success": false,
    "message": "This user has already been invited to the team."
}
```

2. Team/company not found (Code: `404 Not Found`)

```json
{
    "success": false,
    "message": "Company not found"
}
```

3. Incorrect role (Code: `422 Unprocessable Entity`)

```json
{
    "success": false,
    "errors": "The selected role is invalid."
}
```