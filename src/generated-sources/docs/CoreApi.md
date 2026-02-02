# CoreApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createCoreConfig**](#createcoreconfig) | **POST** /api/core | Create Core Config|
|[**deleteCoreConfig**](#deletecoreconfig) | **DELETE** /api/core/{core_id} | Delete Core Config|
|[**getAllCores**](#getallcores) | **GET** /api/cores | Get All Cores|
|[**getCoreConfig**](#getcoreconfig) | **GET** /api/core/{core_id} | Get Core Config|
|[**modifyCoreConfig**](#modifycoreconfig) | **PUT** /api/core/{core_id} | Modify Core Config|
|[**restartCore**](#restartcore) | **POST** /api/core/{core_id}/restart | Restart Core|

# **createCoreConfig**
> CoreResponse createCoreConfig(coreCreate)

Create a new core configuration.

### Example

```typescript
import {
    CoreApi,
    Configuration,
    CoreCreate
} from './api';

const configuration = new Configuration();
const apiInstance = new CoreApi(configuration);

let coreCreate: CoreCreate; //

const { status, data } = await apiInstance.createCoreConfig(
    coreCreate
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **coreCreate** | **CoreCreate**|  | |


### Return type

**CoreResponse**

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

# **deleteCoreConfig**
> deleteCoreConfig()

Delete a core configuration.

### Example

```typescript
import {
    CoreApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new CoreApi(configuration);

let coreId: number; // (default to undefined)
let restartNodes: boolean; // (optional) (default to false)

const { status, data } = await apiInstance.deleteCoreConfig(
    coreId,
    restartNodes
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **coreId** | [**number**] |  | defaults to undefined|
| **restartNodes** | [**boolean**] |  | (optional) defaults to false|


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
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getAllCores**
> CoreResponseList getAllCores()

Get a list of all core configurations.

### Example

```typescript
import {
    CoreApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new CoreApi(configuration);

let offset: number; // (optional) (default to undefined)
let limit: number; // (optional) (default to undefined)

const { status, data } = await apiInstance.getAllCores(
    offset,
    limit
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **offset** | [**number**] |  | (optional) defaults to undefined|
| **limit** | [**number**] |  | (optional) defaults to undefined|


### Return type

**CoreResponseList**

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

# **getCoreConfig**
> CoreResponse getCoreConfig()

Get a core configuration by its ID.

### Example

```typescript
import {
    CoreApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new CoreApi(configuration);

let coreId: number; // (default to undefined)

const { status, data } = await apiInstance.getCoreConfig(
    coreId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **coreId** | [**number**] |  | defaults to undefined|


### Return type

**CoreResponse**

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

# **modifyCoreConfig**
> CoreResponse modifyCoreConfig(coreCreate)

Update an existing core configuration.

### Example

```typescript
import {
    CoreApi,
    Configuration,
    CoreCreate
} from './api';

const configuration = new Configuration();
const apiInstance = new CoreApi(configuration);

let coreId: number; // (default to undefined)
let restartNodes: boolean; // (default to undefined)
let coreCreate: CoreCreate; //

const { status, data } = await apiInstance.modifyCoreConfig(
    coreId,
    restartNodes,
    coreCreate
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **coreCreate** | **CoreCreate**|  | |
| **coreId** | [**number**] |  | defaults to undefined|
| **restartNodes** | [**boolean**] |  | defaults to undefined|


### Return type

**CoreResponse**

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

# **restartCore**
> restartCore()

restart nodes related to the core config

### Example

```typescript
import {
    CoreApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new CoreApi(configuration);

let coreId: number; // (default to undefined)

const { status, data } = await apiInstance.restartCore(
    coreId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **coreId** | [**number**] |  | defaults to undefined|


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
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

