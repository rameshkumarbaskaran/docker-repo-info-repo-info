## `alt:latest`

```console
$ docker pull alt@sha256:f103cbfb2617262dc013e24fb666db7169c623deb8854d0f0545a3152f9a5141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `alt:latest` - linux; amd64

```console
$ docker pull alt@sha256:d16c19c06412015d75bf03323911493e50a8ee6815f34fef7cc09efba14ff72c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41794973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96b8a58d0ba35c66e9fec99e6853798e43bd05027897bc2005ffb92e26a71a61`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Aug 2021 22:28:37 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Wed, 04 Aug 2021 22:28:40 GMT
ADD file:2dee5d901e3b2f9c43864f6978a7e04f73f6abd103e52480eb45fb58be4571bc in / 
# Wed, 04 Aug 2021 22:28:42 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Wed, 04 Aug 2021 22:28:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:86bd305d9be619c50b3f3cadc0f039e8fed0e6e96a170ae9e7470a534e9731ea`  
		Last Modified: Wed, 04 Aug 2021 22:29:35 GMT  
		Size: 41.8 MB (41794786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006b17da32569f0052679e8978e069f7759038ff9f8783935110d33569d92f46`  
		Last Modified: Wed, 04 Aug 2021 22:29:28 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:latest` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:e955faec3f8f11324dfa4a4d864f5f45868e9c5460e8c294ca9fe798836c18b5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41328146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85087d3e094759f08d977c43f5a6e907fe9e308e496458f6378c7f7a1d05b3da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 11 Aug 2020 19:40:59 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Mon, 01 Feb 2021 20:52:52 GMT
ADD file:15b783f7dc1dd5e33ab77cc1e4bc05cc6a7f516e22cada40d2df962b89235dfb in / 
# Mon, 01 Feb 2021 20:52:56 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Mon, 01 Feb 2021 20:52:56 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1e9e2110c1578c23fbc40cf07677a803524a09a39306a63240de0361e7a35a3c`  
		Last Modified: Mon, 01 Feb 2021 20:53:35 GMT  
		Size: 41.3 MB (41327955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5a3b500af59411ea0f64e8ee388f1ca42112878bf00c372a07bc1f6d1629d3`  
		Last Modified: Mon, 01 Feb 2021 20:53:25 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:latest` - linux; 386

```console
$ docker pull alt@sha256:5820cdbeb4c0b256594bad0f7662b397a12b42a7e6d3235669e8ccb0b6b8825b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42493187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e69c9f1f91378adf74b0562083c587e59f95a37f5867071496cc2c37afc027a6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Aug 2021 22:45:24 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Wed, 04 Aug 2021 22:45:29 GMT
ADD file:7385ea329ae7fa1b0b6d1f19e584ac94b43a49585e6563abb0b9e9bb4058f217 in / 
# Wed, 04 Aug 2021 22:45:30 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Wed, 04 Aug 2021 22:45:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b586392f270b8228fe71612d508ba8b186fd1f2176f400c3d174f1f8fe3d310e`  
		Last Modified: Wed, 04 Aug 2021 22:46:34 GMT  
		Size: 42.5 MB (42492999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5844171be14075606171ada741268495264e87dae273655ad759303e850531ef`  
		Last Modified: Wed, 04 Aug 2021 22:46:26 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:latest` - linux; ppc64le

```console
$ docker pull alt@sha256:61c9c02cfe35ac11726b5c850cfa6be5fcd31ea9325bb213a09f6a5238c4c747
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44557045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fe54aa9c7b485ccbfa9a2974afa7b8ed9426ea9f351290ea85375d307443168`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Aug 2021 22:29:43 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Wed, 04 Aug 2021 22:29:49 GMT
ADD file:c0cd9d49037aa84f41061f2bc69c1ce6def0cf8a453db5967e378191c2afd062 in / 
# Wed, 04 Aug 2021 22:30:01 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Wed, 04 Aug 2021 22:30:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:caade519083556b1282dc1b002629dc83c9ad67894d39430973b00ca5c7263bd`  
		Last Modified: Wed, 04 Aug 2021 22:32:02 GMT  
		Size: 44.6 MB (44556853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5065b57674751c1c42172e0a6e5d6661c55821c1c9a746a1b869ab7a925f5cbc`  
		Last Modified: Wed, 04 Aug 2021 22:31:53 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
