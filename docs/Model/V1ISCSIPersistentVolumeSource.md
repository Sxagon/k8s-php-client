# V1ISCSIPersistentVolumeSource

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**chap_auth_discovery** | **bool** | chapAuthDiscovery defines whether support iSCSI Discovery CHAP authentication | [optional]
**chap_auth_session** | **bool** | chapAuthSession defines whether support iSCSI Session CHAP authentication | [optional]
**fs_type** | **string** | fsType is the filesystem type of the volume that you want to mount. Tip: Ensure that the filesystem type is supported by the host operating system. Examples: \&quot;ext4\&quot;, \&quot;xfs\&quot;, \&quot;ntfs\&quot;. Implicitly inferred to be \&quot;ext4\&quot; if unspecified. More info: https://kubernetes.io/docs/concepts/storage/volumes#iscsi | [optional]
**initiator_name** | **string** | initiatorName is the custom iSCSI Initiator Name. If initiatorName is specified with iscsiInterface simultaneously, new iSCSI interface &lt;target portal&gt;:&lt;volume name&gt; will be created for the connection. | [optional]
**iqn** | **string** | iqn is Target iSCSI Qualified Name. |
**iscsi_interface** | **string** | iscsiInterface is the interface Name that uses an iSCSI transport. Defaults to &#39;default&#39; (tcp). | [optional]
**lun** | **int** | lun is iSCSI Target Lun number. |
**portals** | **string[]** | portals is the iSCSI Target Portal List. The Portal is either an IP or ip_addr:port if the port is other than default (typically TCP ports 860 and 3260). | [optional]
**read_only** | **bool** | readOnly here will force the ReadOnly setting in VolumeMounts. Defaults to false. | [optional]
**secret_ref** | [**\Kubernetes\Client\Model\V1SecretReference**](V1SecretReference.md) |  | [optional]
**target_portal** | **string** | targetPortal is iSCSI Target Portal. The Portal is either an IP or ip_addr:port if the port is other than default (typically TCP ports 860 and 3260). |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
