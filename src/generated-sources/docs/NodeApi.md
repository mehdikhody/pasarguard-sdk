# NodeApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**clearUsageData**](#clearusagedata) | **DELETE** /api/nodes/clear_usage_data/{table} | Clear usage data from a specified table|
|[**createNode**](#createnode) | **POST** /api/node | Create Node|
|[**getNode**](#getnode) | **GET** /api/node/{node_id} | Get Node|
|[**getNodeSettings**](#getnodesettings) | **GET** /api/node/settings | Get Node Settings|
|[**getNodeStatsPeriodic**](#getnodestatsperiodic) | **GET** /api/node/{node_id}/stats | Get Node Stats Periodic|
|[**getNodes**](#getnodes) | **GET** /api/nodes | Get Nodes|
|[**getUsage**](#getusage) | **GET** /api/node/usage | Get Usage|
|[**modifyNode**](#modifynode) | **PUT** /api/node/{node_id} | Modify Node|
|[**nodeLogs**](#nodelogs) | **GET** /api/node/{node_id}/logs | Node Logs|
|[**realtimeNodeStats**](#realtimenodestats) | **GET** /api/node/{node_id}/realtime_stats | Realtime Node Stats|
|[**realtimeNodesStats**](#realtimenodesstats) | **GET** /api/nodes/realtime_stats | Realtime Nodes Stats|
|[**reconnectAllNode**](#reconnectallnode) | **POST** /api/nodes/reconnect | Reconnect All Node|
|[**reconnectNode**](#reconnectnode) | **POST** /api/node/{node_id}/reconnect | Reconnect Node|
|[**removeNode**](#removenode) | **DELETE** /api/node/{node_id} | Remove Node|
|[**resetNodeUsage**](#resetnodeusage) | **POST** /api/node/{node_id}/reset | Reset Node Usage|
|[**syncNode**](#syncnode) | **PUT** /api/node/{node_id}/sync | Sync Node|
|[**updateCore**](#updatecore) | **POST** /api/node/{node_id}/core_update | Update Core|
|[**updateGeofiles**](#updategeofiles) | **POST** /api/node/{node_id}/geofiles | Update Geofiles|
|[**updateNode**](#updatenode) | **POST** /api/node/{node_id}/update | Update Node|
|[**userOnlineIpList**](#useronlineiplist) | **GET** /api/node/{node_id}/online_stats/{username}/ip | User Online Ip List|
|[**userOnlineIpListAllNodes**](#useronlineiplistallnodes) | **GET** /api/node/online_stats/{username}/ip | User Online Ip List All Nodes|
|[**userOnlineStats**](#useronlinestats) | **GET** /api/node/{node_id}/online_stats/{username} | User Online Stats|

# **clearUsageData**
> any clearUsageData()

Deletes **all rows** from the selected usage data table. Use with caution.  Allowed tables:     - `node_user_usages`: Deletes user-specific node usage traffic records.     - `node_usages`: Deletes node-level aggregated traffic (uplink/downlink) records.  **Optional filters:**     - `start`: ISO 8601 timestamp to filter from (inclusive)     - `end`: ISO 8601 timestamp to filter to (exclusive)  ⚠️ This operation is irreversible. Ensure correct usage in production environments.

### Example

```typescript
import {
    NodeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new NodeApi(configuration);

let table: UsageTable; // (default to undefined)
let start: string; // (optional) (default to undefined)
let end: string; // (optional) (default to undefined)

const { status, data } = await apiInstance.clearUsageData(
    table,
    start,
    end
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **table** | **UsageTable** |  | defaults to undefined|
| **start** | [**string**] |  | (optional) defaults to undefined|
| **end** | [**string**] |  | (optional) defaults to undefined|


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
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createNode**
> NodeResponse createNode(nodeCreate)

Create a new node to the database.

### Example

```typescript
import {
    NodeApi,
    Configuration,
    NodeCreate
} from './api';

const configuration = new Configuration();
const apiInstance = new NodeApi(configuration);

let nodeCreate: NodeCreate; //

const { status, data } = await apiInstance.createNode(
    nodeCreate
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **nodeCreate** | **NodeCreate**|  | |


### Return type

**NodeResponse**

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
|**409** | Conflict Error |  -  |
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getNode**
> NodeResponse getNode()

Retrieve details of a specific node by its ID.

### Example

```typescript
import {
    NodeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new NodeApi(configuration);

let nodeId: number; // (default to undefined)

const { status, data } = await apiInstance.getNode(
    nodeId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **nodeId** | [**number**] |  | defaults to undefined|


### Return type

**NodeResponse**

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

# **getNodeSettings**
> NodeSettings getNodeSettings()

Retrieve the current node settings.

### Example

```typescript
import {
    NodeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new NodeApi(configuration);

const { status, data } = await apiInstance.getNodeSettings();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**NodeSettings**

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getNodeStatsPeriodic**
> NodeStatsList getNodeStatsPeriodic()


### Example

```typescript
import {
    NodeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new NodeApi(configuration);

let nodeId: number; // (default to undefined)
let start: string; // (optional) (default to undefined)
let end: string; // (optional) (default to undefined)
let period: Period; // (optional) (default to undefined)

const { status, data } = await apiInstance.getNodeStatsPeriodic(
    nodeId,
    start,
    end,
    period
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **nodeId** | [**number**] |  | defaults to undefined|
| **start** | [**string**] |  | (optional) defaults to undefined|
| **end** | [**string**] |  | (optional) defaults to undefined|
| **period** | **Period** |  | (optional) defaults to undefined|


### Return type

**NodeStatsList**

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

# **getNodes**
> NodesResponse getNodes()

Retrieve a list of all nodes. Accessible only to sudo admins.

### Example

```typescript
import {
    NodeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new NodeApi(configuration);

let coreId: number; // (optional) (default to undefined)
let offset: number; // (optional) (default to undefined)
let limit: number; // (optional) (default to undefined)
let status: Array<NodeStatus>; // (optional) (default to undefined)
let enabled: boolean; // (optional) (default to false)
let ids: Array<number>; // (optional) (default to undefined)
let search: string; // (optional) (default to undefined)

const { status, data } = await apiInstance.getNodes(
    coreId,
    offset,
    limit,
    status,
    enabled,
    ids,
    search
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **coreId** | [**number**] |  | (optional) defaults to undefined|
| **offset** | [**number**] |  | (optional) defaults to undefined|
| **limit** | [**number**] |  | (optional) defaults to undefined|
| **status** | **Array&lt;NodeStatus&gt;** |  | (optional) defaults to undefined|
| **enabled** | [**boolean**] |  | (optional) defaults to false|
| **ids** | **Array&lt;number&gt;** |  | (optional) defaults to undefined|
| **search** | [**string**] |  | (optional) defaults to undefined|


### Return type

**NodesResponse**

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

# **getUsage**
> NodeUsageStatsList getUsage()

Retrieve usage statistics for nodes within a specified date range.

### Example

```typescript
import {
    NodeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new NodeApi(configuration);

let start: string; // (optional) (default to undefined)
let end: string; // (optional) (default to undefined)
let period: Period; // (optional) (default to undefined)
let nodeId: number; // (optional) (default to undefined)
let groupByNode: boolean; // (optional) (default to false)

const { status, data } = await apiInstance.getUsage(
    start,
    end,
    period,
    nodeId,
    groupByNode
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **start** | [**string**] |  | (optional) defaults to undefined|
| **end** | [**string**] |  | (optional) defaults to undefined|
| **period** | **Period** |  | (optional) defaults to undefined|
| **nodeId** | [**number**] |  | (optional) defaults to undefined|
| **groupByNode** | [**boolean**] |  | (optional) defaults to false|


### Return type

**NodeUsageStatsList**

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

# **modifyNode**
> NodeResponse modifyNode(nodeModify)

Modify a node\'s details. Only accessible to sudo admins.

### Example

```typescript
import {
    NodeApi,
    Configuration,
    NodeModify
} from './api';

const configuration = new Configuration();
const apiInstance = new NodeApi(configuration);

let nodeId: number; // (default to undefined)
let nodeModify: NodeModify; //

const { status, data } = await apiInstance.modifyNode(
    nodeId,
    nodeModify
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **nodeModify** | **NodeModify**|  | |
| **nodeId** | [**number**] |  | defaults to undefined|


### Return type

**NodeResponse**

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

# **nodeLogs**
> any nodeLogs()

Stream logs for a specific node as Server-Sent Events.

### Example

```typescript
import {
    NodeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new NodeApi(configuration);

let nodeId: number; // (default to undefined)

const { status, data } = await apiInstance.nodeLogs(
    nodeId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **nodeId** | [**number**] |  | defaults to undefined|


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
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **realtimeNodeStats**
> NodeRealtimeStats realtimeNodeStats()

Retrieve node real-time statistics.

### Example

```typescript
import {
    NodeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new NodeApi(configuration);

let nodeId: number; // (default to undefined)

const { status, data } = await apiInstance.realtimeNodeStats(
    nodeId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **nodeId** | [**number**] |  | defaults to undefined|


### Return type

**NodeRealtimeStats**

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

# **realtimeNodesStats**
> { [key: string]: ResponseRealtimeNodesStatsApiNodesRealtimeStatsGetValue; } realtimeNodesStats()

Retrieve nodes real-time statistics.

### Example

```typescript
import {
    NodeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new NodeApi(configuration);

const { status, data } = await apiInstance.realtimeNodesStats();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**{ [key: string]: ResponseRealtimeNodesStatsApiNodesRealtimeStatsGetValue; }**

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **reconnectAllNode**
> any reconnectAllNode()

Trigger reconnection for all nodes or a specific core.

### Example

```typescript
import {
    NodeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new NodeApi(configuration);

let coreId: number; // (optional) (default to undefined)

const { status, data } = await apiInstance.reconnectAllNode(
    coreId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **coreId** | [**number**] |  | (optional) defaults to undefined|


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
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **reconnectNode**
> any reconnectNode()

Trigger a reconnection for the specified node. Only accessible to sudo admins.

### Example

```typescript
import {
    NodeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new NodeApi(configuration);

let nodeId: number; // (default to undefined)

const { status, data } = await apiInstance.reconnectNode(
    nodeId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **nodeId** | [**number**] |  | defaults to undefined|


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
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **removeNode**
> removeNode()

Remove a node and remove it from xray in the background.

### Example

```typescript
import {
    NodeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new NodeApi(configuration);

let nodeId: number; // (default to undefined)

const { status, data } = await apiInstance.removeNode(
    nodeId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **nodeId** | [**number**] |  | defaults to undefined|


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

# **resetNodeUsage**
> NodeResponse resetNodeUsage()

Reset node traffic usage (uplink and downlink). Creates a log entry in node_usage_reset_logs table. Only accessible to sudo admins.

### Example

```typescript
import {
    NodeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new NodeApi(configuration);

let nodeId: number; // (default to undefined)

const { status, data } = await apiInstance.resetNodeUsage(
    nodeId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **nodeId** | [**number**] |  | defaults to undefined|


### Return type

**NodeResponse**

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

# **syncNode**
> any syncNode()


### Example

```typescript
import {
    NodeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new NodeApi(configuration);

let nodeId: number; // (default to undefined)
let flushUsers: boolean; // (optional) (default to false)

const { status, data } = await apiInstance.syncNode(
    nodeId,
    flushUsers
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **nodeId** | [**number**] |  | defaults to undefined|
| **flushUsers** | [**boolean**] |  | (optional) defaults to false|


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
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateCore**
> any updateCore(nodeCoreUpdate)


### Example

```typescript
import {
    NodeApi,
    Configuration,
    NodeCoreUpdate
} from './api';

const configuration = new Configuration();
const apiInstance = new NodeApi(configuration);

let nodeId: number; // (default to undefined)
let nodeCoreUpdate: NodeCoreUpdate; //

const { status, data } = await apiInstance.updateCore(
    nodeId,
    nodeCoreUpdate
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **nodeCoreUpdate** | **NodeCoreUpdate**|  | |
| **nodeId** | [**number**] |  | defaults to undefined|


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
|**200** | Successful Response |  -  |
|**401** | Unauthorized Error |  * WWW-Authenticate - Authentication type <br>  |
|**403** | Forbidden Error |  -  |
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateGeofiles**
> any updateGeofiles(nodeGeoFilesUpdate)


### Example

```typescript
import {
    NodeApi,
    Configuration,
    NodeGeoFilesUpdate
} from './api';

const configuration = new Configuration();
const apiInstance = new NodeApi(configuration);

let nodeId: number; // (default to undefined)
let nodeGeoFilesUpdate: NodeGeoFilesUpdate; //

const { status, data } = await apiInstance.updateGeofiles(
    nodeId,
    nodeGeoFilesUpdate
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **nodeGeoFilesUpdate** | **NodeGeoFilesUpdate**|  | |
| **nodeId** | [**number**] |  | defaults to undefined|


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
|**200** | Successful Response |  -  |
|**401** | Unauthorized Error |  * WWW-Authenticate - Authentication type <br>  |
|**403** | Forbidden Error |  -  |
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateNode**
> any updateNode()


### Example

```typescript
import {
    NodeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new NodeApi(configuration);

let nodeId: number; // (default to undefined)

const { status, data } = await apiInstance.updateNode(
    nodeId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **nodeId** | [**number**] |  | defaults to undefined|


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
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **userOnlineIpList**
> UserIPList userOnlineIpList()

Retrieve user ips by node.

### Example

```typescript
import {
    NodeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new NodeApi(configuration);

let nodeId: number; // (default to undefined)
let username: string; // (default to undefined)

const { status, data } = await apiInstance.userOnlineIpList(
    nodeId,
    username
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **nodeId** | [**number**] |  | defaults to undefined|
| **username** | [**string**] |  | defaults to undefined|


### Return type

**UserIPList**

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

# **userOnlineIpListAllNodes**
> UserIPListAll userOnlineIpListAllNodes()

Retrieve user ips from all nodes.

### Example

```typescript
import {
    NodeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new NodeApi(configuration);

let username: string; // (default to undefined)

const { status, data } = await apiInstance.userOnlineIpListAllNodes(
    username
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|


### Return type

**UserIPListAll**

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

# **userOnlineStats**
> { [key: string]: number | null; } userOnlineStats()

Retrieve user online stats by node.

### Example

```typescript
import {
    NodeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new NodeApi(configuration);

let nodeId: number; // (default to undefined)
let username: string; // (default to undefined)

const { status, data } = await apiInstance.userOnlineStats(
    nodeId,
    username
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **nodeId** | [**number**] |  | defaults to undefined|
| **username** | [**string**] |  | defaults to undefined|


### Return type

**{ [key: string]: number | null; }**

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

