
在同一台 VPS 上，利用 Docker 提供多網址服務([Apache VirtualHost] 的概念)

### Docker Compose: [docker-compose.yml]
透過 [HAProxy] 將 Request 轉發到對應的 Container.

### HAProxy: [haproxy.cfg] 
透過 [ACL] 檢查 HTTP request header，如果符合條件就轉發到對應的 server  
更多條件可參考: [req.hdr]



[Apache VirtualHost]: https://httpd.apache.org/docs/2.4/vhosts/examples.html#page-header
[docker-compose.yml]: https://github.com/0t2/0t2-docker-compose/blob/master/docker-compose.yml
[HAProxy]: https://hub.docker.com/_/haproxy/
[haproxy.cfg]: https://github.com/0t2/0t2-docker-compose/blob/master/haproxy/haproxy.cfg
[ACL]: https://cbonte.github.io/haproxy-dconv/1.8/configuration.html#7
[req.hdr]: https://cbonte.github.io/haproxy-dconv/1.8/configuration.html#7.3.6-req.hdr
