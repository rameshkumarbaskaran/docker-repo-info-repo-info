## `alt:latest`

```console
$ docker pull alt@sha256:547c634a227f037141fbd5c487404ac88d5afde143d097acda15920acbfc55e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `alt:latest` - linux; amd64

```console
$ docker pull alt@sha256:28143858965606980b048f66d0e0442b2cd4be4c46badba24bf049470b96add0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42511153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4177157040d644bcfd8b70f4a16fad1c43533c6569d986a4c58c0b1c42b4803`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 11 Aug 2020 20:19:59 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 11 Aug 2020 20:20:03 GMT
ADD file:fa2206aa87d27af7e61782300c6c650e6cb4323662e94edd3a01a7cac25e5d40 in / 
# Tue, 11 Aug 2020 20:20:03 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 11 Aug 2020 20:20:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f5f59d3f04f02bf1298793f8e3d6b80e662997ec92b48601f6283bb76881c28c`  
		Last Modified: Tue, 11 Aug 2020 20:20:52 GMT  
		Size: 42.5 MB (42510965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73b5b8965c7e28823eab213685a3ebf3c43ae59a790afe57f119b68e4b1697e`  
		Last Modified: Tue, 11 Aug 2020 20:20:45 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:latest` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:8dec3aa7cd48d79cc1ce7a2508530c8776fbd0c685c90084c7d0b21db228e72f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41321305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e6687a01f6ab620a3b1af1642c4d0395643b37ac4f7088c8cdb9360570cc6e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 11 Aug 2020 19:40:59 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Mon, 09 Nov 2020 19:40:41 GMT
ADD file:1302f411b4279b77738009b3cd58e044dec6017e686d29d3e4a036f0d743bf5c in / 
# Mon, 09 Nov 2020 19:40:43 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Mon, 09 Nov 2020 19:40:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9b635f18fc777fb70ec11c83201f5362dde2937a5e78e4449852dd08e7db75b7`  
		Last Modified: Mon, 09 Nov 2020 19:41:25 GMT  
		Size: 41.3 MB (41321114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:535ded812f564833f58038e74fc888ea1f20fb2082ab3e735c1385f067889f4a`  
		Last Modified: Mon, 09 Nov 2020 19:41:13 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:latest` - linux; 386

```console
$ docker pull alt@sha256:e943efcddde05cf362ff4f94943a7f694f079bb43db88740201d80318d9a7317
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.7 MB (42703158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6afb6b6e67f1d94b1d75d0ae6e2fce47b16d923cca11195ab5dd51dae0408644`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 11 Aug 2020 19:38:56 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Mon, 09 Nov 2020 19:38:48 GMT
ADD file:c6aafa1b9d1711f281304a255b0f99d19a35bc98810959fc4ae365f32ae1ab64 in / 
# Mon, 09 Nov 2020 19:38:49 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Mon, 09 Nov 2020 19:38:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4e2ad71ff8d9b33647e383df67f23a76bdbb30a9feb6ab4eb62bc74d038eb5a8`  
		Last Modified: Mon, 09 Nov 2020 19:39:37 GMT  
		Size: 42.7 MB (42702968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a93f476cb166d55843a0c3298c5e0516bd25b9fd4eaad450dd82bb6e1e9ad3`  
		Last Modified: Mon, 09 Nov 2020 19:39:30 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:latest` - linux; ppc64le

```console
$ docker pull alt@sha256:4d8a128b7c2e19c413a1335b6ff2d061fe1915c3d1da6fd762485e756ca2c6bf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46174380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8031fea98a988c38b1b71a3be296c6dfecd92adf8344628821c0f7ddd3f983c3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 11 Aug 2020 20:29:27 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 11 Aug 2020 20:29:34 GMT
ADD file:27ea35c351886e161ec81f839ebf4ea563b8cc74a3ec0763a5af2964ca2fcb8d in / 
# Tue, 11 Aug 2020 20:29:54 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 11 Aug 2020 20:30:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c79ff3f45e8d56dbed10328416292bba1a02433a9394d7a568e92cd455f9bfec`  
		Last Modified: Tue, 11 Aug 2020 20:31:34 GMT  
		Size: 46.2 MB (46174192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcceb213bb5847674da8e3ea28b5aa90492e3fc3ba42636bd074cc569616f24c`  
		Last Modified: Tue, 11 Aug 2020 20:31:24 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
