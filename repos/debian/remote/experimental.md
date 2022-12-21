## `debian:experimental`

```console
$ docker pull debian@sha256:50d4e88c4660e69fd18b30ae62669bb524b7e4a5cf55a2947d4366ac4b08212b
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
$ docker pull debian@sha256:7a1476cb5d50760af94ec91147e23a865797b6762caaf6ed08a180071fc98e1a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50286364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2ebb359d544dccf7850b4e655a3458516ac5382884dd206a7e82540e5e4721`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:22:19 GMT
ADD file:2e535e63bcd92d216719e2afbec679d7b5dac2f0f40f1bf560384525e241f551 in / 
# Wed, 21 Dec 2022 01:22:19 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:22:31 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:41739a274d315a12e71ab28ec3459a8fda61a9b4d41c5e4df45a31239295ed03`  
		Last Modified: Wed, 21 Dec 2022 01:27:48 GMT  
		Size: 50.3 MB (50286145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661158614aeb4d4d8321431332bcd42ca17eb8fc3a30c20f16223d7a3e941051`  
		Last Modified: Wed, 21 Dec 2022 01:28:09 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v5

```console
$ docker pull debian@sha256:ffacf0204338f6edb929939225c1edd35c5593f6de984a5a27392198d684ac83
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49271005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a99df999e0cbf33742e79aadbf3ecffd1c3d15961fa70c60137a4d73930691`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:50:29 GMT
ADD file:bd3e1e6733e15688933fc4c5990756ca231320c4976e87768f9a97917815bbe9 in / 
# Wed, 21 Dec 2022 01:50:30 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:50:43 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:bd2d9851e83eaba372def1b56412f09d95c4bd7c16c66b9ff0b31370e4abe8c7`  
		Last Modified: Wed, 21 Dec 2022 01:56:39 GMT  
		Size: 49.3 MB (49270783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28f5e9347940c7bf00a12c6b749f87c69297adbca2d7cb54efb17601387ac2f`  
		Last Modified: Wed, 21 Dec 2022 01:57:05 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:442c03e9bffb0955bbeafeb851073d4b11ce90034433edd8516f1a6866e698e2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47080907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857c22df76842a82ffb908543b5005e390469a0a147333e9694f14d5b8fd018e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 02:00:53 GMT
ADD file:930ee3b81511945e2edcb3a338f86509cc60ea700a56fbcd07cc50656542dcf6 in / 
# Wed, 21 Dec 2022 02:00:54 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:01:09 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:4f2eabba05374c21c57c8a7a2273ec974af5f0a843cd07b34fee8f5d01d8be04`  
		Last Modified: Wed, 21 Dec 2022 02:09:05 GMT  
		Size: 47.1 MB (47080685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c5a03ffd20d362f94e11512751f84da17118c4c8b0a0cc7b4de5481b4666d8`  
		Last Modified: Wed, 21 Dec 2022 02:09:37 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:a1df7cda5ce746603f096db651c81088ca665e856b46823db42884c9e6b0c98d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50336201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09eb7f72eddc257dd155c7b2b6016efd97e61fc52abee1604c0fdab3e63d5dde`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:41:02 GMT
ADD file:a226780420eceac6d107a9e27b148b1f4ae3396a64b7996b99b41ac721b2a68c in / 
# Wed, 21 Dec 2022 01:41:03 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:41:10 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:8288dccb04ed332f650a89d71ea9b881fd9f0b7fb6b12d8e574ee9e53724705c`  
		Last Modified: Wed, 21 Dec 2022 01:46:11 GMT  
		Size: 50.3 MB (50335978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:118a381ec63cb794d3312b1a873ea905a271d34dd3bc57aa553a9197dfee6b97`  
		Last Modified: Wed, 21 Dec 2022 01:46:30 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:d98cbd4e3851de3c2dc094691d2264adcb0d89f80bfa0747256938978e728a2f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51340351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77fadace25ec54d4a429fbe7cb9f33ae821376a6f43d1af439aa2e050504b7c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:41:25 GMT
ADD file:6ffac3795480c354a83ea1968885ebf1616928a69fa293f4011e2f7613766fa8 in / 
# Wed, 21 Dec 2022 01:41:26 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:41:40 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b614aec88bf425675376d4c25f6a3f9d7c7e9b6d631307ea564765270b6f8c59`  
		Last Modified: Wed, 21 Dec 2022 01:48:21 GMT  
		Size: 51.3 MB (51340129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b74b9e33a0be187b745c8b6e9d6fc5fd1b2197f09988ac4195cb8441a0ea2de`  
		Last Modified: Wed, 21 Dec 2022 01:48:45 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; mips64le

```console
$ docker pull debian@sha256:f9e06349289968e72b817e9fc0511a6059db60d427232035483bc8059c0f0fea
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50293171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a75a28d29ae62f6c840a5af603020882890c8196a724cb963db47c3805b6d22c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:14:36 GMT
ADD file:d86f0e28d7ea72ca80aec16cc53a8efebf43b4802fbbed1b6452a0730f13e73d in / 
# Wed, 21 Dec 2022 01:14:42 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:15:19 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:c1a8c1357338f60ee5392f4bf29f089ea8ef5e17f25a0a3f49fce091aebf025f`  
		Last Modified: Wed, 21 Dec 2022 01:23:08 GMT  
		Size: 50.3 MB (50292947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20db7e5faa75df970592e05e4ee9d6d361a077f5366dd189fd1c1647b5386cc3`  
		Last Modified: Wed, 21 Dec 2022 01:23:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:d13786dbd0794f96615d49d73460d1758b68638789e62e39e91c00f264e180ba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54333208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be450ff8289b2ffa2f6fd60a6fea7cb75b0de56f30069c462563183929fa278a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:19:45 GMT
ADD file:612c98671138c70184edbcfb1f44b94a372b37b35f1c8dff90447173af466a1a in / 
# Wed, 21 Dec 2022 01:19:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:20:09 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:ca12868e5e41d7731e085119b02b75faf07b2b4658b7358f856ec9071294c19c`  
		Last Modified: Wed, 21 Dec 2022 01:26:12 GMT  
		Size: 54.3 MB (54332988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e0c38f047a733206800328e3128eea83c8be7aa2833a96e617ee463866bac5`  
		Last Modified: Wed, 21 Dec 2022 01:26:42 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; riscv64

```console
$ docker pull debian@sha256:ba5cb019da23d5fa175c5e0edbf7358d27e05768ed3086bc9945890bc808d178
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46453774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e89a88090721ab9591f082335fa251eb936435b61c5ad32822be7ac5c4e132`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:13:00 GMT
ADD file:27d33d404549e4270b8c18ff79b55c32563a2158aefa90426337e47b36c81041 in / 
# Wed, 21 Dec 2022 01:13:02 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:16:17 GMT
RUN echo 'deb http://deb.debian.org/debian-ports experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:90f749bea8c8145751b0e1cb50ea7f16f0f18855f572fb4f1ffe67ceb9d6d7db`  
		Last Modified: Wed, 21 Dec 2022 01:30:24 GMT  
		Size: 46.5 MB (46453544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ee7be808be18abe9a9090f32b38245347c9e366a0d55cf87411793a86c61c6`  
		Last Modified: Wed, 21 Dec 2022 01:33:22 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:636d263bddf9018ea3de2a5bfaa8e9d0148598a0898f9cf30b8690f6914916af
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48679736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:553d10249deb35becf98c49b5d9f080924cd6fe45b46815fb8fbde4db344a4a6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:45:52 GMT
ADD file:2cbc80cb1fef4f42388c8874c6db608ed9b843ab21b7a1da11032a641818b603 in / 
# Wed, 21 Dec 2022 01:46:02 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:46:29 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:780f809d6eaf77c1f25f0beca6284b3b526f717f47303c18899236630d7927f4`  
		Last Modified: Wed, 21 Dec 2022 01:50:51 GMT  
		Size: 48.7 MB (48679511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34d55b822f639fbcfe9183241d2fa88ac52fd34697baf0367806559d005dacf`  
		Last Modified: Wed, 21 Dec 2022 01:51:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
