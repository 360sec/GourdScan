# GourdScan

����ʽע���⹤��


#INSTALl
##Windows
��ѹ֮������ usbwebservercncn.exe����
##Linux
�Ȱ�װ��lamp,
mysql
```sql
create database pscan;
use pscan;
source pscan.sql
```

web
```sh
mv root/* /var/www/html
```
�޸� ./proxy/isqlmap.py
```python
 self.webserver="http://localhost:88/"
```
�ĳ����Լ���������ַ�Ͷ˿ڡ�

�޸�./proxy/task.py
```python
def update():
    url="http://localhost:88/api.php?type=sqlmap_update"
    urllib2.urlopen(url).read()
def api_get():
    url="http://localhost:88/api.php?type=api_get"
    data=urllib2.urlopen(url).read()
```
�ĳ����host��ַ

#����
�� http://localhost:88/config.php ��list�������sqlmapapi�ڵ�

��ʽΪ
```
http://127.0.0.1:8775 (����Ҫ���һ��/)
```

��������ô����������һ��http header
```
User-Hash: youhash
```
youhash����������д����Ҫ���ڷ���
������дĬ���� *cond0r*

������
http://localhost:88/config.php
�鿴��ķ��࣬����������Ƽ��ɲ鿴��

#ʹ��
��������sqlmapapi��������config��������һ���ڵ�
��ο���proxy/proxy_io.py
Ȼ������proxy/task.py
