# on_demand_snapshot

Initiate an on-demand snapshot.
```py
def on_demand_snapshot(object_name, object_type, sla_name='current', fileset=None, host_os=None)
```

## Arguments
| Name        | Type | Description                                                                 | Choices |
|-------------|------|-----------------------------------------------------------------------------|---------|
| object_name  | str  | The name of the Rubrik object to take a on-demand snapshot of. |         |
| object_type  | str  | The Rubrik object type you want to backup.  |    vmware, physical_host     |
## Keyword Arguments
| Name        | Type | Description                                                                 | Choices | Default |
|-------------|------|-----------------------------------------------------------------------------|---------|---------|
| sla_name  | str  | The SLA Domain name you want to assign the on-demand snapshot to. By default, the currently assigned SLA Domain will be used.  |         |    current     |
| fileset  | str  | The name of the Fileset you wish to backup. Only required when taking a on-demand snapshot of a physical host.  |         |    None     |
| host_os  | str  | The operating system for the physical host. Only required when taking a on-demand snapshot of a physical host.  |    Linux, Windows     |    None      |

## Returns
| Type | Return Value                                                                                   |
|------|-----------------------------------------------------------------------------------------------|
| tuple  | The full API response for `POST /v1/vmware/vm/{ID}/snapshot` and the job status URL which can be used to monitor progress of the snapshot. (api_response, job_status_url) |
## Example
```py
import rubrik_cdm

rubrik = rubrik_cdm.Connect()

vm_name = "python-sdk-demo"
object_type = "vmware"

snapshot = rubrik.on_demand_snapshot(vm_name, object_type)
```