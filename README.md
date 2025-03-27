# Building-a-SOC-with-Open-Source-tools
In this project I am going to design and implement a robust Security Operations Center (SOC) using four leading open-source tools.
Introduction to SOC: Understand the fundamental concepts and importance of a Security Operations Center in cybersecurity.
**TheHive**: Master TheHive, an open-source SIRP (Security Incident Response Platform) for managing and analyzing security incidents.
**MISP**: Learn how to utilize MISP (Malware Information Sharing Platform) to collect, share, and analyze threat intelligence.
**Elasticsearch**: Dive into Elasticsearch to understand how to store, search, and analyze large volumes of security data efficiently.
**Cortex**: Discover how to use Cortex for automated analysis of observables and integration with other SOC tools.
![image](https://github.com/user-attachments/assets/c56be916-f4d5-40d7-8a53-6a6d75e58b55)

## It starts like this:
Logs are created from operating systems or services such as windows , ubuntu and AWS cloudtrail. Beats are installed on the log sources which then acts as a pipeline to logstash for further analysis.
Logstash then passes the logs with further information in which they make the logs readable to us into elasticsearch. Elasticsearch takes the processsed logs from logstash and acts as a storage for theses logs in addition to its powerful search capabilities.
Elastisearch allows us to quickly find logs and analyze the security data. Then we have Kibana which is a visualization tool where you can interact with the data and write a different sort of queries to fetch the log information  its like an graphical interface for the data
from elasticsearch, with kibana you can create detailed dashboard and analyze data further. These component together are the basis for ELK , and they are all being run on Docker.
Now on to TheHive.
TheHive is an instant response platform which receives alerts from the ELK specifically elasticsearch, and it helps us manage and investigate security incidents. 
Cortex provides automated analysis and enrichment of our observables. For example it can take URLS , analyze them, cross reference with various threat intelligence platforms and give a detailed report back to theHive.
MISP is a threat intelligence sharing platform, which keeps our SOC up to date.
All of this tools helps us, the security analysts , to detect, analyze and respond to a security threat.
We will now implement and manage a Security Operation Center using these open-source tools.
