# NodeModify


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** |  | [optional] [default to undefined]
**address** | **string** |  | [optional] [default to undefined]
**port** | **number** |  | [optional] [default to undefined]
**api_port** | **number** |  | [optional] [default to 62051]
**usage_coefficient** | **number** |  | [optional] [default to undefined]
**connection_type** | [**NodeConnectionType**](NodeConnectionType.md) |  | [optional] [default to undefined]
**server_ca** | **string** |  | [optional] [default to undefined]
**keep_alive** | **number** |  | [optional] [default to undefined]
**core_config_id** | **number** |  | [optional] [default to undefined]
**api_key** | **string** |  | [optional] [default to undefined]
**data_limit** | **number** |  | [optional] [default to undefined]
**data_limit_reset_strategy** | [**DataLimitResetStrategy**](DataLimitResetStrategy.md) |  | [optional] [default to undefined]
**reset_time** | **number** |  | [optional] [default to undefined]
**default_timeout** | **number** |  | [optional] [default to undefined]
**internal_timeout** | **number** |  | [optional] [default to undefined]
**status** | [**NodeStatus**](NodeStatus.md) |  | [optional] [default to undefined]

## Example

```typescript
import { NodeModify } from './api';

const instance: NodeModify = {
    name,
    address,
    port,
    api_port,
    usage_coefficient,
    connection_type,
    server_ca,
    keep_alive,
    core_config_id,
    api_key,
    data_limit,
    data_limit_reset_strategy,
    reset_time,
    default_timeout,
    internal_timeout,
    status,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
