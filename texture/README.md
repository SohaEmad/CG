# texture

for Unable to start debugging. The startup project could not be launched. Verify debug settings for the startup project. error 
solved by deleting CurrentSettings.vssettings

To find the location of this file, go to Tools -> Options -> Environment -> Import and Export Settings. Typically it's found at: Documents\Visual Studio 2015\Settings

copy image_loader.cpp into project source files 

put image_loader.h in C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\VC\Auxiliary\VS\include   folder 

image_loader.cpp should contain a pch.h header file even after set precompiled header to no 

image should be in the same folder or write full path 

glut32.dll is in system32 folder and project folder 

linker include 
opengl32.lib 
glut32.lib

