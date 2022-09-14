## `caddy:windowsservercore-1809`

```console
$ docker pull caddy@sha256:6798cfdec660cdc04af486a38c35fed1ec2a2042c921a0c7f5e3d6ba16064fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `caddy:windowsservercore-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull caddy@sha256:68b8e20841384d71e01556f75192b2879150eb51a16da31a8814f91608b447a9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2718501062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64988fc12079121f48738a673a4545dd2d620abb6b809e10b863ed06ada99012`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Tue, 13 Sep 2022 18:21:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 17:50:30 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/979e498d6d01e1fe7c22db848a3e3bc65369183f/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/979e498d6d01e1fe7c22db848a3e3bc65369183f/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Sep 2022 17:50:31 GMT
ENV CADDY_VERSION=v2.5.2
# Wed, 14 Sep 2022 17:51:29 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.5.2/caddy_2.5.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b104d364a458f457bab24f12f97470612035f705fceb170ce16b567e18e0429a18a726f6b1bb435f92d28a659aee52c08c0bac3be41b7f23887b8e7307507482')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Sep 2022 17:51:30 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Sep 2022 17:51:31 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Sep 2022 17:51:32 GMT
LABEL org.opencontainers.image.version=v2.5.2
# Wed, 14 Sep 2022 17:51:33 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Sep 2022 17:51:34 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Sep 2022 17:51:34 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Sep 2022 17:51:35 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Sep 2022 17:51:36 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Sep 2022 17:51:37 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Sep 2022 17:51:38 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Sep 2022 17:51:39 GMT
EXPOSE 80
# Wed, 14 Sep 2022 17:51:39 GMT
EXPOSE 443
# Wed, 14 Sep 2022 17:51:40 GMT
EXPOSE 443/udp
# Wed, 14 Sep 2022 17:51:41 GMT
EXPOSE 2019
# Wed, 14 Sep 2022 17:52:26 GMT
RUN caddy version
# Wed, 14 Sep 2022 17:52:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2bc395c8c47e61e593d2e905e0e051d40e7d25e4aeac7dbe08d3ec57acd0e68f`  
		Last Modified: Tue, 13 Sep 2022 18:25:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f13fddd15a606b5ef28b6be67672d520e17bbbb2f337744985785bb337d3139`  
		Last Modified: Wed, 14 Sep 2022 18:03:26 GMT  
		Size: 359.9 KB (359892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8155652b663defecf9a36a00bbb35cffc8d26f98605c7bd84efd2778733433f8`  
		Last Modified: Wed, 14 Sep 2022 18:03:25 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24317cb1604048a42bf4d167a0271f84477cc8b9b010450c06de08a81dffaf23`  
		Last Modified: Wed, 14 Sep 2022 18:03:28 GMT  
		Size: 14.2 MB (14244267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87841ae080889a08ca575df8a844d831db279f3b9a6c08a3f80cb3b9c6b8cb37`  
		Last Modified: Wed, 14 Sep 2022 18:03:25 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40631b6551ce2eb7dbdda30b90d681a7a1e66e30f9886f783fd77c8ab2ab2a27`  
		Last Modified: Wed, 14 Sep 2022 18:03:23 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2e582d84f382d67f39b3a40951fb11f8eaffe8353815bdbac202aad3227fa5`  
		Last Modified: Wed, 14 Sep 2022 18:03:23 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4bccb24dd99d0350ea6dd9f2e430486a9df9f46e8708b4a970422c7375a8ea`  
		Last Modified: Wed, 14 Sep 2022 18:03:23 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf386c800d94c58d5cd5a3faf52d7bc2ffe203469a615f0ea353e3be221958cf`  
		Last Modified: Wed, 14 Sep 2022 18:03:23 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30885592de7a596a11f110a1d96cc7e661a76c6d0962f0c1b49eba9988cfd284`  
		Last Modified: Wed, 14 Sep 2022 18:03:22 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f749991657ab4963c35543026b5154422cca9eff6b5c8e3b19ec9ca88edb732`  
		Last Modified: Wed, 14 Sep 2022 18:03:21 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d4ccbde68b755985fe3c2eff0f4be5c68575ffa6d2d222eef08064d7c0d6cf`  
		Last Modified: Wed, 14 Sep 2022 18:03:21 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1644a827a615cc37326812a99055b92683c419d458003a9414c7c8ac1d2327`  
		Last Modified: Wed, 14 Sep 2022 18:03:20 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62092ca7a80d053e94ab2f87d50975ebfcc9d154c4ab61ecb39f9c4485cbd0e0`  
		Last Modified: Wed, 14 Sep 2022 18:03:20 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613d53462057cc2c2e1a7fa0a550353997cb418b493dd041900821b7f7951bbe`  
		Last Modified: Wed, 14 Sep 2022 18:03:20 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c8fc94e1877116b59771a6e02f8a3322cef8edea81ef7977e026a139b16bc16`  
		Last Modified: Wed, 14 Sep 2022 18:03:18 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e537e5851d4b3bf4b8071eb9e1bdc6b3500463c08f1148f4128c51ae01162e0`  
		Last Modified: Wed, 14 Sep 2022 18:03:18 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e43862b132aed8e369a66dfe6448b68dd33ee5b1d62e51700c937b528d3da893`  
		Last Modified: Wed, 14 Sep 2022 18:03:18 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36122730106fb407aea9118d34cac50cdd3d7c0d972a3c6ac23de3d9f493b9d3`  
		Last Modified: Wed, 14 Sep 2022 18:03:18 GMT  
		Size: 308.3 KB (308335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf8ff4a947658e4f3721edb31be314108fdc2b8be36ae4e2c62dbda9b6529e1`  
		Last Modified: Wed, 14 Sep 2022 18:03:18 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
