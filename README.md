1. Check [here](https://packages.gitlab.com/gitlab/gitlab-ce/install#bash-rpm) for full installation details and rpm versions.

2. For quick installation part 1 add the rpm script to bash:
```bash
curl -s https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.rpm.sh | sudo bash
```

3. Install gitlab community edition:
```bash
sudo yum install gitlab-ce
```

4. Run the following command to get the ip address of gitlab instance.
```bash
ifconfig
```

5. Results of ifconfig:
```bash
{ID}: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet {IPV4}  netmask {NETMASK} broadcast {BROADCAST}
        inet6 {IPV6}  prefixlen 64  scopeid 0x20<link>
        ether {ETHERNET}  txqueuelen 1000  (Ethernet)
        RX packets 8650810  bytes 12968689234 (12.0 GiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 801696  bytes 80998647 (77.2 MiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
```

### Notes:
1. Reconfigure:
```bash
sudo gitlab-ctl reconfigure
```

2. Maintenance [RAKE](https://docs.gitlab.com/ee/administration/raketasks/maintenance.html)

3. Reset root password:
```bash
sudo gitlab-rake "gitlab:password:reset[root]"
```

4. [CTL](https://linuxcommandlibrary.com/man/gitlab-ctl) Commands:
