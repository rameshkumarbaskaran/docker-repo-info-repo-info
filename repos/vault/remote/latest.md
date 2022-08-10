## `vault:latest`

```console
$ docker pull vault@sha256:a21876d5fe555d7369084ec3216a38b927da8f9c845d383586c7f54236413ad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:latest` - linux; amd64

```console
$ docker pull vault@sha256:7a238778738551ab26e07ef2c4ac9d9d9e8d393ec9e766301c9b3bb0fa5f2b55
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77492763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22fdc6314051df714eb280680c24524ed01d0ed2eddff1358cc40d528c82579e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 01:26:51 GMT
ARG VAULT_VERSION=1.11.2
# Wed, 10 Aug 2022 01:26:52 GMT
# ARGS: VAULT_VERSION=1.11.2
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 10 Aug 2022 01:27:00 GMT
# ARGS: VAULT_VERSION=1.11.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 10 Aug 2022 01:27:01 GMT
# ARGS: VAULT_VERSION=1.11.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 10 Aug 2022 01:27:01 GMT
VOLUME [/vault/logs]
# Wed, 10 Aug 2022 01:27:01 GMT
VOLUME [/vault/file]
# Wed, 10 Aug 2022 01:27:01 GMT
EXPOSE 8200
# Wed, 10 Aug 2022 01:27:01 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 Aug 2022 01:27:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 01:27:01 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8967aa5130c8a6f6bb7143c8391df393368db6921ab770555efde013985a9d28`  
		Last Modified: Wed, 10 Aug 2022 01:27:51 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db9d0afc6ab490c62cd716176a04cfd75c36714cb67b9e30a2cda0ef0be75f0`  
		Last Modified: Wed, 10 Aug 2022 01:28:01 GMT  
		Size: 74.7 MB (74662006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0119f940dd249e511bdcf111cbe3b317d64b16eaa192d25fb6b9d83326f33acb`  
		Last Modified: Wed, 10 Aug 2022 01:27:51 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98184bebb2e9dc29170e6960d8239418e57b92f48ef4edd5a62482071df9c373`  
		Last Modified: Wed, 10 Aug 2022 01:27:51 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm variant v6

```console
$ docker pull vault@sha256:f7b36d61ef1e198262a672601f06e50c01800f197876613fe38eeaaf19e6faf8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70252099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4840ff699b78218305dbfaa6f8a4e5e4fd09a28544ecfc18f38ee02b39a7bcdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 19 Jul 2022 22:50:02 GMT
ADD file:5a22b2130f6fbe534730df1f47715641a45e55845be7f35c3183e2b74ec43397 in / 
# Tue, 19 Jul 2022 22:50:03 GMT
CMD ["/bin/sh"]
# Thu, 04 Aug 2022 00:49:49 GMT
ARG VAULT_VERSION=1.11.2
# Thu, 04 Aug 2022 00:49:50 GMT
# ARGS: VAULT_VERSION=1.11.2
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 04 Aug 2022 00:50:03 GMT
# ARGS: VAULT_VERSION=1.11.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 04 Aug 2022 00:50:04 GMT
# ARGS: VAULT_VERSION=1.11.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 04 Aug 2022 00:50:04 GMT
VOLUME [/vault/logs]
# Thu, 04 Aug 2022 00:50:04 GMT
VOLUME [/vault/file]
# Thu, 04 Aug 2022 00:50:04 GMT
EXPOSE 8200
# Thu, 04 Aug 2022 00:50:05 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 04 Aug 2022 00:50:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 00:50:05 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:7dc1cbfb63ac7071e143ce96f0f140dc30282039f8d0770eaa7ab97eba515639`  
		Last Modified: Tue, 19 Jul 2022 22:51:41 GMT  
		Size: 2.6 MB (2626632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe5d0bab33752d600ccc29fbfe614ed9b77022cc6917e0d105f43029315d5c1`  
		Last Modified: Thu, 04 Aug 2022 00:51:25 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fddad393ff0b354750574a05b6092fc9d6af3767312789455a8e557815014dca`  
		Last Modified: Thu, 04 Aug 2022 00:51:38 GMT  
		Size: 67.6 MB (67622196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b4fd1bd01fd74ec5a209c0e8ef421017bbc7c6710c69b8167bb4973fbd35d84`  
		Last Modified: Thu, 04 Aug 2022 00:51:25 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8aa266ce16913028810350646722976666d954374379b285b0f65ba4337da8`  
		Last Modified: Thu, 04 Aug 2022 00:51:25 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:80151a9dbdd243c62774b8a1113224c6f519194e6d4571634718d111de4ce50e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72285316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f88fbcce3222d1f7b9912a9b142a8e9e5f245d278638b972bc1eed09289c78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:59 GMT
ADD file:b312c8f512719efd09811d17c2b250bbad03cf3f90c135a00695cc8e152f4ee2 in / 
# Tue, 09 Aug 2022 17:39:59 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 06:21:33 GMT
ARG VAULT_VERSION=1.11.2
# Wed, 10 Aug 2022 06:21:34 GMT
# ARGS: VAULT_VERSION=1.11.2
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 10 Aug 2022 06:21:43 GMT
# ARGS: VAULT_VERSION=1.11.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 10 Aug 2022 06:21:44 GMT
# ARGS: VAULT_VERSION=1.11.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 10 Aug 2022 06:21:45 GMT
VOLUME [/vault/logs]
# Wed, 10 Aug 2022 06:21:46 GMT
VOLUME [/vault/file]
# Wed, 10 Aug 2022 06:21:47 GMT
EXPOSE 8200
# Wed, 10 Aug 2022 06:21:49 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 Aug 2022 06:21:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 06:21:50 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:90cda3b7c32511829cd5ae9074240c36c34507085acb6e55b96f993740d2be93`  
		Last Modified: Tue, 09 Aug 2022 17:41:06 GMT  
		Size: 2.7 MB (2722153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef788ff86a429eec5ae34e7396476bf848be89528ee0c96459e592c54feeed2c`  
		Last Modified: Wed, 10 Aug 2022 06:23:16 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b036828efcfb812eb451a703d86dbba576fe28421489fa6275556eb67492dcf`  
		Last Modified: Wed, 10 Aug 2022 06:23:25 GMT  
		Size: 69.6 MB (69559958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20314912d5144dfe025ddedf1e6e18748a9822da6d162118f0d6b2defff4a25b`  
		Last Modified: Wed, 10 Aug 2022 06:23:16 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8371e722544e476f70a12d21ea938e136e06b2199fbf7dfc1d7beb3e3250c32b`  
		Last Modified: Wed, 10 Aug 2022 06:23:16 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; 386

```console
$ docker pull vault@sha256:556137692bc84155dc5886a12ae852d4ce1d5bb058e207d43a07f5ce716f0808
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73567722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c7a4e16b968a99b1ef223d5cde6b79ad51103581802e72741be70c9ea5db3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:54 GMT
ADD file:fea8a3ba06779852956b0d3a2dd7514ab33217b1fd395231864c443797f077f6 in / 
# Tue, 09 Aug 2022 17:38:54 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 00:13:39 GMT
ARG VAULT_VERSION=1.11.2
# Wed, 10 Aug 2022 00:13:40 GMT
# ARGS: VAULT_VERSION=1.11.2
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 10 Aug 2022 00:13:49 GMT
# ARGS: VAULT_VERSION=1.11.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 10 Aug 2022 00:13:50 GMT
# ARGS: VAULT_VERSION=1.11.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 10 Aug 2022 00:13:51 GMT
VOLUME [/vault/logs]
# Wed, 10 Aug 2022 00:13:52 GMT
VOLUME [/vault/file]
# Wed, 10 Aug 2022 00:13:53 GMT
EXPOSE 8200
# Wed, 10 Aug 2022 00:13:55 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 Aug 2022 00:13:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 00:13:56 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:2c44f983a875883421e7d5bc471f6437e0e377e6e7343b52c856caee71064d31`  
		Last Modified: Tue, 09 Aug 2022 17:40:01 GMT  
		Size: 2.8 MB (2832612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fdb4858833cdfc5a5714d5a19c93b337a0e778ec7d80ef77189fac0471c7566`  
		Last Modified: Wed, 10 Aug 2022 00:15:25 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb24cb72e1a2fdb06de8d1a5f75cd0a549f107b77909b2a0c1b20f9e2d74d29`  
		Last Modified: Wed, 10 Aug 2022 00:15:36 GMT  
		Size: 70.7 MB (70731906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7744188d2a7166aef058bb6d424153beba212e4c8749f465cf86914a226ca7`  
		Last Modified: Wed, 10 Aug 2022 00:15:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90460ac0bbb803713f9962bf787cb7021494e0163af9926e3ac5956d65c240d`  
		Last Modified: Wed, 10 Aug 2022 00:15:25 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
