# ApplicationOutput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** |  | [default to undefined]
**icon_url** | **string** |  | [optional] [default to '']
**import_url** | **string** |  | [optional] [default to '']
**description** | **{ [key: string]: string; }** |  | [optional] [default to undefined]
**recommended** | **boolean** |  | [optional] [default to false]
**platform** | [**Platform**](Platform.md) |  | [default to undefined]
**download_links** | [**Array&lt;DownloadLink&gt;**](DownloadLink.md) |  | [default to undefined]

## Example

```typescript
import { ApplicationOutput } from './api';

const instance: ApplicationOutput = {
    name,
    icon_url,
    import_url,
    description,
    recommended,
    platform,
    download_links,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
