## `traefik:chevrotin-windowsservercore-1809`

```console
$ docker pull traefik@sha256:54f271eb681909b178bde83e99affef920da4fc48082a0c851f94ea5ebded53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `traefik:chevrotin-windowsservercore-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull traefik@sha256:da123e933c848745674445ae56233da3b2e4bb7edf681aa9abadf2eae09c26c4
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2320336869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:930e014ff3305d7f43a9e80cbaeacb0d9233649454001d35bbcba014b551117d`
-	Default Command: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Tue, 09 Jun 2020 22:33:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jul 2020 18:15:14 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.2.2/traefik_v2.2.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 08 Jul 2020 18:15:19 GMT
EXPOSE 80
# Wed, 08 Jul 2020 18:15:20 GMT
CMD ["/traefik"]
# Wed, 08 Jul 2020 18:15:21 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:83b281dcb0aeb7e0424fb993e20f971e6ab29ac1ad4488bc468ead72ac686453`  
		Last Modified: Wed, 08 Jul 2020 18:15:44 GMT  
		Size: 26.4 MB (26418041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f87e7ce9a42e6eb7d8dd5463e51a0c91232df7b5083e9d45d2bb57dc58ac0b9`  
		Last Modified: Wed, 08 Jul 2020 18:15:37 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ffffbcc3290c54724f199c40c4fbf64195fa0ac649fe0abf881f0a4d33a79c0`  
		Last Modified: Wed, 08 Jul 2020 18:15:39 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2c396faa9d420c4d3b6596f94d16942971aa2812be29aa982a5bfe3afb6605`  
		Last Modified: Wed, 08 Jul 2020 18:15:37 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
