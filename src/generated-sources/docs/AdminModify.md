# AdminModify


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**password** | **string** |  | [optional] [default to undefined]
**is_sudo** | **boolean** |  | [default to undefined]
**telegram_id** | **number** |  | [optional] [default to undefined]
**discord_webhook** | **string** |  | [optional] [default to undefined]
**discord_id** | **number** |  | [optional] [default to undefined]
**is_disabled** | **boolean** |  | [optional] [default to undefined]
**sub_template** | **string** |  | [optional] [default to undefined]
**sub_domain** | **string** |  | [optional] [default to undefined]
**profile_title** | **string** |  | [optional] [default to undefined]
**support_url** | **string** |  | [optional] [default to undefined]
**notification_enable** | [**UserNotificationEnable**](UserNotificationEnable.md) |  | [optional] [default to undefined]

## Example

```typescript
import { AdminModify } from './api';

const instance: AdminModify = {
    password,
    is_sudo,
    telegram_id,
    discord_webhook,
    discord_id,
    is_disabled,
    sub_template,
    sub_domain,
    profile_title,
    support_url,
    notification_enable,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
