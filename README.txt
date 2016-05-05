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
		Leave all the rest default
		Choice which folder you want to install
	2.4 Unzip eclipse

3 Build your own OpenCV binary. Because OpenCV only provides Visual compiler pre-built libraries
	3.1 Open CMAKE
	
To be continues ... 
	
CMake Error: CMAKE_CXX_COMPILER not set, after EnableLanguage
CMake Error: CMAKE_C_COMPILER not set, after EnableLanguage