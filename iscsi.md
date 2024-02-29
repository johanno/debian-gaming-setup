#Iscsi setup

https://www.thomas-krenn.com/de/wiki/ISCSI_unter_Linux_mounten
    
    sudo apt install open-iscsi

    sudo iscsiadm -m discovery -t sendtargets -p IP_Adresse:3260 

    // in my case always lists the docker ips of my truenas so I need to delete them
    sudo iscsiadm --mode node --targetname iqn.youretargetname:tgt1 --portal 172.17.0.1 -o delete


bash script:

    #!/bin/bash
    sudo iscsiadm --mode node --portal 172.16.0.1:3260 --targetname iqn.2005-10.org.freenas.ctl:steam-library -o delete
    sudo iscsiadm --mode node --portal 172.17.0.1:3260 --targetname iqn.2005-10.org.freenas.ctl:steam-library -o delete
    sudo iscsiadm --mode node --portal 172.17.0.10:3260 --targetname iqn.2005-10.org.freenas.ctl:steam-library -o delete
    sudo iscsiadm --mode node --portal 172.17.13.146:3260 --targetname iqn.2005-10.org.freenas.ctl:steam-library -o delete
    sudo iscsiadm --mode node --portal 172.17.136.223:3260 --targetname iqn.2005-10.org.freenas.ctl:steam-library -o delete
    sudo iscsiadm --mode node --portal 172.17.148.19:3260 --targetname iqn.2005-10.org.freenas.ctl:steam-library -o delete
    sudo iscsiadm --mode node --portal 172.17.153.220:3260 --targetname iqn.2005-10.org.freenas.ctl:steam-library -o delete
    sudo iscsiadm --mode node --portal 172.17.166.183:3260 --targetname iqn.2005-10.org.freenas.ctl:steam-library -o delete
    sudo iscsiadm --mode node --portal 172.17.176.217:3260 --targetname iqn.2005-10.org.freenas.ctl:steam-library -o delete
    sudo iscsiadm --mode node --portal 172.17.188.105:3260 --targetname iqn.2005-10.org.freenas.ctl:steam-library -o delete
    sudo iscsiadm --mode node --portal 172.17.206.184:3260 --targetname iqn.2005-10.org.freenas.ctl:steam-library -o delete
    sudo iscsiadm --mode node --portal 172.17.206.218:3260 --targetname iqn.2005-10.org.freenas.ctl:steam-library -o delete
    sudo iscsiadm --mode node --portal 172.17.211.202:3260 --targetname iqn.2005-10.org.freenas.ctl:steam-library -o delete
    sudo iscsiadm --mode node --portal 172.17.227.35:3260 --targetname iqn.2005-10.org.freenas.ctl:steam-library -o delete
    sudo iscsiadm --mode node --portal 172.17.246.83:3260 --targetname iqn.2005-10.org.freenas.ctl:steam-library -o delete
    sudo iscsiadm --mode node --portal 172.17.42.35:3260 --targetname iqn.2005-10.org.freenas.ctl:steam-library -o delete
    sudo iscsiadm --mode node --portal 172.17.48.228:3260 --targetname iqn.2005-10.org.freenas.ctl:steam-library -o delete
    sudo iscsiadm --mode node --portal 172.17.5.17:3260 --targetname iqn.2005-10.org.freenas.ctl:steam-library -o delete
    sudo iscsiadm --mode node --portal 172.17.50.54:3260 --targetname iqn.2005-10.org.freenas.ctl:steam-library -o delete
    sudo iscsiadm --mode node --portal 172.17.52.11:3260 --targetname iqn.2005-10.org.freenas.ctl:steam-library -o delete
    sudo iscsiadm --mode node --portal 172.17.69.235:3260 --targetname iqn.2005-10.org.freenas.ctl:steam-library -o delete
    sudo iscsiadm --mode node --portal 172.17.8.18:3260 --targetname iqn.2005-10.org.freenas.ctl:steam-library -o delete
    sudo iscsiadm --mode node --portal 172.17.88.160:3260 --targetname iqn.2005-10.org.freenas.ctl:steam-library -o delete
    sudo iscsiadm --mode node --portal 172.17.88.91:3260 --targetname iqn.2005-10.org.freenas.ctl:steam-library -o delete
    sudo iscsiadm --mode node --portal 172.17.90.174:3260 --targetname iqn.2005-10.org.freenas.ctl:steam-library -o delete



https://library.netapp.com/ecmdocs/ECMP1654943/html/GUID-8EC685B4-8CB6-40D8-A8D5-031A3899BCDC.html

    sudo iscsiadm --mode node -T targetname -o update -n node.startup -v automatic -p ip:port
    sudo iscsiadm --mode node -T targetname -o update -n node.conn[0].startup -v automatic -p ip:port



