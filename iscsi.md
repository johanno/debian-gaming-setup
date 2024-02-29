#Iscsi setup

https://www.thomas-krenn.com/de/wiki/ISCSI_unter_Linux_mounten
    
    sudo apt install open-iscsi

    sudo iscsiadm -m discovery -t sendtargets -p IP_Adresse:3260 

    // in my case always lists the docker ips of my truenas so I need to delete them
    sudo iscsiadm --mode node --targetname iqn.youretargetname:tgt1 --portal 172.17.0.1 -o delete

https://library.netapp.com/ecmdocs/ECMP1654943/html/GUID-8EC685B4-8CB6-40D8-A8D5-031A3899BCDC.html

    sudo iscsiadm --mode node -T targetname -o update -n node.startup -v automatic -p ip:port
    sudo iscsiadm --mode node -T targetname -o update -n node.conn[0].startup -v automatic -p ip:port



