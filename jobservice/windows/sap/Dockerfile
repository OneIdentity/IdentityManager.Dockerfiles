# escape=`

ARG VERSION=8.2
ARG WINDOWSVERSION=windowsservercore-ltsc2019

FROM oneidentity/oneim-job:windows-amd64-${VERSION}-${WINDOWSVERSION}

COPY SAPNCo.msi /Installer/

RUN Start-Process msiexec -ArgumentList '/a','C:\Installer\SAPNCo.msi','TARGETDIR=C:\Installer\sap_nco_extracted','/qn' -Wait ; `
    Copy-Item 'C:\Installer\sap_nco_extracted\sapnco.dll' -Destination 'C:\Program Files\One Identity\One Identity Manager' ; `
    Copy-Item 'C:\Installer\sap_nco_extracted\sapnco_utils.dll' -Destination 'C:\Program Files\One Identity\One Identity Manager' ; `
    Copy-Item 'C:\Installer\sap_nco_extracted\libicudecnumber.dll' -Destination 'C:\Program Files\One Identity\One Identity Manager' ; `
    Copy-Item 'C:\Installer\sap_nco_extracted\rscp4n.dll' -Destination 'C:\Program Files\One Identity\One Identity Manager' ; `
    Copy-Item 'C:\Installer\sap_nco_extracted\Win\System64\msvcp100.dll' -Destination 'C:\Program Files\One Identity\One Identity Manager' ; `
    Copy-Item 'C:\Installer\sap_nco_extracted\Win\System64\msvcr100.dll' -Destination 'C:\Program Files\One Identity\One Identity Manager' ; `
    Remove-Item 'C:\Installer\sap_nco_extracted\' -Recurse
