# NewImportServerSettings


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**allow_partial_sync** | **bool** |  | [optional] 
**hostname** | **str** |  | 
**friendly_name** | **str** |  | 
**ssh_user** | **str** |  | 
**import_type** | [**ImportKind**](ImportKind.md) |  | 
**auth_kind** | [**ServerMigrationSettingsAuthType**](ServerMigrationSettingsAuthType.md) |  | 
**auth_user** | **str** |  | 
**auth_pass** | **str** |  | 
**ssh_port** | **float** |  | 
**api_port** | **float** |  | 

## Example

```python
from openapi_client.models.new_import_server_settings import NewImportServerSettings

# TODO update the JSON string below
json = "{}"
# create an instance of NewImportServerSettings from a JSON string
new_import_server_settings_instance = NewImportServerSettings.from_json(json)
# print the JSON string representation of the object
print(NewImportServerSettings.to_json())

# convert the object into a dict
new_import_server_settings_dict = new_import_server_settings_instance.to_dict()
# create an instance of NewImportServerSettings from a dict
new_import_server_settings_from_dict = NewImportServerSettings.from_dict(new_import_server_settings_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


