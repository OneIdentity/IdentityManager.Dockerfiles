# escape=`

ARG VERSION=8.2
ARG WINDOWSVERSION=windowsservercore-ltsc2019

FROM oneidentity/oneim-job:windows-amd64-${VERSION}-${WINDOWSVERSION}

RUN Install-PackageProvider -Name NuGet -MinimumVersion 2.8.5.201 -Force ; `
    Install-Module -Name ExchangeOnlineManagement -Force