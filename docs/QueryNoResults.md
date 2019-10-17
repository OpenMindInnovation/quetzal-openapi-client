# QueryNoResults

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**dialect** | **str** | Dialect of the query.  Use \&quot;postgresql\&quot; for queries that are written in PostgresSQL. For these queries, there will be one table per family, with as many columns as there are keys in each family.  Use \&quot;postgresql_json\&quot; for queries thar are written in PostgresSQL. For this particular case, there will be one unique table called metadata that has an id column and a column for each family. | 
**id** | **int** | Query identifier | 
**query** | **str** | Query in code as needed by the dialect | 
**workspace_id** | **int** | Workspace identifier where the query operates | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


