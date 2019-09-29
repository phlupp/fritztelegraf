## python script for InfluxData / Telegraf

this script was insptred by [fetzerch/fritzcollectd](https://github.com/fetzerch/fritzcollectd)

You can use this script to collect data from a AVM Fritz!Box and push via Telegraf to InfluxDB

Dependencies
------------
* Python 2.7+
* [fritzconnection](https://bitbucket.org/kbr/fritzconnection)

Installation
------------
1. copy ``fritztelegraf.py`` to ``/usr/local/bin/``
2. Configure the plugin as shown below
3. Restart telefraf

Configuration
-------------
Add the following to your telegraf config (typically ``/etc/telegraf/telegraf.conf``):

```
[[inputs.exec]]
  commands = [
        "/usr/local/bin/fritztelegraf.py"
  ]
  data_format = "influx"
```
