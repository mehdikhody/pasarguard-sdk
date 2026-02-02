# UserApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**activeNextPlan**](#activenextplan) | **POST** /api/user/{username}/active_next | Active Next Plan|
|[**bulkCreateUsersFromTemplate**](#bulkcreateusersfromtemplate) | **POST** /api/users/bulk/from_template | Bulk Create Users From Template|
|[**bulkModifyUsersDatalimit**](#bulkmodifyusersdatalimit) | **POST** /api/users/bulk/data_limit | Bulk sum/sub to data limit of users|
|[**bulkModifyUsersExpire**](#bulkmodifyusersexpire) | **POST** /api/users/bulk/expire | Bulk sum/sub to expire of users|
|[**bulkModifyUsersProxySettings**](#bulkmodifyusersproxysettings) | **POST** /api/users/bulk/proxy_settings | Bulk modify users proxy settings|
|[**createUser**](#createuser) | **POST** /api/user | Create User|
|[**createUserFromTemplate**](#createuserfromtemplate) | **POST** /api/user/from_template | Create User From Template|
|[**deleteExpiredUsers**](#deleteexpiredusers) | **DELETE** /api/users/expired | Delete Expired Users|
|[**getExpiredUsers**](#getexpiredusers) | **GET** /api/users/expired | Get Expired Users|
|[**getUser**](#getuser) | **GET** /api/user/{username} | Get User|
|[**getUserSubUpdateList**](#getusersubupdatelist) | **GET** /api/user/{username}/sub_update | Get User Sub Update List|
|[**getUserUsage**](#getuserusage) | **GET** /api/user/{username}/usage | Get User Usage|
|[**getUsers**](#getusers) | **GET** /api/users | Get Users|
|[**getUsersSubUpdateChart**](#getuserssubupdatechart) | **GET** /api/users/sub_update/chart | Get Users Sub Update Chart|
|[**getUsersUsage**](#getusersusage) | **GET** /api/users/usage | Get Users Usage|
|[**modifyUser**](#modifyuser) | **PUT** /api/user/{username} | Modify User|
|[**modifyUserWithTemplate**](#modifyuserwithtemplate) | **PUT** /api/user/from_template/{username} | Modify User With Template|
|[**removeUser**](#removeuser) | **DELETE** /api/user/{username} | Remove User|
|[**resetUserDataUsage**](#resetuserdatausage) | **POST** /api/user/{username}/reset | Reset User Data Usage|
|[**resetUsersDataUsage**](#resetusersdatausage) | **POST** /api/users/reset | Reset Users Data Usage|
|[**revokeUserSubscription**](#revokeusersubscription) | **POST** /api/user/{username}/revoke_sub | Revoke User Subscription|
|[**setOwner**](#setowner) | **PUT** /api/user/{username}/set_owner | Set Owner|

# **activeNextPlan**
> UserResponse activeNextPlan()

Reset user by next plan

### Example

```typescript
import {
    UserApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new UserApi(configuration);

let username: string; // (default to undefined)

const { status, data } = await apiInstance.activeNextPlan(
    username
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|


### Return type

**UserResponse**

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

# **bulkCreateUsersFromTemplate**
> BulkUsersCreateResponse bulkCreateUsersFromTemplate(bulkUsersFromTemplate)

Bulk create users from a template using configurable username strategies.  - Includes the template creation fields plus `count`, `strategy`, and `start_number` (for sequences). - **strategy**: Username generation strategy — `sequence` or `random`. - **start_number**: Optional starting suffix for `sequence` strategy. Defaults to `1` and does not parse numbers from the base username.  Returns subscription URLs for created users.

### Example

```typescript
import {
    UserApi,
    Configuration,
    BulkUsersFromTemplate
} from './api';

const configuration = new Configuration();
const apiInstance = new UserApi(configuration);

let bulkUsersFromTemplate: BulkUsersFromTemplate; //

const { status, data } = await apiInstance.bulkCreateUsersFromTemplate(
    bulkUsersFromTemplate
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **bulkUsersFromTemplate** | **BulkUsersFromTemplate**|  | |


### Return type

**BulkUsersCreateResponse**

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
|**400** | BadRequest Error |  -  |
|**403** | Forbidden Error |  -  |
|**404** | NotFound Error |  -  |
|**409** | Conflict Error |  -  |
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bulkModifyUsersDatalimit**
> any bulkModifyUsersDatalimit(bulkUser)

Bulk modify users\' data limit based on the provided criteria.  - **amount**: amount to adjust the user\'s quota (positive to increase, negative to decrease) required - **user_ids**: Optional list of user IDs to modify - **admins**: Optional list of admin IDs — their users will be targeted - **status**: Optional status to filter users (e.g., \"expired\", \"active\"), Empty means no filtering - **group_ids**: Optional list of group IDs to filter users by their group membership

### Example

```typescript
import {
    UserApi,
    Configuration,
    BulkUser
} from './api';

const configuration = new Configuration();
const apiInstance = new UserApi(configuration);

let bulkUser: BulkUser; //

const { status, data } = await apiInstance.bulkModifyUsersDatalimit(
    bulkUser
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **bulkUser** | **BulkUser**|  | |


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
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bulkModifyUsersExpire**
> any bulkModifyUsersExpire(bulkUser)

Bulk expire users based on the provided criteria.  - **amount**: amount to adjust the user\'s quota (in seconds, positive to increase, negative to decrease) required - **user_ids**: Optional list of user IDs to modify - **admins**: Optional list of admin IDs — their users will be targeted - **status**: Optional status to filter users (e.g., \"expired\", \"active\"), Empty means no filtering - **group_ids**: Optional list of group IDs to filter users by their group membership

### Example

```typescript
import {
    UserApi,
    Configuration,
    BulkUser
} from './api';

const configuration = new Configuration();
const apiInstance = new UserApi(configuration);

let bulkUser: BulkUser; //

const { status, data } = await apiInstance.bulkModifyUsersExpire(
    bulkUser
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **bulkUser** | **BulkUser**|  | |


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
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bulkModifyUsersProxySettings**
> any bulkModifyUsersProxySettings(bulkUsersProxy)


### Example

```typescript
import {
    UserApi,
    Configuration,
    BulkUsersProxy
} from './api';

const configuration = new Configuration();
const apiInstance = new UserApi(configuration);

let bulkUsersProxy: BulkUsersProxy; //

const { status, data } = await apiInstance.bulkModifyUsersProxySettings(
    bulkUsersProxy
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **bulkUsersProxy** | **BulkUsersProxy**|  | |


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
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createUser**
> UserResponse createUser(userCreate)

Create a new user  - **username**: 3 to 32 characters, can include a-z, 0-9, and underscores. - **status**: User\'s status, defaults to `active`. Special rules if `on_hold`. - **expire**: UTC datetime for account expiration. Use `0` for unlimited. - **data_limit**: Max data usage in bytes (e.g., `1073741824` for 1GB). `0` means unlimited. - **data_limit_reset_strategy**: Defines how/if data limit resets. `no_reset` means it never resets. - **proxy_settings**: Dictionary of protocol settings (e.g., `vmess`, `vless`) will generate data for all protocol by default. - **group_ids**: List of group IDs to assign to the user. - **note**: Optional text field for additional user information or notes. - **on_hold_timeout**: UTC timestamp when `on_hold` status should start or end. - **on_hold_expire_duration**: Duration (in seconds) for how long the user should stay in `on_hold` status. - **next_plan**: Next user plan (resets after use).

### Example

```typescript
import {
    UserApi,
    Configuration,
    UserCreate
} from './api';

const configuration = new Configuration();
const apiInstance = new UserApi(configuration);

let userCreate: UserCreate; //

const { status, data } = await apiInstance.createUser(
    userCreate
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userCreate** | **UserCreate**|  | |


### Return type

**UserResponse**

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
|**400** | BadRequest Error |  -  |
|**409** | Conflict Error |  -  |
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createUserFromTemplate**
> UserResponse createUserFromTemplate(createUserFromTemplate)


### Example

```typescript
import {
    UserApi,
    Configuration,
    CreateUserFromTemplate
} from './api';

const configuration = new Configuration();
const apiInstance = new UserApi(configuration);

let createUserFromTemplate: CreateUserFromTemplate; //

const { status, data } = await apiInstance.createUserFromTemplate(
    createUserFromTemplate
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createUserFromTemplate** | **CreateUserFromTemplate**|  | |


### Return type

**UserResponse**

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
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteExpiredUsers**
> RemoveUsersResponse deleteExpiredUsers()

Delete users who have expired within the specified date range.  - **expired_after** UTC datetime (optional) - **expired_before** UTC datetime (optional) - At least one of expired_after or expired_before must be provided

### Example

```typescript
import {
    UserApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new UserApi(configuration);

let adminUsername: string; // (optional) (default to undefined)
let expiredAfter: string; // (optional) (default to undefined)
let expiredBefore: string; // (optional) (default to undefined)

const { status, data } = await apiInstance.deleteExpiredUsers(
    adminUsername,
    expiredAfter,
    expiredBefore
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **adminUsername** | [**string**] |  | (optional) defaults to undefined|
| **expiredAfter** | [**string**] |  | (optional) defaults to undefined|
| **expiredBefore** | [**string**] |  | (optional) defaults to undefined|


### Return type

**RemoveUsersResponse**

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
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getExpiredUsers**
> Array<string | null> getExpiredUsers()

Get users who have expired within the specified date range.  - **expired_after** UTC datetime (optional) - **expired_before** UTC datetime (optional) - At least one of expired_after or expired_before must be provided for filtering - If both are omitted, returns all expired users

### Example

```typescript
import {
    UserApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new UserApi(configuration);

let adminUsername: string; // (optional) (default to undefined)
let expiredAfter: string; // (optional) (default to undefined)
let expiredBefore: string; // (optional) (default to undefined)

const { status, data } = await apiInstance.getExpiredUsers(
    adminUsername,
    expiredAfter,
    expiredBefore
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **adminUsername** | [**string**] |  | (optional) defaults to undefined|
| **expiredAfter** | [**string**] |  | (optional) defaults to undefined|
| **expiredBefore** | [**string**] |  | (optional) defaults to undefined|


### Return type

**Array<string | null>**

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
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getUser**
> UserResponse getUser()

Get user information

### Example

```typescript
import {
    UserApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new UserApi(configuration);

let username: string; // (default to undefined)

const { status, data } = await apiInstance.getUser(
    username
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|


### Return type

**UserResponse**

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

# **getUserSubUpdateList**
> UserSubscriptionUpdateList getUserSubUpdateList()

Get user subscription agent list

### Example

```typescript
import {
    UserApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new UserApi(configuration);

let username: string; // (default to undefined)
let offset: number; // (optional) (default to 0)
let limit: number; // (optional) (default to 10)

const { status, data } = await apiInstance.getUserSubUpdateList(
    username,
    offset,
    limit
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **offset** | [**number**] |  | (optional) defaults to 0|
| **limit** | [**number**] |  | (optional) defaults to 10|


### Return type

**UserSubscriptionUpdateList**

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

# **getUserUsage**
> UserUsageStatsList getUserUsage()

Get users usage

### Example

```typescript
import {
    UserApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new UserApi(configuration);

let username: string; // (default to undefined)
let period: Period; // (default to undefined)
let nodeId: number; // (optional) (default to undefined)
let groupByNode: boolean; // (optional) (default to false)
let start: string; // (optional) (default to undefined)
let end: string; // (optional) (default to undefined)

const { status, data } = await apiInstance.getUserUsage(
    username,
    period,
    nodeId,
    groupByNode,
    start,
    end
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **period** | **Period** |  | defaults to undefined|
| **nodeId** | [**number**] |  | (optional) defaults to undefined|
| **groupByNode** | [**boolean**] |  | (optional) defaults to false|
| **start** | [**string**] |  | (optional) defaults to undefined|
| **end** | [**string**] |  | (optional) defaults to undefined|


### Return type

**UserUsageStatsList**

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

# **getUsers**
> UsersResponse getUsers()

Get all users

### Example

```typescript
import {
    UserApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new UserApi(configuration);

let offset: number; // (optional) (default to undefined)
let limit: number; // (optional) (default to undefined)
let username: Array<string>; // (optional) (default to undefined)
let admin: Array<string>; // (optional) (default to undefined)
let group: Array<number>; // (optional) (default to undefined)
let search: string; // (optional) (default to undefined)
let status: UserStatus; // (optional) (default to undefined)
let sort: string; // (optional) (default to undefined)
let proxyId: string; // (optional) (default to undefined)
let loadSub: boolean; // (optional) (default to false)

const { status, data } = await apiInstance.getUsers(
    offset,
    limit,
    username,
    admin,
    group,
    search,
    status,
    sort,
    proxyId,
    loadSub
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **offset** | [**number**] |  | (optional) defaults to undefined|
| **limit** | [**number**] |  | (optional) defaults to undefined|
| **username** | **Array&lt;string&gt;** |  | (optional) defaults to undefined|
| **admin** | **Array&lt;string&gt;** |  | (optional) defaults to undefined|
| **group** | **Array&lt;number&gt;** |  | (optional) defaults to undefined|
| **search** | [**string**] |  | (optional) defaults to undefined|
| **status** | **UserStatus** |  | (optional) defaults to undefined|
| **sort** | [**string**] |  | (optional) defaults to undefined|
| **proxyId** | [**string**] |  | (optional) defaults to undefined|
| **loadSub** | [**boolean**] |  | (optional) defaults to false|


### Return type

**UsersResponse**

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
|**400** | BadRequest Error |  -  |
|**403** | Forbidden Error |  -  |
|**404** | NotFound Error |  -  |
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getUsersSubUpdateChart**
> UserSubscriptionUpdateChart getUsersSubUpdateChart()

Get subscription agent distribution percentages (optionally filtered by username)

### Example

```typescript
import {
    UserApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new UserApi(configuration);

let username: string; // (optional) (default to undefined)
let adminId: number; // (optional) (default to undefined)

const { status, data } = await apiInstance.getUsersSubUpdateChart(
    username,
    adminId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | (optional) defaults to undefined|
| **adminId** | [**number**] |  | (optional) defaults to undefined|


### Return type

**UserSubscriptionUpdateChart**

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

# **getUsersUsage**
> UserUsageStatsList getUsersUsage()

Get all users usage

### Example

```typescript
import {
    UserApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new UserApi(configuration);

let period: Period; // (default to undefined)
let nodeId: number; // (optional) (default to undefined)
let groupByNode: boolean; // (optional) (default to false)
let start: string; // (optional) (default to undefined)
let end: string; // (optional) (default to undefined)
let admin: Array<string>; // (optional) (default to undefined)

const { status, data } = await apiInstance.getUsersUsage(
    period,
    nodeId,
    groupByNode,
    start,
    end,
    admin
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **period** | **Period** |  | defaults to undefined|
| **nodeId** | [**number**] |  | (optional) defaults to undefined|
| **groupByNode** | [**boolean**] |  | (optional) defaults to false|
| **start** | [**string**] |  | (optional) defaults to undefined|
| **end** | [**string**] |  | (optional) defaults to undefined|
| **admin** | **Array&lt;string&gt;** |  | (optional) defaults to undefined|


### Return type

**UserUsageStatsList**

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
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **modifyUser**
> UserResponse modifyUser(userModify)

Modify an existing user  - **username**: Cannot be changed. Used to identify the user. - **status**: User\'s new status. Can be \'active\', \'disabled\', \'on_hold\', \'limited\', or \'expired\'. - **expire**: UTC datetime for new account expiration. Set to `0` for unlimited, `null` for no change. - **data_limit**: New max data usage in bytes (e.g., `1073741824` for 1GB). Set to `0` for unlimited, `null` for no change. - **data_limit_reset_strategy**: New strategy for data limit reset. Options include \'daily\', \'weekly\', \'monthly\', or \'no_reset\'. - **proxies**: Dictionary of new protocol settings (e.g., `vmess`, `vless`). Empty dictionary means no change. - **group_ids**: List of new group IDs to assign to the user. Empty list means no change. - **note**: New optional text for additional user information or notes. `null` means no change. - **on_hold_timeout**: New UTC timestamp for when `on_hold` status should start or end. Only applicable if status is changed to \'on_hold\'. - **on_hold_expire_duration**: New duration (in seconds) for how long the user should stay in `on_hold` status. Only applicable if status is changed to \'on_hold\'. - **next_plan**: Next user plan (resets after use).  Note: Fields set to `null` or omitted will not be modified.

### Example

```typescript
import {
    UserApi,
    Configuration,
    UserModify
} from './api';

const configuration = new Configuration();
const apiInstance = new UserApi(configuration);

let username: string; // (default to undefined)
let userModify: UserModify; //

const { status, data } = await apiInstance.modifyUser(
    username,
    userModify
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userModify** | **UserModify**|  | |
| **username** | [**string**] |  | defaults to undefined|


### Return type

**UserResponse**

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
|**400** | BadRequest Error |  -  |
|**403** | Forbidden Error |  -  |
|**404** | NotFound Error |  -  |
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **modifyUserWithTemplate**
> UserResponse modifyUserWithTemplate(modifyUserByTemplate)


### Example

```typescript
import {
    UserApi,
    Configuration,
    ModifyUserByTemplate
} from './api';

const configuration = new Configuration();
const apiInstance = new UserApi(configuration);

let username: string; // (default to undefined)
let modifyUserByTemplate: ModifyUserByTemplate; //

const { status, data } = await apiInstance.modifyUserWithTemplate(
    username,
    modifyUserByTemplate
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **modifyUserByTemplate** | **ModifyUserByTemplate**|  | |
| **username** | [**string**] |  | defaults to undefined|


### Return type

**UserResponse**

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
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **removeUser**
> removeUser()

Remove a user

### Example

```typescript
import {
    UserApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new UserApi(configuration);

let username: string; // (default to undefined)

const { status, data } = await apiInstance.removeUser(
    username
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|


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

# **resetUserDataUsage**
> UserResponse resetUserDataUsage()

Reset user data usage

### Example

```typescript
import {
    UserApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new UserApi(configuration);

let username: string; // (default to undefined)

const { status, data } = await apiInstance.resetUserDataUsage(
    username
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|


### Return type

**UserResponse**

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

# **resetUsersDataUsage**
> any resetUsersDataUsage()

Reset all users data usage

### Example

```typescript
import {
    UserApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new UserApi(configuration);

const { status, data } = await apiInstance.resetUsersDataUsage();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**any**

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **revokeUserSubscription**
> UserResponse revokeUserSubscription()

Revoke users subscription (Subscription link and proxies)

### Example

```typescript
import {
    UserApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new UserApi(configuration);

let username: string; // (default to undefined)

const { status, data } = await apiInstance.revokeUserSubscription(
    username
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|


### Return type

**UserResponse**

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

# **setOwner**
> UserResponse setOwner()

Set a new owner (admin) for a user.

### Example

```typescript
import {
    UserApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new UserApi(configuration);

let username: string; // (default to undefined)
let adminUsername: string; // (default to undefined)

const { status, data } = await apiInstance.setOwner(
    username,
    adminUsername
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **adminUsername** | [**string**] |  | defaults to undefined|


### Return type

**UserResponse**

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

