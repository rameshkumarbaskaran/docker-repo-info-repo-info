## `debian:testing-backports`

```console
$ docker pull debian@sha256:6aac253d9f09628432489514f5aed22ace275d19111ea1fa5188d5eda5fabcdb
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:064e2d5dfe6f0783de35e18471f1fbf425dc80278f6a4e451ce991921ae688dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49043231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:264feadf4da6aacf7ad28f3cd18f1e0d64e1aa248f0456f99c5f11699c191bd3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:53:33 GMT
ADD file:6d6719e60ccbf39132571a488cbe5e0237079ef5a236fda3a19dc7343fc34bac in / 
# Sat, 04 Feb 2023 06:53:34 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 06:53:37 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:57bcb44855e036a00082b63104a953f2e7172588e397422fc4db80abde25ed1a`  
		Last Modified: Sat, 04 Feb 2023 06:58:51 GMT  
		Size: 49.0 MB (49043008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d6ce2ee33c0cadabecc3b34ae52e8d47ca3dd23034884eb4d86595a8d75ed6`  
		Last Modified: Sat, 04 Feb 2023 06:59:00 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:4002f41284247f9c64990bcd89fc0ff034b73e63a931c9ab5535364f19387983
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47993471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7220ce7b48adcb510cffe423a1e94797ff3059a41a38c6aa8c82c458ff303f86`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 02:47:39 GMT
ADD file:98e47e6350976474e8c5ce450917a12c04e080ced6ab05eed9e04772c5728570 in / 
# Sat, 04 Feb 2023 02:47:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 02:47:47 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:01cdab3e0a4d64aa88c8c65852e4599d329659e9aa85a26d1ae3f1565db6ea9b`  
		Last Modified: Sat, 04 Feb 2023 02:53:31 GMT  
		Size: 48.0 MB (47993248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e542969ffccee238f8d18194c3c32fa7352b532da45e6ce9624db3718aa7a1b`  
		Last Modified: Sat, 04 Feb 2023 02:53:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:3380b4c029d9d23ae317710736da2f9727547d681075a81623a2e94da3dcb96a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46896414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ed7a2ddb7b48058c50196c303bd8e0ce9ab21619db48e213332b8d6da0555f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 04:03:03 GMT
ADD file:e265776b6b62da8ec73c72802a5f45c56311664fad279e039488fea3e773baa3 in / 
# Wed, 11 Jan 2023 04:03:05 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 04:03:10 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:eb7363eac3e82dfa1a2e2a380dd18728860c5f00a9451d64956ea62d0a97aa61`  
		Last Modified: Wed, 11 Jan 2023 04:11:04 GMT  
		Size: 46.9 MB (46896191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a65d0f618d512228f2c37f5bae4b7dd0cde0e4722621896b42e504f4b7cc08`  
		Last Modified: Wed, 11 Jan 2023 04:11:15 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:0bb16314a25ac70de6123f70d3bec337e0cfaa28a4ff12aa64af016bdfa4de64
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49081711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed9144778871673a506f483281b74ee61c255f41201c50723a17e9a05ba3a84`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:18:54 GMT
ADD file:45f2f09495aef8ab54f81db15f593e777fb18880028f3099dd77707a143d2acf in / 
# Sat, 04 Feb 2023 06:18:55 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 06:18:58 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d4637841f1417b168a5fcf6ae681705a2726c9ab1178d66fd4b8659b70a858fc`  
		Last Modified: Sat, 04 Feb 2023 06:23:53 GMT  
		Size: 49.1 MB (49081488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b96d3246d7bdd329a2aa74ab010e483380b9db0dc008acb940423693c77165`  
		Last Modified: Sat, 04 Feb 2023 06:24:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:4f8887f629002e963ec510c8b1ed08392464dde3bb09448ee448e44f61fc4931
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50093648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63cde2419dd8434c5743e075934069eec42b3eebed67bf173ba32f0c518e346`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 07:51:12 GMT
ADD file:ad17cd9a85b389575f6b3289675831e1173edaf33986260823441a61f1c904ce in / 
# Sat, 04 Feb 2023 07:51:13 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 07:51:18 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:661528ae13ac034793f44e59402c02c52f6728f6df010da9e53b93360a821eb8`  
		Last Modified: Sat, 04 Feb 2023 07:58:02 GMT  
		Size: 50.1 MB (50093425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c3fafc776e44bfcb3358bd3606e29200dfd77a4154935206a369d0466d7ad69`  
		Last Modified: Sat, 04 Feb 2023 07:58:13 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:54e79cb1c049d1763aa1ba0dad14497e88f1b7733089cda4dd82ee9f2f1b63c9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49041164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60706f6904c91bc4fd5cb15315cf5b68de64eae5c778402d3d009a8dbfa7b0f9`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:23:07 GMT
ADD file:a86d10831e490fd95df396c6c88db321817821efd0ff2e0866d6b5ddb1d0ee83 in / 
# Sat, 04 Feb 2023 06:23:13 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 06:23:22 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2663b89decf1b05f44b3c11d351ce9289c713772abddcb4215d45bed522886c7`  
		Last Modified: Sat, 04 Feb 2023 06:31:41 GMT  
		Size: 49.0 MB (49040938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5665f25f850928400c2438a167c360f579839fb967ebabbcac0beb70e4213a`  
		Last Modified: Sat, 04 Feb 2023 06:31:51 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:dd64c66212fa6c71b4f51b0ef826ba3973a7f2e43c5ced88d060916a3d88849b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54144138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d881f0032e812689381081155e842c744dcfbfdeae0caeb59c98da2f29ce2833`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 03:51:12 GMT
ADD file:f81974c52cc70632419a4bb9e1b0ebce34c50279cccdb80c4c55f25affd62354 in / 
# Wed, 11 Jan 2023 03:51:14 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:51:21 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5a076f88d4e3024706b03ea816ea1848f10b04e81272b548e79f552c7716938a`  
		Last Modified: Wed, 11 Jan 2023 03:57:35 GMT  
		Size: 54.1 MB (54143916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8645d03730215557c0d28075e647402154870ff46934875b407048bfd5147395`  
		Last Modified: Wed, 11 Jan 2023 03:57:46 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:8b316db32eb51d8b035aa9631cd8edd51421637daaf4e1dfde84019d4505df23
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47429925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739da72d284bb05e62815eb38fa84fa807a5edbb7005a9ce9a2379822d1ca096`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 04:07:20 GMT
ADD file:bc5ff0fc30abad7ccd04b372b80a22ffd8fabd60c0b4ddfa367dc841415fbc8e in / 
# Sat, 04 Feb 2023 04:07:24 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 04:07:30 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b0d4d83e89902e21b3d9b4ff69c9a54c6af1968d9820327767ffd6c6f44e07dd`  
		Last Modified: Sat, 04 Feb 2023 04:11:30 GMT  
		Size: 47.4 MB (47429701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b77f205684f5ea27f72fab73a22d60fdd4edf9300ffc6d5a5f788b07e3e2400`  
		Last Modified: Sat, 04 Feb 2023 04:11:36 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
