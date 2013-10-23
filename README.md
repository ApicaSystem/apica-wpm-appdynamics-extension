ApicaAppDynamics JAVA Monitor Extension
=======================================
Links
-------------------
* http://docs.appdynamics.com/display/PRO13S/Build+a+Monitoring+Extension+Using+Scripts

Notes
-------------------
* Input: 3 args. (username, password, baseApiUrl)
* You can hit CTRL-F5 from Netbeans to run it against an API instance running. (Got some hardwired arguments that you can change in project props). Values should show in debug.
* You can also call the .jar file.  >java -jar ApicaMonitor.jar - and output should arrive to the console (stdout)
* Output: For each check, outputs "value" that is the current value gotten from /checks/, and also outputs "uptime", also from /checks/, if severity=IW, then uptime is 1. Otherwise uptime is 0.
