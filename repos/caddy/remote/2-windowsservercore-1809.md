## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:67a59b537826dfa0019b55a7c113d5bdd826062754543ae24cccdcf2a558d407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.5122; amd64

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
