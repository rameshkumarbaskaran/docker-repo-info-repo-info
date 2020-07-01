## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:6a5e85d8268fdf2dc72fc43dfb70a4a170c63e7c68f441fb87943a916142a752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull caddy@sha256:77457a1d020bd33050143d17846f94c0caa328868a22620c22792c842fa9847c
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2312351756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90fe8eb1d91b21db1e55c3cb01033e1ef8ac50675b44e322cfd952468ae3fb37`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Tue, 09 Jun 2020 22:33:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jun 2020 18:02:29 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 10 Jun 2020 18:03:15 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 01 Jul 2020 00:15:29 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 01 Jul 2020 00:15:59 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 01 Jul 2020 00:16:01 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 01 Jul 2020 00:16:02 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 01 Jul 2020 00:16:03 GMT
VOLUME [c:/config]
# Wed, 01 Jul 2020 00:16:04 GMT
VOLUME [c:/data]
# Wed, 01 Jul 2020 00:16:04 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 01 Jul 2020 00:16:05 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 Jul 2020 00:16:06 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 Jul 2020 00:16:07 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 Jul 2020 00:16:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 Jul 2020 00:16:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 Jul 2020 00:16:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 Jul 2020 00:16:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 Jul 2020 00:16:11 GMT
EXPOSE 80
# Wed, 01 Jul 2020 00:16:12 GMT
EXPOSE 443
# Wed, 01 Jul 2020 00:16:13 GMT
EXPOSE 2019
# Wed, 01 Jul 2020 00:16:29 GMT
RUN caddy version
# Wed, 01 Jul 2020 00:16:30 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
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
	-	`sha256:6e676deb3766189ea2b008f69205017c9ee31a77f9c7001fb5a07fb2e2d4fbb0`  
		Last Modified: Wed, 10 Jun 2020 18:09:48 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4ba576338ed5242ba3fb838ce5fa930abb61e22fc422ba46b260dbca773cb9`  
		Last Modified: Wed, 10 Jun 2020 18:09:48 GMT  
		Size: 4.8 MB (4772911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc338e95aacf0df61c8d7a8f6829ca9f7adacd3d48f2f08006bf6c260e6f6a1`  
		Last Modified: Wed, 01 Jul 2020 00:19:33 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e83e5ec896196d3a3b38f7d121d59d2b855f0dad39906b250a24b836c94b08c`  
		Last Modified: Wed, 01 Jul 2020 00:19:34 GMT  
		Size: 13.3 MB (13344221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91139d50f5068c10450d400b2a7f95fd20c7cb9dfafef759b664aa0e3994ac9f`  
		Last Modified: Wed, 01 Jul 2020 00:19:31 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c88a225f30963de8211710e04403d1f5a0977c97667a2f73fe89a8fe8ed78aa`  
		Last Modified: Wed, 01 Jul 2020 00:19:31 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd8b4dc035d4502f79bdc5040291ba7700285c35b2575cdbc6a948cbcbe816a`  
		Last Modified: Wed, 01 Jul 2020 00:19:30 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aade01ab5b296bdffd61a3849c5c2feb03618880c5a257ea02496adf0615f26`  
		Last Modified: Wed, 01 Jul 2020 00:19:30 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd47640bcab2ae58a8eb8b6b28b8babd8cd800966e426abef67c9c237fa756d`  
		Last Modified: Wed, 01 Jul 2020 00:19:29 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa16ffeedca2e162258cff0b1d2f84ea8f35088236dd08e957122949042f4b9b`  
		Last Modified: Wed, 01 Jul 2020 00:19:28 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88aa8b5af14fa9a21fdf1d69de1f539fcbd9ce53dd714cafe2a3fb23506af45`  
		Last Modified: Wed, 01 Jul 2020 00:19:28 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5db36198ee72f508e31517e6883f316d91f95958a81dd9bc386f745282b467`  
		Last Modified: Wed, 01 Jul 2020 00:19:28 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3daa6b70ac7530f10ab82868ce40ee01776676e25eb487fcc76c115d6af264`  
		Last Modified: Wed, 01 Jul 2020 00:19:27 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b566a496c2533383f4f0123fc7c110b861b4ee66bfe2399ba5b60dada395f78`  
		Last Modified: Wed, 01 Jul 2020 00:19:26 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b678d312023c6e6bcc37e8fcd954ccbb28b373021cad45f3c2a1bbca7692ff`  
		Last Modified: Wed, 01 Jul 2020 00:19:26 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:853e01c72e5605721fad676ecef92f48af0afc4a9261755036c45cb19294e50d`  
		Last Modified: Wed, 01 Jul 2020 00:19:26 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8965b8925adb333a05f00219d90ae6cf09de041cfaf8595360fae18080655e70`  
		Last Modified: Wed, 01 Jul 2020 00:19:23 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227dbe25decc1868fbf806fee9b1b273af973a1ebbfe49e5d257cc986f4715a5`  
		Last Modified: Wed, 01 Jul 2020 00:19:23 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258739e6b29b47678291ece5458686f3a59043b4d75cecae04bd82fff7b10e00`  
		Last Modified: Wed, 01 Jul 2020 00:19:24 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf80ae83e0f501d308bec53bf5b048310f827038a13774104a0d551766b0c0cf`  
		Last Modified: Wed, 01 Jul 2020 00:19:24 GMT  
		Size: 298.6 KB (298594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d135756e2e12ff222ace60a5ca0c860b1047e6cb58196b7818b51a1f969272c2`  
		Last Modified: Wed, 01 Jul 2020 00:19:24 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
