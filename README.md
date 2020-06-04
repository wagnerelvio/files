#!/bin/bash
LAN="192.168.240."
RANGE="1 254"
for HOST in `seq $RANGE`;do
	ping -c1 -W1 $LAN$HOST 2>&1> /dev/null && echo "$LAN$HOST up"&
done
