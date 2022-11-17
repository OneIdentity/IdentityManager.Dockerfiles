# escape=`

ARG VERSION=8.2
ARG WINDOWSVERSION=windowsservercore-ltsc2019

FROM oneidentity/oneim-job:windows-amd64-${VERSION}-${WINDOWSVERSION}

COPY mysql-connector-net.msi /Installer/

RUN Start-Process msiexec -ArgumentList '/a','C:\installer\mysql-connector-net.msi','TARGETDIR=C:\Installer\mysql_extracted','/qn' -Wait ; `
    $filePath = (Get-ChildItem 'C:\installer\mysql_extracted\PFiles\MySQL\').FullName + '\Assemblies\v4.8\MySql.Data.dll' ; `
    Copy-Item $filePath -Destination 'C:\Program Files\One Identity\One Identity Manager' ; `
    Remove-Item 'C:\Installer\mysql_extracted\' -Recurse