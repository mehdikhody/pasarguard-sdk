# ProxyTableInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**vmess** | [**VMessSettings**](VMessSettings.md) |  | [optional] [default to undefined]
**vless** | [**VlessSettings**](VlessSettings.md) |  | [optional] [default to undefined]
**trojan** | [**TrojanSettings**](TrojanSettings.md) |  | [optional] [default to undefined]
**shadowsocks** | [**ShadowsocksSettings**](ShadowsocksSettings.md) |  | [optional] [default to undefined]

## Example

```typescript
import { ProxyTableInput } from './api';

const instance: ProxyTableInput = {
    vmess,
    vless,
    trojan,
    shadowsocks,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
