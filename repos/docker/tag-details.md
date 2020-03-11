<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:19`](#docker19)
-	[`docker:19.03`](#docker1903)
-	[`docker:19.03.8`](#docker19038)
-	[`docker:19.03.8-dind`](#docker19038-dind)
-	[`docker:19.03.8-dind-rootless`](#docker19038-dind-rootless)
-	[`docker:19.03.8-git`](#docker19038-git)
-	[`docker:19.03-dind`](#docker1903-dind)
-	[`docker:19.03-dind-rootless`](#docker1903-dind-rootless)
-	[`docker:19.03-git`](#docker1903-git)
-	[`docker:19-dind`](#docker19-dind)
-	[`docker:19-dind-rootless`](#docker19-dind-rootless)
-	[`docker:19-git`](#docker19-git)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:git`](#dockergit)
-	[`docker:latest`](#dockerlatest)
-	[`docker:stable`](#dockerstable)
-	[`docker:stable-dind`](#dockerstable-dind)
-	[`docker:stable-dind-rootless`](#dockerstable-dind-rootless)
-	[`docker:stable-git`](#dockerstable-git)
-	[`docker:test`](#dockertest)
-	[`docker:test-dind`](#dockertest-dind)
-	[`docker:test-dind-rootless`](#dockertest-dind-rootless)
-	[`docker:test-git`](#dockertest-git)

## `docker:19`

```console
$ docker pull docker@sha256:948c0f302dae8ce62d28c32e46817c054cd5b00353fb0037646e92917a4124ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19` - linux; amd64

```console
$ docker pull docker@sha256:7c311f0515f6e2bba92961cbd4c11ea7c74791935260c0c72c0ceebc75e52867
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69448807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f39826ae385e029ae634eb6a81091da60dae2e6ee2a19342c2e05ed4c3cb9171`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 04:42:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 04:42:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:19:32 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:19:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:19:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:39 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd54125436dc48e0d60096d61457bcfd886136eb67815a60210ec67d3793096f`  
		Last Modified: Sat, 18 Jan 2020 04:43:03 GMT  
		Size: 2.4 MB (2425150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d1554c15cbb8c6b81fd21a057c8e97749fb24fd5befeb94ad960d3a350f91f`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dd17ef2c28fbb77b8b589e2e601e3ce86c0b9bcdb9dc73b6330d7ca16dca19`  
		Last Modified: Wed, 11 Mar 2020 21:20:40 GMT  
		Size: 64.2 MB (64218865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca57ea69baf170d62b8d1a51d898ff8d9383e22cd18bbde168ff539e74be8a4`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3af031952ce6719d5ca2f369b2187e1819fdab00252d315555a00048d6b99b7`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29377cccb214061fb46c1d5a1c27f53c366384d34f168cdb8484f5c7fcfb87a`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19` - linux; arm variant v6

```console
$ docker pull docker@sha256:6066e1dbf8e74562362b84d31bfbf3356ab716c355e25d2fb3682f22f0016790
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64901998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbdbf0acc9e925c42921278175492252e55a006bf4ffff577bd68d5f1b29256a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 05:52:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 05:52:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 05:52:35 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:49:22 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:49:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:49:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:49:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:49:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:49:38 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c86f804e7b5cc2f1f9d87340dfef1fcc13615f2cbd25bda470e513c1e4a627`  
		Last Modified: Sat, 18 Jan 2020 05:54:22 GMT  
		Size: 2.4 MB (2355405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d84775c03f92068112e3757afd6ddab1b2c0a3d1073e91b182620b6ec239f7`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592a77d3ce3aac4cb4c252c866f4a65c1541726b2bbdb512444569119b5cd98e`  
		Last Modified: Wed, 11 Mar 2020 21:50:37 GMT  
		Size: 59.9 MB (59927165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0277ab691262af1bf0bf50d6d459874dbf48509a6103991fd9d6225e455cb995`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320285a35393ed08c2ed85f5dc6d6ca6a1c07ac14fcfb8b4e1e5c5a4c30eace9`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e82c58148faac404a83fad42819c701567beb61dac6c2ae6d76ac1f97eefccd`  
		Last Modified: Wed, 11 Mar 2020 21:50:18 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19` - linux; arm variant v7

```console
$ docker pull docker@sha256:32278b2c6a6b432c34a19367f68170d2bff8f79c57962f5cb4aab31f26130c6b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64602871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc2d0d6f635fee2fc5a74c78e7532a964940bead391471966dee40a29eeacc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:01:09 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 03:01:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 03:01:20 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:57:34 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:57:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:57:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:57:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:57:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:57:48 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5014010b799b2f3cc6305fd21cc4b096dd28ad093e165cea5976f92ccb8c462`  
		Last Modified: Sat, 18 Jan 2020 03:03:27 GMT  
		Size: 2.3 MB (2254397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f49247ef05003d569c198c4908b849fdadd330bf360c04360ae48fd0d68b6d`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca62e39536ad2825e9d1db7dbfa88f4cbc9d95659c5fb45691fa224654d2629`  
		Last Modified: Wed, 11 Mar 2020 21:58:49 GMT  
		Size: 59.9 MB (59927053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a96da9a069c4780e3c46bcbd35f4da5d0e173b2888bec333941260f131ccc8`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202349aaae9b658c7d87822ac340735af35c35495f6af77e5db0df2d253880ea`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f43ed55770aa202e0a559ef5505907bdf9e16eb7ea47829463da52a02907f9c`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f7f9c3b259b133a7cca0bfbe5db7f70c955aff499307e2714426c63fac9d5470
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62557924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea45e49e2b3cb4f5dc30b5f16f86e87e685949e8eb7ce7a98e59818c500dd823`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 02:23:05 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 02:23:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 02:23:12 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:39:44 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:39:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:39:52 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:39:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:39:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:39:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:39:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:39:56 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:8fa90b21c985a6fcfff966bdfbde81cdd088de0aa8af38110057f6ac408f4408`  
		Last Modified: Sat, 18 Jan 2020 01:40:23 GMT  
		Size: 2.7 MB (2723075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2917335fcb0a6856d5bf55430ba707c2c1378029a109e61959e62d2769230db`  
		Last Modified: Sat, 18 Jan 2020 02:25:35 GMT  
		Size: 2.4 MB (2445713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d3c84c2515134ddfa5ae5bac6e140953e9576fcd30a0bbc10fbc565d267895`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a828ac2f8d0e08bfd3c5405031bb245a21e469671397bd03e8868ce0925d9f49`  
		Last Modified: Wed, 11 Mar 2020 21:40:56 GMT  
		Size: 57.4 MB (57387269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7b0e4ac96f123613bb6ebd37a1bb99fb6f8a12b1d521f89f4211a970dbc077`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25581ce9dd66a29fecb3a63c9f888a0c6e3c68de7002441092b6a41dd833e995`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc58c5fdb432f00e6a7cdfa6b6507ca3c8598ab0612730e109e4faf5b0fc2d5a`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03`

```console
$ docker pull docker@sha256:948c0f302dae8ce62d28c32e46817c054cd5b00353fb0037646e92917a4124ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19.03` - linux; amd64

```console
$ docker pull docker@sha256:7c311f0515f6e2bba92961cbd4c11ea7c74791935260c0c72c0ceebc75e52867
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69448807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f39826ae385e029ae634eb6a81091da60dae2e6ee2a19342c2e05ed4c3cb9171`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 04:42:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 04:42:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:19:32 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:19:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:19:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:39 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd54125436dc48e0d60096d61457bcfd886136eb67815a60210ec67d3793096f`  
		Last Modified: Sat, 18 Jan 2020 04:43:03 GMT  
		Size: 2.4 MB (2425150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d1554c15cbb8c6b81fd21a057c8e97749fb24fd5befeb94ad960d3a350f91f`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dd17ef2c28fbb77b8b589e2e601e3ce86c0b9bcdb9dc73b6330d7ca16dca19`  
		Last Modified: Wed, 11 Mar 2020 21:20:40 GMT  
		Size: 64.2 MB (64218865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca57ea69baf170d62b8d1a51d898ff8d9383e22cd18bbde168ff539e74be8a4`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3af031952ce6719d5ca2f369b2187e1819fdab00252d315555a00048d6b99b7`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29377cccb214061fb46c1d5a1c27f53c366384d34f168cdb8484f5c7fcfb87a`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03` - linux; arm variant v6

```console
$ docker pull docker@sha256:6066e1dbf8e74562362b84d31bfbf3356ab716c355e25d2fb3682f22f0016790
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64901998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbdbf0acc9e925c42921278175492252e55a006bf4ffff577bd68d5f1b29256a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 05:52:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 05:52:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 05:52:35 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:49:22 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:49:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:49:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:49:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:49:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:49:38 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c86f804e7b5cc2f1f9d87340dfef1fcc13615f2cbd25bda470e513c1e4a627`  
		Last Modified: Sat, 18 Jan 2020 05:54:22 GMT  
		Size: 2.4 MB (2355405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d84775c03f92068112e3757afd6ddab1b2c0a3d1073e91b182620b6ec239f7`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592a77d3ce3aac4cb4c252c866f4a65c1541726b2bbdb512444569119b5cd98e`  
		Last Modified: Wed, 11 Mar 2020 21:50:37 GMT  
		Size: 59.9 MB (59927165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0277ab691262af1bf0bf50d6d459874dbf48509a6103991fd9d6225e455cb995`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320285a35393ed08c2ed85f5dc6d6ca6a1c07ac14fcfb8b4e1e5c5a4c30eace9`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e82c58148faac404a83fad42819c701567beb61dac6c2ae6d76ac1f97eefccd`  
		Last Modified: Wed, 11 Mar 2020 21:50:18 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03` - linux; arm variant v7

```console
$ docker pull docker@sha256:32278b2c6a6b432c34a19367f68170d2bff8f79c57962f5cb4aab31f26130c6b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64602871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc2d0d6f635fee2fc5a74c78e7532a964940bead391471966dee40a29eeacc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:01:09 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 03:01:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 03:01:20 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:57:34 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:57:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:57:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:57:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:57:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:57:48 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5014010b799b2f3cc6305fd21cc4b096dd28ad093e165cea5976f92ccb8c462`  
		Last Modified: Sat, 18 Jan 2020 03:03:27 GMT  
		Size: 2.3 MB (2254397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f49247ef05003d569c198c4908b849fdadd330bf360c04360ae48fd0d68b6d`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca62e39536ad2825e9d1db7dbfa88f4cbc9d95659c5fb45691fa224654d2629`  
		Last Modified: Wed, 11 Mar 2020 21:58:49 GMT  
		Size: 59.9 MB (59927053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a96da9a069c4780e3c46bcbd35f4da5d0e173b2888bec333941260f131ccc8`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202349aaae9b658c7d87822ac340735af35c35495f6af77e5db0df2d253880ea`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f43ed55770aa202e0a559ef5505907bdf9e16eb7ea47829463da52a02907f9c`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f7f9c3b259b133a7cca0bfbe5db7f70c955aff499307e2714426c63fac9d5470
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62557924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea45e49e2b3cb4f5dc30b5f16f86e87e685949e8eb7ce7a98e59818c500dd823`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 02:23:05 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 02:23:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 02:23:12 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:39:44 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:39:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:39:52 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:39:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:39:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:39:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:39:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:39:56 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:8fa90b21c985a6fcfff966bdfbde81cdd088de0aa8af38110057f6ac408f4408`  
		Last Modified: Sat, 18 Jan 2020 01:40:23 GMT  
		Size: 2.7 MB (2723075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2917335fcb0a6856d5bf55430ba707c2c1378029a109e61959e62d2769230db`  
		Last Modified: Sat, 18 Jan 2020 02:25:35 GMT  
		Size: 2.4 MB (2445713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d3c84c2515134ddfa5ae5bac6e140953e9576fcd30a0bbc10fbc565d267895`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a828ac2f8d0e08bfd3c5405031bb245a21e469671397bd03e8868ce0925d9f49`  
		Last Modified: Wed, 11 Mar 2020 21:40:56 GMT  
		Size: 57.4 MB (57387269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7b0e4ac96f123613bb6ebd37a1bb99fb6f8a12b1d521f89f4211a970dbc077`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25581ce9dd66a29fecb3a63c9f888a0c6e3c68de7002441092b6a41dd833e995`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc58c5fdb432f00e6a7cdfa6b6507ca3c8598ab0612730e109e4faf5b0fc2d5a`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03.8`

```console
$ docker pull docker@sha256:948c0f302dae8ce62d28c32e46817c054cd5b00353fb0037646e92917a4124ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19.03.8` - linux; amd64

```console
$ docker pull docker@sha256:7c311f0515f6e2bba92961cbd4c11ea7c74791935260c0c72c0ceebc75e52867
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69448807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f39826ae385e029ae634eb6a81091da60dae2e6ee2a19342c2e05ed4c3cb9171`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 04:42:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 04:42:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:19:32 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:19:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:19:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:39 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd54125436dc48e0d60096d61457bcfd886136eb67815a60210ec67d3793096f`  
		Last Modified: Sat, 18 Jan 2020 04:43:03 GMT  
		Size: 2.4 MB (2425150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d1554c15cbb8c6b81fd21a057c8e97749fb24fd5befeb94ad960d3a350f91f`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dd17ef2c28fbb77b8b589e2e601e3ce86c0b9bcdb9dc73b6330d7ca16dca19`  
		Last Modified: Wed, 11 Mar 2020 21:20:40 GMT  
		Size: 64.2 MB (64218865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca57ea69baf170d62b8d1a51d898ff8d9383e22cd18bbde168ff539e74be8a4`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3af031952ce6719d5ca2f369b2187e1819fdab00252d315555a00048d6b99b7`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29377cccb214061fb46c1d5a1c27f53c366384d34f168cdb8484f5c7fcfb87a`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.8` - linux; arm variant v6

```console
$ docker pull docker@sha256:6066e1dbf8e74562362b84d31bfbf3356ab716c355e25d2fb3682f22f0016790
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64901998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbdbf0acc9e925c42921278175492252e55a006bf4ffff577bd68d5f1b29256a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 05:52:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 05:52:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 05:52:35 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:49:22 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:49:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:49:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:49:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:49:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:49:38 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c86f804e7b5cc2f1f9d87340dfef1fcc13615f2cbd25bda470e513c1e4a627`  
		Last Modified: Sat, 18 Jan 2020 05:54:22 GMT  
		Size: 2.4 MB (2355405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d84775c03f92068112e3757afd6ddab1b2c0a3d1073e91b182620b6ec239f7`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592a77d3ce3aac4cb4c252c866f4a65c1541726b2bbdb512444569119b5cd98e`  
		Last Modified: Wed, 11 Mar 2020 21:50:37 GMT  
		Size: 59.9 MB (59927165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0277ab691262af1bf0bf50d6d459874dbf48509a6103991fd9d6225e455cb995`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320285a35393ed08c2ed85f5dc6d6ca6a1c07ac14fcfb8b4e1e5c5a4c30eace9`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e82c58148faac404a83fad42819c701567beb61dac6c2ae6d76ac1f97eefccd`  
		Last Modified: Wed, 11 Mar 2020 21:50:18 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.8` - linux; arm variant v7

```console
$ docker pull docker@sha256:32278b2c6a6b432c34a19367f68170d2bff8f79c57962f5cb4aab31f26130c6b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64602871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc2d0d6f635fee2fc5a74c78e7532a964940bead391471966dee40a29eeacc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:01:09 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 03:01:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 03:01:20 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:57:34 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:57:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:57:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:57:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:57:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:57:48 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5014010b799b2f3cc6305fd21cc4b096dd28ad093e165cea5976f92ccb8c462`  
		Last Modified: Sat, 18 Jan 2020 03:03:27 GMT  
		Size: 2.3 MB (2254397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f49247ef05003d569c198c4908b849fdadd330bf360c04360ae48fd0d68b6d`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca62e39536ad2825e9d1db7dbfa88f4cbc9d95659c5fb45691fa224654d2629`  
		Last Modified: Wed, 11 Mar 2020 21:58:49 GMT  
		Size: 59.9 MB (59927053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a96da9a069c4780e3c46bcbd35f4da5d0e173b2888bec333941260f131ccc8`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202349aaae9b658c7d87822ac340735af35c35495f6af77e5db0df2d253880ea`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f43ed55770aa202e0a559ef5505907bdf9e16eb7ea47829463da52a02907f9c`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.8` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f7f9c3b259b133a7cca0bfbe5db7f70c955aff499307e2714426c63fac9d5470
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62557924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea45e49e2b3cb4f5dc30b5f16f86e87e685949e8eb7ce7a98e59818c500dd823`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 02:23:05 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 02:23:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 02:23:12 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:39:44 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:39:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:39:52 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:39:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:39:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:39:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:39:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:39:56 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:8fa90b21c985a6fcfff966bdfbde81cdd088de0aa8af38110057f6ac408f4408`  
		Last Modified: Sat, 18 Jan 2020 01:40:23 GMT  
		Size: 2.7 MB (2723075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2917335fcb0a6856d5bf55430ba707c2c1378029a109e61959e62d2769230db`  
		Last Modified: Sat, 18 Jan 2020 02:25:35 GMT  
		Size: 2.4 MB (2445713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d3c84c2515134ddfa5ae5bac6e140953e9576fcd30a0bbc10fbc565d267895`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a828ac2f8d0e08bfd3c5405031bb245a21e469671397bd03e8868ce0925d9f49`  
		Last Modified: Wed, 11 Mar 2020 21:40:56 GMT  
		Size: 57.4 MB (57387269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7b0e4ac96f123613bb6ebd37a1bb99fb6f8a12b1d521f89f4211a970dbc077`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25581ce9dd66a29fecb3a63c9f888a0c6e3c68de7002441092b6a41dd833e995`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc58c5fdb432f00e6a7cdfa6b6507ca3c8598ab0612730e109e4faf5b0fc2d5a`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03.8-dind`

```console
$ docker pull docker@sha256:308dcf9380af44ea492736e8d59605cd0ff2dab0527073f7e718ee4498e85dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19.03.8-dind` - linux; amd64

```console
$ docker pull docker@sha256:0e6d34042007a6f5280838dc045af0d600654b57cd367251d1dd8bba4b55c773
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75051735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe98abf5dda7ec569bc4821f20ceca66945e67882fe32f960fb8b8f179af0e42`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 04:42:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 04:42:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:19:32 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:19:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:19:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:39 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:19:45 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Mar 2020 21:19:45 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:19:46 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Mar 2020 21:19:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Mar 2020 21:19:47 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:47 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Mar 2020 21:19:47 GMT
EXPOSE 2375 2376
# Wed, 11 Mar 2020 21:19:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:47 GMT
CMD []
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd54125436dc48e0d60096d61457bcfd886136eb67815a60210ec67d3793096f`  
		Last Modified: Sat, 18 Jan 2020 04:43:03 GMT  
		Size: 2.4 MB (2425150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d1554c15cbb8c6b81fd21a057c8e97749fb24fd5befeb94ad960d3a350f91f`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dd17ef2c28fbb77b8b589e2e601e3ce86c0b9bcdb9dc73b6330d7ca16dca19`  
		Last Modified: Wed, 11 Mar 2020 21:20:40 GMT  
		Size: 64.2 MB (64218865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca57ea69baf170d62b8d1a51d898ff8d9383e22cd18bbde168ff539e74be8a4`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3af031952ce6719d5ca2f369b2187e1819fdab00252d315555a00048d6b99b7`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29377cccb214061fb46c1d5a1c27f53c366384d34f168cdb8484f5c7fcfb87a`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4939ff19fbb72e09aad6b10bc7440f9b23e0983f05c3cf6679a6392a40103b27`  
		Last Modified: Wed, 11 Mar 2020 21:20:48 GMT  
		Size: 5.6 MB (5598354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617664eed4c7060ec14f8178529d17b8a637b33a19f65101e062e185feda4c1`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8b6f7ec5ec983309648ff91b432c6abc38b547fc0610e3d81ab7e2472ad7ae`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 756.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb8de5d1a5be108527d435aef60a4a041879e0ddcf6d747ff324d57a5000f03`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 2.5 KB (2536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.8-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:04246f289e63b1bc0baf3ee051e2374497207183b9e5b86373aa2f8938893a6c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68121997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08fff432f3d4cd1dae7778792ad2daa258d095691556f760fe82584bb66fa2b8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 05:52:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 05:52:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 05:52:35 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:49:22 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:49:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:49:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:49:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:49:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:49:38 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:49:46 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Mar 2020 21:49:48 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:49:49 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Mar 2020 21:49:51 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Mar 2020 21:49:51 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:49:52 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Mar 2020 21:49:52 GMT
EXPOSE 2375 2376
# Wed, 11 Mar 2020 21:49:53 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Mar 2020 21:49:53 GMT
CMD []
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c86f804e7b5cc2f1f9d87340dfef1fcc13615f2cbd25bda470e513c1e4a627`  
		Last Modified: Sat, 18 Jan 2020 05:54:22 GMT  
		Size: 2.4 MB (2355405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d84775c03f92068112e3757afd6ddab1b2c0a3d1073e91b182620b6ec239f7`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592a77d3ce3aac4cb4c252c866f4a65c1541726b2bbdb512444569119b5cd98e`  
		Last Modified: Wed, 11 Mar 2020 21:50:37 GMT  
		Size: 59.9 MB (59927165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0277ab691262af1bf0bf50d6d459874dbf48509a6103991fd9d6225e455cb995`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320285a35393ed08c2ed85f5dc6d6ca6a1c07ac14fcfb8b4e1e5c5a4c30eace9`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e82c58148faac404a83fad42819c701567beb61dac6c2ae6d76ac1f97eefccd`  
		Last Modified: Wed, 11 Mar 2020 21:50:18 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b1648a96394c26b0e7d5c254c39b36c8eca6d00dfff5aa3776cb6671284ead`  
		Last Modified: Wed, 11 Mar 2020 21:50:49 GMT  
		Size: 3.2 MB (3215398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e63bc9624da4519af0d163fc47db94ef5d7d0ae27deccb9d6b923ba97710251`  
		Last Modified: Wed, 11 Mar 2020 21:50:48 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8f7907ef28cfa8968f389a0e60d2b4a98f2b9da2963e09d86911a36e945825`  
		Last Modified: Wed, 11 Mar 2020 21:50:48 GMT  
		Size: 754.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013cac041612fcb3b3db97e63f70c7f357b31618cd79f2a0852b38181355f5bd`  
		Last Modified: Wed, 11 Mar 2020 21:50:48 GMT  
		Size: 2.5 KB (2532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.8-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:c2d6834d581a10f8d30ae8678d859ad15a3747335051665f21dbe7e602568a8a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67486006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd179934e0f1561bdac8a67db9bf33af7be9c1f7508bdb0c7aa76184817e0d62`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:01:09 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 03:01:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 03:01:20 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:57:34 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:57:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:57:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:57:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:57:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:57:48 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:57:57 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Mar 2020 21:57:59 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:58:00 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Mar 2020 21:58:02 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Mar 2020 21:58:02 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:58:03 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Mar 2020 21:58:03 GMT
EXPOSE 2375 2376
# Wed, 11 Mar 2020 21:58:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Mar 2020 21:58:05 GMT
CMD []
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5014010b799b2f3cc6305fd21cc4b096dd28ad093e165cea5976f92ccb8c462`  
		Last Modified: Sat, 18 Jan 2020 03:03:27 GMT  
		Size: 2.3 MB (2254397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f49247ef05003d569c198c4908b849fdadd330bf360c04360ae48fd0d68b6d`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca62e39536ad2825e9d1db7dbfa88f4cbc9d95659c5fb45691fa224654d2629`  
		Last Modified: Wed, 11 Mar 2020 21:58:49 GMT  
		Size: 59.9 MB (59927053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a96da9a069c4780e3c46bcbd35f4da5d0e173b2888bec333941260f131ccc8`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202349aaae9b658c7d87822ac340735af35c35495f6af77e5db0df2d253880ea`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f43ed55770aa202e0a559ef5505907bdf9e16eb7ea47829463da52a02907f9c`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466cffcfbb54d45db4bfc4d2a4ef125228d8adaa890f4bdf1b64c9305a00e67b`  
		Last Modified: Wed, 11 Mar 2020 21:59:01 GMT  
		Size: 2.9 MB (2878539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6759e573461d1a01a039d460c93cc7394fc6503dcbb5a199b318c51ea84a5b7`  
		Last Modified: Wed, 11 Mar 2020 21:59:00 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62db51a4792cce56454199be1d125345ae07f763e4fda4f56a955259f1ecba93`  
		Last Modified: Wed, 11 Mar 2020 21:59:00 GMT  
		Size: 754.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600fa87244d5da05152b4c389cc3f37aaf0b36cb70a7d0d4294feaeb52abbd12`  
		Last Modified: Wed, 11 Mar 2020 21:59:00 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.8-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6fcdb8d75a9f4a6ee01e57720cb5543bd81035db06ec821383dfde6a4371389e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68163443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac71857cf4ec95c719133d716baecc805697ff6ca79086a80b6e14a77d43d3bc`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 02:23:05 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 02:23:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 02:23:12 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:39:44 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:39:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:39:52 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:39:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:39:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:39:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:39:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:39:56 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:40:05 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Mar 2020 21:40:08 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:40:08 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Mar 2020 21:40:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Mar 2020 21:40:10 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:40:11 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Mar 2020 21:40:12 GMT
EXPOSE 2375 2376
# Wed, 11 Mar 2020 21:40:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Mar 2020 21:40:13 GMT
CMD []
```

-	Layers:
	-	`sha256:8fa90b21c985a6fcfff966bdfbde81cdd088de0aa8af38110057f6ac408f4408`  
		Last Modified: Sat, 18 Jan 2020 01:40:23 GMT  
		Size: 2.7 MB (2723075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2917335fcb0a6856d5bf55430ba707c2c1378029a109e61959e62d2769230db`  
		Last Modified: Sat, 18 Jan 2020 02:25:35 GMT  
		Size: 2.4 MB (2445713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d3c84c2515134ddfa5ae5bac6e140953e9576fcd30a0bbc10fbc565d267895`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a828ac2f8d0e08bfd3c5405031bb245a21e469671397bd03e8868ce0925d9f49`  
		Last Modified: Wed, 11 Mar 2020 21:40:56 GMT  
		Size: 57.4 MB (57387269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7b0e4ac96f123613bb6ebd37a1bb99fb6f8a12b1d521f89f4211a970dbc077`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25581ce9dd66a29fecb3a63c9f888a0c6e3c68de7002441092b6a41dd833e995`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc58c5fdb432f00e6a7cdfa6b6507ca3c8598ab0612730e109e4faf5b0fc2d5a`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d396bfbbbaa91436006cf0e8b86b9e00c9e49a1dcbcd557c3fc331afc8e9e2f3`  
		Last Modified: Wed, 11 Mar 2020 21:41:09 GMT  
		Size: 5.6 MB (5600915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3bdb37e40cba208e5d80d500a33700bdff3ad30ebbfcb014c89a614506038d`  
		Last Modified: Wed, 11 Mar 2020 21:41:07 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269e23372e2e87311644e618cb3e6c09eae4cc41d919662298578a9abfe476ed`  
		Last Modified: Wed, 11 Mar 2020 21:41:07 GMT  
		Size: 758.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6204a0f4fef03aefb0b6ae2c7dfee680f8a6d84e0f59324ded513c256255723`  
		Last Modified: Wed, 11 Mar 2020 21:41:07 GMT  
		Size: 2.5 KB (2535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03.8-dind-rootless`

```console
$ docker pull docker@sha256:b1ba6b5c5d00fdfbf812971cbeb72a81bbb9fca8f70a1809b68c74968a49849c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:19.03.8-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:e0fbfc60a11eae3ce35434bd72828bf2d74b711dd3fd309ee36f646d69fd30a4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.6 MB (98553507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131e19ccffdf6245ad57a0ca98e0abd6e6cc5eb4495fe9358f90e1c9837de9c5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 04:42:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 04:42:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:19:32 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:19:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:19:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:39 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:19:45 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Mar 2020 21:19:45 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:19:46 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Mar 2020 21:19:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Mar 2020 21:19:47 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:47 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Mar 2020 21:19:47 GMT
EXPOSE 2375 2376
# Wed, 11 Mar 2020 21:19:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:47 GMT
CMD []
# Wed, 11 Mar 2020 21:19:52 GMT
RUN apk add --no-cache iproute2
# Wed, 11 Mar 2020 21:19:53 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Wed, 11 Mar 2020 21:19:54 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:19:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O rootless.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-rootless-extras-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-rootless-extras-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		vpnkit --version
# Wed, 11 Mar 2020 21:19:56 GMT
ENV ROOTLESSKIT_VERSION=0.9.1
# Wed, 11 Mar 2020 21:20:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .rootlesskit-build-deps 		go 		libc-dev 	; 	wget -O rootlesskit.tgz "https://github.com/rootless-containers/rootlesskit/archive/v${ROOTLESSKIT_VERSION}.tar.gz"; 	export GOPATH='/go'; mkdir "$GOPATH"; 	mkdir -p "$GOPATH/src/github.com/rootless-containers/rootlesskit"; 	tar --extract --file rootlesskit.tgz --directory "$GOPATH/src/github.com/rootless-containers/rootlesskit" --strip-components 1; 	rm rootlesskit.tgz; 	go build -o /usr/local/bin/rootlesskit github.com/rootless-containers/rootlesskit/cmd/rootlesskit; 	go build -o /usr/local/bin/rootlesskit-docker-proxy github.com/rootless-containers/rootlesskit/cmd/rootlesskit-docker-proxy; 	rm -rf "$GOPATH"; 	apk del --no-network .rootlesskit-build-deps; 	rootlesskit --version
# Wed, 11 Mar 2020 21:20:08 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Wed, 11 Mar 2020 21:20:09 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 11 Mar 2020 21:20:09 GMT
USER rootless
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd54125436dc48e0d60096d61457bcfd886136eb67815a60210ec67d3793096f`  
		Last Modified: Sat, 18 Jan 2020 04:43:03 GMT  
		Size: 2.4 MB (2425150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d1554c15cbb8c6b81fd21a057c8e97749fb24fd5befeb94ad960d3a350f91f`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dd17ef2c28fbb77b8b589e2e601e3ce86c0b9bcdb9dc73b6330d7ca16dca19`  
		Last Modified: Wed, 11 Mar 2020 21:20:40 GMT  
		Size: 64.2 MB (64218865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca57ea69baf170d62b8d1a51d898ff8d9383e22cd18bbde168ff539e74be8a4`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3af031952ce6719d5ca2f369b2187e1819fdab00252d315555a00048d6b99b7`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29377cccb214061fb46c1d5a1c27f53c366384d34f168cdb8484f5c7fcfb87a`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4939ff19fbb72e09aad6b10bc7440f9b23e0983f05c3cf6679a6392a40103b27`  
		Last Modified: Wed, 11 Mar 2020 21:20:48 GMT  
		Size: 5.6 MB (5598354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617664eed4c7060ec14f8178529d17b8a637b33a19f65101e062e185feda4c1`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8b6f7ec5ec983309648ff91b432c6abc38b547fc0610e3d81ab7e2472ad7ae`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 756.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb8de5d1a5be108527d435aef60a4a041879e0ddcf6d747ff324d57a5000f03`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 2.5 KB (2536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af40291eab6e7e25f86e0b385342cfe0318d38212a55bc20dd0aef9d3cc1a708`  
		Last Modified: Wed, 11 Mar 2020 21:20:56 GMT  
		Size: 796.0 KB (796003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd959232e7eccc0e2cb0117fb87809c0a4750269e1486a4ded4cbcff13c7b088`  
		Last Modified: Wed, 11 Mar 2020 21:20:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82aa1d69b9f04b015fb9771d9751d1e6cfe72d91da8d347c8bb83bde351f464b`  
		Last Modified: Wed, 11 Mar 2020 21:20:55 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cdb51a3ef0eb7411052a13cb5c1f4dbcb005a502d6805092f9d0006a963ad7`  
		Last Modified: Wed, 11 Mar 2020 21:20:57 GMT  
		Size: 9.1 MB (9109448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420ff93d35ca71a9e8a6fcfab5be9089f24b654a6c2c9f0fc46727937a534447`  
		Last Modified: Wed, 11 Mar 2020 21:20:57 GMT  
		Size: 13.6 MB (13594708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc08146368fd44217f9c582fc83a67d4d4b6844c8a9ed76700b579a514f8a4a`  
		Last Modified: Wed, 11 Mar 2020 21:20:54 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03.8-git`

```console
$ docker pull docker@sha256:4690f87ef12b57befc03948cfb45125e727469c886ce306268985ffc10c5f117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19.03.8-git` - linux; amd64

```console
$ docker pull docker@sha256:cb428bf67ff328e9cd57b5bbb64f04da465ef3198fbb8b0f0eb539144812cfe7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77662702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147d7d578318b63c7d01ee26605a981701192c4d365a7b72557655cae9225598`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 04:42:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 04:42:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:19:32 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:19:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:19:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:39 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:20:16 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd54125436dc48e0d60096d61457bcfd886136eb67815a60210ec67d3793096f`  
		Last Modified: Sat, 18 Jan 2020 04:43:03 GMT  
		Size: 2.4 MB (2425150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d1554c15cbb8c6b81fd21a057c8e97749fb24fd5befeb94ad960d3a350f91f`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dd17ef2c28fbb77b8b589e2e601e3ce86c0b9bcdb9dc73b6330d7ca16dca19`  
		Last Modified: Wed, 11 Mar 2020 21:20:40 GMT  
		Size: 64.2 MB (64218865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca57ea69baf170d62b8d1a51d898ff8d9383e22cd18bbde168ff539e74be8a4`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3af031952ce6719d5ca2f369b2187e1819fdab00252d315555a00048d6b99b7`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29377cccb214061fb46c1d5a1c27f53c366384d34f168cdb8484f5c7fcfb87a`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254b360be85b0840ff05885a92f88a8c9953477f040fda3328e6ea8eea86de6a`  
		Last Modified: Wed, 11 Mar 2020 21:21:05 GMT  
		Size: 8.2 MB (8213895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.8-git` - linux; arm variant v6

```console
$ docker pull docker@sha256:e1850f9ae57922ee14a032dbf923d1efc8d553b02760378f562f1fb4fd2e499f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72737200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0522fe2ee7c4d185a532637aef5842258a77b0c068ec510a1ed61c9b78774eef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 05:52:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 05:52:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 05:52:35 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:49:22 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:49:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:49:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:49:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:49:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:49:38 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:50:01 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c86f804e7b5cc2f1f9d87340dfef1fcc13615f2cbd25bda470e513c1e4a627`  
		Last Modified: Sat, 18 Jan 2020 05:54:22 GMT  
		Size: 2.4 MB (2355405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d84775c03f92068112e3757afd6ddab1b2c0a3d1073e91b182620b6ec239f7`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592a77d3ce3aac4cb4c252c866f4a65c1541726b2bbdb512444569119b5cd98e`  
		Last Modified: Wed, 11 Mar 2020 21:50:37 GMT  
		Size: 59.9 MB (59927165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0277ab691262af1bf0bf50d6d459874dbf48509a6103991fd9d6225e455cb995`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320285a35393ed08c2ed85f5dc6d6ca6a1c07ac14fcfb8b4e1e5c5a4c30eace9`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e82c58148faac404a83fad42819c701567beb61dac6c2ae6d76ac1f97eefccd`  
		Last Modified: Wed, 11 Mar 2020 21:50:18 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162f34f6eb0f7762945f1e6a261e992d3923e55044cafaff16656007c3811c1d`  
		Last Modified: Wed, 11 Mar 2020 21:51:04 GMT  
		Size: 7.8 MB (7835202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.8-git` - linux; arm variant v7

```console
$ docker pull docker@sha256:f47ed269de366a810d8e18b4df194fbcc6da43c3124ddaf516bb432d61b02804
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71675688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f090014780387159e6d1ca5236562fa2a275f196b6d7aba5d5afb8f3ad86a989`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:01:09 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 03:01:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 03:01:20 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:57:34 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:57:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:57:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:57:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:57:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:57:48 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:58:12 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5014010b799b2f3cc6305fd21cc4b096dd28ad093e165cea5976f92ccb8c462`  
		Last Modified: Sat, 18 Jan 2020 03:03:27 GMT  
		Size: 2.3 MB (2254397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f49247ef05003d569c198c4908b849fdadd330bf360c04360ae48fd0d68b6d`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca62e39536ad2825e9d1db7dbfa88f4cbc9d95659c5fb45691fa224654d2629`  
		Last Modified: Wed, 11 Mar 2020 21:58:49 GMT  
		Size: 59.9 MB (59927053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a96da9a069c4780e3c46bcbd35f4da5d0e173b2888bec333941260f131ccc8`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202349aaae9b658c7d87822ac340735af35c35495f6af77e5db0df2d253880ea`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f43ed55770aa202e0a559ef5505907bdf9e16eb7ea47829463da52a02907f9c`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877200202589a73b4d16451308a3e44508cb4df920be69143f584e1d64407f4c`  
		Last Modified: Wed, 11 Mar 2020 21:59:14 GMT  
		Size: 7.1 MB (7072817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.8-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e940117143b12b2eac9c5565eda0db3bdf8d6f0a13068832eb96d84cafded257
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70963946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08226ded6b73a3e1734672484ecb773d61e8a1e9f50bf7e6f7cfa49ef1056e22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 02:23:05 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 02:23:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 02:23:12 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:39:44 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:39:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:39:52 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:39:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:39:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:39:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:39:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:39:56 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:40:21 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:8fa90b21c985a6fcfff966bdfbde81cdd088de0aa8af38110057f6ac408f4408`  
		Last Modified: Sat, 18 Jan 2020 01:40:23 GMT  
		Size: 2.7 MB (2723075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2917335fcb0a6856d5bf55430ba707c2c1378029a109e61959e62d2769230db`  
		Last Modified: Sat, 18 Jan 2020 02:25:35 GMT  
		Size: 2.4 MB (2445713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d3c84c2515134ddfa5ae5bac6e140953e9576fcd30a0bbc10fbc565d267895`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a828ac2f8d0e08bfd3c5405031bb245a21e469671397bd03e8868ce0925d9f49`  
		Last Modified: Wed, 11 Mar 2020 21:40:56 GMT  
		Size: 57.4 MB (57387269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7b0e4ac96f123613bb6ebd37a1bb99fb6f8a12b1d521f89f4211a970dbc077`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25581ce9dd66a29fecb3a63c9f888a0c6e3c68de7002441092b6a41dd833e995`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc58c5fdb432f00e6a7cdfa6b6507ca3c8598ab0612730e109e4faf5b0fc2d5a`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e0a8bd53622c572d715e352539b455c6a81b69ed96893f228292d785c5051f`  
		Last Modified: Wed, 11 Mar 2020 21:41:22 GMT  
		Size: 8.4 MB (8406022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03-dind`

```console
$ docker pull docker@sha256:308dcf9380af44ea492736e8d59605cd0ff2dab0527073f7e718ee4498e85dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19.03-dind` - linux; amd64

```console
$ docker pull docker@sha256:0e6d34042007a6f5280838dc045af0d600654b57cd367251d1dd8bba4b55c773
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75051735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe98abf5dda7ec569bc4821f20ceca66945e67882fe32f960fb8b8f179af0e42`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 04:42:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 04:42:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:19:32 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:19:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:19:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:39 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:19:45 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Mar 2020 21:19:45 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:19:46 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Mar 2020 21:19:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Mar 2020 21:19:47 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:47 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Mar 2020 21:19:47 GMT
EXPOSE 2375 2376
# Wed, 11 Mar 2020 21:19:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:47 GMT
CMD []
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd54125436dc48e0d60096d61457bcfd886136eb67815a60210ec67d3793096f`  
		Last Modified: Sat, 18 Jan 2020 04:43:03 GMT  
		Size: 2.4 MB (2425150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d1554c15cbb8c6b81fd21a057c8e97749fb24fd5befeb94ad960d3a350f91f`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dd17ef2c28fbb77b8b589e2e601e3ce86c0b9bcdb9dc73b6330d7ca16dca19`  
		Last Modified: Wed, 11 Mar 2020 21:20:40 GMT  
		Size: 64.2 MB (64218865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca57ea69baf170d62b8d1a51d898ff8d9383e22cd18bbde168ff539e74be8a4`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3af031952ce6719d5ca2f369b2187e1819fdab00252d315555a00048d6b99b7`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29377cccb214061fb46c1d5a1c27f53c366384d34f168cdb8484f5c7fcfb87a`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4939ff19fbb72e09aad6b10bc7440f9b23e0983f05c3cf6679a6392a40103b27`  
		Last Modified: Wed, 11 Mar 2020 21:20:48 GMT  
		Size: 5.6 MB (5598354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617664eed4c7060ec14f8178529d17b8a637b33a19f65101e062e185feda4c1`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8b6f7ec5ec983309648ff91b432c6abc38b547fc0610e3d81ab7e2472ad7ae`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 756.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb8de5d1a5be108527d435aef60a4a041879e0ddcf6d747ff324d57a5000f03`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 2.5 KB (2536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:04246f289e63b1bc0baf3ee051e2374497207183b9e5b86373aa2f8938893a6c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68121997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08fff432f3d4cd1dae7778792ad2daa258d095691556f760fe82584bb66fa2b8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 05:52:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 05:52:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 05:52:35 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:49:22 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:49:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:49:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:49:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:49:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:49:38 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:49:46 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Mar 2020 21:49:48 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:49:49 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Mar 2020 21:49:51 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Mar 2020 21:49:51 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:49:52 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Mar 2020 21:49:52 GMT
EXPOSE 2375 2376
# Wed, 11 Mar 2020 21:49:53 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Mar 2020 21:49:53 GMT
CMD []
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c86f804e7b5cc2f1f9d87340dfef1fcc13615f2cbd25bda470e513c1e4a627`  
		Last Modified: Sat, 18 Jan 2020 05:54:22 GMT  
		Size: 2.4 MB (2355405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d84775c03f92068112e3757afd6ddab1b2c0a3d1073e91b182620b6ec239f7`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592a77d3ce3aac4cb4c252c866f4a65c1541726b2bbdb512444569119b5cd98e`  
		Last Modified: Wed, 11 Mar 2020 21:50:37 GMT  
		Size: 59.9 MB (59927165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0277ab691262af1bf0bf50d6d459874dbf48509a6103991fd9d6225e455cb995`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320285a35393ed08c2ed85f5dc6d6ca6a1c07ac14fcfb8b4e1e5c5a4c30eace9`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e82c58148faac404a83fad42819c701567beb61dac6c2ae6d76ac1f97eefccd`  
		Last Modified: Wed, 11 Mar 2020 21:50:18 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b1648a96394c26b0e7d5c254c39b36c8eca6d00dfff5aa3776cb6671284ead`  
		Last Modified: Wed, 11 Mar 2020 21:50:49 GMT  
		Size: 3.2 MB (3215398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e63bc9624da4519af0d163fc47db94ef5d7d0ae27deccb9d6b923ba97710251`  
		Last Modified: Wed, 11 Mar 2020 21:50:48 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8f7907ef28cfa8968f389a0e60d2b4a98f2b9da2963e09d86911a36e945825`  
		Last Modified: Wed, 11 Mar 2020 21:50:48 GMT  
		Size: 754.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013cac041612fcb3b3db97e63f70c7f357b31618cd79f2a0852b38181355f5bd`  
		Last Modified: Wed, 11 Mar 2020 21:50:48 GMT  
		Size: 2.5 KB (2532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:c2d6834d581a10f8d30ae8678d859ad15a3747335051665f21dbe7e602568a8a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67486006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd179934e0f1561bdac8a67db9bf33af7be9c1f7508bdb0c7aa76184817e0d62`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:01:09 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 03:01:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 03:01:20 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:57:34 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:57:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:57:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:57:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:57:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:57:48 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:57:57 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Mar 2020 21:57:59 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:58:00 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Mar 2020 21:58:02 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Mar 2020 21:58:02 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:58:03 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Mar 2020 21:58:03 GMT
EXPOSE 2375 2376
# Wed, 11 Mar 2020 21:58:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Mar 2020 21:58:05 GMT
CMD []
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5014010b799b2f3cc6305fd21cc4b096dd28ad093e165cea5976f92ccb8c462`  
		Last Modified: Sat, 18 Jan 2020 03:03:27 GMT  
		Size: 2.3 MB (2254397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f49247ef05003d569c198c4908b849fdadd330bf360c04360ae48fd0d68b6d`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca62e39536ad2825e9d1db7dbfa88f4cbc9d95659c5fb45691fa224654d2629`  
		Last Modified: Wed, 11 Mar 2020 21:58:49 GMT  
		Size: 59.9 MB (59927053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a96da9a069c4780e3c46bcbd35f4da5d0e173b2888bec333941260f131ccc8`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202349aaae9b658c7d87822ac340735af35c35495f6af77e5db0df2d253880ea`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f43ed55770aa202e0a559ef5505907bdf9e16eb7ea47829463da52a02907f9c`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466cffcfbb54d45db4bfc4d2a4ef125228d8adaa890f4bdf1b64c9305a00e67b`  
		Last Modified: Wed, 11 Mar 2020 21:59:01 GMT  
		Size: 2.9 MB (2878539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6759e573461d1a01a039d460c93cc7394fc6503dcbb5a199b318c51ea84a5b7`  
		Last Modified: Wed, 11 Mar 2020 21:59:00 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62db51a4792cce56454199be1d125345ae07f763e4fda4f56a955259f1ecba93`  
		Last Modified: Wed, 11 Mar 2020 21:59:00 GMT  
		Size: 754.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600fa87244d5da05152b4c389cc3f37aaf0b36cb70a7d0d4294feaeb52abbd12`  
		Last Modified: Wed, 11 Mar 2020 21:59:00 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6fcdb8d75a9f4a6ee01e57720cb5543bd81035db06ec821383dfde6a4371389e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68163443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac71857cf4ec95c719133d716baecc805697ff6ca79086a80b6e14a77d43d3bc`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 02:23:05 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 02:23:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 02:23:12 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:39:44 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:39:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:39:52 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:39:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:39:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:39:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:39:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:39:56 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:40:05 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Mar 2020 21:40:08 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:40:08 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Mar 2020 21:40:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Mar 2020 21:40:10 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:40:11 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Mar 2020 21:40:12 GMT
EXPOSE 2375 2376
# Wed, 11 Mar 2020 21:40:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Mar 2020 21:40:13 GMT
CMD []
```

-	Layers:
	-	`sha256:8fa90b21c985a6fcfff966bdfbde81cdd088de0aa8af38110057f6ac408f4408`  
		Last Modified: Sat, 18 Jan 2020 01:40:23 GMT  
		Size: 2.7 MB (2723075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2917335fcb0a6856d5bf55430ba707c2c1378029a109e61959e62d2769230db`  
		Last Modified: Sat, 18 Jan 2020 02:25:35 GMT  
		Size: 2.4 MB (2445713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d3c84c2515134ddfa5ae5bac6e140953e9576fcd30a0bbc10fbc565d267895`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a828ac2f8d0e08bfd3c5405031bb245a21e469671397bd03e8868ce0925d9f49`  
		Last Modified: Wed, 11 Mar 2020 21:40:56 GMT  
		Size: 57.4 MB (57387269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7b0e4ac96f123613bb6ebd37a1bb99fb6f8a12b1d521f89f4211a970dbc077`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25581ce9dd66a29fecb3a63c9f888a0c6e3c68de7002441092b6a41dd833e995`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc58c5fdb432f00e6a7cdfa6b6507ca3c8598ab0612730e109e4faf5b0fc2d5a`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d396bfbbbaa91436006cf0e8b86b9e00c9e49a1dcbcd557c3fc331afc8e9e2f3`  
		Last Modified: Wed, 11 Mar 2020 21:41:09 GMT  
		Size: 5.6 MB (5600915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3bdb37e40cba208e5d80d500a33700bdff3ad30ebbfcb014c89a614506038d`  
		Last Modified: Wed, 11 Mar 2020 21:41:07 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269e23372e2e87311644e618cb3e6c09eae4cc41d919662298578a9abfe476ed`  
		Last Modified: Wed, 11 Mar 2020 21:41:07 GMT  
		Size: 758.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6204a0f4fef03aefb0b6ae2c7dfee680f8a6d84e0f59324ded513c256255723`  
		Last Modified: Wed, 11 Mar 2020 21:41:07 GMT  
		Size: 2.5 KB (2535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03-dind-rootless`

```console
$ docker pull docker@sha256:b1ba6b5c5d00fdfbf812971cbeb72a81bbb9fca8f70a1809b68c74968a49849c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:19.03-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:e0fbfc60a11eae3ce35434bd72828bf2d74b711dd3fd309ee36f646d69fd30a4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.6 MB (98553507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131e19ccffdf6245ad57a0ca98e0abd6e6cc5eb4495fe9358f90e1c9837de9c5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 04:42:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 04:42:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:19:32 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:19:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:19:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:39 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:19:45 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Mar 2020 21:19:45 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:19:46 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Mar 2020 21:19:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Mar 2020 21:19:47 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:47 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Mar 2020 21:19:47 GMT
EXPOSE 2375 2376
# Wed, 11 Mar 2020 21:19:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:47 GMT
CMD []
# Wed, 11 Mar 2020 21:19:52 GMT
RUN apk add --no-cache iproute2
# Wed, 11 Mar 2020 21:19:53 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Wed, 11 Mar 2020 21:19:54 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:19:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O rootless.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-rootless-extras-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-rootless-extras-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		vpnkit --version
# Wed, 11 Mar 2020 21:19:56 GMT
ENV ROOTLESSKIT_VERSION=0.9.1
# Wed, 11 Mar 2020 21:20:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .rootlesskit-build-deps 		go 		libc-dev 	; 	wget -O rootlesskit.tgz "https://github.com/rootless-containers/rootlesskit/archive/v${ROOTLESSKIT_VERSION}.tar.gz"; 	export GOPATH='/go'; mkdir "$GOPATH"; 	mkdir -p "$GOPATH/src/github.com/rootless-containers/rootlesskit"; 	tar --extract --file rootlesskit.tgz --directory "$GOPATH/src/github.com/rootless-containers/rootlesskit" --strip-components 1; 	rm rootlesskit.tgz; 	go build -o /usr/local/bin/rootlesskit github.com/rootless-containers/rootlesskit/cmd/rootlesskit; 	go build -o /usr/local/bin/rootlesskit-docker-proxy github.com/rootless-containers/rootlesskit/cmd/rootlesskit-docker-proxy; 	rm -rf "$GOPATH"; 	apk del --no-network .rootlesskit-build-deps; 	rootlesskit --version
# Wed, 11 Mar 2020 21:20:08 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Wed, 11 Mar 2020 21:20:09 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 11 Mar 2020 21:20:09 GMT
USER rootless
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd54125436dc48e0d60096d61457bcfd886136eb67815a60210ec67d3793096f`  
		Last Modified: Sat, 18 Jan 2020 04:43:03 GMT  
		Size: 2.4 MB (2425150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d1554c15cbb8c6b81fd21a057c8e97749fb24fd5befeb94ad960d3a350f91f`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dd17ef2c28fbb77b8b589e2e601e3ce86c0b9bcdb9dc73b6330d7ca16dca19`  
		Last Modified: Wed, 11 Mar 2020 21:20:40 GMT  
		Size: 64.2 MB (64218865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca57ea69baf170d62b8d1a51d898ff8d9383e22cd18bbde168ff539e74be8a4`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3af031952ce6719d5ca2f369b2187e1819fdab00252d315555a00048d6b99b7`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29377cccb214061fb46c1d5a1c27f53c366384d34f168cdb8484f5c7fcfb87a`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4939ff19fbb72e09aad6b10bc7440f9b23e0983f05c3cf6679a6392a40103b27`  
		Last Modified: Wed, 11 Mar 2020 21:20:48 GMT  
		Size: 5.6 MB (5598354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617664eed4c7060ec14f8178529d17b8a637b33a19f65101e062e185feda4c1`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8b6f7ec5ec983309648ff91b432c6abc38b547fc0610e3d81ab7e2472ad7ae`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 756.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb8de5d1a5be108527d435aef60a4a041879e0ddcf6d747ff324d57a5000f03`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 2.5 KB (2536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af40291eab6e7e25f86e0b385342cfe0318d38212a55bc20dd0aef9d3cc1a708`  
		Last Modified: Wed, 11 Mar 2020 21:20:56 GMT  
		Size: 796.0 KB (796003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd959232e7eccc0e2cb0117fb87809c0a4750269e1486a4ded4cbcff13c7b088`  
		Last Modified: Wed, 11 Mar 2020 21:20:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82aa1d69b9f04b015fb9771d9751d1e6cfe72d91da8d347c8bb83bde351f464b`  
		Last Modified: Wed, 11 Mar 2020 21:20:55 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cdb51a3ef0eb7411052a13cb5c1f4dbcb005a502d6805092f9d0006a963ad7`  
		Last Modified: Wed, 11 Mar 2020 21:20:57 GMT  
		Size: 9.1 MB (9109448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420ff93d35ca71a9e8a6fcfab5be9089f24b654a6c2c9f0fc46727937a534447`  
		Last Modified: Wed, 11 Mar 2020 21:20:57 GMT  
		Size: 13.6 MB (13594708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc08146368fd44217f9c582fc83a67d4d4b6844c8a9ed76700b579a514f8a4a`  
		Last Modified: Wed, 11 Mar 2020 21:20:54 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03-git`

```console
$ docker pull docker@sha256:4690f87ef12b57befc03948cfb45125e727469c886ce306268985ffc10c5f117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19.03-git` - linux; amd64

```console
$ docker pull docker@sha256:cb428bf67ff328e9cd57b5bbb64f04da465ef3198fbb8b0f0eb539144812cfe7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77662702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147d7d578318b63c7d01ee26605a981701192c4d365a7b72557655cae9225598`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 04:42:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 04:42:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:19:32 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:19:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:19:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:39 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:20:16 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd54125436dc48e0d60096d61457bcfd886136eb67815a60210ec67d3793096f`  
		Last Modified: Sat, 18 Jan 2020 04:43:03 GMT  
		Size: 2.4 MB (2425150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d1554c15cbb8c6b81fd21a057c8e97749fb24fd5befeb94ad960d3a350f91f`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dd17ef2c28fbb77b8b589e2e601e3ce86c0b9bcdb9dc73b6330d7ca16dca19`  
		Last Modified: Wed, 11 Mar 2020 21:20:40 GMT  
		Size: 64.2 MB (64218865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca57ea69baf170d62b8d1a51d898ff8d9383e22cd18bbde168ff539e74be8a4`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3af031952ce6719d5ca2f369b2187e1819fdab00252d315555a00048d6b99b7`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29377cccb214061fb46c1d5a1c27f53c366384d34f168cdb8484f5c7fcfb87a`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254b360be85b0840ff05885a92f88a8c9953477f040fda3328e6ea8eea86de6a`  
		Last Modified: Wed, 11 Mar 2020 21:21:05 GMT  
		Size: 8.2 MB (8213895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03-git` - linux; arm variant v6

```console
$ docker pull docker@sha256:e1850f9ae57922ee14a032dbf923d1efc8d553b02760378f562f1fb4fd2e499f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72737200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0522fe2ee7c4d185a532637aef5842258a77b0c068ec510a1ed61c9b78774eef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 05:52:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 05:52:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 05:52:35 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:49:22 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:49:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:49:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:49:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:49:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:49:38 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:50:01 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c86f804e7b5cc2f1f9d87340dfef1fcc13615f2cbd25bda470e513c1e4a627`  
		Last Modified: Sat, 18 Jan 2020 05:54:22 GMT  
		Size: 2.4 MB (2355405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d84775c03f92068112e3757afd6ddab1b2c0a3d1073e91b182620b6ec239f7`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592a77d3ce3aac4cb4c252c866f4a65c1541726b2bbdb512444569119b5cd98e`  
		Last Modified: Wed, 11 Mar 2020 21:50:37 GMT  
		Size: 59.9 MB (59927165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0277ab691262af1bf0bf50d6d459874dbf48509a6103991fd9d6225e455cb995`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320285a35393ed08c2ed85f5dc6d6ca6a1c07ac14fcfb8b4e1e5c5a4c30eace9`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e82c58148faac404a83fad42819c701567beb61dac6c2ae6d76ac1f97eefccd`  
		Last Modified: Wed, 11 Mar 2020 21:50:18 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162f34f6eb0f7762945f1e6a261e992d3923e55044cafaff16656007c3811c1d`  
		Last Modified: Wed, 11 Mar 2020 21:51:04 GMT  
		Size: 7.8 MB (7835202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03-git` - linux; arm variant v7

```console
$ docker pull docker@sha256:f47ed269de366a810d8e18b4df194fbcc6da43c3124ddaf516bb432d61b02804
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71675688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f090014780387159e6d1ca5236562fa2a275f196b6d7aba5d5afb8f3ad86a989`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:01:09 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 03:01:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 03:01:20 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:57:34 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:57:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:57:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:57:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:57:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:57:48 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:58:12 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5014010b799b2f3cc6305fd21cc4b096dd28ad093e165cea5976f92ccb8c462`  
		Last Modified: Sat, 18 Jan 2020 03:03:27 GMT  
		Size: 2.3 MB (2254397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f49247ef05003d569c198c4908b849fdadd330bf360c04360ae48fd0d68b6d`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca62e39536ad2825e9d1db7dbfa88f4cbc9d95659c5fb45691fa224654d2629`  
		Last Modified: Wed, 11 Mar 2020 21:58:49 GMT  
		Size: 59.9 MB (59927053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a96da9a069c4780e3c46bcbd35f4da5d0e173b2888bec333941260f131ccc8`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202349aaae9b658c7d87822ac340735af35c35495f6af77e5db0df2d253880ea`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f43ed55770aa202e0a559ef5505907bdf9e16eb7ea47829463da52a02907f9c`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877200202589a73b4d16451308a3e44508cb4df920be69143f584e1d64407f4c`  
		Last Modified: Wed, 11 Mar 2020 21:59:14 GMT  
		Size: 7.1 MB (7072817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e940117143b12b2eac9c5565eda0db3bdf8d6f0a13068832eb96d84cafded257
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70963946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08226ded6b73a3e1734672484ecb773d61e8a1e9f50bf7e6f7cfa49ef1056e22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 02:23:05 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 02:23:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 02:23:12 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:39:44 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:39:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:39:52 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:39:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:39:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:39:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:39:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:39:56 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:40:21 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:8fa90b21c985a6fcfff966bdfbde81cdd088de0aa8af38110057f6ac408f4408`  
		Last Modified: Sat, 18 Jan 2020 01:40:23 GMT  
		Size: 2.7 MB (2723075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2917335fcb0a6856d5bf55430ba707c2c1378029a109e61959e62d2769230db`  
		Last Modified: Sat, 18 Jan 2020 02:25:35 GMT  
		Size: 2.4 MB (2445713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d3c84c2515134ddfa5ae5bac6e140953e9576fcd30a0bbc10fbc565d267895`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a828ac2f8d0e08bfd3c5405031bb245a21e469671397bd03e8868ce0925d9f49`  
		Last Modified: Wed, 11 Mar 2020 21:40:56 GMT  
		Size: 57.4 MB (57387269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7b0e4ac96f123613bb6ebd37a1bb99fb6f8a12b1d521f89f4211a970dbc077`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25581ce9dd66a29fecb3a63c9f888a0c6e3c68de7002441092b6a41dd833e995`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc58c5fdb432f00e6a7cdfa6b6507ca3c8598ab0612730e109e4faf5b0fc2d5a`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e0a8bd53622c572d715e352539b455c6a81b69ed96893f228292d785c5051f`  
		Last Modified: Wed, 11 Mar 2020 21:41:22 GMT  
		Size: 8.4 MB (8406022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19-dind`

```console
$ docker pull docker@sha256:308dcf9380af44ea492736e8d59605cd0ff2dab0527073f7e718ee4498e85dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19-dind` - linux; amd64

```console
$ docker pull docker@sha256:0e6d34042007a6f5280838dc045af0d600654b57cd367251d1dd8bba4b55c773
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75051735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe98abf5dda7ec569bc4821f20ceca66945e67882fe32f960fb8b8f179af0e42`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 04:42:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 04:42:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:19:32 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:19:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:19:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:39 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:19:45 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Mar 2020 21:19:45 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:19:46 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Mar 2020 21:19:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Mar 2020 21:19:47 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:47 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Mar 2020 21:19:47 GMT
EXPOSE 2375 2376
# Wed, 11 Mar 2020 21:19:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:47 GMT
CMD []
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd54125436dc48e0d60096d61457bcfd886136eb67815a60210ec67d3793096f`  
		Last Modified: Sat, 18 Jan 2020 04:43:03 GMT  
		Size: 2.4 MB (2425150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d1554c15cbb8c6b81fd21a057c8e97749fb24fd5befeb94ad960d3a350f91f`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dd17ef2c28fbb77b8b589e2e601e3ce86c0b9bcdb9dc73b6330d7ca16dca19`  
		Last Modified: Wed, 11 Mar 2020 21:20:40 GMT  
		Size: 64.2 MB (64218865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca57ea69baf170d62b8d1a51d898ff8d9383e22cd18bbde168ff539e74be8a4`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3af031952ce6719d5ca2f369b2187e1819fdab00252d315555a00048d6b99b7`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29377cccb214061fb46c1d5a1c27f53c366384d34f168cdb8484f5c7fcfb87a`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4939ff19fbb72e09aad6b10bc7440f9b23e0983f05c3cf6679a6392a40103b27`  
		Last Modified: Wed, 11 Mar 2020 21:20:48 GMT  
		Size: 5.6 MB (5598354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617664eed4c7060ec14f8178529d17b8a637b33a19f65101e062e185feda4c1`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8b6f7ec5ec983309648ff91b432c6abc38b547fc0610e3d81ab7e2472ad7ae`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 756.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb8de5d1a5be108527d435aef60a4a041879e0ddcf6d747ff324d57a5000f03`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 2.5 KB (2536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:04246f289e63b1bc0baf3ee051e2374497207183b9e5b86373aa2f8938893a6c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68121997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08fff432f3d4cd1dae7778792ad2daa258d095691556f760fe82584bb66fa2b8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 05:52:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 05:52:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 05:52:35 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:49:22 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:49:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:49:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:49:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:49:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:49:38 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:49:46 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Mar 2020 21:49:48 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:49:49 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Mar 2020 21:49:51 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Mar 2020 21:49:51 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:49:52 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Mar 2020 21:49:52 GMT
EXPOSE 2375 2376
# Wed, 11 Mar 2020 21:49:53 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Mar 2020 21:49:53 GMT
CMD []
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c86f804e7b5cc2f1f9d87340dfef1fcc13615f2cbd25bda470e513c1e4a627`  
		Last Modified: Sat, 18 Jan 2020 05:54:22 GMT  
		Size: 2.4 MB (2355405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d84775c03f92068112e3757afd6ddab1b2c0a3d1073e91b182620b6ec239f7`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592a77d3ce3aac4cb4c252c866f4a65c1541726b2bbdb512444569119b5cd98e`  
		Last Modified: Wed, 11 Mar 2020 21:50:37 GMT  
		Size: 59.9 MB (59927165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0277ab691262af1bf0bf50d6d459874dbf48509a6103991fd9d6225e455cb995`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320285a35393ed08c2ed85f5dc6d6ca6a1c07ac14fcfb8b4e1e5c5a4c30eace9`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e82c58148faac404a83fad42819c701567beb61dac6c2ae6d76ac1f97eefccd`  
		Last Modified: Wed, 11 Mar 2020 21:50:18 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b1648a96394c26b0e7d5c254c39b36c8eca6d00dfff5aa3776cb6671284ead`  
		Last Modified: Wed, 11 Mar 2020 21:50:49 GMT  
		Size: 3.2 MB (3215398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e63bc9624da4519af0d163fc47db94ef5d7d0ae27deccb9d6b923ba97710251`  
		Last Modified: Wed, 11 Mar 2020 21:50:48 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8f7907ef28cfa8968f389a0e60d2b4a98f2b9da2963e09d86911a36e945825`  
		Last Modified: Wed, 11 Mar 2020 21:50:48 GMT  
		Size: 754.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013cac041612fcb3b3db97e63f70c7f357b31618cd79f2a0852b38181355f5bd`  
		Last Modified: Wed, 11 Mar 2020 21:50:48 GMT  
		Size: 2.5 KB (2532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:c2d6834d581a10f8d30ae8678d859ad15a3747335051665f21dbe7e602568a8a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67486006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd179934e0f1561bdac8a67db9bf33af7be9c1f7508bdb0c7aa76184817e0d62`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:01:09 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 03:01:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 03:01:20 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:57:34 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:57:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:57:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:57:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:57:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:57:48 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:57:57 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Mar 2020 21:57:59 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:58:00 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Mar 2020 21:58:02 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Mar 2020 21:58:02 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:58:03 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Mar 2020 21:58:03 GMT
EXPOSE 2375 2376
# Wed, 11 Mar 2020 21:58:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Mar 2020 21:58:05 GMT
CMD []
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5014010b799b2f3cc6305fd21cc4b096dd28ad093e165cea5976f92ccb8c462`  
		Last Modified: Sat, 18 Jan 2020 03:03:27 GMT  
		Size: 2.3 MB (2254397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f49247ef05003d569c198c4908b849fdadd330bf360c04360ae48fd0d68b6d`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca62e39536ad2825e9d1db7dbfa88f4cbc9d95659c5fb45691fa224654d2629`  
		Last Modified: Wed, 11 Mar 2020 21:58:49 GMT  
		Size: 59.9 MB (59927053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a96da9a069c4780e3c46bcbd35f4da5d0e173b2888bec333941260f131ccc8`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202349aaae9b658c7d87822ac340735af35c35495f6af77e5db0df2d253880ea`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f43ed55770aa202e0a559ef5505907bdf9e16eb7ea47829463da52a02907f9c`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466cffcfbb54d45db4bfc4d2a4ef125228d8adaa890f4bdf1b64c9305a00e67b`  
		Last Modified: Wed, 11 Mar 2020 21:59:01 GMT  
		Size: 2.9 MB (2878539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6759e573461d1a01a039d460c93cc7394fc6503dcbb5a199b318c51ea84a5b7`  
		Last Modified: Wed, 11 Mar 2020 21:59:00 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62db51a4792cce56454199be1d125345ae07f763e4fda4f56a955259f1ecba93`  
		Last Modified: Wed, 11 Mar 2020 21:59:00 GMT  
		Size: 754.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600fa87244d5da05152b4c389cc3f37aaf0b36cb70a7d0d4294feaeb52abbd12`  
		Last Modified: Wed, 11 Mar 2020 21:59:00 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6fcdb8d75a9f4a6ee01e57720cb5543bd81035db06ec821383dfde6a4371389e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68163443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac71857cf4ec95c719133d716baecc805697ff6ca79086a80b6e14a77d43d3bc`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 02:23:05 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 02:23:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 02:23:12 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:39:44 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:39:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:39:52 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:39:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:39:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:39:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:39:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:39:56 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:40:05 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Mar 2020 21:40:08 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:40:08 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Mar 2020 21:40:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Mar 2020 21:40:10 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:40:11 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Mar 2020 21:40:12 GMT
EXPOSE 2375 2376
# Wed, 11 Mar 2020 21:40:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Mar 2020 21:40:13 GMT
CMD []
```

-	Layers:
	-	`sha256:8fa90b21c985a6fcfff966bdfbde81cdd088de0aa8af38110057f6ac408f4408`  
		Last Modified: Sat, 18 Jan 2020 01:40:23 GMT  
		Size: 2.7 MB (2723075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2917335fcb0a6856d5bf55430ba707c2c1378029a109e61959e62d2769230db`  
		Last Modified: Sat, 18 Jan 2020 02:25:35 GMT  
		Size: 2.4 MB (2445713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d3c84c2515134ddfa5ae5bac6e140953e9576fcd30a0bbc10fbc565d267895`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a828ac2f8d0e08bfd3c5405031bb245a21e469671397bd03e8868ce0925d9f49`  
		Last Modified: Wed, 11 Mar 2020 21:40:56 GMT  
		Size: 57.4 MB (57387269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7b0e4ac96f123613bb6ebd37a1bb99fb6f8a12b1d521f89f4211a970dbc077`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25581ce9dd66a29fecb3a63c9f888a0c6e3c68de7002441092b6a41dd833e995`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc58c5fdb432f00e6a7cdfa6b6507ca3c8598ab0612730e109e4faf5b0fc2d5a`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d396bfbbbaa91436006cf0e8b86b9e00c9e49a1dcbcd557c3fc331afc8e9e2f3`  
		Last Modified: Wed, 11 Mar 2020 21:41:09 GMT  
		Size: 5.6 MB (5600915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3bdb37e40cba208e5d80d500a33700bdff3ad30ebbfcb014c89a614506038d`  
		Last Modified: Wed, 11 Mar 2020 21:41:07 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269e23372e2e87311644e618cb3e6c09eae4cc41d919662298578a9abfe476ed`  
		Last Modified: Wed, 11 Mar 2020 21:41:07 GMT  
		Size: 758.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6204a0f4fef03aefb0b6ae2c7dfee680f8a6d84e0f59324ded513c256255723`  
		Last Modified: Wed, 11 Mar 2020 21:41:07 GMT  
		Size: 2.5 KB (2535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19-dind-rootless`

```console
$ docker pull docker@sha256:b1ba6b5c5d00fdfbf812971cbeb72a81bbb9fca8f70a1809b68c74968a49849c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:19-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:e0fbfc60a11eae3ce35434bd72828bf2d74b711dd3fd309ee36f646d69fd30a4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.6 MB (98553507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131e19ccffdf6245ad57a0ca98e0abd6e6cc5eb4495fe9358f90e1c9837de9c5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 04:42:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 04:42:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:19:32 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:19:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:19:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:39 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:19:45 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Mar 2020 21:19:45 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:19:46 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Mar 2020 21:19:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Mar 2020 21:19:47 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:47 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Mar 2020 21:19:47 GMT
EXPOSE 2375 2376
# Wed, 11 Mar 2020 21:19:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:47 GMT
CMD []
# Wed, 11 Mar 2020 21:19:52 GMT
RUN apk add --no-cache iproute2
# Wed, 11 Mar 2020 21:19:53 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Wed, 11 Mar 2020 21:19:54 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:19:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O rootless.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-rootless-extras-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-rootless-extras-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		vpnkit --version
# Wed, 11 Mar 2020 21:19:56 GMT
ENV ROOTLESSKIT_VERSION=0.9.1
# Wed, 11 Mar 2020 21:20:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .rootlesskit-build-deps 		go 		libc-dev 	; 	wget -O rootlesskit.tgz "https://github.com/rootless-containers/rootlesskit/archive/v${ROOTLESSKIT_VERSION}.tar.gz"; 	export GOPATH='/go'; mkdir "$GOPATH"; 	mkdir -p "$GOPATH/src/github.com/rootless-containers/rootlesskit"; 	tar --extract --file rootlesskit.tgz --directory "$GOPATH/src/github.com/rootless-containers/rootlesskit" --strip-components 1; 	rm rootlesskit.tgz; 	go build -o /usr/local/bin/rootlesskit github.com/rootless-containers/rootlesskit/cmd/rootlesskit; 	go build -o /usr/local/bin/rootlesskit-docker-proxy github.com/rootless-containers/rootlesskit/cmd/rootlesskit-docker-proxy; 	rm -rf "$GOPATH"; 	apk del --no-network .rootlesskit-build-deps; 	rootlesskit --version
# Wed, 11 Mar 2020 21:20:08 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Wed, 11 Mar 2020 21:20:09 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 11 Mar 2020 21:20:09 GMT
USER rootless
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd54125436dc48e0d60096d61457bcfd886136eb67815a60210ec67d3793096f`  
		Last Modified: Sat, 18 Jan 2020 04:43:03 GMT  
		Size: 2.4 MB (2425150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d1554c15cbb8c6b81fd21a057c8e97749fb24fd5befeb94ad960d3a350f91f`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dd17ef2c28fbb77b8b589e2e601e3ce86c0b9bcdb9dc73b6330d7ca16dca19`  
		Last Modified: Wed, 11 Mar 2020 21:20:40 GMT  
		Size: 64.2 MB (64218865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca57ea69baf170d62b8d1a51d898ff8d9383e22cd18bbde168ff539e74be8a4`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3af031952ce6719d5ca2f369b2187e1819fdab00252d315555a00048d6b99b7`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29377cccb214061fb46c1d5a1c27f53c366384d34f168cdb8484f5c7fcfb87a`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4939ff19fbb72e09aad6b10bc7440f9b23e0983f05c3cf6679a6392a40103b27`  
		Last Modified: Wed, 11 Mar 2020 21:20:48 GMT  
		Size: 5.6 MB (5598354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617664eed4c7060ec14f8178529d17b8a637b33a19f65101e062e185feda4c1`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8b6f7ec5ec983309648ff91b432c6abc38b547fc0610e3d81ab7e2472ad7ae`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 756.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb8de5d1a5be108527d435aef60a4a041879e0ddcf6d747ff324d57a5000f03`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 2.5 KB (2536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af40291eab6e7e25f86e0b385342cfe0318d38212a55bc20dd0aef9d3cc1a708`  
		Last Modified: Wed, 11 Mar 2020 21:20:56 GMT  
		Size: 796.0 KB (796003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd959232e7eccc0e2cb0117fb87809c0a4750269e1486a4ded4cbcff13c7b088`  
		Last Modified: Wed, 11 Mar 2020 21:20:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82aa1d69b9f04b015fb9771d9751d1e6cfe72d91da8d347c8bb83bde351f464b`  
		Last Modified: Wed, 11 Mar 2020 21:20:55 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cdb51a3ef0eb7411052a13cb5c1f4dbcb005a502d6805092f9d0006a963ad7`  
		Last Modified: Wed, 11 Mar 2020 21:20:57 GMT  
		Size: 9.1 MB (9109448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420ff93d35ca71a9e8a6fcfab5be9089f24b654a6c2c9f0fc46727937a534447`  
		Last Modified: Wed, 11 Mar 2020 21:20:57 GMT  
		Size: 13.6 MB (13594708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc08146368fd44217f9c582fc83a67d4d4b6844c8a9ed76700b579a514f8a4a`  
		Last Modified: Wed, 11 Mar 2020 21:20:54 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19-git`

```console
$ docker pull docker@sha256:4690f87ef12b57befc03948cfb45125e727469c886ce306268985ffc10c5f117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19-git` - linux; amd64

```console
$ docker pull docker@sha256:cb428bf67ff328e9cd57b5bbb64f04da465ef3198fbb8b0f0eb539144812cfe7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77662702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147d7d578318b63c7d01ee26605a981701192c4d365a7b72557655cae9225598`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 04:42:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 04:42:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:19:32 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:19:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:19:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:39 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:20:16 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd54125436dc48e0d60096d61457bcfd886136eb67815a60210ec67d3793096f`  
		Last Modified: Sat, 18 Jan 2020 04:43:03 GMT  
		Size: 2.4 MB (2425150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d1554c15cbb8c6b81fd21a057c8e97749fb24fd5befeb94ad960d3a350f91f`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dd17ef2c28fbb77b8b589e2e601e3ce86c0b9bcdb9dc73b6330d7ca16dca19`  
		Last Modified: Wed, 11 Mar 2020 21:20:40 GMT  
		Size: 64.2 MB (64218865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca57ea69baf170d62b8d1a51d898ff8d9383e22cd18bbde168ff539e74be8a4`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3af031952ce6719d5ca2f369b2187e1819fdab00252d315555a00048d6b99b7`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29377cccb214061fb46c1d5a1c27f53c366384d34f168cdb8484f5c7fcfb87a`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254b360be85b0840ff05885a92f88a8c9953477f040fda3328e6ea8eea86de6a`  
		Last Modified: Wed, 11 Mar 2020 21:21:05 GMT  
		Size: 8.2 MB (8213895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19-git` - linux; arm variant v6

```console
$ docker pull docker@sha256:e1850f9ae57922ee14a032dbf923d1efc8d553b02760378f562f1fb4fd2e499f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72737200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0522fe2ee7c4d185a532637aef5842258a77b0c068ec510a1ed61c9b78774eef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 05:52:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 05:52:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 05:52:35 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:49:22 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:49:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:49:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:49:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:49:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:49:38 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:50:01 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c86f804e7b5cc2f1f9d87340dfef1fcc13615f2cbd25bda470e513c1e4a627`  
		Last Modified: Sat, 18 Jan 2020 05:54:22 GMT  
		Size: 2.4 MB (2355405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d84775c03f92068112e3757afd6ddab1b2c0a3d1073e91b182620b6ec239f7`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592a77d3ce3aac4cb4c252c866f4a65c1541726b2bbdb512444569119b5cd98e`  
		Last Modified: Wed, 11 Mar 2020 21:50:37 GMT  
		Size: 59.9 MB (59927165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0277ab691262af1bf0bf50d6d459874dbf48509a6103991fd9d6225e455cb995`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320285a35393ed08c2ed85f5dc6d6ca6a1c07ac14fcfb8b4e1e5c5a4c30eace9`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e82c58148faac404a83fad42819c701567beb61dac6c2ae6d76ac1f97eefccd`  
		Last Modified: Wed, 11 Mar 2020 21:50:18 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162f34f6eb0f7762945f1e6a261e992d3923e55044cafaff16656007c3811c1d`  
		Last Modified: Wed, 11 Mar 2020 21:51:04 GMT  
		Size: 7.8 MB (7835202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19-git` - linux; arm variant v7

```console
$ docker pull docker@sha256:f47ed269de366a810d8e18b4df194fbcc6da43c3124ddaf516bb432d61b02804
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71675688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f090014780387159e6d1ca5236562fa2a275f196b6d7aba5d5afb8f3ad86a989`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:01:09 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 03:01:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 03:01:20 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:57:34 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:57:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:57:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:57:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:57:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:57:48 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:58:12 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5014010b799b2f3cc6305fd21cc4b096dd28ad093e165cea5976f92ccb8c462`  
		Last Modified: Sat, 18 Jan 2020 03:03:27 GMT  
		Size: 2.3 MB (2254397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f49247ef05003d569c198c4908b849fdadd330bf360c04360ae48fd0d68b6d`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca62e39536ad2825e9d1db7dbfa88f4cbc9d95659c5fb45691fa224654d2629`  
		Last Modified: Wed, 11 Mar 2020 21:58:49 GMT  
		Size: 59.9 MB (59927053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a96da9a069c4780e3c46bcbd35f4da5d0e173b2888bec333941260f131ccc8`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202349aaae9b658c7d87822ac340735af35c35495f6af77e5db0df2d253880ea`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f43ed55770aa202e0a559ef5505907bdf9e16eb7ea47829463da52a02907f9c`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877200202589a73b4d16451308a3e44508cb4df920be69143f584e1d64407f4c`  
		Last Modified: Wed, 11 Mar 2020 21:59:14 GMT  
		Size: 7.1 MB (7072817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e940117143b12b2eac9c5565eda0db3bdf8d6f0a13068832eb96d84cafded257
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70963946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08226ded6b73a3e1734672484ecb773d61e8a1e9f50bf7e6f7cfa49ef1056e22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 02:23:05 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 02:23:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 02:23:12 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:39:44 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:39:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:39:52 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:39:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:39:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:39:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:39:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:39:56 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:40:21 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:8fa90b21c985a6fcfff966bdfbde81cdd088de0aa8af38110057f6ac408f4408`  
		Last Modified: Sat, 18 Jan 2020 01:40:23 GMT  
		Size: 2.7 MB (2723075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2917335fcb0a6856d5bf55430ba707c2c1378029a109e61959e62d2769230db`  
		Last Modified: Sat, 18 Jan 2020 02:25:35 GMT  
		Size: 2.4 MB (2445713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d3c84c2515134ddfa5ae5bac6e140953e9576fcd30a0bbc10fbc565d267895`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a828ac2f8d0e08bfd3c5405031bb245a21e469671397bd03e8868ce0925d9f49`  
		Last Modified: Wed, 11 Mar 2020 21:40:56 GMT  
		Size: 57.4 MB (57387269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7b0e4ac96f123613bb6ebd37a1bb99fb6f8a12b1d521f89f4211a970dbc077`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25581ce9dd66a29fecb3a63c9f888a0c6e3c68de7002441092b6a41dd833e995`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc58c5fdb432f00e6a7cdfa6b6507ca3c8598ab0612730e109e4faf5b0fc2d5a`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e0a8bd53622c572d715e352539b455c6a81b69ed96893f228292d785c5051f`  
		Last Modified: Wed, 11 Mar 2020 21:41:22 GMT  
		Size: 8.4 MB (8406022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:dind`

```console
$ docker pull docker@sha256:308dcf9380af44ea492736e8d59605cd0ff2dab0527073f7e718ee4498e85dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:dind` - linux; amd64

```console
$ docker pull docker@sha256:0e6d34042007a6f5280838dc045af0d600654b57cd367251d1dd8bba4b55c773
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75051735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe98abf5dda7ec569bc4821f20ceca66945e67882fe32f960fb8b8f179af0e42`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 04:42:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 04:42:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:19:32 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:19:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:19:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:39 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:19:45 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Mar 2020 21:19:45 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:19:46 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Mar 2020 21:19:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Mar 2020 21:19:47 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:47 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Mar 2020 21:19:47 GMT
EXPOSE 2375 2376
# Wed, 11 Mar 2020 21:19:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:47 GMT
CMD []
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd54125436dc48e0d60096d61457bcfd886136eb67815a60210ec67d3793096f`  
		Last Modified: Sat, 18 Jan 2020 04:43:03 GMT  
		Size: 2.4 MB (2425150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d1554c15cbb8c6b81fd21a057c8e97749fb24fd5befeb94ad960d3a350f91f`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dd17ef2c28fbb77b8b589e2e601e3ce86c0b9bcdb9dc73b6330d7ca16dca19`  
		Last Modified: Wed, 11 Mar 2020 21:20:40 GMT  
		Size: 64.2 MB (64218865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca57ea69baf170d62b8d1a51d898ff8d9383e22cd18bbde168ff539e74be8a4`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3af031952ce6719d5ca2f369b2187e1819fdab00252d315555a00048d6b99b7`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29377cccb214061fb46c1d5a1c27f53c366384d34f168cdb8484f5c7fcfb87a`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4939ff19fbb72e09aad6b10bc7440f9b23e0983f05c3cf6679a6392a40103b27`  
		Last Modified: Wed, 11 Mar 2020 21:20:48 GMT  
		Size: 5.6 MB (5598354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617664eed4c7060ec14f8178529d17b8a637b33a19f65101e062e185feda4c1`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8b6f7ec5ec983309648ff91b432c6abc38b547fc0610e3d81ab7e2472ad7ae`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 756.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb8de5d1a5be108527d435aef60a4a041879e0ddcf6d747ff324d57a5000f03`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 2.5 KB (2536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:04246f289e63b1bc0baf3ee051e2374497207183b9e5b86373aa2f8938893a6c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68121997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08fff432f3d4cd1dae7778792ad2daa258d095691556f760fe82584bb66fa2b8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 05:52:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 05:52:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 05:52:35 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:49:22 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:49:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:49:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:49:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:49:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:49:38 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:49:46 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Mar 2020 21:49:48 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:49:49 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Mar 2020 21:49:51 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Mar 2020 21:49:51 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:49:52 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Mar 2020 21:49:52 GMT
EXPOSE 2375 2376
# Wed, 11 Mar 2020 21:49:53 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Mar 2020 21:49:53 GMT
CMD []
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c86f804e7b5cc2f1f9d87340dfef1fcc13615f2cbd25bda470e513c1e4a627`  
		Last Modified: Sat, 18 Jan 2020 05:54:22 GMT  
		Size: 2.4 MB (2355405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d84775c03f92068112e3757afd6ddab1b2c0a3d1073e91b182620b6ec239f7`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592a77d3ce3aac4cb4c252c866f4a65c1541726b2bbdb512444569119b5cd98e`  
		Last Modified: Wed, 11 Mar 2020 21:50:37 GMT  
		Size: 59.9 MB (59927165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0277ab691262af1bf0bf50d6d459874dbf48509a6103991fd9d6225e455cb995`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320285a35393ed08c2ed85f5dc6d6ca6a1c07ac14fcfb8b4e1e5c5a4c30eace9`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e82c58148faac404a83fad42819c701567beb61dac6c2ae6d76ac1f97eefccd`  
		Last Modified: Wed, 11 Mar 2020 21:50:18 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b1648a96394c26b0e7d5c254c39b36c8eca6d00dfff5aa3776cb6671284ead`  
		Last Modified: Wed, 11 Mar 2020 21:50:49 GMT  
		Size: 3.2 MB (3215398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e63bc9624da4519af0d163fc47db94ef5d7d0ae27deccb9d6b923ba97710251`  
		Last Modified: Wed, 11 Mar 2020 21:50:48 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8f7907ef28cfa8968f389a0e60d2b4a98f2b9da2963e09d86911a36e945825`  
		Last Modified: Wed, 11 Mar 2020 21:50:48 GMT  
		Size: 754.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013cac041612fcb3b3db97e63f70c7f357b31618cd79f2a0852b38181355f5bd`  
		Last Modified: Wed, 11 Mar 2020 21:50:48 GMT  
		Size: 2.5 KB (2532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:c2d6834d581a10f8d30ae8678d859ad15a3747335051665f21dbe7e602568a8a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67486006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd179934e0f1561bdac8a67db9bf33af7be9c1f7508bdb0c7aa76184817e0d62`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:01:09 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 03:01:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 03:01:20 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:57:34 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:57:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:57:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:57:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:57:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:57:48 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:57:57 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Mar 2020 21:57:59 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:58:00 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Mar 2020 21:58:02 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Mar 2020 21:58:02 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:58:03 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Mar 2020 21:58:03 GMT
EXPOSE 2375 2376
# Wed, 11 Mar 2020 21:58:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Mar 2020 21:58:05 GMT
CMD []
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5014010b799b2f3cc6305fd21cc4b096dd28ad093e165cea5976f92ccb8c462`  
		Last Modified: Sat, 18 Jan 2020 03:03:27 GMT  
		Size: 2.3 MB (2254397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f49247ef05003d569c198c4908b849fdadd330bf360c04360ae48fd0d68b6d`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca62e39536ad2825e9d1db7dbfa88f4cbc9d95659c5fb45691fa224654d2629`  
		Last Modified: Wed, 11 Mar 2020 21:58:49 GMT  
		Size: 59.9 MB (59927053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a96da9a069c4780e3c46bcbd35f4da5d0e173b2888bec333941260f131ccc8`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202349aaae9b658c7d87822ac340735af35c35495f6af77e5db0df2d253880ea`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f43ed55770aa202e0a559ef5505907bdf9e16eb7ea47829463da52a02907f9c`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466cffcfbb54d45db4bfc4d2a4ef125228d8adaa890f4bdf1b64c9305a00e67b`  
		Last Modified: Wed, 11 Mar 2020 21:59:01 GMT  
		Size: 2.9 MB (2878539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6759e573461d1a01a039d460c93cc7394fc6503dcbb5a199b318c51ea84a5b7`  
		Last Modified: Wed, 11 Mar 2020 21:59:00 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62db51a4792cce56454199be1d125345ae07f763e4fda4f56a955259f1ecba93`  
		Last Modified: Wed, 11 Mar 2020 21:59:00 GMT  
		Size: 754.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600fa87244d5da05152b4c389cc3f37aaf0b36cb70a7d0d4294feaeb52abbd12`  
		Last Modified: Wed, 11 Mar 2020 21:59:00 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6fcdb8d75a9f4a6ee01e57720cb5543bd81035db06ec821383dfde6a4371389e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68163443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac71857cf4ec95c719133d716baecc805697ff6ca79086a80b6e14a77d43d3bc`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 02:23:05 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 02:23:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 02:23:12 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:39:44 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:39:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:39:52 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:39:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:39:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:39:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:39:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:39:56 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:40:05 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Mar 2020 21:40:08 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:40:08 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Mar 2020 21:40:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Mar 2020 21:40:10 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:40:11 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Mar 2020 21:40:12 GMT
EXPOSE 2375 2376
# Wed, 11 Mar 2020 21:40:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Mar 2020 21:40:13 GMT
CMD []
```

-	Layers:
	-	`sha256:8fa90b21c985a6fcfff966bdfbde81cdd088de0aa8af38110057f6ac408f4408`  
		Last Modified: Sat, 18 Jan 2020 01:40:23 GMT  
		Size: 2.7 MB (2723075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2917335fcb0a6856d5bf55430ba707c2c1378029a109e61959e62d2769230db`  
		Last Modified: Sat, 18 Jan 2020 02:25:35 GMT  
		Size: 2.4 MB (2445713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d3c84c2515134ddfa5ae5bac6e140953e9576fcd30a0bbc10fbc565d267895`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a828ac2f8d0e08bfd3c5405031bb245a21e469671397bd03e8868ce0925d9f49`  
		Last Modified: Wed, 11 Mar 2020 21:40:56 GMT  
		Size: 57.4 MB (57387269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7b0e4ac96f123613bb6ebd37a1bb99fb6f8a12b1d521f89f4211a970dbc077`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25581ce9dd66a29fecb3a63c9f888a0c6e3c68de7002441092b6a41dd833e995`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc58c5fdb432f00e6a7cdfa6b6507ca3c8598ab0612730e109e4faf5b0fc2d5a`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d396bfbbbaa91436006cf0e8b86b9e00c9e49a1dcbcd557c3fc331afc8e9e2f3`  
		Last Modified: Wed, 11 Mar 2020 21:41:09 GMT  
		Size: 5.6 MB (5600915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3bdb37e40cba208e5d80d500a33700bdff3ad30ebbfcb014c89a614506038d`  
		Last Modified: Wed, 11 Mar 2020 21:41:07 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269e23372e2e87311644e618cb3e6c09eae4cc41d919662298578a9abfe476ed`  
		Last Modified: Wed, 11 Mar 2020 21:41:07 GMT  
		Size: 758.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6204a0f4fef03aefb0b6ae2c7dfee680f8a6d84e0f59324ded513c256255723`  
		Last Modified: Wed, 11 Mar 2020 21:41:07 GMT  
		Size: 2.5 KB (2535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:b1ba6b5c5d00fdfbf812971cbeb72a81bbb9fca8f70a1809b68c74968a49849c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:e0fbfc60a11eae3ce35434bd72828bf2d74b711dd3fd309ee36f646d69fd30a4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.6 MB (98553507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131e19ccffdf6245ad57a0ca98e0abd6e6cc5eb4495fe9358f90e1c9837de9c5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 04:42:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 04:42:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:19:32 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:19:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:19:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:39 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:19:45 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Mar 2020 21:19:45 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:19:46 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Mar 2020 21:19:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Mar 2020 21:19:47 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:47 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Mar 2020 21:19:47 GMT
EXPOSE 2375 2376
# Wed, 11 Mar 2020 21:19:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:47 GMT
CMD []
# Wed, 11 Mar 2020 21:19:52 GMT
RUN apk add --no-cache iproute2
# Wed, 11 Mar 2020 21:19:53 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Wed, 11 Mar 2020 21:19:54 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:19:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O rootless.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-rootless-extras-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-rootless-extras-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		vpnkit --version
# Wed, 11 Mar 2020 21:19:56 GMT
ENV ROOTLESSKIT_VERSION=0.9.1
# Wed, 11 Mar 2020 21:20:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .rootlesskit-build-deps 		go 		libc-dev 	; 	wget -O rootlesskit.tgz "https://github.com/rootless-containers/rootlesskit/archive/v${ROOTLESSKIT_VERSION}.tar.gz"; 	export GOPATH='/go'; mkdir "$GOPATH"; 	mkdir -p "$GOPATH/src/github.com/rootless-containers/rootlesskit"; 	tar --extract --file rootlesskit.tgz --directory "$GOPATH/src/github.com/rootless-containers/rootlesskit" --strip-components 1; 	rm rootlesskit.tgz; 	go build -o /usr/local/bin/rootlesskit github.com/rootless-containers/rootlesskit/cmd/rootlesskit; 	go build -o /usr/local/bin/rootlesskit-docker-proxy github.com/rootless-containers/rootlesskit/cmd/rootlesskit-docker-proxy; 	rm -rf "$GOPATH"; 	apk del --no-network .rootlesskit-build-deps; 	rootlesskit --version
# Wed, 11 Mar 2020 21:20:08 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Wed, 11 Mar 2020 21:20:09 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 11 Mar 2020 21:20:09 GMT
USER rootless
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd54125436dc48e0d60096d61457bcfd886136eb67815a60210ec67d3793096f`  
		Last Modified: Sat, 18 Jan 2020 04:43:03 GMT  
		Size: 2.4 MB (2425150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d1554c15cbb8c6b81fd21a057c8e97749fb24fd5befeb94ad960d3a350f91f`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dd17ef2c28fbb77b8b589e2e601e3ce86c0b9bcdb9dc73b6330d7ca16dca19`  
		Last Modified: Wed, 11 Mar 2020 21:20:40 GMT  
		Size: 64.2 MB (64218865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca57ea69baf170d62b8d1a51d898ff8d9383e22cd18bbde168ff539e74be8a4`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3af031952ce6719d5ca2f369b2187e1819fdab00252d315555a00048d6b99b7`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29377cccb214061fb46c1d5a1c27f53c366384d34f168cdb8484f5c7fcfb87a`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4939ff19fbb72e09aad6b10bc7440f9b23e0983f05c3cf6679a6392a40103b27`  
		Last Modified: Wed, 11 Mar 2020 21:20:48 GMT  
		Size: 5.6 MB (5598354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617664eed4c7060ec14f8178529d17b8a637b33a19f65101e062e185feda4c1`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8b6f7ec5ec983309648ff91b432c6abc38b547fc0610e3d81ab7e2472ad7ae`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 756.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb8de5d1a5be108527d435aef60a4a041879e0ddcf6d747ff324d57a5000f03`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 2.5 KB (2536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af40291eab6e7e25f86e0b385342cfe0318d38212a55bc20dd0aef9d3cc1a708`  
		Last Modified: Wed, 11 Mar 2020 21:20:56 GMT  
		Size: 796.0 KB (796003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd959232e7eccc0e2cb0117fb87809c0a4750269e1486a4ded4cbcff13c7b088`  
		Last Modified: Wed, 11 Mar 2020 21:20:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82aa1d69b9f04b015fb9771d9751d1e6cfe72d91da8d347c8bb83bde351f464b`  
		Last Modified: Wed, 11 Mar 2020 21:20:55 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cdb51a3ef0eb7411052a13cb5c1f4dbcb005a502d6805092f9d0006a963ad7`  
		Last Modified: Wed, 11 Mar 2020 21:20:57 GMT  
		Size: 9.1 MB (9109448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420ff93d35ca71a9e8a6fcfab5be9089f24b654a6c2c9f0fc46727937a534447`  
		Last Modified: Wed, 11 Mar 2020 21:20:57 GMT  
		Size: 13.6 MB (13594708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc08146368fd44217f9c582fc83a67d4d4b6844c8a9ed76700b579a514f8a4a`  
		Last Modified: Wed, 11 Mar 2020 21:20:54 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:git`

```console
$ docker pull docker@sha256:4690f87ef12b57befc03948cfb45125e727469c886ce306268985ffc10c5f117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:git` - linux; amd64

```console
$ docker pull docker@sha256:cb428bf67ff328e9cd57b5bbb64f04da465ef3198fbb8b0f0eb539144812cfe7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77662702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147d7d578318b63c7d01ee26605a981701192c4d365a7b72557655cae9225598`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 04:42:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 04:42:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:19:32 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:19:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:19:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:39 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:20:16 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd54125436dc48e0d60096d61457bcfd886136eb67815a60210ec67d3793096f`  
		Last Modified: Sat, 18 Jan 2020 04:43:03 GMT  
		Size: 2.4 MB (2425150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d1554c15cbb8c6b81fd21a057c8e97749fb24fd5befeb94ad960d3a350f91f`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dd17ef2c28fbb77b8b589e2e601e3ce86c0b9bcdb9dc73b6330d7ca16dca19`  
		Last Modified: Wed, 11 Mar 2020 21:20:40 GMT  
		Size: 64.2 MB (64218865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca57ea69baf170d62b8d1a51d898ff8d9383e22cd18bbde168ff539e74be8a4`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3af031952ce6719d5ca2f369b2187e1819fdab00252d315555a00048d6b99b7`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29377cccb214061fb46c1d5a1c27f53c366384d34f168cdb8484f5c7fcfb87a`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254b360be85b0840ff05885a92f88a8c9953477f040fda3328e6ea8eea86de6a`  
		Last Modified: Wed, 11 Mar 2020 21:21:05 GMT  
		Size: 8.2 MB (8213895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm variant v6

```console
$ docker pull docker@sha256:e1850f9ae57922ee14a032dbf923d1efc8d553b02760378f562f1fb4fd2e499f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72737200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0522fe2ee7c4d185a532637aef5842258a77b0c068ec510a1ed61c9b78774eef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 05:52:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 05:52:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 05:52:35 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:49:22 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:49:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:49:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:49:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:49:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:49:38 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:50:01 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c86f804e7b5cc2f1f9d87340dfef1fcc13615f2cbd25bda470e513c1e4a627`  
		Last Modified: Sat, 18 Jan 2020 05:54:22 GMT  
		Size: 2.4 MB (2355405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d84775c03f92068112e3757afd6ddab1b2c0a3d1073e91b182620b6ec239f7`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592a77d3ce3aac4cb4c252c866f4a65c1541726b2bbdb512444569119b5cd98e`  
		Last Modified: Wed, 11 Mar 2020 21:50:37 GMT  
		Size: 59.9 MB (59927165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0277ab691262af1bf0bf50d6d459874dbf48509a6103991fd9d6225e455cb995`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320285a35393ed08c2ed85f5dc6d6ca6a1c07ac14fcfb8b4e1e5c5a4c30eace9`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e82c58148faac404a83fad42819c701567beb61dac6c2ae6d76ac1f97eefccd`  
		Last Modified: Wed, 11 Mar 2020 21:50:18 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162f34f6eb0f7762945f1e6a261e992d3923e55044cafaff16656007c3811c1d`  
		Last Modified: Wed, 11 Mar 2020 21:51:04 GMT  
		Size: 7.8 MB (7835202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm variant v7

```console
$ docker pull docker@sha256:f47ed269de366a810d8e18b4df194fbcc6da43c3124ddaf516bb432d61b02804
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71675688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f090014780387159e6d1ca5236562fa2a275f196b6d7aba5d5afb8f3ad86a989`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:01:09 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 03:01:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 03:01:20 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:57:34 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:57:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:57:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:57:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:57:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:57:48 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:58:12 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5014010b799b2f3cc6305fd21cc4b096dd28ad093e165cea5976f92ccb8c462`  
		Last Modified: Sat, 18 Jan 2020 03:03:27 GMT  
		Size: 2.3 MB (2254397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f49247ef05003d569c198c4908b849fdadd330bf360c04360ae48fd0d68b6d`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca62e39536ad2825e9d1db7dbfa88f4cbc9d95659c5fb45691fa224654d2629`  
		Last Modified: Wed, 11 Mar 2020 21:58:49 GMT  
		Size: 59.9 MB (59927053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a96da9a069c4780e3c46bcbd35f4da5d0e173b2888bec333941260f131ccc8`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202349aaae9b658c7d87822ac340735af35c35495f6af77e5db0df2d253880ea`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f43ed55770aa202e0a559ef5505907bdf9e16eb7ea47829463da52a02907f9c`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877200202589a73b4d16451308a3e44508cb4df920be69143f584e1d64407f4c`  
		Last Modified: Wed, 11 Mar 2020 21:59:14 GMT  
		Size: 7.1 MB (7072817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e940117143b12b2eac9c5565eda0db3bdf8d6f0a13068832eb96d84cafded257
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70963946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08226ded6b73a3e1734672484ecb773d61e8a1e9f50bf7e6f7cfa49ef1056e22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 02:23:05 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 02:23:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 02:23:12 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:39:44 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:39:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:39:52 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:39:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:39:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:39:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:39:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:39:56 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:40:21 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:8fa90b21c985a6fcfff966bdfbde81cdd088de0aa8af38110057f6ac408f4408`  
		Last Modified: Sat, 18 Jan 2020 01:40:23 GMT  
		Size: 2.7 MB (2723075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2917335fcb0a6856d5bf55430ba707c2c1378029a109e61959e62d2769230db`  
		Last Modified: Sat, 18 Jan 2020 02:25:35 GMT  
		Size: 2.4 MB (2445713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d3c84c2515134ddfa5ae5bac6e140953e9576fcd30a0bbc10fbc565d267895`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a828ac2f8d0e08bfd3c5405031bb245a21e469671397bd03e8868ce0925d9f49`  
		Last Modified: Wed, 11 Mar 2020 21:40:56 GMT  
		Size: 57.4 MB (57387269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7b0e4ac96f123613bb6ebd37a1bb99fb6f8a12b1d521f89f4211a970dbc077`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25581ce9dd66a29fecb3a63c9f888a0c6e3c68de7002441092b6a41dd833e995`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc58c5fdb432f00e6a7cdfa6b6507ca3c8598ab0612730e109e4faf5b0fc2d5a`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e0a8bd53622c572d715e352539b455c6a81b69ed96893f228292d785c5051f`  
		Last Modified: Wed, 11 Mar 2020 21:41:22 GMT  
		Size: 8.4 MB (8406022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:latest`

```console
$ docker pull docker@sha256:948c0f302dae8ce62d28c32e46817c054cd5b00353fb0037646e92917a4124ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:latest` - linux; amd64

```console
$ docker pull docker@sha256:7c311f0515f6e2bba92961cbd4c11ea7c74791935260c0c72c0ceebc75e52867
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69448807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f39826ae385e029ae634eb6a81091da60dae2e6ee2a19342c2e05ed4c3cb9171`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 04:42:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 04:42:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:19:32 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:19:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:19:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:39 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd54125436dc48e0d60096d61457bcfd886136eb67815a60210ec67d3793096f`  
		Last Modified: Sat, 18 Jan 2020 04:43:03 GMT  
		Size: 2.4 MB (2425150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d1554c15cbb8c6b81fd21a057c8e97749fb24fd5befeb94ad960d3a350f91f`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dd17ef2c28fbb77b8b589e2e601e3ce86c0b9bcdb9dc73b6330d7ca16dca19`  
		Last Modified: Wed, 11 Mar 2020 21:20:40 GMT  
		Size: 64.2 MB (64218865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca57ea69baf170d62b8d1a51d898ff8d9383e22cd18bbde168ff539e74be8a4`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3af031952ce6719d5ca2f369b2187e1819fdab00252d315555a00048d6b99b7`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29377cccb214061fb46c1d5a1c27f53c366384d34f168cdb8484f5c7fcfb87a`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:6066e1dbf8e74562362b84d31bfbf3356ab716c355e25d2fb3682f22f0016790
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64901998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbdbf0acc9e925c42921278175492252e55a006bf4ffff577bd68d5f1b29256a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 05:52:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 05:52:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 05:52:35 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:49:22 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:49:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:49:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:49:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:49:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:49:38 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c86f804e7b5cc2f1f9d87340dfef1fcc13615f2cbd25bda470e513c1e4a627`  
		Last Modified: Sat, 18 Jan 2020 05:54:22 GMT  
		Size: 2.4 MB (2355405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d84775c03f92068112e3757afd6ddab1b2c0a3d1073e91b182620b6ec239f7`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592a77d3ce3aac4cb4c252c866f4a65c1541726b2bbdb512444569119b5cd98e`  
		Last Modified: Wed, 11 Mar 2020 21:50:37 GMT  
		Size: 59.9 MB (59927165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0277ab691262af1bf0bf50d6d459874dbf48509a6103991fd9d6225e455cb995`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320285a35393ed08c2ed85f5dc6d6ca6a1c07ac14fcfb8b4e1e5c5a4c30eace9`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e82c58148faac404a83fad42819c701567beb61dac6c2ae6d76ac1f97eefccd`  
		Last Modified: Wed, 11 Mar 2020 21:50:18 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:32278b2c6a6b432c34a19367f68170d2bff8f79c57962f5cb4aab31f26130c6b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64602871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc2d0d6f635fee2fc5a74c78e7532a964940bead391471966dee40a29eeacc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:01:09 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 03:01:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 03:01:20 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:57:34 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:57:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:57:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:57:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:57:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:57:48 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5014010b799b2f3cc6305fd21cc4b096dd28ad093e165cea5976f92ccb8c462`  
		Last Modified: Sat, 18 Jan 2020 03:03:27 GMT  
		Size: 2.3 MB (2254397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f49247ef05003d569c198c4908b849fdadd330bf360c04360ae48fd0d68b6d`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca62e39536ad2825e9d1db7dbfa88f4cbc9d95659c5fb45691fa224654d2629`  
		Last Modified: Wed, 11 Mar 2020 21:58:49 GMT  
		Size: 59.9 MB (59927053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a96da9a069c4780e3c46bcbd35f4da5d0e173b2888bec333941260f131ccc8`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202349aaae9b658c7d87822ac340735af35c35495f6af77e5db0df2d253880ea`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f43ed55770aa202e0a559ef5505907bdf9e16eb7ea47829463da52a02907f9c`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f7f9c3b259b133a7cca0bfbe5db7f70c955aff499307e2714426c63fac9d5470
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62557924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea45e49e2b3cb4f5dc30b5f16f86e87e685949e8eb7ce7a98e59818c500dd823`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 02:23:05 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 02:23:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 02:23:12 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:39:44 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:39:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:39:52 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:39:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:39:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:39:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:39:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:39:56 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:8fa90b21c985a6fcfff966bdfbde81cdd088de0aa8af38110057f6ac408f4408`  
		Last Modified: Sat, 18 Jan 2020 01:40:23 GMT  
		Size: 2.7 MB (2723075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2917335fcb0a6856d5bf55430ba707c2c1378029a109e61959e62d2769230db`  
		Last Modified: Sat, 18 Jan 2020 02:25:35 GMT  
		Size: 2.4 MB (2445713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d3c84c2515134ddfa5ae5bac6e140953e9576fcd30a0bbc10fbc565d267895`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a828ac2f8d0e08bfd3c5405031bb245a21e469671397bd03e8868ce0925d9f49`  
		Last Modified: Wed, 11 Mar 2020 21:40:56 GMT  
		Size: 57.4 MB (57387269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7b0e4ac96f123613bb6ebd37a1bb99fb6f8a12b1d521f89f4211a970dbc077`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25581ce9dd66a29fecb3a63c9f888a0c6e3c68de7002441092b6a41dd833e995`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc58c5fdb432f00e6a7cdfa6b6507ca3c8598ab0612730e109e4faf5b0fc2d5a`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:stable`

```console
$ docker pull docker@sha256:948c0f302dae8ce62d28c32e46817c054cd5b00353fb0037646e92917a4124ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:stable` - linux; amd64

```console
$ docker pull docker@sha256:7c311f0515f6e2bba92961cbd4c11ea7c74791935260c0c72c0ceebc75e52867
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69448807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f39826ae385e029ae634eb6a81091da60dae2e6ee2a19342c2e05ed4c3cb9171`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 04:42:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 04:42:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:19:32 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:19:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:19:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:39 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd54125436dc48e0d60096d61457bcfd886136eb67815a60210ec67d3793096f`  
		Last Modified: Sat, 18 Jan 2020 04:43:03 GMT  
		Size: 2.4 MB (2425150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d1554c15cbb8c6b81fd21a057c8e97749fb24fd5befeb94ad960d3a350f91f`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dd17ef2c28fbb77b8b589e2e601e3ce86c0b9bcdb9dc73b6330d7ca16dca19`  
		Last Modified: Wed, 11 Mar 2020 21:20:40 GMT  
		Size: 64.2 MB (64218865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca57ea69baf170d62b8d1a51d898ff8d9383e22cd18bbde168ff539e74be8a4`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3af031952ce6719d5ca2f369b2187e1819fdab00252d315555a00048d6b99b7`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29377cccb214061fb46c1d5a1c27f53c366384d34f168cdb8484f5c7fcfb87a`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:stable` - linux; arm variant v6

```console
$ docker pull docker@sha256:6066e1dbf8e74562362b84d31bfbf3356ab716c355e25d2fb3682f22f0016790
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64901998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbdbf0acc9e925c42921278175492252e55a006bf4ffff577bd68d5f1b29256a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 05:52:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 05:52:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 05:52:35 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:49:22 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:49:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:49:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:49:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:49:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:49:38 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c86f804e7b5cc2f1f9d87340dfef1fcc13615f2cbd25bda470e513c1e4a627`  
		Last Modified: Sat, 18 Jan 2020 05:54:22 GMT  
		Size: 2.4 MB (2355405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d84775c03f92068112e3757afd6ddab1b2c0a3d1073e91b182620b6ec239f7`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592a77d3ce3aac4cb4c252c866f4a65c1541726b2bbdb512444569119b5cd98e`  
		Last Modified: Wed, 11 Mar 2020 21:50:37 GMT  
		Size: 59.9 MB (59927165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0277ab691262af1bf0bf50d6d459874dbf48509a6103991fd9d6225e455cb995`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320285a35393ed08c2ed85f5dc6d6ca6a1c07ac14fcfb8b4e1e5c5a4c30eace9`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e82c58148faac404a83fad42819c701567beb61dac6c2ae6d76ac1f97eefccd`  
		Last Modified: Wed, 11 Mar 2020 21:50:18 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:stable` - linux; arm variant v7

```console
$ docker pull docker@sha256:32278b2c6a6b432c34a19367f68170d2bff8f79c57962f5cb4aab31f26130c6b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64602871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc2d0d6f635fee2fc5a74c78e7532a964940bead391471966dee40a29eeacc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:01:09 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 03:01:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 03:01:20 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:57:34 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:57:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:57:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:57:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:57:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:57:48 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5014010b799b2f3cc6305fd21cc4b096dd28ad093e165cea5976f92ccb8c462`  
		Last Modified: Sat, 18 Jan 2020 03:03:27 GMT  
		Size: 2.3 MB (2254397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f49247ef05003d569c198c4908b849fdadd330bf360c04360ae48fd0d68b6d`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca62e39536ad2825e9d1db7dbfa88f4cbc9d95659c5fb45691fa224654d2629`  
		Last Modified: Wed, 11 Mar 2020 21:58:49 GMT  
		Size: 59.9 MB (59927053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a96da9a069c4780e3c46bcbd35f4da5d0e173b2888bec333941260f131ccc8`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202349aaae9b658c7d87822ac340735af35c35495f6af77e5db0df2d253880ea`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f43ed55770aa202e0a559ef5505907bdf9e16eb7ea47829463da52a02907f9c`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:stable` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f7f9c3b259b133a7cca0bfbe5db7f70c955aff499307e2714426c63fac9d5470
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62557924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea45e49e2b3cb4f5dc30b5f16f86e87e685949e8eb7ce7a98e59818c500dd823`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 02:23:05 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 02:23:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 02:23:12 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:39:44 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:39:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:39:52 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:39:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:39:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:39:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:39:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:39:56 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:8fa90b21c985a6fcfff966bdfbde81cdd088de0aa8af38110057f6ac408f4408`  
		Last Modified: Sat, 18 Jan 2020 01:40:23 GMT  
		Size: 2.7 MB (2723075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2917335fcb0a6856d5bf55430ba707c2c1378029a109e61959e62d2769230db`  
		Last Modified: Sat, 18 Jan 2020 02:25:35 GMT  
		Size: 2.4 MB (2445713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d3c84c2515134ddfa5ae5bac6e140953e9576fcd30a0bbc10fbc565d267895`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a828ac2f8d0e08bfd3c5405031bb245a21e469671397bd03e8868ce0925d9f49`  
		Last Modified: Wed, 11 Mar 2020 21:40:56 GMT  
		Size: 57.4 MB (57387269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7b0e4ac96f123613bb6ebd37a1bb99fb6f8a12b1d521f89f4211a970dbc077`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25581ce9dd66a29fecb3a63c9f888a0c6e3c68de7002441092b6a41dd833e995`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc58c5fdb432f00e6a7cdfa6b6507ca3c8598ab0612730e109e4faf5b0fc2d5a`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:stable-dind`

```console
$ docker pull docker@sha256:308dcf9380af44ea492736e8d59605cd0ff2dab0527073f7e718ee4498e85dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:stable-dind` - linux; amd64

```console
$ docker pull docker@sha256:0e6d34042007a6f5280838dc045af0d600654b57cd367251d1dd8bba4b55c773
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75051735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe98abf5dda7ec569bc4821f20ceca66945e67882fe32f960fb8b8f179af0e42`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 04:42:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 04:42:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:19:32 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:19:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:19:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:39 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:19:45 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Mar 2020 21:19:45 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:19:46 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Mar 2020 21:19:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Mar 2020 21:19:47 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:47 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Mar 2020 21:19:47 GMT
EXPOSE 2375 2376
# Wed, 11 Mar 2020 21:19:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:47 GMT
CMD []
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd54125436dc48e0d60096d61457bcfd886136eb67815a60210ec67d3793096f`  
		Last Modified: Sat, 18 Jan 2020 04:43:03 GMT  
		Size: 2.4 MB (2425150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d1554c15cbb8c6b81fd21a057c8e97749fb24fd5befeb94ad960d3a350f91f`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dd17ef2c28fbb77b8b589e2e601e3ce86c0b9bcdb9dc73b6330d7ca16dca19`  
		Last Modified: Wed, 11 Mar 2020 21:20:40 GMT  
		Size: 64.2 MB (64218865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca57ea69baf170d62b8d1a51d898ff8d9383e22cd18bbde168ff539e74be8a4`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3af031952ce6719d5ca2f369b2187e1819fdab00252d315555a00048d6b99b7`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29377cccb214061fb46c1d5a1c27f53c366384d34f168cdb8484f5c7fcfb87a`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4939ff19fbb72e09aad6b10bc7440f9b23e0983f05c3cf6679a6392a40103b27`  
		Last Modified: Wed, 11 Mar 2020 21:20:48 GMT  
		Size: 5.6 MB (5598354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617664eed4c7060ec14f8178529d17b8a637b33a19f65101e062e185feda4c1`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8b6f7ec5ec983309648ff91b432c6abc38b547fc0610e3d81ab7e2472ad7ae`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 756.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb8de5d1a5be108527d435aef60a4a041879e0ddcf6d747ff324d57a5000f03`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 2.5 KB (2536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:stable-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:04246f289e63b1bc0baf3ee051e2374497207183b9e5b86373aa2f8938893a6c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68121997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08fff432f3d4cd1dae7778792ad2daa258d095691556f760fe82584bb66fa2b8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 05:52:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 05:52:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 05:52:35 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:49:22 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:49:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:49:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:49:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:49:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:49:38 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:49:46 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Mar 2020 21:49:48 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:49:49 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Mar 2020 21:49:51 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Mar 2020 21:49:51 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:49:52 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Mar 2020 21:49:52 GMT
EXPOSE 2375 2376
# Wed, 11 Mar 2020 21:49:53 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Mar 2020 21:49:53 GMT
CMD []
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c86f804e7b5cc2f1f9d87340dfef1fcc13615f2cbd25bda470e513c1e4a627`  
		Last Modified: Sat, 18 Jan 2020 05:54:22 GMT  
		Size: 2.4 MB (2355405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d84775c03f92068112e3757afd6ddab1b2c0a3d1073e91b182620b6ec239f7`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592a77d3ce3aac4cb4c252c866f4a65c1541726b2bbdb512444569119b5cd98e`  
		Last Modified: Wed, 11 Mar 2020 21:50:37 GMT  
		Size: 59.9 MB (59927165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0277ab691262af1bf0bf50d6d459874dbf48509a6103991fd9d6225e455cb995`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320285a35393ed08c2ed85f5dc6d6ca6a1c07ac14fcfb8b4e1e5c5a4c30eace9`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e82c58148faac404a83fad42819c701567beb61dac6c2ae6d76ac1f97eefccd`  
		Last Modified: Wed, 11 Mar 2020 21:50:18 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b1648a96394c26b0e7d5c254c39b36c8eca6d00dfff5aa3776cb6671284ead`  
		Last Modified: Wed, 11 Mar 2020 21:50:49 GMT  
		Size: 3.2 MB (3215398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e63bc9624da4519af0d163fc47db94ef5d7d0ae27deccb9d6b923ba97710251`  
		Last Modified: Wed, 11 Mar 2020 21:50:48 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8f7907ef28cfa8968f389a0e60d2b4a98f2b9da2963e09d86911a36e945825`  
		Last Modified: Wed, 11 Mar 2020 21:50:48 GMT  
		Size: 754.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013cac041612fcb3b3db97e63f70c7f357b31618cd79f2a0852b38181355f5bd`  
		Last Modified: Wed, 11 Mar 2020 21:50:48 GMT  
		Size: 2.5 KB (2532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:stable-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:c2d6834d581a10f8d30ae8678d859ad15a3747335051665f21dbe7e602568a8a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67486006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd179934e0f1561bdac8a67db9bf33af7be9c1f7508bdb0c7aa76184817e0d62`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:01:09 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 03:01:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 03:01:20 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:57:34 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:57:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:57:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:57:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:57:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:57:48 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:57:57 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Mar 2020 21:57:59 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:58:00 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Mar 2020 21:58:02 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Mar 2020 21:58:02 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:58:03 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Mar 2020 21:58:03 GMT
EXPOSE 2375 2376
# Wed, 11 Mar 2020 21:58:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Mar 2020 21:58:05 GMT
CMD []
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5014010b799b2f3cc6305fd21cc4b096dd28ad093e165cea5976f92ccb8c462`  
		Last Modified: Sat, 18 Jan 2020 03:03:27 GMT  
		Size: 2.3 MB (2254397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f49247ef05003d569c198c4908b849fdadd330bf360c04360ae48fd0d68b6d`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca62e39536ad2825e9d1db7dbfa88f4cbc9d95659c5fb45691fa224654d2629`  
		Last Modified: Wed, 11 Mar 2020 21:58:49 GMT  
		Size: 59.9 MB (59927053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a96da9a069c4780e3c46bcbd35f4da5d0e173b2888bec333941260f131ccc8`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202349aaae9b658c7d87822ac340735af35c35495f6af77e5db0df2d253880ea`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f43ed55770aa202e0a559ef5505907bdf9e16eb7ea47829463da52a02907f9c`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466cffcfbb54d45db4bfc4d2a4ef125228d8adaa890f4bdf1b64c9305a00e67b`  
		Last Modified: Wed, 11 Mar 2020 21:59:01 GMT  
		Size: 2.9 MB (2878539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6759e573461d1a01a039d460c93cc7394fc6503dcbb5a199b318c51ea84a5b7`  
		Last Modified: Wed, 11 Mar 2020 21:59:00 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62db51a4792cce56454199be1d125345ae07f763e4fda4f56a955259f1ecba93`  
		Last Modified: Wed, 11 Mar 2020 21:59:00 GMT  
		Size: 754.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600fa87244d5da05152b4c389cc3f37aaf0b36cb70a7d0d4294feaeb52abbd12`  
		Last Modified: Wed, 11 Mar 2020 21:59:00 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:stable-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6fcdb8d75a9f4a6ee01e57720cb5543bd81035db06ec821383dfde6a4371389e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68163443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac71857cf4ec95c719133d716baecc805697ff6ca79086a80b6e14a77d43d3bc`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 02:23:05 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 02:23:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 02:23:12 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:39:44 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:39:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:39:52 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:39:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:39:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:39:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:39:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:39:56 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:40:05 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Mar 2020 21:40:08 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:40:08 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Mar 2020 21:40:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Mar 2020 21:40:10 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:40:11 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Mar 2020 21:40:12 GMT
EXPOSE 2375 2376
# Wed, 11 Mar 2020 21:40:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Mar 2020 21:40:13 GMT
CMD []
```

-	Layers:
	-	`sha256:8fa90b21c985a6fcfff966bdfbde81cdd088de0aa8af38110057f6ac408f4408`  
		Last Modified: Sat, 18 Jan 2020 01:40:23 GMT  
		Size: 2.7 MB (2723075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2917335fcb0a6856d5bf55430ba707c2c1378029a109e61959e62d2769230db`  
		Last Modified: Sat, 18 Jan 2020 02:25:35 GMT  
		Size: 2.4 MB (2445713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d3c84c2515134ddfa5ae5bac6e140953e9576fcd30a0bbc10fbc565d267895`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a828ac2f8d0e08bfd3c5405031bb245a21e469671397bd03e8868ce0925d9f49`  
		Last Modified: Wed, 11 Mar 2020 21:40:56 GMT  
		Size: 57.4 MB (57387269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7b0e4ac96f123613bb6ebd37a1bb99fb6f8a12b1d521f89f4211a970dbc077`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25581ce9dd66a29fecb3a63c9f888a0c6e3c68de7002441092b6a41dd833e995`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc58c5fdb432f00e6a7cdfa6b6507ca3c8598ab0612730e109e4faf5b0fc2d5a`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d396bfbbbaa91436006cf0e8b86b9e00c9e49a1dcbcd557c3fc331afc8e9e2f3`  
		Last Modified: Wed, 11 Mar 2020 21:41:09 GMT  
		Size: 5.6 MB (5600915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3bdb37e40cba208e5d80d500a33700bdff3ad30ebbfcb014c89a614506038d`  
		Last Modified: Wed, 11 Mar 2020 21:41:07 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269e23372e2e87311644e618cb3e6c09eae4cc41d919662298578a9abfe476ed`  
		Last Modified: Wed, 11 Mar 2020 21:41:07 GMT  
		Size: 758.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6204a0f4fef03aefb0b6ae2c7dfee680f8a6d84e0f59324ded513c256255723`  
		Last Modified: Wed, 11 Mar 2020 21:41:07 GMT  
		Size: 2.5 KB (2535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:stable-dind-rootless`

```console
$ docker pull docker@sha256:b1ba6b5c5d00fdfbf812971cbeb72a81bbb9fca8f70a1809b68c74968a49849c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:stable-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:e0fbfc60a11eae3ce35434bd72828bf2d74b711dd3fd309ee36f646d69fd30a4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.6 MB (98553507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131e19ccffdf6245ad57a0ca98e0abd6e6cc5eb4495fe9358f90e1c9837de9c5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 04:42:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 04:42:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:19:32 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:19:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:19:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:39 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:19:45 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Mar 2020 21:19:45 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:19:46 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Mar 2020 21:19:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Mar 2020 21:19:47 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:47 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Mar 2020 21:19:47 GMT
EXPOSE 2375 2376
# Wed, 11 Mar 2020 21:19:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:47 GMT
CMD []
# Wed, 11 Mar 2020 21:19:52 GMT
RUN apk add --no-cache iproute2
# Wed, 11 Mar 2020 21:19:53 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Wed, 11 Mar 2020 21:19:54 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:19:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O rootless.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-rootless-extras-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-rootless-extras-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		vpnkit --version
# Wed, 11 Mar 2020 21:19:56 GMT
ENV ROOTLESSKIT_VERSION=0.9.1
# Wed, 11 Mar 2020 21:20:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .rootlesskit-build-deps 		go 		libc-dev 	; 	wget -O rootlesskit.tgz "https://github.com/rootless-containers/rootlesskit/archive/v${ROOTLESSKIT_VERSION}.tar.gz"; 	export GOPATH='/go'; mkdir "$GOPATH"; 	mkdir -p "$GOPATH/src/github.com/rootless-containers/rootlesskit"; 	tar --extract --file rootlesskit.tgz --directory "$GOPATH/src/github.com/rootless-containers/rootlesskit" --strip-components 1; 	rm rootlesskit.tgz; 	go build -o /usr/local/bin/rootlesskit github.com/rootless-containers/rootlesskit/cmd/rootlesskit; 	go build -o /usr/local/bin/rootlesskit-docker-proxy github.com/rootless-containers/rootlesskit/cmd/rootlesskit-docker-proxy; 	rm -rf "$GOPATH"; 	apk del --no-network .rootlesskit-build-deps; 	rootlesskit --version
# Wed, 11 Mar 2020 21:20:08 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Wed, 11 Mar 2020 21:20:09 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 11 Mar 2020 21:20:09 GMT
USER rootless
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd54125436dc48e0d60096d61457bcfd886136eb67815a60210ec67d3793096f`  
		Last Modified: Sat, 18 Jan 2020 04:43:03 GMT  
		Size: 2.4 MB (2425150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d1554c15cbb8c6b81fd21a057c8e97749fb24fd5befeb94ad960d3a350f91f`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dd17ef2c28fbb77b8b589e2e601e3ce86c0b9bcdb9dc73b6330d7ca16dca19`  
		Last Modified: Wed, 11 Mar 2020 21:20:40 GMT  
		Size: 64.2 MB (64218865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca57ea69baf170d62b8d1a51d898ff8d9383e22cd18bbde168ff539e74be8a4`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3af031952ce6719d5ca2f369b2187e1819fdab00252d315555a00048d6b99b7`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29377cccb214061fb46c1d5a1c27f53c366384d34f168cdb8484f5c7fcfb87a`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4939ff19fbb72e09aad6b10bc7440f9b23e0983f05c3cf6679a6392a40103b27`  
		Last Modified: Wed, 11 Mar 2020 21:20:48 GMT  
		Size: 5.6 MB (5598354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617664eed4c7060ec14f8178529d17b8a637b33a19f65101e062e185feda4c1`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8b6f7ec5ec983309648ff91b432c6abc38b547fc0610e3d81ab7e2472ad7ae`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 756.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb8de5d1a5be108527d435aef60a4a041879e0ddcf6d747ff324d57a5000f03`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 2.5 KB (2536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af40291eab6e7e25f86e0b385342cfe0318d38212a55bc20dd0aef9d3cc1a708`  
		Last Modified: Wed, 11 Mar 2020 21:20:56 GMT  
		Size: 796.0 KB (796003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd959232e7eccc0e2cb0117fb87809c0a4750269e1486a4ded4cbcff13c7b088`  
		Last Modified: Wed, 11 Mar 2020 21:20:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82aa1d69b9f04b015fb9771d9751d1e6cfe72d91da8d347c8bb83bde351f464b`  
		Last Modified: Wed, 11 Mar 2020 21:20:55 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cdb51a3ef0eb7411052a13cb5c1f4dbcb005a502d6805092f9d0006a963ad7`  
		Last Modified: Wed, 11 Mar 2020 21:20:57 GMT  
		Size: 9.1 MB (9109448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420ff93d35ca71a9e8a6fcfab5be9089f24b654a6c2c9f0fc46727937a534447`  
		Last Modified: Wed, 11 Mar 2020 21:20:57 GMT  
		Size: 13.6 MB (13594708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc08146368fd44217f9c582fc83a67d4d4b6844c8a9ed76700b579a514f8a4a`  
		Last Modified: Wed, 11 Mar 2020 21:20:54 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:stable-git`

```console
$ docker pull docker@sha256:4690f87ef12b57befc03948cfb45125e727469c886ce306268985ffc10c5f117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:stable-git` - linux; amd64

```console
$ docker pull docker@sha256:cb428bf67ff328e9cd57b5bbb64f04da465ef3198fbb8b0f0eb539144812cfe7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77662702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147d7d578318b63c7d01ee26605a981701192c4d365a7b72557655cae9225598`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 04:42:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 04:42:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:19:32 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:19:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:19:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:39 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:20:16 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd54125436dc48e0d60096d61457bcfd886136eb67815a60210ec67d3793096f`  
		Last Modified: Sat, 18 Jan 2020 04:43:03 GMT  
		Size: 2.4 MB (2425150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d1554c15cbb8c6b81fd21a057c8e97749fb24fd5befeb94ad960d3a350f91f`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dd17ef2c28fbb77b8b589e2e601e3ce86c0b9bcdb9dc73b6330d7ca16dca19`  
		Last Modified: Wed, 11 Mar 2020 21:20:40 GMT  
		Size: 64.2 MB (64218865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca57ea69baf170d62b8d1a51d898ff8d9383e22cd18bbde168ff539e74be8a4`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3af031952ce6719d5ca2f369b2187e1819fdab00252d315555a00048d6b99b7`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29377cccb214061fb46c1d5a1c27f53c366384d34f168cdb8484f5c7fcfb87a`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254b360be85b0840ff05885a92f88a8c9953477f040fda3328e6ea8eea86de6a`  
		Last Modified: Wed, 11 Mar 2020 21:21:05 GMT  
		Size: 8.2 MB (8213895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:stable-git` - linux; arm variant v6

```console
$ docker pull docker@sha256:e1850f9ae57922ee14a032dbf923d1efc8d553b02760378f562f1fb4fd2e499f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72737200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0522fe2ee7c4d185a532637aef5842258a77b0c068ec510a1ed61c9b78774eef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 05:52:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 05:52:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 05:52:35 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:49:22 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:49:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:49:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:49:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:49:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:49:38 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:50:01 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c86f804e7b5cc2f1f9d87340dfef1fcc13615f2cbd25bda470e513c1e4a627`  
		Last Modified: Sat, 18 Jan 2020 05:54:22 GMT  
		Size: 2.4 MB (2355405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d84775c03f92068112e3757afd6ddab1b2c0a3d1073e91b182620b6ec239f7`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592a77d3ce3aac4cb4c252c866f4a65c1541726b2bbdb512444569119b5cd98e`  
		Last Modified: Wed, 11 Mar 2020 21:50:37 GMT  
		Size: 59.9 MB (59927165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0277ab691262af1bf0bf50d6d459874dbf48509a6103991fd9d6225e455cb995`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320285a35393ed08c2ed85f5dc6d6ca6a1c07ac14fcfb8b4e1e5c5a4c30eace9`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e82c58148faac404a83fad42819c701567beb61dac6c2ae6d76ac1f97eefccd`  
		Last Modified: Wed, 11 Mar 2020 21:50:18 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162f34f6eb0f7762945f1e6a261e992d3923e55044cafaff16656007c3811c1d`  
		Last Modified: Wed, 11 Mar 2020 21:51:04 GMT  
		Size: 7.8 MB (7835202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:stable-git` - linux; arm variant v7

```console
$ docker pull docker@sha256:f47ed269de366a810d8e18b4df194fbcc6da43c3124ddaf516bb432d61b02804
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71675688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f090014780387159e6d1ca5236562fa2a275f196b6d7aba5d5afb8f3ad86a989`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:01:09 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 03:01:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 03:01:20 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:57:34 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:57:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:57:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:57:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:57:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:57:48 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:58:12 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5014010b799b2f3cc6305fd21cc4b096dd28ad093e165cea5976f92ccb8c462`  
		Last Modified: Sat, 18 Jan 2020 03:03:27 GMT  
		Size: 2.3 MB (2254397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f49247ef05003d569c198c4908b849fdadd330bf360c04360ae48fd0d68b6d`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca62e39536ad2825e9d1db7dbfa88f4cbc9d95659c5fb45691fa224654d2629`  
		Last Modified: Wed, 11 Mar 2020 21:58:49 GMT  
		Size: 59.9 MB (59927053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a96da9a069c4780e3c46bcbd35f4da5d0e173b2888bec333941260f131ccc8`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202349aaae9b658c7d87822ac340735af35c35495f6af77e5db0df2d253880ea`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f43ed55770aa202e0a559ef5505907bdf9e16eb7ea47829463da52a02907f9c`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877200202589a73b4d16451308a3e44508cb4df920be69143f584e1d64407f4c`  
		Last Modified: Wed, 11 Mar 2020 21:59:14 GMT  
		Size: 7.1 MB (7072817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:stable-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e940117143b12b2eac9c5565eda0db3bdf8d6f0a13068832eb96d84cafded257
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70963946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08226ded6b73a3e1734672484ecb773d61e8a1e9f50bf7e6f7cfa49ef1056e22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 02:23:05 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 02:23:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 02:23:12 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:39:44 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:39:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:39:52 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:39:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:39:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:39:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:39:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:39:56 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:40:21 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:8fa90b21c985a6fcfff966bdfbde81cdd088de0aa8af38110057f6ac408f4408`  
		Last Modified: Sat, 18 Jan 2020 01:40:23 GMT  
		Size: 2.7 MB (2723075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2917335fcb0a6856d5bf55430ba707c2c1378029a109e61959e62d2769230db`  
		Last Modified: Sat, 18 Jan 2020 02:25:35 GMT  
		Size: 2.4 MB (2445713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d3c84c2515134ddfa5ae5bac6e140953e9576fcd30a0bbc10fbc565d267895`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a828ac2f8d0e08bfd3c5405031bb245a21e469671397bd03e8868ce0925d9f49`  
		Last Modified: Wed, 11 Mar 2020 21:40:56 GMT  
		Size: 57.4 MB (57387269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7b0e4ac96f123613bb6ebd37a1bb99fb6f8a12b1d521f89f4211a970dbc077`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25581ce9dd66a29fecb3a63c9f888a0c6e3c68de7002441092b6a41dd833e995`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc58c5fdb432f00e6a7cdfa6b6507ca3c8598ab0612730e109e4faf5b0fc2d5a`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e0a8bd53622c572d715e352539b455c6a81b69ed96893f228292d785c5051f`  
		Last Modified: Wed, 11 Mar 2020 21:41:22 GMT  
		Size: 8.4 MB (8406022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:test`

```console
$ docker pull docker@sha256:948c0f302dae8ce62d28c32e46817c054cd5b00353fb0037646e92917a4124ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:test` - linux; amd64

```console
$ docker pull docker@sha256:7c311f0515f6e2bba92961cbd4c11ea7c74791935260c0c72c0ceebc75e52867
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69448807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f39826ae385e029ae634eb6a81091da60dae2e6ee2a19342c2e05ed4c3cb9171`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 04:42:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 04:42:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:19:32 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:19:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:19:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:39 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd54125436dc48e0d60096d61457bcfd886136eb67815a60210ec67d3793096f`  
		Last Modified: Sat, 18 Jan 2020 04:43:03 GMT  
		Size: 2.4 MB (2425150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d1554c15cbb8c6b81fd21a057c8e97749fb24fd5befeb94ad960d3a350f91f`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dd17ef2c28fbb77b8b589e2e601e3ce86c0b9bcdb9dc73b6330d7ca16dca19`  
		Last Modified: Wed, 11 Mar 2020 21:20:40 GMT  
		Size: 64.2 MB (64218865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca57ea69baf170d62b8d1a51d898ff8d9383e22cd18bbde168ff539e74be8a4`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3af031952ce6719d5ca2f369b2187e1819fdab00252d315555a00048d6b99b7`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29377cccb214061fb46c1d5a1c27f53c366384d34f168cdb8484f5c7fcfb87a`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test` - linux; arm variant v6

```console
$ docker pull docker@sha256:6066e1dbf8e74562362b84d31bfbf3356ab716c355e25d2fb3682f22f0016790
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64901998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbdbf0acc9e925c42921278175492252e55a006bf4ffff577bd68d5f1b29256a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 05:52:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 05:52:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 05:52:35 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:49:22 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:49:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:49:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:49:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:49:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:49:38 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c86f804e7b5cc2f1f9d87340dfef1fcc13615f2cbd25bda470e513c1e4a627`  
		Last Modified: Sat, 18 Jan 2020 05:54:22 GMT  
		Size: 2.4 MB (2355405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d84775c03f92068112e3757afd6ddab1b2c0a3d1073e91b182620b6ec239f7`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592a77d3ce3aac4cb4c252c866f4a65c1541726b2bbdb512444569119b5cd98e`  
		Last Modified: Wed, 11 Mar 2020 21:50:37 GMT  
		Size: 59.9 MB (59927165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0277ab691262af1bf0bf50d6d459874dbf48509a6103991fd9d6225e455cb995`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320285a35393ed08c2ed85f5dc6d6ca6a1c07ac14fcfb8b4e1e5c5a4c30eace9`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e82c58148faac404a83fad42819c701567beb61dac6c2ae6d76ac1f97eefccd`  
		Last Modified: Wed, 11 Mar 2020 21:50:18 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test` - linux; arm variant v7

```console
$ docker pull docker@sha256:32278b2c6a6b432c34a19367f68170d2bff8f79c57962f5cb4aab31f26130c6b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64602871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc2d0d6f635fee2fc5a74c78e7532a964940bead391471966dee40a29eeacc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:01:09 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 03:01:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 03:01:20 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:57:34 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:57:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:57:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:57:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:57:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:57:48 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5014010b799b2f3cc6305fd21cc4b096dd28ad093e165cea5976f92ccb8c462`  
		Last Modified: Sat, 18 Jan 2020 03:03:27 GMT  
		Size: 2.3 MB (2254397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f49247ef05003d569c198c4908b849fdadd330bf360c04360ae48fd0d68b6d`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca62e39536ad2825e9d1db7dbfa88f4cbc9d95659c5fb45691fa224654d2629`  
		Last Modified: Wed, 11 Mar 2020 21:58:49 GMT  
		Size: 59.9 MB (59927053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a96da9a069c4780e3c46bcbd35f4da5d0e173b2888bec333941260f131ccc8`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202349aaae9b658c7d87822ac340735af35c35495f6af77e5db0df2d253880ea`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f43ed55770aa202e0a559ef5505907bdf9e16eb7ea47829463da52a02907f9c`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f7f9c3b259b133a7cca0bfbe5db7f70c955aff499307e2714426c63fac9d5470
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62557924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea45e49e2b3cb4f5dc30b5f16f86e87e685949e8eb7ce7a98e59818c500dd823`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 02:23:05 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 02:23:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 02:23:12 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:39:44 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:39:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:39:52 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:39:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:39:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:39:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:39:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:39:56 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:8fa90b21c985a6fcfff966bdfbde81cdd088de0aa8af38110057f6ac408f4408`  
		Last Modified: Sat, 18 Jan 2020 01:40:23 GMT  
		Size: 2.7 MB (2723075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2917335fcb0a6856d5bf55430ba707c2c1378029a109e61959e62d2769230db`  
		Last Modified: Sat, 18 Jan 2020 02:25:35 GMT  
		Size: 2.4 MB (2445713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d3c84c2515134ddfa5ae5bac6e140953e9576fcd30a0bbc10fbc565d267895`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a828ac2f8d0e08bfd3c5405031bb245a21e469671397bd03e8868ce0925d9f49`  
		Last Modified: Wed, 11 Mar 2020 21:40:56 GMT  
		Size: 57.4 MB (57387269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7b0e4ac96f123613bb6ebd37a1bb99fb6f8a12b1d521f89f4211a970dbc077`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25581ce9dd66a29fecb3a63c9f888a0c6e3c68de7002441092b6a41dd833e995`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc58c5fdb432f00e6a7cdfa6b6507ca3c8598ab0612730e109e4faf5b0fc2d5a`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:test-dind`

```console
$ docker pull docker@sha256:308dcf9380af44ea492736e8d59605cd0ff2dab0527073f7e718ee4498e85dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:test-dind` - linux; amd64

```console
$ docker pull docker@sha256:0e6d34042007a6f5280838dc045af0d600654b57cd367251d1dd8bba4b55c773
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75051735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe98abf5dda7ec569bc4821f20ceca66945e67882fe32f960fb8b8f179af0e42`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 04:42:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 04:42:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:19:32 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:19:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:19:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:39 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:19:45 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Mar 2020 21:19:45 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:19:46 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Mar 2020 21:19:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Mar 2020 21:19:47 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:47 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Mar 2020 21:19:47 GMT
EXPOSE 2375 2376
# Wed, 11 Mar 2020 21:19:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:47 GMT
CMD []
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd54125436dc48e0d60096d61457bcfd886136eb67815a60210ec67d3793096f`  
		Last Modified: Sat, 18 Jan 2020 04:43:03 GMT  
		Size: 2.4 MB (2425150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d1554c15cbb8c6b81fd21a057c8e97749fb24fd5befeb94ad960d3a350f91f`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dd17ef2c28fbb77b8b589e2e601e3ce86c0b9bcdb9dc73b6330d7ca16dca19`  
		Last Modified: Wed, 11 Mar 2020 21:20:40 GMT  
		Size: 64.2 MB (64218865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca57ea69baf170d62b8d1a51d898ff8d9383e22cd18bbde168ff539e74be8a4`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3af031952ce6719d5ca2f369b2187e1819fdab00252d315555a00048d6b99b7`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29377cccb214061fb46c1d5a1c27f53c366384d34f168cdb8484f5c7fcfb87a`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4939ff19fbb72e09aad6b10bc7440f9b23e0983f05c3cf6679a6392a40103b27`  
		Last Modified: Wed, 11 Mar 2020 21:20:48 GMT  
		Size: 5.6 MB (5598354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617664eed4c7060ec14f8178529d17b8a637b33a19f65101e062e185feda4c1`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8b6f7ec5ec983309648ff91b432c6abc38b547fc0610e3d81ab7e2472ad7ae`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 756.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb8de5d1a5be108527d435aef60a4a041879e0ddcf6d747ff324d57a5000f03`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 2.5 KB (2536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:04246f289e63b1bc0baf3ee051e2374497207183b9e5b86373aa2f8938893a6c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68121997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08fff432f3d4cd1dae7778792ad2daa258d095691556f760fe82584bb66fa2b8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 05:52:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 05:52:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 05:52:35 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:49:22 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:49:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:49:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:49:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:49:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:49:38 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:49:46 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Mar 2020 21:49:48 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:49:49 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Mar 2020 21:49:51 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Mar 2020 21:49:51 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:49:52 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Mar 2020 21:49:52 GMT
EXPOSE 2375 2376
# Wed, 11 Mar 2020 21:49:53 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Mar 2020 21:49:53 GMT
CMD []
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c86f804e7b5cc2f1f9d87340dfef1fcc13615f2cbd25bda470e513c1e4a627`  
		Last Modified: Sat, 18 Jan 2020 05:54:22 GMT  
		Size: 2.4 MB (2355405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d84775c03f92068112e3757afd6ddab1b2c0a3d1073e91b182620b6ec239f7`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592a77d3ce3aac4cb4c252c866f4a65c1541726b2bbdb512444569119b5cd98e`  
		Last Modified: Wed, 11 Mar 2020 21:50:37 GMT  
		Size: 59.9 MB (59927165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0277ab691262af1bf0bf50d6d459874dbf48509a6103991fd9d6225e455cb995`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320285a35393ed08c2ed85f5dc6d6ca6a1c07ac14fcfb8b4e1e5c5a4c30eace9`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e82c58148faac404a83fad42819c701567beb61dac6c2ae6d76ac1f97eefccd`  
		Last Modified: Wed, 11 Mar 2020 21:50:18 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b1648a96394c26b0e7d5c254c39b36c8eca6d00dfff5aa3776cb6671284ead`  
		Last Modified: Wed, 11 Mar 2020 21:50:49 GMT  
		Size: 3.2 MB (3215398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e63bc9624da4519af0d163fc47db94ef5d7d0ae27deccb9d6b923ba97710251`  
		Last Modified: Wed, 11 Mar 2020 21:50:48 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8f7907ef28cfa8968f389a0e60d2b4a98f2b9da2963e09d86911a36e945825`  
		Last Modified: Wed, 11 Mar 2020 21:50:48 GMT  
		Size: 754.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013cac041612fcb3b3db97e63f70c7f357b31618cd79f2a0852b38181355f5bd`  
		Last Modified: Wed, 11 Mar 2020 21:50:48 GMT  
		Size: 2.5 KB (2532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:c2d6834d581a10f8d30ae8678d859ad15a3747335051665f21dbe7e602568a8a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67486006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd179934e0f1561bdac8a67db9bf33af7be9c1f7508bdb0c7aa76184817e0d62`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:01:09 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 03:01:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 03:01:20 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:57:34 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:57:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:57:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:57:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:57:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:57:48 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:57:57 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Mar 2020 21:57:59 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:58:00 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Mar 2020 21:58:02 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Mar 2020 21:58:02 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:58:03 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Mar 2020 21:58:03 GMT
EXPOSE 2375 2376
# Wed, 11 Mar 2020 21:58:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Mar 2020 21:58:05 GMT
CMD []
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5014010b799b2f3cc6305fd21cc4b096dd28ad093e165cea5976f92ccb8c462`  
		Last Modified: Sat, 18 Jan 2020 03:03:27 GMT  
		Size: 2.3 MB (2254397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f49247ef05003d569c198c4908b849fdadd330bf360c04360ae48fd0d68b6d`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca62e39536ad2825e9d1db7dbfa88f4cbc9d95659c5fb45691fa224654d2629`  
		Last Modified: Wed, 11 Mar 2020 21:58:49 GMT  
		Size: 59.9 MB (59927053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a96da9a069c4780e3c46bcbd35f4da5d0e173b2888bec333941260f131ccc8`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202349aaae9b658c7d87822ac340735af35c35495f6af77e5db0df2d253880ea`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f43ed55770aa202e0a559ef5505907bdf9e16eb7ea47829463da52a02907f9c`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466cffcfbb54d45db4bfc4d2a4ef125228d8adaa890f4bdf1b64c9305a00e67b`  
		Last Modified: Wed, 11 Mar 2020 21:59:01 GMT  
		Size: 2.9 MB (2878539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6759e573461d1a01a039d460c93cc7394fc6503dcbb5a199b318c51ea84a5b7`  
		Last Modified: Wed, 11 Mar 2020 21:59:00 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62db51a4792cce56454199be1d125345ae07f763e4fda4f56a955259f1ecba93`  
		Last Modified: Wed, 11 Mar 2020 21:59:00 GMT  
		Size: 754.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600fa87244d5da05152b4c389cc3f37aaf0b36cb70a7d0d4294feaeb52abbd12`  
		Last Modified: Wed, 11 Mar 2020 21:59:00 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6fcdb8d75a9f4a6ee01e57720cb5543bd81035db06ec821383dfde6a4371389e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68163443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac71857cf4ec95c719133d716baecc805697ff6ca79086a80b6e14a77d43d3bc`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 02:23:05 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 02:23:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 02:23:12 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:39:44 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:39:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:39:52 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:39:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:39:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:39:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:39:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:39:56 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:40:05 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Mar 2020 21:40:08 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:40:08 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Mar 2020 21:40:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Mar 2020 21:40:10 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:40:11 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Mar 2020 21:40:12 GMT
EXPOSE 2375 2376
# Wed, 11 Mar 2020 21:40:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Mar 2020 21:40:13 GMT
CMD []
```

-	Layers:
	-	`sha256:8fa90b21c985a6fcfff966bdfbde81cdd088de0aa8af38110057f6ac408f4408`  
		Last Modified: Sat, 18 Jan 2020 01:40:23 GMT  
		Size: 2.7 MB (2723075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2917335fcb0a6856d5bf55430ba707c2c1378029a109e61959e62d2769230db`  
		Last Modified: Sat, 18 Jan 2020 02:25:35 GMT  
		Size: 2.4 MB (2445713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d3c84c2515134ddfa5ae5bac6e140953e9576fcd30a0bbc10fbc565d267895`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a828ac2f8d0e08bfd3c5405031bb245a21e469671397bd03e8868ce0925d9f49`  
		Last Modified: Wed, 11 Mar 2020 21:40:56 GMT  
		Size: 57.4 MB (57387269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7b0e4ac96f123613bb6ebd37a1bb99fb6f8a12b1d521f89f4211a970dbc077`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25581ce9dd66a29fecb3a63c9f888a0c6e3c68de7002441092b6a41dd833e995`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc58c5fdb432f00e6a7cdfa6b6507ca3c8598ab0612730e109e4faf5b0fc2d5a`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d396bfbbbaa91436006cf0e8b86b9e00c9e49a1dcbcd557c3fc331afc8e9e2f3`  
		Last Modified: Wed, 11 Mar 2020 21:41:09 GMT  
		Size: 5.6 MB (5600915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3bdb37e40cba208e5d80d500a33700bdff3ad30ebbfcb014c89a614506038d`  
		Last Modified: Wed, 11 Mar 2020 21:41:07 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269e23372e2e87311644e618cb3e6c09eae4cc41d919662298578a9abfe476ed`  
		Last Modified: Wed, 11 Mar 2020 21:41:07 GMT  
		Size: 758.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6204a0f4fef03aefb0b6ae2c7dfee680f8a6d84e0f59324ded513c256255723`  
		Last Modified: Wed, 11 Mar 2020 21:41:07 GMT  
		Size: 2.5 KB (2535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:test-dind-rootless`

```console
$ docker pull docker@sha256:b1ba6b5c5d00fdfbf812971cbeb72a81bbb9fca8f70a1809b68c74968a49849c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:test-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:e0fbfc60a11eae3ce35434bd72828bf2d74b711dd3fd309ee36f646d69fd30a4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.6 MB (98553507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131e19ccffdf6245ad57a0ca98e0abd6e6cc5eb4495fe9358f90e1c9837de9c5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 04:42:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 04:42:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:19:32 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:19:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:19:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:39 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:19:45 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Mar 2020 21:19:45 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:19:46 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Mar 2020 21:19:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Mar 2020 21:19:47 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:47 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Mar 2020 21:19:47 GMT
EXPOSE 2375 2376
# Wed, 11 Mar 2020 21:19:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:47 GMT
CMD []
# Wed, 11 Mar 2020 21:19:52 GMT
RUN apk add --no-cache iproute2
# Wed, 11 Mar 2020 21:19:53 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Wed, 11 Mar 2020 21:19:54 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:19:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O rootless.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-rootless-extras-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-rootless-extras-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		vpnkit --version
# Wed, 11 Mar 2020 21:19:56 GMT
ENV ROOTLESSKIT_VERSION=0.9.1
# Wed, 11 Mar 2020 21:20:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .rootlesskit-build-deps 		go 		libc-dev 	; 	wget -O rootlesskit.tgz "https://github.com/rootless-containers/rootlesskit/archive/v${ROOTLESSKIT_VERSION}.tar.gz"; 	export GOPATH='/go'; mkdir "$GOPATH"; 	mkdir -p "$GOPATH/src/github.com/rootless-containers/rootlesskit"; 	tar --extract --file rootlesskit.tgz --directory "$GOPATH/src/github.com/rootless-containers/rootlesskit" --strip-components 1; 	rm rootlesskit.tgz; 	go build -o /usr/local/bin/rootlesskit github.com/rootless-containers/rootlesskit/cmd/rootlesskit; 	go build -o /usr/local/bin/rootlesskit-docker-proxy github.com/rootless-containers/rootlesskit/cmd/rootlesskit-docker-proxy; 	rm -rf "$GOPATH"; 	apk del --no-network .rootlesskit-build-deps; 	rootlesskit --version
# Wed, 11 Mar 2020 21:20:08 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Wed, 11 Mar 2020 21:20:09 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 11 Mar 2020 21:20:09 GMT
USER rootless
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd54125436dc48e0d60096d61457bcfd886136eb67815a60210ec67d3793096f`  
		Last Modified: Sat, 18 Jan 2020 04:43:03 GMT  
		Size: 2.4 MB (2425150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d1554c15cbb8c6b81fd21a057c8e97749fb24fd5befeb94ad960d3a350f91f`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dd17ef2c28fbb77b8b589e2e601e3ce86c0b9bcdb9dc73b6330d7ca16dca19`  
		Last Modified: Wed, 11 Mar 2020 21:20:40 GMT  
		Size: 64.2 MB (64218865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca57ea69baf170d62b8d1a51d898ff8d9383e22cd18bbde168ff539e74be8a4`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3af031952ce6719d5ca2f369b2187e1819fdab00252d315555a00048d6b99b7`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29377cccb214061fb46c1d5a1c27f53c366384d34f168cdb8484f5c7fcfb87a`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4939ff19fbb72e09aad6b10bc7440f9b23e0983f05c3cf6679a6392a40103b27`  
		Last Modified: Wed, 11 Mar 2020 21:20:48 GMT  
		Size: 5.6 MB (5598354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617664eed4c7060ec14f8178529d17b8a637b33a19f65101e062e185feda4c1`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8b6f7ec5ec983309648ff91b432c6abc38b547fc0610e3d81ab7e2472ad7ae`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 756.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb8de5d1a5be108527d435aef60a4a041879e0ddcf6d747ff324d57a5000f03`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 2.5 KB (2536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af40291eab6e7e25f86e0b385342cfe0318d38212a55bc20dd0aef9d3cc1a708`  
		Last Modified: Wed, 11 Mar 2020 21:20:56 GMT  
		Size: 796.0 KB (796003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd959232e7eccc0e2cb0117fb87809c0a4750269e1486a4ded4cbcff13c7b088`  
		Last Modified: Wed, 11 Mar 2020 21:20:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82aa1d69b9f04b015fb9771d9751d1e6cfe72d91da8d347c8bb83bde351f464b`  
		Last Modified: Wed, 11 Mar 2020 21:20:55 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cdb51a3ef0eb7411052a13cb5c1f4dbcb005a502d6805092f9d0006a963ad7`  
		Last Modified: Wed, 11 Mar 2020 21:20:57 GMT  
		Size: 9.1 MB (9109448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420ff93d35ca71a9e8a6fcfab5be9089f24b654a6c2c9f0fc46727937a534447`  
		Last Modified: Wed, 11 Mar 2020 21:20:57 GMT  
		Size: 13.6 MB (13594708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc08146368fd44217f9c582fc83a67d4d4b6844c8a9ed76700b579a514f8a4a`  
		Last Modified: Wed, 11 Mar 2020 21:20:54 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:test-git`

```console
$ docker pull docker@sha256:4690f87ef12b57befc03948cfb45125e727469c886ce306268985ffc10c5f117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:test-git` - linux; amd64

```console
$ docker pull docker@sha256:cb428bf67ff328e9cd57b5bbb64f04da465ef3198fbb8b0f0eb539144812cfe7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77662702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147d7d578318b63c7d01ee26605a981701192c4d365a7b72557655cae9225598`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 04:42:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 04:42:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:19:32 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:19:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:19:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:39 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:20:16 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd54125436dc48e0d60096d61457bcfd886136eb67815a60210ec67d3793096f`  
		Last Modified: Sat, 18 Jan 2020 04:43:03 GMT  
		Size: 2.4 MB (2425150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d1554c15cbb8c6b81fd21a057c8e97749fb24fd5befeb94ad960d3a350f91f`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dd17ef2c28fbb77b8b589e2e601e3ce86c0b9bcdb9dc73b6330d7ca16dca19`  
		Last Modified: Wed, 11 Mar 2020 21:20:40 GMT  
		Size: 64.2 MB (64218865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca57ea69baf170d62b8d1a51d898ff8d9383e22cd18bbde168ff539e74be8a4`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3af031952ce6719d5ca2f369b2187e1819fdab00252d315555a00048d6b99b7`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29377cccb214061fb46c1d5a1c27f53c366384d34f168cdb8484f5c7fcfb87a`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254b360be85b0840ff05885a92f88a8c9953477f040fda3328e6ea8eea86de6a`  
		Last Modified: Wed, 11 Mar 2020 21:21:05 GMT  
		Size: 8.2 MB (8213895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test-git` - linux; arm variant v6

```console
$ docker pull docker@sha256:e1850f9ae57922ee14a032dbf923d1efc8d553b02760378f562f1fb4fd2e499f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72737200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0522fe2ee7c4d185a532637aef5842258a77b0c068ec510a1ed61c9b78774eef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 05:52:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 05:52:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 05:52:35 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:49:22 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:49:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:49:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:49:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:49:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:49:38 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:50:01 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c86f804e7b5cc2f1f9d87340dfef1fcc13615f2cbd25bda470e513c1e4a627`  
		Last Modified: Sat, 18 Jan 2020 05:54:22 GMT  
		Size: 2.4 MB (2355405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d84775c03f92068112e3757afd6ddab1b2c0a3d1073e91b182620b6ec239f7`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592a77d3ce3aac4cb4c252c866f4a65c1541726b2bbdb512444569119b5cd98e`  
		Last Modified: Wed, 11 Mar 2020 21:50:37 GMT  
		Size: 59.9 MB (59927165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0277ab691262af1bf0bf50d6d459874dbf48509a6103991fd9d6225e455cb995`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320285a35393ed08c2ed85f5dc6d6ca6a1c07ac14fcfb8b4e1e5c5a4c30eace9`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e82c58148faac404a83fad42819c701567beb61dac6c2ae6d76ac1f97eefccd`  
		Last Modified: Wed, 11 Mar 2020 21:50:18 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162f34f6eb0f7762945f1e6a261e992d3923e55044cafaff16656007c3811c1d`  
		Last Modified: Wed, 11 Mar 2020 21:51:04 GMT  
		Size: 7.8 MB (7835202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test-git` - linux; arm variant v7

```console
$ docker pull docker@sha256:f47ed269de366a810d8e18b4df194fbcc6da43c3124ddaf516bb432d61b02804
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71675688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f090014780387159e6d1ca5236562fa2a275f196b6d7aba5d5afb8f3ad86a989`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:01:09 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 03:01:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 03:01:20 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:57:34 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:57:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:57:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:57:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:57:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:57:48 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:58:12 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5014010b799b2f3cc6305fd21cc4b096dd28ad093e165cea5976f92ccb8c462`  
		Last Modified: Sat, 18 Jan 2020 03:03:27 GMT  
		Size: 2.3 MB (2254397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f49247ef05003d569c198c4908b849fdadd330bf360c04360ae48fd0d68b6d`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca62e39536ad2825e9d1db7dbfa88f4cbc9d95659c5fb45691fa224654d2629`  
		Last Modified: Wed, 11 Mar 2020 21:58:49 GMT  
		Size: 59.9 MB (59927053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a96da9a069c4780e3c46bcbd35f4da5d0e173b2888bec333941260f131ccc8`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202349aaae9b658c7d87822ac340735af35c35495f6af77e5db0df2d253880ea`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f43ed55770aa202e0a559ef5505907bdf9e16eb7ea47829463da52a02907f9c`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877200202589a73b4d16451308a3e44508cb4df920be69143f584e1d64407f4c`  
		Last Modified: Wed, 11 Mar 2020 21:59:14 GMT  
		Size: 7.1 MB (7072817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e940117143b12b2eac9c5565eda0db3bdf8d6f0a13068832eb96d84cafded257
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70963946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08226ded6b73a3e1734672484ecb773d61e8a1e9f50bf7e6f7cfa49ef1056e22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 02:23:05 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 02:23:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 02:23:12 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:39:44 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:39:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:39:52 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:39:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:39:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:39:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:39:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:39:56 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:40:21 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:8fa90b21c985a6fcfff966bdfbde81cdd088de0aa8af38110057f6ac408f4408`  
		Last Modified: Sat, 18 Jan 2020 01:40:23 GMT  
		Size: 2.7 MB (2723075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2917335fcb0a6856d5bf55430ba707c2c1378029a109e61959e62d2769230db`  
		Last Modified: Sat, 18 Jan 2020 02:25:35 GMT  
		Size: 2.4 MB (2445713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d3c84c2515134ddfa5ae5bac6e140953e9576fcd30a0bbc10fbc565d267895`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a828ac2f8d0e08bfd3c5405031bb245a21e469671397bd03e8868ce0925d9f49`  
		Last Modified: Wed, 11 Mar 2020 21:40:56 GMT  
		Size: 57.4 MB (57387269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7b0e4ac96f123613bb6ebd37a1bb99fb6f8a12b1d521f89f4211a970dbc077`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25581ce9dd66a29fecb3a63c9f888a0c6e3c68de7002441092b6a41dd833e995`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc58c5fdb432f00e6a7cdfa6b6507ca3c8598ab0612730e109e4faf5b0fc2d5a`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e0a8bd53622c572d715e352539b455c6a81b69ed96893f228292d785c5051f`  
		Last Modified: Wed, 11 Mar 2020 21:41:22 GMT  
		Size: 8.4 MB (8406022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
