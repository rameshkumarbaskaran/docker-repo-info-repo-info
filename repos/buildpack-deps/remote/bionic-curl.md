## `buildpack-deps:bionic-curl`

```console
$ docker pull buildpack-deps@sha256:8f3b208c5852568bdfaf98a5c8060dc7b555adc7c789baaf963447588189d868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bionic-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b089200dd4fa37e64684e79ca80221b5bb431cbbcd8e00a9817b11c34bf0a85f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36382582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7afe1943809a6327bfc7bb2f8f3fad77a8eda9eab4765442fc525ff398a56f21`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:04 GMT
ADD file:40290d9a94ae76c35ab1f57178130ce1c5b976e34a91e77472ecf7e945ab64f9 in / 
# Mon, 06 Jun 2022 22:21:05 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 02:03:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 02:03:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:09db6f815738b9c8f25420c47e093f89abaabaa653f9678587b57e8f4400b5ff`  
		Last Modified: Wed, 01 Jun 2022 21:51:21 GMT  
		Size: 26.7 MB (26711626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d3b7a8084f0f50ac1b09fe5b075dd39627cf2d5bf67659da7c41138cda7b67`  
		Last Modified: Tue, 07 Jun 2022 02:23:53 GMT  
		Size: 6.6 MB (6644325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd97ebd2067d1a4bead88f69c0cdcc55b5a30fce0416079338359fc29d2bb4a8`  
		Last Modified: Tue, 07 Jun 2022 02:23:52 GMT  
		Size: 3.0 MB (3026631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:acd2ed07ed2cd239b3dea5307670e6bcddcae338d1978c43d9ae0932a9860847
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 MB (30789280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441a36df4e84aa61908d0d77febc076142b2485034c6d77462b77148b3350499`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Jun 2022 05:50:28 GMT
ADD file:d6d276f8f40c095bc2411f4d370eb87f8042a092ebb5bb0076863b2b6182b34f in / 
# Tue, 07 Jun 2022 05:50:29 GMT
CMD ["bash"]
# Thu, 28 Jul 2022 13:34:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 13:34:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:9242055bc3f039f3566a5154c8b1a602652bfe444e9b4291817caae906444e75`  
		Last Modified: Tue, 07 Jun 2022 05:54:37 GMT  
		Size: 22.3 MB (22306284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9012518c07b019eb423f4c44b66270a7e055f601396b9665d3d56137b5b04ff`  
		Last Modified: Thu, 28 Jul 2022 13:59:02 GMT  
		Size: 5.7 MB (5706732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d186bea469dc112002f69f51970c220b48a920066dca3460f0d87f9015613b6e`  
		Last Modified: Thu, 28 Jul 2022 13:59:01 GMT  
		Size: 2.8 MB (2776264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:235d779b5ba96fcf962b04a65dbcd022592e60f60949906d82ad861d3c655563
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32385431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d7d8e1e57ac5bb13a52926ea521cf7176db645c4d2e6c7948de5d27cf18ea3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:29:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:29:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a8ce0030c4c3bf1c638b4471e5162eef4a430b61c537057f0f8ce51fc18444`  
		Last Modified: Tue, 02 Aug 2022 01:48:44 GMT  
		Size: 6.1 MB (6079418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63b2c6b27d8a588f648165c46146db98c94f4640019d6d8caf00868911d4133`  
		Last Modified: Tue, 02 Aug 2022 01:48:43 GMT  
		Size: 2.6 MB (2571299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0252ccf587f9487db325574d1a3fe8bb3eb31d91533fe434630d4477512c27c5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37130904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad2ddbf64a9d8977cd6af1ef106ddd00047be5f711281f3d1e867d0fa203f6b4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:50:55 GMT
ADD file:6d22c6318075d01068d0a9213f33655abf6c251f8a71d98c17b857b9021b43bd in / 
# Tue, 02 Aug 2022 00:50:55 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:15:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:15:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:5496b4c91dece81ce997c62cf2e1ef6f1764e612c6e8f0b385722c6645e4ad30`  
		Last Modified: Tue, 02 Aug 2022 00:51:39 GMT  
		Size: 27.2 MB (27164268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8439504988f2843b5e4ef5dcf3fcec03b31d6e19990975f2aea8b59fac990dd6`  
		Last Modified: Tue, 02 Aug 2022 01:28:03 GMT  
		Size: 6.9 MB (6926590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b6dc1acdd5e447706ea88235a69f6f13e0c84711fc699ba22ed607d3bf8147`  
		Last Modified: Tue, 02 Aug 2022 01:28:02 GMT  
		Size: 3.0 MB (3040046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:28595f53fd9e477286d26c7f9817b0b29e75bc75c6eeb420282705e9559309ac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41520860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad44e9d460d117f971b989345ec4d2327c05946dea5712dd522f5e5594b0dea`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Jun 2022 05:45:31 GMT
ADD file:00feca269255d07b1ddb816beb48357c556d80ab79aa81bc448abc4271d845a5 in / 
# Tue, 07 Jun 2022 05:45:36 GMT
CMD ["bash"]
# Tue, 26 Jul 2022 22:54:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Jul 2022 22:54:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:868ede65862ecf99802bf8944efd378ff1e0751772424cea9084f390deb9f9b2`  
		Last Modified: Tue, 07 Jun 2022 05:48:49 GMT  
		Size: 30.4 MB (30442859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17b26565b0d35480b1dfc4921d472a42568f0d9b39e64be90de6533774e53fd9`  
		Last Modified: Tue, 26 Jul 2022 23:53:55 GMT  
		Size: 7.1 MB (7056280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f00d8045f40230dba407517829fb31be26b3dd8bc8353c97dbc491385bfce305`  
		Last Modified: Tue, 26 Jul 2022 23:53:54 GMT  
		Size: 4.0 MB (4021721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:234d3dc6cd2342a69b57b0f60312185e082d0bff6004b71e701f4be7a0ea8784
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34677626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46a2df4940e4ad7ca511dabe93e18df5b61cabea6c43542e92a66a618f0aa40f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:01:57 GMT
ADD file:3d2e9b401524527b395347bc3847be7c9cb465b9a214a1a1d31e74330e293c45 in / 
# Tue, 02 Aug 2022 01:01:58 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:14:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:14:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:be3ed498266c519f84268ff1f02085fa249c0e32fb60a59466e24c862b5f094b`  
		Last Modified: Tue, 02 Aug 2022 01:03:25 GMT  
		Size: 25.4 MB (25369584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4fae7a4d4ea1c6cff382e8f74717aeaf4318c898d85ce8bb7454752509fb931`  
		Last Modified: Tue, 02 Aug 2022 01:38:08 GMT  
		Size: 6.3 MB (6330826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97089932290a776584a9006d4825a8ef9a13185d90ec2b9075b7691058ebb307`  
		Last Modified: Tue, 02 Aug 2022 01:38:07 GMT  
		Size: 3.0 MB (2977216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
