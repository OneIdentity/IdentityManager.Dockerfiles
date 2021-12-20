# escape=`

ARG VERSION=8.2
ARG WINDOWSVERSION=windowsservercore-ltsc2019

FROM oneidentity/oneim-job:windows-amd64-${VERSION}-${WINDOWSVERSION}

COPY ActiveRoles.exe /Installer/
RUN C:/installer/ActiveRoles.exe /quiet /install ADDLOCAL=Tools /IAcceptActiveRolesLicenseTerms
