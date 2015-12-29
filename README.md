<h1 align="center">InfluxDB</h1>
<p align="center">
  <b>InfluxDB</b> is an open-source, distributed, time series database with no external dependencies.  
</p>

## AWS Setup

#### Notes
This is not an HA setup, that requires clustering which this template doesn't include.  Clustering is not stable in the current release of Influxdb, for that reason, this template will focus on a single instance.

### Install
Upload the Influxdb template.  This will require a valid configuration file for Influxdb, it will replace the default config installed by the Influxdb RPM.  

There is a example config included in this repo.  

This template will create 2 EBS volumes, the first will become the root device for the database, the second will be a small device for the WAL.

#### Management interface

The web interface will be found at your load balancer URL with the API found on port 8086.  Enter the following credentials to gain access to the web interface.
```ruby
USERNAME : admin  
PASSWORD : admin  
```
