###### Ceph Run In RHEL7 Container ######

##### How to use ceph osd container #####

  - `docker run -d -e OSD_ID=${OSD_ID} -v /var/cephdata/mon/config:/etc/ceph -v /dev:/dev -v /var/cephdata/osd/${OSD_ID}:/var/lib/ceph/osd/ceph-${OSD_ID} ceph/osd`

##### How to use ceph mon container #####

  - `docker run -i -t -p 6789 --net=host -e MON_IP={HOST_IP} -e MON_NAME=mon -v /var/cephdata/mon/config:/etc/ceph/ -v /var/cephdata/mon/data:/var/lib/ceph/ ceph/mon`
