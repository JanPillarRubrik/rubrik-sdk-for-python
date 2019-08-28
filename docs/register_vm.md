# register_vm

Register the Rubrik Backup Service on a vSphere VM.

```py
def register_vm(self, name, timeout=15):
```

## Arguments
| Name | Type | Description                 | Choices |
|------|------|-----------------------------|---------|
| name | str  | The name of the vSphere VM. |         |

## Keyword Arguments
| Name    | Type | Description                                                                 | Choices | Default |
|---------|------|-----------------------------------------------------------------------------|---------|---------|
| timeout | int  | The number of seconds to wait to establish a connection the Rubrik cluster. |         | 15      |

## Returns
| Type | Return Value                                                         |
|------|----------------------------------------------------------------------|
| str  | No change required. The VM `name` is already registered.             |
| dict | The result of the call for `POST /v1/vmware/vm/{id}/register_agent`. |

## Example
```py
import rubrik_cdm

rubrik = rubrik_cdm.Connect()

vm_name = "Pyton SDK"

register_vbs_on_bm = rubrik.register_vm(vm_name)
```