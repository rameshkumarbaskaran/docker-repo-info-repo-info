## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:6bea7b35517a171929f356010eb1b9203f6e2425b23bf60eac0416f9ddb84833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64
	-	windows version 10.0.14393.3750; amd64

### `caddy:2-windowsservercore` - windows version 10.0.17763.1282; amd64

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

### `caddy:2-windowsservercore` - windows version 10.0.14393.3750; amd64

```console
$ docker pull caddy@sha256:35faf7e24fb90b61a662f6dc0bb5907b51962e6f9db230ff97a9fffdf519d84f
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5758041528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64c204aa0e66f6a68b3028da90168170b188478eec673c56f7a97bf35ad6e58a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 09 Jun 2020 22:36:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jun 2020 18:04:40 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 10 Jun 2020 18:06:14 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 01 Jul 2020 00:16:38 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 01 Jul 2020 00:17:56 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 01 Jul 2020 00:17:58 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 01 Jul 2020 00:18:00 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 01 Jul 2020 00:18:01 GMT
VOLUME [c:/config]
# Wed, 01 Jul 2020 00:18:02 GMT
VOLUME [c:/data]
# Wed, 01 Jul 2020 00:18:03 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 01 Jul 2020 00:18:04 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 Jul 2020 00:18:05 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 Jul 2020 00:18:05 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 Jul 2020 00:18:06 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 Jul 2020 00:18:07 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 Jul 2020 00:18:08 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 Jul 2020 00:18:09 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 Jul 2020 00:18:10 GMT
EXPOSE 80
# Wed, 01 Jul 2020 00:18:11 GMT
EXPOSE 443
# Wed, 01 Jul 2020 00:18:11 GMT
EXPOSE 2019
# Wed, 01 Jul 2020 00:18:53 GMT
RUN caddy version
# Wed, 01 Jul 2020 00:18:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c938241e0507e1ada5f864325483d86fd08533a5a31e7cb6ec1357db9891b245`  
		Last Modified: Tue, 09 Jun 2020 23:18:33 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22985925139cd6a6e83b6eb5286a8a6e1053a5c6ddd9762f34deea2aa6bcaacc`  
		Last Modified: Wed, 10 Jun 2020 18:10:17 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43c028d6768e901bc64b3edb7e2e5f72050d3ed78ea4e7337fe85725d250c15`  
		Last Modified: Wed, 10 Jun 2020 18:10:17 GMT  
		Size: 5.4 MB (5404509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70815a4e602dcb92adf9e14c510bcf6daa720fb66605edb0b27add0b89bff54f`  
		Last Modified: Wed, 01 Jul 2020 00:19:57 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f44ce30c89d63dc99d1968700a55b80f0d99aad65ba89f4ee3ade2d381c3f4`  
		Last Modified: Wed, 01 Jul 2020 00:20:01 GMT  
		Size: 18.4 MB (18377062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17cf10e58e9a122e35be1735717c61c61cd1deadb0773235286ae62223a2e315`  
		Last Modified: Wed, 01 Jul 2020 00:19:56 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6161a0fcceb4a26debf861062c6829b28f136d137f849005c69597c42417b3e`  
		Last Modified: Wed, 01 Jul 2020 00:19:56 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb7f8a27aae00f64c6aa3145e6c337b93a385cc4b870f3b720a29b031a64914`  
		Last Modified: Wed, 01 Jul 2020 00:19:54 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b36518163a26c3002588a267ddfc7160e6ab70b5379b5c313db0810d393f00`  
		Last Modified: Wed, 01 Jul 2020 00:19:54 GMT  
		Size: 1.2 KB (1203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b567a1e63379dfda7bae18e6795b77debd7fb5ab62d5ae2d10b79096becb381`  
		Last Modified: Wed, 01 Jul 2020 00:19:54 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75eec6a21fc9b9a5f4c2c477a303711c5c1c32af96e7964d34093c46e2fdfdb2`  
		Last Modified: Wed, 01 Jul 2020 00:19:54 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8b46643e395de1cd6d34af71ff25ceec8235661fd565ad75f778234e8dcfc5`  
		Last Modified: Wed, 01 Jul 2020 00:19:53 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a0e022176d77fe5b17cc2164652b8ba67585aad68b9b9fda7279e69c307699`  
		Last Modified: Wed, 01 Jul 2020 00:19:52 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27bb3fd173781cf4aa8c000573dd19d67560e40b8d3fbeda1e8dccb421f579c`  
		Last Modified: Wed, 01 Jul 2020 00:19:52 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904999bb09b75919ca03f67a70d2a35158b27d69df0eccf5fea477d5bf4f6d5f`  
		Last Modified: Wed, 01 Jul 2020 00:19:51 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d50033284bbf2d266f56a8f2b89a8b0a9cf5e9551b2cfb7e9310a7865c2c8ad`  
		Last Modified: Wed, 01 Jul 2020 00:19:51 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228fda428e977e94a9217a57b29b5b0bc3390f1672704f981ea97327281f0a5f`  
		Last Modified: Wed, 01 Jul 2020 00:19:51 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95dbe0b17ebfd63d3ff3126bdfb2b2563c09abac1e153667fd506fe16ff48cdc`  
		Last Modified: Wed, 01 Jul 2020 00:19:49 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3caae4654ac48585a8fb3498155272a4fc11834530bd756163532c7869035a`  
		Last Modified: Wed, 01 Jul 2020 00:19:49 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0340322dd9ac8223b69a845ecf656fe382bb1764b559a6817748c6505040459a`  
		Last Modified: Wed, 01 Jul 2020 00:19:49 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541de31fd9fbe59c99012142d3e1fbc01d00baeceb1cf4025c1bad60ce742d18`  
		Last Modified: Wed, 01 Jul 2020 00:19:49 GMT  
		Size: 240.4 KB (240414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ae3d73e72ea4c0be00a0fc1a9239f8a48bbaa6838d98adfdbbfe38fda4e1ad`  
		Last Modified: Wed, 01 Jul 2020 00:19:49 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
