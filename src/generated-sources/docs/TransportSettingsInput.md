# TransportSettingsInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**xhttp_settings** | [**XHttpSettingsInput**](XHttpSettingsInput.md) |  | [optional] [default to undefined]
**grpc_settings** | [**GRPCSettings**](GRPCSettings.md) |  | [optional] [default to undefined]
**kcp_settings** | [**KCPSettings**](KCPSettings.md) |  | [optional] [default to undefined]
**tcp_settings** | [**TcpSettings**](TcpSettings.md) |  | [optional] [default to undefined]
**websocket_settings** | [**WebSocketSettings**](WebSocketSettings.md) |  | [optional] [default to undefined]

## Example

```typescript
import { TransportSettingsInput } from './api';

const instance: TransportSettingsInput = {
    xhttp_settings,
    grpc_settings,
    kcp_settings,
    tcp_settings,
    websocket_settings,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
