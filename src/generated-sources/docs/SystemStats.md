# SystemStats


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**version** | **string** |  | [default to undefined]
**mem_total** | **number** |  | [optional] [default to undefined]
**mem_used** | **number** |  | [optional] [default to undefined]
**cpu_cores** | **number** |  | [optional] [default to undefined]
**cpu_usage** | **number** |  | [optional] [default to undefined]
**total_user** | **number** |  | [default to undefined]
**online_users** | **number** |  | [default to undefined]
**active_users** | **number** |  | [default to undefined]
**on_hold_users** | **number** |  | [default to undefined]
**disabled_users** | **number** |  | [default to undefined]
**expired_users** | **number** |  | [default to undefined]
**limited_users** | **number** |  | [default to undefined]
**incoming_bandwidth** | **number** |  | [default to undefined]
**outgoing_bandwidth** | **number** |  | [default to undefined]

## Example

```typescript
import { SystemStats } from './api';

const instance: SystemStats = {
    version,
    mem_total,
    mem_used,
    cpu_cores,
    cpu_usage,
    total_user,
    online_users,
    active_users,
    on_hold_users,
    disabled_users,
    expired_users,
    limited_users,
    incoming_bandwidth,
    outgoing_bandwidth,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
