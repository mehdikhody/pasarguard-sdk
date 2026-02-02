# NotificationEnable


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**admin** | [**AdminNotificationEnable**](AdminNotificationEnable.md) |  | [optional] [default to undefined]
**core** | [**BaseNotificationEnable**](BaseNotificationEnable.md) |  | [optional] [default to undefined]
**group** | [**BaseNotificationEnable**](BaseNotificationEnable.md) |  | [optional] [default to undefined]
**host** | [**HostNotificationEnable**](HostNotificationEnable.md) |  | [optional] [default to undefined]
**node** | [**NodeNotificationEnable**](NodeNotificationEnable.md) |  | [optional] [default to undefined]
**user** | [**UserNotificationEnable**](UserNotificationEnable.md) |  | [optional] [default to undefined]
**user_template** | [**BaseNotificationEnable**](BaseNotificationEnable.md) |  | [optional] [default to undefined]
**days_left** | **boolean** |  | [optional] [default to true]
**percentage_reached** | **boolean** |  | [optional] [default to true]

## Example

```typescript
import { NotificationEnable } from './api';

const instance: NotificationEnable = {
    admin,
    core,
    group,
    host,
    node,
    user,
    user_template,
    days_left,
    percentage_reached,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
