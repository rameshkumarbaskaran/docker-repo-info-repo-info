## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:15a41b12319e95bdb54be3d4e5112858227031449cdba3a7f77a3e16a8508c32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2237; amd64
	-	windows version 10.0.14393.4704; amd64

### `caddy:windowsservercore` - windows version 10.0.17763.2237; amd64

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

### `caddy:windowsservercore` - windows version 10.0.14393.4704; amd64

```console
$ docker pull caddy@sha256:38aee92cf27cd4f3496d83ba179be13a90995544f17aacd76d471261a0075eb8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6285624339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea2813b55348626a62596bdeee79661e3bf6b8df64e14bd8f159d47516b9f403`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 06 Oct 2021 21:16:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 Oct 2021 12:40:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Oct 2021 01:18:35 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 09 Nov 2021 01:17:56 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 01:19:05 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 09 Nov 2021 01:19:06 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 09 Nov 2021 01:19:07 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 09 Nov 2021 01:19:08 GMT
VOLUME [c:/config]
# Tue, 09 Nov 2021 01:19:09 GMT
VOLUME [c:/data]
# Tue, 09 Nov 2021 01:19:10 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 01:19:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 01:19:12 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 01:19:13 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 01:19:14 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 01:19:15 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 01:19:16 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 01:19:17 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 01:19:18 GMT
EXPOSE 80
# Tue, 09 Nov 2021 01:19:19 GMT
EXPOSE 443
# Tue, 09 Nov 2021 01:19:20 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 01:19:57 GMT
RUN caddy version
# Tue, 09 Nov 2021 01:19:58 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0c776a8e8e3c02d360995b7fa26a3fd7c0928965795fac57b69ff07418ab07bf`  
		Size: 2.2 GB (2202780626 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6974b1bd85ba3f9ce16d86231eced43f720fed9c13411d37584dfe7193bcde60`  
		Last Modified: Wed, 13 Oct 2021 13:27:57 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d982cd3ea4e0f39b0a59afe2410f4ac8f8ca8c9501681376105ac0756077aaf`  
		Last Modified: Thu, 14 Oct 2021 01:25:13 GMT  
		Size: 364.7 KB (364730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebe8afda08514b059739525bb89d4d104d384aa5a11acb4fc12a7a0f26e56e94`  
		Last Modified: Tue, 09 Nov 2021 01:23:24 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5bbc2af7df2033db063435886ddfe73a411f172e025f55110b2427cec59a92f`  
		Last Modified: Tue, 09 Nov 2021 01:23:27 GMT  
		Size: 12.2 MB (12161888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92230f930317607a7e39e8d26435e0b43f3b2ba5b27d0b8e99b8ddf29e5b0af7`  
		Last Modified: Tue, 09 Nov 2021 01:23:24 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0aa3cbf342d20500bf0caaf4de6064a727523c5a8e77bd6c1b5b8e9f3f84da2`  
		Last Modified: Tue, 09 Nov 2021 01:23:24 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44ae176788884d49d3edf5714107691e2d69bfca6efbb9a08859fccd7c5bc784`  
		Last Modified: Tue, 09 Nov 2021 01:23:22 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff2d2f06e59c90a84a6c3afa72aa4af9790fb3be255084569fc33060bd44040`  
		Last Modified: Tue, 09 Nov 2021 01:23:22 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac8a993a805d3557f25c1d79cf339c52bb528bb5934293718762d1c39632aa4`  
		Last Modified: Tue, 09 Nov 2021 01:23:22 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c3bde9a0210928003c08a80e14c0542b3bf66476af07972a0e2eb0d0a824ee5`  
		Last Modified: Tue, 09 Nov 2021 01:23:22 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efde865fba231dd97660101c9c7a855e2df071928e7556e84add29a26e82b0a9`  
		Last Modified: Tue, 09 Nov 2021 01:23:22 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd1fabe5446cf4b4887b243405c121d1bd29498e9b58ac6e2af9d3ca27fa7d8b`  
		Last Modified: Tue, 09 Nov 2021 01:23:20 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:899d68d53713666329056eba794de7149d4ae4d7dd339cc65fec118ba99ebe49`  
		Last Modified: Tue, 09 Nov 2021 01:23:20 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4904ef178f3e6395f40c2f98d54206b084feee028689e3b91e439f1446c6af05`  
		Last Modified: Tue, 09 Nov 2021 01:23:19 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e83884efb5ada3d1ee15d97c6671988224182d1d0b7fdf1c4d2b729998e9d40e`  
		Last Modified: Tue, 09 Nov 2021 01:23:19 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f925c57a812115f0467c8c9d57e51f75666bb0e16e3763444ca9fd03dd6c9f`  
		Last Modified: Tue, 09 Nov 2021 01:23:19 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42ba224fd565e045e902c47ac6aea13622730316fa24e52c26c6797a8346b29`  
		Last Modified: Tue, 09 Nov 2021 01:23:17 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35d1a370c39f8ce063c2815feea9a5eb92af025c33cacab822e25de97b1869c`  
		Last Modified: Tue, 09 Nov 2021 01:23:17 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac69719d07e774436894baa1c5e65c98c9d770032092cf0068840ceb37a8666`  
		Last Modified: Tue, 09 Nov 2021 01:23:17 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d320beb2939a65b4fcfee9929e70f0c393afcabea99a779c84954f738a4302`  
		Last Modified: Tue, 09 Nov 2021 01:23:17 GMT  
		Size: 305.9 KB (305931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e23e9c9accd2bfb6185843136d9b3448c5f5fd4d82e3692f96d928566b77592`  
		Last Modified: Tue, 09 Nov 2021 01:23:17 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
