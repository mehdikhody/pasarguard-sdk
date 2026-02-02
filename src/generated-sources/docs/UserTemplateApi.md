# UserTemplateApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createUserTemplate**](#createusertemplate) | **POST** /api/user_template | Create User Template|
|[**getUserTemplate**](#getusertemplate) | **GET** /api/user_template/{template_id} | Get User Template|
|[**getUserTemplates**](#getusertemplates) | **GET** /api/user_templates | Get User Templates|
|[**modifyUserTemplate**](#modifyusertemplate) | **PUT** /api/user_template/{template_id} | Modify User Template|
|[**removeUserTemplate**](#removeusertemplate) | **DELETE** /api/user_template/{template_id} | Remove User Template|

# **createUserTemplate**
> UserTemplateResponse createUserTemplate(userTemplateCreate)

Create a new user template  - **name** can be up to 64 characters - **data_limit** must be in bytes and larger or equal to 0 - **expire_duration** must be in seconds and larger or equat to 0 - **group_ids** list of group ids

### Example

```typescript
import {
    UserTemplateApi,
    Configuration,
    UserTemplateCreate
} from './api';

const configuration = new Configuration();
const apiInstance = new UserTemplateApi(configuration);

let userTemplateCreate: UserTemplateCreate; //

const { status, data } = await apiInstance.createUserTemplate(
    userTemplateCreate
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userTemplateCreate** | **UserTemplateCreate**|  | |


### Return type

**UserTemplateResponse**

### Authorization

[OAuth2PasswordBearer](../README.md#OAuth2PasswordBearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** | Successful Response |  -  |
|**403** | Forbidden Error |  -  |
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getUserTemplate**
> UserTemplateResponse getUserTemplate()

Get User Template information with id

### Example

```typescript
import {
    UserTemplateApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new UserTemplateApi(configuration);

let templateId: number; // (default to undefined)

const { status, data } = await apiInstance.getUserTemplate(
    templateId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **templateId** | [**number**] |  | defaults to undefined|


### Return type

**UserTemplateResponse**

### Authorization

[OAuth2PasswordBearer](../README.md#OAuth2PasswordBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Successful Response |  -  |
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getUserTemplates**
> Array<UserTemplateResponse> getUserTemplates()

Get a list of User Templates with optional pagination

### Example

```typescript
import {
    UserTemplateApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new UserTemplateApi(configuration);

let offset: number; // (optional) (default to undefined)
let limit: number; // (optional) (default to undefined)

const { status, data } = await apiInstance.getUserTemplates(
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

**Array<UserTemplateResponse>**

### Authorization

[OAuth2PasswordBearer](../README.md#OAuth2PasswordBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Successful Response |  -  |
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **modifyUserTemplate**
> UserTemplateResponse modifyUserTemplate(userTemplateModify)

Modify User Template  - **name** can be up to 64 characters - **data_limit** must be in bytes and larger or equal to 0 - **expire_duration** must be in seconds and larger or equat to 0 - **group_ids** list of group ids

### Example

```typescript
import {
    UserTemplateApi,
    Configuration,
    UserTemplateModify
} from './api';

const configuration = new Configuration();
const apiInstance = new UserTemplateApi(configuration);

let templateId: number; // (default to undefined)
let userTemplateModify: UserTemplateModify; //

const { status, data } = await apiInstance.modifyUserTemplate(
    templateId,
    userTemplateModify
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userTemplateModify** | **UserTemplateModify**|  | |
| **templateId** | [**number**] |  | defaults to undefined|


### Return type

**UserTemplateResponse**

### Authorization

[OAuth2PasswordBearer](../README.md#OAuth2PasswordBearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Successful Response |  -  |
|**403** | Forbidden Error |  -  |
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **removeUserTemplate**
> removeUserTemplate()

Remove a User Template by its ID

### Example

```typescript
import {
    UserTemplateApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new UserTemplateApi(configuration);

let templateId: number; // (default to undefined)

const { status, data } = await apiInstance.removeUserTemplate(
    templateId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **templateId** | [**number**] |  | defaults to undefined|


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
|**403** | Forbidden Error |  -  |
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

