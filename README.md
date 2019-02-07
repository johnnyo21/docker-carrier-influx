This operates as a proxy server for the Carrier Infinity / Bryant Evolution thermostats, capturing data and sending it to an InfluxDB time-series database (https://www.influxdata.com/time-series-platform/influxdb/)

```
docker run -d -p 8888:8888 --restart=always --name carrier-influx -e INFLUXHOST=<influxdb_host> -e INFLUXPORT=8086 -e INFLUXUSER=root -e INFLUXPASS=root -e INFLUXDB=carrier thecase/bryant-influx

Reconfigure your thermostat to use the IP:port of your new proxy server:
```

`menu -> wireless -> advanced -> manage proxy servers`
