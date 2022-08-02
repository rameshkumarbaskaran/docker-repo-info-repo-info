## `golang:nanoserver`

```console
$ docker pull golang@sha256:ddc6ada8134388919cb81b6be6a69332a4983262983f826cccb4e53b07e8ac1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.825; amd64
	-	windows version 10.0.17763.3165; amd64

### `golang:nanoserver` - windows version 10.0.20348.825; amd64

```console
$ docker pull golang@sha256:a191e148689d31ea6065ef3697ef33c9dbb1d8dd68599be923d416dffc2701b7
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275415159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f516a892124ccc5f5a4e867a3962c1b16afa323aca6d00ffbe5cc9a91c8255d0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Mon, 04 Jul 2022 17:25:17 GMT
RUN Apply image 10.0.20348.825
# Tue, 12 Jul 2022 19:39:12 GMT
SHELL [cmd /S /C]
# Tue, 12 Jul 2022 19:39:13 GMT
ENV GOPATH=C:\go
# Tue, 12 Jul 2022 19:39:14 GMT
USER ContainerAdministrator
# Tue, 12 Jul 2022 19:40:04 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 12 Jul 2022 19:40:05 GMT
USER ContainerUser
# Tue, 02 Aug 2022 19:23:25 GMT
ENV GOLANG_VERSION=1.19
# Tue, 02 Aug 2022 19:25:55 GMT
COPY dir:a0f94dd1112f1f27c08d5ea3b68903d61c05f30a36f261cf395a623cb13deea1 in C:\Program Files\Go 
# Tue, 02 Aug 2022 19:26:50 GMT
RUN go version
# Tue, 02 Aug 2022 19:26:51 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:3719b23d309b17276277110a008a58133c9fc92465d2519f2f32c9961c39887d`  
		Size: 118.0 MB (118046090 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:86ff096ef8c908f52d6e505ea5d69c2a28332387f40883a0d9a119dfbf999132`  
		Last Modified: Tue, 12 Jul 2022 20:22:56 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe23cc7fbe1bbfdb4f04675a25cad3444f0af01973afffe750e10ec965c72ee`  
		Last Modified: Tue, 12 Jul 2022 20:22:56 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde0d76670c26bd142f389e17d685a60ea3799ac70159e807e85edbaec29b888`  
		Last Modified: Tue, 12 Jul 2022 20:22:56 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5634d308ec110917e3cefa0c803d1a6d03a45c1579705e18d5982b22c64f7e46`  
		Last Modified: Tue, 12 Jul 2022 20:22:56 GMT  
		Size: 86.6 KB (86580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2804a718c3b2adb4f6ed1540e5545d671dbb8935188a6d8eaf82d8981f090b8`  
		Last Modified: Tue, 12 Jul 2022 20:22:53 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44dd317ca6ab62a5317f12d094555b987d9cf8594614267a5981c01dcb2d521`  
		Last Modified: Tue, 02 Aug 2022 19:33:51 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84bce00334c470628c6322f8d1f86afd09b82c456b821572c7c20ad1651decf`  
		Last Modified: Tue, 02 Aug 2022 19:34:23 GMT  
		Size: 157.2 MB (157222199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79bfffbf053bb1ad07b4fdeeaffca88835845c02cf403039a5a6e10cb37d3cb4`  
		Last Modified: Tue, 02 Aug 2022 19:33:50 GMT  
		Size: 53.1 KB (53126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83aa49948700ffa634400050d52e955f4a1f0a4104f8696727ff3c9e78e9e726`  
		Last Modified: Tue, 02 Aug 2022 19:33:50 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:nanoserver` - windows version 10.0.17763.3165; amd64

```console
$ docker pull golang@sha256:40bca53cab1c2b61544e6616deca56a75c184f262068f7c29cc9d2b59b19b8b2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.5 MB (260527556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01eeaaf8372e8a34cd080237f9cfca1576971e397f96c68bb322453707513106`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 06 Jul 2022 22:15:10 GMT
RUN Apply image 10.0.17763.3165
# Tue, 12 Jul 2022 19:43:41 GMT
SHELL [cmd /S /C]
# Tue, 12 Jul 2022 19:43:42 GMT
ENV GOPATH=C:\go
# Tue, 12 Jul 2022 19:43:43 GMT
USER ContainerAdministrator
# Tue, 12 Jul 2022 19:44:22 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 12 Jul 2022 19:44:23 GMT
USER ContainerUser
# Tue, 02 Aug 2022 19:27:14 GMT
ENV GOLANG_VERSION=1.19
# Tue, 02 Aug 2022 19:29:49 GMT
COPY dir:a0f94dd1112f1f27c08d5ea3b68903d61c05f30a36f261cf395a623cb13deea1 in C:\Program Files\Go 
# Tue, 02 Aug 2022 19:30:37 GMT
RUN go version
# Tue, 02 Aug 2022 19:30:38 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:5d24e1a2f5c566b0afb1e46fc24e5cec821c8ebf44220276a95a2b91f44a2f2a`  
		Size: 103.2 MB (103155009 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c14e0078b75f39dd734aa5bda1a20ee6aea0391d04d7986262fa35b4ee1b4046`  
		Last Modified: Tue, 12 Jul 2022 20:24:02 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58123f14ee126159f65688fa93c48fd79e7accdb32597dd01733e08a7f53dc2f`  
		Last Modified: Tue, 12 Jul 2022 20:24:01 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fc8029652a8954a5a99d5f3a33f6fdb9063693255e805a20b8963c195815fb`  
		Last Modified: Tue, 12 Jul 2022 20:24:01 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3769b7ac07e824a5ed356258fa6870ca8df0bd37ab1cf016a3033d9a2943f6c1`  
		Last Modified: Tue, 12 Jul 2022 20:24:01 GMT  
		Size: 69.4 KB (69434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dabb95e3ef99b306d606ea8969c68055e25dcada3a0f64ead470fd2f7729835`  
		Last Modified: Tue, 12 Jul 2022 20:23:59 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885db37e031c41d637a06521c5a96f88373e2000513add7be29c35149f625aeb`  
		Last Modified: Tue, 02 Aug 2022 19:34:38 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e439e1f566e512416252e8809ebed066e5ee410538e57d5e48b1b48a6b570f75`  
		Last Modified: Tue, 02 Aug 2022 19:35:10 GMT  
		Size: 157.2 MB (157224393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2578981d4ef1ded283c8043205fc72aaad8e3fdbfa6b3cd3cd19e2c3ded599f1`  
		Last Modified: Tue, 02 Aug 2022 19:34:38 GMT  
		Size: 71.6 KB (71634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f2dec4417c339e2059dce4593e086c91685f024b394265b98af07a6a34db02e`  
		Last Modified: Tue, 02 Aug 2022 19:34:38 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
