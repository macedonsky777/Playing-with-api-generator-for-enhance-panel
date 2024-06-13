# openapi_client.WebsitesApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_domain_nginx_fast_cgi_excluded_path**](WebsitesApi.md#add_domain_nginx_fast_cgi_excluded_path) | **POST** /v2/domains/{domain_id}/nginx_fastcgi_excluded_paths | Add Nginx FastCGI excluded path
[**authorize_website_ssh_key**](WebsitesApi.md#authorize_website_ssh_key) | **POST** /orgs/{org_id}/websites/{website_id}/ssh/keys | Authorize a new SSH key.
[**authorize_website_ssh_password**](WebsitesApi.md#authorize_website_ssh_password) | **POST** /orgs/{org_id}/websites/{website_id}/ssh/password | Authorize a new SSH password for website.
[**clear_domain_nginx_fast_cgi**](WebsitesApi.md#clear_domain_nginx_fast_cgi) | **DELETE** /v2/domains/{domain_id}/nginx_fastcgi | Clear FastCGI cache for domain
[**clone_website**](WebsitesApi.md#clone_website) | **POST** /orgs/{org_id}/websites/clone | Clone website or push live
[**create_ftp_user**](WebsitesApi.md#create_ftp_user) | **POST** /orgs/{org_id}/websites/{website_id}/ftp/users | Creates a new FTP user for a given website
[**create_preview_domain**](WebsitesApi.md#create_preview_domain) | **POST** /orgs/{org_id}/websites/{website_id}/preview | Create a preview domain
[**create_website**](WebsitesApi.md#create_website) | **POST** /orgs/{org_id}/websites | Create a new website or clone an existing one.
[**create_website_domain_letsencrypt_certs**](WebsitesApi.md#create_website_domain_letsencrypt_certs) | **POST** /v2/domains/{domain_id}/letsencrypt | Generate and setup letsencrypt ssl certificates for website&#39;s domain
[**create_website_mail_domain_letsencrypt_certs**](WebsitesApi.md#create_website_mail_domain_letsencrypt_certs) | **POST** /v2/domains/{domain_id}/letsencrypt_mail | Generate and setup letsencrypt ssl certificates for website&#39;s domain with mail. prefix.
[**create_website_mapped_domain**](WebsitesApi.md#create_website_mapped_domain) | **POST** /orgs/{org_id}/websites/{website_id}/domains | Create website mapped domain
[**create_website_my_sqldb**](WebsitesApi.md#create_website_my_sqldb) | **POST** /orgs/{org_id}/websites/{website_id}/mysql-dbs | Create a MySQL database for website
[**delete_domain_nginx_fast_cgi_excluded_path**](WebsitesApi.md#delete_domain_nginx_fast_cgi_excluded_path) | **DELETE** /v2/domains/{domain_id}/nginx_fastcgi_excluded_paths | Delete Nginx FastCGI excluded path
[**delete_domain_webserver_rewrite**](WebsitesApi.md#delete_domain_webserver_rewrite) | **DELETE** /v2/domains/{domain_id}/webserver_rewrites | Delete web server rewrite
[**delete_ftp_user**](WebsitesApi.md#delete_ftp_user) | **DELETE** /orgs/{org_id}/websites/{website_id}/ftp/users/{user_id} | Deletes given FTP user
[**delete_user_crontab**](WebsitesApi.md#delete_user_crontab) | **DELETE** /orgs/{org_id}/websites/{website_id}/crontab | Delete user&#39;s crontab
[**delete_website**](WebsitesApi.md#delete_website) | **DELETE** /orgs/{org_id}/websites/{website_id} | Delete website
[**delete_website_domain_mapping**](WebsitesApi.md#delete_website_domain_mapping) | **DELETE** /orgs/{org_id}/websites/{website_id}/domains/{domain_id} | Delete website domain mapping
[**delete_website_domain_vhost**](WebsitesApi.md#delete_website_domain_vhost) | **DELETE** /v2/domains/{domain_id}/vhost | Deletes domain&#39;s custom vhost file if any
[**delete_website_setting**](WebsitesApi.md#delete_website_setting) | **DELETE** /orgs/{org_id}/websites/{website_id}/settings/{setting_kind}/{setting_key} | Delete a single override setting
[**delete_websites**](WebsitesApi.md#delete_websites) | **DELETE** /orgs/{org_id}/websites | Delete websites
[**disable_website_php_extension**](WebsitesApi.md#disable_website_php_extension) | **DELETE** /websites/{website_id}/php_extensions | Disable a PHP extension
[**enable_website_php_extension**](WebsitesApi.md#enable_website_php_extension) | **POST** /websites/{website_id}/php_extensions | Enable a PHP extension
[**get_domain_nginx_fast_cgi**](WebsitesApi.md#get_domain_nginx_fast_cgi) | **GET** /v2/domains/{domain_id}/nginx_fastcgi | Get status of Nginx FastCGI enablement
[**get_domain_nginx_fast_cgi_excluded_paths**](WebsitesApi.md#get_domain_nginx_fast_cgi_excluded_paths) | **GET** /v2/domains/{domain_id}/nginx_fastcgi_excluded_paths | Get Nginx FastCGI excluded paths
[**get_domain_webserver_rewrites**](WebsitesApi.md#get_domain_webserver_rewrites) | **GET** /v2/domains/{domain_id}/webserver_rewrites | Get web server rewrites for specified domain
[**get_ftp_users**](WebsitesApi.md#get_ftp_users) | **GET** /orgs/{org_id}/websites/{website_id}/ftp/users | Returns all ftp users data for a given website
[**get_screenshot_timestamp**](WebsitesApi.md#get_screenshot_timestamp) | **GET** /orgs/{org_id}/websites/{website_id}/domains/{domain_id}/screenshot/timestamp | Get last screeshot file&#39;s Timestamp
[**get_site_access_token**](WebsitesApi.md#get_site_access_token) | **POST** /orgs/{org_id}/websites/{website_id}/access-tokens | Get an access token for the given website
[**get_user_crontab**](WebsitesApi.md#get_user_crontab) | **GET** /orgs/{org_id}/websites/{website_id}/crontab | Get user&#39;s crontab
[**get_website**](WebsitesApi.md#get_website) | **GET** /orgs/{org_id}/websites/{website_id} | Get website
[**get_website_available_php_extensions**](WebsitesApi.md#get_website_available_php_extensions) | **GET** /websites/{website_id}/available_php_extensions | Get available PHP extensions for a website
[**get_website_backup_status**](WebsitesApi.md#get_website_backup_status) | **GET** /orgs/{org_id}/websites/{website_id}/status/backup | Get the status of an ongoing website backup operation
[**get_website_cgroup_limits**](WebsitesApi.md#get_website_cgroup_limits) | **GET** /orgs/{org_id}/websites/{website_id}/cgroup_limits | Get the active cgroup limits for a website
[**get_website_clone**](WebsitesApi.md#get_website_clone) | **GET** /orgs/{org_id}/websites/clone/{clone_id} | Get&#39;s detail about a single push live
[**get_website_clone_log**](WebsitesApi.md#get_website_clone_log) | **GET** /orgs/{org_id}/websites/clone/{clone_id}/log | Get the log for a given clone id..
[**get_website_clones**](WebsitesApi.md#get_website_clones) | **GET** /orgs/{org_id}/websites/clone | List website clones for given OrgId
[**get_website_domain_dns_query**](WebsitesApi.md#get_website_domain_dns_query) | **GET** /orgs/{org_id}/websites/{website_id}/domains/{domain_id}/dns-query | Recursively query Dns servers for given domain
[**get_website_domain_mapping**](WebsitesApi.md#get_website_domain_mapping) | **GET** /orgs/{org_id}/websites/{website_id}/domains/{domain_id} | Returns website domain mapping
[**get_website_domain_mapping_dns_status**](WebsitesApi.md#get_website_domain_mapping_dns_status) | **GET** /orgs/{org_id}/websites/{website_id}/domains/{domain_id}/dns-status | Returns website domain mapping DNS status
[**get_website_domain_mappings**](WebsitesApi.md#get_website_domain_mappings) | **GET** /orgs/{org_id}/websites/{website_id}/domains | Get website&#39;s mapped domains
[**get_website_domain_mod_sec_status**](WebsitesApi.md#get_website_domain_mod_sec_status) | **GET** /v2/domains/{domain_id}/modsec_status | Get mod security status for a single domain
[**get_website_domain_ssl_cert**](WebsitesApi.md#get_website_domain_ssl_cert) | **GET** /v2/domains/{domain_id}/ssl | Returns the SSL for this website domain
[**get_website_domain_vhost**](WebsitesApi.md#get_website_domain_vhost) | **GET** /v2/domains/{domain_id}/vhost | Get domain&#39;s custom vhost file, if the file does not exist return empty string 
[**get_website_enabled_php_extensions**](WebsitesApi.md#get_website_enabled_php_extensions) | **GET** /websites/{website_id}/php_extensions | Get enabled PHP extensions
[**get_website_fs_quota_limits**](WebsitesApi.md#get_website_fs_quota_limits) | **GET** /orgs/{org_id}/websites/{website_id}/fs_quota_limits | Get the active FS quoa limits for a website
[**get_website_htaccess_ips_rule**](WebsitesApi.md#get_website_htaccess_ips_rule) | **GET** /orgs/{org_id}/websites/{website_id}/htaccess/ips | Returns current rules of blocked/whitelisted IPs
[**get_website_htaccess_rewrites**](WebsitesApi.md#get_website_htaccess_rewrites) | **GET** /orgs/{org_id}/websites/{website_id}/htaccess | Reads chains of rewrite rules
[**get_website_ioncube_status**](WebsitesApi.md#get_website_ioncube_status) | **GET** /v2/websites/{website_id}/ioncube | Get ioncube status for an existing website
[**get_website_mail_domain_ssl_cert**](WebsitesApi.md#get_website_mail_domain_ssl_cert) | **GET** /v2/domains/{domain_id}/mail_ssl | Returns the SSL for this website domain with the mail.prefix
[**get_website_metrics**](WebsitesApi.md#get_website_metrics) | **GET** /orgs/{org_id}/websites/{website_id}/metrics | Get website metrics
[**get_website_my_sqldbs**](WebsitesApi.md#get_website_my_sqldbs) | **GET** /orgs/{org_id}/websites/{website_id}/mysql-dbs | Get website MySQL databases
[**get_website_redis_state**](WebsitesApi.md#get_website_redis_state) | **GET** /v2/websites/{website_id}/redis | Get redis state for a website
[**get_website_server_domains**](WebsitesApi.md#get_website_server_domains) | **GET** /orgs/{org_id}/websites/{website_id}/server_domains | Fetch website server domains
[**get_website_setting**](WebsitesApi.md#get_website_setting) | **GET** /orgs/{org_id}/websites/{website_id}/settings/{setting_kind} | Get the value for a particular setting
[**get_website_ssh_keys**](WebsitesApi.md#get_website_ssh_keys) | **GET** /orgs/{org_id}/websites/{website_id}/ssh/keys | Get website&#39;s authorized SSH keys
[**get_website_webserver_kind**](WebsitesApi.md#get_website_webserver_kind) | **GET** /v2/websites/{website_id}/webserver_kind | Get web server kind for a given website
[**get_websites**](WebsitesApi.md#get_websites) | **GET** /orgs/{org_id}/websites | Get websites
[**perform_lets_encrypt_preflight_check**](WebsitesApi.md#perform_lets_encrypt_preflight_check) | **POST** /v2/domains/{domain_id}/letsencrypt_preflight | Perform the LetsEncrypt preflight check
[**push_website_live**](WebsitesApi.md#push_website_live) | **POST** /orgs/{org_id}/websites/{website_id}/push-live | Making a staging website live
[**restart_website_php**](WebsitesApi.md#restart_website_php) | **POST** /v2/websites/{website_id}/restart_php | Restart PHP container for a website
[**set_domain_nginx_fast_cgi**](WebsitesApi.md#set_domain_nginx_fast_cgi) | **PUT** /v2/domains/{domain_id}/nginx_fastcgi | Set Nginx FastCGI enablement
[**set_domain_webserver_rewrite**](WebsitesApi.md#set_domain_webserver_rewrite) | **PUT** /v2/domains/{domain_id}/webserver_rewrites | Set web server rewrite to file
[**set_website_cgroup_limits**](WebsitesApi.md#set_website_cgroup_limits) | **PUT** /orgs/{org_id}/websites/{website_id}/cgroup_limits | Set the active cgroup limits for a website (Master org only)
[**set_website_domain_force_ssl**](WebsitesApi.md#set_website_domain_force_ssl) | **PUT** /v2/domains/{domain_id}/ssl/force_ssl | Set \&quot;force ssl\&quot; status for domain mapping
[**set_website_domain_mod_sec_status**](WebsitesApi.md#set_website_domain_mod_sec_status) | **PUT** /v2/domains/{domain_id}/modsec_status | Set mod security status on a single domain
[**set_website_domain_vhost**](WebsitesApi.md#set_website_domain_vhost) | **PUT** /v2/domains/{domain_id}/vhost | Set a custom vhost file
[**set_website_fs_quota_limits**](WebsitesApi.md#set_website_fs_quota_limits) | **PUT** /orgs/{org_id}/websites/{website_id}/fs_quota_limits | Set the active FS quota limits for a website (Master org only)
[**set_website_ioncube_status**](WebsitesApi.md#set_website_ioncube_status) | **PUT** /v2/websites/{website_id}/ioncube | Set ioncube status for an existing website
[**set_website_redis_state**](WebsitesApi.md#set_website_redis_state) | **PUT** /v2/websites/{website_id}/redis | Set Redis state for an existing website
[**set_website_setting**](WebsitesApi.md#set_website_setting) | **PUT** /orgs/{org_id}/websites/{website_id}/settings/{setting_kind}/{setting_key} | Set a single override setting
[**take_screenshot**](WebsitesApi.md#take_screenshot) | **POST** /orgs/{org_id}/websites/{website_id}/domains/{domain_id}/screenshot/take | Take website screenshot immediately
[**unauthorize_website_ssh_key**](WebsitesApi.md#unauthorize_website_ssh_key) | **DELETE** /orgs/{org_id}/websites/{website_id}/ssh/keys/{key_id} | Unauthorize the public SSH key with the given ID.
[**update_ftp_user**](WebsitesApi.md#update_ftp_user) | **PATCH** /orgs/{org_id}/websites/{website_id}/ftp/users/{user_id} | Update given FTP user
[**update_user_crontab**](WebsitesApi.md#update_user_crontab) | **PATCH** /orgs/{org_id}/websites/{website_id}/crontab | Update user&#39;s crontab
[**update_website**](WebsitesApi.md#update_website) | **PATCH** /orgs/{org_id}/websites/{website_id} | Update website
[**update_website_domain_mapping**](WebsitesApi.md#update_website_domain_mapping) | **PATCH** /orgs/{org_id}/websites/{website_id}/domains/{domain_id} | Update website domain mapping
[**update_website_htaccess_ips_rule**](WebsitesApi.md#update_website_htaccess_ips_rule) | **PUT** /orgs/{org_id}/websites/{website_id}/htaccess/ips | Sets a rule over provided ips - either block or allow
[**update_website_htaccess_rewrites**](WebsitesApi.md#update_website_htaccess_rewrites) | **PATCH** /orgs/{org_id}/websites/{website_id}/htaccess | Updates rewrite rules
[**update_website_primary_domain**](WebsitesApi.md#update_website_primary_domain) | **PUT** /orgs/{org_id}/websites/{website_id}/domains/primary | Update primary domain mapping
[**update_website_ssh_key**](WebsitesApi.md#update_website_ssh_key) | **PATCH** /orgs/{org_id}/websites/{website_id}/ssh/keys/{key_id} | Update an existing website public SSH key.
[**upload_website_domain_ssl_cert**](WebsitesApi.md#upload_website_domain_ssl_cert) | **POST** /v2/domains/{domain_id}/ssl | Upload custom ssl certificate, key and optional fullchain for a given website
[**upload_website_mail_domain_ssl_cert**](WebsitesApi.md#upload_website_mail_domain_ssl_cert) | **POST** /v2/domains/{domain_id}/mail_ssl | Upload SSL for mail.customerdomain.
[**validate_website_operation**](WebsitesApi.md#validate_website_operation) | **POST** /orgs/{org_id}/websites/{website_id}/validate-operation | Validate whether a website operation is allowed


# **add_domain_nginx_fast_cgi_excluded_path**
> add_domain_nginx_fast_cgi_excluded_path(domain_id, body)

Add Nginx FastCGI excluded path

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
    api_instance = openapi_client.WebsitesApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.
    body = 'body_example' # str | Exclude the following path from nginx fastcgi cache.

    try:
        # Add Nginx FastCGI excluded path
        api_instance.add_domain_nginx_fast_cgi_excluded_path(domain_id, body)
    except Exception as e:
        print("Exception when calling WebsitesApi->add_domain_nginx_fast_cgi_excluded_path: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain_id** | **str**| The id of the domain. | 
 **body** | **str**| Exclude the following path from nginx fastcgi cache. | 

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
**200** | FastCGI excluded path added |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **authorize_website_ssh_key**
> NewSshKeyId authorize_website_ssh_key(org_id, website_id, new_ssh_key, sanitize=sanitize)

Authorize a new SSH key.

This operation will authorize the given public SSH key by appending its content to the website's .ssh/authorized_keys file.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.new_ssh_key import NewSshKey
from openapi_client.models.new_ssh_key_id import NewSshKeyId
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    new_ssh_key = openapi_client.NewSshKey() # NewSshKey | The public SSH key to authorize.
    sanitize = False # bool | If set to true, the SSH keys with unrecognized comments will be sanitized by changing the comment to a valid format that can be used to store metadata. If any of the keys requires sanitization the content of the authorized_keys file will be edited accordingly before returning the set of keys. If instead set to false, only the SSH keys that are recognized as valid (that is, contain valid metadata in their comments), will be returned, all the other keys will be skipped. (optional) (default to False)

    try:
        # Authorize a new SSH key.
        api_response = api_instance.authorize_website_ssh_key(org_id, website_id, new_ssh_key, sanitize=sanitize)
        print("The response of WebsitesApi->authorize_website_ssh_key:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->authorize_website_ssh_key: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **new_ssh_key** | [**NewSshKey**](NewSshKey.md)| The public SSH key to authorize. | 
 **sanitize** | **bool**| If set to true, the SSH keys with unrecognized comments will be sanitized by changing the comment to a valid format that can be used to store metadata. If any of the keys requires sanitization the content of the authorized_keys file will be edited accordingly before returning the set of keys. If instead set to false, only the SSH keys that are recognized as valid (that is, contain valid metadata in their comments), will be returned, all the other keys will be skipped. | [optional] [default to False]

### Return type

[**NewSshKeyId**](NewSshKeyId.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Successful |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **authorize_website_ssh_password**
> authorize_website_ssh_password(org_id, website_id, new_password)

Authorize a new SSH password for website.

This operation will authorize the given SSH password for the website's unix user. this request will replace the existing password for the user if already set.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.new_password import NewPassword
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    new_password = openapi_client.NewPassword() # NewPassword | The SSH password to authorize.

    try:
        # Authorize a new SSH password for website.
        api_instance.authorize_website_ssh_password(org_id, website_id, new_password)
    except Exception as e:
        print("Exception when calling WebsitesApi->authorize_website_ssh_password: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **new_password** | [**NewPassword**](NewPassword.md)| The SSH password to authorize. | 

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
**201** | Successful |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **clear_domain_nginx_fast_cgi**
> clear_domain_nginx_fast_cgi(domain_id)

Clear FastCGI cache for domain

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
    api_instance = openapi_client.WebsitesApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Clear FastCGI cache for domain
        api_instance.clear_domain_nginx_fast_cgi(domain_id)
    except Exception as e:
        print("Exception when calling WebsitesApi->clear_domain_nginx_fast_cgi: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
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
**200** | FastCGI cache cleared successfully |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **clone_website**
> NewResourceUuid clone_website(org_id, website_clone_request)

Clone website or push live

Clone a website or push live to overwrite an existing live website with content from the source website. Operation is asynchronous and returns a clone id. If includeDatabases is ommited, the all databases will be cloned from the source website. If includeDatabaseUsers is ommited, the all database users will be cloned from the source website.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.new_resource_uuid import NewResourceUuid
from openapi_client.models.website_clone_request import WebsiteCloneRequest
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_clone_request = openapi_client.WebsiteCloneRequest() # WebsiteCloneRequest | 

    try:
        # Clone website or push live
        api_response = api_instance.clone_website(org_id, website_clone_request)
        print("The response of WebsitesApi->clone_website:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->clone_website: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_clone_request** | [**WebsiteCloneRequest**](WebsiteCloneRequest.md)|  | 

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
**201** | Created |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_ftp_user**
> NewResourceUuid create_ftp_user(org_id, website_id, new_ftp_user, create_home=create_home)

Creates a new FTP user for a given website

Endpoint for creating a new FTP user. NOTE: user.account well get appended with website's primary domain. i.e. `username` will become `username@domain.com` Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.new_ftp_user import NewFtpUser
from openapi_client.models.new_resource_uuid import NewResourceUuid
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    new_ftp_user = openapi_client.NewFtpUser() # NewFtpUser | FTP User
    create_home = True # bool | If set to true we will try to crete a new home_dir for the user if does not exist. (optional)

    try:
        # Creates a new FTP user for a given website
        api_response = api_instance.create_ftp_user(org_id, website_id, new_ftp_user, create_home=create_home)
        print("The response of WebsitesApi->create_ftp_user:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->create_ftp_user: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **new_ftp_user** | [**NewFtpUser**](NewFtpUser.md)| FTP User | 
 **create_home** | **bool**| If set to true we will try to crete a new home_dir for the user if does not exist. | [optional] 

### Return type

[**NewResourceUuid**](NewResourceUuid.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | FTP user successfully created |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |
**409** | Already exists |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_preview_domain**
> str create_preview_domain(org_id, website_id)

Create a preview domain

Creates a preview domain for the given website and returns its full domain.  If a preview domain already exists, returns that instead.  Will error if a preview domain cannot be created. Returns 200 if an existing preview domain is returned and 201 if one has been created.

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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.

    try:
        # Create a preview domain
        api_response = api_instance.create_preview_domain(org_id, website_id)
        print("The response of WebsitesApi->create_preview_domain:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->create_preview_domain: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 

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
**200** | Preview domain existed |  -  |
**201** | Domain successfully created |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_website**
> NewResourceUuid create_website(org_id, new_website, kind=kind)

Create a new website or clone an existing one.

Creates or clone a website under the organization. If the org is the MO, the request need not contain a subscription ID, but if it's a customer and the session holder is not an MO admin, the subscription to which to attach the website must be supplied. If the website to be created is 'staging' kind then the subscription must include stagingWebsites resource > 1.  If 'normal' then the subscription must include websites > 1. If the website to be created is a control panel, the reseller's subscription id must match the reseller subscription. Session holder must be at least a `SuperAdmin` in this org or a parent org.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.new_resource_uuid import NewResourceUuid
from openapi_client.models.new_website import NewWebsite
from openapi_client.models.website_kind import WebsiteKind
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    new_website = openapi_client.NewWebsite() # NewWebsite | New website details. If the organization is the MO, they need not have a subscription to create a website. In all other cases organization needs to be subscribed to a plan that allows creating websites.
    kind = openapi_client.WebsiteKind() # WebsiteKind | The kind of a *special* website that needs to be created. Whether this website is to be a *control panel* website or a *phpMyAdmin* website. Note: in order to create a new *phpMyAdmin* website the control panel website needs to be created first, since the new phpMyAdmin website will be under the control panel domain. (optional)

    try:
        # Create a new website or clone an existing one.
        api_response = api_instance.create_website(org_id, new_website, kind=kind)
        print("The response of WebsitesApi->create_website:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->create_website: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **new_website** | [**NewWebsite**](NewWebsite.md)| New website details. If the organization is the MO, they need not have a subscription to create a website. In all other cases organization needs to be subscribed to a plan that allows creating websites. | 
 **kind** | [**WebsiteKind**](.md)| The kind of a *special* website that needs to be created. Whether this website is to be a *control panel* website or a *phpMyAdmin* website. Note: in order to create a new *phpMyAdmin* website the control panel website needs to be created first, since the new phpMyAdmin website will be under the control panel domain. | [optional] 

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
**201** | New website successfully created |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_website_domain_letsencrypt_certs**
> create_website_domain_letsencrypt_certs(domain_id)

Generate and setup letsencrypt ssl certificates for website's domain

Generates letsencrypt certificates for the domain. This is a longer running task, that will do a complete ssl setup for a given domain. Once completed any given domain will get served over `https`. Given domain must be publicly accessible and being served from our service. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

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
    api_instance = openapi_client.WebsitesApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Generate and setup letsencrypt ssl certificates for website's domain
        api_instance.create_website_domain_letsencrypt_certs(domain_id)
    except Exception as e:
        print("Exception when calling WebsitesApi->create_website_domain_letsencrypt_certs: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain_id** | **str**| The id of the domain. | 

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
**201** | SSL Certs successfully created |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_website_mail_domain_letsencrypt_certs**
> create_website_mail_domain_letsencrypt_certs(domain_id)

Generate and setup letsencrypt ssl certificates for website's domain with mail. prefix.

Generates letsencrypt certificate for the mail server at mail.customerdomain.

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
    api_instance = openapi_client.WebsitesApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Generate and setup letsencrypt ssl certificates for website's domain with mail. prefix.
        api_instance.create_website_mail_domain_letsencrypt_certs(domain_id)
    except Exception as e:
        print("Exception when calling WebsitesApi->create_website_mail_domain_letsencrypt_certs: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain_id** | **str**| The id of the domain. | 

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
**201** | SSL Certs successfully created |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_website_mapped_domain**
> NewResourceUuid create_website_mapped_domain(org_id, website_id, new_mapped_domain)

Create website mapped domain

Creates a domain mapping, where subscription resources are sufficient. The mapping kind will default to 'alias' if unspecified.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.new_mapped_domain import NewMappedDomain
from openapi_client.models.new_resource_uuid import NewResourceUuid
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    new_mapped_domain = openapi_client.NewMappedDomain() # NewMappedDomain | Domain details.

    try:
        # Create website mapped domain
        api_response = api_instance.create_website_mapped_domain(org_id, website_id, new_mapped_domain)
        print("The response of WebsitesApi->create_website_mapped_domain:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->create_website_mapped_domain: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **new_mapped_domain** | [**NewMappedDomain**](NewMappedDomain.md)| Domain details. | 

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
**201** | Successful |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_website_my_sqldb**
> NewResourceUuid create_website_my_sqldb(org_id, website_id, new_my_sqldb)

Create a MySQL database for website

Creates a new MySQL database for the given website. The supplied name must conform to the following regular expression: `^[0-9a-z$_]+$`. That is, a name may only contain alphanumerical characters, dollar signs, and underscores. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.new_my_sqldb import NewMySQLDB
from openapi_client.models.new_resource_uuid import NewResourceUuid
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    new_my_sqldb = openapi_client.NewMySQLDB() # NewMySQLDB | New database details.

    try:
        # Create a MySQL database for website
        api_response = api_instance.create_website_my_sqldb(org_id, website_id, new_my_sqldb)
        print("The response of WebsitesApi->create_website_my_sqldb:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->create_website_my_sqldb: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **new_my_sqldb** | [**NewMySQLDB**](NewMySQLDB.md)| New database details. | 

### Return type

[**NewResourceUuid**](NewResourceUuid.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Database successfully created |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |
**409** | Already exists |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_domain_nginx_fast_cgi_excluded_path**
> delete_domain_nginx_fast_cgi_excluded_path(domain_id, path)

Delete Nginx FastCGI excluded path

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
    api_instance = openapi_client.WebsitesApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.
    path = 'path_example' # str | 

    try:
        # Delete Nginx FastCGI excluded path
        api_instance.delete_domain_nginx_fast_cgi_excluded_path(domain_id, path)
    except Exception as e:
        print("Exception when calling WebsitesApi->delete_domain_nginx_fast_cgi_excluded_path: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain_id** | **str**| The id of the domain. | 
 **path** | **str**|  | 

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
**200** | FastCGI excluded path deleted |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_domain_webserver_rewrite**
> delete_domain_webserver_rewrite(domain_id, path)

Delete web server rewrite

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
    api_instance = openapi_client.WebsitesApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.
    path = 'path_example' # str | 

    try:
        # Delete web server rewrite
        api_instance.delete_domain_webserver_rewrite(domain_id, path)
    except Exception as e:
        print("Exception when calling WebsitesApi->delete_domain_webserver_rewrite: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain_id** | **str**| The id of the domain. | 
 **path** | **str**|  | 

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
**200** | Rewrite deleted |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_ftp_user**
> delete_ftp_user(org_id, website_id, user_id, delete_home=delete_home)

Deletes given FTP user

Endpoint for deleting FTP user for a given website. User homeDir can only be deleted if it is a subdir for the website home. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    user_id = 'user_id_example' # str | The id of an FTP user.
    delete_home = True # bool | If set to true we will try to delete the homeDir for the user. User homeDir can only be deleted if it is a subdir for the website home. (optional)

    try:
        # Deletes given FTP user
        api_instance.delete_ftp_user(org_id, website_id, user_id, delete_home=delete_home)
    except Exception as e:
        print("Exception when calling WebsitesApi->delete_ftp_user: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **user_id** | **str**| The id of an FTP user. | 
 **delete_home** | **bool**| If set to true we will try to delete the homeDir for the user. User homeDir can only be deleted if it is a subdir for the website home. | [optional] 

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
**204** | FTP user successfully deleted |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_user_crontab**
> delete_user_crontab(org_id, website_id)

Delete user's crontab

Delete user's crontab. Remove crontab file from disk.

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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.

    try:
        # Delete user's crontab
        api_instance.delete_user_crontab(org_id, website_id)
    except Exception as e:
        print("Exception when calling WebsitesApi->delete_user_crontab: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_website**
> delete_website(org_id, website_id, force=force)

Delete website

Mark a website as deleted, which does not remove its data, or force remove all its data. For removing all data and metadata belonging to a website (including DB records), pass the `force=true` query parameter. This can only be done by a privileged MO member. In this case, all data is wiped, so use carefully. Session holder must be at least a `SuperAdmin` in this org or a parent org.

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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    force = False # bool |  (optional) (default to False)

    try:
        # Delete website
        api_instance.delete_website(org_id, website_id, force=force)
    except Exception as e:
        print("Exception when calling WebsitesApi->delete_website: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **force** | **bool**|  | [optional] [default to False]

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

# **delete_website_domain_mapping**
> delete_website_domain_mapping(org_id, website_id, domain_id)

Delete website domain mapping

Deletes the domain mapping and decrements the domain alias quota usage in the website's subscription, if applicable. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Delete website domain mapping
        api_instance.delete_website_domain_mapping(org_id, website_id, domain_id)
    except Exception as e:
        print("Exception when calling WebsitesApi->delete_website_domain_mapping: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
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
**204** | Website domain mapping successfully deleted |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_website_domain_vhost**
> delete_website_domain_vhost(domain_id, delete_website_domain_vhost_request)

Deletes domain's custom vhost file if any

### Example


```python
import openapi_client
from openapi_client.models.delete_website_domain_vhost_request import DeleteWebsiteDomainVhostRequest
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
    api_instance = openapi_client.WebsitesApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.
    delete_website_domain_vhost_request = openapi_client.DeleteWebsiteDomainVhostRequest() # DeleteWebsiteDomainVhostRequest | 

    try:
        # Deletes domain's custom vhost file if any
        api_instance.delete_website_domain_vhost(domain_id, delete_website_domain_vhost_request)
    except Exception as e:
        print("Exception when calling WebsitesApi->delete_website_domain_vhost: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain_id** | **str**| The id of the domain. | 
 **delete_website_domain_vhost_request** | [**DeleteWebsiteDomainVhostRequest**](DeleteWebsiteDomainVhostRequest.md)|  | 

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
**200** | Vhost deleted |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_website_setting**
> delete_website_setting(org_id, website_id, setting_kind, setting_key)

Delete a single override setting

Delete a single website level service setting

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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    setting_kind = openapi_client.SettingKind() # SettingKind | The type of setting being applied
    setting_key = 'setting_key_example' # str | A key for updating an existing setting, some known values are - hard_delete_after_secs - letsencrypt_enabled - myhostname - org_websites_same_server - screenshot_driver_pool_size - screenshot_interval - sged_smtp - smtp_smart_host - website_backup

    try:
        # Delete a single override setting
        api_instance.delete_website_setting(org_id, website_id, setting_kind, setting_key)
    except Exception as e:
        print("Exception when calling WebsitesApi->delete_website_setting: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **setting_kind** | [**SettingKind**](.md)| The type of setting being applied | 
 **setting_key** | **str**| A key for updating an existing setting, some known values are - hard_delete_after_secs - letsencrypt_enabled - myhostname - org_websites_same_server - screenshot_driver_pool_size - screenshot_interval - sged_smtp - smtp_smart_host - website_backup | 

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

# **delete_websites**
> delete_websites(org_id, uuid_listing)

Delete websites

This operation can only be done by a logged in superadmin or owner of the organization or its parent organization(s).

### Example


```python
import openapi_client
from openapi_client.models.uuid_listing import UuidListing
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    uuid_listing = openapi_client.UuidListing() # UuidListing | The ids of the websites to delete.

    try:
        # Delete websites
        api_instance.delete_websites(org_id, uuid_listing)
    except Exception as e:
        print("Exception when calling WebsitesApi->delete_websites: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **uuid_listing** | [**UuidListing**](UuidListing.md)| The ids of the websites to delete. | 

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
**204** | Websites successfully deleted |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **disable_website_php_extension**
> disable_website_php_extension(website_id, body=body)

Disable a PHP extension

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
    api_instance = openapi_client.WebsitesApi(api_client)
    website_id = 'website_id_example' # str | The id of the website.
    body = 'body_example' # str |  (optional)

    try:
        # Disable a PHP extension
        api_instance.disable_website_php_extension(website_id, body=body)
    except Exception as e:
        print("Exception when calling WebsitesApi->disable_website_php_extension: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **website_id** | **str**| The id of the website. | 
 **body** | **str**|  | [optional] 

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
**200** | Extension disabled |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **enable_website_php_extension**
> enable_website_php_extension(website_id, body=body)

Enable a PHP extension

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
    api_instance = openapi_client.WebsitesApi(api_client)
    website_id = 'website_id_example' # str | The id of the website.
    body = 'body_example' # str |  (optional)

    try:
        # Enable a PHP extension
        api_instance.enable_website_php_extension(website_id, body=body)
    except Exception as e:
        print("Exception when calling WebsitesApi->enable_website_php_extension: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **website_id** | **str**| The id of the website. | 
 **body** | **str**|  | [optional] 

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
**200** | Extension enabled |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_domain_nginx_fast_cgi**
> bool get_domain_nginx_fast_cgi(domain_id)

Get status of Nginx FastCGI enablement

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
    api_instance = openapi_client.WebsitesApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Get status of Nginx FastCGI enablement
        api_response = api_instance.get_domain_nginx_fast_cgi(domain_id)
        print("The response of WebsitesApi->get_domain_nginx_fast_cgi:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->get_domain_nginx_fast_cgi: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain_id** | **str**| The id of the domain. | 

### Return type

**bool**

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

# **get_domain_nginx_fast_cgi_excluded_paths**
> List[str] get_domain_nginx_fast_cgi_excluded_paths(domain_id)

Get Nginx FastCGI excluded paths

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
    api_instance = openapi_client.WebsitesApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Get Nginx FastCGI excluded paths
        api_response = api_instance.get_domain_nginx_fast_cgi_excluded_paths(domain_id)
        print("The response of WebsitesApi->get_domain_nginx_fast_cgi_excluded_paths:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->get_domain_nginx_fast_cgi_excluded_paths: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain_id** | **str**| The id of the domain. | 

### Return type

**List[str]**

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

# **get_domain_webserver_rewrites**
> List[WebServerRewrite] get_domain_webserver_rewrites(domain_id)

Get web server rewrites for specified domain

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.web_server_rewrite import WebServerRewrite
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
    api_instance = openapi_client.WebsitesApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Get web server rewrites for specified domain
        api_response = api_instance.get_domain_webserver_rewrites(domain_id)
        print("The response of WebsitesApi->get_domain_webserver_rewrites:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->get_domain_webserver_rewrites: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain_id** | **str**| The id of the domain. | 

### Return type

[**List[WebServerRewrite]**](WebServerRewrite.md)

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

# **get_ftp_users**
> FtpUsersFullListing get_ftp_users(org_id, website_id)

Returns all ftp users data for a given website

Endpoint for retreaving ftp users for a given website Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.ftp_users_full_listing import FtpUsersFullListing
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.

    try:
        # Returns all ftp users data for a given website
        api_response = api_instance.get_ftp_users(org_id, website_id)
        print("The response of WebsitesApi->get_ftp_users:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->get_ftp_users: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 

### Return type

[**FtpUsersFullListing**](FtpUsersFullListing.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Ftp Users |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_screenshot_timestamp**
> UnixTimestamp get_screenshot_timestamp(org_id, website_id, domain_id)

Get last screeshot file's Timestamp

Returns Unix Timestamp for the last screenshot png file, if no screenshot found returns undefined

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.unix_timestamp import UnixTimestamp
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Get last screeshot file's Timestamp
        api_response = api_instance.get_screenshot_timestamp(org_id, website_id, domain_id)
        print("The response of WebsitesApi->get_screenshot_timestamp:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->get_screenshot_timestamp: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **domain_id** | **str**| The id of the domain. | 

### Return type

[**UnixTimestamp**](UnixTimestamp.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Unix Timestamp if screenshot exists |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_site_access_token**
> str get_site_access_token(org_id, website_id)

Get an access token for the given website

Request an access token for the given website. Note that access tokens may only be requested for normal websites, not for control panel websites. The access token is returned as an encrypted JWT in the response body. Session holder must either be a parent organization admin, or be a member with Site Access role of the given organization.

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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.

    try:
        # Get an access token for the given website
        api_response = api_instance.get_site_access_token(org_id, website_id)
        print("The response of WebsitesApi->get_site_access_token:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->get_site_access_token: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 

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
**200** | Site access request successful |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_user_crontab**
> CrontabFullListing get_user_crontab(org_id, website_id)

Get user's crontab

Get user's crontab. Only editable parts of crontab is returned.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.crontab_full_listing import CrontabFullListing
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.

    try:
        # Get user's crontab
        api_response = api_instance.get_user_crontab(org_id, website_id)
        print("The response of WebsitesApi->get_user_crontab:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->get_user_crontab: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 

### Return type

[**CrontabFullListing**](CrontabFullListing.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Successfully parsed crontab and found crontab exprestions |  -  |
**400** | Invalid input |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_website**
> Website get_website(org_id, website_id)

Get website

Returns detailed information about a single website. Session holder must be at least a `SuperAdmin` in this org or a parent org.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.website import Website
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.

    try:
        # Get website
        api_response = api_instance.get_website(org_id, website_id)
        print("The response of WebsitesApi->get_website:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->get_website: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 

### Return type

[**Website**](Website.md)

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

# **get_website_available_php_extensions**
> List[str] get_website_available_php_extensions(website_id)

Get available PHP extensions for a website

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
    api_instance = openapi_client.WebsitesApi(api_client)
    website_id = 'website_id_example' # str | The id of the website.

    try:
        # Get available PHP extensions for a website
        api_response = api_instance.get_website_available_php_extensions(website_id)
        print("The response of WebsitesApi->get_website_available_php_extensions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->get_website_available_php_extensions: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **website_id** | **str**| The id of the website. | 

### Return type

**List[str]**

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Extensions returned |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_website_backup_status**
> BackupStatus get_website_backup_status(org_id, website_id)

Get the status of an ongoing website backup operation

Returns the status of the currently ongoing backup or restore, if any. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.backup_status import BackupStatus
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.

    try:
        # Get the status of an ongoing website backup operation
        api_response = api_instance.get_website_backup_status(org_id, website_id)
        print("The response of WebsitesApi->get_website_backup_status:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->get_website_backup_status: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 

### Return type

[**BackupStatus**](BackupStatus.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**400** | Invalid arguments |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_website_cgroup_limits**
> CgroupLimits get_website_cgroup_limits(org_id, website_id)

Get the active cgroup limits for a website

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.cgroup_limits import CgroupLimits
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.

    try:
        # Get the active cgroup limits for a website
        api_response = api_instance.get_website_cgroup_limits(org_id, website_id)
        print("The response of WebsitesApi->get_website_cgroup_limits:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->get_website_cgroup_limits: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 

### Return type

[**CgroupLimits**](CgroupLimits.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Cgroup limitations if set |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_website_clone**
> WebsiteCloneResponse get_website_clone(org_id, clone_id)

Get's detail about a single push live

Fetches details about a single website clone. cloneWebsite call operation just enqueues the request and returns immediately. Use this endpoint to monitor how the clone finishes.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.website_clone_response import WebsiteCloneResponse
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    clone_id = 'clone_id_example' # str | The id of the website push live.

    try:
        # Get's detail about a single push live
        api_response = api_instance.get_website_clone(org_id, clone_id)
        print("The response of WebsitesApi->get_website_clone:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->get_website_clone: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **clone_id** | **str**| The id of the website push live. | 

### Return type

[**WebsiteCloneResponse**](WebsiteCloneResponse.md)

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

# **get_website_clone_log**
> List[WebsiteCloneLogEntry] get_website_clone_log(org_id, clone_id)

Get the log for a given clone id..

Fetches the import migration log for a single website clone.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.website_clone_log_entry import WebsiteCloneLogEntry
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    clone_id = 'clone_id_example' # str | The id of the website push live.

    try:
        # Get the log for a given clone id..
        api_response = api_instance.get_website_clone_log(org_id, clone_id)
        print("The response of WebsitesApi->get_website_clone_log:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->get_website_clone_log: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **clone_id** | **str**| The id of the website push live. | 

### Return type

[**List[WebsiteCloneLogEntry]**](WebsiteCloneLogEntry.md)

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

# **get_website_clones**
> WebsiteCloneFullListing get_website_clones(org_id)

List website clones for given OrgId

List of all webiste clones for the given OrgId.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.website_clone_full_listing import WebsiteCloneFullListing
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.

    try:
        # List website clones for given OrgId
        api_response = api_instance.get_website_clones(org_id)
        print("The response of WebsitesApi->get_website_clones:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->get_website_clones: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 

### Return type

[**WebsiteCloneFullListing**](WebsiteCloneFullListing.md)

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

# **get_website_domain_dns_query**
> DnsQueryOutcome get_website_domain_dns_query(org_id, website_id, domain_id, resolve_depth=resolve_depth)

Recursively query Dns servers for given domain

Returns details about the dns servers of given domain. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.dns_query_outcome import DnsQueryOutcome
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    domain_id = 'domain_id_example' # str | The id of the domain.
    resolve_depth = 'resolve_depth_example' # str | DNS query resolve depth, defaults to `short` if not provided. `short` -> takes the shortest path to resolve domain IP. `detailed` -> queries and returns output from all found Authoritative name servers. `queryAllTldNs` -> queries and returns results from all TLD name servers (very expensive). (optional)

    try:
        # Recursively query Dns servers for given domain
        api_response = api_instance.get_website_domain_dns_query(org_id, website_id, domain_id, resolve_depth=resolve_depth)
        print("The response of WebsitesApi->get_website_domain_dns_query:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->get_website_domain_dns_query: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **domain_id** | **str**| The id of the domain. | 
 **resolve_depth** | **str**| DNS query resolve depth, defaults to &#x60;short&#x60; if not provided. &#x60;short&#x60; -&gt; takes the shortest path to resolve domain IP. &#x60;detailed&#x60; -&gt; queries and returns output from all found Authoritative name servers. &#x60;queryAllTldNs&#x60; -&gt; queries and returns results from all TLD name servers (very expensive). | [optional] 

### Return type

[**DnsQueryOutcome**](DnsQueryOutcome.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Dns query outcome successfully returned |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_website_domain_mapping**
> DomainMapping get_website_domain_mapping(org_id, website_id, domain_id)

Returns website domain mapping

Returns a domain by its id that is mapped to this website. Requires login to have admin privileges in this org. Since only the MO can create standalone domains, session holder must be at least a `SuperAdmin` in the MO.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.domain_mapping import DomainMapping
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Returns website domain mapping
        api_response = api_instance.get_website_domain_mapping(org_id, website_id, domain_id)
        print("The response of WebsitesApi->get_website_domain_mapping:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->get_website_domain_mapping: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **domain_id** | **str**| The id of the domain. | 

### Return type

[**DomainMapping**](DomainMapping.md)

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

# **get_website_domain_mapping_dns_status**
> DnsStatus get_website_domain_mapping_dns_status(org_id, website_id, domain_id)

Returns website domain mapping DNS status

Returns an indication of whether the domain correctly resolves to the server this website is on.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.dns_status import DnsStatus
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Returns website domain mapping DNS status
        api_response = api_instance.get_website_domain_mapping_dns_status(org_id, website_id, domain_id)
        print("The response of WebsitesApi->get_website_domain_mapping_dns_status:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->get_website_domain_mapping_dns_status: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **domain_id** | **str**| The id of the domain. | 

### Return type

[**DnsStatus**](DnsStatus.md)

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

# **get_website_domain_mappings**
> DomainMappingsFullListing get_website_domain_mappings(org_id, website_id, with_ssl=with_ssl)

Get website's mapped domains

Returns a list of domains that are mapped to this website. Requires login to have admin privileges in this org.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.domain_mappings_full_listing import DomainMappingsFullListing
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    with_ssl = True # bool | If set to true, domains are returned with applicable ssl certificates. (optional)

    try:
        # Get website's mapped domains
        api_response = api_instance.get_website_domain_mappings(org_id, website_id, with_ssl=with_ssl)
        print("The response of WebsitesApi->get_website_domain_mappings:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->get_website_domain_mappings: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **with_ssl** | **bool**| If set to true, domains are returned with applicable ssl certificates. | [optional] 

### Return type

[**DomainMappingsFullListing**](DomainMappingsFullListing.md)

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

# **get_website_domain_mod_sec_status**
> ModSecStatus get_website_domain_mod_sec_status(domain_id)

Get mod security status for a single domain

### Example


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


# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.WebsitesApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Get mod security status for a single domain
        api_response = api_instance.get_website_domain_mod_sec_status(domain_id)
        print("The response of WebsitesApi->get_website_domain_mod_sec_status:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->get_website_domain_mod_sec_status: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain_id** | **str**| The id of the domain. | 

### Return type

[**ModSecStatus**](ModSecStatus.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Modsec status queried |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_website_domain_ssl_cert**
> DomainSslCertWithData get_website_domain_ssl_cert(domain_id)

Returns the SSL for this website domain

Endpoint for retrieving SSL certificates for a given website including certificates generated by letsencrypt

### Example


```python
import openapi_client
from openapi_client.models.domain_ssl_cert_with_data import DomainSslCertWithData
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
    api_instance = openapi_client.WebsitesApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Returns the SSL for this website domain
        api_response = api_instance.get_website_domain_ssl_cert(domain_id)
        print("The response of WebsitesApi->get_website_domain_ssl_cert:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->get_website_domain_ssl_cert: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain_id** | **str**| The id of the domain. | 

### Return type

[**DomainSslCertWithData**](DomainSslCertWithData.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | SSL details |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_website_domain_vhost**
> Vhost get_website_domain_vhost(domain_id)

Get domain's custom vhost file, if the file does not exist return empty string 

### Example


```python
import openapi_client
from openapi_client.models.vhost import Vhost
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
    api_instance = openapi_client.WebsitesApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Get domain's custom vhost file, if the file does not exist return empty string 
        api_response = api_instance.get_website_domain_vhost(domain_id)
        print("The response of WebsitesApi->get_website_domain_vhost:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->get_website_domain_vhost: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain_id** | **str**| The id of the domain. | 

### Return type

[**Vhost**](Vhost.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Vhost file queried |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_website_enabled_php_extensions**
> List[str] get_website_enabled_php_extensions(website_id)

Get enabled PHP extensions

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
    api_instance = openapi_client.WebsitesApi(api_client)
    website_id = 'website_id_example' # str | The id of the website.

    try:
        # Get enabled PHP extensions
        api_response = api_instance.get_website_enabled_php_extensions(website_id)
        print("The response of WebsitesApi->get_website_enabled_php_extensions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->get_website_enabled_php_extensions: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **website_id** | **str**| The id of the website. | 

### Return type

**List[str]**

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Extensions returned |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_website_fs_quota_limits**
> FsQuotaInfo get_website_fs_quota_limits(org_id, website_id)

Get the active FS quoa limits for a website

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.fs_quota_info import FsQuotaInfo
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.

    try:
        # Get the active FS quoa limits for a website
        api_response = api_instance.get_website_fs_quota_limits(org_id, website_id)
        print("The response of WebsitesApi->get_website_fs_quota_limits:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->get_website_fs_quota_limits: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 

### Return type

[**FsQuotaInfo**](FsQuotaInfo.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | FS quota limitations if set |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_website_htaccess_ips_rule**
> RequireIpsRule get_website_htaccess_ips_rule(org_id, website_id)

Returns current rules of blocked/whitelisted IPs

Allowlisting or blocklisting IPs via .htaccess is done using Require ip rule. This endpoint reads the rules from the .htaccess in the website's public_html. Note that this is not the same .htaccess that is used for writing redirect rules. In future this endpoint might be merged with the htaccess endpoint to allow writing rewrite rules and ip allow lists to any website directory.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.require_ips_rule import RequireIpsRule
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.

    try:
        # Returns current rules of blocked/whitelisted IPs
        api_response = api_instance.get_website_htaccess_ips_rule(org_id, website_id)
        print("The response of WebsitesApi->get_website_htaccess_ips_rule:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->get_website_htaccess_ips_rule: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 

### Return type

[**RequireIpsRule**](RequireIpsRule.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of ip and whether they&#39;re allowed or blocked |  -  |
**400** | Invalid .htaccess file |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | No rules found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_website_htaccess_rewrites**
> RewriteChainFullListing get_website_htaccess_rewrites(org_id, website_id)

Reads chains of rewrite rules

Rewrites are `RewriteRule`s in website's .htaccess. We use terminology \"rewrite chain\" to refer to 0 or more `RewriteCond`s directive ended by a `RewriteRule`. To identify a rewrite chain in the .htaccess file, we use line numbers. Line numbers serve two purposes. It acts loosely as an identifier, i.e. if you want to remove some chain or replace it by another, you would use the same line number you received when you read the `GET` endpoint. Second purpose is that of ordering. If you want some chain to be above another in the file, you have to make sure that the line number is less.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.rewrite_chain_full_listing import RewriteChainFullListing
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.

    try:
        # Reads chains of rewrite rules
        api_response = api_instance.get_website_htaccess_rewrites(org_id, website_id)
        print("The response of WebsitesApi->get_website_htaccess_rewrites:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->get_website_htaccess_rewrites: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 

### Return type

[**RewriteChainFullListing**](RewriteChainFullListing.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successfully parsed .htaccess and found rewrite chains |  -  |
**400** | Invalid .htaccess file |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_website_ioncube_status**
> bool get_website_ioncube_status(website_id)

Get ioncube status for an existing website

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
    api_instance = openapi_client.WebsitesApi(api_client)
    website_id = 'website_id_example' # str | The id of the website.

    try:
        # Get ioncube status for an existing website
        api_response = api_instance.get_website_ioncube_status(website_id)
        print("The response of WebsitesApi->get_website_ioncube_status:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->get_website_ioncube_status: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **website_id** | **str**| The id of the website. | 

### Return type

**bool**

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

# **get_website_mail_domain_ssl_cert**
> DomainSslCertWithData get_website_mail_domain_ssl_cert(domain_id)

Returns the SSL for this website domain with the mail.prefix

Endpoint for retrieving SSL certificates for a given website including certificates generated by letsencrypt

### Example


```python
import openapi_client
from openapi_client.models.domain_ssl_cert_with_data import DomainSslCertWithData
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
    api_instance = openapi_client.WebsitesApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Returns the SSL for this website domain with the mail.prefix
        api_response = api_instance.get_website_mail_domain_ssl_cert(domain_id)
        print("The response of WebsitesApi->get_website_mail_domain_ssl_cert:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->get_website_mail_domain_ssl_cert: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain_id** | **str**| The id of the domain. | 

### Return type

[**DomainSslCertWithData**](DomainSslCertWithData.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | SSL details |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    start = '2013-10-20T19:20:30+01:00' # datetime | Start datetime UTC. (optional)
    end = '2013-10-20T19:20:30+01:00' # datetime | End datetime UTC. (optional)
    granularity = 'granularity_example' # str | Takes one of `hour`, `day`, defaults to `day` (optional)

    try:
        # Get website metrics
        api_response = api_instance.get_website_metrics(org_id, website_id, start=start, end=end, granularity=granularity)
        print("The response of WebsitesApi->get_website_metrics:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->get_website_metrics: %s\n" % e)
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

# **get_website_my_sqldbs**
> MySQLDBsFullListing get_website_my_sqldbs(org_id, website_id)

Get website MySQL databases

Returns all MySQL databases belonging to the given website. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.my_sqldbs_full_listing import MySQLDBsFullListing
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.

    try:
        # Get website MySQL databases
        api_response = api_instance.get_website_my_sqldbs(org_id, website_id)
        print("The response of WebsitesApi->get_website_my_sqldbs:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->get_website_my_sqldbs: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 

### Return type

[**MySQLDBsFullListing**](MySQLDBsFullListing.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Databases successfully queried |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_website_redis_state**
> bool get_website_redis_state(website_id)

Get redis state for a website

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
    api_instance = openapi_client.WebsitesApi(api_client)
    website_id = 'website_id_example' # str | The id of the website.

    try:
        # Get redis state for a website
        api_response = api_instance.get_website_redis_state(website_id)
        print("The response of WebsitesApi->get_website_redis_state:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->get_website_redis_state: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **website_id** | **str**| The id of the website. | 

### Return type

**bool**

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

# **get_website_server_domains**
> WebsiteServerDomains get_website_server_domains(org_id, website_id)

Fetch website server domains

This endpoint will return the server domain for the application, email and database roles to which this website is assigned.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.website_server_domains import WebsiteServerDomains
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.

    try:
        # Fetch website server domains
        api_response = api_instance.get_website_server_domains(org_id, website_id)
        print("The response of WebsitesApi->get_website_server_domains:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->get_website_server_domains: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 

### Return type

[**WebsiteServerDomains**](WebsiteServerDomains.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Website server domains |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_website_setting**
> object get_website_setting(org_id, website_id, setting_kind)

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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    setting_kind = openapi_client.SettingKind() # SettingKind | The type of setting being applied

    try:
        # Get the value for a particular setting
        api_response = api_instance.get_website_setting(org_id, website_id, setting_kind)
        print("The response of WebsitesApi->get_website_setting:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->get_website_setting: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
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

# **get_website_ssh_keys**
> SshKeyFullListing get_website_ssh_keys(org_id, website_id, sanitize=sanitize)

Get website's authorized SSH keys

Returns a list of authorized public SSH keys. Invalid SSH keys entries in the authorized_keys file will be ignored. If the authorized_keys file does not exists, an empty set will be returned.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.ssh_key_full_listing import SshKeyFullListing
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    sanitize = False # bool | If set to true, the SSH keys with unrecognized comments will be sanitized by changing the comment to a valid format that can be used to store metadata. If any of the keys requires sanitization the content of the authorized_keys file will be edited accordingly before returning the set of keys. If instead set to false, only the SSH keys that are recognized as valid (that is, contain valid metadata in their comments), will be returned, all the other keys will be skipped. (optional) (default to False)

    try:
        # Get website's authorized SSH keys
        api_response = api_instance.get_website_ssh_keys(org_id, website_id, sanitize=sanitize)
        print("The response of WebsitesApi->get_website_ssh_keys:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->get_website_ssh_keys: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **sanitize** | **bool**| If set to true, the SSH keys with unrecognized comments will be sanitized by changing the comment to a valid format that can be used to store metadata. If any of the keys requires sanitization the content of the authorized_keys file will be edited accordingly before returning the set of keys. If instead set to false, only the SSH keys that are recognized as valid (that is, contain valid metadata in their comments), will be returned, all the other keys will be skipped. | [optional] [default to False]

### Return type

[**SshKeyFullListing**](SshKeyFullListing.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_website_webserver_kind**
> WebserverKind get_website_webserver_kind(website_id)

Get web server kind for a given website

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
    api_instance = openapi_client.WebsitesApi(api_client)
    website_id = 'website_id_example' # str | The id of the website.

    try:
        # Get web server kind for a given website
        api_response = api_instance.get_website_webserver_kind(website_id)
        print("The response of WebsitesApi->get_website_webserver_kind:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->get_website_webserver_kind: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **website_id** | **str**| The id of the website. | 

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
**200** | Query successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_websites**
> WebsitesListing get_websites(org_id, offset=offset, limit=limit, sort_by=sort_by, sort_order=sort_order, search=search, recursion=recursion, plan_id=plan_id, subscription_id=subscription_id, status=status, is_suspended=is_suspended, roles=roles, servers=servers, kind=kind, show_deleted=show_deleted, show_aliases=show_aliases)

Get websites

Returns all websites belonging to the organization. The results may optionally be sorted and paginated. If the recursive flag is set, the websites of customers of reseller customers are returned as well recursively, up to an optional max depth value. Session holder must be at least a `SuperAdmin` in this org or a parent org, or must have access to at least one website in this org. If the member is not an admin but has access to one or more websites, only those websites are returned.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.recursion import Recursion
from openapi_client.models.server_role import ServerRole
from openapi_client.models.website_kind import WebsiteKind
from openapi_client.models.website_status import WebsiteStatus
from openapi_client.models.websites_listing import WebsitesListing
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    offset = 56 # int | The offset from which to return items. (optional)
    limit = 56 # int | The maximum number of items to return. (optional)
    sort_by = 'sort_by_example' # str | The field by which to sort. (optional)
    sort_order = 'sort_order_example' # str | The direction in which to sort. Possible values are 'asc' and 'desc', defaulting to 'asc'. (optional)
    search = 'search_example' # str | Limit the result set to the resources whose names, partially and case insensitively, match the specified search term. E.g. for websites, this is their domain or tag, for databases the database name, for emails the email address or mailbox name, etc. A website will also be returned if the search term exactly matches the website's uuid. (optional)
    recursion = openapi_client.Recursion() # Recursion | If set to directCustomers then websites belonging to direct customers of the orgId will be returned.  If set to infinite then websites belonging to customers of customers (and so on) will be returned.  If unset then no recursion will be performed. (optional)
    plan_id = 56 # int | Limit the result set to resources under subscriptions to the plan. (optional)
    subscription_id = 56 # int | Limit the result set to resources under subscription. (optional)
    status = openapi_client.WebsiteStatus() # WebsiteStatus | Limit the result set to websites with the specified status. Only applicable if `recursive` is set to true. (optional)
    is_suspended = True # bool | Limit the result set to websites which are currently suspended or not suspended. (optional)
    roles = [openapi_client.ServerRole()] # List[ServerRole] | Limit the result set to websites having one of these roles assigned to a server. (optional)
    servers = ['servers_example'] # List[str] | Limit the result set to websites having one of the selected roles (or all roles) on one of these servers. (optional)
    kind = openapi_client.WebsiteKind() # WebsiteKind | Limit the results to websites of the specified type. (optional)
    show_deleted = True # bool | Filters out deleted websites, which are otherwise returned in the result. Defaults to `showDeleted=true` if not set. Can only be set by MO, if set by others, a 403 is returned. (optional)
    show_aliases = True # bool | Includes domain aliases in search results and listings in addition to the website's primary domain. (optional)

    try:
        # Get websites
        api_response = api_instance.get_websites(org_id, offset=offset, limit=limit, sort_by=sort_by, sort_order=sort_order, search=search, recursion=recursion, plan_id=plan_id, subscription_id=subscription_id, status=status, is_suspended=is_suspended, roles=roles, servers=servers, kind=kind, show_deleted=show_deleted, show_aliases=show_aliases)
        print("The response of WebsitesApi->get_websites:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->get_websites: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **offset** | **int**| The offset from which to return items. | [optional] 
 **limit** | **int**| The maximum number of items to return. | [optional] 
 **sort_by** | **str**| The field by which to sort. | [optional] 
 **sort_order** | **str**| The direction in which to sort. Possible values are &#39;asc&#39; and &#39;desc&#39;, defaulting to &#39;asc&#39;. | [optional] 
 **search** | **str**| Limit the result set to the resources whose names, partially and case insensitively, match the specified search term. E.g. for websites, this is their domain or tag, for databases the database name, for emails the email address or mailbox name, etc. A website will also be returned if the search term exactly matches the website&#39;s uuid. | [optional] 
 **recursion** | [**Recursion**](.md)| If set to directCustomers then websites belonging to direct customers of the orgId will be returned.  If set to infinite then websites belonging to customers of customers (and so on) will be returned.  If unset then no recursion will be performed. | [optional] 
 **plan_id** | **int**| Limit the result set to resources under subscriptions to the plan. | [optional] 
 **subscription_id** | **int**| Limit the result set to resources under subscription. | [optional] 
 **status** | [**WebsiteStatus**](.md)| Limit the result set to websites with the specified status. Only applicable if &#x60;recursive&#x60; is set to true. | [optional] 
 **is_suspended** | **bool**| Limit the result set to websites which are currently suspended or not suspended. | [optional] 
 **roles** | [**List[ServerRole]**](ServerRole.md)| Limit the result set to websites having one of these roles assigned to a server. | [optional] 
 **servers** | [**List[str]**](str.md)| Limit the result set to websites having one of the selected roles (or all roles) on one of these servers. | [optional] 
 **kind** | [**WebsiteKind**](.md)| Limit the results to websites of the specified type. | [optional] 
 **show_deleted** | **bool**| Filters out deleted websites, which are otherwise returned in the result. Defaults to &#x60;showDeleted&#x3D;true&#x60; if not set. Can only be set by MO, if set by others, a 403 is returned. | [optional] 
 **show_aliases** | **bool**| Includes domain aliases in search results and listings in addition to the website&#39;s primary domain. | [optional] 

### Return type

[**WebsitesListing**](WebsitesListing.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Websites successfully queried |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **perform_lets_encrypt_preflight_check**
> LetsEncryptPreflightResult perform_lets_encrypt_preflight_check(domain_id)

Perform the LetsEncrypt preflight check

Will attempt to verify that the domain will successfully achieve a LetsEncrypt certificate if attempted.  Provides debug information.

### Example


```python
import openapi_client
from openapi_client.models.lets_encrypt_preflight_result import LetsEncryptPreflightResult
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
    api_instance = openapi_client.WebsitesApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Perform the LetsEncrypt preflight check
        api_response = api_instance.perform_lets_encrypt_preflight_check(domain_id)
        print("The response of WebsitesApi->perform_lets_encrypt_preflight_check:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->perform_lets_encrypt_preflight_check: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain_id** | **str**| The id of the domain. | 

### Return type

[**LetsEncryptPreflightResult**](LetsEncryptPreflightResult.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Preflight check completed |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **push_website_live**
> push_website_live(org_id, website_id)

Making a staging website live

Validates that the operation is allowed for the website. Session holder must be at least a `SuperAdmin` in the org which owns the website, or a parent org. If the website is not owned by the MO, the subscription must have sufficient available 'websites' resource

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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.

    try:
        # Making a staging website live
        api_instance.push_website_live(org_id, website_id)
    except Exception as e:
        print("Exception when calling WebsitesApi->push_website_live: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 

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

# **restart_website_php**
> restart_website_php(website_id)

Restart PHP container for a website

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
    api_instance = openapi_client.WebsitesApi(api_client)
    website_id = 'website_id_example' # str | The id of the website.

    try:
        # Restart PHP container for a website
        api_instance.restart_website_php(website_id)
    except Exception as e:
        print("Exception when calling WebsitesApi->restart_website_php: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **website_id** | **str**| The id of the website. | 

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
**200** | PHP restarted successfully |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_domain_nginx_fast_cgi**
> set_domain_nginx_fast_cgi(domain_id, body)

Set Nginx FastCGI enablement

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
    api_instance = openapi_client.WebsitesApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.
    body = True # bool | Boolean value, set true to enable and false to disable FastCGI cache.

    try:
        # Set Nginx FastCGI enablement
        api_instance.set_domain_nginx_fast_cgi(domain_id, body)
    except Exception as e:
        print("Exception when calling WebsitesApi->set_domain_nginx_fast_cgi: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain_id** | **str**| The id of the domain. | 
 **body** | **bool**| Boolean value, set true to enable and false to disable FastCGI cache. | 

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
**200** | FastCGI enablement updated |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_domain_webserver_rewrite**
> set_domain_webserver_rewrite(domain_id, web_server_rewrite)

Set web server rewrite to file

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.web_server_rewrite import WebServerRewrite
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
    api_instance = openapi_client.WebsitesApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.
    web_server_rewrite = openapi_client.WebServerRewrite() # WebServerRewrite | Rewrite a path to a file

    try:
        # Set web server rewrite to file
        api_instance.set_domain_webserver_rewrite(domain_id, web_server_rewrite)
    except Exception as e:
        print("Exception when calling WebsitesApi->set_domain_webserver_rewrite: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain_id** | **str**| The id of the domain. | 
 **web_server_rewrite** | [**WebServerRewrite**](WebServerRewrite.md)| Rewrite a path to a file | 

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
**200** | Rewrite added |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_website_cgroup_limits**
> set_website_cgroup_limits(org_id, website_id, set_cgroup_limits)

Set the active cgroup limits for a website (Master org only)

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.set_cgroup_limits import SetCgroupLimits
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    set_cgroup_limits = openapi_client.SetCgroupLimits() # SetCgroupLimits | Cgroup limits.

    try:
        # Set the active cgroup limits for a website (Master org only)
        api_instance.set_website_cgroup_limits(org_id, website_id, set_cgroup_limits)
    except Exception as e:
        print("Exception when calling WebsitesApi->set_website_cgroup_limits: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **set_cgroup_limits** | [**SetCgroupLimits**](SetCgroupLimits.md)| Cgroup limits. | 

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
**200** | Cgroup limits successfully updated |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_website_domain_force_ssl**
> set_website_domain_force_ssl(domain_id, body)

Set \"force ssl\" status for domain mapping

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
    api_instance = openapi_client.WebsitesApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.
    body = True # bool | Boolean \"force ssl\" setting

    try:
        # Set \"force ssl\" status for domain mapping
        api_instance.set_website_domain_force_ssl(domain_id, body)
    except Exception as e:
        print("Exception when calling WebsitesApi->set_website_domain_force_ssl: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain_id** | **str**| The id of the domain. | 
 **body** | **bool**| Boolean \&quot;force ssl\&quot; setting | 

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
**201** | Setting updated |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_website_domain_mod_sec_status**
> set_website_domain_mod_sec_status(domain_id, mod_sec_status)

Set mod security status on a single domain

### Example


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


# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.WebsitesApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.
    mod_sec_status = openapi_client.ModSecStatus() # ModSecStatus | 

    try:
        # Set mod security status on a single domain
        api_instance.set_website_domain_mod_sec_status(domain_id, mod_sec_status)
    except Exception as e:
        print("Exception when calling WebsitesApi->set_website_domain_mod_sec_status: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain_id** | **str**| The id of the domain. | 
 **mod_sec_status** | [**ModSecStatus**](ModSecStatus.md)|  | 

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
**200** | Modsec status updated |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_website_domain_vhost**
> set_website_domain_vhost(domain_id, vhost)

Set a custom vhost file

### Example


```python
import openapi_client
from openapi_client.models.vhost import Vhost
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
    api_instance = openapi_client.WebsitesApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.
    vhost = openapi_client.Vhost() # Vhost | 

    try:
        # Set a custom vhost file
        api_instance.set_website_domain_vhost(domain_id, vhost)
    except Exception as e:
        print("Exception when calling WebsitesApi->set_website_domain_vhost: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain_id** | **str**| The id of the domain. | 
 **vhost** | [**Vhost**](Vhost.md)|  | 

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
**200** | Vhost file updated |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_website_fs_quota_limits**
> set_website_fs_quota_limits(org_id, website_id, fs_quota_limit)

Set the active FS quota limits for a website (Master org only)

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.fs_quota_limit import FsQuotaLimit
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    fs_quota_limit = openapi_client.FsQuotaLimit() # FsQuotaLimit | FS quota limits.

    try:
        # Set the active FS quota limits for a website (Master org only)
        api_instance.set_website_fs_quota_limits(org_id, website_id, fs_quota_limit)
    except Exception as e:
        print("Exception when calling WebsitesApi->set_website_fs_quota_limits: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **fs_quota_limit** | [**FsQuotaLimit**](FsQuotaLimit.md)| FS quota limits. | 

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
**200** | FS quota limits successfully updated |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_website_ioncube_status**
> set_website_ioncube_status(website_id, body=body)

Set ioncube status for an existing website

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
    api_instance = openapi_client.WebsitesApi(api_client)
    website_id = 'website_id_example' # str | The id of the website.
    body = True # bool |  (optional)

    try:
        # Set ioncube status for an existing website
        api_instance.set_website_ioncube_status(website_id, body=body)
    except Exception as e:
        print("Exception when calling WebsitesApi->set_website_ioncube_status: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **website_id** | **str**| The id of the website. | 
 **body** | **bool**|  | [optional] 

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
**200** | Status updated |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_website_redis_state**
> set_website_redis_state(website_id, body=body)

Set Redis state for an existing website

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
    api_instance = openapi_client.WebsitesApi(api_client)
    website_id = 'website_id_example' # str | The id of the website.
    body = True # bool |  (optional)

    try:
        # Set Redis state for an existing website
        api_instance.set_website_redis_state(website_id, body=body)
    except Exception as e:
        print("Exception when calling WebsitesApi->set_website_redis_state: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **website_id** | **str**| The id of the website. | 
 **body** | **bool**|  | [optional] 

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
**200** | Status updated |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_website_setting**
> set_website_setting(org_id, website_id, setting_kind, setting_key, service_setting_value)

Set a single override setting

Set or replace a single website level service setting

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    setting_kind = openapi_client.SettingKind() # SettingKind | The type of setting being applied
    setting_key = 'setting_key_example' # str | A key for updating an existing setting, some known values are - hard_delete_after_secs - letsencrypt_enabled - myhostname - org_websites_same_server - screenshot_driver_pool_size - screenshot_interval - sged_smtp - smtp_smart_host - website_backup
    service_setting_value = openapi_client.ServiceSettingValue() # ServiceSettingValue | 

    try:
        # Set a single override setting
        api_instance.set_website_setting(org_id, website_id, setting_kind, setting_key, service_setting_value)
    except Exception as e:
        print("Exception when calling WebsitesApi->set_website_setting: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **setting_kind** | [**SettingKind**](.md)| The type of setting being applied | 
 **setting_key** | **str**| A key for updating an existing setting, some known values are - hard_delete_after_secs - letsencrypt_enabled - myhostname - org_websites_same_server - screenshot_driver_pool_size - screenshot_interval - sged_smtp - smtp_smart_host - website_backup | 
 **service_setting_value** | [**ServiceSettingValue**](ServiceSettingValue.md)|  | 

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
**204** | Successful |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **take_screenshot**
> take_screenshot(org_id, website_id, domain_id)

Take website screenshot immediately

Take website screenshot immediately

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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Take website screenshot immediately
        api_instance.take_screenshot(org_id, website_id, domain_id)
    except Exception as e:
        print("Exception when calling WebsitesApi->take_screenshot: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
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
**200** | Successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **unauthorize_website_ssh_key**
> unauthorize_website_ssh_key(org_id, website_id, key_id)

Unauthorize the public SSH key with the given ID.

This operation will unauthorize the given public SSH key by deleting its content from the website's .ssh/authorized_keys file.

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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    key_id = 'key_id_example' # str | The unique ID of the SSH key within the same authorized_keys file.

    try:
        # Unauthorize the public SSH key with the given ID.
        api_instance.unauthorize_website_ssh_key(org_id, website_id, key_id)
    except Exception as e:
        print("Exception when calling WebsitesApi->unauthorize_website_ssh_key: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **key_id** | **str**| The unique ID of the SSH key within the same authorized_keys file. | 

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
**204** | SSH key successfully deleted |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_ftp_user**
> update_ftp_user(org_id, website_id, user_id, ftp_user_update)

Update given FTP user

Endpoint for updating FTP user for a given website We only allow user's homeDir and password to be updated. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.ftp_user_update import FtpUserUpdate
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    user_id = 'user_id_example' # str | The id of an FTP user.
    ftp_user_update = openapi_client.FtpUserUpdate() # FtpUserUpdate | FTP User

    try:
        # Update given FTP user
        api_instance.update_ftp_user(org_id, website_id, user_id, ftp_user_update)
    except Exception as e:
        print("Exception when calling WebsitesApi->update_ftp_user: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **user_id** | **str**| The id of an FTP user. | 
 **ftp_user_update** | [**FtpUserUpdate**](FtpUserUpdate.md)| FTP User | 

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
**204** | FTP user successfully updated |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_user_crontab**
> update_user_crontab(org_id, website_id, update_crontab_full_listing)

Update user's crontab

Update user's crontab. Note that users are able to update only cron expressions and environment variables.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.update_crontab_full_listing import UpdateCrontabFullListing
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    update_crontab_full_listing = openapi_client.UpdateCrontabFullListing() # UpdateCrontabFullListing | List of crontab expressions to be inserted into user's crontab. To identify a crontab expressions in the crontab file, we use line numbers.

    try:
        # Update user's crontab
        api_instance.update_user_crontab(org_id, website_id, update_crontab_full_listing)
    except Exception as e:
        print("Exception when calling WebsitesApi->update_user_crontab: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **update_crontab_full_listing** | [**UpdateCrontabFullListing**](UpdateCrontabFullListing.md)| List of crontab expressions to be inserted into user&#39;s crontab. To identify a crontab expressions in the crontab file, we use line numbers. | 

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
**204** | Successful |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_website**
> update_website(org_id, website_id, update_website)

Update website

Updates the website. It may be used to enable or disable a specific version of PHP for a website, in which case a corresponding `PhpCd` instance is installed or uninstalled on the same server of the website. When enabling the website PHP it is also possible to specify whether the SSH daemon will need to be enabled in the `PhpCd` service at startup, via the `ssh` boolean flag. Moreover, if PHP is already enabled for a website, it is possible to enable or disable its SSH by only specifying the `ssh` flag. The endpoint is also responsible for assigning tags to a website. Note that the input overwrites all existing tags, so when adding a new tag, the `tags` property also has to include existing tags that are to be kept. Only a parent organization or MO admin may suspend websites. The website may be moved to another subscription, if that subscription has enough quota to accommodate the new website, unless the MO is performing the action, in which case they may move any website off a subscription or to a subscription that doesn't necessary have quota left. Session holder must be at least a `SuperAdmin` in this org or a parent org.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.update_website import UpdateWebsite
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    update_website = openapi_client.UpdateWebsite() # UpdateWebsite | Website update details.

    try:
        # Update website
        api_instance.update_website(org_id, website_id, update_website)
    except Exception as e:
        print("Exception when calling WebsitesApi->update_website: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **update_website** | [**UpdateWebsite**](UpdateWebsite.md)| Website update details. | 

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
**204** | Successful |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_website_domain_mapping**
> update_website_domain_mapping(org_id, website_id, domain_id, domain_mapping_update)

Update website domain mapping

Partially updates the domain mapping. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.domain_mapping_update import DomainMappingUpdate
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    domain_id = 'domain_id_example' # str | The id of the domain.
    domain_mapping_update = openapi_client.DomainMappingUpdate() # DomainMappingUpdate | 

    try:
        # Update website domain mapping
        api_instance.update_website_domain_mapping(org_id, website_id, domain_id, domain_mapping_update)
    except Exception as e:
        print("Exception when calling WebsitesApi->update_website_domain_mapping: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **domain_id** | **str**| The id of the domain. | 
 **domain_mapping_update** | [**DomainMappingUpdate**](DomainMappingUpdate.md)|  | 

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
**204** | Successful |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_website_htaccess_ips_rule**
> update_website_htaccess_ips_rule(org_id, website_id, require_ips_rule)

Sets a rule over provided ips - either block or allow

Allowlisting or blocklisting IPs via .htaccess is done using Require ip rule. This endpoint puts the rule (creating .htaccess if it doesn't exist in process) into the public_html/.htaccess file. Note that this is not the same .htaccess that is used for writing redirect rules. In future this endpoint might be merged with the htaccess endpoint to allow writing rewrite rules and ip allow lists to any website directory.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.require_ips_rule import RequireIpsRule
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    require_ips_rule = openapi_client.RequireIpsRule() # RequireIpsRule | List of ips and a rule which should apply to them - either block all these ips or allow only these ips.

    try:
        # Sets a rule over provided ips - either block or allow
        api_instance.update_website_htaccess_ips_rule(org_id, website_id, require_ips_rule)
    except Exception as e:
        print("Exception when calling WebsitesApi->update_website_htaccess_ips_rule: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **require_ips_rule** | [**RequireIpsRule**](RequireIpsRule.md)| List of ips and a rule which should apply to them - either block all these ips or allow only these ips. | 

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
**204** | Successfully parsed .htaccess and updated ip rules |  -  |
**400** | Invalid .htaccess file |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_website_htaccess_rewrites**
> update_website_htaccess_rewrites(org_id, website_id, update_rewrite_chain_full_listing)

Updates rewrite rules

Rewrites are `RewriteRule`s in website's .htaccess file. We use terminology \"rewrite chain\" to refer to 0 or more `RewriteCond`s directive ended by `RewriteRule`.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.update_rewrite_chain_full_listing import UpdateRewriteChainFullListing
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    update_rewrite_chain_full_listing = openapi_client.UpdateRewriteChainFullListing() # UpdateRewriteChainFullListing | List of rewrite chains to be inserted into the .htaccess file. To identify a rewrite chain in the .htaccess file, we use line numbers. Line numbers serve two purposes. It acts loosely as an identifier, i.e. if you want to remove some chain or replace it by another, you would use the same line number you received when you read the `GET` endpoint. Second purpose is that of ordering. If you want some chain to be above another in the file, you have to make sure that the line number is less. To delete a rewrite chain, just send a line number without any additional information for a single `RewriteChain` object.

    try:
        # Updates rewrite rules
        api_instance.update_website_htaccess_rewrites(org_id, website_id, update_rewrite_chain_full_listing)
    except Exception as e:
        print("Exception when calling WebsitesApi->update_website_htaccess_rewrites: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **update_rewrite_chain_full_listing** | [**UpdateRewriteChainFullListing**](UpdateRewriteChainFullListing.md)| List of rewrite chains to be inserted into the .htaccess file. To identify a rewrite chain in the .htaccess file, we use line numbers. Line numbers serve two purposes. It acts loosely as an identifier, i.e. if you want to remove some chain or replace it by another, you would use the same line number you received when you read the &#x60;GET&#x60; endpoint. Second purpose is that of ordering. If you want some chain to be above another in the file, you have to make sure that the line number is less. To delete a rewrite chain, just send a line number without any additional information for a single &#x60;RewriteChain&#x60; object. | 

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
**204** | Successfully parsed .htaccess and updated rewrite chains |  -  |
**400** | Invalid .htaccess file |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_website_primary_domain**
> update_website_primary_domain(org_id, website_id, new_primary_domain_mapping)

Update primary domain mapping

This operation can only be done by a logged in superadmin or owner of the organization or its parent organization(s). Domain and website has to belong to this organization.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.new_primary_domain_mapping import NewPrimaryDomainMapping
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    new_primary_domain_mapping = openapi_client.NewPrimaryDomainMapping() # NewPrimaryDomainMapping | Domain mapping details.

    try:
        # Update primary domain mapping
        api_instance.update_website_primary_domain(org_id, website_id, new_primary_domain_mapping)
    except Exception as e:
        print("Exception when calling WebsitesApi->update_website_primary_domain: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **new_primary_domain_mapping** | [**NewPrimaryDomainMapping**](NewPrimaryDomainMapping.md)| Domain mapping details. | 

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
**200** | Successfully made domain the primary domain of website |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_website_ssh_key**
> update_website_ssh_key(org_id, website_id, key_id, ssh_key_update)

Update an existing website public SSH key.

This operation will update the given public SSH key value, and/or its associated friendly name. An error will be returned if none of the expected arguments of the request body is specified.

### Example


```python
import openapi_client
from openapi_client.models.ssh_key_update import SshKeyUpdate
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    key_id = 'key_id_example' # str | The unique ID of the SSH key within the same authorized_keys file.
    ssh_key_update = openapi_client.SshKeyUpdate() # SshKeyUpdate | The public SSH key updatable fields.

    try:
        # Update an existing website public SSH key.
        api_instance.update_website_ssh_key(org_id, website_id, key_id, ssh_key_update)
    except Exception as e:
        print("Exception when calling WebsitesApi->update_website_ssh_key: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **key_id** | **str**| The unique ID of the SSH key within the same authorized_keys file. | 
 **ssh_key_update** | [**SshKeyUpdate**](SshKeyUpdate.md)| The public SSH key updatable fields. | 

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
**200** | SSH key successfully updated |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **upload_website_domain_ssl_cert**
> NewSslCert upload_website_domain_ssl_cert(domain_id, ssl_cert)

Upload custom ssl certificate, key and optional fullchain for a given website

Endpoint for uploading custom SSL certificate for a given website. Verifies the cert key and maps to relevant domains that the certificate can be applied to. Returns error if no domain match is found. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.new_ssl_cert import NewSslCert
from openapi_client.models.ssl_cert import SslCert
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
    api_instance = openapi_client.WebsitesApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.
    ssl_cert = openapi_client.SslCert() # SslCert | Cert, private key and optional fullchain.

    try:
        # Upload custom ssl certificate, key and optional fullchain for a given website
        api_response = api_instance.upload_website_domain_ssl_cert(domain_id, ssl_cert)
        print("The response of WebsitesApi->upload_website_domain_ssl_cert:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->upload_website_domain_ssl_cert: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain_id** | **str**| The id of the domain. | 
 **ssl_cert** | [**SslCert**](SslCert.md)| Cert, private key and optional fullchain. | 

### Return type

[**NewSslCert**](NewSslCert.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | SSL Cert successfully uploaded, returns list of applicable domains |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **upload_website_mail_domain_ssl_cert**
> NewSslCert upload_website_mail_domain_ssl_cert(domain_id, ssl_cert)

Upload SSL for mail.customerdomain.

### Example


```python
import openapi_client
from openapi_client.models.new_ssl_cert import NewSslCert
from openapi_client.models.ssl_cert import SslCert
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
    api_instance = openapi_client.WebsitesApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.
    ssl_cert = openapi_client.SslCert() # SslCert | Cert, private key and optional fullchain.

    try:
        # Upload SSL for mail.customerdomain.
        api_response = api_instance.upload_website_mail_domain_ssl_cert(domain_id, ssl_cert)
        print("The response of WebsitesApi->upload_website_mail_domain_ssl_cert:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->upload_website_mail_domain_ssl_cert: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain_id** | **str**| The id of the domain. | 
 **ssl_cert** | [**SslCert**](SslCert.md)| Cert, private key and optional fullchain. | 

### Return type

[**NewSslCert**](NewSslCert.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | SSL Cert successfully uploaded |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **validate_website_operation**
> ValidationResult validate_website_operation(org_id, website_id, website_operation_validation)

Validate whether a website operation is allowed

Validates that the operation is allowed for the website. Currently this is only for verifying whether a website may be moved to another subscription, but this could later be expanded with other actions that can be verified. Session holder must be at least a `SuperAdmin` in this org or a parent org.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.validation_result import ValidationResult
from openapi_client.models.website_operation_validation import WebsiteOperationValidation
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
    api_instance = openapi_client.WebsitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    website_operation_validation = openapi_client.WebsiteOperationValidation() # WebsiteOperationValidation | 

    try:
        # Validate whether a website operation is allowed
        api_response = api_instance.validate_website_operation(org_id, website_id, website_operation_validation)
        print("The response of WebsitesApi->validate_website_operation:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsitesApi->validate_website_operation: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **website_operation_validation** | [**WebsiteOperationValidation**](WebsiteOperationValidation.md)|  | 

### Return type

[**ValidationResult**](ValidationResult.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
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

