portscan

Travis CI

Scan a network for ports that are open on an ip/ip range, and ips that are in use on that network.

$ portscan -h
NAME:
   portscan - Scan network ips and ports.

USAGE:
   netscan [global options] command [command options] [arguments...]

VERSION:
   v0.1.1

AUTHOR(S):
   @scpman <freeddser@gmail.com>

COMMANDS:
   help, h  Shows a list of commands or help for one command

GLOBAL OPTIONS:
   --debug, -d          run in debug mode
   --timeout, -t "1s"   override timeout used for check
   --port, -p "1-1000"  port range to check
   --proto "tcp,udp"    protocol/s to check
   --help, -h           show help
   --version, -v        print the version
Examples:

# for a cidr
$ portscan 192.168.0.1/24

# for a single ip
$ portscan 192.168.104.30

# for a single ip some port
$portscan  -p 1-3306   --proto tcp 192.168.1.101 
# for a cidr tcp
$portscan --proto tcp 192.168.1.1/24

#the project fork from https://github.com/jessfraz/netscan
#thanks:
#github.com/Sirupsen/logrus
#github.com/urfave/cli

#----------------------------
#v0.1.1:
add scan log in a $ip.log file
