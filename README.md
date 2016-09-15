#Netconf

This configuration is an extension of MDT API. This code is a netconf configuration that extends the capability of MDT API for supporting multi path within the same subscription group.


The extension API takes six arguments.
	1 - RouterId (Router IP address)
	2 - Username (Router username)
	3 - password (Router Password)
	4 - RouterPort (Router Port number)
	5 - SGroupName (Subscription group name)
	6- SPath (Subscription path)


To run the script:
	python netconf.py RouterId Username password RouterPort SGroupName SPath

Ex.:
	python netconf.py 192.168.2.3 vagrant vagrant 22 SGroup4 CiscoWorld:arp/nodes/node/entries/entry



This code will be integrated within the main MDT API
