# escape=`

ARG VERSION=8.2
ARG WINDOWSVERSION=windowsservercore-ltsc2019

FROM oneidentity/oneim-job:windows-amd64-${VERSION}-${WINDOWSVERSION}

COPY DSDRIVER.zip /Installer/

RUN Expand-Archive -Path 'C:\installer\DSDRIVER.zip' -DestinationPath 'C:\installer'; `
    Start-Process 'C:\installer\DSDRIVER\setup.exe' -ArgumentList '/o' -Wait; `
    Remove-Item 'C:\installer\DSDRIVER\' -Recurse