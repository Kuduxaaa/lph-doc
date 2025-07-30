## 📡 Endpoint: POST `/api/v1/find-representation`

**Content-Type**: `application/json`

**Accept**: `application/json`

**Returns JSON always.**

-------

### 📥 Request Body (JSON):


| Field           | Type     | Required | Description                                                                                                                                                   |
| --------------- | -------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `case_type`     | `string` | ✅        | One of the following:<br>- `Auto Accident`<br>- `Personal Injury`<br>- `Workers Comp`<br>- `Slip And Fall`<br>- `Medical Malpractice`<br>- `Not Sure / Other` |
| `accident_time` | `string` | ❌        | Optional. Must be one of:<br>- `1 year ago`<br>- `2 years ago`<br>- `3 years ago`<br>- `More than 3 years ago`                                                |
| `hospitalized`  | `string` | ❌        | Must be either `yes` or `no`                                                                                                                                  |
| `at_fault`      | `string` | ❌        | Must be either `yes` or `no`                                                                                                                                  |
| `injured`       | `string` | ❌        | Must be either `yes` or `no`                                                                                                                                  |
| `law_firm`      | `string` | ❌        | Must be either `yes` or `no`                                                                                                                                  |
| `injury_type`   | `string` | ❌        | One of:<br>- `Back or Neck Pain`<br>- `Cuts and Bruises`<br>- `Headaches`<br>- `Broken Bones`<br>- `Other`                                                    |
| `case_details`  | `string` | ❌        | Optional. Max length: `500` characters                                                                                                                        |
| `full_name`     | `string` | ✅        | Full name of the person                                                                                                                                       |
| `phone_number`  | `string` | ✅        | Must be 12 digits (E.164 formatted). Invalid if starts with `+1`                                                                                              |
| `email`         | `string` | ✅        | Must be valid email format                                                                                                                                    |
| `zip_code`      | `string` | ✅        | Must be 5 characters                                                                                                                                          |

------

### ✅ Success Response:

> HTTP Code: 200 OK

```json
{
  "success": true,
  "message": "Submission received"
}
```

------

### ❌ Error Response (Validation or Logical Fail):

> HTTP Code: 422 (Unprocessable Entity) (Or may be 400, 404, 500)

```json
{
    "success": false,
    "message": "The selected case type is invalid."
}
```
