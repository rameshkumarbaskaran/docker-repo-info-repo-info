## `mongo:nanoserver-1809`

```console
$ docker pull mongo@sha256:465d31ab80b0b7f59639767681de8ef43b0a8bea84a2b3af7cbecabe75e81fb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `mongo:nanoserver-1809` - windows version 10.0.17763.4377; amd64

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
