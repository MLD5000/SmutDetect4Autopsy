# SmutDetect4Autopsy
====================

   
# Description:  
    
    This is an Autopsy module plugin that uses skin tone algorithms to analyze a
    subject image or disk and attempts to find image files that are potentially 
    contraband.
    
# Windows-Based Compile instructions:
    1.  Download NetBeans with JDK 8 from Oracle website;
        http://www.oracle.com/technetwork/java/javase/downloads/jdk-netbeans-jsp-142931.html
        -either Version x86 or x64 for Windows
    2.  Install the downloaded install file using the default options.
    3.  Download and install latest version of Autopsy, if you haven't already.
    4.  Download SmutDetect4Autopsy source code files from Github repo.
    5.  Open the NetBeans IDE application.
    6.  Select file->New Project...
    7.  Under "categories" select "NetBeans Modules", and under "Projects" select "Module", then
        click next.
    8.  Set the project name and location (user preference).
    9.  Select Standalone Module and click "Manage".
    10.  Click "Add Platform" and navigate to and select the Autopsy application folder in its install location, 
         then click "Finish".  (probably in Program files/AutopsyX.X.X)
    11.  Click "close" and then "next".
    12.  Set code base name to uk.co.smutdetect, and click "finish".
    13.  In the Projects window pane, right click on the "Source Packages" branch under your project directory tree,
         and select new->Java package.
    14.  Name the package uk.co.smutdetect.autopsy and click finish.
    15.  Open the smutdetect4autopsy source files.
    16.  click and drag the following files to the uk.co.smutdetect package in the NetBeans project tree:
         -Bundle.properties
         -RgbSkinToneDetector.java
         -SmutDetectCategorisedImage.java
         -SmutDetectImageScanner.java
         -YCbCrSkinToneDetector.java
    17.  In the smutDetect4autopsy source files, open the "autopsy" directory and click and drag the following files
         to the uk.co.smutdetect.autopsy package in the NetBeans project tree:
         -Bundle.properties
         -SmutDetectFileIngestModule.java
         -SmutDetectIngestJobSettings.java
         -SmutDetectIngestJobSettingsPanel.form
         -SmutDetectIngestJobSettingsPanel.java
         -SmutDetectIngestModuleFactory.java
         -SmutDetect_32.png
    18.  Right click on the project in the project pane and select "Properties".
    19.  Under Categories and select "libraries".
    20.  Add the following to the "Module Dependencies":
         -Actions APIs
         -Autopsy-Core
         -Lookup API
         -UI Utilities API
         -Utilities API
         Click OK.
    21.  From the NetBean menu bar select Run->Build Poject.
    22.  Right click on the project in the NetBeans Project pane and select "Create nbm".
    23.  Locate this nbm file in the NetBeans project directory.
    24.  Open the Autopsy application.
    25.  From the Autopsy menu bar, select Tools->Plugins.
    26.  Select the "Downloaded" tab and click "Add Plugins".
    27.  Navigate to and select the nbm file created in the NetBeans project folder and click "open".
    28.  Click "install" and use the default options to install the plugin.
    
    This procedure should build and install the SmutDetect4Autopsy module to Autopsy.  To use this module, 
    select tools->Run Ingest Modules and then select the image or device to run the module on.  Then select the 
    available modules to run, which should have smutdetect4autopsy available.
         
    
    
    
