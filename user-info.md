## 📡 Endpoint: POST `/api/v1/user/info`

**Content-Type**: `application/json`

**Accept**: `application/json`

**Needs Auth**: `YES`

**Returns JSON always.**

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
    "user": {
        "id": 133,
        "name": "TEST CRM",
        "email": "shavgulidzelasha66@gmail.com",
        "email_verified_at": "2025-07-09T15:20:52.000000Z",
        "two_factor_confirmed_at": null,
        "current_team_id": 42,
        "profile_photo_path": null,
        "source_id": null,
        "created_at": "2025-07-09T15:20:53.000000Z",
        "updated_at": "2025-07-29T19:35:20.000000Z",
        "last_renew_password_at": null,
        "profile_photo_url": "https://ui-avatars.com/api/?name=T+C&color=7F9CF5&background=EBF4FF",
        "attorney": {
            "id": 42,
            "user_id": 133,
            "salutation": "mr",
            "first_name": "TEST",
            "last_name": "CRM",
            "email": "shavgulidzelasha66@gmail.com",
            "phone": "3827328829",
            "address": "TEST TEST",
            "license_details": null,
            "firm_name": "TEST CRM",
            "page_slug": "test-crm",
            "invite_over_phone": false,
            "show_thank_you_page": false,
            "max_reach_limit": 3,
            "refund_cost_percent": "100.00",
            "notes": "",
            "max_days_to_report_lead": 10,
            "min_days_to_report_unreachable": 2,
            "auto_assignment": false,
            "last_charge_at": "2025-07-09T15:20:53.000000Z",
            "next_cycle": "2025-08-09T15:20:53.000000Z",
            "attorney_payment_failed_status": false,
            "refill_status": "0",
            "next_lead": false,
            "created_at": "2025-07-09T15:20:53.000000Z",
            "updated_at": "2025-07-09T15:20:53.000000Z",
            "deleted_at": null
        },
        "current_team": {
            "id": 42,
            "user_id": 133,
            "name": "TEST CRM",
            "personal_team": false,
            "created_at": "2025-07-09T15:20:53.000000Z",
            "updated_at": "2025-07-09T15:20:53.000000Z",
            "owner": {
                "id": 133,
                "name": "TEST CRM",
                "email": "shavgulidzelasha66@gmail.com",
                "email_verified_at": "2025-07-09T15:20:52.000000Z",
                "two_factor_confirmed_at": null,
                "current_team_id": 42,
                "profile_photo_path": null,
                "source_id": null,
                "created_at": "2025-07-09T15:20:53.000000Z",
                "updated_at": "2025-07-29T19:35:20.000000Z",
                "last_renew_password_at": null,
                "profile_photo_url": "https://ui-avatars.com/api/?name=T+C&color=7F9CF5&background=EBF4FF",
                "attorney": {
                    "id": 42,
                    "user_id": 133,
                    "salutation": "mr",
                    "first_name": "TEST",
                    "last_name": "CRM",
                    "email": "shavgulidzelasha66@gmail.com",
                    "phone": "3827328829",
                    "address": "TEST TEST",
                    "license_details": null,
                    "firm_name": "TEST CRM",
                    "page_slug": "test-crm",
                    "invite_over_phone": false,
                    "show_thank_you_page": false,
                    "max_reach_limit": 3,
                    "refund_cost_percent": "100.00",
                    "notes": "",
                    "max_days_to_report_lead": 10,
                    "min_days_to_report_unreachable": 2,
                    "auto_assignment": false,
                    "last_charge_at": "2025-07-09T15:20:53.000000Z",
                    "next_cycle": "2025-08-09T15:20:53.000000Z",
                    "attorney_payment_failed_status": false,
                    "refill_status": "0",
                    "next_lead": false,
                    "created_at": "2025-07-09T15:20:53.000000Z",
                    "updated_at": "2025-07-09T15:20:53.000000Z",
                    "deleted_at": null
                }
            }
        }
    },
    "leads": [],
    "plans": [
        {
            "id": 51,
            "name": "TEST CRM",
            "attorney_id": 42,
            "case_type_id": 1,
            "number_of_leads": 10,
            "fee": 10000,
            "lead_cost": 1000,
            "currency": "USD",
            "enabled": true,
            "is_special": false,
            "test_mode": false,
            "created_at": "2025-07-09T15:20:53.000000Z",
            "updated_at": "2025-07-09T15:20:53.000000Z",
            "balance": 10000
        }
    ]
}
```
