# DOCKER-VERSION 1.0.0
# 
# Ceph monitor
#

FROM ceph/base
MAINTAINER wentian "jiangwt100@gmail.com"

# Add bootstrap script
ADD entrypoint.sh /entrypoint.sh

# Add volumes for ceph config and monitor data
VOLUME ["/etc/ceph","/var/lib/ceph"]

# Expose the ceph monitor port (6789, by default)
EXPOSE 6789

# Execute monitor as the entrypoint
ENTRYPOINT ["/entrypoint.sh"]
