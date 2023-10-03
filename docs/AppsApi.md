# {{classname}}

All URIs are relative to *https://api.machines.dev/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**AppsCreate**](AppsApi.md#AppsCreate) | **Post** /apps | 
[**AppsDelete**](AppsApi.md#AppsDelete) | **Delete** /apps/{app_name} | 
[**AppsList**](AppsApi.md#AppsList) | **Get** /apps | 
[**AppsShow**](AppsApi.md#AppsShow) | **Get** /apps/{app_name} | 

# **AppsCreate**
> AppsCreate(ctx, body)


### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **body** | [**CreateAppRequest**](CreateAppRequest.md)| App body | 

### Return type

 (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **AppsDelete**
> AppsDelete(ctx, appName)


### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **appName** | **string**| Fly App Name | 

### Return type

 (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **AppsList**
> ListAppsResponse AppsList(ctx, optional)


### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***AppsApiAppsListOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a AppsApiAppsListOpts struct
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orgSlug** | **optional.String**| The org slug, or &#x27;personal&#x27;, to filter apps | 

### Return type

[**ListAppsResponse**](ListAppsResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **AppsShow**
> App AppsShow(ctx, appName)


### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **appName** | **string**| Fly App Name | 

### Return type

[**App**](App.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

