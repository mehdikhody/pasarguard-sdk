# UserTemplateModify


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** |  | [optional] [default to undefined]
**data_limit** | **number** |  | [optional] [default to undefined]
**expire_duration** | **number** |  | [optional] [default to undefined]
**username_prefix** | **string** |  | [optional] [default to undefined]
**username_suffix** | **string** |  | [optional] [default to undefined]
**group_ids** | **Array&lt;number&gt;** |  | [optional] [default to undefined]
**extra_settings** | [**ExtraSettings**](ExtraSettings.md) |  | [optional] [default to undefined]
**status** | [**UserStatusCreate**](UserStatusCreate.md) |  | [optional] [default to undefined]
**reset_usages** | **boolean** |  | [optional] [default to undefined]
**on_hold_timeout** | **number** |  | [optional] [default to undefined]
**data_limit_reset_strategy** | [**DataLimitResetStrategy**](DataLimitResetStrategy.md) |  | [optional] [default to undefined]
**is_disabled** | **boolean** |  | [optional] [default to undefined]

## Example

```typescript
import { UserTemplateModify } from './api';

const instance: UserTemplateModify = {
    name,
    data_limit,
    expire_duration,
    username_prefix,
    username_suffix,
    group_ids,
    extra_settings,
    status,
    reset_usages,
    on_hold_timeout,
    data_limit_reset_strategy,
    is_disabled,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
