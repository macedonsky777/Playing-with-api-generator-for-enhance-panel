# UpdateImportServerSettings


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**hostname** | **str** |  | [optional] 
**friendly_name** | **str** |  | [optional] 
**ssh_user** | **str** |  | [optional] 
**ssh_public_key** | **str** |  | [optional] 
**ssh_private_key** | **str** |  | [optional] 
**import_type** | [**ImportKind**](ImportKind.md) |  | [optional] 
**auth_kind** | [**ServerMigrationSettingsAuthType**](ServerMigrationSettingsAuthType.md) |  | [optional] 
**auth_user** | **str** |  | [optional] 
**ssh_port** | **float** |  | [optional] 
**api_port** | **float** |  | [optional] 
**allow_partial_sync** | **bool** |  | [optional] 

## Example

```python
from openapi_client.models.update_import_server_settings import UpdateImportServerSettings

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateImportServerSettings from a JSON string
update_import_server_settings_instance = UpdateImportServerSettings.from_json(json)
# print the JSON string representation of the object
print(UpdateImportServerSettings.to_json())

# convert the object into a dict
update_import_server_settings_dict = update_import_server_settings_instance.to_dict()
# create an instance of UpdateImportServerSettings from a dict
update_import_server_settings_from_dict = UpdateImportServerSettings.from_dict(update_import_server_settings_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


