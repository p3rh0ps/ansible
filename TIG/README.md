# GRAFANA Dashboard Showcases with NXOS

Inspired from excellent NWMICHL Blog: https://nwmichl.net/2020/06/14/monitor-cisco-nx-os-aci-via-snmp-and-the-tig-stack/

Updated to work with influxdb2 query language

## Specs

Grafana  v9.2.5
InfluxDB v2.5.1
Telegraf v1.24.3

## HowTo

- influxdb and grafana must be installed (plethor of methods available on the web...)
- Generate Telegraf configuration for each nexus  
  'ansible-playbook -i inventory telegraf.yml'
- Place all configuration generated in /etc/telegraf/telegraf.d
- If you want to test telegraf generated configuration
  'telegraf  --test --config /etc/telegraf/telegraf.d/file.cfg'
- Restart telegraf
  'systemctl restart telegraf'

## Useful tools

- sflowtool, net-snmp

## Grafana NXOS SNMP/SYSLOG

<a href="url"><img src="https://github.com/p3rh0ps/ansible/blob/master/TIG/imgs/NXOS%20Grafana%20SNMP%20data.png" align="center" height="1000" width="1000" ></a>

## Grafana NXOS TELEMETRY with NX-API/DME/YANG Data

<a href="url"><img src="https://github.com/p3rh0ps/ansible/blob/master/TIG/imgs/Grafana%20NXOS%20Telemetry%20Data.png" align="center" height="1000" width="1000" ></a>
