# {{classname}}

All URIs are relative to *https://api.machines.dev/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**VolumeDelete**](VolumesApi.md#VolumeDelete) | **Delete** /apps/{app_name}/volumes/{volume_id} | 
[**VolumesCreate**](VolumesApi.md#VolumesCreate) | **Post** /apps/{app_name}/volumes | 
[**VolumesExtend**](VolumesApi.md#VolumesExtend) | **Put** /apps/{app_name}/volumes/{volume_id}/extend | 
[**VolumesGetById**](VolumesApi.md#VolumesGetById) | **Get** /apps/{app_name}/volumes/{volume_id} | 
[**VolumesGetSnapshots**](VolumesApi.md#VolumesGetSnapshots) | **Get** /apps/{app_name}/volumes/{volume_id}/snapshots | 
[**VolumesList**](VolumesApi.md#VolumesList) | **Get** /apps/{app_name}/volumes | 

# **VolumeDelete**
> Volume VolumeDelete(ctx, appName, volumeId)


### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **appName** | **string**| Fly App Name | 
  **volumeId** | **string**| Volume ID | 

### Return type

[**Volume**](Volume.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **VolumesCreate**
> Volume VolumesCreate(ctx, body, appName)


### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **body** | [**CreateVolumeRequest**](CreateVolumeRequest.md)| Request body | 
  **appName** | **string**| Fly App Name | 

### Return type

[**Volume**](Volume.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **VolumesExtend**
> ExtendVolumeResponse VolumesExtend(ctx, body, appName, volumeId)


### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **body** | [**ExtendVolumeRequest**](ExtendVolumeRequest.md)| Request body | 
  **appName** | **string**| Fly App Name | 
  **volumeId** | **string**| Volume ID | 

### Return type

[**ExtendVolumeResponse**](ExtendVolumeResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **VolumesGetById**
> Volume VolumesGetById(ctx, appName, volumeId)


### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **appName** | **string**| Fly App Name | 
  **volumeId** | **string**| Volume ID | 

### Return type

[**Volume**](Volume.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **VolumesGetSnapshots**
> []VolumeSnapshot VolumesGetSnapshots(ctx, appName, volumeId)


### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **appName** | **string**| Fly App Name | 
  **volumeId** | **string**| Volume ID | 

### Return type

[**[]VolumeSnapshot**](VolumeSnapshot.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **VolumesList**
> []Volume VolumesList(ctx, appName)


### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **appName** | **string**| Fly App Name | 

### Return type

[**[]Volume**](Volume.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

