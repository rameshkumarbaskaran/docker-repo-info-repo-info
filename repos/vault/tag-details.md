<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `vault`

-	[`vault:1.10.0`](#vault1100)
-	[`vault:1.7.10`](#vault1710)
-	[`vault:1.8.9`](#vault189)
-	[`vault:1.9.4`](#vault194)
-	[`vault:latest`](#vaultlatest)

## `vault:1.10.0`

```console
$ docker pull vault@sha256:6f0349625bd51d69ded3a6b4f4e1a924f3cc51ceeb27f5dd5d894420dce131b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.10.0` - linux; amd64

```console
$ docker pull vault@sha256:3e3d3ae982561d4f616df2ebbb4cc40ba2bc555830ba17293f48221b2154b7d4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73961495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c49fe1359bf33cbee42b4ef8aa1b709bd846bf32abe3874fc5944dac596955c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 15:57:48 GMT
ARG VAULT_VERSION=1.10.0
# Tue, 29 Mar 2022 15:57:49 GMT
# ARGS: VAULT_VERSION=1.10.0
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 29 Mar 2022 15:57:56 GMT
# ARGS: VAULT_VERSION=1.10.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 29 Mar 2022 15:57:57 GMT
# ARGS: VAULT_VERSION=1.10.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 29 Mar 2022 15:57:57 GMT
VOLUME [/vault/logs]
# Tue, 29 Mar 2022 15:57:57 GMT
VOLUME [/vault/file]
# Tue, 29 Mar 2022 15:57:58 GMT
EXPOSE 8200
# Tue, 29 Mar 2022 15:57:58 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 15:57:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 15:57:58 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9410e6698beb0d9bdefd3d892667953f658175a2304498169a05ed357cb86f90`  
		Last Modified: Tue, 29 Mar 2022 15:58:47 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac2d612d86969aef5d60606ecad167329bc0cf7b1eae36d1e4e46cf1f66836a`  
		Last Modified: Tue, 29 Mar 2022 15:58:55 GMT  
		Size: 71.1 MB (71139872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcaa515f14be0794ee1300df37f35e83b63cd540bbdddd71369b90124a229e8f`  
		Last Modified: Tue, 29 Mar 2022 15:58:47 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915ca5d61cef7bc0679d5d2229b1f793c205c4af372fe0f405042c18994b51e0`  
		Last Modified: Tue, 29 Mar 2022 15:58:47 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.10.0` - linux; arm variant v6

```console
$ docker pull vault@sha256:c35cfe9414758c5f71f04c2912c44d0c8b5bc451cd38ab038bf70b8483a6ab18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.3 MB (67255459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f6f4acc3550d99055a4794023e7c7ce702ed93896746a188052de7f2f58fdf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:46 GMT
ADD file:9670f4f7de6a9b8eb844e418daedd0dbad90009126790eb65e246b29cac5ea47 in / 
# Tue, 29 Mar 2022 00:49:46 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:27:28 GMT
ARG VAULT_VERSION=1.10.0
# Tue, 29 Mar 2022 08:27:29 GMT
# ARGS: VAULT_VERSION=1.10.0
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 29 Mar 2022 08:27:46 GMT
# ARGS: VAULT_VERSION=1.10.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 29 Mar 2022 08:27:48 GMT
# ARGS: VAULT_VERSION=1.10.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 29 Mar 2022 08:27:49 GMT
VOLUME [/vault/logs]
# Tue, 29 Mar 2022 08:27:49 GMT
VOLUME [/vault/file]
# Tue, 29 Mar 2022 08:27:50 GMT
EXPOSE 8200
# Tue, 29 Mar 2022 08:27:50 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 08:27:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:27:51 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:79f5c9df0b90097bae07a9861e9e0e3f52a16b0bfde2793c4e14ad033cfb47f4`  
		Last Modified: Tue, 29 Mar 2022 00:51:45 GMT  
		Size: 2.6 MB (2626017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddd0f53daa0f78b16019fa50926206dbb94275796b463f8444d6303f5fbfb11`  
		Last Modified: Tue, 29 Mar 2022 08:30:09 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7bad6793b2ca8b8236d93e261cfab49dd6d02259d11c52be41f784a5f1c061`  
		Last Modified: Tue, 29 Mar 2022 08:30:46 GMT  
		Size: 64.6 MB (64626174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa351481278dde48c5ede5ce353f4a58bd9ab38275e51d16a3c6a49bf82c8fa3`  
		Last Modified: Tue, 29 Mar 2022 08:30:09 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507324d593de6a89aa536e2c16e564543c4a8b7d2873352a6d6446caf64deb9e`  
		Last Modified: Tue, 29 Mar 2022 08:30:09 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.10.0` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:d57ec114c479f1e15b8aa656f37200cad14cf67dd45d6db29f0313dfe0ba8945
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69006932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8180b24c16acf420e65b2c9b4eabaa27cf58cd1e890e2b4e5326617b50753ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:12 GMT
ADD file:d0894581cf2fb7d7911ecb25bf0368675197db96d762977964ffc3a7ae8c774c in / 
# Tue, 29 Mar 2022 00:40:13 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 19:15:30 GMT
ARG VAULT_VERSION=1.10.0
# Tue, 29 Mar 2022 19:15:31 GMT
# ARGS: VAULT_VERSION=1.10.0
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 29 Mar 2022 19:15:41 GMT
# ARGS: VAULT_VERSION=1.10.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 29 Mar 2022 19:15:41 GMT
# ARGS: VAULT_VERSION=1.10.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 29 Mar 2022 19:15:42 GMT
VOLUME [/vault/logs]
# Tue, 29 Mar 2022 19:15:43 GMT
VOLUME [/vault/file]
# Tue, 29 Mar 2022 19:15:44 GMT
EXPOSE 8200
# Tue, 29 Mar 2022 19:15:46 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 19:15:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 19:15:47 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:810d54c7e01bab9975c1fb485c543715b76de7708166132520dfec0fc32c3754`  
		Last Modified: Tue, 29 Mar 2022 00:41:26 GMT  
		Size: 2.7 MB (2717494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac2e81760fed4a5aa8ae3e2f9e652bb6202b03d25114efcdf0188d1570ec4d6`  
		Last Modified: Tue, 29 Mar 2022 19:17:12 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7840b2fe57ad7a4506d621a6331cad15a364833f8580dde46af6f67713fb996d`  
		Last Modified: Tue, 29 Mar 2022 19:17:21 GMT  
		Size: 66.3 MB (66286233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91efb256ac946e31487cad9bfa5e5e7b34f6243baafa849cea6be0dbce899f5`  
		Last Modified: Tue, 29 Mar 2022 19:17:12 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab27a80fcce5ee3a55694d37bd6b35c0948a33343ee14ef11b3e7462e4c8535`  
		Last Modified: Tue, 29 Mar 2022 19:17:12 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.10.0` - linux; 386

```console
$ docker pull vault@sha256:3e6639fd531c4a574094e4eb55de537366522c1d00e08590921fcbaebb8c148d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70341183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127fb11a8581e188357eecd7cb4230ed3b8a805e14c133e41e397d692da11b0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 29 Mar 2022 00:38:40 GMT
ADD file:b779b35f4afe33387545e54afc23f09a30d43ad4817cc92ed6b083099748b3cb in / 
# Tue, 29 Mar 2022 00:38:40 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 11:15:09 GMT
ARG VAULT_VERSION=1.10.0
# Tue, 29 Mar 2022 11:15:10 GMT
# ARGS: VAULT_VERSION=1.10.0
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 29 Mar 2022 11:15:19 GMT
# ARGS: VAULT_VERSION=1.10.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 29 Mar 2022 11:15:19 GMT
# ARGS: VAULT_VERSION=1.10.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 29 Mar 2022 11:15:20 GMT
VOLUME [/vault/logs]
# Tue, 29 Mar 2022 11:15:21 GMT
VOLUME [/vault/file]
# Tue, 29 Mar 2022 11:15:22 GMT
EXPOSE 8200
# Tue, 29 Mar 2022 11:15:24 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 11:15:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 11:15:25 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:ff47816780f28cb5e3d0a86624e638d039b84373892ba3065b1ff9cd4b55b356`  
		Last Modified: Tue, 29 Mar 2022 00:39:52 GMT  
		Size: 2.8 MB (2821065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560dd7bc67f74f27fccfd88ade0898357779d6bfa50cde2191923c91214a2756`  
		Last Modified: Tue, 29 Mar 2022 11:16:48 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4521e0d6d64b0047c0b8598dec94ca862ea9311830a9ca398183f3074e6c5573`  
		Last Modified: Tue, 29 Mar 2022 11:16:56 GMT  
		Size: 67.5 MB (67516913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e2ebf18ed955a3f91512534e7352d0981376744ec88e83ff45b90d2d8d2b5e`  
		Last Modified: Tue, 29 Mar 2022 11:16:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1149e8be2b11e5246e72fb7c49493c9521bafed63ec060f71d66027b7dc77f10`  
		Last Modified: Tue, 29 Mar 2022 11:16:48 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.7.10`

```console
$ docker pull vault@sha256:bd12f9eba283fe77dec8636b36e64218d68c49ed8e138aded13cdb943473713e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.7.10` - linux; amd64

```console
$ docker pull vault@sha256:84b2c21e167b26465579496bdda1a680ffd92557c22b6b34f66eb5e0a7a2095e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68118956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624cf2f42a6ced5aa7fb5f8afa14284e9e3ae666b6eb2111046f6c53a8080375`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 15:58:25 GMT
ARG VAULT_VERSION=1.7.10
# Tue, 29 Mar 2022 15:58:26 GMT
# ARGS: VAULT_VERSION=1.7.10
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 29 Mar 2022 15:58:32 GMT
# ARGS: VAULT_VERSION=1.7.10
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 29 Mar 2022 15:58:33 GMT
# ARGS: VAULT_VERSION=1.7.10
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 29 Mar 2022 15:58:33 GMT
VOLUME [/vault/logs]
# Tue, 29 Mar 2022 15:58:33 GMT
VOLUME [/vault/file]
# Tue, 29 Mar 2022 15:58:33 GMT
EXPOSE 8200
# Tue, 29 Mar 2022 15:58:34 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 15:58:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 15:58:34 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f9563cb18c66380e1d0b2850d43c036d00a3046d670cf8bf6423f53813c605`  
		Last Modified: Tue, 29 Mar 2022 15:59:38 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16f637fdfcd02ca5d3b4c234b77c684a36282cabd0d816f3e4d2b6496e4a459`  
		Last Modified: Tue, 29 Mar 2022 15:59:47 GMT  
		Size: 65.3 MB (65297335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065d05db24d0da0ef90b14f4e7e3c33b30b89095b74cceef33d1234380dbd9ea`  
		Last Modified: Tue, 29 Mar 2022 15:59:39 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:397a196250ba69509af4a1a53a660c6f68d83aae4cd0e0de8bf6dc8463348cfd`  
		Last Modified: Tue, 29 Mar 2022 15:59:38 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.10` - linux; arm variant v6

```console
$ docker pull vault@sha256:8550d07bc6d99be153c2c1ba0150768986625947588fe1dfb132ac4a4ef32ada
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62850783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b62def064136aa61e48661f1e3f4c64f91a926874207ac558b75b4a5263e81`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:46 GMT
ADD file:9670f4f7de6a9b8eb844e418daedd0dbad90009126790eb65e246b29cac5ea47 in / 
# Tue, 29 Mar 2022 00:49:46 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:29:13 GMT
ARG VAULT_VERSION=1.7.10
# Tue, 29 Mar 2022 08:29:14 GMT
# ARGS: VAULT_VERSION=1.7.10
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 29 Mar 2022 08:29:30 GMT
# ARGS: VAULT_VERSION=1.7.10
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 29 Mar 2022 08:29:32 GMT
# ARGS: VAULT_VERSION=1.7.10
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 29 Mar 2022 08:29:33 GMT
VOLUME [/vault/logs]
# Tue, 29 Mar 2022 08:29:33 GMT
VOLUME [/vault/file]
# Tue, 29 Mar 2022 08:29:33 GMT
EXPOSE 8200
# Tue, 29 Mar 2022 08:29:34 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 08:29:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:29:35 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:79f5c9df0b90097bae07a9861e9e0e3f52a16b0bfde2793c4e14ad033cfb47f4`  
		Last Modified: Tue, 29 Mar 2022 00:51:45 GMT  
		Size: 2.6 MB (2626017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dead6a4f26e8c071eb5d94e027513a1f2d3ef9f0af0df88a594af168fca1e85f`  
		Last Modified: Tue, 29 Mar 2022 08:32:22 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fb2dff03f41be5059fdf3a8bac3e0795822a2850c7432a77b21b7b5d0edfdb`  
		Last Modified: Tue, 29 Mar 2022 08:32:46 GMT  
		Size: 60.2 MB (60221496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13b1dc3dc576aa75eed3f5ea80f2bd193b722eab88643b61a5464c86fed1219`  
		Last Modified: Tue, 29 Mar 2022 08:32:22 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4a7119f67e33c69611573108577e3f1d8282e3eaa853a1675a86ebd438e075`  
		Last Modified: Tue, 29 Mar 2022 08:32:22 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.10` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:d700b947acaf0ff3b9d901355e0d9edb0612344ef996d818f36cd4fd7fd4b28d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64538607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b009cd4bec62c0ab36b1ce624ea90841b047047808b988ae3d1767d7e310a533`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:12 GMT
ADD file:d0894581cf2fb7d7911ecb25bf0368675197db96d762977964ffc3a7ae8c774c in / 
# Tue, 29 Mar 2022 00:40:13 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 19:16:38 GMT
ARG VAULT_VERSION=1.7.10
# Tue, 29 Mar 2022 19:16:39 GMT
# ARGS: VAULT_VERSION=1.7.10
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 29 Mar 2022 19:16:47 GMT
# ARGS: VAULT_VERSION=1.7.10
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 29 Mar 2022 19:16:47 GMT
# ARGS: VAULT_VERSION=1.7.10
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 29 Mar 2022 19:16:48 GMT
VOLUME [/vault/logs]
# Tue, 29 Mar 2022 19:16:49 GMT
VOLUME [/vault/file]
# Tue, 29 Mar 2022 19:16:50 GMT
EXPOSE 8200
# Tue, 29 Mar 2022 19:16:52 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 19:16:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 19:16:53 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:810d54c7e01bab9975c1fb485c543715b76de7708166132520dfec0fc32c3754`  
		Last Modified: Tue, 29 Mar 2022 00:41:26 GMT  
		Size: 2.7 MB (2717494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa10e1b1e1fb3a3016aed042d5c43581861ff908366151153bc617955ffdcddf`  
		Last Modified: Tue, 29 Mar 2022 19:18:06 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfdb59622e2b2a7b84d32df3d5ed77c5f875b48161b129084c7da5c6d95e107e`  
		Last Modified: Tue, 29 Mar 2022 19:18:13 GMT  
		Size: 61.8 MB (61817903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bceec76572aa25fac87fb5aeebe8e8827c0f050bd8d72cb510b88ff800a07c9`  
		Last Modified: Tue, 29 Mar 2022 19:18:05 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b69c584796704410c0d5f92b565838f182bb98cae334c18fbfb2b17df90909`  
		Last Modified: Tue, 29 Mar 2022 19:18:05 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.10` - linux; 386

```console
$ docker pull vault@sha256:a91823756f3452760eb1e256fb9b1758652f5b64259fffad82c590865bc7e3d4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (65976408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9427be51da175ef46e00b706871db602efb7145f0ef905de72e933ce03b04bb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 29 Mar 2022 00:38:40 GMT
ADD file:b779b35f4afe33387545e54afc23f09a30d43ad4817cc92ed6b083099748b3cb in / 
# Tue, 29 Mar 2022 00:38:40 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 11:16:13 GMT
ARG VAULT_VERSION=1.7.10
# Tue, 29 Mar 2022 11:16:14 GMT
# ARGS: VAULT_VERSION=1.7.10
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 29 Mar 2022 11:16:22 GMT
# ARGS: VAULT_VERSION=1.7.10
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 29 Mar 2022 11:16:22 GMT
# ARGS: VAULT_VERSION=1.7.10
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 29 Mar 2022 11:16:23 GMT
VOLUME [/vault/logs]
# Tue, 29 Mar 2022 11:16:24 GMT
VOLUME [/vault/file]
# Tue, 29 Mar 2022 11:16:25 GMT
EXPOSE 8200
# Tue, 29 Mar 2022 11:16:27 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 11:16:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 11:16:28 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:ff47816780f28cb5e3d0a86624e638d039b84373892ba3065b1ff9cd4b55b356`  
		Last Modified: Tue, 29 Mar 2022 00:39:52 GMT  
		Size: 2.8 MB (2821065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea890550e5f23cf0fd71ffea100c03d3f14da3f24aefdbd6b9e839a25fa6f561`  
		Last Modified: Tue, 29 Mar 2022 11:17:41 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2177c013f5f1cc91215a166f390cb16675a920cc97210263676e04fc949121`  
		Last Modified: Tue, 29 Mar 2022 11:17:48 GMT  
		Size: 63.2 MB (63152139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa94bdf71d22cce791cacc41bd58bd10125340e8b0b3cd1ba6dc6423e8c4cb77`  
		Last Modified: Tue, 29 Mar 2022 11:17:41 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d359be8d5a0c4f63e6d062a913b5437c61420e9443aaa81e8c16659b8403db4`  
		Last Modified: Tue, 29 Mar 2022 11:17:41 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.8.9`

```console
$ docker pull vault@sha256:2b6bd43e8dd5147174db12dc177edacc34c3a4ac8e0bc2575999d4d3b771fb83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.8.9` - linux; amd64

```console
$ docker pull vault@sha256:be067966b5f33de8e8059e60c591cada30993d53d1d8fe628b753ae36951c5cc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70594516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1562a1d4fd29d73fdf324e797c28620faa2422c43bc733f2cd374911e978d993`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 15:58:14 GMT
ARG VAULT_VERSION=1.8.9
# Tue, 29 Mar 2022 15:58:14 GMT
# ARGS: VAULT_VERSION=1.8.9
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 29 Mar 2022 15:58:21 GMT
# ARGS: VAULT_VERSION=1.8.9
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 29 Mar 2022 15:58:22 GMT
# ARGS: VAULT_VERSION=1.8.9
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 29 Mar 2022 15:58:22 GMT
VOLUME [/vault/logs]
# Tue, 29 Mar 2022 15:58:22 GMT
VOLUME [/vault/file]
# Tue, 29 Mar 2022 15:58:22 GMT
EXPOSE 8200
# Tue, 29 Mar 2022 15:58:23 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 15:58:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 15:58:23 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616f91b8ceea0bb43521f60e2eeeec3d3fd38c8ee0f21a28457b8af6d42a7aac`  
		Last Modified: Tue, 29 Mar 2022 15:59:22 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6faea0a254bb8c3a32fbf4c62a7b3172c2b2825f08b5dfc1815a3d7993c1323`  
		Last Modified: Tue, 29 Mar 2022 15:59:31 GMT  
		Size: 67.8 MB (67772895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ad8109267b84d9d9ab768344769e07736cfb2da19ca759a05ad690e88fd5e4`  
		Last Modified: Tue, 29 Mar 2022 15:59:22 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a57cf2dfd247c4878aba5df33b8db54d629d59ad57cc23d504bc01ba071247`  
		Last Modified: Tue, 29 Mar 2022 15:59:22 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.8.9` - linux; arm variant v6

```console
$ docker pull vault@sha256:f52b2481370a052039253f883d739babe7ecb04176f65dc2c83d38d7030aa207
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64943281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee163e04b0f4f3509a28350bdee7cf3d207c2ac1cab013416b270e9bc5cf94ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:46 GMT
ADD file:9670f4f7de6a9b8eb844e418daedd0dbad90009126790eb65e246b29cac5ea47 in / 
# Tue, 29 Mar 2022 00:49:46 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:28:36 GMT
ARG VAULT_VERSION=1.8.9
# Tue, 29 Mar 2022 08:28:37 GMT
# ARGS: VAULT_VERSION=1.8.9
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 29 Mar 2022 08:28:56 GMT
# ARGS: VAULT_VERSION=1.8.9
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 29 Mar 2022 08:28:58 GMT
# ARGS: VAULT_VERSION=1.8.9
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 29 Mar 2022 08:28:59 GMT
VOLUME [/vault/logs]
# Tue, 29 Mar 2022 08:28:59 GMT
VOLUME [/vault/file]
# Tue, 29 Mar 2022 08:29:00 GMT
EXPOSE 8200
# Tue, 29 Mar 2022 08:29:00 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 08:29:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:29:01 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:79f5c9df0b90097bae07a9861e9e0e3f52a16b0bfde2793c4e14ad033cfb47f4`  
		Last Modified: Tue, 29 Mar 2022 00:51:45 GMT  
		Size: 2.6 MB (2626017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cd4e0e42e837a09ad59f54fee14741bd065cc90e40d609ff350b39ec320620`  
		Last Modified: Tue, 29 Mar 2022 08:31:41 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c603a68d521e330ec202387a057191cc94eb20c816ae6054a27e0de1e43c43e`  
		Last Modified: Tue, 29 Mar 2022 08:32:15 GMT  
		Size: 62.3 MB (62313998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2dee612a4de616b72ffdf492aaa3443e7e101ae6d9403f4269bffd0b2f468cb`  
		Last Modified: Tue, 29 Mar 2022 08:31:41 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2885b7aae017b60f13c74e29ff65d0079af5b04fa29a714863cc9ed8ee796cfa`  
		Last Modified: Tue, 29 Mar 2022 08:31:41 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.8.9` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:9e26b9f8939b3243eedec5bf00f0c34bf3b77d11059d349abf7a00154bce2292
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66860422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85500058834d8a84df999ab4a4eb3e977d3d9e00a248aa20a8083f113d4ec514`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:12 GMT
ADD file:d0894581cf2fb7d7911ecb25bf0368675197db96d762977964ffc3a7ae8c774c in / 
# Tue, 29 Mar 2022 00:40:13 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 19:16:16 GMT
ARG VAULT_VERSION=1.8.9
# Tue, 29 Mar 2022 19:16:17 GMT
# ARGS: VAULT_VERSION=1.8.9
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 29 Mar 2022 19:16:25 GMT
# ARGS: VAULT_VERSION=1.8.9
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 29 Mar 2022 19:16:26 GMT
# ARGS: VAULT_VERSION=1.8.9
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 29 Mar 2022 19:16:27 GMT
VOLUME [/vault/logs]
# Tue, 29 Mar 2022 19:16:28 GMT
VOLUME [/vault/file]
# Tue, 29 Mar 2022 19:16:29 GMT
EXPOSE 8200
# Tue, 29 Mar 2022 19:16:31 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 19:16:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 19:16:32 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:810d54c7e01bab9975c1fb485c543715b76de7708166132520dfec0fc32c3754`  
		Last Modified: Tue, 29 Mar 2022 00:41:26 GMT  
		Size: 2.7 MB (2717494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dffca0d1b2b90640459a8cc2951bbd2779615ae70b90a6669a0adea06cde5b5`  
		Last Modified: Tue, 29 Mar 2022 19:17:49 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fadb2a644d33732c6b29fa7359f1596e2414ed38956991b503f91aa59c9ffa3`  
		Last Modified: Tue, 29 Mar 2022 19:17:57 GMT  
		Size: 64.1 MB (64139720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4231e51556d2f4cb94c856446b127635a9d1148648bec24f8946ab756e96a275`  
		Last Modified: Tue, 29 Mar 2022 19:17:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29223c4779f8ef68d5aaf23c7235cb7e31239eca5b8ebf9cee42600cbb74ea1`  
		Last Modified: Tue, 29 Mar 2022 19:17:49 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.8.9` - linux; 386

```console
$ docker pull vault@sha256:ccaa2d8afc0c7b18a0bce18fa18c3c43ce21e574225e5c1aee58bfb2fa1ace97
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68311608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945fab0a815e27e83485ca4640291634388f88b01b3262356ee0ce1527bed054`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 29 Mar 2022 00:38:40 GMT
ADD file:b779b35f4afe33387545e54afc23f09a30d43ad4817cc92ed6b083099748b3cb in / 
# Tue, 29 Mar 2022 00:38:40 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 11:15:51 GMT
ARG VAULT_VERSION=1.8.9
# Tue, 29 Mar 2022 11:15:52 GMT
# ARGS: VAULT_VERSION=1.8.9
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 29 Mar 2022 11:16:00 GMT
# ARGS: VAULT_VERSION=1.8.9
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 29 Mar 2022 11:16:01 GMT
# ARGS: VAULT_VERSION=1.8.9
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 29 Mar 2022 11:16:02 GMT
VOLUME [/vault/logs]
# Tue, 29 Mar 2022 11:16:03 GMT
VOLUME [/vault/file]
# Tue, 29 Mar 2022 11:16:04 GMT
EXPOSE 8200
# Tue, 29 Mar 2022 11:16:06 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 11:16:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 11:16:07 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:ff47816780f28cb5e3d0a86624e638d039b84373892ba3065b1ff9cd4b55b356`  
		Last Modified: Tue, 29 Mar 2022 00:39:52 GMT  
		Size: 2.8 MB (2821065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae0f966810c44aca2472089e5a80ed84e414637955787083ccbfd2e8b466b5d4`  
		Last Modified: Tue, 29 Mar 2022 11:17:25 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6676b6be2ff3d9b132d7557f7ad9b840387dc15aaf5c787b0cbc9fa6d06d9c09`  
		Last Modified: Tue, 29 Mar 2022 11:17:33 GMT  
		Size: 65.5 MB (65487338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52aa994909b7c8d1071fa2e7c31989879a0270cac18b36fc9796d214b2312c3`  
		Last Modified: Tue, 29 Mar 2022 11:17:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e170f6f008f41fa803910fd1d31cb15cc0f5de584b11b456e07cc6240b608b`  
		Last Modified: Tue, 29 Mar 2022 11:17:25 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.9.4`

```console
$ docker pull vault@sha256:bf30d85a3c7900dfabcaf6d57b3a9de442a37fd02e68bf85a3b75ecbcd7689db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.9.4` - linux; amd64

```console
$ docker pull vault@sha256:78b254e8cbd05b8223f4b275e091e97a308dc3be625f3dde9397ec8e80907ded
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73150877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f46d80d52533bb3d6ecbe27f629ab5609fbb2e0200fec7e9eb92d67f5659d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 15:58:00 GMT
ARG VAULT_VERSION=1.9.4
# Tue, 29 Mar 2022 15:58:01 GMT
# ARGS: VAULT_VERSION=1.9.4
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 29 Mar 2022 15:58:10 GMT
# ARGS: VAULT_VERSION=1.9.4
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 29 Mar 2022 15:58:11 GMT
# ARGS: VAULT_VERSION=1.9.4
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 29 Mar 2022 15:58:11 GMT
VOLUME [/vault/logs]
# Tue, 29 Mar 2022 15:58:12 GMT
VOLUME [/vault/file]
# Tue, 29 Mar 2022 15:58:12 GMT
EXPOSE 8200
# Tue, 29 Mar 2022 15:58:12 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 15:58:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 15:58:12 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3b67ba0d582b1cc8df507208e71355104b9b785dfb26cd72773c1e9492cd8a`  
		Last Modified: Tue, 29 Mar 2022 15:59:05 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727ab257599852120f913b87329880682741c35540765f967693179029f913f0`  
		Last Modified: Tue, 29 Mar 2022 15:59:14 GMT  
		Size: 70.3 MB (70329256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b35dad4735d0bdf4836aaeeebb3a5665eb049f57c7499868cf0e4bbd41d8a6`  
		Last Modified: Tue, 29 Mar 2022 15:59:05 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e5ab24152b73feeddbb49dd4db6b378ebc2dc48c44d14ac1f61f2c95122cee6`  
		Last Modified: Tue, 29 Mar 2022 15:59:05 GMT  
		Size: 1.8 KB (1810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.9.4` - linux; arm variant v6

```console
$ docker pull vault@sha256:ebcc1cb17d4dcbd2e7f12afaac4fdddbf2cb60324fe045a26234f4460a6bfc27
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66490849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8139d7e4d76af8bb63e361e05801686f38e2e81b34d0e1903b876d4097f16874`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:46 GMT
ADD file:9670f4f7de6a9b8eb844e418daedd0dbad90009126790eb65e246b29cac5ea47 in / 
# Tue, 29 Mar 2022 00:49:46 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:28:03 GMT
ARG VAULT_VERSION=1.9.4
# Tue, 29 Mar 2022 08:28:04 GMT
# ARGS: VAULT_VERSION=1.9.4
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 29 Mar 2022 08:28:20 GMT
# ARGS: VAULT_VERSION=1.9.4
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 29 Mar 2022 08:28:22 GMT
# ARGS: VAULT_VERSION=1.9.4
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 29 Mar 2022 08:28:23 GMT
VOLUME [/vault/logs]
# Tue, 29 Mar 2022 08:28:24 GMT
VOLUME [/vault/file]
# Tue, 29 Mar 2022 08:28:24 GMT
EXPOSE 8200
# Tue, 29 Mar 2022 08:28:25 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 08:28:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:28:26 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:79f5c9df0b90097bae07a9861e9e0e3f52a16b0bfde2793c4e14ad033cfb47f4`  
		Last Modified: Tue, 29 Mar 2022 00:51:45 GMT  
		Size: 2.6 MB (2626017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c523e0b26096611a809fb47e54a11fd3846be8fe1886d3e5d271a0b36ba9993`  
		Last Modified: Tue, 29 Mar 2022 08:30:57 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162c49f08613c6b2614e1184596bd9299f61c69dd37c30aeecd7e1607c26499c`  
		Last Modified: Tue, 29 Mar 2022 08:31:33 GMT  
		Size: 63.9 MB (63861564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4335beadf524075fb6db6db9784bab74f25909bf555e853cc45e9bd5dad7248b`  
		Last Modified: Tue, 29 Mar 2022 08:30:57 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18f6785f84a728b03fece3748eef06ee7bd01e71542de92a2d1e810bb55179f`  
		Last Modified: Tue, 29 Mar 2022 08:30:57 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.9.4` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:642591d8bb3e79fdd52e1f5c3ca30d22a8605268834a3498799b0b52dd7b551c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68261610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f4c48b8f89c067bf883d6f793694df15860feae1d879065efa08c56b7093622`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:12 GMT
ADD file:d0894581cf2fb7d7911ecb25bf0368675197db96d762977964ffc3a7ae8c774c in / 
# Tue, 29 Mar 2022 00:40:13 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 19:15:53 GMT
ARG VAULT_VERSION=1.9.4
# Tue, 29 Mar 2022 19:15:54 GMT
# ARGS: VAULT_VERSION=1.9.4
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 29 Mar 2022 19:16:03 GMT
# ARGS: VAULT_VERSION=1.9.4
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 29 Mar 2022 19:16:04 GMT
# ARGS: VAULT_VERSION=1.9.4
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 29 Mar 2022 19:16:04 GMT
VOLUME [/vault/logs]
# Tue, 29 Mar 2022 19:16:05 GMT
VOLUME [/vault/file]
# Tue, 29 Mar 2022 19:16:06 GMT
EXPOSE 8200
# Tue, 29 Mar 2022 19:16:08 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 19:16:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 19:16:09 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:810d54c7e01bab9975c1fb485c543715b76de7708166132520dfec0fc32c3754`  
		Last Modified: Tue, 29 Mar 2022 00:41:26 GMT  
		Size: 2.7 MB (2717494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e319ea78e6c5052babac3e0a801f2e40364fdf4b01e2f586d5f761a7ccf7711b`  
		Last Modified: Tue, 29 Mar 2022 19:17:32 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33bab5bb13e15ce9a5e4f4c60eacbec6b752b6e7f0ef7985ca5e731d17bcb8a1`  
		Last Modified: Tue, 29 Mar 2022 19:17:41 GMT  
		Size: 65.5 MB (65540913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885847a90bbb02310beb24a661835a274df697ccb1fb7bb789961c457ecef9f5`  
		Last Modified: Tue, 29 Mar 2022 19:17:32 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0027195d21a37dd94185eece9875c6c3ad5aa032eb5aecd0d82832cbbac701`  
		Last Modified: Tue, 29 Mar 2022 19:17:33 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.9.4` - linux; 386

```console
$ docker pull vault@sha256:b88d5392d780935755e1a406d010c7fe5130d1c0605830c4fcfa76f8c0b42a9d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69532760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061a4324d47b8eebf50420b7c272fd37c44e31826d3b6b6832a89e3a22e7167d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 29 Mar 2022 00:38:40 GMT
ADD file:b779b35f4afe33387545e54afc23f09a30d43ad4817cc92ed6b083099748b3cb in / 
# Tue, 29 Mar 2022 00:38:40 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 11:15:31 GMT
ARG VAULT_VERSION=1.9.4
# Tue, 29 Mar 2022 11:15:32 GMT
# ARGS: VAULT_VERSION=1.9.4
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 29 Mar 2022 11:15:40 GMT
# ARGS: VAULT_VERSION=1.9.4
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 29 Mar 2022 11:15:41 GMT
# ARGS: VAULT_VERSION=1.9.4
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 29 Mar 2022 11:15:41 GMT
VOLUME [/vault/logs]
# Tue, 29 Mar 2022 11:15:42 GMT
VOLUME [/vault/file]
# Tue, 29 Mar 2022 11:15:43 GMT
EXPOSE 8200
# Tue, 29 Mar 2022 11:15:45 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 11:15:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 11:15:46 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:ff47816780f28cb5e3d0a86624e638d039b84373892ba3065b1ff9cd4b55b356`  
		Last Modified: Tue, 29 Mar 2022 00:39:52 GMT  
		Size: 2.8 MB (2821065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82926d4dff7ea2969f58260171d8803f6e307b2d42831b69db2594544c40b25a`  
		Last Modified: Tue, 29 Mar 2022 11:17:08 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0fadb59d7c2e86417907079b6c49f1b7cc1c7676813dda9a14dd2e13676cfc0`  
		Last Modified: Tue, 29 Mar 2022 11:17:17 GMT  
		Size: 66.7 MB (66708487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f568a7e357b5a8cb2bc7577d3bf8c44f661c758b14dbc6f164a31e703bb908d7`  
		Last Modified: Tue, 29 Mar 2022 11:17:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b5ab9af5af18d842c72f7f00af6d52732680438f19e78529db61f00f1cdad1`  
		Last Modified: Tue, 29 Mar 2022 11:17:08 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:latest`

```console
$ docker pull vault@sha256:6f0349625bd51d69ded3a6b4f4e1a924f3cc51ceeb27f5dd5d894420dce131b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:latest` - linux; amd64

```console
$ docker pull vault@sha256:3e3d3ae982561d4f616df2ebbb4cc40ba2bc555830ba17293f48221b2154b7d4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73961495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c49fe1359bf33cbee42b4ef8aa1b709bd846bf32abe3874fc5944dac596955c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 15:57:48 GMT
ARG VAULT_VERSION=1.10.0
# Tue, 29 Mar 2022 15:57:49 GMT
# ARGS: VAULT_VERSION=1.10.0
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 29 Mar 2022 15:57:56 GMT
# ARGS: VAULT_VERSION=1.10.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 29 Mar 2022 15:57:57 GMT
# ARGS: VAULT_VERSION=1.10.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 29 Mar 2022 15:57:57 GMT
VOLUME [/vault/logs]
# Tue, 29 Mar 2022 15:57:57 GMT
VOLUME [/vault/file]
# Tue, 29 Mar 2022 15:57:58 GMT
EXPOSE 8200
# Tue, 29 Mar 2022 15:57:58 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 15:57:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 15:57:58 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9410e6698beb0d9bdefd3d892667953f658175a2304498169a05ed357cb86f90`  
		Last Modified: Tue, 29 Mar 2022 15:58:47 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac2d612d86969aef5d60606ecad167329bc0cf7b1eae36d1e4e46cf1f66836a`  
		Last Modified: Tue, 29 Mar 2022 15:58:55 GMT  
		Size: 71.1 MB (71139872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcaa515f14be0794ee1300df37f35e83b63cd540bbdddd71369b90124a229e8f`  
		Last Modified: Tue, 29 Mar 2022 15:58:47 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915ca5d61cef7bc0679d5d2229b1f793c205c4af372fe0f405042c18994b51e0`  
		Last Modified: Tue, 29 Mar 2022 15:58:47 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm variant v6

```console
$ docker pull vault@sha256:c35cfe9414758c5f71f04c2912c44d0c8b5bc451cd38ab038bf70b8483a6ab18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.3 MB (67255459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f6f4acc3550d99055a4794023e7c7ce702ed93896746a188052de7f2f58fdf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:46 GMT
ADD file:9670f4f7de6a9b8eb844e418daedd0dbad90009126790eb65e246b29cac5ea47 in / 
# Tue, 29 Mar 2022 00:49:46 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:27:28 GMT
ARG VAULT_VERSION=1.10.0
# Tue, 29 Mar 2022 08:27:29 GMT
# ARGS: VAULT_VERSION=1.10.0
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 29 Mar 2022 08:27:46 GMT
# ARGS: VAULT_VERSION=1.10.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 29 Mar 2022 08:27:48 GMT
# ARGS: VAULT_VERSION=1.10.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 29 Mar 2022 08:27:49 GMT
VOLUME [/vault/logs]
# Tue, 29 Mar 2022 08:27:49 GMT
VOLUME [/vault/file]
# Tue, 29 Mar 2022 08:27:50 GMT
EXPOSE 8200
# Tue, 29 Mar 2022 08:27:50 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 08:27:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:27:51 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:79f5c9df0b90097bae07a9861e9e0e3f52a16b0bfde2793c4e14ad033cfb47f4`  
		Last Modified: Tue, 29 Mar 2022 00:51:45 GMT  
		Size: 2.6 MB (2626017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddd0f53daa0f78b16019fa50926206dbb94275796b463f8444d6303f5fbfb11`  
		Last Modified: Tue, 29 Mar 2022 08:30:09 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7bad6793b2ca8b8236d93e261cfab49dd6d02259d11c52be41f784a5f1c061`  
		Last Modified: Tue, 29 Mar 2022 08:30:46 GMT  
		Size: 64.6 MB (64626174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa351481278dde48c5ede5ce353f4a58bd9ab38275e51d16a3c6a49bf82c8fa3`  
		Last Modified: Tue, 29 Mar 2022 08:30:09 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507324d593de6a89aa536e2c16e564543c4a8b7d2873352a6d6446caf64deb9e`  
		Last Modified: Tue, 29 Mar 2022 08:30:09 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:d57ec114c479f1e15b8aa656f37200cad14cf67dd45d6db29f0313dfe0ba8945
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69006932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8180b24c16acf420e65b2c9b4eabaa27cf58cd1e890e2b4e5326617b50753ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:12 GMT
ADD file:d0894581cf2fb7d7911ecb25bf0368675197db96d762977964ffc3a7ae8c774c in / 
# Tue, 29 Mar 2022 00:40:13 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 19:15:30 GMT
ARG VAULT_VERSION=1.10.0
# Tue, 29 Mar 2022 19:15:31 GMT
# ARGS: VAULT_VERSION=1.10.0
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 29 Mar 2022 19:15:41 GMT
# ARGS: VAULT_VERSION=1.10.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 29 Mar 2022 19:15:41 GMT
# ARGS: VAULT_VERSION=1.10.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 29 Mar 2022 19:15:42 GMT
VOLUME [/vault/logs]
# Tue, 29 Mar 2022 19:15:43 GMT
VOLUME [/vault/file]
# Tue, 29 Mar 2022 19:15:44 GMT
EXPOSE 8200
# Tue, 29 Mar 2022 19:15:46 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 19:15:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 19:15:47 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:810d54c7e01bab9975c1fb485c543715b76de7708166132520dfec0fc32c3754`  
		Last Modified: Tue, 29 Mar 2022 00:41:26 GMT  
		Size: 2.7 MB (2717494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac2e81760fed4a5aa8ae3e2f9e652bb6202b03d25114efcdf0188d1570ec4d6`  
		Last Modified: Tue, 29 Mar 2022 19:17:12 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7840b2fe57ad7a4506d621a6331cad15a364833f8580dde46af6f67713fb996d`  
		Last Modified: Tue, 29 Mar 2022 19:17:21 GMT  
		Size: 66.3 MB (66286233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91efb256ac946e31487cad9bfa5e5e7b34f6243baafa849cea6be0dbce899f5`  
		Last Modified: Tue, 29 Mar 2022 19:17:12 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab27a80fcce5ee3a55694d37bd6b35c0948a33343ee14ef11b3e7462e4c8535`  
		Last Modified: Tue, 29 Mar 2022 19:17:12 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; 386

```console
$ docker pull vault@sha256:3e6639fd531c4a574094e4eb55de537366522c1d00e08590921fcbaebb8c148d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70341183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127fb11a8581e188357eecd7cb4230ed3b8a805e14c133e41e397d692da11b0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 29 Mar 2022 00:38:40 GMT
ADD file:b779b35f4afe33387545e54afc23f09a30d43ad4817cc92ed6b083099748b3cb in / 
# Tue, 29 Mar 2022 00:38:40 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 11:15:09 GMT
ARG VAULT_VERSION=1.10.0
# Tue, 29 Mar 2022 11:15:10 GMT
# ARGS: VAULT_VERSION=1.10.0
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 29 Mar 2022 11:15:19 GMT
# ARGS: VAULT_VERSION=1.10.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 29 Mar 2022 11:15:19 GMT
# ARGS: VAULT_VERSION=1.10.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 29 Mar 2022 11:15:20 GMT
VOLUME [/vault/logs]
# Tue, 29 Mar 2022 11:15:21 GMT
VOLUME [/vault/file]
# Tue, 29 Mar 2022 11:15:22 GMT
EXPOSE 8200
# Tue, 29 Mar 2022 11:15:24 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 11:15:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 11:15:25 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:ff47816780f28cb5e3d0a86624e638d039b84373892ba3065b1ff9cd4b55b356`  
		Last Modified: Tue, 29 Mar 2022 00:39:52 GMT  
		Size: 2.8 MB (2821065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560dd7bc67f74f27fccfd88ade0898357779d6bfa50cde2191923c91214a2756`  
		Last Modified: Tue, 29 Mar 2022 11:16:48 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4521e0d6d64b0047c0b8598dec94ca862ea9311830a9ca398183f3074e6c5573`  
		Last Modified: Tue, 29 Mar 2022 11:16:56 GMT  
		Size: 67.5 MB (67516913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e2ebf18ed955a3f91512534e7352d0981376744ec88e83ff45b90d2d8d2b5e`  
		Last Modified: Tue, 29 Mar 2022 11:16:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1149e8be2b11e5246e72fb7c49493c9521bafed63ec060f71d66027b7dc77f10`  
		Last Modified: Tue, 29 Mar 2022 11:16:48 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
