The CustomRules script measures the QoE(Quality of Experience) metrics for video streaming on Dailymotion.
This script works with Fiddler proxy (available at http://www.telerik.com/fiddler) on Windows OS.

Setup of the proxy:
1) Download the proxy and install it. It will be installed to C:\Program Files (x86)\Fiddler2.
2) In the Fiddler proxy, go to Rules-> Customize Rules and replace the contents of the original script with the CustomRules script.
3) The QoE metrics will be stored in the MS Access database qoe.mdb. So download it and save it in an appropriate location. Now use the
	path name of its location for the variable 'strMDB' in the CustomRules script.
4) The database connector  will work only for 32-bit OS. So if the OS is 64-bit, do as follows:
	a) Close the fiddler proxy.
	b) Open command prompt in admin mode and then cd to 'C:\Program Files (x86)\Fiddler2'.
	c) Now type the command 'ForceCPU.exe x86'. It will then show 'Setting MachineType to x86'.
	d) Restart the fiddler proxy.
5) Now use any embedded Dailymotion video and track its QoE metrics. The embedded videos in the ExampleVideos folder can be used as examples.

