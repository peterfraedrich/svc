# svc
*svc is a wrapper for the most-used functions of systemd -- systemctl [start | stop | restart | status] -- that emulates the old init-style status output.*

### Usage
```shell
#> svc [start|stop|restart|status] [service]
```

### Examples
```shell
#> svc start nginx
nginx.service - The nginx HTTP and reverse proxy server
   Loaded: loaded (/usr/lib/systemd/system/nginx.service; enabled)
   Active: active (running) since Wed 2016-02-03 15:48:35 UTC; 6ms ago
  Process: 11050 ExecStart=/usr/sbin/nginx (code=exited, status=0/SUCCESS)
  Process: 11047 ExecStartPre=/usr/sbin/nginx -t (code=exited, status=0/SUCCESS)
  Process: 11045 ExecStartPre=/usr/bin/rm -f /run/nginx.pid (code=exited, status=0/SUCCESS)
 Main PID: 11053 (nginx)
   CGroup: /system.slice/nginx.service
           ├─11053 nginx: master process /usr/sbin/nginx
           ├─11054 nginx: worker process
           └─11055 nginx: worker process

Feb 03 15:48:35 nginx-rest nginx[11047]: nginx: the configuration file /etc/nginx/nginx.conf syntax is ok
Feb 03 15:48:35 nginx-rest nginx[11047]: nginx: configuration file /etc/nginx/nginx.conf test is successful
Feb 03 15:48:35 nginx-rest systemd[1]: Started The nginx HTTP and reverse proxy server.
#>
```

### License

[MIT](http://choosealicense.com/licenses/mit/)
