# Incident report analysis

## Summary

The organization recently experienced a DDoS attack, caused by an ICMP flood attack through an unconfigured firewall. 
This resulted in the organization's internal network not being able to access network resources. 
This prevented employees of the organization from working, causing a hit to organization's operations.  

The disruption lasted for two hours until the incident was resolved by the incident management team blocking all incoming ICMP packets, stopping all non-critical network services, and restoring critical network services. 

In response to this security event, the network security team implemented: 
1. A new firewall rule to limit the rate of incoming ICMP packets
2. Source IP address verification on the firewall to check for spoofed IP addresses on incoming ICMP packets
3. Network monitoring software to detect abnormal traffic patterns
4. An IPS system to filter out some ICMP traffic based on suspicious characteristics

## Identify

The company's cybersecurity team reviewed the systems, network services, firewall configurations and logs involved in the attack. 
The team found a flood of ICMP pings sent to internal network services from various different IP addresses indicating that this was a DDoS attack and an ICMP flood attack. 

An ICMP flood attack works because for each ICMP ping the server receives it send back an ICMP response. 
However, if too many pings are sent in a short period of time, it overwhelms the server's resources, network bandwidth and processing power. 

The ICMP packets could reach the internal network from outside because the firewall was not configured. 

## Protect

In order to protect the organization's internal network, the network security team has implemented a new firewall rule to limit the rate of incoming ICMP packets.
This should greatly reduce the effectiveness of ICMP flood attacks. By limiting the rate of incoming ICMP packets, it'll be more difficult for network services to be overwhelmed and out of service. 

The network security team and incident management team should be made aware of this attack. They should be able to recognize and respond to this type of attack quickly. 
Training should also be provided to help identify and prevent similar attacks in the future, such as DDoS attacks.

Source IP address verification on the firewall has also been implemented to ensure ICMP packets with the source IP of a device in the network is not coming from outside the firewall. This can prevent IP spoofing attacks. 

An IPS system has also been implemented which could filter out some ICMP traffic based on suspicious characteristics. 

Critical services should be segmented into a restricted zone, so if one network segments gets compromised it won't affect the rest. 

## Detect

To detect future ICMP flood attacks, an IPS (Intrusion Prevention Software) has been implemented. 
An IPS could detect and prevent ICMP flood attacks if it matches suspicious characteristics. 
The network security team will also use SIEM tools to detect and prevent similar attacks.  

## Respond

The incident management team blocked all incoming ICMP packets and stopped all non-critical network services incase they were compromised. 
We informed the organization's management of the security incident. 
In future events like this, analyzing the logs either from a SIEM tool or directly in the firewall log. 
To mitigate events like this requires trained staff who can respond quickly to this security incident. 

## Recover

The incident management team restored all critical network services so the organization can continue to operate. 
Non-critical network services have not yet been restored and will be restored later. 
We have informed management that data entered on the day of the incident may be lost, and they should inform employees and customers. 
If management deems the network services critical enough, more frequent backups should be made, for example hourly. 

## Reflections/Notes

