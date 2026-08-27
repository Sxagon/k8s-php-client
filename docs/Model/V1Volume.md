# V1Volume

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**aws_elastic_block_store** | [**\Kubernetes\Client\Model\V1AWSElasticBlockStoreVolumeSource**](V1AWSElasticBlockStoreVolumeSource.md) |  | [optional]
**azure_disk** | [**\Kubernetes\Client\Model\V1AzureDiskVolumeSource**](V1AzureDiskVolumeSource.md) |  | [optional]
**azure_file** | [**\Kubernetes\Client\Model\V1AzureFileVolumeSource**](V1AzureFileVolumeSource.md) |  | [optional]
**cephfs** | [**\Kubernetes\Client\Model\V1CephFSVolumeSource**](V1CephFSVolumeSource.md) |  | [optional]
**cinder** | [**\Kubernetes\Client\Model\V1CinderVolumeSource**](V1CinderVolumeSource.md) |  | [optional]
**config_map** | [**\Kubernetes\Client\Model\V1ConfigMapVolumeSource**](V1ConfigMapVolumeSource.md) |  | [optional]
**csi** | [**\Kubernetes\Client\Model\V1CSIVolumeSource**](V1CSIVolumeSource.md) |  | [optional]
**downward_api** | [**\Kubernetes\Client\Model\V1DownwardAPIVolumeSource**](V1DownwardAPIVolumeSource.md) |  | [optional]
**empty_dir** | [**\Kubernetes\Client\Model\V1EmptyDirVolumeSource**](V1EmptyDirVolumeSource.md) |  | [optional]
**ephemeral** | [**\Kubernetes\Client\Model\V1EphemeralVolumeSource**](V1EphemeralVolumeSource.md) |  | [optional]
**fc** | [**\Kubernetes\Client\Model\V1FCVolumeSource**](V1FCVolumeSource.md) |  | [optional]
**flex_volume** | [**\Kubernetes\Client\Model\V1FlexVolumeSource**](V1FlexVolumeSource.md) |  | [optional]
**flocker** | [**\Kubernetes\Client\Model\V1FlockerVolumeSource**](V1FlockerVolumeSource.md) |  | [optional]
**gce_persistent_disk** | [**\Kubernetes\Client\Model\V1GCEPersistentDiskVolumeSource**](V1GCEPersistentDiskVolumeSource.md) |  | [optional]
**git_repo** | [**\Kubernetes\Client\Model\V1GitRepoVolumeSource**](V1GitRepoVolumeSource.md) |  | [optional]
**glusterfs** | [**\Kubernetes\Client\Model\V1GlusterfsVolumeSource**](V1GlusterfsVolumeSource.md) |  | [optional]
**host_path** | [**\Kubernetes\Client\Model\V1HostPathVolumeSource**](V1HostPathVolumeSource.md) |  | [optional]
**image** | [**\Kubernetes\Client\Model\V1ImageVolumeSource**](V1ImageVolumeSource.md) |  | [optional]
**iscsi** | [**\Kubernetes\Client\Model\V1ISCSIVolumeSource**](V1ISCSIVolumeSource.md) |  | [optional]
**name** | **string** | name of the volume. Must be a DNS_LABEL and unique within the pod. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names |
**nfs** | [**\Kubernetes\Client\Model\V1NFSVolumeSource**](V1NFSVolumeSource.md) |  | [optional]
**persistent_volume_claim** | [**\Kubernetes\Client\Model\V1PersistentVolumeClaimVolumeSource**](V1PersistentVolumeClaimVolumeSource.md) |  | [optional]
**photon_persistent_disk** | [**\Kubernetes\Client\Model\V1PhotonPersistentDiskVolumeSource**](V1PhotonPersistentDiskVolumeSource.md) |  | [optional]
**portworx_volume** | [**\Kubernetes\Client\Model\V1PortworxVolumeSource**](V1PortworxVolumeSource.md) |  | [optional]
**projected** | [**\Kubernetes\Client\Model\V1ProjectedVolumeSource**](V1ProjectedVolumeSource.md) |  | [optional]
**quobyte** | [**\Kubernetes\Client\Model\V1QuobyteVolumeSource**](V1QuobyteVolumeSource.md) |  | [optional]
**rbd** | [**\Kubernetes\Client\Model\V1RBDVolumeSource**](V1RBDVolumeSource.md) |  | [optional]
**scale_io** | [**\Kubernetes\Client\Model\V1ScaleIOVolumeSource**](V1ScaleIOVolumeSource.md) |  | [optional]
**secret** | [**\Kubernetes\Client\Model\V1SecretVolumeSource**](V1SecretVolumeSource.md) |  | [optional]
**storageos** | [**\Kubernetes\Client\Model\V1StorageOSVolumeSource**](V1StorageOSVolumeSource.md) |  | [optional]
**vsphere_volume** | [**\Kubernetes\Client\Model\V1VsphereVirtualDiskVolumeSource**](V1VsphereVirtualDiskVolumeSource.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
