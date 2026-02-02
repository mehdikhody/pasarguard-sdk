# GroupsApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**bulkAddGroupsToUsers**](#bulkaddgroupstousers) | **POST** /api/groups/bulk/add | Bulk add groups to users|
|[**bulkRemoveUsersFromGroups**](#bulkremoveusersfromgroups) | **POST** /api/groups/bulk/remove | Bulk remove groups from users|
|[**createGroup**](#creategroup) | **POST** /api/group | Create a new group|
|[**getAllGroups**](#getallgroups) | **GET** /api/groups | List all groups|
|[**getGroup**](#getgroup) | **GET** /api/group/{group_id} | Get group details|
|[**modifyGroup**](#modifygroup) | **PUT** /api/group/{group_id} | Modify group|
|[**removeGroup**](#removegroup) | **DELETE** /api/group/{group_id} | Remove group|

# **bulkAddGroupsToUsers**
> any bulkAddGroupsToUsers(bulkGroup)

Bulk assign groups to multiple users, users under specific admins, or all users.  - **group_ids**: List of group IDs to add (required) - **users**: Optional list of user IDs to assign the groups to - **admins**: Optional list of admin IDs — their users will be targeted  Notes: - If neither \'users\' nor \'admins\' are provided, groups will be added to *all users* - Existing user-group associations will be ignored (no duplication) - Returns list of affected users (those who received new group associations)

### Example

```typescript
import {
    GroupsApi,
    Configuration,
    BulkGroup
} from './api';

const configuration = new Configuration();
const apiInstance = new GroupsApi(configuration);

let bulkGroup: BulkGroup; //

const { status, data } = await apiInstance.bulkAddGroupsToUsers(
    bulkGroup
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **bulkGroup** | **BulkGroup**|  | |


### Return type

**any**

### Authorization

[OAuth2PasswordBearer](../README.md#OAuth2PasswordBearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success confirmation |  -  |
|**401** | Unauthorized Error |  * WWW-Authenticate - Authentication type <br>  |
|**403** | Forbidden Error |  -  |
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bulkRemoveUsersFromGroups**
> any bulkRemoveUsersFromGroups(bulkGroup)

Bulk remove groups from multiple users, users under specific admins, or all users.  - **group_ids**: List of group IDs to remove (required) - **users**: Optional list of user IDs to remove the groups from - **admins**: Optional list of admin IDs — their users will be targeted  Notes: - If neither \'users\' nor \'admins\' are provided, groups will be removed from *all users* - Only existing user-group associations will be removed - Returns list of affected users (those who had groups removed)

### Example

```typescript
import {
    GroupsApi,
    Configuration,
    BulkGroup
} from './api';

const configuration = new Configuration();
const apiInstance = new GroupsApi(configuration);

let bulkGroup: BulkGroup; //

const { status, data } = await apiInstance.bulkRemoveUsersFromGroups(
    bulkGroup
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **bulkGroup** | **BulkGroup**|  | |


### Return type

**any**

### Authorization

[OAuth2PasswordBearer](../README.md#OAuth2PasswordBearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success confirmation |  -  |
|**401** | Unauthorized Error |  * WWW-Authenticate - Authentication type <br>  |
|**403** | Forbidden Error |  -  |
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createGroup**
> GroupResponse createGroup(groupCreate)

Creates a new group in the system. Only sudo administrators can create groups.

### Example

```typescript
import {
    GroupsApi,
    Configuration,
    GroupCreate
} from './api';

const configuration = new Configuration();
const apiInstance = new GroupsApi(configuration);

let groupCreate: GroupCreate; //

const { status, data } = await apiInstance.createGroup(
    groupCreate
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupCreate** | **GroupCreate**|  | |


### Return type

**GroupResponse**

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

# **getAllGroups**
> GroupsResponse getAllGroups()

Retrieves a paginated list of all groups in the system. Requires admin authentication.

### Example

```typescript
import {
    GroupsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new GroupsApi(configuration);

let offset: number; // (optional) (default to undefined)
let limit: number; // (optional) (default to undefined)

const { status, data } = await apiInstance.getAllGroups(
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

**GroupsResponse**

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

# **getGroup**
> GroupResponse getGroup()

Retrieves detailed information about a specific group by its ID.

### Example

```typescript
import {
    GroupsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new GroupsApi(configuration);

let groupId: number; // (default to undefined)

const { status, data } = await apiInstance.getGroup(
    groupId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupId** | [**number**] |  | defaults to undefined|


### Return type

**GroupResponse**

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
|**404** | NotFound Error |  -  |
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **modifyGroup**
> GroupResponse modifyGroup(groupModify)

Updates an existing group\'s information. Only sudo administrators can modify groups.

### Example

```typescript
import {
    GroupsApi,
    Configuration,
    GroupModify
} from './api';

const configuration = new Configuration();
const apiInstance = new GroupsApi(configuration);

let groupId: number; // (default to undefined)
let groupModify: GroupModify; //

const { status, data } = await apiInstance.modifyGroup(
    groupId,
    groupModify
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupModify** | **GroupModify**|  | |
| **groupId** | [**number**] |  | defaults to undefined|


### Return type

**GroupResponse**

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

# **removeGroup**
> removeGroup()

Deletes a group from the system. Only sudo administrators can delete groups.

### Example

```typescript
import {
    GroupsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new GroupsApi(configuration);

let groupId: number; // (default to undefined)

const { status, data } = await apiInstance.removeGroup(
    groupId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupId** | [**number**] |  | defaults to undefined|


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

