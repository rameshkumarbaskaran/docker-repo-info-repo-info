## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:cbe12ae000173a703fc39a26b28806a84000e95e96d9a5cda1d15cdbda0c9cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
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
$ docker pull debian@sha256:29223aded45ca92f12c719970ab5c42aae68df83c46b39093599cb42b41486ff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54927907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3a1c5e40069f9ae82d036fbec723047f7c89665eed6244e956958fe7d03667`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:22:25 GMT
ADD file:d05a14b1e57f9cc8eeb316a843403bbb35176d6222d60d6ddbb34faba977e316 in / 
# Tue, 28 Sep 2021 01:22:25 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 01:22:29 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:df5590a8898bedd76f02205dc8caa5cc9863267dbcd8aac038bcd212688c1cc7`  
		Last Modified: Tue, 28 Sep 2021 01:28:33 GMT  
		Size: 54.9 MB (54927682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dae4a85b0ed46e56c415e3482da8fa633a8f47b0e007309d77252511c600ef7`  
		Last Modified: Tue, 28 Sep 2021 01:28:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:96d16fb911e1bdb4856c459a8344f9aac828f8f0b53368378aad6732ddd19e05
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52452426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c79f29141f679338338bc53354a1416ca2cd20ca9a726ef8ee3814657bee44`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 00:49:54 GMT
ADD file:b9969604315238de271e1769a4b8dd85cdf0d33f9fac387e940d5195ac3030a1 in / 
# Tue, 12 Oct 2021 00:49:55 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 00:50:12 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a97c782f2538791984ce12c859cada96e395e3950d4cb7d1238e08acd2eb74ec`  
		Last Modified: Tue, 12 Oct 2021 01:05:12 GMT  
		Size: 52.5 MB (52452198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a06514d4dff5ba89305dc9bb3d0e5da4e123193ba836b6e5b172d0c5859cfe`  
		Last Modified: Tue, 12 Oct 2021 01:05:40 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:b25dedbb396dd85738891aa1979bbbd95ac5730760bb2341c51ff8c08b976855
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50128218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:064d051c6b9394f3b1e73cc6287ed72273afc824fdf8327ee18143e5963f21de`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Sep 2021 18:02:22 GMT
ADD file:115027696fb1d5399fef64911cc256fcf5562dda4edb505b3dd4123c432dce15 in / 
# Thu, 30 Sep 2021 18:02:23 GMT
CMD ["bash"]
# Thu, 30 Sep 2021 18:02:39 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ca892bcf1f9684aa35cc7f69492753430648a330f879d42dac2b69a9ac5292a2`  
		Last Modified: Thu, 30 Sep 2021 18:18:38 GMT  
		Size: 50.1 MB (50127990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aed33a6596980fe469cd51dbe80e25d86500951fdbb4d04723a8f1a93bb0b7c`  
		Last Modified: Thu, 30 Sep 2021 18:19:02 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:90c53c04603b72deaab03b592d9011562b4123e08ef8d443921ffcc7cac75cdb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53613823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba1d8795ddff6749cdafc85666fb057aafbe14501ca04c5a08a06c587cbd4a99`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:40:26 GMT
ADD file:08680140d1528c796f24dc7d0f5a83fa0ceb307a1d5da1e6ccef21471d975cd9 in / 
# Tue, 28 Sep 2021 01:40:26 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 01:40:34 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fa98001816c83c32d601f854ff21729167d2205310fcab15f8f9c26bdf6788d7`  
		Last Modified: Tue, 28 Sep 2021 01:47:53 GMT  
		Size: 53.6 MB (53613599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55bf91a68aa3eeda16c1c42c39c000114a33ded2617eee358755a1184bc76a5`  
		Last Modified: Tue, 28 Sep 2021 01:48:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:f359ef240325e492797a4bd627333a752101ddc5ff983facbee6b299db74d8dd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55932463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aed41a0d70b57cfd9280c8ad50ae9a0a0cd13bf5d04d07e9ff72eb8d1399b73`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:39:47 GMT
ADD file:a666560999115997edd232185b410db82d88832f98f754ee331f505de6fca72b in / 
# Tue, 28 Sep 2021 01:39:48 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 01:39:55 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fdfe255b6e1e8f9836f895e8f412f81c3be9ff0081a6e681c62b3bd736c4118a`  
		Last Modified: Tue, 28 Sep 2021 01:48:32 GMT  
		Size: 55.9 MB (55932237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648b8798ad6d5a39fcddf3eac777c7c94924500830b0f77145faf04a5f71bcb1`  
		Last Modified: Tue, 28 Sep 2021 01:48:52 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; mips64le

```console
$ docker pull debian@sha256:3319415597cb58bbf2de4416f5ce8d1ee5144ea01e457dfaef7095341e3869f1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53178045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ffa490dc24483e1a7f4ee3bf595a511f9edaa6259dd4e34419be663de4efc2b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 02:10:05 GMT
ADD file:fa139347f50faea85a5b3b4670c35cefd41b93de492dc47fcac13844e6ef3fa7 in / 
# Tue, 28 Sep 2021 02:10:06 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 02:10:16 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8238f36a9a08cb584f6fed203a421c1179967398b18223c38b40a04204650099`  
		Last Modified: Tue, 28 Sep 2021 02:20:00 GMT  
		Size: 53.2 MB (53177818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6189566a78d12b6dcc52028012799982f3f011e91965eb66cfe4d803682a1a24`  
		Last Modified: Tue, 28 Sep 2021 02:20:18 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:020dc431c83a6e588f2ad5acc705f2b685f2c5f432479d6b3ef8ca3c3b8363ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58819474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c625ab43ee412782d349d5f8b79dc94144ff757bc9e6ac0d8d4b995f7682c2d3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 04 Oct 2021 17:54:17 GMT
ADD file:93d3870bae0f248555dd980b0ace97ff93346d3ff1afe9b1d5af8841cc49fcad in / 
# Mon, 04 Oct 2021 17:54:23 GMT
CMD ["bash"]
# Mon, 04 Oct 2021 17:54:41 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e36f639ee9b1930012e80af1c5b20beca48e17fbd629e9b6df4137425a6da2ce`  
		Last Modified: Mon, 04 Oct 2021 18:06:52 GMT  
		Size: 58.8 MB (58819246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac1445fbf3ce0260db964eaea6ded7fada4a82787f3702b19e3e0e57cd9b08c`  
		Last Modified: Mon, 04 Oct 2021 18:07:15 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; s390x

```console
$ docker pull debian@sha256:b197bc5c4de0dc464c4e04dc9afc53a974157b59b36c5eee0ed80b8994feb7e5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53193120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:194a980937758b4f99a072dd0852f765701e9b001b176f5ed422ba5a9a89e918`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 00:42:09 GMT
ADD file:a7a74f6be757ceb5e84c440e739019782df1a118264eef70aa49886a976c43f6 in / 
# Tue, 12 Oct 2021 00:42:12 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 00:42:20 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:081299fd984cd296112766e1cc55f44fffbf898b2900b01c0333962494a2dd80`  
		Last Modified: Tue, 12 Oct 2021 00:47:43 GMT  
		Size: 53.2 MB (53192895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659e14461d58f8fb62b8e8f7631205eb1ff6eea842d61605a55232b8583d46f3`  
		Last Modified: Tue, 12 Oct 2021 00:47:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
