# get_floating_ips

Returns list of floating IPs

```py
def get_floating_ips(self, wait_for_completion=True, timeout=15):
```



## Returns

| Type | Return Value                                                                                  |
|------|-----------------------------------------------------------------------------------------------|
| dict | When wait_for_completion is False, the full API response for `GET /internal/node_management/cluster_ip` |
| dict | When wait_for_completion is True, the full API response of the job status |



