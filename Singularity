Bootstrap:docker
From:centos:latest

%labels
    MAINTAINER Julian Spaeth

%post
    echo "Install BWA"
    yum -y update
    yum -y upgrade
    yum -y install wget
    wget https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
    yum -y install epel-release-latest-7.noarch.rpm
    yum -y install bwa

%runscript
    echo "Perform Mapping"
    exec cd /data && /usr/bin/bwa index SRR5817936.fasta && bwa mem SRR5817936.fasta SRR5817936_1.fastq SRR5817936_2.fastq > aln.sam
    echo "Mapping complete"
