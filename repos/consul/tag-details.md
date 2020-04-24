<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `consul`

-	[`consul:0.9`](#consul09)
-	[`consul:0.9.4`](#consul094)
-	[`consul:1.0`](#consul10)
-	[`consul:1.0.8`](#consul108)
-	[`consul:1.1`](#consul11)
-	[`consul:1.1.1`](#consul111)
-	[`consul:1.2`](#consul12)
-	[`consul:1.2.4`](#consul124)
-	[`consul:1.3`](#consul13)
-	[`consul:1.3.1`](#consul131)
-	[`consul:1.4`](#consul14)
-	[`consul:1.4.5`](#consul145)
-	[`consul:1.5`](#consul15)
-	[`consul:1.5.3`](#consul153)
-	[`consul:1.6`](#consul16)
-	[`consul:1.6.4`](#consul164)
-	[`consul:1.7`](#consul17)
-	[`consul:1.7.2`](#consul172)
-	[`consul:latest`](#consullatest)

## `consul:0.9`

```console
$ docker pull consul@sha256:8ab71058e72ad880ffbc5ceb96be7b5cbaae0205126308e745fca0f50a188815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:0.9` - linux; amd64

```console
$ docker pull consul@sha256:c5dc83dce10cde85e81b69e35ea41e0bbdacdf0a548dabd001482075ae27a395
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14581666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8940e357b6bdbb1c47c1a1632c7765b284b627a69262bc6fd6181b33931ad45a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:15:11 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Jan 2020 17:17:29 GMT
ENV CONSUL_VERSION=0.9.4
# Thu, 23 Jan 2020 17:17:30 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Jan 2020 17:17:31 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Jan 2020 17:17:35 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Jan 2020 17:17:36 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Jan 2020 17:17:38 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Jan 2020 17:17:38 GMT
VOLUME [/consul/data]
# Thu, 23 Jan 2020 17:17:38 GMT
EXPOSE 8300
# Thu, 23 Jan 2020 17:17:38 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Jan 2020 17:17:39 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Jan 2020 17:17:39 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 17:17:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 17:17:40 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eddad4b3e0ff70fc3cd94dd63ff91a03452fd185e7c590e4cfd9f13c2b0b0172`  
		Last Modified: Thu, 23 Jan 2020 17:20:28 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebcd1743e6f6912b7484b82019b94682e0c2ec57af17ed92b27af365cf97e79f`  
		Last Modified: Thu, 23 Jan 2020 17:20:36 GMT  
		Size: 11.8 MB (11814266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f42004c8c977650144f1b96957d7e31a2c97a656cf0fc836289cde24a86b8d`  
		Last Modified: Thu, 23 Jan 2020 17:20:28 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d50e5c336e354355843c8bca67d6ff1cf681eff136a085a8c951d29ee554762`  
		Last Modified: Thu, 23 Jan 2020 17:20:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0fe4da42f21bfdd71a1427a509b2eb94632875b29740619b390bd23e54e4d49`  
		Last Modified: Thu, 23 Jan 2020 17:20:28 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:0.9` - linux; arm variant v6

```console
$ docker pull consul@sha256:7567e9daf88ce6f5c3ff06710d7eb7f9956f4acf0613e2b7579ce5ab92c34eb8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13744277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef19efb76fc0cd13439abe95f8ff14ec99374f710debeaf34e6ac84358d8fadf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:44 GMT
ADD file:7dd2657543fac7f63a125194d27bd38a8e472a3076831a2331c43a471794c210 in / 
# Thu, 23 Apr 2020 15:51:45 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 16:53:13 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Apr 2020 16:58:10 GMT
ENV CONSUL_VERSION=0.9.4
# Thu, 23 Apr 2020 16:58:10 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Apr 2020 16:58:13 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Apr 2020 16:58:19 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Apr 2020 16:58:21 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Apr 2020 16:58:23 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 16:58:24 GMT
VOLUME [/consul/data]
# Thu, 23 Apr 2020 16:58:25 GMT
EXPOSE 8300
# Thu, 23 Apr 2020 16:58:25 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Apr 2020 16:58:26 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Apr 2020 16:58:27 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Apr 2020 16:58:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 16:58:29 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:27da80392aebe463671b839837d59af1261218364b4261ceb2eca0f814075270`  
		Last Modified: Thu, 23 Apr 2020 15:52:21 GMT  
		Size: 2.5 MB (2548725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76cd6ccb5c863262652eb924f8fad144167bc57c0d809638215e0b7ee9fbf24b`  
		Last Modified: Thu, 23 Apr 2020 17:01:16 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e33b1c033f4186a0a18e46808783676a25e443b2ef4db7613505f75e3adb683`  
		Last Modified: Thu, 23 Apr 2020 17:01:19 GMT  
		Size: 11.2 MB (11192262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce2b4a49fbd7a45b7e64b1dc4909e585d0c5ac77bdeb3332b39e3c3538c94bf`  
		Last Modified: Thu, 23 Apr 2020 17:01:16 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92133243f7d8f6ea4f2cc13d1ee9ffcc95daa49bc59fbe68f5015626a5bf0f2`  
		Last Modified: Thu, 23 Apr 2020 17:01:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abfe004a5f39aafa0e044b0d38c6724bf0731fdc42d563c3736a01a9541aef70`  
		Last Modified: Thu, 23 Apr 2020 17:01:16 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:0.9` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:702520973c43b475f43e292c994868f8736c5f66f12add272f58705572f358f1
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13789386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d36b08285c9d7d26d8bf2782a491bc712d3a3d0cba7bb7af3e09e441db0606d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:54:58 GMT
ADD file:92767b5525acd9dbf8657931d32bdcc7cc504cdc33c95e84a75e478b00569bab in / 
# Thu, 23 Jan 2020 16:54:59 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:19:49 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Jan 2020 17:23:54 GMT
ENV CONSUL_VERSION=0.9.4
# Thu, 23 Jan 2020 17:23:54 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Jan 2020 17:23:57 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Jan 2020 17:24:02 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Jan 2020 17:24:04 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Jan 2020 17:24:06 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Jan 2020 17:24:07 GMT
VOLUME [/consul/data]
# Thu, 23 Jan 2020 17:24:08 GMT
EXPOSE 8300
# Thu, 23 Jan 2020 17:24:08 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Jan 2020 17:24:09 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Jan 2020 17:24:10 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 17:24:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 17:24:11 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:eb93038481ddcf86a625b70f7551cdc583e38886f206fe7e40ad644008efa815`  
		Last Modified: Thu, 23 Jan 2020 16:55:31 GMT  
		Size: 2.7 MB (2693238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9a35ae03d22d598f34c3da928c9df1b7e124636713866ad031f0da661fc4f5`  
		Last Modified: Thu, 23 Jan 2020 17:27:53 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddbce5dac2f91e5b3d055229e892fac0dfd28a357d6e4be602155d6d692bd1d`  
		Last Modified: Thu, 23 Jan 2020 17:28:00 GMT  
		Size: 11.1 MB (11092860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c15a21030316cfbc6b490af6c31965c1a7e756af92f28e3805c3a893ab9cbf7`  
		Last Modified: Thu, 23 Jan 2020 17:27:53 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7416948ef4f56d8d07606ce587d84828afd30f04dd99ff2b78c23f5c0acdbaf`  
		Last Modified: Thu, 23 Jan 2020 17:27:54 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb0d01e82b8ff8965f3b7e8cb102cc13b16924bac20e67c8b57963f94952703`  
		Last Modified: Thu, 23 Jan 2020 17:27:54 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:0.9` - linux; 386

```console
$ docker pull consul@sha256:31ea1133901a3a61a3c218f49014fac7707d16a3db9728ccc6c905366ecf2726
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14265875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:585de4ef211624baf2105478bcb70e75a11b0e6afb07bcbd420d456db3abbc6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:18 GMT
ADD file:68d5786259963a2b97cf808d79de83cbd0281dfea284e1a401bc851a3585e1bd in / 
# Thu, 23 Apr 2020 21:16:19 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 04:30:33 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Fri, 24 Apr 2020 04:32:14 GMT
ENV CONSUL_VERSION=0.9.4
# Fri, 24 Apr 2020 04:32:15 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 24 Apr 2020 04:32:15 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 24 Apr 2020 04:32:19 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 24 Apr 2020 04:32:19 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 24 Apr 2020 04:32:20 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 04:32:21 GMT
VOLUME [/consul/data]
# Fri, 24 Apr 2020 04:32:21 GMT
EXPOSE 8300
# Fri, 24 Apr 2020 04:32:21 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 24 Apr 2020 04:32:21 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 24 Apr 2020 04:32:21 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Apr 2020 04:32:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 04:32:22 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2f4fdbe0599cb5bbd0664b1cdad4997f428ce2495ae3eabf942129dc197d991c`  
		Last Modified: Thu, 23 Apr 2020 21:16:41 GMT  
		Size: 2.8 MB (2769736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3dde02e4ce4dd058fad4111743215f058954357fc76e8e20fb918adc771dfe3`  
		Last Modified: Fri, 24 Apr 2020 04:34:04 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c1e7e0fb63189ec6bfbb90501d4f96dc49953831824701ae5a10ca0491f5cd`  
		Last Modified: Fri, 24 Apr 2020 04:34:07 GMT  
		Size: 11.5 MB (11492906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b85c312c486461e74b80e7b051099d2df0cd64a79c2696da5a1d88e89819cdf`  
		Last Modified: Fri, 24 Apr 2020 04:34:04 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b13c19a5bad8979d00839c34c4d237be507d819433fdb4e4269ff08a37fd95e9`  
		Last Modified: Fri, 24 Apr 2020 04:34:04 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94136c6ef89b0afa76471ccebd405716f5ddbb1e77c70fd2565218903d226c28`  
		Last Modified: Fri, 24 Apr 2020 04:34:04 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:0.9.4`

```console
$ docker pull consul@sha256:8ab71058e72ad880ffbc5ceb96be7b5cbaae0205126308e745fca0f50a188815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:0.9.4` - linux; amd64

```console
$ docker pull consul@sha256:c5dc83dce10cde85e81b69e35ea41e0bbdacdf0a548dabd001482075ae27a395
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14581666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8940e357b6bdbb1c47c1a1632c7765b284b627a69262bc6fd6181b33931ad45a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:15:11 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Jan 2020 17:17:29 GMT
ENV CONSUL_VERSION=0.9.4
# Thu, 23 Jan 2020 17:17:30 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Jan 2020 17:17:31 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Jan 2020 17:17:35 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Jan 2020 17:17:36 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Jan 2020 17:17:38 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Jan 2020 17:17:38 GMT
VOLUME [/consul/data]
# Thu, 23 Jan 2020 17:17:38 GMT
EXPOSE 8300
# Thu, 23 Jan 2020 17:17:38 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Jan 2020 17:17:39 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Jan 2020 17:17:39 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 17:17:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 17:17:40 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eddad4b3e0ff70fc3cd94dd63ff91a03452fd185e7c590e4cfd9f13c2b0b0172`  
		Last Modified: Thu, 23 Jan 2020 17:20:28 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebcd1743e6f6912b7484b82019b94682e0c2ec57af17ed92b27af365cf97e79f`  
		Last Modified: Thu, 23 Jan 2020 17:20:36 GMT  
		Size: 11.8 MB (11814266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f42004c8c977650144f1b96957d7e31a2c97a656cf0fc836289cde24a86b8d`  
		Last Modified: Thu, 23 Jan 2020 17:20:28 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d50e5c336e354355843c8bca67d6ff1cf681eff136a085a8c951d29ee554762`  
		Last Modified: Thu, 23 Jan 2020 17:20:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0fe4da42f21bfdd71a1427a509b2eb94632875b29740619b390bd23e54e4d49`  
		Last Modified: Thu, 23 Jan 2020 17:20:28 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:0.9.4` - linux; arm variant v6

```console
$ docker pull consul@sha256:7567e9daf88ce6f5c3ff06710d7eb7f9956f4acf0613e2b7579ce5ab92c34eb8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13744277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef19efb76fc0cd13439abe95f8ff14ec99374f710debeaf34e6ac84358d8fadf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:44 GMT
ADD file:7dd2657543fac7f63a125194d27bd38a8e472a3076831a2331c43a471794c210 in / 
# Thu, 23 Apr 2020 15:51:45 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 16:53:13 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Apr 2020 16:58:10 GMT
ENV CONSUL_VERSION=0.9.4
# Thu, 23 Apr 2020 16:58:10 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Apr 2020 16:58:13 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Apr 2020 16:58:19 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Apr 2020 16:58:21 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Apr 2020 16:58:23 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 16:58:24 GMT
VOLUME [/consul/data]
# Thu, 23 Apr 2020 16:58:25 GMT
EXPOSE 8300
# Thu, 23 Apr 2020 16:58:25 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Apr 2020 16:58:26 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Apr 2020 16:58:27 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Apr 2020 16:58:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 16:58:29 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:27da80392aebe463671b839837d59af1261218364b4261ceb2eca0f814075270`  
		Last Modified: Thu, 23 Apr 2020 15:52:21 GMT  
		Size: 2.5 MB (2548725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76cd6ccb5c863262652eb924f8fad144167bc57c0d809638215e0b7ee9fbf24b`  
		Last Modified: Thu, 23 Apr 2020 17:01:16 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e33b1c033f4186a0a18e46808783676a25e443b2ef4db7613505f75e3adb683`  
		Last Modified: Thu, 23 Apr 2020 17:01:19 GMT  
		Size: 11.2 MB (11192262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce2b4a49fbd7a45b7e64b1dc4909e585d0c5ac77bdeb3332b39e3c3538c94bf`  
		Last Modified: Thu, 23 Apr 2020 17:01:16 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92133243f7d8f6ea4f2cc13d1ee9ffcc95daa49bc59fbe68f5015626a5bf0f2`  
		Last Modified: Thu, 23 Apr 2020 17:01:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abfe004a5f39aafa0e044b0d38c6724bf0731fdc42d563c3736a01a9541aef70`  
		Last Modified: Thu, 23 Apr 2020 17:01:16 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:0.9.4` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:702520973c43b475f43e292c994868f8736c5f66f12add272f58705572f358f1
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13789386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d36b08285c9d7d26d8bf2782a491bc712d3a3d0cba7bb7af3e09e441db0606d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:54:58 GMT
ADD file:92767b5525acd9dbf8657931d32bdcc7cc504cdc33c95e84a75e478b00569bab in / 
# Thu, 23 Jan 2020 16:54:59 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:19:49 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Jan 2020 17:23:54 GMT
ENV CONSUL_VERSION=0.9.4
# Thu, 23 Jan 2020 17:23:54 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Jan 2020 17:23:57 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Jan 2020 17:24:02 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Jan 2020 17:24:04 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Jan 2020 17:24:06 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Jan 2020 17:24:07 GMT
VOLUME [/consul/data]
# Thu, 23 Jan 2020 17:24:08 GMT
EXPOSE 8300
# Thu, 23 Jan 2020 17:24:08 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Jan 2020 17:24:09 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Jan 2020 17:24:10 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 17:24:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 17:24:11 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:eb93038481ddcf86a625b70f7551cdc583e38886f206fe7e40ad644008efa815`  
		Last Modified: Thu, 23 Jan 2020 16:55:31 GMT  
		Size: 2.7 MB (2693238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9a35ae03d22d598f34c3da928c9df1b7e124636713866ad031f0da661fc4f5`  
		Last Modified: Thu, 23 Jan 2020 17:27:53 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddbce5dac2f91e5b3d055229e892fac0dfd28a357d6e4be602155d6d692bd1d`  
		Last Modified: Thu, 23 Jan 2020 17:28:00 GMT  
		Size: 11.1 MB (11092860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c15a21030316cfbc6b490af6c31965c1a7e756af92f28e3805c3a893ab9cbf7`  
		Last Modified: Thu, 23 Jan 2020 17:27:53 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7416948ef4f56d8d07606ce587d84828afd30f04dd99ff2b78c23f5c0acdbaf`  
		Last Modified: Thu, 23 Jan 2020 17:27:54 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb0d01e82b8ff8965f3b7e8cb102cc13b16924bac20e67c8b57963f94952703`  
		Last Modified: Thu, 23 Jan 2020 17:27:54 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:0.9.4` - linux; 386

```console
$ docker pull consul@sha256:31ea1133901a3a61a3c218f49014fac7707d16a3db9728ccc6c905366ecf2726
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14265875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:585de4ef211624baf2105478bcb70e75a11b0e6afb07bcbd420d456db3abbc6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:18 GMT
ADD file:68d5786259963a2b97cf808d79de83cbd0281dfea284e1a401bc851a3585e1bd in / 
# Thu, 23 Apr 2020 21:16:19 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 04:30:33 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Fri, 24 Apr 2020 04:32:14 GMT
ENV CONSUL_VERSION=0.9.4
# Fri, 24 Apr 2020 04:32:15 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 24 Apr 2020 04:32:15 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 24 Apr 2020 04:32:19 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 24 Apr 2020 04:32:19 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 24 Apr 2020 04:32:20 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 04:32:21 GMT
VOLUME [/consul/data]
# Fri, 24 Apr 2020 04:32:21 GMT
EXPOSE 8300
# Fri, 24 Apr 2020 04:32:21 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 24 Apr 2020 04:32:21 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 24 Apr 2020 04:32:21 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Apr 2020 04:32:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 04:32:22 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2f4fdbe0599cb5bbd0664b1cdad4997f428ce2495ae3eabf942129dc197d991c`  
		Last Modified: Thu, 23 Apr 2020 21:16:41 GMT  
		Size: 2.8 MB (2769736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3dde02e4ce4dd058fad4111743215f058954357fc76e8e20fb918adc771dfe3`  
		Last Modified: Fri, 24 Apr 2020 04:34:04 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c1e7e0fb63189ec6bfbb90501d4f96dc49953831824701ae5a10ca0491f5cd`  
		Last Modified: Fri, 24 Apr 2020 04:34:07 GMT  
		Size: 11.5 MB (11492906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b85c312c486461e74b80e7b051099d2df0cd64a79c2696da5a1d88e89819cdf`  
		Last Modified: Fri, 24 Apr 2020 04:34:04 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b13c19a5bad8979d00839c34c4d237be507d819433fdb4e4269ff08a37fd95e9`  
		Last Modified: Fri, 24 Apr 2020 04:34:04 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94136c6ef89b0afa76471ccebd405716f5ddbb1e77c70fd2565218903d226c28`  
		Last Modified: Fri, 24 Apr 2020 04:34:04 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.0`

```console
$ docker pull consul@sha256:3871d38fa96388f05f1c942ea095d1bcf067beffe19e9a4dfba34e8b6b51cfcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.0` - linux; amd64

```console
$ docker pull consul@sha256:9942f0518293aa00ae0d6439f5074bd48e83b0e4e9f21e18ba3e9976668b7dbd
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16595618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cbb12477735f3eb626b19b811ea28e7149aeafd5f47563becb8aa6b6fc9a88e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:15:11 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Jan 2020 17:17:14 GMT
ENV CONSUL_VERSION=1.0.8
# Thu, 23 Jan 2020 17:17:14 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Jan 2020 17:17:16 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Jan 2020 17:17:20 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Jan 2020 17:17:21 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Jan 2020 17:17:22 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Jan 2020 17:17:23 GMT
VOLUME [/consul/data]
# Thu, 23 Jan 2020 17:17:23 GMT
EXPOSE 8300
# Thu, 23 Jan 2020 17:17:23 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Jan 2020 17:17:23 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Jan 2020 17:17:24 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 17:17:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 17:17:24 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299a735925e960bfb965103741eb84a295fcd5a8859074cadd495564d41ce2c6`  
		Last Modified: Thu, 23 Jan 2020 17:20:19 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eecfab37a9845176e6c457eead6da1e495088da00c448e95556de198a9d5a99`  
		Last Modified: Thu, 23 Jan 2020 17:20:23 GMT  
		Size: 13.8 MB (13828214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94c3d997d679c833acef18a377aabb870578d73991dd031501b59520d5b1068`  
		Last Modified: Thu, 23 Jan 2020 17:20:19 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f7ba4eb550de2fd79fc9f84acc66a0de6bec680408ead05b69ab53fc158329`  
		Last Modified: Thu, 23 Jan 2020 17:20:19 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66ce656d5b4660e3baf0c4e5b9537bf8dc221ebae1bb581ca049ed997398eee`  
		Last Modified: Thu, 23 Jan 2020 17:20:19 GMT  
		Size: 1.7 KB (1680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.0` - linux; arm variant v6

```console
$ docker pull consul@sha256:8ed068a4e959077cf3763ea930cafdfa67faad921b172d853c503548fa23b09f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15927267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a8ea9bd4bd84c23339c822cc1d664f27f2fb430d174cd40a15ddd102098268`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:44 GMT
ADD file:7dd2657543fac7f63a125194d27bd38a8e472a3076831a2331c43a471794c210 in / 
# Thu, 23 Apr 2020 15:51:45 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 16:53:13 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Apr 2020 16:57:39 GMT
ENV CONSUL_VERSION=1.0.8
# Thu, 23 Apr 2020 16:57:40 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Apr 2020 16:57:42 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Apr 2020 16:57:49 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Apr 2020 16:57:55 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Apr 2020 16:57:58 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 16:57:58 GMT
VOLUME [/consul/data]
# Thu, 23 Apr 2020 16:57:59 GMT
EXPOSE 8300
# Thu, 23 Apr 2020 16:58:00 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Apr 2020 16:58:01 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Apr 2020 16:58:02 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Apr 2020 16:58:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 16:58:03 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:27da80392aebe463671b839837d59af1261218364b4261ceb2eca0f814075270`  
		Last Modified: Thu, 23 Apr 2020 15:52:21 GMT  
		Size: 2.5 MB (2548725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7f1ec021b4538db3c83f84b62bb94da1519016e0073c4f5148322e57043678`  
		Last Modified: Thu, 23 Apr 2020 17:01:02 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1d832c9019f7acf2ca2a1b554704ed90a4fd3815998118c9ab8f2d5700daa0`  
		Last Modified: Thu, 23 Apr 2020 17:01:07 GMT  
		Size: 13.4 MB (13375251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1973747b0151219f88c7cab68412c0aaa44445791287c96a838bc3d0cca8018e`  
		Last Modified: Thu, 23 Apr 2020 17:01:01 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50cb5fffaf1ddd735c3e52e4ca181126c92329f3d43ef2cb6b38869f87e661a`  
		Last Modified: Thu, 23 Apr 2020 17:01:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f475845735cc1de22cdcb0faeadf59b78ecbb89fe44f32adcc5986d73eaae827`  
		Last Modified: Thu, 23 Apr 2020 17:01:02 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.0` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:a4ad77f0ab5e582b7fbbfd0b5c24a3ba0ddcc6958e17cab54a39a46a59aab36c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15937701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615191e2ff98d07c86cf3a061b752808ba17abd0932c3ad79c9b8a88bc10f478`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:54:58 GMT
ADD file:92767b5525acd9dbf8657931d32bdcc7cc504cdc33c95e84a75e478b00569bab in / 
# Thu, 23 Jan 2020 16:54:59 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:19:49 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Jan 2020 17:23:29 GMT
ENV CONSUL_VERSION=1.0.8
# Thu, 23 Jan 2020 17:23:30 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Jan 2020 17:23:32 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Jan 2020 17:23:37 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Jan 2020 17:23:39 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Jan 2020 17:23:41 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Jan 2020 17:23:42 GMT
VOLUME [/consul/data]
# Thu, 23 Jan 2020 17:23:42 GMT
EXPOSE 8300
# Thu, 23 Jan 2020 17:23:43 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Jan 2020 17:23:44 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Jan 2020 17:23:44 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 17:23:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 17:23:46 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:eb93038481ddcf86a625b70f7551cdc583e38886f206fe7e40ad644008efa815`  
		Last Modified: Thu, 23 Jan 2020 16:55:31 GMT  
		Size: 2.7 MB (2693238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90f67b753ffa58715006a169c5bc0fc97254389a09fc4d2994d6ecfa462ad612`  
		Last Modified: Thu, 23 Jan 2020 17:27:41 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca863c51b1fd31d8934a25dcedc9a2ecbce9637b5f5eeca7e05791f31c928827`  
		Last Modified: Thu, 23 Jan 2020 17:27:46 GMT  
		Size: 13.2 MB (13241178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d957ab1b179315468f071fd09af8b8cf4ecb5c5738227aabb8e21f30ba0f6c15`  
		Last Modified: Thu, 23 Jan 2020 17:27:41 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48b27b30d4ccd928a8dfa42042e7addf3b950bf32e1611f2db862000773c793`  
		Last Modified: Thu, 23 Jan 2020 17:27:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5be6bcaf9e62af8f545358f75e3aceb0d225ce628d5d51f05ac1cb6a467a5a`  
		Last Modified: Thu, 23 Jan 2020 17:27:41 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.0` - linux; 386

```console
$ docker pull consul@sha256:1d77c81c3039fad28156b6e55137082061933af879bac32bdf2793ea8fad9f8a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16488482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e0d131c2161d7707dc210fe3845fa107d1bdf531574631e8ae38a417c3b9198`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:18 GMT
ADD file:68d5786259963a2b97cf808d79de83cbd0281dfea284e1a401bc851a3585e1bd in / 
# Thu, 23 Apr 2020 21:16:19 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 04:30:33 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Fri, 24 Apr 2020 04:32:04 GMT
ENV CONSUL_VERSION=1.0.8
# Fri, 24 Apr 2020 04:32:04 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 24 Apr 2020 04:32:05 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 24 Apr 2020 04:32:08 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 24 Apr 2020 04:32:09 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 24 Apr 2020 04:32:10 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 04:32:10 GMT
VOLUME [/consul/data]
# Fri, 24 Apr 2020 04:32:10 GMT
EXPOSE 8300
# Fri, 24 Apr 2020 04:32:10 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 24 Apr 2020 04:32:10 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 24 Apr 2020 04:32:11 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Apr 2020 04:32:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 04:32:11 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2f4fdbe0599cb5bbd0664b1cdad4997f428ce2495ae3eabf942129dc197d991c`  
		Last Modified: Thu, 23 Apr 2020 21:16:41 GMT  
		Size: 2.8 MB (2769736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850240b833ceb1a2c21f19767158367cc05e0dfce3b9ab8400783540669769d3`  
		Last Modified: Fri, 24 Apr 2020 04:33:55 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c56ab7d56e42aabf7140922618da2a3da26d2ca704983eeafa728c0c1e91c1`  
		Last Modified: Fri, 24 Apr 2020 04:33:59 GMT  
		Size: 13.7 MB (13715515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16846dd8889e312196cb104f75ff12d5ebfebc6e9e0e4d6009ba0f3e8f1c464`  
		Last Modified: Fri, 24 Apr 2020 04:33:55 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b35ea71b0133f4d25007c58be12051c0cfd1ecc56c0319920da065e220f7ed6`  
		Last Modified: Fri, 24 Apr 2020 04:33:55 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a089445a55f289bec444acc9e912f021d47dcd4e8c6c3a9c7d05bdf6d4fb03`  
		Last Modified: Fri, 24 Apr 2020 04:33:55 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.0.8`

```console
$ docker pull consul@sha256:3871d38fa96388f05f1c942ea095d1bcf067beffe19e9a4dfba34e8b6b51cfcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.0.8` - linux; amd64

```console
$ docker pull consul@sha256:9942f0518293aa00ae0d6439f5074bd48e83b0e4e9f21e18ba3e9976668b7dbd
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16595618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cbb12477735f3eb626b19b811ea28e7149aeafd5f47563becb8aa6b6fc9a88e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:15:11 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Jan 2020 17:17:14 GMT
ENV CONSUL_VERSION=1.0.8
# Thu, 23 Jan 2020 17:17:14 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Jan 2020 17:17:16 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Jan 2020 17:17:20 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Jan 2020 17:17:21 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Jan 2020 17:17:22 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Jan 2020 17:17:23 GMT
VOLUME [/consul/data]
# Thu, 23 Jan 2020 17:17:23 GMT
EXPOSE 8300
# Thu, 23 Jan 2020 17:17:23 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Jan 2020 17:17:23 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Jan 2020 17:17:24 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 17:17:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 17:17:24 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299a735925e960bfb965103741eb84a295fcd5a8859074cadd495564d41ce2c6`  
		Last Modified: Thu, 23 Jan 2020 17:20:19 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eecfab37a9845176e6c457eead6da1e495088da00c448e95556de198a9d5a99`  
		Last Modified: Thu, 23 Jan 2020 17:20:23 GMT  
		Size: 13.8 MB (13828214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94c3d997d679c833acef18a377aabb870578d73991dd031501b59520d5b1068`  
		Last Modified: Thu, 23 Jan 2020 17:20:19 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f7ba4eb550de2fd79fc9f84acc66a0de6bec680408ead05b69ab53fc158329`  
		Last Modified: Thu, 23 Jan 2020 17:20:19 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66ce656d5b4660e3baf0c4e5b9537bf8dc221ebae1bb581ca049ed997398eee`  
		Last Modified: Thu, 23 Jan 2020 17:20:19 GMT  
		Size: 1.7 KB (1680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.0.8` - linux; arm variant v6

```console
$ docker pull consul@sha256:8ed068a4e959077cf3763ea930cafdfa67faad921b172d853c503548fa23b09f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15927267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a8ea9bd4bd84c23339c822cc1d664f27f2fb430d174cd40a15ddd102098268`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:44 GMT
ADD file:7dd2657543fac7f63a125194d27bd38a8e472a3076831a2331c43a471794c210 in / 
# Thu, 23 Apr 2020 15:51:45 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 16:53:13 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Apr 2020 16:57:39 GMT
ENV CONSUL_VERSION=1.0.8
# Thu, 23 Apr 2020 16:57:40 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Apr 2020 16:57:42 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Apr 2020 16:57:49 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Apr 2020 16:57:55 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Apr 2020 16:57:58 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 16:57:58 GMT
VOLUME [/consul/data]
# Thu, 23 Apr 2020 16:57:59 GMT
EXPOSE 8300
# Thu, 23 Apr 2020 16:58:00 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Apr 2020 16:58:01 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Apr 2020 16:58:02 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Apr 2020 16:58:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 16:58:03 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:27da80392aebe463671b839837d59af1261218364b4261ceb2eca0f814075270`  
		Last Modified: Thu, 23 Apr 2020 15:52:21 GMT  
		Size: 2.5 MB (2548725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7f1ec021b4538db3c83f84b62bb94da1519016e0073c4f5148322e57043678`  
		Last Modified: Thu, 23 Apr 2020 17:01:02 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1d832c9019f7acf2ca2a1b554704ed90a4fd3815998118c9ab8f2d5700daa0`  
		Last Modified: Thu, 23 Apr 2020 17:01:07 GMT  
		Size: 13.4 MB (13375251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1973747b0151219f88c7cab68412c0aaa44445791287c96a838bc3d0cca8018e`  
		Last Modified: Thu, 23 Apr 2020 17:01:01 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50cb5fffaf1ddd735c3e52e4ca181126c92329f3d43ef2cb6b38869f87e661a`  
		Last Modified: Thu, 23 Apr 2020 17:01:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f475845735cc1de22cdcb0faeadf59b78ecbb89fe44f32adcc5986d73eaae827`  
		Last Modified: Thu, 23 Apr 2020 17:01:02 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.0.8` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:a4ad77f0ab5e582b7fbbfd0b5c24a3ba0ddcc6958e17cab54a39a46a59aab36c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15937701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615191e2ff98d07c86cf3a061b752808ba17abd0932c3ad79c9b8a88bc10f478`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:54:58 GMT
ADD file:92767b5525acd9dbf8657931d32bdcc7cc504cdc33c95e84a75e478b00569bab in / 
# Thu, 23 Jan 2020 16:54:59 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:19:49 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Jan 2020 17:23:29 GMT
ENV CONSUL_VERSION=1.0.8
# Thu, 23 Jan 2020 17:23:30 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Jan 2020 17:23:32 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Jan 2020 17:23:37 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Jan 2020 17:23:39 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Jan 2020 17:23:41 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Jan 2020 17:23:42 GMT
VOLUME [/consul/data]
# Thu, 23 Jan 2020 17:23:42 GMT
EXPOSE 8300
# Thu, 23 Jan 2020 17:23:43 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Jan 2020 17:23:44 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Jan 2020 17:23:44 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 17:23:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 17:23:46 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:eb93038481ddcf86a625b70f7551cdc583e38886f206fe7e40ad644008efa815`  
		Last Modified: Thu, 23 Jan 2020 16:55:31 GMT  
		Size: 2.7 MB (2693238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90f67b753ffa58715006a169c5bc0fc97254389a09fc4d2994d6ecfa462ad612`  
		Last Modified: Thu, 23 Jan 2020 17:27:41 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca863c51b1fd31d8934a25dcedc9a2ecbce9637b5f5eeca7e05791f31c928827`  
		Last Modified: Thu, 23 Jan 2020 17:27:46 GMT  
		Size: 13.2 MB (13241178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d957ab1b179315468f071fd09af8b8cf4ecb5c5738227aabb8e21f30ba0f6c15`  
		Last Modified: Thu, 23 Jan 2020 17:27:41 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48b27b30d4ccd928a8dfa42042e7addf3b950bf32e1611f2db862000773c793`  
		Last Modified: Thu, 23 Jan 2020 17:27:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5be6bcaf9e62af8f545358f75e3aceb0d225ce628d5d51f05ac1cb6a467a5a`  
		Last Modified: Thu, 23 Jan 2020 17:27:41 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.0.8` - linux; 386

```console
$ docker pull consul@sha256:1d77c81c3039fad28156b6e55137082061933af879bac32bdf2793ea8fad9f8a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16488482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e0d131c2161d7707dc210fe3845fa107d1bdf531574631e8ae38a417c3b9198`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:18 GMT
ADD file:68d5786259963a2b97cf808d79de83cbd0281dfea284e1a401bc851a3585e1bd in / 
# Thu, 23 Apr 2020 21:16:19 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 04:30:33 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Fri, 24 Apr 2020 04:32:04 GMT
ENV CONSUL_VERSION=1.0.8
# Fri, 24 Apr 2020 04:32:04 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 24 Apr 2020 04:32:05 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 24 Apr 2020 04:32:08 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 24 Apr 2020 04:32:09 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 24 Apr 2020 04:32:10 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 04:32:10 GMT
VOLUME [/consul/data]
# Fri, 24 Apr 2020 04:32:10 GMT
EXPOSE 8300
# Fri, 24 Apr 2020 04:32:10 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 24 Apr 2020 04:32:10 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 24 Apr 2020 04:32:11 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Apr 2020 04:32:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 04:32:11 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2f4fdbe0599cb5bbd0664b1cdad4997f428ce2495ae3eabf942129dc197d991c`  
		Last Modified: Thu, 23 Apr 2020 21:16:41 GMT  
		Size: 2.8 MB (2769736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850240b833ceb1a2c21f19767158367cc05e0dfce3b9ab8400783540669769d3`  
		Last Modified: Fri, 24 Apr 2020 04:33:55 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c56ab7d56e42aabf7140922618da2a3da26d2ca704983eeafa728c0c1e91c1`  
		Last Modified: Fri, 24 Apr 2020 04:33:59 GMT  
		Size: 13.7 MB (13715515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16846dd8889e312196cb104f75ff12d5ebfebc6e9e0e4d6009ba0f3e8f1c464`  
		Last Modified: Fri, 24 Apr 2020 04:33:55 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b35ea71b0133f4d25007c58be12051c0cfd1ecc56c0319920da065e220f7ed6`  
		Last Modified: Fri, 24 Apr 2020 04:33:55 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a089445a55f289bec444acc9e912f021d47dcd4e8c6c3a9c7d05bdf6d4fb03`  
		Last Modified: Fri, 24 Apr 2020 04:33:55 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.1`

```console
$ docker pull consul@sha256:042b0a618921b6ab9f21e60c8d42204555d420bcd30f3909d7812fdaed5e2749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.1` - linux; amd64

```console
$ docker pull consul@sha256:aedb271ea421fd2ee887a277561f91aae8d16974fafc83e9ebc661b98c81d3b3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18060530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c84316bdbffdd5d803370f5bb4aee5ca44095cca1945a0497ea1f5ed9cee6b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:15:11 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Jan 2020 17:16:59 GMT
ENV CONSUL_VERSION=1.1.1
# Thu, 23 Jan 2020 17:16:59 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Jan 2020 17:17:00 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Jan 2020 17:17:05 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Jan 2020 17:17:07 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Jan 2020 17:17:08 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Jan 2020 17:17:08 GMT
VOLUME [/consul/data]
# Thu, 23 Jan 2020 17:17:08 GMT
EXPOSE 8300
# Thu, 23 Jan 2020 17:17:09 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Jan 2020 17:17:09 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Jan 2020 17:17:09 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 17:17:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 17:17:10 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc1e00ae4e082537fd3e9c26ce3f3b4f8f2228a8253ce4708d780b1204de609`  
		Last Modified: Thu, 23 Jan 2020 17:20:02 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b6c21e5e36bcf90f10f67bebf2da4ab0231b886781a5eb881a4d6e1cb085ee`  
		Last Modified: Thu, 23 Jan 2020 17:20:15 GMT  
		Size: 15.3 MB (15293128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4bfa000875e68bccfd819005555b8933cac08802ca05c3513233a6cb83ed901`  
		Last Modified: Thu, 23 Jan 2020 17:20:02 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39c82f8ebb31874c3a37c3ca7f52ea3e32927c59376c2627c03052c416137ac`  
		Last Modified: Thu, 23 Jan 2020 17:20:02 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29feee2c223abf0f89639b4626ea25459b42054765d588bd4aca36a9725ff32f`  
		Last Modified: Thu, 23 Jan 2020 17:20:02 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.1` - linux; arm variant v6

```console
$ docker pull consul@sha256:a0fa5de1a39eed6614e477f3e3319c99495493dd5d5c1e8b74bbc94e0db62bdb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17390617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d02828dfd615d155ebe7e24a956db44dba5c23d3b32d55bd6e4f0a3957602eee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:44 GMT
ADD file:7dd2657543fac7f63a125194d27bd38a8e472a3076831a2331c43a471794c210 in / 
# Thu, 23 Apr 2020 15:51:45 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 16:53:13 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Apr 2020 16:57:03 GMT
ENV CONSUL_VERSION=1.1.1
# Thu, 23 Apr 2020 16:57:04 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Apr 2020 16:57:05 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Apr 2020 16:57:12 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Apr 2020 16:57:21 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Apr 2020 16:57:25 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 16:57:26 GMT
VOLUME [/consul/data]
# Thu, 23 Apr 2020 16:57:26 GMT
EXPOSE 8300
# Thu, 23 Apr 2020 16:57:27 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Apr 2020 16:57:28 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Apr 2020 16:57:28 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Apr 2020 16:57:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 16:57:29 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:27da80392aebe463671b839837d59af1261218364b4261ceb2eca0f814075270`  
		Last Modified: Thu, 23 Apr 2020 15:52:21 GMT  
		Size: 2.5 MB (2548725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1a16aa19bbf6b544dc6929c42ee2bdd9f4e744998365e9c33316b04c835ada`  
		Last Modified: Thu, 23 Apr 2020 17:00:50 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f49072c61926a893f1cab6572bcafbc9879a83b81b4cc9f7ce195723a64ac2`  
		Last Modified: Thu, 23 Apr 2020 17:00:55 GMT  
		Size: 14.8 MB (14838606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb7df641eaf55de68bf5895395ab1b3226e4f5b0b0a529021349bfb8099e36e`  
		Last Modified: Thu, 23 Apr 2020 17:00:50 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7b10f5e9dee1a269b0d214de927b08485c0139d30e80396f9b061d589aee59e`  
		Last Modified: Thu, 23 Apr 2020 17:00:50 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7c40f6de602110916c804223738d168850c5db10e634ef04a8a4e8f7e71350`  
		Last Modified: Thu, 23 Apr 2020 17:00:50 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.1` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:02eb2dde0d018065a76a70cae855a202c84ac6a3110b68618d48a53ba29a96cd
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17374078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d935f232d5588eafa4f0684f9df8dd18019458d059d7cb013dac2211e4004a82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:54:58 GMT
ADD file:92767b5525acd9dbf8657931d32bdcc7cc504cdc33c95e84a75e478b00569bab in / 
# Thu, 23 Jan 2020 16:54:59 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:19:49 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Jan 2020 17:23:04 GMT
ENV CONSUL_VERSION=1.1.1
# Thu, 23 Jan 2020 17:23:04 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Jan 2020 17:23:06 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Jan 2020 17:23:11 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Jan 2020 17:23:14 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Jan 2020 17:23:15 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Jan 2020 17:23:16 GMT
VOLUME [/consul/data]
# Thu, 23 Jan 2020 17:23:17 GMT
EXPOSE 8300
# Thu, 23 Jan 2020 17:23:18 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Jan 2020 17:23:19 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Jan 2020 17:23:19 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 17:23:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 17:23:21 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:eb93038481ddcf86a625b70f7551cdc583e38886f206fe7e40ad644008efa815`  
		Last Modified: Thu, 23 Jan 2020 16:55:31 GMT  
		Size: 2.7 MB (2693238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de208071910e8a219ffff4644d9cfe2b6d6c0dfe7f65e1e2f4efeda76e44fe0`  
		Last Modified: Thu, 23 Jan 2020 17:27:29 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:025019ed2ed7b39bcc56028d228b5687941f0f9af8ec077d779fc0046d53a5b8`  
		Last Modified: Thu, 23 Jan 2020 17:27:35 GMT  
		Size: 14.7 MB (14677552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ee18ebf1c4e1ec04ee4d405e4bb74eda52a1c7b53bd50bd1285fce31ecb7f0`  
		Last Modified: Thu, 23 Jan 2020 17:27:29 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b0fd5160a24d544362517f237ec81e53f1fe7f662b783da54679338246a5c9`  
		Last Modified: Thu, 23 Jan 2020 17:27:30 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59490a75b95de035d3d2c2d69fe7d92a3165c0552dcabeaa8e9c765b9385201f`  
		Last Modified: Thu, 23 Jan 2020 17:27:30 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.1` - linux; 386

```console
$ docker pull consul@sha256:e1a43e2d64d69c8d3653ee646430183e08556e6feac71e79beb0015c7eafd8e4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17960253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7b4ecea4861c81a2ed5fd1ec5222d0802c39a3c66efc6e147dcd6b056cd931`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:18 GMT
ADD file:68d5786259963a2b97cf808d79de83cbd0281dfea284e1a401bc851a3585e1bd in / 
# Thu, 23 Apr 2020 21:16:19 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 04:30:33 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Fri, 24 Apr 2020 04:31:53 GMT
ENV CONSUL_VERSION=1.1.1
# Fri, 24 Apr 2020 04:31:53 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 24 Apr 2020 04:31:54 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 24 Apr 2020 04:31:57 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 24 Apr 2020 04:31:58 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 24 Apr 2020 04:31:59 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 04:31:59 GMT
VOLUME [/consul/data]
# Fri, 24 Apr 2020 04:31:59 GMT
EXPOSE 8300
# Fri, 24 Apr 2020 04:31:59 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 24 Apr 2020 04:31:59 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 24 Apr 2020 04:32:00 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Apr 2020 04:32:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 04:32:00 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2f4fdbe0599cb5bbd0664b1cdad4997f428ce2495ae3eabf942129dc197d991c`  
		Last Modified: Thu, 23 Apr 2020 21:16:41 GMT  
		Size: 2.8 MB (2769736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d29818b9044046d6411c4fc801bc923c8c1b927e298e7ab2dc918a838551d939`  
		Last Modified: Fri, 24 Apr 2020 04:33:41 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82024872e9d3c48b8ecf7cee0fa0cb357e20c4a5d47aae161597e702689529f1`  
		Last Modified: Fri, 24 Apr 2020 04:33:44 GMT  
		Size: 15.2 MB (15187288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9848c4a2e774d7260fd7abd8bf55c21b93d4739a5d97d669f3a4415854e1f65a`  
		Last Modified: Fri, 24 Apr 2020 04:33:40 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fccc47ff63aef6639dcec62889f890b94c256ee6ced64bd35573e0081810c0e6`  
		Last Modified: Fri, 24 Apr 2020 04:33:41 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce866c09d565e3efb843bc7c65209d46b5acc12a8a922c95b12f72a13ac1de67`  
		Last Modified: Fri, 24 Apr 2020 04:33:40 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.1.1`

```console
$ docker pull consul@sha256:042b0a618921b6ab9f21e60c8d42204555d420bcd30f3909d7812fdaed5e2749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.1.1` - linux; amd64

```console
$ docker pull consul@sha256:aedb271ea421fd2ee887a277561f91aae8d16974fafc83e9ebc661b98c81d3b3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18060530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c84316bdbffdd5d803370f5bb4aee5ca44095cca1945a0497ea1f5ed9cee6b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:15:11 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Jan 2020 17:16:59 GMT
ENV CONSUL_VERSION=1.1.1
# Thu, 23 Jan 2020 17:16:59 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Jan 2020 17:17:00 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Jan 2020 17:17:05 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Jan 2020 17:17:07 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Jan 2020 17:17:08 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Jan 2020 17:17:08 GMT
VOLUME [/consul/data]
# Thu, 23 Jan 2020 17:17:08 GMT
EXPOSE 8300
# Thu, 23 Jan 2020 17:17:09 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Jan 2020 17:17:09 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Jan 2020 17:17:09 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 17:17:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 17:17:10 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc1e00ae4e082537fd3e9c26ce3f3b4f8f2228a8253ce4708d780b1204de609`  
		Last Modified: Thu, 23 Jan 2020 17:20:02 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b6c21e5e36bcf90f10f67bebf2da4ab0231b886781a5eb881a4d6e1cb085ee`  
		Last Modified: Thu, 23 Jan 2020 17:20:15 GMT  
		Size: 15.3 MB (15293128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4bfa000875e68bccfd819005555b8933cac08802ca05c3513233a6cb83ed901`  
		Last Modified: Thu, 23 Jan 2020 17:20:02 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39c82f8ebb31874c3a37c3ca7f52ea3e32927c59376c2627c03052c416137ac`  
		Last Modified: Thu, 23 Jan 2020 17:20:02 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29feee2c223abf0f89639b4626ea25459b42054765d588bd4aca36a9725ff32f`  
		Last Modified: Thu, 23 Jan 2020 17:20:02 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.1.1` - linux; arm variant v6

```console
$ docker pull consul@sha256:a0fa5de1a39eed6614e477f3e3319c99495493dd5d5c1e8b74bbc94e0db62bdb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17390617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d02828dfd615d155ebe7e24a956db44dba5c23d3b32d55bd6e4f0a3957602eee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:44 GMT
ADD file:7dd2657543fac7f63a125194d27bd38a8e472a3076831a2331c43a471794c210 in / 
# Thu, 23 Apr 2020 15:51:45 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 16:53:13 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Apr 2020 16:57:03 GMT
ENV CONSUL_VERSION=1.1.1
# Thu, 23 Apr 2020 16:57:04 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Apr 2020 16:57:05 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Apr 2020 16:57:12 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Apr 2020 16:57:21 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Apr 2020 16:57:25 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 16:57:26 GMT
VOLUME [/consul/data]
# Thu, 23 Apr 2020 16:57:26 GMT
EXPOSE 8300
# Thu, 23 Apr 2020 16:57:27 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Apr 2020 16:57:28 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Apr 2020 16:57:28 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Apr 2020 16:57:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 16:57:29 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:27da80392aebe463671b839837d59af1261218364b4261ceb2eca0f814075270`  
		Last Modified: Thu, 23 Apr 2020 15:52:21 GMT  
		Size: 2.5 MB (2548725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1a16aa19bbf6b544dc6929c42ee2bdd9f4e744998365e9c33316b04c835ada`  
		Last Modified: Thu, 23 Apr 2020 17:00:50 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f49072c61926a893f1cab6572bcafbc9879a83b81b4cc9f7ce195723a64ac2`  
		Last Modified: Thu, 23 Apr 2020 17:00:55 GMT  
		Size: 14.8 MB (14838606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb7df641eaf55de68bf5895395ab1b3226e4f5b0b0a529021349bfb8099e36e`  
		Last Modified: Thu, 23 Apr 2020 17:00:50 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7b10f5e9dee1a269b0d214de927b08485c0139d30e80396f9b061d589aee59e`  
		Last Modified: Thu, 23 Apr 2020 17:00:50 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7c40f6de602110916c804223738d168850c5db10e634ef04a8a4e8f7e71350`  
		Last Modified: Thu, 23 Apr 2020 17:00:50 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.1.1` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:02eb2dde0d018065a76a70cae855a202c84ac6a3110b68618d48a53ba29a96cd
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17374078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d935f232d5588eafa4f0684f9df8dd18019458d059d7cb013dac2211e4004a82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:54:58 GMT
ADD file:92767b5525acd9dbf8657931d32bdcc7cc504cdc33c95e84a75e478b00569bab in / 
# Thu, 23 Jan 2020 16:54:59 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:19:49 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Jan 2020 17:23:04 GMT
ENV CONSUL_VERSION=1.1.1
# Thu, 23 Jan 2020 17:23:04 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Jan 2020 17:23:06 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Jan 2020 17:23:11 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Jan 2020 17:23:14 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Jan 2020 17:23:15 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Jan 2020 17:23:16 GMT
VOLUME [/consul/data]
# Thu, 23 Jan 2020 17:23:17 GMT
EXPOSE 8300
# Thu, 23 Jan 2020 17:23:18 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Jan 2020 17:23:19 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Jan 2020 17:23:19 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 17:23:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 17:23:21 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:eb93038481ddcf86a625b70f7551cdc583e38886f206fe7e40ad644008efa815`  
		Last Modified: Thu, 23 Jan 2020 16:55:31 GMT  
		Size: 2.7 MB (2693238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de208071910e8a219ffff4644d9cfe2b6d6c0dfe7f65e1e2f4efeda76e44fe0`  
		Last Modified: Thu, 23 Jan 2020 17:27:29 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:025019ed2ed7b39bcc56028d228b5687941f0f9af8ec077d779fc0046d53a5b8`  
		Last Modified: Thu, 23 Jan 2020 17:27:35 GMT  
		Size: 14.7 MB (14677552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ee18ebf1c4e1ec04ee4d405e4bb74eda52a1c7b53bd50bd1285fce31ecb7f0`  
		Last Modified: Thu, 23 Jan 2020 17:27:29 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b0fd5160a24d544362517f237ec81e53f1fe7f662b783da54679338246a5c9`  
		Last Modified: Thu, 23 Jan 2020 17:27:30 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59490a75b95de035d3d2c2d69fe7d92a3165c0552dcabeaa8e9c765b9385201f`  
		Last Modified: Thu, 23 Jan 2020 17:27:30 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.1.1` - linux; 386

```console
$ docker pull consul@sha256:e1a43e2d64d69c8d3653ee646430183e08556e6feac71e79beb0015c7eafd8e4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17960253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7b4ecea4861c81a2ed5fd1ec5222d0802c39a3c66efc6e147dcd6b056cd931`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:18 GMT
ADD file:68d5786259963a2b97cf808d79de83cbd0281dfea284e1a401bc851a3585e1bd in / 
# Thu, 23 Apr 2020 21:16:19 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 04:30:33 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Fri, 24 Apr 2020 04:31:53 GMT
ENV CONSUL_VERSION=1.1.1
# Fri, 24 Apr 2020 04:31:53 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 24 Apr 2020 04:31:54 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 24 Apr 2020 04:31:57 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 24 Apr 2020 04:31:58 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 24 Apr 2020 04:31:59 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 04:31:59 GMT
VOLUME [/consul/data]
# Fri, 24 Apr 2020 04:31:59 GMT
EXPOSE 8300
# Fri, 24 Apr 2020 04:31:59 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 24 Apr 2020 04:31:59 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 24 Apr 2020 04:32:00 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Apr 2020 04:32:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 04:32:00 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2f4fdbe0599cb5bbd0664b1cdad4997f428ce2495ae3eabf942129dc197d991c`  
		Last Modified: Thu, 23 Apr 2020 21:16:41 GMT  
		Size: 2.8 MB (2769736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d29818b9044046d6411c4fc801bc923c8c1b927e298e7ab2dc918a838551d939`  
		Last Modified: Fri, 24 Apr 2020 04:33:41 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82024872e9d3c48b8ecf7cee0fa0cb357e20c4a5d47aae161597e702689529f1`  
		Last Modified: Fri, 24 Apr 2020 04:33:44 GMT  
		Size: 15.2 MB (15187288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9848c4a2e774d7260fd7abd8bf55c21b93d4739a5d97d669f3a4415854e1f65a`  
		Last Modified: Fri, 24 Apr 2020 04:33:40 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fccc47ff63aef6639dcec62889f890b94c256ee6ced64bd35573e0081810c0e6`  
		Last Modified: Fri, 24 Apr 2020 04:33:41 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce866c09d565e3efb843bc7c65209d46b5acc12a8a922c95b12f72a13ac1de67`  
		Last Modified: Fri, 24 Apr 2020 04:33:40 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.2`

```console
$ docker pull consul@sha256:b330491bf5f04e5287e128cc6d1476215a0a0027450a33ed9aa02ad862b8d2e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.2` - linux; amd64

```console
$ docker pull consul@sha256:c72e7c8e3423ebbe3313ef8903fd00c3f1f3b6f41ed5578698ad64a1299fea50
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28360024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67f00a3cbd8ae9cb81252ee2890ab2a8779ee614a4d9820e8fb0332b1cd72b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:15:11 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Jan 2020 17:16:41 GMT
ENV CONSUL_VERSION=1.2.4
# Thu, 23 Jan 2020 17:16:41 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Jan 2020 17:16:42 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Jan 2020 17:16:49 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Jan 2020 17:16:50 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Jan 2020 17:16:51 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Jan 2020 17:16:51 GMT
VOLUME [/consul/data]
# Thu, 23 Jan 2020 17:16:51 GMT
EXPOSE 8300
# Thu, 23 Jan 2020 17:16:52 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Jan 2020 17:16:52 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Jan 2020 17:16:52 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 17:16:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 17:16:53 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05236fbe333350c71e205c5a48e5c1498c79fcc4370068a86859fdb4dcc8ba6`  
		Last Modified: Thu, 23 Jan 2020 17:19:50 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25b9e9afae6f3f1764ac7c3dcc7c599ee824ebf4c24ad86fb8b6f926a5d2c36`  
		Last Modified: Thu, 23 Jan 2020 17:19:58 GMT  
		Size: 25.6 MB (25592623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6805bf2501087e0ba3f659513f496a23990d725531ab0be38fae74a3c831fa9`  
		Last Modified: Thu, 23 Jan 2020 17:19:50 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f551ea7fa1939e487e14e28cf0e6ccfa55439ef8c7a52e644e88924f0fcf71`  
		Last Modified: Thu, 23 Jan 2020 17:19:50 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cecee1f7625c248fca92b3d57e5f1f2a39180057b479eb182d0329f7cdc371a`  
		Last Modified: Thu, 23 Jan 2020 17:19:50 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.2` - linux; arm variant v6

```console
$ docker pull consul@sha256:0d6f34d42d8c26690901030ac0382f77be4afaa8ad4706286860e8944088f9fe
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27345781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad66141a43a06cc1daa7be94e6c1610972ea616993dc0ef2e59cdeb0fdc4b9c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:44 GMT
ADD file:7dd2657543fac7f63a125194d27bd38a8e472a3076831a2331c43a471794c210 in / 
# Thu, 23 Apr 2020 15:51:45 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 16:53:13 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Apr 2020 16:56:21 GMT
ENV CONSUL_VERSION=1.2.4
# Thu, 23 Apr 2020 16:56:23 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Apr 2020 16:56:28 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Apr 2020 16:56:38 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Apr 2020 16:56:41 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Apr 2020 16:56:43 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 16:56:44 GMT
VOLUME [/consul/data]
# Thu, 23 Apr 2020 16:56:45 GMT
EXPOSE 8300
# Thu, 23 Apr 2020 16:56:46 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Apr 2020 16:56:47 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Apr 2020 16:56:48 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Apr 2020 16:56:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 16:56:51 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:27da80392aebe463671b839837d59af1261218364b4261ceb2eca0f814075270`  
		Last Modified: Thu, 23 Apr 2020 15:52:21 GMT  
		Size: 2.5 MB (2548725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f3902c6755e51bc4deae181fb9e3f445726058a580540b34180b1d901bc6ad`  
		Last Modified: Thu, 23 Apr 2020 17:00:31 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d2907d69059834ae38df9cb5ce5abea2286c44944108ddc8df3b64d2072e3c`  
		Last Modified: Thu, 23 Apr 2020 17:00:42 GMT  
		Size: 24.8 MB (24793766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5639b6974ec6a0586ead06dbf648a68278de4759d13602db9a1829dc2cb25d75`  
		Last Modified: Thu, 23 Apr 2020 17:00:30 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39db0dc08d2fae5a5b6e0fb7f21074ba1438c9b266a6d744c8b6f8822e742bca`  
		Last Modified: Thu, 23 Apr 2020 17:00:30 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ebcc61ca2620bd4f870fb0a74fdb77fcb9537c8db1fd17e40ab67a24ebc32e5`  
		Last Modified: Thu, 23 Apr 2020 17:00:30 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.2` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:001ecb2e473fecff4a92b05a066f68a15daf84b3c3c1d0c0d07ab6de3b9720c5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27144711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81dbc650e06f84574778ad7203e4618603b88765f3b1c016f0981bc283d3ac77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:54:58 GMT
ADD file:92767b5525acd9dbf8657931d32bdcc7cc504cdc33c95e84a75e478b00569bab in / 
# Thu, 23 Jan 2020 16:54:59 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:19:49 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Jan 2020 17:22:35 GMT
ENV CONSUL_VERSION=1.2.4
# Thu, 23 Jan 2020 17:22:36 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Jan 2020 17:22:38 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Jan 2020 17:22:46 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Jan 2020 17:22:48 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Jan 2020 17:22:51 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Jan 2020 17:22:53 GMT
VOLUME [/consul/data]
# Thu, 23 Jan 2020 17:22:55 GMT
EXPOSE 8300
# Thu, 23 Jan 2020 17:22:56 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Jan 2020 17:22:56 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Jan 2020 17:22:57 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 17:22:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 17:22:58 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:eb93038481ddcf86a625b70f7551cdc583e38886f206fe7e40ad644008efa815`  
		Last Modified: Thu, 23 Jan 2020 16:55:31 GMT  
		Size: 2.7 MB (2693238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598f5b3b590a3b748748a66708d7f62a3b4fad4f172cbbfd22d6d9283cc7abf8`  
		Last Modified: Thu, 23 Jan 2020 17:27:14 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4691413d5a5f19170da5084a3cb6131835489f7868f17153fd895f9f27acc43a`  
		Last Modified: Thu, 23 Jan 2020 17:27:22 GMT  
		Size: 24.4 MB (24448187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:644a1a197a254512b001fe802115f9b0b9e87a389e7205e3ec998dfca101653b`  
		Last Modified: Thu, 23 Jan 2020 17:27:14 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05aa6ffb25367f0b6e471b03152190e5b08c2c92c5ba63c4463b9f456840939`  
		Last Modified: Thu, 23 Jan 2020 17:27:14 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b8fc21306eef0dc0bc89ab67ad9de13287b2bc4d3418e563ed13d2ad2edd57`  
		Last Modified: Thu, 23 Jan 2020 17:27:14 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.2` - linux; 386

```console
$ docker pull consul@sha256:b9a93a22356863237ed47a3692f6e2fc40a5b0fa5e3d8b8c95f76ba507cdc9db
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28101751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3e502fdb651377d03b343346bda8d434d8718463104359331977ee30ed7bbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:18 GMT
ADD file:68d5786259963a2b97cf808d79de83cbd0281dfea284e1a401bc851a3585e1bd in / 
# Thu, 23 Apr 2020 21:16:19 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 04:30:33 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Fri, 24 Apr 2020 04:31:40 GMT
ENV CONSUL_VERSION=1.2.4
# Fri, 24 Apr 2020 04:31:41 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 24 Apr 2020 04:31:41 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 24 Apr 2020 04:31:46 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 24 Apr 2020 04:31:47 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 24 Apr 2020 04:31:48 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 04:31:48 GMT
VOLUME [/consul/data]
# Fri, 24 Apr 2020 04:31:48 GMT
EXPOSE 8300
# Fri, 24 Apr 2020 04:31:48 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 24 Apr 2020 04:31:48 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 24 Apr 2020 04:31:49 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Apr 2020 04:31:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 04:31:49 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2f4fdbe0599cb5bbd0664b1cdad4997f428ce2495ae3eabf942129dc197d991c`  
		Last Modified: Thu, 23 Apr 2020 21:16:41 GMT  
		Size: 2.8 MB (2769736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cdc7080aa5cc8080f04d30e5771a15fbf5d8d6dd249e30fb0039e632a12c856`  
		Last Modified: Fri, 24 Apr 2020 04:33:30 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee895264375d68e371e42de8cdb7676ede8f2201c9d50f0a794d8cc7065eb56`  
		Last Modified: Fri, 24 Apr 2020 04:33:36 GMT  
		Size: 25.3 MB (25328787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b88d9a79f4beb250b040b661aa73be2a783b1b2c85e25577546c1187245ac3`  
		Last Modified: Fri, 24 Apr 2020 04:33:30 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e95e69b1d54b002d348a2c673da9bcc4688a23a90f0d8d91d8a584cd72bec7`  
		Last Modified: Fri, 24 Apr 2020 04:33:30 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fddd71981e8a6865516e8d14d62639591c70baaee9bb2e595a73b30fca471616`  
		Last Modified: Fri, 24 Apr 2020 04:33:30 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.2.4`

```console
$ docker pull consul@sha256:b330491bf5f04e5287e128cc6d1476215a0a0027450a33ed9aa02ad862b8d2e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.2.4` - linux; amd64

```console
$ docker pull consul@sha256:c72e7c8e3423ebbe3313ef8903fd00c3f1f3b6f41ed5578698ad64a1299fea50
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28360024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67f00a3cbd8ae9cb81252ee2890ab2a8779ee614a4d9820e8fb0332b1cd72b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:15:11 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Jan 2020 17:16:41 GMT
ENV CONSUL_VERSION=1.2.4
# Thu, 23 Jan 2020 17:16:41 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Jan 2020 17:16:42 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Jan 2020 17:16:49 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Jan 2020 17:16:50 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Jan 2020 17:16:51 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Jan 2020 17:16:51 GMT
VOLUME [/consul/data]
# Thu, 23 Jan 2020 17:16:51 GMT
EXPOSE 8300
# Thu, 23 Jan 2020 17:16:52 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Jan 2020 17:16:52 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Jan 2020 17:16:52 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 17:16:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 17:16:53 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05236fbe333350c71e205c5a48e5c1498c79fcc4370068a86859fdb4dcc8ba6`  
		Last Modified: Thu, 23 Jan 2020 17:19:50 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25b9e9afae6f3f1764ac7c3dcc7c599ee824ebf4c24ad86fb8b6f926a5d2c36`  
		Last Modified: Thu, 23 Jan 2020 17:19:58 GMT  
		Size: 25.6 MB (25592623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6805bf2501087e0ba3f659513f496a23990d725531ab0be38fae74a3c831fa9`  
		Last Modified: Thu, 23 Jan 2020 17:19:50 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f551ea7fa1939e487e14e28cf0e6ccfa55439ef8c7a52e644e88924f0fcf71`  
		Last Modified: Thu, 23 Jan 2020 17:19:50 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cecee1f7625c248fca92b3d57e5f1f2a39180057b479eb182d0329f7cdc371a`  
		Last Modified: Thu, 23 Jan 2020 17:19:50 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.2.4` - linux; arm variant v6

```console
$ docker pull consul@sha256:0d6f34d42d8c26690901030ac0382f77be4afaa8ad4706286860e8944088f9fe
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27345781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad66141a43a06cc1daa7be94e6c1610972ea616993dc0ef2e59cdeb0fdc4b9c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:44 GMT
ADD file:7dd2657543fac7f63a125194d27bd38a8e472a3076831a2331c43a471794c210 in / 
# Thu, 23 Apr 2020 15:51:45 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 16:53:13 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Apr 2020 16:56:21 GMT
ENV CONSUL_VERSION=1.2.4
# Thu, 23 Apr 2020 16:56:23 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Apr 2020 16:56:28 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Apr 2020 16:56:38 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Apr 2020 16:56:41 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Apr 2020 16:56:43 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 16:56:44 GMT
VOLUME [/consul/data]
# Thu, 23 Apr 2020 16:56:45 GMT
EXPOSE 8300
# Thu, 23 Apr 2020 16:56:46 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Apr 2020 16:56:47 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Apr 2020 16:56:48 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Apr 2020 16:56:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 16:56:51 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:27da80392aebe463671b839837d59af1261218364b4261ceb2eca0f814075270`  
		Last Modified: Thu, 23 Apr 2020 15:52:21 GMT  
		Size: 2.5 MB (2548725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f3902c6755e51bc4deae181fb9e3f445726058a580540b34180b1d901bc6ad`  
		Last Modified: Thu, 23 Apr 2020 17:00:31 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d2907d69059834ae38df9cb5ce5abea2286c44944108ddc8df3b64d2072e3c`  
		Last Modified: Thu, 23 Apr 2020 17:00:42 GMT  
		Size: 24.8 MB (24793766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5639b6974ec6a0586ead06dbf648a68278de4759d13602db9a1829dc2cb25d75`  
		Last Modified: Thu, 23 Apr 2020 17:00:30 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39db0dc08d2fae5a5b6e0fb7f21074ba1438c9b266a6d744c8b6f8822e742bca`  
		Last Modified: Thu, 23 Apr 2020 17:00:30 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ebcc61ca2620bd4f870fb0a74fdb77fcb9537c8db1fd17e40ab67a24ebc32e5`  
		Last Modified: Thu, 23 Apr 2020 17:00:30 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.2.4` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:001ecb2e473fecff4a92b05a066f68a15daf84b3c3c1d0c0d07ab6de3b9720c5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27144711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81dbc650e06f84574778ad7203e4618603b88765f3b1c016f0981bc283d3ac77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:54:58 GMT
ADD file:92767b5525acd9dbf8657931d32bdcc7cc504cdc33c95e84a75e478b00569bab in / 
# Thu, 23 Jan 2020 16:54:59 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:19:49 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Jan 2020 17:22:35 GMT
ENV CONSUL_VERSION=1.2.4
# Thu, 23 Jan 2020 17:22:36 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Jan 2020 17:22:38 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Jan 2020 17:22:46 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Jan 2020 17:22:48 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Jan 2020 17:22:51 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Jan 2020 17:22:53 GMT
VOLUME [/consul/data]
# Thu, 23 Jan 2020 17:22:55 GMT
EXPOSE 8300
# Thu, 23 Jan 2020 17:22:56 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Jan 2020 17:22:56 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Jan 2020 17:22:57 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 17:22:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 17:22:58 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:eb93038481ddcf86a625b70f7551cdc583e38886f206fe7e40ad644008efa815`  
		Last Modified: Thu, 23 Jan 2020 16:55:31 GMT  
		Size: 2.7 MB (2693238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598f5b3b590a3b748748a66708d7f62a3b4fad4f172cbbfd22d6d9283cc7abf8`  
		Last Modified: Thu, 23 Jan 2020 17:27:14 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4691413d5a5f19170da5084a3cb6131835489f7868f17153fd895f9f27acc43a`  
		Last Modified: Thu, 23 Jan 2020 17:27:22 GMT  
		Size: 24.4 MB (24448187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:644a1a197a254512b001fe802115f9b0b9e87a389e7205e3ec998dfca101653b`  
		Last Modified: Thu, 23 Jan 2020 17:27:14 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05aa6ffb25367f0b6e471b03152190e5b08c2c92c5ba63c4463b9f456840939`  
		Last Modified: Thu, 23 Jan 2020 17:27:14 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b8fc21306eef0dc0bc89ab67ad9de13287b2bc4d3418e563ed13d2ad2edd57`  
		Last Modified: Thu, 23 Jan 2020 17:27:14 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.2.4` - linux; 386

```console
$ docker pull consul@sha256:b9a93a22356863237ed47a3692f6e2fc40a5b0fa5e3d8b8c95f76ba507cdc9db
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28101751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3e502fdb651377d03b343346bda8d434d8718463104359331977ee30ed7bbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:18 GMT
ADD file:68d5786259963a2b97cf808d79de83cbd0281dfea284e1a401bc851a3585e1bd in / 
# Thu, 23 Apr 2020 21:16:19 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 04:30:33 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Fri, 24 Apr 2020 04:31:40 GMT
ENV CONSUL_VERSION=1.2.4
# Fri, 24 Apr 2020 04:31:41 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 24 Apr 2020 04:31:41 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 24 Apr 2020 04:31:46 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 24 Apr 2020 04:31:47 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 24 Apr 2020 04:31:48 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 04:31:48 GMT
VOLUME [/consul/data]
# Fri, 24 Apr 2020 04:31:48 GMT
EXPOSE 8300
# Fri, 24 Apr 2020 04:31:48 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 24 Apr 2020 04:31:48 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 24 Apr 2020 04:31:49 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Apr 2020 04:31:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 04:31:49 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2f4fdbe0599cb5bbd0664b1cdad4997f428ce2495ae3eabf942129dc197d991c`  
		Last Modified: Thu, 23 Apr 2020 21:16:41 GMT  
		Size: 2.8 MB (2769736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cdc7080aa5cc8080f04d30e5771a15fbf5d8d6dd249e30fb0039e632a12c856`  
		Last Modified: Fri, 24 Apr 2020 04:33:30 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee895264375d68e371e42de8cdb7676ede8f2201c9d50f0a794d8cc7065eb56`  
		Last Modified: Fri, 24 Apr 2020 04:33:36 GMT  
		Size: 25.3 MB (25328787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b88d9a79f4beb250b040b661aa73be2a783b1b2c85e25577546c1187245ac3`  
		Last Modified: Fri, 24 Apr 2020 04:33:30 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e95e69b1d54b002d348a2c673da9bcc4688a23a90f0d8d91d8a584cd72bec7`  
		Last Modified: Fri, 24 Apr 2020 04:33:30 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fddd71981e8a6865516e8d14d62639591c70baaee9bb2e595a73b30fca471616`  
		Last Modified: Fri, 24 Apr 2020 04:33:30 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.3`

```console
$ docker pull consul@sha256:693cb30874b1f98858bb3c88e2b2767332bce9f9e7576c5a90ca60deabdf4ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.3` - linux; amd64

```console
$ docker pull consul@sha256:1bedb45a13dccadfe00d032b7432f5069e76fd6726e94946879f9531c5f5b1c8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38563269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a1b14382a5b435edfcb5a194a60406bd861fabb75effcfe278f0f7ccd58965`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:15:11 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Jan 2020 17:16:23 GMT
ENV CONSUL_VERSION=1.3.1
# Thu, 23 Jan 2020 17:16:23 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Jan 2020 17:16:25 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Jan 2020 17:16:31 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Jan 2020 17:16:32 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Jan 2020 17:16:33 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Jan 2020 17:16:34 GMT
VOLUME [/consul/data]
# Thu, 23 Jan 2020 17:16:34 GMT
EXPOSE 8300
# Thu, 23 Jan 2020 17:16:34 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Jan 2020 17:16:34 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Jan 2020 17:16:35 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 17:16:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 17:16:35 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f35c11f4344ff830f784baa710a9b2c18b608b3e72ef47fba038762e7307b9`  
		Last Modified: Thu, 23 Jan 2020 17:19:37 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a8452a9f508b85fc7f8488e1bd2a5f1532616c4cfbe2e0144698bd6b50ea4a`  
		Last Modified: Thu, 23 Jan 2020 17:19:46 GMT  
		Size: 35.8 MB (35795870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a940220db4bbb696ce4e3c8c9c0aaa2d8a3143974fc01516b8fc0c739f85b5e`  
		Last Modified: Thu, 23 Jan 2020 17:19:37 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cadae00f277c0b29d5edbc5976825a70e9597afe0b6711ec2af29a7ff13dcf88`  
		Last Modified: Thu, 23 Jan 2020 17:19:38 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b5793fa9cc319a37def4538c53d0961fb328e2272d8176a9f5afe8c94672ed`  
		Last Modified: Thu, 23 Jan 2020 17:19:37 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.3` - linux; arm variant v6

```console
$ docker pull consul@sha256:4bc706953ad42c620d87e67bcc6816fa3d3a6e22f39056333816bec9aa7776c7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36396594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c24e4e72fa9e4b19c5fb8f63caf838628e8b9db75f2911aaf021bee6132872de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:44 GMT
ADD file:7dd2657543fac7f63a125194d27bd38a8e472a3076831a2331c43a471794c210 in / 
# Thu, 23 Apr 2020 15:51:45 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 16:53:13 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Apr 2020 16:55:28 GMT
ENV CONSUL_VERSION=1.3.1
# Thu, 23 Apr 2020 16:55:29 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Apr 2020 16:55:31 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Apr 2020 16:55:46 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Apr 2020 16:55:52 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Apr 2020 16:55:58 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 16:55:59 GMT
VOLUME [/consul/data]
# Thu, 23 Apr 2020 16:56:00 GMT
EXPOSE 8300
# Thu, 23 Apr 2020 16:56:02 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Apr 2020 16:56:03 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Apr 2020 16:56:04 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Apr 2020 16:56:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 16:56:07 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:27da80392aebe463671b839837d59af1261218364b4261ceb2eca0f814075270`  
		Last Modified: Thu, 23 Apr 2020 15:52:21 GMT  
		Size: 2.5 MB (2548725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eb0dfd7e7346167838c1a76eec79673081440d7b0f96016cdd1b80419120ce`  
		Last Modified: Thu, 23 Apr 2020 17:00:06 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989235e8aafc3d56452784c31382fba7d60f9b1e4229e2943397a348cbb91e51`  
		Last Modified: Thu, 23 Apr 2020 17:00:19 GMT  
		Size: 33.8 MB (33844579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec087e98bcb596767137ea813be12c851540803b8c3e42d61cbb046fc7830fa`  
		Last Modified: Thu, 23 Apr 2020 17:00:06 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a9b94ae73012b59492f3fa8e1d7806fd04f7691e6a0064bf8dbd8edac7b6fc`  
		Last Modified: Thu, 23 Apr 2020 17:00:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb0c0e3165cdf269e929600f84320db083f7c296dcddbd701ce61cb9e980ee9`  
		Last Modified: Thu, 23 Apr 2020 17:00:06 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.3` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:2418b650cb5ea9bc4af38e5e0b249567bcee490ff3b46312100e3b51be757be3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36217075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb81762c89f3e79d1b604d9b61afed84e8b1ff1f6e81ee99adc217167dd0635`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:54:58 GMT
ADD file:92767b5525acd9dbf8657931d32bdcc7cc504cdc33c95e84a75e478b00569bab in / 
# Thu, 23 Jan 2020 16:54:59 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:19:49 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Jan 2020 17:22:01 GMT
ENV CONSUL_VERSION=1.3.1
# Thu, 23 Jan 2020 17:22:02 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Jan 2020 17:22:05 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Jan 2020 17:22:13 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Jan 2020 17:22:17 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Jan 2020 17:22:19 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Jan 2020 17:22:20 GMT
VOLUME [/consul/data]
# Thu, 23 Jan 2020 17:22:21 GMT
EXPOSE 8300
# Thu, 23 Jan 2020 17:22:22 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Jan 2020 17:22:22 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Jan 2020 17:22:23 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 17:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 17:22:25 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:eb93038481ddcf86a625b70f7551cdc583e38886f206fe7e40ad644008efa815`  
		Last Modified: Thu, 23 Jan 2020 16:55:31 GMT  
		Size: 2.7 MB (2693238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98012cd647e1d27e020c00fae0d589a965b7ecc830bda18c66aceb6ac72fae7`  
		Last Modified: Thu, 23 Jan 2020 17:27:01 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023f9aef35688822464cb5df3ee78a055a71ef63161969bd0f04bd25abdd79bc`  
		Last Modified: Thu, 23 Jan 2020 17:27:06 GMT  
		Size: 33.5 MB (33520552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599be1f23dcb5d8099d3eb5e0e46e58bbaa2c66143a7c9c76c7be5d5c05fc344`  
		Last Modified: Thu, 23 Jan 2020 17:27:01 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2c8ee332607e9b33817745e2162932c2b13cf5ccdb02cc8aa6ab1c14ef4f40`  
		Last Modified: Thu, 23 Jan 2020 17:27:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4b8b1de504b0c2fa582f0ad0f528fbfe2695451a47c5ca49febfd321c31d9f`  
		Last Modified: Thu, 23 Jan 2020 17:27:00 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.3` - linux; 386

```console
$ docker pull consul@sha256:3f2640bd30e022b61ce7a9cf1660fc998fc5185355d23c44c73be440906bac16
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 MB (37754435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a1f2d3dd5e0ca24dd18892ec8283293dc45db41fb32a073d4ac64a2430f710`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:18 GMT
ADD file:68d5786259963a2b97cf808d79de83cbd0281dfea284e1a401bc851a3585e1bd in / 
# Thu, 23 Apr 2020 21:16:19 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 04:30:33 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Fri, 24 Apr 2020 04:31:28 GMT
ENV CONSUL_VERSION=1.3.1
# Fri, 24 Apr 2020 04:31:28 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 24 Apr 2020 04:31:29 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 24 Apr 2020 04:31:34 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 24 Apr 2020 04:31:34 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 24 Apr 2020 04:31:35 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 04:31:35 GMT
VOLUME [/consul/data]
# Fri, 24 Apr 2020 04:31:36 GMT
EXPOSE 8300
# Fri, 24 Apr 2020 04:31:36 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 24 Apr 2020 04:31:36 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 24 Apr 2020 04:31:36 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Apr 2020 04:31:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 04:31:37 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2f4fdbe0599cb5bbd0664b1cdad4997f428ce2495ae3eabf942129dc197d991c`  
		Last Modified: Thu, 23 Apr 2020 21:16:41 GMT  
		Size: 2.8 MB (2769736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1e9a4531a2d9978c118f72f554e90497f39bf1e9c4a3a96ded33d874076c61`  
		Last Modified: Fri, 24 Apr 2020 04:33:19 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4554f2aa7ab01b93d8c18cbdfee24588b194d763f19972138273ea2fd052d480`  
		Last Modified: Fri, 24 Apr 2020 04:33:25 GMT  
		Size: 35.0 MB (34981467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f81c8f14470667483b45dcedc54df4e89fd8d1a192d77ab918c34523a5d2f2f`  
		Last Modified: Fri, 24 Apr 2020 04:33:20 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51f091770b7dc5333f1f62ec308f1ccd4a895272fd521ffc3a78c712b578f25`  
		Last Modified: Fri, 24 Apr 2020 04:33:19 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7fdaec4321a4851d744f73e3241aabdf9292e9942fbf7f7bd457faac310c06`  
		Last Modified: Fri, 24 Apr 2020 04:33:19 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.3.1`

```console
$ docker pull consul@sha256:693cb30874b1f98858bb3c88e2b2767332bce9f9e7576c5a90ca60deabdf4ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.3.1` - linux; amd64

```console
$ docker pull consul@sha256:1bedb45a13dccadfe00d032b7432f5069e76fd6726e94946879f9531c5f5b1c8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38563269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a1b14382a5b435edfcb5a194a60406bd861fabb75effcfe278f0f7ccd58965`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:15:11 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Jan 2020 17:16:23 GMT
ENV CONSUL_VERSION=1.3.1
# Thu, 23 Jan 2020 17:16:23 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Jan 2020 17:16:25 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Jan 2020 17:16:31 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Jan 2020 17:16:32 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Jan 2020 17:16:33 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Jan 2020 17:16:34 GMT
VOLUME [/consul/data]
# Thu, 23 Jan 2020 17:16:34 GMT
EXPOSE 8300
# Thu, 23 Jan 2020 17:16:34 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Jan 2020 17:16:34 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Jan 2020 17:16:35 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 17:16:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 17:16:35 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f35c11f4344ff830f784baa710a9b2c18b608b3e72ef47fba038762e7307b9`  
		Last Modified: Thu, 23 Jan 2020 17:19:37 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a8452a9f508b85fc7f8488e1bd2a5f1532616c4cfbe2e0144698bd6b50ea4a`  
		Last Modified: Thu, 23 Jan 2020 17:19:46 GMT  
		Size: 35.8 MB (35795870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a940220db4bbb696ce4e3c8c9c0aaa2d8a3143974fc01516b8fc0c739f85b5e`  
		Last Modified: Thu, 23 Jan 2020 17:19:37 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cadae00f277c0b29d5edbc5976825a70e9597afe0b6711ec2af29a7ff13dcf88`  
		Last Modified: Thu, 23 Jan 2020 17:19:38 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b5793fa9cc319a37def4538c53d0961fb328e2272d8176a9f5afe8c94672ed`  
		Last Modified: Thu, 23 Jan 2020 17:19:37 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.3.1` - linux; arm variant v6

```console
$ docker pull consul@sha256:4bc706953ad42c620d87e67bcc6816fa3d3a6e22f39056333816bec9aa7776c7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36396594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c24e4e72fa9e4b19c5fb8f63caf838628e8b9db75f2911aaf021bee6132872de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:44 GMT
ADD file:7dd2657543fac7f63a125194d27bd38a8e472a3076831a2331c43a471794c210 in / 
# Thu, 23 Apr 2020 15:51:45 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 16:53:13 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Apr 2020 16:55:28 GMT
ENV CONSUL_VERSION=1.3.1
# Thu, 23 Apr 2020 16:55:29 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Apr 2020 16:55:31 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Apr 2020 16:55:46 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Apr 2020 16:55:52 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Apr 2020 16:55:58 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 16:55:59 GMT
VOLUME [/consul/data]
# Thu, 23 Apr 2020 16:56:00 GMT
EXPOSE 8300
# Thu, 23 Apr 2020 16:56:02 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Apr 2020 16:56:03 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Apr 2020 16:56:04 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Apr 2020 16:56:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 16:56:07 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:27da80392aebe463671b839837d59af1261218364b4261ceb2eca0f814075270`  
		Last Modified: Thu, 23 Apr 2020 15:52:21 GMT  
		Size: 2.5 MB (2548725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eb0dfd7e7346167838c1a76eec79673081440d7b0f96016cdd1b80419120ce`  
		Last Modified: Thu, 23 Apr 2020 17:00:06 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989235e8aafc3d56452784c31382fba7d60f9b1e4229e2943397a348cbb91e51`  
		Last Modified: Thu, 23 Apr 2020 17:00:19 GMT  
		Size: 33.8 MB (33844579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec087e98bcb596767137ea813be12c851540803b8c3e42d61cbb046fc7830fa`  
		Last Modified: Thu, 23 Apr 2020 17:00:06 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a9b94ae73012b59492f3fa8e1d7806fd04f7691e6a0064bf8dbd8edac7b6fc`  
		Last Modified: Thu, 23 Apr 2020 17:00:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb0c0e3165cdf269e929600f84320db083f7c296dcddbd701ce61cb9e980ee9`  
		Last Modified: Thu, 23 Apr 2020 17:00:06 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.3.1` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:2418b650cb5ea9bc4af38e5e0b249567bcee490ff3b46312100e3b51be757be3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36217075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb81762c89f3e79d1b604d9b61afed84e8b1ff1f6e81ee99adc217167dd0635`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:54:58 GMT
ADD file:92767b5525acd9dbf8657931d32bdcc7cc504cdc33c95e84a75e478b00569bab in / 
# Thu, 23 Jan 2020 16:54:59 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:19:49 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Jan 2020 17:22:01 GMT
ENV CONSUL_VERSION=1.3.1
# Thu, 23 Jan 2020 17:22:02 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Jan 2020 17:22:05 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Jan 2020 17:22:13 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Jan 2020 17:22:17 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Jan 2020 17:22:19 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Jan 2020 17:22:20 GMT
VOLUME [/consul/data]
# Thu, 23 Jan 2020 17:22:21 GMT
EXPOSE 8300
# Thu, 23 Jan 2020 17:22:22 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Jan 2020 17:22:22 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Jan 2020 17:22:23 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 17:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 17:22:25 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:eb93038481ddcf86a625b70f7551cdc583e38886f206fe7e40ad644008efa815`  
		Last Modified: Thu, 23 Jan 2020 16:55:31 GMT  
		Size: 2.7 MB (2693238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98012cd647e1d27e020c00fae0d589a965b7ecc830bda18c66aceb6ac72fae7`  
		Last Modified: Thu, 23 Jan 2020 17:27:01 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023f9aef35688822464cb5df3ee78a055a71ef63161969bd0f04bd25abdd79bc`  
		Last Modified: Thu, 23 Jan 2020 17:27:06 GMT  
		Size: 33.5 MB (33520552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599be1f23dcb5d8099d3eb5e0e46e58bbaa2c66143a7c9c76c7be5d5c05fc344`  
		Last Modified: Thu, 23 Jan 2020 17:27:01 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2c8ee332607e9b33817745e2162932c2b13cf5ccdb02cc8aa6ab1c14ef4f40`  
		Last Modified: Thu, 23 Jan 2020 17:27:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4b8b1de504b0c2fa582f0ad0f528fbfe2695451a47c5ca49febfd321c31d9f`  
		Last Modified: Thu, 23 Jan 2020 17:27:00 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.3.1` - linux; 386

```console
$ docker pull consul@sha256:3f2640bd30e022b61ce7a9cf1660fc998fc5185355d23c44c73be440906bac16
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 MB (37754435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a1f2d3dd5e0ca24dd18892ec8283293dc45db41fb32a073d4ac64a2430f710`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:18 GMT
ADD file:68d5786259963a2b97cf808d79de83cbd0281dfea284e1a401bc851a3585e1bd in / 
# Thu, 23 Apr 2020 21:16:19 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 04:30:33 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Fri, 24 Apr 2020 04:31:28 GMT
ENV CONSUL_VERSION=1.3.1
# Fri, 24 Apr 2020 04:31:28 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 24 Apr 2020 04:31:29 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 24 Apr 2020 04:31:34 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 24 Apr 2020 04:31:34 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 24 Apr 2020 04:31:35 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 04:31:35 GMT
VOLUME [/consul/data]
# Fri, 24 Apr 2020 04:31:36 GMT
EXPOSE 8300
# Fri, 24 Apr 2020 04:31:36 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 24 Apr 2020 04:31:36 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 24 Apr 2020 04:31:36 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Apr 2020 04:31:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 04:31:37 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2f4fdbe0599cb5bbd0664b1cdad4997f428ce2495ae3eabf942129dc197d991c`  
		Last Modified: Thu, 23 Apr 2020 21:16:41 GMT  
		Size: 2.8 MB (2769736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1e9a4531a2d9978c118f72f554e90497f39bf1e9c4a3a96ded33d874076c61`  
		Last Modified: Fri, 24 Apr 2020 04:33:19 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4554f2aa7ab01b93d8c18cbdfee24588b194d763f19972138273ea2fd052d480`  
		Last Modified: Fri, 24 Apr 2020 04:33:25 GMT  
		Size: 35.0 MB (34981467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f81c8f14470667483b45dcedc54df4e89fd8d1a192d77ab918c34523a5d2f2f`  
		Last Modified: Fri, 24 Apr 2020 04:33:20 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51f091770b7dc5333f1f62ec308f1ccd4a895272fd521ffc3a78c712b578f25`  
		Last Modified: Fri, 24 Apr 2020 04:33:19 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7fdaec4321a4851d744f73e3241aabdf9292e9942fbf7f7bd457faac310c06`  
		Last Modified: Fri, 24 Apr 2020 04:33:19 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.4`

```console
$ docker pull consul@sha256:ca338881abc9f24b8f29874f74c757c12ced9b53eb7a53fce2072f19eea5dac2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.4` - linux; amd64

```console
$ docker pull consul@sha256:068a9a19ecd914c3364c5633917b72a898b461923ff56dd7500aa926f421c4b8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39199490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad32393b859a2a3bdd3411af9926171c1f5c96558f796a03dce84b164c314613`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:15:11 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Jan 2020 17:16:05 GMT
ENV CONSUL_VERSION=1.4.5
# Thu, 23 Jan 2020 17:16:05 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Jan 2020 17:16:07 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Jan 2020 17:16:13 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Jan 2020 17:16:14 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Jan 2020 17:16:15 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Jan 2020 17:16:16 GMT
VOLUME [/consul/data]
# Thu, 23 Jan 2020 17:16:16 GMT
EXPOSE 8300
# Thu, 23 Jan 2020 17:16:16 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Jan 2020 17:16:16 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Jan 2020 17:16:17 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 17:16:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 17:16:17 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7651bd62600c8b706e5120d2fe48d72e94904be0cc8d1a82d4d3f5de592b37`  
		Last Modified: Thu, 23 Jan 2020 17:19:00 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae6d22bb36b77217cd3fb3e007589cbfaf4076d1a1ad009150594dd270334d9`  
		Last Modified: Thu, 23 Jan 2020 17:19:32 GMT  
		Size: 36.4 MB (36432087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9697a7a1e3d9f33fe5891a4a3afab1ca81826b415f1575967c96fb7426b8d45e`  
		Last Modified: Thu, 23 Jan 2020 17:19:00 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5d89b529d3cc118de1dbf8c3b2554bc84510eb7afa942267aa3ffc94f94923`  
		Last Modified: Thu, 23 Jan 2020 17:19:00 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71722bc46238839f701198cdccdf1bd8330aa287d814044f6721c15038d9baeb`  
		Last Modified: Thu, 23 Jan 2020 17:19:00 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.4` - linux; arm variant v6

```console
$ docker pull consul@sha256:b46336852e3dbfc6455cdbc9f93ec6f106bd4ddaa683ea345f17afa10c39dc27
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36975963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b23daecfc8abc2af29f8313f7ecde84a78c6ab55449160103c2e9a5b0290957`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:44 GMT
ADD file:7dd2657543fac7f63a125194d27bd38a8e472a3076831a2331c43a471794c210 in / 
# Thu, 23 Apr 2020 15:51:45 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 16:53:13 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Apr 2020 16:55:01 GMT
ENV CONSUL_VERSION=1.4.5
# Thu, 23 Apr 2020 16:55:01 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Apr 2020 16:55:03 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Apr 2020 16:55:11 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Apr 2020 16:55:14 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Apr 2020 16:55:16 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 16:55:17 GMT
VOLUME [/consul/data]
# Thu, 23 Apr 2020 16:55:18 GMT
EXPOSE 8300
# Thu, 23 Apr 2020 16:55:18 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Apr 2020 16:55:19 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Apr 2020 16:55:19 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Apr 2020 16:55:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 16:55:21 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:27da80392aebe463671b839837d59af1261218364b4261ceb2eca0f814075270`  
		Last Modified: Thu, 23 Apr 2020 15:52:21 GMT  
		Size: 2.5 MB (2548725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fc6a2c1c9905f1c2e05293927bd4dca9b2ea4d887a292d6c383e99f16e98e15`  
		Last Modified: Thu, 23 Apr 2020 16:59:49 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c1169780ec696a64b499a35ca473a20f4a2eeb0b742e572c9d1c1183ad122f`  
		Last Modified: Thu, 23 Apr 2020 16:59:54 GMT  
		Size: 34.4 MB (34423949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5a1d631b6086463cbdcad0750c6fd5864c28576b34df2bc29a22f89669f836`  
		Last Modified: Thu, 23 Apr 2020 16:59:49 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4dc00e27cb34467f4575dbc7966a56be1aa3be4f75d686a49ec7d6a6acb9a49`  
		Last Modified: Thu, 23 Apr 2020 16:59:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7b66a04b11afc36bbd5445117a1847f7b2093d02cb552802a4457cc9a311e83`  
		Last Modified: Thu, 23 Apr 2020 16:59:49 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.4` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:9d0b270062ca7bfc7e3cce9fe333356a8d3c748f272eb600c3ac4d0976838d67
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36791030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2a735556e7041d4de6c339d8f68ebbbd3ec4154495c5a96212c0d99b02ad11c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:54:58 GMT
ADD file:92767b5525acd9dbf8657931d32bdcc7cc504cdc33c95e84a75e478b00569bab in / 
# Thu, 23 Jan 2020 16:54:59 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:19:49 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Jan 2020 17:21:29 GMT
ENV CONSUL_VERSION=1.4.5
# Thu, 23 Jan 2020 17:21:30 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Jan 2020 17:21:33 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Jan 2020 17:21:41 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Jan 2020 17:21:43 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Jan 2020 17:21:47 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Jan 2020 17:21:48 GMT
VOLUME [/consul/data]
# Thu, 23 Jan 2020 17:21:49 GMT
EXPOSE 8300
# Thu, 23 Jan 2020 17:21:51 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Jan 2020 17:21:52 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Jan 2020 17:21:53 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 17:21:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 17:21:55 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:eb93038481ddcf86a625b70f7551cdc583e38886f206fe7e40ad644008efa815`  
		Last Modified: Thu, 23 Jan 2020 16:55:31 GMT  
		Size: 2.7 MB (2693238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152e314dadf8047c6af841428cd8f0e500b91d95d966b8e359644f2b59e20dbf`  
		Last Modified: Thu, 23 Jan 2020 17:26:18 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006c1a2a8bff1a062065f40aabd554fd4b8c518b856b9545969d48cd15c3a6c2`  
		Last Modified: Thu, 23 Jan 2020 17:26:50 GMT  
		Size: 34.1 MB (34094503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0eba5dacc287ff2bb7a9e2e93aaeb71bd297a017e6857df3e238c1e4edd348`  
		Last Modified: Thu, 23 Jan 2020 17:26:18 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1336cd3d92ebf35a59362b380985997672ab714945382c8bbf5638881135ed0a`  
		Last Modified: Thu, 23 Jan 2020 17:26:18 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6439e5bb7c9d7f3da8a7dd4a24467cf249e7bffef27f589c62012510b3d48cd0`  
		Last Modified: Thu, 23 Jan 2020 17:26:17 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.4` - linux; 386

```console
$ docker pull consul@sha256:86423594c5d6c41564cba1f9d40e4326d67382d3b2f4aaa5e06a08e3289141ae
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.4 MB (38368757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48f8b7990c7b5663a89f420f2bf180b0928be2fc0aa7f75c56d48a9cbc907bf2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:18 GMT
ADD file:68d5786259963a2b97cf808d79de83cbd0281dfea284e1a401bc851a3585e1bd in / 
# Thu, 23 Apr 2020 21:16:19 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 04:30:33 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Fri, 24 Apr 2020 04:31:15 GMT
ENV CONSUL_VERSION=1.4.5
# Fri, 24 Apr 2020 04:31:16 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 24 Apr 2020 04:31:16 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 24 Apr 2020 04:31:21 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 24 Apr 2020 04:31:22 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 24 Apr 2020 04:31:23 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 04:31:23 GMT
VOLUME [/consul/data]
# Fri, 24 Apr 2020 04:31:23 GMT
EXPOSE 8300
# Fri, 24 Apr 2020 04:31:23 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 24 Apr 2020 04:31:24 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 24 Apr 2020 04:31:24 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Apr 2020 04:31:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 04:31:24 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2f4fdbe0599cb5bbd0664b1cdad4997f428ce2495ae3eabf942129dc197d991c`  
		Last Modified: Thu, 23 Apr 2020 21:16:41 GMT  
		Size: 2.8 MB (2769736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c8b2b8200addb01a891e59e12456203f3628107edfd46fb6dc482da42fea289`  
		Last Modified: Fri, 24 Apr 2020 04:33:08 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f135280e1333dafa73df7d8473f7ee64f9c8f95d7c47b7b9dd152cd7f3770b05`  
		Last Modified: Fri, 24 Apr 2020 04:33:14 GMT  
		Size: 35.6 MB (35595790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9f6cc9c31ec9b55c5e894fd8717b29a969f109444e94167194b8e2dfaac0c7`  
		Last Modified: Fri, 24 Apr 2020 04:33:08 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85771b22dfb460e940cd0ae5bf5daaf56a177c1c1a161a69512c803e5c2eb9d`  
		Last Modified: Fri, 24 Apr 2020 04:33:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c599d350e76f776c8f981b6fa6d19dc1788d92a1a3f557d109a2ea0126bdcc`  
		Last Modified: Fri, 24 Apr 2020 04:33:08 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.4.5`

```console
$ docker pull consul@sha256:ca338881abc9f24b8f29874f74c757c12ced9b53eb7a53fce2072f19eea5dac2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.4.5` - linux; amd64

```console
$ docker pull consul@sha256:068a9a19ecd914c3364c5633917b72a898b461923ff56dd7500aa926f421c4b8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39199490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad32393b859a2a3bdd3411af9926171c1f5c96558f796a03dce84b164c314613`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:15:11 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Jan 2020 17:16:05 GMT
ENV CONSUL_VERSION=1.4.5
# Thu, 23 Jan 2020 17:16:05 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Jan 2020 17:16:07 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Jan 2020 17:16:13 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Jan 2020 17:16:14 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Jan 2020 17:16:15 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Jan 2020 17:16:16 GMT
VOLUME [/consul/data]
# Thu, 23 Jan 2020 17:16:16 GMT
EXPOSE 8300
# Thu, 23 Jan 2020 17:16:16 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Jan 2020 17:16:16 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Jan 2020 17:16:17 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 17:16:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 17:16:17 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7651bd62600c8b706e5120d2fe48d72e94904be0cc8d1a82d4d3f5de592b37`  
		Last Modified: Thu, 23 Jan 2020 17:19:00 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae6d22bb36b77217cd3fb3e007589cbfaf4076d1a1ad009150594dd270334d9`  
		Last Modified: Thu, 23 Jan 2020 17:19:32 GMT  
		Size: 36.4 MB (36432087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9697a7a1e3d9f33fe5891a4a3afab1ca81826b415f1575967c96fb7426b8d45e`  
		Last Modified: Thu, 23 Jan 2020 17:19:00 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5d89b529d3cc118de1dbf8c3b2554bc84510eb7afa942267aa3ffc94f94923`  
		Last Modified: Thu, 23 Jan 2020 17:19:00 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71722bc46238839f701198cdccdf1bd8330aa287d814044f6721c15038d9baeb`  
		Last Modified: Thu, 23 Jan 2020 17:19:00 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.4.5` - linux; arm variant v6

```console
$ docker pull consul@sha256:b46336852e3dbfc6455cdbc9f93ec6f106bd4ddaa683ea345f17afa10c39dc27
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36975963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b23daecfc8abc2af29f8313f7ecde84a78c6ab55449160103c2e9a5b0290957`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:44 GMT
ADD file:7dd2657543fac7f63a125194d27bd38a8e472a3076831a2331c43a471794c210 in / 
# Thu, 23 Apr 2020 15:51:45 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 16:53:13 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Apr 2020 16:55:01 GMT
ENV CONSUL_VERSION=1.4.5
# Thu, 23 Apr 2020 16:55:01 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Apr 2020 16:55:03 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Apr 2020 16:55:11 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Apr 2020 16:55:14 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Apr 2020 16:55:16 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 16:55:17 GMT
VOLUME [/consul/data]
# Thu, 23 Apr 2020 16:55:18 GMT
EXPOSE 8300
# Thu, 23 Apr 2020 16:55:18 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Apr 2020 16:55:19 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Apr 2020 16:55:19 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Apr 2020 16:55:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 16:55:21 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:27da80392aebe463671b839837d59af1261218364b4261ceb2eca0f814075270`  
		Last Modified: Thu, 23 Apr 2020 15:52:21 GMT  
		Size: 2.5 MB (2548725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fc6a2c1c9905f1c2e05293927bd4dca9b2ea4d887a292d6c383e99f16e98e15`  
		Last Modified: Thu, 23 Apr 2020 16:59:49 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c1169780ec696a64b499a35ca473a20f4a2eeb0b742e572c9d1c1183ad122f`  
		Last Modified: Thu, 23 Apr 2020 16:59:54 GMT  
		Size: 34.4 MB (34423949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5a1d631b6086463cbdcad0750c6fd5864c28576b34df2bc29a22f89669f836`  
		Last Modified: Thu, 23 Apr 2020 16:59:49 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4dc00e27cb34467f4575dbc7966a56be1aa3be4f75d686a49ec7d6a6acb9a49`  
		Last Modified: Thu, 23 Apr 2020 16:59:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7b66a04b11afc36bbd5445117a1847f7b2093d02cb552802a4457cc9a311e83`  
		Last Modified: Thu, 23 Apr 2020 16:59:49 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.4.5` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:9d0b270062ca7bfc7e3cce9fe333356a8d3c748f272eb600c3ac4d0976838d67
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36791030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2a735556e7041d4de6c339d8f68ebbbd3ec4154495c5a96212c0d99b02ad11c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:54:58 GMT
ADD file:92767b5525acd9dbf8657931d32bdcc7cc504cdc33c95e84a75e478b00569bab in / 
# Thu, 23 Jan 2020 16:54:59 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:19:49 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Jan 2020 17:21:29 GMT
ENV CONSUL_VERSION=1.4.5
# Thu, 23 Jan 2020 17:21:30 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Jan 2020 17:21:33 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Jan 2020 17:21:41 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Jan 2020 17:21:43 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Jan 2020 17:21:47 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Jan 2020 17:21:48 GMT
VOLUME [/consul/data]
# Thu, 23 Jan 2020 17:21:49 GMT
EXPOSE 8300
# Thu, 23 Jan 2020 17:21:51 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Jan 2020 17:21:52 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Jan 2020 17:21:53 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 17:21:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 17:21:55 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:eb93038481ddcf86a625b70f7551cdc583e38886f206fe7e40ad644008efa815`  
		Last Modified: Thu, 23 Jan 2020 16:55:31 GMT  
		Size: 2.7 MB (2693238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152e314dadf8047c6af841428cd8f0e500b91d95d966b8e359644f2b59e20dbf`  
		Last Modified: Thu, 23 Jan 2020 17:26:18 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006c1a2a8bff1a062065f40aabd554fd4b8c518b856b9545969d48cd15c3a6c2`  
		Last Modified: Thu, 23 Jan 2020 17:26:50 GMT  
		Size: 34.1 MB (34094503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0eba5dacc287ff2bb7a9e2e93aaeb71bd297a017e6857df3e238c1e4edd348`  
		Last Modified: Thu, 23 Jan 2020 17:26:18 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1336cd3d92ebf35a59362b380985997672ab714945382c8bbf5638881135ed0a`  
		Last Modified: Thu, 23 Jan 2020 17:26:18 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6439e5bb7c9d7f3da8a7dd4a24467cf249e7bffef27f589c62012510b3d48cd0`  
		Last Modified: Thu, 23 Jan 2020 17:26:17 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.4.5` - linux; 386

```console
$ docker pull consul@sha256:86423594c5d6c41564cba1f9d40e4326d67382d3b2f4aaa5e06a08e3289141ae
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.4 MB (38368757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48f8b7990c7b5663a89f420f2bf180b0928be2fc0aa7f75c56d48a9cbc907bf2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:18 GMT
ADD file:68d5786259963a2b97cf808d79de83cbd0281dfea284e1a401bc851a3585e1bd in / 
# Thu, 23 Apr 2020 21:16:19 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 04:30:33 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Fri, 24 Apr 2020 04:31:15 GMT
ENV CONSUL_VERSION=1.4.5
# Fri, 24 Apr 2020 04:31:16 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 24 Apr 2020 04:31:16 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 24 Apr 2020 04:31:21 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 24 Apr 2020 04:31:22 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 24 Apr 2020 04:31:23 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 04:31:23 GMT
VOLUME [/consul/data]
# Fri, 24 Apr 2020 04:31:23 GMT
EXPOSE 8300
# Fri, 24 Apr 2020 04:31:23 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 24 Apr 2020 04:31:24 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 24 Apr 2020 04:31:24 GMT
COPY file:2fc9ee792fd5d6e21568c1fcc92d825866250fafd9f3c82331ad98c840b3dd45 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Apr 2020 04:31:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 04:31:24 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2f4fdbe0599cb5bbd0664b1cdad4997f428ce2495ae3eabf942129dc197d991c`  
		Last Modified: Thu, 23 Apr 2020 21:16:41 GMT  
		Size: 2.8 MB (2769736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c8b2b8200addb01a891e59e12456203f3628107edfd46fb6dc482da42fea289`  
		Last Modified: Fri, 24 Apr 2020 04:33:08 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f135280e1333dafa73df7d8473f7ee64f9c8f95d7c47b7b9dd152cd7f3770b05`  
		Last Modified: Fri, 24 Apr 2020 04:33:14 GMT  
		Size: 35.6 MB (35595790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9f6cc9c31ec9b55c5e894fd8717b29a969f109444e94167194b8e2dfaac0c7`  
		Last Modified: Fri, 24 Apr 2020 04:33:08 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85771b22dfb460e940cd0ae5bf5daaf56a177c1c1a161a69512c803e5c2eb9d`  
		Last Modified: Fri, 24 Apr 2020 04:33:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c599d350e76f776c8f981b6fa6d19dc1788d92a1a3f557d109a2ea0126bdcc`  
		Last Modified: Fri, 24 Apr 2020 04:33:08 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.5`

```console
$ docker pull consul@sha256:de31807eba3f4a418faea8832681ba0bb707ecc617eade26e45310f9c1c28b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.5` - linux; amd64

```console
$ docker pull consul@sha256:9417ce87d497f80f8282d3b74f74c511f41f903b7178d4b3a894dd15e265fe03
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44182203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5ce9a832eeab346273f7d1afffc1b80f770c2cf945c42ec159a183fc7ef989b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:15:11 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Jan 2020 17:15:47 GMT
ENV CONSUL_VERSION=1.5.3
# Thu, 23 Jan 2020 17:15:48 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Jan 2020 17:15:49 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Jan 2020 17:15:56 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Jan 2020 17:15:57 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Jan 2020 17:15:58 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Jan 2020 17:15:59 GMT
VOLUME [/consul/data]
# Thu, 23 Jan 2020 17:15:59 GMT
EXPOSE 8300
# Thu, 23 Jan 2020 17:15:59 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Jan 2020 17:15:59 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Jan 2020 17:16:00 GMT
COPY file:1c5f16053db7ac80ca2606114b1597e5421edf31162ea24a1ae8b059f48426f0 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 17:16:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 17:16:00 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4fdbcc757f800c98634ea57a90e25a5d71c8085047e7ef27a211baf791fbdf`  
		Last Modified: Thu, 23 Jan 2020 17:18:28 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c44a9b8d9f471fc81fea2fc3f754811b086921ce0e6ddc722666eeee59f4eab`  
		Last Modified: Thu, 23 Jan 2020 17:18:55 GMT  
		Size: 41.4 MB (41414773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b242415903bd0e91c2cf4db11a46a35e8ce72ce17cfb5bbc04c8ce1b4b37352`  
		Last Modified: Thu, 23 Jan 2020 17:18:29 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c602c8120e311bf687ab5541322da039164743f236c5d4dc8043b482e1662d`  
		Last Modified: Thu, 23 Jan 2020 17:18:29 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085df52b698732618e7ef9a5ab9ddb19f16a7225fb7e3b18757b7356529e85e8`  
		Last Modified: Thu, 23 Jan 2020 17:18:28 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.5` - linux; arm variant v6

```console
$ docker pull consul@sha256:ff332dcbc1c975cf0e9f97b7cdc17628d86613ec97dd177ab8d910b7b52edaab
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41568703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14709419af3bf1f0a49998d7b68286650003b784c886e1f0317cb01b2fffaed0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:44 GMT
ADD file:7dd2657543fac7f63a125194d27bd38a8e472a3076831a2331c43a471794c210 in / 
# Thu, 23 Apr 2020 15:51:45 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 16:53:13 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Apr 2020 16:54:25 GMT
ENV CONSUL_VERSION=1.5.3
# Thu, 23 Apr 2020 16:54:25 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Apr 2020 16:54:27 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Apr 2020 16:54:38 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Apr 2020 16:54:43 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Apr 2020 16:54:47 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 16:54:49 GMT
VOLUME [/consul/data]
# Thu, 23 Apr 2020 16:54:50 GMT
EXPOSE 8300
# Thu, 23 Apr 2020 16:54:51 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Apr 2020 16:54:52 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Apr 2020 16:54:53 GMT
COPY file:1c5f16053db7ac80ca2606114b1597e5421edf31162ea24a1ae8b059f48426f0 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Apr 2020 16:54:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 16:54:55 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:27da80392aebe463671b839837d59af1261218364b4261ceb2eca0f814075270`  
		Last Modified: Thu, 23 Apr 2020 15:52:21 GMT  
		Size: 2.5 MB (2548725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828086b8d7d91f4c09cb0970444f1c9d4e21273a3c999ec514a666c74d92361d`  
		Last Modified: Thu, 23 Apr 2020 16:59:28 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5d7a670146edc486ef7717c5bc485a5fd43b1ef268b8573d83ce0d99eae508`  
		Last Modified: Thu, 23 Apr 2020 16:59:38 GMT  
		Size: 39.0 MB (39016662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d856f5478a381990258f8f0eccf2a569669ac03142d17ecaa855fe570b140a`  
		Last Modified: Thu, 23 Apr 2020 16:59:28 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19539467f60ea7c0deafae4c562165c8225b6046047b740a3d7446aa4005e322`  
		Last Modified: Thu, 23 Apr 2020 16:59:28 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9ed0d4d8a34d9590b1e5c97972755278a3b19ee99303dcc4c46c36c87f7a98`  
		Last Modified: Thu, 23 Apr 2020 16:59:28 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.5` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:b93c8d7effcca6871ef3dc097b014579924e0e9e53562e153104c61467e2794f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41736776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78d71d8a623b84732d5eb46672cbd1526aa74216b8d824250ef3bebf908db4f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:54:58 GMT
ADD file:92767b5525acd9dbf8657931d32bdcc7cc504cdc33c95e84a75e478b00569bab in / 
# Thu, 23 Jan 2020 16:54:59 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:19:49 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Jan 2020 17:20:53 GMT
ENV CONSUL_VERSION=1.5.3
# Thu, 23 Jan 2020 17:20:55 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Jan 2020 17:20:58 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Jan 2020 17:21:06 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Jan 2020 17:21:09 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Jan 2020 17:21:12 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Jan 2020 17:21:13 GMT
VOLUME [/consul/data]
# Thu, 23 Jan 2020 17:21:14 GMT
EXPOSE 8300
# Thu, 23 Jan 2020 17:21:15 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Jan 2020 17:21:15 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Jan 2020 17:21:16 GMT
COPY file:1c5f16053db7ac80ca2606114b1597e5421edf31162ea24a1ae8b059f48426f0 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 17:21:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 17:21:18 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:eb93038481ddcf86a625b70f7551cdc583e38886f206fe7e40ad644008efa815`  
		Last Modified: Thu, 23 Jan 2020 16:55:31 GMT  
		Size: 2.7 MB (2693238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66847b9d670332a71d6ede4a344d51162e0bdc6abd08a754f4de9c778ccfa1e4`  
		Last Modified: Thu, 23 Jan 2020 17:25:59 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add30ea62b96d1847e5af034c9942292447570d2feec35e349a29f3735569813`  
		Last Modified: Thu, 23 Jan 2020 17:26:11 GMT  
		Size: 39.0 MB (39040224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be64c310d7e9e83c8eadea0c99bce2a7949b115ceb55cc1470be31aaa8f7d21`  
		Last Modified: Thu, 23 Jan 2020 17:25:59 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5a2cf4964adaae1e25835708056bd14251cab62851cffa4452be09bd8c04a8`  
		Last Modified: Thu, 23 Jan 2020 17:25:59 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f808e5522e7eb3f5020ce3a4b64f87a4511c14ef14229c479ac2796d10ff6d52`  
		Last Modified: Thu, 23 Jan 2020 17:25:59 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.5` - linux; 386

```console
$ docker pull consul@sha256:6b984cc5dae695862a8d7b2a075e011d81f9b9b710d392c99845d902ff36bced
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43094688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a6106b89ce5d052f34ccd0848d646e1bb0a3cca64488b2ebf2f65b534ceafb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:18 GMT
ADD file:68d5786259963a2b97cf808d79de83cbd0281dfea284e1a401bc851a3585e1bd in / 
# Thu, 23 Apr 2020 21:16:19 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 04:30:33 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Fri, 24 Apr 2020 04:31:01 GMT
ENV CONSUL_VERSION=1.5.3
# Fri, 24 Apr 2020 04:31:02 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 24 Apr 2020 04:31:02 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 24 Apr 2020 04:31:08 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 24 Apr 2020 04:31:08 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 24 Apr 2020 04:31:09 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 04:31:09 GMT
VOLUME [/consul/data]
# Fri, 24 Apr 2020 04:31:10 GMT
EXPOSE 8300
# Fri, 24 Apr 2020 04:31:10 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 24 Apr 2020 04:31:10 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 24 Apr 2020 04:31:10 GMT
COPY file:1c5f16053db7ac80ca2606114b1597e5421edf31162ea24a1ae8b059f48426f0 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Apr 2020 04:31:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 04:31:11 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2f4fdbe0599cb5bbd0664b1cdad4997f428ce2495ae3eabf942129dc197d991c`  
		Last Modified: Thu, 23 Apr 2020 21:16:41 GMT  
		Size: 2.8 MB (2769736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3374db1f49fc2155d0d21f82a744d34851aa1e0e549d7e7f043e3106952a8c1e`  
		Last Modified: Fri, 24 Apr 2020 04:32:57 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a332ea3adc7dfdbb16bf9023e1ab94df85adaad801c06931061d599296df37e`  
		Last Modified: Fri, 24 Apr 2020 04:33:03 GMT  
		Size: 40.3 MB (40321693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:118c0e8dc76e675fdc5b57fe37ea1bf62e5a14688cbf471324d5df068ca27cc0`  
		Last Modified: Fri, 24 Apr 2020 04:32:56 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2482ee4cfa303bdd919ed1245d7cefb6db230d741d24e7d335ea89f6fac9bc1`  
		Last Modified: Fri, 24 Apr 2020 04:32:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24266bee77a3f06e1448eda49f0b1a15ac0eae7bf313a82e55512d12b4b2b6e0`  
		Last Modified: Fri, 24 Apr 2020 04:32:56 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.5.3`

```console
$ docker pull consul@sha256:de31807eba3f4a418faea8832681ba0bb707ecc617eade26e45310f9c1c28b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.5.3` - linux; amd64

```console
$ docker pull consul@sha256:9417ce87d497f80f8282d3b74f74c511f41f903b7178d4b3a894dd15e265fe03
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44182203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5ce9a832eeab346273f7d1afffc1b80f770c2cf945c42ec159a183fc7ef989b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:15:11 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Jan 2020 17:15:47 GMT
ENV CONSUL_VERSION=1.5.3
# Thu, 23 Jan 2020 17:15:48 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Jan 2020 17:15:49 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Jan 2020 17:15:56 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Jan 2020 17:15:57 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Jan 2020 17:15:58 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Jan 2020 17:15:59 GMT
VOLUME [/consul/data]
# Thu, 23 Jan 2020 17:15:59 GMT
EXPOSE 8300
# Thu, 23 Jan 2020 17:15:59 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Jan 2020 17:15:59 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Jan 2020 17:16:00 GMT
COPY file:1c5f16053db7ac80ca2606114b1597e5421edf31162ea24a1ae8b059f48426f0 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 17:16:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 17:16:00 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4fdbcc757f800c98634ea57a90e25a5d71c8085047e7ef27a211baf791fbdf`  
		Last Modified: Thu, 23 Jan 2020 17:18:28 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c44a9b8d9f471fc81fea2fc3f754811b086921ce0e6ddc722666eeee59f4eab`  
		Last Modified: Thu, 23 Jan 2020 17:18:55 GMT  
		Size: 41.4 MB (41414773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b242415903bd0e91c2cf4db11a46a35e8ce72ce17cfb5bbc04c8ce1b4b37352`  
		Last Modified: Thu, 23 Jan 2020 17:18:29 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c602c8120e311bf687ab5541322da039164743f236c5d4dc8043b482e1662d`  
		Last Modified: Thu, 23 Jan 2020 17:18:29 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085df52b698732618e7ef9a5ab9ddb19f16a7225fb7e3b18757b7356529e85e8`  
		Last Modified: Thu, 23 Jan 2020 17:18:28 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.5.3` - linux; arm variant v6

```console
$ docker pull consul@sha256:ff332dcbc1c975cf0e9f97b7cdc17628d86613ec97dd177ab8d910b7b52edaab
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41568703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14709419af3bf1f0a49998d7b68286650003b784c886e1f0317cb01b2fffaed0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:44 GMT
ADD file:7dd2657543fac7f63a125194d27bd38a8e472a3076831a2331c43a471794c210 in / 
# Thu, 23 Apr 2020 15:51:45 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 16:53:13 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Apr 2020 16:54:25 GMT
ENV CONSUL_VERSION=1.5.3
# Thu, 23 Apr 2020 16:54:25 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Apr 2020 16:54:27 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Apr 2020 16:54:38 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Apr 2020 16:54:43 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Apr 2020 16:54:47 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 16:54:49 GMT
VOLUME [/consul/data]
# Thu, 23 Apr 2020 16:54:50 GMT
EXPOSE 8300
# Thu, 23 Apr 2020 16:54:51 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Apr 2020 16:54:52 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Apr 2020 16:54:53 GMT
COPY file:1c5f16053db7ac80ca2606114b1597e5421edf31162ea24a1ae8b059f48426f0 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Apr 2020 16:54:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 16:54:55 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:27da80392aebe463671b839837d59af1261218364b4261ceb2eca0f814075270`  
		Last Modified: Thu, 23 Apr 2020 15:52:21 GMT  
		Size: 2.5 MB (2548725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828086b8d7d91f4c09cb0970444f1c9d4e21273a3c999ec514a666c74d92361d`  
		Last Modified: Thu, 23 Apr 2020 16:59:28 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5d7a670146edc486ef7717c5bc485a5fd43b1ef268b8573d83ce0d99eae508`  
		Last Modified: Thu, 23 Apr 2020 16:59:38 GMT  
		Size: 39.0 MB (39016662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d856f5478a381990258f8f0eccf2a569669ac03142d17ecaa855fe570b140a`  
		Last Modified: Thu, 23 Apr 2020 16:59:28 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19539467f60ea7c0deafae4c562165c8225b6046047b740a3d7446aa4005e322`  
		Last Modified: Thu, 23 Apr 2020 16:59:28 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9ed0d4d8a34d9590b1e5c97972755278a3b19ee99303dcc4c46c36c87f7a98`  
		Last Modified: Thu, 23 Apr 2020 16:59:28 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.5.3` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:b93c8d7effcca6871ef3dc097b014579924e0e9e53562e153104c61467e2794f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41736776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78d71d8a623b84732d5eb46672cbd1526aa74216b8d824250ef3bebf908db4f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:54:58 GMT
ADD file:92767b5525acd9dbf8657931d32bdcc7cc504cdc33c95e84a75e478b00569bab in / 
# Thu, 23 Jan 2020 16:54:59 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:19:49 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Jan 2020 17:20:53 GMT
ENV CONSUL_VERSION=1.5.3
# Thu, 23 Jan 2020 17:20:55 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Jan 2020 17:20:58 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Jan 2020 17:21:06 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Jan 2020 17:21:09 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Jan 2020 17:21:12 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Jan 2020 17:21:13 GMT
VOLUME [/consul/data]
# Thu, 23 Jan 2020 17:21:14 GMT
EXPOSE 8300
# Thu, 23 Jan 2020 17:21:15 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Jan 2020 17:21:15 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Jan 2020 17:21:16 GMT
COPY file:1c5f16053db7ac80ca2606114b1597e5421edf31162ea24a1ae8b059f48426f0 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 17:21:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 17:21:18 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:eb93038481ddcf86a625b70f7551cdc583e38886f206fe7e40ad644008efa815`  
		Last Modified: Thu, 23 Jan 2020 16:55:31 GMT  
		Size: 2.7 MB (2693238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66847b9d670332a71d6ede4a344d51162e0bdc6abd08a754f4de9c778ccfa1e4`  
		Last Modified: Thu, 23 Jan 2020 17:25:59 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add30ea62b96d1847e5af034c9942292447570d2feec35e349a29f3735569813`  
		Last Modified: Thu, 23 Jan 2020 17:26:11 GMT  
		Size: 39.0 MB (39040224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be64c310d7e9e83c8eadea0c99bce2a7949b115ceb55cc1470be31aaa8f7d21`  
		Last Modified: Thu, 23 Jan 2020 17:25:59 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5a2cf4964adaae1e25835708056bd14251cab62851cffa4452be09bd8c04a8`  
		Last Modified: Thu, 23 Jan 2020 17:25:59 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f808e5522e7eb3f5020ce3a4b64f87a4511c14ef14229c479ac2796d10ff6d52`  
		Last Modified: Thu, 23 Jan 2020 17:25:59 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.5.3` - linux; 386

```console
$ docker pull consul@sha256:6b984cc5dae695862a8d7b2a075e011d81f9b9b710d392c99845d902ff36bced
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43094688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a6106b89ce5d052f34ccd0848d646e1bb0a3cca64488b2ebf2f65b534ceafb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:18 GMT
ADD file:68d5786259963a2b97cf808d79de83cbd0281dfea284e1a401bc851a3585e1bd in / 
# Thu, 23 Apr 2020 21:16:19 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 04:30:33 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Fri, 24 Apr 2020 04:31:01 GMT
ENV CONSUL_VERSION=1.5.3
# Fri, 24 Apr 2020 04:31:02 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 24 Apr 2020 04:31:02 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 24 Apr 2020 04:31:08 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 24 Apr 2020 04:31:08 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 24 Apr 2020 04:31:09 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 04:31:09 GMT
VOLUME [/consul/data]
# Fri, 24 Apr 2020 04:31:10 GMT
EXPOSE 8300
# Fri, 24 Apr 2020 04:31:10 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 24 Apr 2020 04:31:10 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 24 Apr 2020 04:31:10 GMT
COPY file:1c5f16053db7ac80ca2606114b1597e5421edf31162ea24a1ae8b059f48426f0 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Apr 2020 04:31:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 04:31:11 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2f4fdbe0599cb5bbd0664b1cdad4997f428ce2495ae3eabf942129dc197d991c`  
		Last Modified: Thu, 23 Apr 2020 21:16:41 GMT  
		Size: 2.8 MB (2769736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3374db1f49fc2155d0d21f82a744d34851aa1e0e549d7e7f043e3106952a8c1e`  
		Last Modified: Fri, 24 Apr 2020 04:32:57 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a332ea3adc7dfdbb16bf9023e1ab94df85adaad801c06931061d599296df37e`  
		Last Modified: Fri, 24 Apr 2020 04:33:03 GMT  
		Size: 40.3 MB (40321693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:118c0e8dc76e675fdc5b57fe37ea1bf62e5a14688cbf471324d5df068ca27cc0`  
		Last Modified: Fri, 24 Apr 2020 04:32:56 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2482ee4cfa303bdd919ed1245d7cefb6db230d741d24e7d335ea89f6fac9bc1`  
		Last Modified: Fri, 24 Apr 2020 04:32:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24266bee77a3f06e1448eda49f0b1a15ac0eae7bf313a82e55512d12b4b2b6e0`  
		Last Modified: Fri, 24 Apr 2020 04:32:56 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.6`

```console
$ docker pull consul@sha256:ac893e01feedc4b8c65335d646f7d7cbac24879f3d72c1ab8de88b8abaac3b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.6` - linux; amd64

```console
$ docker pull consul@sha256:7e78b7230a1df63eb3afa97e98b49589d1a7c9d81b90ac477cf4b4700464dfc8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44655160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b77370cb915a06783766956432788e0c2e3c3b3e1fecf33a974b4a34dc5d5c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:15:11 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Fri, 21 Feb 2020 02:36:25 GMT
ENV CONSUL_VERSION=1.6.4
# Fri, 21 Feb 2020 02:36:25 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 21 Feb 2020 02:36:27 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 21 Feb 2020 02:36:35 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 21 Feb 2020 02:36:36 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 21 Feb 2020 02:36:38 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 21 Feb 2020 02:36:38 GMT
VOLUME [/consul/data]
# Fri, 21 Feb 2020 02:36:38 GMT
EXPOSE 8300
# Fri, 21 Feb 2020 02:36:39 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 21 Feb 2020 02:36:39 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 21 Feb 2020 02:36:40 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 21 Feb 2020 02:36:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 02:36:40 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d5cef50d4b38b608f5e38cd313b050ac76949636fa4bc270c374edd7a2da46`  
		Last Modified: Fri, 21 Feb 2020 02:37:49 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4a7f3b259832af2b8a6e252d20c95d7720ed9be13139ddb532c42dce8bd76e`  
		Last Modified: Fri, 21 Feb 2020 02:37:55 GMT  
		Size: 41.9 MB (41887732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13bc04b0405b2cd7f2f79fc2db365db82715bf4cd37cfad3f7d9c48560a03bf`  
		Last Modified: Fri, 21 Feb 2020 02:37:49 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e720e5ab18939c7f2d4a7eb572953396fa40512d197e9e94a1a72ca1b74ba45`  
		Last Modified: Fri, 21 Feb 2020 02:37:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42311f725a9b1184e0991185958ed031c62752342ebefd7a56b779aa04bd2337`  
		Last Modified: Fri, 21 Feb 2020 02:37:49 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.6` - linux; arm variant v6

```console
$ docker pull consul@sha256:ffde7f7119ba2b82be0cd46bc4a1b4b1046406c4541c2acee537a9eb594ee83d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (42041119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a961cfe68259a8f46766449996b547295ae12aaa5a8fea3f2ef4d1b304f169d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:44 GMT
ADD file:7dd2657543fac7f63a125194d27bd38a8e472a3076831a2331c43a471794c210 in / 
# Thu, 23 Apr 2020 15:51:45 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 16:53:13 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Apr 2020 16:53:53 GMT
ENV CONSUL_VERSION=1.6.4
# Thu, 23 Apr 2020 16:53:54 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Apr 2020 16:53:56 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Apr 2020 16:54:07 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Apr 2020 16:54:10 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Apr 2020 16:54:12 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 16:54:13 GMT
VOLUME [/consul/data]
# Thu, 23 Apr 2020 16:54:13 GMT
EXPOSE 8300
# Thu, 23 Apr 2020 16:54:14 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Apr 2020 16:54:15 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Apr 2020 16:54:15 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Apr 2020 16:54:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 16:54:17 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:27da80392aebe463671b839837d59af1261218364b4261ceb2eca0f814075270`  
		Last Modified: Thu, 23 Apr 2020 15:52:21 GMT  
		Size: 2.5 MB (2548725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83c6e486bc251b948d2220b5138f16af3c90eafb66c61ddfb288ba9bc16c488`  
		Last Modified: Thu, 23 Apr 2020 16:59:11 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753852023b66df826ee77175e8071aceba91596dbb826636735502f592f5b7b2`  
		Last Modified: Thu, 23 Apr 2020 16:59:21 GMT  
		Size: 39.5 MB (39489079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171ce168cc0eec5045f16c757a6e195ee850a0c6fe5a35455eade5b7b21205b3`  
		Last Modified: Thu, 23 Apr 2020 16:59:11 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97521971145e342b2c6d92e6ad348d8ab8299fec5f5effe422e6a7dd66191b71`  
		Last Modified: Thu, 23 Apr 2020 16:59:11 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44fdbe8131b8e1d3d21d683cf220bd62dc9acf2e1789eaa2c0748ce98ac0b358`  
		Last Modified: Thu, 23 Apr 2020 16:59:10 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.6` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:45c251efcd9fdc153a57a1e9c550bf2828036095270e4d3e20cfed16ba5a59df
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40230231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f282ac0e02ae37a1787090557d669063197b2c5efd95044e012c20907aa3fd0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:54:58 GMT
ADD file:92767b5525acd9dbf8657931d32bdcc7cc504cdc33c95e84a75e478b00569bab in / 
# Thu, 23 Jan 2020 16:54:59 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:19:49 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Fri, 21 Feb 2020 00:42:00 GMT
ENV CONSUL_VERSION=1.6.4
# Fri, 21 Feb 2020 00:42:04 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 21 Feb 2020 00:42:12 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 21 Feb 2020 00:42:20 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 21 Feb 2020 00:42:23 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 21 Feb 2020 00:42:25 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 21 Feb 2020 00:42:26 GMT
VOLUME [/consul/data]
# Fri, 21 Feb 2020 00:42:27 GMT
EXPOSE 8300
# Fri, 21 Feb 2020 00:42:29 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 21 Feb 2020 00:42:29 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 21 Feb 2020 00:42:31 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 21 Feb 2020 00:42:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 00:42:34 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:eb93038481ddcf86a625b70f7551cdc583e38886f206fe7e40ad644008efa815`  
		Last Modified: Thu, 23 Jan 2020 16:55:31 GMT  
		Size: 2.7 MB (2693238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55512e1a6a5525e7fb15efa167d7b8ed30d1a2723c34a719c45c74a95ba8ebcf`  
		Last Modified: Fri, 21 Feb 2020 00:43:50 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb7968d4ace046b77e9b05c2b398c7a5e86000cee7996f0e698cfcb1598540a`  
		Last Modified: Fri, 21 Feb 2020 00:44:01 GMT  
		Size: 37.5 MB (37533680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c9f416575dcc099e0506c1b942c901424b400787ff46c1cc11a9af93890e1b`  
		Last Modified: Fri, 21 Feb 2020 00:43:50 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3114b18a4e7ae06ce6b0a199fc1d5f315c27b489ee9913b18311dc1457f2250`  
		Last Modified: Fri, 21 Feb 2020 00:43:50 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244002b6859d532f222a92e6c92a20588aeefc33c15352db6663d463afacad52`  
		Last Modified: Fri, 21 Feb 2020 00:43:50 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.6` - linux; 386

```console
$ docker pull consul@sha256:a56cd17592810ef83c8b2cfea552e80ea1ff47e30a143e8dfd85f58d091edac0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43564854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e51ebb91e20f2ab0eab9b14934ace03d5c0c533dd2e65fddbbded72050ab651b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:18 GMT
ADD file:68d5786259963a2b97cf808d79de83cbd0281dfea284e1a401bc851a3585e1bd in / 
# Thu, 23 Apr 2020 21:16:19 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 04:30:33 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Fri, 24 Apr 2020 04:30:47 GMT
ENV CONSUL_VERSION=1.6.4
# Fri, 24 Apr 2020 04:30:47 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 24 Apr 2020 04:30:48 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 24 Apr 2020 04:30:53 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 24 Apr 2020 04:30:54 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 24 Apr 2020 04:30:55 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 04:30:55 GMT
VOLUME [/consul/data]
# Fri, 24 Apr 2020 04:30:55 GMT
EXPOSE 8300
# Fri, 24 Apr 2020 04:30:56 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 24 Apr 2020 04:30:56 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 24 Apr 2020 04:30:56 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Apr 2020 04:30:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 04:30:56 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2f4fdbe0599cb5bbd0664b1cdad4997f428ce2495ae3eabf942129dc197d991c`  
		Last Modified: Thu, 23 Apr 2020 21:16:41 GMT  
		Size: 2.8 MB (2769736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f568d665eb8b0a76b0aa1413fda0d4420e3d26176df683dc9b5df735622a94`  
		Last Modified: Fri, 24 Apr 2020 04:32:45 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc8283ec022c872af08a5afbf7824fdb4f2250430a67afeb903c7ff57b33af9`  
		Last Modified: Fri, 24 Apr 2020 04:32:52 GMT  
		Size: 40.8 MB (40791861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a07385c2a70b08fb4573241222b0941b800763c74eb13ee946bdbcd89d0ec3c`  
		Last Modified: Fri, 24 Apr 2020 04:32:45 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3321e56ff68bad78adef6232b96a4cc1b2ea8b969e53ceb906ef71257982f195`  
		Last Modified: Fri, 24 Apr 2020 04:32:45 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b6c76dbfbce3561478fe4a0afa0a544f01b73515f8bbbbb3b817774d1bd876a`  
		Last Modified: Fri, 24 Apr 2020 04:32:45 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.6.4`

```console
$ docker pull consul@sha256:ac893e01feedc4b8c65335d646f7d7cbac24879f3d72c1ab8de88b8abaac3b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.6.4` - linux; amd64

```console
$ docker pull consul@sha256:7e78b7230a1df63eb3afa97e98b49589d1a7c9d81b90ac477cf4b4700464dfc8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44655160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b77370cb915a06783766956432788e0c2e3c3b3e1fecf33a974b4a34dc5d5c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:15:11 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Fri, 21 Feb 2020 02:36:25 GMT
ENV CONSUL_VERSION=1.6.4
# Fri, 21 Feb 2020 02:36:25 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 21 Feb 2020 02:36:27 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 21 Feb 2020 02:36:35 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 21 Feb 2020 02:36:36 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 21 Feb 2020 02:36:38 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 21 Feb 2020 02:36:38 GMT
VOLUME [/consul/data]
# Fri, 21 Feb 2020 02:36:38 GMT
EXPOSE 8300
# Fri, 21 Feb 2020 02:36:39 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 21 Feb 2020 02:36:39 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 21 Feb 2020 02:36:40 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 21 Feb 2020 02:36:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 02:36:40 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d5cef50d4b38b608f5e38cd313b050ac76949636fa4bc270c374edd7a2da46`  
		Last Modified: Fri, 21 Feb 2020 02:37:49 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4a7f3b259832af2b8a6e252d20c95d7720ed9be13139ddb532c42dce8bd76e`  
		Last Modified: Fri, 21 Feb 2020 02:37:55 GMT  
		Size: 41.9 MB (41887732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13bc04b0405b2cd7f2f79fc2db365db82715bf4cd37cfad3f7d9c48560a03bf`  
		Last Modified: Fri, 21 Feb 2020 02:37:49 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e720e5ab18939c7f2d4a7eb572953396fa40512d197e9e94a1a72ca1b74ba45`  
		Last Modified: Fri, 21 Feb 2020 02:37:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42311f725a9b1184e0991185958ed031c62752342ebefd7a56b779aa04bd2337`  
		Last Modified: Fri, 21 Feb 2020 02:37:49 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.6.4` - linux; arm variant v6

```console
$ docker pull consul@sha256:ffde7f7119ba2b82be0cd46bc4a1b4b1046406c4541c2acee537a9eb594ee83d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (42041119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a961cfe68259a8f46766449996b547295ae12aaa5a8fea3f2ef4d1b304f169d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:44 GMT
ADD file:7dd2657543fac7f63a125194d27bd38a8e472a3076831a2331c43a471794c210 in / 
# Thu, 23 Apr 2020 15:51:45 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 16:53:13 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Apr 2020 16:53:53 GMT
ENV CONSUL_VERSION=1.6.4
# Thu, 23 Apr 2020 16:53:54 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Apr 2020 16:53:56 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Apr 2020 16:54:07 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Apr 2020 16:54:10 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Apr 2020 16:54:12 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 16:54:13 GMT
VOLUME [/consul/data]
# Thu, 23 Apr 2020 16:54:13 GMT
EXPOSE 8300
# Thu, 23 Apr 2020 16:54:14 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Apr 2020 16:54:15 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Apr 2020 16:54:15 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Apr 2020 16:54:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 16:54:17 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:27da80392aebe463671b839837d59af1261218364b4261ceb2eca0f814075270`  
		Last Modified: Thu, 23 Apr 2020 15:52:21 GMT  
		Size: 2.5 MB (2548725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83c6e486bc251b948d2220b5138f16af3c90eafb66c61ddfb288ba9bc16c488`  
		Last Modified: Thu, 23 Apr 2020 16:59:11 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753852023b66df826ee77175e8071aceba91596dbb826636735502f592f5b7b2`  
		Last Modified: Thu, 23 Apr 2020 16:59:21 GMT  
		Size: 39.5 MB (39489079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171ce168cc0eec5045f16c757a6e195ee850a0c6fe5a35455eade5b7b21205b3`  
		Last Modified: Thu, 23 Apr 2020 16:59:11 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97521971145e342b2c6d92e6ad348d8ab8299fec5f5effe422e6a7dd66191b71`  
		Last Modified: Thu, 23 Apr 2020 16:59:11 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44fdbe8131b8e1d3d21d683cf220bd62dc9acf2e1789eaa2c0748ce98ac0b358`  
		Last Modified: Thu, 23 Apr 2020 16:59:10 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.6.4` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:45c251efcd9fdc153a57a1e9c550bf2828036095270e4d3e20cfed16ba5a59df
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40230231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f282ac0e02ae37a1787090557d669063197b2c5efd95044e012c20907aa3fd0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:54:58 GMT
ADD file:92767b5525acd9dbf8657931d32bdcc7cc504cdc33c95e84a75e478b00569bab in / 
# Thu, 23 Jan 2020 16:54:59 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:19:49 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Fri, 21 Feb 2020 00:42:00 GMT
ENV CONSUL_VERSION=1.6.4
# Fri, 21 Feb 2020 00:42:04 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 21 Feb 2020 00:42:12 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 21 Feb 2020 00:42:20 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 21 Feb 2020 00:42:23 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 21 Feb 2020 00:42:25 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 21 Feb 2020 00:42:26 GMT
VOLUME [/consul/data]
# Fri, 21 Feb 2020 00:42:27 GMT
EXPOSE 8300
# Fri, 21 Feb 2020 00:42:29 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 21 Feb 2020 00:42:29 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 21 Feb 2020 00:42:31 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 21 Feb 2020 00:42:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 00:42:34 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:eb93038481ddcf86a625b70f7551cdc583e38886f206fe7e40ad644008efa815`  
		Last Modified: Thu, 23 Jan 2020 16:55:31 GMT  
		Size: 2.7 MB (2693238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55512e1a6a5525e7fb15efa167d7b8ed30d1a2723c34a719c45c74a95ba8ebcf`  
		Last Modified: Fri, 21 Feb 2020 00:43:50 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb7968d4ace046b77e9b05c2b398c7a5e86000cee7996f0e698cfcb1598540a`  
		Last Modified: Fri, 21 Feb 2020 00:44:01 GMT  
		Size: 37.5 MB (37533680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c9f416575dcc099e0506c1b942c901424b400787ff46c1cc11a9af93890e1b`  
		Last Modified: Fri, 21 Feb 2020 00:43:50 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3114b18a4e7ae06ce6b0a199fc1d5f315c27b489ee9913b18311dc1457f2250`  
		Last Modified: Fri, 21 Feb 2020 00:43:50 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244002b6859d532f222a92e6c92a20588aeefc33c15352db6663d463afacad52`  
		Last Modified: Fri, 21 Feb 2020 00:43:50 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.6.4` - linux; 386

```console
$ docker pull consul@sha256:a56cd17592810ef83c8b2cfea552e80ea1ff47e30a143e8dfd85f58d091edac0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43564854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e51ebb91e20f2ab0eab9b14934ace03d5c0c533dd2e65fddbbded72050ab651b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:18 GMT
ADD file:68d5786259963a2b97cf808d79de83cbd0281dfea284e1a401bc851a3585e1bd in / 
# Thu, 23 Apr 2020 21:16:19 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 04:30:33 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Fri, 24 Apr 2020 04:30:47 GMT
ENV CONSUL_VERSION=1.6.4
# Fri, 24 Apr 2020 04:30:47 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 24 Apr 2020 04:30:48 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 24 Apr 2020 04:30:53 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 24 Apr 2020 04:30:54 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 24 Apr 2020 04:30:55 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 04:30:55 GMT
VOLUME [/consul/data]
# Fri, 24 Apr 2020 04:30:55 GMT
EXPOSE 8300
# Fri, 24 Apr 2020 04:30:56 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 24 Apr 2020 04:30:56 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 24 Apr 2020 04:30:56 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Apr 2020 04:30:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 04:30:56 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2f4fdbe0599cb5bbd0664b1cdad4997f428ce2495ae3eabf942129dc197d991c`  
		Last Modified: Thu, 23 Apr 2020 21:16:41 GMT  
		Size: 2.8 MB (2769736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f568d665eb8b0a76b0aa1413fda0d4420e3d26176df683dc9b5df735622a94`  
		Last Modified: Fri, 24 Apr 2020 04:32:45 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc8283ec022c872af08a5afbf7824fdb4f2250430a67afeb903c7ff57b33af9`  
		Last Modified: Fri, 24 Apr 2020 04:32:52 GMT  
		Size: 40.8 MB (40791861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a07385c2a70b08fb4573241222b0941b800763c74eb13ee946bdbcd89d0ec3c`  
		Last Modified: Fri, 24 Apr 2020 04:32:45 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3321e56ff68bad78adef6232b96a4cc1b2ea8b969e53ceb906ef71257982f195`  
		Last Modified: Fri, 24 Apr 2020 04:32:45 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b6c76dbfbce3561478fe4a0afa0a544f01b73515f8bbbbb3b817774d1bd876a`  
		Last Modified: Fri, 24 Apr 2020 04:32:45 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.7`

```console
$ docker pull consul@sha256:4d31a97cf30de8ea670dc4c26029be905ae41917e04e9666e0d2be899d4f20be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.7` - linux; amd64

```console
$ docker pull consul@sha256:2f03c533527fdf8b579647f093eb7fe88fc7f2038794cfbe20347b02eef68e1e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (44031134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213e00e87c53c5489ba357ba79b831abd46b13de4f94f6ce73991eb2c4966910`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:15:11 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Tue, 17 Mar 2020 02:21:42 GMT
ENV CONSUL_VERSION=1.7.2
# Tue, 17 Mar 2020 02:21:42 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 17 Mar 2020 02:21:43 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 17 Mar 2020 02:21:48 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 17 Mar 2020 02:21:49 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 17 Mar 2020 02:21:50 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 17 Mar 2020 02:21:50 GMT
VOLUME [/consul/data]
# Tue, 17 Mar 2020 02:21:50 GMT
EXPOSE 8300
# Tue, 17 Mar 2020 02:21:50 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 17 Mar 2020 02:21:50 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 17 Mar 2020 02:21:51 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 17 Mar 2020 02:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2020 02:21:51 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e53a83f2205caac853dba979ee0e2ec8c8b5d90afca5e4108f8467c0f71379`  
		Last Modified: Tue, 17 Mar 2020 02:22:31 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64aa8d4cc8e6904c634c53644e5dd89e3de02465084a361007d8a7edc8bbb10`  
		Last Modified: Tue, 17 Mar 2020 02:22:38 GMT  
		Size: 41.3 MB (41263699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82481eff66f7571652f4b8322f7254ec061549efd50280ff1e4222151ce378a8`  
		Last Modified: Tue, 17 Mar 2020 02:22:31 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79aba2a452b629a1689862dce05fc3664b37849089dad576172dff92e127b037`  
		Last Modified: Tue, 17 Mar 2020 02:22:31 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe81d1cfdb2572cbdf90464dba06a3a2508ec42f60b0740b17860bef517cb20a`  
		Last Modified: Tue, 17 Mar 2020 02:22:31 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7` - linux; arm variant v6

```console
$ docker pull consul@sha256:2576c59acc486392580e50ded105e64b1978b932db016d9e90938b8e6d33d4b3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41373378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79208c31c835cd5fec058474d924af104bdeeb4b9d96f534a2ff1896b12e7ff4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:44 GMT
ADD file:7dd2657543fac7f63a125194d27bd38a8e472a3076831a2331c43a471794c210 in / 
# Thu, 23 Apr 2020 15:51:45 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 16:53:13 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Apr 2020 16:53:14 GMT
ENV CONSUL_VERSION=1.7.2
# Thu, 23 Apr 2020 16:53:15 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Apr 2020 16:53:17 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Apr 2020 16:53:38 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Apr 2020 16:53:40 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Apr 2020 16:53:42 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 16:53:43 GMT
VOLUME [/consul/data]
# Thu, 23 Apr 2020 16:53:43 GMT
EXPOSE 8300
# Thu, 23 Apr 2020 16:53:44 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Apr 2020 16:53:45 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Apr 2020 16:53:46 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Apr 2020 16:53:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 16:53:47 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:27da80392aebe463671b839837d59af1261218364b4261ceb2eca0f814075270`  
		Last Modified: Thu, 23 Apr 2020 15:52:21 GMT  
		Size: 2.5 MB (2548725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9874fc1eb1d8751a0b682ebbc5d8c79d232643ec2a56f3b01f2fc7d1d0d2ebf2`  
		Last Modified: Thu, 23 Apr 2020 16:58:48 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564cdd5be6d3d2f6363923b22e5b77dcc12bf2b1bd669768afda1448739539c4`  
		Last Modified: Thu, 23 Apr 2020 16:59:02 GMT  
		Size: 38.8 MB (38821333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685d58b44180c7be022003e491ecd91499d30bf07744be7129d578aedef8315c`  
		Last Modified: Thu, 23 Apr 2020 16:58:48 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ac0ffd1df9fea7f273b6d0d2c4fe39c72b0734f71b4d228f3b8df05faf62da`  
		Last Modified: Thu, 23 Apr 2020 16:58:48 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2aef728bacc9219868ef13d7868146b3397a1a23089fc08e14751f2740a6cbf`  
		Last Modified: Thu, 23 Apr 2020 16:58:48 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:722bf1c625cc356868b999bb71942880db3de719fb1575cc643be9616da99a1c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41717466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cbd2e6f19ef2f7eca2a608471f4f3cc1106fcb167836254ea32139208b056ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:54:58 GMT
ADD file:92767b5525acd9dbf8657931d32bdcc7cc504cdc33c95e84a75e478b00569bab in / 
# Thu, 23 Jan 2020 16:54:59 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:19:49 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Tue, 17 Mar 2020 01:41:06 GMT
ENV CONSUL_VERSION=1.7.2
# Tue, 17 Mar 2020 01:41:07 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 17 Mar 2020 01:41:10 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 17 Mar 2020 01:41:21 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 17 Mar 2020 01:41:23 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 17 Mar 2020 01:41:25 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 17 Mar 2020 01:41:25 GMT
VOLUME [/consul/data]
# Tue, 17 Mar 2020 01:41:26 GMT
EXPOSE 8300
# Tue, 17 Mar 2020 01:41:27 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 17 Mar 2020 01:41:28 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 17 Mar 2020 01:41:28 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 17 Mar 2020 01:41:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2020 01:41:30 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:eb93038481ddcf86a625b70f7551cdc583e38886f206fe7e40ad644008efa815`  
		Last Modified: Thu, 23 Jan 2020 16:55:31 GMT  
		Size: 2.7 MB (2693238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16a290e0722d9ba02ecd57e64344813e3fbb0e36a0349fae7f659844dbf65be`  
		Last Modified: Tue, 17 Mar 2020 01:42:26 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553963123c347234d9b628a4752e54566f63a2433fcb9fff1e82345b1e22c8c0`  
		Last Modified: Tue, 17 Mar 2020 01:42:36 GMT  
		Size: 39.0 MB (39020908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85194eac93fdf9bccb929349405df065c17bcae470d52df5ec33a1b5d678677c`  
		Last Modified: Tue, 17 Mar 2020 01:42:26 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf62bdd07dd68e7efaa2e683c7708a54095a75ec3b01a12f2a1e76e751288cb`  
		Last Modified: Tue, 17 Mar 2020 01:42:26 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c468b02becd03fba58d2e5d6d23ca84d0aa0d7777ee7ca2fdb478d0a0189773e`  
		Last Modified: Tue, 17 Mar 2020 01:42:26 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7` - linux; 386

```console
$ docker pull consul@sha256:392bdf13ef1354c14d04d1356edd45529424a37f05fed2fcdca5978ee4f4dba8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42801277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcde118126e62a34d36134d9f724ca494890204eac937d9ea6e74a3562fec002`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:18 GMT
ADD file:68d5786259963a2b97cf808d79de83cbd0281dfea284e1a401bc851a3585e1bd in / 
# Thu, 23 Apr 2020 21:16:19 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 04:30:33 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Fri, 24 Apr 2020 04:30:33 GMT
ENV CONSUL_VERSION=1.7.2
# Fri, 24 Apr 2020 04:30:33 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 24 Apr 2020 04:30:34 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 24 Apr 2020 04:30:40 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 24 Apr 2020 04:30:41 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 24 Apr 2020 04:30:41 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 04:30:42 GMT
VOLUME [/consul/data]
# Fri, 24 Apr 2020 04:30:42 GMT
EXPOSE 8300
# Fri, 24 Apr 2020 04:30:42 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 24 Apr 2020 04:30:42 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 24 Apr 2020 04:30:42 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Apr 2020 04:30:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 04:30:43 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2f4fdbe0599cb5bbd0664b1cdad4997f428ce2495ae3eabf942129dc197d991c`  
		Last Modified: Thu, 23 Apr 2020 21:16:41 GMT  
		Size: 2.8 MB (2769736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607b7bb5061a95937d87f9ad985e42dacc435a6370d94152fc391ff32aa301be`  
		Last Modified: Fri, 24 Apr 2020 04:32:33 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa42f73ce141d946a080e2f0aefb7db4bbba77a41a6c4a264adc4e8d9520a2a2`  
		Last Modified: Fri, 24 Apr 2020 04:32:39 GMT  
		Size: 40.0 MB (40028283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d96e36abb3279217e16cf3ffcd6760567a8622deaf39a270c24d607e169d84`  
		Last Modified: Fri, 24 Apr 2020 04:32:32 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779aad3ecbda91cac2157b2d97bf8adc4f2b5bfd94304258f6e501bae7db49c3`  
		Last Modified: Fri, 24 Apr 2020 04:32:32 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38a902a831ce487125d829e4fe709443d1c1558ea81a5990448511187ea97d8`  
		Last Modified: Fri, 24 Apr 2020 04:32:33 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.7.2`

```console
$ docker pull consul@sha256:4d31a97cf30de8ea670dc4c26029be905ae41917e04e9666e0d2be899d4f20be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.7.2` - linux; amd64

```console
$ docker pull consul@sha256:2f03c533527fdf8b579647f093eb7fe88fc7f2038794cfbe20347b02eef68e1e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (44031134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213e00e87c53c5489ba357ba79b831abd46b13de4f94f6ce73991eb2c4966910`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:15:11 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Tue, 17 Mar 2020 02:21:42 GMT
ENV CONSUL_VERSION=1.7.2
# Tue, 17 Mar 2020 02:21:42 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 17 Mar 2020 02:21:43 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 17 Mar 2020 02:21:48 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 17 Mar 2020 02:21:49 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 17 Mar 2020 02:21:50 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 17 Mar 2020 02:21:50 GMT
VOLUME [/consul/data]
# Tue, 17 Mar 2020 02:21:50 GMT
EXPOSE 8300
# Tue, 17 Mar 2020 02:21:50 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 17 Mar 2020 02:21:50 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 17 Mar 2020 02:21:51 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 17 Mar 2020 02:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2020 02:21:51 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e53a83f2205caac853dba979ee0e2ec8c8b5d90afca5e4108f8467c0f71379`  
		Last Modified: Tue, 17 Mar 2020 02:22:31 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64aa8d4cc8e6904c634c53644e5dd89e3de02465084a361007d8a7edc8bbb10`  
		Last Modified: Tue, 17 Mar 2020 02:22:38 GMT  
		Size: 41.3 MB (41263699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82481eff66f7571652f4b8322f7254ec061549efd50280ff1e4222151ce378a8`  
		Last Modified: Tue, 17 Mar 2020 02:22:31 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79aba2a452b629a1689862dce05fc3664b37849089dad576172dff92e127b037`  
		Last Modified: Tue, 17 Mar 2020 02:22:31 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe81d1cfdb2572cbdf90464dba06a3a2508ec42f60b0740b17860bef517cb20a`  
		Last Modified: Tue, 17 Mar 2020 02:22:31 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7.2` - linux; arm variant v6

```console
$ docker pull consul@sha256:2576c59acc486392580e50ded105e64b1978b932db016d9e90938b8e6d33d4b3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41373378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79208c31c835cd5fec058474d924af104bdeeb4b9d96f534a2ff1896b12e7ff4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:44 GMT
ADD file:7dd2657543fac7f63a125194d27bd38a8e472a3076831a2331c43a471794c210 in / 
# Thu, 23 Apr 2020 15:51:45 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 16:53:13 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Apr 2020 16:53:14 GMT
ENV CONSUL_VERSION=1.7.2
# Thu, 23 Apr 2020 16:53:15 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Apr 2020 16:53:17 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Apr 2020 16:53:38 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Apr 2020 16:53:40 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Apr 2020 16:53:42 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 16:53:43 GMT
VOLUME [/consul/data]
# Thu, 23 Apr 2020 16:53:43 GMT
EXPOSE 8300
# Thu, 23 Apr 2020 16:53:44 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Apr 2020 16:53:45 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Apr 2020 16:53:46 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Apr 2020 16:53:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 16:53:47 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:27da80392aebe463671b839837d59af1261218364b4261ceb2eca0f814075270`  
		Last Modified: Thu, 23 Apr 2020 15:52:21 GMT  
		Size: 2.5 MB (2548725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9874fc1eb1d8751a0b682ebbc5d8c79d232643ec2a56f3b01f2fc7d1d0d2ebf2`  
		Last Modified: Thu, 23 Apr 2020 16:58:48 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564cdd5be6d3d2f6363923b22e5b77dcc12bf2b1bd669768afda1448739539c4`  
		Last Modified: Thu, 23 Apr 2020 16:59:02 GMT  
		Size: 38.8 MB (38821333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685d58b44180c7be022003e491ecd91499d30bf07744be7129d578aedef8315c`  
		Last Modified: Thu, 23 Apr 2020 16:58:48 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ac0ffd1df9fea7f273b6d0d2c4fe39c72b0734f71b4d228f3b8df05faf62da`  
		Last Modified: Thu, 23 Apr 2020 16:58:48 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2aef728bacc9219868ef13d7868146b3397a1a23089fc08e14751f2740a6cbf`  
		Last Modified: Thu, 23 Apr 2020 16:58:48 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7.2` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:722bf1c625cc356868b999bb71942880db3de719fb1575cc643be9616da99a1c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41717466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cbd2e6f19ef2f7eca2a608471f4f3cc1106fcb167836254ea32139208b056ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:54:58 GMT
ADD file:92767b5525acd9dbf8657931d32bdcc7cc504cdc33c95e84a75e478b00569bab in / 
# Thu, 23 Jan 2020 16:54:59 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:19:49 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Tue, 17 Mar 2020 01:41:06 GMT
ENV CONSUL_VERSION=1.7.2
# Tue, 17 Mar 2020 01:41:07 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 17 Mar 2020 01:41:10 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 17 Mar 2020 01:41:21 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 17 Mar 2020 01:41:23 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 17 Mar 2020 01:41:25 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 17 Mar 2020 01:41:25 GMT
VOLUME [/consul/data]
# Tue, 17 Mar 2020 01:41:26 GMT
EXPOSE 8300
# Tue, 17 Mar 2020 01:41:27 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 17 Mar 2020 01:41:28 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 17 Mar 2020 01:41:28 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 17 Mar 2020 01:41:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2020 01:41:30 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:eb93038481ddcf86a625b70f7551cdc583e38886f206fe7e40ad644008efa815`  
		Last Modified: Thu, 23 Jan 2020 16:55:31 GMT  
		Size: 2.7 MB (2693238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16a290e0722d9ba02ecd57e64344813e3fbb0e36a0349fae7f659844dbf65be`  
		Last Modified: Tue, 17 Mar 2020 01:42:26 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553963123c347234d9b628a4752e54566f63a2433fcb9fff1e82345b1e22c8c0`  
		Last Modified: Tue, 17 Mar 2020 01:42:36 GMT  
		Size: 39.0 MB (39020908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85194eac93fdf9bccb929349405df065c17bcae470d52df5ec33a1b5d678677c`  
		Last Modified: Tue, 17 Mar 2020 01:42:26 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf62bdd07dd68e7efaa2e683c7708a54095a75ec3b01a12f2a1e76e751288cb`  
		Last Modified: Tue, 17 Mar 2020 01:42:26 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c468b02becd03fba58d2e5d6d23ca84d0aa0d7777ee7ca2fdb478d0a0189773e`  
		Last Modified: Tue, 17 Mar 2020 01:42:26 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7.2` - linux; 386

```console
$ docker pull consul@sha256:392bdf13ef1354c14d04d1356edd45529424a37f05fed2fcdca5978ee4f4dba8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42801277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcde118126e62a34d36134d9f724ca494890204eac937d9ea6e74a3562fec002`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:18 GMT
ADD file:68d5786259963a2b97cf808d79de83cbd0281dfea284e1a401bc851a3585e1bd in / 
# Thu, 23 Apr 2020 21:16:19 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 04:30:33 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Fri, 24 Apr 2020 04:30:33 GMT
ENV CONSUL_VERSION=1.7.2
# Fri, 24 Apr 2020 04:30:33 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 24 Apr 2020 04:30:34 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 24 Apr 2020 04:30:40 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 24 Apr 2020 04:30:41 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 24 Apr 2020 04:30:41 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 04:30:42 GMT
VOLUME [/consul/data]
# Fri, 24 Apr 2020 04:30:42 GMT
EXPOSE 8300
# Fri, 24 Apr 2020 04:30:42 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 24 Apr 2020 04:30:42 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 24 Apr 2020 04:30:42 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Apr 2020 04:30:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 04:30:43 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2f4fdbe0599cb5bbd0664b1cdad4997f428ce2495ae3eabf942129dc197d991c`  
		Last Modified: Thu, 23 Apr 2020 21:16:41 GMT  
		Size: 2.8 MB (2769736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607b7bb5061a95937d87f9ad985e42dacc435a6370d94152fc391ff32aa301be`  
		Last Modified: Fri, 24 Apr 2020 04:32:33 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa42f73ce141d946a080e2f0aefb7db4bbba77a41a6c4a264adc4e8d9520a2a2`  
		Last Modified: Fri, 24 Apr 2020 04:32:39 GMT  
		Size: 40.0 MB (40028283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d96e36abb3279217e16cf3ffcd6760567a8622deaf39a270c24d607e169d84`  
		Last Modified: Fri, 24 Apr 2020 04:32:32 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779aad3ecbda91cac2157b2d97bf8adc4f2b5bfd94304258f6e501bae7db49c3`  
		Last Modified: Fri, 24 Apr 2020 04:32:32 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38a902a831ce487125d829e4fe709443d1c1558ea81a5990448511187ea97d8`  
		Last Modified: Fri, 24 Apr 2020 04:32:33 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:latest`

```console
$ docker pull consul@sha256:4d31a97cf30de8ea670dc4c26029be905ae41917e04e9666e0d2be899d4f20be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:latest` - linux; amd64

```console
$ docker pull consul@sha256:2f03c533527fdf8b579647f093eb7fe88fc7f2038794cfbe20347b02eef68e1e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (44031134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213e00e87c53c5489ba357ba79b831abd46b13de4f94f6ce73991eb2c4966910`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:15:11 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Tue, 17 Mar 2020 02:21:42 GMT
ENV CONSUL_VERSION=1.7.2
# Tue, 17 Mar 2020 02:21:42 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 17 Mar 2020 02:21:43 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 17 Mar 2020 02:21:48 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 17 Mar 2020 02:21:49 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 17 Mar 2020 02:21:50 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 17 Mar 2020 02:21:50 GMT
VOLUME [/consul/data]
# Tue, 17 Mar 2020 02:21:50 GMT
EXPOSE 8300
# Tue, 17 Mar 2020 02:21:50 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 17 Mar 2020 02:21:50 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 17 Mar 2020 02:21:51 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 17 Mar 2020 02:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2020 02:21:51 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e53a83f2205caac853dba979ee0e2ec8c8b5d90afca5e4108f8467c0f71379`  
		Last Modified: Tue, 17 Mar 2020 02:22:31 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64aa8d4cc8e6904c634c53644e5dd89e3de02465084a361007d8a7edc8bbb10`  
		Last Modified: Tue, 17 Mar 2020 02:22:38 GMT  
		Size: 41.3 MB (41263699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82481eff66f7571652f4b8322f7254ec061549efd50280ff1e4222151ce378a8`  
		Last Modified: Tue, 17 Mar 2020 02:22:31 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79aba2a452b629a1689862dce05fc3664b37849089dad576172dff92e127b037`  
		Last Modified: Tue, 17 Mar 2020 02:22:31 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe81d1cfdb2572cbdf90464dba06a3a2508ec42f60b0740b17860bef517cb20a`  
		Last Modified: Tue, 17 Mar 2020 02:22:31 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm variant v6

```console
$ docker pull consul@sha256:2576c59acc486392580e50ded105e64b1978b932db016d9e90938b8e6d33d4b3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41373378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79208c31c835cd5fec058474d924af104bdeeb4b9d96f534a2ff1896b12e7ff4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:44 GMT
ADD file:7dd2657543fac7f63a125194d27bd38a8e472a3076831a2331c43a471794c210 in / 
# Thu, 23 Apr 2020 15:51:45 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 16:53:13 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Apr 2020 16:53:14 GMT
ENV CONSUL_VERSION=1.7.2
# Thu, 23 Apr 2020 16:53:15 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Apr 2020 16:53:17 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Apr 2020 16:53:38 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Apr 2020 16:53:40 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Apr 2020 16:53:42 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 16:53:43 GMT
VOLUME [/consul/data]
# Thu, 23 Apr 2020 16:53:43 GMT
EXPOSE 8300
# Thu, 23 Apr 2020 16:53:44 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Apr 2020 16:53:45 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Apr 2020 16:53:46 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Apr 2020 16:53:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 16:53:47 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:27da80392aebe463671b839837d59af1261218364b4261ceb2eca0f814075270`  
		Last Modified: Thu, 23 Apr 2020 15:52:21 GMT  
		Size: 2.5 MB (2548725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9874fc1eb1d8751a0b682ebbc5d8c79d232643ec2a56f3b01f2fc7d1d0d2ebf2`  
		Last Modified: Thu, 23 Apr 2020 16:58:48 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564cdd5be6d3d2f6363923b22e5b77dcc12bf2b1bd669768afda1448739539c4`  
		Last Modified: Thu, 23 Apr 2020 16:59:02 GMT  
		Size: 38.8 MB (38821333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685d58b44180c7be022003e491ecd91499d30bf07744be7129d578aedef8315c`  
		Last Modified: Thu, 23 Apr 2020 16:58:48 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ac0ffd1df9fea7f273b6d0d2c4fe39c72b0734f71b4d228f3b8df05faf62da`  
		Last Modified: Thu, 23 Apr 2020 16:58:48 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2aef728bacc9219868ef13d7868146b3397a1a23089fc08e14751f2740a6cbf`  
		Last Modified: Thu, 23 Apr 2020 16:58:48 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:722bf1c625cc356868b999bb71942880db3de719fb1575cc643be9616da99a1c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41717466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cbd2e6f19ef2f7eca2a608471f4f3cc1106fcb167836254ea32139208b056ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:54:58 GMT
ADD file:92767b5525acd9dbf8657931d32bdcc7cc504cdc33c95e84a75e478b00569bab in / 
# Thu, 23 Jan 2020 16:54:59 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:19:49 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Tue, 17 Mar 2020 01:41:06 GMT
ENV CONSUL_VERSION=1.7.2
# Tue, 17 Mar 2020 01:41:07 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 17 Mar 2020 01:41:10 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 17 Mar 2020 01:41:21 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 17 Mar 2020 01:41:23 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 17 Mar 2020 01:41:25 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 17 Mar 2020 01:41:25 GMT
VOLUME [/consul/data]
# Tue, 17 Mar 2020 01:41:26 GMT
EXPOSE 8300
# Tue, 17 Mar 2020 01:41:27 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 17 Mar 2020 01:41:28 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 17 Mar 2020 01:41:28 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 17 Mar 2020 01:41:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2020 01:41:30 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:eb93038481ddcf86a625b70f7551cdc583e38886f206fe7e40ad644008efa815`  
		Last Modified: Thu, 23 Jan 2020 16:55:31 GMT  
		Size: 2.7 MB (2693238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16a290e0722d9ba02ecd57e64344813e3fbb0e36a0349fae7f659844dbf65be`  
		Last Modified: Tue, 17 Mar 2020 01:42:26 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553963123c347234d9b628a4752e54566f63a2433fcb9fff1e82345b1e22c8c0`  
		Last Modified: Tue, 17 Mar 2020 01:42:36 GMT  
		Size: 39.0 MB (39020908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85194eac93fdf9bccb929349405df065c17bcae470d52df5ec33a1b5d678677c`  
		Last Modified: Tue, 17 Mar 2020 01:42:26 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf62bdd07dd68e7efaa2e683c7708a54095a75ec3b01a12f2a1e76e751288cb`  
		Last Modified: Tue, 17 Mar 2020 01:42:26 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c468b02becd03fba58d2e5d6d23ca84d0aa0d7777ee7ca2fdb478d0a0189773e`  
		Last Modified: Tue, 17 Mar 2020 01:42:26 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; 386

```console
$ docker pull consul@sha256:392bdf13ef1354c14d04d1356edd45529424a37f05fed2fcdca5978ee4f4dba8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42801277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcde118126e62a34d36134d9f724ca494890204eac937d9ea6e74a3562fec002`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:18 GMT
ADD file:68d5786259963a2b97cf808d79de83cbd0281dfea284e1a401bc851a3585e1bd in / 
# Thu, 23 Apr 2020 21:16:19 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 04:30:33 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Fri, 24 Apr 2020 04:30:33 GMT
ENV CONSUL_VERSION=1.7.2
# Fri, 24 Apr 2020 04:30:33 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 24 Apr 2020 04:30:34 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 24 Apr 2020 04:30:40 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 24 Apr 2020 04:30:41 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 24 Apr 2020 04:30:41 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 04:30:42 GMT
VOLUME [/consul/data]
# Fri, 24 Apr 2020 04:30:42 GMT
EXPOSE 8300
# Fri, 24 Apr 2020 04:30:42 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 24 Apr 2020 04:30:42 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 24 Apr 2020 04:30:42 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Apr 2020 04:30:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 04:30:43 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2f4fdbe0599cb5bbd0664b1cdad4997f428ce2495ae3eabf942129dc197d991c`  
		Last Modified: Thu, 23 Apr 2020 21:16:41 GMT  
		Size: 2.8 MB (2769736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607b7bb5061a95937d87f9ad985e42dacc435a6370d94152fc391ff32aa301be`  
		Last Modified: Fri, 24 Apr 2020 04:32:33 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa42f73ce141d946a080e2f0aefb7db4bbba77a41a6c4a264adc4e8d9520a2a2`  
		Last Modified: Fri, 24 Apr 2020 04:32:39 GMT  
		Size: 40.0 MB (40028283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d96e36abb3279217e16cf3ffcd6760567a8622deaf39a270c24d607e169d84`  
		Last Modified: Fri, 24 Apr 2020 04:32:32 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779aad3ecbda91cac2157b2d97bf8adc4f2b5bfd94304258f6e501bae7db49c3`  
		Last Modified: Fri, 24 Apr 2020 04:32:32 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38a902a831ce487125d829e4fe709443d1c1558ea81a5990448511187ea97d8`  
		Last Modified: Fri, 24 Apr 2020 04:32:33 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
