# {{classname}}

All URIs are relative to *https://api.machines.dev/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**MachinesCordon**](MachinesApi.md#MachinesCordon) | **Post** /apps/{app_name}/machines/{machine_id}/cordon | 
[**MachinesCreate**](MachinesApi.md#MachinesCreate) | **Post** /apps/{app_name}/machines | 
[**MachinesCreateLease**](MachinesApi.md#MachinesCreateLease) | **Post** /apps/{app_name}/machines/{machine_id}/lease | 
[**MachinesDelete**](MachinesApi.md#MachinesDelete) | **Delete** /apps/{app_name}/machines/{machine_id} | 
[**MachinesDeleteMetadata**](MachinesApi.md#MachinesDeleteMetadata) | **Delete** /apps/{app_name}/machines/{machine_id}/metadata/{key} | 
[**MachinesExec**](MachinesApi.md#MachinesExec) | **Post** /apps/{app_name}/machines/{machine_id}/exec | 
[**MachinesList**](MachinesApi.md#MachinesList) | **Get** /apps/{app_name}/machines | 
[**MachinesListEvents**](MachinesApi.md#MachinesListEvents) | **Get** /apps/{app_name}/machines/{machine_id}/events | 
[**MachinesListProcesses**](MachinesApi.md#MachinesListProcesses) | **Get** /apps/{app_name}/machines/{machine_id}/ps | 
[**MachinesListVersions**](MachinesApi.md#MachinesListVersions) | **Get** /apps/{app_name}/machines/{machine_id}/versions | 
[**MachinesReleaseLease**](MachinesApi.md#MachinesReleaseLease) | **Delete** /apps/{app_name}/machines/{machine_id}/lease | 
[**MachinesRestart**](MachinesApi.md#MachinesRestart) | **Post** /apps/{app_name}/machines/{machine_id}/restart | 
[**MachinesShow**](MachinesApi.md#MachinesShow) | **Get** /apps/{app_name}/machines/{machine_id} | 
[**MachinesShowLease**](MachinesApi.md#MachinesShowLease) | **Get** /apps/{app_name}/machines/{machine_id}/lease | 
[**MachinesShowMetadata**](MachinesApi.md#MachinesShowMetadata) | **Get** /apps/{app_name}/machines/{machine_id}/metadata | 
[**MachinesSignal**](MachinesApi.md#MachinesSignal) | **Post** /apps/{app_name}/machines/{machine_id}/signal | 
[**MachinesStart**](MachinesApi.md#MachinesStart) | **Post** /apps/{app_name}/machines/{machine_id}/start | 
[**MachinesStop**](MachinesApi.md#MachinesStop) | **Post** /apps/{app_name}/machines/{machine_id}/stop | 
[**MachinesUncordon**](MachinesApi.md#MachinesUncordon) | **Post** /apps/{app_name}/machines/{machine_id}/uncordon | 
[**MachinesUpdate**](MachinesApi.md#MachinesUpdate) | **Post** /apps/{app_name}/machines/{machine_id} | 
[**MachinesUpdateMetadata**](MachinesApi.md#MachinesUpdateMetadata) | **Post** /apps/{app_name}/machines/{machine_id}/metadata/{key} | 
[**MachinesWait**](MachinesApi.md#MachinesWait) | **Get** /apps/{app_name}/machines/{machine_id}/wait | 

# **MachinesCordon**
> MachinesCordon(ctx, appName, machineId)


“Cordoning” a machine refers to disabling its services, so the proxy won’t route requests to it. In flyctl this is used by blue/green deployments; one set of machines is started up with services disabled, and when they are all healthy, the services are enabled on the new machines and disabled on the old ones.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **appName** | **string**| Fly App Name | 
  **machineId** | **string**| Machine ID | 

### Return type

 (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **MachinesCreate**
> Machine MachinesCreate(ctx, body, appName)


### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **body** | [**CreateMachineRequest**](CreateMachineRequest.md)| Create machine request | 
  **appName** | **string**| Fly App Name | 

### Return type

[**Machine**](Machine.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **MachinesCreateLease**
> Lease MachinesCreateLease(ctx, body, appName, machineId)


### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **body** | [**CreateLeaseRequest**](CreateLeaseRequest.md)| Request body | 
  **appName** | **string**| Fly App Name | 
  **machineId** | **string**| Machine ID | 

### Return type

[**Lease**](Lease.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **MachinesDelete**
> MachinesDelete(ctx, appName, machineId)


### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **appName** | **string**| Fly App Name | 
  **machineId** | **string**| Machine ID | 

### Return type

 (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **MachinesDeleteMetadata**
> MachinesDeleteMetadata(ctx, appName, machineId, key)


### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **appName** | **string**| Fly App Name | 
  **machineId** | **string**| Machine ID | 
  **key** | **string**| Metadata Key | 

### Return type

 (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **MachinesExec**
> string MachinesExec(ctx, body, appName, machineId)


### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **body** | [**MachineExecRequest**](MachineExecRequest.md)| Request body | 
  **appName** | **string**| Fly App Name | 
  **machineId** | **string**| Machine ID | 

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/octet-stream, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **MachinesList**
> []Machine MachinesList(ctx, appName, optional)


### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **appName** | **string**| Fly App Name | 
 **optional** | ***MachinesApiMachinesListOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a MachinesApiMachinesListOpts struct
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **includeDeleted** | **optional.Bool**| Include deleted machines | 
 **region** | **optional.String**| Region filter | 

### Return type

[**[]Machine**](Machine.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **MachinesListEvents**
> []MachineEvent MachinesListEvents(ctx, appName, machineId)


### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **appName** | **string**| Fly App Name | 
  **machineId** | **string**| Machine ID | 

### Return type

[**[]MachineEvent**](MachineEvent.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **MachinesListProcesses**
> []ProcessStat MachinesListProcesses(ctx, appName, machineId, optional)


### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **appName** | **string**| Fly App Name | 
  **machineId** | **string**| Machine ID | 
 **optional** | ***MachinesApiMachinesListProcessesOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a MachinesApiMachinesListProcessesOpts struct
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **sortBy** | **optional.String**| Sort by | 
 **order** | **optional.String**| Order | 

### Return type

[**[]ProcessStat**](ProcessStat.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **MachinesListVersions**
> []MachineVersion MachinesListVersions(ctx, appName, machineId)


### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **appName** | **string**| Fly App Name | 
  **machineId** | **string**| Machine ID | 

### Return type

[**[]MachineVersion**](MachineVersion.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **MachinesReleaseLease**
> MachinesReleaseLease(ctx, appName, machineId)


### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **appName** | **string**| Fly App Name | 
  **machineId** | **string**| Machine ID | 

### Return type

 (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **MachinesRestart**
> MachinesRestart(ctx, appName, machineId, optional)


### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **appName** | **string**| Fly App Name | 
  **machineId** | **string**| Machine ID | 
 **optional** | ***MachinesApiMachinesRestartOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a MachinesApiMachinesRestartOpts struct
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **timeout** | **optional.String**| Restart timeout as a Go duration string or number of seconds | 

### Return type

 (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **MachinesShow**
> Machine MachinesShow(ctx, appName, machineId)


### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **appName** | **string**| Fly App Name | 
  **machineId** | **string**| Machine ID | 

### Return type

[**Machine**](Machine.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **MachinesShowLease**
> Lease MachinesShowLease(ctx, appName, machineId)


### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **appName** | **string**| Fly App Name | 
  **machineId** | **string**| Machine ID | 

### Return type

[**Lease**](Lease.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **MachinesShowMetadata**
> map[string]string MachinesShowMetadata(ctx, appName, machineId)


### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **appName** | **string**| Fly App Name | 
  **machineId** | **string**| Machine ID | 

### Return type

**map[string]string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **MachinesSignal**
> MachinesSignal(ctx, body, appName, machineId)


### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **body** | [**SignalRequest**](SignalRequest.md)| Request body | 
  **appName** | **string**| Fly App Name | 
  **machineId** | **string**| Machine ID | 

### Return type

 (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **MachinesStart**
> MachinesStart(ctx, appName, machineId)


### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **appName** | **string**| Fly App Name | 
  **machineId** | **string**| Machine ID | 

### Return type

 (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **MachinesStop**
> MachinesStop(ctx, appName, machineId, optional)


### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **appName** | **string**| Fly App Name | 
  **machineId** | **string**| Machine ID | 
 **optional** | ***MachinesApiMachinesStopOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a MachinesApiMachinesStopOpts struct
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **body** | [**optional.Interface of StopRequest**](StopRequest.md)| Optional request body | 

### Return type

 (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **MachinesUncordon**
> MachinesUncordon(ctx, appName, machineId)


“Cordoning” a machine refers to disabling its services, so the proxy won’t route requests to it. In flyctl this is used by blue/green deployments; one set of machines is started up with services disabled, and when they are all healthy, the services are enabled on the new machines and disabled on the old ones.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **appName** | **string**| Fly App Name | 
  **machineId** | **string**| Machine ID | 

### Return type

 (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **MachinesUpdate**
> Machine MachinesUpdate(ctx, body, appName, machineId)


### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **body** | [**UpdateMachineRequest**](UpdateMachineRequest.md)| Request body | 
  **appName** | **string**| Fly App Name | 
  **machineId** | **string**| Machine ID | 

### Return type

[**Machine**](Machine.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **MachinesUpdateMetadata**
> MachinesUpdateMetadata(ctx, appName, machineId, key)


### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **appName** | **string**| Fly App Name | 
  **machineId** | **string**| Machine ID | 
  **key** | **string**| Metadata Key | 

### Return type

 (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **MachinesWait**
> MachinesWait(ctx, appName, machineId, optional)


### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **appName** | **string**| Fly App Name | 
  **machineId** | **string**| Machine ID | 
 **optional** | ***MachinesApiMachinesWaitOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a MachinesApiMachinesWaitOpts struct
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **instanceId** | **optional.String**| instance? version? TODO | 
 **timeout** | **optional.Int32**| wait timeout. default 60s | 
 **state** | **optional.String**| desired state | 

### Return type

 (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

