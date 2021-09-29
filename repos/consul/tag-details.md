<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `consul`

-	[`consul:1.10`](#consul110)
-	[`consul:1.10.3`](#consul1103)
-	[`consul:1.8`](#consul18)
-	[`consul:1.8.16`](#consul1816)
-	[`consul:1.9`](#consul19)
-	[`consul:1.9.10`](#consul1910)
-	[`consul:latest`](#consullatest)

## `consul:1.10`

```console
$ docker pull consul@sha256:663a30db7e1f86af14c9084dd63920043e506f8cc3e15dc58abe393f95a4d449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.10` - linux; amd64

```console
$ docker pull consul@sha256:2c69d8bee4e99c083f0930bc09cdd45b88365ae6b427221283502230ba1c1ed5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43219430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74a0a01afc431799adac9d7911b8e0d6961a3b9909380ec61af211e342f7a97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:13:55 GMT
ARG CONSUL_VERSION=1.10.2
# Wed, 01 Sep 2021 00:13:56 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 01 Sep 2021 00:13:56 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 01 Sep 2021 00:13:57 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 01 Sep 2021 00:14:15 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 01 Sep 2021 00:14:17 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 01 Sep 2021 00:14:19 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:14:19 GMT
VOLUME [/consul/data]
# Wed, 01 Sep 2021 00:14:20 GMT
EXPOSE 8300
# Wed, 01 Sep 2021 00:14:20 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 01 Sep 2021 00:14:21 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 01 Sep 2021 00:14:21 GMT
COPY file:f4999c9300ae549cb312108a9d1a23840829249bac4cd51e46d8466cfee3a6a1 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 01 Sep 2021 00:14:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 00:14:22 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6085f992def430ed8f2556f38262c7a72f4b73b90938c7b10d23ee8948153f50`  
		Last Modified: Wed, 01 Sep 2021 00:15:39 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e185403d62712206d4d670a6dc1e9343046bcc9d308944262faeb165ab68a3`  
		Last Modified: Wed, 01 Sep 2021 00:15:47 GMT  
		Size: 40.4 MB (40402053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52efdf2644d28f50e4d3a9beec818e4edd8d3af82a0b5154e335b0278e6da441`  
		Last Modified: Wed, 01 Sep 2021 00:15:39 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585a8413c32a8e922dbaba4d4e1028376cf9f171f84083e0bdf28e5921f37486`  
		Last Modified: Wed, 01 Sep 2021 00:15:39 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76b82ffb99af04063532bb252dc67c726dc483d2b709022906503c446ab3725`  
		Last Modified: Wed, 01 Sep 2021 00:15:39 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10` - linux; arm variant v6

```console
$ docker pull consul@sha256:ec8833a883ccf61695c9e118f2561cc812ce6081de1c5d6ca99ac64eca263313
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39258860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302051b3bba1f7ac9355a831077280d848dac2c45e05aa37961ff4b352e617e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 22:30:33 GMT
ADD file:ed2b5e0fbd1e7ae37ab8f808c827d23c6841ce1edd7427552d5bf741d67ebcc0 in / 
# Tue, 31 Aug 2021 22:30:33 GMT
CMD ["/bin/sh"]
# Tue, 28 Sep 2021 22:49:33 GMT
ARG CONSUL_VERSION=1.10.3
# Tue, 28 Sep 2021 22:49:33 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 28 Sep 2021 22:49:34 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 28 Sep 2021 22:49:35 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 28 Sep 2021 22:49:56 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 28 Sep 2021 22:49:58 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 28 Sep 2021 22:49:59 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 28 Sep 2021 22:50:00 GMT
VOLUME [/consul/data]
# Tue, 28 Sep 2021 22:50:00 GMT
EXPOSE 8300
# Tue, 28 Sep 2021 22:50:01 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 28 Sep 2021 22:50:01 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 28 Sep 2021 22:50:02 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 28 Sep 2021 22:50:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Sep 2021 22:50:03 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:840d18d84f6afdc3231d126fdd3f84f23f0335b61cbfa9cb8808b888a4308919`  
		Last Modified: Tue, 31 Aug 2021 22:32:11 GMT  
		Size: 2.6 MB (2623761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da7cefa00df6ff78bfc7540608f8d14649f5d72fdb973673d3aa7e9bde2b2c9`  
		Last Modified: Tue, 28 Sep 2021 22:52:12 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f4e2def815a282bc7d6b5f58239973151625a75cff173cc6848adcef176428`  
		Last Modified: Tue, 28 Sep 2021 22:52:31 GMT  
		Size: 36.6 MB (36631725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a0535cc4b7bf1cc2a78c3f39aafed9e8069d5682717d91d22108f7afc66287`  
		Last Modified: Tue, 28 Sep 2021 22:52:12 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c0e7873b44e40365bbd3553506da5bc0670e4d37b1f417cba61a267f73e7ce`  
		Last Modified: Tue, 28 Sep 2021 22:52:12 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98806548710feafb3559dbdf485a8df1f51e44d8c3f54f4d624e6043223a070b`  
		Last Modified: Tue, 28 Sep 2021 22:52:12 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:f26011f45780401726505a90ed523341d6ceb7de95829bf5765138446d4bc479
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39190748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3f3b5ddf0a993047c2c8d87b49b8df0d82de8f6cf33dbf39aafa1ad02d8b7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 01 Sep 2021 02:50:45 GMT
ADD file:924de68748d5d710724ceb45b3bff9d38eedcad50d5744be4ce74f8f731a791f in / 
# Wed, 01 Sep 2021 02:50:45 GMT
CMD ["/bin/sh"]
# Wed, 29 Sep 2021 09:25:25 GMT
ARG CONSUL_VERSION=1.10.3
# Wed, 29 Sep 2021 09:25:25 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 29 Sep 2021 09:25:26 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 29 Sep 2021 09:25:26 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 29 Sep 2021 09:25:39 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 29 Sep 2021 09:25:40 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 29 Sep 2021 09:25:40 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 29 Sep 2021 09:25:41 GMT
VOLUME [/consul/data]
# Wed, 29 Sep 2021 09:25:41 GMT
EXPOSE 8300
# Wed, 29 Sep 2021 09:25:41 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 29 Sep 2021 09:25:41 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 29 Sep 2021 09:25:41 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 29 Sep 2021 09:25:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Sep 2021 09:25:42 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bbf911997326f5b56d515142e8dbdbe01d2f308276938ddbce3ab347584ed8ce`  
		Last Modified: Wed, 01 Sep 2021 02:51:37 GMT  
		Size: 2.7 MB (2713008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7783ed468dcd3af389a95cb4561f34aa40f0a042a9717bbc5a9bf47e24d165`  
		Last Modified: Wed, 29 Sep 2021 09:26:40 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20243290e6e7c34c15347c4f6a6dce80878be453180fbf74b073348a112630a2`  
		Last Modified: Wed, 29 Sep 2021 09:26:45 GMT  
		Size: 36.5 MB (36474369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed7ba7a17cd3cfc998e4594eee0c262c5a74c721ce4026c324e67232e540f4a`  
		Last Modified: Wed, 29 Sep 2021 09:26:40 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a5e393b66dcac25e0327d50cae70457a1b32e7476937f091dcdc9c768874a60`  
		Last Modified: Wed, 29 Sep 2021 09:26:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87becd5aa787811856a60855445d8a871d5bf2f10fb5c08ad68c06bda0c1cdd4`  
		Last Modified: Wed, 29 Sep 2021 09:26:40 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10` - linux; 386

```console
$ docker pull consul@sha256:810147172165d1861193f87a55583023f135919737afcc5ddad863e448c7395f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42615890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4e310ee1a1fa6e171ce608cf2476764a1e654e5a0a8c85c970b52e9e908929`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 21:23:28 GMT
ADD file:fb9d541cffc3a5660d23426ba847aa696b59a9d7f14e00ba0a63b28c9ec272c0 in / 
# Tue, 31 Aug 2021 21:23:29 GMT
CMD ["/bin/sh"]
# Wed, 29 Sep 2021 06:43:31 GMT
ARG CONSUL_VERSION=1.10.3
# Wed, 29 Sep 2021 06:43:32 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 29 Sep 2021 06:43:32 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 29 Sep 2021 06:43:33 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 29 Sep 2021 06:43:49 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 29 Sep 2021 06:43:50 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 29 Sep 2021 06:43:51 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 29 Sep 2021 06:43:51 GMT
VOLUME [/consul/data]
# Wed, 29 Sep 2021 06:43:52 GMT
EXPOSE 8300
# Wed, 29 Sep 2021 06:43:52 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 29 Sep 2021 06:43:52 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 29 Sep 2021 06:43:52 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 29 Sep 2021 06:43:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Sep 2021 06:43:53 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4ed7d06bd90bc8d13b87220ccc6204a7d235ec943be9fb4289d856f9ff0a5b7b`  
		Last Modified: Tue, 31 Aug 2021 21:24:28 GMT  
		Size: 2.8 MB (2821095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13f0394e9f2305788f6bafd0975a6a2e3c43418e6809e2ff439872aca4d09da`  
		Last Modified: Wed, 29 Sep 2021 06:45:06 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f971848c51ab8cf8b89d1b92921f705f9a5a545155a698680d858e779047481`  
		Last Modified: Wed, 29 Sep 2021 06:45:12 GMT  
		Size: 39.8 MB (39791423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e73d59ac52bd93d9f63af1624940f851d392f5df22973301a63d1d813fb25f3`  
		Last Modified: Wed, 29 Sep 2021 06:45:06 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb57764966449a0e7bf852ccc6219dcb1440bb2017faf2f7982331a2d1b4933d`  
		Last Modified: Wed, 29 Sep 2021 06:45:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66c11a991a1bc7d745b856c61084aeacc8d7d1eed3dc64e79effab644d8ec91`  
		Last Modified: Wed, 29 Sep 2021 06:45:05 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.10.3`

```console
$ docker pull consul@sha256:9e59754378c32b98ce67a7e6c9d39d3e9f7424a2729815c24b76ee46c1c11a41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.10.3` - linux; arm variant v6

```console
$ docker pull consul@sha256:ec8833a883ccf61695c9e118f2561cc812ce6081de1c5d6ca99ac64eca263313
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39258860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302051b3bba1f7ac9355a831077280d848dac2c45e05aa37961ff4b352e617e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 22:30:33 GMT
ADD file:ed2b5e0fbd1e7ae37ab8f808c827d23c6841ce1edd7427552d5bf741d67ebcc0 in / 
# Tue, 31 Aug 2021 22:30:33 GMT
CMD ["/bin/sh"]
# Tue, 28 Sep 2021 22:49:33 GMT
ARG CONSUL_VERSION=1.10.3
# Tue, 28 Sep 2021 22:49:33 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 28 Sep 2021 22:49:34 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 28 Sep 2021 22:49:35 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 28 Sep 2021 22:49:56 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 28 Sep 2021 22:49:58 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 28 Sep 2021 22:49:59 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 28 Sep 2021 22:50:00 GMT
VOLUME [/consul/data]
# Tue, 28 Sep 2021 22:50:00 GMT
EXPOSE 8300
# Tue, 28 Sep 2021 22:50:01 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 28 Sep 2021 22:50:01 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 28 Sep 2021 22:50:02 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 28 Sep 2021 22:50:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Sep 2021 22:50:03 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:840d18d84f6afdc3231d126fdd3f84f23f0335b61cbfa9cb8808b888a4308919`  
		Last Modified: Tue, 31 Aug 2021 22:32:11 GMT  
		Size: 2.6 MB (2623761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da7cefa00df6ff78bfc7540608f8d14649f5d72fdb973673d3aa7e9bde2b2c9`  
		Last Modified: Tue, 28 Sep 2021 22:52:12 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f4e2def815a282bc7d6b5f58239973151625a75cff173cc6848adcef176428`  
		Last Modified: Tue, 28 Sep 2021 22:52:31 GMT  
		Size: 36.6 MB (36631725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a0535cc4b7bf1cc2a78c3f39aafed9e8069d5682717d91d22108f7afc66287`  
		Last Modified: Tue, 28 Sep 2021 22:52:12 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c0e7873b44e40365bbd3553506da5bc0670e4d37b1f417cba61a267f73e7ce`  
		Last Modified: Tue, 28 Sep 2021 22:52:12 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98806548710feafb3559dbdf485a8df1f51e44d8c3f54f4d624e6043223a070b`  
		Last Modified: Tue, 28 Sep 2021 22:52:12 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.3` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:f26011f45780401726505a90ed523341d6ceb7de95829bf5765138446d4bc479
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39190748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3f3b5ddf0a993047c2c8d87b49b8df0d82de8f6cf33dbf39aafa1ad02d8b7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 01 Sep 2021 02:50:45 GMT
ADD file:924de68748d5d710724ceb45b3bff9d38eedcad50d5744be4ce74f8f731a791f in / 
# Wed, 01 Sep 2021 02:50:45 GMT
CMD ["/bin/sh"]
# Wed, 29 Sep 2021 09:25:25 GMT
ARG CONSUL_VERSION=1.10.3
# Wed, 29 Sep 2021 09:25:25 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 29 Sep 2021 09:25:26 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 29 Sep 2021 09:25:26 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 29 Sep 2021 09:25:39 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 29 Sep 2021 09:25:40 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 29 Sep 2021 09:25:40 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 29 Sep 2021 09:25:41 GMT
VOLUME [/consul/data]
# Wed, 29 Sep 2021 09:25:41 GMT
EXPOSE 8300
# Wed, 29 Sep 2021 09:25:41 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 29 Sep 2021 09:25:41 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 29 Sep 2021 09:25:41 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 29 Sep 2021 09:25:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Sep 2021 09:25:42 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bbf911997326f5b56d515142e8dbdbe01d2f308276938ddbce3ab347584ed8ce`  
		Last Modified: Wed, 01 Sep 2021 02:51:37 GMT  
		Size: 2.7 MB (2713008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7783ed468dcd3af389a95cb4561f34aa40f0a042a9717bbc5a9bf47e24d165`  
		Last Modified: Wed, 29 Sep 2021 09:26:40 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20243290e6e7c34c15347c4f6a6dce80878be453180fbf74b073348a112630a2`  
		Last Modified: Wed, 29 Sep 2021 09:26:45 GMT  
		Size: 36.5 MB (36474369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed7ba7a17cd3cfc998e4594eee0c262c5a74c721ce4026c324e67232e540f4a`  
		Last Modified: Wed, 29 Sep 2021 09:26:40 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a5e393b66dcac25e0327d50cae70457a1b32e7476937f091dcdc9c768874a60`  
		Last Modified: Wed, 29 Sep 2021 09:26:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87becd5aa787811856a60855445d8a871d5bf2f10fb5c08ad68c06bda0c1cdd4`  
		Last Modified: Wed, 29 Sep 2021 09:26:40 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.3` - linux; 386

```console
$ docker pull consul@sha256:810147172165d1861193f87a55583023f135919737afcc5ddad863e448c7395f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42615890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4e310ee1a1fa6e171ce608cf2476764a1e654e5a0a8c85c970b52e9e908929`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 21:23:28 GMT
ADD file:fb9d541cffc3a5660d23426ba847aa696b59a9d7f14e00ba0a63b28c9ec272c0 in / 
# Tue, 31 Aug 2021 21:23:29 GMT
CMD ["/bin/sh"]
# Wed, 29 Sep 2021 06:43:31 GMT
ARG CONSUL_VERSION=1.10.3
# Wed, 29 Sep 2021 06:43:32 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 29 Sep 2021 06:43:32 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 29 Sep 2021 06:43:33 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 29 Sep 2021 06:43:49 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 29 Sep 2021 06:43:50 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 29 Sep 2021 06:43:51 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 29 Sep 2021 06:43:51 GMT
VOLUME [/consul/data]
# Wed, 29 Sep 2021 06:43:52 GMT
EXPOSE 8300
# Wed, 29 Sep 2021 06:43:52 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 29 Sep 2021 06:43:52 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 29 Sep 2021 06:43:52 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 29 Sep 2021 06:43:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Sep 2021 06:43:53 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4ed7d06bd90bc8d13b87220ccc6204a7d235ec943be9fb4289d856f9ff0a5b7b`  
		Last Modified: Tue, 31 Aug 2021 21:24:28 GMT  
		Size: 2.8 MB (2821095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13f0394e9f2305788f6bafd0975a6a2e3c43418e6809e2ff439872aca4d09da`  
		Last Modified: Wed, 29 Sep 2021 06:45:06 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f971848c51ab8cf8b89d1b92921f705f9a5a545155a698680d858e779047481`  
		Last Modified: Wed, 29 Sep 2021 06:45:12 GMT  
		Size: 39.8 MB (39791423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e73d59ac52bd93d9f63af1624940f851d392f5df22973301a63d1d813fb25f3`  
		Last Modified: Wed, 29 Sep 2021 06:45:06 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb57764966449a0e7bf852ccc6219dcb1440bb2017faf2f7982331a2d1b4933d`  
		Last Modified: Wed, 29 Sep 2021 06:45:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66c11a991a1bc7d745b856c61084aeacc8d7d1eed3dc64e79effab644d8ec91`  
		Last Modified: Wed, 29 Sep 2021 06:45:05 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.8`

```console
$ docker pull consul@sha256:1409fae8601a6e9dc3b83875aee9e1fa3018b0e41072e1d382a685c0d1b14793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.8` - linux; amd64

```console
$ docker pull consul@sha256:c0c9ec672dcf87c94bb555080b187d1e9254a60e2d9100904b0b15217f6298a7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47432770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d457d6d43b12eb65504a59bfdcd71e930c56063b7eebba1dbe5dd8c946a3b7c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:14:53 GMT
ARG CONSUL_VERSION=1.8.15
# Wed, 01 Sep 2021 00:14:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.8.15 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 01 Sep 2021 00:14:54 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 01 Sep 2021 00:14:56 GMT
# ARGS: CONSUL_VERSION=1.8.15
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 01 Sep 2021 00:15:10 GMT
# ARGS: CONSUL_VERSION=1.8.15
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 01 Sep 2021 00:15:12 GMT
# ARGS: CONSUL_VERSION=1.8.15
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 01 Sep 2021 00:15:14 GMT
# ARGS: CONSUL_VERSION=1.8.15
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:15:14 GMT
VOLUME [/consul/data]
# Wed, 01 Sep 2021 00:15:15 GMT
EXPOSE 8300
# Wed, 01 Sep 2021 00:15:15 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 01 Sep 2021 00:15:15 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 01 Sep 2021 00:15:16 GMT
COPY file:f4999c9300ae549cb312108a9d1a23840829249bac4cd51e46d8466cfee3a6a1 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 01 Sep 2021 00:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 00:15:16 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0022ca2a5ccb519cc3605c37a29ef3a45038c36c196ec86055031a29fce2240a`  
		Last Modified: Wed, 01 Sep 2021 00:16:20 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b522424ab277ad162c8bfb55a2a14da0ac041b7785afef0528193f8b8a4dcdb7`  
		Last Modified: Wed, 01 Sep 2021 00:16:28 GMT  
		Size: 44.6 MB (44615396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6252447adce3c19393d4834b6a26429bcd0e9c7eb56284a2d0a910331c9710`  
		Last Modified: Wed, 01 Sep 2021 00:16:20 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd78b1ee93bf1b3b98bf06fecbbce5615b42405d83038ce1edeb26ef09c99b77`  
		Last Modified: Wed, 01 Sep 2021 00:16:20 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31049982da237f431af58917845758512e4f3a00364a42f514a0761160498487`  
		Last Modified: Wed, 01 Sep 2021 00:16:20 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; arm variant v6

```console
$ docker pull consul@sha256:212568d44af123b93b4a51b038f451308b9c0fc422616f6f89e622ea95e03079
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42637093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a63d875876f14e61e461aff09b97c3b84485a47b1dd5e68b67b6a78d0be7fb1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 22:30:33 GMT
ADD file:ed2b5e0fbd1e7ae37ab8f808c827d23c6841ce1edd7427552d5bf741d67ebcc0 in / 
# Tue, 31 Aug 2021 22:30:33 GMT
CMD ["/bin/sh"]
# Tue, 28 Sep 2021 22:50:58 GMT
ARG CONSUL_VERSION=1.8.16
# Tue, 28 Sep 2021 22:50:59 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.8.16 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 28 Sep 2021 22:50:59 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 28 Sep 2021 22:51:02 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 28 Sep 2021 22:51:17 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 28 Sep 2021 22:51:20 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 28 Sep 2021 22:51:23 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 28 Sep 2021 22:51:23 GMT
VOLUME [/consul/data]
# Tue, 28 Sep 2021 22:51:24 GMT
EXPOSE 8300
# Tue, 28 Sep 2021 22:51:24 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 28 Sep 2021 22:51:25 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 28 Sep 2021 22:51:25 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 28 Sep 2021 22:51:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Sep 2021 22:51:26 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:840d18d84f6afdc3231d126fdd3f84f23f0335b61cbfa9cb8808b888a4308919`  
		Last Modified: Tue, 31 Aug 2021 22:32:11 GMT  
		Size: 2.6 MB (2623761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552b65dc67d0c2d8f24041d8539eee777260120a3e7c81b5e24fe47ff3fd326d`  
		Last Modified: Tue, 28 Sep 2021 22:53:20 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d423dcfd9ab7587eb44dd25933fbd105b64a0ddc9673b2f4bcd73fa45ba36d45`  
		Last Modified: Tue, 28 Sep 2021 22:53:41 GMT  
		Size: 40.0 MB (40009963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f59d958324ee13e57568f5c5e887cb7dccac273caecccd1566b539ac8ae15b`  
		Last Modified: Tue, 28 Sep 2021 22:53:20 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6054beb8b485f747924f5b732cd51cb43cb00786d6e4abbc8e0ce83dccfe5b0`  
		Last Modified: Tue, 28 Sep 2021 22:53:20 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89cf0b300b3ec50d1edc3293a8c73f098643e87d5f2a04a7dd2296e828c24d0`  
		Last Modified: Tue, 28 Sep 2021 22:53:21 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:529564821198411427f2021158ad0e53d92e34a0138576b12fc181fde2375533
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42833423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d6dddb9334f3557594c5b70ce6b690cdef9b415a90248e986c8a8784fda7b2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 01 Sep 2021 02:50:45 GMT
ADD file:924de68748d5d710724ceb45b3bff9d38eedcad50d5744be4ce74f8f731a791f in / 
# Wed, 01 Sep 2021 02:50:45 GMT
CMD ["/bin/sh"]
# Wed, 29 Sep 2021 09:26:06 GMT
ARG CONSUL_VERSION=1.8.16
# Wed, 29 Sep 2021 09:26:06 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.8.16 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 29 Sep 2021 09:26:06 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 29 Sep 2021 09:26:07 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 29 Sep 2021 09:26:13 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 29 Sep 2021 09:26:14 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 29 Sep 2021 09:26:14 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 29 Sep 2021 09:26:14 GMT
VOLUME [/consul/data]
# Wed, 29 Sep 2021 09:26:15 GMT
EXPOSE 8300
# Wed, 29 Sep 2021 09:26:15 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 29 Sep 2021 09:26:15 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 29 Sep 2021 09:26:15 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 29 Sep 2021 09:26:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Sep 2021 09:26:16 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bbf911997326f5b56d515142e8dbdbe01d2f308276938ddbce3ab347584ed8ce`  
		Last Modified: Wed, 01 Sep 2021 02:51:37 GMT  
		Size: 2.7 MB (2713008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8be4d8b0b26e9c9d69b3075877351167c569ee4c0f0bd8f7972c646bde1f547`  
		Last Modified: Wed, 29 Sep 2021 09:27:16 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32b83d407723111df0341446ad6dcb288ebf148cb47bb4ae80186a456e99380`  
		Last Modified: Wed, 29 Sep 2021 09:27:22 GMT  
		Size: 40.1 MB (40117042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548497ba9971a3beeb7983b8157032b84a621ef621f31ff0365fe135c5f2faf0`  
		Last Modified: Wed, 29 Sep 2021 09:27:16 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba1a017efcb78fcacc63a0da6e07be641694d3ff070448ad4a53b64e5b800e0`  
		Last Modified: Wed, 29 Sep 2021 09:27:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7800e2bd817ecb866f932a878f74661dedc035c52bb3e13a281c3b32ac4e9877`  
		Last Modified: Wed, 29 Sep 2021 09:27:16 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; 386

```console
$ docker pull consul@sha256:361c717924df5cd6632cb07dd54f3d4f7082637e85509433dfeb069a09054d60
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (46989208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e43b746d063c56f847d7d3c5f48fdcc20e3ba16e7d24333f49ab14c6a0552b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 21:23:28 GMT
ADD file:fb9d541cffc3a5660d23426ba847aa696b59a9d7f14e00ba0a63b28c9ec272c0 in / 
# Tue, 31 Aug 2021 21:23:29 GMT
CMD ["/bin/sh"]
# Wed, 29 Sep 2021 06:44:21 GMT
ARG CONSUL_VERSION=1.8.16
# Wed, 29 Sep 2021 06:44:22 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.8.16 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 29 Sep 2021 06:44:22 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 29 Sep 2021 06:44:23 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 29 Sep 2021 06:44:36 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 29 Sep 2021 06:44:37 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 29 Sep 2021 06:44:38 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 29 Sep 2021 06:44:38 GMT
VOLUME [/consul/data]
# Wed, 29 Sep 2021 06:44:38 GMT
EXPOSE 8300
# Wed, 29 Sep 2021 06:44:39 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 29 Sep 2021 06:44:39 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 29 Sep 2021 06:44:39 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 29 Sep 2021 06:44:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Sep 2021 06:44:40 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4ed7d06bd90bc8d13b87220ccc6204a7d235ec943be9fb4289d856f9ff0a5b7b`  
		Last Modified: Tue, 31 Aug 2021 21:24:28 GMT  
		Size: 2.8 MB (2821095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436e3116e857618df66c0ce22a2efded7fb820518882b8faf212ded43aab2ce3`  
		Last Modified: Wed, 29 Sep 2021 06:45:48 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e03f97f7c9b7cc0be55215c447246aca11123569a9e1c83f32f698f9a7df8e5`  
		Last Modified: Wed, 29 Sep 2021 06:45:55 GMT  
		Size: 44.2 MB (44164743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2fe6a8d58e6b8945124e83780b4e355be4faeb4f36802f5a3be15f82d075868`  
		Last Modified: Wed, 29 Sep 2021 06:45:48 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9007abe05f8fe4fd9b551b01e15fc0582ac06f53d9cb7f9f545620b714cf04a5`  
		Last Modified: Wed, 29 Sep 2021 06:45:48 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b411f00b4262e1b8bb8f2e9fab570842d04059220a743e554ba7380a15c53e0`  
		Last Modified: Wed, 29 Sep 2021 06:45:48 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.8.16`

```console
$ docker pull consul@sha256:b8a1f9d192509a2b74b00efecbb03b4e684e3a083099db51bb8d49e9342c0b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.8.16` - linux; arm variant v6

```console
$ docker pull consul@sha256:212568d44af123b93b4a51b038f451308b9c0fc422616f6f89e622ea95e03079
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42637093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a63d875876f14e61e461aff09b97c3b84485a47b1dd5e68b67b6a78d0be7fb1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 22:30:33 GMT
ADD file:ed2b5e0fbd1e7ae37ab8f808c827d23c6841ce1edd7427552d5bf741d67ebcc0 in / 
# Tue, 31 Aug 2021 22:30:33 GMT
CMD ["/bin/sh"]
# Tue, 28 Sep 2021 22:50:58 GMT
ARG CONSUL_VERSION=1.8.16
# Tue, 28 Sep 2021 22:50:59 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.8.16 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 28 Sep 2021 22:50:59 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 28 Sep 2021 22:51:02 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 28 Sep 2021 22:51:17 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 28 Sep 2021 22:51:20 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 28 Sep 2021 22:51:23 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 28 Sep 2021 22:51:23 GMT
VOLUME [/consul/data]
# Tue, 28 Sep 2021 22:51:24 GMT
EXPOSE 8300
# Tue, 28 Sep 2021 22:51:24 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 28 Sep 2021 22:51:25 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 28 Sep 2021 22:51:25 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 28 Sep 2021 22:51:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Sep 2021 22:51:26 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:840d18d84f6afdc3231d126fdd3f84f23f0335b61cbfa9cb8808b888a4308919`  
		Last Modified: Tue, 31 Aug 2021 22:32:11 GMT  
		Size: 2.6 MB (2623761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552b65dc67d0c2d8f24041d8539eee777260120a3e7c81b5e24fe47ff3fd326d`  
		Last Modified: Tue, 28 Sep 2021 22:53:20 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d423dcfd9ab7587eb44dd25933fbd105b64a0ddc9673b2f4bcd73fa45ba36d45`  
		Last Modified: Tue, 28 Sep 2021 22:53:41 GMT  
		Size: 40.0 MB (40009963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f59d958324ee13e57568f5c5e887cb7dccac273caecccd1566b539ac8ae15b`  
		Last Modified: Tue, 28 Sep 2021 22:53:20 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6054beb8b485f747924f5b732cd51cb43cb00786d6e4abbc8e0ce83dccfe5b0`  
		Last Modified: Tue, 28 Sep 2021 22:53:20 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89cf0b300b3ec50d1edc3293a8c73f098643e87d5f2a04a7dd2296e828c24d0`  
		Last Modified: Tue, 28 Sep 2021 22:53:21 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.16` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:529564821198411427f2021158ad0e53d92e34a0138576b12fc181fde2375533
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42833423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d6dddb9334f3557594c5b70ce6b690cdef9b415a90248e986c8a8784fda7b2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 01 Sep 2021 02:50:45 GMT
ADD file:924de68748d5d710724ceb45b3bff9d38eedcad50d5744be4ce74f8f731a791f in / 
# Wed, 01 Sep 2021 02:50:45 GMT
CMD ["/bin/sh"]
# Wed, 29 Sep 2021 09:26:06 GMT
ARG CONSUL_VERSION=1.8.16
# Wed, 29 Sep 2021 09:26:06 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.8.16 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 29 Sep 2021 09:26:06 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 29 Sep 2021 09:26:07 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 29 Sep 2021 09:26:13 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 29 Sep 2021 09:26:14 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 29 Sep 2021 09:26:14 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 29 Sep 2021 09:26:14 GMT
VOLUME [/consul/data]
# Wed, 29 Sep 2021 09:26:15 GMT
EXPOSE 8300
# Wed, 29 Sep 2021 09:26:15 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 29 Sep 2021 09:26:15 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 29 Sep 2021 09:26:15 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 29 Sep 2021 09:26:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Sep 2021 09:26:16 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bbf911997326f5b56d515142e8dbdbe01d2f308276938ddbce3ab347584ed8ce`  
		Last Modified: Wed, 01 Sep 2021 02:51:37 GMT  
		Size: 2.7 MB (2713008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8be4d8b0b26e9c9d69b3075877351167c569ee4c0f0bd8f7972c646bde1f547`  
		Last Modified: Wed, 29 Sep 2021 09:27:16 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32b83d407723111df0341446ad6dcb288ebf148cb47bb4ae80186a456e99380`  
		Last Modified: Wed, 29 Sep 2021 09:27:22 GMT  
		Size: 40.1 MB (40117042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548497ba9971a3beeb7983b8157032b84a621ef621f31ff0365fe135c5f2faf0`  
		Last Modified: Wed, 29 Sep 2021 09:27:16 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba1a017efcb78fcacc63a0da6e07be641694d3ff070448ad4a53b64e5b800e0`  
		Last Modified: Wed, 29 Sep 2021 09:27:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7800e2bd817ecb866f932a878f74661dedc035c52bb3e13a281c3b32ac4e9877`  
		Last Modified: Wed, 29 Sep 2021 09:27:16 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.16` - linux; 386

```console
$ docker pull consul@sha256:361c717924df5cd6632cb07dd54f3d4f7082637e85509433dfeb069a09054d60
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (46989208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e43b746d063c56f847d7d3c5f48fdcc20e3ba16e7d24333f49ab14c6a0552b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 21:23:28 GMT
ADD file:fb9d541cffc3a5660d23426ba847aa696b59a9d7f14e00ba0a63b28c9ec272c0 in / 
# Tue, 31 Aug 2021 21:23:29 GMT
CMD ["/bin/sh"]
# Wed, 29 Sep 2021 06:44:21 GMT
ARG CONSUL_VERSION=1.8.16
# Wed, 29 Sep 2021 06:44:22 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.8.16 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 29 Sep 2021 06:44:22 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 29 Sep 2021 06:44:23 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 29 Sep 2021 06:44:36 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 29 Sep 2021 06:44:37 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 29 Sep 2021 06:44:38 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 29 Sep 2021 06:44:38 GMT
VOLUME [/consul/data]
# Wed, 29 Sep 2021 06:44:38 GMT
EXPOSE 8300
# Wed, 29 Sep 2021 06:44:39 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 29 Sep 2021 06:44:39 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 29 Sep 2021 06:44:39 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 29 Sep 2021 06:44:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Sep 2021 06:44:40 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4ed7d06bd90bc8d13b87220ccc6204a7d235ec943be9fb4289d856f9ff0a5b7b`  
		Last Modified: Tue, 31 Aug 2021 21:24:28 GMT  
		Size: 2.8 MB (2821095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436e3116e857618df66c0ce22a2efded7fb820518882b8faf212ded43aab2ce3`  
		Last Modified: Wed, 29 Sep 2021 06:45:48 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e03f97f7c9b7cc0be55215c447246aca11123569a9e1c83f32f698f9a7df8e5`  
		Last Modified: Wed, 29 Sep 2021 06:45:55 GMT  
		Size: 44.2 MB (44164743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2fe6a8d58e6b8945124e83780b4e355be4faeb4f36802f5a3be15f82d075868`  
		Last Modified: Wed, 29 Sep 2021 06:45:48 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9007abe05f8fe4fd9b551b01e15fc0582ac06f53d9cb7f9f545620b714cf04a5`  
		Last Modified: Wed, 29 Sep 2021 06:45:48 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b411f00b4262e1b8bb8f2e9fab570842d04059220a743e554ba7380a15c53e0`  
		Last Modified: Wed, 29 Sep 2021 06:45:48 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9`

```console
$ docker pull consul@sha256:46d94ef87fcdd424dc66db35fca974e3de11cbd4cef63ae163fcfe1fb55ab99d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.9` - linux; amd64

```console
$ docker pull consul@sha256:d08355ef1555bb782d486bc903bf75d397a32ed38f16d033b1e1cc28392b702e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45890066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f5d27f4606766adacd7db1f010bc5f056b9411c6285d981c2122cf143a6696`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:14:27 GMT
ARG CONSUL_VERSION=1.9.9
# Wed, 01 Sep 2021 00:14:27 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 01 Sep 2021 00:14:28 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 01 Sep 2021 00:14:30 GMT
# ARGS: CONSUL_VERSION=1.9.9
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 01 Sep 2021 00:14:42 GMT
# ARGS: CONSUL_VERSION=1.9.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 01 Sep 2021 00:14:43 GMT
# ARGS: CONSUL_VERSION=1.9.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 01 Sep 2021 00:14:44 GMT
# ARGS: CONSUL_VERSION=1.9.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:14:45 GMT
VOLUME [/consul/data]
# Wed, 01 Sep 2021 00:14:45 GMT
EXPOSE 8300
# Wed, 01 Sep 2021 00:14:46 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 01 Sep 2021 00:14:46 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 01 Sep 2021 00:14:46 GMT
COPY file:f4999c9300ae549cb312108a9d1a23840829249bac4cd51e46d8466cfee3a6a1 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 01 Sep 2021 00:14:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 00:14:47 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1002deffc8d522ac27816e38f624fb99eb60e144f5ddae64c1db963f9f1f71c5`  
		Last Modified: Wed, 01 Sep 2021 00:16:01 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585556722091a5853a673738ea0566385bddf805ae5d39b3ed5d875b1886bb8a`  
		Last Modified: Wed, 01 Sep 2021 00:16:10 GMT  
		Size: 43.1 MB (43072684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4118856830e8594ee52c9ce8f3c1a8130af6b714e1ea7d33eed9399a313ace`  
		Last Modified: Wed, 01 Sep 2021 00:16:01 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76ee2bdeec48e7dbda3f1f9e1ccd0decaa72db4e54b2de9563763e3ec68be6d`  
		Last Modified: Wed, 01 Sep 2021 00:16:02 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b0d9dcde6a01972e13fc192727e0831d3b9ecd74412e8b9df5bc22baaf84a0`  
		Last Modified: Wed, 01 Sep 2021 00:16:02 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; arm variant v6

```console
$ docker pull consul@sha256:91dfa900b195c54464c486e9529a1f316fc10253345f201cbdeb28a5a161754d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41080020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b50e96235aa66d0be636b7fca50e46fd18f82d8f16bf8528b5c170d6e731c745`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 22:30:33 GMT
ADD file:ed2b5e0fbd1e7ae37ab8f808c827d23c6841ce1edd7427552d5bf741d67ebcc0 in / 
# Tue, 31 Aug 2021 22:30:33 GMT
CMD ["/bin/sh"]
# Tue, 28 Sep 2021 22:50:15 GMT
ARG CONSUL_VERSION=1.9.10
# Tue, 28 Sep 2021 22:50:16 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.10 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 28 Sep 2021 22:50:17 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 28 Sep 2021 22:50:20 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 28 Sep 2021 22:50:35 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 28 Sep 2021 22:50:38 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 28 Sep 2021 22:50:41 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 28 Sep 2021 22:50:42 GMT
VOLUME [/consul/data]
# Tue, 28 Sep 2021 22:50:43 GMT
EXPOSE 8300
# Tue, 28 Sep 2021 22:50:44 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 28 Sep 2021 22:50:44 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 28 Sep 2021 22:50:45 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 28 Sep 2021 22:50:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Sep 2021 22:50:47 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:840d18d84f6afdc3231d126fdd3f84f23f0335b61cbfa9cb8808b888a4308919`  
		Last Modified: Tue, 31 Aug 2021 22:32:11 GMT  
		Size: 2.6 MB (2623761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca0e30d54b8381f34b7a1e6b27a5cf266a93c3003d4dd958e200a78935acebb`  
		Last Modified: Tue, 28 Sep 2021 22:52:47 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3194cce0709f6da752b841103f390ba550b8527cc8934bd28ef97e589252cbe`  
		Last Modified: Tue, 28 Sep 2021 22:53:08 GMT  
		Size: 38.5 MB (38452887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5308cdfcf6a5e99774de613127df969d670dbd6549fca35ea17ea6a3ca83cee`  
		Last Modified: Tue, 28 Sep 2021 22:52:47 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5921b2b8c69f70330fc2993534bcb33a52f8de510dcd25e2041acf4da30b408f`  
		Last Modified: Tue, 28 Sep 2021 22:52:47 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ebe4aeae5d3513eb375ac5c50b58ef8e6d4cb3541dc3ccb75472eb903bb1297`  
		Last Modified: Tue, 28 Sep 2021 22:52:47 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:b7c01fceabc1baa63493414aa461473871dc210507917e69bd68b8eab56cbeb4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41340124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e10829891c63c8f232703dd5432b467c68a6282461f53e1c47515388b957d99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 01 Sep 2021 02:50:45 GMT
ADD file:924de68748d5d710724ceb45b3bff9d38eedcad50d5744be4ce74f8f731a791f in / 
# Wed, 01 Sep 2021 02:50:45 GMT
CMD ["/bin/sh"]
# Wed, 29 Sep 2021 09:25:48 GMT
ARG CONSUL_VERSION=1.9.10
# Wed, 29 Sep 2021 09:25:48 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.10 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 29 Sep 2021 09:25:48 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 29 Sep 2021 09:25:49 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 29 Sep 2021 09:25:58 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 29 Sep 2021 09:25:58 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 29 Sep 2021 09:25:59 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 29 Sep 2021 09:25:59 GMT
VOLUME [/consul/data]
# Wed, 29 Sep 2021 09:25:59 GMT
EXPOSE 8300
# Wed, 29 Sep 2021 09:26:00 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 29 Sep 2021 09:26:00 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 29 Sep 2021 09:26:00 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 29 Sep 2021 09:26:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Sep 2021 09:26:00 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bbf911997326f5b56d515142e8dbdbe01d2f308276938ddbce3ab347584ed8ce`  
		Last Modified: Wed, 01 Sep 2021 02:51:37 GMT  
		Size: 2.7 MB (2713008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56df6a7bcb6b62a854962afb1d8e9a7ebffe7545d89f5d6d6375551429c035a1`  
		Last Modified: Wed, 29 Sep 2021 09:27:00 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e616a6b837541f664ed2b86976957fdf7ca4c9a2bdbbc6fab316278b78a1b5d2`  
		Last Modified: Wed, 29 Sep 2021 09:27:05 GMT  
		Size: 38.6 MB (38623746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2540bf63b645a0daa7e39c1cacd7370c8b5b6f86b9402356f7ba8214f53ad1e7`  
		Last Modified: Wed, 29 Sep 2021 09:26:59 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50b1723e235cc11348ba89262f1b06c08c470355e54f4b7bcb31aac5d977a6e`  
		Last Modified: Wed, 29 Sep 2021 09:26:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347034c3f964d941e9079e758325c995832b6ad70a592b743fef185bb0bc7f64`  
		Last Modified: Wed, 29 Sep 2021 09:27:00 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; 386

```console
$ docker pull consul@sha256:22ce0571ccf36151c98b515af2f14c04029ef1d6954769dc85609731d3b47d8c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45271915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ec8d54ddc9278a2fef971dd094f71aa4e7c6300873019baabb2acc50bfe790`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 21:23:28 GMT
ADD file:fb9d541cffc3a5660d23426ba847aa696b59a9d7f14e00ba0a63b28c9ec272c0 in / 
# Tue, 31 Aug 2021 21:23:29 GMT
CMD ["/bin/sh"]
# Wed, 29 Sep 2021 06:43:59 GMT
ARG CONSUL_VERSION=1.9.10
# Wed, 29 Sep 2021 06:43:59 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.10 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 29 Sep 2021 06:43:59 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 29 Sep 2021 06:44:00 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 29 Sep 2021 06:44:12 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 29 Sep 2021 06:44:13 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 29 Sep 2021 06:44:14 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 29 Sep 2021 06:44:14 GMT
VOLUME [/consul/data]
# Wed, 29 Sep 2021 06:44:15 GMT
EXPOSE 8300
# Wed, 29 Sep 2021 06:44:15 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 29 Sep 2021 06:44:15 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 29 Sep 2021 06:44:15 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 29 Sep 2021 06:44:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Sep 2021 06:44:16 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4ed7d06bd90bc8d13b87220ccc6204a7d235ec943be9fb4289d856f9ff0a5b7b`  
		Last Modified: Tue, 31 Aug 2021 21:24:28 GMT  
		Size: 2.8 MB (2821095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101feacb8d52e7d34b0e0c701153e86a1ef24c60762496369dcf0c2597fb8f4f`  
		Last Modified: Wed, 29 Sep 2021 06:45:30 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad94defe75eac084f6836520a04b8aab302d914ad90488973dfc06b9746e202`  
		Last Modified: Wed, 29 Sep 2021 06:45:37 GMT  
		Size: 42.4 MB (42447446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daf12315d1950ac09ece349c87003bf6efe9ec66ecb43ba040768740ed5f969`  
		Last Modified: Wed, 29 Sep 2021 06:45:30 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9ebbdb289f021c8e22969bb3f1a02123c544704aafba5de7f4e373b61a2fe4`  
		Last Modified: Wed, 29 Sep 2021 06:45:30 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c16e0641d298f627a32f6abf782dabc6fd5454b33a25c22049846f7a51fdaebe`  
		Last Modified: Wed, 29 Sep 2021 06:45:31 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9.10`

```console
$ docker pull consul@sha256:dc0b0fdcc754bb303febddf80defa6ab7808b57cd96562feb0ec76bb899ce58d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.9.10` - linux; arm variant v6

```console
$ docker pull consul@sha256:91dfa900b195c54464c486e9529a1f316fc10253345f201cbdeb28a5a161754d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41080020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b50e96235aa66d0be636b7fca50e46fd18f82d8f16bf8528b5c170d6e731c745`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 22:30:33 GMT
ADD file:ed2b5e0fbd1e7ae37ab8f808c827d23c6841ce1edd7427552d5bf741d67ebcc0 in / 
# Tue, 31 Aug 2021 22:30:33 GMT
CMD ["/bin/sh"]
# Tue, 28 Sep 2021 22:50:15 GMT
ARG CONSUL_VERSION=1.9.10
# Tue, 28 Sep 2021 22:50:16 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.10 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 28 Sep 2021 22:50:17 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 28 Sep 2021 22:50:20 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 28 Sep 2021 22:50:35 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 28 Sep 2021 22:50:38 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 28 Sep 2021 22:50:41 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 28 Sep 2021 22:50:42 GMT
VOLUME [/consul/data]
# Tue, 28 Sep 2021 22:50:43 GMT
EXPOSE 8300
# Tue, 28 Sep 2021 22:50:44 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 28 Sep 2021 22:50:44 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 28 Sep 2021 22:50:45 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 28 Sep 2021 22:50:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Sep 2021 22:50:47 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:840d18d84f6afdc3231d126fdd3f84f23f0335b61cbfa9cb8808b888a4308919`  
		Last Modified: Tue, 31 Aug 2021 22:32:11 GMT  
		Size: 2.6 MB (2623761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca0e30d54b8381f34b7a1e6b27a5cf266a93c3003d4dd958e200a78935acebb`  
		Last Modified: Tue, 28 Sep 2021 22:52:47 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3194cce0709f6da752b841103f390ba550b8527cc8934bd28ef97e589252cbe`  
		Last Modified: Tue, 28 Sep 2021 22:53:08 GMT  
		Size: 38.5 MB (38452887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5308cdfcf6a5e99774de613127df969d670dbd6549fca35ea17ea6a3ca83cee`  
		Last Modified: Tue, 28 Sep 2021 22:52:47 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5921b2b8c69f70330fc2993534bcb33a52f8de510dcd25e2041acf4da30b408f`  
		Last Modified: Tue, 28 Sep 2021 22:52:47 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ebe4aeae5d3513eb375ac5c50b58ef8e6d4cb3541dc3ccb75472eb903bb1297`  
		Last Modified: Tue, 28 Sep 2021 22:52:47 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.10` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:b7c01fceabc1baa63493414aa461473871dc210507917e69bd68b8eab56cbeb4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41340124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e10829891c63c8f232703dd5432b467c68a6282461f53e1c47515388b957d99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 01 Sep 2021 02:50:45 GMT
ADD file:924de68748d5d710724ceb45b3bff9d38eedcad50d5744be4ce74f8f731a791f in / 
# Wed, 01 Sep 2021 02:50:45 GMT
CMD ["/bin/sh"]
# Wed, 29 Sep 2021 09:25:48 GMT
ARG CONSUL_VERSION=1.9.10
# Wed, 29 Sep 2021 09:25:48 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.10 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 29 Sep 2021 09:25:48 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 29 Sep 2021 09:25:49 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 29 Sep 2021 09:25:58 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 29 Sep 2021 09:25:58 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 29 Sep 2021 09:25:59 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 29 Sep 2021 09:25:59 GMT
VOLUME [/consul/data]
# Wed, 29 Sep 2021 09:25:59 GMT
EXPOSE 8300
# Wed, 29 Sep 2021 09:26:00 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 29 Sep 2021 09:26:00 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 29 Sep 2021 09:26:00 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 29 Sep 2021 09:26:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Sep 2021 09:26:00 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bbf911997326f5b56d515142e8dbdbe01d2f308276938ddbce3ab347584ed8ce`  
		Last Modified: Wed, 01 Sep 2021 02:51:37 GMT  
		Size: 2.7 MB (2713008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56df6a7bcb6b62a854962afb1d8e9a7ebffe7545d89f5d6d6375551429c035a1`  
		Last Modified: Wed, 29 Sep 2021 09:27:00 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e616a6b837541f664ed2b86976957fdf7ca4c9a2bdbbc6fab316278b78a1b5d2`  
		Last Modified: Wed, 29 Sep 2021 09:27:05 GMT  
		Size: 38.6 MB (38623746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2540bf63b645a0daa7e39c1cacd7370c8b5b6f86b9402356f7ba8214f53ad1e7`  
		Last Modified: Wed, 29 Sep 2021 09:26:59 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50b1723e235cc11348ba89262f1b06c08c470355e54f4b7bcb31aac5d977a6e`  
		Last Modified: Wed, 29 Sep 2021 09:26:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347034c3f964d941e9079e758325c995832b6ad70a592b743fef185bb0bc7f64`  
		Last Modified: Wed, 29 Sep 2021 09:27:00 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.10` - linux; 386

```console
$ docker pull consul@sha256:22ce0571ccf36151c98b515af2f14c04029ef1d6954769dc85609731d3b47d8c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45271915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ec8d54ddc9278a2fef971dd094f71aa4e7c6300873019baabb2acc50bfe790`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 21:23:28 GMT
ADD file:fb9d541cffc3a5660d23426ba847aa696b59a9d7f14e00ba0a63b28c9ec272c0 in / 
# Tue, 31 Aug 2021 21:23:29 GMT
CMD ["/bin/sh"]
# Wed, 29 Sep 2021 06:43:59 GMT
ARG CONSUL_VERSION=1.9.10
# Wed, 29 Sep 2021 06:43:59 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.10 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 29 Sep 2021 06:43:59 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 29 Sep 2021 06:44:00 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 29 Sep 2021 06:44:12 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 29 Sep 2021 06:44:13 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 29 Sep 2021 06:44:14 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 29 Sep 2021 06:44:14 GMT
VOLUME [/consul/data]
# Wed, 29 Sep 2021 06:44:15 GMT
EXPOSE 8300
# Wed, 29 Sep 2021 06:44:15 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 29 Sep 2021 06:44:15 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 29 Sep 2021 06:44:15 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 29 Sep 2021 06:44:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Sep 2021 06:44:16 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4ed7d06bd90bc8d13b87220ccc6204a7d235ec943be9fb4289d856f9ff0a5b7b`  
		Last Modified: Tue, 31 Aug 2021 21:24:28 GMT  
		Size: 2.8 MB (2821095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101feacb8d52e7d34b0e0c701153e86a1ef24c60762496369dcf0c2597fb8f4f`  
		Last Modified: Wed, 29 Sep 2021 06:45:30 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad94defe75eac084f6836520a04b8aab302d914ad90488973dfc06b9746e202`  
		Last Modified: Wed, 29 Sep 2021 06:45:37 GMT  
		Size: 42.4 MB (42447446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daf12315d1950ac09ece349c87003bf6efe9ec66ecb43ba040768740ed5f969`  
		Last Modified: Wed, 29 Sep 2021 06:45:30 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9ebbdb289f021c8e22969bb3f1a02123c544704aafba5de7f4e373b61a2fe4`  
		Last Modified: Wed, 29 Sep 2021 06:45:30 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c16e0641d298f627a32f6abf782dabc6fd5454b33a25c22049846f7a51fdaebe`  
		Last Modified: Wed, 29 Sep 2021 06:45:31 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:latest`

```console
$ docker pull consul@sha256:663a30db7e1f86af14c9084dd63920043e506f8cc3e15dc58abe393f95a4d449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:latest` - linux; amd64

```console
$ docker pull consul@sha256:2c69d8bee4e99c083f0930bc09cdd45b88365ae6b427221283502230ba1c1ed5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43219430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74a0a01afc431799adac9d7911b8e0d6961a3b9909380ec61af211e342f7a97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:13:55 GMT
ARG CONSUL_VERSION=1.10.2
# Wed, 01 Sep 2021 00:13:56 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 01 Sep 2021 00:13:56 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 01 Sep 2021 00:13:57 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 01 Sep 2021 00:14:15 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 01 Sep 2021 00:14:17 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 01 Sep 2021 00:14:19 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:14:19 GMT
VOLUME [/consul/data]
# Wed, 01 Sep 2021 00:14:20 GMT
EXPOSE 8300
# Wed, 01 Sep 2021 00:14:20 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 01 Sep 2021 00:14:21 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 01 Sep 2021 00:14:21 GMT
COPY file:f4999c9300ae549cb312108a9d1a23840829249bac4cd51e46d8466cfee3a6a1 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 01 Sep 2021 00:14:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 00:14:22 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6085f992def430ed8f2556f38262c7a72f4b73b90938c7b10d23ee8948153f50`  
		Last Modified: Wed, 01 Sep 2021 00:15:39 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e185403d62712206d4d670a6dc1e9343046bcc9d308944262faeb165ab68a3`  
		Last Modified: Wed, 01 Sep 2021 00:15:47 GMT  
		Size: 40.4 MB (40402053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52efdf2644d28f50e4d3a9beec818e4edd8d3af82a0b5154e335b0278e6da441`  
		Last Modified: Wed, 01 Sep 2021 00:15:39 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585a8413c32a8e922dbaba4d4e1028376cf9f171f84083e0bdf28e5921f37486`  
		Last Modified: Wed, 01 Sep 2021 00:15:39 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76b82ffb99af04063532bb252dc67c726dc483d2b709022906503c446ab3725`  
		Last Modified: Wed, 01 Sep 2021 00:15:39 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm variant v6

```console
$ docker pull consul@sha256:ec8833a883ccf61695c9e118f2561cc812ce6081de1c5d6ca99ac64eca263313
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39258860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302051b3bba1f7ac9355a831077280d848dac2c45e05aa37961ff4b352e617e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 22:30:33 GMT
ADD file:ed2b5e0fbd1e7ae37ab8f808c827d23c6841ce1edd7427552d5bf741d67ebcc0 in / 
# Tue, 31 Aug 2021 22:30:33 GMT
CMD ["/bin/sh"]
# Tue, 28 Sep 2021 22:49:33 GMT
ARG CONSUL_VERSION=1.10.3
# Tue, 28 Sep 2021 22:49:33 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 28 Sep 2021 22:49:34 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 28 Sep 2021 22:49:35 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 28 Sep 2021 22:49:56 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 28 Sep 2021 22:49:58 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 28 Sep 2021 22:49:59 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 28 Sep 2021 22:50:00 GMT
VOLUME [/consul/data]
# Tue, 28 Sep 2021 22:50:00 GMT
EXPOSE 8300
# Tue, 28 Sep 2021 22:50:01 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 28 Sep 2021 22:50:01 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 28 Sep 2021 22:50:02 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 28 Sep 2021 22:50:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Sep 2021 22:50:03 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:840d18d84f6afdc3231d126fdd3f84f23f0335b61cbfa9cb8808b888a4308919`  
		Last Modified: Tue, 31 Aug 2021 22:32:11 GMT  
		Size: 2.6 MB (2623761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da7cefa00df6ff78bfc7540608f8d14649f5d72fdb973673d3aa7e9bde2b2c9`  
		Last Modified: Tue, 28 Sep 2021 22:52:12 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f4e2def815a282bc7d6b5f58239973151625a75cff173cc6848adcef176428`  
		Last Modified: Tue, 28 Sep 2021 22:52:31 GMT  
		Size: 36.6 MB (36631725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a0535cc4b7bf1cc2a78c3f39aafed9e8069d5682717d91d22108f7afc66287`  
		Last Modified: Tue, 28 Sep 2021 22:52:12 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c0e7873b44e40365bbd3553506da5bc0670e4d37b1f417cba61a267f73e7ce`  
		Last Modified: Tue, 28 Sep 2021 22:52:12 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98806548710feafb3559dbdf485a8df1f51e44d8c3f54f4d624e6043223a070b`  
		Last Modified: Tue, 28 Sep 2021 22:52:12 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:f26011f45780401726505a90ed523341d6ceb7de95829bf5765138446d4bc479
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39190748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3f3b5ddf0a993047c2c8d87b49b8df0d82de8f6cf33dbf39aafa1ad02d8b7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 01 Sep 2021 02:50:45 GMT
ADD file:924de68748d5d710724ceb45b3bff9d38eedcad50d5744be4ce74f8f731a791f in / 
# Wed, 01 Sep 2021 02:50:45 GMT
CMD ["/bin/sh"]
# Wed, 29 Sep 2021 09:25:25 GMT
ARG CONSUL_VERSION=1.10.3
# Wed, 29 Sep 2021 09:25:25 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 29 Sep 2021 09:25:26 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 29 Sep 2021 09:25:26 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 29 Sep 2021 09:25:39 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 29 Sep 2021 09:25:40 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 29 Sep 2021 09:25:40 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 29 Sep 2021 09:25:41 GMT
VOLUME [/consul/data]
# Wed, 29 Sep 2021 09:25:41 GMT
EXPOSE 8300
# Wed, 29 Sep 2021 09:25:41 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 29 Sep 2021 09:25:41 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 29 Sep 2021 09:25:41 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 29 Sep 2021 09:25:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Sep 2021 09:25:42 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bbf911997326f5b56d515142e8dbdbe01d2f308276938ddbce3ab347584ed8ce`  
		Last Modified: Wed, 01 Sep 2021 02:51:37 GMT  
		Size: 2.7 MB (2713008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7783ed468dcd3af389a95cb4561f34aa40f0a042a9717bbc5a9bf47e24d165`  
		Last Modified: Wed, 29 Sep 2021 09:26:40 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20243290e6e7c34c15347c4f6a6dce80878be453180fbf74b073348a112630a2`  
		Last Modified: Wed, 29 Sep 2021 09:26:45 GMT  
		Size: 36.5 MB (36474369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed7ba7a17cd3cfc998e4594eee0c262c5a74c721ce4026c324e67232e540f4a`  
		Last Modified: Wed, 29 Sep 2021 09:26:40 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a5e393b66dcac25e0327d50cae70457a1b32e7476937f091dcdc9c768874a60`  
		Last Modified: Wed, 29 Sep 2021 09:26:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87becd5aa787811856a60855445d8a871d5bf2f10fb5c08ad68c06bda0c1cdd4`  
		Last Modified: Wed, 29 Sep 2021 09:26:40 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; 386

```console
$ docker pull consul@sha256:810147172165d1861193f87a55583023f135919737afcc5ddad863e448c7395f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42615890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4e310ee1a1fa6e171ce608cf2476764a1e654e5a0a8c85c970b52e9e908929`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 21:23:28 GMT
ADD file:fb9d541cffc3a5660d23426ba847aa696b59a9d7f14e00ba0a63b28c9ec272c0 in / 
# Tue, 31 Aug 2021 21:23:29 GMT
CMD ["/bin/sh"]
# Wed, 29 Sep 2021 06:43:31 GMT
ARG CONSUL_VERSION=1.10.3
# Wed, 29 Sep 2021 06:43:32 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 29 Sep 2021 06:43:32 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 29 Sep 2021 06:43:33 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 29 Sep 2021 06:43:49 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 29 Sep 2021 06:43:50 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 29 Sep 2021 06:43:51 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 29 Sep 2021 06:43:51 GMT
VOLUME [/consul/data]
# Wed, 29 Sep 2021 06:43:52 GMT
EXPOSE 8300
# Wed, 29 Sep 2021 06:43:52 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 29 Sep 2021 06:43:52 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 29 Sep 2021 06:43:52 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 29 Sep 2021 06:43:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Sep 2021 06:43:53 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4ed7d06bd90bc8d13b87220ccc6204a7d235ec943be9fb4289d856f9ff0a5b7b`  
		Last Modified: Tue, 31 Aug 2021 21:24:28 GMT  
		Size: 2.8 MB (2821095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13f0394e9f2305788f6bafd0975a6a2e3c43418e6809e2ff439872aca4d09da`  
		Last Modified: Wed, 29 Sep 2021 06:45:06 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f971848c51ab8cf8b89d1b92921f705f9a5a545155a698680d858e779047481`  
		Last Modified: Wed, 29 Sep 2021 06:45:12 GMT  
		Size: 39.8 MB (39791423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e73d59ac52bd93d9f63af1624940f851d392f5df22973301a63d1d813fb25f3`  
		Last Modified: Wed, 29 Sep 2021 06:45:06 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb57764966449a0e7bf852ccc6219dcb1440bb2017faf2f7982331a2d1b4933d`  
		Last Modified: Wed, 29 Sep 2021 06:45:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66c11a991a1bc7d745b856c61084aeacc8d7d1eed3dc64e79effab644d8ec91`  
		Last Modified: Wed, 29 Sep 2021 06:45:05 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
