# HostApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createHost**](#createhost) | **POST** /api/host/ | Create Host|
|[**getHost**](#gethost) | **GET** /api/host/{host_id} | Get Host|
|[**getHosts**](#gethosts) | **GET** /api/hosts | Get Hosts|
|[**modifyHost**](#modifyhost) | **PUT** /api/host/{host_id} | Modify Host|
|[**modifyHosts**](#modifyhosts) | **PUT** /api/hosts | Modify Hosts|
|[**removeHost**](#removehost) | **DELETE** /api/host/{host_id} | Remove Host|

# **createHost**
> BaseHost createHost(createHost)

create a new host  **inbound_tag** must be available in one of xray config

### Example

```typescript
import {
    HostApi,
    Configuration,
    CreateHost
} from './api';

const configuration = new Configuration();
const apiInstance = new HostApi(configuration);

let createHost: CreateHost; //

const { status, data } = await apiInstance.createHost(
    createHost
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createHost** | **CreateHost**|  | |


### Return type

**BaseHost**

### Authorization

[OAuth2PasswordBearer](../README.md#OAuth2PasswordBearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** | Successful Response |  -  |
|**401** | Unauthorized Error |  * WWW-Authenticate - Authentication type <br>  |
|**403** | Forbidden Error |  -  |
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getHost**
> BaseHost getHost()

get host by **id**

### Example

```typescript
import {
    HostApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new HostApi(configuration);

let hostId: number; // (default to undefined)

const { status, data } = await apiInstance.getHost(
    hostId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hostId** | [**number**] |  | defaults to undefined|


### Return type

**BaseHost**

### Authorization

[OAuth2PasswordBearer](../README.md#OAuth2PasswordBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Successful Response |  -  |
|**401** | Unauthorized Error |  * WWW-Authenticate - Authentication type <br>  |
|**403** | Forbidden Error |  -  |
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getHosts**
> Array<BaseHost> getHosts()

Get proxy hosts.

### Example

```typescript
import {
    HostApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new HostApi(configuration);

let offset: number; // (optional) (default to 0)
let limit: number; // (optional) (default to 0)

const { status, data } = await apiInstance.getHosts(
    offset,
    limit
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **offset** | [**number**] |  | (optional) defaults to 0|
| **limit** | [**number**] |  | (optional) defaults to 0|


### Return type

**Array<BaseHost>**

### Authorization

[OAuth2PasswordBearer](../README.md#OAuth2PasswordBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Successful Response |  -  |
|**401** | Unauthorized Error |  * WWW-Authenticate - Authentication type <br>  |
|**403** | Forbidden Error |  -  |
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **modifyHost**
> BaseHost modifyHost(createHost)

modify host by **id**  **inbound_tag** must be available in one of xray configs

### Example

```typescript
import {
    HostApi,
    Configuration,
    CreateHost
} from './api';

const configuration = new Configuration();
const apiInstance = new HostApi(configuration);

let hostId: number; // (default to undefined)
let createHost: CreateHost; //

const { status, data } = await apiInstance.modifyHost(
    hostId,
    createHost
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createHost** | **CreateHost**|  | |
| **hostId** | [**number**] |  | defaults to undefined|


### Return type

**BaseHost**

### Authorization

[OAuth2PasswordBearer](../README.md#OAuth2PasswordBearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Successful Response |  -  |
|**401** | Unauthorized Error |  * WWW-Authenticate - Authentication type <br>  |
|**403** | Forbidden Error |  -  |
|**404** | NotFound Error |  -  |
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **modifyHosts**
> Array<BaseHost> modifyHosts(createHost)

Modify proxy hosts and update the configuration.

### Example

```typescript
import {
    HostApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new HostApi(configuration);

let createHost: Array<CreateHost>; //

const { status, data } = await apiInstance.modifyHosts(
    createHost
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createHost** | **Array<CreateHost>**|  | |


### Return type

**Array<BaseHost>**

### Authorization

[OAuth2PasswordBearer](../README.md#OAuth2PasswordBearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Successful Response |  -  |
|**401** | Unauthorized Error |  * WWW-Authenticate - Authentication type <br>  |
|**403** | Forbidden Error |  -  |
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **removeHost**
> removeHost()

remove host by **id**

### Example

```typescript
import {
    HostApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new HostApi(configuration);

let hostId: number; // (default to undefined)

const { status, data } = await apiInstance.removeHost(
    hostId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hostId** | [**number**] |  | defaults to undefined|


### Return type

void (empty response body)

### Authorization

[OAuth2PasswordBearer](../README.md#OAuth2PasswordBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**204** | Successful Response |  -  |
|**401** | Unauthorized Error |  * WWW-Authenticate - Authentication type <br>  |
|**403** | Forbidden Error |  -  |
|**404** | NotFound Error |  -  |
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

