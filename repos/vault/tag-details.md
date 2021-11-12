<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `vault`

-	[`vault:1.5.9`](#vault159)
-	[`vault:1.6.7`](#vault167)
-	[`vault:1.7.6`](#vault176)
-	[`vault:1.8.5`](#vault185)
-	[`vault:1.9.0-rc1`](#vault190-rc1)
-	[`vault:latest`](#vaultlatest)

## `vault:1.5.9`

```console
$ docker pull vault@sha256:0a5c1b1b95419fb5b96fdfdda00ec689f0136060fbacf9ccc4753007b0de7c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.5.9` - linux; amd64

```console
$ docker pull vault@sha256:173212142be586a2558b2ff8cf701632c49dcd46cd522c69ff55265258d5bb74
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55101261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be2afbafea177c86d7b64ed1ff6882843a7e3d4c6630ee73fcf0af5d066f960`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 06:17:28 GMT
ARG VAULT_VERSION=1.5.9
# Wed, 01 Sep 2021 06:17:29 GMT
# ARGS: VAULT_VERSION=1.5.9
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 01 Sep 2021 06:17:38 GMT
# ARGS: VAULT_VERSION=1.5.9
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 01 Sep 2021 06:17:39 GMT
# ARGS: VAULT_VERSION=1.5.9
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 01 Sep 2021 06:17:39 GMT
VOLUME [/vault/logs]
# Wed, 01 Sep 2021 06:17:39 GMT
VOLUME [/vault/file]
# Wed, 01 Sep 2021 06:17:39 GMT
EXPOSE 8200
# Wed, 01 Sep 2021 06:17:40 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 01 Sep 2021 06:17:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 06:17:40 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6aff56fc2a66d6bdeb572825b481b1f259938d30c7986413d03f8ac63de529e`  
		Last Modified: Wed, 01 Sep 2021 06:17:56 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f81065ca5f94fdf96731590daeaf8625fe6d2ea5400126d45786af2ddc2389d`  
		Last Modified: Wed, 01 Sep 2021 06:18:04 GMT  
		Size: 52.3 MB (52283917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6ec1ddb9f38f190ec9c39107d0be9b4c858b4393f22a66ddba652cb4acb6088`  
		Last Modified: Wed, 01 Sep 2021 06:17:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9dcfeccf207be3e2d11842039700746f151e2b4ad65f253f23141b4517e4e6`  
		Last Modified: Wed, 01 Sep 2021 06:17:56 GMT  
		Size: 1.8 KB (1819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.5.9` - linux; arm variant v6

```console
$ docker pull vault@sha256:4cfcea87ecabed6cd3ccf97ee3a3d0e5703cba0270996945a32aa417e4e4ce75
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51678088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e96b2c38c3c2127ca6c4e2487bc683075a0be6a2dceeddcc2e6fe6e50e6d5ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 31 Aug 2021 22:30:33 GMT
ADD file:ed2b5e0fbd1e7ae37ab8f808c827d23c6841ce1edd7427552d5bf741d67ebcc0 in / 
# Tue, 31 Aug 2021 22:30:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 07:07:21 GMT
ARG VAULT_VERSION=1.5.9
# Wed, 01 Sep 2021 07:07:23 GMT
# ARGS: VAULT_VERSION=1.5.9
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 01 Sep 2021 07:07:44 GMT
# ARGS: VAULT_VERSION=1.5.9
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 01 Sep 2021 07:07:46 GMT
# ARGS: VAULT_VERSION=1.5.9
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 01 Sep 2021 07:07:46 GMT
VOLUME [/vault/logs]
# Wed, 01 Sep 2021 07:07:47 GMT
VOLUME [/vault/file]
# Wed, 01 Sep 2021 07:07:47 GMT
EXPOSE 8200
# Wed, 01 Sep 2021 07:07:48 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 01 Sep 2021 07:07:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 07:07:49 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:840d18d84f6afdc3231d126fdd3f84f23f0335b61cbfa9cb8808b888a4308919`  
		Last Modified: Tue, 31 Aug 2021 22:32:11 GMT  
		Size: 2.6 MB (2623761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2107291f0e709da064928dd447aaf165be6a0b712b651e5b0ff0b609cdc65033`  
		Last Modified: Wed, 01 Sep 2021 07:08:29 GMT  
		Size: 1.3 KB (1253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e401f7fbd59182ba7d9c0e35d40dd847288edfde0971c0c319361381898fa02b`  
		Last Modified: Wed, 01 Sep 2021 07:08:55 GMT  
		Size: 49.1 MB (49051063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede0959067494ad5fe9751f205afaff5a47b89e34d43f96406aca555547edd04`  
		Last Modified: Wed, 01 Sep 2021 07:08:29 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3f48e0dfa7371c6003bc8fb359287257b9f6f941a2932ff196dbf0c6765ab3`  
		Last Modified: Wed, 01 Sep 2021 07:08:29 GMT  
		Size: 1.8 KB (1823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.5.9` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:4a9663bc9ceae0033808db773126c1e61c7e928f046a2903f2ee13d21b2fb98f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (52008931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb15a824c14083ebf6cdc88790fafa97e4899a43345012dd919034994d951464`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:14:18 GMT
ARG VAULT_VERSION=1.5.9
# Fri, 12 Nov 2021 18:14:19 GMT
# ARGS: VAULT_VERSION=1.5.9
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 12 Nov 2021 18:14:25 GMT
# ARGS: VAULT_VERSION=1.5.9
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 12 Nov 2021 18:14:26 GMT
# ARGS: VAULT_VERSION=1.5.9
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 12 Nov 2021 18:14:27 GMT
VOLUME [/vault/logs]
# Fri, 12 Nov 2021 18:14:28 GMT
VOLUME [/vault/file]
# Fri, 12 Nov 2021 18:14:29 GMT
EXPOSE 8200
# Fri, 12 Nov 2021 18:14:31 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 12 Nov 2021 18:14:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 18:14:32 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57012237527e5f7c92402850533b0cde4a8f7b0663d8e324539ab6f3ac921c1`  
		Last Modified: Fri, 12 Nov 2021 18:16:01 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b2444d85c939227e9e761a421ce15b9eb0acf838415d822644313dc6be18de4`  
		Last Modified: Fri, 12 Nov 2021 18:16:14 GMT  
		Size: 49.3 MB (49286089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e166723a1eaaa030c31c6f58107014ddf10ea0202ed8bba9ffb35fc809608e`  
		Last Modified: Fri, 12 Nov 2021 18:16:02 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141483f166d53c65dd5c75dc28421cfe8363be7c98d31309762bd2e2ca3180af`  
		Last Modified: Fri, 12 Nov 2021 18:16:01 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.5.9` - linux; 386

```console
$ docker pull vault@sha256:8cd25a0a42e35180334d03bb685047b1c4f98d344b011d81478e11678864f250
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53203973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae69f056beef377729aec96728291b83ac6637931c45a58a98a120b69be423bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 17:33:25 GMT
ARG VAULT_VERSION=1.5.9
# Fri, 12 Nov 2021 17:33:26 GMT
# ARGS: VAULT_VERSION=1.5.9
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 12 Nov 2021 17:33:41 GMT
# ARGS: VAULT_VERSION=1.5.9
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 12 Nov 2021 17:33:43 GMT
# ARGS: VAULT_VERSION=1.5.9
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 12 Nov 2021 17:33:43 GMT
VOLUME [/vault/logs]
# Fri, 12 Nov 2021 17:33:44 GMT
VOLUME [/vault/file]
# Fri, 12 Nov 2021 17:33:44 GMT
EXPOSE 8200
# Fri, 12 Nov 2021 17:33:44 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 12 Nov 2021 17:33:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 17:33:45 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3781f653853df20ff8ed1a6c0d64c706a200be67b38bbced252bb208450e534`  
		Last Modified: Fri, 12 Nov 2021 17:36:02 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6faff79e956df13d75d5ce9413db500593747d59034d7766d23c1436539445bc`  
		Last Modified: Fri, 12 Nov 2021 17:36:16 GMT  
		Size: 50.4 MB (50371899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f663b340629ebab911be8c892a9eef2ffabb73ae109d6bb254c279b48bbd48`  
		Last Modified: Fri, 12 Nov 2021 17:36:03 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd9620d1d956b1fb5ade86d324c6f8d80a78ad53eab628eb76a8ecafec0c287`  
		Last Modified: Fri, 12 Nov 2021 17:36:02 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.6.7`

```console
$ docker pull vault@sha256:7c1fd8f9b54349d09b0a0df8f11cb5df1dd5a4cebcacd91a8017535cdcf40ac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.6.7` - linux; amd64

```console
$ docker pull vault@sha256:2d8756c6fca35d543fc46fd80053e0796f324df3d1bdca531067a9d3d4b3d498
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69116075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3dd301251a36c603611e32e0e3bb70efd1674f536f5f589fd61bc447e22ecd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 29 Sep 2021 23:21:28 GMT
ARG VAULT_VERSION=1.6.7
# Wed, 29 Sep 2021 23:21:29 GMT
# ARGS: VAULT_VERSION=1.6.7
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 29 Sep 2021 23:21:38 GMT
# ARGS: VAULT_VERSION=1.6.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 29 Sep 2021 23:21:39 GMT
# ARGS: VAULT_VERSION=1.6.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 29 Sep 2021 23:21:39 GMT
VOLUME [/vault/logs]
# Wed, 29 Sep 2021 23:21:39 GMT
VOLUME [/vault/file]
# Wed, 29 Sep 2021 23:21:40 GMT
EXPOSE 8200
# Wed, 29 Sep 2021 23:21:40 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 29 Sep 2021 23:21:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Sep 2021 23:21:40 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c809dc7df9d461752a3095819fbc3b8b6aa86cd941ac83b88d80bf6302c9e08e`  
		Last Modified: Wed, 29 Sep 2021 23:22:30 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc277f62c9d01426a993bc060c1f619915558d1184993d042f3a608ec805778`  
		Last Modified: Wed, 29 Sep 2021 23:22:39 GMT  
		Size: 66.3 MB (66298355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a556b4be5c34f8d1c1ea7cace44793c58e0533b33d7c4d8026aa1c18de8d83`  
		Last Modified: Wed, 29 Sep 2021 23:22:30 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b617bd7d7c1e1e40d6948ddbfbbb58c6d865bdaa4011a3d698acbed28095621`  
		Last Modified: Wed, 29 Sep 2021 23:22:30 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.6.7` - linux; arm variant v6

```console
$ docker pull vault@sha256:6ba577725b49717624ac4f44b226f3db46328b1b11b10c10a5f8b8c0420a41e4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63848880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85eaef2d95593c47b92f33af01aaf89af9c3b0fa530b7b5168318c44dd477b1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Thu, 30 Sep 2021 00:03:22 GMT
ARG VAULT_VERSION=1.6.7
# Thu, 30 Sep 2021 00:03:23 GMT
# ARGS: VAULT_VERSION=1.6.7
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 30 Sep 2021 00:03:43 GMT
# ARGS: VAULT_VERSION=1.6.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 30 Sep 2021 00:03:45 GMT
# ARGS: VAULT_VERSION=1.6.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 30 Sep 2021 00:03:46 GMT
VOLUME [/vault/logs]
# Thu, 30 Sep 2021 00:03:46 GMT
VOLUME [/vault/file]
# Thu, 30 Sep 2021 00:03:47 GMT
EXPOSE 8200
# Thu, 30 Sep 2021 00:03:47 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 30 Sep 2021 00:03:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Sep 2021 00:03:48 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841a4942881c001052d328110df75e1bcb3b7363bb805dc2d15fdc42b17607a7`  
		Last Modified: Thu, 30 Sep 2021 00:05:55 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2a97fa1cf3cee6494775f48aefbb72d289524609329fe55743edbaf4e9a9e9`  
		Last Modified: Thu, 30 Sep 2021 00:06:28 GMT  
		Size: 61.2 MB (61218158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4e30d4882c25b3f0f4b9c21bfd2489227f87460a1e1b3f8a8ee23e3a7b5631`  
		Last Modified: Thu, 30 Sep 2021 00:05:55 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906676deb9c98b785d3d7a69d2710a0628a143fcd0570bfeb6b941b603afc1b8`  
		Last Modified: Thu, 30 Sep 2021 00:05:55 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.6.7` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:8840b7d40be013e9cdab9d2d3fd7be773c393b7fc54d9397b31685079acb82f9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65140796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d1a77203679f54ddf4caeae615c322f45566c862584011b5cadf9a71440381`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:13:56 GMT
ARG VAULT_VERSION=1.6.7
# Fri, 12 Nov 2021 18:13:57 GMT
# ARGS: VAULT_VERSION=1.6.7
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 12 Nov 2021 18:14:06 GMT
# ARGS: VAULT_VERSION=1.6.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 12 Nov 2021 18:14:06 GMT
# ARGS: VAULT_VERSION=1.6.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 12 Nov 2021 18:14:07 GMT
VOLUME [/vault/logs]
# Fri, 12 Nov 2021 18:14:08 GMT
VOLUME [/vault/file]
# Fri, 12 Nov 2021 18:14:09 GMT
EXPOSE 8200
# Fri, 12 Nov 2021 18:14:11 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 12 Nov 2021 18:14:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 18:14:12 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3935f9db61a7b34b1919b3b80256bba49848c270324a2bd588211470b1dff16e`  
		Last Modified: Fri, 12 Nov 2021 18:15:45 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8dff2b8919eb42c25188a65f6e57a79078ba59cd83d05523de7da486c63a194`  
		Last Modified: Fri, 12 Nov 2021 18:15:54 GMT  
		Size: 62.4 MB (62419882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2280cedd357aedae89538f83f73221c1532723e29e2b1238ea78213a11f5797`  
		Last Modified: Fri, 12 Nov 2021 18:15:46 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c647a93f11944fbcdebdbd789ed54da45d27b7bfe5d5b610986a0e5800a9dc18`  
		Last Modified: Fri, 12 Nov 2021 18:15:45 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.6.7` - linux; 386

```console
$ docker pull vault@sha256:967f16406d097d62460fbc18b68cb72d2a722ae1a772b97ee851af7970662ba7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67164972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f64270dc212452748714f3e270f2e08ed6fdaef36b141351bc4a050fa213460`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:42 GMT
ADD file:403428c2903dd9dea10d069185873cb2c2c3149c553797807c69f22aa3d12fe3 in / 
# Fri, 12 Nov 2021 16:38:42 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 17:32:53 GMT
ARG VAULT_VERSION=1.6.7
# Fri, 12 Nov 2021 17:32:54 GMT
# ARGS: VAULT_VERSION=1.6.7
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 12 Nov 2021 17:33:11 GMT
# ARGS: VAULT_VERSION=1.6.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 12 Nov 2021 17:33:13 GMT
# ARGS: VAULT_VERSION=1.6.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 12 Nov 2021 17:33:13 GMT
VOLUME [/vault/logs]
# Fri, 12 Nov 2021 17:33:14 GMT
VOLUME [/vault/file]
# Fri, 12 Nov 2021 17:33:14 GMT
EXPOSE 8200
# Fri, 12 Nov 2021 17:33:14 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 12 Nov 2021 17:33:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 17:33:15 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:5420e0d28c84ecb16748cb90cc6acf8e2a81dab10cb1f674f3eee8533e53c62a`  
		Last Modified: Fri, 12 Nov 2021 16:39:36 GMT  
		Size: 2.8 MB (2830948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5687af1e758a81cb56968feabeb4df42f60ba6f22267571b48e04f30c8b669`  
		Last Modified: Fri, 12 Nov 2021 17:35:38 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e6d591c10a0632df92caf56171ceda32aea7eaf3cf2605bbb78b4958e868552`  
		Last Modified: Fri, 12 Nov 2021 17:35:53 GMT  
		Size: 64.3 MB (64330751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:926a723f3932c401b81e4a0896005dd52ff449a3fcd29f2ca4b10d842f48d9c2`  
		Last Modified: Fri, 12 Nov 2021 17:35:38 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280f02b1aec09a9f6bba587e771bafcad59c851053c9f0fa1963b5d0413dc981`  
		Last Modified: Fri, 12 Nov 2021 17:35:38 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.7.6`

```console
$ docker pull vault@sha256:61245b9779bbd5b049dd0d650af4163a7655bda96179784a087a62e7392e1d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.7.6` - linux; amd64

```console
$ docker pull vault@sha256:6aba3b680a0a0351543a689e8366563967e6e432479ff043bdae2f927149961b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74061313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10998961125833ffa1a3dfc834b3a1402cbd612065a2edb93abf00758802bc99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 05 Nov 2021 01:42:47 GMT
ARG VAULT_VERSION=1.7.6
# Fri, 05 Nov 2021 01:42:48 GMT
# ARGS: VAULT_VERSION=1.7.6
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 05 Nov 2021 01:42:56 GMT
# ARGS: VAULT_VERSION=1.7.6
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 05 Nov 2021 01:42:57 GMT
# ARGS: VAULT_VERSION=1.7.6
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 05 Nov 2021 01:42:57 GMT
VOLUME [/vault/logs]
# Fri, 05 Nov 2021 01:42:57 GMT
VOLUME [/vault/file]
# Fri, 05 Nov 2021 01:42:57 GMT
EXPOSE 8200
# Fri, 05 Nov 2021 01:42:58 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 05 Nov 2021 01:42:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Nov 2021 01:42:58 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fbdf289d37d2ea83a3d933a80381142dba92d85aab37c2a56ececc9f9d825b9`  
		Last Modified: Fri, 05 Nov 2021 01:43:31 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fa0bc24758d0b4565083a402b2dddd59712b41ec0acbe1b17dea435daeb4636`  
		Last Modified: Fri, 05 Nov 2021 01:43:40 GMT  
		Size: 71.2 MB (71243587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ec8f9d96880c1debf9146ce4545edaaf776ed1f662898506a9e0dd1430ccee`  
		Last Modified: Fri, 05 Nov 2021 01:43:31 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:634dd0246394986fdce60da19774269f214cda6a7397fe125ff2a05e1c157da1`  
		Last Modified: Fri, 05 Nov 2021 01:43:31 GMT  
		Size: 1.8 KB (1823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.6` - linux; arm variant v6

```console
$ docker pull vault@sha256:1a9d099a2d0a0af9c6ab84d61d2d0ada6e5ccab3c1b505b46c60fbae90be5b3c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67880522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:367beca8fb2f4cd22e2d031b8d764b188cc8acb4594c0be3b9d0b15dcc3daec9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Fri, 05 Nov 2021 01:45:04 GMT
ARG VAULT_VERSION=1.7.6
# Fri, 05 Nov 2021 01:45:05 GMT
# ARGS: VAULT_VERSION=1.7.6
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 05 Nov 2021 01:45:25 GMT
# ARGS: VAULT_VERSION=1.7.6
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 05 Nov 2021 01:45:27 GMT
# ARGS: VAULT_VERSION=1.7.6
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 05 Nov 2021 01:45:28 GMT
VOLUME [/vault/logs]
# Fri, 05 Nov 2021 01:45:28 GMT
VOLUME [/vault/file]
# Fri, 05 Nov 2021 01:45:28 GMT
EXPOSE 8200
# Fri, 05 Nov 2021 01:45:29 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 05 Nov 2021 01:45:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Nov 2021 01:45:30 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0391a164b39439bf18db91ed84475e1b02555edadf3d1ceb0d193d603b6702db`  
		Last Modified: Fri, 05 Nov 2021 01:47:03 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7663dc98be92d43ec1650ca3dbdd1701fd11b7fd3dc3420b028fa0ce40f202e7`  
		Last Modified: Fri, 05 Nov 2021 01:47:38 GMT  
		Size: 65.2 MB (65249799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f531ba7ca13116cf51d57342a3f158dfef60a7f8e878107c413c89221da6d0e5`  
		Last Modified: Fri, 05 Nov 2021 01:47:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81849cad18910a7a201ee5ffbf2deba89ea01dd65675e7354d0886cd641f2f00`  
		Last Modified: Fri, 05 Nov 2021 01:47:03 GMT  
		Size: 1.8 KB (1819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.6` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:25b183e58a318000721fcfb4495c60c6b50879e10db43c7312e3e0e8a3c3237d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69837583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7266ae67366d664cd1f6eeec87fede386436ffeecb0c1c6a22c5f4670e48b966`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:13:34 GMT
ARG VAULT_VERSION=1.7.6
# Fri, 12 Nov 2021 18:13:35 GMT
# ARGS: VAULT_VERSION=1.7.6
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 12 Nov 2021 18:13:42 GMT
# ARGS: VAULT_VERSION=1.7.6
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 12 Nov 2021 18:13:43 GMT
# ARGS: VAULT_VERSION=1.7.6
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 12 Nov 2021 18:13:44 GMT
VOLUME [/vault/logs]
# Fri, 12 Nov 2021 18:13:45 GMT
VOLUME [/vault/file]
# Fri, 12 Nov 2021 18:13:46 GMT
EXPOSE 8200
# Fri, 12 Nov 2021 18:13:48 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 12 Nov 2021 18:13:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 18:13:49 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7405f8e7d46cc992c34be460828210708126d918a6b1d5eb20d6936a8239a5`  
		Last Modified: Fri, 12 Nov 2021 18:15:29 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:384bbf9ef2793c45a718dafcbc7d09ec7875c3b5a020ce2b486d152f96fe0e0f`  
		Last Modified: Fri, 12 Nov 2021 18:15:38 GMT  
		Size: 67.1 MB (67116670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021944269df473101306f97203d0c0577e8af85a24648732e977aa0ba5c59d5a`  
		Last Modified: Fri, 12 Nov 2021 18:15:29 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222844418e5da44577a44bf71ee9ad13370713ab99fe1d69c991bffe1a9301aa`  
		Last Modified: Fri, 12 Nov 2021 18:15:29 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.6` - linux; 386

```console
$ docker pull vault@sha256:9f1dfb6db4f6b4a7de0cfc4da352907266cca689c754e7e2fc401a6d7bcb7344
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71909917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29fd32bf55104a01b6dbe667b13cfe7cf15d20564c8107fa3d9b78363d4f9565`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:42 GMT
ADD file:403428c2903dd9dea10d069185873cb2c2c3149c553797807c69f22aa3d12fe3 in / 
# Fri, 12 Nov 2021 16:38:42 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 17:32:26 GMT
ARG VAULT_VERSION=1.7.6
# Fri, 12 Nov 2021 17:32:27 GMT
# ARGS: VAULT_VERSION=1.7.6
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 12 Nov 2021 17:32:42 GMT
# ARGS: VAULT_VERSION=1.7.6
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 12 Nov 2021 17:32:44 GMT
# ARGS: VAULT_VERSION=1.7.6
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 12 Nov 2021 17:32:45 GMT
VOLUME [/vault/logs]
# Fri, 12 Nov 2021 17:32:45 GMT
VOLUME [/vault/file]
# Fri, 12 Nov 2021 17:32:45 GMT
EXPOSE 8200
# Fri, 12 Nov 2021 17:32:46 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 12 Nov 2021 17:32:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 17:32:46 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:5420e0d28c84ecb16748cb90cc6acf8e2a81dab10cb1f674f3eee8533e53c62a`  
		Last Modified: Fri, 12 Nov 2021 16:39:36 GMT  
		Size: 2.8 MB (2830948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbd846890b62c7ccbe8c19ed015550c61d7eea572dcfd68bb578b97399dee96`  
		Last Modified: Fri, 12 Nov 2021 17:35:12 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08af0c79b16f768276bedcd26e449c43b5ee223f8fdbf0292d632e227e413ece`  
		Last Modified: Fri, 12 Nov 2021 17:35:29 GMT  
		Size: 69.1 MB (69075695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4abf0d119684625a6b92965eb35381abc3f59aa0def74bcc0637332bd906ddab`  
		Last Modified: Fri, 12 Nov 2021 17:35:12 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cebf831e5f8973371418e4177cfab97dde534c317f3d6c286c0085eb67e7ef0`  
		Last Modified: Fri, 12 Nov 2021 17:35:12 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.8.5`

```console
$ docker pull vault@sha256:73244cde52f78b2531674f81c3db1433d1b7f00eb4a9c6bda817468a9cb9c1fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.8.5` - linux; amd64

```console
$ docker pull vault@sha256:d08d5ff28b547c493c1ac500848382024a9cc706f455cb714455dcbc39c6ff37
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70531897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2fe93ed4b6578d187283a0fac58632e5ec9dbf3802519e08fa6495dcee7002c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 05 Nov 2021 01:42:20 GMT
ARG VAULT_VERSION=1.8.5
# Fri, 05 Nov 2021 01:42:20 GMT
# ARGS: VAULT_VERSION=1.8.5
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 05 Nov 2021 01:42:39 GMT
# ARGS: VAULT_VERSION=1.8.5
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 05 Nov 2021 01:42:40 GMT
# ARGS: VAULT_VERSION=1.8.5
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 05 Nov 2021 01:42:40 GMT
VOLUME [/vault/logs]
# Fri, 05 Nov 2021 01:42:40 GMT
VOLUME [/vault/file]
# Fri, 05 Nov 2021 01:42:41 GMT
EXPOSE 8200
# Fri, 05 Nov 2021 01:42:41 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 05 Nov 2021 01:42:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Nov 2021 01:42:41 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0ce591d1d92675fc7cddd0e3d1e86dce1426a27f2f54c4f75264ab494c3da7`  
		Last Modified: Fri, 05 Nov 2021 01:43:12 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c48e3a03f5cdf8787c7bc120b27267522ee232598cf3777dbc46c47f2dd507`  
		Last Modified: Fri, 05 Nov 2021 01:43:21 GMT  
		Size: 67.7 MB (67714171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b648a93e52cb9adaa31451ad455d96f714aea64ce1f52eeb396352790cd024`  
		Last Modified: Fri, 05 Nov 2021 01:43:12 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa94d3724a7fcf5a134a37bf1cd97827a8d3f34d23ec752a81ea3e99b84c1106`  
		Last Modified: Fri, 05 Nov 2021 01:43:12 GMT  
		Size: 1.8 KB (1824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.8.5` - linux; arm variant v6

```console
$ docker pull vault@sha256:1dee343a1d8398d3932e5534d863a53f450ec5d75db5564fcdca4a98a355cec3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64901276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9f6f18123e77e6c4627656016420f73bcf9e52169e6900a7ab30d8fe2ee6616`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Fri, 05 Nov 2021 01:44:21 GMT
ARG VAULT_VERSION=1.8.5
# Fri, 05 Nov 2021 01:44:22 GMT
# ARGS: VAULT_VERSION=1.8.5
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 05 Nov 2021 01:44:47 GMT
# ARGS: VAULT_VERSION=1.8.5
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 05 Nov 2021 01:44:49 GMT
# ARGS: VAULT_VERSION=1.8.5
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 05 Nov 2021 01:44:49 GMT
VOLUME [/vault/logs]
# Fri, 05 Nov 2021 01:44:50 GMT
VOLUME [/vault/file]
# Fri, 05 Nov 2021 01:44:50 GMT
EXPOSE 8200
# Fri, 05 Nov 2021 01:44:50 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 05 Nov 2021 01:44:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Nov 2021 01:44:51 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885b822523b48f580685a4b7bfc6635cc702e7d51b5bb9837ac745533c186173`  
		Last Modified: Fri, 05 Nov 2021 01:46:19 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55710bbd741cf26c2aeaba8337b3520476e684438e183da9448b773fcf4b7344`  
		Last Modified: Fri, 05 Nov 2021 01:46:52 GMT  
		Size: 62.3 MB (62270548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2368999dddd5fa4fb572762adcb99f57bf8b79fab460d2a9210507f1aeb191ac`  
		Last Modified: Fri, 05 Nov 2021 01:46:20 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d7c59ebb88433224c433a44bd3a04456b0a0d96560863cdcdc6b667875b7ec`  
		Last Modified: Fri, 05 Nov 2021 01:46:19 GMT  
		Size: 1.8 KB (1825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.8.5` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:0e95fc43a67e977e066a13a001e4a2c0e995ff2657de330a28cca0164d372cac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66854957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:481906745721411dcb4230595a83ee7f9bfdf0823529c5a39034c4d7cf33ac5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:13:11 GMT
ARG VAULT_VERSION=1.8.5
# Fri, 12 Nov 2021 18:13:12 GMT
# ARGS: VAULT_VERSION=1.8.5
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 12 Nov 2021 18:13:21 GMT
# ARGS: VAULT_VERSION=1.8.5
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 12 Nov 2021 18:13:21 GMT
# ARGS: VAULT_VERSION=1.8.5
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 12 Nov 2021 18:13:22 GMT
VOLUME [/vault/logs]
# Fri, 12 Nov 2021 18:13:23 GMT
VOLUME [/vault/file]
# Fri, 12 Nov 2021 18:13:24 GMT
EXPOSE 8200
# Fri, 12 Nov 2021 18:13:26 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 12 Nov 2021 18:13:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 18:13:27 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4adb27be142b8b5fe9dd195df174830ecb7a44c86f0568a74a6cf0fab8c9f3`  
		Last Modified: Fri, 12 Nov 2021 18:15:10 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d822e2f0230aba3d2cefd2dc4d3be8f3652c7fe368e4a43aba7f97cc6f10b6`  
		Last Modified: Fri, 12 Nov 2021 18:15:18 GMT  
		Size: 64.1 MB (64134043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1eaf15d533bc354dc7bf18782417d0d931a97b2909017217700b9b06956cd5c`  
		Last Modified: Fri, 12 Nov 2021 18:15:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c61c78635277cd50980496d80918f364be79e0b6309177291e5a642c35ad3b`  
		Last Modified: Fri, 12 Nov 2021 18:15:10 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.8.5` - linux; 386

```console
$ docker pull vault@sha256:f5d4dce800fd5d4cd54fc88d07ce521dcf074ccb43f48dff68b170447d728703
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68279456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe955277ce65f87e247a2b72fb52963c7a139b0d0abb959aad68dce45667239`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:42 GMT
ADD file:403428c2903dd9dea10d069185873cb2c2c3149c553797807c69f22aa3d12fe3 in / 
# Fri, 12 Nov 2021 16:38:42 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 17:31:55 GMT
ARG VAULT_VERSION=1.8.5
# Fri, 12 Nov 2021 17:31:57 GMT
# ARGS: VAULT_VERSION=1.8.5
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 12 Nov 2021 17:32:14 GMT
# ARGS: VAULT_VERSION=1.8.5
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 12 Nov 2021 17:32:16 GMT
# ARGS: VAULT_VERSION=1.8.5
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 12 Nov 2021 17:32:16 GMT
VOLUME [/vault/logs]
# Fri, 12 Nov 2021 17:32:16 GMT
VOLUME [/vault/file]
# Fri, 12 Nov 2021 17:32:17 GMT
EXPOSE 8200
# Fri, 12 Nov 2021 17:32:17 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 12 Nov 2021 17:32:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 17:32:18 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:5420e0d28c84ecb16748cb90cc6acf8e2a81dab10cb1f674f3eee8533e53c62a`  
		Last Modified: Fri, 12 Nov 2021 16:39:36 GMT  
		Size: 2.8 MB (2830948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf4c0c927d2593dfbd7926d38039f4c03d2102ba0776b1ad493dcc66db4167f`  
		Last Modified: Fri, 12 Nov 2021 17:34:43 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403f2827665674e108c599a90050421a8b9a40e3ba0f62680b69af2524cc00e9`  
		Last Modified: Fri, 12 Nov 2021 17:34:59 GMT  
		Size: 65.4 MB (65445233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a95c32fa455bb256f024f90c52ded7e07c49ca98bd27aee9b2b7f34cffb343a`  
		Last Modified: Fri, 12 Nov 2021 17:34:43 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5102adb48bdd2d3c560f0c47ae8df04a5684cd951650d89351071cf3eb5db290`  
		Last Modified: Fri, 12 Nov 2021 17:34:43 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.9.0-rc1`

```console
$ docker pull vault@sha256:b718a06dcf4e9d3e9442157564ddbfda731e5984698e32c008f5b8c032475070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.9.0-rc1` - linux; amd64

```console
$ docker pull vault@sha256:263ce89ad36d75ebd7cadb1625c147666145595c13ef303b7e1303c76a4915b3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71425358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c9967c249e528e92cceca5e39e22567c86988dbbbba8e8fe46e8b9c9a46a85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 05 Nov 2021 21:19:59 GMT
ARG VAULT_VERSION=1.9.0-rc1
# Fri, 05 Nov 2021 21:20:00 GMT
# ARGS: VAULT_VERSION=1.9.0-rc1
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 05 Nov 2021 21:20:15 GMT
# ARGS: VAULT_VERSION=1.9.0-rc1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 05 Nov 2021 21:20:16 GMT
# ARGS: VAULT_VERSION=1.9.0-rc1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 05 Nov 2021 21:20:16 GMT
VOLUME [/vault/logs]
# Fri, 05 Nov 2021 21:20:17 GMT
VOLUME [/vault/file]
# Fri, 05 Nov 2021 21:20:17 GMT
EXPOSE 8200
# Fri, 05 Nov 2021 21:20:17 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 05 Nov 2021 21:20:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Nov 2021 21:20:17 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0270d23de3d9f793feaea99eab57bbdbc8b9ffa50c0a24ebe5a247eb695125e`  
		Last Modified: Fri, 05 Nov 2021 21:20:39 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96dffc58d7edbbec9c30d975640881e5649b15d4af64b5636b3f82bd5b3aa32`  
		Last Modified: Fri, 05 Nov 2021 21:20:48 GMT  
		Size: 68.6 MB (68607631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49fa04d4d8b8d0a11ec614c09d354001a3d57d4ea36587d2fe642771c650bd64`  
		Last Modified: Fri, 05 Nov 2021 21:20:39 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce177b8266da2aa3cb84ab305ee81710cbea4f94371eb3fde286dd5c9823ed41`  
		Last Modified: Fri, 05 Nov 2021 21:20:39 GMT  
		Size: 1.8 KB (1826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.9.0-rc1` - linux; arm variant v6

```console
$ docker pull vault@sha256:5a269e84fc5a884408428e996e9b1a3f1d1441cf0ddce378431a454b5781f076
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65062967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85057c95c4a772990fb53f36be2c907f9f34bb61d060210249f9a867c902005`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Fri, 05 Nov 2021 21:49:48 GMT
ARG VAULT_VERSION=1.9.0-rc1
# Fri, 05 Nov 2021 21:49:50 GMT
# ARGS: VAULT_VERSION=1.9.0-rc1
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 05 Nov 2021 21:50:09 GMT
# ARGS: VAULT_VERSION=1.9.0-rc1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 05 Nov 2021 21:50:11 GMT
# ARGS: VAULT_VERSION=1.9.0-rc1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 05 Nov 2021 21:50:11 GMT
VOLUME [/vault/logs]
# Fri, 05 Nov 2021 21:50:12 GMT
VOLUME [/vault/file]
# Fri, 05 Nov 2021 21:50:12 GMT
EXPOSE 8200
# Fri, 05 Nov 2021 21:50:13 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 05 Nov 2021 21:50:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Nov 2021 21:50:14 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea7089403ef8dbc17c903c56c4434a9e4ccb07d9ad25c5b49c9d4512d668226`  
		Last Modified: Fri, 05 Nov 2021 21:51:26 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e075293d7db88ac49f1dfb15dbc755d5b8a7c108a2a751cb221841c5ca9e563`  
		Last Modified: Fri, 05 Nov 2021 21:52:00 GMT  
		Size: 62.4 MB (62432241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c9725e4969bfae4158aa81b749832d789a3120d6f3dd027ef41f890310be18`  
		Last Modified: Fri, 05 Nov 2021 21:51:26 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ffa131fa9d319799785a6dcaf9d1e3b36a545c8cd5dfe4d38afdde946c8235`  
		Last Modified: Fri, 05 Nov 2021 21:51:26 GMT  
		Size: 1.8 KB (1825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.9.0-rc1` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:30be4d4d6122706cf93a4e930a31176bb4691f58f46276fbfd743fdcf408dd70
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66733426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95482d93a659a046cd7c7763a27abc117cad47d28cbf78abde252796af0d7f4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:12:49 GMT
ARG VAULT_VERSION=1.9.0-rc1
# Fri, 12 Nov 2021 18:12:49 GMT
# ARGS: VAULT_VERSION=1.9.0-rc1
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 12 Nov 2021 18:12:58 GMT
# ARGS: VAULT_VERSION=1.9.0-rc1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 12 Nov 2021 18:12:59 GMT
# ARGS: VAULT_VERSION=1.9.0-rc1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 12 Nov 2021 18:13:00 GMT
VOLUME [/vault/logs]
# Fri, 12 Nov 2021 18:13:01 GMT
VOLUME [/vault/file]
# Fri, 12 Nov 2021 18:13:02 GMT
EXPOSE 8200
# Fri, 12 Nov 2021 18:13:04 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 12 Nov 2021 18:13:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 18:13:05 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00abc20a3d8d765a43117b6fb1bce5f5e76dcaeaf47974d1a607625e8b5a1476`  
		Last Modified: Fri, 12 Nov 2021 18:14:53 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:069e6a3f5fcf2756827286bf30b48fae1e5286ff0226269f2373139d18093c5c`  
		Last Modified: Fri, 12 Nov 2021 18:15:02 GMT  
		Size: 64.0 MB (64012515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03b35b7ad903521891280408d5d81b108a81b48a10810a75c048dfec67cc86c`  
		Last Modified: Fri, 12 Nov 2021 18:14:53 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac4690c95343eb7cc554163630f7e89a059ef3220e90a8cee2588c649779881`  
		Last Modified: Fri, 12 Nov 2021 18:14:53 GMT  
		Size: 1.8 KB (1819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.9.0-rc1` - linux; 386

```console
$ docker pull vault@sha256:192ce3ec409f0b34db76e1f5fa4de9c9f13bd6e2ea90579897ca75ecd1f47de1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67941174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8915fb6b53ca4dd7b39190a3e205594179ff17624d608a3c0bb7cd66e9dfdbc0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:42 GMT
ADD file:403428c2903dd9dea10d069185873cb2c2c3149c553797807c69f22aa3d12fe3 in / 
# Fri, 12 Nov 2021 16:38:42 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 17:31:17 GMT
ARG VAULT_VERSION=1.9.0-rc1
# Fri, 12 Nov 2021 17:31:19 GMT
# ARGS: VAULT_VERSION=1.9.0-rc1
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 12 Nov 2021 17:31:39 GMT
# ARGS: VAULT_VERSION=1.9.0-rc1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 12 Nov 2021 17:31:41 GMT
# ARGS: VAULT_VERSION=1.9.0-rc1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 12 Nov 2021 17:31:41 GMT
VOLUME [/vault/logs]
# Fri, 12 Nov 2021 17:31:42 GMT
VOLUME [/vault/file]
# Fri, 12 Nov 2021 17:31:42 GMT
EXPOSE 8200
# Fri, 12 Nov 2021 17:31:43 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 12 Nov 2021 17:31:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 17:31:44 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:5420e0d28c84ecb16748cb90cc6acf8e2a81dab10cb1f674f3eee8533e53c62a`  
		Last Modified: Fri, 12 Nov 2021 16:39:36 GMT  
		Size: 2.8 MB (2830948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f82288ea3a51ce7c4d88784ed062726f719f10dd2c9b1aeec85264b690f467`  
		Last Modified: Fri, 12 Nov 2021 17:34:16 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d0436400299f6c4e2798a6eaba7e8c73b756bc0947cbb6262d10edf73df549`  
		Last Modified: Fri, 12 Nov 2021 17:34:34 GMT  
		Size: 65.1 MB (65106947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a335fd18ada97239718149ee704526f3ce70ddaaa01e1a31958a75e3e1e257`  
		Last Modified: Fri, 12 Nov 2021 17:34:16 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b91b7abdb39d21aacb34c8840419a9a46fa3ad2d79e34e9d7b4444a2d41e60`  
		Last Modified: Fri, 12 Nov 2021 17:34:16 GMT  
		Size: 1.8 KB (1823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:latest`

```console
$ docker pull vault@sha256:73244cde52f78b2531674f81c3db1433d1b7f00eb4a9c6bda817468a9cb9c1fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:latest` - linux; amd64

```console
$ docker pull vault@sha256:d08d5ff28b547c493c1ac500848382024a9cc706f455cb714455dcbc39c6ff37
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70531897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2fe93ed4b6578d187283a0fac58632e5ec9dbf3802519e08fa6495dcee7002c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 05 Nov 2021 01:42:20 GMT
ARG VAULT_VERSION=1.8.5
# Fri, 05 Nov 2021 01:42:20 GMT
# ARGS: VAULT_VERSION=1.8.5
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 05 Nov 2021 01:42:39 GMT
# ARGS: VAULT_VERSION=1.8.5
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 05 Nov 2021 01:42:40 GMT
# ARGS: VAULT_VERSION=1.8.5
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 05 Nov 2021 01:42:40 GMT
VOLUME [/vault/logs]
# Fri, 05 Nov 2021 01:42:40 GMT
VOLUME [/vault/file]
# Fri, 05 Nov 2021 01:42:41 GMT
EXPOSE 8200
# Fri, 05 Nov 2021 01:42:41 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 05 Nov 2021 01:42:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Nov 2021 01:42:41 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0ce591d1d92675fc7cddd0e3d1e86dce1426a27f2f54c4f75264ab494c3da7`  
		Last Modified: Fri, 05 Nov 2021 01:43:12 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c48e3a03f5cdf8787c7bc120b27267522ee232598cf3777dbc46c47f2dd507`  
		Last Modified: Fri, 05 Nov 2021 01:43:21 GMT  
		Size: 67.7 MB (67714171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b648a93e52cb9adaa31451ad455d96f714aea64ce1f52eeb396352790cd024`  
		Last Modified: Fri, 05 Nov 2021 01:43:12 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa94d3724a7fcf5a134a37bf1cd97827a8d3f34d23ec752a81ea3e99b84c1106`  
		Last Modified: Fri, 05 Nov 2021 01:43:12 GMT  
		Size: 1.8 KB (1824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm variant v6

```console
$ docker pull vault@sha256:1dee343a1d8398d3932e5534d863a53f450ec5d75db5564fcdca4a98a355cec3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64901276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9f6f18123e77e6c4627656016420f73bcf9e52169e6900a7ab30d8fe2ee6616`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Fri, 05 Nov 2021 01:44:21 GMT
ARG VAULT_VERSION=1.8.5
# Fri, 05 Nov 2021 01:44:22 GMT
# ARGS: VAULT_VERSION=1.8.5
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 05 Nov 2021 01:44:47 GMT
# ARGS: VAULT_VERSION=1.8.5
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 05 Nov 2021 01:44:49 GMT
# ARGS: VAULT_VERSION=1.8.5
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 05 Nov 2021 01:44:49 GMT
VOLUME [/vault/logs]
# Fri, 05 Nov 2021 01:44:50 GMT
VOLUME [/vault/file]
# Fri, 05 Nov 2021 01:44:50 GMT
EXPOSE 8200
# Fri, 05 Nov 2021 01:44:50 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 05 Nov 2021 01:44:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Nov 2021 01:44:51 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885b822523b48f580685a4b7bfc6635cc702e7d51b5bb9837ac745533c186173`  
		Last Modified: Fri, 05 Nov 2021 01:46:19 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55710bbd741cf26c2aeaba8337b3520476e684438e183da9448b773fcf4b7344`  
		Last Modified: Fri, 05 Nov 2021 01:46:52 GMT  
		Size: 62.3 MB (62270548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2368999dddd5fa4fb572762adcb99f57bf8b79fab460d2a9210507f1aeb191ac`  
		Last Modified: Fri, 05 Nov 2021 01:46:20 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d7c59ebb88433224c433a44bd3a04456b0a0d96560863cdcdc6b667875b7ec`  
		Last Modified: Fri, 05 Nov 2021 01:46:19 GMT  
		Size: 1.8 KB (1825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:0e95fc43a67e977e066a13a001e4a2c0e995ff2657de330a28cca0164d372cac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66854957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:481906745721411dcb4230595a83ee7f9bfdf0823529c5a39034c4d7cf33ac5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:13:11 GMT
ARG VAULT_VERSION=1.8.5
# Fri, 12 Nov 2021 18:13:12 GMT
# ARGS: VAULT_VERSION=1.8.5
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 12 Nov 2021 18:13:21 GMT
# ARGS: VAULT_VERSION=1.8.5
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 12 Nov 2021 18:13:21 GMT
# ARGS: VAULT_VERSION=1.8.5
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 12 Nov 2021 18:13:22 GMT
VOLUME [/vault/logs]
# Fri, 12 Nov 2021 18:13:23 GMT
VOLUME [/vault/file]
# Fri, 12 Nov 2021 18:13:24 GMT
EXPOSE 8200
# Fri, 12 Nov 2021 18:13:26 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 12 Nov 2021 18:13:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 18:13:27 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4adb27be142b8b5fe9dd195df174830ecb7a44c86f0568a74a6cf0fab8c9f3`  
		Last Modified: Fri, 12 Nov 2021 18:15:10 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d822e2f0230aba3d2cefd2dc4d3be8f3652c7fe368e4a43aba7f97cc6f10b6`  
		Last Modified: Fri, 12 Nov 2021 18:15:18 GMT  
		Size: 64.1 MB (64134043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1eaf15d533bc354dc7bf18782417d0d931a97b2909017217700b9b06956cd5c`  
		Last Modified: Fri, 12 Nov 2021 18:15:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c61c78635277cd50980496d80918f364be79e0b6309177291e5a642c35ad3b`  
		Last Modified: Fri, 12 Nov 2021 18:15:10 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; 386

```console
$ docker pull vault@sha256:f5d4dce800fd5d4cd54fc88d07ce521dcf074ccb43f48dff68b170447d728703
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68279456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe955277ce65f87e247a2b72fb52963c7a139b0d0abb959aad68dce45667239`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:42 GMT
ADD file:403428c2903dd9dea10d069185873cb2c2c3149c553797807c69f22aa3d12fe3 in / 
# Fri, 12 Nov 2021 16:38:42 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 17:31:55 GMT
ARG VAULT_VERSION=1.8.5
# Fri, 12 Nov 2021 17:31:57 GMT
# ARGS: VAULT_VERSION=1.8.5
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 12 Nov 2021 17:32:14 GMT
# ARGS: VAULT_VERSION=1.8.5
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 12 Nov 2021 17:32:16 GMT
# ARGS: VAULT_VERSION=1.8.5
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 12 Nov 2021 17:32:16 GMT
VOLUME [/vault/logs]
# Fri, 12 Nov 2021 17:32:16 GMT
VOLUME [/vault/file]
# Fri, 12 Nov 2021 17:32:17 GMT
EXPOSE 8200
# Fri, 12 Nov 2021 17:32:17 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 12 Nov 2021 17:32:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 17:32:18 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:5420e0d28c84ecb16748cb90cc6acf8e2a81dab10cb1f674f3eee8533e53c62a`  
		Last Modified: Fri, 12 Nov 2021 16:39:36 GMT  
		Size: 2.8 MB (2830948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf4c0c927d2593dfbd7926d38039f4c03d2102ba0776b1ad493dcc66db4167f`  
		Last Modified: Fri, 12 Nov 2021 17:34:43 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403f2827665674e108c599a90050421a8b9a40e3ba0f62680b69af2524cc00e9`  
		Last Modified: Fri, 12 Nov 2021 17:34:59 GMT  
		Size: 65.4 MB (65445233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a95c32fa455bb256f024f90c52ded7e07c49ca98bd27aee9b2b7f34cffb343a`  
		Last Modified: Fri, 12 Nov 2021 17:34:43 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5102adb48bdd2d3c560f0c47ae8df04a5684cd951650d89351071cf3eb5db290`  
		Last Modified: Fri, 12 Nov 2021 17:34:43 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
