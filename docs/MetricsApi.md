# openapi_client.MetricsApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_website_metrics**](MetricsApi.md#get_website_metrics) | **GET** /orgs/{org_id}/websites/{website_id}/metrics | Get website metrics


# **get_website_metrics**
> WebsiteMetricsFullListing get_website_metrics(org_id, website_id, start=start, end=end, granularity=granularity)

Get website metrics

Returns website metrics between the optional start and end date. Defaults to last 24 hours. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.website_metrics_full_listing import WebsiteMetricsFullListing
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.MetricsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    start = '2013-10-20T19:20:30+01:00' # datetime | Start datetime UTC. (optional)
    end = '2013-10-20T19:20:30+01:00' # datetime | End datetime UTC. (optional)
    granularity = 'granularity_example' # str | Takes one of `hour`, `day`, defaults to `day` (optional)

    try:
        # Get website metrics
        api_response = api_instance.get_website_metrics(org_id, website_id, start=start, end=end, granularity=granularity)
        print("The response of MetricsApi->get_website_metrics:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MetricsApi->get_website_metrics: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **start** | **datetime**| Start datetime UTC. | [optional] 
 **end** | **datetime**| End datetime UTC. | [optional] 
 **granularity** | **str**| Takes one of &#x60;hour&#x60;, &#x60;day&#x60;, defaults to &#x60;day&#x60; | [optional] 

### Return type

[**WebsiteMetricsFullListing**](WebsiteMetricsFullListing.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**400** | Invalid input |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

