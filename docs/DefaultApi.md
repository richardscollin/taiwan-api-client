# openapi_client.DefaultApi

All URIs are relative to *http://data.gcis.nat.gov.tw/od/data/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_business_info**](DefaultApi.md#get_business_info) | **GET** /426D5542-5F05-43EB-83F9-F1300F14E1F1 | 商業登記基本資料-應用三


# **get_business_info**
> list[InlineResponse200] get_business_info(format, filter, skip=skip, top=top)

商業登記基本資料-應用三

### Example

```python
from __future__ import print_function
import time
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to http://data.gcis.nat.gov.tw/od/data/api
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://data.gcis.nat.gov.tw/od/data/api"
)


# Enter a context with an instance of the API client
with openapi_client.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DefaultApi(api_client)
    format = 'format_example' # str | 指定來源格式
filter = 'filter_example' # str | 過濾<br>公式:President_No eq [0-9]{8}<br>說明:President_No :商業登記之下的商業統一編號。
skip = 'skip_example' # str | 從第n筆開始條列。請填入阿拉伯數字，預設為0，下限為0，上限為500000。 (optional)
top = 'top_example' # str | 每次可撈取筆數。請填入阿拉伯數字，預設為50，下限為1，上限為1000。 (optional)

    try:
        # 商業登記基本資料-應用三
        api_response = api_instance.get_business_info(format, filter, skip=skip, top=top)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling DefaultApi->get_business_info: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **format** | **str**| 指定來源格式 | 
 **filter** | **str**| 過濾&lt;br&gt;公式:President_No eq [0-9]{8}&lt;br&gt;說明:President_No :商業登記之下的商業統一編號。 | 
 **skip** | **str**| 從第n筆開始條列。請填入阿拉伯數字，預設為0，下限為0，上限為500000。 | [optional] 
 **top** | **str**| 每次可撈取筆數。請填入阿拉伯數字，預設為50，下限為1，上限為1000。 | [optional] 

### Return type

[**list[InlineResponse200]**](InlineResponse200.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | 資料來源:商業公示資料 |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

