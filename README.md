#MDTSSH.py


This API is model driven implementation to router using Netmiko (SSH)

This API has 11 arguments and 4 functions;

Arguments are:-

1- Command : This argument is used to choose the configuration type
						 ex;
						 1- newConfig : To have a new configuration with new Destination Group, Sensor Group and Subscription
						 2- subscription: To only create a new subscription
						 3- destination: To only create a new destination group
						 4- sensor: To only create a new sensor group

2- RouterId : The router IP address
3- Username : The router username
4- Password : The router password
5- RouterPort : The router port number
6- DgroupName : Destination Group Name
7- DIPAddress : Destination IPv4 address
8- DgroupPort : Destination port number
9- SenorGroupName : Sensor Group Name
10- SensorPath : Sensor path
11- SubName : Subscription Name
12- interval : Streaming interval


Funtions are:-

	configureAll(): To invoke:
										python mdtssh.py  newConfig RouterId Username Password RouterPort DgroupName DIPAddress  DgroupPort SenorGroupName SensorPath SubName interval

							  	Ex:
										python mdtssh.py  newConfig  192.168.2.3 vagrant vagrant 22 Dgroup1 172.16.18.5 5001 SGroup1 sgroup1/ciscorouter/com Sub1 3000


	subscription():To invoke:
										python mdtssh.py  subscription RouterId Username Password RouterPort DgroupName SubName SenorGroupName interval

							 Ex:
							 			python mdtssh.py  subscription  192.168.2.3 vagrant vagrant 22 Dgroup1 Sub2  SGroup1  3000


	destination(): To invoke:

											python mdtssh.py  destination RouterId Username Password RouterPort DgroupName DIPAddress DgroupPort
								 Ex:
											python mdtssh.py  destination  192.168.2.3 vagrant vagrant 22 Dgroup2 192.168.4.3  7872


	sensor(): 		 To invoke:
											python mdtssh.py  sensor RouterId Username Password RouterPort SenorGroupName SensorPath


								 Ex:
								 			python mdtssh.py  sensor  192.168.2.3 vagrant vagrant 22 SGroup2 Cisco-IOS-XR-infra-statsd-oper:infra-statistics/interfaces/interface/latest/generic-counters






#Netconf

#netconf.py

This configuration is an extension of MDT API. This code is a Configuring Model-Driven Telemetry (MDT) with OpenConfig YANG OpenConfig YANG that uses a netconf client. This configuration extends the capability of MDT API for supporting multi path within the same subscription group.


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
