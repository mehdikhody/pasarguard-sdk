# UserResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**proxy_settings** | [**ProxyTableOutput**](ProxyTableOutput.md) |  | [optional] [default to undefined]
**expire** | [**Expire**](Expire.md) |  | [optional] [default to undefined]
**data_limit** | **number** |  | [optional] [default to undefined]
**data_limit_reset_strategy** | [**DataLimitResetStrategy**](DataLimitResetStrategy.md) |  | [optional] [default to undefined]
**note** | **string** |  | [optional] [default to undefined]
**on_hold_expire_duration** | **number** |  | [optional] [default to undefined]
**on_hold_timeout** | [**OnHoldTimeout**](OnHoldTimeout.md) |  | [optional] [default to undefined]
**group_ids** | **Array&lt;number&gt;** |  | [optional] [default to undefined]
**auto_delete_in_days** | **number** |  | [optional] [default to undefined]
**next_plan** | [**NextPlanModel**](NextPlanModel.md) |  | [optional] [default to undefined]
**id** | **number** |  | [default to undefined]
**username** | **string** |  | [default to undefined]
**status** | [**UserStatus**](UserStatus.md) |  | [default to undefined]
**used_traffic** | **number** |  | [default to undefined]
**lifetime_used_traffic** | **number** |  | [optional] [default to 0]
**created_at** | **string** |  | [default to undefined]
**edit_at** | **string** |  | [optional] [default to undefined]
**online_at** | **string** |  | [optional] [default to undefined]
**subscription_url** | **string** |  | [optional] [default to '']
**admin** | [**AdminBase**](AdminBase.md) |  | [optional] [default to undefined]

## Example

```typescript
import { UserResponse } from './api';

const instance: UserResponse = {
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
    id,
    username,
    status,
    used_traffic,
    lifetime_used_traffic,
    created_at,
    edit_at,
    online_at,
    subscription_url,
    admin,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
