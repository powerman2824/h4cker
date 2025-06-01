# RaspberryPi4-WebSploit


## Lab Enviroment


### Lab Setup:

<details>
<summary>Equipment:</summary>

- **Model**:  
  - Raspberry Pi 4 Model B  
- **Operating System**:  
  - Linux parrot 6.12.25+rpt-rpi-v8 #1 SMP PREEMPT Debian 1:6.12.25-1+rpt1 (2025-04-30) aarch64 GNU/Linux  
- **Memory**:  
  - 8GB  
- **Storage**:  
  - 128GB  
- **Infographic**:  
  - ![507](/pics/507.png)
  - cmdline:
```bash
┌─[root@parrot]─[~]
└──╼ #uname -a
Linux parrot 6.12.25+rpt-rpi-v8 #1 SMP PREEMPT Debian 1:6.12.25-1+rpt1 (2025-04-30) aarch64 GNU/Linux
┌─[root@parrot]─[~]
└──╼ #free -h
           	total    	used    	free  	shared  buff/cache   available
Mem:       	7.6Gi   	3.0Gi   	1.5Gi   	486Mi   	3.7Gi   	4.6Gi
Swap:       	99Mi   	512Ki    	99Mi
┌─[root@parrot]─[~]
└──╼ #df -h
Filesystem  	Size  Used Avail Use% Mounted on
udev        	3.6G 	0  3.6G   0% /dev
tmpfs       	783M  1.8M  781M   1% /run
/dev/mmcblk0p2  117G   32G   80G  29% /
tmpfs       	3.9G 	0  3.9G   0% /dev/shm
tmpfs       	5.0M   16K  5.0M   1% /run/lock
/dev/mmcblk0p1  510M  156M  355M  31% /boot/firmware
tmpfs       	783M   84K  783M   1% /run/user/1000
overlay     	117G   32G   80G  29% /var/lib/docker/overlay2/ed680fa0ce29360f2cbcff3d1632e2debeea5d656e754deff51308c9c2a05d1b/merged
overlay     	117G   32G   80G  29% /var/lib/docker/overlay2/7e4559539a5a7c09ae0f40149a342beef3b9b675cb3a17ad1ee8a138158325f3/merged
overlay     	117G   32G   80G  29% /var/lib/docker/overlay2/866b8c8f7df850453ebab6f9799e8fede3109b733d380ee62db85c2be9c19d69/merged
┌─[root@parrot]─[~]
└──╼ #
```
</details>
<details>
<summary>Installation:</summary>

- **Download Operating System (Parrot or Kali)**:  
  - [ParrotOS](https://www.parrotsec.org/)  
- **Operating System**:  
  - Linux parrot 6.12.25+rpt-rpi-v8 #1 SMP PREEMPT Debian 1:6.12.25-1+rpt1 (2025-04-30) aarch64 GNU/Linux  
- **Memory**:  
  - 8GB  
- **Storage**:  
  - 128GB  
- **Infographic**:  
  - ![507](/pics/507.png)

</details>


#### Installation:


##### Download Operating System (Parrot or Kali):


###### Download ParrotOS for RaspberryPi 4 here: 


- https://www.parrotsec.org/

###### Download Kali Linux for RaspberryPi 4 here:


- n/a

##### Flash image to disk using RaspberryPi Imager:


###### 

![464](C:/Users/mrcaf/Documents/h4ckForLife/464.png)

###### Download RaspberryPi Imager here:


- https://www.raspberrypi.org/

##### Boot Pi with Parrot or Kali OS default login's:


###### ParrotOS:


- pi

- parrot

###### Kali Linux:


- n/a

- n/a

##### Download and install Websploit Labs:


###### Download and Installation Script


<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0//EN" "http://www.w3.org/TR/REC-html40/strict.dtd">
<html><head><meta name="qrichtext" content="1" /><style type="text/css">
p, li { white-space: pre-wrap; }
</style></head><body style=" font-family:'Consolas'; font-size:9pt; font-weight:400; font-style:normal;">
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">curl -sSL https://websploit.org/install.sh | sudo bash</p></body></html>

- 
![659](C:/Users/mrcaf/Documents/h4ckForLife/659.png)

###### Updating Websploit Docker containers to support ARM arch:


- From the cmdline login into root

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0//EN" "http://www.w3.org/TR/REC-html40/strict.dtd">
<html><head><meta name="qrichtext" content="1" /><style type="text/css">
p, li { white-space: pre-wrap; }
</style></head><body style=" font-family:'Consolas'; font-size:9pt; font-weight:400; font-style:normal;">
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">sudo su</p></body></html>

- Move to Root's root directory to find the Websploit home directory ~/h4cker

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0//EN" "http://www.w3.org/TR/REC-html40/strict.dtd">
<html><head><meta name="qrichtext" content="1" /><style type="text/css">
p, li { white-space: pre-wrap; }
</style></head><body style=" font-family:'Consolas'; font-size:9pt; font-weight:400; font-style:normal;">
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">cd ~/</p></body></html>

- Stay in the root directory & shutdown & remove all running conatiners

  - 1. Stop All Containers

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0//EN" "http://www.w3.org/TR/REC-html40/strict.dtd">
<html><head><meta name="qrichtext" content="1" /><style type="text/css">
p, li { white-space: pre-wrap; }
</style></head><body style=" font-family:'Consolas'; font-size:9pt; font-weight:400; font-style:normal;">
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px;">docker stop $(docker ps -aq)</p></body></html>

  - 2. Remove All Containers

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0//EN" "http://www.w3.org/TR/REC-html40/strict.dtd">
<html><head><meta name="qrichtext" content="1" /><style type="text/css">
p, li { white-space: pre-wrap; }
</style></head><body style=" font-family:'Consolas'; font-size:9pt; font-weight:400; font-style:normal;">
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px;">docker rm $(docker ps -aq)</p></body></html>

  - 3. (Optional) Clean Up Volumes and Networks

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0//EN" "http://www.w3.org/TR/REC-html40/strict.dtd">
<html><head><meta name="qrichtext" content="1" /><style type="text/css">
p, li { white-space: pre-wrap; }
</style></head><body style=" font-family:'Consolas'; font-size:9pt; font-weight:400; font-style:normal;">
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px;">docker volume prune -f</p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px;">docker network prune -f</p></body></html>

  - 4. (Optional) Verify Clean State

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0//EN" "http://www.w3.org/TR/REC-html40/strict.dtd">
<html><head><meta name="qrichtext" content="1" /><style type="text/css">
p, li { white-space: pre-wrap; }
</style></head><body style=" font-family:'Consolas'; font-size:9pt; font-weight:400; font-style:normal;">
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px;">docker ps -a</p></body></html>

- Copy provider docker-compose file & keep as referance

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0//EN" "http://www.w3.org/TR/REC-html40/strict.dtd">
<html><head><meta name="qrichtext" content="1" /><style type="text/css">
p, li { white-space: pre-wrap; }
</style></head><body style=" font-family:'Consolas'; font-size:9pt; font-weight:400; font-style:normal;">
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">cp docker-compose.yml example-docker-compose.yml</p></body></html>

  - 
![689](C:/Users/mrcaf/Documents/h4ckForLife/689.png)

- Create/Edit docker-compose file that supports ARM arch

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0//EN" "http://www.w3.org/TR/REC-html40/strict.dtd">
<html><head><meta name="qrichtext" content="1" /><style type="text/css">
p, li { white-space: pre-wrap; }
</style></head><body style=" font-family:'Consolas'; font-size:9pt; font-weight:400; font-style:normal;">
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">nano docker-compose.yml</p></body></html>

  - 
![693](C:/Users/mrcaf/Documents/h4ckForLife/693.png)

  - New docker-compose.yml file that supports ARM arch & recreates networks

    - docker-compose.yaml

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0//EN" "http://www.w3.org/TR/REC-html40/strict.dtd">
<html><head><meta name="qrichtext" content="1" /><style type="text/css">
p, li { white-space: pre-wrap; }
</style></head><body style=" font-family:'Consolas'; font-size:9pt; font-weight:400; font-style:normal;">
<p style="-qt-paragraph-type:empty; margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><br /></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">services:</p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">  webgoat:</p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">	container_name: webgoat</p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">	image: webgoat/webgoat:v2023.5</p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">	restart: unless-stopped</p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">	networks:</p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">  	websploit:</p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">    	ipv4_address: 10.6.6.11</p>
<p style="-qt-paragraph-type:empty; margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><br /></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">  juice-shop:</p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">	container_name: juice-shop</p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">	image: bkimminich/juice-shop</p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">	restart: unless-stopped</p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">	networks:</p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">  	websploit:</p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">    	ipv4_address: 10.6.6.12</p>
<p style="-qt-paragraph-type:empty; margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><br /></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">  dvwa:</p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">	container_name: dvwa</p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">	image: cambarts/arm-dvwa:latest</p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">	restart: unless-stopped</p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">	networks:</p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">  	websploit:</p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">    	ipv4_address: 10.6.6.13</p>
<p style="-qt-paragraph-type:empty; margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><br /></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">networks:</p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">  websploit:</p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">	driver: bridge</p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">	ipam:</p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">  	config:</p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">    	- subnet: 10.6.6.0/24</p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">      	gateway: 10.6.6.1</p>
<p style="-qt-paragraph-type:empty; margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><br /></p></body></html>

- Build & start new docker containers & network

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0//EN" "http://www.w3.org/TR/REC-html40/strict.dtd">
<html><head><meta name="qrichtext" content="1" /><style type="text/css">
p, li { white-space: pre-wrap; }
</style></head><body style=" font-family:'Consolas'; font-size:9pt; font-weight:400; font-style:normal;">
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">docker-compose up -d</p></body></html>

- Confirm containers and network are working properly

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0//EN" "http://www.w3.org/TR/REC-html40/strict.dtd">
<html><head><meta name="qrichtext" content="1" /><style type="text/css">
p, li { white-space: pre-wrap; }
</style></head><body style=" font-family:'Consolas'; font-size:9pt; font-weight:400; font-style:normal;">
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">docker ps</p></body></html>

  - 
![707](C:/Users/mrcaf/Documents/h4ckForLife/707.png)

- Use Websploit built in container scanner

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0//EN" "http://www.w3.org/TR/REC-html40/strict.dtd">
<html><head><meta name="qrichtext" content="1" /><style type="text/css">
p, li { white-space: pre-wrap; }
</style></head><body style=" font-family:'Consolas'; font-size:9pt; font-weight:400; font-style:normal;">
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;">containers</p></body></html>

  - 
![710](C:/Users/mrcaf/Documents/h4ckForLife/710.png)

## Recon


### Phase 1: Network Recon (Nmap)


#### What I did:


##### I began by scanning the internal RaspberryPi4-WebSploit network (10.6.6.0/24) using Nmap to identify live hosts and open TCP ports. This provided a broad view of available services and gave me three target IPs with interesting ports, including web-facing services on ports 80, 8080, 3000, and 9090.


#### Why I did it:


##### To enumerate active hosts and map the attack surface


##### Identify potential web services to investigate further


#### Started with a scan using Nmap on network 10.6.6.0/24


<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0//EN" "http://www.w3.org/TR/REC-html40/strict.dtd">
<html><head><meta name="qrichtext" content="1" /><style type="text/css">
p, li { white-space: pre-wrap; }
</style></head><body style=" font-family:'MS Shell Dlg 2'; font-size:8.25pt; font-weight:400; font-style:normal;">
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">nmap -sP 10.6.6.0/24</span></p></body></html>

##### 

![374](C:/Users/mrcaf/Documents/h4ckForLife/374.png)

###### cmdline:


<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0//EN" "http://www.w3.org/TR/REC-html40/strict.dtd">
<html><head><meta name="qrichtext" content="1" /><style type="text/css">
p, li { white-space: pre-wrap; }
</style></head><body style=" font-family:'MS Shell Dlg 2'; font-size:8.25pt; font-weight:400; font-style:normal;">
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">┌─[root@parrot]─[~/h4cker/cheat_sheets]</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">└──╼ #nmap -sP 10.6.6.0/24</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">Starting Nmap 7.94SVN ( https://nmap.org ) at 2025-05-31 22:40 BST</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">Nmap scan report for 10.6.6.11</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">Host is up (0.000020s latency).</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">MAC Address: 02:42:0A:06:06:0B (Unknown)</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">Nmap scan report for 10.6.6.12</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">Host is up (0.000015s latency).</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">MAC Address: 02:42:0A:06:06:0C (Unknown)</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">Nmap scan report for 10.6.6.13</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">Host is up (0.000028s latency).</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">MAC Address: 02:42:0A:06:06:0D (Unknown)</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">Nmap scan report for 10.6.6.1</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">Host is up.</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">Nmap done: 256 IP addresses (4 hosts up) scanned in 2.05 seconds</span></p></body></html>

#### DIscovered Host :


##### Host-1


###### IP Address


- 10.6.6.11

###### MAC Address


- 02:42:0A:06:06:0B

###### PORT


- 8080/tcp

-  9090/tcp

###### STATE


- open

- open

###### SERVICE


- http-proxy

- zues-admin

##### Host-2


###### IP Address


- 10.6.6.12

###### MAC Address


- 02:42:0A:06:06:0C

###### PORT


- 3000/tcp

###### STATE


- open

###### SERVICE


- ppp

##### Host-3


###### IP Address


- 10.6.6.13

###### MAC Address


- 02:42:0A:06:06:0D

###### PORT


- 80/tcp

-  3306/tcp

###### STATE


- open

- open

###### SERVICE


- http

- mysql

#### Scanned the network host with defualt Nmap scripts


<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0//EN" "http://www.w3.org/TR/REC-html40/strict.dtd">
<html><head><meta name="qrichtext" content="1" /><style type="text/css">
p, li { white-space: pre-wrap; }
</style></head><body style=" font-family:'MS Shell Dlg 2'; font-size:8.25pt; font-weight:400; font-style:normal;">
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">nmap -sC 10.6.6.0/24</span></p></body></html>

##### 

![369](C:/Users/mrcaf/Documents/h4ckForLife/369.png)

###### cmdline:


<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0//EN" "http://www.w3.org/TR/REC-html40/strict.dtd">
<html><head><meta name="qrichtext" content="1" /><style type="text/css">
p, li { white-space: pre-wrap; }
</style></head><body style=" font-family:'MS Shell Dlg 2'; font-size:8.25pt; font-weight:400; font-style:normal;">
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">┌─[root@parrot]─[~/h4cker/cheat_sheets]</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">└──╼ #nmap -sC 10.6.6.0/24</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">Starting Nmap 7.94SVN ( https://nmap.org ) at 2025-05-31 22:49 BST</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">Nmap scan report for 10.6.6.11</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">Host is up (0.000027s latency).</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">Not shown: 998 closed tcp ports (reset)</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">PORT 	STATE SERVICE</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">8080/tcp open  http-proxy</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">|_http-title: Site doesn't have a title.</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">9090/tcp open  zeus-admin</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">MAC Address: 02:42:0A:06:06:0B (Unknown)</span></p>
<p style="-qt-paragraph-type:empty; margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%; font-family:'Consolas'; font-size:9pt;"><br /></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">Nmap scan report for 10.6.6.12</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">Host is up (0.000027s latency).</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">Not shown: 999 closed tcp ports (reset)</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">PORT 	STATE SERVICE</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">3000/tcp open  ppp</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">MAC Address: 02:42:0A:06:06:0C (Unknown)</span></p>
<p style="-qt-paragraph-type:empty; margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%; font-family:'Consolas'; font-size:9pt;"><br /></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">Nmap scan report for 10.6.6.13</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">Host is up (0.000026s latency).</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">Not shown: 998 closed tcp ports (reset)</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">PORT 	STATE SERVICE</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">80/tcp   open  http</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">| http-title: Setup :: Damn Vulnerable Web Application (DVWA) v1.9</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">|_Requested resource was setup.php</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">| http-cookie-flags:</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">|   /:</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">| 	PHPSESSID:</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">|_  	httponly flag not set</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">| http-robots.txt: 1 disallowed entry</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">|_/</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">3306/tcp open  mysql</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">MAC Address: 02:42:0A:06:06:0D (Unknown)</span></p>
<p style="-qt-paragraph-type:empty; margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%; font-family:'Consolas'; font-size:9pt;"><br /></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">Nmap scan report for 10.6.6.1</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">Host is up (0.000026s latency).</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">Not shown: 999 closed tcp ports (reset)</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">PORT   STATE SERVICE</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">53/tcp open  domain</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">| dns-nsid:</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">|_  bind.version: dnsmasq-2.90</span></p>
<p style="-qt-paragraph-type:empty; margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%; font-family:'Consolas'; font-size:9pt;"><br /></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">Nmap done: 256 IP addresses (4 hosts up) scanned in 17.64 seconds</span></p></body></html>

### Phase 2: Web Recon (Nikto)


#### What I did:


##### I then ran Nikto on the discovered web services to detect common vulnerabilities, misconfigurations, and hidden directories. This revealed accessible paths like /dump.tgz, /database.tgz, and /config/, as well as outdated Apache and PHP versions.


#### Why I did it:


##### To find low-hanging fruit like open directories, outdated versions


##### Nikto is fast and automated, making it great for early recon


#### Scaned host indivisual with Nikto


<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0//EN" "http://www.w3.org/TR/REC-html40/strict.dtd">
<html><head><meta name="qrichtext" content="1" /><style type="text/css">
p, li { white-space: pre-wrap; }
</style></head><body style=" font-family:'MS Shell Dlg 2'; font-size:8.25pt; font-weight:400; font-style:normal;">
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">nikto -h http://10.6.6.13</span></p></body></html>

##### 

![307](C:/Users/mrcaf/Documents/h4ckForLife/307.png)

###### cmdline:


<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0//EN" "http://www.w3.org/TR/REC-html40/strict.dtd">
<html><head><meta name="qrichtext" content="1" /><style type="text/css">
p, li { white-space: pre-wrap; }
</style></head><body style=" font-family:'MS Shell Dlg 2'; font-size:8.25pt; font-weight:400; font-style:normal;">
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">┌─[root@parrot]─[~/h4cker/cheat_sheets]</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">└──╼ #nikto -h http://10.6.6.13</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">- Nikto v2.5.0</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">---------------------------------------------------------------------------</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ Target IP:      	10.6.6.13</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ Target Hostname:	10.6.6.13</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ Target Port:    	80</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ Start Time:     	2025-06-01 00:44:16 (GMT1)</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">---------------------------------------------------------------------------</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ Server: Apache/2.4.7 (Ubuntu)</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /: Retrieved x-powered-by header: PHP/5.5.9-1ubuntu4.29.</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /: The anti-clickjacking X-Frame-Options header is not present. See: https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /: The X-Content-Type-Options header is not set. This could allow the user agent to render the content of the site in a different fashion to the MIME type. See: https://www.netsparker.com/web-vulnerability-scanner/vulnerabilities/missing-content-type-header/</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /: Cookie PHPSESSID created without the httponly flag. See: https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ Root page / redirects to: login.php</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ Apache/2.4.7 appears to be outdated (current is at least Apache/2.4.54). Apache 2.2.34 is the EOL for the 2.x branch.</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /config/: Directory indexing found.</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /config/: Configuration information may be available remotely.</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /docs/: Directory indexing found.</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /icons/README: Apache default file found. See: https://www.vntweb.co.uk/apache-restricting-access-to-iconsreadme/</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ 8881 requests: 0 error(s) and 9 item(s) reported on remote host</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ End Time:       	2025-06-01 00:44:41 (GMT1) (25 seconds)</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">---------------------------------------------------------------------------</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ 1 host(s) tested</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">┌─[✗]─[root@parrot]─[~/h4cker/cheat_sheets]</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">└──╼ #nikto -h http://10.6.6.13 -p 9090</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">- Nikto v2.5.0</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">---------------------------------------------------------------------------</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">- ERROR: The -port option cannot be used with a full URI</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">┌─[✗]─[root@parrot]─[~/h4cker/cheat_sheets]</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">└──╼ #nikto -h http://10.6.6.13:9090</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">- Nikto v2.5.0</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">---------------------------------------------------------------------------</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">---------------------------------------------------------------------------</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ 0 host(s) tested</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">┌─[root@parrot]─[~/h4cker/cheat_sheets]</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">└──╼ #nikto -h http://10.6.6.11:9090</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">- Nikto v2.5.0</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">---------------------------------------------------------------------------</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ Target IP:      	10.6.6.11</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ Target Hostname:	10.6.6.11</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ Target Port:    	9090</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ Start Time:     	2025-06-01 00:47:39 (GMT1)</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">---------------------------------------------------------------------------</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ Server: No banner retrieved</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /: The anti-clickjacking X-Frame-Options header is not present. See: https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /: The X-Content-Type-Options header is not set. This could allow the user agent to render the content of the site in a different fashion to the MIME type. See: https://www.netsparker.com/web-vulnerability-scanner/vulnerabilities/missing-content-type-header/</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ No CGI Directories found (use '-C all' to force check all possible dirs)</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ 8073 requests: 0 error(s) and 2 item(s) reported on remote host</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ End Time:       	2025-06-01 00:47:59 (GMT1) (20 seconds)</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">---------------------------------------------------------------------------</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ 1 host(s) tested</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">┌─[✗]─[root@parrot]─[~/h4cker/cheat_sheets]</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">└──╼ #nikto -h http://10.6.6.11:8080</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">- Nikto v2.5.0</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">---------------------------------------------------------------------------</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ Target IP:      	10.6.6.11</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ Target Hostname:	10.6.6.11</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ Target Port:    	8080</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ Start Time:     	2025-06-01 00:48:47 (GMT1)</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">---------------------------------------------------------------------------</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ Server: No banner retrieved</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /: The anti-clickjacking X-Frame-Options header is not present. See: https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /: The X-Content-Type-Options header is not set. This could allow the user agent to render the content of the site in a different fashion to the MIME type. See: https://www.netsparker.com/web-vulnerability-scanner/vulnerabilities/missing-content-type-header/</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ No CGI Directories found (use '-C all' to force check all possible dirs)</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ 8073 requests: 0 error(s) and 2 item(s) reported on remote host</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ End Time:       	2025-06-01 00:49:05 (GMT1) (18 seconds)</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">---------------------------------------------------------------------------</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ 1 host(s) tested</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">┌─[✗]─[root@parrot]─[~/h4cker/cheat_sheets]</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">└──╼ #nikto -h http://10.6.6.12:3000</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">- Nikto v2.5.0</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">---------------------------------------------------------------------------</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ Target IP:      	10.6.6.12</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ Target Hostname:	10.6.6.12</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ Target Port:    	3000</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ Start Time:     	2025-06-01 03:47:33 (GMT1)</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">---------------------------------------------------------------------------</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ Server: No banner retrieved</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /: Retrieved access-control-allow-origin header: *.</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /: Uncommon header 'x-recruiting' found, with contents: /#/jobs.</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ No CGI Directories found (use '-C all' to force check all possible dirs)</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /robots.txt: Entry '/ftp/' is returned a non-forbidden or redirect HTTP code (200). See: https://portswigger.net/kb/issues/00600600_robots-txt-file</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /robots.txt: contains 1 entry which should be manually viewed. See: https://developer.mozilla.org/en-US/docs/Glossary/Robots.txt</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /: The X-Content-Type-Options header is not set. This could allow the user agent to render the content of the site in a different fashion to the MIME type. See: https://www.netsparker.com/web-vulnerability-scanner/vulnerabilities/missing-content-type-header/</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.jks: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /archive.alz: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.6.egg: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /6.tgz: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /1066.tar.bz2: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /106612.jks: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /1066.alz: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /106.tar.lzma: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /dump.cer: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /site.tar.bz2: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /6.alz: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /backup.war: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /backup.pem: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /106612.tar.bz2: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /site.alz: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10_6_6_12.tar.bz2: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /106612.tar.lzma: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /archive.egg: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /database.egg: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /106.pem: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /dump.tar.lzma: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /12.tar.lzma: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.egg: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /106.tgz: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /database.tar: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /12.cer: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /dump.egg: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /1066.tar: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.6.6.12.alz: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.6.cer: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /site.pem: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /12.pem: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /archive.jks: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /106612.tgz: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.6.6.alz: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /archive.pem: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /1066.pem: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /backup.egg: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.6.tar.lzma: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.6.6.12.egg: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /106.cer: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /106612.cer: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /site.tar: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /backup.alz: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.6.tar.bz2: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /database.pem: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.6.6.egg: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.6.alz: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /dump.tar: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /database.tar.bz2: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /archive.tar.bz2: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /1066.egg: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.cer: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /site.egg: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /dump.pem: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.pem: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.6.6.12.cer: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.6.6.war: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.6.6.pem: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /1066.cer: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10_6_6_12.tar.lzma: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /dump.alz: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /106612.tar: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /dump.tar.bz2: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /archive.tar.lzma: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.6.6.12.jks: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /6.tar: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10_6_6_12.war: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /site.tar.lzma: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /database.tar.lzma: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.6.tar: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /12.egg: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.tar.lzma: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /1066.tar.lzma: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /12.jks: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.6.6.12.tgz: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /6.cer: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /site.cer: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10_6_6_12.pem: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10_6_6_12.tar: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.6.pem: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /database.war: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /database.cer: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.6.6.12.tar: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.6.6.12.pem: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10_6_6_12.tgz: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.tgz: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /site.tgz: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /6.jks: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.alz: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /12.tar.bz2: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /backup.cer: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /1066.tgz: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.tar: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /database.jks: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.6.6.12.tar.lzma: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /backup.tgz: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.6.6.12.war: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /106.war: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10_6_6_12.jks: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /106612.egg: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /dump.war: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /1066.jks: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /backup.jks: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10_6_6_12.cer: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.war: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /database.alz: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /backup.tar.lzma: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /6.pem: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /6.war: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /site.jks: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /106612.war: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /106612.pem: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.6.war: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.6.6.tar: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /backup.tar.bz2: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.6.6.tar.lzma: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /106.jks: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /106.alz: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10_6_6_12.egg: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /6.tar.lzma: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /backup.tar: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /dump.jks: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.6.6.tar.bz2: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10_6_6_12.alz: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.6.6.jks: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /6.tar.bz2: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /12.war: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.6.tgz: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /archive.tgz: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.tar.bz2: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.6.6.cer: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.6.6.12.tar.bz2: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /12.alz: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /archive.tar: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /12.tar: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /archive.cer: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /106612.alz: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.6.jks: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /10.6.6.tgz: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /site.war: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /6.egg: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /1066.war: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /106.tar: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /database.tgz: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /archive.war: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /106.tar.bz2: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /dump.tgz: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /12.tgz: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /106.egg: Potentially interesting backup/cert file found. . See: https://cwe.mitre.org/data/definitions/530.html</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /ftp/: This might be interesting.</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /public/: This might be interesting.</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /wp-content/plugins/nextgen-gallery/products/photocrati_nextgen/modules/nextgen_addgallery_page/static/jquery.filetree/connectors/jqueryFileTree.php: NextGEN Gallery LFI. See: https://seclists.org/fulldisclosure/2014/Feb/171</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ /wordpress/wp-content/plugins/nextgen-gallery/products/photocrati_nextgen/modules/nextgen_addgallery_page/static/jquery.filetree/connectors/jqueryFileTree.php: NextGEN Gallery LFI. See: https://seclists.org/fulldisclosure/2014/Feb/171</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ 7933 requests: 2 error(s) and 159 item(s) reported on remote host</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ End Time:       	2025-06-01 03:54:43 (GMT1) (430 seconds)</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">---------------------------------------------------------------------------</span></p>
<p style=" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px; line-height:100%;"><span style=" font-family:'Consolas'; font-size:9pt;">+ 1 host(s) tested</span></p></body></html>

#### Interesting Finds per host


#####  Host-1


###### Target Port


- 8080

- 9090

###### Server


- No banner retrieved

- No banner retrieved

###### Header


- not set

- not set

#####  Host-2


###### Target Port


- 3000

###### Server


- No banner retrieved

###### Header


- not set

###### DIrectories Discovered


- /dump.tgz

- /database.tgz

- /ftp/

- /public/

#####  Host-3


###### Target Port


- 80

###### Server


- Apache/2.4.7 (Ubuntu)

###### Header


- PHP/5.5.9-1ubuntu4.29

###### Root Page


- redirects to: login.php

###### DIrectories Discovered


- /config/

- /docs/

- /icons/REAME

### Phase 3: Web App Assessment (ZAP)


#### What I did:


##### Based on the Nikto results, I progressed to OWASP ZAP for a more in-depth and interactive analysis of the web applications. I chose ZAP to perform both passive and active scans, observe requests in real time, and explore site structure using spidering tools.


#### Why I did it:


##### Unlike Nikto, ZAP allows manual interaction, auth testing, and deeper scan customization


##### I can inspect HTTP headers, cookies, authentication flows, and inject test payloads


##### ZAP supports proxying a browser, ideal for dynamic and client-heavy web apps


## Attack


### 

## ExFill & Reporting


## References


