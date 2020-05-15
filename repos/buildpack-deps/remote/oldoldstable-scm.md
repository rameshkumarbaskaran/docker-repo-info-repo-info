## `buildpack-deps:oldoldstable-scm`

```console
$ docker pull buildpack-deps@sha256:35be10ea32dcff5ace91caba69191da67d962fd5718a3ebc8d72ddb8c057937c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; 386

### `buildpack-deps:oldoldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a2126d54b9400cf310087de8f68f54f5c3a1d93cd1af58727afed59d7aad6828
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115271458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d781dd9c1478a52511916e446959fd6856ae8fa6fd1888cef508c095663c1e07`
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
# Wed, 13 May 2020 22:34:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:ddb3decbe8c76a4818f476de7732333bc00cdb7c3a75887374dd6d6450202e76`  
		Last Modified: Wed, 13 May 2020 22:46:46 GMT  
		Size: 43.3 MB (43334784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:11ad853c1a3252899edbe37b895204e92aef86f5b965ea61c126e8563be6561f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110775825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57c5cf974f4c743ef6a73bbd4bd5b24e2f5ef88bff23d5d4305d4344a103773`
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
# Fri, 15 May 2020 03:48:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:90476d81b98379937371481027b6bee589dad9dbda48c9b553b41f039ff3dc2b`  
		Last Modified: Fri, 15 May 2020 04:03:50 GMT  
		Size: 41.2 MB (41156510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9358379376f157069fe774887f60e8122c24838705c5b643871b05a182297893
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106806991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23357c3adba65571c436c71aec05501e81ee4c08d002bea66729e03caa8716b`
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
# Thu, 14 May 2020 00:02:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:0a5c0933ac15f5a3d4ea8317d3ccec86327de17987d9262818b5c832440327fe`  
		Last Modified: Thu, 14 May 2020 00:22:01 GMT  
		Size: 39.8 MB (39779306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:332a5ff4fcc353cfde372bb4cbf030a946139f2b4187343429e6d437d80ba8ef
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118453620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0589ac2e3f89b9c02e6f258961ff40afe9b1c77296020cb6f456d0c6d81db4bc`
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
# Wed, 13 May 2020 23:49:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:9716e17289a4b0c8f800234eeecfdaac67fe336e111d4cfefafa845d074a0c65`  
		Last Modified: Thu, 14 May 2020 00:04:00 GMT  
		Size: 44.0 MB (43989891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
