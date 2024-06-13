# MetricsEntry

Each Metrics entry represts an hourly window of banwidth usage Note: depending upon the polling time, most recent hour values might not       be complete yet and are subject to change if fetched at a later time.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**datetime** | **datetime** | Time at the beginning of the unit for this bandwidth consumption entry | 
**bytes_received** | **float** |  | 
**bytes_sent** | **float** |  | 
**unique_hits** | **float** |  | 
**bot_hits** | **float** |  | 
**total_hits** | **float** |  | 

## Example

```python
from openapi_client.models.metrics_entry import MetricsEntry

# TODO update the JSON string below
json = "{}"
# create an instance of MetricsEntry from a JSON string
metrics_entry_instance = MetricsEntry.from_json(json)
# print the JSON string representation of the object
print(MetricsEntry.to_json())

# convert the object into a dict
metrics_entry_dict = metrics_entry_instance.to_dict()
# create an instance of MetricsEntry from a dict
metrics_entry_from_dict = MetricsEntry.from_dict(metrics_entry_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


