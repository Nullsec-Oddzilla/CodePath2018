# Project 9 - Honeypot

Time spent: **~7-8** hours spent in total

> Objective: Successful configuration and deployment of a network-accessible honeypot server and live record of captured attacks.

#Honeypot
For this example I used the default dionaea honeypot.

#Summary of Data
(There may be minor differences between summary and .json due to a slight time difference between the snapshot and this writeup)
Number of attacks: 2,850
Top 5 attacker IP's
1.)USA - 340 attacks
2.)Tor Browser, IP unknown - 179 attacks
3.)Unidenitifable IP Orgin - 169 attacks
4.)Russia -139 attacks
5.)China - 100 attacks

#JSON
/session.json

#Issues
I encountered multiple issues stemming from glcoud being unable to install in my %path%, even when manually added to the environment. Thus I used workarounds but often had to modify the instructions. It took a few attemps to figure out mhn-admin was not allowing http access at first. Possibly due to all this, the script to deploy the dionaea honeypot used the wrong souce ip, making ti unable to download the files. It was an easy fix, but took some time troubleshooting. Additionally due to the gcloud issue, some extra work was required to successfully download the session.json file using securecopy.


