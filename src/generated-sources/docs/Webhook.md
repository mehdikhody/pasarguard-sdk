# Webhook


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enable** | **boolean** |  | [optional] [default to false]
**webhooks** | [**Array&lt;WebhookInfo&gt;**](WebhookInfo.md) |  | [optional] [default to undefined]
**days_left** | **Array&lt;number&gt;** |  | [optional] [default to undefined]
**usage_percent** | **Array&lt;number&gt;** |  | [optional] [default to undefined]
**timeout** | **number** |  | [default to undefined]
**recurrent** | **number** |  | [default to undefined]
**proxy_url** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { Webhook } from './api';

const instance: Webhook = {
    enable,
    webhooks,
    days_left,
    usage_percent,
    timeout,
    recurrent,
    proxy_url,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
