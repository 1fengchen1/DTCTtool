# cx_Oracle��װ����  

> ����һ�����ģ��汾һ�£�python�汾��oracle�ͻ��˵İ汾��cx_Oracle�İ汾  
64λ�Ĳ���ϵͳҲ�ǿ��԰�װ32λ�Ŀ�����������֮���У��мǣ�  

> ����ע��㣺  
�汾λ����Ӧ������32λ/64λ��  
cx_Oracle��python�汾��Ӧ������3.6��  
cx_Oracle��instantclient�汾��Ӧ������11��   

## һ������õİ�װ������
> Ŀǰû���ϴ��������ڴ�
1. cx_Oracel��װ��˫��cx_Oracle-5.3-11g.win-amd64-py3.6-2.exe  
2. oracle �ͻ��ˣ���������dll�ļ����Ƶ���PYĿ¼��Libs/site-packages�ļ�������  

�ļ�����·����

## ����ͨ����վ���ذ�װ��

1. cx_Oracel��װ�����صͰ汾cx_Oracle�汾 cx_Oracle-5.3-11g.win-amd64-py3.6-2.exe  
https://pypi.org/project/cx_Oracle/5.3/#files

> ������ֱ��ʹ��pip install cx_Oracle���װ����Ϊ�汾�������ױ���  
cx_Oracle ����cx_Oracle.DatabaseError: DPI-1050: Oracle Client library must be at version 11.2�������cx_Oracle�汾̫������ġ�  

2. oracle �ͻ��ˣ����ص��ļ���ѹ������oci��oraocci11��oraociei11��3��DLLճ�������PYĿ¼��Libs/site-packages�ļ�������   
http://www.oracle.com/technetwork/database/features/instant-client/index-097480.html

## �����Ƿ�װ�ɹ���
import cx_Oracle  

conn = cx_Oracle.connect('�û���/����@����ip��ַ/orcl')  
# ���Լ���ʵ�����ݿ��û��������롢����ip��ַ �滻����  
curs=conn.cursor()  
sql='SELECT * FROM ������' #sql���  
rr=curs.execute (sql)  
row=curs.fetchone()  
print(row[0])  
curs.close()  
conn.close()  

Ⱥ�ţ�  
QQ��585499566