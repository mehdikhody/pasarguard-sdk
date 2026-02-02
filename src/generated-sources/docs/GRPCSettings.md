# GRPCSettings


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**multi_mode** | **boolean** |  | [optional] [default to false]
**idle_timeout** | **number** |  | [optional] [default to undefined]
**health_check_timeout** | **number** |  | [optional] [default to undefined]
**permit_without_stream** | **boolean** |  | [optional] [default to false]
**initial_windows_size** | **number** |  | [optional] [default to undefined]

## Example

```typescript
import { GRPCSettings } from './api';

const instance: GRPCSettings = {
    multi_mode,
    idle_timeout,
    health_check_timeout,
    permit_without_stream,
    initial_windows_size,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
