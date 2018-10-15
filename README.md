# sysproxy
Agent of updating network proxy settings for x86/x64 Windows.

# Description
X64 Windows doesn't allow applications running in x86 mode to modify system proxy settings and vise versa.
This project provides a tiny tool in both x86 and x64 binary to alert system proxy settings so you could
pack them into your own application and run accordingly without having to compile your own application
in both x86 and x64 platforms.

# Usage
Compile the whole project with Visual Studio.

Run it in command line with the following parameters:
```
sysproxy global <proxy-server> [<bypass>]
         Set the global proxy to <proxy-server> with the given bypass list.
         The proxy server is a string like: localhost:8080 or 127.0.0.1:8080
         The bypass list is a string like: localhost;127.*;10.* without trailing semicolon.
sysproxy pac <pac-url>
         Use a PAC for proxy settings.
         The pac url is a url to the PAC file you try to use.
sysproxy off
         Don't use proxy at all.
```
