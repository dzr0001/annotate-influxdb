*****************
annotate-influxdb
*****************

Grafana annotations provide a way to mark points on the graph with rich events. When you hover over an annotation you can get title, tags, and text information for the event.
This utility is command line tool to send annotation into InfluxDB database.

This has been updated and tested to work with InfluxDB v0.12. If you are using InfluxDB that is older than v0.9, please use version 0.0.1.

Grafana configuration
=====================

http://grafana.org/docs/features/annotations/

Usage examples
==============

  * send-annotation -h <influx host> -d <influx db name> -U <user> -P <password> -T <title> -t <tag1> -t <optional tag 2> -D "this is test"
  * git log -1 | send-annotation -h <influx host> -d <influx db name> -U <user> -P <password> -T "production upgrade" -t production
