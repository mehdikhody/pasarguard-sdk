# SubscriptionInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url_prefix** | **string** |  | [optional] [default to '']
**update_interval** | **number** |  | [optional] [default to 12]
**support_url** | **string** |  | [optional] [default to 'https://t.me/']
**profile_title** | **string** |  | [optional] [default to 'Subscription']
**announce** | **string** |  | [optional] [default to '']
**announce_url** | **string** |  | [optional] [default to '']
**rules** | [**Array&lt;SubRule&gt;**](SubRule.md) |  | [default to undefined]
**manual_sub_request** | [**SubFormatEnable**](SubFormatEnable.md) |  | [optional] [default to undefined]
**applications** | [**Array&lt;ApplicationInput&gt;**](ApplicationInput.md) |  | [optional] [default to undefined]
**allow_browser_config** | **boolean** |  | [optional] [default to true]
**disable_sub_template** | **boolean** |  | [optional] [default to false]

## Example

```typescript
import { SubscriptionInput } from './api';

const instance: SubscriptionInput = {
    url_prefix,
    update_interval,
    support_url,
    profile_title,
    announce,
    announce_url,
    rules,
    manual_sub_request,
    applications,
    allow_browser_config,
    disable_sub_template,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
