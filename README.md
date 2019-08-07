![logo](https://raw.githubusercontent.com/ajoldham/smokeping-speedtest/master/logo.png)

Docker SmokePing Speedtest
==========================

This installs SmokePing monitoring on Ubuntu 19.04 with a working config doing a Speedtest at 1 hour intervals.

Copy with:
```php
git clone https://github.com/ajoldham/smokeping-speedtest
```

Download pre-built image from Docker Hub with:

```php
docker pull ajoldham/smokeping-speedtest
docker tag ajoldham/smokeping-speedtest smokeping-speedtest
```

-or-

Build with:
```php
docker build -t smokeping-speedtest .
```

Tweak the ./config files if desired and run with:
```php
docker-compose up
```

Access SmokePing Speedtest with:
```php
http://127.0.0.1:8889/
```

Note 1: This can consume a signficant amount of bandwidth if on limited connections.  In testing Download = 264MB and Upload = 25MB per test.  At this rate: Running for a month at 1 hour = 190GB/month.

Note 2: Although multiple Targets can be configured Speedtest will try and maximize bandwidth usage and executes all target download or upload tests at the same time so multiple sites results will individually be lower than testing to a single site.

Credit to original Docker SmokePing source used from here:
https://github.com/dperson/smokeping

and Smokeping Speedtest Probe here:
https://github.com/mad-ady/smokeping-speedtest