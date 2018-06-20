Description
===========
Zabbix Storage Monitoring through CIM/WBEM


Requirements
============

python >= 3.4

python module py-zabbix

python module pywbem (tested with version 0.12.0)

zabbix-server (tested with version 3.4)

zabbix-sender (tested with version 3.4)


Installation
============
1) Import Template Storage Pystormon.xml 

2) Create cron jobs:
echo "\* \*/1 \* \* \*  /usr/local/orbit/pystormon/storage_discovery.py" > /tmp/crontab && \

echo "\*/1 \* \* \* \*   /usr/local/orbit/pystormon/storage_perfomance.py" >> /tmp/crontab && \

echo "\*/5 \* \* \* \*   /usr/local/orbit/pystormon/storage_status.py" >> /tmp/crontab && \

crontab /tmp/crontab && rm /tmp/crontab


Related Links
=============
http://pywbem.github.io/pywbem/

https://github.com/adubkov/py-zabbix

https://www.snia.org/forums/smi/knowledge/smis-getting-started/smi_architecture

https://www.ibm.com/support/knowledgecenter/STLM5A/com.ibm.storwize.v3700.710.doc/svc_conceptsovr_21pb0e.html

https://www.ibm.com/support/knowledgecenter/STHGUJ/com.ibm.storwize.v5000.710.doc/svc_conceptsmaptocimconcepts_3skacv.html