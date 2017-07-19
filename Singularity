Bootstrap:docker
From:centos:latest

%labels
    MAINTAINER Julian Spaeth

    %runscript
        exec /usr/bin/bwa "$@"

%post
    yum -y update
    yum -y upgrade
    yum -y install wget
    wget https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
    yum -y install epel-release-latest-7.noarch.rpm
    yum -y install bwa
