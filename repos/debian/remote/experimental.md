## `debian:experimental`

```console
$ docker pull debian@sha256:fac7a314d132a43510f7bf124ef07b058953d0c4507a4e8027299b823eb8c981
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

### `debian:experimental` - linux; amd64

```console
$ docker pull debian@sha256:c3c489139dfbf095085247562b0a17cba9656eb395dd86821485bab3578aec87
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52247047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c9ba25194d4f03f0a863126acc26fc25cf914cdbac0d902649a290fc205dbd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:23:30 GMT
ADD file:a15103578eec126916f03fcffc30fc68c2784ff4137ab891659c15c648ae0458 in / 
# Tue, 19 Dec 2023 01:23:30 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 01:23:44 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:ac1e917d2652641c1443e5c509c042b31a6e06c85f5a4d97796b4212c9cd049e`  
		Last Modified: Tue, 19 Dec 2023 01:30:10 GMT  
		Size: 52.2 MB (52246825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc5401ae9c8d8003f3e684b1437f469200194a438d4b2271833468448bc8bd4`  
		Last Modified: Tue, 19 Dec 2023 01:30:32 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v5

```console
$ docker pull debian@sha256:707cf00330e59ce5e1cb9acd55078800b6014af51fbda859bd43486532d073fa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47266286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:197c2e61f19d5b57c017a3ada9900a15f8a4ab511cbe61f9a776e8edb5718fda`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:57:05 GMT
ADD file:1ad4ce430c88442f1130f70b99ac8bb1c7b6ca2b6e72cbaa4d28e1387cd20864 in / 
# Tue, 19 Dec 2023 01:57:06 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 01:57:14 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:0a7a3869a18520688e4e53f422d45f34a4c34a812d80cdc1e982179484d53019`  
		Last Modified: Tue, 19 Dec 2023 02:02:44 GMT  
		Size: 47.3 MB (47266066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fee0673b2e926a8083b537be16cd967213522133c50c2048008e3c4b0af0254`  
		Last Modified: Tue, 19 Dec 2023 02:03:06 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:6cc2df07be03c77387ffc0c3326c5638fbbd9c0d4c49e8543619c29867a3a428
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44844227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54b48e13819400565bd72d93bc3069ac76c065dc3f0f0605b02a6348f5aa1cfa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:00:15 GMT
ADD file:8e091f00e04d8cb85cfce52bbabcbac6c260e95c3f3a00752186e465f583b2ca in / 
# Tue, 21 Nov 2023 04:00:15 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 04:00:27 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:bc7b160f4eb0bdcb6d980297d91f215375ca0669f74456162ed2c3a6534ceddc`  
		Last Modified: Tue, 21 Nov 2023 04:07:09 GMT  
		Size: 44.8 MB (44844006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a69e60ef4d54cab41871e2cb5a7bec428aea9ce83d55e58fff0dee9198f58e0`  
		Last Modified: Tue, 21 Nov 2023 04:07:32 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:7ac54b683197b79aaadca21cccd9b4d99c008ac83332e2701571216306bbc383
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49690032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f395af462003e1e25af91cd8d9cb504b81f3c270a4ec07186bdb125df022f3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:43:09 GMT
ADD file:ba5dd365f875207e1dd5cf456a6700fba8d9523bdcccadb14783bcd1ebdc1a8c in / 
# Tue, 19 Dec 2023 01:43:10 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 01:43:18 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:2aab20151d2b9073aa22f609ec58666e04cbdaba4d6482dfc7b6cbbded98d393`  
		Last Modified: Tue, 19 Dec 2023 01:49:23 GMT  
		Size: 49.7 MB (49689810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23778b90b7e9176dcefef10573d5c79fb7fe3212c92d0cdea26a09225cf9ea60`  
		Last Modified: Tue, 19 Dec 2023 01:49:42 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:b282ca696fad9a440c7f53da0b166ddfc4ff176022ea89bee6fa59431fd05f1c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50559480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00dc49934329a988456e0f9b19a1ca6ed44c6ea9ad48c1b3039889e7011136b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:42:12 GMT
ADD file:c306ca084269bac3e73eca11b9cf1fde32b2438ef4a2daf50aa7d796a583b727 in / 
# Tue, 19 Dec 2023 01:42:13 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 01:42:25 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b251e852034d95763dad2b2bd66c9c9046c09adac90fa5b77002410e77e32ca3`  
		Last Modified: Tue, 19 Dec 2023 01:49:32 GMT  
		Size: 50.6 MB (50559261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83592bf926afec21b96646cdbdda37310bdc738d957dc6b99bd14e41f4d63c86`  
		Last Modified: Tue, 19 Dec 2023 01:50:01 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; mips64le

```console
$ docker pull debian@sha256:ac3424f8285aee17a00a654ec7dde3bea039e6c5ebc497b154bff00be19800ef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49342071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d1e922c701c25bf651d83210ea4fe69259140b9ad07101bb3eb0ab2af93972`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:17:31 GMT
ADD file:32388f25898c590557e184be8d1a25de1c8d0d46118ef57a0a76b0c893108d41 in / 
# Tue, 21 Nov 2023 04:17:36 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 04:18:13 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:e3dc12456ffa080d32be43a02cb6024e94ce186c09ce60151090c1296700a438`  
		Last Modified: Tue, 21 Nov 2023 04:28:44 GMT  
		Size: 49.3 MB (49341850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce08a81bc78ed1a698eb461ccfcbed917c55142347a46fce41f97411329887c`  
		Last Modified: Tue, 21 Nov 2023 04:29:22 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:363296841e6bbbcf0f0f360d0e5975cf3d4de993e576d6084aa7812e1f58902a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53455919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de49033379b62fc7d8367d1d79ed602e018b3ff36cec525d55e10fec5e1314a0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:24:40 GMT
ADD file:0af0381b54263356d67da658e91aa4daf9a7626ec1eb50937a01f950c70269ae in / 
# Tue, 19 Dec 2023 01:24:43 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 01:24:57 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:bbd2991f9801d49e2e978fc288252c5eb7d6e502ce66c9ba0d1bec7394a94f99`  
		Last Modified: Tue, 19 Dec 2023 01:30:50 GMT  
		Size: 53.5 MB (53455698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b07a8dd4ef570b865cb61683551cacc9daff3728e5e2f63ccc1a7cad5fb942`  
		Last Modified: Tue, 19 Dec 2023 01:31:14 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; riscv64

```console
$ docker pull debian@sha256:1e72d63906b9a8c4d0a64ed1e98c02cf05a02268f3e6fe285b8ca0a325aab6dd
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48206923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:013871bd9721543bf4ec97e375d9c2223b75834ecf613fa142e2035ea46d9b5b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:10:08 GMT
ADD file:f926dc89ba0815e0a23356d88037340957f7a57bea917a3aaed678d1decf7b22 in / 
# Tue, 21 Nov 2023 04:10:10 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 04:10:48 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b1fcc4091b722aae5f7f102ced62233745368e2095d318f03282cc819757f97e`  
		Last Modified: Tue, 21 Nov 2023 04:13:22 GMT  
		Size: 48.2 MB (48206699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60afd7f2b0f8844688b4d838bb33218c480848fcdfac7245abf07bd96e9286dc`  
		Last Modified: Tue, 21 Nov 2023 04:14:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:43a5891c839c84d8f00810d182dc7deedb90f7501e016622111a2e517e4f59b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49328408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2197ae7fd96dd8061f82064e02169216990665b0b1692c7e6a5cca87df3db77`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:46:00 GMT
ADD file:eb03e79389a9a1f4792c7626177965861c32abc4748916db20ba724280d5f823 in / 
# Tue, 19 Dec 2023 01:46:04 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 01:46:22 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b28c9c2dc4e251d259f8365924ee2d21e2009c71547be061b371715dc3b1a975`  
		Last Modified: Tue, 19 Dec 2023 01:50:24 GMT  
		Size: 49.3 MB (49328190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929b7667049be57c42cf6e22296c8733c1f0232829d20ef83ab5fa4f6e9b037a`  
		Last Modified: Tue, 19 Dec 2023 01:50:38 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
