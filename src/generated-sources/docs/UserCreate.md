# UserCreate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**proxy_settings** | [**ProxyTableInput**](ProxyTableInput.md) |  | [optional] [default to undefined]
**expire** | [**Expire**](Expire.md) |  | [optional] [default to undefined]
**data_limit** | **number** |  | [optional] [default to undefined]
**data_limit_reset_strategy** | [**DataLimitResetStrategy**](DataLimitResetStrategy.md) |  | [optional] [default to undefined]
**note** | **string** |  | [optional] [default to undefined]
**on_hold_expire_duration** | **number** |  | [optional] [default to undefined]
**on_hold_timeout** | [**OnHoldTimeout**](OnHoldTimeout.md) |  | [optional] [default to undefined]
**group_ids** | **Array&lt;number&gt;** |  | [optional] [default to undefined]
**auto_delete_in_days** | **number** |  | [optional] [default to undefined]
**next_plan** | [**NextPlanModel**](NextPlanModel.md) |  | [optional] [default to undefined]
**username** | **string** |  | [default to undefined]
**status** | [**UserStatusCreate**](UserStatusCreate.md) |  | [optional] [default to undefined]

## Example

```typescript
import { UserCreate } from './api';

const instance: UserCreate = {
    proxy_settings,
    expire,
    data_limit,
    data_limit_reset_strategy,
    note,
    on_hold_expire_duration,
    on_hold_timeout,
    group_ids,
    auto_delete_in_days,
    next_plan,
    username,
    status,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
