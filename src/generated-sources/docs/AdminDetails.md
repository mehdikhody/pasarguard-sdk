# AdminDetails

Complete admin model with all fields for database representation and API responses.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**username** | **string** |  | [default to undefined]
**telegram_id** | **number** |  | [optional] [default to undefined]
**discord_webhook** | **string** |  | [optional] [default to undefined]
**sub_domain** | **string** |  | [optional] [default to undefined]
**profile_title** | **string** |  | [optional] [default to undefined]
**support_url** | **string** |  | [optional] [default to undefined]
**notification_enable** | [**UserNotificationEnable**](UserNotificationEnable.md) |  | [optional] [default to undefined]
**id** | **number** |  | [optional] [default to undefined]
**is_sudo** | **boolean** |  | [default to undefined]
**total_users** | **number** |  | [optional] [default to 0]
**used_traffic** | **number** |  | [optional] [default to 0]
**is_disabled** | **boolean** |  | [optional] [default to false]
**discord_id** | **number** |  | [optional] [default to undefined]
**sub_template** | **string** |  | [optional] [default to undefined]
**lifetime_used_traffic** | **number** |  | [optional] [default to undefined]

## Example

```typescript
import { AdminDetails } from './api';

const instance: AdminDetails = {
    username,
    telegram_id,
    discord_webhook,
    sub_domain,
    profile_title,
    support_url,
    notification_enable,
    id,
    is_sudo,
    total_users,
    used_traffic,
    is_disabled,
    discord_id,
    sub_template,
    lifetime_used_traffic,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
