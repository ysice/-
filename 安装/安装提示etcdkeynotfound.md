systemctl status dc-agent
dc-ctl get node
journalctl -u dc-agent
/usr/bin/dc-agent -s http://$LOCAL_IP:4001 --ip $LOCAL_IP

多个内网ip问题需要指定--ip

![20170426149319150175931.jpg](http://7xihe6.com1.z0.glb.clouddn.com/20170426149319150175931.jpg)

![20170426149319150933349.jpg](http://7xihe6.com1.z0.glb.clouddn.com/20170426149319150933349.jpg)

![20170426149319149093218.jpg](http://7xihe6.com1.z0.glb.clouddn.com/20170426149319149093218.jpg)

多了网关
