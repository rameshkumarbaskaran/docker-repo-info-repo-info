## `caddy:windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:3f88aabc0b2d55a45411b9751f8115fabcb2f3287a98bbaee17a9ff00a314b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3808; amd64

### `caddy:windowsservercore-ltsc2016` - windows version 10.0.14393.3808; amd64

```console
$ docker pull caddy@sha256:9309bb10d0c669007e988170de8a41389199e441213ccb1008719045ebd871ca
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5770427260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec3aa4c7384a5a7cba1c487c1d02e49f9614a0b77af72f9b61c3552842418ad`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Jul 2020 18:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jul 2020 21:00:41 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 15 Jul 2020 21:02:16 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Jul 2020 21:02:17 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 15 Jul 2020 21:03:59 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Jul 2020 21:04:01 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Jul 2020 21:04:02 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Jul 2020 21:04:03 GMT
VOLUME [c:/config]
# Wed, 15 Jul 2020 21:04:04 GMT
VOLUME [c:/data]
# Wed, 15 Jul 2020 21:04:05 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 15 Jul 2020 21:04:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Jul 2020 21:04:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Jul 2020 21:04:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Jul 2020 21:04:09 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Jul 2020 21:04:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Jul 2020 21:04:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Jul 2020 21:04:11 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Jul 2020 21:04:12 GMT
EXPOSE 80
# Wed, 15 Jul 2020 21:04:13 GMT
EXPOSE 443
# Wed, 15 Jul 2020 21:04:14 GMT
EXPOSE 2019
# Wed, 15 Jul 2020 21:05:07 GMT
RUN caddy version
# Wed, 15 Jul 2020 21:05:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9a64f8d0454dba1fb133615caae6ab4d76b85b8be54102ee2ce5f7fd034edbff`  
		Last Modified: Tue, 14 Jul 2020 19:42:07 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7973eea74d5e1ffbee09352aaa6979a2d5e7f3c706dadaf44f4735b71528e922`  
		Last Modified: Wed, 15 Jul 2020 21:06:19 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b6f61001103e65bd146a657498ccfcfef4b3e655e152634f152f700fdabc17`  
		Last Modified: Wed, 15 Jul 2020 21:06:20 GMT  
		Size: 9.9 MB (9860229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed887351cc64ca113fa7bf7f7a2aebb4211ddce4e231d0788faf2901d728f73`  
		Last Modified: Wed, 15 Jul 2020 21:06:15 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77c505dc3cb2fb08c1762e86cec96351555b1abe4c696257d5bd6bf8ad8d63fa`  
		Last Modified: Wed, 15 Jul 2020 21:06:22 GMT  
		Size: 22.8 MB (22833934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495a4007452fe320b5bcd5eaff6043e3e7109e555aaef70fe48415a0f0421da3`  
		Last Modified: Wed, 15 Jul 2020 21:06:14 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61ef463accb9b7440da0074a6a76406c2609cae40dfb7e2c5a86f2b6f2c710a`  
		Last Modified: Wed, 15 Jul 2020 21:06:14 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba58a4c1dc0267ebcdd7a394efe0579230d6e1978d432f0a26655f9cd08f55c`  
		Last Modified: Wed, 15 Jul 2020 21:06:13 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6251cd849c18772101da9a5f71426f8339bef0c24e203b9bd825db4cae16d12`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a002e23d61ce3428e1fa084e6ffd1b9be668908d71de91e1faaa786c8e6fba78`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cb19c35b49270f4d2aeaaf824025a60155e944919f9f004388a17cfff48484`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ddc2a191bf998f6e818f0d60659d7d3c484ad20278f9833a5907dffde86892`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a9d6373b17b66ef4c716a0c96d055a68fc978ff714db11cb09c3308884a4a1`  
		Last Modified: Wed, 15 Jul 2020 21:06:11 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5095f9f74e5647a4a6b1b98cc35e2c569db0850b6aec715fb3baab1623ee5a8`  
		Last Modified: Wed, 15 Jul 2020 21:06:10 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c897ee4b18292062520147945a013cfa6c8a0d3797a4d2524e3534beaefd575c`  
		Last Modified: Wed, 15 Jul 2020 21:06:10 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8794fd0e5e655ec2d89a9d9d1f47d5f2caef36c2ec2a6cc991b8f7c67cec6a41`  
		Last Modified: Wed, 15 Jul 2020 21:06:09 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2493d876886903285caa29fb7b4832d31e2151d3a67bcda7826d46481df75760`  
		Last Modified: Wed, 15 Jul 2020 21:06:09 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf378561c7f8518ef0225407bd8313de0cca4163ac035bff87df4c4be9b03b6`  
		Last Modified: Wed, 15 Jul 2020 21:06:07 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67aacd0d404da37e5ea550034d905b05d5213a8d9031693c6872af21dbcd22e5`  
		Last Modified: Wed, 15 Jul 2020 21:06:08 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba977b186a4be8e23c17faa98503f4515730562bfcb2743db73e049f1bf88f19`  
		Last Modified: Wed, 15 Jul 2020 21:06:07 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd44d05094d09ad50f236a4bcf6fed122d75c70ee60acdaea9d1e3047b26e09`  
		Last Modified: Wed, 15 Jul 2020 21:06:08 GMT  
		Size: 250.2 KB (250201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67070899e7f7404e80024c2189b2ccde88bd8732fe4d93ee92b3eebeb90c63e`  
		Last Modified: Wed, 15 Jul 2020 21:06:07 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
