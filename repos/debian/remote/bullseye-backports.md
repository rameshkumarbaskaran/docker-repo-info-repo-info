## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:795e703c052b4959cd43fd8894a72fcad2bbf877a7f4e111e3af4de1601e92fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:bullseye-backports` - linux; amd64

```console
$ docker pull debian@sha256:4b397d37bd4a4d2548611241faea287a10608afb61114e87ffe481eda2ee12c5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54868175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0145c8edd129b4b702810270570bf295fcb22acf43395a2a8f90545ca7261ca5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:11 GMT
ADD file:54b23fc0b4b728c85082d50693e314d74e46329004bb55a97f43fea46c497dd2 in / 
# Fri, 26 Mar 2021 15:20:12 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 15:20:17 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:efee637ec1bae521f17fb8d92548c288e3396988c475551b8774c0d08c01c70f`  
		Last Modified: Fri, 26 Mar 2021 15:26:18 GMT  
		Size: 54.9 MB (54867948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218807b970e3585f74923b96c5295f745f16f15a09ff18119c6ff50193b88be0`  
		Last Modified: Fri, 26 Mar 2021 15:26:30 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:020a4e98296299b5459523a996abdd8235d001cc513f871ee553d565b021f35f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52404752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5667d63e1eb7d2bd2cfe10a4f25398e82bba685dd809147f0cab82b17c90151`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 07:50:33 GMT
ADD file:1b779b19b47bb1848292d2bf671b599eb9041626b747d8016817e0c7d46ff881 in / 
# Fri, 26 Mar 2021 07:50:38 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 07:50:48 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d8d862331f8860c127d174052922618c93a166777e5b776e8b08e87702af28cd`  
		Last Modified: Fri, 26 Mar 2021 07:59:08 GMT  
		Size: 52.4 MB (52404525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65cc754ac4139f2bac54816f6123446fdf99a092925500e9583adeb19e1f357`  
		Last Modified: Fri, 26 Mar 2021 07:59:18 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:999b3475e2b8378fa4102a6f3ae7b53c050f6e93d2e30c247c576758db001510
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50074204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf3d0e70a6659295e538c7e91837233232b969f179c472554061d65502953b73`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 11:15:27 GMT
ADD file:e3651409d9338da981cd9fbd8d9b8511edbde0700ac9e0df8937b859e004990d in / 
# Fri, 26 Mar 2021 11:15:29 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 11:15:40 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:dd9021b04def024e25507cdd1b0967a20a384ad5cc255120cfb8c5f43495fa74`  
		Last Modified: Fri, 26 Mar 2021 11:26:11 GMT  
		Size: 50.1 MB (50073977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2647116fbb65b814f1d78a86d7f70b64f52cc4d7f129074f4e792ebdbf0a05a0`  
		Last Modified: Fri, 26 Mar 2021 11:26:18 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:7c3c1d7cce98058c97ad1830d0f89720848de4df2e6a3601372fd8e18cdfbd4e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53555396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed92e2473b3cc79f24005f3917dc8288360a7e9340bed7c6d191fa286f101d8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:40:38 GMT
ADD file:7a01671cc1e0be7531bee33435db95fa465b434bb5f683b3418f6e0768eb5367 in / 
# Fri, 26 Mar 2021 15:40:42 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 15:40:52 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:aadeaa81c69d313bcee9d050d099f2efd49d3c36d4dc100444f09cd71321f257`  
		Last Modified: Fri, 26 Mar 2021 15:47:37 GMT  
		Size: 53.6 MB (53555170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6226b5d42fec9cc88eeea446924d5cf719d758b888a6fd4481be872e7b6e52f2`  
		Last Modified: Fri, 26 Mar 2021 15:47:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:53e9238b28c470b04caf298f175abdff2c5daab94485be85468676a6ea9f4b71
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55881687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde1931aba0a4889dae55d66d31745536d48455ca9a2bd3a3f5721d82362eff4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 13:52:22 GMT
ADD file:a351d1298a5051f829e330b747943dba9a67cc050d1f23f62be062f669830e9a in / 
# Fri, 26 Mar 2021 13:52:23 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 13:52:29 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fb6fc5804fde9f18c538230f43ec9b5dc9c2466d8fc49f7510911c12de70d991`  
		Last Modified: Fri, 26 Mar 2021 14:00:05 GMT  
		Size: 55.9 MB (55881460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fbb0497e89095f8f4d101343ad8fb9cee5289ed6ecb400497ae39c272db534f`  
		Last Modified: Fri, 26 Mar 2021 14:00:18 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; mips64le

```console
$ docker pull debian@sha256:ade49c26d85a30b04f6c1f3cecc3390f2ec19ede6c6a4cd7408415da96c3f9ee
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53129021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c174eff2d9ae29fd2b2d8662e0ca423ed7fe164807ea3f9e24918c7a86d1bd0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 08:08:46 GMT
ADD file:7e11d2e31071a03f4f43a78cd6af64c7034e2267c839bee84afd1e3bb9916f3e in / 
# Fri, 26 Mar 2021 08:08:47 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 08:08:52 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8e3b00636426049a0189d8511a90dd5801df2b5793acbaa564ad20c57c4ff115`  
		Last Modified: Fri, 26 Mar 2021 08:14:22 GMT  
		Size: 53.1 MB (53128793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7ff116e17d1fe9182fdec970c341a14050809e7ce66718add79a790732dd30`  
		Last Modified: Fri, 26 Mar 2021 08:14:37 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:c6ea45d7ce4c7a8131892992f3c3e505ada868558ee2ee00492b8837d2c31879
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58756930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b7d16002d6ab4584d9f60ff124c74c215cee7cb6aa91dca0b0c7ca4fdce248`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:12:40 GMT
ADD file:28f7d129aaacc2de6bb78dec104b788d0aa25aaac87e07873668354a5b755268 in / 
# Fri, 26 Mar 2021 15:12:49 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 15:13:11 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:18ddfb418fe2dc2d92f9b851d0345827010c7b001ef98bb5a8b1730d80e2eace`  
		Last Modified: Fri, 26 Mar 2021 15:20:35 GMT  
		Size: 58.8 MB (58756702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a91cad4f5cf8d2ca6d53be0d841529d2c54ac1d1169defdf2289499bd1afaec`  
		Last Modified: Fri, 26 Mar 2021 15:20:50 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; s390x

```console
$ docker pull debian@sha256:368dde589d760c4d65a72defdf540b546ec26d652ae790d511bcbe6172668711
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53148045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f762b62592955ac9ef4b442e7e3387e96577d5883456fa5c6214f7ab9f35f51a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 10:52:51 GMT
ADD file:6dd7d4b323fd63c8ee8a655a79017b62cdad999e420310b15e9568404d02e856 in / 
# Fri, 26 Mar 2021 10:52:58 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 10:53:07 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7fcb7355b5dda69e2044a1c24be0597b43954f9d3183dde70ac38aac25df7adb`  
		Last Modified: Fri, 26 Mar 2021 10:56:55 GMT  
		Size: 53.1 MB (53147819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef999da25d4176e644604d892ae93e62b610655b1245092677e88fea8ce7d49`  
		Last Modified: Fri, 26 Mar 2021 10:57:00 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
