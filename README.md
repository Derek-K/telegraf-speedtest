# telegraf-speedtest
Using official SpeedTest.net cli for telegraf

Tested with Ubuntu 18.04.4 LTS, Telegraf 1.14.1

HOWTO:
1) Install the official SpeedTest CLI from SpeedTest.net - https://www.speedtest.net/apps/cli
2) Run 'speedtest' once (to accept the license)
3) Add the configuration into telegraf, either
   - store speedtest.conf under /etc/telegraf.d
    * OR *
   - copy the config and add to your telegraf.conf
4) Restart telegraf (e.g. under Ubuntu "sudo systemctl restart telegraf")

Optionally, install Grafana dashboard #12428
  https://grafana.com/grafana/dashboards/12428
  
Enjoy!
p.s. Do not set the interval too short or you may get banned...
