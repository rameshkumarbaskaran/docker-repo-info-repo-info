<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `consul`

-	[`consul:1.13`](#consul113)
-	[`consul:1.13.8`](#consul1138)
-	[`consul:1.14`](#consul114)
-	[`consul:1.14.7`](#consul1147)
-	[`consul:1.15`](#consul115)
-	[`consul:1.15.3`](#consul1153)
-	[`consul:latest`](#consullatest)

## `consul:1.13`

```console
$ docker pull consul@sha256:87a6211d80a13038e2497e7cd10bc83beb24b26deda6b4a0dc3a952cd841fb69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.13` - linux; amd64

```console
$ docker pull consul@sha256:b6ba521928cdb554f8fd160a537cad0f43073d48c0d8daaeeee553ef265feb3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53249938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3c7ef92a2c93c74afd836dc58c7b3d5a45240cc23ce8d5304e64d5c8fd992a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:33 GMT
ADD file:08ad6c1c886a26e30ae4ab103ff377ee6cfbc1be2437fa227ec28a335c63d78a in / 
# Wed, 29 Mar 2023 18:19:33 GMT
CMD ["/bin/sh"]
# Wed, 17 May 2023 23:21:54 GMT
ARG CONSUL_VERSION=1.13.8
# Wed, 17 May 2023 23:21:55 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.8 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 17 May 2023 23:21:55 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 17 May 2023 23:21:55 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 17 May 2023 23:22:00 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 17 May 2023 23:22:01 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 17 May 2023 23:22:02 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 17 May 2023 23:22:02 GMT
VOLUME [/consul/data]
# Wed, 17 May 2023 23:22:02 GMT
EXPOSE 8300
# Wed, 17 May 2023 23:22:02 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 17 May 2023 23:22:02 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 17 May 2023 23:22:02 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 17 May 2023 23:22:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 May 2023 23:22:02 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0ce1dd7918a48990ab749aab2e805c26f691a3a8103495530e7ea5a1d168af4a`  
		Last Modified: Wed, 29 Mar 2023 18:20:17 GMT  
		Size: 2.8 MB (2826596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8286ff1bc4a634dcd9b1566cbfa82c58f18aac2aa1356f6041cad9330001e979`  
		Last Modified: Wed, 17 May 2023 23:22:28 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a38b9bc9b1f6484e62df572e77c880973a6a6b576167953550f5b7caaac0b88`  
		Last Modified: Wed, 17 May 2023 23:22:34 GMT  
		Size: 50.4 MB (50419917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1287366eeaa3b9fe5bae2eae5869cac08b74e18d4a4affc04646329f7bcbe04e`  
		Last Modified: Wed, 17 May 2023 23:22:28 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e762d9c652f2055032bad6d4d7961fb7fdc268e576f21888ef1ac4d478f5871e`  
		Last Modified: Wed, 17 May 2023 23:22:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81f71f475104174cd0a87cbc84764e046c3390b091e7fa751e14269b8bd69b0`  
		Last Modified: Wed, 17 May 2023 23:22:28 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13` - linux; arm variant v6

```console
$ docker pull consul@sha256:f210e3c58d4d2bf0f0d2210e0f05658b86528ef4a121b932ee40c3a409b33b87
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50745679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de83b749234589b8fa3a587f7e4968961d21e7f357df5219c9b80fe126211f6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:13 GMT
ADD file:3fb55ad8134002858be264c3c2477d784e4a60f2f6501afa7cf3b10bfede51aa in / 
# Wed, 29 Mar 2023 18:01:13 GMT
CMD ["/bin/sh"]
# Wed, 17 May 2023 23:49:31 GMT
ARG CONSUL_VERSION=1.13.8
# Wed, 17 May 2023 23:49:31 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.8 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 17 May 2023 23:49:31 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 17 May 2023 23:49:31 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 17 May 2023 23:49:38 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 17 May 2023 23:49:39 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 17 May 2023 23:49:39 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 17 May 2023 23:49:39 GMT
VOLUME [/consul/data]
# Wed, 17 May 2023 23:49:40 GMT
EXPOSE 8300
# Wed, 17 May 2023 23:49:40 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 17 May 2023 23:49:40 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 17 May 2023 23:49:40 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 17 May 2023 23:49:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 May 2023 23:49:40 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:872c99a87729fa48dce303fb615edbb1a5da837f627a0b3d28495a0400ca8335`  
		Last Modified: Wed, 29 Mar 2023 18:02:12 GMT  
		Size: 2.6 MB (2634030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ccf0e2dc5c29a8056b8bc33ecf07999545fa14f6a09bdce2de0bb51ad42766`  
		Last Modified: Wed, 17 May 2023 23:50:06 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062ffef33578245610a23c22ebedd3a33e05fca19f3d3a6d715ad26339f0ca39`  
		Last Modified: Wed, 17 May 2023 23:50:13 GMT  
		Size: 48.1 MB (48108219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebc3dff9a69caf1e5fba8e851aa55e90c38c109b6f21ee34c5e1df4f4230787`  
		Last Modified: Wed, 17 May 2023 23:50:06 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f89157c3d183175d83f364b1f19388cf498af7562af1cb55c1de2bd23bf8cf`  
		Last Modified: Wed, 17 May 2023 23:50:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdeae0fd79149bb34869eeeea196b788f7e189f9769f3f46dbb59ce08d160723`  
		Last Modified: Wed, 17 May 2023 23:50:06 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:7ddd8b37b8d6af91196bb8efa75a728ff7974e427fdd3efb3acdf6b98e550f87
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50285993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89dd6606b1a40c524c9b088feed70021fde908fe35e74eec64612c502d74ad10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:22 GMT
ADD file:4acfda16c71abce07068ed23839e9de60c1d1145ab8002b3a92c15b1e80d4356 in / 
# Wed, 29 Mar 2023 17:39:23 GMT
CMD ["/bin/sh"]
# Wed, 17 May 2023 23:40:43 GMT
ARG CONSUL_VERSION=1.13.8
# Wed, 17 May 2023 23:40:43 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.8 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 17 May 2023 23:40:43 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 17 May 2023 23:40:43 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 17 May 2023 23:40:48 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 17 May 2023 23:40:49 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 17 May 2023 23:40:49 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 17 May 2023 23:40:49 GMT
VOLUME [/consul/data]
# Wed, 17 May 2023 23:40:49 GMT
EXPOSE 8300
# Wed, 17 May 2023 23:40:50 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 17 May 2023 23:40:50 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 17 May 2023 23:40:50 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 17 May 2023 23:40:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 May 2023 23:40:50 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:60a00c11adf5202a365ec8215b889c3390d67fa295ab79940e1c5dc4cbed9db1`  
		Last Modified: Wed, 29 Mar 2023 17:40:04 GMT  
		Size: 2.7 MB (2722002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd52b8df794831a0e529e3dfa4b04e14f4e00e85736887eed71534bca4a19c9d`  
		Last Modified: Wed, 17 May 2023 23:41:14 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73f3c56d5861528c75515294bf455bf682fe7d9920f473687a55af1690a5470`  
		Last Modified: Wed, 17 May 2023 23:41:19 GMT  
		Size: 47.6 MB (47560561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fafc441266cd150cb29b0806b1f3fe00d22cfee571b43d1dca4ea5b8e78eeb4`  
		Last Modified: Wed, 17 May 2023 23:41:14 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad42ead8b0ab1e612061091eb0a981ec2880182f228f10c7a28e241d90f2b9c`  
		Last Modified: Wed, 17 May 2023 23:41:14 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952d2f7cc5486aaa27106aa48d5bbb6efe6a4eef4379b9eabd7bcf3fe57beeaa`  
		Last Modified: Wed, 17 May 2023 23:41:14 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13` - linux; 386

```console
$ docker pull consul@sha256:027d4a05b2565d784d8eda9972f7f681ebae7ef35ebd359b5d57cd79830a61cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52081128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7887aaeb4ef31b62bcb0a70829bbf1a23c2bacd15051f86bc2d446a94e5dddd7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:36 GMT
ADD file:fca96dde137b6b045359aec9d24257996738ac6cb7cce9518460a66802a27bd7 in / 
# Wed, 29 Mar 2023 17:38:36 GMT
CMD ["/bin/sh"]
# Wed, 17 May 2023 23:38:36 GMT
ARG CONSUL_VERSION=1.13.8
# Wed, 17 May 2023 23:38:36 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.8 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 17 May 2023 23:38:36 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 17 May 2023 23:38:37 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 17 May 2023 23:38:43 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 17 May 2023 23:38:44 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 17 May 2023 23:38:45 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 17 May 2023 23:38:45 GMT
VOLUME [/consul/data]
# Wed, 17 May 2023 23:38:45 GMT
EXPOSE 8300
# Wed, 17 May 2023 23:38:45 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 17 May 2023 23:38:45 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 17 May 2023 23:38:45 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 17 May 2023 23:38:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 May 2023 23:38:46 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:333f5f619d7efe58316b2d71276f19d0a59bcb471f4dadaa85762b2c9e02775c`  
		Last Modified: Wed, 29 Mar 2023 17:39:19 GMT  
		Size: 2.8 MB (2832576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e3dfc612c84c3f094831c30c57376db17e60f0ed5725e92cd67924cdaa1c8c`  
		Last Modified: Wed, 17 May 2023 23:39:54 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f19267a32a84564526fc959b5c552a57a9000e2c43786cbbcc23618cca73389`  
		Last Modified: Wed, 17 May 2023 23:40:02 GMT  
		Size: 49.2 MB (49245120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1843eba94584a5d0f99333b17c897298dc41300bac89c5e11a4e30eea0f8f0be`  
		Last Modified: Wed, 17 May 2023 23:39:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f485cf85cd150c9df1742ec82e2002e9ad6acacab50c40f31f7b46adda4d8c21`  
		Last Modified: Wed, 17 May 2023 23:39:54 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50290dfffbcb30a78bf125fdaec0f1750cefa90df90e93267a32fef375e85344`  
		Last Modified: Wed, 17 May 2023 23:39:54 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.13.8`

```console
$ docker pull consul@sha256:87a6211d80a13038e2497e7cd10bc83beb24b26deda6b4a0dc3a952cd841fb69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.13.8` - linux; amd64

```console
$ docker pull consul@sha256:b6ba521928cdb554f8fd160a537cad0f43073d48c0d8daaeeee553ef265feb3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53249938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3c7ef92a2c93c74afd836dc58c7b3d5a45240cc23ce8d5304e64d5c8fd992a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:33 GMT
ADD file:08ad6c1c886a26e30ae4ab103ff377ee6cfbc1be2437fa227ec28a335c63d78a in / 
# Wed, 29 Mar 2023 18:19:33 GMT
CMD ["/bin/sh"]
# Wed, 17 May 2023 23:21:54 GMT
ARG CONSUL_VERSION=1.13.8
# Wed, 17 May 2023 23:21:55 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.8 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 17 May 2023 23:21:55 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 17 May 2023 23:21:55 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 17 May 2023 23:22:00 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 17 May 2023 23:22:01 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 17 May 2023 23:22:02 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 17 May 2023 23:22:02 GMT
VOLUME [/consul/data]
# Wed, 17 May 2023 23:22:02 GMT
EXPOSE 8300
# Wed, 17 May 2023 23:22:02 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 17 May 2023 23:22:02 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 17 May 2023 23:22:02 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 17 May 2023 23:22:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 May 2023 23:22:02 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0ce1dd7918a48990ab749aab2e805c26f691a3a8103495530e7ea5a1d168af4a`  
		Last Modified: Wed, 29 Mar 2023 18:20:17 GMT  
		Size: 2.8 MB (2826596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8286ff1bc4a634dcd9b1566cbfa82c58f18aac2aa1356f6041cad9330001e979`  
		Last Modified: Wed, 17 May 2023 23:22:28 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a38b9bc9b1f6484e62df572e77c880973a6a6b576167953550f5b7caaac0b88`  
		Last Modified: Wed, 17 May 2023 23:22:34 GMT  
		Size: 50.4 MB (50419917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1287366eeaa3b9fe5bae2eae5869cac08b74e18d4a4affc04646329f7bcbe04e`  
		Last Modified: Wed, 17 May 2023 23:22:28 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e762d9c652f2055032bad6d4d7961fb7fdc268e576f21888ef1ac4d478f5871e`  
		Last Modified: Wed, 17 May 2023 23:22:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81f71f475104174cd0a87cbc84764e046c3390b091e7fa751e14269b8bd69b0`  
		Last Modified: Wed, 17 May 2023 23:22:28 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13.8` - linux; arm variant v6

```console
$ docker pull consul@sha256:f210e3c58d4d2bf0f0d2210e0f05658b86528ef4a121b932ee40c3a409b33b87
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50745679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de83b749234589b8fa3a587f7e4968961d21e7f357df5219c9b80fe126211f6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:13 GMT
ADD file:3fb55ad8134002858be264c3c2477d784e4a60f2f6501afa7cf3b10bfede51aa in / 
# Wed, 29 Mar 2023 18:01:13 GMT
CMD ["/bin/sh"]
# Wed, 17 May 2023 23:49:31 GMT
ARG CONSUL_VERSION=1.13.8
# Wed, 17 May 2023 23:49:31 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.8 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 17 May 2023 23:49:31 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 17 May 2023 23:49:31 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 17 May 2023 23:49:38 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 17 May 2023 23:49:39 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 17 May 2023 23:49:39 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 17 May 2023 23:49:39 GMT
VOLUME [/consul/data]
# Wed, 17 May 2023 23:49:40 GMT
EXPOSE 8300
# Wed, 17 May 2023 23:49:40 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 17 May 2023 23:49:40 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 17 May 2023 23:49:40 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 17 May 2023 23:49:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 May 2023 23:49:40 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:872c99a87729fa48dce303fb615edbb1a5da837f627a0b3d28495a0400ca8335`  
		Last Modified: Wed, 29 Mar 2023 18:02:12 GMT  
		Size: 2.6 MB (2634030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ccf0e2dc5c29a8056b8bc33ecf07999545fa14f6a09bdce2de0bb51ad42766`  
		Last Modified: Wed, 17 May 2023 23:50:06 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062ffef33578245610a23c22ebedd3a33e05fca19f3d3a6d715ad26339f0ca39`  
		Last Modified: Wed, 17 May 2023 23:50:13 GMT  
		Size: 48.1 MB (48108219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebc3dff9a69caf1e5fba8e851aa55e90c38c109b6f21ee34c5e1df4f4230787`  
		Last Modified: Wed, 17 May 2023 23:50:06 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f89157c3d183175d83f364b1f19388cf498af7562af1cb55c1de2bd23bf8cf`  
		Last Modified: Wed, 17 May 2023 23:50:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdeae0fd79149bb34869eeeea196b788f7e189f9769f3f46dbb59ce08d160723`  
		Last Modified: Wed, 17 May 2023 23:50:06 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13.8` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:7ddd8b37b8d6af91196bb8efa75a728ff7974e427fdd3efb3acdf6b98e550f87
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50285993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89dd6606b1a40c524c9b088feed70021fde908fe35e74eec64612c502d74ad10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:22 GMT
ADD file:4acfda16c71abce07068ed23839e9de60c1d1145ab8002b3a92c15b1e80d4356 in / 
# Wed, 29 Mar 2023 17:39:23 GMT
CMD ["/bin/sh"]
# Wed, 17 May 2023 23:40:43 GMT
ARG CONSUL_VERSION=1.13.8
# Wed, 17 May 2023 23:40:43 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.8 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 17 May 2023 23:40:43 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 17 May 2023 23:40:43 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 17 May 2023 23:40:48 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 17 May 2023 23:40:49 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 17 May 2023 23:40:49 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 17 May 2023 23:40:49 GMT
VOLUME [/consul/data]
# Wed, 17 May 2023 23:40:49 GMT
EXPOSE 8300
# Wed, 17 May 2023 23:40:50 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 17 May 2023 23:40:50 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 17 May 2023 23:40:50 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 17 May 2023 23:40:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 May 2023 23:40:50 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:60a00c11adf5202a365ec8215b889c3390d67fa295ab79940e1c5dc4cbed9db1`  
		Last Modified: Wed, 29 Mar 2023 17:40:04 GMT  
		Size: 2.7 MB (2722002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd52b8df794831a0e529e3dfa4b04e14f4e00e85736887eed71534bca4a19c9d`  
		Last Modified: Wed, 17 May 2023 23:41:14 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73f3c56d5861528c75515294bf455bf682fe7d9920f473687a55af1690a5470`  
		Last Modified: Wed, 17 May 2023 23:41:19 GMT  
		Size: 47.6 MB (47560561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fafc441266cd150cb29b0806b1f3fe00d22cfee571b43d1dca4ea5b8e78eeb4`  
		Last Modified: Wed, 17 May 2023 23:41:14 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad42ead8b0ab1e612061091eb0a981ec2880182f228f10c7a28e241d90f2b9c`  
		Last Modified: Wed, 17 May 2023 23:41:14 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952d2f7cc5486aaa27106aa48d5bbb6efe6a4eef4379b9eabd7bcf3fe57beeaa`  
		Last Modified: Wed, 17 May 2023 23:41:14 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13.8` - linux; 386

```console
$ docker pull consul@sha256:027d4a05b2565d784d8eda9972f7f681ebae7ef35ebd359b5d57cd79830a61cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52081128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7887aaeb4ef31b62bcb0a70829bbf1a23c2bacd15051f86bc2d446a94e5dddd7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:36 GMT
ADD file:fca96dde137b6b045359aec9d24257996738ac6cb7cce9518460a66802a27bd7 in / 
# Wed, 29 Mar 2023 17:38:36 GMT
CMD ["/bin/sh"]
# Wed, 17 May 2023 23:38:36 GMT
ARG CONSUL_VERSION=1.13.8
# Wed, 17 May 2023 23:38:36 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.8 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 17 May 2023 23:38:36 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 17 May 2023 23:38:37 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 17 May 2023 23:38:43 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 17 May 2023 23:38:44 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 17 May 2023 23:38:45 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 17 May 2023 23:38:45 GMT
VOLUME [/consul/data]
# Wed, 17 May 2023 23:38:45 GMT
EXPOSE 8300
# Wed, 17 May 2023 23:38:45 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 17 May 2023 23:38:45 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 17 May 2023 23:38:45 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 17 May 2023 23:38:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 May 2023 23:38:46 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:333f5f619d7efe58316b2d71276f19d0a59bcb471f4dadaa85762b2c9e02775c`  
		Last Modified: Wed, 29 Mar 2023 17:39:19 GMT  
		Size: 2.8 MB (2832576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e3dfc612c84c3f094831c30c57376db17e60f0ed5725e92cd67924cdaa1c8c`  
		Last Modified: Wed, 17 May 2023 23:39:54 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f19267a32a84564526fc959b5c552a57a9000e2c43786cbbcc23618cca73389`  
		Last Modified: Wed, 17 May 2023 23:40:02 GMT  
		Size: 49.2 MB (49245120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1843eba94584a5d0f99333b17c897298dc41300bac89c5e11a4e30eea0f8f0be`  
		Last Modified: Wed, 17 May 2023 23:39:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f485cf85cd150c9df1742ec82e2002e9ad6acacab50c40f31f7b46adda4d8c21`  
		Last Modified: Wed, 17 May 2023 23:39:54 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50290dfffbcb30a78bf125fdaec0f1750cefa90df90e93267a32fef375e85344`  
		Last Modified: Wed, 17 May 2023 23:39:54 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.14`

```console
$ docker pull consul@sha256:bafda0bbe79b2514c19112a1a2587a4b074e80ef72d02860e214b6870b5e21c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.14` - linux; amd64

```console
$ docker pull consul@sha256:c5363f57ebd80acdb08eda2706da303d574800d96686d598991107ce24c4a001
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (57044114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e9cc702d7e2c93f02d73f6bc9900bf40e573cdb6fe7909dc26ab96b4847964`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:33 GMT
ADD file:08ad6c1c886a26e30ae4ab103ff377ee6cfbc1be2437fa227ec28a335c63d78a in / 
# Wed, 29 Mar 2023 18:19:33 GMT
CMD ["/bin/sh"]
# Wed, 17 May 2023 23:21:43 GMT
ARG CONSUL_VERSION=1.14.7
# Wed, 17 May 2023 23:21:43 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 17 May 2023 23:21:43 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 17 May 2023 23:21:44 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 17 May 2023 23:21:50 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 17 May 2023 23:21:50 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 17 May 2023 23:21:51 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 17 May 2023 23:21:51 GMT
VOLUME [/consul/data]
# Wed, 17 May 2023 23:21:51 GMT
EXPOSE 8300
# Wed, 17 May 2023 23:21:51 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 17 May 2023 23:21:51 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 17 May 2023 23:21:51 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 17 May 2023 23:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 May 2023 23:21:51 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0ce1dd7918a48990ab749aab2e805c26f691a3a8103495530e7ea5a1d168af4a`  
		Last Modified: Wed, 29 Mar 2023 18:20:17 GMT  
		Size: 2.8 MB (2826596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001bd6942da9d529f3ee86b01a88dcc743c72ecbf1d0194c81b4a9a46153e098`  
		Last Modified: Wed, 17 May 2023 23:22:13 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0349ac67f6ae8d5912668dbf97fc9b77f276f3d74b18e8d088ec322b22ae7e74`  
		Last Modified: Wed, 17 May 2023 23:22:20 GMT  
		Size: 54.2 MB (54214088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dca13136f6774035c2dde75e01445cfeba66d37c4f4d5cb339ff16c7d08b098`  
		Last Modified: Wed, 17 May 2023 23:22:13 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8316eeeac047103fd632fd127a134a8a087670a870090c849ed9169ed3797e7a`  
		Last Modified: Wed, 17 May 2023 23:22:13 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cbce098aeaa4602998aa92509a72512a177c6063ee11b0895f0a41176b1ec6`  
		Last Modified: Wed, 17 May 2023 23:22:13 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.14` - linux; arm variant v6

```console
$ docker pull consul@sha256:5655fb4055e2450049912d6d293303ea62a257d031ef4d8c0ccb6275d27d3f40
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54308385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba837fa528da48784bfeb8791354cafb9199115878ae852b79cca48d1ef2b21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:13 GMT
ADD file:3fb55ad8134002858be264c3c2477d784e4a60f2f6501afa7cf3b10bfede51aa in / 
# Wed, 29 Mar 2023 18:01:13 GMT
CMD ["/bin/sh"]
# Wed, 17 May 2023 23:49:12 GMT
ARG CONSUL_VERSION=1.14.7
# Wed, 17 May 2023 23:49:12 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 17 May 2023 23:49:12 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 17 May 2023 23:49:12 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 17 May 2023 23:49:27 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 17 May 2023 23:49:28 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 17 May 2023 23:49:29 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 17 May 2023 23:49:29 GMT
VOLUME [/consul/data]
# Wed, 17 May 2023 23:49:29 GMT
EXPOSE 8300
# Wed, 17 May 2023 23:49:29 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 17 May 2023 23:49:29 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 17 May 2023 23:49:29 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 17 May 2023 23:49:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 May 2023 23:49:29 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:872c99a87729fa48dce303fb615edbb1a5da837f627a0b3d28495a0400ca8335`  
		Last Modified: Wed, 29 Mar 2023 18:02:12 GMT  
		Size: 2.6 MB (2634030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273c34ece0209fbfa6f5c20e538b06e0fe3d7c904246b027d4d80d892c3c15e9`  
		Last Modified: Wed, 17 May 2023 23:49:50 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c8e726a483682bc8a4b0ce5b6401c5caacaa7528bbc1d7a43b12b3fe6e805f`  
		Last Modified: Wed, 17 May 2023 23:49:56 GMT  
		Size: 51.7 MB (51670920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5a537bd10bf41bd9c79cde64f5823d1df3fed99b4f13077e9848c6f1b01837`  
		Last Modified: Wed, 17 May 2023 23:49:50 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b015e82dda4e7cd8cbcfe706ac16fc8b656f17923e0618d5577d68776ab4230b`  
		Last Modified: Wed, 17 May 2023 23:49:50 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329fcb89beab57f240eb5ae8b8fb02523a46683c6adb9ab4886110d2831fed1b`  
		Last Modified: Wed, 17 May 2023 23:49:50 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.14` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:1a9c635fa7016f6692f687dd4fb7f996cb2a842e68e577f2c395373a5b837f66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53872276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6d49fc719d3c23b0441a7100d0f086874c46a8edc1c24b16b7da36a707d1e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:22 GMT
ADD file:4acfda16c71abce07068ed23839e9de60c1d1145ab8002b3a92c15b1e80d4356 in / 
# Wed, 29 Mar 2023 17:39:23 GMT
CMD ["/bin/sh"]
# Wed, 17 May 2023 23:40:34 GMT
ARG CONSUL_VERSION=1.14.7
# Wed, 17 May 2023 23:40:34 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 17 May 2023 23:40:34 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 17 May 2023 23:40:34 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 17 May 2023 23:40:39 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 17 May 2023 23:40:40 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 17 May 2023 23:40:41 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 17 May 2023 23:40:41 GMT
VOLUME [/consul/data]
# Wed, 17 May 2023 23:40:41 GMT
EXPOSE 8300
# Wed, 17 May 2023 23:40:41 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 17 May 2023 23:40:41 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 17 May 2023 23:40:41 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 17 May 2023 23:40:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 May 2023 23:40:41 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:60a00c11adf5202a365ec8215b889c3390d67fa295ab79940e1c5dc4cbed9db1`  
		Last Modified: Wed, 29 Mar 2023 17:40:04 GMT  
		Size: 2.7 MB (2722002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21d1d67a6981816fd01dff38912392e2e4cad193338588d9b274eb6481918f2`  
		Last Modified: Wed, 17 May 2023 23:41:00 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a933981abe60a01c127ca720b7e94fda26ad93e300ef99634e3b3da44e55731`  
		Last Modified: Wed, 17 May 2023 23:41:06 GMT  
		Size: 51.1 MB (51146845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f07c7234663f0cd3513b5dfc018961a737c6f81a6edefa7515749716522836a`  
		Last Modified: Wed, 17 May 2023 23:40:59 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8482637c8898f6882b3d8a6fdef6fb5d4994af297dc3b267a42f95a83e35290e`  
		Last Modified: Wed, 17 May 2023 23:40:59 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3868973e3e7b46b5220cf52896b6fb0b78fa7813a03e170a247e86621648eee`  
		Last Modified: Wed, 17 May 2023 23:40:59 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.14` - linux; 386

```console
$ docker pull consul@sha256:bda75767f3cbe46660ef3a9e135dd8beaf7b7e5277e38aa08c4e6770fa3a492f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55689370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7aeafd8d3c68469573129014824f6762c06313fc2ab7c76b1d48593595b9e09`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:36 GMT
ADD file:fca96dde137b6b045359aec9d24257996738ac6cb7cce9518460a66802a27bd7 in / 
# Wed, 29 Mar 2023 17:38:36 GMT
CMD ["/bin/sh"]
# Wed, 17 May 2023 23:38:17 GMT
ARG CONSUL_VERSION=1.14.7
# Wed, 17 May 2023 23:38:17 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 17 May 2023 23:38:17 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 17 May 2023 23:38:17 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 17 May 2023 23:38:32 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 17 May 2023 23:38:33 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 17 May 2023 23:38:34 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 17 May 2023 23:38:34 GMT
VOLUME [/consul/data]
# Wed, 17 May 2023 23:38:34 GMT
EXPOSE 8300
# Wed, 17 May 2023 23:38:34 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 17 May 2023 23:38:34 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 17 May 2023 23:38:34 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 17 May 2023 23:38:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 May 2023 23:38:34 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:333f5f619d7efe58316b2d71276f19d0a59bcb471f4dadaa85762b2c9e02775c`  
		Last Modified: Wed, 29 Mar 2023 17:39:19 GMT  
		Size: 2.8 MB (2832576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec131e0b6632221ff9abc57e740f3182da56f0b7cd935b35c2ca57224fade45`  
		Last Modified: Wed, 17 May 2023 23:38:55 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4bf1af25f5a48c5d01905de3ad55e923f6e085ec47a267c8652baa59b18c860`  
		Last Modified: Wed, 17 May 2023 23:39:46 GMT  
		Size: 52.9 MB (52853361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f411bd4ff09feaf26f3787434434afe4634a9931eecf684ab6e78131cd632a0`  
		Last Modified: Wed, 17 May 2023 23:38:55 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6ce0a9ce342baff51d3838fb013a4eba97a019e925062063691317ef2d0090`  
		Last Modified: Wed, 17 May 2023 23:38:55 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85763bc5c2a26b714e92b97746fe271701120e1f2846cd0379ab4a012b86c328`  
		Last Modified: Wed, 17 May 2023 23:38:55 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.14.7`

```console
$ docker pull consul@sha256:bafda0bbe79b2514c19112a1a2587a4b074e80ef72d02860e214b6870b5e21c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.14.7` - linux; amd64

```console
$ docker pull consul@sha256:c5363f57ebd80acdb08eda2706da303d574800d96686d598991107ce24c4a001
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (57044114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e9cc702d7e2c93f02d73f6bc9900bf40e573cdb6fe7909dc26ab96b4847964`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:33 GMT
ADD file:08ad6c1c886a26e30ae4ab103ff377ee6cfbc1be2437fa227ec28a335c63d78a in / 
# Wed, 29 Mar 2023 18:19:33 GMT
CMD ["/bin/sh"]
# Wed, 17 May 2023 23:21:43 GMT
ARG CONSUL_VERSION=1.14.7
# Wed, 17 May 2023 23:21:43 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 17 May 2023 23:21:43 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 17 May 2023 23:21:44 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 17 May 2023 23:21:50 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 17 May 2023 23:21:50 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 17 May 2023 23:21:51 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 17 May 2023 23:21:51 GMT
VOLUME [/consul/data]
# Wed, 17 May 2023 23:21:51 GMT
EXPOSE 8300
# Wed, 17 May 2023 23:21:51 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 17 May 2023 23:21:51 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 17 May 2023 23:21:51 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 17 May 2023 23:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 May 2023 23:21:51 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0ce1dd7918a48990ab749aab2e805c26f691a3a8103495530e7ea5a1d168af4a`  
		Last Modified: Wed, 29 Mar 2023 18:20:17 GMT  
		Size: 2.8 MB (2826596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001bd6942da9d529f3ee86b01a88dcc743c72ecbf1d0194c81b4a9a46153e098`  
		Last Modified: Wed, 17 May 2023 23:22:13 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0349ac67f6ae8d5912668dbf97fc9b77f276f3d74b18e8d088ec322b22ae7e74`  
		Last Modified: Wed, 17 May 2023 23:22:20 GMT  
		Size: 54.2 MB (54214088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dca13136f6774035c2dde75e01445cfeba66d37c4f4d5cb339ff16c7d08b098`  
		Last Modified: Wed, 17 May 2023 23:22:13 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8316eeeac047103fd632fd127a134a8a087670a870090c849ed9169ed3797e7a`  
		Last Modified: Wed, 17 May 2023 23:22:13 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cbce098aeaa4602998aa92509a72512a177c6063ee11b0895f0a41176b1ec6`  
		Last Modified: Wed, 17 May 2023 23:22:13 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.14.7` - linux; arm variant v6

```console
$ docker pull consul@sha256:5655fb4055e2450049912d6d293303ea62a257d031ef4d8c0ccb6275d27d3f40
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54308385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba837fa528da48784bfeb8791354cafb9199115878ae852b79cca48d1ef2b21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:13 GMT
ADD file:3fb55ad8134002858be264c3c2477d784e4a60f2f6501afa7cf3b10bfede51aa in / 
# Wed, 29 Mar 2023 18:01:13 GMT
CMD ["/bin/sh"]
# Wed, 17 May 2023 23:49:12 GMT
ARG CONSUL_VERSION=1.14.7
# Wed, 17 May 2023 23:49:12 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 17 May 2023 23:49:12 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 17 May 2023 23:49:12 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 17 May 2023 23:49:27 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 17 May 2023 23:49:28 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 17 May 2023 23:49:29 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 17 May 2023 23:49:29 GMT
VOLUME [/consul/data]
# Wed, 17 May 2023 23:49:29 GMT
EXPOSE 8300
# Wed, 17 May 2023 23:49:29 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 17 May 2023 23:49:29 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 17 May 2023 23:49:29 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 17 May 2023 23:49:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 May 2023 23:49:29 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:872c99a87729fa48dce303fb615edbb1a5da837f627a0b3d28495a0400ca8335`  
		Last Modified: Wed, 29 Mar 2023 18:02:12 GMT  
		Size: 2.6 MB (2634030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273c34ece0209fbfa6f5c20e538b06e0fe3d7c904246b027d4d80d892c3c15e9`  
		Last Modified: Wed, 17 May 2023 23:49:50 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c8e726a483682bc8a4b0ce5b6401c5caacaa7528bbc1d7a43b12b3fe6e805f`  
		Last Modified: Wed, 17 May 2023 23:49:56 GMT  
		Size: 51.7 MB (51670920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5a537bd10bf41bd9c79cde64f5823d1df3fed99b4f13077e9848c6f1b01837`  
		Last Modified: Wed, 17 May 2023 23:49:50 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b015e82dda4e7cd8cbcfe706ac16fc8b656f17923e0618d5577d68776ab4230b`  
		Last Modified: Wed, 17 May 2023 23:49:50 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329fcb89beab57f240eb5ae8b8fb02523a46683c6adb9ab4886110d2831fed1b`  
		Last Modified: Wed, 17 May 2023 23:49:50 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.14.7` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:1a9c635fa7016f6692f687dd4fb7f996cb2a842e68e577f2c395373a5b837f66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53872276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6d49fc719d3c23b0441a7100d0f086874c46a8edc1c24b16b7da36a707d1e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:22 GMT
ADD file:4acfda16c71abce07068ed23839e9de60c1d1145ab8002b3a92c15b1e80d4356 in / 
# Wed, 29 Mar 2023 17:39:23 GMT
CMD ["/bin/sh"]
# Wed, 17 May 2023 23:40:34 GMT
ARG CONSUL_VERSION=1.14.7
# Wed, 17 May 2023 23:40:34 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 17 May 2023 23:40:34 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 17 May 2023 23:40:34 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 17 May 2023 23:40:39 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 17 May 2023 23:40:40 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 17 May 2023 23:40:41 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 17 May 2023 23:40:41 GMT
VOLUME [/consul/data]
# Wed, 17 May 2023 23:40:41 GMT
EXPOSE 8300
# Wed, 17 May 2023 23:40:41 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 17 May 2023 23:40:41 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 17 May 2023 23:40:41 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 17 May 2023 23:40:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 May 2023 23:40:41 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:60a00c11adf5202a365ec8215b889c3390d67fa295ab79940e1c5dc4cbed9db1`  
		Last Modified: Wed, 29 Mar 2023 17:40:04 GMT  
		Size: 2.7 MB (2722002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21d1d67a6981816fd01dff38912392e2e4cad193338588d9b274eb6481918f2`  
		Last Modified: Wed, 17 May 2023 23:41:00 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a933981abe60a01c127ca720b7e94fda26ad93e300ef99634e3b3da44e55731`  
		Last Modified: Wed, 17 May 2023 23:41:06 GMT  
		Size: 51.1 MB (51146845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f07c7234663f0cd3513b5dfc018961a737c6f81a6edefa7515749716522836a`  
		Last Modified: Wed, 17 May 2023 23:40:59 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8482637c8898f6882b3d8a6fdef6fb5d4994af297dc3b267a42f95a83e35290e`  
		Last Modified: Wed, 17 May 2023 23:40:59 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3868973e3e7b46b5220cf52896b6fb0b78fa7813a03e170a247e86621648eee`  
		Last Modified: Wed, 17 May 2023 23:40:59 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.14.7` - linux; 386

```console
$ docker pull consul@sha256:bda75767f3cbe46660ef3a9e135dd8beaf7b7e5277e38aa08c4e6770fa3a492f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55689370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7aeafd8d3c68469573129014824f6762c06313fc2ab7c76b1d48593595b9e09`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:36 GMT
ADD file:fca96dde137b6b045359aec9d24257996738ac6cb7cce9518460a66802a27bd7 in / 
# Wed, 29 Mar 2023 17:38:36 GMT
CMD ["/bin/sh"]
# Wed, 17 May 2023 23:38:17 GMT
ARG CONSUL_VERSION=1.14.7
# Wed, 17 May 2023 23:38:17 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 17 May 2023 23:38:17 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 17 May 2023 23:38:17 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 17 May 2023 23:38:32 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 17 May 2023 23:38:33 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 17 May 2023 23:38:34 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 17 May 2023 23:38:34 GMT
VOLUME [/consul/data]
# Wed, 17 May 2023 23:38:34 GMT
EXPOSE 8300
# Wed, 17 May 2023 23:38:34 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 17 May 2023 23:38:34 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 17 May 2023 23:38:34 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 17 May 2023 23:38:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 May 2023 23:38:34 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:333f5f619d7efe58316b2d71276f19d0a59bcb471f4dadaa85762b2c9e02775c`  
		Last Modified: Wed, 29 Mar 2023 17:39:19 GMT  
		Size: 2.8 MB (2832576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec131e0b6632221ff9abc57e740f3182da56f0b7cd935b35c2ca57224fade45`  
		Last Modified: Wed, 17 May 2023 23:38:55 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4bf1af25f5a48c5d01905de3ad55e923f6e085ec47a267c8652baa59b18c860`  
		Last Modified: Wed, 17 May 2023 23:39:46 GMT  
		Size: 52.9 MB (52853361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f411bd4ff09feaf26f3787434434afe4634a9931eecf684ab6e78131cd632a0`  
		Last Modified: Wed, 17 May 2023 23:38:55 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6ce0a9ce342baff51d3838fb013a4eba97a019e925062063691317ef2d0090`  
		Last Modified: Wed, 17 May 2023 23:38:55 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85763bc5c2a26b714e92b97746fe271701120e1f2846cd0379ab4a012b86c328`  
		Last Modified: Wed, 17 May 2023 23:38:55 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.15`

```console
$ docker pull consul@sha256:4649f00e13177a5ace9620f5746abf6dd3cfb48b7828957e94db2f03616a780e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.15` - linux; amd64

```console
$ docker pull consul@sha256:3e1bd5bccd3e78b0aedb6c145ea6d5541f56d1a1156285a1323662367f52fc92
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60732422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99d8a688dd368dfc01d7c582a58cce6499b05073367a431a0f1923ae1e75a37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:33 GMT
ADD file:08ad6c1c886a26e30ae4ab103ff377ee6cfbc1be2437fa227ec28a335c63d78a in / 
# Wed, 29 Mar 2023 18:19:33 GMT
CMD ["/bin/sh"]
# Sun, 04 Jun 2023 17:39:56 GMT
ARG CONSUL_VERSION=1.15.3
# Sun, 04 Jun 2023 17:39:56 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sun, 04 Jun 2023 17:39:56 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sun, 04 Jun 2023 17:39:57 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN addgroup consul &&     adduser -S -G consul consul
# Sun, 04 Jun 2023 17:40:03 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sun, 04 Jun 2023 17:40:04 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sun, 04 Jun 2023 17:40:04 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sun, 04 Jun 2023 17:40:04 GMT
VOLUME [/consul/data]
# Sun, 04 Jun 2023 17:40:04 GMT
EXPOSE 8300
# Sun, 04 Jun 2023 17:40:04 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sun, 04 Jun 2023 17:40:04 GMT
EXPOSE 8500 8600 8600/udp
# Sun, 04 Jun 2023 17:40:05 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Sun, 04 Jun 2023 17:40:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 04 Jun 2023 17:40:05 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0ce1dd7918a48990ab749aab2e805c26f691a3a8103495530e7ea5a1d168af4a`  
		Last Modified: Wed, 29 Mar 2023 18:20:17 GMT  
		Size: 2.8 MB (2826596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b915e8f855b6690f0165f7483cef7426ea7282acab6c7b3702b3717021dd89a`  
		Last Modified: Sun, 04 Jun 2023 17:40:19 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab4e1ebead2514ccc0c2dbe58db284c6cf68996f3c4810d393e144eaccd0ab0`  
		Last Modified: Sun, 04 Jun 2023 17:40:25 GMT  
		Size: 57.9 MB (57902395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef376008726bca2cf9c89957ce3f2d98b94b8fe38125f5250510378ab918391`  
		Last Modified: Sun, 04 Jun 2023 17:40:19 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06ea914c246d6fc3771aef0af68d090aa389bace0ea5039e9814bc4fccccd3b`  
		Last Modified: Sun, 04 Jun 2023 17:40:19 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c5462ee475b4cfd8b65edf36981eb63a7db89e1112e7939e1c26b79fbec28c`  
		Last Modified: Sun, 04 Jun 2023 17:40:19 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.15` - linux; arm variant v6

```console
$ docker pull consul@sha256:ffc0b9ac394e56f9f3464d459d68491b0b87cf755ac047d3238f8031c6fc7548
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.4 MB (56396434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637faabcc495bd1314e04284dbfe69a8d2c5fce1fd748bd7b73e40271a43afb6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:13 GMT
ADD file:3fb55ad8134002858be264c3c2477d784e4a60f2f6501afa7cf3b10bfede51aa in / 
# Wed, 29 Mar 2023 18:01:13 GMT
CMD ["/bin/sh"]
# Fri, 02 Jun 2023 18:49:14 GMT
ARG CONSUL_VERSION=1.15.3
# Fri, 02 Jun 2023 18:49:14 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 02 Jun 2023 18:49:15 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 02 Jun 2023 18:49:15 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 02 Jun 2023 18:49:27 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 02 Jun 2023 18:49:28 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 02 Jun 2023 18:49:29 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 02 Jun 2023 18:49:29 GMT
VOLUME [/consul/data]
# Fri, 02 Jun 2023 18:49:29 GMT
EXPOSE 8300
# Fri, 02 Jun 2023 18:49:29 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 02 Jun 2023 18:49:29 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 02 Jun 2023 18:49:29 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jun 2023 18:49:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jun 2023 18:49:30 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:872c99a87729fa48dce303fb615edbb1a5da837f627a0b3d28495a0400ca8335`  
		Last Modified: Wed, 29 Mar 2023 18:02:12 GMT  
		Size: 2.6 MB (2634030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaed5ddc617d0eb1a14dae5dad411f7c5d20b584fe3f689ba445c1a0204dbeab`  
		Last Modified: Fri, 02 Jun 2023 18:49:44 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ad912b6763ca763bcd669566ef1af9dec649f9b2b8dc0af37f55c5ef58263a`  
		Last Modified: Fri, 02 Jun 2023 18:49:57 GMT  
		Size: 53.8 MB (53758972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476da9112b22e4239b61f986e54301aff2cd2b892b9c5cf84b6ef94381b2c44d`  
		Last Modified: Fri, 02 Jun 2023 18:49:44 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deec611eb874877b4b97f4937d152d9c78150a6e77f4a08a243089130115b57c`  
		Last Modified: Fri, 02 Jun 2023 18:49:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f7b1985432074aa9e1b042577f8edfef38cbb20bea5a0017ba682a762e8899d`  
		Last Modified: Fri, 02 Jun 2023 18:49:44 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.15` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:d76e5d6c02d677af958fb795b4a25570c1d51ed5c956d5408ee5e2be5dfb3e76
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (55966023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab943cdbbf734392e1a4b583a9429dc9ce48a73fe1960b2a771e377868dcdb35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:22 GMT
ADD file:4acfda16c71abce07068ed23839e9de60c1d1145ab8002b3a92c15b1e80d4356 in / 
# Wed, 29 Mar 2023 17:39:23 GMT
CMD ["/bin/sh"]
# Fri, 02 Jun 2023 19:39:19 GMT
ARG CONSUL_VERSION=1.15.3
# Fri, 02 Jun 2023 19:39:19 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 02 Jun 2023 19:39:20 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 02 Jun 2023 19:39:20 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 02 Jun 2023 19:39:25 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 02 Jun 2023 19:39:26 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 02 Jun 2023 19:39:27 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 02 Jun 2023 19:39:27 GMT
VOLUME [/consul/data]
# Fri, 02 Jun 2023 19:39:27 GMT
EXPOSE 8300
# Fri, 02 Jun 2023 19:39:27 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 02 Jun 2023 19:39:27 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 02 Jun 2023 19:39:27 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jun 2023 19:39:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jun 2023 19:39:27 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:60a00c11adf5202a365ec8215b889c3390d67fa295ab79940e1c5dc4cbed9db1`  
		Last Modified: Wed, 29 Mar 2023 17:40:04 GMT  
		Size: 2.7 MB (2722002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65fe27fa4b748ffb44cdd57bc954bacf73fcd06174ff6e24862294c556209700`  
		Last Modified: Fri, 02 Jun 2023 19:39:40 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa889f72f540d2ccc320b9ab84bdb9c00e9d7bfdc56e4acde6f004f8d5b2b0d`  
		Last Modified: Fri, 02 Jun 2023 19:39:45 GMT  
		Size: 53.2 MB (53240590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4a76575ed35c5feb5304ed796ccf72671910ea1d72932c0b66c5f3c11bb59e`  
		Last Modified: Fri, 02 Jun 2023 19:39:40 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2833ff0491c869bf1637e1a65f096ae6887dcfd39fecd92d8f539df1ace96f`  
		Last Modified: Fri, 02 Jun 2023 19:39:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d1f58347668ed7680a65524d03bc091df4beb2ca6ad821ab3ef0922f6bd369`  
		Last Modified: Fri, 02 Jun 2023 19:39:40 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.15` - linux; 386

```console
$ docker pull consul@sha256:01b108a1a2a8326c056229a0a0632bf5d9a1aa5624fcf03d071b5b7cd65a1b92
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59272636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a81b0671c7828f178893775dc3a974e950af0fb0ca6832cad2ccb775c5e25b0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:36 GMT
ADD file:fca96dde137b6b045359aec9d24257996738ac6cb7cce9518460a66802a27bd7 in / 
# Wed, 29 Mar 2023 17:38:36 GMT
CMD ["/bin/sh"]
# Fri, 02 Jun 2023 19:38:14 GMT
ARG CONSUL_VERSION=1.15.3
# Fri, 02 Jun 2023 19:38:14 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 02 Jun 2023 19:38:14 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 02 Jun 2023 19:38:15 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 02 Jun 2023 19:38:30 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 02 Jun 2023 19:38:31 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 02 Jun 2023 19:38:31 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 02 Jun 2023 19:38:31 GMT
VOLUME [/consul/data]
# Fri, 02 Jun 2023 19:38:31 GMT
EXPOSE 8300
# Fri, 02 Jun 2023 19:38:32 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 02 Jun 2023 19:38:32 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 02 Jun 2023 19:38:32 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jun 2023 19:38:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jun 2023 19:38:32 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:333f5f619d7efe58316b2d71276f19d0a59bcb471f4dadaa85762b2c9e02775c`  
		Last Modified: Wed, 29 Mar 2023 17:39:19 GMT  
		Size: 2.8 MB (2832576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d32ca13c154fa47b1489aaa22373c89c457e0dc2749f7c49957951b934fdb62`  
		Last Modified: Fri, 02 Jun 2023 19:38:43 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c083da367850361ff166d595d2444cf0498464b453bf44a769713cd1a6774d1`  
		Last Modified: Fri, 02 Jun 2023 19:38:52 GMT  
		Size: 56.4 MB (56436631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b5968913b40daee57281517d5f32722a7ee3954d3cc13ef610eeae053c79f3`  
		Last Modified: Fri, 02 Jun 2023 19:38:43 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86bc4d621b13451b0f62bc5463f6474a46b43f0ad70e4d85931e1a2e1a662c13`  
		Last Modified: Fri, 02 Jun 2023 19:38:43 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a70266e0f7ce261d87f054a6dece387e39d558065144bf4379d9b1bfa7f630`  
		Last Modified: Fri, 02 Jun 2023 19:38:43 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.15.3`

```console
$ docker pull consul@sha256:4649f00e13177a5ace9620f5746abf6dd3cfb48b7828957e94db2f03616a780e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.15.3` - linux; amd64

```console
$ docker pull consul@sha256:3e1bd5bccd3e78b0aedb6c145ea6d5541f56d1a1156285a1323662367f52fc92
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60732422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99d8a688dd368dfc01d7c582a58cce6499b05073367a431a0f1923ae1e75a37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:33 GMT
ADD file:08ad6c1c886a26e30ae4ab103ff377ee6cfbc1be2437fa227ec28a335c63d78a in / 
# Wed, 29 Mar 2023 18:19:33 GMT
CMD ["/bin/sh"]
# Sun, 04 Jun 2023 17:39:56 GMT
ARG CONSUL_VERSION=1.15.3
# Sun, 04 Jun 2023 17:39:56 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sun, 04 Jun 2023 17:39:56 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sun, 04 Jun 2023 17:39:57 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN addgroup consul &&     adduser -S -G consul consul
# Sun, 04 Jun 2023 17:40:03 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sun, 04 Jun 2023 17:40:04 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sun, 04 Jun 2023 17:40:04 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sun, 04 Jun 2023 17:40:04 GMT
VOLUME [/consul/data]
# Sun, 04 Jun 2023 17:40:04 GMT
EXPOSE 8300
# Sun, 04 Jun 2023 17:40:04 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sun, 04 Jun 2023 17:40:04 GMT
EXPOSE 8500 8600 8600/udp
# Sun, 04 Jun 2023 17:40:05 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Sun, 04 Jun 2023 17:40:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 04 Jun 2023 17:40:05 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0ce1dd7918a48990ab749aab2e805c26f691a3a8103495530e7ea5a1d168af4a`  
		Last Modified: Wed, 29 Mar 2023 18:20:17 GMT  
		Size: 2.8 MB (2826596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b915e8f855b6690f0165f7483cef7426ea7282acab6c7b3702b3717021dd89a`  
		Last Modified: Sun, 04 Jun 2023 17:40:19 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab4e1ebead2514ccc0c2dbe58db284c6cf68996f3c4810d393e144eaccd0ab0`  
		Last Modified: Sun, 04 Jun 2023 17:40:25 GMT  
		Size: 57.9 MB (57902395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef376008726bca2cf9c89957ce3f2d98b94b8fe38125f5250510378ab918391`  
		Last Modified: Sun, 04 Jun 2023 17:40:19 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06ea914c246d6fc3771aef0af68d090aa389bace0ea5039e9814bc4fccccd3b`  
		Last Modified: Sun, 04 Jun 2023 17:40:19 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c5462ee475b4cfd8b65edf36981eb63a7db89e1112e7939e1c26b79fbec28c`  
		Last Modified: Sun, 04 Jun 2023 17:40:19 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.15.3` - linux; arm variant v6

```console
$ docker pull consul@sha256:ffc0b9ac394e56f9f3464d459d68491b0b87cf755ac047d3238f8031c6fc7548
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.4 MB (56396434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637faabcc495bd1314e04284dbfe69a8d2c5fce1fd748bd7b73e40271a43afb6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:13 GMT
ADD file:3fb55ad8134002858be264c3c2477d784e4a60f2f6501afa7cf3b10bfede51aa in / 
# Wed, 29 Mar 2023 18:01:13 GMT
CMD ["/bin/sh"]
# Fri, 02 Jun 2023 18:49:14 GMT
ARG CONSUL_VERSION=1.15.3
# Fri, 02 Jun 2023 18:49:14 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 02 Jun 2023 18:49:15 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 02 Jun 2023 18:49:15 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 02 Jun 2023 18:49:27 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 02 Jun 2023 18:49:28 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 02 Jun 2023 18:49:29 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 02 Jun 2023 18:49:29 GMT
VOLUME [/consul/data]
# Fri, 02 Jun 2023 18:49:29 GMT
EXPOSE 8300
# Fri, 02 Jun 2023 18:49:29 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 02 Jun 2023 18:49:29 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 02 Jun 2023 18:49:29 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jun 2023 18:49:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jun 2023 18:49:30 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:872c99a87729fa48dce303fb615edbb1a5da837f627a0b3d28495a0400ca8335`  
		Last Modified: Wed, 29 Mar 2023 18:02:12 GMT  
		Size: 2.6 MB (2634030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaed5ddc617d0eb1a14dae5dad411f7c5d20b584fe3f689ba445c1a0204dbeab`  
		Last Modified: Fri, 02 Jun 2023 18:49:44 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ad912b6763ca763bcd669566ef1af9dec649f9b2b8dc0af37f55c5ef58263a`  
		Last Modified: Fri, 02 Jun 2023 18:49:57 GMT  
		Size: 53.8 MB (53758972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476da9112b22e4239b61f986e54301aff2cd2b892b9c5cf84b6ef94381b2c44d`  
		Last Modified: Fri, 02 Jun 2023 18:49:44 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deec611eb874877b4b97f4937d152d9c78150a6e77f4a08a243089130115b57c`  
		Last Modified: Fri, 02 Jun 2023 18:49:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f7b1985432074aa9e1b042577f8edfef38cbb20bea5a0017ba682a762e8899d`  
		Last Modified: Fri, 02 Jun 2023 18:49:44 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.15.3` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:d76e5d6c02d677af958fb795b4a25570c1d51ed5c956d5408ee5e2be5dfb3e76
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (55966023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab943cdbbf734392e1a4b583a9429dc9ce48a73fe1960b2a771e377868dcdb35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:22 GMT
ADD file:4acfda16c71abce07068ed23839e9de60c1d1145ab8002b3a92c15b1e80d4356 in / 
# Wed, 29 Mar 2023 17:39:23 GMT
CMD ["/bin/sh"]
# Fri, 02 Jun 2023 19:39:19 GMT
ARG CONSUL_VERSION=1.15.3
# Fri, 02 Jun 2023 19:39:19 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 02 Jun 2023 19:39:20 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 02 Jun 2023 19:39:20 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 02 Jun 2023 19:39:25 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 02 Jun 2023 19:39:26 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 02 Jun 2023 19:39:27 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 02 Jun 2023 19:39:27 GMT
VOLUME [/consul/data]
# Fri, 02 Jun 2023 19:39:27 GMT
EXPOSE 8300
# Fri, 02 Jun 2023 19:39:27 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 02 Jun 2023 19:39:27 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 02 Jun 2023 19:39:27 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jun 2023 19:39:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jun 2023 19:39:27 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:60a00c11adf5202a365ec8215b889c3390d67fa295ab79940e1c5dc4cbed9db1`  
		Last Modified: Wed, 29 Mar 2023 17:40:04 GMT  
		Size: 2.7 MB (2722002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65fe27fa4b748ffb44cdd57bc954bacf73fcd06174ff6e24862294c556209700`  
		Last Modified: Fri, 02 Jun 2023 19:39:40 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa889f72f540d2ccc320b9ab84bdb9c00e9d7bfdc56e4acde6f004f8d5b2b0d`  
		Last Modified: Fri, 02 Jun 2023 19:39:45 GMT  
		Size: 53.2 MB (53240590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4a76575ed35c5feb5304ed796ccf72671910ea1d72932c0b66c5f3c11bb59e`  
		Last Modified: Fri, 02 Jun 2023 19:39:40 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2833ff0491c869bf1637e1a65f096ae6887dcfd39fecd92d8f539df1ace96f`  
		Last Modified: Fri, 02 Jun 2023 19:39:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d1f58347668ed7680a65524d03bc091df4beb2ca6ad821ab3ef0922f6bd369`  
		Last Modified: Fri, 02 Jun 2023 19:39:40 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.15.3` - linux; 386

```console
$ docker pull consul@sha256:01b108a1a2a8326c056229a0a0632bf5d9a1aa5624fcf03d071b5b7cd65a1b92
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59272636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a81b0671c7828f178893775dc3a974e950af0fb0ca6832cad2ccb775c5e25b0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:36 GMT
ADD file:fca96dde137b6b045359aec9d24257996738ac6cb7cce9518460a66802a27bd7 in / 
# Wed, 29 Mar 2023 17:38:36 GMT
CMD ["/bin/sh"]
# Fri, 02 Jun 2023 19:38:14 GMT
ARG CONSUL_VERSION=1.15.3
# Fri, 02 Jun 2023 19:38:14 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 02 Jun 2023 19:38:14 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 02 Jun 2023 19:38:15 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 02 Jun 2023 19:38:30 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 02 Jun 2023 19:38:31 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 02 Jun 2023 19:38:31 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 02 Jun 2023 19:38:31 GMT
VOLUME [/consul/data]
# Fri, 02 Jun 2023 19:38:31 GMT
EXPOSE 8300
# Fri, 02 Jun 2023 19:38:32 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 02 Jun 2023 19:38:32 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 02 Jun 2023 19:38:32 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jun 2023 19:38:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jun 2023 19:38:32 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:333f5f619d7efe58316b2d71276f19d0a59bcb471f4dadaa85762b2c9e02775c`  
		Last Modified: Wed, 29 Mar 2023 17:39:19 GMT  
		Size: 2.8 MB (2832576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d32ca13c154fa47b1489aaa22373c89c457e0dc2749f7c49957951b934fdb62`  
		Last Modified: Fri, 02 Jun 2023 19:38:43 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c083da367850361ff166d595d2444cf0498464b453bf44a769713cd1a6774d1`  
		Last Modified: Fri, 02 Jun 2023 19:38:52 GMT  
		Size: 56.4 MB (56436631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b5968913b40daee57281517d5f32722a7ee3954d3cc13ef610eeae053c79f3`  
		Last Modified: Fri, 02 Jun 2023 19:38:43 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86bc4d621b13451b0f62bc5463f6474a46b43f0ad70e4d85931e1a2e1a662c13`  
		Last Modified: Fri, 02 Jun 2023 19:38:43 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a70266e0f7ce261d87f054a6dece387e39d558065144bf4379d9b1bfa7f630`  
		Last Modified: Fri, 02 Jun 2023 19:38:43 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:latest`

```console
$ docker pull consul@sha256:4649f00e13177a5ace9620f5746abf6dd3cfb48b7828957e94db2f03616a780e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:latest` - linux; amd64

```console
$ docker pull consul@sha256:3e1bd5bccd3e78b0aedb6c145ea6d5541f56d1a1156285a1323662367f52fc92
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60732422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99d8a688dd368dfc01d7c582a58cce6499b05073367a431a0f1923ae1e75a37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:33 GMT
ADD file:08ad6c1c886a26e30ae4ab103ff377ee6cfbc1be2437fa227ec28a335c63d78a in / 
# Wed, 29 Mar 2023 18:19:33 GMT
CMD ["/bin/sh"]
# Sun, 04 Jun 2023 17:39:56 GMT
ARG CONSUL_VERSION=1.15.3
# Sun, 04 Jun 2023 17:39:56 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sun, 04 Jun 2023 17:39:56 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sun, 04 Jun 2023 17:39:57 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN addgroup consul &&     adduser -S -G consul consul
# Sun, 04 Jun 2023 17:40:03 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sun, 04 Jun 2023 17:40:04 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sun, 04 Jun 2023 17:40:04 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sun, 04 Jun 2023 17:40:04 GMT
VOLUME [/consul/data]
# Sun, 04 Jun 2023 17:40:04 GMT
EXPOSE 8300
# Sun, 04 Jun 2023 17:40:04 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sun, 04 Jun 2023 17:40:04 GMT
EXPOSE 8500 8600 8600/udp
# Sun, 04 Jun 2023 17:40:05 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Sun, 04 Jun 2023 17:40:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 04 Jun 2023 17:40:05 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0ce1dd7918a48990ab749aab2e805c26f691a3a8103495530e7ea5a1d168af4a`  
		Last Modified: Wed, 29 Mar 2023 18:20:17 GMT  
		Size: 2.8 MB (2826596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b915e8f855b6690f0165f7483cef7426ea7282acab6c7b3702b3717021dd89a`  
		Last Modified: Sun, 04 Jun 2023 17:40:19 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab4e1ebead2514ccc0c2dbe58db284c6cf68996f3c4810d393e144eaccd0ab0`  
		Last Modified: Sun, 04 Jun 2023 17:40:25 GMT  
		Size: 57.9 MB (57902395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef376008726bca2cf9c89957ce3f2d98b94b8fe38125f5250510378ab918391`  
		Last Modified: Sun, 04 Jun 2023 17:40:19 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06ea914c246d6fc3771aef0af68d090aa389bace0ea5039e9814bc4fccccd3b`  
		Last Modified: Sun, 04 Jun 2023 17:40:19 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c5462ee475b4cfd8b65edf36981eb63a7db89e1112e7939e1c26b79fbec28c`  
		Last Modified: Sun, 04 Jun 2023 17:40:19 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm variant v6

```console
$ docker pull consul@sha256:ffc0b9ac394e56f9f3464d459d68491b0b87cf755ac047d3238f8031c6fc7548
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.4 MB (56396434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637faabcc495bd1314e04284dbfe69a8d2c5fce1fd748bd7b73e40271a43afb6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:13 GMT
ADD file:3fb55ad8134002858be264c3c2477d784e4a60f2f6501afa7cf3b10bfede51aa in / 
# Wed, 29 Mar 2023 18:01:13 GMT
CMD ["/bin/sh"]
# Fri, 02 Jun 2023 18:49:14 GMT
ARG CONSUL_VERSION=1.15.3
# Fri, 02 Jun 2023 18:49:14 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 02 Jun 2023 18:49:15 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 02 Jun 2023 18:49:15 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 02 Jun 2023 18:49:27 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 02 Jun 2023 18:49:28 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 02 Jun 2023 18:49:29 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 02 Jun 2023 18:49:29 GMT
VOLUME [/consul/data]
# Fri, 02 Jun 2023 18:49:29 GMT
EXPOSE 8300
# Fri, 02 Jun 2023 18:49:29 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 02 Jun 2023 18:49:29 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 02 Jun 2023 18:49:29 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jun 2023 18:49:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jun 2023 18:49:30 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:872c99a87729fa48dce303fb615edbb1a5da837f627a0b3d28495a0400ca8335`  
		Last Modified: Wed, 29 Mar 2023 18:02:12 GMT  
		Size: 2.6 MB (2634030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaed5ddc617d0eb1a14dae5dad411f7c5d20b584fe3f689ba445c1a0204dbeab`  
		Last Modified: Fri, 02 Jun 2023 18:49:44 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ad912b6763ca763bcd669566ef1af9dec649f9b2b8dc0af37f55c5ef58263a`  
		Last Modified: Fri, 02 Jun 2023 18:49:57 GMT  
		Size: 53.8 MB (53758972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476da9112b22e4239b61f986e54301aff2cd2b892b9c5cf84b6ef94381b2c44d`  
		Last Modified: Fri, 02 Jun 2023 18:49:44 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deec611eb874877b4b97f4937d152d9c78150a6e77f4a08a243089130115b57c`  
		Last Modified: Fri, 02 Jun 2023 18:49:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f7b1985432074aa9e1b042577f8edfef38cbb20bea5a0017ba682a762e8899d`  
		Last Modified: Fri, 02 Jun 2023 18:49:44 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:d76e5d6c02d677af958fb795b4a25570c1d51ed5c956d5408ee5e2be5dfb3e76
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (55966023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab943cdbbf734392e1a4b583a9429dc9ce48a73fe1960b2a771e377868dcdb35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:22 GMT
ADD file:4acfda16c71abce07068ed23839e9de60c1d1145ab8002b3a92c15b1e80d4356 in / 
# Wed, 29 Mar 2023 17:39:23 GMT
CMD ["/bin/sh"]
# Fri, 02 Jun 2023 19:39:19 GMT
ARG CONSUL_VERSION=1.15.3
# Fri, 02 Jun 2023 19:39:19 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 02 Jun 2023 19:39:20 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 02 Jun 2023 19:39:20 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 02 Jun 2023 19:39:25 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 02 Jun 2023 19:39:26 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 02 Jun 2023 19:39:27 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 02 Jun 2023 19:39:27 GMT
VOLUME [/consul/data]
# Fri, 02 Jun 2023 19:39:27 GMT
EXPOSE 8300
# Fri, 02 Jun 2023 19:39:27 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 02 Jun 2023 19:39:27 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 02 Jun 2023 19:39:27 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jun 2023 19:39:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jun 2023 19:39:27 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:60a00c11adf5202a365ec8215b889c3390d67fa295ab79940e1c5dc4cbed9db1`  
		Last Modified: Wed, 29 Mar 2023 17:40:04 GMT  
		Size: 2.7 MB (2722002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65fe27fa4b748ffb44cdd57bc954bacf73fcd06174ff6e24862294c556209700`  
		Last Modified: Fri, 02 Jun 2023 19:39:40 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa889f72f540d2ccc320b9ab84bdb9c00e9d7bfdc56e4acde6f004f8d5b2b0d`  
		Last Modified: Fri, 02 Jun 2023 19:39:45 GMT  
		Size: 53.2 MB (53240590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4a76575ed35c5feb5304ed796ccf72671910ea1d72932c0b66c5f3c11bb59e`  
		Last Modified: Fri, 02 Jun 2023 19:39:40 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2833ff0491c869bf1637e1a65f096ae6887dcfd39fecd92d8f539df1ace96f`  
		Last Modified: Fri, 02 Jun 2023 19:39:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d1f58347668ed7680a65524d03bc091df4beb2ca6ad821ab3ef0922f6bd369`  
		Last Modified: Fri, 02 Jun 2023 19:39:40 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; 386

```console
$ docker pull consul@sha256:01b108a1a2a8326c056229a0a0632bf5d9a1aa5624fcf03d071b5b7cd65a1b92
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59272636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a81b0671c7828f178893775dc3a974e950af0fb0ca6832cad2ccb775c5e25b0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:36 GMT
ADD file:fca96dde137b6b045359aec9d24257996738ac6cb7cce9518460a66802a27bd7 in / 
# Wed, 29 Mar 2023 17:38:36 GMT
CMD ["/bin/sh"]
# Fri, 02 Jun 2023 19:38:14 GMT
ARG CONSUL_VERSION=1.15.3
# Fri, 02 Jun 2023 19:38:14 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 02 Jun 2023 19:38:14 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 02 Jun 2023 19:38:15 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 02 Jun 2023 19:38:30 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 02 Jun 2023 19:38:31 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 02 Jun 2023 19:38:31 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 02 Jun 2023 19:38:31 GMT
VOLUME [/consul/data]
# Fri, 02 Jun 2023 19:38:31 GMT
EXPOSE 8300
# Fri, 02 Jun 2023 19:38:32 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 02 Jun 2023 19:38:32 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 02 Jun 2023 19:38:32 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jun 2023 19:38:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jun 2023 19:38:32 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:333f5f619d7efe58316b2d71276f19d0a59bcb471f4dadaa85762b2c9e02775c`  
		Last Modified: Wed, 29 Mar 2023 17:39:19 GMT  
		Size: 2.8 MB (2832576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d32ca13c154fa47b1489aaa22373c89c457e0dc2749f7c49957951b934fdb62`  
		Last Modified: Fri, 02 Jun 2023 19:38:43 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c083da367850361ff166d595d2444cf0498464b453bf44a769713cd1a6774d1`  
		Last Modified: Fri, 02 Jun 2023 19:38:52 GMT  
		Size: 56.4 MB (56436631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b5968913b40daee57281517d5f32722a7ee3954d3cc13ef610eeae053c79f3`  
		Last Modified: Fri, 02 Jun 2023 19:38:43 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86bc4d621b13451b0f62bc5463f6474a46b43f0ad70e4d85931e1a2e1a662c13`  
		Last Modified: Fri, 02 Jun 2023 19:38:43 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a70266e0f7ce261d87f054a6dece387e39d558065144bf4379d9b1bfa7f630`  
		Last Modified: Fri, 02 Jun 2023 19:38:43 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
