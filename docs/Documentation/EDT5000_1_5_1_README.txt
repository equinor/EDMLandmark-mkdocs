********************************************************************************
Halliburton | Landmark Software & Services

Readme for EDT™ Software Version 5000.1.5.1 Patch
********************************************************************************

DATE:            November 20, 2009
PRODUCT:         EDT
PATCH VERSION:   5000.1.5.1.5404 

PLATFORM:        MS Windows XP SP2
                 MS Windows Vista
                 MS Windows Server 2003 SP1

Prerequisite Updates:  EDT 5000.1.5.0    

********************************************************************************

What's In This Release
----------------------
This patch includes a number of bug fixes for the following software 
applications: EDT™, OpenWells®, PROFILE™, StressCheck™, WELLCAT™, and WELLPLAN™. 
For more details, see the sections below:

          Patch Dependencies
          Defects and Enhancements Addressed
          Known Issues
          Installation Instructions
          Patch Bundle File Details
          Landmark Customer Support Information

********************************************************************************

Patch Dependencies
------------------

This patch includes key EDT, OpenWells, PROFILE, StressCheck, WELLCAT and 
WELLPLAN software fixes for customers. 

********************************************************************************

Defects and Enhancements Addressed
----------------------------------

EDT:

823386 - When high amounts of SAM traffic exist in a system, both the SAM server 
	 and client EDT applications encounter performance issues including 
	 applications hanging.
	 
	 To resolve this issue, modifications were made to the SAM service and 
	 Clients which require configuration/verification when deploying this 
	 patch.

         Verify the following parameters on the machine hosting the SAM service.
	 To edit these parameters:
	 - Using the Start/Programs menu navigate to the tools section of the 
	   Engineers Desktop™ program group.
	 - Start the EDM™ Services Controller and double click on the traffic 
	   light icon in the system tray to see the services controller dialog.
	 - Select the “LGC EDM Simultaneous Activity Monitor” service in the 
	   service selection list and press the “Configure Service” button to 
	   see the dialog that allows configuration of the following parameters.
 
	 
	 1) Server Message Buffer (in milliseconds): The time buffer between 
	    outgoing SAM messages at the server. Default value is "0".  A value 
	    of "1000" has produced positive testing results. 

	 2) Server Memory (Mb): The maximum amount of memory, in Mb, that the 
	    SAM server (JVM) is allowed to allocate.  Default value is 64 Mb.  
	    For production environments the recommended setting is 512 Mb. 
	    Increase this value if the SAM server appears to hang due to a lack 
	    of memory.

	 Verify the following System Environment Variables on the machines 
	 hosting EDT Applications.

	    LGC_SAM_CONNECTION_TIMEOUT - In milliseconds, defines the length 
	       of time that client applications should wait for a response when 
	       communicating with the SAM server.  Default is 3 seconds.

	    LGC_SAM_CONNECTION_INTERVAL - In milliseconds, the amount of time 
	       to wait between attempts to contact the SAM server.  Default is 
	       100ms.    


OpenWells:

821664 - Historian - Approving Wellplanning report does not lock associated 
         design.  

821862 - COMPASS re-calculations on application startup potentially causing 
	 loss of other users' data if other user is in OpenWells entering 
	 surveys at the time.

822391 - Cancel option in Catalog selection dialog reverts Section
         Type  selection back to previous value. 

822630 - Report Date incorrect when comparing previous approval point 
	 (Historian Service).

823703 - Problem with producing Norwegian characters in NPD Regulatory 
	 Reporting module


PROFILE:

822271 - Wellbore equipment components are lost if Unit System is changed 
	 before saving to the database.


StressCheck:

819671 - StressCheck Normalized Minimum Safety Factor plot does not match 
	 values. 

821779 - StressCheck displays unsupported Section Type error and prevents
         Save. 

822144 - Triaxial Safety Factor Plot displays normalized safety factors
	 by design, however the toggle button to display absolute safety
	 factors is enabled.  


WELLCAT:

821790 - WELLCAT Annulus Content is not complete.  


WELLPLAN:


821776 - WELLPLAN asking for riser OD/ID for a land well\non subsea
         well on 'create cases from casing design'. 

822387 - WELLPLAN crashes when changing a plot Print Preview from Portrait to
         Landscape. 



********************************************************************************

Known Issues
------------

No additional known issues.


********************************************************************************

Installation Instructions
-------------------------

1)  If running, shut down the current EDT applications.

2)  Run the R5000_EDT_5000.1.5.1.exe to start the installation procedure.

3)  Click OK when a message appears indicating you are about to install Landmark 
    Engineer's Desktop 5000.1.5.1. If you click Cancel, the installation
    will abort. 

4)  Click Setup on the WinZip Self-Extractor dialog.

5)  Press any key to continue when prompted. The required files will auto-
    matically be copied to the correct folder.

6)  Press any key again when prompted. A ** Success!  message will be displayed
    above the prompt to press any key. 


********************************************************************************

EDT5000-1-5-0 BUNDLE FILE NAMES:
--------------------------------------------------------------------------------
 File Details:

 November 20, 2009  R5000_EDT_5000.1.5.1.exe
 November 20, 2009  5000.1.5.1_README.txt
 - Version 5000.1.5.1.5404 

CONTENTS OF PATCH:
--------------------------------------------------------------------------------
Nov 18, 2009 2:07:40 PM, 9170 bytes, Apply-5000.1.5.1.bat
Nov 20, 2009 3:12:52 PM, 3905556 bytes, Common.jar
Jul 10, 2009 7:37:26 AM, 6719 bytes, Copy-Files.bat
Nov 20, 2009 3:26:32 PM, 24576 bytes, DSRegistryService.exe
Nov 20, 2009 3:27:12 PM, 208896 bytes, DSWSController.exe
Nov 20, 2009 2:57:58 PM, 12361928 bytes, DimsNG.jar
Nov 20, 2009 3:17:54 PM, 3977216 bytes, DsGUI.dll
Nov 20, 2009 3:32:50 PM, 3985408 bytes, DsGUIU.dll
Nov 20, 2009 3:11:50 PM, 3191884 bytes, JDataServices.jar
Nov 20, 2009 3:26:32 PM, 143360 bytes, ManagedDSLib.dll
Nov 20, 2009 3:50:56 PM, 3477504 bytes, NGProfile.exe
Aug 5, 2009 1:06:52 PM, 1024 bytes, SetEDTEnvVars_5000_1.bat
Nov 20, 2009 5:46:18 PM, 18731008 bytes, Wellcat.exe
Aug 13, 2009 2:41:30 PM, 5477 bytes, shortcuts.vbs
Nov 20, 2009 5:33:34 PM, 6270976 bytes, stressck.exe
Jul 10, 2009 7:37:26 AM, 1886 bytes, update.vbs
Jul 10, 2009 7:37:26 AM, 1144 bytes, updatelam.vbs

********************************************************************************

Landmark Customer Support Information
-------------------------------------


NORTH AMERICA	
-------------
For support during reg. business hours (7:30am-5:30pm Local Time, Mon. - Fri., 
excluding holidays)*: Houston, Texas TAC (Technical Support Center):

	Telephone: 713-839-2200 or toll free 1-877-HELP-LGC (1-877-435-7542)
	Email:	support@lgc.com  


SOUTH (LATIN) AMERICA	
---------------------
For support during reg. business hours (7:00am-5:00pm Local Time, Mon. - Fri., 
excluding holidays)*: Houston, Texas TAC (Technical Support Center):

Telephone: 1-713-839-3405
Email:     soporte@lgc.com

from:       Local                 Toll Free
Argentina   54-11-4312-8411       0800-800-5263    (9:00am - 6:00pm Local time)* 
Brazil      55-21-3974-4000       0800-891-0837    (8:00am - 5:30pm Local time)*
Chile		                  800-201-898
Colombia    57-1-326-4000         01800-915-4743   (8:00am - 5:00pm Local time)*
Ecuador     59-32-226-1844        (02)226-1908     (8:00am - 5:00pm Local time)*
Mexico      52-555-208-3533       001-888-438-1296 (8:00am - 6:00pm Local time)*
Peru		                  0800-51634
Trinidad	                  1-888-438-1296   (7:00am - 5:00pm Local time)*
Venezuela   58-212-953-0774       0-800-526-3627   (8:00am - 5:00pm Local time)*


EUROPE, MIDDLE EAST, RUSSIA, & AFRICA (Monday - Friday) 	
-------------------------------------
For support during regular business hours (8:00am-5:30pm Local Time, Mon. - 
Fri., excluding holidays)*: Leatherhead, United Kingdom TAC (Technical Support 
Center):

Telephone: 44-1372-868686
Email:     eame_helpdesk@lgc.com

From             Local		    Toll Free
Angola (Luanda)                     1-817-493-5900 (8:00am - 5:00pm Local time)*
Nigeria (Lagos)  234-1-262-0765                   (8:00am - 5:00pm Local time)*
Russia (Moscow)  7-095-755-8300                   (7:00am - 5:00pm Local time)*


MIDDLE EAST & AFRICA (Saturday - Wednesday) 	
---------------------
For support during reg. business hours (Saturday - Wednesday, excluding 
holidays)*: Email:    eame_helpdesk@lgc.com

From			     Local
United Arab Emirates (Dubai) 971-4-3313142  (7:00am - 5:00pm Local time)*
                             971-4-3036446  (7:00am - 5:00pm Local time)*
			     Email: gulf_support@lgc.com
				    eame_helpdesk@lgc.com

Algeria (Algiers)            21-337-7239    (8:30am - 4:30pm Local time)*
Egypt (Cairo)                20-2-517-3095  (8:00am - 4:00pm Local time)*
                             20-2-759-1717  (8:00am - 4:00pm Local time)*
			     Email: eame_helpdesk@lgc.com


ASIA & PACIFIC	
--------------
For support during regular business hours (8am-5pm Local Time, Monday - 
Friday, excluding holidays)*: Perth, Australia TAC 
(Technical Support Center):

Telephone: +61-8-9481-4488 (local) or 1-800-448-488 (toll free)
Email:     apsupport@lgc.com

From                Local            Toll Free
Australia (Perth)   61-8-9481-4488   1-800-448-488    
                    (8:00am - 5:00pm Local time)*
Brunei (Bandar)     67-3-233-5319                     
                    (8:30am - 5:30pm Local time)*
China (Beijing)     86-10-8486-4501  10-800-810-0209  
                    (9:00am - 5:30pm Local time)*
                    2nd Email: bjsupport@lgc.com       10 800 6100 253
India (New Delhi)   91-11-622-1885 (Samit Enterprises) 
                    (9:00am - 5:30pm Local time)*
Indonesia (Jakarta) 62-21-3003-9039  001 803 61284     
                    (7:30am - 4:30pm Local time)*
Japan 		                    00531 61 0021     
                    (8:00am - 5:00pm Local time)*
Malaysia (KL)	    603-2164-1121    1800 803 687      
                    (8:30am - 5:30pm Local time)*
New Zealand (NP)    61-6-755-2318    0800 400 555      
                    (8:00am - 5:00pm Local time)*
Philippines 	                    1800 1611 0207
South Korea 	                    00308 61 0046     
                    (8:00am - 5:00pm Local time)*
Taiwan 		                    0080 161 1350     
                    (8:30am - 5:30pm Local time)*
Thailand (Bangkok)  66-2-278-8100    001 800 611 2784  
                    (8:00am - 5:00pm Local time)*
Vietnam		                    84-8-910-1901     
                    (8:00am - 5:00pm Local time)*



For more information, see the Landmark Support website:

	http://css.lgc.com/InfoCenter/index?page=home

********************************************************************************

© 2009 Halliburton. All rights reserved.

