# DnsQueryOutcome

Detailed DNS query outcome, walking from root DNS to all the way back to IP addresses for a domain

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**fqdn** | **str** | Fully qualified domain name | 
**root** | **Dict[str, str]** | name and IP of the root server that was queried | 
**tld_ns_map** | [**Dict[str, TldNs]**](TldNs.md) | Tree of top level domain name servers | 

## Example

```python
from openapi_client.models.dns_query_outcome import DnsQueryOutcome

# TODO update the JSON string below
json = "{}"
# create an instance of DnsQueryOutcome from a JSON string
dns_query_outcome_instance = DnsQueryOutcome.from_json(json)
# print the JSON string representation of the object
print(DnsQueryOutcome.to_json())

# convert the object into a dict
dns_query_outcome_dict = dns_query_outcome_instance.to_dict()
# create an instance of DnsQueryOutcome from a dict
dns_query_outcome_from_dict = DnsQueryOutcome.from_dict(dns_query_outcome_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


