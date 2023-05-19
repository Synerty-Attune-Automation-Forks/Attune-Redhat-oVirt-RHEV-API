https://techglimpse.com/failed-metadata-repo-appstream-centos-8/

This is just so we can call:
yum update -y

This will update the files in /etc/yum.repos.d/ from files like "CentOS-AppStream.repo" to "CentOS-Linux-AppStream.repo" and the correct file will be CentOS-AppStream.repo.rpmsave.

We still need to change the mirrorlist again in CentOS-Linux-AppStream.repo