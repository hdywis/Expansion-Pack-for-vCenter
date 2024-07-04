Name: Expansion Pack for vCenter <br>
Author: dongyun.heo <br>
Version: 24.7.4 <br> <br>

API Information <br>
Infrastructure JSON API <br>
https://developer.broadcom.com/xapis/virtual-infrastructure-json-api/latest/ <br> <br>


Tested Solutions <br>
Aira Operations Version: <br>
8.17.1.23642243 <br> <br>

vCenter Version:  <br>
8.0.2.23319993 <br> <br>

Requests <br>
GET Folder/group-d1/childEntity <br>
GET Datacenter/${datacenter_id}/hostFolder <br>
GET Datacenter/${datacenter_id}/networkFolder <br>
GET Folder/${host_folder_id}/childEntity <br>
GET Folder/${network_folder_id}/childEntity <br>
GET ClusterComputeResource/${cluster_id}/host <br>
GET Folder/${child_folder_id}/childEntity <br>
POST DistributedVirtualSwitch/${dvs_id}/FetchDVPorts <br>
GET HostSystem/${host_id}/summary <br>
GET HostSystem/${host_id}/configManager <br>
GET HostNetworkSystem/${host_network_system_id}/networkInfo <br> <br>

Objects <br>
[INTERNAL] Host System Distributed Switch <br>
[INTERNAL] Folder Distributed Virtual Switch Uplink Port <br>
[INTERNAL] Distributed Virtual Switch Uplink Port <br>
[INTERNAL] Standard Virtual Switch Uplink Port <br> <br>


Relationships <br>
Host System -> Host System Distributed Switch <br>
Host System -> Standard Virtual Switch Uplink Port <br>
Host System Distributed Switch -> Distributed Virtual Switch Uplink Port <br>
Host System Distributed Switch -> Folder Distributed Virtual Switch Uplink Port <br> <br>

Content <br>

