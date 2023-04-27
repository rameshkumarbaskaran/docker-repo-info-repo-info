<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `vault`

-	[`vault:1.10.11`](#vault11011)
-	[`vault:1.11.10`](#vault11110)
-	[`vault:1.12.6`](#vault1126)
-	[`vault:1.13.2`](#vault1132)
-	[`vault:latest`](#vaultlatest)

## `vault:1.10.11`

```console
$ docker pull vault@sha256:50d5bd215f38ba19c81dc79c0fa7a4af7f07f9138dcef7a48e80cb0baeb5c15f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.10.11` - linux; amd64

```console
$ docker pull vault@sha256:75d3f21a85bf56090b6618f69b5f5f26e28ba53a4143600304d7a45d801505db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.3 MB (85316786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b809bc2115c80c225ea47c43f07497ad2ad7df8d518646409ec94da84f7cf92d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:37 GMT
ADD file:9663235f252e072c52b0f9e25845841e4321cce2caa7467a0d736c6003b05c00 in / 
# Wed, 29 Mar 2023 18:19:37 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 02:09:40 GMT
ARG VAULT_VERSION=1.10.11
# Thu, 30 Mar 2023 02:09:40 GMT
# ARGS: VAULT_VERSION=1.10.11
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 30 Mar 2023 02:09:48 GMT
# ARGS: VAULT_VERSION=1.10.11
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 30 Mar 2023 02:09:49 GMT
# ARGS: VAULT_VERSION=1.10.11
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 30 Mar 2023 02:09:49 GMT
VOLUME [/vault/logs]
# Thu, 30 Mar 2023 02:09:49 GMT
VOLUME [/vault/file]
# Thu, 30 Mar 2023 02:09:49 GMT
EXPOSE 8200
# Thu, 30 Mar 2023 02:09:49 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 30 Mar 2023 02:09:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Mar 2023 02:09:49 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:f7dab3ab2d6ec29aa28769bec35331fb485b5837501b1e8556413d8b5a79c9c8`  
		Last Modified: Wed, 29 Mar 2023 18:20:25 GMT  
		Size: 2.8 MB (2829647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a595cb706262d9ad4495290dbbee803e36483e0f8b0d65ed7294857e83cc7230`  
		Last Modified: Thu, 30 Mar 2023 02:10:44 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f98402efd4abc517916cab9d37d4dffa310fbe5493f03d4ed76141d33224c1`  
		Last Modified: Thu, 30 Mar 2023 02:10:53 GMT  
		Size: 82.5 MB (82483870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f0e2518f957cd7642dfae1aa486be2529cdde2144a32377280e87c7aa19daf`  
		Last Modified: Thu, 30 Mar 2023 02:10:45 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1adb5c23e4fa3350eb9c6b0956847253ad627f414d46c568e710f5098ec3da47`  
		Last Modified: Thu, 30 Mar 2023 02:10:44 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.10.11` - linux; arm variant v6

```console
$ docker pull vault@sha256:906dcbae9aaba8ccf17dc95d9f677ed4c5f24067c41301065fb1b8d1a6bb4e66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.4 MB (80432324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b6c49afcd39e5f79f60f2f6f7adc4211a74de6185f4e70adc446cd80b20fb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:15 GMT
ADD file:1039802413c644346f599dac53a7c6dabd123027756231b9d8f64a1068c9779d in / 
# Wed, 29 Mar 2023 18:01:15 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 00:36:39 GMT
ARG VAULT_VERSION=1.10.11
# Thu, 30 Mar 2023 00:36:40 GMT
# ARGS: VAULT_VERSION=1.10.11
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 30 Mar 2023 00:36:50 GMT
# ARGS: VAULT_VERSION=1.10.11
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 30 Mar 2023 00:36:51 GMT
# ARGS: VAULT_VERSION=1.10.11
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 30 Mar 2023 00:36:51 GMT
VOLUME [/vault/logs]
# Thu, 30 Mar 2023 00:36:51 GMT
VOLUME [/vault/file]
# Thu, 30 Mar 2023 00:36:51 GMT
EXPOSE 8200
# Thu, 30 Mar 2023 00:36:51 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 30 Mar 2023 00:36:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Mar 2023 00:36:51 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:ffeb76b9ee2f52d46487f4f9a7074ea62dea819a2dd53c9a2c6d703ca7b5aa06`  
		Last Modified: Wed, 29 Mar 2023 18:02:21 GMT  
		Size: 2.6 MB (2638259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97278dfb127bd4709df09cdd936a6ab3af4c9d2d2dd3e25a7bd1c5b0b634608a`  
		Last Modified: Thu, 30 Mar 2023 23:51:07 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2281f965dc065abfa35c2fc06bd03df4bd56f2297d4d98dcd289398626901f3c`  
		Last Modified: Thu, 30 Mar 2023 23:51:16 GMT  
		Size: 77.8 MB (77790799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552a5bfae99f19c489b29955c5c28990f94b437d83f4ed55b7f32850fbd87f90`  
		Last Modified: Thu, 30 Mar 2023 23:51:07 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a3329135580172f19bcfc9aee00870ae87e490d8511bbce4645f074de4cb99`  
		Last Modified: Thu, 30 Mar 2023 23:51:07 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.10.11` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:640bab2894464de6520fc3fd7eff6b27a0afa35aa64ffaa31454d3d525312667
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.4 MB (80433961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1561994ce7554b6e098bcf471073761381ff00f486b3404083242656a8616706`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:25 GMT
ADD file:c3d52cc254959a9ff493e7347e6b1bc25c0ccfdcf9532dbf43173ddd182d0e4d in / 
# Wed, 29 Mar 2023 17:39:25 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 03:29:18 GMT
ARG VAULT_VERSION=1.10.11
# Thu, 30 Mar 2023 03:29:18 GMT
# ARGS: VAULT_VERSION=1.10.11
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 30 Mar 2023 03:29:26 GMT
# ARGS: VAULT_VERSION=1.10.11
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 30 Mar 2023 03:29:28 GMT
# ARGS: VAULT_VERSION=1.10.11
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 30 Mar 2023 03:29:28 GMT
VOLUME [/vault/logs]
# Thu, 30 Mar 2023 03:29:28 GMT
VOLUME [/vault/file]
# Thu, 30 Mar 2023 03:29:28 GMT
EXPOSE 8200
# Thu, 30 Mar 2023 03:29:28 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 30 Mar 2023 03:29:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Mar 2023 03:29:28 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:422ed46b1a92579f7c475c0c19fade6880a8d98f23a2b4ccfb77c265d4f72dfc`  
		Last Modified: Wed, 29 Mar 2023 17:40:13 GMT  
		Size: 2.7 MB (2725148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da0f19ec15f778ed9e8591fff8d298a3e6198c19c9acc840b8bb6c4cc9353a85`  
		Last Modified: Thu, 30 Mar 2023 03:30:15 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aace7303cdb787ab8d7ef93516a0e2bcd4826fd0caaa2ec81884a37d6586d3f`  
		Last Modified: Thu, 30 Mar 2023 03:30:22 GMT  
		Size: 77.7 MB (77705543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28cab760b48c2c74483d454fdd28fdbc4f4ea243f804f0cda25834aef171eeed`  
		Last Modified: Thu, 30 Mar 2023 03:30:16 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c263c747704609fd576d2cf4b944e0bc5ffd0ac0dc60b84ba2131be6f600e143`  
		Last Modified: Thu, 30 Mar 2023 03:30:16 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.10.11` - linux; 386

```console
$ docker pull vault@sha256:5e4beab006468875f48feed52015fd23cd6fb5b6861a478ef8f5223177210af3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.1 MB (82076916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c374289237b520251a9f980537c841e6b0dbf8219f3e61f2fb9f51873cc7c388`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:38 GMT
ADD file:0fbd9a88e784719a5d50377c069ea125f9a27568d6d02b43a9512c65ae72870d in / 
# Wed, 29 Mar 2023 17:38:39 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 01:40:02 GMT
ARG VAULT_VERSION=1.10.11
# Thu, 30 Mar 2023 01:40:03 GMT
# ARGS: VAULT_VERSION=1.10.11
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 30 Mar 2023 01:40:12 GMT
# ARGS: VAULT_VERSION=1.10.11
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 30 Mar 2023 01:40:14 GMT
# ARGS: VAULT_VERSION=1.10.11
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 30 Mar 2023 01:40:14 GMT
VOLUME [/vault/logs]
# Thu, 30 Mar 2023 01:40:14 GMT
VOLUME [/vault/file]
# Thu, 30 Mar 2023 01:40:14 GMT
EXPOSE 8200
# Thu, 30 Mar 2023 01:40:14 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 30 Mar 2023 01:40:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Mar 2023 01:40:14 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:ebcdc7813a6f23dca055a9257561eabd5fc5c5c21d7a72bb208439bd92f47f70`  
		Last Modified: Wed, 29 Mar 2023 17:39:28 GMT  
		Size: 2.8 MB (2835200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa6b106cb9fa6d8655cfc1069b3cca334dc0e00866a45c769f0183009174685c`  
		Last Modified: Thu, 30 Mar 2023 01:41:15 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8617e2641ad7e45255e4cc0c48c0bd042ad1ff40559be20734eeb89f946a8b34`  
		Last Modified: Thu, 30 Mar 2023 01:41:27 GMT  
		Size: 79.2 MB (79238453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130e603b6b6e6cf25d315c89244a3ab01f64e41665e7e68e1aba80d08f0be7b8`  
		Last Modified: Thu, 30 Mar 2023 01:41:15 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb234f1b29d32a5d33e570a1afcd3d171d020dae3141cba4e212943052eae796`  
		Last Modified: Thu, 30 Mar 2023 01:41:15 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.11.10`

```console
$ docker pull vault@sha256:44312ba88303f97e7937d5b360787702a203cdde37f0b181ddcba16d271a6d51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.11.10` - linux; amd64

```console
$ docker pull vault@sha256:f59b37b2390b17938d228b8b8d6350e9e9fe163fd2853c6865c52dcbaf090c0c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81278081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3269ab5d08bcfda88d5afe987bfb87e34127008f357af67c2b7b9c87a0224b42`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:37 GMT
ADD file:9663235f252e072c52b0f9e25845841e4321cce2caa7467a0d736c6003b05c00 in / 
# Wed, 29 Mar 2023 18:19:37 GMT
CMD ["/bin/sh"]
# Thu, 27 Apr 2023 19:22:41 GMT
ARG VAULT_VERSION=1.11.10
# Thu, 27 Apr 2023 19:22:42 GMT
# ARGS: VAULT_VERSION=1.11.10
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 27 Apr 2023 19:22:49 GMT
# ARGS: VAULT_VERSION=1.11.10
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 27 Apr 2023 19:22:50 GMT
# ARGS: VAULT_VERSION=1.11.10
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 27 Apr 2023 19:22:50 GMT
VOLUME [/vault/logs]
# Thu, 27 Apr 2023 19:22:50 GMT
VOLUME [/vault/file]
# Thu, 27 Apr 2023 19:22:50 GMT
EXPOSE 8200
# Thu, 27 Apr 2023 19:22:50 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 27 Apr 2023 19:22:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Apr 2023 19:22:50 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:f7dab3ab2d6ec29aa28769bec35331fb485b5837501b1e8556413d8b5a79c9c8`  
		Last Modified: Wed, 29 Mar 2023 18:20:25 GMT  
		Size: 2.8 MB (2829647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3aed1f80c837b94294b42a9d6e3e4d312ca56e855bb69d06bdd5345e2f6b39`  
		Last Modified: Thu, 27 Apr 2023 19:23:33 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd80ef16ca6284e43ab6a23307870b12516ed5d0756dd231ef745e4dcf2c54d4`  
		Last Modified: Thu, 27 Apr 2023 19:23:41 GMT  
		Size: 78.4 MB (78445163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd870711099bd5e60f50e2005eaf9b75bf0cf94aa53bf6885770051827dd7bf9`  
		Last Modified: Thu, 27 Apr 2023 19:23:33 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6b48e42e33c13e625f13116a1f5bc30b5137afe76d0f49abd76933f5c1f309`  
		Last Modified: Thu, 27 Apr 2023 19:23:33 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.11.10` - linux; arm variant v6

```console
$ docker pull vault@sha256:504605d80b5e069efb61b2103c0ae85c576d0bee63cc58442e87ca9f4b4cd64a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76393889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023fe3ad8a6666d8b90b2a04e2749975e1a7f774def6259770373e5f6fab2768`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:15 GMT
ADD file:1039802413c644346f599dac53a7c6dabd123027756231b9d8f64a1068c9779d in / 
# Wed, 29 Mar 2023 18:01:15 GMT
CMD ["/bin/sh"]
# Thu, 27 Apr 2023 19:49:59 GMT
ARG VAULT_VERSION=1.11.10
# Thu, 27 Apr 2023 19:50:00 GMT
# ARGS: VAULT_VERSION=1.11.10
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 27 Apr 2023 19:50:09 GMT
# ARGS: VAULT_VERSION=1.11.10
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 27 Apr 2023 19:50:10 GMT
# ARGS: VAULT_VERSION=1.11.10
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 27 Apr 2023 19:50:10 GMT
VOLUME [/vault/logs]
# Thu, 27 Apr 2023 19:50:10 GMT
VOLUME [/vault/file]
# Thu, 27 Apr 2023 19:50:10 GMT
EXPOSE 8200
# Thu, 27 Apr 2023 19:50:10 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 27 Apr 2023 19:50:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Apr 2023 19:50:10 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:ffeb76b9ee2f52d46487f4f9a7074ea62dea819a2dd53c9a2c6d703ca7b5aa06`  
		Last Modified: Wed, 29 Mar 2023 18:02:21 GMT  
		Size: 2.6 MB (2638259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f01861775909d434922d5743cbbeef060f614f3617615378dd7d955257db120`  
		Last Modified: Thu, 27 Apr 2023 19:50:59 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed0f8f3bf652f1b756e0d700730f0499392f2d48464f2b347fad95add9ef586`  
		Last Modified: Thu, 27 Apr 2023 19:51:08 GMT  
		Size: 73.8 MB (73752360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ec1a9f631e330a001830e271fc6a3761b40358c09771a533de9f1f4c8c430f`  
		Last Modified: Thu, 27 Apr 2023 19:50:59 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df65ef497b231ead4f7b7264e03e1bea488ddf52498fa18313491c1630228c1`  
		Last Modified: Thu, 27 Apr 2023 19:50:59 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.11.10` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:9ac91de368bb8c0827c0f705d50c2798c25456ff1bd09bb349deaec18603de1c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76556844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78eaa3316371eda69249d6303d46af0efdc379209ebc67cd5fae03e15bc04382`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:25 GMT
ADD file:c3d52cc254959a9ff493e7347e6b1bc25c0ccfdcf9532dbf43173ddd182d0e4d in / 
# Wed, 29 Mar 2023 17:39:25 GMT
CMD ["/bin/sh"]
# Thu, 27 Apr 2023 19:47:26 GMT
ARG VAULT_VERSION=1.11.10
# Thu, 27 Apr 2023 19:47:27 GMT
# ARGS: VAULT_VERSION=1.11.10
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 27 Apr 2023 19:47:34 GMT
# ARGS: VAULT_VERSION=1.11.10
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 27 Apr 2023 19:47:35 GMT
# ARGS: VAULT_VERSION=1.11.10
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 27 Apr 2023 19:47:35 GMT
VOLUME [/vault/logs]
# Thu, 27 Apr 2023 19:47:35 GMT
VOLUME [/vault/file]
# Thu, 27 Apr 2023 19:47:36 GMT
EXPOSE 8200
# Thu, 27 Apr 2023 19:47:36 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 27 Apr 2023 19:47:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Apr 2023 19:47:36 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:422ed46b1a92579f7c475c0c19fade6880a8d98f23a2b4ccfb77c265d4f72dfc`  
		Last Modified: Wed, 29 Mar 2023 17:40:13 GMT  
		Size: 2.7 MB (2725148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba4f28e81c708d567cf5091aef05b4bb386292ab4c5bff42ec8d73714237e35f`  
		Last Modified: Thu, 27 Apr 2023 19:48:12 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972fd115e9747fe7a7d2a4912f9ff31fcb54a5ebb484c775177d1ec1f1a8c013`  
		Last Modified: Thu, 27 Apr 2023 19:48:19 GMT  
		Size: 73.8 MB (73828426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223173dbfdfcd5dc1eda42d316ff83e8bc561cb35f5d8d05153f760a2264a898`  
		Last Modified: Thu, 27 Apr 2023 19:48:12 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf7b8a3b2f190ecd1738124b9ca5bc47fb748ce634ec226b2e024fea5f5911a`  
		Last Modified: Thu, 27 Apr 2023 19:48:12 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.11.10` - linux; 386

```console
$ docker pull vault@sha256:bba8ca22d67ba769816c6ca03bcfc11570c5b53596f7f1c78c4af34825152a9a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78103155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d6ae435a1988681a4b70a784c45dfe8477618a9b460e966d6331fe89788524f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:38 GMT
ADD file:0fbd9a88e784719a5d50377c069ea125f9a27568d6d02b43a9512c65ae72870d in / 
# Wed, 29 Mar 2023 17:38:39 GMT
CMD ["/bin/sh"]
# Thu, 27 Apr 2023 19:38:57 GMT
ARG VAULT_VERSION=1.11.10
# Thu, 27 Apr 2023 19:38:57 GMT
# ARGS: VAULT_VERSION=1.11.10
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 27 Apr 2023 19:39:07 GMT
# ARGS: VAULT_VERSION=1.11.10
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 27 Apr 2023 19:39:08 GMT
# ARGS: VAULT_VERSION=1.11.10
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 27 Apr 2023 19:39:08 GMT
VOLUME [/vault/logs]
# Thu, 27 Apr 2023 19:39:08 GMT
VOLUME [/vault/file]
# Thu, 27 Apr 2023 19:39:09 GMT
EXPOSE 8200
# Thu, 27 Apr 2023 19:39:09 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 27 Apr 2023 19:39:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Apr 2023 19:39:09 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:ebcdc7813a6f23dca055a9257561eabd5fc5c5c21d7a72bb208439bd92f47f70`  
		Last Modified: Wed, 29 Mar 2023 17:39:28 GMT  
		Size: 2.8 MB (2835200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733e3d2729e957176027b8f7ce56896330cc456dda867e1ec3a9cf3549b89a7f`  
		Last Modified: Thu, 27 Apr 2023 19:39:56 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70271108f8096b4178f8bbe66e0b90eca485abbee399b1a99eca55b23041f7eb`  
		Last Modified: Thu, 27 Apr 2023 19:40:06 GMT  
		Size: 75.3 MB (75264682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cfc22d4c0bf3f92b3b2daf8c55f8a074939b5aa49b91c9064bbebe668f1dcd4`  
		Last Modified: Thu, 27 Apr 2023 19:39:56 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17fc67e5dc0869f22f58da564099fba81abd92829e381a4d548c28e1f237f3f2`  
		Last Modified: Thu, 27 Apr 2023 19:39:56 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.12.6`

```console
$ docker pull vault@sha256:dca2d65d52400b70a3e4b809dcafb46cf779682601a11cf7a315ab96315f85d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.12.6` - linux; amd64

```console
$ docker pull vault@sha256:595c183652dfa6b6f12fd3b0caee6b499e84fccbc9de64eea6e89d8fe387ba71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.0 MB (86027460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40000effba873f6dd54b8af17f4a8faaa4084a3146b356054b9b3361bcd4d9ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:37 GMT
ADD file:9663235f252e072c52b0f9e25845841e4321cce2caa7467a0d736c6003b05c00 in / 
# Wed, 29 Mar 2023 18:19:37 GMT
CMD ["/bin/sh"]
# Thu, 27 Apr 2023 19:22:27 GMT
ARG VAULT_VERSION=1.12.6
# Thu, 27 Apr 2023 19:22:28 GMT
# ARGS: VAULT_VERSION=1.12.6
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 27 Apr 2023 19:22:36 GMT
# ARGS: VAULT_VERSION=1.12.6
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 27 Apr 2023 19:22:37 GMT
# ARGS: VAULT_VERSION=1.12.6
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 27 Apr 2023 19:22:37 GMT
VOLUME [/vault/logs]
# Thu, 27 Apr 2023 19:22:37 GMT
VOLUME [/vault/file]
# Thu, 27 Apr 2023 19:22:37 GMT
EXPOSE 8200
# Thu, 27 Apr 2023 19:22:37 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 27 Apr 2023 19:22:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Apr 2023 19:22:37 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:f7dab3ab2d6ec29aa28769bec35331fb485b5837501b1e8556413d8b5a79c9c8`  
		Last Modified: Wed, 29 Mar 2023 18:20:25 GMT  
		Size: 2.8 MB (2829647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c73755ecc16cd7ca70252b262b18eebe558ee7727c1b33715eb3f1eb267ae04b`  
		Last Modified: Thu, 27 Apr 2023 19:23:18 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9c75b93f6f7213a76a04a69b3c32bee9cf5101099ea858667c925f396a6d17`  
		Last Modified: Thu, 27 Apr 2023 19:23:27 GMT  
		Size: 83.2 MB (83194543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee0a3c255bf8baf2ff4c48023568021dc44e33a9cab00486fefdeab6c09252b`  
		Last Modified: Thu, 27 Apr 2023 19:23:18 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b970b4689c0a435241b26048a5adac862aef4711388381ea9886fc34149c557`  
		Last Modified: Thu, 27 Apr 2023 19:23:18 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.12.6` - linux; arm variant v6

```console
$ docker pull vault@sha256:be5687cd7b6b605231c51f6e66cac24dbd4359bd07b9d68f2a6d1e4f6d1b159e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80749367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6822ab6589fcd56d88d1ab81203cdc9373fd22248f1029b0460460a624ff01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:15 GMT
ADD file:1039802413c644346f599dac53a7c6dabd123027756231b9d8f64a1068c9779d in / 
# Wed, 29 Mar 2023 18:01:15 GMT
CMD ["/bin/sh"]
# Thu, 27 Apr 2023 19:49:46 GMT
ARG VAULT_VERSION=1.12.6
# Thu, 27 Apr 2023 19:49:46 GMT
# ARGS: VAULT_VERSION=1.12.6
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 27 Apr 2023 19:49:56 GMT
# ARGS: VAULT_VERSION=1.12.6
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 27 Apr 2023 19:49:57 GMT
# ARGS: VAULT_VERSION=1.12.6
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 27 Apr 2023 19:49:58 GMT
VOLUME [/vault/logs]
# Thu, 27 Apr 2023 19:49:58 GMT
VOLUME [/vault/file]
# Thu, 27 Apr 2023 19:49:58 GMT
EXPOSE 8200
# Thu, 27 Apr 2023 19:49:58 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 27 Apr 2023 19:49:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Apr 2023 19:49:58 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:ffeb76b9ee2f52d46487f4f9a7074ea62dea819a2dd53c9a2c6d703ca7b5aa06`  
		Last Modified: Wed, 29 Mar 2023 18:02:21 GMT  
		Size: 2.6 MB (2638259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a13de55932cd4f2d41d3047f402bfc3c7a9e51cc5cdf44e43cffda4bf2e55f`  
		Last Modified: Thu, 27 Apr 2023 19:50:40 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d87473584171c17793353557f796767841f5ac5aeeae06018bc15f9ea57d37`  
		Last Modified: Thu, 27 Apr 2023 19:50:52 GMT  
		Size: 78.1 MB (78107837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c05c3ba0e395e5674d5cbd056154d67ca4f5b0eaebcba90ca7fc5c596b4549ed`  
		Last Modified: Thu, 27 Apr 2023 19:50:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e71efdbb9b13523d95be1b32b8d0567a9d3af45cc5166c128dc52496c1273fc`  
		Last Modified: Thu, 27 Apr 2023 19:50:40 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.12.6` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:dbfbd2238e4ed32f929f73612c5bcbd0ae523e30fb334ee0c78983a36fec5454
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81067889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd142bbb186a886df0a9ff422d433fd636a1bfa58db3b27dbb485c58e7870aa2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:25 GMT
ADD file:c3d52cc254959a9ff493e7347e6b1bc25c0ccfdcf9532dbf43173ddd182d0e4d in / 
# Wed, 29 Mar 2023 17:39:25 GMT
CMD ["/bin/sh"]
# Thu, 27 Apr 2023 19:47:13 GMT
ARG VAULT_VERSION=1.12.6
# Thu, 27 Apr 2023 19:47:14 GMT
# ARGS: VAULT_VERSION=1.12.6
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 27 Apr 2023 19:47:22 GMT
# ARGS: VAULT_VERSION=1.12.6
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 27 Apr 2023 19:47:23 GMT
# ARGS: VAULT_VERSION=1.12.6
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 27 Apr 2023 19:47:23 GMT
VOLUME [/vault/logs]
# Thu, 27 Apr 2023 19:47:23 GMT
VOLUME [/vault/file]
# Thu, 27 Apr 2023 19:47:23 GMT
EXPOSE 8200
# Thu, 27 Apr 2023 19:47:23 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 27 Apr 2023 19:47:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Apr 2023 19:47:24 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:422ed46b1a92579f7c475c0c19fade6880a8d98f23a2b4ccfb77c265d4f72dfc`  
		Last Modified: Wed, 29 Mar 2023 17:40:13 GMT  
		Size: 2.7 MB (2725148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a84ca6a39328a56668bfc4a89e85c018d3c4a8d3e46e5036a57f7a48d860f7`  
		Last Modified: Thu, 27 Apr 2023 19:48:00 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d9f62c75b9c07c2a954d7eac763bd07c5c4b4931216cc6adbb1b1090207e04`  
		Last Modified: Thu, 27 Apr 2023 19:48:06 GMT  
		Size: 78.3 MB (78339471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914ac04622349acd3638d58d1b63241b2e29047e25f7acdd8a9215f344d64b57`  
		Last Modified: Thu, 27 Apr 2023 19:48:00 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837f67bd522507aac1c4e1f8c1eda4d61c94052060d4cc69ddbc4de3a93985b1`  
		Last Modified: Thu, 27 Apr 2023 19:48:00 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.12.6` - linux; 386

```console
$ docker pull vault@sha256:054aedb45f9032938e8d14396d452c99f7aef73895ed97e2eab7905867061ebc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82478635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9700e2ff70a633083b6a6cd6b582c84b43060fcfa8de66816b601edf9bd4be77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:38 GMT
ADD file:0fbd9a88e784719a5d50377c069ea125f9a27568d6d02b43a9512c65ae72870d in / 
# Wed, 29 Mar 2023 17:38:39 GMT
CMD ["/bin/sh"]
# Thu, 27 Apr 2023 19:38:43 GMT
ARG VAULT_VERSION=1.12.6
# Thu, 27 Apr 2023 19:38:44 GMT
# ARGS: VAULT_VERSION=1.12.6
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 27 Apr 2023 19:38:54 GMT
# ARGS: VAULT_VERSION=1.12.6
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 27 Apr 2023 19:38:55 GMT
# ARGS: VAULT_VERSION=1.12.6
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 27 Apr 2023 19:38:55 GMT
VOLUME [/vault/logs]
# Thu, 27 Apr 2023 19:38:55 GMT
VOLUME [/vault/file]
# Thu, 27 Apr 2023 19:38:55 GMT
EXPOSE 8200
# Thu, 27 Apr 2023 19:38:55 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 27 Apr 2023 19:38:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Apr 2023 19:38:55 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:ebcdc7813a6f23dca055a9257561eabd5fc5c5c21d7a72bb208439bd92f47f70`  
		Last Modified: Wed, 29 Mar 2023 17:39:28 GMT  
		Size: 2.8 MB (2835200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2735d42fe3fe32bb4b1777a62a29009f758952995ec37243c5f2da4f6a201b`  
		Last Modified: Thu, 27 Apr 2023 19:39:38 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a1c2dc148a7b42a504762fd72f39f938d543e55ad7707d9dee9089234b431b`  
		Last Modified: Thu, 27 Apr 2023 19:39:50 GMT  
		Size: 79.6 MB (79640166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb34db1b876fd72a455d43202e8973ec42f5c226ed2869bf5e344254fe926c3`  
		Last Modified: Thu, 27 Apr 2023 19:39:38 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231d0b9ee4047303e6482eec8c9aa59edd696265070c07a4d5eacc0e97d1bc43`  
		Last Modified: Thu, 27 Apr 2023 19:39:38 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.13.2`

```console
$ docker pull vault@sha256:eb910358ab988d1f132fbe67869f3a5e63e210f9a4d97dfbb4929a4922ede421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.13.2` - linux; amd64

```console
$ docker pull vault@sha256:472e3f23f87d3b342e192040032a5b180c71b5a79ef74fc3597ab9d6f7af19b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52944948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa9c3f0708d01b46c50683d6f12dee2f1573e2dfc8e290142bfb1392c0245a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:37 GMT
ADD file:9663235f252e072c52b0f9e25845841e4321cce2caa7467a0d736c6003b05c00 in / 
# Wed, 29 Mar 2023 18:19:37 GMT
CMD ["/bin/sh"]
# Thu, 27 Apr 2023 19:22:16 GMT
ARG VAULT_VERSION=1.13.2
# Thu, 27 Apr 2023 19:22:16 GMT
# ARGS: VAULT_VERSION=1.13.2
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 27 Apr 2023 19:22:23 GMT
# ARGS: VAULT_VERSION=1.13.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 27 Apr 2023 19:22:24 GMT
# ARGS: VAULT_VERSION=1.13.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 27 Apr 2023 19:22:24 GMT
VOLUME [/vault/logs]
# Thu, 27 Apr 2023 19:22:24 GMT
VOLUME [/vault/file]
# Thu, 27 Apr 2023 19:22:24 GMT
EXPOSE 8200
# Thu, 27 Apr 2023 19:22:24 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 27 Apr 2023 19:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Apr 2023 19:22:24 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:f7dab3ab2d6ec29aa28769bec35331fb485b5837501b1e8556413d8b5a79c9c8`  
		Last Modified: Wed, 29 Mar 2023 18:20:25 GMT  
		Size: 2.8 MB (2829647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5c87a2b3cf5178bb2b01489a0896610aa75b4d74d827a75ebe1c1f6220ffe0`  
		Last Modified: Thu, 27 Apr 2023 19:23:02 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e09e6dc12b97e85b5509f1ab3022ab16868d9dd0f9595f65c26d12446c870c0`  
		Last Modified: Thu, 27 Apr 2023 19:23:09 GMT  
		Size: 50.1 MB (50112033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b003dccbe77bf2dccff4024e42e4b8504aedfe3efc81e8500005e073e38ad2a`  
		Last Modified: Thu, 27 Apr 2023 19:23:02 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640451d14d72c74b1eed8c79a3009ef61474533c2480cf15d0c69ba939cd4a15`  
		Last Modified: Thu, 27 Apr 2023 19:23:02 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.13.2` - linux; arm variant v6

```console
$ docker pull vault@sha256:ad2d30d1ab890817b09020d72cbbcfff38d9443c073750a1aca2799c1a45a30f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50025624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046ce76f70c01101780912889feb12748f64f62462d9607568222f178cf62ef2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:15 GMT
ADD file:1039802413c644346f599dac53a7c6dabd123027756231b9d8f64a1068c9779d in / 
# Wed, 29 Mar 2023 18:01:15 GMT
CMD ["/bin/sh"]
# Thu, 27 Apr 2023 19:49:27 GMT
ARG VAULT_VERSION=1.13.2
# Thu, 27 Apr 2023 19:49:27 GMT
# ARGS: VAULT_VERSION=1.13.2
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 27 Apr 2023 19:49:42 GMT
# ARGS: VAULT_VERSION=1.13.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 27 Apr 2023 19:49:43 GMT
# ARGS: VAULT_VERSION=1.13.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 27 Apr 2023 19:49:43 GMT
VOLUME [/vault/logs]
# Thu, 27 Apr 2023 19:49:43 GMT
VOLUME [/vault/file]
# Thu, 27 Apr 2023 19:49:43 GMT
EXPOSE 8200
# Thu, 27 Apr 2023 19:49:44 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 27 Apr 2023 19:49:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Apr 2023 19:49:44 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:ffeb76b9ee2f52d46487f4f9a7074ea62dea819a2dd53c9a2c6d703ca7b5aa06`  
		Last Modified: Wed, 29 Mar 2023 18:02:21 GMT  
		Size: 2.6 MB (2638259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81cd9319c9e96c0d74a2f37945c7a6ebeefd3afb563225cdd4d6de82637f3a2`  
		Last Modified: Thu, 27 Apr 2023 19:50:21 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811e6ae161b1d746eb72519482618ebd06b08b801cdd606be98b548486f34cd8`  
		Last Modified: Thu, 27 Apr 2023 19:50:30 GMT  
		Size: 47.4 MB (47384095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6b43dd5e88bb79a43ca4940445db5214aac5b59ce19eb374de7109c971ceb3`  
		Last Modified: Thu, 27 Apr 2023 19:50:21 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47987bdff503410a6c7392fb3bd3486e1156e51ea5cff36c8f352719b85bc107`  
		Last Modified: Thu, 27 Apr 2023 19:50:21 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.13.2` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:533b8cc77262ea254a098628dfd9d1d8ca970e2ef07ba79646a5cb4eeb725c28
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48802428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc57a2ad9f154824f52b24424fe2b96518e33cb84be6653b31eb8adea6a55b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:25 GMT
ADD file:c3d52cc254959a9ff493e7347e6b1bc25c0ccfdcf9532dbf43173ddd182d0e4d in / 
# Wed, 29 Mar 2023 17:39:25 GMT
CMD ["/bin/sh"]
# Thu, 27 Apr 2023 19:47:02 GMT
ARG VAULT_VERSION=1.13.2
# Thu, 27 Apr 2023 19:47:03 GMT
# ARGS: VAULT_VERSION=1.13.2
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 27 Apr 2023 19:47:09 GMT
# ARGS: VAULT_VERSION=1.13.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 27 Apr 2023 19:47:10 GMT
# ARGS: VAULT_VERSION=1.13.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 27 Apr 2023 19:47:10 GMT
VOLUME [/vault/logs]
# Thu, 27 Apr 2023 19:47:10 GMT
VOLUME [/vault/file]
# Thu, 27 Apr 2023 19:47:10 GMT
EXPOSE 8200
# Thu, 27 Apr 2023 19:47:10 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 27 Apr 2023 19:47:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Apr 2023 19:47:11 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:422ed46b1a92579f7c475c0c19fade6880a8d98f23a2b4ccfb77c265d4f72dfc`  
		Last Modified: Wed, 29 Mar 2023 17:40:13 GMT  
		Size: 2.7 MB (2725148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e97f0b119a2f5a8e0f00d0890aa69ff142c47ebf09eb894f03d7d05af92db40`  
		Last Modified: Thu, 27 Apr 2023 19:47:47 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce5a2b6799700f279a3dde8c9ff0b95286944146bdd8d725c33f87fa99c4a2c`  
		Last Modified: Thu, 27 Apr 2023 19:47:51 GMT  
		Size: 46.1 MB (46074010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf4649dcb8a3476d927316442beb05516fd44ae8b41408f54ea01445a997348`  
		Last Modified: Thu, 27 Apr 2023 19:47:46 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe1d68cd01d93e81ea286bab38202928cfb045d0db9c3d8954badff60115ab7c`  
		Last Modified: Thu, 27 Apr 2023 19:47:46 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.13.2` - linux; 386

```console
$ docker pull vault@sha256:d8658d8297c41e1735d881821308824a611aed85a9d3ceaab26b4f9c728d5f2a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49636809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:475f47ad2fd5c9054f60a886e2b7391c258b5fb9b87a05a5f4aca998dc628a2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:38 GMT
ADD file:0fbd9a88e784719a5d50377c069ea125f9a27568d6d02b43a9512c65ae72870d in / 
# Wed, 29 Mar 2023 17:38:39 GMT
CMD ["/bin/sh"]
# Thu, 27 Apr 2023 19:38:27 GMT
ARG VAULT_VERSION=1.13.2
# Thu, 27 Apr 2023 19:38:28 GMT
# ARGS: VAULT_VERSION=1.13.2
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 27 Apr 2023 19:38:40 GMT
# ARGS: VAULT_VERSION=1.13.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 27 Apr 2023 19:38:41 GMT
# ARGS: VAULT_VERSION=1.13.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 27 Apr 2023 19:38:41 GMT
VOLUME [/vault/logs]
# Thu, 27 Apr 2023 19:38:41 GMT
VOLUME [/vault/file]
# Thu, 27 Apr 2023 19:38:41 GMT
EXPOSE 8200
# Thu, 27 Apr 2023 19:38:41 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 27 Apr 2023 19:38:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Apr 2023 19:38:42 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:ebcdc7813a6f23dca055a9257561eabd5fc5c5c21d7a72bb208439bd92f47f70`  
		Last Modified: Wed, 29 Mar 2023 17:39:28 GMT  
		Size: 2.8 MB (2835200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ea130633cae1a572c761a4728f37e1df1b2b29b956269149063e5f55dd2f30`  
		Last Modified: Thu, 27 Apr 2023 19:39:21 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84d4d0677d342258cb20902dbecea128eab19360a127859be376bba6b44e635`  
		Last Modified: Thu, 27 Apr 2023 19:39:30 GMT  
		Size: 46.8 MB (46798337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c032fbbf147af3fde561aafac6afc459f9fd1af1c178512ee2b6fdebaaeefd7`  
		Last Modified: Thu, 27 Apr 2023 19:39:21 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f209a2868f1846c7024afab6803c993a1bd711888b19d72dd68b44dc622b418`  
		Last Modified: Thu, 27 Apr 2023 19:39:21 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:latest`

```console
$ docker pull vault@sha256:eb910358ab988d1f132fbe67869f3a5e63e210f9a4d97dfbb4929a4922ede421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:latest` - linux; amd64

```console
$ docker pull vault@sha256:472e3f23f87d3b342e192040032a5b180c71b5a79ef74fc3597ab9d6f7af19b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52944948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa9c3f0708d01b46c50683d6f12dee2f1573e2dfc8e290142bfb1392c0245a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:37 GMT
ADD file:9663235f252e072c52b0f9e25845841e4321cce2caa7467a0d736c6003b05c00 in / 
# Wed, 29 Mar 2023 18:19:37 GMT
CMD ["/bin/sh"]
# Thu, 27 Apr 2023 19:22:16 GMT
ARG VAULT_VERSION=1.13.2
# Thu, 27 Apr 2023 19:22:16 GMT
# ARGS: VAULT_VERSION=1.13.2
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 27 Apr 2023 19:22:23 GMT
# ARGS: VAULT_VERSION=1.13.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 27 Apr 2023 19:22:24 GMT
# ARGS: VAULT_VERSION=1.13.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 27 Apr 2023 19:22:24 GMT
VOLUME [/vault/logs]
# Thu, 27 Apr 2023 19:22:24 GMT
VOLUME [/vault/file]
# Thu, 27 Apr 2023 19:22:24 GMT
EXPOSE 8200
# Thu, 27 Apr 2023 19:22:24 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 27 Apr 2023 19:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Apr 2023 19:22:24 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:f7dab3ab2d6ec29aa28769bec35331fb485b5837501b1e8556413d8b5a79c9c8`  
		Last Modified: Wed, 29 Mar 2023 18:20:25 GMT  
		Size: 2.8 MB (2829647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5c87a2b3cf5178bb2b01489a0896610aa75b4d74d827a75ebe1c1f6220ffe0`  
		Last Modified: Thu, 27 Apr 2023 19:23:02 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e09e6dc12b97e85b5509f1ab3022ab16868d9dd0f9595f65c26d12446c870c0`  
		Last Modified: Thu, 27 Apr 2023 19:23:09 GMT  
		Size: 50.1 MB (50112033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b003dccbe77bf2dccff4024e42e4b8504aedfe3efc81e8500005e073e38ad2a`  
		Last Modified: Thu, 27 Apr 2023 19:23:02 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640451d14d72c74b1eed8c79a3009ef61474533c2480cf15d0c69ba939cd4a15`  
		Last Modified: Thu, 27 Apr 2023 19:23:02 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm variant v6

```console
$ docker pull vault@sha256:ad2d30d1ab890817b09020d72cbbcfff38d9443c073750a1aca2799c1a45a30f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50025624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046ce76f70c01101780912889feb12748f64f62462d9607568222f178cf62ef2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:15 GMT
ADD file:1039802413c644346f599dac53a7c6dabd123027756231b9d8f64a1068c9779d in / 
# Wed, 29 Mar 2023 18:01:15 GMT
CMD ["/bin/sh"]
# Thu, 27 Apr 2023 19:49:27 GMT
ARG VAULT_VERSION=1.13.2
# Thu, 27 Apr 2023 19:49:27 GMT
# ARGS: VAULT_VERSION=1.13.2
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 27 Apr 2023 19:49:42 GMT
# ARGS: VAULT_VERSION=1.13.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 27 Apr 2023 19:49:43 GMT
# ARGS: VAULT_VERSION=1.13.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 27 Apr 2023 19:49:43 GMT
VOLUME [/vault/logs]
# Thu, 27 Apr 2023 19:49:43 GMT
VOLUME [/vault/file]
# Thu, 27 Apr 2023 19:49:43 GMT
EXPOSE 8200
# Thu, 27 Apr 2023 19:49:44 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 27 Apr 2023 19:49:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Apr 2023 19:49:44 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:ffeb76b9ee2f52d46487f4f9a7074ea62dea819a2dd53c9a2c6d703ca7b5aa06`  
		Last Modified: Wed, 29 Mar 2023 18:02:21 GMT  
		Size: 2.6 MB (2638259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81cd9319c9e96c0d74a2f37945c7a6ebeefd3afb563225cdd4d6de82637f3a2`  
		Last Modified: Thu, 27 Apr 2023 19:50:21 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811e6ae161b1d746eb72519482618ebd06b08b801cdd606be98b548486f34cd8`  
		Last Modified: Thu, 27 Apr 2023 19:50:30 GMT  
		Size: 47.4 MB (47384095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6b43dd5e88bb79a43ca4940445db5214aac5b59ce19eb374de7109c971ceb3`  
		Last Modified: Thu, 27 Apr 2023 19:50:21 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47987bdff503410a6c7392fb3bd3486e1156e51ea5cff36c8f352719b85bc107`  
		Last Modified: Thu, 27 Apr 2023 19:50:21 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:533b8cc77262ea254a098628dfd9d1d8ca970e2ef07ba79646a5cb4eeb725c28
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48802428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc57a2ad9f154824f52b24424fe2b96518e33cb84be6653b31eb8adea6a55b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:25 GMT
ADD file:c3d52cc254959a9ff493e7347e6b1bc25c0ccfdcf9532dbf43173ddd182d0e4d in / 
# Wed, 29 Mar 2023 17:39:25 GMT
CMD ["/bin/sh"]
# Thu, 27 Apr 2023 19:47:02 GMT
ARG VAULT_VERSION=1.13.2
# Thu, 27 Apr 2023 19:47:03 GMT
# ARGS: VAULT_VERSION=1.13.2
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 27 Apr 2023 19:47:09 GMT
# ARGS: VAULT_VERSION=1.13.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 27 Apr 2023 19:47:10 GMT
# ARGS: VAULT_VERSION=1.13.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 27 Apr 2023 19:47:10 GMT
VOLUME [/vault/logs]
# Thu, 27 Apr 2023 19:47:10 GMT
VOLUME [/vault/file]
# Thu, 27 Apr 2023 19:47:10 GMT
EXPOSE 8200
# Thu, 27 Apr 2023 19:47:10 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 27 Apr 2023 19:47:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Apr 2023 19:47:11 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:422ed46b1a92579f7c475c0c19fade6880a8d98f23a2b4ccfb77c265d4f72dfc`  
		Last Modified: Wed, 29 Mar 2023 17:40:13 GMT  
		Size: 2.7 MB (2725148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e97f0b119a2f5a8e0f00d0890aa69ff142c47ebf09eb894f03d7d05af92db40`  
		Last Modified: Thu, 27 Apr 2023 19:47:47 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce5a2b6799700f279a3dde8c9ff0b95286944146bdd8d725c33f87fa99c4a2c`  
		Last Modified: Thu, 27 Apr 2023 19:47:51 GMT  
		Size: 46.1 MB (46074010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf4649dcb8a3476d927316442beb05516fd44ae8b41408f54ea01445a997348`  
		Last Modified: Thu, 27 Apr 2023 19:47:46 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe1d68cd01d93e81ea286bab38202928cfb045d0db9c3d8954badff60115ab7c`  
		Last Modified: Thu, 27 Apr 2023 19:47:46 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; 386

```console
$ docker pull vault@sha256:d8658d8297c41e1735d881821308824a611aed85a9d3ceaab26b4f9c728d5f2a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49636809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:475f47ad2fd5c9054f60a886e2b7391c258b5fb9b87a05a5f4aca998dc628a2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:38 GMT
ADD file:0fbd9a88e784719a5d50377c069ea125f9a27568d6d02b43a9512c65ae72870d in / 
# Wed, 29 Mar 2023 17:38:39 GMT
CMD ["/bin/sh"]
# Thu, 27 Apr 2023 19:38:27 GMT
ARG VAULT_VERSION=1.13.2
# Thu, 27 Apr 2023 19:38:28 GMT
# ARGS: VAULT_VERSION=1.13.2
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 27 Apr 2023 19:38:40 GMT
# ARGS: VAULT_VERSION=1.13.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 27 Apr 2023 19:38:41 GMT
# ARGS: VAULT_VERSION=1.13.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 27 Apr 2023 19:38:41 GMT
VOLUME [/vault/logs]
# Thu, 27 Apr 2023 19:38:41 GMT
VOLUME [/vault/file]
# Thu, 27 Apr 2023 19:38:41 GMT
EXPOSE 8200
# Thu, 27 Apr 2023 19:38:41 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 27 Apr 2023 19:38:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Apr 2023 19:38:42 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:ebcdc7813a6f23dca055a9257561eabd5fc5c5c21d7a72bb208439bd92f47f70`  
		Last Modified: Wed, 29 Mar 2023 17:39:28 GMT  
		Size: 2.8 MB (2835200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ea130633cae1a572c761a4728f37e1df1b2b29b956269149063e5f55dd2f30`  
		Last Modified: Thu, 27 Apr 2023 19:39:21 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84d4d0677d342258cb20902dbecea128eab19360a127859be376bba6b44e635`  
		Last Modified: Thu, 27 Apr 2023 19:39:30 GMT  
		Size: 46.8 MB (46798337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c032fbbf147af3fde561aafac6afc459f9fd1af1c178512ee2b6fdebaaeefd7`  
		Last Modified: Thu, 27 Apr 2023 19:39:21 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f209a2868f1846c7024afab6803c993a1bd711888b19d72dd68b44dc622b418`  
		Last Modified: Thu, 27 Apr 2023 19:39:21 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
