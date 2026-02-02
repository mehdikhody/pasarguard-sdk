# AdminContactInfo

Base model containing the core admin identification fields.

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

## Example

```typescript
import { AdminContactInfo } from './api';

const instance: AdminContactInfo = {
    username,
    telegram_id,
    discord_webhook,
    sub_domain,
    profile_title,
    support_url,
    notification_enable,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
