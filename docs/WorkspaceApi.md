# quetzal.openapi_client.WorkspaceApi

All URIs are relative to *https://api.quetz.al/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**public_query_details**](WorkspaceApi.md#public_query_details) | **GET** /data/queries/{qid} | Query details.
[**workspace_commit**](WorkspaceApi.md#workspace_commit) | **PUT** /data/workspaces/{wid}/commit | Commit workspace.
[**workspace_details**](WorkspaceApi.md#workspace_details) | **GET** /data/workspaces/{wid} | Workspace details.
[**workspace_fetch**](WorkspaceApi.md#workspace_fetch) | **GET** /data/workspaces/ | List workspaces.
[**workspace_file_create**](WorkspaceApi.md#workspace_file_create) | **POST** /data/workspaces/{wid}/files/ | Upload file.
[**workspace_file_delete**](WorkspaceApi.md#workspace_file_delete) | **DELETE** /data/workspaces/{wid}/files/{uuid} | Delete a file.
[**workspace_file_details**](WorkspaceApi.md#workspace_file_details) | **GET** /data/workspaces/{wid}/files/{uuid} | Fetch file.
[**workspace_file_fetch**](WorkspaceApi.md#workspace_file_fetch) | **GET** /data/workspaces/{wid}/files/ | List files.
[**workspace_file_set_metadata**](WorkspaceApi.md#workspace_file_set_metadata) | **PUT** /data/workspaces/{wid}/files/{uuid} | Rewrite metadata.
[**workspace_file_update_metadata**](WorkspaceApi.md#workspace_file_update_metadata) | **PATCH** /data/workspaces/{wid}/files/{uuid} | Modify metadata.
[**workspace_query_create**](WorkspaceApi.md#workspace_query_create) | **POST** /data/workspaces/{wid}/queries/ | Prepare a query.
[**workspace_query_details**](WorkspaceApi.md#workspace_query_details) | **GET** /data/workspaces/{wid}/queries/{qid} | Query details.
[**workspace_query_fetch**](WorkspaceApi.md#workspace_query_fetch) | **GET** /data/workspaces/{wid}/queries/ | List queries.
[**workspace_scan**](WorkspaceApi.md#workspace_scan) | **PUT** /data/workspaces/{wid}/scan | Update views.


# **public_query_details**
> Query public_query_details(qid, page=page, per_page=per_page)

Query details.

The details of a query, which contains the query itself and a paginated list of its results.

### Example

* Api Key Authentication (apiKey):
```python
from __future__ import print_function
import time
import quetzal.openapi_client
from quetzal.openapi_client.rest import ApiException
from pprint import pprint
configuration = quetzal.openapi_client.Configuration()
# Configure API key authorization: apiKey
configuration.api_key['X-API-KEY'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-API-KEY'] = 'Bearer'
configuration = quetzal.openapi_client.Configuration()
# Configure Bearer authorization: bearer
configuration.access_token = 'YOUR_BEARER_TOKEN'

# create an instance of the API class
api_instance = quetzal.openapi_client.WorkspaceApi(quetzal.openapi_client.ApiClient(configuration))
qid = 56 # int | Query identifier
page = 1 # int | The page of a collection to return. (optional) (default to 1)
per_page = 100 # int | Number of items to return per page. (optional) (default to 100)

try:
    # Query details.
    api_response = api_instance.public_query_details(qid, page=page, per_page=per_page)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WorkspaceApi->public_query_details: %s\n" % e)
```

* Bearer Authentication (bearer):
```python
from __future__ import print_function
import time
import quetzal.openapi_client
from quetzal.openapi_client.rest import ApiException
from pprint import pprint
configuration = quetzal.openapi_client.Configuration()
# Configure API key authorization: apiKey
configuration.api_key['X-API-KEY'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-API-KEY'] = 'Bearer'
configuration = quetzal.openapi_client.Configuration()
# Configure Bearer authorization: bearer
configuration.access_token = 'YOUR_BEARER_TOKEN'

# create an instance of the API class
api_instance = quetzal.openapi_client.WorkspaceApi(quetzal.openapi_client.ApiClient(configuration))
qid = 56 # int | Query identifier
page = 1 # int | The page of a collection to return. (optional) (default to 1)
per_page = 100 # int | Number of items to return per page. (optional) (default to 100)

try:
    # Query details.
    api_response = api_instance.public_query_details(qid, page=page, per_page=per_page)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WorkspaceApi->public_query_details: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **qid** | **int**| Query identifier | 
 **page** | **int**| The page of a collection to return. | [optional] [default to 1]
 **per_page** | **int**| Number of items to return per page. | [optional] [default to 100]

### Return type

[**Query**](Query.md)

### Authorization

[apiKey](../README.md#apiKey), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_commit**
> Workspace workspace_commit(wid)

Commit workspace.

Requests a workspace commit. That is, all metadata added or modified in this workspace will be moved to the global, public workspace, becoming available to all users. Metadata versions will be incremented.

### Example

* Api Key Authentication (apiKey):
```python
from __future__ import print_function
import time
import quetzal.openapi_client
from quetzal.openapi_client.rest import ApiException
from pprint import pprint
configuration = quetzal.openapi_client.Configuration()
# Configure API key authorization: apiKey
configuration.api_key['X-API-KEY'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-API-KEY'] = 'Bearer'
configuration = quetzal.openapi_client.Configuration()
# Configure Bearer authorization: bearer
configuration.access_token = 'YOUR_BEARER_TOKEN'

# create an instance of the API class
api_instance = quetzal.openapi_client.WorkspaceApi(quetzal.openapi_client.ApiClient(configuration))
wid = 56 # int | Workspace identifier.

try:
    # Commit workspace.
    api_response = api_instance.workspace_commit(wid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WorkspaceApi->workspace_commit: %s\n" % e)
```

* Bearer Authentication (bearer):
```python
from __future__ import print_function
import time
import quetzal.openapi_client
from quetzal.openapi_client.rest import ApiException
from pprint import pprint
configuration = quetzal.openapi_client.Configuration()
# Configure API key authorization: apiKey
configuration.api_key['X-API-KEY'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-API-KEY'] = 'Bearer'
configuration = quetzal.openapi_client.Configuration()
# Configure Bearer authorization: bearer
configuration.access_token = 'YOUR_BEARER_TOKEN'

# create an instance of the API class
api_instance = quetzal.openapi_client.WorkspaceApi(quetzal.openapi_client.ApiClient(configuration))
wid = 56 # int | Workspace identifier.

try:
    # Commit workspace.
    api_response = api_instance.workspace_commit(wid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WorkspaceApi->workspace_commit: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **wid** | **int**| Workspace identifier. | 

### Return type

[**Workspace**](Workspace.md)

### Authorization

[apiKey](../README.md#apiKey), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_details**
> Workspace workspace_details(wid)

Workspace details.

Obtain all information of a workspace.

### Example

* Api Key Authentication (apiKey):
```python
from __future__ import print_function
import time
import quetzal.openapi_client
from quetzal.openapi_client.rest import ApiException
from pprint import pprint
configuration = quetzal.openapi_client.Configuration()
# Configure API key authorization: apiKey
configuration.api_key['X-API-KEY'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-API-KEY'] = 'Bearer'
configuration = quetzal.openapi_client.Configuration()
# Configure Bearer authorization: bearer
configuration.access_token = 'YOUR_BEARER_TOKEN'

# create an instance of the API class
api_instance = quetzal.openapi_client.WorkspaceApi(quetzal.openapi_client.ApiClient(configuration))
wid = 56 # int | Workspace identifier.

try:
    # Workspace details.
    api_response = api_instance.workspace_details(wid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WorkspaceApi->workspace_details: %s\n" % e)
```

* Bearer Authentication (bearer):
```python
from __future__ import print_function
import time
import quetzal.openapi_client
from quetzal.openapi_client.rest import ApiException
from pprint import pprint
configuration = quetzal.openapi_client.Configuration()
# Configure API key authorization: apiKey
configuration.api_key['X-API-KEY'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-API-KEY'] = 'Bearer'
configuration = quetzal.openapi_client.Configuration()
# Configure Bearer authorization: bearer
configuration.access_token = 'YOUR_BEARER_TOKEN'

# create an instance of the API class
api_instance = quetzal.openapi_client.WorkspaceApi(quetzal.openapi_client.ApiClient(configuration))
wid = 56 # int | Workspace identifier.

try:
    # Workspace details.
    api_response = api_instance.workspace_details(wid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WorkspaceApi->workspace_details: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **wid** | **int**| Workspace identifier. | 

### Return type

[**Workspace**](Workspace.md)

### Authorization

[apiKey](../README.md#apiKey), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_fetch**
> PaginatedWorkspaces workspace_fetch(page=page, per_page=per_page, name=name, owner=owner, deleted=deleted)

List workspaces.

List workspace details. Optionally, filter workspaces according to their name, owner or whether they have been deleted.

### Example

* Api Key Authentication (apiKey):
```python
from __future__ import print_function
import time
import quetzal.openapi_client
from quetzal.openapi_client.rest import ApiException
from pprint import pprint
configuration = quetzal.openapi_client.Configuration()
# Configure API key authorization: apiKey
configuration.api_key['X-API-KEY'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-API-KEY'] = 'Bearer'
configuration = quetzal.openapi_client.Configuration()
# Configure Bearer authorization: bearer
configuration.access_token = 'YOUR_BEARER_TOKEN'

# create an instance of the API class
api_instance = quetzal.openapi_client.WorkspaceApi(quetzal.openapi_client.ApiClient(configuration))
page = 1 # int | The page of a collection to return. (optional) (default to 1)
per_page = 100 # int | Number of items to return per page. (optional) (default to 100)
name = 'name_example' # str | Filter workspaces by name (optional)
owner = 'owner_example' # str | Filter workspaces by owner (optional)
deleted = True # bool | Include deleted workspaces (optional)

try:
    # List workspaces.
    api_response = api_instance.workspace_fetch(page=page, per_page=per_page, name=name, owner=owner, deleted=deleted)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WorkspaceApi->workspace_fetch: %s\n" % e)
```

* Bearer Authentication (bearer):
```python
from __future__ import print_function
import time
import quetzal.openapi_client
from quetzal.openapi_client.rest import ApiException
from pprint import pprint
configuration = quetzal.openapi_client.Configuration()
# Configure API key authorization: apiKey
configuration.api_key['X-API-KEY'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-API-KEY'] = 'Bearer'
configuration = quetzal.openapi_client.Configuration()
# Configure Bearer authorization: bearer
configuration.access_token = 'YOUR_BEARER_TOKEN'

# create an instance of the API class
api_instance = quetzal.openapi_client.WorkspaceApi(quetzal.openapi_client.ApiClient(configuration))
page = 1 # int | The page of a collection to return. (optional) (default to 1)
per_page = 100 # int | Number of items to return per page. (optional) (default to 100)
name = 'name_example' # str | Filter workspaces by name (optional)
owner = 'owner_example' # str | Filter workspaces by owner (optional)
deleted = True # bool | Include deleted workspaces (optional)

try:
    # List workspaces.
    api_response = api_instance.workspace_fetch(page=page, per_page=per_page, name=name, owner=owner, deleted=deleted)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WorkspaceApi->workspace_fetch: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**| The page of a collection to return. | [optional] [default to 1]
 **per_page** | **int**| Number of items to return per page. | [optional] [default to 100]
 **name** | **str**| Filter workspaces by name | [optional] 
 **owner** | **str**| Filter workspaces by owner | [optional] 
 **deleted** | **bool**| Include deleted workspaces | [optional] 

### Return type

[**PaginatedWorkspaces**](PaginatedWorkspaces.md)

### Authorization

[apiKey](../README.md#apiKey), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_file_create**
> BaseMetadata workspace_file_create(wid, path=path, temporary=temporary, content=content)

Upload file.

Upload a new file to a workspace by sending its contents. The file will not have any additional metadata associated to it.

### Example

* Api Key Authentication (apiKey):
```python
from __future__ import print_function
import time
import quetzal.openapi_client
from quetzal.openapi_client.rest import ApiException
from pprint import pprint
configuration = quetzal.openapi_client.Configuration()
# Configure API key authorization: apiKey
configuration.api_key['X-API-KEY'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-API-KEY'] = 'Bearer'
configuration = quetzal.openapi_client.Configuration()
# Configure Bearer authorization: bearer
configuration.access_token = 'YOUR_BEARER_TOKEN'

# create an instance of the API class
api_instance = quetzal.openapi_client.WorkspaceApi(quetzal.openapi_client.ApiClient(configuration))
wid = 56 # int | Workspace identifier.
path = study/s001 # str | Path for the filename that will be set on the base metadata. This parameter is provided as a workaround to the fact that files are usually uploaded without their complete path on the filename field of the form-data request. (optional)
temporary = True # bool | True when the uploaded file is a temporary file. (optional)
content = '/path/to/file' # file | File contents in binary. (optional)

try:
    # Upload file.
    api_response = api_instance.workspace_file_create(wid, path=path, temporary=temporary, content=content)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WorkspaceApi->workspace_file_create: %s\n" % e)
```

* Bearer Authentication (bearer):
```python
from __future__ import print_function
import time
import quetzal.openapi_client
from quetzal.openapi_client.rest import ApiException
from pprint import pprint
configuration = quetzal.openapi_client.Configuration()
# Configure API key authorization: apiKey
configuration.api_key['X-API-KEY'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-API-KEY'] = 'Bearer'
configuration = quetzal.openapi_client.Configuration()
# Configure Bearer authorization: bearer
configuration.access_token = 'YOUR_BEARER_TOKEN'

# create an instance of the API class
api_instance = quetzal.openapi_client.WorkspaceApi(quetzal.openapi_client.ApiClient(configuration))
wid = 56 # int | Workspace identifier.
path = study/s001 # str | Path for the filename that will be set on the base metadata. This parameter is provided as a workaround to the fact that files are usually uploaded without their complete path on the filename field of the form-data request. (optional)
temporary = True # bool | True when the uploaded file is a temporary file. (optional)
content = '/path/to/file' # file | File contents in binary. (optional)

try:
    # Upload file.
    api_response = api_instance.workspace_file_create(wid, path=path, temporary=temporary, content=content)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WorkspaceApi->workspace_file_create: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **wid** | **int**| Workspace identifier. | 
 **path** | **str**| Path for the filename that will be set on the base metadata. This parameter is provided as a workaround to the fact that files are usually uploaded without their complete path on the filename field of the form-data request. | [optional] 
 **temporary** | **bool**| True when the uploaded file is a temporary file. | [optional] 
 **content** | **file**| File contents in binary. | [optional] 

### Return type

[**BaseMetadata**](BaseMetadata.md)

### Authorization

[apiKey](../README.md#apiKey), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_file_delete**
> workspace_file_delete(wid, uuid)

Delete a file.

Marks a file for deletion. File deletion will only occur when the workspace is committed. This operation will set the base metadata \"state\" to \"deleted\". Note that, in order to delete a file, the workspace must have access to all the families related to the file. In other words, if a file has metadata on families `base`, `foo` and `bar`, then the workspace of this operation must have these three families. Otherwise, this operation returns an error.

### Example

* Api Key Authentication (apiKey):
```python
from __future__ import print_function
import time
import quetzal.openapi_client
from quetzal.openapi_client.rest import ApiException
from pprint import pprint
configuration = quetzal.openapi_client.Configuration()
# Configure API key authorization: apiKey
configuration.api_key['X-API-KEY'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-API-KEY'] = 'Bearer'
configuration = quetzal.openapi_client.Configuration()
# Configure Bearer authorization: bearer
configuration.access_token = 'YOUR_BEARER_TOKEN'

# create an instance of the API class
api_instance = quetzal.openapi_client.WorkspaceApi(quetzal.openapi_client.ApiClient(configuration))
wid = 56 # int | Workspace identifier.
uuid = 'uuid_example' # str | File identifier

try:
    # Delete a file.
    api_instance.workspace_file_delete(wid, uuid)
except ApiException as e:
    print("Exception when calling WorkspaceApi->workspace_file_delete: %s\n" % e)
```

* Bearer Authentication (bearer):
```python
from __future__ import print_function
import time
import quetzal.openapi_client
from quetzal.openapi_client.rest import ApiException
from pprint import pprint
configuration = quetzal.openapi_client.Configuration()
# Configure API key authorization: apiKey
configuration.api_key['X-API-KEY'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-API-KEY'] = 'Bearer'
configuration = quetzal.openapi_client.Configuration()
# Configure Bearer authorization: bearer
configuration.access_token = 'YOUR_BEARER_TOKEN'

# create an instance of the API class
api_instance = quetzal.openapi_client.WorkspaceApi(quetzal.openapi_client.ApiClient(configuration))
wid = 56 # int | Workspace identifier.
uuid = 'uuid_example' # str | File identifier

try:
    # Delete a file.
    api_instance.workspace_file_delete(wid, uuid)
except ApiException as e:
    print("Exception when calling WorkspaceApi->workspace_file_delete: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **wid** | **int**| Workspace identifier. | 
 **uuid** | [**str**](.md)| File identifier | 

### Return type

void (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_file_details**
> MetadataByFamily workspace_file_details(wid, uuid)

Fetch file.

Serves the file contents or its metadata, according to the accepted content response header. When the metadata is requested, this returns the updated version with the modifications that may have been introduced in this workspace.

### Example

* Api Key Authentication (apiKey):
```python
from __future__ import print_function
import time
import quetzal.openapi_client
from quetzal.openapi_client.rest import ApiException
from pprint import pprint
configuration = quetzal.openapi_client.Configuration()
# Configure API key authorization: apiKey
configuration.api_key['X-API-KEY'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-API-KEY'] = 'Bearer'
configuration = quetzal.openapi_client.Configuration()
# Configure Bearer authorization: bearer
configuration.access_token = 'YOUR_BEARER_TOKEN'

# create an instance of the API class
api_instance = quetzal.openapi_client.WorkspaceApi(quetzal.openapi_client.ApiClient(configuration))
wid = 56 # int | Workspace identifier.
uuid = 'uuid_example' # str | File identifier

try:
    # Fetch file.
    api_response = api_instance.workspace_file_details(wid, uuid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WorkspaceApi->workspace_file_details: %s\n" % e)
```

* Bearer Authentication (bearer):
```python
from __future__ import print_function
import time
import quetzal.openapi_client
from quetzal.openapi_client.rest import ApiException
from pprint import pprint
configuration = quetzal.openapi_client.Configuration()
# Configure API key authorization: apiKey
configuration.api_key['X-API-KEY'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-API-KEY'] = 'Bearer'
configuration = quetzal.openapi_client.Configuration()
# Configure Bearer authorization: bearer
configuration.access_token = 'YOUR_BEARER_TOKEN'

# create an instance of the API class
api_instance = quetzal.openapi_client.WorkspaceApi(quetzal.openapi_client.ApiClient(configuration))
wid = 56 # int | Workspace identifier.
uuid = 'uuid_example' # str | File identifier

try:
    # Fetch file.
    api_response = api_instance.workspace_file_details(wid, uuid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WorkspaceApi->workspace_file_details: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **wid** | **int**| Workspace identifier. | 
 **uuid** | [**str**](.md)| File identifier | 

### Return type

[**MetadataByFamily**](MetadataByFamily.md)

### Authorization

[apiKey](../README.md#apiKey), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/octet-stream, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_file_fetch**
> PaginatedFiles workspace_file_fetch(wid, page=page, per_page=per_page, filters=filters)

List files.

Fetches all the files that have been added in this workspace. Files whose metadata has been modified in this workspace will also be included.  The file details included in the response only show their base metadata.

### Example

* Api Key Authentication (apiKey):
```python
from __future__ import print_function
import time
import quetzal.openapi_client
from quetzal.openapi_client.rest import ApiException
from pprint import pprint
configuration = quetzal.openapi_client.Configuration()
# Configure API key authorization: apiKey
configuration.api_key['X-API-KEY'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-API-KEY'] = 'Bearer'
configuration = quetzal.openapi_client.Configuration()
# Configure Bearer authorization: bearer
configuration.access_token = 'YOUR_BEARER_TOKEN'

# create an instance of the API class
api_instance = quetzal.openapi_client.WorkspaceApi(quetzal.openapi_client.ApiClient(configuration))
wid = 56 # int | Workspace identifier.
page = 1 # int | The page of a collection to return. (optional) (default to 1)
per_page = 100 # int | Number of items to return per page. (optional) (default to 100)
filters = filename=foo.png,path=images,size=12314 # str | Filters on the workspace files, separated by commas. These filters are applied only the base metadata family. This can be used to get a file by name, path, size or checksum. (optional)

try:
    # List files.
    api_response = api_instance.workspace_file_fetch(wid, page=page, per_page=per_page, filters=filters)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WorkspaceApi->workspace_file_fetch: %s\n" % e)
```

* Bearer Authentication (bearer):
```python
from __future__ import print_function
import time
import quetzal.openapi_client
from quetzal.openapi_client.rest import ApiException
from pprint import pprint
configuration = quetzal.openapi_client.Configuration()
# Configure API key authorization: apiKey
configuration.api_key['X-API-KEY'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-API-KEY'] = 'Bearer'
configuration = quetzal.openapi_client.Configuration()
# Configure Bearer authorization: bearer
configuration.access_token = 'YOUR_BEARER_TOKEN'

# create an instance of the API class
api_instance = quetzal.openapi_client.WorkspaceApi(quetzal.openapi_client.ApiClient(configuration))
wid = 56 # int | Workspace identifier.
page = 1 # int | The page of a collection to return. (optional) (default to 1)
per_page = 100 # int | Number of items to return per page. (optional) (default to 100)
filters = filename=foo.png,path=images,size=12314 # str | Filters on the workspace files, separated by commas. These filters are applied only the base metadata family. This can be used to get a file by name, path, size or checksum. (optional)

try:
    # List files.
    api_response = api_instance.workspace_file_fetch(wid, page=page, per_page=per_page, filters=filters)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WorkspaceApi->workspace_file_fetch: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **wid** | **int**| Workspace identifier. | 
 **page** | **int**| The page of a collection to return. | [optional] [default to 1]
 **per_page** | **int**| Number of items to return per page. | [optional] [default to 100]
 **filters** | **str**| Filters on the workspace files, separated by commas. These filters are applied only the base metadata family. This can be used to get a file by name, path, size or checksum. | [optional] 

### Return type

[**PaginatedFiles**](PaginatedFiles.md)

### Authorization

[apiKey](../README.md#apiKey), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_file_set_metadata**
> MetadataByFamily workspace_file_set_metadata(wid, uuid, metadata_by_family=metadata_by_family)

Rewrite metadata.

Change the file metadata entirely. In contrast to the PATCH method to on this endpoint, this method sets the new metadata and discards any previous metadata that was defined before.

### Example

* Api Key Authentication (apiKey):
```python
from __future__ import print_function
import time
import quetzal.openapi_client
from quetzal.openapi_client.rest import ApiException
from pprint import pprint
configuration = quetzal.openapi_client.Configuration()
# Configure API key authorization: apiKey
configuration.api_key['X-API-KEY'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-API-KEY'] = 'Bearer'
configuration = quetzal.openapi_client.Configuration()
# Configure Bearer authorization: bearer
configuration.access_token = 'YOUR_BEARER_TOKEN'

# create an instance of the API class
api_instance = quetzal.openapi_client.WorkspaceApi(quetzal.openapi_client.ApiClient(configuration))
wid = 56 # int | Workspace identifier.
uuid = 'uuid_example' # str | File identifier
metadata_by_family = quetzal.openapi_client.MetadataByFamily() # MetadataByFamily |  (optional)

try:
    # Rewrite metadata.
    api_response = api_instance.workspace_file_set_metadata(wid, uuid, metadata_by_family=metadata_by_family)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WorkspaceApi->workspace_file_set_metadata: %s\n" % e)
```

* Bearer Authentication (bearer):
```python
from __future__ import print_function
import time
import quetzal.openapi_client
from quetzal.openapi_client.rest import ApiException
from pprint import pprint
configuration = quetzal.openapi_client.Configuration()
# Configure API key authorization: apiKey
configuration.api_key['X-API-KEY'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-API-KEY'] = 'Bearer'
configuration = quetzal.openapi_client.Configuration()
# Configure Bearer authorization: bearer
configuration.access_token = 'YOUR_BEARER_TOKEN'

# create an instance of the API class
api_instance = quetzal.openapi_client.WorkspaceApi(quetzal.openapi_client.ApiClient(configuration))
wid = 56 # int | Workspace identifier.
uuid = 'uuid_example' # str | File identifier
metadata_by_family = quetzal.openapi_client.MetadataByFamily() # MetadataByFamily |  (optional)

try:
    # Rewrite metadata.
    api_response = api_instance.workspace_file_set_metadata(wid, uuid, metadata_by_family=metadata_by_family)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WorkspaceApi->workspace_file_set_metadata: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **wid** | **int**| Workspace identifier. | 
 **uuid** | [**str**](.md)| File identifier | 
 **metadata_by_family** | [**MetadataByFamily**](MetadataByFamily.md)|  | [optional] 

### Return type

[**MetadataByFamily**](MetadataByFamily.md)

### Authorization

[apiKey](../README.md#apiKey), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_file_update_metadata**
> MetadataByFamily workspace_file_update_metadata(wid, uuid, metadata_by_family=metadata_by_family)

Modify metadata.

Change the file metadata by updating it. Updating metadata changes key/value pairs, adding a new key/value pair if does not exist and changing the value if the key already exists. However, it cannot delete a key/value that already exists. To delete metadata, refer to the PUT method on this endpoint.

### Example

* Api Key Authentication (apiKey):
```python
from __future__ import print_function
import time
import quetzal.openapi_client
from quetzal.openapi_client.rest import ApiException
from pprint import pprint
configuration = quetzal.openapi_client.Configuration()
# Configure API key authorization: apiKey
configuration.api_key['X-API-KEY'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-API-KEY'] = 'Bearer'
configuration = quetzal.openapi_client.Configuration()
# Configure Bearer authorization: bearer
configuration.access_token = 'YOUR_BEARER_TOKEN'

# create an instance of the API class
api_instance = quetzal.openapi_client.WorkspaceApi(quetzal.openapi_client.ApiClient(configuration))
wid = 56 # int | Workspace identifier.
uuid = 'uuid_example' # str | File identifier
metadata_by_family = quetzal.openapi_client.MetadataByFamily() # MetadataByFamily |  (optional)

try:
    # Modify metadata.
    api_response = api_instance.workspace_file_update_metadata(wid, uuid, metadata_by_family=metadata_by_family)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WorkspaceApi->workspace_file_update_metadata: %s\n" % e)
```

* Bearer Authentication (bearer):
```python
from __future__ import print_function
import time
import quetzal.openapi_client
from quetzal.openapi_client.rest import ApiException
from pprint import pprint
configuration = quetzal.openapi_client.Configuration()
# Configure API key authorization: apiKey
configuration.api_key['X-API-KEY'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-API-KEY'] = 'Bearer'
configuration = quetzal.openapi_client.Configuration()
# Configure Bearer authorization: bearer
configuration.access_token = 'YOUR_BEARER_TOKEN'

# create an instance of the API class
api_instance = quetzal.openapi_client.WorkspaceApi(quetzal.openapi_client.ApiClient(configuration))
wid = 56 # int | Workspace identifier.
uuid = 'uuid_example' # str | File identifier
metadata_by_family = quetzal.openapi_client.MetadataByFamily() # MetadataByFamily |  (optional)

try:
    # Modify metadata.
    api_response = api_instance.workspace_file_update_metadata(wid, uuid, metadata_by_family=metadata_by_family)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WorkspaceApi->workspace_file_update_metadata: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **wid** | **int**| Workspace identifier. | 
 **uuid** | [**str**](.md)| File identifier | 
 **metadata_by_family** | [**MetadataByFamily**](MetadataByFamily.md)|  | [optional] 

### Return type

[**MetadataByFamily**](MetadataByFamily.md)

### Authorization

[apiKey](../README.md#apiKey), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_query_create**
> Query workspace_query_create(wid, query, page=page, per_page=per_page)

Prepare a query.

Queries in Quetzal are saved as a resource associated to a workspace. This endpoint creates one and responds with a *see other* status referencing the query details endpoint.  Since the query details contains the query results as a paginated list, this endpoint also accepts the normal pagination parameters.

### Example

* Api Key Authentication (apiKey):
```python
from __future__ import print_function
import time
import quetzal.openapi_client
from quetzal.openapi_client.rest import ApiException
from pprint import pprint
configuration = quetzal.openapi_client.Configuration()
# Configure API key authorization: apiKey
configuration.api_key['X-API-KEY'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-API-KEY'] = 'Bearer'
configuration = quetzal.openapi_client.Configuration()
# Configure Bearer authorization: bearer
configuration.access_token = 'YOUR_BEARER_TOKEN'

# create an instance of the API class
api_instance = quetzal.openapi_client.WorkspaceApi(quetzal.openapi_client.ApiClient(configuration))
wid = 56 # int | Workspace identifier.
query = quetzal.openapi_client.Query() # Query | 
page = 1 # int | The page of a collection to return. (optional) (default to 1)
per_page = 100 # int | Number of items to return per page. (optional) (default to 100)

try:
    # Prepare a query.
    api_response = api_instance.workspace_query_create(wid, query, page=page, per_page=per_page)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WorkspaceApi->workspace_query_create: %s\n" % e)
```

* Bearer Authentication (bearer):
```python
from __future__ import print_function
import time
import quetzal.openapi_client
from quetzal.openapi_client.rest import ApiException
from pprint import pprint
configuration = quetzal.openapi_client.Configuration()
# Configure API key authorization: apiKey
configuration.api_key['X-API-KEY'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-API-KEY'] = 'Bearer'
configuration = quetzal.openapi_client.Configuration()
# Configure Bearer authorization: bearer
configuration.access_token = 'YOUR_BEARER_TOKEN'

# create an instance of the API class
api_instance = quetzal.openapi_client.WorkspaceApi(quetzal.openapi_client.ApiClient(configuration))
wid = 56 # int | Workspace identifier.
query = quetzal.openapi_client.Query() # Query | 
page = 1 # int | The page of a collection to return. (optional) (default to 1)
per_page = 100 # int | Number of items to return per page. (optional) (default to 100)

try:
    # Prepare a query.
    api_response = api_instance.workspace_query_create(wid, query, page=page, per_page=per_page)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WorkspaceApi->workspace_query_create: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **wid** | **int**| Workspace identifier. | 
 **query** | [**Query**](Query.md)|  | 
 **page** | **int**| The page of a collection to return. | [optional] [default to 1]
 **per_page** | **int**| Number of items to return per page. | [optional] [default to 100]

### Return type

[**Query**](Query.md)

### Authorization

[apiKey](../README.md#apiKey), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_query_details**
> Query workspace_query_details(wid, qid, page=page, per_page=per_page)

Query details.

The details of a query, which contains the query itself and a paginated list of its results.

### Example

* Api Key Authentication (apiKey):
```python
from __future__ import print_function
import time
import quetzal.openapi_client
from quetzal.openapi_client.rest import ApiException
from pprint import pprint
configuration = quetzal.openapi_client.Configuration()
# Configure API key authorization: apiKey
configuration.api_key['X-API-KEY'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-API-KEY'] = 'Bearer'
configuration = quetzal.openapi_client.Configuration()
# Configure Bearer authorization: bearer
configuration.access_token = 'YOUR_BEARER_TOKEN'

# create an instance of the API class
api_instance = quetzal.openapi_client.WorkspaceApi(quetzal.openapi_client.ApiClient(configuration))
wid = 56 # int | Workspace identifier.
qid = 56 # int | Query identifier
page = 1 # int | The page of a collection to return. (optional) (default to 1)
per_page = 100 # int | Number of items to return per page. (optional) (default to 100)

try:
    # Query details.
    api_response = api_instance.workspace_query_details(wid, qid, page=page, per_page=per_page)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WorkspaceApi->workspace_query_details: %s\n" % e)
```

* Bearer Authentication (bearer):
```python
from __future__ import print_function
import time
import quetzal.openapi_client
from quetzal.openapi_client.rest import ApiException
from pprint import pprint
configuration = quetzal.openapi_client.Configuration()
# Configure API key authorization: apiKey
configuration.api_key['X-API-KEY'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-API-KEY'] = 'Bearer'
configuration = quetzal.openapi_client.Configuration()
# Configure Bearer authorization: bearer
configuration.access_token = 'YOUR_BEARER_TOKEN'

# create an instance of the API class
api_instance = quetzal.openapi_client.WorkspaceApi(quetzal.openapi_client.ApiClient(configuration))
wid = 56 # int | Workspace identifier.
qid = 56 # int | Query identifier
page = 1 # int | The page of a collection to return. (optional) (default to 1)
per_page = 100 # int | Number of items to return per page. (optional) (default to 100)

try:
    # Query details.
    api_response = api_instance.workspace_query_details(wid, qid, page=page, per_page=per_page)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WorkspaceApi->workspace_query_details: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **wid** | **int**| Workspace identifier. | 
 **qid** | **int**| Query identifier | 
 **page** | **int**| The page of a collection to return. | [optional] [default to 1]
 **per_page** | **int**| Number of items to return per page. | [optional] [default to 100]

### Return type

[**Query**](Query.md)

### Authorization

[apiKey](../README.md#apiKey), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_query_fetch**
> PaginatedQueries workspace_query_fetch(wid, page=page, per_page=per_page)

List queries.

List all the queries that are associated with a workspace. Note that each query listed here is shown _without_ its results, for brevity.

### Example

* Api Key Authentication (apiKey):
```python
from __future__ import print_function
import time
import quetzal.openapi_client
from quetzal.openapi_client.rest import ApiException
from pprint import pprint
configuration = quetzal.openapi_client.Configuration()
# Configure API key authorization: apiKey
configuration.api_key['X-API-KEY'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-API-KEY'] = 'Bearer'
configuration = quetzal.openapi_client.Configuration()
# Configure Bearer authorization: bearer
configuration.access_token = 'YOUR_BEARER_TOKEN'

# create an instance of the API class
api_instance = quetzal.openapi_client.WorkspaceApi(quetzal.openapi_client.ApiClient(configuration))
wid = 56 # int | Workspace identifier.
page = 1 # int | The page of a collection to return. (optional) (default to 1)
per_page = 100 # int | Number of items to return per page. (optional) (default to 100)

try:
    # List queries.
    api_response = api_instance.workspace_query_fetch(wid, page=page, per_page=per_page)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WorkspaceApi->workspace_query_fetch: %s\n" % e)
```

* Bearer Authentication (bearer):
```python
from __future__ import print_function
import time
import quetzal.openapi_client
from quetzal.openapi_client.rest import ApiException
from pprint import pprint
configuration = quetzal.openapi_client.Configuration()
# Configure API key authorization: apiKey
configuration.api_key['X-API-KEY'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-API-KEY'] = 'Bearer'
configuration = quetzal.openapi_client.Configuration()
# Configure Bearer authorization: bearer
configuration.access_token = 'YOUR_BEARER_TOKEN'

# create an instance of the API class
api_instance = quetzal.openapi_client.WorkspaceApi(quetzal.openapi_client.ApiClient(configuration))
wid = 56 # int | Workspace identifier.
page = 1 # int | The page of a collection to return. (optional) (default to 1)
per_page = 100 # int | Number of items to return per page. (optional) (default to 100)

try:
    # List queries.
    api_response = api_instance.workspace_query_fetch(wid, page=page, per_page=per_page)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WorkspaceApi->workspace_query_fetch: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **wid** | **int**| Workspace identifier. | 
 **page** | **int**| The page of a collection to return. | [optional] [default to 1]
 **per_page** | **int**| Number of items to return per page. | [optional] [default to 100]

### Return type

[**PaginatedQueries**](PaginatedQueries.md)

### Authorization

[apiKey](../README.md#apiKey), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_scan**
> Workspace workspace_scan(wid)

Update views.

Requests the update of the views of a workspace. All the internal databases used for the query operation will be updated to contain the latest modifications of the metadata.

### Example

* Api Key Authentication (apiKey):
```python
from __future__ import print_function
import time
import quetzal.openapi_client
from quetzal.openapi_client.rest import ApiException
from pprint import pprint
configuration = quetzal.openapi_client.Configuration()
# Configure API key authorization: apiKey
configuration.api_key['X-API-KEY'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-API-KEY'] = 'Bearer'
configuration = quetzal.openapi_client.Configuration()
# Configure Bearer authorization: bearer
configuration.access_token = 'YOUR_BEARER_TOKEN'

# create an instance of the API class
api_instance = quetzal.openapi_client.WorkspaceApi(quetzal.openapi_client.ApiClient(configuration))
wid = 56 # int | Workspace identifier.

try:
    # Update views.
    api_response = api_instance.workspace_scan(wid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WorkspaceApi->workspace_scan: %s\n" % e)
```

* Bearer Authentication (bearer):
```python
from __future__ import print_function
import time
import quetzal.openapi_client
from quetzal.openapi_client.rest import ApiException
from pprint import pprint
configuration = quetzal.openapi_client.Configuration()
# Configure API key authorization: apiKey
configuration.api_key['X-API-KEY'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-API-KEY'] = 'Bearer'
configuration = quetzal.openapi_client.Configuration()
# Configure Bearer authorization: bearer
configuration.access_token = 'YOUR_BEARER_TOKEN'

# create an instance of the API class
api_instance = quetzal.openapi_client.WorkspaceApi(quetzal.openapi_client.ApiClient(configuration))
wid = 56 # int | Workspace identifier.

try:
    # Update views.
    api_response = api_instance.workspace_scan(wid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WorkspaceApi->workspace_scan: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **wid** | **int**| Workspace identifier. | 

### Return type

[**Workspace**](Workspace.md)

### Authorization

[apiKey](../README.md#apiKey), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

