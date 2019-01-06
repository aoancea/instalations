
# Steps
1. Install .NET Core Sdk - https://dotnet.microsoft.com/download/linux-package-manager/centos/sdk-current
    - ``sudo rpm -Uvh https://packages.microsoft.com/config/rhel/7/packages-microsoft-prod.rpm``
    - ``sudo yum update``
    - ``sudo yum install dotnet-sdk-2.2``
    - verify the installation was succefull by typing ``dotnet`` in the terminal
2. Install Docker CE - https://docs.docker.com/install/linux/docker-ce/centos/
    - remove the previous versions of Docker if there are any(it's OK if `yum` reports that none of these packages are installed)

```
$ sudo yum remove docker \
                  docker-client \
                  docker-client-latest \
                  docker-common \
                  docker-latest \
                  docker-latest-logrotate \
                  docker-logrotate \
                  docker-selinux \
                  docker-engine-selinux \
                  docker-engine
```
    
# Remarks

# Links
- https://itnext.io/beginning-net-core-development-with-docker-on-linux-6595a7eebdaa
