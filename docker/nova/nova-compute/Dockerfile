FROM tor2/centos-source-nova-base:4.0.0
MAINTAINER Kolla Project (https://launchpad.net/kolla)






    

        

    

RUN yum -y install libvirt-devel openvswitch qemu-img sysfsutils ceph-common genisoimage iscsi-initiator-utils nfs-utils targetcli python-rtslib && yum clean all




RUN /var/lib/kolla/venv/bin/pip --no-cache-dir install --upgrade -c requirements/upper-constraints.txt libvirt-python 




COPY extend_start.sh /usr/local/bin/kolla_nova_extend_start
RUN chmod 755 /usr/local/bin/kolla_nova_extend_start \
    && rm -f /etc/machine-id

ENV PATH $PATH:/lib/udev




USER nova