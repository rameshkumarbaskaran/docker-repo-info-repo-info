## `caddy:2-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:54f2ce6cefa5785e781847e6fe0fbe6ce716fb6c5bc0de5a49b4cb71cc8f1cda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4350; amd64

### `caddy:2-windowsservercore-ltsc2016` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:b61efb630c29dfd10f857eed823207497fd9c94176f47243f48c641119c663d3
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5818059080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3940d8ab2b2d69a458bd9951c005b3703a5ac35754896cbfd380305f8dfe27`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 May 2021 00:18:49 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 11 May 2021 00:18:50 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 00:20:38 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.0/caddy_2.4.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('66c1f96e5ceb44aec53727ec02bbbb52eb58b4a41ac1134c5635693f40aa81cc4fa8e5418fdf712c8aa9c710aa0b19d6f52c0b46c6af54b4c79ca602e599694a')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 11 May 2021 00:20:39 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 11 May 2021 00:20:40 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 11 May 2021 00:20:42 GMT
VOLUME [c:/config]
# Tue, 11 May 2021 00:20:43 GMT
VOLUME [c:/data]
# Tue, 11 May 2021 00:20:45 GMT
LABEL org.opencontainers.image.version=v2.4.0
# Tue, 11 May 2021 00:20:46 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 11 May 2021 00:20:47 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 11 May 2021 00:20:49 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 11 May 2021 00:20:50 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 11 May 2021 00:20:52 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 11 May 2021 00:20:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 11 May 2021 00:20:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 11 May 2021 00:20:56 GMT
EXPOSE 80
# Tue, 11 May 2021 00:20:58 GMT
EXPOSE 443
# Tue, 11 May 2021 00:20:59 GMT
EXPOSE 2019
# Tue, 11 May 2021 00:22:14 GMT
RUN caddy version
# Tue, 11 May 2021 00:22:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc088e7513f9bd5e2261035715cd5f39aff459f086737be39631a5c03dd0bc9`  
		Last Modified: Tue, 11 May 2021 00:27:00 GMT  
		Size: 5.7 MB (5678806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a94477e69ebd7355bfc6230d3309aa20d4fda7d504dc34bd3b2adae7f5f2b4`  
		Last Modified: Tue, 11 May 2021 00:26:57 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47db416be1d5a7c97652523c359440855c0ef2127ac11cb08595aa068d99d8a5`  
		Last Modified: Tue, 11 May 2021 00:27:03 GMT  
		Size: 17.2 MB (17201492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e500af558c7988b44d7fae2a1a8c1d4498cb130d1de721a37712c33f09147a`  
		Last Modified: Tue, 11 May 2021 00:26:55 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87b8476ce7fba27f66c08050c4a692f8a19ec0c84e9d42537b4b4b8bbb5f56e`  
		Last Modified: Tue, 11 May 2021 00:26:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2d6240d48682965790d983fc3f6b5404aeb7f3f023b517ab83b6e47c20af5c`  
		Last Modified: Tue, 11 May 2021 00:26:53 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:757d21ff239a36a372b7fb98d22d42afd8f3c779c7b342605186d6b2a14925e7`  
		Last Modified: Tue, 11 May 2021 00:26:53 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5e64a8fa017a3b5df9f60508bc7b3f72fe2835f00c086648f26235c9358b14`  
		Last Modified: Tue, 11 May 2021 00:26:52 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac63d4edb89dc9920755d7e04e444610a75ac1268b103c178ebff146f490d73`  
		Last Modified: Tue, 11 May 2021 00:26:52 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27fbb5cca77bbd06aabe9371bf1fe894938b82367a0ef11be873b231a43b64ab`  
		Last Modified: Tue, 11 May 2021 00:26:52 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b0ecb05ae3d1fffc947acf96dea7fe481fd9a745d4fcf79bff9f4b21a28817`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f292068b665f33bccf70f8100aa252145e0f63abb2283fa29d36cadcc6291c52`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1995472761eea00392fa2ce2d1566a7233a89a019e939892cbb0aeb4a8a3a07a`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e8f37215e61d4f10f002f5ad82c4acadf4a56b559cf036050f33242bfe1e35`  
		Last Modified: Tue, 11 May 2021 00:26:49 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e2f6fb7cf636418bada10647c66ee3b92246da967ebb611d58aad6725f5e2b`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8271eda8ea06432cb0dae8fd93e8a85314e86201450cdbebf3efcbba2dbd4331`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3147a4da75f19907c0ee148b5369a63863a2752457cc31b02fe68779d83d56c1`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7013990e537c69857c80a4d6fb386f6d0f04e5a0a5ee5b12ed57c0e458fc8e`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b661b1f2a589a6717a5599a78cb0f3ef950c1a36bd411039dfd39afb20e901b`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 269.3 KB (269349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882e686f1164cdcf35434a7d997c0c9ff058302aaade06ace7c5f8a2e4a718aa`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
