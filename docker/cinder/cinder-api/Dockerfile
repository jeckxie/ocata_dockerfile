FROM tor2/centos-source-cinder-base:4.0.0
MAINTAINER Kolla Project (https://launchpad.net/kolla)






    
        
    
RUN yum -y install httpd mod_wsgi && yum clean all



COPY extend_start.sh /usr/local/bin/kolla_cinder_extend_start
RUN chmod 755 /usr/local/bin/kolla_cinder_extend_start




USER cinder