## `buildpack-deps:oldoldstable-curl`

```console
$ docker pull buildpack-deps@sha256:11a38430437a646526bc7bd63499a6d2b83c5cbf9e3e1fa805028aaa7a143ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; 386

### `buildpack-deps:oldoldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9c03cc1d3e1d8b740a1a21b596031bcb8c34b7f5288c08b3cba309c34282592a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71936674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ffe66d54be973f7c35124f35888d421014eebf8b3f9493b5690bfc8bb95b9d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:20:54 GMT
ADD file:63fdbdcc45a46a993700d252a6f9652db8ab25688daa8bbceaed90b73b2654cf in / 
# Wed, 13 May 2020 21:20:55 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:31:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:31:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:0bc53e9ecf017dd9c8c8ba0c497d08e2d7c04f4a57dfce491d755cb37613f58a`  
		Last Modified: Wed, 13 May 2020 21:26:59 GMT  
		Size: 54.4 MB (54390659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedf82ca715cf8b41a88bfb26ad7225ae77537b5999a2f9a3ed1c430b19bc98d`  
		Last Modified: Wed, 13 May 2020 22:46:29 GMT  
		Size: 17.5 MB (17546015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4b6f3012cd03ef014e3fb2a49e92f488a66b520384e32061e6d3b6cca9709d18
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69619315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0801eda1228a5e6d493c654d385deb0a4694eb777d419e60e2ad8a69b771517d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 14 May 2020 22:38:25 GMT
ADD file:63b1bfb335518fc40ecfe92c179a8d32d00b3dee86ccf70751c74ed2ca14cd28 in / 
# Thu, 14 May 2020 22:38:30 GMT
CMD ["bash"]
# Fri, 15 May 2020 03:47:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 03:47:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2ef4eb1ad38349445de10c8a3682121a581770f589f1a35b7cb327b49bb1797d`  
		Last Modified: Thu, 14 May 2020 22:47:16 GMT  
		Size: 52.6 MB (52582082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303f3d44466578cfe6461e4b482b19224356c7b6537b39780b2e75a727ff8ed7`  
		Last Modified: Fri, 15 May 2020 04:03:29 GMT  
		Size: 17.0 MB (17037233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:818a15ace8692901b0a13d635a75d0d4de4705e5c1296b9eeb265476177a4b73
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (67027685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3651525a76ef4ef3786c1dad952c20cc4f62eec39a94da2a93052079ca914bac`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:14:33 GMT
ADD file:c27f6b9fb44500f82ed124d104a7cab3fed859c9cca4bbd0be2c77f3db082fa2 in / 
# Wed, 13 May 2020 21:14:36 GMT
CMD ["bash"]
# Thu, 14 May 2020 00:01:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 00:01:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2fb6d2bc03cec7adf4767dfcb7ac7a2740b65bd196c1071b809768619b12a0d4`  
		Last Modified: Wed, 13 May 2020 21:25:14 GMT  
		Size: 50.3 MB (50304251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e32375e9074306a5d2a3cec4864995cabaaefd56b21eace9822bfed9dc2169d1`  
		Last Modified: Thu, 14 May 2020 00:21:41 GMT  
		Size: 16.7 MB (16723434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:55a05307a37673e27f5e2c71c578e543290f99ae763f512817fe5440fd8cb400
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74463729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e562c09eb6e2e6145bb11fbc43d5c89b8866cb4480f15c10d3411ed883e2d976`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:39:42 GMT
ADD file:c41a548ee5a118fc5c8efefd084aca1f4629d3f462ed9d1bc5ddc568db89b0d2 in / 
# Wed, 13 May 2020 21:39:43 GMT
CMD ["bash"]
# Wed, 13 May 2020 23:46:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 23:46:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3ecac86f3144ef4bfa8747d585400212884f0a7fb2a71c1eb54483af30ca0449`  
		Last Modified: Wed, 13 May 2020 21:46:50 GMT  
		Size: 54.6 MB (54607906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f067623bec4e0179ef9af3ffa91e7197a238ad23d31f534e3ee78a83f4547351`  
		Last Modified: Thu, 14 May 2020 00:03:33 GMT  
		Size: 19.9 MB (19855823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
