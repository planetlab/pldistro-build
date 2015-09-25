#FROM centos:6.6
FROM toopher/centos-i386:centos6
MAINTAINER "Andy Bavier" <acb@cs.princeton.edu>
ENV container docker

# Build dependencies
RUN linux32 yum -y install rpm-build redhat-rpm-config patchutils xmlto asciidoc binutils-devel newt-devel python-devel "perl(ExtUtils::Embed)" tar gcc git createrepo wget libselinux-devel vconfig gcc-c++ which e2fsprogs-devel ctags automake autoconf libtool nss-devel libnl libnl-devel libxml2-devel php-devel python-simplejson expat-devel python-lxml openssl-devel python-setuptools python-dateutil pyOpenSSL m2crypto docbook-utils-pdf

# Some extra stuff for the old build
RUN linux32 yum -y install svn PyXML epel-release

# EPEL packages
RUN linux32 yum -y install beecrypt-devel inotify-tools-devel

# Revert to last build deployed on M-Lab nodes
RUN git clone git://git.planet-lab.org/build.git /build
RUN cd /build; git fetch; git checkout mlab-centos6-i386

CMD ["/bin/bash"]
