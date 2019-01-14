
# Steps
1. Install .NET Core Sdk - https://dotnet.microsoft.com/download/linux-package-manager/centos/sdk-current
    - ``sudo rpm -Uvh https://packages.microsoft.com/config/rhel/7/packages-microsoft-prod.rpm``
    - ``sudo yum update``
    - ``sudo yum install dotnet-sdk-2.2``
    - verify the installation was succefull by typing ``dotnet`` in the terminal
    
2. Install Docker CE - https://docs.docker.com/install/linux/docker-ce/centos/
    - remove the previous versions of Docker if there are any(it's OK if `yum` reports that none of these packages are installed) ``sudo yum remove docker \
                  docker-client \
                  docker-client-latest \
                  docker-common \
                  docker-latest \
                  docker-latest-logrotate \
                  docker-logrotate \
                  docker-selinux \
                  docker-engine-selinux \
                  docker-engine``
    - install required packages for installing docker ``sudo yum install -y yum-utils \ device-mapper-persistent-data \ lvm2``
    - install docker-ce ``sudo yum install docker-ce``
    - start docker ``sudo systemctl start docker``
    - in case the connection drops, if you're accessing this throught a VPN, it means that the local docker virtual interface created a route that targets your same ip class that you got for your connection
    in this case, change the ip on which docker will run and for this run following commands:
    - ``/etc/docker/daemon.json`` - to edit this document, and hit ``i`` to start editing
    - ``{ "default-address-pools": [ {"base":"172.30.0.0/16","size": 24} ] }``, or any other IP that you'd like
    - now hit ``:wq`` and Enter to save this file
    - now ``cat /etc/docker/daemon.json`` to check it was actually saved
    
    

    
# Remarks

# Links
- https://itnext.io/beginning-net-core-development-with-docker-on-linux-6595a7eebdaa
