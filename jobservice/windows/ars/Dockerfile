# escape=`

ARG VERSION=8.2
ARG WINDOWSVERSION=windowsservercore-ltsc2019

FROM oneidentity/oneim-job:windows-amd64-${VERSION}-${WINDOWSVERSION}

COPY ActiveRoles.exe /Installer/

RUN Start-Process C:/installer/ActiveRoles.exe -ArgumentList '/quiet','/install','ADDLOCAL=Tools','/IAcceptActiveRolesLicenseTerms' -Wait
