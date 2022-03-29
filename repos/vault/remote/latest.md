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
