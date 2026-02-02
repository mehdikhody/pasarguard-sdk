# SubscriptionApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getSubUserUsage**](#getsubuserusage) | **GET** /sub/{token}/usage | Get Sub User Usage|
|[**userSubscription**](#usersubscription) | **GET** /sub/{token}/ | User Subscription|
|[**userSubscriptionApps**](#usersubscriptionapps) | **GET** /sub/{token}/apps | User Subscription Apps|
|[**userSubscriptionInfo**](#usersubscriptioninfo) | **GET** /sub/{token}/info | User Subscription Info|
|[**userSubscriptionWithClientType**](#usersubscriptionwithclienttype) | **GET** /sub/{token}/{client_type} | User Subscription With Client Type|

# **getSubUserUsage**
> UserUsageStatsList getSubUserUsage()

Fetches the usage statistics for the user within a specified date range.

### Example

```typescript
import {
    SubscriptionApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new SubscriptionApi(configuration);

let token: string; // (default to undefined)
let start: string; // (optional) (default to undefined)
let end: string; // (optional) (default to undefined)
let period: Period; // (optional) (default to undefined)

const { status, data } = await apiInstance.getSubUserUsage(
    token,
    start,
    end,
    period
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **token** | [**string**] |  | defaults to undefined|
| **start** | [**string**] |  | (optional) defaults to undefined|
| **end** | [**string**] |  | (optional) defaults to undefined|
| **period** | **Period** |  | (optional) defaults to undefined|


### Return type

**UserUsageStatsList**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Successful Response |  -  |
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **userSubscription**
> any userSubscription()

Provides a subscription link based on the user agent (Clash, V2Ray, etc.).

### Example

```typescript
import {
    SubscriptionApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new SubscriptionApi(configuration);

let token: string; // (default to undefined)
let userAgent: string; // (optional) (default to '')

const { status, data } = await apiInstance.userSubscription(
    token,
    userAgent
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **token** | [**string**] |  | defaults to undefined|
| **userAgent** | [**string**] |  | (optional) defaults to ''|


### Return type

**any**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Successful Response |  -  |
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **userSubscriptionApps**
> Array<ApplicationOutput> userSubscriptionApps()

Get applications available for user\'s subscription.

### Example

```typescript
import {
    SubscriptionApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new SubscriptionApi(configuration);

let token: string; // (default to undefined)

const { status, data } = await apiInstance.userSubscriptionApps(
    token
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **token** | [**string**] |  | defaults to undefined|


### Return type

**Array<ApplicationOutput>**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Successful Response |  -  |
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **userSubscriptionInfo**
> SubscriptionUserResponse userSubscriptionInfo()

Retrieves detailed information about the user\'s subscription.

### Example

```typescript
import {
    SubscriptionApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new SubscriptionApi(configuration);

let token: string; // (default to undefined)

const { status, data } = await apiInstance.userSubscriptionInfo(
    token
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **token** | [**string**] |  | defaults to undefined|


### Return type

**SubscriptionUserResponse**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Successful Response |  -  |
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **userSubscriptionWithClientType**
> any userSubscriptionWithClientType()

Provides a subscription link based on the specified client type (e.g., Clash, V2Ray).

### Example

```typescript
import {
    SubscriptionApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new SubscriptionApi(configuration);

let token: string; // (default to undefined)
let clientType: ConfigFormat; // (default to undefined)

const { status, data } = await apiInstance.userSubscriptionWithClientType(
    token,
    clientType
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **token** | [**string**] |  | defaults to undefined|
| **clientType** | **ConfigFormat** |  | defaults to undefined|


### Return type

**any**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Successful Response |  -  |
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

