# Wireshark Statistics

<h2>Description</h2>
In this wireshark task, I explore wiresharks statistics feature to nagivate to capture file properties, hierarchy stats, conversations, endpoints, and even follow http streams to extract a malicious object from a privious pcap used in tcpdump but with much greater ease. 


<h2>Languages and Utilities Used</h2>

- <b>wireshark</b>
- <b>linux CLI</b>


<h2>Environments Used </h2>

- <b>Unbuntu</b> 

<br />
<br />
Using statistics in wireshark on a sample pcap containing a malicious object.

![1) using statistics](https://github.com/user-attachments/assets/84e0398a-a0cf-45b6-a74c-a336ec43c999)

<br />
<br />
Exploring capture file properties to show basic hashes of the pcap and time of first/last pcap to match up with the investigation timeline. 

![2) capture file properties](https://github.com/user-attachments/assets/50d3c220-d42b-45d2-b25d-3fa9678da2c4)

<br />
<br />  
Exploring protocol heriarchy stats to show tcp, udp, smb, tls, http, etc protocols.

![3) hierarchy statistics](https://github.com/user-attachments/assets/7269bf04-bb5d-45a5-8a3b-361613cf36f1)

<br />
<br />
Filtering conversations statistics by bytes in descending order to show the top conversation within the pcap.

![4) conversations sort by bytes to see top convo](https://github.com/user-attachments/assets/c26c066d-80ad-4f6a-8a22-9fecf8acd28f)

<br />
<br />
Enumerating endpoint statistics by bytes to show top endpoints within the pcap. 

![5) endpoints sort by bytes](https://github.com/user-attachments/assets/11afdbee-7d99-4a9d-b1f3-8e3b0cb0ace7)

<br />
<br />
Using http>requests to show all http requests within the pcap making it visually easier to see what objects were requested from which ip. This instance shows .audiodg.exe retreived from 103.232.55.148 

![6) http request shows exe](https://github.com/user-attachments/assets/0c91c78e-bedf-484d-9404-39e93eb8f658)

<br />
<br />
Using packet 1186 as an example and right clicking to select follow http stream shows the entire http stream for that specific packet. Furhter filtering can occur by changing the Entire Convseration section in the bototm left. 

![7) following http stream for entire conversation](https://github.com/user-attachments/assets/d67ab165-8f1d-4096-8a7f-03bf668fe29e)

<br />
<br />  
File>export> http objects allows me to export specfic objects within the pcap. In this isntance, it is the .audiodg.exe malware. 

![8) extracting object from http](https://github.com/user-attachments/assets/36123d5b-e6e3-45fe-94f4-70105cd6f9ee)

<br />
<br />
Running file on .audiodg.exe shows it is a PE32 executable. Running its sha256 hash in virustotal shows 57 vendor flags for the malware. 

![9) sha256 check on virus total](https://github.com/user-attachments/assets/1d7b4fe0-0d1d-4fc9-b3a5-e96d00d0ecf9)
<br />
<br />
