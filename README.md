## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

![Network_Watcher_Diagram](https://github.com/Nalinio/Project_1/blob/main/Diagrams/Network_Watcher.JPG)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the _Yml____ file may be used to install only certain pieces of it, such as Filebeat.

![ELK_Playbook](https://github.com/Nalinio/Project_1/blob/main/Ansible/ELK_Playbook.JPG)

This document contains the following details:
- Description of the Topologu
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly redundancy, in addition to restricting access to the network.
- _TODO: What aspect of security do load balancers protect? What is the advantage of a jump box?_

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the _Jumpbox____ and system network.
- _TODO: What does Filebeat watch for?Filebeat is a lightweight shipper for forwarding and centralizing log data. Installed as an agent on your servers, Filebeat monitors the log files or locations that you specify, collects log events, and forwards them either to Elasticsearch or Logstash for indexing._
- _TODO: What does Metricbeat record?_Metricbeat is a lightweight shipper that you can install on your servers to periodically collect metrics from the operating system and from services running on the server. Metricbeat takes the metrics and statistics that it collects and ships them to the output that you specify, such as Elasticsearch or Logstash.

The configuration details of each machine may be found below.
_Note: Use the [Markdown Table Generator](http://www.tablesgenerator.com/markdown_tables) to add/remove values from the table_.

| Name     | Function | IP Address | Operating System |
|----------|----------|------------|------------------|
| Jump Box | Gateway  | 10.0.0.1   | Linux            |
| web1    |  server     10.0.0.4  |  Linux          |                  |
| web2    |   server    10.0.0.5     Linux             |
| elkvm     server     10.2.0.4       Linux             |

### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the kibana machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- _TODO: Add whitelisted IP addresses_

Machines within the network can only be accessed by ssh.
- _TODO: Which machine did you allow to access your ELK VM? What was its IP address?_my IP 155.45.25.35
- 232
- 

A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses |
|----------|---------------------|----------------------|
| Jump Box | Yes/No              | 10.0.0.1 10.0.0.2    |
|          |                     |                      |
|          |                     |                      |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- _TODO: What is the main advantage of automating configuration with Ansible?_The primary benefit of Ansible is it allows IT administrators to automate away the drudgery from their daily tasks. That frees them to focus on efforts that help deliver more value to the business by spending time on more important tasks.

The playbook implements the following tasks:
- _TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
- ...
- ...

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

![Docker_PS](https://github.com/Nalinio/Project_1/blob/main/Ansible/Docker_PS.JPG)

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- _TODO: List the IP addresses of the machines you are monitoring_List the IP addresses of the machines you are monitoring
webVM1 10.0.0.4
webVM2 10.0.0.5

We have installed the following Beats on these machines:
- _TODO: Specify which Beats you successfully installed_

These Beats allow us to collect the following information from each machine:
- _TODO: In 1-2 sentences, explain what kind of data each beat collects, and provide 1 example of what you expect to see. E.g., `Winlogbeat` collects Windows logs, which we use to track user logon events, etc._

### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 

SSH into the control node and follow the steps below:
- Copy the _playbook file to .
- Update the host file to include.
- Run the playbook, and navigate to web server to check that the installation worked as expected.

_TODO: Answer the following questions to fill in the blanks:/etc/ansible/file/filebeat-configuration.yml_
- _Which file is the playbook? Where do you copy it?_
- _Which file do you update to make Ansible run the playbook on a specific machine? How do I specify which machine to install the ELK server on versus which to install Filebeat on?_edit the /etc/ansible/host file to add webserver/elkserver ip addresses
- _Which URL do you navigate to in order to check that the ELK server is running?www.publicip:5601 (Kibana)



_As a **Bonus**, provide the specific commands the user will need to run to download the playbook, update the files, etc._
