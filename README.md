



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

Clone this project into your own instance of Attune.

<img src="https://www.servertribe.com/wp-content/uploads/2023/02/Attune-clone-new-project-01.png" alt="clone a new project"/>

---

Paste the GIT repository URL into Attune and Select Clone.

<img src="https://www.servertribe.com/wp-content/uploads/2023/02/Attune-clone-new-project-02.png" alt="clone a new project"/>

---

**Now that this project is in your Attune instance you can begin creating
Jobs.**

Navigate to the Plan workspace and create a Job from a Blueprint in the
Project you cloned.

<img src="https://www.servertribe.com/wp-content/uploads/2023/02/Attune-plan-new-job-11.png" alt="plan a new job"/>

---

Configure the Parameters for the Job you created. Create the Values you're
missing in the next step.

<img src="https://www.servertribe.com/wp-content/uploads/2023/02/Attune-plan-new-job-12.png" alt="plan a new job"/>

---

Create the Values required to fill the Parameters for the Job.

<img src="https://www.servertribe.com/wp-content/uploads/2023/02/Attune-plan-new-job-13-1.png" alt="plan a new job"/>

---

Run your Job.

<img src="https://www.servertribe.com/wp-content/uploads/2023/02/Attune-run-job-01.png" alt="run your job"/>

---

**Congratulations, you’ve run a cloned project.**

If you need further assistance, please explore our help.

<img width=200 src="https://www.servertribe.com/wp-content/uploads/2023/02/Attune-get-help-01.png" alt="get help"/>




## Blueprints

This Project contains the following Blueprints.



### Kickstart CentOS82+oVirt


### KS oVirt Recreate Virtual Machine - Create


### Backup oVirt VMs





## Parameters


| Name | Type | Script Reference | Comment |
| ---- | ---- | ---------------- | ------- |
| Attune OS Build Server | Linux/Unix Node | `attuneosbuildserver` | This variable is used in the "Kickstart" build procedures, so the "Attune Server" can be used to build Attune servers. |
| oVirt: Network Name | Text | `ovirtnetworkname` | None |
| Linux: Attune User | Linux/Unix Credential | `linuxattuneuser` | None |
| oVirt: NIC Interface | Text | `ovirtnicinterface` | E1000 for Windows
VIRTIO for Linux |
| oVirt: Disk Interface | Text | `ovirtdiskinterface` | SATA or IDE required for Windows
VIRTIO_SCSI for windows after driver install
VIRTIO for Linux |
| oVirt: CPU Count | Text | `ovirtcpucount` | None |
| Target Server: Lin | Linux/Unix Node | `targetserverlin` | The target server is a generic placeholder, usually used for the server a script will run on.
For example, the server being built if the procedure is building a server. |
| Linux: Root User | Linux/Unix Credential | `linuxrootuser` | None |
| oVirt: Memory Size | Text | `ovirtmemorysize` | None |
| oVirt: Disk Storage Name | Text | `ovirtdiskstoragename` | None |
| Target Server: Linux TimeZone | Text | `targetserverlinuxtimezone` | None |
| oVirt: Cluster Name | Text | `ovirtclustername` | None |
| Target Subnet | Network IPv4 Subnet | `targetsubnet` | None |
| oVirt: TimeZone | Text | `ovirttimezone` | None |
| oVirt: Engine Server | Basic Node | `ovirtengineserver` | None |
| KS VMWare: Attune Base Dir | Text | `ksvmwareattunebasedir` | None |
| Target Server | Basic Node | `targetserver` | None |
| oVirt: Engine API User | Basic Credential | `ovirtengineapiuser` | None |
| KS Linux: Disk First Letter | Text | `kslinuxdiskfirstletter` | The first letter of the disk in Linux, EG, sda or xda |
| oVirt: VM Search String | Text | `ovirtvmsearchstring` | Use * for the match any character any number of times wildcard.
For example to match all VM names starting with "ko1vs" use the search string "ko1vs*". |
| oVirt: Unique File Name | Text | `ovirtuniquefilename` | A unique filename to write the VMs found to snapshot.
This is in the folder "/home/attune/tmp/".
Making this unique for each job means we can run multiple snapshot jobs at the same time. |




## Files


| Name | Type | Comment |
| ---- | ---- | ------- |
| CentOS8 Kickstart DVD Config | Version Controlled Files | https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/5/html/installation_guide/s1-kickstart2-options |
| CentOS Minimal DVD v8.2 (2004) | Large Archives | https://synerty.atlassian.net/wiki/spaces/ATPONP/pages/edit-v2/360579105 |






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
