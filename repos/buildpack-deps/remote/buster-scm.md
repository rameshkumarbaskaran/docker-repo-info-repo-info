## `buildpack-deps:buster-scm`

```console
$ docker pull buildpack-deps@sha256:08db31ec9162ccd59615dbf55c2eca0f88580f909096f259e7f5845cfb708ef7
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

### `buildpack-deps:buster-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:fb2d0990619ed3dc6203f8be4953146175b28e4d5462a08a79a31a7284097969
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120109523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0167bfe7e2deaba2bc8b079ca60aef2926b5bb3937e3744a7d678b871055c263`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:22:53 GMT
ADD file:be998d04a8927e9c4b105995e3b9d6800ea798807389f7c5921c0f4774328e21 in / 
# Tue, 21 Dec 2021 01:22:53 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:53:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 01:53:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 01:53:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b99af5931b39ce167150ad668cfa57ddf7664697be9996cb7e0e6aebbf05843`  
		Last Modified: Tue, 21 Dec 2021 01:28:07 GMT  
		Size: 50.4 MB (50437136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6013b3e77fe6fd3dcf46a05f8e5b3afa9fbca7ba0161c62e56beb4058334dec`  
		Last Modified: Tue, 21 Dec 2021 02:02:46 GMT  
		Size: 7.8 MB (7833863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbced17b6899896c8e4016d62c885d737fe667acace2733e17c64bb974232887`  
		Last Modified: Tue, 21 Dec 2021 02:02:46 GMT  
		Size: 10.0 MB (9997172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b609dabefa83fae157bcd42123a8ed45199bb6c301e09a11260c1cad9babfef`  
		Last Modified: Tue, 21 Dec 2021 02:03:05 GMT  
		Size: 51.8 MB (51841352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d0d0e6dcf3dd93bb03a9b5dc8cf890312928e1b114be03356f8c2156c413cea6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114794268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b887b73a84ea0722eb93dbefdc2a8a48d37d1d342d6d6e61f9297f82fe7621`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:50:59 GMT
ADD file:f13b1e11ddbb56252b3e6e03b983781bdb18391decd8e7fe849d9ef411ee19d2 in / 
# Tue, 21 Dec 2021 01:51:00 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:58:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:59:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 03:00:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f72054d57c0f356b780c117a8b1bcec66a89bbe239433df38bd1177b987f011d`  
		Last Modified: Tue, 21 Dec 2021 02:06:39 GMT  
		Size: 48.2 MB (48154368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c6d242f1f1540fc8e353628dfd119de23a8fcbce3b678d1d01633c0c5b278b`  
		Last Modified: Tue, 21 Dec 2021 03:21:37 GMT  
		Size: 7.4 MB (7377197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790ff822382a92816aafd7ee78dd6f3ae04d685e84252cf9a0ad2d8b19baa951`  
		Last Modified: Tue, 21 Dec 2021 03:21:38 GMT  
		Size: 9.7 MB (9687552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:644113c206cc6c90bb22e9e00ea9f578ac53dac6b843e1dde5650a768b153ab2`  
		Last Modified: Tue, 21 Dec 2021 03:22:26 GMT  
		Size: 49.6 MB (49575151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:cd0a580d9fd5df902f04293e518beddb4d1175f9db022d33d7a363a59f305d30
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.7 MB (109743475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff4b20e90e29bbd5952ec4881f335298c33a3df43a7b1c4024baaf3dbba374c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:00:17 GMT
ADD file:36bf5b8bdd9066b06cc35d26df3f4dad2b1cbcb41985b85f070ed97a3e85f8a9 in / 
# Tue, 21 Dec 2021 02:00:18 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:49:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:50:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 02:50:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:328389035fdd79ece4f520541a84b3de974050fe012ed1566da6b869dd34ea29`  
		Last Modified: Tue, 21 Dec 2021 02:16:11 GMT  
		Size: 45.9 MB (45918102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80397c5626b1d4e58b7b7dd9219674dd86caa03ddcaac1d3d6791189a44b0ff`  
		Last Modified: Tue, 21 Dec 2021 03:14:47 GMT  
		Size: 7.1 MB (7125168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816c475148f8e55cc2b8593f29d0ddd67ad1359f3c69061f043d461495bad179`  
		Last Modified: Tue, 21 Dec 2021 03:14:48 GMT  
		Size: 9.3 MB (9343808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d30bc5ea112783bdcbfaba962b58338c0f61b12d68a5cc7474c0b639098c6a`  
		Last Modified: Tue, 21 Dec 2021 03:15:32 GMT  
		Size: 47.4 MB (47356397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d960df5afa6b3c223913083b6b7b4f7522b85a805400c79b7840fe8bad6dc1d0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118854359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:809ba71d793dd0bf303a81a8ae0c046f5bb58a4871d69c68996ce0f7eac1de93`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:34 GMT
ADD file:73bd5e773b257a6ea5d29845b2b112ebce468878a9467e7c0fe61c69994bb47f in / 
# Tue, 21 Dec 2021 01:42:35 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:13:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:13:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 02:14:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:741eb94195433e00f9799629cc66740c97d607d6f3ed207e5738995897c52959`  
		Last Modified: Tue, 21 Dec 2021 01:49:16 GMT  
		Size: 49.2 MB (49223144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d098cf33298807975a4d84f59f6689e0bf729b62fca9b7320adb80ebeaabc578`  
		Last Modified: Tue, 21 Dec 2021 02:23:45 GMT  
		Size: 7.7 MB (7695163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0317c7db28bd6855b787608d1f4236185907b452f6f545a9954be870828af6`  
		Last Modified: Tue, 21 Dec 2021 02:23:45 GMT  
		Size: 9.8 MB (9767165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4301bfae0dab5df877b31fde90c919b02335f783b7405d66b6123acfe03e69e`  
		Last Modified: Tue, 21 Dec 2021 02:24:05 GMT  
		Size: 52.2 MB (52168887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6796e6185a246ca4b1cc836375a882caae3bc75decdf616b42a59a8e66d8e74f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (122986427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c6c9ef58b1e4cd4d99a0107e9b96794bb50c1b741bb6d7456f0e31334c81f9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:40:24 GMT
ADD file:4e982be228380a8d7632e31f19e39ed55ee76fb1db32130fa88d696904d6acde in / 
# Tue, 21 Dec 2021 01:40:25 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:15:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:15:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 02:15:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:342b01a61e0af68dc09681004efdfcf66d0443632988d6f247dd7b34bc18b1db`  
		Last Modified: Tue, 21 Dec 2021 01:49:14 GMT  
		Size: 51.2 MB (51207766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4759b0dba897041c21e226a9db50a85ca5685f19bb5036f16df5b231fd177919`  
		Last Modified: Tue, 21 Dec 2021 02:27:24 GMT  
		Size: 8.0 MB (8000238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a258e8ae475665e88b0ebd438d4a945fa152a99c6d2ff863c06087a6dd4c7d`  
		Last Modified: Tue, 21 Dec 2021 02:27:24 GMT  
		Size: 10.3 MB (10340145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7754201e052c276668b8474d86f55c0df401d90074d1090dc57d978ce0be1a2d`  
		Last Modified: Tue, 21 Dec 2021 02:27:48 GMT  
		Size: 53.4 MB (53438278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:1534325d69a0197e6415e8a8584031cc98a441e5ec74889fe056560f0f45256a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.2 MB (117194878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ded5d1cbca967ea2c766ba1599909249376f4db5b580e5e12fad07d00961817`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:09:33 GMT
ADD file:f955c235588264a795d4f22cd0b6e343cc7b64c6c545c65ca1634fe8a1c664a1 in / 
# Tue, 21 Dec 2021 02:09:34 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:52:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:52:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 02:53:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c8948017ab035edb3d02daf180d7bc682ff63bc2ed281155da62060a3202c19b`  
		Last Modified: Tue, 21 Dec 2021 02:19:09 GMT  
		Size: 49.1 MB (49079634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4ee7bfb43763dcbeb287fb1d9bb0d4888986ebaa2eb6c2dbe9787043f53bb0`  
		Last Modified: Tue, 21 Dec 2021 03:09:55 GMT  
		Size: 7.3 MB (7253611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f00d4797ade3fe7297c1976df673831385af66ec0ab390c932279b9fdfd90ae`  
		Last Modified: Tue, 21 Dec 2021 03:09:52 GMT  
		Size: 10.0 MB (10016335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df0caf1c958ae1ba4df2c1afb1822046fcaa408b26a634dfe165c4d198e582f`  
		Last Modified: Tue, 21 Dec 2021 03:10:54 GMT  
		Size: 50.8 MB (50845298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2dd3b63176be92bcc8c6d0a495d453b50e5b6009d52fea95cd07e669ebfce271
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130640852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab2bbf998ae0a08753572d4ef9cc0f01f4c06b898b1acd9ef75fd66e200cb1b9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:20:42 GMT
ADD file:8056891c6381c1ff352984edda0a56834740c6dd16fb5d53cf6b6c2b4b3aad81 in / 
# Tue, 21 Dec 2021 02:20:48 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 03:06:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 03:06:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 03:08:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b07d0e315feadfc6b984834ea9bd062e7d0b75d60ca9fe83ac8516760c195fc8`  
		Last Modified: Tue, 21 Dec 2021 02:29:46 GMT  
		Size: 54.2 MB (54183767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58e7e1514e19554ca83c5952d5d4a888777f5719cb940d735b4ae13554f93a03`  
		Last Modified: Tue, 21 Dec 2021 03:32:32 GMT  
		Size: 8.3 MB (8272883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2122cccbee40e2064d7312947ab5464933c34df0d0dc57e5211831d057cabb89`  
		Last Modified: Tue, 21 Dec 2021 03:32:32 GMT  
		Size: 10.7 MB (10727604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d001a79f85db34f9fafac6f363f7d8219a6af526ff489448e6de64515b376aa9`  
		Last Modified: Tue, 21 Dec 2021 03:32:55 GMT  
		Size: 57.5 MB (57456598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9f3213860594aa2427e86f93f0f516bda8b96fc10d97b7ddd3bb3df5bc5d1fbe
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117670197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c72dc161b766b179cb43858d5e3721736ca63c3ec5dacc964f3298a9852c87`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:39 GMT
ADD file:def95923e24cb6059ca87ed32edda32704debf3cdd64fb6c50e156b7528dce0f in / 
# Tue, 21 Dec 2021 01:42:42 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:10:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:10:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 02:10:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:506fcc46017f6aa41ccd20bb2ea02ae7698abd4e52104cd94243f7aa64ce5ee0`  
		Last Modified: Tue, 21 Dec 2021 01:48:31 GMT  
		Size: 49.0 MB (49005442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772d29bde24f2fb280843cce37b4d501dc938c6dd3a0d7b773ddfa9d88436c8c`  
		Last Modified: Tue, 21 Dec 2021 02:18:25 GMT  
		Size: 7.4 MB (7401365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c399d86e51de8a9246ca00799d46792b4022f28a3eaf98791e69f39047566f38`  
		Last Modified: Tue, 21 Dec 2021 02:18:26 GMT  
		Size: 9.9 MB (9882996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90037fcd44cf83c4b37c676c05e2c9d1594bc8eb2efbbc73b8d78836f08eaa8`  
		Last Modified: Tue, 21 Dec 2021 02:18:39 GMT  
		Size: 51.4 MB (51380394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
