This introduction will guide you to create Open CV 3.1 project in eclipse KEPLEP
OS : Window 10 64 bit
1. Download installations
	1.1 CMake: http://www.cmake.org/ .You'd choice Windows ZIP
	1.2 OpenCV: http://opencv.org/
	1.3 MinGW 64bit: https://sourceforge.net/projects/mingw-w64/ or direct link :
	http://iweb.dl.sourceforge.net/project/mingw-w64/Toolchains%20targetting%20Win32/Personal%20Builds/mingw-builds/installer/mingw-w64-install.exe
	1.4 Eclipse: http://www.eclipse.org/downloads/packages/eclipse-ide-cc-developers/keplersr2
2. Install
	2.1 CMake
		Unzip CMake to %CMAKE_HOME% folder (You'd choice your own location). Example C:\cmake-3.5.2-win32-x86
		Add %CMAKE_HOME%\bin to PATH [Optional]
	2.1 OpenCV
		Open opencv-3.1.0.exe choice your own location -> %OPENCV_DIR%. C:\Programming\OpenCV
		OpenCV folder will look like this:
			build
			sources
			...
	2.3 Install MinGW by open mingw-w64-install.exe
		Select Architecture x86_64
		Leave all the rest defaul
		Choice which folder you want to install -> %MINGW_HOME%
		Add %MINGW_HOME%\bin to PATH. Example C:\~\mingw64\bin
	2.4 Unzip eclipse
	

3 Build your own OpenCV binary. Because OpenCV only provides Visual compiler pre-built libraries
	3.1 Open CMAKE
		SET source code to %OPENCV_DIR%\source
		SET build the binaries to %OPENCV_DIR%\mingw-bin
		Hit Configure
			MinGW Makefies
			Use default native compilers
			Finish
		If you see some errors like
			CMake Error: CMAKE_CXX_COMPILER not set, after EnableLanguage
			CMake Error: CMAKE_C_COMPILER not set, after EnableLanguage
		Make sure g++ is available in PATH. Hit Configure button again. ( For the long story : http://stackoverflow.com/questions/13054451/cmake-problems-specifying-the-compiler-2)
		When you see Configuring done. Hit Generate button
		When you see
			Configuring done
			Generating done
		You've been done with cmake
	3.2 Move to %OPENCV_DIR%\mingw-bin
		Run cmd mingw32-make.exe and wait
	3.3 Create project. Open eclipse
			Create c++ project
			Right click project select Properties
			C/C++ Build >> Setting
				GCC C++ Compiler/ Includes 
					Add ${OPENCV_DIR}\build\include or fullpath to that folder
				MinGW c++ linker
					Libraries
						in -l
							Add libopencv_highgui310
							Add libopencv_core310
						in -Leave
							Add %OPENCV_DIR%\mingw-bin\bin
That's it!

Reference
http://eyalarubas.com/opencv-installation-on-windows-netbeans-mingw.html
http://stackoverflow.com/questions/13054451/cmake-problems-specifying-the-compiler-2
http://stackoverflow.com/questions/34724768/c-opencv-3-1-cant-use-mat-or-most-of-the-opencv-things-like-in-the-tutorial
			
		
	
