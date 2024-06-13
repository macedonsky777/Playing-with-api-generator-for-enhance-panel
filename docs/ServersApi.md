# openapi_client.ServersApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**configure_server**](ServersApi.md#configure_server) | **PATCH** /servers/{server_id} | Configure a server
[**create_server_domain**](ServersApi.md#create_server_domain) | **POST** /servers/{server_id}/domains | Create a domain which is mapped to a server
[**create_server_group**](ServersApi.md#create_server_group) | **POST** /servers/groups | Creates a new server group
[**create_server_network_interface_ip**](ServersApi.md#create_server_network_interface_ip) | **POST** /servers/{server_id}/interfaces/{interface}/ips | Create server network interface secondary IP
[**create_slave**](ServersApi.md#create_slave) | **POST** /servers/slaves | Create a slave node
[**delete_server_domain**](ServersApi.md#delete_server_domain) | **DELETE** /servers/{server_id}/domains/{domain_id} | Delete a mapped server domain
[**delete_server_from_group**](ServersApi.md#delete_server_from_group) | **DELETE** /servers/{server_id}/group | Delete server from group
[**delete_server_group**](ServersApi.md#delete_server_group) | **DELETE** /servers/groups/{group_id} | Deletes an existing server group
[**delete_server_network_interface_ip**](ServersApi.md#delete_server_network_interface_ip) | **DELETE** /servers/{server_id}/interfaces/{interface}/ips/{ip} | Delete server network interface secondary IP
[**delete_server_primary_ipv6**](ServersApi.md#delete_server_primary_ipv6) | **DELETE** /v2/servers/{server_id}/primary-ipv6 | Deletes/unsets the primary IPv6 address for a server.
[**delete_service_setting**](ServersApi.md#delete_service_setting) | **DELETE** /servers/{server_id}/settings/{setting_kind}/{setting_key} | Delete a single override setting
[**delete_slave**](ServersApi.md#delete_slave) | **DELETE** /servers/{server_id} | Delete a (slave) server
[**enable_fs_quota_limits**](ServersApi.md#enable_fs_quota_limits) | **POST** /servers/{server_id}/fs-quota-limits | Enable FS quota limits on the server
[**get_appcd_screenshot_config**](ServersApi.md#get_appcd_screenshot_config) | **GET** /servers/{server_id}/appcd/screenshot/config | Get the screenshot config of the running appcd
[**get_appcd_version**](ServersApi.md#get_appcd_version) | **GET** /servers/{server_id}/appcd/version | Get the version of the running appcd
[**get_client_ip**](ServersApi.md#get_client_ip) | **GET** /client_ip | Reflect back the IP of the API consumer
[**get_control_panel_role_info**](ServersApi.md#get_control_panel_role_info) | **GET** /servers/master/roles/control | Get master server control panel role info
[**get_database_role_mysql_kind**](ServersApi.md#get_database_role_mysql_kind) | **GET** /v2/servers/{server_id}/database-role | Gets the MySQL kind for a given server.
[**get_dns_pool_ips**](ServersApi.md#get_dns_pool_ips) | **GET** /v2/servers/dns_pool | Get DNS pool IPs
[**get_fs_quota_status**](ServersApi.md#get_fs_quota_status) | **GET** /servers/{server_id}/fs-quota-limits | Get whether FS quota was enabled on the server
[**get_httpd_status**](ServersApi.md#get_httpd_status) | **GET** /servers/{server_id}/roles/{role}/httpd_status | Get status of a running httpd server.
[**get_install_cmd**](ServersApi.md#get_install_cmd) | **GET** /servers/install-cmd | Get slave installation command
[**get_mysql_my_cnf**](ServersApi.md#get_mysql_my_cnf) | **GET** /v2/servers/{server_id}/my-cnf | Download my.cnf for a given server
[**get_owasp_rules_version**](ServersApi.md#get_owasp_rules_version) | **GET** /v2/servers/{server_id}/owasp | Get the current and available version of the OWASP rules
[**get_registration_key**](ServersApi.md#get_registration_key) | **GET** /servers/registration-key | Get slave registration key
[**get_server_disk_usage**](ServersApi.md#get_server_disk_usage) | **GET** /servers/{server_id}/disk-usage | Get server disk usage
[**get_server_fpm_settings**](ServersApi.md#get_server_fpm_settings) | **GET** /servers/{server_id}/php/fpm | Get php-fpm config for all the websites on a server
[**get_server_groups**](ServersApi.md#get_server_groups) | **GET** /servers/groups | Returns all server groups
[**get_server_hostname_website**](ServersApi.md#get_server_hostname_website) | **GET** /servers/{server_id}/domains | Get domains which are mapped to a server
[**get_server_info**](ServersApi.md#get_server_info) | **GET** /servers/{server_id} | Get server info
[**get_server_iowait**](ServersApi.md#get_server_iowait) | **GET** /servers/{server_id}/iowait | Get server iowait
[**get_server_load**](ServersApi.md#get_server_load) | **GET** /servers/{server_id}/load | Get server system load
[**get_server_memory_usage**](ServersApi.md#get_server_memory_usage) | **GET** /servers/{server_id}/memory-usage | Get server memory usage
[**get_server_mod_security_config**](ServersApi.md#get_server_mod_security_config) | **GET** /v2/servers/{server_id}/modsec_conf | Get mod security config
[**get_server_mod_security_status**](ServersApi.md#get_server_mod_security_status) | **GET** /v2/servers/{server_id}/modsec_status | Get mod security status for a server
[**get_server_network_interfaces**](ServersApi.md#get_server_network_interfaces) | **GET** /servers/{server_id}/interfaces | Get server network interfaces
[**get_server_network_stats**](ServersApi.md#get_server_network_stats) | **GET** /servers/{server_id}/network-stats | Get server network stats
[**get_server_role**](ServersApi.md#get_server_role) | **GET** /servers/{server_id}/roles/{role} | Get server role info
[**get_server_roles**](ServersApi.md#get_server_roles) | **GET** /servers/{server_id}/roles | Get server roles info
[**get_server_stats**](ServersApi.md#get_server_stats) | **GET** /servers/{server_id}/historic-stats | Get Server stats
[**get_server_status**](ServersApi.md#get_server_status) | **GET** /servers/{server_id}/status | Get server status
[**get_server_uptime**](ServersApi.md#get_server_uptime) | **GET** /servers/{server_id}/uptime | Get server uptime in seconds
[**get_servers**](ServersApi.md#get_servers) | **GET** /servers | Get installed servers
[**get_service_setting**](ServersApi.md#get_service_setting) | **GET** /servers/{server_id}/settings/{setting_kind} | Get the value for a particular setting
[**get_system_package_update_info**](ServersApi.md#get_system_package_update_info) | **GET** /servers/{server_id}/packages/update | Returns a map of upgradable packages.
[**get_webserver_kind**](ServersApi.md#get_webserver_kind) | **GET** /servers/{server_id}/webserver | Get web server
[**get_website_fpm_settings**](ServersApi.md#get_website_fpm_settings) | **GET** /servers/{server_id}/php/fpm/{website_id} | Get php-fpm config for the specified website
[**init_all_servers**](ServersApi.md#init_all_servers) | **POST** /servers/init | Attempts to initialize all roles
[**install_database_role**](ServersApi.md#install_database_role) | **PUT** /v2/servers/{server_id}/database-role | Enables the database role on a given ServerUuid
[**install_server_role**](ServersApi.md#install_server_role) | **PUT** /servers/{server_id}/roles/{role} | Install server role
[**reset_server_mod_security_config**](ServersApi.md#reset_server_mod_security_config) | **DELETE** /v2/servers/{server_id}/modsec_conf | Delete custom mod_security config and reset to default
[**reset_web_server_config**](ServersApi.md#reset_web_server_config) | **POST** /servers/{server_id}/webserver/config/reset | Reset the config for the web server to default.
[**restart_mysql**](ServersApi.md#restart_mysql) | **POST** /v2/servers/{server_id}/database-role/restart | Restart MySQL gracefully
[**save_mysql_my_cnf**](ServersApi.md#save_mysql_my_cnf) | **PUT** /v2/servers/{server_id}/my-cnf | Save a new my.cnf
[**set_lite_speed_admin_password**](ServersApi.md#set_lite_speed_admin_password) | **POST** /servers/{server_id}/webserver/litespeed/password | Set a new LiteSpeed admin password.
[**set_server_decommissioned**](ServersApi.md#set_server_decommissioned) | **PUT** /servers/{server_id}/decommissioned | Set server to decommissioned
[**set_server_mod_security_config**](ServersApi.md#set_server_mod_security_config) | **PUT** /v2/servers/{server_id}/modsec_conf | Set mod security config
[**set_server_mod_security_status**](ServersApi.md#set_server_mod_security_status) | **PUT** /v2/servers/{server_id}/modsec_status | Set mod security status for a server
[**set_server_status**](ServersApi.md#set_server_status) | **POST** /servers/{server_id}/status | Set the status of one server.
[**set_service_setting**](ServersApi.md#set_service_setting) | **PUT** /servers/{server_id}/settings/{setting_kind}/{setting_key} | Set a single service setting
[**set_service_status**](ServersApi.md#set_service_status) | **POST** /servers/{server_id}/services/{service_id}/status | Set the status of one service installed in the server specified.
[**set_webserver_kind**](ServersApi.md#set_webserver_kind) | **PUT** /servers/{server_id}/webserver | Set the web server kind for one server.
[**uninstall_server_role**](ServersApi.md#uninstall_server_role) | **DELETE** /servers/{server_id}/roles/{role} | Uninstall a server role
[**update_appcd_screenshot_config**](ServersApi.md#update_appcd_screenshot_config) | **PATCH** /servers/{server_id}/appcd/screenshot/config | Update the screenshot config of the running appcd
[**update_owasp_rules**](ServersApi.md#update_owasp_rules) | **POST** /v2/servers/{server_id}/owasp | Upgrade OWASP rules
[**update_server_group**](ServersApi.md#update_server_group) | **PUT** /servers/groups/{group_id} | Updates an existing server group&#39;s name
[**update_server_primary_ip**](ServersApi.md#update_server_primary_ip) | **PUT** /servers/{server_id}/primary-ip | Updates the primary IP of the server in the database and in-memory metadata. This operation will not affect the IP used for service communication until the next restart of orchd. The new IP will be used for creation of new resources such as websites on this server but existing websites will not have their IP changed.
[**update_server_primary_ipv6**](ServersApi.md#update_server_primary_ipv6) | **PUT** /v2/servers/{server_id}/primary-ipv6 | Updates or sets the primary ipv6 address of the server.  This endpoint will not change existing websites&#39; DNS but the new record will be applied to all future zones.
[**update_server_role**](ServersApi.md#update_server_role) | **PATCH** /servers/{server_id}/roles/{role} | Update server role
[**update_service**](ServersApi.md#update_service) | **PUT** /servers/{server_id}/services/{service_id}/update | Special endpoint to update a particular stopped service to its latest version.
[**update_system_package**](ServersApi.md#update_system_package) | **PUT** /servers/{server_id}/packages/update | Updates a system package to its latest version.
[**validate_registration_key**](ServersApi.md#validate_registration_key) | **POST** /servers/registration-key/validate | Validate slave registration key


# **configure_server**
> configure_server(server_id, server_conf)

Configure a server

Configures a server with roles to enable or disable, a friendly name to give (for identification purposes), and/or to assign server to a group. Session holder must be an `Owner`, `SuperAdmin`, or `Sysadmin` in the MO.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.server_conf import ServerConf
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server
    server_conf = openapi_client.ServerConf() # ServerConf | 

    try:
        # Configure a server
        api_instance.configure_server(server_id, server_conf)
    except Exception as e:
        print("Exception when calling ServersApi->configure_server: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 
 **server_conf** | [**ServerConf**](ServerConf.md)|  | 

### Return type

void (empty response body)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Configuration successful |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_server_domain**
> WebsiteAndDomainUuid create_server_domain(server_id, body)

Create a domain which is mapped to a server

Maps a hostname to a server by creating a special kind of website with kind `ServerHostname`.  This can be used for POP/IMAP/SMTP as well as HTTP. LetsEncrypt certificates will be issued if the DNS resolves.  Only one server hostname website will be created, additional domains will be added as aliases.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.website_and_domain_uuid import WebsiteAndDomainUuid
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server
    body = 'body_example' # str | 

    try:
        # Create a domain which is mapped to a server
        api_response = api_instance.create_server_domain(server_id, body)
        print("The response of ServersApi->create_server_domain:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->create_server_domain: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 
 **body** | **str**|  | 

### Return type

[**WebsiteAndDomainUuid**](WebsiteAndDomainUuid.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Created |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_server_group**
> NewResourceUuid create_server_group(new_server_group)

Creates a new server group

Session holder must be an `Owner`, `SuperAdmin`, or `Sysadmin` in the MO.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.new_resource_uuid import NewResourceUuid
from openapi_client.models.new_server_group import NewServerGroup
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    new_server_group = openapi_client.NewServerGroup() # NewServerGroup | The name of the new server group.

    try:
        # Creates a new server group
        api_response = api_instance.create_server_group(new_server_group)
        print("The response of ServersApi->create_server_group:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->create_server_group: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **new_server_group** | [**NewServerGroup**](NewServerGroup.md)| The name of the new server group. | 

### Return type

[**NewResourceUuid**](NewResourceUuid.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Server group successfully created |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**409** | Already exists |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_server_network_interface_ip**
> create_server_network_interface_ip(server_id, interface, new_server_ip)

Create server network interface secondary IP

Creates a new secondary IP address for the server's network interface. Session holder must be an `Owner`, `SuperAdmin`, or `Sysadmin` in the MO.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.new_server_ip import NewServerIp
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server
    interface = 'interface_example' # str | The name of the network interface
    new_server_ip = openapi_client.NewServerIp() # NewServerIp | 

    try:
        # Create server network interface secondary IP
        api_instance.create_server_network_interface_ip(server_id, interface, new_server_ip)
    except Exception as e:
        print("Exception when calling ServersApi->create_server_network_interface_ip: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 
 **interface** | **str**| The name of the network interface | 
 **new_server_ip** | [**NewServerIp**](NewServerIp.md)|  | 

### Return type

void (empty response body)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |
**409** | Already exists |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_slave**
> create_slave(key, slave_registration)

Create a slave node

This endpoint is called by the slave server installation script and not by the API. Only included for completeness.

### Example


```python
import openapi_client
from openapi_client.models.slave_registration import SlaveRegistration
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
    api_instance = openapi_client.ServersApi(api_client)
    key = 'key_example' # str | The secret registration key
    slave_registration = openapi_client.SlaveRegistration() # SlaveRegistration | 

    try:
        # Create a slave node
        api_instance.create_slave(key, slave_registration)
    except Exception as e:
        print("Exception when calling ServersApi->create_slave: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **key** | **str**| The secret registration key | 
 **slave_registration** | [**SlaveRegistration**](SlaveRegistration.md)|  | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Registration successful |  -  |
**400** | Invalid input |  -  |
**401** | Invalid registration key |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_server_domain**
> delete_server_domain(server_id, domain_id)

Delete a mapped server domain

Deletes a server domain mapping and the domain itself.  Does not delete associated SSLs.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Delete a mapped server domain
        api_instance.delete_server_domain(server_id, domain_id)
    except Exception as e:
        print("Exception when calling ServersApi->delete_server_domain: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 
 **domain_id** | **str**| The id of the domain. | 

### Return type

void (empty response body)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Server domain deleted |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_server_from_group**
> delete_server_from_group(server_id)

Delete server from group

Deletes a server from the server group it is in, if any. Session holder must be an `Owner`, `SuperAdmin`, or `Sysadmin` in the MO.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server

    try:
        # Delete server from group
        api_instance.delete_server_from_group(server_id)
    except Exception as e:
        print("Exception when calling ServersApi->delete_server_from_group: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 

### Return type

void (empty response body)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_server_group**
> delete_server_group(group_id)

Deletes an existing server group

Does not delete servers in the group, but instead simply unlinks those servers from this group. These servers, if any, will end up not being in any group after this call succeeds. Session holder must be an `Owner`, `SuperAdmin`, or `Sysadmin` in the MO.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    group_id = 'group_id_example' # str | The id of the server group.

    try:
        # Deletes an existing server group
        api_instance.delete_server_group(group_id)
    except Exception as e:
        print("Exception when calling ServersApi->delete_server_group: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **group_id** | **str**| The id of the server group. | 

### Return type

void (empty response body)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Server group successfully deleted |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_server_network_interface_ip**
> delete_server_network_interface_ip(server_id, interface, ip)

Delete server network interface secondary IP

Deletes a secondary IP address from the server's network interface. Fails if the IP address is the primary address of the server. Session holder must be an `Owner`, `SuperAdmin`, or `Sysadmin` in the MO.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server
    interface = 'interface_example' # str | The name of the network interface
    ip = 'ip_example' # str | The IP address in quad dot notation

    try:
        # Delete server network interface secondary IP
        api_instance.delete_server_network_interface_ip(server_id, interface, ip)
    except Exception as e:
        print("Exception when calling ServersApi->delete_server_network_interface_ip: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 
 **interface** | **str**| The name of the network interface | 
 **ip** | **str**| The IP address in quad dot notation | 

### Return type

void (empty response body)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_server_primary_ipv6**
> delete_server_primary_ipv6(server_id)

Deletes/unsets the primary IPv6 address for a server.

### Example


```python
import openapi_client
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
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server

    try:
        # Deletes/unsets the primary IPv6 address for a server.
        api_instance.delete_server_primary_ipv6(server_id)
    except Exception as e:
        print("Exception when calling ServersApi->delete_server_primary_ipv6: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | IPv6 address delete |  -  |
**400** | Invalid argument |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_service_setting**
> Outcome delete_service_setting(server_id, setting_kind, setting_key)

Delete a single override setting

Delete a single service setting value

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.outcome import Outcome
from openapi_client.models.setting_kind import SettingKind
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server
    setting_kind = openapi_client.SettingKind() # SettingKind | The type of setting being applied
    setting_key = 'setting_key_example' # str | A key for updating an existing setting, some known values are - hard_delete_after_secs - letsencrypt_enabled - myhostname - org_websites_same_server - screenshot_driver_pool_size - screenshot_interval - sged_smtp - smtp_smart_host - website_backup

    try:
        # Delete a single override setting
        api_response = api_instance.delete_service_setting(server_id, setting_kind, setting_key)
        print("The response of ServersApi->delete_service_setting:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->delete_service_setting: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 
 **setting_kind** | [**SettingKind**](.md)| The type of setting being applied | 
 **setting_key** | **str**| A key for updating an existing setting, some known values are - hard_delete_after_secs - letsencrypt_enabled - myhostname - org_websites_same_server - screenshot_driver_pool_size - screenshot_interval - sged_smtp - smtp_smart_host - website_backup | 

### Return type

[**Outcome**](Outcome.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**202** | Accepted but not applied |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_slave**
> delete_slave(server_id)

Delete a (slave) server

Removes a given server from the Enhance cluster. The server to be removed may only be a slave server as the master server cannot be removed (the error code `invalid_argument` is returned in such a case). Moreover, the server cannot be deleted if it has any data (such as running/suspended website, emails, etc) on it. Session holder must be an `Owner`, `SuperAdmin`, or `Sysadmin` in the MO.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server

    try:
        # Delete a (slave) server
        api_instance.delete_slave(server_id)
    except Exception as e:
        print("Exception when calling ServersApi->delete_slave: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 

### Return type

void (empty response body)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Deletion successful |  -  |
**400** | Invalid argument |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **enable_fs_quota_limits**
> enable_fs_quota_limits(server_id)

Enable FS quota limits on the server

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server

    try:
        # Enable FS quota limits on the server
        api_instance.enable_fs_quota_limits(server_id)
    except Exception as e:
        print("Exception when calling ServersApi->enable_fs_quota_limits: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 

### Return type

void (empty response body)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | FS quota limits enabled |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_appcd_screenshot_config**
> ScreenshotConfig get_appcd_screenshot_config(server_id)

Get the screenshot config of the running appcd

Returns the screenshot config of the running appcd instance on this server.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.screenshot_config import ScreenshotConfig
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server

    try:
        # Get the screenshot config of the running appcd
        api_response = api_instance.get_appcd_screenshot_config(server_id)
        print("The response of ServersApi->get_appcd_screenshot_config:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->get_appcd_screenshot_config: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 

### Return type

[**ScreenshotConfig**](ScreenshotConfig.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Query successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_appcd_version**
> str get_appcd_version(server_id)

Get the version of the running appcd

Returns the version of the running appcd instance on this server.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server

    try:
        # Get the version of the running appcd
        api_response = api_instance.get_appcd_version(server_id)
        print("The response of ServersApi->get_appcd_version:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->get_appcd_version: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 

### Return type

**str**

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Query successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_client_ip**
> str get_client_ip()

Reflect back the IP of the API consumer

### Example


```python
import openapi_client
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
    api_instance = openapi_client.ServersApi(api_client)

    try:
        # Reflect back the IP of the API consumer
        api_response = api_instance.get_client_ip()
        print("The response of ServersApi->get_client_ip:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->get_client_ip: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

**str**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_control_panel_role_info**
> ControlRoleInfo get_control_panel_role_info()

Get master server control panel role info

Returns information about the control panel role. This includes generic information about the role as well as each control panel service (such as authd). Session holder must be an `Owner`, `SuperAdmin`, or `Sysadmin` in the MO.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.control_role_info import ControlRoleInfo
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)

    try:
        # Get master server control panel role info
        api_response = api_instance.get_control_panel_role_info()
        print("The response of ServersApi->get_control_panel_role_info:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->get_control_panel_role_info: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**ControlRoleInfo**](ControlRoleInfo.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_database_role_mysql_kind**
> MysqlKind get_database_role_mysql_kind(server_id, mysql_kind=mysql_kind)

Gets the MySQL kind for a given server.

### Example


```python
import openapi_client
from openapi_client.models.mysql_kind import MysqlKind
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
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server
    mysql_kind = openapi_client.MysqlKind() # MysqlKind |  (optional)

    try:
        # Gets the MySQL kind for a given server.
        api_response = api_instance.get_database_role_mysql_kind(server_id, mysql_kind=mysql_kind)
        print("The response of ServersApi->get_database_role_mysql_kind:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->get_database_role_mysql_kind: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 
 **mysql_kind** | [**MysqlKind**](.md)|  | [optional] 

### Return type

[**MysqlKind**](MysqlKind.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Role enabled successfully |  -  |
**400** | Invalid argument |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_dns_pool_ips**
> List[str] get_dns_pool_ips()

Get DNS pool IPs

### Example


```python
import openapi_client
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
    api_instance = openapi_client.ServersApi(api_client)

    try:
        # Get DNS pool IPs
        api_response = api_instance.get_dns_pool_ips()
        print("The response of ServersApi->get_dns_pool_ips:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->get_dns_pool_ips: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

**List[str]**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | A list of all DNS server IPs |  -  |
**400** | Invalid argument |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_fs_quota_status**
> FsQuotaStatus get_fs_quota_status(server_id)

Get whether FS quota was enabled on the server

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.fs_quota_status import FsQuotaStatus
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server

    try:
        # Get whether FS quota was enabled on the server
        api_response = api_instance.get_fs_quota_status(server_id)
        print("The response of ServersApi->get_fs_quota_status:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->get_fs_quota_status: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 

### Return type

[**FsQuotaStatus**](FsQuotaStatus.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_httpd_status**
> HttpdStatus get_httpd_status(server_id, role)

Get status of a running httpd server.

`httpd` exposes some server stats through https://httpd.apache.org/docs/2.4/mod/mod_status.html API. Complete response from `httpd` is returned as a string.

### Example


```python
import openapi_client
from openapi_client.models.httpd_status import HttpdStatus
from openapi_client.models.server_role import ServerRole
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
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server
    role = openapi_client.ServerRole() # ServerRole | The role of the server.

    try:
        # Get status of a running httpd server.
        api_response = api_instance.get_httpd_status(server_id, role)
        print("The response of ServersApi->get_httpd_status:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->get_httpd_status: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 
 **role** | [**ServerRole**](.md)| The role of the server. | 

### Return type

[**HttpdStatus**](HttpdStatus.md)

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
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_install_cmd**
> InstallCmd get_install_cmd()

Get slave installation command

Returns the install script that can be used to register more servers in the Enhance cluster. Session holder must be an `Owner`, `SuperAdmin`, or `Sysadmin` in the MO.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.install_cmd import InstallCmd
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)

    try:
        # Get slave installation command
        api_response = api_instance.get_install_cmd()
        print("The response of ServersApi->get_install_cmd:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->get_install_cmd: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**InstallCmd**](InstallCmd.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_mysql_my_cnf**
> str get_mysql_my_cnf(server_id)

Download my.cnf for a given server

### Example


```python
import openapi_client
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
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server

    try:
        # Download my.cnf for a given server
        api_response = api_instance.get_mysql_my_cnf(server_id)
        print("The response of ServersApi->get_mysql_my_cnf:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->get_mysql_my_cnf: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 

### Return type

**str**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | my.cnf content returned |  -  |
**400** | Invalid argument |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_owasp_rules_version**
> OwaspVersion get_owasp_rules_version(server_id)

Get the current and available version of the OWASP rules

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.owasp_version import OwaspVersion
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server

    try:
        # Get the current and available version of the OWASP rules
        api_response = api_instance.get_owasp_rules_version(server_id)
        print("The response of ServersApi->get_owasp_rules_version:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->get_owasp_rules_version: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 

### Return type

[**OwaspVersion**](OwaspVersion.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OWASP version successfully queried |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_registration_key**
> str get_registration_key()

Get slave registration key

Key may be used to install yet more servers in the Enhance cluster. Session holder must be an `Owner`, `SuperAdmin`, or `Sysadmin` in the MO.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)

    try:
        # Get slave registration key
        api_response = api_instance.get_registration_key()
        print("The response of ServersApi->get_registration_key:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->get_registration_key: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

**str**

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_server_disk_usage**
> ServerDiskUsage get_server_disk_usage(server_id)

Get server disk usage

Returns disk usage of all disks on the given server. Session holder must be an `Owner`, `SuperAdmin`, or `Sysadmin` in the MO.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.server_disk_usage import ServerDiskUsage
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server

    try:
        # Get server disk usage
        api_response = api_instance.get_server_disk_usage(server_id)
        print("The response of ServersApi->get_server_disk_usage:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->get_server_disk_usage: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 

### Return type

[**ServerDiskUsage**](ServerDiskUsage.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_server_fpm_settings**
> List[WebsitePhpSettings] get_server_fpm_settings(server_id)

Get php-fpm config for all the websites on a server

Returns a list of php-fpm settings for each website on the server. Settings are queried from the running PHP instance for each website. Session holder must be an `Owner`, `SuperAdmin`, or `Sysadmin` in the MO.

### Example


```python
import openapi_client
from openapi_client.models.website_php_settings import WebsitePhpSettings
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
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server

    try:
        # Get php-fpm config for all the websites on a server
        api_response = api_instance.get_server_fpm_settings(server_id)
        print("The response of ServersApi->get_server_fpm_settings:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->get_server_fpm_settings: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 

### Return type

[**List[WebsitePhpSettings]**](WebsitePhpSettings.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_server_groups**
> ServerGroups get_server_groups()

Returns all server groups

Each group object has a list of ids of the servers that are part of this group. Note that pagination may not be applied so this endpoint always returns all server groups. Session holder must be an `Owner`, `SuperAdmin`, or `Sysadmin` in the MO.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.server_groups import ServerGroups
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)

    try:
        # Returns all server groups
        api_response = api_instance.get_server_groups()
        print("The response of ServersApi->get_server_groups:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->get_server_groups: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**ServerGroups**](ServerGroups.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Query successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_server_hostname_website**
> ServerHostnameWebsite get_server_hostname_website(server_id)

Get domains which are mapped to a server

Returns the server hostname website for this server

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.server_hostname_website import ServerHostnameWebsite
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server

    try:
        # Get domains which are mapped to a server
        api_response = api_instance.get_server_hostname_website(server_id)
        print("The response of ServersApi->get_server_hostname_website:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->get_server_hostname_website: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 

### Return type

[**ServerHostnameWebsite**](ServerHostnameWebsite.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Query successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_server_info**
> ServerInfo get_server_info(server_id)

Get server info

Returns info about the selected server, if it exists. Session holder must be an `Owner`, `SuperAdmin`, or `Sysadmin` in the MO.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.server_info import ServerInfo
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server

    try:
        # Get server info
        api_response = api_instance.get_server_info(server_id)
        print("The response of ServersApi->get_server_info:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->get_server_info: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 

### Return type

[**ServerInfo**](ServerInfo.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Query successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_server_iowait**
> ServerIowait get_server_iowait(server_id)

Get server iowait

Returns system iowait of the given server in number of elapsed seconds since power-on. Session holder must be an `Owner`, `SuperAdmin`, or `Sysadmin` in the MO.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.server_iowait import ServerIowait
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server

    try:
        # Get server iowait
        api_response = api_instance.get_server_iowait(server_id)
        print("The response of ServersApi->get_server_iowait:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->get_server_iowait: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 

### Return type

[**ServerIowait**](ServerIowait.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_server_load**
> ServerLoad get_server_load(server_id)

Get server system load

Returns one minute system load of the given server. Session holder must be an `Owner`, `SuperAdmin`, or `Sysadmin` in the MO.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.server_load import ServerLoad
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server

    try:
        # Get server system load
        api_response = api_instance.get_server_load(server_id)
        print("The response of ServersApi->get_server_load:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->get_server_load: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 

### Return type

[**ServerLoad**](ServerLoad.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_server_memory_usage**
> ServerMemoryUsage get_server_memory_usage(server_id)

Get server memory usage

Returns RAM and swap space usage on the given server. Session holder must be an `Owner`, `SuperAdmin`, or `Sysadmin` in the MO.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.server_memory_usage import ServerMemoryUsage
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server

    try:
        # Get server memory usage
        api_response = api_instance.get_server_memory_usage(server_id)
        print("The response of ServersApi->get_server_memory_usage:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->get_server_memory_usage: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 

### Return type

[**ServerMemoryUsage**](ServerMemoryUsage.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_server_mod_security_config**
> str get_server_mod_security_config(server_id)

Get mod security config

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server

    try:
        # Get mod security config
        api_response = api_instance.get_server_mod_security_config(server_id)
        print("The response of ServersApi->get_server_mod_security_config:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->get_server_mod_security_config: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 

### Return type

**str**

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | mod_security config successfully queried |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_server_mod_security_status**
> ModSecStatus get_server_mod_security_status(server_id)

Get mod security status for a server

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.mod_sec_status import ModSecStatus
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server

    try:
        # Get mod security status for a server
        api_response = api_instance.get_server_mod_security_status(server_id)
        print("The response of ServersApi->get_server_mod_security_status:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->get_server_mod_security_status: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 

### Return type

[**ModSecStatus**](ModSecStatus.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | mod_security status successfully queried |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_server_network_interfaces**
> ServerNetworkInterfaces get_server_network_interfaces(server_id)

Get server network interfaces

Returns the network interfaces of the given server. Session holder must be an `Owner`, `SuperAdmin`, or `Sysadmin` in the MO.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.server_network_interfaces import ServerNetworkInterfaces
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server

    try:
        # Get server network interfaces
        api_response = api_instance.get_server_network_interfaces(server_id)
        print("The response of ServersApi->get_server_network_interfaces:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->get_server_network_interfaces: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 

### Return type

[**ServerNetworkInterfaces**](ServerNetworkInterfaces.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_server_network_stats**
> ServerNetworkStats get_server_network_stats(server_id)

Get server network stats

Returns network stats of the given server. Session holder must be an `Owner`, `SuperAdmin`, or `Sysadmin` in the MO.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.server_network_stats import ServerNetworkStats
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server

    try:
        # Get server network stats
        api_response = api_instance.get_server_network_stats(server_id)
        print("The response of ServersApi->get_server_network_stats:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->get_server_network_stats: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 

### Return type

[**ServerNetworkStats**](ServerNetworkStats.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_server_role**
> GetServerRole200Response get_server_role(server_id, role)

Get server role info

Returns information about the given role on the server. This includes generic information about the role as well as each service in the role. Session holder must be an `Owner`, `SuperAdmin`, or `Sysadmin` in the MO.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.get_server_role200_response import GetServerRole200Response
from openapi_client.models.server_role import ServerRole
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server
    role = openapi_client.ServerRole() # ServerRole | The role of the server.

    try:
        # Get server role info
        api_response = api_instance.get_server_role(server_id, role)
        print("The response of ServersApi->get_server_role:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->get_server_role: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 
 **role** | [**ServerRole**](.md)| The role of the server. | 

### Return type

[**GetServerRole200Response**](GetServerRole200Response.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_server_roles**
> RolesInfo get_server_roles(server_id)

Get server roles info

Returns all configured roles of the given server. This includes generic information about the role as well as each service in the role. Session holder must be an `Owner`, `SuperAdmin`, or `Sysadmin` in the MO.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.roles_info import RolesInfo
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server

    try:
        # Get server roles info
        api_response = api_instance.get_server_roles(server_id)
        print("The response of ServersApi->get_server_roles:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->get_server_roles: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 

### Return type

[**RolesInfo**](RolesInfo.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_server_stats**
> ServerStatsFullListing get_server_stats(server_id, start=start, end=end)

Get Server stats

Returns server stats between the optional start and end date. Defaults to last 24 hours. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.server_stats_full_listing import ServerStatsFullListing
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
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server
    start = '2013-10-20T19:20:30+01:00' # datetime | Start datetime UTC. (optional)
    end = '2013-10-20T19:20:30+01:00' # datetime | End datetime UTC. (optional)

    try:
        # Get Server stats
        api_response = api_instance.get_server_stats(server_id, start=start, end=end)
        print("The response of ServersApi->get_server_stats:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->get_server_stats: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 
 **start** | **datetime**| Start datetime UTC. | [optional] 
 **end** | **datetime**| End datetime UTC. | [optional] 

### Return type

[**ServerStatsFullListing**](ServerStatsFullListing.md)

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

# **get_server_status**
> ServerStatus get_server_status(server_id)

Get server status

Returns system (online or offline) status of the given server. Session holder must be an `Owner`, `SuperAdmin`, or `Sysadmin` in the MO.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.server_status import ServerStatus
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server

    try:
        # Get server status
        api_response = api_instance.get_server_status(server_id)
        print("The response of ServersApi->get_server_status:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->get_server_status: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 

### Return type

[**ServerStatus**](ServerStatus.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_server_uptime**
> ServerUptime get_server_uptime(server_id)

Get server uptime in seconds

Returns system iowait of the given server. Session holder must be an `Owner`, `SuperAdmin`, or `Sysadmin` in the MO.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.server_uptime import ServerUptime
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server

    try:
        # Get server uptime in seconds
        api_response = api_instance.get_server_uptime(server_id)
        print("The response of ServersApi->get_server_uptime:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->get_server_uptime: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 

### Return type

[**ServerUptime**](ServerUptime.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_servers**
> ServersListing get_servers(offset=offset, limit=limit, sort_order=sort_order, sort_by=sort_by)

Get installed servers

Returns a list of all servers in this Enhance cluster (including the master server and all slaves). The result set of servers may optionally be sorted, paginated, as well as grouped by a server's group id. If not grouped, the returned items are a flat list of server resource objects, whereas if grouped, the returned items are an object (map) of list of servers mapped to their group ids. Grouping is applied after pagination and sorting, and in the latter case the servers within one group will be sorted. Therefore, if paginated, the last group in items, i.e. the group on the \"border\", may not contain all servers belonging to that group if the given limit was such as would be exceeded if all its servers were included. In such a case, the remaining servers of the group are returned in the next batch. Example: Assume servers server1, server2, server3, server4, server5 and groups group1, group2, where group1 contains server1 and group2 contains server2, server3, and server4 is not in a group. If the request specifies an offset of 0 and a limit of 2, then the returned structure may be as follows: ```json {     items: {         group1_id: [             server1,         ],         group2_id: [             server2,         ],     },     total: 4 } ``` Then, in the next request, if offset is changed to 2, the returned items may be: ```json {     items: {         group2_id: [             server3,         ],         \"ungrouped\": [             server4         ],     },     total: 4 } ``` Containing the rest of group2's servers as well as the ungrouped servers. Session holder must be an `Owner`, `SuperAdmin`, or `Sysadmin` in the MO.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.servers_listing import ServersListing
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    offset = 56 # int | The offset from which to return items. (optional)
    limit = 56 # int | The maximum number of items to return. (optional)
    sort_order = 'sort_order_example' # str | The direction in which to sort. Possible values are 'asc' and 'desc', defaulting to 'asc'. (optional)
    sort_by = 'sort_by_example' # str | The field by which to sort. (optional)

    try:
        # Get installed servers
        api_response = api_instance.get_servers(offset=offset, limit=limit, sort_order=sort_order, sort_by=sort_by)
        print("The response of ServersApi->get_servers:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->get_servers: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **offset** | **int**| The offset from which to return items. | [optional] 
 **limit** | **int**| The maximum number of items to return. | [optional] 
 **sort_order** | **str**| The direction in which to sort. Possible values are &#39;asc&#39; and &#39;desc&#39;, defaulting to &#39;asc&#39;. | [optional] 
 **sort_by** | **str**| The field by which to sort. | [optional] 

### Return type

[**ServersListing**](ServersListing.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Query successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_service_setting**
> object get_service_setting(server_id, setting_kind)

Get the value for a particular setting

Returns the value for a particular setting as a JSON object

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.setting_kind import SettingKind
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server
    setting_kind = openapi_client.SettingKind() # SettingKind | The type of setting being applied

    try:
        # Get the value for a particular setting
        api_response = api_instance.get_service_setting(server_id, setting_kind)
        print("The response of ServersApi->get_service_setting:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->get_service_setting: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 
 **setting_kind** | [**SettingKind**](.md)| The type of setting being applied | 

### Return type

**object**

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_system_package_update_info**
> UpgradableSystemPackage get_system_package_update_info(server_id, system_package_name=system_package_name)

Returns a map of upgradable packages.

Map of upgradable system packages is returned along with latest Version if the package update is available.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.system_package_name import SystemPackageName
from openapi_client.models.upgradable_system_package import UpgradableSystemPackage
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server
    system_package_name = openapi_client.SystemPackageName() # SystemPackageName |  (optional)

    try:
        # Returns a map of upgradable packages.
        api_response = api_instance.get_system_package_update_info(server_id, system_package_name=system_package_name)
        print("The response of ServersApi->get_system_package_update_info:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->get_system_package_update_info: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 
 **system_package_name** | [**SystemPackageName**](.md)|  | [optional] 

### Return type

[**UpgradableSystemPackage**](UpgradableSystemPackage.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of upgradable packages |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_webserver_kind**
> WebserverKind get_webserver_kind(server_id)

Get web server

Fetches the current web server kind for this server.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.webserver_kind import WebserverKind
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server

    try:
        # Get web server
        api_response = api_instance.get_webserver_kind(server_id)
        print("The response of ServersApi->get_webserver_kind:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->get_webserver_kind: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 

### Return type

[**WebserverKind**](WebserverKind.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_website_fpm_settings**
> PhpIni get_website_fpm_settings(server_id, website_id)

Get php-fpm config for the specified website

Returns a list of php-fpm settings for specified website on the server. Settings are queried from the running PHP instance for each website. Session holder must be an `Owner`, `SuperAdmin`, or `Sysadmin` in the MO.

### Example


```python
import openapi_client
from openapi_client.models.php_ini import PhpIni
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
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server
    website_id = 'website_id_example' # str | The id of the website.

    try:
        # Get php-fpm config for the specified website
        api_response = api_instance.get_website_fpm_settings(server_id, website_id)
        print("The response of ServersApi->get_website_fpm_settings:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->get_website_fpm_settings: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 
 **website_id** | **str**| The id of the website. | 

### Return type

[**PhpIni**](PhpIni.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **init_all_servers**
> init_all_servers()

Attempts to initialize all roles

Attempts to initialize roles and other resources on all servers. Manual initialization (via this endpoint) shouldn't be necessary as usually even if some slave server is unavailable to `orchd` in the beginning, `orchd` periodically retries the role initialization. However, if something needs a manual intervention, then calling this endpoint is helpful to identify further issue and hasten up the full availability of `orchd`. This endpoint can be called multiple times and it will initialize resources at most once. Once this endpoint returns 200, there is no point in calling it again. Session holder must be an `Owner`, `SuperAdmin`, or `Sysadmin` in the MO.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)

    try:
        # Attempts to initialize all roles
        api_instance.init_all_servers()
    except Exception as e:
        print("Exception when calling ServersApi->init_all_servers: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Everything is initialized |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **install_database_role**
> install_database_role(server_id, mysql_kind=mysql_kind)

Enables the database role on a given ServerUuid

### Example


```python
import openapi_client
from openapi_client.models.mysql_kind import MysqlKind
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
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server
    mysql_kind = openapi_client.MysqlKind() # MysqlKind |  (optional)

    try:
        # Enables the database role on a given ServerUuid
        api_instance.install_database_role(server_id, mysql_kind=mysql_kind)
    except Exception as e:
        print("Exception when calling ServersApi->install_database_role: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 
 **mysql_kind** | [**MysqlKind**](.md)|  | [optional] 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Role enabled successfully |  -  |
**400** | Invalid argument |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **install_server_role**
> install_server_role(server_id, role, new_backup_role=new_backup_role)

Install server role

Installs a role on the server. The backup role takes additional parameters, but all other roles take no parameters. The block device size is optional and defaults to 100 GiB if not set. In this case, the mount point has to be the absolute path where the backup volume should be mounted. If there is already a valid btrfs backup volume mounted at this path, besides installing the `bkupd` service, this is a noop. In the case of an existing mount point, it is verified that it has at least the block device size bytes available. The block device is an absolute path that may or may not exist. If it exists, the block device size is used to verify if the device has at least the specified space available, if it doesn't exist, a loopback device is created with the this size. Session holder must be an `Owner`, `SuperAdmin`, or `Sysadmin` in the MO.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.new_backup_role import NewBackupRole
from openapi_client.models.server_role import ServerRole
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server
    role = openapi_client.ServerRole() # ServerRole | The role of the server.
    new_backup_role = openapi_client.NewBackupRole() # NewBackupRole | Information for the backup role. (optional)

    try:
        # Install server role
        api_instance.install_server_role(server_id, role, new_backup_role=new_backup_role)
    except Exception as e:
        print("Exception when calling ServersApi->install_server_role: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 
 **role** | [**ServerRole**](.md)| The role of the server. | 
 **new_backup_role** | [**NewBackupRole**](NewBackupRole.md)| Information for the backup role. | [optional] 

### Return type

void (empty response body)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **reset_server_mod_security_config**
> reset_server_mod_security_config(server_id)

Delete custom mod_security config and reset to default

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server

    try:
        # Delete custom mod_security config and reset to default
        api_instance.reset_server_mod_security_config(server_id)
    except Exception as e:
        print("Exception when calling ServersApi->reset_server_mod_security_config: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 

### Return type

void (empty response body)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | mod_security config customisations deleted |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **reset_web_server_config**
> reset_web_server_config(server_id)

Reset the config for the web server to default.

Will reset the config for the running web server to \"known good\" defaults.  Currently only available for LiteSpeed.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server

    try:
        # Reset the config for the web server to default.
        api_instance.reset_web_server_config(server_id)
    except Exception as e:
        print("Exception when calling ServersApi->reset_web_server_config: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 

### Return type

void (empty response body)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Web server config reset |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **restart_mysql**
> restart_mysql(server_id)

Restart MySQL gracefully

### Example


```python
import openapi_client
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
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server

    try:
        # Restart MySQL gracefully
        api_instance.restart_mysql(server_id)
    except Exception as e:
        print("Exception when calling ServersApi->restart_mysql: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Mysql restart initiated |  -  |
**400** | Invalid argument |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **save_mysql_my_cnf**
> save_mysql_my_cnf(server_id, body)

Save a new my.cnf

### Example


```python
import openapi_client
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
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server
    body = 'body_example' # str | New my.cnf to be applied

    try:
        # Save a new my.cnf
        api_instance.save_mysql_my_cnf(server_id, body)
    except Exception as e:
        print("Exception when calling ServersApi->save_mysql_my_cnf: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 
 **body** | **str**| New my.cnf to be applied | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | My.cnf updated |  -  |
**400** | Invalid argument |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_lite_speed_admin_password**
> set_lite_speed_admin_password(server_id, body)

Set a new LiteSpeed admin password.

Will reset the LiteSpeed or OpenLiteSpeed admin password.  The username is always \"admin\".

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server
    body = 'body_example' # str | 

    try:
        # Set a new LiteSpeed admin password.
        api_instance.set_lite_speed_admin_password(server_id, body)
    except Exception as e:
        print("Exception when calling ServersApi->set_lite_speed_admin_password: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 
 **body** | **str**|  | 

### Return type

void (empty response body)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | LiteSpeed password has been reset |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_server_decommissioned**
> set_server_decommissioned(server_id)

Set server to decommissioned

If a server was decommissioned outside of Enhance, set its status to decommissioned.  This will remove the server from any status checks, will prevent website placement and will enable websites to be moved from it to another server using backups if available.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server

    try:
        # Set server to decommissioned
        api_instance.set_server_decommissioned(server_id)
    except Exception as e:
        print("Exception when calling ServersApi->set_server_decommissioned: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 

### Return type

void (empty response body)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_server_mod_security_config**
> set_server_mod_security_config(server_id, body)

Set mod security config

This config is included in the web server config when mod_security is enabled.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server
    body = 'body_example' # str | 

    try:
        # Set mod security config
        api_instance.set_server_mod_security_config(server_id, body)
    except Exception as e:
        print("Exception when calling ServersApi->set_server_mod_security_config: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 
 **body** | **str**|  | 

### Return type

void (empty response body)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | mod_security config updated |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_server_mod_security_status**
> set_server_mod_security_status(server_id, mod_sec_status)

Set mod security status for a server

If enabled, all websites on this server by default will have mod security enabled, unless explicitly disabled.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.mod_sec_status import ModSecStatus
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server
    mod_sec_status = openapi_client.ModSecStatus() # ModSecStatus | 

    try:
        # Set mod security status for a server
        api_instance.set_server_mod_security_status(server_id, mod_sec_status)
    except Exception as e:
        print("Exception when calling ServersApi->set_server_mod_security_status: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 
 **mod_sec_status** | [**ModSecStatus**](ModSecStatus.md)|  | 

### Return type

void (empty response body)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | mod_security status updated |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_server_status**
> set_server_status(server_id, set_server_status)

Set the status of one server.

Set the status of one server by rebooting it for example.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.set_server_status import SetServerStatus
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server
    set_server_status = openapi_client.SetServerStatus() # SetServerStatus | The action to be taken for a specific server. When rebooting a server if the reboot is graceful before the server itself is rebooted all the installed services which make use of an underlying daemon will be asked to shutdown the daemon in question (such as mysqld, httpd or pdns). If the reboot is forced the underlying daemon stop will be forced as well. Note: Primary server reboots are never allowed. The server reboot will only happens 1 minute after the request is sent.

    try:
        # Set the status of one server.
        api_instance.set_server_status(server_id, set_server_status)
    except Exception as e:
        print("Exception when calling ServersApi->set_server_status: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 
 **set_server_status** | [**SetServerStatus**](SetServerStatus.md)| The action to be taken for a specific server. When rebooting a server if the reboot is graceful before the server itself is rebooted all the installed services which make use of an underlying daemon will be asked to shutdown the daemon in question (such as mysqld, httpd or pdns). If the reboot is forced the underlying daemon stop will be forced as well. Note: Primary server reboots are never allowed. The server reboot will only happens 1 minute after the request is sent. | 

### Return type

void (empty response body)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Server status successfully set |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_service_setting**
> Outcome set_service_setting(server_id, setting_kind, setting_key, service_setting_value)

Set a single service setting

Set or replace a single service level override setting

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.outcome import Outcome
from openapi_client.models.service_setting_value import ServiceSettingValue
from openapi_client.models.setting_kind import SettingKind
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server
    setting_kind = openapi_client.SettingKind() # SettingKind | The type of setting being applied
    setting_key = 'setting_key_example' # str | A key for updating an existing setting, some known values are - hard_delete_after_secs - letsencrypt_enabled - myhostname - org_websites_same_server - screenshot_driver_pool_size - screenshot_interval - sged_smtp - smtp_smart_host - website_backup
    service_setting_value = openapi_client.ServiceSettingValue() # ServiceSettingValue | 

    try:
        # Set a single service setting
        api_response = api_instance.set_service_setting(server_id, setting_kind, setting_key, service_setting_value)
        print("The response of ServersApi->set_service_setting:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->set_service_setting: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 
 **setting_kind** | [**SettingKind**](.md)| The type of setting being applied | 
 **setting_key** | **str**| A key for updating an existing setting, some known values are - hard_delete_after_secs - letsencrypt_enabled - myhostname - org_websites_same_server - screenshot_driver_pool_size - screenshot_interval - sged_smtp - smtp_smart_host - website_backup | 
 **service_setting_value** | [**ServiceSettingValue**](ServiceSettingValue.md)|  | 

### Return type

[**Outcome**](Outcome.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**202** | Accepted but not applied |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_service_status**
> set_service_status(server_id, service_id, set_service_status)

Set the status of one service installed in the server specified.

Set the status of one service by restarting it for example.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.set_service_status import SetServiceStatus
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server
    service_id = 'service_id_example' # str | The UUID of the service
    set_service_status = openapi_client.SetServiceStatus() # SetServiceStatus | The action to be taken for a specific service.

    try:
        # Set the status of one service installed in the server specified.
        api_instance.set_service_status(server_id, service_id, set_service_status)
    except Exception as e:
        print("Exception when calling ServersApi->set_service_status: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 
 **service_id** | **str**| The UUID of the service | 
 **set_service_status** | [**SetServiceStatus**](SetServiceStatus.md)| The action to be taken for a specific service. | 

### Return type

void (empty response body)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Service status successfully set |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_webserver_kind**
> set_webserver_kind(server_id, set_webserver_kind)

Set the web server kind for one server.

Changes the web server kind for this server.  This will rebuild any application containers if required.  It may be a long running operation.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.set_webserver_kind import SetWebserverKind
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server
    set_webserver_kind = openapi_client.SetWebserverKind() # SetWebserverKind | 

    try:
        # Set the web server kind for one server.
        api_instance.set_webserver_kind(server_id, set_webserver_kind)
    except Exception as e:
        print("Exception when calling ServersApi->set_webserver_kind: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 
 **set_webserver_kind** | [**SetWebserverKind**](SetWebserverKind.md)|  | 

### Return type

void (empty response body)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Web server kind successfully set |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **uninstall_server_role**
> uninstall_server_role(server_id, role)

Uninstall a server role

Uninstalls role from server, if role has no websites assigned to it. If the role to be uninstalled is the control panel application role, the request returns an error, since this role may only be disabled but not uninstalled (since it is required to serve the control panel). Session holder must be an `Owner`, `SuperAdmin`, or `Sysadmin` in the MO.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.server_role import ServerRole
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server
    role = openapi_client.ServerRole() # ServerRole | The role of the server.

    try:
        # Uninstall a server role
        api_instance.uninstall_server_role(server_id, role)
    except Exception as e:
        print("Exception when calling ServersApi->uninstall_server_role: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 
 **role** | [**ServerRole**](.md)| The role of the server. | 

### Return type

void (empty response body)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Successful |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_appcd_screenshot_config**
> update_appcd_screenshot_config(server_id, screenshot_config_update)

Update the screenshot config of the running appcd

Update the screenshot config of the running appcd instance on this server.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.screenshot_config_update import ScreenshotConfigUpdate
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server
    screenshot_config_update = openapi_client.ScreenshotConfigUpdate() # ScreenshotConfigUpdate | 

    try:
        # Update the screenshot config of the running appcd
        api_instance.update_appcd_screenshot_config(server_id, screenshot_config_update)
    except Exception as e:
        print("Exception when calling ServersApi->update_appcd_screenshot_config: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 
 **screenshot_config_update** | [**ScreenshotConfigUpdate**](ScreenshotConfigUpdate.md)|  | 

### Return type

void (empty response body)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Query successful |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_owasp_rules**
> update_owasp_rules(server_id)

Upgrade OWASP rules

Will update the owasp rules to the latest version.  If the current version is the latest, it will be reinstalled.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server

    try:
        # Upgrade OWASP rules
        api_instance.update_owasp_rules(server_id)
    except Exception as e:
        print("Exception when calling ServersApi->update_owasp_rules: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 

### Return type

void (empty response body)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OWASP rules updated |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_server_group**
> update_server_group(group_id, server_group_update)

Updates an existing server group's name

Session holder must be an `Owner`, `SuperAdmin`, or `Sysadmin` in the MO.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.server_group_update import ServerGroupUpdate
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    group_id = 'group_id_example' # str | The id of the server group.
    server_group_update = openapi_client.ServerGroupUpdate() # ServerGroupUpdate | Server group info.

    try:
        # Updates an existing server group's name
        api_instance.update_server_group(group_id, server_group_update)
    except Exception as e:
        print("Exception when calling ServersApi->update_server_group: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **group_id** | **str**| The id of the server group. | 
 **server_group_update** | [**ServerGroupUpdate**](ServerGroupUpdate.md)| Server group info. | 

### Return type

void (empty response body)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Server group successfully updated |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_server_primary_ip**
> update_server_primary_ip(server_id, body)

Updates the primary IP of the server in the database and in-memory metadata. This operation will not affect the IP used for service communication until the next restart of orchd. The new IP will be used for creation of new resources such as websites on this server but existing websites will not have their IP changed.

### Example


```python
import openapi_client
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
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server
    body = 'body_example' # str | 

    try:
        # Updates the primary IP of the server in the database and in-memory metadata. This operation will not affect the IP used for service communication until the next restart of orchd. The new IP will be used for creation of new resources such as websites on this server but existing websites will not have their IP changed.
        api_instance.update_server_primary_ip(server_id, body)
    except Exception as e:
        print("Exception when calling ServersApi->update_server_primary_ip: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 
 **body** | **str**|  | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Update successful |  -  |
**400** | Invalid argument |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_server_primary_ipv6**
> update_server_primary_ipv6(server_id, body)

Updates or sets the primary ipv6 address of the server.  This endpoint will not change existing websites' DNS but the new record will be applied to all future zones.

### Example


```python
import openapi_client
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
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server
    body = 'body_example' # str | 

    try:
        # Updates or sets the primary ipv6 address of the server.  This endpoint will not change existing websites' DNS but the new record will be applied to all future zones.
        api_instance.update_server_primary_ipv6(server_id, body)
    except Exception as e:
        print("Exception when calling ServersApi->update_server_primary_ipv6: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 
 **body** | **str**|  | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Update successful |  -  |
**400** | Invalid argument |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_server_role**
> update_server_role(server_id, role, update_server_role_request)

Update server role

Updates role and role state. A role, if activated on a server, may be in a state of enabled or disabled. If enabled, it means that new resources (e.g. websites for the application role) may be installed on the server, but if it's disabled, existing resources (e.g. websites) are kept but no new resources may be added. Session holder must be an `Owner`, `SuperAdmin`, or `Sysadmin` in the MO.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.server_role import ServerRole
from openapi_client.models.update_server_role_request import UpdateServerRoleRequest
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server
    role = openapi_client.ServerRole() # ServerRole | The role of the server.
    update_server_role_request = openapi_client.UpdateServerRoleRequest() # UpdateServerRoleRequest | Info for updating the server role.

    try:
        # Update server role
        api_instance.update_server_role(server_id, role, update_server_role_request)
    except Exception as e:
        print("Exception when calling ServersApi->update_server_role: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 
 **role** | [**ServerRole**](.md)| The role of the server. | 
 **update_server_role_request** | [**UpdateServerRoleRequest**](UpdateServerRoleRequest.md)| Info for updating the server role. | 

### Return type

void (empty response body)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_service**
> update_service(server_id, service_id)

Special endpoint to update a particular stopped service to its latest version.

This endpoint should not be used to for updates in general. Useful to update/recover from a broken/stopped service from previous update. NOTE: if service is already running, no changes are made.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server
    service_id = 'service_id_example' # str | The UUID of the service

    try:
        # Special endpoint to update a particular stopped service to its latest version.
        api_instance.update_service(server_id, service_id)
    except Exception as e:
        print("Exception when calling ServersApi->update_service: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 
 **service_id** | **str**| The UUID of the service | 

### Return type

void (empty response body)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Service updated successfully |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_system_package**
> update_system_package(server_id, system_package, system_package_name=system_package_name)

Updates a system package to its latest version.

Can only update installed package to its latest version.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.system_package import SystemPackage
from openapi_client.models.system_package_name import SystemPackageName
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ServersApi(api_client)
    server_id = 'server_id_example' # str | The UUID of the server
    system_package = openapi_client.SystemPackage() # SystemPackage | Package to be updated.
    system_package_name = openapi_client.SystemPackageName() # SystemPackageName |  (optional)

    try:
        # Updates a system package to its latest version.
        api_instance.update_system_package(server_id, system_package, system_package_name=system_package_name)
    except Exception as e:
        print("Exception when calling ServersApi->update_system_package: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **str**| The UUID of the server | 
 **system_package** | [**SystemPackage**](SystemPackage.md)| Package to be updated. | 
 **system_package_name** | [**SystemPackageName**](.md)|  | [optional] 

### Return type

void (empty response body)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Package Updated |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **validate_registration_key**
> ValidationResult validate_registration_key(key)

Validate slave registration key

Session holder must be an `Owner`, `SuperAdmin`, or `Sysadmin` in the MO.

### Example


```python
import openapi_client
from openapi_client.models.validation_result import ValidationResult
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
    api_instance = openapi_client.ServersApi(api_client)
    key = 'key_example' # str | The secret registration key

    try:
        # Validate slave registration key
        api_response = api_instance.validate_registration_key(key)
        print("The response of ServersApi->validate_registration_key:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServersApi->validate_registration_key: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **key** | **str**| The secret registration key | 

### Return type

[**ValidationResult**](ValidationResult.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Master org has been set up |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

