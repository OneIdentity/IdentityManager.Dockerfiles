# Jobservice for MySQL sync services

Build the container image:

```
copy path/to/mysql-connector-net-<Version>.msi mysql-connector-net.msi
docker build . --tag oneim-job-mysql --build-arg VERSION=8.2 --build-arg WINDOWSVERSION=windowsservercore-ltsc2019
```

You can set the following build arguments:

| Name             | Default                    | Description                                                |
|------------------|----------------------------|------------------------------------------------------------|
| VERSION          | 8.2                        | Version of Identity Manager containers to be used as base. |
| WINDOWSVERSION   | windowsservercore-ltsc2019 | Windows version the base containers are built for.         |
