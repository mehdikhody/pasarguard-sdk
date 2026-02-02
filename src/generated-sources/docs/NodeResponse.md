# NodeResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** |  | [default to undefined]
**address** | **string** |  | [default to undefined]
**port** | **number** |  | [optional] [default to 62050]
**api_port** | **number** |  | [optional] [default to 62051]
**usage_coefficient** | **number** |  | [optional] [default to 1.0]
**connection_type** | [**NodeConnectionType**](NodeConnectionType.md) |  | [default to undefined]
**server_ca** | **string** |  | [default to undefined]
**keep_alive** | **number** |  | [default to undefined]
**core_config_id** | **number** |  | [default to undefined]
**api_key** | **string** |  | [default to undefined]
**data_limit** | **number** |  | [optional] [default to 0]
**data_limit_reset_strategy** | [**DataLimitResetStrategy**](DataLimitResetStrategy.md) |  | [optional] [default to undefined]
**reset_time** | **number** |  | [optional] [default to -1]
**default_timeout** | **number** |  | [optional] [default to 10]
**internal_timeout** | **number** |  | [optional] [default to 15]
**id** | **number** |  | [default to undefined]
**xray_version** | **string** |  | [default to undefined]
**node_version** | **string** |  | [default to undefined]
**status** | [**NodeStatus**](NodeStatus.md) |  | [default to undefined]
**message** | **string** |  | [default to undefined]
**uplink** | **number** |  | [optional] [default to 0]
**downlink** | **number** |  | [optional] [default to 0]
**lifetime_uplink** | **number** |  | [optional] [default to undefined]
**lifetime_downlink** | **number** |  | [optional] [default to undefined]

## Example

```typescript
import { NodeResponse } from './api';

const instance: NodeResponse = {
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
    id,
    xray_version,
    node_version,
    status,
    message,
    uplink,
    downlink,
    lifetime_uplink,
    lifetime_downlink,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
