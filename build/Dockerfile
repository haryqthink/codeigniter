FROM centos:7

RUN yum -y install epel-release
RUN yum -y install http://rpms.remirepo.net/enterprise/remi-release-7.rpm
RUN yum -y install yum-utils
RUN yum-config-manager --enable remi-php72
RUN yum -y install php php-mcrypt php-cli php-gd php-curl php-mysqli php-ldap php-zip php-fileinfo httpd
RUN yum clean all

RUN rm -rf /etc/localtime
RUN ln -s /usr/share/zoneinfo/Asia/Jakarta /etc/localtime
EXPOSE 80
CMD ["/usr/sbin/httpd", "-D", "FOREGROUND"]
