# escape=`
FROM windows-base

SHELL [ "powershell", "-Command", "$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]
RUN chocolatey feature enable -n allowGlobalConfirmation
#RUN $env:PATH
#Install .NET 4.6.2
SHELL [ "powershell", "-Command", "$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]
RUN choco install dotnet-4.6.2
#RUN cinst -y dotnet-4.6.2
#Install 7zip
RUN choco install 7zip.install
#Install MVC3
RUN choco install aspnetmvc.install
#Install MVC4
RUN choco install aspnetmvc4.install
#Install Visual Studio Code
RUN choco install vscode
#Install TortoiseHG
RUN choco install tortoisehg
#Install webdeploy
RUN choco install webdeploy
#Install git
RUN choco install git
#Install ssdt15
#RUN choco install --execution-timeout=0 ssdt15
RUN powershell -Command `
    wget 'https://go.microsoft.com/fwlink/?linkid=863440' -Outfile 'C:\SSDTSetup2015.exe' ; `
    Start-Process -filepath C:\SSDTSetup2015.exe -passthru -wait  ; `
    del C:\SSDTSetup2015.exe
#Install reportviewer2012
RUN choco install reportviewer2012
#Install ms-reportviewer2015
RUN choco install ms-reportviewer2015

#To build it
#docker build -t windows-build .