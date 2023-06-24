## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:834d39cbaf2d19dc96612b0f6f966b134e7dfffd63468c53ffa0fc843c063ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.4499; amd64

```console
$ docker pull caddy@sha256:f0b23c79f4f0636e49dc6099b31a9575d50625b72c6e6a8ccdd47bbc00291688
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1665953086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29de5c78eeb566d45bdbaeca1d1d4c4a5505acfd32f1f0e6bd0bb9115d95b53d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:47:17 GMT
RUN Apply image 10.0.17763.4499
# Sat, 24 Jun 2023 00:40:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:21:18 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Sat, 24 Jun 2023 03:21:19 GMT
ENV CADDY_VERSION=v2.6.4
# Sat, 24 Jun 2023 03:21:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e2a9a708786cc498cf4b12c0aaf2c9731cc89ccef71a7da4c2be60e18d730675890c2d6bbddd3d8347e5f89f348d5e74fbfbf339ed1ec280f5caf69c3849a243')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Sat, 24 Jun 2023 03:21:53 GMT
ENV XDG_CONFIG_HOME=c:/config
# Sat, 24 Jun 2023 03:21:53 GMT
ENV XDG_DATA_HOME=c:/data
# Sat, 24 Jun 2023 03:21:54 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Sat, 24 Jun 2023 03:21:55 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 24 Jun 2023 03:21:56 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 24 Jun 2023 03:21:57 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 24 Jun 2023 03:21:57 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 24 Jun 2023 03:21:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 24 Jun 2023 03:21:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 24 Jun 2023 03:22:00 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 24 Jun 2023 03:22:01 GMT
EXPOSE 80
# Sat, 24 Jun 2023 03:22:01 GMT
EXPOSE 443
# Sat, 24 Jun 2023 03:22:02 GMT
EXPOSE 443/udp
# Sat, 24 Jun 2023 03:22:03 GMT
EXPOSE 2019
# Sat, 24 Jun 2023 03:22:21 GMT
RUN caddy version
# Sat, 24 Jun 2023 03:22:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b1471cc22404d036d95728a9c37c1e3f025a1f0a331072c8613e38cf8f7ff1ed`  
		Last Modified: Fri, 23 Jun 2023 02:36:08 GMT  
		Size: 1.7 GB (1650736778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58717a727cd3a756d7c1180dfb74e95d49735ed12628bd25d2058bc90fa96991`  
		Last Modified: Sat, 24 Jun 2023 01:20:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d526a2e3e0b935854dde55fe6a4b8e59d1bd5cb5e1d95f64fefa72527096cd12`  
		Last Modified: Sat, 24 Jun 2023 03:29:57 GMT  
		Size: 318.4 KB (318440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726e17ce822b395c99da84e071563e73b1c26d5ee8f778d61cfb92576a125c01`  
		Last Modified: Sat, 24 Jun 2023 03:29:57 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21662822c4ac36fa855d3f00994c23b6f1ef959af9001d509d5ddfd85e809ad7`  
		Last Modified: Sat, 24 Jun 2023 03:30:00 GMT  
		Size: 14.6 MB (14605794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c982fd3f9deb7642dc22c1b47087f4b6d9a2ac65cf67cf0737ebbcd441c0328`  
		Last Modified: Sat, 24 Jun 2023 03:29:56 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70eee5bf56221462513cfe49cc444aa981dd9988f66075c80d453841e7a63bf0`  
		Last Modified: Sat, 24 Jun 2023 03:29:55 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694da407532196c14e780047c28b25bbf104d3a165aa61f8668c397198a92ee5`  
		Last Modified: Sat, 24 Jun 2023 03:29:55 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c7c2f97f4c62e6562a6e34048622854c3602c4b0e491c2ecac5e1efb07ae49`  
		Last Modified: Sat, 24 Jun 2023 03:29:55 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e667082cb24584ce0403c8a3434dc5a9208287b744579f66b57ebe88f6750489`  
		Last Modified: Sat, 24 Jun 2023 03:29:55 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6cb80d9d347fc421afdb4b15a39f89d7131e105545dc4a1747b35900f918939`  
		Last Modified: Sat, 24 Jun 2023 03:29:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b0d65540af4eee45de5fd1ce90eaf5e129df4e30dfab08d5e1790b286028af`  
		Last Modified: Sat, 24 Jun 2023 03:29:53 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2e066ee0150dc89c60d1eb9d1414087aa6efad3a689eac13c1a98af5b2a2c9`  
		Last Modified: Sat, 24 Jun 2023 03:29:53 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f39f8248d0fcf98cb261c4973e7b8fff7baf4ed06466fb10d41ac1b1c649172`  
		Last Modified: Sat, 24 Jun 2023 03:29:53 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c5c4ed3fda9389f17148e60e946be2f5767721cd4185ecce7bf2d9384805cb`  
		Last Modified: Sat, 24 Jun 2023 03:29:53 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983e7785318ed4fac98ec47e505736926dde75c4e9f1afe222c5b43022cdb326`  
		Last Modified: Sat, 24 Jun 2023 03:29:52 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd82344255b7055240b416082750ccfe136ffe864d8f74d1a3ca0fb84d8db107`  
		Last Modified: Sat, 24 Jun 2023 03:29:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f07edb7f90243b4ebd980d6f6aa95caac695188be0ac4851cfa29382d58a8da`  
		Last Modified: Sat, 24 Jun 2023 03:29:51 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a2e3aca706de9330e4a2f58f58cc885a8001272711310cb7782fb267ddb4e1b`  
		Last Modified: Sat, 24 Jun 2023 03:29:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da0cf7e3dd77608c18328936eff1c28d37bf0b97fa4836baa39e26f4a30772cb`  
		Last Modified: Sat, 24 Jun 2023 03:29:51 GMT  
		Size: 270.0 KB (269970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b4a0185eb3e9d972b1c8eb98ea694267c493b96468a884e4de45932880b13e`  
		Last Modified: Sat, 24 Jun 2023 03:29:51 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
