## `caddy:windowsservercore-1809`

```console
$ docker pull caddy@sha256:4de609d607c34cf2ea1522c43daa2a4d087afb50f9e0f73bd81bcc739f6d67b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2237; amd64

### `caddy:windowsservercore-1809` - windows version 10.0.17763.2237; amd64

```console
$ docker pull caddy@sha256:7ffc83541ca93ec8aabc84749474cd6b424ea4797732243993531a22008d3d27
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2699145857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55f954d03526617006da02a56e5f44e041e850095bb28e677019c0cbc63f5e4e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 07 Oct 2021 08:25:51 GMT
RUN Install update 1809-amd64
# Wed, 13 Oct 2021 12:02:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Oct 2021 01:14:55 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 09 Nov 2021 01:15:44 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 01:16:44 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 09 Nov 2021 01:16:45 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 09 Nov 2021 01:16:46 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 09 Nov 2021 01:16:47 GMT
VOLUME [c:/config]
# Tue, 09 Nov 2021 01:16:48 GMT
VOLUME [c:/data]
# Tue, 09 Nov 2021 01:16:49 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 01:16:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 01:16:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 01:16:52 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 01:16:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 01:16:54 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 01:16:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 01:16:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 01:16:56 GMT
EXPOSE 80
# Tue, 09 Nov 2021 01:16:57 GMT
EXPOSE 443
# Tue, 09 Nov 2021 01:16:58 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 01:17:43 GMT
RUN caddy version
# Tue, 09 Nov 2021 01:17:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c0698cf91ebd6bcfb319be6a50421b356d6a3dbbd213d9b2b9dca0f837d7a999`  
		Size: 968.0 MB (967985917 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cc0c4e719f418d49c6a0fb87abd2e0e480c5b6fec1bacc3077cacfad9b4ab3e0`  
		Last Modified: Wed, 13 Oct 2021 12:18:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665e492ba7ee5015a57b1707f6f38dba54fce78ec0702f8835e1706514399f08`  
		Last Modified: Thu, 14 Oct 2021 01:24:39 GMT  
		Size: 359.9 KB (359912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc6a9a7e197217bb5075b8bd5e591437105daff56d5ec7f84ead8b2302818fa`  
		Last Modified: Tue, 09 Nov 2021 01:22:58 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883d75525dd8871c9e5ae144d06f15b71610f2edacf6af249d4b67a95f24c3a3`  
		Last Modified: Tue, 09 Nov 2021 01:23:00 GMT  
		Size: 12.1 MB (12145857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7a33608c2f8b762fa0394a4b43395e1bcaacab7176b5d32104ab0d2b231c53`  
		Last Modified: Tue, 09 Nov 2021 01:22:57 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613d66c44ad62a493692eca498b94856db418fd0b48ae5aaf60e2a0631ae5f5c`  
		Last Modified: Tue, 09 Nov 2021 01:22:57 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e5bb9a8697d8598607189eb72de45178812f178a242c06c3509a3ac787a3088`  
		Last Modified: Tue, 09 Nov 2021 01:22:56 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69251a136c1e503c295bd9c2fe6c29d3d2f3e7f0a4a5663ad500550a313b9e78`  
		Last Modified: Tue, 09 Nov 2021 01:22:56 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788a4df0ecc1b2c6ad02384d2368b476611584ad82741d2b7e7628708306101a`  
		Last Modified: Tue, 09 Nov 2021 01:22:55 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42beab20cc488e7e48dcac0a4747583d774f7e5e25614d045ece8a5e0533e6d8`  
		Last Modified: Tue, 09 Nov 2021 01:22:55 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761b62a4c9d9b5d5428bb7912f1c5e1335c713f91d26e4ed9cdec513c3a0d691`  
		Last Modified: Tue, 09 Nov 2021 01:22:55 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8dbc4d488cd9a4bf00d35b9137bf6a19127b845c1e5e0437e9d1eaff8415c03`  
		Last Modified: Tue, 09 Nov 2021 01:22:53 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3eaf79d6c061a13d7a0e7dacab48fce6c6d98c445ec3221d275c0dd35e87fc`  
		Last Modified: Tue, 09 Nov 2021 01:22:53 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dde1b492d04701d3bad082691a7178c1006e47cb0435330b253e88d85058e6`  
		Last Modified: Tue, 09 Nov 2021 01:22:53 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa377b11990d21c36a8fd56b8bd0128971ebaf4048a73dbe0f11d51568f57279`  
		Last Modified: Tue, 09 Nov 2021 01:22:53 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07465ba285635d7cbb73744c007fc76422125bd0c984f5f92ec3c09df6d6907f`  
		Last Modified: Tue, 09 Nov 2021 01:22:53 GMT  
		Size: 1.5 KB (1456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20bf667cb2833de183f8105c5f19f657b24f6a1e9f41f0cea93d29d70e9fba62`  
		Last Modified: Tue, 09 Nov 2021 01:22:50 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2165d402d6a0958d2f8e6a196f229262fff87eecfa641bb5b54a633cfb610a`  
		Last Modified: Tue, 09 Nov 2021 01:22:51 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ccc3aa5cec9a9e7d16df9163d080042b31157c94d7a4bfcd4f16b9dfee13ae`  
		Last Modified: Tue, 09 Nov 2021 01:22:50 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c445b1ad002ff2d6cd41abb107f0066ce1c948f71acfb120b853a70d0a0e493`  
		Last Modified: Tue, 09 Nov 2021 01:22:51 GMT  
		Size: 295.8 KB (295794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c171a4641731b5ab002e50a34838cd9d0cb928d85aadbf3014ed4c14ca0f597`  
		Last Modified: Tue, 09 Nov 2021 01:22:51 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
