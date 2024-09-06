# **Google Dorking (Google Hacking)**

# **Google Dorking Cheat Sheet**

# ---

# **Overview:**

Google Dorking, or Google Hacking, is a technique that uses advanced search operators to find information online that may not be easily accessible through standard searches. Despite the term "hacking," it is legal and often used by security professionals to identify system vulnerabilities.

# **How It Works:**

Google Dorking uses specific search operators combined with keywords to refine search results.These operators can help locate specific file types, search within a particular website, find certain keywords in page titles, and more. The technique leverages Google's indexing of web pages, making all accessible information available to anyone searching.

# **Common Techniques:**

**\- filetype::** Searches for specific file types (e.g., filetype:pdf).  
**\- inurl::** Finds words within a URL (e.g., inurl:login).  
**\- intext:**: Searches for text within a webpage (e.g., intext:"password").  
**\- intitle::** Looks for terms in page titles (e.g., intitle:"index of").  
**\- link:**: Finds pages linking to a specific URL (e.g., link:example.com).  
**\- site::** Searches within a specific site (e.g., site:example.com).

# **Dangers:**

Google Dorking can inadvertently expose sensitive information like unprotected databases or server credentials. It can reveal website vulnerabilities, leading to potential cyberattacks, data breaches,and privacy violations. Misuse of these techniques can breach privacy laws and Google's terms of service.

# **Prevention Measures:**

\- **Restrict Information:** Avoid sharing sensitive data online or ensure it is properly protected.  
\- **Robust Robots.txt:** Configure the robots.txt file to prevent search engines from indexing sensitive pages.  
\- **NoIndex/NoFollow Tags:** Use these tags to keep specific pages out of search results.  
\- **Regular Website Audits:** Conduct audits to identify and fix vulnerabilities.  
\- **Limit Permissions:** Set proper file and directory permissions.  
\- **Security Tools:** Implement security tools and firewalls to monitor and prevent a

# **Cheat Sheet:**

* ## **File Searching**

Use these commands to find different types of files (Word documents, PDFs, Excel spreadsheets, etc.) on web servers

| Purpose | Google Dorking Command |
| :---: | :---: |
| Find Microsoft Word documents | filetype:doc |
| Find text documents | filetype:txt |
| Find PowerPoint presentations | filetype:ppt |
| Find PDF files | filetype:pdf |
| Find Excel spreadsheets | filetype:xls |

* ## **Directories & Indexes**

Find open directories or indexes that are publicly accessible on web servers.

| Purpose | Google Dorking Command |
| ----- | ----- |
| Find open directories | intitle:"Index of /" |
| Search for directory listings | intitle:"Index of /" or intitle:"Browse Directory" |
| Identify exposed Git repositories | intitle:"index of" inurl:.git |

* ## **Default Pages**

Locate default or misconfigured pages for common web servers.

| Purpose | Google Dorking Command |
| ----- | ----- |
| Find Apache default pages | intitle:"Apache2 Debian Default Page" |
| Find Nginx default pages | intitle:"Welcome to nginx\!" |
| Find open IIS servers | intitle:"Welcome to IIS" |

* ## **Login Pages**

Find common login pages of web services.

| Purpose | Google Dorking Command |
| ----- | ----- |
| Search for login pages | intitle:"Login" or intitle:"Log In" |

* ## **Configuration & Admin Pages**

Locate administrative or configuration files that may have been exposed on the web.

| Purpose | Google Dorking Command |
| ----- | ----- |
| Find exposed configuration files | intitle:"config.json" |
| Find vulnerable Apache Tomcat installations | intitle:"Apache Tomcat" intitle:"Administration" |
| Discover open Jenkins instances | intitle:"Dashboard \[Jenkins\]" |

* ## **Database & Repositories**

Identify publicly accessible databases or repositories.

| Purpose | Google Dorking Command |
| ----- | ----- |
| Search for exposed Subversion repositories | intitle:"Index of /svn" |
| Discover exposed MongoDB databases | intitle:"MongoDB Server Information" |
| Search for open Elasticsearch instances | intitle:"Elasticsearch Head" |
| Identify open CouchDB instances | intitle:"CouchDB \- Welcome" |

* ## **Web Services**

Identify misconfigured or unprotected web services.

| Purpose | Google Dorking Command |
| ----- | ----- |
| Find open phpMyAdmin installations | intitle:"phpMyAdmin" or intext:"phpMyAdmin MySQL-Dump" |
| Locate exposed Microsoft SharePoint docs | intitle:"Microsoft SharePoint" intext:"Sign in to SharePoint" |
| Find exposed Redis servers | intitle:"Redis" intext:"Server Information" |

* ## **Networking Devices**

Find exposed networking devices like routers, printers, and SCADA systems.

| Purpose | Google Dorking Command |
| ----- | ----- |
| Find open RDP servers | intitle:"remote desktop inurl:rdweb" |
| Find open SMB shares | intitle:"Index of /smb.conf" |
| Identify open AXIS cameras | intitle:"Live View / \- AXIS" |
| Find open Siemens SCADA systems | intitle:"Siemens SIMATIC" intext:"Web Server" |

* ## **Devices & Webcams**

Search for publicly accessible cameras and IoT devices.

| Purpose | Google Dorking Command |
| ----- | ----- |
| Discover unsecured webcams | intitle:"webcamXP 5" inurl:8080 |
| Find open Panasonic IP cameras | intitle:"Panasonic Network Camera" |
| Identify open Samsung Smart TVs | intext:"SMART TV" inurl:password.txt |

* ## **Routers & Networking Devices**

Identify routers and networking equipment that may be vulnerable.

| Purpose | Google Dorking Command |
| ----- | ----- |
| Find open Netgear routers | intitle:"Netgear" intext:"NETGEAR" |
| Search for open MikroTik routers | intext:"MikroTik RouterOS" inurl:winbox |
| Discover open Ubiquiti devices | intext:"Ubiquiti" intitle:"AirOS" |

## 

## 

* ## **Advanced Google Dorking Command**

Use advanced commands for more targeted searches.

| Purpose | Google Dorking Command |
| ----- | ----- |
| Search for vulnerable webcams | intitle:"D-Link" inurl:"/view.htm" |
| Find Elasticsearch instances with specific data | intext:"kibana" intitle:"Kibana" |
| Explore open MongoDB instances with no authentication | intext:"MongoDB Server Information" intitle:"MongoDB" |
| Identify exposed OpenCV instances | intitle:"OpenCV Server" inurl:"/cgi-bin/guestimage.html" |
| Find exposed InfluxDB instances | intitle:"InfluxDB \- Admin Interface" |
| Locate RabbitMQ management interfaces | intitle:"RabbitMQ Management" |
| Discover exposed Jenkins builds | intitle:"Console Output" intext:"Finished: SUCCESS" |
| Find exposed Grafana dashboards | intitle:"Grafana" inurl:"/dashboard/db" |
| Explore open NVIDIA Jetson devices | intitle:"NVIDIA Jetson" intext:"NVIDIA Jetson" |
| Locate open Fortinet devices | intext:"FortiGate Console" intitle:"Dashboard" |
| Discover exposed OpenEMR installations | intitle:"OpenEMR Login" inurl:"/interface" |
| Find exposed Jenkins Script Console | intitle:"Jenkins Script Console" intext:"Run groovy script" |

