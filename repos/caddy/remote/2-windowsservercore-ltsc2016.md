## `caddy:2-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:08473cebef31a1a368655af46bdef8b775914f10527be9200df9d398451df182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4169; amd64

### `caddy:2-windowsservercore-ltsc2016` - windows version 10.0.14393.4169; amd64

```console
$ docker pull caddy@sha256:a95daaf163b6206c31bd5a9fefe535e199796f81dcd7eab682df687a2016f3ad
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5826167615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dfb6fe190c1d40eeebb3d48201b9d03df7a5f0c87d3ba6226b1004504e9e287`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 07 Jan 2021 11:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 Jan 2021 13:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jan 2021 23:57:42 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 14 Jan 2021 00:03:41 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 14 Jan 2021 00:05:09 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('afc504cb0a641729ba546c0cadea524a170dcca2a915473aaf032a7c666c7c56ac059752f34b5d50700a692647b9b395b530cd8299ac3650c729adce5daa1ba5')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 14 Jan 2021 00:05:10 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 14 Jan 2021 00:05:12 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 14 Jan 2021 00:05:13 GMT
VOLUME [c:/config]
# Thu, 14 Jan 2021 00:05:14 GMT
VOLUME [c:/data]
# Thu, 14 Jan 2021 00:05:15 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Thu, 14 Jan 2021 00:05:16 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 14 Jan 2021 00:05:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 14 Jan 2021 00:05:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 14 Jan 2021 00:05:19 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 14 Jan 2021 00:05:19 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 14 Jan 2021 00:05:20 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 14 Jan 2021 00:05:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 14 Jan 2021 00:05:21 GMT
EXPOSE 80
# Thu, 14 Jan 2021 00:05:22 GMT
EXPOSE 443
# Thu, 14 Jan 2021 00:05:23 GMT
EXPOSE 2019
# Thu, 14 Jan 2021 00:06:10 GMT
RUN caddy version
# Thu, 14 Jan 2021 00:06:11 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bd091f41e44cabc11504b7e130c74a7ef654f58840ba102e3507c4fdf2bae994`  
		Size: 1.7 GB (1723908142 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:51e9c5c519fdcd28aa0ed033a3cc16cf37dd76bea8ec06b2dc4a344415bdd224`  
		Last Modified: Wed, 13 Jan 2021 15:10:27 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ab8111d5c5970d277cc720aa8b29d9a8929b6c0ed278f6d3baf0abf3a5c283`  
		Last Modified: Thu, 14 Jan 2021 00:10:25 GMT  
		Size: 10.2 MB (10161407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbbd4a3517a3e193644d8a9898ba2f50513b1beaf3f5e9689251145863a7223`  
		Last Modified: Thu, 14 Jan 2021 00:12:08 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4126f87d2fce56ced828634969035d1897145822d09845feac67f7875601d6`  
		Last Modified: Thu, 14 Jan 2021 00:12:34 GMT  
		Size: 21.8 MB (21838247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef97a5d3119fca76ed34dac487bec7550646029f68f221d679350fcbba50bae`  
		Last Modified: Thu, 14 Jan 2021 00:12:08 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598d4c368c88dc8321865eca56ac8d45771c31e8adc870f4be14376ba4485807`  
		Last Modified: Thu, 14 Jan 2021 00:12:08 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c28a06a7d063d3d3cb6439a248c19aa743448cd057b6e1955a673f8130e1ee`  
		Last Modified: Thu, 14 Jan 2021 00:12:05 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0054b245b8193dbbd656c99ccdb315c0f9b685eff6edbb6ed07eb90aa6b113a3`  
		Last Modified: Thu, 14 Jan 2021 00:12:04 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d0ed80aa1b02523018d619bf17139788621800c16d15ac388bb65b7660d368`  
		Last Modified: Thu, 14 Jan 2021 00:12:05 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52af04661019721e096d89b055d565982b8f0b342c4b1b4a847529f20b209546`  
		Last Modified: Thu, 14 Jan 2021 00:12:04 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b6e926bea3b9f9a8853e4be32181b75be97d5e430e45337fd063f0aee784bf`  
		Last Modified: Thu, 14 Jan 2021 00:12:02 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc5dd85c535f4866f5a00f179dffc5473da3c500ab31326bfd71c2ff1a48c59`  
		Last Modified: Thu, 14 Jan 2021 00:12:01 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5048f14b9e8f2e82ae7a81ef1b42359b98dbf3ed743cb3a5da805393df979cf`  
		Last Modified: Thu, 14 Jan 2021 00:12:01 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334073bfe9b6f1f64b1405c7da17e07bc8d32a586d2a0352f72def2e10a196af`  
		Last Modified: Thu, 14 Jan 2021 00:12:01 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6149e51c45c48dc3d10d8017bb209b066f3567342568725e8816e9cab588b9`  
		Last Modified: Thu, 14 Jan 2021 00:11:59 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743fb1a090761c6a1c8cd2b5846400a8ff0879c50e6df8e6ffcb2647b312fa1a`  
		Last Modified: Thu, 14 Jan 2021 00:11:59 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f8e5f898b74d4c8116bc0ef43023da55b8e9d6ea558c259ac507ab98512e22`  
		Last Modified: Thu, 14 Jan 2021 00:11:57 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf3a01455bd5bb8fe621f0458e773a9d589b1ec97c7531cbe0ba06c459aad58`  
		Last Modified: Thu, 14 Jan 2021 00:11:57 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10548a36a748b3d59e79857d64fa321af0a803d8d98c1ca668ef19cca9df3022`  
		Last Modified: Thu, 14 Jan 2021 00:11:57 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3eaa62b592ca108e8599ec9769a20acb86a8532f82bb8504fb4c311b53968d1`  
		Last Modified: Thu, 14 Jan 2021 00:11:56 GMT  
		Size: 253.5 KB (253489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542abf7478499e56d7b85ec8d24eadb385d11de89ef946d5c0e9d89060c70262`  
		Last Modified: Thu, 14 Jan 2021 00:11:56 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
