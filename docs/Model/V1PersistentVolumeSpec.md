# V1PersistentVolumeSpec

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**access_modes** | **string[]** | accessModes contains all ways the volume can be mounted. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#access-modes | [optional]
**aws_elastic_block_store** | [**\Kubernetes\Client\Model\V1AWSElasticBlockStoreVolumeSource**](V1AWSElasticBlockStoreVolumeSource.md) |  | [optional]
**azure_disk** | [**\Kubernetes\Client\Model\V1AzureDiskVolumeSource**](V1AzureDiskVolumeSource.md) |  | [optional]
**azure_file** | [**\Kubernetes\Client\Model\V1AzureFilePersistentVolumeSource**](V1AzureFilePersistentVolumeSource.md) |  | [optional]
**capacity** | **array<string,string>** | capacity is the description of the persistent volume&#39;s resources and capacity. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#capacity | [optional]
**cephfs** | [**\Kubernetes\Client\Model\V1CephFSPersistentVolumeSource**](V1CephFSPersistentVolumeSource.md) |  | [optional]
**cinder** | [**\Kubernetes\Client\Model\V1CinderPersistentVolumeSource**](V1CinderPersistentVolumeSource.md) |  | [optional]
**claim_ref** | [**\Kubernetes\Client\Model\V1ObjectReference**](V1ObjectReference.md) |  | [optional]
**csi** | [**\Kubernetes\Client\Model\V1CSIPersistentVolumeSource**](V1CSIPersistentVolumeSource.md) |  | [optional]
**fc** | [**\Kubernetes\Client\Model\V1FCVolumeSource**](V1FCVolumeSource.md) |  | [optional]
**flex_volume** | [**\Kubernetes\Client\Model\V1FlexPersistentVolumeSource**](V1FlexPersistentVolumeSource.md) |  | [optional]
**flocker** | [**\Kubernetes\Client\Model\V1FlockerVolumeSource**](V1FlockerVolumeSource.md) |  | [optional]
**gce_persistent_disk** | [**\Kubernetes\Client\Model\V1GCEPersistentDiskVolumeSource**](V1GCEPersistentDiskVolumeSource.md) |  | [optional]
**glusterfs** | [**\Kubernetes\Client\Model\V1GlusterfsPersistentVolumeSource**](V1GlusterfsPersistentVolumeSource.md) |  | [optional]
**host_path** | [**\Kubernetes\Client\Model\V1HostPathVolumeSource**](V1HostPathVolumeSource.md) |  | [optional]
**iscsi** | [**\Kubernetes\Client\Model\V1ISCSIPersistentVolumeSource**](V1ISCSIPersistentVolumeSource.md) |  | [optional]
**local** | [**\Kubernetes\Client\Model\V1LocalVolumeSource**](V1LocalVolumeSource.md) |  | [optional]
**mount_options** | **string[]** | mountOptions is the list of mount options, e.g. [\&quot;ro\&quot;, \&quot;soft\&quot;]. Not validated - mount will simply fail if one is invalid. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes/#mount-options | [optional]
**nfs** | [**\Kubernetes\Client\Model\V1NFSVolumeSource**](V1NFSVolumeSource.md) |  | [optional]
**node_affinity** | [**\Kubernetes\Client\Model\V1VolumeNodeAffinity**](V1VolumeNodeAffinity.md) |  | [optional]
**persistent_volume_reclaim_policy** | **string** | persistentVolumeReclaimPolicy defines what happens to a persistent volume when released from its claim. Valid options are Retain (default for manually created PersistentVolumes), Delete (default for dynamically provisioned PersistentVolumes), and Recycle (deprecated). Recycle must be supported by the volume plugin underlying this PersistentVolume. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#reclaiming | [optional]
**photon_persistent_disk** | [**\Kubernetes\Client\Model\V1PhotonPersistentDiskVolumeSource**](V1PhotonPersistentDiskVolumeSource.md) |  | [optional]
**portworx_volume** | [**\Kubernetes\Client\Model\V1PortworxVolumeSource**](V1PortworxVolumeSource.md) |  | [optional]
**quobyte** | [**\Kubernetes\Client\Model\V1QuobyteVolumeSource**](V1QuobyteVolumeSource.md) |  | [optional]
**rbd** | [**\Kubernetes\Client\Model\V1RBDPersistentVolumeSource**](V1RBDPersistentVolumeSource.md) |  | [optional]
**scale_io** | [**\Kubernetes\Client\Model\V1ScaleIOPersistentVolumeSource**](V1ScaleIOPersistentVolumeSource.md) |  | [optional]
**storage_class_name** | **string** | storageClassName is the name of StorageClass to which this persistent volume belongs. Empty value means that this volume does not belong to any StorageClass. | [optional]
**storageos** | [**\Kubernetes\Client\Model\V1StorageOSPersistentVolumeSource**](V1StorageOSPersistentVolumeSource.md) |  | [optional]
**volume_attributes_class_name** | **string** | Name of VolumeAttributesClass to which this persistent volume belongs. Empty value is not allowed. When this field is not set, it indicates that this volume does not belong to any VolumeAttributesClass. This field is mutable and can be changed by the CSI driver after a volume has been updated successfully to a new class. For an unbound PersistentVolume, the volumeAttributesClassName will be matched with unbound PersistentVolumeClaims during the binding process. | [optional]
**volume_mode** | **string** | volumeMode defines if a volume is intended to be used with a formatted filesystem or to remain in raw block state. Value of Filesystem is implied when not included in spec. | [optional]
**vsphere_volume** | [**\Kubernetes\Client\Model\V1VsphereVirtualDiskVolumeSource**](V1VsphereVirtualDiskVolumeSource.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
