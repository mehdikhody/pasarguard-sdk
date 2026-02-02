# KCPSettings


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**header** | **string** |  | [optional] [default to 'none']
**mtu** | **number** |  | [optional] [default to undefined]
**tti** | **number** |  | [optional] [default to undefined]
**uplink_capacity** | **number** |  | [optional] [default to undefined]
**downlink_capacity** | **number** |  | [optional] [default to undefined]
**congestion** | **number** |  | [optional] [default to undefined]
**read_buffer_size** | **number** |  | [optional] [default to undefined]
**write_buffer_size** | **number** |  | [optional] [default to undefined]

## Example

```typescript
import { KCPSettings } from './api';

const instance: KCPSettings = {
    header,
    mtu,
    tti,
    uplink_capacity,
    downlink_capacity,
    congestion,
    read_buffer_size,
    write_buffer_size,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
