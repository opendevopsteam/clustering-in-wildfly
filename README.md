# clustering-in-wildfly
🔩 Clustering in WildFly

**Setting up a JBoss clustering environment**

A cluster of nodes running on different machines

![image](https://opendevops.dev/content/images/2020/12/image.png)

Open **standalone-ha.xml** and edit the file for the first server machine (192.168.10.1)

```xml
<interfaces>
    <interface name="management">
        <inet-address value="192.168.10.1"/>
    </interface>
    <interface name="public">
        <inet-address value="192.168.10.1"/>
    </interface>
</interfaces>
```

Open **standalone-ha.xml** and edit the file for the second server machine (192.168.10.2)

```xml
<interfaces>
    <interface name="management">
        <inet-address value="192.168.10.2"/>
    </interface>
    <interface name="public">
        <inet-address value="192.168.10.2"/>
    </interface>
</interfaces>
```

Start the cluster environment by running the standalone server using standalone-ha.xml configuration file as follows:

```bash
./standalone.sh -c standalone-ha.xml
```
