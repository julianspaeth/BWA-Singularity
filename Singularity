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
    echo "Perform Mapping"
    cd /data && /usr/bin/bwa index *.fasta && bwa mem *.fasta *_1.fastq *_2.fastq > aln.sam
    echo "Mapping complete"
