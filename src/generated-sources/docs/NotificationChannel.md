# NotificationChannel

Channel configuration for sending notifications to a specific entity

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**telegram_chat_id** | **number** |  | [optional] [default to undefined]
**telegram_topic_id** | **number** |  | [optional] [default to undefined]
**discord_webhook_url** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { NotificationChannel } from './api';

const instance: NotificationChannel = {
    telegram_chat_id,
    telegram_topic_id,
    discord_webhook_url,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
