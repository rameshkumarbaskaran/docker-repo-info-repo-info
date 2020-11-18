## `buildpack-deps:jessie-curl`

```console
$ docker pull buildpack-deps@sha256:27d3e5370665fa0f17db225653e7b82757a4dca99f10d0cb598534fb3f924b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; 386

### `buildpack-deps:jessie-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:920aaad99b891e026abc039228b3267c20748da56e40278c10656b7a79f121f7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71934838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9a1dda4899997db71c7adafc70c92f451419a1bd2f806e298167e8d1adf00e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:39:33 GMT
ADD file:7b9ac38d270ca27e5fb553f80effa79883356f259ca9c3a1386f94c504626233 in / 
# Tue, 13 Oct 2020 01:39:33 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:18:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:18:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:0c57dff6aebdc848ab6cb6f56e094fe0a36bfe02230a16dc07e3acc5afc7f455`  
		Last Modified: Tue, 13 Oct 2020 01:48:35 GMT  
		Size: 54.4 MB (54388880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46109a4143b58cf9597de61dcb265516944d45ed3effc5ac56e1b90603402dfd`  
		Last Modified: Tue, 13 Oct 2020 02:29:40 GMT  
		Size: 17.5 MB (17545958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jessie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:adf3b0f4a487ad5fea1181ca5995656ae17c0faa86f2b2a25980d2db2686f617
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69620011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:911a60057036ac0988f989ddb842b8378c6578599781a7def4af5d9c1dfc735d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:09 GMT
ADD file:06d0d96a3590043e004bbd651614b8c1b4b048df6ce8706542c12613e2ef83f3 in / 
# Tue, 17 Nov 2020 20:21:10 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:47:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:47:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2950e78c0ac6ca79b0455caabb98b5d25fa715881ced046fe07f25029b96bd01`  
		Last Modified: Tue, 17 Nov 2020 20:30:58 GMT  
		Size: 52.6 MB (52582709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d215fc87b1798e34927476d1004914e87fa45af53379310422e62443ed2654`  
		Last Modified: Tue, 17 Nov 2020 22:10:02 GMT  
		Size: 17.0 MB (17037302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jessie-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:79ae1bda1a22d52a8061221d189f9085d9e899444f5a5c5375e0d01ee11d2df0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (67028641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4147bbc14a72d7310e55211aed16dfa0df6a006edb0afa5f0fe4381e20a0c6a2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:34 GMT
ADD file:b2545152b2d5298539a3587be3ec1f7ecfececebb4ee80eaff97f66143feac5e in / 
# Tue, 17 Nov 2020 20:21:35 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:46:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:46:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d4af4a46f2c554db32c2423a35e7d1fd96ec1a41633404963392957596e60a5b`  
		Last Modified: Tue, 17 Nov 2020 20:32:10 GMT  
		Size: 50.3 MB (50305387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc5e67e7f7b7f724bbb49fbc0795a7c5d76ac00b944870eb1d2ea3a69994caa`  
		Last Modified: Tue, 17 Nov 2020 22:08:52 GMT  
		Size: 16.7 MB (16723254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jessie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5553bcc1c77a5c1b77207790e17323d6c0be000a3f3e832943b3f5ab0b5173d8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74464725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4b35e65dcf4699a6bdecec9aaa3c094b3d82c184be2bce1551ea2e619a7fab`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:16 GMT
ADD file:843de10973ffdcb28448f75b968c0f3f47adc33e3bb0fa5adf1c488c8fbbf5f1 in / 
# Tue, 17 Nov 2020 20:20:16 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:09:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:09:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b79b7651073e6b6c71d7e4168850a7ded5ca4e7d948a7035975a0e83ad6703c6`  
		Last Modified: Tue, 17 Nov 2020 20:27:07 GMT  
		Size: 54.6 MB (54608823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c14b2d754487de7f15aff3e85e50a59c7af0d8f0fcd3ce1c40e8ec436e5fb2d`  
		Last Modified: Tue, 17 Nov 2020 21:25:19 GMT  
		Size: 19.9 MB (19855902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
