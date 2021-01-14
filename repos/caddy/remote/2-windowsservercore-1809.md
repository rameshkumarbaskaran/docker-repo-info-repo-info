## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:abecf61dde479eb83f03aadca4ce1c7c981ba8ab6a290667fd76a7dbf1105bc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull caddy@sha256:de839e0815b0a64817e61c71de6127bfc07914bb69f87e8408e643af10877328
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2461830878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40640a52040a4245cca4882fc1e070c53ded8b097c9200d6817927ba384d4407`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 13:13:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jan 2021 23:55:04 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 14 Jan 2021 00:02:29 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 14 Jan 2021 00:02:58 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('afc504cb0a641729ba546c0cadea524a170dcca2a915473aaf032a7c666c7c56ac059752f34b5d50700a692647b9b395b530cd8299ac3650c729adce5daa1ba5')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 14 Jan 2021 00:03:00 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 14 Jan 2021 00:03:01 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 14 Jan 2021 00:03:02 GMT
VOLUME [c:/config]
# Thu, 14 Jan 2021 00:03:03 GMT
VOLUME [c:/data]
# Thu, 14 Jan 2021 00:03:03 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Thu, 14 Jan 2021 00:03:04 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 14 Jan 2021 00:03:05 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 14 Jan 2021 00:03:05 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 14 Jan 2021 00:03:06 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 14 Jan 2021 00:03:07 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 14 Jan 2021 00:03:08 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 14 Jan 2021 00:03:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 14 Jan 2021 00:03:09 GMT
EXPOSE 80
# Thu, 14 Jan 2021 00:03:10 GMT
EXPOSE 443
# Thu, 14 Jan 2021 00:03:10 GMT
EXPOSE 2019
# Thu, 14 Jan 2021 00:03:26 GMT
RUN caddy version
# Thu, 14 Jan 2021 00:03:26 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4dcc9a9b9e680514ef3fdfcc2ce08a3768f9e412703faa137f4a7c8297600052`  
		Size: 717.4 MB (717439216 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e00081a98bb2679c3c5f469e09d475980133a20987f9cae4cf4f7aedf59f9d8f`  
		Last Modified: Wed, 13 Jan 2021 13:17:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e6ce3956b2be5c16af8c4b12fb9eee40a47169a238e2ef8cb910eea6f6a86e`  
		Last Modified: Thu, 14 Jan 2021 00:09:40 GMT  
		Size: 9.4 MB (9370292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ace9d6991a65c9a920c33512761b565801eb9b5db738b41e18b582195bc0437`  
		Last Modified: Thu, 14 Jan 2021 00:11:32 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cac05c73067e06026b63884d2b0ceecc7bfacb99a453af02c6a0868528ac912`  
		Last Modified: Thu, 14 Jan 2021 00:11:35 GMT  
		Size: 16.4 MB (16392257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1b6c4adde3cc3d3e32fe5549d3dea1a2216348b2d97fae69675b6eb7b3f309`  
		Last Modified: Thu, 14 Jan 2021 00:11:31 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e765211ebb418fe8b27582dbaabf0486499eb2ccd591809893c71655a671bfe`  
		Last Modified: Thu, 14 Jan 2021 00:11:31 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:731a2a977bca2f5da7bc83330664f2e41bf76620a188990374b8c3506f6a7779`  
		Last Modified: Thu, 14 Jan 2021 00:11:28 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fac4d340ec37627761b8ae0a5418ae1fbc95f883bf3d2ab94212f6be113ecde`  
		Last Modified: Thu, 14 Jan 2021 00:11:27 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c07d9917863b6ffa78ad654c2658efaef97774e1d238b208b45b430a4327234`  
		Last Modified: Thu, 14 Jan 2021 00:11:27 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7157e44941a360dfe52e95269c91abc19d34c68d59525cfbe38abd16a62a7b38`  
		Last Modified: Thu, 14 Jan 2021 00:11:26 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f687a5918c96313c6f725550d164c3b5c5727c8dab0fb262d32061cbc3531c3`  
		Last Modified: Thu, 14 Jan 2021 00:11:26 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae8eb7df7525322bb70878976063664f7b4cca0d57cf6ad2dd2314e4ec86035a`  
		Last Modified: Thu, 14 Jan 2021 00:11:25 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2412a0df7d8e2af00ae106f91f34fdbe43ff37fbce05f7aad93337f5e43d62`  
		Last Modified: Thu, 14 Jan 2021 00:11:24 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43fda527bf8c7062b86fc263da411b54c3bbf3514327f842c99c344970197998`  
		Last Modified: Thu, 14 Jan 2021 00:11:23 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e813b50511cd7ce703252be8d3acd03a640ccc6d5f77fca0de4817699d9a8f0`  
		Last Modified: Thu, 14 Jan 2021 00:11:23 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97840cd7ebfa98613147c2a4c98663d64ebe1616cc1e746c59403444f443c63b`  
		Last Modified: Thu, 14 Jan 2021 00:11:23 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36419b63a395c8d53fbc2751314f3ae78746df2163d2795cc6601c0e8286e6de`  
		Last Modified: Thu, 14 Jan 2021 00:11:20 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e0d2113b0eaf06dbcb1d47f151b1634149a5279c4e1826257a0440e388c379`  
		Last Modified: Thu, 14 Jan 2021 00:11:20 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e44705418f08c2ea5b58e8958be7b17e1056fdd1cb3e0ac76d169577f83dfd`  
		Last Modified: Thu, 14 Jan 2021 00:11:20 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613471c47f93daf8cf5c203eba41926449d587028540640a60864d2b8070444a`  
		Last Modified: Thu, 14 Jan 2021 00:11:20 GMT  
		Size: 275.7 KB (275718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b85d427824d62b9858e31e20e9eece84c0544d2baafa60c9af3373c5358d6db`  
		Last Modified: Thu, 14 Jan 2021 00:11:19 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
