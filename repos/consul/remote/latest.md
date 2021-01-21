## `consul:latest`

```console
$ docker pull consul@sha256:b5997e3f71b674f511033939cb7b9541b7cc2281ca7f81fb63933c64bed5c104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:latest` - linux; amd64

```console
$ docker pull consul@sha256:6f2b6f616ba2c208159379693ed998fed315dc8994c0bf39ee5a29cd2c7b51e0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45572498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2823bc69f80fe3c71d5fd94f188752b28066d118732da47cea866c693a8fe74d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:01:24 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 17 Dec 2020 13:01:25 GMT
ENV CONSUL_VERSION=1.9.1
# Thu, 17 Dec 2020 13:01:25 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 17 Dec 2020 13:01:27 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 17 Dec 2020 13:01:34 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 17 Dec 2020 13:01:35 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 17 Dec 2020 13:01:37 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Dec 2020 13:01:37 GMT
VOLUME [/consul/data]
# Thu, 17 Dec 2020 13:01:37 GMT
EXPOSE 8300
# Thu, 17 Dec 2020 13:01:38 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 17 Dec 2020 13:01:38 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 17 Dec 2020 13:01:39 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 17 Dec 2020 13:01:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 13:01:39 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365f82ba126180eddf3edbe8597b07845b62ee977e466199c841a7cf6307e6e0`  
		Last Modified: Thu, 17 Dec 2020 13:02:42 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4e74a5b5f7c36a408c2d9a3aca0bdac954e961d7fd85e7be48da3d257192d4`  
		Last Modified: Thu, 17 Dec 2020 13:02:49 GMT  
		Size: 42.8 MB (42770199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ef039d7e5d2b79db3587f87e6d789496e5969106bc837b74c97bb9b1bfd803`  
		Last Modified: Thu, 17 Dec 2020 13:02:41 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a29f03702b28af76b938efacb1f254f9e131c776d0e45dbe6d5616e124f147`  
		Last Modified: Thu, 17 Dec 2020 13:02:41 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0cc116ba6cdddf467ed810fe5e4047a09cfbf67a763df5aa3e624d23a21ca05`  
		Last Modified: Thu, 17 Dec 2020 13:02:41 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm variant v6

```console
$ docker pull consul@sha256:09433ed5adc26846cadd9d07b88b6ca6995452488be29937b4018e00d07b3a2c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 MB (40846565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a259b57b45460fbaaae246878625657976c75a381d0dbbf8dcca5e5595a3024f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:43 GMT
ADD file:0a16715e2d0e5811c3c578945d618db0e269847a799340248f9ba8d393c9eec2 in / 
# Wed, 16 Dec 2020 23:49:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:15:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 21 Jan 2021 21:52:56 GMT
ARG CONSUL_VERSION=1.9.2
# Thu, 21 Jan 2021 21:52:57 GMT
LABEL org.opencontainers.image.version=1.9.2
# Thu, 21 Jan 2021 21:52:58 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 21 Jan 2021 21:53:01 GMT
# ARGS: CONSUL_VERSION=1.9.2
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 21 Jan 2021 21:55:13 GMT
# ARGS: CONSUL_VERSION=1.9.2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 21 Jan 2021 21:55:18 GMT
# ARGS: CONSUL_VERSION=1.9.2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 21 Jan 2021 21:55:21 GMT
# ARGS: CONSUL_VERSION=1.9.2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 21 Jan 2021 21:55:22 GMT
VOLUME [/consul/data]
# Thu, 21 Jan 2021 21:55:23 GMT
EXPOSE 8300
# Thu, 21 Jan 2021 21:55:24 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 21 Jan 2021 21:55:24 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 21 Jan 2021 21:55:25 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 21 Jan 2021 21:55:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Jan 2021 21:55:26 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:93247449aef3c56eb4f7ab7b3fed95743c974b823def6dd86ec84008126e7903`  
		Last Modified: Wed, 16 Dec 2020 23:50:24 GMT  
		Size: 2.6 MB (2604163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68886bcad55540156824b7334ba6968f2e2aef5edbbdb7c99ce6778a138e5346`  
		Last Modified: Thu, 21 Jan 2021 21:56:08 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5537d2ff2a79a77ac5c53d677805c1fb4688881a633541faac2a3c4591000b`  
		Last Modified: Thu, 21 Jan 2021 21:56:19 GMT  
		Size: 38.2 MB (38239103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38219ace88131be232012db73dfa3543d0cb585db03a36434b3bedec8de7e2f`  
		Last Modified: Thu, 21 Jan 2021 21:56:08 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02356861ba79b91256c9d428795d7d6aae4f95f07bb09cde3a5ba9a743bf390`  
		Last Modified: Thu, 21 Jan 2021 21:56:08 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c65106acd946ef239362e33bcabf1b5d9e6adce96283311e72c2f1a928c0f33`  
		Last Modified: Thu, 21 Jan 2021 21:56:09 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:7b878010be55876f2dd419e0e95aad54cd87ae078d5de54e232e4135eb1069c6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41054728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c2dd1235f58df53d892cd4409a01d2296d79bc0659075097fb3e59b5333e5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:26 GMT
ADD file:a4845c3840a3fd0e41e4635a179cce20c81afc6c02e34e3fd5bd2d535698918b in / 
# Wed, 16 Dec 2020 23:40:29 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:36:45 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 17 Dec 2020 00:36:46 GMT
ENV CONSUL_VERSION=1.9.1
# Thu, 17 Dec 2020 00:36:47 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 17 Dec 2020 00:36:50 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 17 Dec 2020 00:36:58 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 17 Dec 2020 00:37:01 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 17 Dec 2020 00:37:03 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Dec 2020 00:37:04 GMT
VOLUME [/consul/data]
# Thu, 17 Dec 2020 00:37:05 GMT
EXPOSE 8300
# Thu, 17 Dec 2020 00:37:06 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 17 Dec 2020 00:37:06 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 17 Dec 2020 00:37:07 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 17 Dec 2020 00:37:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 00:37:09 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:159e5727ea618dfe8b08811112e2c51f5bd2b9ae7db9eb214914a65249f70ca0`  
		Last Modified: Wed, 16 Dec 2020 23:41:08 GMT  
		Size: 2.7 MB (2709048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24525bced0a98ca04a6bf6cb635d7ace15e937a5e07dd76ea668c8b17a04eef0`  
		Last Modified: Thu, 17 Dec 2020 00:38:29 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e054bc9eeb5c27e7bad342cd91e18906bae54f1a547575e127a457dd16db0822`  
		Last Modified: Thu, 17 Dec 2020 00:38:38 GMT  
		Size: 38.3 MB (38342392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd86a9d50d9ca247d25fde48735e28e11f324632bf1d5dde3a4931999371c99`  
		Last Modified: Thu, 17 Dec 2020 00:38:29 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c07c99456488116d12e65a590c7b4d913b4d439f37335597add07d9d55330b6`  
		Last Modified: Thu, 17 Dec 2020 00:38:29 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1e94d05b445e0a2626bc88419fc01eeaa7e31f09719e972624fb8409a536b2`  
		Last Modified: Thu, 17 Dec 2020 00:38:29 GMT  
		Size: 1.7 KB (1702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; 386

```console
$ docker pull consul@sha256:4284d75590380ce58a8023acbb14e7546cd3942af86107e9e2cbb0c93dbba051
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44906113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d2745507a476ffe17334220110a29eddf92dcdaddaf862b45ddb7aa57d65e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 17 Dec 2020 00:38:32 GMT
ADD file:de33fda50a142403e842620d20bc4404e66fc4ace16edc6946c4539e8a797458 in / 
# Thu, 17 Dec 2020 00:38:32 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:24:05 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 17 Dec 2020 01:24:05 GMT
ENV CONSUL_VERSION=1.9.1
# Thu, 17 Dec 2020 01:24:06 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 17 Dec 2020 01:24:08 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 17 Dec 2020 01:24:15 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 17 Dec 2020 01:24:16 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 17 Dec 2020 01:24:18 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Dec 2020 01:24:18 GMT
VOLUME [/consul/data]
# Thu, 17 Dec 2020 01:24:19 GMT
EXPOSE 8300
# Thu, 17 Dec 2020 01:24:19 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 17 Dec 2020 01:24:19 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 17 Dec 2020 01:24:20 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 17 Dec 2020 01:24:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 01:24:21 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:455793c72b878001f0905634ed52a2524ba51796e7377bf00683a85123f7dce9`  
		Last Modified: Thu, 17 Dec 2020 00:39:18 GMT  
		Size: 2.8 MB (2794130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5db229948ed4f23c5fa2a001626e9894183d373f65ac8caaf8d0737f2d9033`  
		Last Modified: Thu, 17 Dec 2020 01:25:16 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c8410709bb1642c76a0f1c8fa9f0f309c9e173662a87301e2f3df4732d9ee3`  
		Last Modified: Thu, 17 Dec 2020 01:25:27 GMT  
		Size: 42.1 MB (42108752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb354e7ccbca6b3933d05091a9ca0d1ba33ceb1555043143ee59628c872b664`  
		Last Modified: Thu, 17 Dec 2020 01:25:16 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a4e3e62f6116e137fc176d2281871d2181f52caf1cd484c99b37054e614e9e`  
		Last Modified: Thu, 17 Dec 2020 01:25:16 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c0e10dadd218a28f522c0276020dab975fbc50ae6ca58763e9246ada1a60c41`  
		Last Modified: Thu, 17 Dec 2020 01:25:16 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
