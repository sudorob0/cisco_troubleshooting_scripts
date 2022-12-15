# cisco_troubleshooting

This is a readme for cisco trouble shooting repo

These scripts are only for cisco equipment only. These scripts are to allow for quick and easy troubleshooting for metro ethernet and t1 circuit issues. The scripts will get the necessary information and condense it into an easy to read output. 

**First the output for the T1 script should look like the our put below** The uptime, bgp uptime and gatway are grouped together so you can compare the times and routes to look for bouncing. Then you can see what interfaces/ circuits are up and if they are taking errors. You also get ping response times.

------- Router uptime + BGP Status + Gateway ------

XXXXXXX uptime is 21 weeks, 4 days, 15 hours, 58 minutes

Gateway of last resort is 10.1.1.1 to network 0.0.0.0

Neighbor        V           AS MsgRcvd MsgSent   TblVer  InQ OutQ Up/Down  State/PfxRcd

10.1.1.1    4        13979  218397  240351        6    0    0 21w4d           1
 
------- Tunnel + Interface Status ------

Tunnel0                    10.1.1.2   YES unset  up                    up

Tunnel1                    10.1.1.3   YES TFTP   up                    down
 
Gi0/1                          up             up       Backup connection to Cradle-Point
 
------- Bundle ------

  Member links: 3 active, 0 inactive (max 255, min not set)
  
    Se0/0/0:0, since 21w4d
    Se0/0/1:0, since 1d02h
    Se0/0/2:0, since 00:07:03
    
T1 0/0/0 is up.
  Total Data (last 24 hours)
     0 Line Code Violations, 0 Path Code Violations,
     0 Slip Secs, 0 Fr Loss Secs, 0 Line Err Secs, 0 Degraded Mins,
     0 Errored Secs, 0 Bursty Err Secs, 0 Severely Err Secs, 0 Unavail Secs
     
T1 0/0/1 is up.
  Total Data (last 24 hours)
     0 Line Code Violations, 11 Path Code Violations,
     0 Slip Secs, 1 Fr Loss Secs, 0 Line Err Secs, 0 Degraded Mins,
     3 Errored Secs, 2 Bursty Err Secs, 1 Severely Err Secs, 0 Unavail Secs
     
T1 0/0/2 is up.
  Total Data (last 24 hours)
     7058 Line Code Violations, 41 Path Code Violations,
     0 Slip Secs, 21 Fr Loss Secs, 2 Line Err Secs, 0 Degraded Mins,
     7 Errored Secs, 3 Bursty Err Secs, 3 Severely Err Secs, 26 Unavail Secs
     
T1 0/0/3 is administratively down.

------- PING Stats for google ------

Type escape sequence to abort.
Sending 10, 1500-byte ICMP Echos to 8.8.8.8, timeout is 2 seconds:
Packet has data pattern 0xFFFF
..........
Success rate is 0 percent (0/10)

**The metro script has a very similar script output but with interface errors instead of circuit errors**



