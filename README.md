# dynatrace-appmon-bt-logstash
a logstash configuration for feeding Dynatrace AppMon BTs via logstash to influxdb

This configuration is built for and meant to be used with my Dynatrace AppMon fastpack for monitoring hybris ecommerce environments.

## How to use

 * Install a recent logstash version (5.5.x +)
 * install logstash plugins: logstash-codec-protobuf and logstash-output-influxdb
 * As there are some 'bugs' in the logstash output for influxdb patch the file in LSHOME/vendor/bundle/jruby/2.3.0/gems/logstash-output-influxdb-5.0.3/lib/logstash/outputs/influxdb.rb
   with the one from this repo (in logstash-influxdb)
 * copy the conf.d contents to your logstash conf directory (/etc/logstash/conf.d)
 * enjoy Dynatrace AppMon BT data in InfluxDB (e.g. by hooking it up to Grafana Dashboards)
