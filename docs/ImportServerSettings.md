# ImportServerSettings


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**hostname** | **str** |  | 
**friendly_name** | **str** |  | 
**ssh_user** | **str** |  | 
**ssh_public_key** | **str** |  | 
**import_type** | [**ImportKind**](ImportKind.md) |  | 
**auth_kind** | [**ServerMigrationSettingsAuthType**](ServerMigrationSettingsAuthType.md) |  | 
**auth_user** | **str** |  | 
**ssh_port** | **float** |  | 
**api_port** | **float** |  | 
**allow_partial_sync** | **bool** |  | 

## Example

```python
from openapi_client.models.import_server_settings import ImportServerSettings

# TODO update the JSON string below
json = "{}"
# create an instance of ImportServerSettings from a JSON string
import_server_settings_instance = ImportServerSettings.from_json(json)
# print the JSON string representation of the object
print(ImportServerSettings.to_json())

# convert the object into a dict
import_server_settings_dict = import_server_settings_instance.to_dict()
# create an instance of ImportServerSettings from a dict
import_server_settings_from_dict = ImportServerSettings.from_dict(import_server_settings_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


