# quetzal.openapi_client.PublicApi

All URIs are relative to *https://api.quetz.al/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**public_file_details**](PublicApi.md#public_file_details) | **GET** /data/files/{uuid} | Fetch public file.
[**public_file_fetch**](PublicApi.md#public_file_fetch) | **GET** /data/files/ | List public files.
[**public_query_create**](PublicApi.md#public_query_create) | **POST** /data/queries/ | Prepare a query.
[**public_query_fetch**](PublicApi.md#public_query_fetch) | **GET** /data/queries/ | List public queries.
[**workspace_create**](PublicApi.md#workspace_create) | **POST** /data/workspaces/ | Create workspace.
[**workspace_fetch**](PublicApi.md#workspace_fetch) | **GET** /data/workspaces/ | List workspaces.


# **public_file_details**
> MetadataByFamily public_file_details(uuid)

Fetch public file.

This endpoint can be used to fetch the file contents or its metadata. The type of response, data or metadata, depends on the `Accept` request header. In the case of metadata, this endpoint returns the most recent metadata that has been committed.

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
api_instance = quetzal.openapi_client.PublicApi(quetzal.openapi_client.ApiClient(configuration))
uuid = 'uuid_example' # str | File identifier

try:
    # Fetch public file.
    api_response = api_instance.public_file_details(uuid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PublicApi->public_file_details: %s\n" % e)
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
api_instance = quetzal.openapi_client.PublicApi(quetzal.openapi_client.ApiClient(configuration))
uuid = 'uuid_example' # str | File identifier

try:
    # Fetch public file.
    api_response = api_instance.public_file_details(uuid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PublicApi->public_file_details: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| File identifier | 

### Return type

[**MetadataByFamily**](MetadataByFamily.md)

### Authorization

[apiKey](../README.md#apiKey), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/octet-stream, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **public_file_fetch**
> PaginatedFiles public_file_fetch(page=page, per_page=per_page, filters=filters)

List public files.

Fetches all the files that have been committed.  The file details included in the response only show their base metadata.

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
api_instance = quetzal.openapi_client.PublicApi(quetzal.openapi_client.ApiClient(configuration))
page = 1 # int | The page of a collection to return. (optional) (default to 1)
per_page = 100 # int | Number of items to return per page. (optional) (default to 100)
filters = filename=foo.png,path=images,size=12314 # str | Filters on the workspace files, separated by commas. These filters are applied only the base metadata family. This can be used to get a file by name, path, size or checksum. (optional)

try:
    # List public files.
    api_response = api_instance.public_file_fetch(page=page, per_page=per_page, filters=filters)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PublicApi->public_file_fetch: %s\n" % e)
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
api_instance = quetzal.openapi_client.PublicApi(quetzal.openapi_client.ApiClient(configuration))
page = 1 # int | The page of a collection to return. (optional) (default to 1)
per_page = 100 # int | Number of items to return per page. (optional) (default to 100)
filters = filename=foo.png,path=images,size=12314 # str | Filters on the workspace files, separated by commas. These filters are applied only the base metadata family. This can be used to get a file by name, path, size or checksum. (optional)

try:
    # List public files.
    api_response = api_instance.public_file_fetch(page=page, per_page=per_page, filters=filters)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PublicApi->public_file_fetch: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
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

# **public_query_create**
> Query public_query_create(query, page=page, per_page=per_page)

Prepare a query.

Queries in Quetzal are saved as a resource, in this case, associated with the global workspace. This endpoint creates one and responds with a *see other* status referencing the query details endpoint.  Since the query details contains the query results as a paginated list, this endpoint also accepts the normal pagination parameters.

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
api_instance = quetzal.openapi_client.PublicApi(quetzal.openapi_client.ApiClient(configuration))
query = quetzal.openapi_client.Query() # Query | 
page = 1 # int | The page of a collection to return. (optional) (default to 1)
per_page = 100 # int | Number of items to return per page. (optional) (default to 100)

try:
    # Prepare a query.
    api_response = api_instance.public_query_create(query, page=page, per_page=per_page)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PublicApi->public_query_create: %s\n" % e)
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
api_instance = quetzal.openapi_client.PublicApi(quetzal.openapi_client.ApiClient(configuration))
query = quetzal.openapi_client.Query() # Query | 
page = 1 # int | The page of a collection to return. (optional) (default to 1)
per_page = 100 # int | Number of items to return per page. (optional) (default to 100)

try:
    # Prepare a query.
    api_response = api_instance.public_query_create(query, page=page, per_page=per_page)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PublicApi->public_query_create: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
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

# **public_query_fetch**
> PaginatedQueries public_query_fetch(page=page, per_page=per_page)

List public queries.

List all the queries that are associated with the global workspace. Note that each query listed here is shown _without_ its results, for brevity.

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
api_instance = quetzal.openapi_client.PublicApi(quetzal.openapi_client.ApiClient(configuration))
page = 1 # int | The page of a collection to return. (optional) (default to 1)
per_page = 100 # int | Number of items to return per page. (optional) (default to 100)

try:
    # List public queries.
    api_response = api_instance.public_query_fetch(page=page, per_page=per_page)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PublicApi->public_query_fetch: %s\n" % e)
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
api_instance = quetzal.openapi_client.PublicApi(quetzal.openapi_client.ApiClient(configuration))
page = 1 # int | The page of a collection to return. (optional) (default to 1)
per_page = 100 # int | Number of items to return per page. (optional) (default to 100)

try:
    # List public queries.
    api_response = api_instance.public_query_fetch(page=page, per_page=per_page)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PublicApi->public_query_fetch: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
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

# **workspace_create**
> Workspace workspace_create(workspace)

Create workspace.

Create a workspace, which initializes the basic resources and information associated with it, and then schedules some background tasks to initialize Cloud resources.

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
api_instance = quetzal.openapi_client.PublicApi(quetzal.openapi_client.ApiClient(configuration))
workspace = quetzal.openapi_client.Workspace() # Workspace | 

try:
    # Create workspace.
    api_response = api_instance.workspace_create(workspace)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PublicApi->workspace_create: %s\n" % e)
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
api_instance = quetzal.openapi_client.PublicApi(quetzal.openapi_client.ApiClient(configuration))
workspace = quetzal.openapi_client.Workspace() # Workspace | 

try:
    # Create workspace.
    api_response = api_instance.workspace_create(workspace)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PublicApi->workspace_create: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace** | [**Workspace**](Workspace.md)|  | 

### Return type

[**Workspace**](Workspace.md)

### Authorization

[apiKey](../README.md#apiKey), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
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
api_instance = quetzal.openapi_client.PublicApi(quetzal.openapi_client.ApiClient(configuration))
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
    print("Exception when calling PublicApi->workspace_fetch: %s\n" % e)
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
api_instance = quetzal.openapi_client.PublicApi(quetzal.openapi_client.ApiClient(configuration))
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
    print("Exception when calling PublicApi->workspace_fetch: %s\n" % e)
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

