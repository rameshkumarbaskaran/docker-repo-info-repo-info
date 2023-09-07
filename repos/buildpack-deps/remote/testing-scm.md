## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:8d0c2b52853f23a22d2dc2524236f5037d1c41a56751a2d379733f674464b25e
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

### `buildpack-deps:testing-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a4dfd87847d6fa84c5002afc1b5768b7ba8b174e016e35eb542a49b14c029fed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 MB (134448146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6de79ce7ae844b70a9cf5b602b3104534e1ebded6dfafe47c136bdd6449991e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:23:27 GMT
ADD file:34ee641d9bad402a9422c8f96269ac2c74e06369bc362a916c8cdb087156bf70 in / 
# Thu, 07 Sep 2023 00:23:28 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 03:02:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 03:02:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e32a7bcba7c1847ff42b03e176da563d6447b045a6f2d5a9ece6acdce60297cc`  
		Last Modified: Thu, 07 Sep 2023 00:30:28 GMT  
		Size: 49.5 MB (49514761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df261e695bd837ce65c269e99eb1a12049f82c345fa073f411be6c5b6d7d3b75`  
		Last Modified: Thu, 07 Sep 2023 03:09:01 GMT  
		Size: 20.3 MB (20254789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54069e7c97fd71d1911c5424269e3102695ad98bc0a3de4b91415dc3e80fb6c3`  
		Last Modified: Thu, 07 Sep 2023 03:09:18 GMT  
		Size: 64.7 MB (64678596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:58ef84833f6f40d5c9265613e25ac370ea2377a4bb6de1ee4a641d5b87735cae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.9 MB (129944093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d440eaeb8ebe37f5bd260a4ce5361d5a8ad9890f8dfe4e266e6d886b82f1479`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:49:56 GMT
ADD file:d0da838ea8ff64a44e445dfb0001a4f6a2442085f0c0f942d0129b6f8054c7fa in / 
# Tue, 15 Aug 2023 23:49:56 GMT
CMD ["bash"]
# Sat, 26 Aug 2023 01:57:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 26 Aug 2023 01:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e6d8f24fa9802404161e1d0ef0d1db6d5f4c20cb1f0e5884dd191e1d77f2373c`  
		Last Modified: Tue, 15 Aug 2023 23:54:43 GMT  
		Size: 47.4 MB (47395127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f867d323ed66972b6c492120ce3fa78d7e1d63e0279362a9a55229db8e7127`  
		Last Modified: Sat, 26 Aug 2023 02:00:38 GMT  
		Size: 20.3 MB (20250269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9dfbc5e6b18e516ad072378c62dcfa42e9981f0925b16c44303b5c7f6424eca`  
		Last Modified: Sat, 26 Aug 2023 02:00:57 GMT  
		Size: 62.3 MB (62298697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f33c8e96705c40209ee56dd09395a9ecb5b713a223dad78a41f6dc954a02c144
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.6 MB (123566268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4c450fc305174f9eb7d21e13717c1d3512ed305729d8775f1410a84fdab7814`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 01:00:27 GMT
ADD file:56aa0cd11d12862eaf421a2ff6a2a518ae07f7d6180a2f0f58a9d10930215950 in / 
# Thu, 07 Sep 2023 01:00:28 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 01:42:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:42:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cbe28254d81156b7683ab6feb96334538a6b59d12717973205a1077d3bcabba5`  
		Last Modified: Thu, 07 Sep 2023 01:06:54 GMT  
		Size: 45.0 MB (45010494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbe3001385a2b717c083b0eb81363b8210958afe6ccf0dfe6a62a78df022ec5`  
		Last Modified: Thu, 07 Sep 2023 01:49:25 GMT  
		Size: 18.6 MB (18600941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39960ddda116bc7eddff9010f7bdc11c97332a0ea990a5a7e825d0cdcc2868a`  
		Last Modified: Thu, 07 Sep 2023 01:49:43 GMT  
		Size: 60.0 MB (59954833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1099c74a36aa3e7994816236eaafd33977cee3e8856f0c7489006a4113204ef1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134198876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690f08e5887bba5afdddc9f0866feaa0fed5ee90a92507fde699e7721764e317`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:41:42 GMT
ADD file:16621389c05de9ece6b8d40e6c62ca81465940296cc58f7f1c56571fac05b33e in / 
# Tue, 15 Aug 2023 23:41:43 GMT
CMD ["bash"]
# Sat, 26 Aug 2023 02:57:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 26 Aug 2023 02:57:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c5fc9f67522f8eb1fc65844ccc91e1d93595f85d410842d334c85f7e0a15d841`  
		Last Modified: Tue, 15 Aug 2023 23:47:22 GMT  
		Size: 49.5 MB (49521978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:392c849b78c27f87cf11f7bfc3a6c274880955ddcf718ceae8fe425a331d69fb`  
		Last Modified: Sat, 26 Aug 2023 02:59:50 GMT  
		Size: 20.0 MB (20038140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d90315047ca31a048692ffac9ca9412c3013153dff0ae8d9d7fa6d3dc5fc787`  
		Last Modified: Sat, 26 Aug 2023 03:00:07 GMT  
		Size: 64.6 MB (64638758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:31878c48a551e60acfe2aa68406016be01f64a82e69b53d72d0ee701a6f32cbe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137871241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a958d70d6528e570ffe292108ab492680225ccec8f02c354a108b0551e4342`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:41:44 GMT
ADD file:5d53bf28b6cbc8eac8124a07c0bb8e04ee2d0c8989a8b7219612f6ced4f064bc in / 
# Thu, 07 Sep 2023 00:41:45 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 05:35:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 05:35:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1e0d37cd24f690f803c53e61b67871ef6d1dd8980331679da74a8059a191a9fa`  
		Last Modified: Thu, 07 Sep 2023 00:49:00 GMT  
		Size: 50.5 MB (50534548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b76d6a16699dd100cc2549b60405a4d0d78dc30f81cc263bee0da056e922a5`  
		Last Modified: Thu, 07 Sep 2023 05:42:45 GMT  
		Size: 20.8 MB (20840661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc12640afdfa7cf01b8781ab7883502fe26134031f798e3a1391eb3c53ff9125`  
		Last Modified: Thu, 07 Sep 2023 05:43:08 GMT  
		Size: 66.5 MB (66496032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:046462eed28745d1caadd54b9dda3bc4b442d35bbd759eb1657dcacd290ea312
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132549205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b26e1bffc8263b56c40daf67e3080482d2c74fb716bd092b220df4286228a706`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 01:15:52 GMT
ADD file:83fc4a798915040b0cd8aee9a3ff972cb051d033b36a5b578933e29e1b55dc9a in / 
# Thu, 07 Sep 2023 01:15:58 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 04:11:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 04:13:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2b910e4082f491e2e9e9e85a065d99a76c730b5911893631d48aebe5740c1e71`  
		Last Modified: Thu, 07 Sep 2023 01:27:12 GMT  
		Size: 49.4 MB (49357507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9d654b3c49c164cc43a4683b85bf2e1374ecf02ddb2c3f7187cfd204ec3309`  
		Last Modified: Thu, 07 Sep 2023 04:30:10 GMT  
		Size: 19.6 MB (19559687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8decd0a052b38d92ca1b1753f6ddbe6c1df433473ed31f5705fe4bb91479355`  
		Last Modified: Thu, 07 Sep 2023 04:31:01 GMT  
		Size: 63.6 MB (63632011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7b32a345016b781e47dec28c46825f7da2036dd83c3ad1ad4da3ad69b0dc01b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145281887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a1d2b38ee31b2b6245fea316fe55669c11a884ec021e8c04497ae91f1609ef`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 01:12:56 GMT
ADD file:121000b06bc7b1fdd1e3c87b4b93debc6d4ff153c7e305f8fb9fe076a52c4ccc in / 
# Wed, 16 Aug 2023 01:12:58 GMT
CMD ["bash"]
# Sat, 26 Aug 2023 06:49:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 26 Aug 2023 06:50:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:aa279ce1030b6b03f549d223eeb76ece36944bfb3a79e0a2758b54fcadc346bc`  
		Last Modified: Wed, 16 Aug 2023 01:20:59 GMT  
		Size: 53.5 MB (53544042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330f840446ff0bbf07de565959e01855c0e142613b5f006ab2f5cdc4e09b455a`  
		Last Modified: Sat, 26 Aug 2023 06:58:44 GMT  
		Size: 21.6 MB (21603708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8fe9c71703a01801c5c80761bf60bc5b1022d6b71cc118df1566ef403d28b3`  
		Last Modified: Sat, 26 Aug 2023 06:59:18 GMT  
		Size: 70.1 MB (70134137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3153912f470e6f219f1573347037607b8e81fbccebee62687e23ca51e0e949f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132592718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb32cd1818329edfddb10d6ffbe980fc8bb2beb29bed3e7c591f60dd2ba2689`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:47:24 GMT
ADD file:85c1414a9b16cd9b51c31b6e346dff8675b8a78ca36b9b6e41fe6711444ec72a in / 
# Thu, 07 Sep 2023 00:47:27 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 01:16:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:16:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:020f83d738584194c53a58d8f6c431413868b7fb51d9873c9bc0e26b4292e8cd`  
		Last Modified: Thu, 07 Sep 2023 00:52:16 GMT  
		Size: 48.6 MB (48573746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c6a12ceebdf73872641b973e28cbc96d9146f8098bfd6cd4d37ad06255121c`  
		Last Modified: Thu, 07 Sep 2023 01:24:56 GMT  
		Size: 19.9 MB (19925579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb9a0498809282410280aaa414903e32de7d35875c64b8c0cf8bbd99ad0d45a`  
		Last Modified: Thu, 07 Sep 2023 01:25:12 GMT  
		Size: 64.1 MB (64093393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
