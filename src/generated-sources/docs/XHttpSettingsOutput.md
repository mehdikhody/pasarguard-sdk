# XHttpSettingsOutput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**mode** | [**XHttpModes**](XHttpModes.md) |  | [optional] [default to undefined]
**no_grpc_header** | **boolean** |  | [optional] [default to undefined]
**x_padding_bytes** | **string** |  | [optional] [default to undefined]
**sc_max_each_post_bytes** | **string** |  | [optional] [default to undefined]
**sc_min_posts_interval_ms** | **string** |  | [optional] [default to undefined]
**xmux** | [**XMuxSettingsOutput**](XMuxSettingsOutput.md) |  | [optional] [default to undefined]
**download_settings** | **number** |  | [optional] [default to undefined]

## Example

```typescript
import { XHttpSettingsOutput } from './api';

const instance: XHttpSettingsOutput = {
    mode,
    no_grpc_header,
    x_padding_bytes,
    sc_max_each_post_bytes,
    sc_min_posts_interval_ms,
    xmux,
    download_settings,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
