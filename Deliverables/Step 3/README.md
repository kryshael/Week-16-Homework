### Step 3: Shodan

Using Shodan and the information gathered from Google Dorking, find any other useful information that can be used in an attack.

- Navigate to [shodan.io](https://www.shodan.io/). 

- Run a scan against the IP address of the DNS server for `demo.testfire.net`. 

#### What open ports and running services did Shodan find? 
|   Ports  |                Services                |
|:--------:|:--------------------------------------:|
|  80 TCP  | HTTP (Apache Tomcat/Coyote JSP Engine) |
|  443 TCP |                  HTTPS                 |
| 8080 TCP | HTTP (Apache Tomcat/Coyote JSP Engine) |

