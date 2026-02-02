# XMuxSettingsInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**max_concurrency** | [**MaxConcurrency**](MaxConcurrency.md) |  | [optional] [default to undefined]
**max_connections** | [**MaxConnections**](MaxConnections.md) |  | [optional] [default to undefined]
**c_max_reuse_times** | [**CMaxReuseTimes**](CMaxReuseTimes.md) |  | [optional] [default to undefined]
**h_max_reusable_secs** | [**HMaxReusableSecs**](HMaxReusableSecs.md) |  | [optional] [default to undefined]
**h_max_request_times** | [**HMaxRequestTimes**](HMaxRequestTimes.md) |  | [optional] [default to undefined]
**h_keep_alive_period** | **number** |  | [optional] [default to undefined]

## Example

```typescript
import { XMuxSettingsInput } from './api';

const instance: XMuxSettingsInput = {
    max_concurrency,
    max_connections,
    c_max_reuse_times,
    h_max_reusable_secs,
    h_max_request_times,
    h_keep_alive_period,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
