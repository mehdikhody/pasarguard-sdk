# NotificationSettingsInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**notify_telegram** | **boolean** |  | [optional] [default to false]
**notify_discord** | **boolean** |  | [optional] [default to false]
**telegram_api_token** | **string** |  | [optional] [default to undefined]
**telegram_chat_id** | **number** |  | [optional] [default to undefined]
**telegram_topic_id** | **number** |  | [optional] [default to undefined]
**discord_webhook_url** | **string** |  | [optional] [default to undefined]
**channels** | [**NotificationChannels**](NotificationChannels.md) |  | [optional] [default to undefined]
**proxy_url** | **string** |  | [optional] [default to undefined]
**max_retries** | **number** |  | [default to undefined]

## Example

```typescript
import { NotificationSettingsInput } from './api';

const instance: NotificationSettingsInput = {
    notify_telegram,
    notify_discord,
    telegram_api_token,
    telegram_chat_id,
    telegram_topic_id,
    discord_webhook_url,
    channels,
    proxy_url,
    max_retries,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
