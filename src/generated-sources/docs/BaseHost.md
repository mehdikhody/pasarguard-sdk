# BaseHost


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **number** |  | [optional] [default to undefined]
**remark** | **string** |  | [default to undefined]
**address** | **Set&lt;string&gt;** |  | [optional] [default to undefined]
**inbound_tag** | **string** |  | [optional] [default to undefined]
**port** | **number** |  | [optional] [default to undefined]
**sni** | **Set&lt;string&gt;** |  | [optional] [default to undefined]
**host** | **Set&lt;string&gt;** |  | [optional] [default to undefined]
**path** | **string** |  | [optional] [default to undefined]
**security** | [**ProxyHostSecurity**](ProxyHostSecurity.md) |  | [optional] [default to undefined]
**alpn** | [**Array&lt;ProxyHostALPN&gt;**](ProxyHostALPN.md) |  | [optional] [default to undefined]
**fingerprint** | [**ProxyHostFingerprint**](ProxyHostFingerprint.md) |  | [optional] [default to undefined]
**allowinsecure** | **boolean** |  | [optional] [default to undefined]
**is_disabled** | **boolean** |  | [optional] [default to false]
**http_headers** | **{ [key: string]: string; }** |  | [optional] [default to undefined]
**transport_settings** | [**TransportSettingsOutput**](TransportSettingsOutput.md) |  | [optional] [default to undefined]
**mux_settings** | [**MuxSettingsOutput**](MuxSettingsOutput.md) |  | [optional] [default to undefined]
**fragment_settings** | [**FragmentSettings**](FragmentSettings.md) |  | [optional] [default to undefined]
**noise_settings** | [**NoiseSettings**](NoiseSettings.md) |  | [optional] [default to undefined]
**random_user_agent** | **boolean** |  | [optional] [default to false]
**use_sni_as_host** | **boolean** |  | [optional] [default to false]
**priority** | **number** |  | [default to undefined]
**status** | [**Set&lt;UserStatus&gt;**](UserStatus.md) |  | [optional] [default to undefined]
**ech_config_list** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { BaseHost } from './api';

const instance: BaseHost = {
    id,
    remark,
    address,
    inbound_tag,
    port,
    sni,
    host,
    path,
    security,
    alpn,
    fingerprint,
    allowinsecure,
    is_disabled,
    http_headers,
    transport_settings,
    mux_settings,
    fragment_settings,
    noise_settings,
    random_user_agent,
    use_sni_as_host,
    priority,
    status,
    ech_config_list,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
