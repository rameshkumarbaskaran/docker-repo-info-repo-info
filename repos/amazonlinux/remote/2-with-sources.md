## `amazonlinux:2-with-sources`

```console
$ docker pull amazonlinux@sha256:c4b2a5f5fb26e7450ea583866daabe17846bf5153dd32f528c87677fabb1e117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:3fa69e7667e2798b355efa1cb986e0ce87646a102faef7c1557982eb1b0411fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.7 MB (492732704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da14082e500f08e79e37c063e3ed02b7a4ddef1a580b553c91045fec60f0146`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Feb 2023 21:20:09 GMT
ADD file:29cd40b7c56d98385ece53bcbadfefd25bc70ccf0326777986ef6a5720bdfe83 in / 
# Thu, 16 Feb 2023 21:20:10 GMT
CMD ["/bin/bash"]
# Thu, 16 Feb 2023 21:20:38 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-7e289542d782642b256d8350ebcc22b568c00303c6cedda53c0cc26f5de6cca4.tar.gz"     && echo "28173c8559de7e4838d9ae0e1c163243d6d1274f28d242ced6e7fa44272b36bb  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:d78505e615251c4f4af6eaa9507b67917d263d23551dcc5a1eed3c012d32a54d`  
		Last Modified: Wed, 15 Feb 2023 00:09:42 GMT  
		Size: 62.4 MB (62386320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e448b8061a833ba558b9628ae3dc088e3690f1a0c1624d5813333ca0224c06`  
		Last Modified: Thu, 16 Feb 2023 21:21:46 GMT  
		Size: 430.3 MB (430346384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:ba3f1afa6fa0103b96d2c2d4a70a860e5e21426cc566d1fba15be4558808f5b9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.4 MB (494350183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b75bcfc11d633380eb8a00eaa5fbd5672efa3107a1d65f850b71dfea70bf46`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Feb 2023 20:39:31 GMT
ADD file:17574026c2754afa903450c59a6d8f7d0905209b174cbe9c13252a61d5a6f916 in / 
# Thu, 16 Feb 2023 20:39:31 GMT
CMD ["/bin/bash"]
# Thu, 16 Feb 2023 20:39:53 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-7e289542d782642b256d8350ebcc22b568c00303c6cedda53c0cc26f5de6cca4.tar.gz"     && echo "28173c8559de7e4838d9ae0e1c163243d6d1274f28d242ced6e7fa44272b36bb  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:71343c2791199c6e2c19c308cff6493497a02f57e225c11405e1934dc7428b3c`  
		Last Modified: Wed, 15 Feb 2023 03:16:17 GMT  
		Size: 64.0 MB (64003805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64a7d1a6cba2e41239f96a04c0f08457a2254983add1e7c6f48ed5668abad4b`  
		Last Modified: Thu, 16 Feb 2023 20:40:47 GMT  
		Size: 430.3 MB (430346378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
