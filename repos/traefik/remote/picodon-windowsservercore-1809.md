## `traefik:picodon-windowsservercore-1809`

```console
$ docker pull traefik@sha256:03dfa678a159a65ff61a6d77b63a9ccd7143c4c15b8c256615a9bc269802781d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `traefik:picodon-windowsservercore-1809` - windows version 10.0.17763.1339; amd64

```console
$ docker pull traefik@sha256:dada4ba39c53d3dd67ca751b0cab5a84d63149cfdf1574faeac509c86f005c21
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2345769677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b799eb5b2877b05fe6b0cc88737b837b86b29fd0361762d886eb3b75006c89f`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Tue, 14 Jul 2020 18:41:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 Jul 2020 00:15:20 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.3.0-rc3/traefik_v2.3.0-rc3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 29 Jul 2020 00:15:23 GMT
EXPOSE 80
# Wed, 29 Jul 2020 00:15:25 GMT
ENTRYPOINT ["/traefik"]
# Wed, 29 Jul 2020 00:15:27 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:25edfecb5915de420000d722dc47ef9b13bc344a8330c4300e36a4ec8ca73033`  
		Last Modified: Tue, 14 Jul 2020 19:42:57 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45ca99b872c08e3fa56bd4f52b8fd3dbe9321d5acc07c4b8e119a548a783e12`  
		Last Modified: Wed, 29 Jul 2020 00:18:26 GMT  
		Size: 35.6 MB (35572779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac8a0f5b2f7ec43171e450abdd429db668956d38574abcab1088e89d7967a75`  
		Last Modified: Wed, 29 Jul 2020 00:18:18 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfe3736596b07c6ef3c5bfc412ccad185073dc0cb9b02f67e220da5be1bbe02`  
		Last Modified: Wed, 29 Jul 2020 00:18:17 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878da7b62854e2ecba3c47188c49c3d11dc92d8621fb56e9596ffaa884d3ede6`  
		Last Modified: Wed, 29 Jul 2020 00:18:18 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
