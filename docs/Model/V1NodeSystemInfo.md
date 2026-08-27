# V1NodeSystemInfo

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**architecture** | **string** | The Architecture reported by the node |
**boot_id** | **string** | Boot ID reported by the node. |
**container_runtime_version** | **string** | ContainerRuntime Version reported by the node through runtime remote API (e.g. containerd://1.4.2). |
**kernel_version** | **string** | Kernel Version reported by the node from &#39;uname -r&#39; (e.g. 3.16.0-0.bpo.4-amd64). |
**kube_proxy_version** | **string** | Deprecated: KubeProxy Version reported by the node. |
**kubelet_version** | **string** | Kubelet Version reported by the node. |
**machine_id** | **string** | MachineID reported by the node. For unique machine identification in the cluster this field is preferred. Learn more from man(5) machine-id: http://man7.org/linux/man-pages/man5/machine-id.5.html |
**operating_system** | **string** | The Operating System reported by the node |
**os_image** | **string** | OS Image reported by the node from /etc/os-release (e.g. Debian GNU/Linux 7 (wheezy)). |
**running_in_user_namespace** | **bool** | Whether the node is running in a user namespace. | [optional]
**swap** | [**\Kubernetes\Client\Model\V1NodeSwapStatus**](V1NodeSwapStatus.md) |  | [optional]
**system_uuid** | **string** | SystemUUID reported by the node. For unique machine identification MachineID is preferred. This field is specific to Red Hat hosts https://access.redhat.com/documentation/en-us/red_hat_subscription_management/1/html/rhsm/uuid |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
