Apica WPM - AppDynamics Java Monitor Extension
=======================================
Links
-------------------
* http://docs.appdynamics.com/display/PRO13S/Build+a+Monitoring+Extension+Using+Scripts

Information
-------------------
This AppDynamics Extension will fetch data (response time) from Apica WebPerformance Monitoring (WPM) API and integrate them into the Metric Browser inside of AppDynamics. 
It works on all platforms supported by AppDynamics as it is written in java.

Installation
-------------------
* Requires the AppDynamics Machine Agent
* Requires AppDynamics with support for extensions
* Requires account for Apica WebPerformance Monitoring (http://www.apicasystem.com)

1. Copy the created .jar file (and its lib dependencies) to the /Monitor/ folder in the installation dir of the Machine Agent
2. Set the required values in monitor.xml
3. Start the Machine Agent and it will scan the /Monitor/ folder and execute the Jar file with arguments it finds in monitor.xml
4. Observe the MachineAgent/Log/agent.log
5. Metrics should be popping in into the Metric Browser inside of AppDynamics

Notes
-------------------
* Input: 2 args. (AuthTicket, BaseApiUrl)
* You can hit CTRL-F5 from Netbeans to run it against an API instance running. (Got some hardwired arguments that you can change in project props). Values should show in debug.
* You can also call the .jar file.  >java -jar ApicaMonitor.jar - and output should arrive to the console (stdout)
* Output: For each check, outputs "value" that is the current value gotten from /checks/, and also outputs "uptime", also from /checks/, if severity=IW, then uptime is 1. Otherwise uptime is 0.
