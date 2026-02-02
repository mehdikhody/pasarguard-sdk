# SettingsSchemaInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**telegram** | [**Telegram**](Telegram.md) |  | [optional] [default to undefined]
**discord** | [**Discord**](Discord.md) |  | [optional] [default to undefined]
**webhook** | [**Webhook**](Webhook.md) |  | [optional] [default to undefined]
**notification_settings** | [**NotificationSettingsInput**](NotificationSettingsInput.md) |  | [optional] [default to undefined]
**notification_enable** | [**NotificationEnable**](NotificationEnable.md) |  | [optional] [default to undefined]
**subscription** | [**SubscriptionInput**](SubscriptionInput.md) |  | [optional] [default to undefined]
**general** | [**General**](General.md) |  | [optional] [default to undefined]

## Example

```typescript
import { SettingsSchemaInput } from './api';

const instance: SettingsSchemaInput = {
    telegram,
    discord,
    webhook,
    notification_settings,
    notification_enable,
    subscription,
    general,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
