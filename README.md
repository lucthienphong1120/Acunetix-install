# Acunetix-install

Acunetix 13 - Vulnerability Scanner install (included docker version)

## Prebuild version

```sh
docker pull ltp1120/acunetix_13:latest
docker run -d -p 3443:3443 --name acunetix acunetix_13
```

Reference: [Docker Hub](https://hub.docker.com/r/ltp1120/acunetix_13)

![image](https://github.com/user-attachments/assets/b02ea690-6d53-411f-aae2-6c901e6a7d1f)

Default account:
+ Email: `admin@acunetix.com`
+ Password: `Acunetix@123`

## Docker setup guide

### Build image

```sh
docker build -t acunetix_13 .
```

### Run the container

```sh
docker run -d -p 3443:3443 --name acunetix acunetix_13
```

## Local setup guide

Acunetix 13 Linux Install：
1. Install using `bash acunetix_13.0.200217097_x64.sh`
2. Copy the "wvsc" file to the install directory: "/home/acunetix/.acunetix/v_200217097/scanner/"
3. Copy the "license_info.json" license file to the license directory: "/home/acunetix/.acunetix/data/license/"
4. service acunetix status
5. service acunetix stop
6. service acunetix start
