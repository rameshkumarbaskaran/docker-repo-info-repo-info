## `mongo:6-nanoserver`

```console
$ docker pull mongo@sha256:37b5ba6b86572eebfcac58d032d7a2c0f1b89ed20082035ca06bdd9e335ffa87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1726; amd64
	-	windows version 10.0.17763.4377; amd64

### `mongo:6-nanoserver` - windows version 10.0.20348.1726; amd64

```console
$ docker pull mongo@sha256:114816461e1b9cd05c32834dfcb729f6f580f8b5a1a516185c5d53bc4d77392c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.5 MB (635519288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7f38835454af7395aef9fd73793bf1bfee81e3cfe2014190e4735155b64676a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 05 May 2023 12:52:54 GMT
RUN Apply image 10.0.20348.1726
# Wed, 10 May 2023 01:28:38 GMT
SHELL [cmd /S /C]
# Wed, 10 May 2023 01:59:56 GMT
USER ContainerAdministrator
# Wed, 10 May 2023 02:00:07 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 10 May 2023 02:00:08 GMT
USER ContainerUser
# Wed, 10 May 2023 02:00:09 GMT
COPY multi:4abffac378fdd7fd5082d54935b2f9dc2024a93fc9837ae8701ac6e024ef02ee in C:\Windows\System32\ 
# Wed, 24 May 2023 01:20:44 GMT
ENV MONGO_VERSION=6.0.6
# Wed, 24 May 2023 01:21:22 GMT
COPY dir:f255d7e00c887e6b06f18133f01bba238bdbaee13791df8bb9e0f4062260c28f in C:\mongodb 
# Wed, 24 May 2023 01:21:44 GMT
RUN mongod --version
# Wed, 24 May 2023 01:21:44 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 24 May 2023 01:21:45 GMT
EXPOSE 27017
# Wed, 24 May 2023 01:21:46 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7d382efe6974b94c05000b6a95c1fd28e1b8bb3e81cc4592b2aa1cc46b90192c`  
		Last Modified: Wed, 10 May 2023 01:48:23 GMT  
		Size: 120.0 MB (120001338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d879624716c16bfc9a9e8c219f4a25a8d311021e41efa6a951e95c4bb6fc44`  
		Last Modified: Wed, 10 May 2023 01:47:58 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91148a7dea4dbf3b1028e81c00818780ec56bdbb7563cc6100dacaf0aef85da2`  
		Last Modified: Wed, 10 May 2023 02:25:01 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35d61dd28046e22574977fb6b4d943048979c432dd7d414debb3684a58405c4`  
		Last Modified: Wed, 10 May 2023 02:24:59 GMT  
		Size: 78.2 KB (78198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd2e0389b82941ae5dd46a94665227d43b3fea67bff14cbf6ecc35cd654bb269`  
		Last Modified: Wed, 10 May 2023 02:24:59 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e7a5644fdc14b36e2d367b2a0cd0e92984d2f33a59df4c7ff7b370ca858b249`  
		Last Modified: Wed, 10 May 2023 02:24:59 GMT  
		Size: 267.1 KB (267075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9e0444d020f49fe843af7915e1165915fa75308204304f534b4e160b2aff6c`  
		Last Modified: Wed, 24 May 2023 01:39:40 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213511bdfddd00e0e89513fb4a57e1db803f446182a46bcdc7b1a7ce1c9dd6e3`  
		Last Modified: Wed, 24 May 2023 01:40:52 GMT  
		Size: 515.1 MB (515112560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0949a3e1f334dc9280d6d18955fa37fa287daad4506e47543d3821d44712c6`  
		Last Modified: Wed, 24 May 2023 01:39:38 GMT  
		Size: 52.1 KB (52093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7594e1297debb98e07fae000c1349346132bccf1733a9ef8155f7ab25ee71941`  
		Last Modified: Wed, 24 May 2023 01:39:38 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39373997733a9d66bf0de4c69236972a769d24e06ddb710f206b89a918afda9d`  
		Last Modified: Wed, 24 May 2023 01:39:38 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4cbab100e33aade0a4730bd79c63f23e720f6d2aea896cab26fc64b19626bfc`  
		Last Modified: Wed, 24 May 2023 01:39:38 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:6-nanoserver` - windows version 10.0.17763.4377; amd64

```console
$ docker pull mongo@sha256:bc34d689626d3b667cf7c9baa9aa17bd4d5cb7286c241da0ffc54a5d5b223b45
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.9 MB (619900248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d20c65cc27d18369b09813326280b08e2a0692f32fbc0cce5f7b0be9b439eca7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 01:31:05 GMT
SHELL [cmd /S /C]
# Wed, 10 May 2023 02:01:10 GMT
USER ContainerAdministrator
# Wed, 10 May 2023 02:01:23 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 10 May 2023 02:01:23 GMT
USER ContainerUser
# Wed, 10 May 2023 02:01:24 GMT
COPY multi:4abffac378fdd7fd5082d54935b2f9dc2024a93fc9837ae8701ac6e024ef02ee in C:\Windows\System32\ 
# Wed, 24 May 2023 01:21:57 GMT
ENV MONGO_VERSION=6.0.6
# Wed, 24 May 2023 01:23:12 GMT
COPY dir:f255d7e00c887e6b06f18133f01bba238bdbaee13791df8bb9e0f4062260c28f in C:\mongodb 
# Wed, 24 May 2023 01:23:33 GMT
RUN mongod --version
# Wed, 24 May 2023 01:23:33 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 24 May 2023 01:23:34 GMT
EXPOSE 27017
# Wed, 24 May 2023 01:23:35 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:f7885e3a2dfeae5eea125d00da688c29930a05e4d904884fe43e093ce6223664`  
		Last Modified: Wed, 10 May 2023 01:49:01 GMT  
		Size: 104.4 MB (104383998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ddac9d33b62fa0bb37c6743a1992a622e53b5bb070758474e92416b5f031ba`  
		Last Modified: Wed, 10 May 2023 01:48:38 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca1a117e5be28c4247978f3dfd437fff6feffb4a11ea43d4338f5d2b068ac76`  
		Last Modified: Wed, 10 May 2023 02:26:28 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba404708f5c409a4327ef9a8ea3e3601dd2db287f5d90c7794dada10f4ae9e69`  
		Last Modified: Wed, 10 May 2023 02:26:26 GMT  
		Size: 62.9 KB (62943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc7f80cef905cfe3aae8cf8ef021d8f598871b9df0222b4cc3f5b66899cac64`  
		Last Modified: Wed, 10 May 2023 02:26:26 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5883016a4e02b85dace5bd9fe10a5466a6aa4896b34b6c5148945751cc896318`  
		Last Modified: Wed, 10 May 2023 02:26:27 GMT  
		Size: 267.1 KB (267062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf98185f5d58e9fcaffd3ffeb676d00d9f8c2bfe82a10f428a73f35e123e14f2`  
		Last Modified: Wed, 24 May 2023 01:41:08 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96052da46ffb1a0fd07e7a549bcdd70b3762f4f8d253b4e417007324dff01129`  
		Last Modified: Wed, 24 May 2023 01:42:22 GMT  
		Size: 515.1 MB (515112671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f136d0e8a0b46ab690ce0c78043deb623fe8b4a0e42b09654ca63dbe6691c6d5`  
		Last Modified: Wed, 24 May 2023 01:41:06 GMT  
		Size: 65.7 KB (65691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b5df77774e02bb309ff759198889e57039578c7a1268321b852e56eb284e84`  
		Last Modified: Wed, 24 May 2023 01:41:06 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db348d21cdbd94ca57fa14143c97bd710f2851152c5a1922273c1ad21afbaf8`  
		Last Modified: Wed, 24 May 2023 01:41:06 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ddbc3dea9289d69b8981e687c342482a945e09a05216fe2972e18f30bb7ab5`  
		Last Modified: Wed, 24 May 2023 01:41:06 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
