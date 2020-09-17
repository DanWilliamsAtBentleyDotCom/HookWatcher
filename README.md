# HookWatcher
Developer tool to help identify hookable events in ProjectWise Explorer.

Last built and tested with:
	ProjectWise Explorer 10.0.3.280
	ProjectWise SDK 10.0.3.49
	Visual Studio Professional 2015

This project builds a Custom Module.  You must register the custom module (x86) in order for the DLL to get loaded and for the hooks to be set. 
Please see the ProjectWise V8i SDK Documentation for information about Custom Modules and hooking.
This customizaton is only intended to be used in a development environment since all "output" is to the Output-Debug window.

You may need to modify some of the solution or project properties to match your development environment.

You may also want to set the command line arguments specified on Configuration Properties -> Debugging -> Command Arguments.

Something like this:
-d "servername:datasourcename" -u username -p password

Note that I set the following Windows Environmental Variables via PowerShell, so you many want to create them and set them to valid vaules for your development environment.

[Environment]::SetEnvironmentVariable("PWBinx86Dir", "C:\Program Files (x86)\Bentley\ProjectWise\bin\", "Machine")
[Environment]::SetEnvironmentVariable("PWIncludeX86Dir", "C:\Program Files\Bentley\ProjectWise\SDK\include\", "Machine")
[Environment]::SetEnvironmentVariable("PWLibx86Dir", "C:\Program Files\Bentley\ProjectWise\SDK\lib\Win32\", "Machine")
[Environment]::SetEnvironmentVariable("PWRsrcx86Dir", "C:\Program Files (x86)\Bentley\ProjectWise\rsrc\", "Machine")
[Environment]::SetEnvironmentVariable("PWSDKx86Dir", "C:\Program Files\Bentley\ProjectWise\SDK\", "Machine")

[Environment]::SetEnvironmentVariable("PWBinx64Dir", "C:\Program Files\Bentley\ProjectWise\bin\", "Machine")
[Environment]::SetEnvironmentVariable("PWIncludeX64Dir", "C:\Program Files\Bentley\ProjectWise\SDK\include\", "Machine")
[Environment]::SetEnvironmentVariable("PWLibx64Dir", "C:\Program Files\Bentley\ProjectWise\SDK\lib\x64\", "Machine")
[Environment]::SetEnvironmentVariable("PWRsrcx64Dir", "C:\Program Files\Bentley\ProjectWise\rsrc\", "Machine")
[Environment]::SetEnvironmentVariable("PWSDKx64Dir", "C:\Program Files\Bentley\ProjectWise\SDK\", "Machine")

[Environment]::SetEnvironmentVariable("PythonDir", "C:\DevTools\Python27\", "Machine")
