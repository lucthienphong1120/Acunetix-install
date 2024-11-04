## Docker setup guice

### Build image

```sh
docker build -t acunetix_13 .
```

### Run the container

```sh
docker run -d -p 3444:3443 --name acunetix acunetix_13
```

## Local setup guide

Acunetix 13 Linux Install：
1. Install using `bash acunetix_13.0.200217097_x64.sh`
2. Copy the "wvsc" file to the install directory: "/home/acunetix/.acunetix/v_200217097/scanner/"
3. Copy the "license_info.json" license file to the license directory: "/home/acunetix/.acunetix/data/license/"
4. service acunetix status
5. service acunetix stop
6. service acunetix start
