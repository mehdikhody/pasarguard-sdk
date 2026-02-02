# SettingsSchemaOutput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**telegram** | [**Telegram**](Telegram.md) |  | [optional] [default to undefined]
**discord** | [**Discord**](Discord.md) |  | [optional] [default to undefined]
**webhook** | [**Webhook**](Webhook.md) |  | [optional] [default to undefined]
**notification_settings** | [**NotificationSettingsOutput**](NotificationSettingsOutput.md) |  | [optional] [default to undefined]
**notification_enable** | [**NotificationEnable**](NotificationEnable.md) |  | [optional] [default to undefined]
**subscription** | [**SubscriptionOutput**](SubscriptionOutput.md) |  | [optional] [default to undefined]
**general** | [**General**](General.md) |  | [optional] [default to undefined]

## Example

```typescript
import { SettingsSchemaOutput } from './api';

const instance: SettingsSchemaOutput = {
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
