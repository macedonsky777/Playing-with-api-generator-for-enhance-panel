# Website


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**domain** | [**WebsiteDomain**](WebsiteDomain.md) |  | 
**aliases** | [**List[WebsiteDomain]**](WebsiteDomain.md) |  | 
**subdomains** | **List[object]** |  | 
**subscription_id** | **float** |  | [optional] 
**plan_id** | **float** |  | [optional] 
**plan** | **str** |  | [optional] 
**status** | [**WebsiteStatus**](WebsiteStatus.md) |  | 
**suspended_by** | **str** |  | [optional] 
**color_code** | **str** |  | 
**tags** | [**List[Tag]**](Tag.md) |  | [optional] 
**size** | **int** |  | 
**org_id** | **str** |  | 
**org** | **str** |  | [optional] 
**kind** | [**WebsiteKind**](WebsiteKind.md) |  | 
**pending_backup** | [**BackupAction**](BackupAction.md) |  | [optional] 
**parent** | **str** |  | [optional] 
**parent_id** | **str** |  | [optional] 
**app_server_id** | **str** | The id of the server on which this website is located. This is only returned when websites are queried recursively by an MO member, as the MO is in charge of servers and thus this information only concerns them. | [optional] 
**backup_server_id** | **str** | The id of the server on which the backups of this website are located. This is only returned when websites are queried recursively by an MO member, as the MO is in charge of servers and thus this information only concerns them. | [optional] 
**db_server_id** | **str** | The id of the server on which the databases of this website are located. This is only returned when websites are queried recursively by an MO member, as the MO is in charge of servers and thus this information only concerns them. | [optional] 
**email_server_id** | **str** | The id of the server on which the emails of this website are located. This is only returned when websites are queried recursively by an MO member, as the MO is in charge of servers and thus this information only concerns them. | [optional] 
**unix_user** | **str** | The unix user assigned to this website, used for ssh shells, prefixing website databases and databse users, etc. | [optional] 
**site_access_members** | [**List[SiteAccessMember]**](SiteAccessMember.md) |  | [optional] 
**server_ips** | [**List[ServerIp]**](ServerIp.md) | The addresses of the the server on which this website is located. | [optional] 
**backup_server_ips** | [**List[ServerIp]**](ServerIp.md) | The addresses of the the server on which this website&#39;s backups are located. | [optional] 
**db_server_ips** | [**List[ServerIp]**](ServerIp.md) | The addresses of the the server on which this website&#39;s databases are located. | [optional] 
**email_server_ips** | [**List[ServerIp]**](ServerIp.md) | The addresses of the the server on which this website&#39;s emails are located. | [optional] 
**filerd_address** | **str** | The path relative to the control panel domain where filerd can be accessed. | [optional] 
**php_version** | [**PhpVersion**](PhpVersion.md) |  | [optional] 
**created_at** | **str** | The date the site was first added | 
**app_server_name** | **str** |  | [optional] 
**db_server_name** | **str** |  | [optional] 
**email_server_name** | **str** |  | [optional] 
**backup_server_name** | **str** |  | [optional] 
**can_use** | [**CanUse**](CanUse.md) |  | [optional] 
**app_server_ipv6** | **str** |  | [optional] 
**db_server_ipv6** | **str** |  | [optional] 
**email_server_ipv6** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.website import Website

# TODO update the JSON string below
json = "{}"
# create an instance of Website from a JSON string
website_instance = Website.from_json(json)
# print the JSON string representation of the object
print(Website.to_json())

# convert the object into a dict
website_dict = website_instance.to_dict()
# create an instance of Website from a dict
website_from_dict = Website.from_dict(website_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


