#### A easy way to convert hosts file to Bind .zone file.


> edit the flowing code to custom attribute.
```
#Files Involved
hostsFile="/etc/hosts"
outputZoneFile="/Users/user/Desktop/hosts.zone"
nameServer="ns1"
# I don't know what the means of following fields. Just copied from others.
domainName="xxx.com"
zoneSerial=datetime.datetime.strftime(datetime.datetime.now(), '%Y%m%d%H%M%S')
refresh = "3H"
retry = "15M"
expiry = "1W"
SOA = [ ''+zoneSerial+'	; serial',
        '3H		; refresh',
        '15M		; retry',
        '1W		; expiry',
        '1D)		; minimum'
       ]
```