## `alt:latest`

```console
$ docker pull alt@sha256:993cc660531ec8f9a48290729fe8dcf4f10d90cbda294bdc5f9d3a7db913ab50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `alt:latest` - linux; amd64

```console
$ docker pull alt@sha256:273a48ec7b1cda9be55fd7ae344c7c00d92ab925e40c871705861eb523107e4e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41819986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9738cf9e9ed3c895c1252ea483a3b346026268532290548425045aa33bbf4451`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Aug 2021 22:28:37 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 05 Oct 2021 22:19:46 GMT
ADD file:f3865144ef386c3910ffd911a2b8505180236b68aeb88d5930269e460a893be2 in / 
# Tue, 05 Oct 2021 22:19:47 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 05 Oct 2021 22:19:47 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:89621db199c966be4c1eb1c9225983a5095f5809450540f8bd7250effcc71a92`  
		Last Modified: Tue, 05 Oct 2021 22:20:28 GMT  
		Size: 41.8 MB (41819794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7686f1e15c306644b670ab5796d2f33309b1e868cc1160cc23bf5bbb6ca352e4`  
		Last Modified: Tue, 05 Oct 2021 22:20:22 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:latest` - linux; arm variant v7

```console
$ docker pull alt@sha256:44e5e059bb978698974e28308bf3c418a1d4bb4e05772ba3608fc767f36d48cd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 MB (38286844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad719e52f0136b4bb8aeea2e9385a86c2f015c0888813c4c943476668fbc0252`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Aug 2021 01:09:27 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Thu, 05 Aug 2021 01:09:38 GMT
ADD file:60ae57cf5437fd8825004ab0bb326db4524bdbd06320c56ff9e386045cdfd47f in / 
# Thu, 05 Aug 2021 01:09:40 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Thu, 05 Aug 2021 01:09:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3b4b7cf260715942c5ded0ea00276068310de498d77fd664c4858ce357368e67`  
		Last Modified: Thu, 05 Aug 2021 01:11:28 GMT  
		Size: 38.3 MB (38286652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd8b308e9578b6d78633b7eeca89aa54d1845a5771a74942cd04931656d081f`  
		Last Modified: Thu, 05 Aug 2021 01:11:04 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:latest` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:cae253d247a47d098e72f009db3fc9b75f748fbd7766528f834fa97df0f94d01
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 MB (40803855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ef382274d41e0c4976b427d2a4d451f41e960def6d834a08654f556bed57983`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Aug 2021 23:11:19 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 05 Oct 2021 22:39:48 GMT
ADD file:2e8b90a92499ef5adf1d8e269489f5200db1e84d2ca1343e1cd8a3bfa3a55234 in / 
# Tue, 05 Oct 2021 22:39:50 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 05 Oct 2021 22:39:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:aa6113068268a552f8c4dd6f1a26ad0a46bbaeef09546674e95c1c0486a00c44`  
		Last Modified: Tue, 05 Oct 2021 22:40:33 GMT  
		Size: 40.8 MB (40803663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee086f6d364c7f7ee7f0ca591bdba7490bee9f03884754e2b5452a8b1c5934c`  
		Last Modified: Tue, 05 Oct 2021 22:40:27 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:latest` - linux; 386

```console
$ docker pull alt@sha256:46dc4854afa63ab93315076e344158d391225dfeb47bccdaa21a1d0e5854eab7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42530199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0a3f2d315b2208e0d588b57c95595d836c167a88b19309bc286f54df838841`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Aug 2021 22:45:24 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 05 Oct 2021 22:38:31 GMT
ADD file:70d38e61326d67a3511ba7a891499ef9b0ab4c12dcd6366cb244194af52ef01c in / 
# Tue, 05 Oct 2021 22:38:32 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 05 Oct 2021 22:38:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ec73ddddf89886a88827955c9a8bbc4c944ceea5315338d49e5f620c682164cf`  
		Last Modified: Tue, 05 Oct 2021 22:39:22 GMT  
		Size: 42.5 MB (42530006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4638dbdd87db8e166f5b39241ff1fde618a6d0e5287b7a9e4e86266a9bd70e64`  
		Last Modified: Tue, 05 Oct 2021 22:39:14 GMT  
		Size: 193.0 B  
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
