# basic-ssl-decryption-policy
This skillet creates a basic ssl decryption policy that installs a self-signed certificate and a decryption policy that decrypts high-risk categories and the eicar antivirus test site.

This skillet pushes a self-signed certificate to a firewall, configures it as the forward-trust-certificate and creates a decryption policy and profile.  It also creates a custom URL category for the *.eicar.org website and enables high-risk and this custom category for decryption.  This skillet is meant mostly for POC or demonstration purposes.  Production environments are likely to leverage an internal PKI environment to perform decryption instead of using a self-signed certificate.
To use the skillet, select the VSYS (default vsys1) and deploy to the firewall.  If testing decryption with AntiVirus, browse to the eicar test virus site through the firewall and download the test file using https.  If you have not imported the certificate in the system’s local trusted certificate store, you will receive a certificate error.  The download will be blocked.  The other high-risk URL categories that are part of the decryption rule are:
•	Adult
•	Command-and-Control
•	Content-Delivery-Networks
•	Copyright-Infringement
•	Dynamic-DNS
•	Gambling
•	Hacking
•	High-Risk
•	Malware
•	Parked
•	Peer-to-Peer
•	Proxy-Avoidance-and-Anonymizers
•	Shareware-and-Freeware
•	Social-Networking
•	Unknown

