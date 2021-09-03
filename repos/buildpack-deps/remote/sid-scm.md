## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:dc3d89c3c1a5a9a751a15b83c33071837b4224ce80dd596a295f29aaf71f50b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:sid-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:102436679d78c1a1df93a0df1cf1a746f2ee87ab361ecbcaef1bc6511b088d17
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127266014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d451671b4cace0a1bdb070461238745a9108f3cd0f904c13a25123e8f1b370fc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:22:48 GMT
ADD file:7ab12da96bcf5f352bcecb8ee3269debf1ca1bd2d25aa9a7b66b1e4f84e07c3a in / 
# Fri, 03 Sep 2021 01:22:49 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 06:34:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 06:34:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Sep 2021 06:35:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f9ad9a9c210fa67e2eb0faace583b349a4623b682daec47e2b4c65c33ac9a92f`  
		Last Modified: Fri, 03 Sep 2021 01:30:17 GMT  
		Size: 55.5 MB (55493249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35da5ad7bf2e9855b50b45a4232e9232a0a526295c6e37dd03c8cb83aaec56bd`  
		Last Modified: Fri, 03 Sep 2021 06:41:43 GMT  
		Size: 5.2 MB (5172175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7bd4995fd96d3e3b0abdc38efcafa24cd3e63ea4cfa16baff0b5d41248f9ef`  
		Last Modified: Fri, 03 Sep 2021 06:41:44 GMT  
		Size: 10.9 MB (10897876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a082b765aa23e12f531481435cba94fa174a79bd68f7b8e23647b03cb826438`  
		Last Modified: Fri, 03 Sep 2021 06:42:04 GMT  
		Size: 55.7 MB (55702714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:f4d652abef61df48e9ffc5b9cfa0ff60275c7ece073c683f3470789e1ee2eae4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (122045084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce452975c108df26a1608befc48d7763e67342afecc2dc1030811fa8f36585aa`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 00:53:41 GMT
ADD file:9d67c83a2e727f33502861325786047b9c6034b490854b93efb2d59cf973e5b6 in / 
# Fri, 03 Sep 2021 00:53:42 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 02:39:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 02:40:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Sep 2021 02:41:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c25501d6a46457c5895808abc531a7dcd2b4008bc42a432fcd73b6325c3fdacf`  
		Last Modified: Fri, 03 Sep 2021 01:10:41 GMT  
		Size: 53.0 MB (52980070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ca497a6979f627d04639faa5571c98e112e1c56465986fce9d78c17101a5ce`  
		Last Modified: Fri, 03 Sep 2021 02:57:25 GMT  
		Size: 5.1 MB (5077618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eab0927e6f1d00c87c3eed02237eb8b36a819bc0188dabfab4074f096423576`  
		Last Modified: Fri, 03 Sep 2021 02:57:28 GMT  
		Size: 10.6 MB (10595736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab42f59e6f95fa1040561c411658a005c01b13425791de2b04eb66b15d32f5a3`  
		Last Modified: Fri, 03 Sep 2021 02:58:18 GMT  
		Size: 53.4 MB (53391660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f32366e726d463b8b44074e8d52b67014454695c7c369b00e831b192be630c09
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.2 MB (117166520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66bd916dc15c506f89d8e19388c84db2f0194f3b14ebb0ed7a0bf806bb9960c6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:03:00 GMT
ADD file:78431ef521d2864441ad8fd6f5238d8c49ff519c7f8510394048cc042f270288 in / 
# Fri, 03 Sep 2021 01:03:01 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 02:59:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 02:59:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Sep 2021 03:00:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:669a70f2eaf280942d3e643fd270beb3d6f313daba0d40fa8f3a72810a1e9bbb`  
		Last Modified: Fri, 03 Sep 2021 01:19:37 GMT  
		Size: 50.6 MB (50637968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df9116db71fd664add238def53f5a22bec8a3292c6838466fb4f27cab0a4f32`  
		Last Modified: Fri, 03 Sep 2021 03:19:09 GMT  
		Size: 4.9 MB (4938329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b370eb59a5763f3c415a9a5237b8e0f6513d04e87645086ddebd2c455a1322e1`  
		Last Modified: Fri, 03 Sep 2021 03:19:10 GMT  
		Size: 10.2 MB (10238093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12cf3547f848e6beb2122f9de522d93a9deb5cf45d1a602f3a7c51317ce9dfa`  
		Last Modified: Fri, 03 Sep 2021 03:19:59 GMT  
		Size: 51.4 MB (51352130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:14cbf3ebf4fa91d65624ff14352814e1da867333f242462a635b4b5d95590d95
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 MB (126423138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ebed91b38753d909086f1695d753fdc8713e1d33314b750ea10522b1494b937`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 00:41:54 GMT
ADD file:e9cb8fff7ac62f9bc8a4ccbc3960693736104975b5c3ffc855a1b6dea13b4c10 in / 
# Fri, 03 Sep 2021 00:41:54 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 04:35:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 04:35:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Sep 2021 04:35:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2cf0882b72727438ab6f57aa6a77711053bee00d53c08f527d6fc8e582fcdb3f`  
		Last Modified: Fri, 03 Sep 2021 00:51:39 GMT  
		Size: 54.5 MB (54529119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb5fa429768d201e6729375041d9f10e3f1c4f37f2be592556628bd633b52b63`  
		Last Modified: Fri, 03 Sep 2021 04:43:31 GMT  
		Size: 5.2 MB (5160231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e36c7a8c3d951e4bab7bb201143c723a1db2d463482ff21f205c9a80f4d132c`  
		Last Modified: Fri, 03 Sep 2021 04:43:31 GMT  
		Size: 10.9 MB (10891597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9b729d5d692c90d9a49e0e886e5d1e8ab3165d31c7eddebf1f3560b9f836763`  
		Last Modified: Fri, 03 Sep 2021 04:43:52 GMT  
		Size: 55.8 MB (55842191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5e902fe3e8b8a92742d88713fae4924948e30a80da779cbbb73d5209c94f20d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.2 MB (130210303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a489eac282dc42cf470be83be408afb4620ba4535365f52b1c9a23b11639610a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 00:41:36 GMT
ADD file:64515d15f0b2fac0544e320a88716de6bf306c10f7e9400a945fca420a730843 in / 
# Fri, 03 Sep 2021 00:41:37 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 01:14:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 01:14:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Sep 2021 01:15:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:965ebee0ec76f6f76a0d14e40b7923292e9028532546ec1a748a8fed8267c897`  
		Last Modified: Fri, 03 Sep 2021 00:51:22 GMT  
		Size: 56.5 MB (56525268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56089068afb291eba965e50fb15a03f5ae7c433295ed8d952822fe54d1c1dd97`  
		Last Modified: Fri, 03 Sep 2021 01:22:57 GMT  
		Size: 5.3 MB (5303864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab52954bb9b6200d56553ce69fb7dae734a92c479ff8e38af69fa29a7d28110c`  
		Last Modified: Fri, 03 Sep 2021 01:22:58 GMT  
		Size: 11.3 MB (11270876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e266a96f5269409185770fdf13c62fab48d43de3f82cf97cb0f93890ae2b4a2`  
		Last Modified: Fri, 03 Sep 2021 01:23:25 GMT  
		Size: 57.1 MB (57110295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:e7bbed7ac5659c6cd1aececdfaa4dc4744c5e258ee5c650a8ec37b539fda309b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124674074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41f801a22581fced8c27b30a1378a19368e58a491bf7f4c84d59eb7a011e8343`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:12:04 GMT
ADD file:d3a974d875f356507b0ce365ec750c6109f909b93c690b9778a4c115aa14a20b in / 
# Fri, 03 Sep 2021 01:12:05 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 01:53:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 01:53:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Sep 2021 01:54:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3d38c5abd667c8252a6e859616365d153c0ebf15516c401ad631183f19343ec1`  
		Last Modified: Fri, 03 Sep 2021 01:21:53 GMT  
		Size: 54.1 MB (54135005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee8b578c68c33ad5ddf748ce7497de380f1903d441aee0c8b0b1af0471180e1`  
		Last Modified: Fri, 03 Sep 2021 02:04:43 GMT  
		Size: 5.1 MB (5132409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814a57f2a02c7810a593cba16221fab32426c75881bc128a91ef728048538e53`  
		Last Modified: Fri, 03 Sep 2021 02:04:45 GMT  
		Size: 10.9 MB (10900458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a709b007930a1acd8d8ea50132cb0b6a34e4f6f470c1b917f467d1263256229`  
		Last Modified: Fri, 03 Sep 2021 02:05:35 GMT  
		Size: 54.5 MB (54506202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a5c418dd1d0e473e559b3a703a9e40757ead45790002b65bfc2bb736e31a077f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136722538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19cf7cb6d58a64ecbd4e666e5dc9905f0bb6786a021d2c2d955cf233ab37f7ef`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:26:09 GMT
ADD file:eb825a05756409572b414e35fa1f7f58986be1d8d7b4251cf7ea2eab299ccbd4 in / 
# Fri, 03 Sep 2021 01:26:18 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 06:44:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 06:46:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Sep 2021 06:50:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eeb3edf1a6fea1725c5b8863036bbeeab17fd1ba2d09e50f1a016800ecc239a4`  
		Last Modified: Fri, 03 Sep 2021 01:42:46 GMT  
		Size: 59.5 MB (59534072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a95302a54a7fa51cdd0cd0117968b05d9f71d3c40eafe66873816a3b43ba14`  
		Last Modified: Fri, 03 Sep 2021 07:14:06 GMT  
		Size: 5.4 MB (5422617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da11fea16e40da1a9b66dee60a49dee27fffb468c778b12670ed59f3cd11837`  
		Last Modified: Fri, 03 Sep 2021 07:14:07 GMT  
		Size: 11.7 MB (11650959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd39c289a3baa1fff8358db49e63fac02746752ceae177b4b7a19642ba640995`  
		Last Modified: Fri, 03 Sep 2021 07:14:30 GMT  
		Size: 60.1 MB (60114890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:75dacb3d7efa37c55a2ee04f476c40809377e9cbe9f4873bbb31898f271409e3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.4 MB (118351561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0997c4f2769ed1634128d9554d1a4e7dd0308c463b797eeb1c5b77933109c777`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:16:10 GMT
ADD file:22169a464bc792387d0c6cd4ca985b70527601306f274a47f7a26223b125d1b8 in / 
# Fri, 03 Sep 2021 01:16:13 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 01:59:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 02:00:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Sep 2021 02:04:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d209f64ed888c716b8fc1f768d766ccf831d8a034eb5e3ca12945873acb106f6`  
		Last Modified: Fri, 03 Sep 2021 01:32:35 GMT  
		Size: 51.3 MB (51289049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da873824fc3fcd77f59d7598fa94a4e0eef799c270584961cd61b0193ad259c`  
		Last Modified: Fri, 03 Sep 2021 02:39:12 GMT  
		Size: 5.0 MB (4986349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfba85c856d5ce39bea54898a8e2d95aa9c37df4c646386dfd0d1099c262561`  
		Last Modified: Fri, 03 Sep 2021 02:39:16 GMT  
		Size: 10.3 MB (10313344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4008dd868e4d390b41b3510374a17a33a9fe636188767c8e61b168424fb1ec02`  
		Last Modified: Fri, 03 Sep 2021 02:41:24 GMT  
		Size: 51.8 MB (51762819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:75558dfed6e9f5fec05b1fdb390d686321ea9d9e006fbe11632fd936473b5cd9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124871121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4667324b850550595dc9a21fae5846f605d83d5551da54cc420b955bdffabc72`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 00:46:03 GMT
ADD file:4dec873e9e3022f644e228769ed26be34f63fb2d9b0ddc10816af8c9eaa11a15 in / 
# Fri, 03 Sep 2021 00:46:13 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 02:11:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 02:12:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Sep 2021 02:12:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2c1522cfd5f84804048a7cb823dfa679d77781943db2c6e71d872921d6d7542e`  
		Last Modified: Fri, 03 Sep 2021 00:54:32 GMT  
		Size: 53.8 MB (53772150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305bda156f1bbe0e441c40cfe1badc3590f18bfe3b1708ce8d2050c033c40ea2`  
		Last Modified: Fri, 03 Sep 2021 02:21:38 GMT  
		Size: 5.2 MB (5153859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9ac738bf714d2148f583c8c4ff6147a0840fc80305cf406c832bb05ad7eeaa9`  
		Last Modified: Fri, 03 Sep 2021 02:21:39 GMT  
		Size: 10.8 MB (10791081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d4c39e7ec2e00b89fdc841a618fe0f405052037f5cfe5c1660d4c10ca31846`  
		Last Modified: Fri, 03 Sep 2021 02:21:56 GMT  
		Size: 55.2 MB (55154031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
