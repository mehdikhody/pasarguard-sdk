# ClashMuxSettings


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enable** | **boolean** |  | [optional] [default to false]
**protocol** | [**MultiplexProtocol**](MultiplexProtocol.md) |  | [optional] [default to undefined]
**max_connections** | **number** |  | [optional] [default to undefined]
**max_streams** | **number** |  | [optional] [default to undefined]
**min_streams** | **number** |  | [optional] [default to undefined]
**padding** | **boolean** |  | [optional] [default to false]
**brutal** | [**Brutal**](Brutal.md) |  | [optional] [default to undefined]
**statistic** | **boolean** |  | [optional] [default to false]
**only_tcp** | **boolean** |  | [optional] [default to false]

## Example

```typescript
import { ClashMuxSettings } from './api';

const instance: ClashMuxSettings = {
    enable,
    protocol,
    max_connections,
    max_streams,
    min_streams,
    padding,
    brutal,
    statistic,
    only_tcp,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
