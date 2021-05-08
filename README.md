# yamaha-rt-zabbix-template
YAMAHA Router monitoring Zabbix template

## Description
This is YAMAHA Router Zabbix monitoring template using SNMP.
This template based on [mib2zabbix](https://github.com/cavaliercoder/mib2zabbix).

This template is checked on following environment:
- Zabbix Server 5.2
- RTX1210, RTX810
  - If RTX810, some item cannot use because these item is not implemented on RTX810.
- SNMPv1
  - not checked SNMPv2/v3.

## Usage
**Before using this template, set snmp config on YAMAHA Router (probability default is off).**
Import this template and link this template to YAMAHA Router host config.
If create YAMAHA Router host using this template,
- interface is set `SNMP`
- If many snmp error is occured, `using bulk request` set DISABLED.
  - Sometimes, this option `using bulk request` causes many SNMP errors(ex: general error/network error/etc...) and increase Router's CPU usage.

## TODO(Feature Work)
- change item names (now: SNMP key name from MIB)
- create trigger, graph and screen prototype
- check snmptrap item (now: default disabled and no check)
- check all items and delete some item if need not.

## Author
author: hinananoha
