## `mongo:nanoserver`

```console
$ docker pull mongo@sha256:139bbb9216db47d92a6381fd8e598a389e11d47d57398b6246ed8c9c5607cb2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.473; amd64
	-	windows version 10.0.17763.2458; amd64

### `mongo:nanoserver` - windows version 10.0.20348.473; amd64

```console
$ docker pull mongo@sha256:85493f2ee8a36184510155028f28009522defb1aefa980ddfdcba0280b487c46
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.1 MB (420129393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79805395bdd86a3b67854e1a02d38b79544ed2c445c71243a0e375e98f72395f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 16 Jan 2022 04:54:46 GMT
RUN Apply image ltsc2022-amd64
# Mon, 24 Jan 2022 23:22:08 GMT
SHELL [cmd /S /C]
# Mon, 24 Jan 2022 23:22:09 GMT
USER ContainerAdministrator
# Mon, 24 Jan 2022 23:22:27 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Mon, 24 Jan 2022 23:22:28 GMT
USER ContainerUser
# Mon, 24 Jan 2022 23:32:34 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Tue, 01 Feb 2022 02:49:24 GMT
ENV MONGO_VERSION=5.0.6
# Tue, 01 Feb 2022 02:50:53 GMT
COPY dir:8054396aef21c43e8eb1e82c0d52daca301fb548900656fb893eece57b5d6e88 in C:\mongodb 
# Tue, 01 Feb 2022 02:51:12 GMT
RUN mongo --version && mongod --version
# Tue, 01 Feb 2022 02:51:13 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 01 Feb 2022 02:51:14 GMT
EXPOSE 27017
# Tue, 01 Feb 2022 02:51:15 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7691725ee3658d154f940d82fd8c3ff07c0dc589a0c9a93df47ed0ede92a76ab`  
		Size: 117.3 MB (117333150 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:af941a54762cda1c0e1e5ddbfe84c7d2f98e61a1f8ac9d819645377dd6d79003`  
		Last Modified: Tue, 25 Jan 2022 00:13:29 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349bf4556263f9c2b81ba296856d4ed419c51b44511c80012a51d9623732722c`  
		Last Modified: Tue, 25 Jan 2022 00:13:29 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5001cb7c0b016929260a25f63cdfc4d975053b0aad01932d3b1210673c87c78b`  
		Last Modified: Tue, 25 Jan 2022 00:13:27 GMT  
		Size: 83.6 KB (83556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24267e91ffbab34bda76a4360c00b630a61176344a205ee2f0a6bc7c06e18ce2`  
		Last Modified: Tue, 25 Jan 2022 00:13:27 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6d4b11520b61fa06a6215d786fb5bdaf12dcf75da502a70e5000b5a3849cf5`  
		Last Modified: Tue, 25 Jan 2022 00:31:41 GMT  
		Size: 263.5 KB (263489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa628d9e782a103353a0b2d65516a67830c990c6f153a8c2bd1b0597e09b7d4`  
		Last Modified: Tue, 01 Feb 2022 03:08:24 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d9b6e760b7e2d43412771b923da978f386243fcecef367510f9b3654624e6a2`  
		Last Modified: Tue, 01 Feb 2022 03:13:36 GMT  
		Size: 302.4 MB (302387811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d65809cf3466f03790a1f627e5f8a89b03de670d9354a3bb61a9302c402bf4`  
		Last Modified: Tue, 01 Feb 2022 03:08:22 GMT  
		Size: 53.3 KB (53299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b937d6f4b7eaa311738dd794b1172f28e7b88912cd89c7b5a1f1862753dcb9d4`  
		Last Modified: Tue, 01 Feb 2022 03:08:22 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5435ec9c7eaf11650c65da42a68979737ae45c84a68fd54d4f5a65983d7476`  
		Last Modified: Tue, 01 Feb 2022 03:08:22 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61357aa93d98d3ebb377f97723ae69c16fbc226135649ba9e8285e05d90f9a8e`  
		Last Modified: Tue, 01 Feb 2022 03:08:22 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:nanoserver` - windows version 10.0.17763.2458; amd64

```console
$ docker pull mongo@sha256:4923880687e416fa0c208868b12df8e6c20365e669dc9dea54c0e1f680fc7165
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.8 MB (405830135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b4a40fdedcce469c91d64331828d7eafedbad8089a17886f630d154cc3194c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 18 Jan 2022 01:20:34 GMT
RUN Apply image 1809-amd64
# Mon, 24 Jan 2022 23:24:23 GMT
SHELL [cmd /S /C]
# Mon, 24 Jan 2022 23:24:23 GMT
USER ContainerAdministrator
# Mon, 24 Jan 2022 23:24:38 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Mon, 24 Jan 2022 23:24:39 GMT
USER ContainerUser
# Mon, 24 Jan 2022 23:33:48 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Tue, 01 Feb 2022 02:51:23 GMT
ENV MONGO_VERSION=5.0.6
# Tue, 01 Feb 2022 02:52:50 GMT
COPY dir:8054396aef21c43e8eb1e82c0d52daca301fb548900656fb893eece57b5d6e88 in C:\mongodb 
# Tue, 01 Feb 2022 02:53:08 GMT
RUN mongo --version && mongod --version
# Tue, 01 Feb 2022 02:53:09 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 01 Feb 2022 02:53:10 GMT
EXPOSE 27017
# Tue, 01 Feb 2022 02:53:11 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:b5c97e1d373f591225559869af7f4f01399c201f89d21f903b1d23c830aa0a3f`  
		Size: 103.0 MB (103046552 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fdb052c4016b3238a417abae6ce3a3c81e145118a4325ab2c01bba6cc9eedc3f`  
		Last Modified: Tue, 25 Jan 2022 00:19:35 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239067809343d5f4e095b39624dfb9ca941d8dded1963d405cf946c066fc3988`  
		Last Modified: Tue, 25 Jan 2022 00:19:34 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e4524972be3a240be3eceb5d9e1b0ba086c38be42fbd75d9a9eda4bbd6d716`  
		Last Modified: Tue, 25 Jan 2022 00:19:33 GMT  
		Size: 75.2 KB (75231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d41aa32bc9bad3c1aaf1a0eeddb9f7aa652e2114e669ad049b3935d95e7bd92`  
		Last Modified: Tue, 25 Jan 2022 00:19:32 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5974c0cdcac59d5825eddb11dde33d91ff93ec2e6d4fec50dec35b2e017fa0b1`  
		Last Modified: Tue, 25 Jan 2022 00:32:40 GMT  
		Size: 263.5 KB (263507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4d8eb443ca2339c59fc8868b1781cd8f869c0309892d1e74708e46f123fbb8`  
		Last Modified: Tue, 01 Feb 2022 03:13:55 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5002d8af3a05227a05ff6f7544a1638b4da86b94b4eb425ac08c88a7bdb404`  
		Last Modified: Tue, 01 Feb 2022 03:14:55 GMT  
		Size: 302.4 MB (302387803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e71bd4b927f125b1e64addfeeeea9bf60633acd21b04bf90b67b73b9902424`  
		Last Modified: Tue, 01 Feb 2022 03:13:53 GMT  
		Size: 48.9 KB (48936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8999930e82ed46b6e84bf99b3c418fe52ea06ee3f480cd6f7e61ccd441aed19b`  
		Last Modified: Tue, 01 Feb 2022 03:13:53 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47886c0d5134c1112286d1ea37f3b0c181ddf7ac6e5e45f959d1ff4bccc2c4d`  
		Last Modified: Tue, 01 Feb 2022 03:13:53 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062de7e8d2e42a3ad81193e371ece255d57df8313bbaaf0f02d9afe3180782d4`  
		Last Modified: Tue, 01 Feb 2022 03:13:53 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
