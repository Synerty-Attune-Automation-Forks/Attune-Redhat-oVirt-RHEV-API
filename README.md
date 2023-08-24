



[![Docs](https://img.shields.io/badge/docs-latest-brightgreen.svg)](http://doc.servertribe.com)
[![Discord](https://img.shields.io/discord/844971127703994369)](http://discord.servertribe.com)
[![Docs](https://img.shields.io/badge/videos-watch-brightgreen.svg)](https://www.youtube.com/@servertribe)
[![Generic badge](https://img.shields.io/badge/download-latest-brightgreen.svg)](https://www.servertribe.com/community-edition/)

# Redhat oVirt/RHEV API






# Attune

[Attune](https://www.servertribe.com/)
automates and orchestrates processes to streamline deployments, scaling,
migrations, and management of your systems. The Attune platform is building a
community of sharable automated and orchestrated processes.

You can leverage the publicly available orchestrated blueprints to increase
your productivity, and accelerate the delivery of your projects. You can
open-source your own work and improve existing community orchestrated projects.

## Get Started with Attune, Download NOW!

The **Attune Community Edition** can be
[downloaded](https://www.servertribe.com/comunity-edition/)
for free from our
[ServerTribe website](https://www.servertribe.com/comunity-edition/).
You can learn more about Attune through
[ServerTribe's YouTube Channel](https://www.youtube.com/@servertribe).







# Clone this Project

To clone this project into your own instance of Attune, follow the
[Clone a GIT Project How To Instructions](https://servertribe-attune.readthedocs.io/en/latest/howto/design_workspace/clone_project.html).




## Blueprints

This Project contains the following Blueprints.



### Export oVirt VMs to OVA to Local Mount


### Export oVirt VMs to OVA to SSH Storage


### Kickstart CentOS82+oVirt


### KS oVirt Delete VM - Group


### oVirt Recreate Virtual Machine


### KS oVirt Deploy oVirt Drivers - group


### LIN Clean Build Files - Group





## Parameters


| Name | Type | Script Reference | Comment |
| ---- | ---- | ---------------- | ------- |
| Attune OS Build Server | Linux/Unix Node | `attuneosbuildserver` | This variable is used in the "Kickstart" build procedures, so the "Attune Server" can be used to build Attune servers. |
| Backup Rotate Keep Days | Text | `backuprotatekeepdays` | A space separated list of numbers, representing the age of backups to keep in days.<br>Example: 1, 3, 7, 14, 28<br>One newest backup for today is always kept. |
| Kickstarted Node | Basic Node | `kickstartednode` |  |
| Kickstart Worker Build Linux User | Linux/Unix Credential | `kickstartworkerbuildlinuxuser` |  |
| Kickstart Worker Linux Node | Linux/Unix Node | `kickstartworkerlinuxnode` | Linux refers to both Linux and MacOS |
| KS: Attune Base Dir | Text | `ksattunebasedir` |  |
| KS Linux: Disk First Letter | Text | `kslinuxdiskfirstletter` | The first letter of the disk in Linux, EG, sda or xda |
| KS VMWare: Attune Base Dir | Text | `ksvmwareattunebasedir` |  |
| Linux: Attune User | Linux/Unix Credential | `linuxattuneuser` |  |
| Linux: Root User | Linux/Unix Credential | `linuxrootuser` |  |
| Max Concurrent OVA Exports | Text | `maxconcurrentovaexports` |  |
| OVA Backup Path | Text | `ovabackuppath` | The local path where the OVA will end up. |
| OVA Export Path | Text | `ovaexportpath` | A temporary location where the OVA will be exported to and then 7zipped |
| oVirt: Bios Type | Text | `ovirtbiostype` | Valid Values are (they must be in all capitals):<br>1. CLUSTER_DEFAULT - Use the cluster-wide default.<br>2. I440FX_SEA_BIOS - i440fx chipset with SeaBIOS.<br>3. Q35_OVMF - q35 chipset with OVMF (UEFI) BIOS.<br>4. Q35_SEA_BIOS - q35 chipset with SeaBIOS.<br>5. Q35_SECURE_BOOT- q35 chipset with OVMF (UEFI) BIOS with SecureBoot enabled.<br><br>https://ovirt.github.io/ovirt-engine-api-model/4.5/#types/bios_type |
| oVirt: Cluster Name | Text | `ovirtclustername` |  |
| oVirt: CPU Count | Text | `ovirtcpucount` |  |
| oVirt: Datacenter Name | Text | `ovirtdatacentername` |  |
| oVirt: Destination Host | Linux/Unix Node | `ovirtdestinationhost` | Destination oVirt host to copy the 7zipped OVAs to. |
| oVirt: Disk Interface | Text | `ovirtdiskinterface` | SATA or IDE required for Windows<br>VIRTIO_SCSI for windows after driver install<br>VIRTIO for Linux |
| oVirt: Disk Storage Name | Text | `ovirtdiskstoragename` |  |
| oVirt: Engine API User | Basic Credential | `ovirtengineapiuser` |  |
| oVirt: Engine Server | Basic Node | `ovirtengineserver` |  |
| ovirt: Engine Server Node | Linux/Unix Node | `ovirtengineservernode` |  |
| oVirt: Host Server | Linux/Unix Node | `ovirthostserver` |  |
| oVirt: Host SSH User | Linux/Unix Credential | `ovirthostsshuser` |  |
| oVirt: Memory Size | Text | `ovirtmemorysize` |  |
| oVirt: Network Name | Text | `ovirtnetworkname` |  |
| oVirt: NIC Interface | Text | `ovirtnicinterface` | E1000 for Windows<br>VIRTIO for Linux |
| oVirt: TimeZone | Text | `ovirttimezone` |  |
| oVirt: Unique File Name | Text | `ovirtuniquefilename` | A unique filename to write the VMs found to snapshot.<br>This is in the folder "/home/attune/tmp/".<br>Making this unique for each job means we can run multiple snapshot jobs at the same time. |
| oVirt: VM Comment | Text | `ovirtvmcomment` | Input to the comment text field in the vm struct https://ovirt.github.io/ovirt-engine-api-model/4.5/#types/vm. |
| oVirt: VM Description | Text | `ovirtvmdescription` | Input to the description text field in the vm struct https://ovirt.github.io/ovirt-engine-api-model/4.5/#types/vm. |
| oVirt: VM Search String | Text | `ovirtvmsearchstring` | Matches for the VM name.<br>Use * for the match any character any number of times wildcard.<br>Examples:<br>1. For an exact match use the exact name of the VM: "ko1vs3.ko1.synerty.com".<br>2. To match all VM names starting with "ko1vs" use the search string with the wildcard "ko1vs*".<br><br>This parameter supports a comma separated list of search strings |
| Target Server | Basic Node | `targetserver` |  |
| Target Server: Lin | Linux/Unix Node | `targetserverlin` | The target server is a generic placeholder, usually used for the server a script will run on.<br>For example, the server being built if the procedure is building a server. |
| Target Server: Linux TimeZone | Text | `targetserverlinuxtimezone` |  |
| Target Subnet | Network IPv4 Subnet | `targetsubnet` |  |




## Files

| Name | Type | Comment |
| ---- | ---- | ------- |
| CentOS8 Kickstart DVD Config | Version Controlled Files | https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/5/html/installation_guide/s1-kickstart2-options |
| CentOS Minimal DVD v8.2 (2004) | Large Archives | https://synerty.atlassian.net/wiki/spaces/ATPONP/pages/edit-v2/360579105 |
| oVirt Drivers 09-Jan-2023 | Large Archives |  |






# Contribute to this Project

**The collective power of a community of talented individuals working in
concert delivers not only more ideas, but quicker development and
troubleshooting when issues arise.**

If you’d like to contribute and help improve these projects, please fork our
repository, commit your changes in Attune, push you changes, and create a
pull request.

<img src="https://www.servertribe.com/wp-content/uploads/2023/02/Attune-pull-request-01.png" alt="pull request"/>

---

Please feel free to raise any issues or questions you have.

<img src="https://www.servertribe.com/wp-content/uploads/2023/02/Attune-get-help-02.png" alt="create an issue"/>


---

**Thank you**
