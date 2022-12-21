## `debian:testing-backports`

```console
$ docker pull debian@sha256:d7b332e597ca7900643eed406f707e757c5bbdd8d27644f591d372c2f737ecc9
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
$ docker pull debian@sha256:70553f53132c2d7f0993d8993ecea4dde4223d3281d7d44d6fb039007e43de18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50324648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097d959267ad4d8fa88eb378675173452e208092bfc6e6a4061539ae78d945a4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:21:59 GMT
ADD file:ff5fa70eb0a7068aedb937779779d17d7d63eee0d72da581f001a8f4091a497b in / 
# Wed, 21 Dec 2022 01:21:59 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:22:03 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:74d507d4af7a32f1dd119810020dbf55fc9518a701717445a793d1fc6c137077`  
		Last Modified: Wed, 21 Dec 2022 01:27:13 GMT  
		Size: 50.3 MB (50324426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c24b07c38ca32d2528e7f62d2d2f67c1d1c3d883d0ecb739bdd266ad618ab8b`  
		Last Modified: Wed, 21 Dec 2022 01:27:21 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:b6a78187a3852efa028abf8b8319a4e696334d58fcd9c41800cf1acb00d870f7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49285591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f3f4b3f4401c952522ac06af69e279f9fffcaa2d19feca52dc0e2eb5ff6c5f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:50:03 GMT
ADD file:b7b501b49f0c9e48466ce7338d0fd06daab1d0d79c969098f46fdc4e017111ca in / 
# Wed, 21 Dec 2022 01:50:04 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:50:10 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:42ab6c9b1941b45f7850197f0c66f60c64f3a6a720479ff8a40069adc913ddf3`  
		Last Modified: Wed, 21 Dec 2022 01:55:56 GMT  
		Size: 49.3 MB (49285368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b6222ec952f97005b9c23caee5183256bc0357388ebef240d0c6f5c2e862ac`  
		Last Modified: Wed, 21 Dec 2022 01:56:07 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:5ab5fdd42b7ee8e9715eb9673816fa66d57b316ee01067185595efee282e028e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47101498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:665aac10d1e249b528687669700ea6ba099060c5c4073263dc2fc42b3d50701b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 02:00:23 GMT
ADD file:2464d580ef377342093ea4da0745280f6d8fba2b913d8f3728bf125268e2065c in / 
# Wed, 21 Dec 2022 02:00:25 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:00:31 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:35b273b4faaae730a4309cfd0e073cfa7605d57066ec7dc0223010364de06667`  
		Last Modified: Wed, 21 Dec 2022 02:08:23 GMT  
		Size: 47.1 MB (47101274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe1010a70ea4c1c98419b91746d67668040a3fd028dba57a3e59bbde58d3a88`  
		Last Modified: Wed, 21 Dec 2022 02:08:34 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:531d592744a9b350532f3f4899b5ad06cac1c526bcfd432c350a8634f261b126
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50373028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce8e54506b8208e266c4ab6a6ac548397013e0b51386d476232b80650ee0b37`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:40:48 GMT
ADD file:ab6b87a9aaf2f8e8ec2a67e108e8a72b1c46a03e679e470916b8755b418dd610 in / 
# Wed, 21 Dec 2022 01:40:49 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:40:51 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5900a1826e0c77e1df02eecd788f48e6e41f057d996eb5659f98d3ae558750df`  
		Last Modified: Wed, 21 Dec 2022 01:45:39 GMT  
		Size: 50.4 MB (50372804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9aaddb6310a64678172f454c2451d0098de37b6c52aba7c3ae05df5b12f5ff`  
		Last Modified: Wed, 21 Dec 2022 01:45:47 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:518cfff5b2ce9bf7056007602800457902fc0aa36f676d644012fc128e9a6c57
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51363737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:231b3cdd267a0d29a90ffc828471d9d69511a0cb8a91a3cd9add7cc7c0b2fa2d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:41:02 GMT
ADD file:d991e45c94fa44a539a1a5fdfbef980c16b011cab2cb4197fd13c259a68ff614 in / 
# Wed, 21 Dec 2022 01:41:02 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:41:07 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c5fe1baa1ff5a4a37995fba395775466e48ac406bf23665a42cde4dd1e1ba4a1`  
		Last Modified: Wed, 21 Dec 2022 01:47:45 GMT  
		Size: 51.4 MB (51363511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28128f120cffd3a21d7b465d7315619991666c4cb263b8e6f243d55106eff29c`  
		Last Modified: Wed, 21 Dec 2022 01:47:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:a791edfe77bcbac554a24c6ad63240495f41ca53fd9b689211fc0de9c7aff904
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50336974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbcb6471465eee3c21095b46a9e5673ebbdbbd2efe84d814ac1d17aa9a8c5534`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:13:23 GMT
ADD file:0ea57818080c1e2a27e984470ee82b0bab064d2e4b4be6ca9d01d22a5809e021 in / 
# Wed, 21 Dec 2022 01:13:29 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:13:41 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9ca4c0ef78d0e2f931410fff75dce27a7514137f55186f813fab43dee045e67b`  
		Last Modified: Wed, 21 Dec 2022 01:21:51 GMT  
		Size: 50.3 MB (50336750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deef66fb7c7edf26847770ed5aaf0895d243ba7188a88fe333f07c0b706d9489`  
		Last Modified: Wed, 21 Dec 2022 01:22:02 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:2496a891fd3de654847a8b871d4e83c4b0d5bf9541a59244fcabc2cdc2e3eac2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.4 MB (54374071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a3af2cacf3a5bb06b49e26f4797afe4e7b1949038f2ec4d4a471c55f02bfac`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:19:07 GMT
ADD file:c58cc45feb60d65ccecf542b088f713fa2decc069cecaf0ff37bbca477c34ac4 in / 
# Wed, 21 Dec 2022 01:19:11 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:19:16 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2a152fa39f694f5032f5c8d0a519acb4cdafaf4169f0b86827d60fcd95708b5a`  
		Last Modified: Wed, 21 Dec 2022 01:25:23 GMT  
		Size: 54.4 MB (54373846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27485ef592734350f4a51c35679d38f5d41266df9e21251f5019aab13d59f177`  
		Last Modified: Wed, 21 Dec 2022 01:25:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:bb561ac1c5b692205199681877493cc231fb2b4e7f1902058b616fb5df6524b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48719644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c228845093b44a8091610c528fae160da1d4b5ff662c388bbf032bbee772e333`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:45:01 GMT
ADD file:de056ef64c072173021b31308d248f45e185e1b54cdb3c8c6803753bd5c0753b in / 
# Wed, 21 Dec 2022 01:45:08 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:45:16 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d0718090a9c33cfdb37b335b417262550f5588b94a1391c498785f8fc1e21804`  
		Last Modified: Wed, 21 Dec 2022 01:50:22 GMT  
		Size: 48.7 MB (48719418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421bffa79f09fc2b84c7db40b4fbc39b4ae5d007f660ba1fee725d7a641e4c3c`  
		Last Modified: Wed, 21 Dec 2022 01:50:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
