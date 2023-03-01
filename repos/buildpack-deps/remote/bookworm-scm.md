## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:1a8f55ac0afee0fa50cbf37d26bf9539d1d16fada3a5d6d90695b72083d27969
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

### `buildpack-deps:bookworm-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4694b99479c611535b15deb73873e8796d2c1323de95c4e53aec6aeb37bdd1d4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133859462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd5bc499e0a4139e6473088c83bbefc0ed47e96b60dacb2f2f65e05977883b3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Feb 2023 03:19:36 GMT
ADD file:99a61197d7273704581c44eae01f3342e9f3562e84fe66cc2d56ce563e58450a in / 
# Thu, 09 Feb 2023 03:19:37 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 09:08:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 09:08:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 09 Feb 2023 09:09:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:45c04dd46fbf614b423b54561d34c6339a0376d1717729ef6dcf101dbfd20f8c`  
		Last Modified: Thu, 09 Feb 2023 03:24:14 GMT  
		Size: 49.1 MB (49054961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666db2f0c3920c26fca8be06c139f8e93863caba116d9677e3ca33d4f46a074f`  
		Last Modified: Thu, 09 Feb 2023 09:16:52 GMT  
		Size: 9.0 MB (9033134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887d37599cf7cd74d72dc9d56f19300520564439f19992bb2e8de2ce584df713`  
		Last Modified: Thu, 09 Feb 2023 09:16:52 GMT  
		Size: 11.4 MB (11354763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9f5103cc59ff9f92590beaed1d1a0320afb6a600adac22bfb4497e37e008a7`  
		Last Modified: Thu, 09 Feb 2023 09:17:10 GMT  
		Size: 64.4 MB (64416604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e368a980ce07d0d05c407f5f83fd7eaa214a94ab89a68fd65bcc72113d126c75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129141721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f1ccaedc02174ef64b93a8f0f326ec4ffec1458f1c54768a5da3d2e53c616d2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:48:24 GMT
ADD file:1685939a153ab7a7aa03035565c60e99663abd3a416ef0d00bddaf24e0ae6f08 in / 
# Wed, 01 Mar 2023 01:48:25 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:14:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:14:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Mar 2023 02:15:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f7516928cdf57280d137bb31220dd9f0b6ca54e290189b42a68ab64d0d2065b7`  
		Last Modified: Wed, 01 Mar 2023 01:51:43 GMT  
		Size: 48.1 MB (48072838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b402a03a1c745fc42a93ed0082abf13d52e0c961da496b7b2d7d9a60a1d8031f`  
		Last Modified: Wed, 01 Mar 2023 02:23:46 GMT  
		Size: 8.5 MB (8496389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea6f1f01cbcb26c4e22bf2c443b3515e57d9267d84661daeb7ae809ff62ff82`  
		Last Modified: Wed, 01 Mar 2023 02:23:46 GMT  
		Size: 11.1 MB (11051495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db38c030ddb0562da5b6a4ed2e4333299c295c785959c19faae6aecfee04f841`  
		Last Modified: Wed, 01 Mar 2023 02:24:07 GMT  
		Size: 61.5 MB (61520999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:50c3989256c2843a2b482de025d801e81e3428fbc329c541d0c692bdb6b9bed6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124152337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68aaa7136576ff661d037e2e63c93c75fb8650daf6586cf8e8b4a2bb02a308c0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Feb 2023 06:11:15 GMT
ADD file:00a7b86df7c1e3b1064f9848e66b835d60203374321048b004728889f9033be6 in / 
# Thu, 09 Feb 2023 06:11:17 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 17:34:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 17:35:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 09 Feb 2023 17:35:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cc1adfc8958bbc0fb16a7e0a1534193e67c7436227ac284a68c36601ef15914c`  
		Last Modified: Thu, 09 Feb 2023 06:18:07 GMT  
		Size: 45.8 MB (45795912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7377a44228d605548594ad5afaed8f41257a1d7a090828d18171500dabe541`  
		Last Modified: Thu, 09 Feb 2023 17:45:53 GMT  
		Size: 8.1 MB (8124839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c807de20421b260151ee3eb132429b34a5c6336f5e0d0b16dcab34dbc01809c`  
		Last Modified: Thu, 09 Feb 2023 17:45:53 GMT  
		Size: 10.6 MB (10635770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403dac43fbe1292186670418f1f2d9137b55d87c6d38dbe1761e8b31b11995aa`  
		Last Modified: Thu, 09 Feb 2023 17:46:15 GMT  
		Size: 59.6 MB (59595816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:fe5bc0a10f85e1d412fd3ac919199f23ed21076d282fa4e087816586dd32d66b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133603302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9a22fd68a4ca446cc93d1715bd8f97e2c626be32f7be9fd4c19d832dc44a19`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Feb 2023 03:58:10 GMT
ADD file:bb3880a9ad854cde236b0e81a38e30cc0a4164d2d9ef140f29c28314ad31223d in / 
# Thu, 09 Feb 2023 03:58:10 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 09:06:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 09:06:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 09 Feb 2023 09:06:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:65cbd465e3f6368144b4429f3d79a2ef3faba24e97c701076009f84c0ed82a6a`  
		Last Modified: Thu, 09 Feb 2023 04:01:39 GMT  
		Size: 49.1 MB (49105777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95aa4eba0cc6b3f79d40a859b9545ba8a7d82ca90ca963ffb0d8b8aceeb9794`  
		Last Modified: Thu, 09 Feb 2023 09:13:24 GMT  
		Size: 8.9 MB (8865552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4af4383486dc9f58a0ce41730a60fc0d02f4751b99f733f5a6892ab841ea456`  
		Last Modified: Thu, 09 Feb 2023 09:13:25 GMT  
		Size: 11.3 MB (11319820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e4f09b81041b1ebe6ac8c4c6598c178218f530c037c945ff427b3ae385d4fc`  
		Last Modified: Thu, 09 Feb 2023 09:13:41 GMT  
		Size: 64.3 MB (64312153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ae8e961a9e40fd1cc67a16b2eeb562541342ae4bdaa1e6a49ac66fb1484f8e96
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137251175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38c2068c6e1d78739e77ceabcc05f5cb988caed03f0c045bd5c99279abfe372a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:38:40 GMT
ADD file:0ccdbb7b1f104c23abcf77c506eed771d5759d210c2284a95f85e558405a5390 in / 
# Wed, 01 Mar 2023 01:38:40 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:05:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:05:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Mar 2023 02:05:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b5ba6d7d02dd42cc6291ae5b4e129956756f664662a78db71f320107a1b6d189`  
		Last Modified: Wed, 01 Mar 2023 01:43:30 GMT  
		Size: 50.3 MB (50273396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f35c12f0528f81569a1c99e040f4d3527ee4391aa4079d740a4c6638bcece0`  
		Last Modified: Wed, 01 Mar 2023 02:22:07 GMT  
		Size: 9.2 MB (9230996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1319f35836381f914f3bbf4d55b955e9cf90a83165b64e829c72b52051b5e5c5`  
		Last Modified: Wed, 01 Mar 2023 02:22:07 GMT  
		Size: 11.8 MB (11808790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a8ff813204e629160f019ffdb45960b87b39f586133418d3fd5f36323e5f03`  
		Last Modified: Wed, 01 Mar 2023 02:22:30 GMT  
		Size: 65.9 MB (65937993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:58f7776ae5802beb5ff95c124b893ff3a2ce121f93e98d305337e9feeeb340d9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131875223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dde5105ffa4ba49e36c8a2afa67c343d1f83bde2ad9dde91a2a56b5056c6d4f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Feb 2023 02:43:09 GMT
ADD file:bff5ae942e6561f2afffbbd0267d57706f7fdd71ebe43c64b369b20940d55f00 in / 
# Thu, 09 Feb 2023 02:43:14 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 07:31:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 07:32:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 09 Feb 2023 07:33:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9aa6addfe979ac43879ea9517851622f7a6c1516568fbd6a0c101c3b86cc1163`  
		Last Modified: Thu, 09 Feb 2023 02:51:51 GMT  
		Size: 49.1 MB (49063446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6db93799880bf6f9525fc696324e0d450fd37ebbb37d356955a9057236da38`  
		Last Modified: Thu, 09 Feb 2023 07:56:29 GMT  
		Size: 8.4 MB (8399010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b19fed47eb69b023968097b12ef67cad0d7e15a03675cc16e3efc9b67a44e4`  
		Last Modified: Thu, 09 Feb 2023 07:56:29 GMT  
		Size: 11.1 MB (11105521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7152f2a237e2d177c5dc02d27a4b1e0433902b36280eb92369c2a9e5620678e`  
		Last Modified: Thu, 09 Feb 2023 07:57:24 GMT  
		Size: 63.3 MB (63307246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3eaab5084ad16813a4280bb47d15c82a49601e69a42a711c30c5fc73ffdbff7b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144734327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fdfbf4b0971a467daa63a9718f39df505e93c5f3468470039f8c3408ca81d84`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Feb 2023 06:20:33 GMT
ADD file:75adb66a2aa7c2e1853eed8d1b1a56d49de769582f417c0cb985662918634614 in / 
# Thu, 09 Feb 2023 06:20:36 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 12:20:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 12:20:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 09 Feb 2023 12:21:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b80d527d8ce70064c3ea21b4b5821ff792b80c344f46b22db738eb4abf5675c8`  
		Last Modified: Thu, 09 Feb 2023 06:27:02 GMT  
		Size: 53.1 MB (53065014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a33a62de1f22fdafc06ebf50e3c1a8773b08a8e1e13742338852bfbf84bb4d32`  
		Last Modified: Thu, 09 Feb 2023 12:37:10 GMT  
		Size: 9.6 MB (9613605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9495f7521938fcaa764b980d858ba9d419fd73def42c0c18571f4886d2eff98`  
		Last Modified: Thu, 09 Feb 2023 12:37:10 GMT  
		Size: 12.1 MB (12114598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a32910a210be110b494341b4ad40c4bdeb7742660743c6d7c9d46d3f6d9ed9`  
		Last Modified: Thu, 09 Feb 2023 12:37:39 GMT  
		Size: 69.9 MB (69941110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:34df88bcae10c5f6c08701e3d38c3c7058b80d1291458843d1e242251076b9dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130704781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f58248367caeacdb8799058f1735bf37cccd19ac2f573cae283bf951e27eae`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Feb 2023 02:40:45 GMT
ADD file:0edac1ca3f05ba1f621c1dab181be5479d166d4a4c6a303bf07be225c572bb84 in / 
# Thu, 09 Feb 2023 02:40:55 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 07:22:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 07:22:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 09 Feb 2023 07:23:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:667517dccb1c9b12f559214da46416c75d071090a71194ab7882908fd3eddc8f`  
		Last Modified: Thu, 09 Feb 2023 02:45:19 GMT  
		Size: 47.4 MB (47428619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50816d8e878439c60f498af4735ce27a1ac8c0c9b4fb1af0b2cc5eb3b170d3b9`  
		Last Modified: Thu, 09 Feb 2023 07:39:38 GMT  
		Size: 8.7 MB (8666639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b757e546fa8d91f119cec4fc64f69f4cb03d686f61e9c39493d98bf75ec0b5d`  
		Last Modified: Thu, 09 Feb 2023 07:39:38 GMT  
		Size: 11.2 MB (11218326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545f4f8d16022f0b19ec3c8035e95c53e495713d06ca6d692cda8901987c1671`  
		Last Modified: Thu, 09 Feb 2023 07:39:53 GMT  
		Size: 63.4 MB (63391197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
