FROM windows-java:jre1.8.0_91

ENV chocolateyUseWindowsCompression false

RUN powershell -Command \
    iex ((new-object net.webclient).DownloadString('https://chocolatey.org/install.ps1')); \
    choco feature disable --name showDownloadProgress

#To build it
#docker build -t windows-base .