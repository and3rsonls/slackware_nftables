nftable is native to Slackware 14.2 installation

# mv -v nftables.conf /etc/nftables/
   - copy or move nftables.conf (configuration file) to "/etc/nftables/"

# chmod + x /etc/nftables/nftables.conf
   - changing permissions

# mv -v rc.nftables /etc/rc.d/
   - copy or move rc.nftables (initialization file) to "/etc/rc.d/"

# chmod + x /etc/rc.d/rc.nftables
   - make the script executable at startup

# vim /etc/rc.d/rc.inet2

	| if [-x /etc/rc.d/rc.nftables]; then
	| /etc/rc.d/rc.nftables start
	| fi
	- add the lines above in "/etc/rc.d/r.inet2" for boot-up