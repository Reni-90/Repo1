# Tizen Studio 2.3 Release Notes

## IDE and Tools

### New Features

-	Tizen Studio

    -   JAVA 9 support is added in Tizen Studio. Users can now download and install Tizen Studio along with JAVA 9.
-	Base IDE
	-   Tizen Studio is updated from Eclipse Mars to Eclipse Oxygen, to help user with improved performance and bug fixes.
	-   CDT is updated to 9.3.2 and the Debugger is migrated from CDI to DSF enabling faster debugging and easier extension.
-	Emulator Manager
	-   The Emulator Manager is updated to support JAVA 9.
	-   Intel HAXM is upgraded to 7.0.0 to support Tizen Emulators on Windows 10 and Mac.
-	Device Manager
	-   The Emulator Manager is updated to support JAVA 9.
-	Profiling Tools
	-   Dynamic Analyzer and TTrace are updated to support JAVA 9.
-	Installer, Package Manager, and Uninstaller
	-   Package Manager and Installer are updated to support JAVA 9.
-	RT IDE
	-   RT IDE Base IDE is migrated from Eclipse Mars to Eclipse Oxygen, to help user with improved performance and bug fixes.
-   Config SDK
	-   Supports Import/Export of device-def.json file.
	
### Changed Features

-	Certificate Manager
	-   ST Certification is simplified by enabling auto certification generation using Samsung Account Sign-in.

### Fixed Bugs

-	Emulators
	-   Fixed a bug in emulator-manager which shows the deleted skin in the list of device definition.
-	Device Manager
	-   Fixed a bug in Tizen studio and Device manager. Now the remote device manager of Tizen studio and remote device manager of Device Manager are in sync.
-	Web and Native IDE
	-   Fixed a bug in common-eplugin, earlier it used to return last connected device even if the device was disconnected.

### Known Issues

-	Common
   	-   If you install the Tizen Studio in a directory that requires administrator privileges for access, e.g. C:\ProgramFiles, administrator privileges are required to run the Tizen SDK tools.   The Tizen Installer and the Baseline SDK Installer alerts you if you try to install into such a directory.
-	Web and Native IDE
	-   Since Tizen Studio 2.0, the Connection Explorer is replaced with the Device Manager, this can cause errors in the Connection Explorer view. You can fix this in 2 ways:
	    -   Reset the perspective.
            In the Tizen Studio menu, select Window > Perspective > Reset Perspective
    	-   After updating to the Tizen Studio 2.0, run the eclipse.exe -clean -clearPersistedState command. Then launch the Tizen Studio normally.
	-   You can create unit tests for Tizen 2.3.2 and higher version projects only. Now Tizen Studio does not support unit testing for older versions.
-	Web IDE
	-   The Preview tab in the Web Page Editor sometimes does not appear properly. Use an alternative feature, named Web SDK HTML Editor, which has enhanced features compared to the Web Page Editor. Instead of the Previewtab in the Web Page Editor, use the preview (Ctrl + 4) feature of the Web SDK HTML Editor.
	-   In RDS mode, the web unit test result is not updated. 
-	Certificate Manager
	-   Overwriting a duplicate certificate profile in the migration wizard works incorrectly on macOS.
	-   IoT Certification currently requires a user, to manually download and select the certificate.
-	Native UI Builder
	-   If the expanded attribute in a multibutton entry component is set to false, + is displayed.
-	Native Component Designer
	-   The vector-type part is not supported. You cannot see the vector image and change the SVG file.
	-   Playing sound is not supported on Windows® or macOS.
	-   The Component Designer crashes if an alias is selected as the source group of an added item.
-	Emulator
	-   To use the Tizen emulator, install an Intel VTx supported by the CPU, and the latest version of the graphic card driver provided by the vendor. Check the prerequisites for the Tizen emulator from Prerequisites for the Tizen Studio.
	    -   If the host machine is using NVIDIA® Optimus® technology on either Ubuntu or Windows®, you must set the Tizen emulator to run with your NVIDIA graphics card.       For Ubuntu, check the bumblebee project (https://wiki.ubuntu.com/Bumblebee ).           For Windows®, select "High Speed NVIDIA Processor" as "Preferred Graphics processor" in the NVIDIA control panel.
	    -   On Ubuntu if the graphics driver is out-of-date, your Ubuntu desktop session occasionally logs out while launching the Emulator Manager, or the emulator skin is displayed improperly. Check the prerequisites and upgrade to the latest graphics driver.
	-   On Ubuntu 14.04, a shortcut menu can sometimes appear transparent.
	-   On Windows®, depending on your OS theme (such as Non-Aero themes and Windows XP themes), a display surface can be erased for a while if the emulator window is covered with another window. If you click the emulator window, the display surface runs correctly again.
	-   On Windows®, if an error with message ‘Failed to allocate memory’ occurs while executing the emulator, try the following:
	    -   Close some other programs and try to launch the emulator again.
	    -   If the RAM size is set to 768 or 1024 MB for the VM in the Emulator Manager, change it to 512 MB.
	    -   Increase the user area of the virtual memory in the system to 3 GB by entering the bcdedit /setincreaseuserva 3072 command on the console with administrator rights (Windows® 7 only), and reboot.
	-   If you use a MacBook Pro which has both Intel HD and NVIDIA® GPUs, the emulator can be unexpectedly terminated when you execute the emulator with OpenGL ES Ver set to v1.1 & v2.0. Check the emulator configuration in the Emulator Manager, and on the General tab in the Emulator Configuration window, set OpenGL ES Ver to v2.0 & v3.0.
	-   When you launch the Emulator Manager in the Tizen IDE, the Emulator Manager shortcut image is not exposed properly.
	-   Basic Web applications do not install on SD cards.
-	CLI and SDB
	-   The Tizen Studio does not support the SDB bash auto-completion on Windows® (it is available on Ubuntu and macOS).
-	Dynamic Analyzer
	-   When analyzing applications on commercial devices running Tizen 3.0, both newly-released or after a firmware update, the following issues prompts:
	    -   The Core Frequency information is not shown.
	    -   The Screenshots on scene transitions feature will not work.
	-   When analyzing applications on the Tizen 4.0 emulator or reference device, the start-up profiling information is not shown.
	-   The UI Hierarchy viewer feature and start-up profiling are not performed simultaneously.
	-   The Dynamic Analyzer cannot perform Web application profiling with a commercial Tizen device, due to the security policy.
	-   The Dynamic Analyzer cannot show life-cycle information for Web applications.
	-   Widget applications cannot be profiled with the Dynamic Analyzer. They are hidden in the application list on the toolbar for all Tizen platforms, except Tizen 2.3.2.
-	Web Inspector
	-   If your Google Chrome™ browser version is higher than 54, the Web Inspector console and some other functions does not work properly due to Web core compatibility issues.
