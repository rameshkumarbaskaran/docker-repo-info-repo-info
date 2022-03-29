<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `vault`

-	[`vault:1.10.0`](#vault1100)
-	[`vault:1.7.10`](#vault1710)
-	[`vault:1.8.9`](#vault189)
-	[`vault:1.9.4`](#vault194)
-	[`vault:latest`](#vaultlatest)

## `vault:1.10.0`

```console
$ docker pull vault@sha256:a08ab01f649e2393a80d5ee4105118b46160fc81a9839d7bc93d6a88af73f9b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.10.0` - linux; amd64

```console
$ docker pull vault@sha256:cf915299a7a3372bea3e920f190c3b5e8a058f6cbdebf8c698edc6eef56608a0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73959284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc8c55968dfd0952942fa598f45752aaf2b061b1171e4b24c70e9ec5e7922a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 01:41:41 GMT
ARG VAULT_VERSION=1.10.0
# Thu, 24 Mar 2022 01:41:42 GMT
# ARGS: VAULT_VERSION=1.10.0
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 24 Mar 2022 01:41:50 GMT
# ARGS: VAULT_VERSION=1.10.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 24 Mar 2022 01:41:50 GMT
# ARGS: VAULT_VERSION=1.10.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 24 Mar 2022 01:41:51 GMT
VOLUME [/vault/logs]
# Thu, 24 Mar 2022 01:41:51 GMT
VOLUME [/vault/file]
# Thu, 24 Mar 2022 01:41:51 GMT
EXPOSE 8200
# Thu, 24 Mar 2022 01:41:51 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 24 Mar 2022 01:41:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Mar 2022 01:41:51 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fcd5c91b545b170c3df782b6f4d0fe2cc842f921a444d1f88d4ce4283e77fb`  
		Last Modified: Thu, 24 Mar 2022 01:42:06 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55650c8ff25aea687c7b9ed20f8a6c1c5f7a64797e9f77be32536d3a8b154c5c`  
		Last Modified: Thu, 24 Mar 2022 01:42:15 GMT  
		Size: 71.1 MB (71139845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49389f799b89b1f417ece330364ca79c08d5076386e03eefe19f06698df8cc70`  
		Last Modified: Thu, 24 Mar 2022 01:42:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052166a21f5a3e55f8f3791b0de5b332b3e52986826f9ce7af7a0f8707b6799a`  
		Last Modified: Thu, 24 Mar 2022 01:42:06 GMT  
		Size: 1.8 KB (1811 bytes)  
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
$ docker pull vault@sha256:c0e7ef35040b72ecd41fad1582a8e5e6746302c4c37bd1820d7b51ef0dc8bf79
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69005318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66d19936bb9c4bfac3fb587bb214d394314643156bac17bd3173253dbbdfbc8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 05:01:19 GMT
ARG VAULT_VERSION=1.10.0
# Thu, 24 Mar 2022 05:01:20 GMT
# ARGS: VAULT_VERSION=1.10.0
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 24 Mar 2022 05:01:28 GMT
# ARGS: VAULT_VERSION=1.10.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 24 Mar 2022 05:01:28 GMT
# ARGS: VAULT_VERSION=1.10.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 24 Mar 2022 05:01:29 GMT
VOLUME [/vault/logs]
# Thu, 24 Mar 2022 05:01:30 GMT
VOLUME [/vault/file]
# Thu, 24 Mar 2022 05:01:31 GMT
EXPOSE 8200
# Thu, 24 Mar 2022 05:01:33 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 24 Mar 2022 05:01:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Mar 2022 05:01:34 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0345d45f88ab1581e59610ee7c3e1fbcb18f0beca6c2ec3d38a6733d67be18`  
		Last Modified: Thu, 24 Mar 2022 05:02:04 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fbb2bd104f22a3cb2409e54521d5aaec2ec7681a992f0004725d35d017f8bf6`  
		Last Modified: Thu, 24 Mar 2022 05:02:12 GMT  
		Size: 66.3 MB (66286221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47eb2ed54a038e4f717ec7137afd45e52641967887e587ce919e9735ca1a4457`  
		Last Modified: Thu, 24 Mar 2022 05:02:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf50cb4d3613ef3733ece941d45994af7db2c98041f10b459f8a306d5495531`  
		Last Modified: Thu, 24 Mar 2022 05:02:04 GMT  
		Size: 1.8 KB (1814 bytes)  
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
$ docker pull vault@sha256:bc50b4e27b1511896ca7b37f5fd38cddb52c9cc2ff1d700524107a0287eb1416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.7.10` - linux; amd64

```console
$ docker pull vault@sha256:fd1bd1eaa4f5fa63b5c786688a0053732bc87a447328196c0b9ec64720883f95
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68116759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a06826f2eccb8617b2f9abf3deb2a9378272e4fbb2fb71254b6ae33165488e7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 06:09:57 GMT
ARG VAULT_VERSION=1.7.10
# Fri, 18 Mar 2022 06:09:58 GMT
# ARGS: VAULT_VERSION=1.7.10
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 18 Mar 2022 06:10:06 GMT
# ARGS: VAULT_VERSION=1.7.10
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 18 Mar 2022 06:10:07 GMT
# ARGS: VAULT_VERSION=1.7.10
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 18 Mar 2022 06:10:07 GMT
VOLUME [/vault/logs]
# Fri, 18 Mar 2022 06:10:08 GMT
VOLUME [/vault/file]
# Fri, 18 Mar 2022 06:10:08 GMT
EXPOSE 8200
# Fri, 18 Mar 2022 06:10:08 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 18 Mar 2022 06:10:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 06:10:08 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb4b9537c027109ec19372dc29ed2b3f279b0bbd625d554a1f798794e1601e4`  
		Last Modified: Fri, 18 Mar 2022 06:11:15 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6350df29b1eff600e4f6afa14109a626df1a2659e4755f37ffdfe55f49998fb`  
		Last Modified: Fri, 18 Mar 2022 06:11:27 GMT  
		Size: 65.3 MB (65297320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3322187b1172f7634af6e3df6cd08eb084437fe9acd38ba5e2799a07ded461`  
		Last Modified: Fri, 18 Mar 2022 06:11:15 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ad62b825dd56132c58906d824f919055c7192e66205b090cd49b2c9a47787f`  
		Last Modified: Fri, 18 Mar 2022 06:11:15 GMT  
		Size: 1.8 KB (1813 bytes)  
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
$ docker pull vault@sha256:53137247125158276c533bf3ddb44fe68b0b935c08e14e71f1c416e996b463e2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64536945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4ad691c6711e4cf1656ee244175a32f2d13201600e5a6fb22b48d491adc9bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:22:11 GMT
ARG VAULT_VERSION=1.7.10
# Thu, 17 Mar 2022 21:22:12 GMT
# ARGS: VAULT_VERSION=1.7.10
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 17 Mar 2022 21:22:19 GMT
# ARGS: VAULT_VERSION=1.7.10
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 17 Mar 2022 21:22:19 GMT
# ARGS: VAULT_VERSION=1.7.10
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 17 Mar 2022 21:22:20 GMT
VOLUME [/vault/logs]
# Thu, 17 Mar 2022 21:22:21 GMT
VOLUME [/vault/file]
# Thu, 17 Mar 2022 21:22:22 GMT
EXPOSE 8200
# Thu, 17 Mar 2022 21:22:24 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 17 Mar 2022 21:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 21:22:25 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd13d7d106c122c0a4a4a5ed9ff61dcf8754710ea5dc3638602df45a6693066`  
		Last Modified: Thu, 17 Mar 2022 21:23:39 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40cce72deac51a902601afc78ca35aae6a7205df390e537fde3e2910dc042ce`  
		Last Modified: Thu, 17 Mar 2022 21:23:48 GMT  
		Size: 61.8 MB (61817852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4892bdea507ec04abe9984bc4e0376203aa8b9fb2823dfd0eea4342083b1c71a`  
		Last Modified: Thu, 17 Mar 2022 21:23:39 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4de0c9398f7d24c114c8e074d91da860bc835ad2da8976f831dffcd8d886d96`  
		Last Modified: Thu, 17 Mar 2022 21:23:39 GMT  
		Size: 1.8 KB (1811 bytes)  
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
$ docker pull vault@sha256:a544f5b3ff3fc73630761961e657816af7493b2401fb323abd7127dbf56d6782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.8.9` - linux; amd64

```console
$ docker pull vault@sha256:8a0a62d51cfa0ad57de4c6bc6bc9ad671ecc3547bb9596d152a8f7780d40ac6b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70592291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c3b4d5f8e8cb595d55119cb6d080d4df0a99bba12326f737cd5f11e25a2d88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 06:09:40 GMT
ARG VAULT_VERSION=1.8.9
# Fri, 18 Mar 2022 06:09:41 GMT
# ARGS: VAULT_VERSION=1.8.9
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 18 Mar 2022 06:09:51 GMT
# ARGS: VAULT_VERSION=1.8.9
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 18 Mar 2022 06:09:52 GMT
# ARGS: VAULT_VERSION=1.8.9
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 18 Mar 2022 06:09:52 GMT
VOLUME [/vault/logs]
# Fri, 18 Mar 2022 06:09:52 GMT
VOLUME [/vault/file]
# Fri, 18 Mar 2022 06:09:52 GMT
EXPOSE 8200
# Fri, 18 Mar 2022 06:09:53 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 18 Mar 2022 06:09:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 06:09:53 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4099bee20305be9d397f0a5f16cdc708ee6f346b69a29411e6b6526fb765a0b2`  
		Last Modified: Fri, 18 Mar 2022 06:10:57 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c97522e2613d3a3e3b29f19b8982271d578b04887f6502f5164c4a7409d04da`  
		Last Modified: Fri, 18 Mar 2022 06:11:07 GMT  
		Size: 67.8 MB (67772854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7dad1471df7bbcddf38caa50e76d6d746261a0c8b775d10c0e94c5721eeb86`  
		Last Modified: Fri, 18 Mar 2022 06:10:57 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8600c16ab1de1a99e8114607ce920907e00234899669f55288f87a0c5947c3a`  
		Last Modified: Fri, 18 Mar 2022 06:10:57 GMT  
		Size: 1.8 KB (1812 bytes)  
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
$ docker pull vault@sha256:69196905f039bbc53826c5ad24b31640596074ce101a067768510c5e14e79413
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66858763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2abf260c24fe32eb22d4f30cd1a692b421c6cefb14b8933eb507eec2d990f5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:21:51 GMT
ARG VAULT_VERSION=1.8.9
# Thu, 17 Mar 2022 21:21:52 GMT
# ARGS: VAULT_VERSION=1.8.9
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 17 Mar 2022 21:21:59 GMT
# ARGS: VAULT_VERSION=1.8.9
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 17 Mar 2022 21:22:00 GMT
# ARGS: VAULT_VERSION=1.8.9
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 17 Mar 2022 21:22:01 GMT
VOLUME [/vault/logs]
# Thu, 17 Mar 2022 21:22:02 GMT
VOLUME [/vault/file]
# Thu, 17 Mar 2022 21:22:03 GMT
EXPOSE 8200
# Thu, 17 Mar 2022 21:22:05 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 17 Mar 2022 21:22:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 21:22:06 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a7297336d7f661e2b659153d30784ff7446d75cbf52d4d284c3160d403f3c7`  
		Last Modified: Thu, 17 Mar 2022 21:23:22 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b17be52b002a15336d2f31c3570c074b0da159439b478027ff22ac0f2179ab92`  
		Last Modified: Thu, 17 Mar 2022 21:23:31 GMT  
		Size: 64.1 MB (64139672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c066f87390fa8fa57be11b522737e5dd4ebcd550c429d561e538631dc42c1501`  
		Last Modified: Thu, 17 Mar 2022 21:23:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbaeba50cc34a51c09edbf6b157f728539d38ac5a231c45b16d80eb9ff934d38`  
		Last Modified: Thu, 17 Mar 2022 21:23:22 GMT  
		Size: 1.8 KB (1812 bytes)  
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
$ docker pull vault@sha256:fa1872d4aeb3bf1573d635680cefa8f9f59f755d25ed31091268505cbe44cae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.9.4` - linux; amd64

```console
$ docker pull vault@sha256:2f69ca64144ed051fce5c56662275638018ccc8abdca36c081c7d8d13c6e5eef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73148656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea101960f4b2ee058f5c271c8648638fe99681f35a4e7e93e17afe6464f726b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 06:09:23 GMT
ARG VAULT_VERSION=1.9.4
# Fri, 18 Mar 2022 06:09:23 GMT
# ARGS: VAULT_VERSION=1.9.4
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 18 Mar 2022 06:09:33 GMT
# ARGS: VAULT_VERSION=1.9.4
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 18 Mar 2022 06:09:34 GMT
# ARGS: VAULT_VERSION=1.9.4
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 18 Mar 2022 06:09:34 GMT
VOLUME [/vault/logs]
# Fri, 18 Mar 2022 06:09:34 GMT
VOLUME [/vault/file]
# Fri, 18 Mar 2022 06:09:34 GMT
EXPOSE 8200
# Fri, 18 Mar 2022 06:09:35 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 18 Mar 2022 06:09:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 06:09:35 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b0c57e7bd2053caa92e6d1a842e92613d7e03acae03b8c01599696c8a4618f`  
		Last Modified: Fri, 18 Mar 2022 06:10:38 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9151986c9e0e51544b8aa0381d6c3a7fddde89ef20da9da6922b4b7c79e6fab4`  
		Last Modified: Fri, 18 Mar 2022 06:10:47 GMT  
		Size: 70.3 MB (70329219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eafa7257e3b0259d6322d1cec41b4c0d06963cf88f7f79e67f21c5307ad0b94`  
		Last Modified: Fri, 18 Mar 2022 06:10:38 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1319691e2a6f384311de3d4e49fd05106b3ea45c75bbc1749dc61ad4dd9de9af`  
		Last Modified: Fri, 18 Mar 2022 06:10:38 GMT  
		Size: 1.8 KB (1812 bytes)  
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
$ docker pull vault@sha256:5f9d8e975f8a84c4ec936a26226a8e671187d9aab7b18cc68e58e340e2c1258e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68259983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27c250705bc5e11453057b1e017074f7d58d6ca093de25edd4e1c062b14b526`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:21:32 GMT
ARG VAULT_VERSION=1.9.4
# Thu, 17 Mar 2022 21:21:33 GMT
# ARGS: VAULT_VERSION=1.9.4
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 17 Mar 2022 21:21:40 GMT
# ARGS: VAULT_VERSION=1.9.4
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 17 Mar 2022 21:21:41 GMT
# ARGS: VAULT_VERSION=1.9.4
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 17 Mar 2022 21:21:41 GMT
VOLUME [/vault/logs]
# Thu, 17 Mar 2022 21:21:42 GMT
VOLUME [/vault/file]
# Thu, 17 Mar 2022 21:21:43 GMT
EXPOSE 8200
# Thu, 17 Mar 2022 21:21:45 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 17 Mar 2022 21:21:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 21:21:46 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50b8311591d8ad7007a6ab76dcc2338e5e055311f99f30641b7e15bb6a2d7bfb`  
		Last Modified: Thu, 17 Mar 2022 21:23:00 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf62ddb38aff6e05f3c9a71f3a0fb9c399c8ceb23f2fc282067f27883caa447`  
		Last Modified: Thu, 17 Mar 2022 21:23:10 GMT  
		Size: 65.5 MB (65540890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88aebca7138380de1e56351f1983f4ca1e79abfb20b3323a0917b98be30aa93`  
		Last Modified: Thu, 17 Mar 2022 21:23:00 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2253c5b1e2bcefc0c5c9c0054f18ba791cf5cba954d4f568a7955899bf18384f`  
		Last Modified: Thu, 17 Mar 2022 21:23:00 GMT  
		Size: 1.8 KB (1815 bytes)  
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
$ docker pull vault@sha256:a08ab01f649e2393a80d5ee4105118b46160fc81a9839d7bc93d6a88af73f9b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:latest` - linux; amd64

```console
$ docker pull vault@sha256:cf915299a7a3372bea3e920f190c3b5e8a058f6cbdebf8c698edc6eef56608a0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73959284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc8c55968dfd0952942fa598f45752aaf2b061b1171e4b24c70e9ec5e7922a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 01:41:41 GMT
ARG VAULT_VERSION=1.10.0
# Thu, 24 Mar 2022 01:41:42 GMT
# ARGS: VAULT_VERSION=1.10.0
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 24 Mar 2022 01:41:50 GMT
# ARGS: VAULT_VERSION=1.10.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 24 Mar 2022 01:41:50 GMT
# ARGS: VAULT_VERSION=1.10.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 24 Mar 2022 01:41:51 GMT
VOLUME [/vault/logs]
# Thu, 24 Mar 2022 01:41:51 GMT
VOLUME [/vault/file]
# Thu, 24 Mar 2022 01:41:51 GMT
EXPOSE 8200
# Thu, 24 Mar 2022 01:41:51 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 24 Mar 2022 01:41:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Mar 2022 01:41:51 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fcd5c91b545b170c3df782b6f4d0fe2cc842f921a444d1f88d4ce4283e77fb`  
		Last Modified: Thu, 24 Mar 2022 01:42:06 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55650c8ff25aea687c7b9ed20f8a6c1c5f7a64797e9f77be32536d3a8b154c5c`  
		Last Modified: Thu, 24 Mar 2022 01:42:15 GMT  
		Size: 71.1 MB (71139845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49389f799b89b1f417ece330364ca79c08d5076386e03eefe19f06698df8cc70`  
		Last Modified: Thu, 24 Mar 2022 01:42:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052166a21f5a3e55f8f3791b0de5b332b3e52986826f9ce7af7a0f8707b6799a`  
		Last Modified: Thu, 24 Mar 2022 01:42:06 GMT  
		Size: 1.8 KB (1811 bytes)  
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
$ docker pull vault@sha256:c0e7ef35040b72ecd41fad1582a8e5e6746302c4c37bd1820d7b51ef0dc8bf79
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69005318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66d19936bb9c4bfac3fb587bb214d394314643156bac17bd3173253dbbdfbc8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 05:01:19 GMT
ARG VAULT_VERSION=1.10.0
# Thu, 24 Mar 2022 05:01:20 GMT
# ARGS: VAULT_VERSION=1.10.0
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 24 Mar 2022 05:01:28 GMT
# ARGS: VAULT_VERSION=1.10.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 24 Mar 2022 05:01:28 GMT
# ARGS: VAULT_VERSION=1.10.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 24 Mar 2022 05:01:29 GMT
VOLUME [/vault/logs]
# Thu, 24 Mar 2022 05:01:30 GMT
VOLUME [/vault/file]
# Thu, 24 Mar 2022 05:01:31 GMT
EXPOSE 8200
# Thu, 24 Mar 2022 05:01:33 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 24 Mar 2022 05:01:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Mar 2022 05:01:34 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0345d45f88ab1581e59610ee7c3e1fbcb18f0beca6c2ec3d38a6733d67be18`  
		Last Modified: Thu, 24 Mar 2022 05:02:04 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fbb2bd104f22a3cb2409e54521d5aaec2ec7681a992f0004725d35d017f8bf6`  
		Last Modified: Thu, 24 Mar 2022 05:02:12 GMT  
		Size: 66.3 MB (66286221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47eb2ed54a038e4f717ec7137afd45e52641967887e587ce919e9735ca1a4457`  
		Last Modified: Thu, 24 Mar 2022 05:02:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf50cb4d3613ef3733ece941d45994af7db2c98041f10b459f8a306d5495531`  
		Last Modified: Thu, 24 Mar 2022 05:02:04 GMT  
		Size: 1.8 KB (1814 bytes)  
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
