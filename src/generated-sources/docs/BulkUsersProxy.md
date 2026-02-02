# BulkUsersProxy


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**flow** | [**XTLSFlows**](XTLSFlows.md) |  | [optional] [default to undefined]
**method** | [**ShadowsocksMethods**](ShadowsocksMethods.md) |  | [optional] [default to undefined]
**group_ids** | **Set&lt;number&gt;** |  | [optional] [default to undefined]
**admins** | **Set&lt;number&gt;** |  | [optional] [default to undefined]
**users** | **Set&lt;number&gt;** |  | [optional] [default to undefined]

## Example

```typescript
import { BulkUsersProxy } from './api';

const instance: BulkUsersProxy = {
    flow,
    method,
    group_ids,
    admins,
    users,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
