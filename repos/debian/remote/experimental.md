## `debian:experimental`

```console
$ docker pull debian@sha256:b849d83daf63c2aec3cb4610603a400f3fd0d6c3fddbd9dc38156dcf082241ac
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

### `debian:experimental` - linux; amd64

```console
$ docker pull debian@sha256:1f477cee84285417a36b091cb62423e7050cb61857cdfbac84742712c71dfbc7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.8 MB (54840831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b49678acf661d06bc3e532b5c1cad6e31572dcf32f1426d6ee45c069bf506b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 02:23:20 GMT
ADD file:e5e9ec8e65d163255761ecab0b3b02b5b3b9d8c72a927c4b41884f2abb7a6dab in / 
# Fri, 12 Mar 2021 02:23:21 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:23:34 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:784276bda577c362c89e3af4b9da7c8537bfed9871e1a3bdd68a61a6f21d022b`  
		Last Modified: Fri, 12 Mar 2021 02:31:36 GMT  
		Size: 54.8 MB (54840611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc3910afca9cb30338e2437cbadfa47f0d72297f563d2644226942940737876`  
		Last Modified: Fri, 12 Mar 2021 02:32:02 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v5

```console
$ docker pull debian@sha256:e6a9dfb39feb4fd4dda653c0a314139016da9f96eb63ad81fb138789232b8869
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52402643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ecf2885ec922297062365506f6d406c87094025e7d94466c6c9c135ed67dc8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 07:57:13 GMT
ADD file:32612d584d6e838fda991bcee065f36db394c6848444220ab925641eed015030 in / 
# Fri, 26 Mar 2021 07:57:16 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 07:57:40 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:ea6af2ab5e68178d221322a9de282a1dc71dad081d87e92a0861e9cbd6b706cd`  
		Last Modified: Fri, 26 Mar 2021 08:05:41 GMT  
		Size: 52.4 MB (52402421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa483613c27c2a61b6db5546785369669d2578b1680819499ead7e37599ec18`  
		Last Modified: Fri, 26 Mar 2021 08:06:04 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:32644de6b358ffe01575b9e40ef774434d110f95ab14e496fdcda14531f4960c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50071404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:152ba7496a9b1df42d58cbd475bddcbab1be8810e7cc9412cf45007ed0b2aed2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 11:24:04 GMT
ADD file:e1d5e4c7271fc5fa55d179768a79a0c6de2e179ee0bb16862bde35ca8e55eb96 in / 
# Fri, 26 Mar 2021 11:24:06 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 11:24:36 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:fada62bc534bd047cc273dfb6f0f66fb5d1475ae32d4a65bec935661d502b55c`  
		Last Modified: Fri, 26 Mar 2021 11:32:37 GMT  
		Size: 50.1 MB (50071182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c455c1fe90483c2d4575e1676d087140eda7102553a82c31700d472d6688cb`  
		Last Modified: Fri, 26 Mar 2021 11:33:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:2752a88868446c47ffb88543c62dfc6e2bbaa02b3da833576098b476ad35552c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53528974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7233eb4a70abd2f9caec1b49ca1e0d0cf0bd869bdfbf43f9e9ecf0a658be4ee6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:58:38 GMT
ADD file:6f5e59009f303ad248bd8e79abfaa711a6e5729de38bc1d123156aded54d7665 in / 
# Fri, 12 Mar 2021 01:58:40 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 01:59:14 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:88f01d8cac092ca4b0fdbd1d6f6f12f588ca6b1d67e4edbf961546df579f92e9`  
		Last Modified: Fri, 12 Mar 2021 02:05:16 GMT  
		Size: 53.5 MB (53528753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d847b6e039295a31815c4adfb62da59533712cc216bc815c25347c73987b5d`  
		Last Modified: Fri, 12 Mar 2021 02:05:39 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:6a89627d564a1602b27f49f322a01c652fd45d18e78d56f318ebf55ab087b21a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55863419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840678863d84790e54b80ae2eaf46679764a842fa431aa4caa79d487d1943224`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:47:49 GMT
ADD file:5f739ae1e3365731e11a9e3b8bebe7a5a3c667a307e6fa88465cf4806cd3604c in / 
# Fri, 12 Mar 2021 01:47:49 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 01:48:05 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:7399a8a959ed16266f4366d3e8fdfa0d117b88b2c8474c0f2dce9e8b44260e74`  
		Last Modified: Fri, 12 Mar 2021 01:58:21 GMT  
		Size: 55.9 MB (55863197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacbf659db129dc7dfaecf0d062d9bed23aca8daf0515a0234d0579bc0497cba`  
		Last Modified: Fri, 12 Mar 2021 01:58:52 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; mips64le

```console
$ docker pull debian@sha256:f8a69b4993283e7f37546958ca36a488ea80857d996f3f278dfb7676f2fa5feb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53127031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8367223de90e6e5ed6869860066c83594e0cf319b09af633fa8cb3bb30d322bb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 08:12:45 GMT
ADD file:c79a17a0f871c489c33a2d475b8e5371996f90bbc7760e45557108da54e86545 in / 
# Fri, 26 Mar 2021 08:12:46 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 08:13:10 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:75c364cc452cddccfec518752d444a6600aed010f6c6fb415dd2924ecd097fa8`  
		Last Modified: Fri, 26 Mar 2021 08:21:20 GMT  
		Size: 53.1 MB (53126809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee942771ebd98062575efc7cc7107c8dc519eee1e1d12981ade8d08be4bc8a5`  
		Last Modified: Fri, 26 Mar 2021 08:22:01 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:7231101792cd836809742bda34fcdc1253a024156389d43484df2a45ce2924f8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58754023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da4ba30c58a70444add9e14efe5ddc51644aca9dbdfcdaea0cf6e502bc49d94`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 02:36:33 GMT
ADD file:f3ddf49a1e87013415035eea5fb56efa4d9d2741c185c94d8300b6fb796f1b53 in / 
# Fri, 12 Mar 2021 02:36:45 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:37:37 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:54e933183a8c23fd50992a1ceb4410fe0961dd1b715d84131a4ff5de7e59fae9`  
		Last Modified: Fri, 12 Mar 2021 02:56:00 GMT  
		Size: 58.8 MB (58753799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5159bba23412a635e7dbfc645faa576f537f92d2abaa0e9d188965a78db51a`  
		Last Modified: Fri, 12 Mar 2021 02:56:36 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:67371218461743627b3d651ae87a54d278bf02302851f73bf4a3dd6edef95436
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53147631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1c29905e7b765d9f00e2daa83295d56d9ce7c43212a1fae6e0e93d31c81af2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 10:55:39 GMT
ADD file:be0444532eac39590c141ccfa52d1b344c0d211c810693d49ca4097a2d815356 in / 
# Fri, 26 Mar 2021 10:55:42 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 10:55:57 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:91a464b0980fed0c0cdac10a0067b2f7fee33fca30d4b13b011215700fb80fb8`  
		Last Modified: Fri, 26 Mar 2021 10:59:24 GMT  
		Size: 53.1 MB (53147412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5aaafdce3fce4144797817f76d6dbcc3d77684dfc39c41488fc08b3e77d3ff8`  
		Last Modified: Fri, 26 Mar 2021 10:59:41 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
