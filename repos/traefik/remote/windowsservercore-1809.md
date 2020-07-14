## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:30ce49ddff8e974e13c8e48d51a6d5958cbb6f668794ed5f148e0fb8acacd64d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull traefik@sha256:91a5bedffb34552d444e1b2142184b25ad8f007b5ff35938f6c853d9b9f8f654
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2320333200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411b19cd4c1c1822c1d20ad0ac34cb4cfa9b14b6e56800afbeeae50aae283f56`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Tue, 09 Jun 2020 22:33:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jul 2020 02:59:39 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.2.5/traefik_v2.2.5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 14 Jul 2020 02:59:43 GMT
EXPOSE 80
# Tue, 14 Jul 2020 02:59:45 GMT
ENTRYPOINT ["/traefik"]
# Tue, 14 Jul 2020 02:59:45 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f841c6a0c622cd36b5b2688011a224ac3e8e96273758f4a2804f2f3f099f267d`  
		Last Modified: Tue, 09 Jun 2020 23:17:50 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e2f6c5068bce4ace2cd32c4ff2c07a3338b013be1feceb022b8d31426b854e`  
		Last Modified: Tue, 14 Jul 2020 03:00:34 GMT  
		Size: 26.4 MB (26414529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69362c6bdb94ac25bad51f862b64c41905b07ad5f628d55e9c6116a04a76e64e`  
		Last Modified: Tue, 14 Jul 2020 03:00:06 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42dfcd3e790c608a2ee40ce269a28fe848786bd4a67fc25567831ad9ac9b4d16`  
		Last Modified: Tue, 14 Jul 2020 03:00:04 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459647495bba353e160a39cec2f6563459d3c243b3a46ac709ab4ce0fd4a0bb7`  
		Last Modified: Tue, 14 Jul 2020 03:00:04 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
