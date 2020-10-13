
# telegraf-speedtest
Utilise the official [Ookla Speedtest CLI](https://www.speedtest.net/apps/cli) to export results to Influxdb via Telegraf to be displayed within Grafana.

Tested with Ubuntu 18.04.5 LTS, Telegraf 1.15.3, Grafana v7.2.1, Speedtest by Ookla 1.0.0.2

A sound understanding of TIG(Telegraf, Influxdb & Grafana) is assumed moving forward

HOWTO:
1. Install the the official [Ookla Speedtest CLI](https://www.speedtest.net/apps/cli) onto your system (select whichever version suits your particular requirements)
2. Add the configuration into telegraf, either
   * store speedtest.conf under ```/etc/telegraf/telegraf.d/speedtest.conf```  
    _\* OR \*_
   * copy the config and add to your telegraf.conf  
3. Restart telegraf (e.g. under Ubuntu ```~$ sudo systemctl restart telegraf.service```)
4. Import the provided json template into Grafana
5. Select the appropriate host variable from the top left of the dashboard
6. Happy trending!
  
p.s. be careful when setting the interval time, too often and you may risk being being blocked from utilising the service.

![Example Screenshot](https://raw.githubusercontent.com/risb0r/telegraf-speedtest/master/screenshot.png)
