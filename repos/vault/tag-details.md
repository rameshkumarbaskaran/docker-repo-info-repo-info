<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `vault`

-	[`vault:1.4.7`](#vault147)
-	[`vault:1.5.7`](#vault157)
-	[`vault:1.6.3`](#vault163)
-	[`vault:1.7.0`](#vault170)
-	[`vault:1.7.0-rc1`](#vault170-rc1)
-	[`vault:1.7.0-rc2`](#vault170-rc2)
-	[`vault:latest`](#vaultlatest)

## `vault:1.4.7`

```console
$ docker pull vault@sha256:d1acbc06be11e7da479a6df08d4dac188222e545a67286d91565a8055454b017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.4.7` - linux; amd64

```console
$ docker pull vault@sha256:efce1d7a6d51f0f4a3ca11cdf71af5d4a26167540cec763aa26cda073f91b143
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52081953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399211ba7e802a8bc2671369bd03b209694dc6f5c1c5e6933078726005d782a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:48 GMT
ADD file:41685950b607fe90e0886c857e4efdafab1e43a09def174a4ea97f8ec624370b in / 
# Thu, 25 Mar 2021 22:19:48 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 05:04:30 GMT
ARG VAULT_VERSION=1.4.7
# Fri, 26 Mar 2021 05:04:31 GMT
# ARGS: VAULT_VERSION=1.4.7
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 26 Mar 2021 05:04:36 GMT
# ARGS: VAULT_VERSION=1.4.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 26 Mar 2021 05:04:37 GMT
# ARGS: VAULT_VERSION=1.4.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 26 Mar 2021 05:04:37 GMT
VOLUME [/vault/logs]
# Fri, 26 Mar 2021 05:04:38 GMT
VOLUME [/vault/file]
# Fri, 26 Mar 2021 05:04:38 GMT
EXPOSE 8200
# Fri, 26 Mar 2021 05:04:38 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 05:04:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 05:04:38 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:c8bc66e2636f8133df434e1bce741b6b7fb21515e7c8a554a805b73f5fdae2de`  
		Last Modified: Thu, 25 Mar 2021 22:20:57 GMT  
		Size: 2.8 MB (2797179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ac20e13ef02f7cef8d8a0a19bc6001ba5ebfc945fe2f40f7bfb1c19010b218`  
		Last Modified: Fri, 26 Mar 2021 05:06:39 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792a5e5d70ba9827ebb2518cab64bbcf5690de2777367e61a78cda687964692c`  
		Last Modified: Fri, 26 Mar 2021 05:06:48 GMT  
		Size: 49.3 MB (49281483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e6a499157b7cd8993a265416b1c026c2094e634e8340d2f8a43978ebef3ffd`  
		Last Modified: Fri, 26 Mar 2021 05:06:39 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a8342e9c9160b83f34a3520b9fc9e30ab48db104d1ae284b9cf6b41c8c1cdb`  
		Last Modified: Fri, 26 Mar 2021 05:06:39 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.4.7` - linux; arm variant v6

```console
$ docker pull vault@sha256:d0dca2f945d8e822b6a03243a6c4415616182dae7f7ff6c047800fb6d57c2f6e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48719926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:332eecd75d39566a3836c088ee1b7c0d91dc68b8d57ccabad4018b91e0773fca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 31 Mar 2021 17:19:28 GMT
ADD file:c67892974e87ac461e5f35f8cbbc4f25201ec62130f4e8691e52d79679fc10db in / 
# Wed, 31 Mar 2021 17:19:30 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 03:58:33 GMT
ARG VAULT_VERSION=1.4.7
# Thu, 01 Apr 2021 03:58:36 GMT
# ARGS: VAULT_VERSION=1.4.7
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 01 Apr 2021 03:58:47 GMT
# ARGS: VAULT_VERSION=1.4.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 01 Apr 2021 03:58:52 GMT
# ARGS: VAULT_VERSION=1.4.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 01 Apr 2021 03:58:53 GMT
VOLUME [/vault/logs]
# Thu, 01 Apr 2021 03:58:55 GMT
VOLUME [/vault/file]
# Thu, 01 Apr 2021 03:58:57 GMT
EXPOSE 8200
# Thu, 01 Apr 2021 03:58:58 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 01 Apr 2021 03:58:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 03:59:01 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:be6c23f3cb48f40fb3644ad115f4edc90f13074ffe485e8a6cdb64d36450000d`  
		Last Modified: Wed, 31 Mar 2021 17:20:28 GMT  
		Size: 2.6 MB (2574738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d5f49a707d58744b3f2f9090c7b32ae943e59a356e14b1e34b3dc5ebcddc45`  
		Last Modified: Thu, 01 Apr 2021 04:01:14 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dea79ab9087b53a729823f42ab9fb00712fb2c818e88ace527e3cc34eba2c41`  
		Last Modified: Thu, 01 Apr 2021 04:01:27 GMT  
		Size: 46.1 MB (46141890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bacb85e2fcebdd7abec669bf90f60f7c743a67a54f8f7750154481a8dbbc85a7`  
		Last Modified: Thu, 01 Apr 2021 04:01:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5348eb55f5cdf6d57790efcfa0a9ff2e43de7fa86c9c62561ea8db52e4c2781`  
		Last Modified: Thu, 01 Apr 2021 04:01:14 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.4.7` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:8cc9b11c41d3d548f20c9372abe9c2fa61cb76d88d001fd4dd7c53c37eb5bb21
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48964606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cfcc717da55b17d38d94ab422a30a7fddbfe1ad425f21a04958c987615f49eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 25 Mar 2021 22:42:23 GMT
ADD file:a65de3d22c60aa364e967325d628757aa1f842fbefa48420403da87f91e9b7fd in / 
# Thu, 25 Mar 2021 22:42:41 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 08:15:41 GMT
ARG VAULT_VERSION=1.4.7
# Fri, 26 Mar 2021 08:15:44 GMT
# ARGS: VAULT_VERSION=1.4.7
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 26 Mar 2021 08:15:52 GMT
# ARGS: VAULT_VERSION=1.4.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 26 Mar 2021 08:15:55 GMT
# ARGS: VAULT_VERSION=1.4.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 26 Mar 2021 08:15:56 GMT
VOLUME [/vault/logs]
# Fri, 26 Mar 2021 08:15:57 GMT
VOLUME [/vault/file]
# Fri, 26 Mar 2021 08:15:58 GMT
EXPOSE 8200
# Fri, 26 Mar 2021 08:15:59 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 08:15:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 08:16:00 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:c7baec6fc76f48bce7341e4ed36b01d548ba0189f534e42f20fa08c907fe9961`  
		Last Modified: Thu, 25 Mar 2021 22:46:29 GMT  
		Size: 2.7 MB (2720368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a43479f256af47516077cd77761ad6cd5700477be79ea80adc876bfc4755b1`  
		Last Modified: Fri, 26 Mar 2021 08:18:15 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae474a0d021cea326bee7d13a234f92067fde4ab5bb303964aeac19d3a97f47`  
		Last Modified: Fri, 26 Mar 2021 08:18:25 GMT  
		Size: 46.2 MB (46240944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8e9c39d5db46d135a7ef39e9d02fc580a16b124dc132571eda0f1266a4b567`  
		Last Modified: Fri, 26 Mar 2021 08:18:15 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895e239fcedd3726c9988f1acae38413fcc730cc6c6871340984dc7dc7a5c6c4`  
		Last Modified: Fri, 26 Mar 2021 08:18:15 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.4.7` - linux; 386

```console
$ docker pull vault@sha256:fd94a95b062e2263a6bb6a4acbbb4f068ef0b62334dfce2eb71a4fad60dac8e7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50214674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edaaf1726e365fbf040060e70a28136fb36703136ff9016c0cd09f2dc23dfa2a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 31 Mar 2021 17:43:22 GMT
ADD file:7c227b0f23be0e208436424088c5275e9c1f6c62278ba35d6932e866af7cd534 in / 
# Wed, 31 Mar 2021 17:43:22 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 07:40:34 GMT
ARG VAULT_VERSION=1.4.7
# Thu, 01 Apr 2021 07:40:35 GMT
# ARGS: VAULT_VERSION=1.4.7
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 01 Apr 2021 07:40:46 GMT
# ARGS: VAULT_VERSION=1.4.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 01 Apr 2021 07:40:47 GMT
# ARGS: VAULT_VERSION=1.4.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 01 Apr 2021 07:40:47 GMT
VOLUME [/vault/logs]
# Thu, 01 Apr 2021 07:40:48 GMT
VOLUME [/vault/file]
# Thu, 01 Apr 2021 07:40:48 GMT
EXPOSE 8200
# Thu, 01 Apr 2021 07:40:48 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 01 Apr 2021 07:40:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 07:40:49 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:04a0b419ffe8e723a360cb667a2dace5907d4c994fb4da925108371a2936f954`  
		Last Modified: Wed, 31 Mar 2021 17:44:51 GMT  
		Size: 2.8 MB (2788886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d12935759d706f774b74906a761ee982e1b3c3c3c93f9494e97879acc4890ac5`  
		Last Modified: Thu, 01 Apr 2021 07:43:01 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9adc5f55a834e81d2a7e942d6eefcdacbf899e7a37c9e00cb79074eef121f0e`  
		Last Modified: Thu, 01 Apr 2021 07:43:07 GMT  
		Size: 47.4 MB (47422493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc49f6a441aa3c2f0ae71a27ce2e2c82f332d26dead16f6a0ee8658b3991a9b9`  
		Last Modified: Thu, 01 Apr 2021 07:43:01 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3d4915b3cded174f4bf62ac3895cd84bd76fea0f134c3df0e1806e5c95c673`  
		Last Modified: Thu, 01 Apr 2021 07:43:01 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.5.7`

```console
$ docker pull vault@sha256:3bef396c9548b38378a25ef99d16c17807ccf643c720fe0d52618c23b8f8dc2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.5.7` - linux; amd64

```console
$ docker pull vault@sha256:90f81843d6449824ebc3f69a6337145c62d2d25066856d4fa3d20a819f8aabe2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (55009991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8968f6dc172f97547ec98d8a82de53bbb25c71362e5e3b4e088328ba7065805d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:48 GMT
ADD file:41685950b607fe90e0886c857e4efdafab1e43a09def174a4ea97f8ec624370b in / 
# Thu, 25 Mar 2021 22:19:48 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 05:04:17 GMT
ARG VAULT_VERSION=1.5.7
# Fri, 26 Mar 2021 05:04:18 GMT
# ARGS: VAULT_VERSION=1.5.7
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 26 Mar 2021 05:04:24 GMT
# ARGS: VAULT_VERSION=1.5.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 26 Mar 2021 05:04:25 GMT
# ARGS: VAULT_VERSION=1.5.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 26 Mar 2021 05:04:25 GMT
VOLUME [/vault/logs]
# Fri, 26 Mar 2021 05:04:26 GMT
VOLUME [/vault/file]
# Fri, 26 Mar 2021 05:04:26 GMT
EXPOSE 8200
# Fri, 26 Mar 2021 05:04:26 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 05:04:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 05:04:26 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:c8bc66e2636f8133df434e1bce741b6b7fb21515e7c8a554a805b73f5fdae2de`  
		Last Modified: Thu, 25 Mar 2021 22:20:57 GMT  
		Size: 2.8 MB (2797179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33fd36bf290dbeb2f64ce41780423d3530d00e5aa3337b545e5be3d52a3bf7f`  
		Last Modified: Fri, 26 Mar 2021 05:06:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604044eae043c2d599c3f06d97fdc7cf15e332bddb95a175f922716cb652a186`  
		Last Modified: Fri, 26 Mar 2021 05:06:30 GMT  
		Size: 52.2 MB (52209515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfa123b5cb9b8cd356acd7fee7a8d082beae1567ab06505be83708d6ee1c444`  
		Last Modified: Fri, 26 Mar 2021 05:06:21 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1089c5632db335189e5a662717d29f38293ac08eab3a4df6057de2c9b82c05e9`  
		Last Modified: Fri, 26 Mar 2021 05:06:21 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.5.7` - linux; arm variant v6

```console
$ docker pull vault@sha256:3357d3045a27aa29c392cd93bae177ad9391598ee4fd35c4e62cd24cc7847401
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51563662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:febf1562db612f245583630216a74b0e1ebdb85a97310e8b7f82f404ee5b8e57`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 31 Mar 2021 17:19:28 GMT
ADD file:c67892974e87ac461e5f35f8cbbc4f25201ec62130f4e8691e52d79679fc10db in / 
# Wed, 31 Mar 2021 17:19:30 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 03:57:59 GMT
ARG VAULT_VERSION=1.5.7
# Thu, 01 Apr 2021 03:58:03 GMT
# ARGS: VAULT_VERSION=1.5.7
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 01 Apr 2021 03:58:14 GMT
# ARGS: VAULT_VERSION=1.5.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 01 Apr 2021 03:58:18 GMT
# ARGS: VAULT_VERSION=1.5.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 01 Apr 2021 03:58:19 GMT
VOLUME [/vault/logs]
# Thu, 01 Apr 2021 03:58:21 GMT
VOLUME [/vault/file]
# Thu, 01 Apr 2021 03:58:21 GMT
EXPOSE 8200
# Thu, 01 Apr 2021 03:58:22 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 01 Apr 2021 03:58:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 03:58:25 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:be6c23f3cb48f40fb3644ad115f4edc90f13074ffe485e8a6cdb64d36450000d`  
		Last Modified: Wed, 31 Mar 2021 17:20:28 GMT  
		Size: 2.6 MB (2574738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8c983a5d00827bd572e20fc04f3b39fc56a3d650e35bf1679a95b85209d50f`  
		Last Modified: Thu, 01 Apr 2021 04:00:51 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbfa587963d2764da1967eeba7dce68b51ffa2523c024d632ca6e7f93f658129`  
		Last Modified: Thu, 01 Apr 2021 04:01:04 GMT  
		Size: 49.0 MB (48985628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49da638d8131344e1b62846c51c54389349d6cfa71a20fb24f3e818975032e17`  
		Last Modified: Thu, 01 Apr 2021 04:00:51 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d162537167491a21b4cee6e7262250273c6088e550411f6915420050dc37006`  
		Last Modified: Thu, 01 Apr 2021 04:00:51 GMT  
		Size: 1.8 KB (1819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.5.7` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:a95ddb80eb8d0c528b68974f538dc308daf195868b57ecaba9975d636de4949a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51917984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb5afa9dc4e2053dbc36a399c95c55408b70ee67c61e9d8d2a2a8fc135ab810d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 25 Mar 2021 22:42:23 GMT
ADD file:a65de3d22c60aa364e967325d628757aa1f842fbefa48420403da87f91e9b7fd in / 
# Thu, 25 Mar 2021 22:42:41 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 08:15:13 GMT
ARG VAULT_VERSION=1.5.7
# Fri, 26 Mar 2021 08:15:16 GMT
# ARGS: VAULT_VERSION=1.5.7
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 26 Mar 2021 08:15:25 GMT
# ARGS: VAULT_VERSION=1.5.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 26 Mar 2021 08:15:28 GMT
# ARGS: VAULT_VERSION=1.5.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 26 Mar 2021 08:15:29 GMT
VOLUME [/vault/logs]
# Fri, 26 Mar 2021 08:15:30 GMT
VOLUME [/vault/file]
# Fri, 26 Mar 2021 08:15:31 GMT
EXPOSE 8200
# Fri, 26 Mar 2021 08:15:32 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 08:15:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 08:15:34 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:c7baec6fc76f48bce7341e4ed36b01d548ba0189f534e42f20fa08c907fe9961`  
		Last Modified: Thu, 25 Mar 2021 22:46:29 GMT  
		Size: 2.7 MB (2720368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e0a85d4ff4095a26e8bc5aecdcf86033817a2419927df41e869eb3cee1e384`  
		Last Modified: Fri, 26 Mar 2021 08:17:57 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc46f6ebf437349f70be56b14aade2473e49e4ff664b83ed9d21d25549fbd569`  
		Last Modified: Fri, 26 Mar 2021 08:18:08 GMT  
		Size: 49.2 MB (49194320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e1ea1af4f2afe8c0e2ff20a247ae1c2da0eae1904afe755185b87a5c6c4298`  
		Last Modified: Fri, 26 Mar 2021 08:17:57 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d247919a344e41e07c2ec2ef609bb3331181db07e7ce9dedaf0583c0516f9b43`  
		Last Modified: Fri, 26 Mar 2021 08:17:58 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.5.7` - linux; 386

```console
$ docker pull vault@sha256:8d53fdcfb6eb252827d4f8c2410b7ab39ddc84ac75d92997418edabb3158e7ab
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53087413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc0466cda58f7b40445e9c0dfbdf883b7cfaecf277ce6f141ea95c5d479a5fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 31 Mar 2021 17:43:22 GMT
ADD file:7c227b0f23be0e208436424088c5275e9c1f6c62278ba35d6932e866af7cd534 in / 
# Wed, 31 Mar 2021 17:43:22 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 07:40:18 GMT
ARG VAULT_VERSION=1.5.7
# Thu, 01 Apr 2021 07:40:19 GMT
# ARGS: VAULT_VERSION=1.5.7
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 01 Apr 2021 07:40:26 GMT
# ARGS: VAULT_VERSION=1.5.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 01 Apr 2021 07:40:27 GMT
# ARGS: VAULT_VERSION=1.5.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 01 Apr 2021 07:40:27 GMT
VOLUME [/vault/logs]
# Thu, 01 Apr 2021 07:40:28 GMT
VOLUME [/vault/file]
# Thu, 01 Apr 2021 07:40:28 GMT
EXPOSE 8200
# Thu, 01 Apr 2021 07:40:28 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 01 Apr 2021 07:40:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 07:40:29 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:04a0b419ffe8e723a360cb667a2dace5907d4c994fb4da925108371a2936f954`  
		Last Modified: Wed, 31 Mar 2021 17:44:51 GMT  
		Size: 2.8 MB (2788886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4c93180af1ac026f74867f66f738819c3a6c5f61ce7c1a055d025fe25326fd`  
		Last Modified: Thu, 01 Apr 2021 07:42:42 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea8ba055ad0de265a31174c8fb41a36721f210f7021d624f174a48ba13c0ccd`  
		Last Modified: Thu, 01 Apr 2021 07:42:51 GMT  
		Size: 50.3 MB (50295233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296db6c0defdd53542aeb869240130df1474e3e19a6659675aabcea35d6b0159`  
		Last Modified: Thu, 01 Apr 2021 07:42:42 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9552c0192dae283787dea14ffad97c75386c9c308b42100c6595c0509dc0f5ee`  
		Last Modified: Thu, 01 Apr 2021 07:42:43 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.6.3`

```console
$ docker pull vault@sha256:e290600e3a472e061283f161f83f1f3fbd2e54be29ac7f27c2ece08bada8007a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.6.3` - linux; amd64

```console
$ docker pull vault@sha256:c3b98bbd8e571bd76e97f692d90143d949251fbb95a6160a1c2344f5e0560cc9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68982834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7363ef5cdf1e5d2c2ce8c20a274dcfb37c91bce0ba6f6370e30b1b097ab8b224`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:32 GMT
ADD file:6b081cabb4b256ee07587d249c4989b5b679375529542b81550a65b6f19f274e in / 
# Thu, 25 Mar 2021 22:19:32 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 05:04:01 GMT
ARG VAULT_VERSION=1.6.3
# Fri, 26 Mar 2021 05:04:03 GMT
# ARGS: VAULT_VERSION=1.6.3
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 26 Mar 2021 05:04:11 GMT
# ARGS: VAULT_VERSION=1.6.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 26 Mar 2021 05:04:12 GMT
# ARGS: VAULT_VERSION=1.6.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 26 Mar 2021 05:04:12 GMT
VOLUME [/vault/logs]
# Fri, 26 Mar 2021 05:04:13 GMT
VOLUME [/vault/file]
# Fri, 26 Mar 2021 05:04:13 GMT
EXPOSE 8200
# Fri, 26 Mar 2021 05:04:13 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 05:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 05:04:14 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:9aae54b2144e5b2b00c610f8805128f4f86822e1e52d3714c463744a431f0f4a`  
		Last Modified: Thu, 25 Mar 2021 22:20:18 GMT  
		Size: 2.8 MB (2811681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a434ea0ba104f607ea9e907135e6d9864d4607d7fccdacb450799d2c28926918`  
		Last Modified: Fri, 26 Mar 2021 05:05:57 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680018afd3e10264426e015a9df3efb577e55a7f34471e3e5eb600497d844c88`  
		Last Modified: Fri, 26 Mar 2021 05:06:09 GMT  
		Size: 66.2 MB (66167888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba35ea1e81e0aa2b819506fba7d623924a50f9017c2bd6842c6be4f03f61825`  
		Last Modified: Fri, 26 Mar 2021 05:05:57 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780a58f777556d5839094a1fcdb8a6c187b632455943fc301acbdab08e177c28`  
		Last Modified: Fri, 26 Mar 2021 05:05:57 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.6.3` - linux; arm variant v6

```console
$ docker pull vault@sha256:af3df371e4c0af651fa91ed7fa02eda3d25caa5f02b7a545bee9769e4467fa94
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63718984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3a600bd0006785302e582f039df932398490653cff3ccc7e525751a901e96f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 31 Mar 2021 17:18:49 GMT
ADD file:988879d74f643b89539e5a0b6d74221621f19f4f87f722614addadc46ce47200 in / 
# Wed, 31 Mar 2021 17:18:50 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 03:57:28 GMT
ARG VAULT_VERSION=1.6.3
# Thu, 01 Apr 2021 03:57:30 GMT
# ARGS: VAULT_VERSION=1.6.3
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 01 Apr 2021 03:57:42 GMT
# ARGS: VAULT_VERSION=1.6.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 01 Apr 2021 03:57:45 GMT
# ARGS: VAULT_VERSION=1.6.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 01 Apr 2021 03:57:46 GMT
VOLUME [/vault/logs]
# Thu, 01 Apr 2021 03:57:47 GMT
VOLUME [/vault/file]
# Thu, 01 Apr 2021 03:57:48 GMT
EXPOSE 8200
# Thu, 01 Apr 2021 03:57:49 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 01 Apr 2021 03:57:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 03:57:50 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:bb87125c6ee1ce30c6b33d2c96a9fbe46da4a290f7cb1dd73fd62d4e06503699`  
		Last Modified: Wed, 31 Mar 2021 17:19:55 GMT  
		Size: 2.6 MB (2622116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ce309e6e5a01b40af1594950ece8755a1bfe5379c7691aed095109f568c05b`  
		Last Modified: Thu, 01 Apr 2021 04:00:29 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc750f866fd134ec1f96948dbd2e62a9cfd08868d3b162e0034ff22e3463578`  
		Last Modified: Thu, 01 Apr 2021 04:00:44 GMT  
		Size: 61.1 MB (61093605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97926d0b63a116ed6da0e06032e50ff30a5c5d794fa401841a7dfb1e8101e95a`  
		Last Modified: Thu, 01 Apr 2021 04:00:29 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c300997714121a041f195730b3bdcefccd443081666432fe426b57feb9376a`  
		Last Modified: Thu, 01 Apr 2021 04:00:29 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.6.3` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:2a3fcd4e44aa5291ed10b2535e9d13e04875f025154d6f086a8c8eef940a2f03
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (65016293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8209178a8a480af25fec96281f3f0b640654a477048db02d9b78aebda10fb20e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 25 Mar 2021 22:40:10 GMT
ADD file:8d7431f7e3e42b162a1626e7abf4ef7605146671dccc753d490de6b7fe429261 in / 
# Thu, 25 Mar 2021 22:40:23 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 08:14:46 GMT
ARG VAULT_VERSION=1.6.3
# Fri, 26 Mar 2021 08:14:48 GMT
# ARGS: VAULT_VERSION=1.6.3
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 26 Mar 2021 08:14:57 GMT
# ARGS: VAULT_VERSION=1.6.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 26 Mar 2021 08:15:01 GMT
# ARGS: VAULT_VERSION=1.6.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 26 Mar 2021 08:15:02 GMT
VOLUME [/vault/logs]
# Fri, 26 Mar 2021 08:15:02 GMT
VOLUME [/vault/file]
# Fri, 26 Mar 2021 08:15:03 GMT
EXPOSE 8200
# Fri, 26 Mar 2021 08:15:04 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 08:15:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 08:15:06 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:5ceb5101e3b0d54efb5f18318982508a04b181b4d5ae52b096dd35dea3a006cc`  
		Last Modified: Thu, 25 Mar 2021 22:44:41 GMT  
		Size: 2.7 MB (2711898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b2f8b128aa711c1ad9c2d3b773b7b6f8d48d41ef140e2eeedea8c88b47b3ca`  
		Last Modified: Fri, 26 Mar 2021 08:17:37 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6492bdc2fc593fa06a5274d2109adadc62453a6585e29b876ff28786e7238f9`  
		Last Modified: Fri, 26 Mar 2021 08:17:51 GMT  
		Size: 62.3 MB (62301127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d803c1830a0df4de0f473e700c19f5ad71456dcc4561a33f10e97f47448a7466`  
		Last Modified: Fri, 26 Mar 2021 08:17:37 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2652120b47a31370fe540e0b4795336e64d41651f48ed34a6747f40c9d43bbd5`  
		Last Modified: Fri, 26 Mar 2021 08:17:37 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.6.3` - linux; 386

```console
$ docker pull vault@sha256:264ad1c2dc56cee7d0084792d154b6d0ebeba6a3803e889a92da3e8657b67d78
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (67033806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b003192a1cc10541ddc869e8ffe0939d4ceed0c257cad42caca94852bedbcd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 31 Mar 2021 17:43:00 GMT
ADD file:245767f958e2b5e6fad41d45d3361849e7c6b2255303e3c785f0f2c86019553a in / 
# Wed, 31 Mar 2021 17:43:00 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 07:39:51 GMT
ARG VAULT_VERSION=1.6.3
# Thu, 01 Apr 2021 07:39:51 GMT
# ARGS: VAULT_VERSION=1.6.3
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 01 Apr 2021 07:40:09 GMT
# ARGS: VAULT_VERSION=1.6.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 01 Apr 2021 07:40:10 GMT
# ARGS: VAULT_VERSION=1.6.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 01 Apr 2021 07:40:11 GMT
VOLUME [/vault/logs]
# Thu, 01 Apr 2021 07:40:11 GMT
VOLUME [/vault/file]
# Thu, 01 Apr 2021 07:40:11 GMT
EXPOSE 8200
# Thu, 01 Apr 2021 07:40:11 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 01 Apr 2021 07:40:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 07:40:12 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:b22e590ebf70a9a5901c380b07232ef3c07cb13440402934dfdffb8f8721a949`  
		Last Modified: Wed, 31 Mar 2021 17:44:05 GMT  
		Size: 2.8 MB (2818802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd19dd98dc640a3767602128f49255ee769d83548842d11ad6e3ef1740b2619`  
		Last Modified: Thu, 01 Apr 2021 07:42:18 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805151cbb986e3fcd3f9d86bd93e662de8bf352ab4834e0b3f40b14d09798bbd`  
		Last Modified: Thu, 01 Apr 2021 07:42:33 GMT  
		Size: 64.2 MB (64211740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c20b08ef78c8b4dda1c38c8fbe81144c2e60fb8e271ba14415e7b9cdefe6e4`  
		Last Modified: Thu, 01 Apr 2021 07:42:18 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8902e15ecbb84df8e81b22cb54101ab6a1ca6a5def92f186ba2cde9857e6d42`  
		Last Modified: Thu, 01 Apr 2021 07:42:18 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.7.0`

```console
$ docker pull vault@sha256:6bf0c0e22aeee4fa42d22fc5a201c8901818edee9c4bf12151d40aea2318d966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.7.0` - linux; amd64

```console
$ docker pull vault@sha256:d51a9c82d0d45857acabea988c7b2ec673855438a7718138569d199e80db2ad3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72706694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b359df68a663cd5d2528caab398298a176375aeaa13ae199d8b5f615c2a38bce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:32 GMT
ADD file:6b081cabb4b256ee07587d249c4989b5b679375529542b81550a65b6f19f274e in / 
# Thu, 25 Mar 2021 22:19:32 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 05:02:55 GMT
ARG VAULT_VERSION=1.7.0
# Fri, 26 Mar 2021 05:02:56 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 26 Mar 2021 05:03:07 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 26 Mar 2021 05:03:09 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 26 Mar 2021 05:03:09 GMT
VOLUME [/vault/logs]
# Fri, 26 Mar 2021 05:03:09 GMT
VOLUME [/vault/file]
# Fri, 26 Mar 2021 05:03:10 GMT
EXPOSE 8200
# Fri, 26 Mar 2021 05:03:10 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 05:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 05:03:11 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:9aae54b2144e5b2b00c610f8805128f4f86822e1e52d3714c463744a431f0f4a`  
		Last Modified: Thu, 25 Mar 2021 22:20:18 GMT  
		Size: 2.8 MB (2811681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1d6dd05beb921063752a0e4b43d2dc08582069eaaeb4e32ffa7a370ede3515`  
		Last Modified: Fri, 26 Mar 2021 05:04:52 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4de46febc3613de2118ec655d1fffbe87968c11570858a476e7dc4fd74c6ff4`  
		Last Modified: Fri, 26 Mar 2021 05:05:03 GMT  
		Size: 69.9 MB (69891751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc279c1e752b4ac2f1af5f2c54603b7bbf0e712414a1383d79b2c684b895ff4`  
		Last Modified: Fri, 26 Mar 2021 05:04:52 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e437bfd1f45e31c4442a7038debd89139a36421ac53cf2e579c1f773a45432ea`  
		Last Modified: Fri, 26 Mar 2021 05:04:52 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.0` - linux; arm variant v6

```console
$ docker pull vault@sha256:767919f77e45c4294de6e32d3b893b5036c762e51d560b76330932192e404d2f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66726620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8bde904bf2e29386a8fb240f6b1fb95f45ebf9d38f7fe2077517b1b514eb4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 31 Mar 2021 17:18:49 GMT
ADD file:988879d74f643b89539e5a0b6d74221621f19f4f87f722614addadc46ce47200 in / 
# Wed, 31 Mar 2021 17:18:50 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 03:55:36 GMT
ARG VAULT_VERSION=1.7.0
# Thu, 01 Apr 2021 03:55:38 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 01 Apr 2021 03:55:51 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 01 Apr 2021 03:55:54 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 01 Apr 2021 03:55:55 GMT
VOLUME [/vault/logs]
# Thu, 01 Apr 2021 03:55:56 GMT
VOLUME [/vault/file]
# Thu, 01 Apr 2021 03:55:57 GMT
EXPOSE 8200
# Thu, 01 Apr 2021 03:55:58 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 01 Apr 2021 03:55:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 03:55:59 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:bb87125c6ee1ce30c6b33d2c96a9fbe46da4a290f7cb1dd73fd62d4e06503699`  
		Last Modified: Wed, 31 Mar 2021 17:19:55 GMT  
		Size: 2.6 MB (2622116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad73fe886cac5dcb33a379031cfe005dda18d2607759d02d567e1a7f3f92dbdc`  
		Last Modified: Thu, 01 Apr 2021 03:59:20 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5ffa7fbdf0fe366fdafb6a2123b019f1febe00b3c8ce5ab4c74d95b9b1512d`  
		Last Modified: Thu, 01 Apr 2021 03:59:36 GMT  
		Size: 64.1 MB (64101238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f0d98dbcea4800176a5738fab3df0551316a16e5268fb5cc21cdf4b308ab390`  
		Last Modified: Thu, 01 Apr 2021 03:59:20 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9187438e2855de2e5af03cd0105dd1eb20593f9ad6f0b5f166eb83324d20402`  
		Last Modified: Thu, 01 Apr 2021 03:59:20 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.0` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:7bb03087f1872bba59add852953ac3e35a54d63798a5a42d53cc147d335150d4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68535695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7c6e9941803130f0b68e0749e872a59bd13cd4c57b0aae51a46a532a37a3d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 25 Mar 2021 22:40:10 GMT
ADD file:8d7431f7e3e42b162a1626e7abf4ef7605146671dccc753d490de6b7fe429261 in / 
# Thu, 25 Mar 2021 22:40:23 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 08:13:10 GMT
ARG VAULT_VERSION=1.7.0
# Fri, 26 Mar 2021 08:13:13 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 26 Mar 2021 08:13:22 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 26 Mar 2021 08:13:25 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 26 Mar 2021 08:13:27 GMT
VOLUME [/vault/logs]
# Fri, 26 Mar 2021 08:13:28 GMT
VOLUME [/vault/file]
# Fri, 26 Mar 2021 08:13:30 GMT
EXPOSE 8200
# Fri, 26 Mar 2021 08:13:31 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 08:13:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 08:13:33 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:5ceb5101e3b0d54efb5f18318982508a04b181b4d5ae52b096dd35dea3a006cc`  
		Last Modified: Thu, 25 Mar 2021 22:44:41 GMT  
		Size: 2.7 MB (2711898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532760a713fdcc47b0750cf149032179ac109897d27a4a7387254e873782ef5a`  
		Last Modified: Fri, 26 Mar 2021 08:16:21 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da9e5d008656a72a376d31d7c1cf4c750c1d20fdc9725470e92748f3d902aeb`  
		Last Modified: Fri, 26 Mar 2021 08:16:38 GMT  
		Size: 65.8 MB (65820533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6121bcad7cba7d37518917de5d2e4bb729cc62708b2c847ea1df48ccb757483f`  
		Last Modified: Fri, 26 Mar 2021 08:16:21 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8253019ed837881d065d263f197f95708f7073be3629b60a1e367d07f44a853c`  
		Last Modified: Fri, 26 Mar 2021 08:16:21 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.0` - linux; 386

```console
$ docker pull vault@sha256:d36e98f13ac378cbfe847d7b589b64f2bada4f3ff90bdb8104989158840c981d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70570703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c26749e2878226c02eeba1c262288c19c01cc6d0684b9bab0b810254544e25`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 31 Mar 2021 17:43:00 GMT
ADD file:245767f958e2b5e6fad41d45d3361849e7c6b2255303e3c785f0f2c86019553a in / 
# Wed, 31 Mar 2021 17:43:00 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 07:38:55 GMT
ARG VAULT_VERSION=1.7.0
# Thu, 01 Apr 2021 07:38:56 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 01 Apr 2021 07:39:08 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 01 Apr 2021 07:39:09 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 01 Apr 2021 07:39:09 GMT
VOLUME [/vault/logs]
# Thu, 01 Apr 2021 07:39:10 GMT
VOLUME [/vault/file]
# Thu, 01 Apr 2021 07:39:10 GMT
EXPOSE 8200
# Thu, 01 Apr 2021 07:39:10 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 01 Apr 2021 07:39:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 07:39:11 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:b22e590ebf70a9a5901c380b07232ef3c07cb13440402934dfdffb8f8721a949`  
		Last Modified: Wed, 31 Mar 2021 17:44:05 GMT  
		Size: 2.8 MB (2818802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253b6fe11e847937b3bb907714a7ba2d39bfe7574e23a0b57a5492261959a9ca`  
		Last Modified: Thu, 01 Apr 2021 07:41:16 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ee58c78adb286aa02cf737f3ef4e76eaaa4501219874cc1b1edd91955ab2e8`  
		Last Modified: Thu, 01 Apr 2021 07:41:29 GMT  
		Size: 67.7 MB (67748638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc29516badcc93e7963cd6ac28767a2e3d4cc53aa6da2393e8e786479ef11c41`  
		Last Modified: Thu, 01 Apr 2021 07:41:16 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e4c24c4948e932b7b5761fe9af854282834a76e1e7d7f24267473911695c8e`  
		Last Modified: Thu, 01 Apr 2021 07:41:16 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.7.0-rc1`

```console
$ docker pull vault@sha256:cf10e5bcca279d9c75815f356ce3bd82e0a1698a5225f55b6e025be317fc96a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.7.0-rc1` - linux; amd64

```console
$ docker pull vault@sha256:279bedc3775cd2d4709344d09844d0a3b69cc6e75da0998b3e6d6f270d9af04f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72670615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f48d30eaee4d3e3433a177470c5b2a76bb57ea1d631902ed4eec8b148726ecf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:32 GMT
ADD file:6b081cabb4b256ee07587d249c4989b5b679375529542b81550a65b6f19f274e in / 
# Thu, 25 Mar 2021 22:19:32 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 05:03:39 GMT
ARG VAULT_VERSION=1.7.0-rc1
# Fri, 26 Mar 2021 05:03:41 GMT
# ARGS: VAULT_VERSION=1.7.0-rc1
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 26 Mar 2021 05:03:52 GMT
# ARGS: VAULT_VERSION=1.7.0-rc1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 26 Mar 2021 05:03:54 GMT
# ARGS: VAULT_VERSION=1.7.0-rc1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 26 Mar 2021 05:03:54 GMT
VOLUME [/vault/logs]
# Fri, 26 Mar 2021 05:03:54 GMT
VOLUME [/vault/file]
# Fri, 26 Mar 2021 05:03:55 GMT
EXPOSE 8200
# Fri, 26 Mar 2021 05:03:55 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 05:03:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 05:03:56 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:9aae54b2144e5b2b00c610f8805128f4f86822e1e52d3714c463744a431f0f4a`  
		Last Modified: Thu, 25 Mar 2021 22:20:18 GMT  
		Size: 2.8 MB (2811681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5e3fad7b25f9966da1ed73b673927d38f8639b801dd42c45cd14122dc8faaf`  
		Last Modified: Fri, 26 Mar 2021 05:05:38 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca21ae151d70a79ac49ede65588f342677fd343ab77bf83d659e0d30a59d4af`  
		Last Modified: Fri, 26 Mar 2021 05:05:48 GMT  
		Size: 69.9 MB (69855668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bea0c58469c7ca8e3f98ee85522201f1786a5b09352fd41027b88329c95506e`  
		Last Modified: Fri, 26 Mar 2021 05:05:38 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bedbd52da6757129511a9fc2fcc52c881cfb3e39e13616c02869f48f2821052`  
		Last Modified: Fri, 26 Mar 2021 05:05:38 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.0-rc1` - linux; arm variant v6

```console
$ docker pull vault@sha256:5f2104257d57fa6d0cfda5db2be3a8991d3e88009ef1e01f7029bdda9b1a6dc7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66701345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2babc4a35ac6d29f28f5f7de7af65a8c80442569cc94af14127b36f1d7c8cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 31 Mar 2021 17:18:49 GMT
ADD file:988879d74f643b89539e5a0b6d74221621f19f4f87f722614addadc46ce47200 in / 
# Wed, 31 Mar 2021 17:18:50 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 03:56:45 GMT
ARG VAULT_VERSION=1.7.0-rc1
# Thu, 01 Apr 2021 03:56:48 GMT
# ARGS: VAULT_VERSION=1.7.0-rc1
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 01 Apr 2021 03:57:02 GMT
# ARGS: VAULT_VERSION=1.7.0-rc1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 01 Apr 2021 03:57:10 GMT
# ARGS: VAULT_VERSION=1.7.0-rc1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 01 Apr 2021 03:57:11 GMT
VOLUME [/vault/logs]
# Thu, 01 Apr 2021 03:57:12 GMT
VOLUME [/vault/file]
# Thu, 01 Apr 2021 03:57:13 GMT
EXPOSE 8200
# Thu, 01 Apr 2021 03:57:14 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 01 Apr 2021 03:57:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 03:57:17 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:bb87125c6ee1ce30c6b33d2c96a9fbe46da4a290f7cb1dd73fd62d4e06503699`  
		Last Modified: Wed, 31 Mar 2021 17:19:55 GMT  
		Size: 2.6 MB (2622116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5ba71ddedad5e323c1fcf258f7f81d053635d689060ade0c9a8cac0ad970de`  
		Last Modified: Thu, 01 Apr 2021 04:00:08 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f55bab30045ce5ff32810fbd51e7bc6fc6564daa660437e4570d0abd26e10a`  
		Last Modified: Thu, 01 Apr 2021 04:00:24 GMT  
		Size: 64.1 MB (64075962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57c74fdb785c3b36ec26f0eb2a7a9012f348fdca66fdc15380298df89798d5e`  
		Last Modified: Thu, 01 Apr 2021 04:00:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5310f0f572a9d76a9f33bfdbc38e7262b3ea318ee0f5e9ff8d5e94929ac592c5`  
		Last Modified: Thu, 01 Apr 2021 04:00:07 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.0-rc1` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:3ecb0f69c8be43b1e09bc5121bbf470c180089ef5935d09e1112a2ced5713dd5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68500286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a67ba1b71e53fe2f51a5998d18f9fdab955afc5c221c9f32df56a03d7b9e325`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 25 Mar 2021 22:40:10 GMT
ADD file:8d7431f7e3e42b162a1626e7abf4ef7605146671dccc753d490de6b7fe429261 in / 
# Thu, 25 Mar 2021 22:40:23 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 08:14:14 GMT
ARG VAULT_VERSION=1.7.0-rc1
# Fri, 26 Mar 2021 08:14:17 GMT
# ARGS: VAULT_VERSION=1.7.0-rc1
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 26 Mar 2021 08:14:26 GMT
# ARGS: VAULT_VERSION=1.7.0-rc1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 26 Mar 2021 08:14:29 GMT
# ARGS: VAULT_VERSION=1.7.0-rc1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 26 Mar 2021 08:14:30 GMT
VOLUME [/vault/logs]
# Fri, 26 Mar 2021 08:14:31 GMT
VOLUME [/vault/file]
# Fri, 26 Mar 2021 08:14:32 GMT
EXPOSE 8200
# Fri, 26 Mar 2021 08:14:33 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 08:14:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 08:14:35 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:5ceb5101e3b0d54efb5f18318982508a04b181b4d5ae52b096dd35dea3a006cc`  
		Last Modified: Thu, 25 Mar 2021 22:44:41 GMT  
		Size: 2.7 MB (2711898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8187b8e1d03228a2752f63c7e39eba5d389ec3dd2c52cc7824506210e0dc4ad4`  
		Last Modified: Fri, 26 Mar 2021 08:17:09 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913d028ecb1aefdeb268ebcdc3a78e7e53a3a71461d068c75fcaf1b1f869426d`  
		Last Modified: Fri, 26 Mar 2021 08:17:25 GMT  
		Size: 65.8 MB (65785125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2dbe9b4063b6e8925a0a3d387f5c4bbf9a0c2c6942c2efd766c02358e876b5`  
		Last Modified: Fri, 26 Mar 2021 08:17:09 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9c0c8956878f4eeee1251253694692a6430b23c001e471423e9b19096ce925`  
		Last Modified: Fri, 26 Mar 2021 08:17:09 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.0-rc1` - linux; 386

```console
$ docker pull vault@sha256:81a15f9c8805e7842995786b8244bd1bc05ef58aa4d438f65b17418ac188a393
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70535844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab538c608b36b5fe509039ff7578630cd153d3e82aa30c56e32418ae83f9e9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 31 Mar 2021 17:43:00 GMT
ADD file:245767f958e2b5e6fad41d45d3361849e7c6b2255303e3c785f0f2c86019553a in / 
# Wed, 31 Mar 2021 17:43:00 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 07:39:34 GMT
ARG VAULT_VERSION=1.7.0-rc1
# Thu, 01 Apr 2021 07:39:35 GMT
# ARGS: VAULT_VERSION=1.7.0-rc1
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 01 Apr 2021 07:39:43 GMT
# ARGS: VAULT_VERSION=1.7.0-rc1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 01 Apr 2021 07:39:44 GMT
# ARGS: VAULT_VERSION=1.7.0-rc1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 01 Apr 2021 07:39:45 GMT
VOLUME [/vault/logs]
# Thu, 01 Apr 2021 07:39:45 GMT
VOLUME [/vault/file]
# Thu, 01 Apr 2021 07:39:45 GMT
EXPOSE 8200
# Thu, 01 Apr 2021 07:39:45 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 01 Apr 2021 07:39:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 07:39:46 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:b22e590ebf70a9a5901c380b07232ef3c07cb13440402934dfdffb8f8721a949`  
		Last Modified: Wed, 31 Mar 2021 17:44:05 GMT  
		Size: 2.8 MB (2818802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590eaae62029bf0be7673568af39ccfcaa2bd1e816d4112c516c841cd285fcd8`  
		Last Modified: Thu, 01 Apr 2021 07:42:00 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ff76ea2cca657b626fdbd0e292c098cd6cef2ecb25dd00f523dd452c4fdb10`  
		Last Modified: Thu, 01 Apr 2021 07:42:10 GMT  
		Size: 67.7 MB (67713778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a703ee07424215cd277d1d6d47504f925b4ab6a33a1a8c0d6db0db966ca8ac6d`  
		Last Modified: Thu, 01 Apr 2021 07:42:01 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5696e88fe90abfaad846797c87afbb0587c321b5d5cffa1aa1989e2152e84d0`  
		Last Modified: Thu, 01 Apr 2021 07:42:00 GMT  
		Size: 1.8 KB (1819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.7.0-rc2`

```console
$ docker pull vault@sha256:594ff577f18f48b9c12f0373a49de92b809b0e5216cdf91b7ff8f8b158ac47c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.7.0-rc2` - linux; amd64

```console
$ docker pull vault@sha256:b9006897b7a05a94a21424934c0702a8901cae52e0af754d34d1984fba0a6eaf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72667408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30252bbbc5eb3dd58af3b61067ac619c6820fece03d58d504be2d730f15bf35e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:32 GMT
ADD file:6b081cabb4b256ee07587d249c4989b5b679375529542b81550a65b6f19f274e in / 
# Thu, 25 Mar 2021 22:19:32 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 05:03:17 GMT
ARG VAULT_VERSION=1.7.0-rc2
# Fri, 26 Mar 2021 05:03:18 GMT
# ARGS: VAULT_VERSION=1.7.0-rc2
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 26 Mar 2021 05:03:29 GMT
# ARGS: VAULT_VERSION=1.7.0-rc2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 26 Mar 2021 05:03:31 GMT
# ARGS: VAULT_VERSION=1.7.0-rc2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 26 Mar 2021 05:03:31 GMT
VOLUME [/vault/logs]
# Fri, 26 Mar 2021 05:03:32 GMT
VOLUME [/vault/file]
# Fri, 26 Mar 2021 05:03:32 GMT
EXPOSE 8200
# Fri, 26 Mar 2021 05:03:33 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 05:03:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 05:03:33 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:9aae54b2144e5b2b00c610f8805128f4f86822e1e52d3714c463744a431f0f4a`  
		Last Modified: Thu, 25 Mar 2021 22:20:18 GMT  
		Size: 2.8 MB (2811681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe5e3f6abe5a49305d2ca8342d4f34c71ffccbeb1f742401d25eb87182074b65`  
		Last Modified: Fri, 26 Mar 2021 05:05:17 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a824ecbb1efa7047912500b38d4d7b1db6f8efadd38723d1cef3033b6aed75`  
		Last Modified: Fri, 26 Mar 2021 05:05:26 GMT  
		Size: 69.9 MB (69852460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1358f7df2c9c0eabf8f36b00315469ccf0025d8b2f6e635bf81dc8699b2721`  
		Last Modified: Fri, 26 Mar 2021 05:05:16 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c683d5c63b7dfb69908ada4e5f7ac73c5c2b785aec61a75155a96383f348e4`  
		Last Modified: Fri, 26 Mar 2021 05:05:16 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.0-rc2` - linux; arm variant v6

```console
$ docker pull vault@sha256:dd84b8beb1d5d365ac3fcf37eb36a5566281d0e7175325c7ad4ee705c293d2f3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66702771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8f445612edbef36da3cbe796108934b166458052bf4af3d37c956e5b2554434`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 31 Mar 2021 17:18:49 GMT
ADD file:988879d74f643b89539e5a0b6d74221621f19f4f87f722614addadc46ce47200 in / 
# Wed, 31 Mar 2021 17:18:50 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 03:56:08 GMT
ARG VAULT_VERSION=1.7.0-rc2
# Thu, 01 Apr 2021 03:56:11 GMT
# ARGS: VAULT_VERSION=1.7.0-rc2
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 01 Apr 2021 03:56:25 GMT
# ARGS: VAULT_VERSION=1.7.0-rc2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 01 Apr 2021 03:56:29 GMT
# ARGS: VAULT_VERSION=1.7.0-rc2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 01 Apr 2021 03:56:30 GMT
VOLUME [/vault/logs]
# Thu, 01 Apr 2021 03:56:31 GMT
VOLUME [/vault/file]
# Thu, 01 Apr 2021 03:56:32 GMT
EXPOSE 8200
# Thu, 01 Apr 2021 03:56:34 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 01 Apr 2021 03:56:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 03:56:36 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:bb87125c6ee1ce30c6b33d2c96a9fbe46da4a290f7cb1dd73fd62d4e06503699`  
		Last Modified: Wed, 31 Mar 2021 17:19:55 GMT  
		Size: 2.6 MB (2622116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f930327c92277e0956645dc2f700c5bcb45bd3df1dc7ca6fa710e4c954b7c8`  
		Last Modified: Thu, 01 Apr 2021 03:59:44 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f77723b385f3c34e858e442810c83498a93b11396e952d2c1e812034979eb1e`  
		Last Modified: Thu, 01 Apr 2021 04:00:00 GMT  
		Size: 64.1 MB (64077386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c39c772f5c36d7308d31a9835fbdc4cdc1d80225c48ebe3db1d3624f5155896`  
		Last Modified: Thu, 01 Apr 2021 03:59:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ab94140bc7099cf76311c54014077beb69bd9e1b64d28f231eb76f9c30a4f8`  
		Last Modified: Thu, 01 Apr 2021 03:59:44 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.0-rc2` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:2dd9c1fe2c8d4c61e60fdfc8f99662ff80ed0f463fa7e9585f5db5989f6feaaa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68525636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf9bf2c8461fa4ce891e6c0d771fa43e57d1b18882a7ce6130fc2eef41cab5c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 25 Mar 2021 22:40:10 GMT
ADD file:8d7431f7e3e42b162a1626e7abf4ef7605146671dccc753d490de6b7fe429261 in / 
# Thu, 25 Mar 2021 22:40:23 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 08:13:44 GMT
ARG VAULT_VERSION=1.7.0-rc2
# Fri, 26 Mar 2021 08:13:46 GMT
# ARGS: VAULT_VERSION=1.7.0-rc2
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 26 Mar 2021 08:13:56 GMT
# ARGS: VAULT_VERSION=1.7.0-rc2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 26 Mar 2021 08:13:59 GMT
# ARGS: VAULT_VERSION=1.7.0-rc2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 26 Mar 2021 08:14:00 GMT
VOLUME [/vault/logs]
# Fri, 26 Mar 2021 08:14:01 GMT
VOLUME [/vault/file]
# Fri, 26 Mar 2021 08:14:02 GMT
EXPOSE 8200
# Fri, 26 Mar 2021 08:14:03 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 08:14:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 08:14:05 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:5ceb5101e3b0d54efb5f18318982508a04b181b4d5ae52b096dd35dea3a006cc`  
		Last Modified: Thu, 25 Mar 2021 22:44:41 GMT  
		Size: 2.7 MB (2711898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47962abfdb64002920dc8fcf30ff78d74e29162dbd11fa9003eb42ac60c01461`  
		Last Modified: Fri, 26 Mar 2021 08:16:49 GMT  
		Size: 1.3 KB (1253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ae5c56a9776e27efd2361547ee2322fd9c05596ca0845adab426969178dbad`  
		Last Modified: Fri, 26 Mar 2021 08:17:03 GMT  
		Size: 65.8 MB (65810476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3d054dda0f8af57d9f3330c5d563744ace79e88eb2e0ad2a8cb3a7da88d283`  
		Last Modified: Fri, 26 Mar 2021 08:16:48 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767177bd639431f5c83efdfb16fdddf5ec1ec42260a8bd807d2f61a4983d8083`  
		Last Modified: Fri, 26 Mar 2021 08:16:48 GMT  
		Size: 1.8 KB (1823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.0-rc2` - linux; 386

```console
$ docker pull vault@sha256:437cd8adf9f2d358600e56ee007e6a573848784d3e82560bf1e1d034ef16cef6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70540267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37877c15431950f167453c2017945c1c86c7d5a6f2ace2db9c46700547d9a261`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 31 Mar 2021 17:43:00 GMT
ADD file:245767f958e2b5e6fad41d45d3361849e7c6b2255303e3c785f0f2c86019553a in / 
# Wed, 31 Mar 2021 17:43:00 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 07:39:17 GMT
ARG VAULT_VERSION=1.7.0-rc2
# Thu, 01 Apr 2021 07:39:18 GMT
# ARGS: VAULT_VERSION=1.7.0-rc2
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 01 Apr 2021 07:39:26 GMT
# ARGS: VAULT_VERSION=1.7.0-rc2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 01 Apr 2021 07:39:28 GMT
# ARGS: VAULT_VERSION=1.7.0-rc2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 01 Apr 2021 07:39:28 GMT
VOLUME [/vault/logs]
# Thu, 01 Apr 2021 07:39:28 GMT
VOLUME [/vault/file]
# Thu, 01 Apr 2021 07:39:28 GMT
EXPOSE 8200
# Thu, 01 Apr 2021 07:39:29 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 01 Apr 2021 07:39:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 07:39:29 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:b22e590ebf70a9a5901c380b07232ef3c07cb13440402934dfdffb8f8721a949`  
		Last Modified: Wed, 31 Mar 2021 17:44:05 GMT  
		Size: 2.8 MB (2818802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fbbf718bb3dabb9e2dc5fcce8ab3d30bd37469858b9983d02221ed8147d3398`  
		Last Modified: Thu, 01 Apr 2021 07:41:43 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23dffce4eec8032ff13f7e4455b865dfee11863441720e87194f375f9133ee7`  
		Last Modified: Thu, 01 Apr 2021 07:41:50 GMT  
		Size: 67.7 MB (67718199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4b82687d428025e6098a9059e35fe51f6cfcc879dba5e5c564bb0ca30eb99d`  
		Last Modified: Thu, 01 Apr 2021 07:41:43 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3780390f30b878bc253ddec7f011e7015de79d32a0db39398d89aee6db2e838`  
		Last Modified: Thu, 01 Apr 2021 07:41:40 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:latest`

```console
$ docker pull vault@sha256:6bf0c0e22aeee4fa42d22fc5a201c8901818edee9c4bf12151d40aea2318d966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:latest` - linux; amd64

```console
$ docker pull vault@sha256:d51a9c82d0d45857acabea988c7b2ec673855438a7718138569d199e80db2ad3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72706694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b359df68a663cd5d2528caab398298a176375aeaa13ae199d8b5f615c2a38bce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:32 GMT
ADD file:6b081cabb4b256ee07587d249c4989b5b679375529542b81550a65b6f19f274e in / 
# Thu, 25 Mar 2021 22:19:32 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 05:02:55 GMT
ARG VAULT_VERSION=1.7.0
# Fri, 26 Mar 2021 05:02:56 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 26 Mar 2021 05:03:07 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 26 Mar 2021 05:03:09 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 26 Mar 2021 05:03:09 GMT
VOLUME [/vault/logs]
# Fri, 26 Mar 2021 05:03:09 GMT
VOLUME [/vault/file]
# Fri, 26 Mar 2021 05:03:10 GMT
EXPOSE 8200
# Fri, 26 Mar 2021 05:03:10 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 05:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 05:03:11 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:9aae54b2144e5b2b00c610f8805128f4f86822e1e52d3714c463744a431f0f4a`  
		Last Modified: Thu, 25 Mar 2021 22:20:18 GMT  
		Size: 2.8 MB (2811681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1d6dd05beb921063752a0e4b43d2dc08582069eaaeb4e32ffa7a370ede3515`  
		Last Modified: Fri, 26 Mar 2021 05:04:52 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4de46febc3613de2118ec655d1fffbe87968c11570858a476e7dc4fd74c6ff4`  
		Last Modified: Fri, 26 Mar 2021 05:05:03 GMT  
		Size: 69.9 MB (69891751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc279c1e752b4ac2f1af5f2c54603b7bbf0e712414a1383d79b2c684b895ff4`  
		Last Modified: Fri, 26 Mar 2021 05:04:52 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e437bfd1f45e31c4442a7038debd89139a36421ac53cf2e579c1f773a45432ea`  
		Last Modified: Fri, 26 Mar 2021 05:04:52 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm variant v6

```console
$ docker pull vault@sha256:767919f77e45c4294de6e32d3b893b5036c762e51d560b76330932192e404d2f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66726620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8bde904bf2e29386a8fb240f6b1fb95f45ebf9d38f7fe2077517b1b514eb4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 31 Mar 2021 17:18:49 GMT
ADD file:988879d74f643b89539e5a0b6d74221621f19f4f87f722614addadc46ce47200 in / 
# Wed, 31 Mar 2021 17:18:50 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 03:55:36 GMT
ARG VAULT_VERSION=1.7.0
# Thu, 01 Apr 2021 03:55:38 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 01 Apr 2021 03:55:51 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 01 Apr 2021 03:55:54 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 01 Apr 2021 03:55:55 GMT
VOLUME [/vault/logs]
# Thu, 01 Apr 2021 03:55:56 GMT
VOLUME [/vault/file]
# Thu, 01 Apr 2021 03:55:57 GMT
EXPOSE 8200
# Thu, 01 Apr 2021 03:55:58 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 01 Apr 2021 03:55:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 03:55:59 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:bb87125c6ee1ce30c6b33d2c96a9fbe46da4a290f7cb1dd73fd62d4e06503699`  
		Last Modified: Wed, 31 Mar 2021 17:19:55 GMT  
		Size: 2.6 MB (2622116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad73fe886cac5dcb33a379031cfe005dda18d2607759d02d567e1a7f3f92dbdc`  
		Last Modified: Thu, 01 Apr 2021 03:59:20 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5ffa7fbdf0fe366fdafb6a2123b019f1febe00b3c8ce5ab4c74d95b9b1512d`  
		Last Modified: Thu, 01 Apr 2021 03:59:36 GMT  
		Size: 64.1 MB (64101238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f0d98dbcea4800176a5738fab3df0551316a16e5268fb5cc21cdf4b308ab390`  
		Last Modified: Thu, 01 Apr 2021 03:59:20 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9187438e2855de2e5af03cd0105dd1eb20593f9ad6f0b5f166eb83324d20402`  
		Last Modified: Thu, 01 Apr 2021 03:59:20 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:7bb03087f1872bba59add852953ac3e35a54d63798a5a42d53cc147d335150d4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68535695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7c6e9941803130f0b68e0749e872a59bd13cd4c57b0aae51a46a532a37a3d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 25 Mar 2021 22:40:10 GMT
ADD file:8d7431f7e3e42b162a1626e7abf4ef7605146671dccc753d490de6b7fe429261 in / 
# Thu, 25 Mar 2021 22:40:23 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 08:13:10 GMT
ARG VAULT_VERSION=1.7.0
# Fri, 26 Mar 2021 08:13:13 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 26 Mar 2021 08:13:22 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 26 Mar 2021 08:13:25 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 26 Mar 2021 08:13:27 GMT
VOLUME [/vault/logs]
# Fri, 26 Mar 2021 08:13:28 GMT
VOLUME [/vault/file]
# Fri, 26 Mar 2021 08:13:30 GMT
EXPOSE 8200
# Fri, 26 Mar 2021 08:13:31 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 08:13:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 08:13:33 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:5ceb5101e3b0d54efb5f18318982508a04b181b4d5ae52b096dd35dea3a006cc`  
		Last Modified: Thu, 25 Mar 2021 22:44:41 GMT  
		Size: 2.7 MB (2711898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532760a713fdcc47b0750cf149032179ac109897d27a4a7387254e873782ef5a`  
		Last Modified: Fri, 26 Mar 2021 08:16:21 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da9e5d008656a72a376d31d7c1cf4c750c1d20fdc9725470e92748f3d902aeb`  
		Last Modified: Fri, 26 Mar 2021 08:16:38 GMT  
		Size: 65.8 MB (65820533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6121bcad7cba7d37518917de5d2e4bb729cc62708b2c847ea1df48ccb757483f`  
		Last Modified: Fri, 26 Mar 2021 08:16:21 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8253019ed837881d065d263f197f95708f7073be3629b60a1e367d07f44a853c`  
		Last Modified: Fri, 26 Mar 2021 08:16:21 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; 386

```console
$ docker pull vault@sha256:d36e98f13ac378cbfe847d7b589b64f2bada4f3ff90bdb8104989158840c981d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70570703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c26749e2878226c02eeba1c262288c19c01cc6d0684b9bab0b810254544e25`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 31 Mar 2021 17:43:00 GMT
ADD file:245767f958e2b5e6fad41d45d3361849e7c6b2255303e3c785f0f2c86019553a in / 
# Wed, 31 Mar 2021 17:43:00 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 07:38:55 GMT
ARG VAULT_VERSION=1.7.0
# Thu, 01 Apr 2021 07:38:56 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 01 Apr 2021 07:39:08 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 01 Apr 2021 07:39:09 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 01 Apr 2021 07:39:09 GMT
VOLUME [/vault/logs]
# Thu, 01 Apr 2021 07:39:10 GMT
VOLUME [/vault/file]
# Thu, 01 Apr 2021 07:39:10 GMT
EXPOSE 8200
# Thu, 01 Apr 2021 07:39:10 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 01 Apr 2021 07:39:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 07:39:11 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:b22e590ebf70a9a5901c380b07232ef3c07cb13440402934dfdffb8f8721a949`  
		Last Modified: Wed, 31 Mar 2021 17:44:05 GMT  
		Size: 2.8 MB (2818802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253b6fe11e847937b3bb907714a7ba2d39bfe7574e23a0b57a5492261959a9ca`  
		Last Modified: Thu, 01 Apr 2021 07:41:16 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ee58c78adb286aa02cf737f3ef4e76eaaa4501219874cc1b1edd91955ab2e8`  
		Last Modified: Thu, 01 Apr 2021 07:41:29 GMT  
		Size: 67.7 MB (67748638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc29516badcc93e7963cd6ac28767a2e3d4cc53aa6da2393e8e786479ef11c41`  
		Last Modified: Thu, 01 Apr 2021 07:41:16 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e4c24c4948e932b7b5761fe9af854282834a76e1e7d7f24267473911695c8e`  
		Last Modified: Thu, 01 Apr 2021 07:41:16 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
