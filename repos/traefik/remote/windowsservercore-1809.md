## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:56c556d77094bf8a496466fe0ec56ff819930ef465d252dd4887a68581bbf65b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1757; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.1757; amd64

```console
$ docker pull traefik@sha256:dccfae71811f7f07f664e6e60cb651ecdb00d1cb0754b7d7e920eaa494718111
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2474658912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678cdb23a8e3694a9f36cc33974dfcf56d9d68726c676dfdb05fcdc0ceca6dd1`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 06 Feb 2021 05:03:14 GMT
RUN Install update 1809-amd64
# Wed, 10 Feb 2021 13:14:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 18 Feb 2021 19:16:05 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.4.5/traefik_v2.4.5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 18 Feb 2021 19:16:07 GMT
EXPOSE 80
# Thu, 18 Feb 2021 19:16:08 GMT
ENTRYPOINT ["/traefik"]
# Thu, 18 Feb 2021 19:16:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:db4edcf0861ff3fdc41851a5a218965ecb2ab6cf4ec9448fb80cc4b6792fd46c`  
		Size: 720.9 MB (720933935 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:433d24156d44dde3b3c6c0094ba5824a315286ae537c68f272e464fc426510f6`  
		Last Modified: Wed, 10 Feb 2021 13:40:44 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f6a9a190cd76e08337bdbcb4151e2209a8eb869350410b69abc00520909b49`  
		Last Modified: Thu, 18 Feb 2021 19:16:58 GMT  
		Size: 35.4 MB (35386459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3842dc9cd16d601823a69250f2125c318e7c55f63a7a247d9359f2ffe84a662`  
		Last Modified: Thu, 18 Feb 2021 19:16:50 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba0a130b3c525c6d7cdd4a3661e9ceaa11bb9287f0823bf8220028c6878d78d`  
		Last Modified: Thu, 18 Feb 2021 19:16:49 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9924892ced120ed01c98e4f2489c0d44fa78f5258239f969a9910a81ef17c234`  
		Last Modified: Thu, 18 Feb 2021 19:16:49 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
