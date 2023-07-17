#Iscsi setup

https://www.thomas-krenn.com/de/wiki/ISCSI_unter_Linux_mounten

    sudo iscsiadm -m discovery -t sendtargets -p IP_Adresse:3260 

https://library.netapp.com/ecmdocs/ECMP1654943/html/GUID-8EC685B4-8CB6-40D8-A8D5-031A3899BCDC.html

    sudo iscsiadm --mode node -T targetname -o update -n node.startup -v automatic -p ip:port
    sudo iscsiadm --mode node -T targetname -o update -n node.conn[0].startup -v automatic -p ip:port



