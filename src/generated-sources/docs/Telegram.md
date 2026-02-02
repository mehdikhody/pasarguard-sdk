# Telegram


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enable** | **boolean** |  | [optional] [default to false]
**token** | **string** |  | [optional] [default to undefined]
**webhook_url** | **string** |  | [optional] [default to undefined]
**webhook_secret** | **string** |  | [optional] [default to undefined]
**proxy_url** | **string** |  | [optional] [default to undefined]
**method** | [**RunMethod**](RunMethod.md) |  | [optional] [default to undefined]
**mini_app_login** | **boolean** |  | [optional] [default to true]
**mini_app_web_url** | **string** |  | [optional] [default to undefined]
**for_admins_only** | **boolean** |  | [optional] [default to true]

## Example

```typescript
import { Telegram } from './api';

const instance: Telegram = {
    enable,
    token,
    webhook_url,
    webhook_secret,
    proxy_url,
    method,
    mini_app_login,
    mini_app_web_url,
    for_admins_only,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
