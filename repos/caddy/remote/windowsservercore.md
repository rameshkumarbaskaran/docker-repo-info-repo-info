## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:15ab27bc74e57efd5696d07c55c77215737f2126a3311699f0a189a5836a5ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.4499; amd64
	-	windows version 10.0.20348.1787; amd64

### `caddy:windowsservercore` - windows version 10.0.17763.4499; amd64

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

### `caddy:windowsservercore` - windows version 10.0.20348.1787; amd64

```console
$ docker pull caddy@sha256:b350bbfc40c59b095224cf7f10cca6ab7dc5dab3a797a503437dfb8ed682503c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1441546738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f20a5653ba8b670ade246e1a846778e99ec23d6dbb8795ce05e1a68d38d6d4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:51:34 GMT
RUN Apply image 10.0.20348.1787
# Sat, 24 Jun 2023 00:38:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:22:56 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Sat, 24 Jun 2023 03:22:57 GMT
ENV CADDY_VERSION=v2.6.4
# Sat, 24 Jun 2023 03:23:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e2a9a708786cc498cf4b12c0aaf2c9731cc89ccef71a7da4c2be60e18d730675890c2d6bbddd3d8347e5f89f348d5e74fbfbf339ed1ec280f5caf69c3849a243')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Sat, 24 Jun 2023 03:23:25 GMT
ENV XDG_CONFIG_HOME=c:/config
# Sat, 24 Jun 2023 03:23:25 GMT
ENV XDG_DATA_HOME=c:/data
# Sat, 24 Jun 2023 03:23:26 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Sat, 24 Jun 2023 03:23:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 24 Jun 2023 03:23:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 24 Jun 2023 03:23:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 24 Jun 2023 03:23:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 24 Jun 2023 03:23:30 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 24 Jun 2023 03:23:31 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 24 Jun 2023 03:23:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 24 Jun 2023 03:23:33 GMT
EXPOSE 80
# Sat, 24 Jun 2023 03:23:33 GMT
EXPOSE 443
# Sat, 24 Jun 2023 03:23:34 GMT
EXPOSE 443/udp
# Sat, 24 Jun 2023 03:23:35 GMT
EXPOSE 2019
# Sat, 24 Jun 2023 03:23:53 GMT
RUN caddy version
# Sat, 24 Jun 2023 03:23:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:0ce49598e7371c2c318cfa408f639c917d1f43843fb9e0a3316db1ba7fbb14db`  
		Last Modified: Fri, 23 Jun 2023 03:10:46 GMT  
		Size: 1.4 GB (1426298723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27db350c833f7fe0378bc977cd819c1ffe4133ff02ff69f1531f8ddc552c2366`  
		Last Modified: Sat, 24 Jun 2023 01:15:58 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf12af79c3182c5b6918aaa388811d299d489b35aed7471972a49c6aec0b3ebb`  
		Last Modified: Sat, 24 Jun 2023 03:30:25 GMT  
		Size: 337.0 KB (337026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d066a29d338abd6bd893b6e71d0327f5eaf0ad23de35974184182883c2f701f`  
		Last Modified: Sat, 24 Jun 2023 03:30:25 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103f320f81582a324d4a0beb81d14b3446da590077578d39850e4025a04d2eb7`  
		Last Modified: Sat, 24 Jun 2023 03:30:28 GMT  
		Size: 14.6 MB (14612161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866c34d29347629243285755638ef84672d7faf64c3f8cdb30ac94ca31b52067`  
		Last Modified: Sat, 24 Jun 2023 03:30:24 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a7138c16d93ff7b269147b482bc8dbd57f957c918abedbd2114d3c9709d174`  
		Last Modified: Sat, 24 Jun 2023 03:30:23 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b13d9ffcf2e5d66b423e44e44956972d233d59a8837256e673ce1d548e9b4f`  
		Last Modified: Sat, 24 Jun 2023 03:30:23 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5916fac4206fe6cda2da6c4bc54feea7d994b13c8ce1160bbd5c151b4c877923`  
		Last Modified: Sat, 24 Jun 2023 03:30:23 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eed66465011095640fb52273127a14393a46355093b3e2488e8f64e898b4dfc`  
		Last Modified: Sat, 24 Jun 2023 03:30:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2482e28b4cebd20bc002debd5108cc52d08cdbd44bed3b3eeda9cedf4cf2a0e5`  
		Last Modified: Sat, 24 Jun 2023 03:30:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a97688c8a82301751eaad64a35dd55728a0cd84d136ac8e7f03a18de4c0d31`  
		Last Modified: Sat, 24 Jun 2023 03:30:21 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd34e1891d4e9e1d2eeb74a779d01b27a44c45d4e7d2f44ff2093d0b3039cee`  
		Last Modified: Sat, 24 Jun 2023 03:30:20 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8840e12ba12adaf54bda14a2df5658e2fa88c2f52366d9d104a41e18a2c93fcf`  
		Last Modified: Sat, 24 Jun 2023 03:30:20 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9e26b4f9276af535283e46871c0f2675808be9faecaf27bdd9307cda910c44`  
		Last Modified: Sat, 24 Jun 2023 03:30:20 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce0d021df7cece7dd4b8ed6eb4e60fcb1bcd7881e53da2572fbf5016df89547f`  
		Last Modified: Sat, 24 Jun 2023 03:30:20 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58687b7983f1a99555089f91fa9ea76ba8a4e1da1bb653cab59dfb5b65426f92`  
		Last Modified: Sat, 24 Jun 2023 03:30:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671babdf0e141d5a04ee1966a12b046291bd8a8922b07b759779353608aa15ca`  
		Last Modified: Sat, 24 Jun 2023 03:30:18 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4a6d6945103aff95379b7e353eb5cebbb94896862221705f44361ad6161b6d`  
		Last Modified: Sat, 24 Jun 2023 03:30:18 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98321f5a2867aa6c28ab75f191aa503b1b6910d7e788a459a0ce519d95daa72e`  
		Last Modified: Sat, 24 Jun 2023 03:30:19 GMT  
		Size: 276.8 KB (276760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72bff8552454507d04c3227e3c94412acef095745026d4a86b3ae4ef4c094516`  
		Last Modified: Sat, 24 Jun 2023 03:30:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
