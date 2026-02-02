# HTTPResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**version** | **string** |  | [optional] [default to '1.1']
**headers** | **{ [key: string]: Array&lt;string&gt;; }** |  | [optional] [default to undefined]
**status** | **string** |  | [optional] [default to '200']
**reason** | **string** |  | [optional] [default to 'OK']

## Example

```typescript
import { HTTPResponse } from './api';

const instance: HTTPResponse = {
    version,
    headers,
    status,
    reason,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
