# XrayMuxSettingsInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **boolean** |  | [optional] [default to false]
**concurrency** | **number** |  | [optional] [default to undefined]
**xudp_concurrency** | **number** |  | [optional] [default to undefined]
**xudp_proxy_udp_443** | [**XUDP**](XUDP.md) |  | [optional] [default to undefined]

## Example

```typescript
import { XrayMuxSettingsInput } from './api';

const instance: XrayMuxSettingsInput = {
    enabled,
    concurrency,
    xudp_concurrency,
    xudp_proxy_udp_443,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
