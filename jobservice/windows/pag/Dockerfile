# escape=`

ARG VERSION=8.2
ARG WINDOWSVERSION=windowsservercore-ltsc2019

FROM oneidentity/oneim-job:windows-amd64-${VERSION}-${WINDOWSVERSION}

ARG SAFEGUARDVERSION
ENV SAFEGUARDVERSION=${SAFEGUARDVERSION:-6.11.30528}

RUN Install-PackageProvider -Name NuGet -Force ; `
    Install-Module -Name safeguard-ps -RequiredVersion $ENV:SAFEGUARDVERSION -Force