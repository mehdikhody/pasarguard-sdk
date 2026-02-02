# AdminsResponse

Response model for admins list with pagination and statistics.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**admins** | [**Array&lt;AdminDetails&gt;**](AdminDetails.md) |  | [default to undefined]
**total** | **number** |  | [default to undefined]
**active** | **number** |  | [default to undefined]
**disabled** | **number** |  | [default to undefined]

## Example

```typescript
import { AdminsResponse } from './api';

const instance: AdminsResponse = {
    admins,
    total,
    active,
    disabled,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
