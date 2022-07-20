<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `vault`

-	[`vault:1.10.4`](#vault1104)
-	[`vault:1.11.0`](#vault1110)
-	[`vault:1.8.12`](#vault1812)
-	[`vault:1.9.7`](#vault197)
-	[`vault:latest`](#vaultlatest)

## `vault:1.10.4`

```console
$ docker pull vault@sha256:e57dca891ccc5f6d553d39956f5e0ab5f4c8f93cfb9262c46395b02ae1404ca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.10.4` - linux; amd64

```console
$ docker pull vault@sha256:8151c48c182a8da1f27c419fe637ac2e037414a2ccbe8f78bfccb90991ddc681
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74052131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb60aaf6d8e49669d28db1a770f537278138f910ecfe0016eb118f186caff726`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:18 GMT
ADD file:80b46be2fe86b402518b00758ff5d8556d92113dc267a002b6c72a5f9c6742a3 in / 
# Tue, 19 Jul 2022 22:20:18 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 02:03:14 GMT
ARG VAULT_VERSION=1.10.4
# Wed, 20 Jul 2022 02:03:14 GMT
# ARGS: VAULT_VERSION=1.10.4
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 20 Jul 2022 02:03:22 GMT
# ARGS: VAULT_VERSION=1.10.4
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 20 Jul 2022 02:03:23 GMT
# ARGS: VAULT_VERSION=1.10.4
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 20 Jul 2022 02:03:23 GMT
VOLUME [/vault/logs]
# Wed, 20 Jul 2022 02:03:23 GMT
VOLUME [/vault/file]
# Wed, 20 Jul 2022 02:03:23 GMT
EXPOSE 8200
# Wed, 20 Jul 2022 02:03:23 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 20 Jul 2022 02:03:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Jul 2022 02:03:23 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:decfdc335d9bae9ca06166e1a4fc2cdf8c2344a42d85c8a1d3f964aab59ecff5`  
		Last Modified: Tue, 19 Jul 2022 22:20:55 GMT  
		Size: 2.8 MB (2818512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7870ba8da11395af2cba36c662ded76d0e872eddc670986fd5ce0b3321fcc1e0`  
		Last Modified: Wed, 20 Jul 2022 02:04:18 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd5763a0789a9cf2911bba88e8912277fb01c08a63b6bd2b8ee833cea05a303`  
		Last Modified: Wed, 20 Jul 2022 02:04:27 GMT  
		Size: 71.2 MB (71230352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a016affbe794bae2673d1cb4394102e0eecf1ca00a082a2427a54e021d39a7c4`  
		Last Modified: Wed, 20 Jul 2022 02:04:18 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6f8290c0ee8e98ccb25019c71754890a0e7d25e068c85cab1ab81b1fadc7a1`  
		Last Modified: Wed, 20 Jul 2022 02:04:18 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.10.4` - linux; arm variant v6

```console
$ docker pull vault@sha256:764f075252b60cb5ea09c33c0aa9739599aa8422f781eae08cfe474b999c3677
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.3 MB (67334395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd0b7fed9555e5596dbd9e8fd6e8a507bc533346d964b587038b07d0897cd4c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:55 GMT
ADD file:2e4db0cea3f5eecfbb82c5abd09eb100749fed0189fc30d2c51980d2560e3ccb in / 
# Mon, 04 Apr 2022 23:49:56 GMT
CMD ["/bin/sh"]
# Mon, 13 Jun 2022 17:54:54 GMT
ARG VAULT_VERSION=1.10.4
# Mon, 13 Jun 2022 17:54:56 GMT
# ARGS: VAULT_VERSION=1.10.4
RUN addgroup vault &&     adduser -S -G vault vault
# Mon, 13 Jun 2022 17:55:13 GMT
# ARGS: VAULT_VERSION=1.10.4
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Mon, 13 Jun 2022 17:55:15 GMT
# ARGS: VAULT_VERSION=1.10.4
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Mon, 13 Jun 2022 17:55:16 GMT
VOLUME [/vault/logs]
# Mon, 13 Jun 2022 17:55:16 GMT
VOLUME [/vault/file]
# Mon, 13 Jun 2022 17:55:17 GMT
EXPOSE 8200
# Mon, 13 Jun 2022 17:55:17 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 13 Jun 2022 17:55:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jun 2022 17:55:18 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:f9f2e4e531ad51ee917e8311e91a223a4893c1d754acb8246af87375ea60c6aa`  
		Last Modified: Mon, 04 Apr 2022 23:51:47 GMT  
		Size: 2.6 MB (2626056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768193988085f0299c2c56bff8505bafc8e7ef254178c023311a91f9fb5400b6`  
		Last Modified: Mon, 13 Jun 2022 17:57:54 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e76c4e81347d8848a6cc055156b657ea7387369c8fce1fffb2cdc495f4a9070`  
		Last Modified: Mon, 13 Jun 2022 17:58:32 GMT  
		Size: 64.7 MB (64705073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2d524ba77680ee349468953b499c602e499884db91375c0a435df02591073e`  
		Last Modified: Mon, 13 Jun 2022 17:57:55 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4e405e281407fc2bdfcc09a4feeadf0fa82d04df527f6a6616bb14bb8cc58d`  
		Last Modified: Mon, 13 Jun 2022 17:57:55 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.10.4` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:02ac21617aa273224711d6c6abf40b1dbb44d39628215501fb3157c2c6974250
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69101307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd479fe8703857bad69d68f40432f17834172ae53e39507ed1b46c8af4df4ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Mon, 13 Jun 2022 18:16:36 GMT
ARG VAULT_VERSION=1.10.4
# Mon, 13 Jun 2022 18:16:37 GMT
# ARGS: VAULT_VERSION=1.10.4
RUN addgroup vault &&     adduser -S -G vault vault
# Mon, 13 Jun 2022 18:16:44 GMT
# ARGS: VAULT_VERSION=1.10.4
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Mon, 13 Jun 2022 18:16:45 GMT
# ARGS: VAULT_VERSION=1.10.4
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Mon, 13 Jun 2022 18:16:46 GMT
VOLUME [/vault/logs]
# Mon, 13 Jun 2022 18:16:47 GMT
VOLUME [/vault/file]
# Mon, 13 Jun 2022 18:16:48 GMT
EXPOSE 8200
# Mon, 13 Jun 2022 18:16:50 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 13 Jun 2022 18:16:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jun 2022 18:16:51 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1506755f7238e40d0f86f538246192225b4d68cd22ed8e18cb1d264e244f6e61`  
		Last Modified: Mon, 13 Jun 2022 18:18:10 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1935b8650f6f5d196ab7114ad31bc9b922a984b417e3f71551291782f267bfdf`  
		Last Modified: Mon, 13 Jun 2022 18:18:19 GMT  
		Size: 66.4 MB (66380713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7b94a32356ab47070ebff58e82c3b71c99ef66e7771c6758b157b8ef217a76`  
		Last Modified: Mon, 13 Jun 2022 18:18:10 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0866c6bdd34f367391c3914133395d61df7fcc9830ed130b1cb6061c41a84f67`  
		Last Modified: Mon, 13 Jun 2022 18:18:10 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.10.4` - linux; 386

```console
$ docker pull vault@sha256:2bccee85e590f72bf6f2e1927fc1dbeab86dd74fc54d9c7ff27ada913e087839
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70416643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e770d044763d8e3ccab6d2d35fda3c07c77adf27318c256ff4a052d84e333c7b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 19 Jul 2022 22:38:40 GMT
ADD file:4ae4391bf852a3e83cff6c0baebf0241d4955d580e24c180f882a142e4adaf1d in / 
# Tue, 19 Jul 2022 22:38:40 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 02:28:52 GMT
ARG VAULT_VERSION=1.10.4
# Wed, 20 Jul 2022 02:28:53 GMT
# ARGS: VAULT_VERSION=1.10.4
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 20 Jul 2022 02:29:03 GMT
# ARGS: VAULT_VERSION=1.10.4
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 20 Jul 2022 02:29:03 GMT
# ARGS: VAULT_VERSION=1.10.4
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 20 Jul 2022 02:29:04 GMT
VOLUME [/vault/logs]
# Wed, 20 Jul 2022 02:29:05 GMT
VOLUME [/vault/file]
# Wed, 20 Jul 2022 02:29:06 GMT
EXPOSE 8200
# Wed, 20 Jul 2022 02:29:08 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 20 Jul 2022 02:29:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Jul 2022 02:29:09 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:cbf9934fc184d27d98bef2567dbcecbee05767c8762c95e63984577a8c23e961`  
		Last Modified: Tue, 19 Jul 2022 22:39:35 GMT  
		Size: 2.8 MB (2821611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72398b4cd893f51d343a06bf0700c73c7ce9d7dfe2c760756f72befd94c346bd`  
		Last Modified: Wed, 20 Jul 2022 02:30:33 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c446c50f168ee2755c557b02235612c2acc05cfaaaf1cf9f9f46394a00efc3d4`  
		Last Modified: Wed, 20 Jul 2022 02:30:40 GMT  
		Size: 67.6 MB (67591827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48baef26c6c5b0973da7479deb065271875385dbf2f7cf399d33a87d3c3dc9a`  
		Last Modified: Wed, 20 Jul 2022 02:30:33 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb1ec2be5d78742b209a14c0e32ae27afe2425f4e39334d3dccc9850d48028f`  
		Last Modified: Wed, 20 Jul 2022 02:30:33 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.11.0`

```console
$ docker pull vault@sha256:d1b01a601faaef36a120aee0670ca353918747ae7315375193141ebbabf5114b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.11.0` - linux; amd64

```console
$ docker pull vault@sha256:3a02bc2790896cc2cc71a378921e352d632e85224264ef65702c658bafe68acb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77436390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0e2e3e92cc1fc3fc678713e8cc2c01c6e0e4b7890ee3916dbff264b4eb08458`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:18 GMT
ADD file:80b46be2fe86b402518b00758ff5d8556d92113dc267a002b6c72a5f9c6742a3 in / 
# Tue, 19 Jul 2022 22:20:18 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 02:03:00 GMT
ARG VAULT_VERSION=1.11.0
# Wed, 20 Jul 2022 02:03:00 GMT
# ARGS: VAULT_VERSION=1.11.0
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 20 Jul 2022 02:03:09 GMT
# ARGS: VAULT_VERSION=1.11.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 20 Jul 2022 02:03:10 GMT
# ARGS: VAULT_VERSION=1.11.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 20 Jul 2022 02:03:10 GMT
VOLUME [/vault/logs]
# Wed, 20 Jul 2022 02:03:10 GMT
VOLUME [/vault/file]
# Wed, 20 Jul 2022 02:03:10 GMT
EXPOSE 8200
# Wed, 20 Jul 2022 02:03:11 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 20 Jul 2022 02:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Jul 2022 02:03:11 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:decfdc335d9bae9ca06166e1a4fc2cdf8c2344a42d85c8a1d3f964aab59ecff5`  
		Last Modified: Tue, 19 Jul 2022 22:20:55 GMT  
		Size: 2.8 MB (2818512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d956a01be9b2774ee707e6e4f973fff9058a152abeb17efa034f94aae02ab413`  
		Last Modified: Wed, 20 Jul 2022 02:03:58 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd756534f170e83d5ab09fc8101cf4ebe3697a074641bfcc4336b87eaf1b302`  
		Last Modified: Wed, 20 Jul 2022 02:04:08 GMT  
		Size: 74.6 MB (74614611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ad3c30d4a3356947d585ef81c5ed41b085af39957b2a3438450c62231a7d01`  
		Last Modified: Wed, 20 Jul 2022 02:03:58 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c2b86d13bb969c199bb7d9ab72f929ae239f8e363cfe03a8a87773afcc62a7`  
		Last Modified: Wed, 20 Jul 2022 02:03:59 GMT  
		Size: 1.8 KB (1810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.11.0` - linux; arm variant v6

```console
$ docker pull vault@sha256:ae7d7b19458c2e2566623e6a32d2ac39e68ca72af02c596fa875c364f3d52184
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70208271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745c6f428116885bb53b0e56bf6895d53b8c181f02c3511f4480034a337fbaeb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:55 GMT
ADD file:2e4db0cea3f5eecfbb82c5abd09eb100749fed0189fc30d2c51980d2560e3ccb in / 
# Mon, 04 Apr 2022 23:49:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Jun 2022 23:51:06 GMT
ARG VAULT_VERSION=1.11.0
# Tue, 21 Jun 2022 23:51:08 GMT
# ARGS: VAULT_VERSION=1.11.0
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 21 Jun 2022 23:51:27 GMT
# ARGS: VAULT_VERSION=1.11.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 21 Jun 2022 23:51:30 GMT
# ARGS: VAULT_VERSION=1.11.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 21 Jun 2022 23:51:30 GMT
VOLUME [/vault/logs]
# Tue, 21 Jun 2022 23:51:30 GMT
VOLUME [/vault/file]
# Tue, 21 Jun 2022 23:51:31 GMT
EXPOSE 8200
# Tue, 21 Jun 2022 23:51:31 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 21 Jun 2022 23:51:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jun 2022 23:51:32 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:f9f2e4e531ad51ee917e8311e91a223a4893c1d754acb8246af87375ea60c6aa`  
		Last Modified: Mon, 04 Apr 2022 23:51:47 GMT  
		Size: 2.6 MB (2626056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61510bfcfaebed522571694f06bc8e6f60afdbfe5928246f5007c7e8e03bd500`  
		Last Modified: Tue, 21 Jun 2022 23:52:29 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2d1e980fe553c83740bb98b55b61f089aa8fdb053622f7021e042ec9bccdf4`  
		Last Modified: Tue, 21 Jun 2022 23:53:06 GMT  
		Size: 67.6 MB (67578948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938218f9a2801982962aa75e217eb4d0e5f5e968f6e1342200647380d6db7b12`  
		Last Modified: Tue, 21 Jun 2022 23:52:29 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289b1df03577decc3cb73f38551da8e247922f1ffe3a66bc7c7e05ace23a9cc4`  
		Last Modified: Tue, 21 Jun 2022 23:52:29 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.11.0` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:810ded0e55ab1d0b8fa57bc7060c071945c79f086bbd413101ba446f03bd3aa6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72252336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc1951f8812bf1c51db0a42edf1bbed44a263d3bea537d025fc368e2aa29e49a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Wed, 22 Jun 2022 03:17:09 GMT
ARG VAULT_VERSION=1.11.0
# Wed, 22 Jun 2022 03:17:10 GMT
# ARGS: VAULT_VERSION=1.11.0
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 22 Jun 2022 03:17:19 GMT
# ARGS: VAULT_VERSION=1.11.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 22 Jun 2022 03:17:20 GMT
# ARGS: VAULT_VERSION=1.11.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 22 Jun 2022 03:17:21 GMT
VOLUME [/vault/logs]
# Wed, 22 Jun 2022 03:17:22 GMT
VOLUME [/vault/file]
# Wed, 22 Jun 2022 03:17:23 GMT
EXPOSE 8200
# Wed, 22 Jun 2022 03:17:25 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 03:17:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 03:17:26 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ec8b7e7fc35cf2f287ea02c195d99090ae431c4aa4e66c31a2f8e58ef66fec`  
		Last Modified: Wed, 22 Jun 2022 03:17:56 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25bda75901f25501bca193e34ef0bfba67636bf2edd90f687dba610a6a48087`  
		Last Modified: Wed, 22 Jun 2022 03:18:07 GMT  
		Size: 69.5 MB (69531741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0b092a015fb79c9f94c5d3e8b1d5714ca072d6d2e22fc5557bfe60ac359c67`  
		Last Modified: Wed, 22 Jun 2022 03:17:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4a35fc984c96a1d024f43ee8eb6b8e020d104d092d954b29b65d96fd633674`  
		Last Modified: Wed, 22 Jun 2022 03:17:56 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.11.0` - linux; 386

```console
$ docker pull vault@sha256:4c806a4d4ec9f4768d915f62492145f6f74a995f4095aaf3312efb230c037f69
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73513954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f7cc43c3deb0f19a9df127826cf70ccd679fee378d7bb93c98b3b41b82a0ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 19 Jul 2022 22:38:40 GMT
ADD file:4ae4391bf852a3e83cff6c0baebf0241d4955d580e24c180f882a142e4adaf1d in / 
# Tue, 19 Jul 2022 22:38:40 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 02:28:26 GMT
ARG VAULT_VERSION=1.11.0
# Wed, 20 Jul 2022 02:28:26 GMT
# ARGS: VAULT_VERSION=1.11.0
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 20 Jul 2022 02:28:37 GMT
# ARGS: VAULT_VERSION=1.11.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 20 Jul 2022 02:28:38 GMT
# ARGS: VAULT_VERSION=1.11.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 20 Jul 2022 02:28:39 GMT
VOLUME [/vault/logs]
# Wed, 20 Jul 2022 02:28:40 GMT
VOLUME [/vault/file]
# Wed, 20 Jul 2022 02:28:41 GMT
EXPOSE 8200
# Wed, 20 Jul 2022 02:28:43 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 20 Jul 2022 02:28:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Jul 2022 02:28:44 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:cbf9934fc184d27d98bef2567dbcecbee05767c8762c95e63984577a8c23e961`  
		Last Modified: Tue, 19 Jul 2022 22:39:35 GMT  
		Size: 2.8 MB (2821611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0bb95aaac0e25567f0cfa105f48d4688aa8e4c2295449c262829100e15f8ae`  
		Last Modified: Wed, 20 Jul 2022 02:30:13 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a798eb7234ffd982626ced03ac5b39f8141ac3cc859e2ee66b892ea905e750a0`  
		Last Modified: Wed, 20 Jul 2022 02:30:21 GMT  
		Size: 70.7 MB (70689137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c0417c8514ab964bfc4ab6320293299fe3cd1cfd51128e3e711ea5905efcfbc`  
		Last Modified: Wed, 20 Jul 2022 02:30:13 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:965749261b8aa41475e103c9016ff3b8a27543ce8b7c39cfcc4575d94da649ae`  
		Last Modified: Wed, 20 Jul 2022 02:30:13 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.8.12`

```console
$ docker pull vault@sha256:672de24e0d688a24dd24fd4fce3b00da8684ebb8bfd07e6f4d111c3fcd76535a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.8.12` - linux; amd64

```console
$ docker pull vault@sha256:f760660f16abe1798452e9a65f24764ab3d221842e585c9964750747d6666079
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70629338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957d5923bcda57d3479c7c7a59628034d45a1793c213b74aeac7d35a69303766`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:18 GMT
ADD file:80b46be2fe86b402518b00758ff5d8556d92113dc267a002b6c72a5f9c6742a3 in / 
# Tue, 19 Jul 2022 22:20:18 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 02:03:37 GMT
ARG VAULT_VERSION=1.8.12
# Wed, 20 Jul 2022 02:03:38 GMT
# ARGS: VAULT_VERSION=1.8.12
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 20 Jul 2022 02:03:45 GMT
# ARGS: VAULT_VERSION=1.8.12
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 20 Jul 2022 02:03:46 GMT
# ARGS: VAULT_VERSION=1.8.12
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 20 Jul 2022 02:03:46 GMT
VOLUME [/vault/logs]
# Wed, 20 Jul 2022 02:03:46 GMT
VOLUME [/vault/file]
# Wed, 20 Jul 2022 02:03:47 GMT
EXPOSE 8200
# Wed, 20 Jul 2022 02:03:47 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 20 Jul 2022 02:03:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Jul 2022 02:03:47 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:decfdc335d9bae9ca06166e1a4fc2cdf8c2344a42d85c8a1d3f964aab59ecff5`  
		Last Modified: Tue, 19 Jul 2022 22:20:55 GMT  
		Size: 2.8 MB (2818512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764680553f286ca79045e8c7f9f2483ceb44654fe33ff10bc468e847be04d915`  
		Last Modified: Wed, 20 Jul 2022 02:04:49 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea08665a6659cdbcc6a670501d66afb7e19381519017deb9f4a9a3236f6c632`  
		Last Modified: Wed, 20 Jul 2022 02:04:58 GMT  
		Size: 67.8 MB (67807558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abec44ce6906be260218571543938318bdf357c0a6f032c08b4ed020683d013`  
		Last Modified: Wed, 20 Jul 2022 02:04:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1796437a6c9404a3aeb93ab7502b09ecdb74e5d8dae7af5192bd5ea7a25e225`  
		Last Modified: Wed, 20 Jul 2022 02:04:49 GMT  
		Size: 1.8 KB (1810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.8.12` - linux; arm variant v6

```console
$ docker pull vault@sha256:73b13b345428f26dfd14f80ce5d2c8a28d209715f473ad4bae4ec9f7896b2f2c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64957559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f70429388162fe12ce3260f0c0e3861f012ee962e9b8406c4fd57553998f1cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:55 GMT
ADD file:2e4db0cea3f5eecfbb82c5abd09eb100749fed0189fc30d2c51980d2560e3ccb in / 
# Mon, 04 Apr 2022 23:49:56 GMT
CMD ["/bin/sh"]
# Mon, 13 Jun 2022 17:56:03 GMT
ARG VAULT_VERSION=1.8.12
# Mon, 13 Jun 2022 17:56:04 GMT
# ARGS: VAULT_VERSION=1.8.12
RUN addgroup vault &&     adduser -S -G vault vault
# Mon, 13 Jun 2022 17:56:20 GMT
# ARGS: VAULT_VERSION=1.8.12
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Mon, 13 Jun 2022 17:56:22 GMT
# ARGS: VAULT_VERSION=1.8.12
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Mon, 13 Jun 2022 17:56:22 GMT
VOLUME [/vault/logs]
# Mon, 13 Jun 2022 17:56:22 GMT
VOLUME [/vault/file]
# Mon, 13 Jun 2022 17:56:23 GMT
EXPOSE 8200
# Mon, 13 Jun 2022 17:56:23 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 13 Jun 2022 17:56:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jun 2022 17:56:24 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:f9f2e4e531ad51ee917e8311e91a223a4893c1d754acb8246af87375ea60c6aa`  
		Last Modified: Mon, 04 Apr 2022 23:51:47 GMT  
		Size: 2.6 MB (2626056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063a27e90a289fc3a7f542a3c008ae09e524435a139ec196577f65d827217d08`  
		Last Modified: Mon, 13 Jun 2022 17:59:25 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:384e9ec962d169d8ec9b85771f5e78717af008b3e08634e33d4f2b2e81ac36e0`  
		Last Modified: Mon, 13 Jun 2022 17:59:57 GMT  
		Size: 62.3 MB (62328231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5fdc04bc1729dbe0bd5fe6e4ba02b24b205f1f542fbc22d97d0990a225ac07d`  
		Last Modified: Mon, 13 Jun 2022 17:59:25 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d9739193c24f2cbd93ce338449e0e1a63a0d8e6c1c2ea8aa45f05a926eb5a9`  
		Last Modified: Mon, 13 Jun 2022 17:59:35 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.8.12` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:dfa52d3a2a145d93b56112aa2c7b883773fd751ee75ab6ccca7db688ca922eb5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66894157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218fa82d5eb1593fe04e724120965796baa7dd208d472e7d6010c530b7068cb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Mon, 13 Jun 2022 18:17:16 GMT
ARG VAULT_VERSION=1.8.12
# Mon, 13 Jun 2022 18:17:16 GMT
# ARGS: VAULT_VERSION=1.8.12
RUN addgroup vault &&     adduser -S -G vault vault
# Mon, 13 Jun 2022 18:17:23 GMT
# ARGS: VAULT_VERSION=1.8.12
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Mon, 13 Jun 2022 18:17:23 GMT
# ARGS: VAULT_VERSION=1.8.12
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Mon, 13 Jun 2022 18:17:24 GMT
VOLUME [/vault/logs]
# Mon, 13 Jun 2022 18:17:25 GMT
VOLUME [/vault/file]
# Mon, 13 Jun 2022 18:17:26 GMT
EXPOSE 8200
# Mon, 13 Jun 2022 18:17:28 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 13 Jun 2022 18:17:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jun 2022 18:17:29 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8255df8d240ead170699d5d2977dae568c0ad8ebcf05285c9d1753194cc87090`  
		Last Modified: Mon, 13 Jun 2022 18:18:47 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a44d86d973044b5f8fdae5055398eb0045e186b04be6ff6f91ac042dd06ccd1`  
		Last Modified: Mon, 13 Jun 2022 18:18:56 GMT  
		Size: 64.2 MB (64173569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298777db23abf788ff293e162d86c9ce0272eaff62866a6ffa91903b495a7fe4`  
		Last Modified: Mon, 13 Jun 2022 18:18:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ede68199949ffac61fe89cafb80cedf93930d561da8515e5e7aa68c43d35b1`  
		Last Modified: Mon, 13 Jun 2022 18:18:47 GMT  
		Size: 1.8 KB (1809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.8.12` - linux; 386

```console
$ docker pull vault@sha256:32ebaf7e4529bfe81aeedaa8216c99a19669562da53b4b1204f11d031c560360
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68326802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21fc5a803a9a87bdb00bc441ec078c9547dd4e3cb04d89d3783fbd8e918db0b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 19 Jul 2022 22:38:40 GMT
ADD file:4ae4391bf852a3e83cff6c0baebf0241d4955d580e24c180f882a142e4adaf1d in / 
# Tue, 19 Jul 2022 22:38:40 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 02:29:36 GMT
ARG VAULT_VERSION=1.8.12
# Wed, 20 Jul 2022 02:29:37 GMT
# ARGS: VAULT_VERSION=1.8.12
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 20 Jul 2022 02:29:46 GMT
# ARGS: VAULT_VERSION=1.8.12
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 20 Jul 2022 02:29:46 GMT
# ARGS: VAULT_VERSION=1.8.12
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 20 Jul 2022 02:29:47 GMT
VOLUME [/vault/logs]
# Wed, 20 Jul 2022 02:29:48 GMT
VOLUME [/vault/file]
# Wed, 20 Jul 2022 02:29:49 GMT
EXPOSE 8200
# Wed, 20 Jul 2022 02:29:51 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 20 Jul 2022 02:29:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Jul 2022 02:29:52 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:cbf9934fc184d27d98bef2567dbcecbee05767c8762c95e63984577a8c23e961`  
		Last Modified: Tue, 19 Jul 2022 22:39:35 GMT  
		Size: 2.8 MB (2821611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e49728480c9e7419ec19690d2aa5b56574e1322ba5d41e26c470f89aa75ee5b`  
		Last Modified: Wed, 20 Jul 2022 02:31:04 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7624d2c9bbf9e52e3e90d53e674a621327d42ac4bfd7c084c8fd09d8573240f`  
		Last Modified: Wed, 20 Jul 2022 02:31:14 GMT  
		Size: 65.5 MB (65501989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809ecc92ae4da1a4298fb8657ea292248d8c835f2f82bfd8ad0653fd6b8f7232`  
		Last Modified: Wed, 20 Jul 2022 02:31:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b8b5dc478893db3d6e132d54ffe7186a24dc97a4147b2c2a863c66de57f81f`  
		Last Modified: Wed, 20 Jul 2022 02:31:04 GMT  
		Size: 1.8 KB (1809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.9.7`

```console
$ docker pull vault@sha256:915f33368e7c954186d78bae792211ef43e444ca902849a27a4c7a7b9c95b3e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.9.7` - linux; amd64

```console
$ docker pull vault@sha256:ca3dda86cf38ffa638cce17f5a3875d2eddf632fa5d4abf505eb9bf07619c07c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73182098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d5447a60051c69740be1da4230cbd9e3ad08aaae18b17e6e5a40d55a7919a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:18 GMT
ADD file:80b46be2fe86b402518b00758ff5d8556d92113dc267a002b6c72a5f9c6742a3 in / 
# Tue, 19 Jul 2022 22:20:18 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 02:03:25 GMT
ARG VAULT_VERSION=1.9.7
# Wed, 20 Jul 2022 02:03:26 GMT
# ARGS: VAULT_VERSION=1.9.7
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 20 Jul 2022 02:03:34 GMT
# ARGS: VAULT_VERSION=1.9.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 20 Jul 2022 02:03:34 GMT
# ARGS: VAULT_VERSION=1.9.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 20 Jul 2022 02:03:34 GMT
VOLUME [/vault/logs]
# Wed, 20 Jul 2022 02:03:35 GMT
VOLUME [/vault/file]
# Wed, 20 Jul 2022 02:03:35 GMT
EXPOSE 8200
# Wed, 20 Jul 2022 02:03:35 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 20 Jul 2022 02:03:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Jul 2022 02:03:35 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:decfdc335d9bae9ca06166e1a4fc2cdf8c2344a42d85c8a1d3f964aab59ecff5`  
		Last Modified: Tue, 19 Jul 2022 22:20:55 GMT  
		Size: 2.8 MB (2818512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7330e71556a101ef84fd51172fd0fc0b87b319c90e00a5f476b7eefe326ec3`  
		Last Modified: Wed, 20 Jul 2022 02:04:33 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4266ab9d194d528f62c1cd9451ddb4ad4073f7bdbeded373eeab0794a415a2dd`  
		Last Modified: Wed, 20 Jul 2022 02:04:42 GMT  
		Size: 70.4 MB (70360322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810debd7f11a49306085befc8056f87e395116e1ee504848545aa79acf595930`  
		Last Modified: Wed, 20 Jul 2022 02:04:33 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5130b3bf690020113bd1280f9f58b131a50fd6e9695889ca302441a99c32fdb`  
		Last Modified: Wed, 20 Jul 2022 02:04:33 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.9.7` - linux; arm variant v6

```console
$ docker pull vault@sha256:b8b808bb489b4278d38b68a5386834dd4ce1e415916c5838c94abb93103c2fe1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66505606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a122763094736ceb1719301b1467d3e287377fea7524dddbcb298e85dfff1fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:55 GMT
ADD file:2e4db0cea3f5eecfbb82c5abd09eb100749fed0189fc30d2c51980d2560e3ccb in / 
# Mon, 04 Apr 2022 23:49:56 GMT
CMD ["/bin/sh"]
# Mon, 13 Jun 2022 17:55:29 GMT
ARG VAULT_VERSION=1.9.7
# Mon, 13 Jun 2022 17:55:31 GMT
# ARGS: VAULT_VERSION=1.9.7
RUN addgroup vault &&     adduser -S -G vault vault
# Mon, 13 Jun 2022 17:55:47 GMT
# ARGS: VAULT_VERSION=1.9.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Mon, 13 Jun 2022 17:55:49 GMT
# ARGS: VAULT_VERSION=1.9.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Mon, 13 Jun 2022 17:55:50 GMT
VOLUME [/vault/logs]
# Mon, 13 Jun 2022 17:55:50 GMT
VOLUME [/vault/file]
# Mon, 13 Jun 2022 17:55:51 GMT
EXPOSE 8200
# Mon, 13 Jun 2022 17:55:51 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 13 Jun 2022 17:55:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jun 2022 17:55:52 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:f9f2e4e531ad51ee917e8311e91a223a4893c1d754acb8246af87375ea60c6aa`  
		Last Modified: Mon, 04 Apr 2022 23:51:47 GMT  
		Size: 2.6 MB (2626056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9250424af433f7b094c30a60bb6df05b871b3d067f144b6cb48070e9be8a23`  
		Last Modified: Mon, 13 Jun 2022 17:58:43 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f884ddef8d2672d429e1f96191db93defc30c8ae8ff85c352132c71795ff13`  
		Last Modified: Mon, 13 Jun 2022 17:59:18 GMT  
		Size: 63.9 MB (63876281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cbc147c97ef291fb92073ccb8c89139f8831f0cddcc72849c746f5e4866ea65`  
		Last Modified: Mon, 13 Jun 2022 17:58:43 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1338e0443ab92f26c8d4d4ee4e10e8a1b23cf11440a8519810da21cc8a11f1c`  
		Last Modified: Mon, 13 Jun 2022 17:58:43 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.9.7` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:2a5141add519a7cf5a35a6c87efb14a3ab920055f22c5ef6e2e14ae786239cb4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68285655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a779ea15c00d877fef0d7188d4293b11f573874f9c2a9bab5df42feb337155`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Mon, 13 Jun 2022 18:16:56 GMT
ARG VAULT_VERSION=1.9.7
# Mon, 13 Jun 2022 18:16:57 GMT
# ARGS: VAULT_VERSION=1.9.7
RUN addgroup vault &&     adduser -S -G vault vault
# Mon, 13 Jun 2022 18:17:03 GMT
# ARGS: VAULT_VERSION=1.9.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Mon, 13 Jun 2022 18:17:04 GMT
# ARGS: VAULT_VERSION=1.9.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Mon, 13 Jun 2022 18:17:05 GMT
VOLUME [/vault/logs]
# Mon, 13 Jun 2022 18:17:06 GMT
VOLUME [/vault/file]
# Mon, 13 Jun 2022 18:17:07 GMT
EXPOSE 8200
# Mon, 13 Jun 2022 18:17:09 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 13 Jun 2022 18:17:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jun 2022 18:17:10 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8ca4a6c8ffbd61f824762d25685564a2d4a27eda894b669c8ceadf1ce24077`  
		Last Modified: Mon, 13 Jun 2022 18:18:30 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462355e7ec8f054b00710daead792a5f0e461001e8d807139cf48edac0fd13fa`  
		Last Modified: Mon, 13 Jun 2022 18:18:38 GMT  
		Size: 65.6 MB (65565058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d928b90aac5571da33be0954f118e1b81f72a6d15e043cfa3d94ff4884000f1`  
		Last Modified: Mon, 13 Jun 2022 18:18:30 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc80c9ebba10b16e0f8340d64b50197de0eb8489a01b20b44b4dc74f496ac613`  
		Last Modified: Mon, 13 Jun 2022 18:18:30 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.9.7` - linux; 386

```console
$ docker pull vault@sha256:1e86193cb54f60ef25482ff70ef088620d448393549504659bc61f69f95b23cd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69561363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0dee24961727bee7a243119d73824621e242598172f8126d02b1b977e19ee6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 19 Jul 2022 22:38:40 GMT
ADD file:4ae4391bf852a3e83cff6c0baebf0241d4955d580e24c180f882a142e4adaf1d in / 
# Tue, 19 Jul 2022 22:38:40 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 02:29:14 GMT
ARG VAULT_VERSION=1.9.7
# Wed, 20 Jul 2022 02:29:15 GMT
# ARGS: VAULT_VERSION=1.9.7
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 20 Jul 2022 02:29:23 GMT
# ARGS: VAULT_VERSION=1.9.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 20 Jul 2022 02:29:24 GMT
# ARGS: VAULT_VERSION=1.9.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 20 Jul 2022 02:29:25 GMT
VOLUME [/vault/logs]
# Wed, 20 Jul 2022 02:29:26 GMT
VOLUME [/vault/file]
# Wed, 20 Jul 2022 02:29:27 GMT
EXPOSE 8200
# Wed, 20 Jul 2022 02:29:29 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 20 Jul 2022 02:29:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Jul 2022 02:29:30 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:cbf9934fc184d27d98bef2567dbcecbee05767c8762c95e63984577a8c23e961`  
		Last Modified: Tue, 19 Jul 2022 22:39:35 GMT  
		Size: 2.8 MB (2821611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f035116b109faf6d1eb88e7161b1a75db74262bba8489b26345adac510c661`  
		Last Modified: Wed, 20 Jul 2022 02:30:49 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36289cb3c9f75b5202affca4161fc7ec561d9053c411502b0934772fa77e258d`  
		Last Modified: Wed, 20 Jul 2022 02:30:56 GMT  
		Size: 66.7 MB (66736546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0186c6018349333b991478f4c59616542359c076d5b744874497764873ac2b47`  
		Last Modified: Wed, 20 Jul 2022 02:30:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e089073e374322465f768a995e6f4c5513a5544853000f89b065b72e1a0f4a8b`  
		Last Modified: Wed, 20 Jul 2022 02:30:48 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:latest`

```console
$ docker pull vault@sha256:d1b01a601faaef36a120aee0670ca353918747ae7315375193141ebbabf5114b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:latest` - linux; amd64

```console
$ docker pull vault@sha256:3a02bc2790896cc2cc71a378921e352d632e85224264ef65702c658bafe68acb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77436390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0e2e3e92cc1fc3fc678713e8cc2c01c6e0e4b7890ee3916dbff264b4eb08458`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:18 GMT
ADD file:80b46be2fe86b402518b00758ff5d8556d92113dc267a002b6c72a5f9c6742a3 in / 
# Tue, 19 Jul 2022 22:20:18 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 02:03:00 GMT
ARG VAULT_VERSION=1.11.0
# Wed, 20 Jul 2022 02:03:00 GMT
# ARGS: VAULT_VERSION=1.11.0
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 20 Jul 2022 02:03:09 GMT
# ARGS: VAULT_VERSION=1.11.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 20 Jul 2022 02:03:10 GMT
# ARGS: VAULT_VERSION=1.11.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 20 Jul 2022 02:03:10 GMT
VOLUME [/vault/logs]
# Wed, 20 Jul 2022 02:03:10 GMT
VOLUME [/vault/file]
# Wed, 20 Jul 2022 02:03:10 GMT
EXPOSE 8200
# Wed, 20 Jul 2022 02:03:11 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 20 Jul 2022 02:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Jul 2022 02:03:11 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:decfdc335d9bae9ca06166e1a4fc2cdf8c2344a42d85c8a1d3f964aab59ecff5`  
		Last Modified: Tue, 19 Jul 2022 22:20:55 GMT  
		Size: 2.8 MB (2818512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d956a01be9b2774ee707e6e4f973fff9058a152abeb17efa034f94aae02ab413`  
		Last Modified: Wed, 20 Jul 2022 02:03:58 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd756534f170e83d5ab09fc8101cf4ebe3697a074641bfcc4336b87eaf1b302`  
		Last Modified: Wed, 20 Jul 2022 02:04:08 GMT  
		Size: 74.6 MB (74614611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ad3c30d4a3356947d585ef81c5ed41b085af39957b2a3438450c62231a7d01`  
		Last Modified: Wed, 20 Jul 2022 02:03:58 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c2b86d13bb969c199bb7d9ab72f929ae239f8e363cfe03a8a87773afcc62a7`  
		Last Modified: Wed, 20 Jul 2022 02:03:59 GMT  
		Size: 1.8 KB (1810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm variant v6

```console
$ docker pull vault@sha256:ae7d7b19458c2e2566623e6a32d2ac39e68ca72af02c596fa875c364f3d52184
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70208271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745c6f428116885bb53b0e56bf6895d53b8c181f02c3511f4480034a337fbaeb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:55 GMT
ADD file:2e4db0cea3f5eecfbb82c5abd09eb100749fed0189fc30d2c51980d2560e3ccb in / 
# Mon, 04 Apr 2022 23:49:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Jun 2022 23:51:06 GMT
ARG VAULT_VERSION=1.11.0
# Tue, 21 Jun 2022 23:51:08 GMT
# ARGS: VAULT_VERSION=1.11.0
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 21 Jun 2022 23:51:27 GMT
# ARGS: VAULT_VERSION=1.11.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 21 Jun 2022 23:51:30 GMT
# ARGS: VAULT_VERSION=1.11.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 21 Jun 2022 23:51:30 GMT
VOLUME [/vault/logs]
# Tue, 21 Jun 2022 23:51:30 GMT
VOLUME [/vault/file]
# Tue, 21 Jun 2022 23:51:31 GMT
EXPOSE 8200
# Tue, 21 Jun 2022 23:51:31 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 21 Jun 2022 23:51:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jun 2022 23:51:32 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:f9f2e4e531ad51ee917e8311e91a223a4893c1d754acb8246af87375ea60c6aa`  
		Last Modified: Mon, 04 Apr 2022 23:51:47 GMT  
		Size: 2.6 MB (2626056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61510bfcfaebed522571694f06bc8e6f60afdbfe5928246f5007c7e8e03bd500`  
		Last Modified: Tue, 21 Jun 2022 23:52:29 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2d1e980fe553c83740bb98b55b61f089aa8fdb053622f7021e042ec9bccdf4`  
		Last Modified: Tue, 21 Jun 2022 23:53:06 GMT  
		Size: 67.6 MB (67578948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938218f9a2801982962aa75e217eb4d0e5f5e968f6e1342200647380d6db7b12`  
		Last Modified: Tue, 21 Jun 2022 23:52:29 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289b1df03577decc3cb73f38551da8e247922f1ffe3a66bc7c7e05ace23a9cc4`  
		Last Modified: Tue, 21 Jun 2022 23:52:29 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:810ded0e55ab1d0b8fa57bc7060c071945c79f086bbd413101ba446f03bd3aa6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72252336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc1951f8812bf1c51db0a42edf1bbed44a263d3bea537d025fc368e2aa29e49a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Wed, 22 Jun 2022 03:17:09 GMT
ARG VAULT_VERSION=1.11.0
# Wed, 22 Jun 2022 03:17:10 GMT
# ARGS: VAULT_VERSION=1.11.0
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 22 Jun 2022 03:17:19 GMT
# ARGS: VAULT_VERSION=1.11.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 22 Jun 2022 03:17:20 GMT
# ARGS: VAULT_VERSION=1.11.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 22 Jun 2022 03:17:21 GMT
VOLUME [/vault/logs]
# Wed, 22 Jun 2022 03:17:22 GMT
VOLUME [/vault/file]
# Wed, 22 Jun 2022 03:17:23 GMT
EXPOSE 8200
# Wed, 22 Jun 2022 03:17:25 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jun 2022 03:17:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jun 2022 03:17:26 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ec8b7e7fc35cf2f287ea02c195d99090ae431c4aa4e66c31a2f8e58ef66fec`  
		Last Modified: Wed, 22 Jun 2022 03:17:56 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25bda75901f25501bca193e34ef0bfba67636bf2edd90f687dba610a6a48087`  
		Last Modified: Wed, 22 Jun 2022 03:18:07 GMT  
		Size: 69.5 MB (69531741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0b092a015fb79c9f94c5d3e8b1d5714ca072d6d2e22fc5557bfe60ac359c67`  
		Last Modified: Wed, 22 Jun 2022 03:17:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4a35fc984c96a1d024f43ee8eb6b8e020d104d092d954b29b65d96fd633674`  
		Last Modified: Wed, 22 Jun 2022 03:17:56 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; 386

```console
$ docker pull vault@sha256:4c806a4d4ec9f4768d915f62492145f6f74a995f4095aaf3312efb230c037f69
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73513954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f7cc43c3deb0f19a9df127826cf70ccd679fee378d7bb93c98b3b41b82a0ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 19 Jul 2022 22:38:40 GMT
ADD file:4ae4391bf852a3e83cff6c0baebf0241d4955d580e24c180f882a142e4adaf1d in / 
# Tue, 19 Jul 2022 22:38:40 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 02:28:26 GMT
ARG VAULT_VERSION=1.11.0
# Wed, 20 Jul 2022 02:28:26 GMT
# ARGS: VAULT_VERSION=1.11.0
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 20 Jul 2022 02:28:37 GMT
# ARGS: VAULT_VERSION=1.11.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 20 Jul 2022 02:28:38 GMT
# ARGS: VAULT_VERSION=1.11.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 20 Jul 2022 02:28:39 GMT
VOLUME [/vault/logs]
# Wed, 20 Jul 2022 02:28:40 GMT
VOLUME [/vault/file]
# Wed, 20 Jul 2022 02:28:41 GMT
EXPOSE 8200
# Wed, 20 Jul 2022 02:28:43 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 20 Jul 2022 02:28:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Jul 2022 02:28:44 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:cbf9934fc184d27d98bef2567dbcecbee05767c8762c95e63984577a8c23e961`  
		Last Modified: Tue, 19 Jul 2022 22:39:35 GMT  
		Size: 2.8 MB (2821611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0bb95aaac0e25567f0cfa105f48d4688aa8e4c2295449c262829100e15f8ae`  
		Last Modified: Wed, 20 Jul 2022 02:30:13 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a798eb7234ffd982626ced03ac5b39f8141ac3cc859e2ee66b892ea905e750a0`  
		Last Modified: Wed, 20 Jul 2022 02:30:21 GMT  
		Size: 70.7 MB (70689137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c0417c8514ab964bfc4ab6320293299fe3cd1cfd51128e3e711ea5905efcfbc`  
		Last Modified: Wed, 20 Jul 2022 02:30:13 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:965749261b8aa41475e103c9016ff3b8a27543ce8b7c39cfcc4575d94da649ae`  
		Last Modified: Wed, 20 Jul 2022 02:30:13 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
