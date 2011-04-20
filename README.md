# Never Lost
if you are tired of looking for your ip and doing _ifconfig_ and getting sometimes a big response like this

```bash
lo0: flags=8049<UP,LOOPBACK,RUNNING,MULTICAST> mtu 16384
	inet6 ::1 prefixlen 128 
	inet6 fe80::1%lo0 prefixlen 64 scopeid 0x1 
	inet 127.0.0.1 netmask 0xff000000 
gif0: flags=8010<POINTOPOINT,MULTICAST> mtu 1280
stf0: flags=0<> mtu 1280
en0: flags=8863<UP,BROADCAST,SMART,RUNNING,SIMPLEX,MULTICAST> mtu 1500
	ether 34:15:9e:02:5b:24 
	media: autoselect
	status: inactive
fw0: flags=8863<UP,BROADCAST,SMART,RUNNING,SIMPLEX,MULTICAST> mtu 4078
	lladdr 34:15:9e:ff:fe:02:5b:24 
	media: autoselect <full-duplex>
	status: inactive
en1: flags=8863<UP,BROADCAST,SMART,RUNNING,SIMPLEX,MULTICAST> mtu 1500
	ether f8:1e:df:e5:17:d9 
	inet6 fe80::fa1e:dfff:fee5:17d9%en1 prefixlen 64 scopeid 0x6 
	inet 192.168.1.101 netmask 0xffffff00 broadcast 192.168.1.255
	media: autoselect
	status: active
vmnet1: flags=8863<UP,BROADCAST,SMART,RUNNING,SIMPLEX,MULTICAST> mtu 1500
	ether 00:50:56:c0:00:01 
	inet 192.168.63.1 netmask 0xffffff00 broadcast 192.168.63.255
vmnet8: flags=8863<UP,BROADCAST,SMART,RUNNING,SIMPLEX,MULTICAST> mtu 1500
	ether 00:50:56:c0:00:08 
	inet 192.168.46.1 netmask 0xffffff00 broadcast 192.168.46.255
```

and would like less complicated, like this

```bash
nlost
```
![nlost growl sample](http://ramonroche.com/content/nlost_sample_a.png "nlos Growl Sample")

or would like to output the buffer to your clipboard using pbcopy (_warning as this will replace everything on your current clipboard_)

```bash
nlost pb
-> WIFI: 192.168.1.101
nlost pb wifi
-> 192.168.1.101
```
## USAGE
#### Growl Sample
```bash
nlost
```
#### pbcopy Samples
```bash
nlost pb
nlost pb eth
nlost pb wifi
```

## INSTALLATION
First make sure you have something on your path

```bash
echo $PATH -> /opt/local/bin:/opt/local/sbin:/usr/bin:/bin:/usr/sbin:/sbin:/usr/local/bin
```
it should output something similar to the above, now the next part depends on your preferences, my favorite place to store my scripts is on /usr/local/bin (if you don't know or don't have a preference then just use the script below)

```bash
git clone git://github.com/mrpollo/Never-Lost.git Never-Lost | sudo ln -sv Never-Lost/nlost /usr/local/bin/nlost
```
_if you need further assistance just email me_ mrpollo@gmail.com

## REQUIREMENTS
### OSX:
_OSX_ is required to run initially but support for other OS's will be added in the future
### Growl (_growlnotify_):
requires that you previously installed _'growlnotify'_ Growl and _growlnotify_ can be found on their website http://growl.info/
please see them for help installing or using
### pbcopy
pbcopy comes standard on OSX since 10.3