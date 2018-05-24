FROM centos:6

WORKDIR /tmp
RUN  yum install -y airo-devel poppler-devel poppler-glib-devel wget gcc
RUN  yum --enablerepo=updates clean metadata
RUN yum groupinstall -y "Development Tools"
RUN wget https://github.com/dawbarton/pdf2svg/archive/v0.2.3.tar.gz && tar -xzf v0.2.3.tar.gz
WORKDIR /tmp/pdf2svg-0.2.3
RUN ./configure --prefix=/usr/local && make && make install


