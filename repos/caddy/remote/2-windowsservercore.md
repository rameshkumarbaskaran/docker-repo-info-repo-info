## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:23526c514f90e81e3b94593ed41182252a81ba946c70cf1d2638381f84849d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.5122; amd64
	-	windows version 10.0.20348.2113; amd64

### `caddy:2-windowsservercore` - windows version 10.0.17763.5122; amd64

```console
$ docker pull caddy@sha256:3d281f8c1d34b38abb3b5ca4ff98d70312daad9b0654a470374d0447a69a3ccf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073448315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e423604e6f05b59d8afa51e2d09a8fc11e1ac3353a126e3ce73b1c2bc65872b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 08 Dec 2023 20:16:24 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 08 Dec 2023 20:16:25 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:17:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 08 Dec 2023 20:17:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 08 Dec 2023 20:17:34 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 08 Dec 2023 20:17:35 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:17:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:17:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:17:37 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:17:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:17:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:17:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:17:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:17:41 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:17:42 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:17:42 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:17:43 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:18:34 GMT
RUN caddy version
# Fri, 08 Dec 2023 20:18:35 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09e9b6b38c0082853f1d6caa4d3536344a04da2aa5b674837aba8781b265e0d`  
		Last Modified: Fri, 08 Dec 2023 20:22:45 GMT  
		Size: 462.7 KB (462693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb778801cf9547a5b9021d3090bd8e4fc05f09e3aed56b6950dcbd044211d3f`  
		Last Modified: Fri, 08 Dec 2023 20:22:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ec815279848293cd980ed43a496bf4d3e8f8035f8d46dd1a3278e02c4558a8`  
		Last Modified: Fri, 08 Dec 2023 20:22:46 GMT  
		Size: 15.3 MB (15274633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9671feff108f8e0d8be270b64952394b3eaf7d16a7e9163cffc500ad3a42bd17`  
		Last Modified: Fri, 08 Dec 2023 20:22:43 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44f97706c45d8ebb4578d93d6c1cb5ecc4625f2f78fa40f25f9e72af014449a`  
		Last Modified: Fri, 08 Dec 2023 20:22:42 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7b5732d0f0e4f61cac2e09f77054657b1bfc21c56b5b4b842e96ee7de3d45d`  
		Last Modified: Fri, 08 Dec 2023 20:22:42 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348bbb9a26a300473cbb347ce3e405736e7a71ef7d2e67068452760fe4a1a67e`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4dc80dd8b7091a5cb553a95c06fa14380bf94a6f80467e3d7a36cb649fce8c`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6e2ab9cd2c6c903f643bcab22655dc93ec72fcc2f748a47375e2209580eed8`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a498a93a315d79030214cb59d847ede547dfc1159616120a3b48f2b1585bccfc`  
		Last Modified: Fri, 08 Dec 2023 20:22:40 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6a7d0f8e26a8dd06b83bb38bfecf51f24ec1456947f459528e71b2544d13f5`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0da3c95480c1f76c862487e0683bed75c660c5cce3e3864677b8c956228e64`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1712e0793bc7067adabbb602cf9eaf0e6ab60f33be0b2b10282325884270ab07`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26aa77bbc553e8bf9318552da7ffe35258b387e04151dd211a006f50cb57a6`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e384f6873d9619640183b8c67671c94c80eb3725ac52c312de84b314b2cd4c53`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7ecef2ca51e4738a30164e40d773f9bfcc9a55bda13a00745349db1618fbf0`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29866626f3b37691b2e593b7ad8a6d3f6e916d9ca428c22e1b3834e568c605c9`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dff7ab50f452876c91da33fe48a0e1409de6cbb0ffca4e1aefa68caa5722d01`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 256.7 KB (256705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55865895b10a6247b60406c70eaa3584e7904512f0092bd7d9013bd9fe64c740`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.20348.2113; amd64

```console
$ docker pull caddy@sha256:cca2801fca8e41625ec6c3c42ee17cc76b64320f93ec2c37999b29b5f9ff0747
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1902845713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ad0d44150328d8253edf3d339d33f508e3a25395c8fd773d2d2fe5966eb244`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 09 Nov 2023 06:47:20 GMT
RUN Install update 10.0.20348.2113
# Thu, 16 Nov 2023 01:36:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 08 Dec 2023 20:19:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 08 Dec 2023 20:19:10 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:19:33 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 08 Dec 2023 20:19:34 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 08 Dec 2023 20:19:35 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 08 Dec 2023 20:19:36 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:19:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:19:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:19:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:19:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:19:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:19:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:19:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:19:42 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:19:42 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:19:43 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:19:44 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:19:58 GMT
RUN caddy version
# Fri, 08 Dec 2023 20:19:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7989ef2c4cfb06d845746a3c3660481ea84d3f5c8216041855ce528f0ac4015c`  
		Last Modified: Tue, 14 Nov 2023 20:43:13 GMT  
		Size: 498.2 MB (498182566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbeb193d02c2ca7f9a9ea438fbf1bcdb6ea4a6fea626713330fd1ebb514424f`  
		Last Modified: Thu, 16 Nov 2023 02:25:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9e496904b6bbc7ce10b08f4c5c00b922d19bb8ebfca4735ba504c9ca77dd2b`  
		Last Modified: Fri, 08 Dec 2023 20:23:12 GMT  
		Size: 474.4 KB (474429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d370d88e3c2ee411f6f86dd892eba2c381cf5706823fcf82fec94a47d7d3bb4`  
		Last Modified: Fri, 08 Dec 2023 20:23:11 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1861a873425170bdbe2b563cd2b9584401a7be0e3d9a6ceac998eef4eab482ae`  
		Last Modified: Fri, 08 Dec 2023 20:23:13 GMT  
		Size: 15.3 MB (15274241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e17c8887831a9d0a255eb44daaaedffc1bb98b51fc0177786dd130c85034006`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2595203a1e7cbe5c30c3a77633ff7b832c6f07580e688e7c2bc89b5442e72ae`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b5a75922e76c5c96d069952df83b51d1243d2d6955db5b45dd7b63aea2b3a1`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bbe845ab80dc71320eea94c3d56888074ea930dc6fbe934c60e6c801e9cee3`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74052a6ffee1242926db0907e5406b7e5d81e181d3c9c266d381aaf221bf0252`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbd2ebe3b760156655b6475d7ff52b549e20b5115cf815016c902f834bf3f14`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5945b936f7903435999bc26916fd896f5c645c5b70834243317e66b14d7c2d97`  
		Last Modified: Fri, 08 Dec 2023 20:23:07 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4345b37fb7af089771ba8cf5542de3045ebb0f1d247ea038535504b320c4ac2c`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12593e8f188e5024af21891d9f3141bc5b85d9e2e9e2b61d7c2634f9f491b9a4`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3632692d5118ec05512cfb67c4aa09a8dfdfe1e40467dfc5ee8e5d2e9a349b2a`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e694808297bceaf6299316f20be2a78e4d2eef8a2ca455dd79ce544cf0a00e66`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258e53ea4c6d9b42de13f722ade5338a5393993985f05ca5b438982dde948654`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20692d7b4da06a40fca6c59bffc5e13dc0a0ffc429f70ed8701dc1d5d8c087fd`  
		Last Modified: Fri, 08 Dec 2023 20:23:05 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f686dbb1484378b8f73bbbfac32eb04d8f9a6b2b3f4db7d17c1f997941475a7f`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84003630e1340399082b07e0df6cb438545136bc3f0c134d52e8fe9d878e7239`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 292.2 KB (292197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9991bbf8fb125121b7478726325dcb657bfbeb24af279019b7b2f7ac0c404f7`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
