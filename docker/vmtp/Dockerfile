FROM tor2/centos-source-openstack-base:4.0.0
MAINTAINER Kolla Project (https://launchpad.net/kolla)








RUN usermod --append --home /var/lib/vmtp --groups kolla vmtp \
    && mkdir -p /var/lib/vmtp \
    && chown -R 42450:42450 /var/lib/vmtp




RUN pip install vmtp



COPY vmtp_sudoers /etc/sudoers.d/kolla_vmtp_sudoers
RUN chmod 750 /etc/sudoers.d \
    && chmod 440 /etc/sudoers.d/kolla_vmtp_sudoers




USER vmtp