# escape=`

ARG VERSION=8.2
ARG WINDOWSVERSION=windowsservercore-ltsc2019

FROM oneidentity/oneim-job:windows-amd64-${VERSION}-${WINDOWSVERSION}

COPY HDB_CLIENT_WINDOWS_X86_64.zip /Installer/

RUN Expand-Archive -Path 'C:\installer\HDB_CLIENT_WINDOWS_X86_64.zip' -DestinationPath 'C:\installer'; `
    Start-Process 'C:\installer\HDB_CLIENT_WINDOWS_X86_64\hdbinst.exe' -ArgumentList '--batch' -Wait; `
    Remove-Item 'C:\installer\HDB_CLIENT_WINDOWS_X86_64\' -Recurse