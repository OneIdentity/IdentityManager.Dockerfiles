# Jobservice for SAP R/3 sync services

Build the container image:

```
copy path/to/NCo30<Patch>_Net40_x64.msi SAPNCo.msi
docker build . --tag oneim-job-sap --build-arg VERSION=8.2 --build-arg WINDOWSVERSION=windowsservercore-ltsc2019
```

You can set the following build arguments:

| Name             | Default                    | Description                                                |
|------------------|----------------------------|------------------------------------------------------------|
| VERSION          | 8.2                        | Version of Identity Manager containers to be used as base. |
| WINDOWSVERSION   | windowsservercore-ltsc2019 | Windows version the base containers are built for.         |
