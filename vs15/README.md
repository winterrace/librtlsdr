Compilation instructions
===========
To compile the library and the programs in Visual Studio 2015 (newer versions should work as well), you first need to acquire the libusb and pthreads-win32 libraries and copy the relevant files (see below) in folders called "libusb" and "pthread" placed parallel to the librtlsdr folder. Suitable sources are https://github.com/libusb/libusb/releases (tested with 1.0.22 zip) and the subdirectory "Pre-built.2" from ftp://sourceware.org/pub/pthreads-win32/pthreads-w32-2-9-1-release.zip. 

The folder structure has to look like this

    librtlsdr
        include
        src
        vs15
        <and so on>
    
    pthread
        include
        lib
        <and so on>
	
    libusb
        libusb
        msvc
        <and so on>
    
Next you have to open libusb/msvc/libusb_2015.sln and compile libusb for Win64 (Release and Debug Build).
   
Then simply open librtlsdr/vs15/librtlsdr.sln in Visual Studio and select between debug/release build options.
