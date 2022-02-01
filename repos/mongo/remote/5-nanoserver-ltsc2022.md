## `mongo:5-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:f955a3e161ce24b4e76da73b1debd1d337bbc34b01326d73dcb83c86c38b5cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.473; amd64

### `mongo:5-nanoserver-ltsc2022` - windows version 10.0.20348.473; amd64

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
