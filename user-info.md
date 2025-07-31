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
        "current_team_id": 45,
        "profile_photo_path": null,
        "source_id": null,
        "created_at": "2025-07-09T15:20:53.000000Z",
        "updated_at": "2025-07-31T14:38:48.000000Z",
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
            "id": 45,
            "user_id": 133,
            "name": "test company",
            "personal_team": false,
            "created_at": "2025-07-28T15:53:25.000000Z",
            "updated_at": "2025-07-28T15:53:25.000000Z",
            "owner": {
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
    "leads": [
        {
            "id": 29807,
            "name": "lkn",
            "phone_number": "+11111111111",
            "email": "dsakl@nlks.com",
            "zip_codes_id": 9654,
            "case_type": "Auto Accident",
            "case_history": "nlkn",
            "ip_address": "185.132.178.140",
            "status": "assigned",
            "spam_score": null,
            "attorney_id": 42,
            "plan_id": 51,
            "cost": null,
            "price": 1000,
            "score": null,
            "source_id": 2,
            "source_subid": null,
            "qualified_by": "Admin",
            "accepted_tos": false,
            "collected_at": "2025-07-30T12:16:31.000000Z",
            "auto_assign_reason": null,
            "note": null,
            "followup_status": null,
            "starred": false,
            "disqualify": false,
            "call_ended": false,
            "dont_call_back": false,
            "opted_out": false,
            "unresponsive": false,
            "test_mode": false,
            "call_counter": 0,
            "case_type_id": 1,
            "state_name": "Virginia",
            "sub_id": null,
            "created_at": "2025-07-30T12:16:31.000000Z",
            "updated_at": "2025-07-30T16:50:28.000000Z",
            "deleted_at": null
        },
        {
            "id": 29808,
            "name": "John Doe",
            "phone_number": "555-1234",
            "email": "john@example.com",
            "zip_codes_id": 13086,
            "case_type": "Personal Injury",
            "case_history": "Car accident on I-95",
            "ip_address": "54.86.50.139",
            "status": "assigned",
            "spam_score": null,
            "attorney_id": 42,
            "plan_id": 51,
            "cost": null,
            "price": 1000,
            "score": null,
            "source_id": 2,
            "source_subid": null,
            "qualified_by": "Admin",
            "accepted_tos": false,
            "collected_at": "2025-07-30T12:55:37.000000Z",
            "auto_assign_reason": null,
            "note": null,
            "followup_status": null,
            "starred": false,
            "disqualify": false,
            "call_ended": false,
            "dont_call_back": false,
            "opted_out": false,
            "unresponsive": false,
            "test_mode": false,
            "call_counter": 0,
            "case_type_id": 2,
            "state_name": "Georgia",
            "sub_id": null,
            "created_at": "2025-07-30T12:55:37.000000Z",
            "updated_at": "2025-07-30T17:03:18.000000Z",
            "deleted_at": null
        },
        {
            "id": 29810,
            "name": "Jane Doe",
            "phone_number": "+11234567890",
            "email": "jane.doe@example.com",
            "zip_codes_id": 38206,
            "case_type": "Auto Accident",
            "case_history": "Rear-ended by another driver on the highway. Still experiencing pain.",
            "ip_address": "54.86.50.139",
            "status": "assigned",
            "spam_score": null,
            "attorney_id": 42,
            "plan_id": 51,
            "cost": null,
            "price": 1000,
            "score": null,
            "source_id": 2,
            "source_subid": null,
            "qualified_by": "Admin",
            "accepted_tos": false,
            "collected_at": "2025-07-30T13:30:24.000000Z",
            "auto_assign_reason": null,
            "note": null,
            "followup_status": null,
            "starred": false,
            "disqualify": false,
            "call_ended": false,
            "dont_call_back": false,
            "opted_out": false,
            "unresponsive": false,
            "test_mode": false,
            "call_counter": 1,
            "case_type_id": 1,
            "state_name": "California",
            "sub_id": null,
            "created_at": "2025-07-30T13:30:24.000000Z",
            "updated_at": "2025-07-30T17:02:55.000000Z",
            "deleted_at": null
        }
    ],
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
            "balance": 7000
        }
    ]
}
```
