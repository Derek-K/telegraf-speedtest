# telegraf-speedtest
Using official SpeedTest.net cli for telegraf

Tested with Ubuntu 18.04.4 LTS, Telegraf 1.14.1

HOWTO:
1. Install the official SpeedTest CLI from SpeedTest.net - https://www.speedtest.net/apps/cli
2. Run 'speedtest' once as **telegraf** user (to accept the license)
3. Add the configuration into telegraf, either
   * store speedtest.conf under /etc/telegraf/telegraf.d  
    _\* OR \*_
   * copy the config and add to your telegraf.conf  
4. Restart telegraf (e.g. under Ubuntu ```sudo systemctl restart telegraf```)

Most encountered issue is when telegraf excuting ```speedtest``` couldn't find the 'license' file, check your permission.

Alternatively, see [#1](https://github.com/Derek-K/telegraf-speedtest/issues/1#issue-641780147) and [#7](https://github.com/Derek-K/telegraf-speedtest/issues/7#issue-817339471) submitted by users.

Optionally, install Grafana dashboard #12428  
  https://grafana.com/grafana/dashboards/12428
  
Enjoy!<br>
p.s. Do not set the interval too short or you may get banned...
