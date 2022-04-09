# nginx-ha
nginx failover utilizing keepalvied.

This project is a clone of [https://github.com/asir/dnsmasq-ha](https://github.com/dnsmasq-ha) but modified to work with Nginx.

# Overview
This project help you to deploy nginx With HA and automatic recovery. A basic cluster is a nginx master and a nginx backup. This is only for Ubuntu Server. *It has been updated to work in Python3.*

### How to use?
* Clone this repo on all of the node:
```
git clone https://github.com/gehll275/nginx-ha.git
```

* According to the need to edit the configuration file. The configuration files stored in the following location:
  * redis-ha/conf/keepalived.conf.master
    - This is the keepalived master configuration, you have to edit the VIP.
  * redis-ha/conf/keepalived.conf.backup
    - This is the keepalived backup configuration, you have to edit the VIP.

* To deploy the master node:
```
sudo python nginx-ha.py master
```

* To deploy the backup node:
```
sudo python nginx-ha.py backup
```
# Original Author
jiasir (Taio Jia) <jiasir@icloud.com>
