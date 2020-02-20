## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:0259147e1c2948488566cce22add60c4c9d015c0ab83c0cad5326369207ffdb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1040; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.1040; amd64

```console
$ docker pull traefik@sha256:0d8a4d21a3ead1268dda0b75994711ed4a9e1442b7c360fb4b0b72bcb737cbd0
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2254614482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f4d9bbba7707130be947cacf6d7bf25d0c0fa309e0bc57a1c01d2c56a14580`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 17 Feb 2020 06:57:13 GMT
RUN Install update 1809-amd64
# Thu, 20 Feb 2020 01:13:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2020 04:09:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.1.4/traefik_v2.1.4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 20 Feb 2020 04:09:38 GMT
EXPOSE 80
# Thu, 20 Feb 2020 04:09:40 GMT
ENTRYPOINT ["/traefik"]
# Thu, 20 Feb 2020 04:09:41 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b5405b7580792436b60c664b5fa766ea57f5a60c1d9a8c522cf53e99e4813355`  
		Size: 695.8 MB (695818606 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2061e035d6ba931d9f00238104b970d3410f4ef0d9603b4f074c7052858e01e3`  
		Last Modified: Thu, 20 Feb 2020 03:03:21 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c60a73e575d57222e8843fb64304b2ad26e626f1a8e630b96eb634b4084ec2`  
		Last Modified: Thu, 20 Feb 2020 04:12:03 GMT  
		Size: 24.1 MB (24105807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b74827fa03828ff650d42ccbd438a71c76f21f75d808d9a4edc1d49c98f6ce`  
		Last Modified: Thu, 20 Feb 2020 04:11:38 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1325439ba377e72162df98641f409c9d49c72bb29a932bdf9fe3faae9898aa2`  
		Last Modified: Thu, 20 Feb 2020 04:11:38 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c08705395bfeaf239a907f9b9241976a6a7fd77a367b4d3d3523f86a735ca4a`  
		Last Modified: Thu, 20 Feb 2020 04:11:39 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
