## `caddy:windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:e6e167d7848926db64dc7882fdc689f69405ea5306161d6f5665a74358a7c760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4402; amd64

### `caddy:windowsservercore-ltsc2016` - windows version 10.0.14393.4402; amd64

```console
$ docker pull caddy@sha256:838ae0adcb062de173e145d0796c15d6fb9bd9c336b76162ead2e187d2774083
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5819049733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:639aa79ba7fccaa86390dac55ea0a3b3015deca7f880237c3260907aae4a9e4d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 26 Apr 2021 17:25:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 12 May 2021 12:29:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 May 2021 19:58:49 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 12 May 2021 19:58:50 GMT
ENV CADDY_VERSION=v2.4.0
# Wed, 12 May 2021 20:00:20 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.0/caddy_2.4.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('66c1f96e5ceb44aec53727ec02bbbb52eb58b4a41ac1134c5635693f40aa81cc4fa8e5418fdf712c8aa9c710aa0b19d6f52c0b46c6af54b4c79ca602e599694a')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 12 May 2021 20:00:21 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 12 May 2021 20:00:22 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 12 May 2021 20:00:23 GMT
VOLUME [c:/config]
# Wed, 12 May 2021 20:00:24 GMT
VOLUME [c:/data]
# Wed, 12 May 2021 20:00:26 GMT
LABEL org.opencontainers.image.version=v2.4.0
# Wed, 12 May 2021 20:00:26 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 12 May 2021 20:00:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 12 May 2021 20:00:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 12 May 2021 20:00:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 12 May 2021 20:00:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 12 May 2021 20:00:32 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 12 May 2021 20:00:33 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 12 May 2021 20:00:34 GMT
EXPOSE 80
# Wed, 12 May 2021 20:00:35 GMT
EXPOSE 443
# Wed, 12 May 2021 20:00:36 GMT
EXPOSE 2019
# Wed, 12 May 2021 20:01:29 GMT
RUN caddy version
# Wed, 12 May 2021 20:01:30 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7f532f88613ca85064b055f6b93f8517bd05feba8fdce495a6ad1421573e765e`  
		Size: 1.7 GB (1725791397 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a280ee47051c0dfafc65e567f555ec59b7415288f965b44cf55c9187407d4248`  
		Last Modified: Wed, 12 May 2021 12:55:16 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c26858854e9a4d33437022a0cbf481973fa7709cc09d3402af046620cbbe5c0`  
		Last Modified: Wed, 12 May 2021 20:07:13 GMT  
		Size: 5.7 MB (5714091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e7166d23985a06cbd08c0306a8b0ff5ef83c32e025fca0cb276ab170c27352`  
		Last Modified: Wed, 12 May 2021 20:07:11 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4068f3bcd403fb79c99aa76f07730960238098fe5808e2e7713b9faf6aaab3`  
		Last Modified: Wed, 12 May 2021 20:07:15 GMT  
		Size: 17.3 MB (17254278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c03a57df592a560d888220cba4e7fe2b06f5410505292cb0b1ad2a840a418f`  
		Last Modified: Wed, 12 May 2021 20:07:10 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50169407a95b556efb846552a4c0bebf342bd6b93a2a9c515bfefa6f59a6f566`  
		Last Modified: Wed, 12 May 2021 20:07:10 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0496cbceda3449349c3fad11bb07712b2eb6d339037f14cec194b00dcb559045`  
		Last Modified: Wed, 12 May 2021 20:07:08 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f7ccad3e924ca06af935bb3f105e6ec1c7f5bf4dc794df7343b24e0f91c9b8`  
		Last Modified: Wed, 12 May 2021 20:07:07 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cd579cd39feec54d6644d366d86e5326892e849793b6b57c272cc6e005116a`  
		Last Modified: Wed, 12 May 2021 20:07:07 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573df736fe3c12bfbf4e563cb2bdb7c0a7c36554e4b452b26e2629eb86117899`  
		Last Modified: Wed, 12 May 2021 20:07:07 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ca33eab3fdbb102f21d1e96d4d11a7456de6fd59991369612d137f075bb093`  
		Last Modified: Wed, 12 May 2021 20:07:08 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5801e9252319511ac618dd4ed87de597a11d991e9880cd9d10c3577f03298b`  
		Last Modified: Wed, 12 May 2021 20:07:05 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3450f045350f8e214aeff68c08e2ded42fe0c6f2f85a179eda2727bbba21fd45`  
		Last Modified: Wed, 12 May 2021 20:07:05 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb8b0a02b9bdf3ee28de9083933a9b35766f20fd0151bf70062acdf1e86fc35`  
		Last Modified: Wed, 12 May 2021 20:07:05 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a47d134b87c7f8c844d59735119823a17b27f1f78afda8f29751f8d88671d7`  
		Last Modified: Wed, 12 May 2021 20:07:04 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf10a836e3d3030e65f9608b9a8d425cc4dd5e8882fcdcc21084edb8bf7a3f8`  
		Last Modified: Wed, 12 May 2021 20:07:04 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9bfbeff13e0d1ffcc8229e74b5e564e3b5eeb7a947084db856f2fdc6e105cd`  
		Last Modified: Wed, 12 May 2021 20:07:02 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb78cf7ed64ccf3a6d810a56dad7b0035f86ae42749b6cb3ab6739fa8142617`  
		Last Modified: Wed, 12 May 2021 20:07:02 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f443a34b54dbc5419852d048ce2da89de2fa90a64c375bfb1d784d9613a9247b`  
		Last Modified: Wed, 12 May 2021 20:07:02 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bddd1bba1ef33f62ad9a2112d9781acc3e6af560bd67d42f67d31e28dd17b71`  
		Last Modified: Wed, 12 May 2021 20:07:02 GMT  
		Size: 278.7 KB (278682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c02d5422753f120a445ecf958996865f559ba862d0b43666b212c10005e4ada`  
		Last Modified: Wed, 12 May 2021 20:07:02 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
