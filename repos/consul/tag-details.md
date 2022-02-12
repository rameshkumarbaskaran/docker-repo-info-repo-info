<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `consul`

-	[`consul:1.10`](#consul110)
-	[`consul:1.10.8`](#consul1108)
-	[`consul:1.11`](#consul111)
-	[`consul:1.11.3`](#consul1113)
-	[`consul:1.9`](#consul19)
-	[`consul:1.9.15`](#consul1915)
-	[`consul:latest`](#consullatest)

## `consul:1.10`

```console
$ docker pull consul@sha256:9dc017dc725902a21b869cff19f880e4f3396b5030d76d2ca2614e9432f441df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.10` - linux; amd64

```console
$ docker pull consul@sha256:64bb8a400463ba49f5d7df6a03bf3e24dd60c58388eb50768f5e5d218bc8cc18
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43702129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2448a121106f91690ef1735213740106070d1b2fc2a906eec6ccd18bc8b726c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:19:54 GMT
ARG CONSUL_VERSION=1.10.7
# Fri, 14 Jan 2022 18:19:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 14 Jan 2022 18:19:54 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 14 Jan 2022 18:19:55 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 14 Jan 2022 18:20:09 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 14 Jan 2022 18:20:10 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 14 Jan 2022 18:20:11 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 14 Jan 2022 18:20:11 GMT
VOLUME [/consul/data]
# Fri, 14 Jan 2022 18:20:11 GMT
EXPOSE 8300
# Fri, 14 Jan 2022 18:20:12 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 14 Jan 2022 18:20:12 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 14 Jan 2022 18:20:12 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 14 Jan 2022 18:20:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:20:12 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6386278449b4403e5f923aac925a34ffa25337b82712c40ca70b934d3676ed31`  
		Last Modified: Fri, 14 Jan 2022 18:22:23 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d494b414b865191a9d497d3835f3e50e93e6b6d6fdd86de4d63a0db9d9fe7285`  
		Last Modified: Fri, 14 Jan 2022 18:22:29 GMT  
		Size: 40.9 MB (40876330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5ac0b6f22d44c76dad4a624baed2d802668d239f7fc1776fa2722a8b040eff`  
		Last Modified: Fri, 14 Jan 2022 18:22:23 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d32c50e5a3bd7e41f92e7dd23998d0364bb09eb86577543fc2eb1f77b8250c`  
		Last Modified: Fri, 14 Jan 2022 18:22:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc85959dfa405726f5adc6a22712fa59e307977ed41311a0cfcf3cbbe200884c`  
		Last Modified: Fri, 14 Jan 2022 18:22:23 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10` - linux; arm variant v6

```console
$ docker pull consul@sha256:298ac8d6cb57014379dfeea323a4f40253234e0346bc4855db3c7f939646c918
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41767102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7146de82d58c8360314657ab9f3bb7d74aac8b75d8cc255f6965bb8eb9bdf8aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Sat, 12 Feb 2022 01:50:21 GMT
ARG CONSUL_VERSION=1.10.8
# Sat, 12 Feb 2022 01:50:21 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.8 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 12 Feb 2022 01:50:22 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 12 Feb 2022 01:50:24 GMT
# ARGS: CONSUL_VERSION=1.10.8
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 12 Feb 2022 01:50:51 GMT
# ARGS: CONSUL_VERSION=1.10.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 12 Feb 2022 01:50:52 GMT
# ARGS: CONSUL_VERSION=1.10.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 12 Feb 2022 01:50:54 GMT
# ARGS: CONSUL_VERSION=1.10.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 12 Feb 2022 01:50:55 GMT
VOLUME [/consul/data]
# Sat, 12 Feb 2022 01:50:55 GMT
EXPOSE 8300
# Sat, 12 Feb 2022 01:50:56 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 12 Feb 2022 01:50:56 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 12 Feb 2022 01:50:56 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 12 Feb 2022 01:50:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Feb 2022 01:50:57 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6433b6bf5bed8b3be159441dfeb9712971674bac4560ce7f8a4eff5ce13a7565`  
		Last Modified: Sat, 12 Feb 2022 01:53:02 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878f28cb8b52e741264e9f23c9e4b5591c3d645ad1f067025f9dd4d593c75def`  
		Last Modified: Sat, 12 Feb 2022 01:53:24 GMT  
		Size: 39.1 MB (39130384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a653e69a81e17e79e5c5c36302da1cfa43006b3728d594d6d7e7c2fb4858d2`  
		Last Modified: Sat, 12 Feb 2022 01:53:03 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9424e86dc77f20fb6ec25edf6c8122ceead8b081ec1f0da24ef376da60e31f`  
		Last Modified: Sat, 12 Feb 2022 01:53:02 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6919833dce23fe2753532ef08cc421715f317809ba4e185fbc8811c8fa7c3a`  
		Last Modified: Sat, 12 Feb 2022 01:53:02 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:cd5ec37f682d4f5998bb84f5cc17d18a111f445026e2786897ca8768ea62a872
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41715478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35c19bfeda29c379abb37f674152c071f4a3cc76203229fcd2999628899f06dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:40:11 GMT
ARG CONSUL_VERSION=1.10.7
# Fri, 14 Jan 2022 18:40:12 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 14 Jan 2022 18:40:13 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 14 Jan 2022 18:40:14 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 14 Jan 2022 18:40:25 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 14 Jan 2022 18:40:26 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 14 Jan 2022 18:40:26 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 14 Jan 2022 18:40:27 GMT
VOLUME [/consul/data]
# Fri, 14 Jan 2022 18:40:28 GMT
EXPOSE 8300
# Fri, 14 Jan 2022 18:40:29 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 14 Jan 2022 18:40:30 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 14 Jan 2022 18:40:32 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 14 Jan 2022 18:40:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:40:33 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced2d5fdae89a98eb6a468152f0c8f1733d8b50be03db3287cd7a463a161c489`  
		Last Modified: Fri, 14 Jan 2022 18:41:40 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2877b7539508f4b04e834ce7af2f7a67ce9725d5b4b2897eeabc79ea91886eb`  
		Last Modified: Fri, 14 Jan 2022 18:41:45 GMT  
		Size: 39.0 MB (38992524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe1b75107d00040bfda8eb53591367afb62a5c493adfe258a3a18b17f37ea8ad`  
		Last Modified: Fri, 14 Jan 2022 18:41:40 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e7fc7f191dd1df6a3b31dfa66172ecf4ab927d9c6a7e0ee4ad5b5829e8522e4`  
		Last Modified: Fri, 14 Jan 2022 18:41:40 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:845f76ea5b7d91648c13339a4892ca1d4b1eadbe818d31bfc46e09ac8bb17d96`  
		Last Modified: Fri, 14 Jan 2022 18:41:40 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10` - linux; 386

```console
$ docker pull consul@sha256:be64a2fed0233627503f4541fa778d07dcd424ff4da861b425e3c2c3f9564238
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43094625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23295a8e8cbbfd6e3304c88db6c1c927efb08848165f1b2914e85d71457e0271`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Sat, 12 Feb 2022 01:41:32 GMT
ARG CONSUL_VERSION=1.10.8
# Sat, 12 Feb 2022 01:41:32 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.8 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 12 Feb 2022 01:41:32 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 12 Feb 2022 01:41:33 GMT
# ARGS: CONSUL_VERSION=1.10.8
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 12 Feb 2022 01:42:11 GMT
# ARGS: CONSUL_VERSION=1.10.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 12 Feb 2022 01:42:12 GMT
# ARGS: CONSUL_VERSION=1.10.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 12 Feb 2022 01:42:13 GMT
# ARGS: CONSUL_VERSION=1.10.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 12 Feb 2022 01:42:13 GMT
VOLUME [/consul/data]
# Sat, 12 Feb 2022 01:42:13 GMT
EXPOSE 8300
# Sat, 12 Feb 2022 01:42:14 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 12 Feb 2022 01:42:14 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 12 Feb 2022 01:42:14 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 12 Feb 2022 01:42:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Feb 2022 01:42:15 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3259d3be13e1fda280e5018f614200af83e3e58eefe3dc0cb7174a325253d5c5`  
		Last Modified: Sat, 12 Feb 2022 01:43:48 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5a2980bd7e4eee5cda163a94f9adccae5e306cc64592af53d019a776dd25bf`  
		Last Modified: Sat, 12 Feb 2022 01:43:55 GMT  
		Size: 40.3 MB (40262442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28a217fece634a56740b237cf65ff30148c35190d97d26ff0694f25052aafa9`  
		Last Modified: Sat, 12 Feb 2022 01:43:48 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6e01be3cf21cc803ab05104e8b2c25c381df12a8330a7da8215823dbedbe40`  
		Last Modified: Sat, 12 Feb 2022 01:43:48 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f34f69bc3459c2893ea74360bd5a1da6c08468c085b9105759d663d6429f314`  
		Last Modified: Sat, 12 Feb 2022 01:43:48 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.10.8`

```console
$ docker pull consul@sha256:0c40e937d720dd2df03801bc02e8e91b0e15e86b5c217ff27686f9955cf025bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; arm variant v6
	-	linux; 386

### `consul:1.10.8` - linux; arm variant v6

```console
$ docker pull consul@sha256:298ac8d6cb57014379dfeea323a4f40253234e0346bc4855db3c7f939646c918
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41767102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7146de82d58c8360314657ab9f3bb7d74aac8b75d8cc255f6965bb8eb9bdf8aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Sat, 12 Feb 2022 01:50:21 GMT
ARG CONSUL_VERSION=1.10.8
# Sat, 12 Feb 2022 01:50:21 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.8 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 12 Feb 2022 01:50:22 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 12 Feb 2022 01:50:24 GMT
# ARGS: CONSUL_VERSION=1.10.8
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 12 Feb 2022 01:50:51 GMT
# ARGS: CONSUL_VERSION=1.10.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 12 Feb 2022 01:50:52 GMT
# ARGS: CONSUL_VERSION=1.10.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 12 Feb 2022 01:50:54 GMT
# ARGS: CONSUL_VERSION=1.10.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 12 Feb 2022 01:50:55 GMT
VOLUME [/consul/data]
# Sat, 12 Feb 2022 01:50:55 GMT
EXPOSE 8300
# Sat, 12 Feb 2022 01:50:56 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 12 Feb 2022 01:50:56 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 12 Feb 2022 01:50:56 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 12 Feb 2022 01:50:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Feb 2022 01:50:57 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6433b6bf5bed8b3be159441dfeb9712971674bac4560ce7f8a4eff5ce13a7565`  
		Last Modified: Sat, 12 Feb 2022 01:53:02 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878f28cb8b52e741264e9f23c9e4b5591c3d645ad1f067025f9dd4d593c75def`  
		Last Modified: Sat, 12 Feb 2022 01:53:24 GMT  
		Size: 39.1 MB (39130384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a653e69a81e17e79e5c5c36302da1cfa43006b3728d594d6d7e7c2fb4858d2`  
		Last Modified: Sat, 12 Feb 2022 01:53:03 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9424e86dc77f20fb6ec25edf6c8122ceead8b081ec1f0da24ef376da60e31f`  
		Last Modified: Sat, 12 Feb 2022 01:53:02 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6919833dce23fe2753532ef08cc421715f317809ba4e185fbc8811c8fa7c3a`  
		Last Modified: Sat, 12 Feb 2022 01:53:02 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.8` - linux; 386

```console
$ docker pull consul@sha256:be64a2fed0233627503f4541fa778d07dcd424ff4da861b425e3c2c3f9564238
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43094625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23295a8e8cbbfd6e3304c88db6c1c927efb08848165f1b2914e85d71457e0271`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Sat, 12 Feb 2022 01:41:32 GMT
ARG CONSUL_VERSION=1.10.8
# Sat, 12 Feb 2022 01:41:32 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.8 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 12 Feb 2022 01:41:32 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 12 Feb 2022 01:41:33 GMT
# ARGS: CONSUL_VERSION=1.10.8
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 12 Feb 2022 01:42:11 GMT
# ARGS: CONSUL_VERSION=1.10.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 12 Feb 2022 01:42:12 GMT
# ARGS: CONSUL_VERSION=1.10.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 12 Feb 2022 01:42:13 GMT
# ARGS: CONSUL_VERSION=1.10.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 12 Feb 2022 01:42:13 GMT
VOLUME [/consul/data]
# Sat, 12 Feb 2022 01:42:13 GMT
EXPOSE 8300
# Sat, 12 Feb 2022 01:42:14 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 12 Feb 2022 01:42:14 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 12 Feb 2022 01:42:14 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 12 Feb 2022 01:42:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Feb 2022 01:42:15 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3259d3be13e1fda280e5018f614200af83e3e58eefe3dc0cb7174a325253d5c5`  
		Last Modified: Sat, 12 Feb 2022 01:43:48 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5a2980bd7e4eee5cda163a94f9adccae5e306cc64592af53d019a776dd25bf`  
		Last Modified: Sat, 12 Feb 2022 01:43:55 GMT  
		Size: 40.3 MB (40262442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28a217fece634a56740b237cf65ff30148c35190d97d26ff0694f25052aafa9`  
		Last Modified: Sat, 12 Feb 2022 01:43:48 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6e01be3cf21cc803ab05104e8b2c25c381df12a8330a7da8215823dbedbe40`  
		Last Modified: Sat, 12 Feb 2022 01:43:48 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f34f69bc3459c2893ea74360bd5a1da6c08468c085b9105759d663d6429f314`  
		Last Modified: Sat, 12 Feb 2022 01:43:48 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.11`

```console
$ docker pull consul@sha256:14973ad1d1164a23196ab4860df88ed2845584c8b84cc63462cc40002ea885ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.11` - linux; amd64

```console
$ docker pull consul@sha256:0ddc0dfddad8ff2b8ea64923383d4a84ddba21864b85a2a39b28f09b1d18c6a2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43912305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5cebfabb812332fce28693fbc088cfbb79e55dd2d338af0cfcaa9e4fc569cbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:19:31 GMT
ARG CONSUL_VERSION=1.11.2
# Fri, 14 Jan 2022 18:19:31 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 14 Jan 2022 18:19:31 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 14 Jan 2022 18:19:32 GMT
# ARGS: CONSUL_VERSION=1.11.2
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 14 Jan 2022 18:19:47 GMT
# ARGS: CONSUL_VERSION=1.11.2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 14 Jan 2022 18:19:48 GMT
# ARGS: CONSUL_VERSION=1.11.2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 14 Jan 2022 18:19:49 GMT
# ARGS: CONSUL_VERSION=1.11.2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 14 Jan 2022 18:19:49 GMT
VOLUME [/consul/data]
# Fri, 14 Jan 2022 18:19:49 GMT
EXPOSE 8300
# Fri, 14 Jan 2022 18:19:49 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 14 Jan 2022 18:19:50 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 14 Jan 2022 18:19:50 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 14 Jan 2022 18:19:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:19:50 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8172e279c1c8f35c79da13d439f1ce449c70895f6f918c8641f26978a051cbc`  
		Last Modified: Fri, 14 Jan 2022 18:21:29 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a0277f92f8d6f6e6698de8e5bebe73eda01da0b19d25fcb7d2599b4082668a`  
		Last Modified: Fri, 14 Jan 2022 18:21:37 GMT  
		Size: 41.1 MB (41086508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4994383046332c8f84b52a6efe15f1adb4c79a81f429f8dde7b0f778e9ae698`  
		Last Modified: Fri, 14 Jan 2022 18:21:29 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04bf5ee831d9822e74be0b1aea3215bee1e25cbc8d5d1e311bc8238d0cb03d36`  
		Last Modified: Fri, 14 Jan 2022 18:21:30 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2ee0a4e8fce601328442d907bc0ae97b9abc1db1792545dc2dcc58160941fe`  
		Last Modified: Fri, 14 Jan 2022 18:21:31 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11` - linux; arm variant v6

```console
$ docker pull consul@sha256:dbbfd2b35c83bf48da8b50ffad63773357b3e694f66cb06caa93f08534708838
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41682452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c03b367769374b1a71345ab0c2186a0c83919bd442e8e118be0262d6984b46f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Sat, 12 Feb 2022 01:49:33 GMT
ARG CONSUL_VERSION=1.11.3
# Sat, 12 Feb 2022 01:49:33 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 12 Feb 2022 01:49:34 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 12 Feb 2022 01:49:35 GMT
# ARGS: CONSUL_VERSION=1.11.3
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 12 Feb 2022 01:50:00 GMT
# ARGS: CONSUL_VERSION=1.11.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 12 Feb 2022 01:50:02 GMT
# ARGS: CONSUL_VERSION=1.11.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 12 Feb 2022 01:50:04 GMT
# ARGS: CONSUL_VERSION=1.11.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 12 Feb 2022 01:50:04 GMT
VOLUME [/consul/data]
# Sat, 12 Feb 2022 01:50:05 GMT
EXPOSE 8300
# Sat, 12 Feb 2022 01:50:06 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 12 Feb 2022 01:50:06 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 12 Feb 2022 01:50:07 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 12 Feb 2022 01:50:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Feb 2022 01:50:08 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87008e907ff201560ab56249dd1fe2e0f38bef1f5607ba09eaf4426e29bc28b3`  
		Last Modified: Sat, 12 Feb 2022 01:52:26 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17fa1c0968f07bbcf8466495b357c19a158f4899674e2893740d832c54bf55d`  
		Last Modified: Sat, 12 Feb 2022 01:52:47 GMT  
		Size: 39.0 MB (39045731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f7c3cf0aa9b8598143005b4a18a66a01deddf3a6d8bd68a8a894980a623ce1`  
		Last Modified: Sat, 12 Feb 2022 01:52:26 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8f3ed270d044d28bb625f443e8feb3f47f4c0778a862389d185897088151f0`  
		Last Modified: Sat, 12 Feb 2022 01:52:26 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c2d53002a37c745be8236d738a0c2f947f0f12facb6237a5550a407466983d`  
		Last Modified: Sat, 12 Feb 2022 01:52:26 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:7df6609e86fb72a0f623ff21519798b5f06597cd77e79d3dde53c86eedbdecfb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41520118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6665c9735fea0297e8e98b868bada7f411f257b6f80dbdbfba7202bedc77f4ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:39:34 GMT
ARG CONSUL_VERSION=1.11.2
# Fri, 14 Jan 2022 18:39:35 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 14 Jan 2022 18:39:36 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 14 Jan 2022 18:39:37 GMT
# ARGS: CONSUL_VERSION=1.11.2
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 14 Jan 2022 18:39:53 GMT
# ARGS: CONSUL_VERSION=1.11.2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 14 Jan 2022 18:39:54 GMT
# ARGS: CONSUL_VERSION=1.11.2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 14 Jan 2022 18:39:55 GMT
# ARGS: CONSUL_VERSION=1.11.2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 14 Jan 2022 18:39:56 GMT
VOLUME [/consul/data]
# Fri, 14 Jan 2022 18:39:57 GMT
EXPOSE 8300
# Fri, 14 Jan 2022 18:39:58 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 14 Jan 2022 18:39:59 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 14 Jan 2022 18:40:01 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 14 Jan 2022 18:40:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:40:02 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c038088c0871b6cf21d44268e04b69630960f81ea50cbac71923dd4d755f14a`  
		Last Modified: Fri, 14 Jan 2022 18:41:20 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177d0d5d31460160d580ecbb087e91a8c604280bf9cd67fa71e6eb71c1187226`  
		Last Modified: Fri, 14 Jan 2022 18:41:26 GMT  
		Size: 38.8 MB (38797162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ead2c6b0b970b32503ce0c0a48cf2eaeb73b73b5ddb6e983a920a5fd981674`  
		Last Modified: Fri, 14 Jan 2022 18:41:20 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3181d6b79134cda51bfa818e966e88da033a76fbacfee2814c19f7114eea5f9a`  
		Last Modified: Fri, 14 Jan 2022 18:41:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c8e41024fb0d850e8d0342ab7a1fc601fe7f969b25025568ee70f7c751ca62`  
		Last Modified: Fri, 14 Jan 2022 18:41:20 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11` - linux; 386

```console
$ docker pull consul@sha256:1304773a9fe880a58e228887819f227f1e3702246c34602a5a5a2ca7bce3d0d5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.7 MB (42735297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa0b311cd86f249cb811d35a57cffe14cf609863798aa111922ab2918842ab4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Sat, 12 Feb 2022 01:38:37 GMT
ARG CONSUL_VERSION=1.11.3
# Sat, 12 Feb 2022 01:38:37 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 12 Feb 2022 01:38:37 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 12 Feb 2022 01:38:39 GMT
# ARGS: CONSUL_VERSION=1.11.3
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 12 Feb 2022 01:41:10 GMT
# ARGS: CONSUL_VERSION=1.11.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 12 Feb 2022 01:41:11 GMT
# ARGS: CONSUL_VERSION=1.11.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 12 Feb 2022 01:41:12 GMT
# ARGS: CONSUL_VERSION=1.11.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 12 Feb 2022 01:41:12 GMT
VOLUME [/consul/data]
# Sat, 12 Feb 2022 01:41:13 GMT
EXPOSE 8300
# Sat, 12 Feb 2022 01:41:13 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 12 Feb 2022 01:41:13 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 12 Feb 2022 01:41:13 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 12 Feb 2022 01:41:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Feb 2022 01:41:14 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fbd61929fc21fd52ad4759e0e3d437b2e1aa30ad7e8d4ae6daf652e6ae8403b`  
		Last Modified: Sat, 12 Feb 2022 01:43:21 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bad2d753f0541317860d8bc2f2962125b4f4eea60f19a31633d666e38c8418`  
		Last Modified: Sat, 12 Feb 2022 01:43:27 GMT  
		Size: 39.9 MB (39903112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbc31b349a8590c9fb6b4cdd492db6d8ee0c2a1633f71d9862dfb7102c66342`  
		Last Modified: Sat, 12 Feb 2022 01:43:21 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ffe2fca8726b330c2452bad3261605b912b590481a82c00ae8ec3da02f9e72`  
		Last Modified: Sat, 12 Feb 2022 01:43:21 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea127a71de44806c1cf6109eae7118a56eed39379cef7fd64c5fb96a9c84c37d`  
		Last Modified: Sat, 12 Feb 2022 01:43:21 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.11.3`

```console
$ docker pull consul@sha256:49dd9119b0f5c6490320e8e917182d5b68ba79c300197a6b1345a3a70a1f9102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; arm variant v6
	-	linux; 386

### `consul:1.11.3` - linux; arm variant v6

```console
$ docker pull consul@sha256:dbbfd2b35c83bf48da8b50ffad63773357b3e694f66cb06caa93f08534708838
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41682452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c03b367769374b1a71345ab0c2186a0c83919bd442e8e118be0262d6984b46f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Sat, 12 Feb 2022 01:49:33 GMT
ARG CONSUL_VERSION=1.11.3
# Sat, 12 Feb 2022 01:49:33 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 12 Feb 2022 01:49:34 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 12 Feb 2022 01:49:35 GMT
# ARGS: CONSUL_VERSION=1.11.3
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 12 Feb 2022 01:50:00 GMT
# ARGS: CONSUL_VERSION=1.11.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 12 Feb 2022 01:50:02 GMT
# ARGS: CONSUL_VERSION=1.11.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 12 Feb 2022 01:50:04 GMT
# ARGS: CONSUL_VERSION=1.11.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 12 Feb 2022 01:50:04 GMT
VOLUME [/consul/data]
# Sat, 12 Feb 2022 01:50:05 GMT
EXPOSE 8300
# Sat, 12 Feb 2022 01:50:06 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 12 Feb 2022 01:50:06 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 12 Feb 2022 01:50:07 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 12 Feb 2022 01:50:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Feb 2022 01:50:08 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87008e907ff201560ab56249dd1fe2e0f38bef1f5607ba09eaf4426e29bc28b3`  
		Last Modified: Sat, 12 Feb 2022 01:52:26 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17fa1c0968f07bbcf8466495b357c19a158f4899674e2893740d832c54bf55d`  
		Last Modified: Sat, 12 Feb 2022 01:52:47 GMT  
		Size: 39.0 MB (39045731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f7c3cf0aa9b8598143005b4a18a66a01deddf3a6d8bd68a8a894980a623ce1`  
		Last Modified: Sat, 12 Feb 2022 01:52:26 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8f3ed270d044d28bb625f443e8feb3f47f4c0778a862389d185897088151f0`  
		Last Modified: Sat, 12 Feb 2022 01:52:26 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c2d53002a37c745be8236d738a0c2f947f0f12facb6237a5550a407466983d`  
		Last Modified: Sat, 12 Feb 2022 01:52:26 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11.3` - linux; 386

```console
$ docker pull consul@sha256:1304773a9fe880a58e228887819f227f1e3702246c34602a5a5a2ca7bce3d0d5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.7 MB (42735297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa0b311cd86f249cb811d35a57cffe14cf609863798aa111922ab2918842ab4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Sat, 12 Feb 2022 01:38:37 GMT
ARG CONSUL_VERSION=1.11.3
# Sat, 12 Feb 2022 01:38:37 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 12 Feb 2022 01:38:37 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 12 Feb 2022 01:38:39 GMT
# ARGS: CONSUL_VERSION=1.11.3
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 12 Feb 2022 01:41:10 GMT
# ARGS: CONSUL_VERSION=1.11.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 12 Feb 2022 01:41:11 GMT
# ARGS: CONSUL_VERSION=1.11.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 12 Feb 2022 01:41:12 GMT
# ARGS: CONSUL_VERSION=1.11.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 12 Feb 2022 01:41:12 GMT
VOLUME [/consul/data]
# Sat, 12 Feb 2022 01:41:13 GMT
EXPOSE 8300
# Sat, 12 Feb 2022 01:41:13 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 12 Feb 2022 01:41:13 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 12 Feb 2022 01:41:13 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 12 Feb 2022 01:41:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Feb 2022 01:41:14 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fbd61929fc21fd52ad4759e0e3d437b2e1aa30ad7e8d4ae6daf652e6ae8403b`  
		Last Modified: Sat, 12 Feb 2022 01:43:21 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bad2d753f0541317860d8bc2f2962125b4f4eea60f19a31633d666e38c8418`  
		Last Modified: Sat, 12 Feb 2022 01:43:27 GMT  
		Size: 39.9 MB (39903112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbc31b349a8590c9fb6b4cdd492db6d8ee0c2a1633f71d9862dfb7102c66342`  
		Last Modified: Sat, 12 Feb 2022 01:43:21 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ffe2fca8726b330c2452bad3261605b912b590481a82c00ae8ec3da02f9e72`  
		Last Modified: Sat, 12 Feb 2022 01:43:21 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea127a71de44806c1cf6109eae7118a56eed39379cef7fd64c5fb96a9c84c37d`  
		Last Modified: Sat, 12 Feb 2022 01:43:21 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9`

```console
$ docker pull consul@sha256:3f6cd292068f8e40f05851bc2390815344b1e1431a14459017cc9d0508073459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.9` - linux; amd64

```console
$ docker pull consul@sha256:6aa8b6869809d0e522cf3098abb8164749a9a9642e6458ca084a81546fd7af24
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40186817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12fec3b64b99ae4a4f5a0213ea4b17ef35b361adccd5fdb2572ecc96810ceb22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:20:17 GMT
ARG CONSUL_VERSION=1.9.14
# Fri, 14 Jan 2022 18:20:17 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.14 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 14 Jan 2022 18:20:17 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 14 Jan 2022 18:20:18 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 14 Jan 2022 18:20:52 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 14 Jan 2022 18:20:53 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 14 Jan 2022 18:20:54 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 14 Jan 2022 18:20:54 GMT
VOLUME [/consul/data]
# Fri, 14 Jan 2022 18:20:55 GMT
EXPOSE 8300
# Fri, 14 Jan 2022 18:20:55 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 14 Jan 2022 18:20:55 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 14 Jan 2022 18:20:55 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 14 Jan 2022 18:20:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:20:56 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9404fc309f18dec67cc01caf7f46c70d5063f23b93e5cf58c794dff89e9dffb8`  
		Last Modified: Fri, 14 Jan 2022 18:23:00 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db6fd1d712f19f5e37518a8928338690f0aea86b37a79e115229dd3e7f62688`  
		Last Modified: Fri, 14 Jan 2022 18:23:05 GMT  
		Size: 37.4 MB (37361020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef22807f8bd72cf8f2e407f8840a9b9236326a08b747bf4cbe5fe288231302e`  
		Last Modified: Fri, 14 Jan 2022 18:22:59 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296f4b2065d929c8308b295c4257e2af845e2b47d637f11249c644d8b912200b`  
		Last Modified: Fri, 14 Jan 2022 18:23:00 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfae83c0341b8317db13a32e6abed487c1bd04a028fb837fef096ede4cb5b7d1`  
		Last Modified: Fri, 14 Jan 2022 18:23:00 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; arm variant v6

```console
$ docker pull consul@sha256:114d0fa7fbf8364b43de2be40dd4fe7f85019156dbbc8e57e268c0ce10d7d6d8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38215792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308a6fa2bf51e81b458920abbbb8a09dc28a0e9a56ad9c3c8a74c6090675e8ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Sat, 12 Feb 2022 01:51:11 GMT
ARG CONSUL_VERSION=1.9.15
# Sat, 12 Feb 2022 01:51:12 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.15 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 12 Feb 2022 01:51:12 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 12 Feb 2022 01:51:14 GMT
# ARGS: CONSUL_VERSION=1.9.15
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 12 Feb 2022 01:51:36 GMT
# ARGS: CONSUL_VERSION=1.9.15
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 12 Feb 2022 01:51:38 GMT
# ARGS: CONSUL_VERSION=1.9.15
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 12 Feb 2022 01:51:39 GMT
# ARGS: CONSUL_VERSION=1.9.15
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 12 Feb 2022 01:51:40 GMT
VOLUME [/consul/data]
# Sat, 12 Feb 2022 01:51:40 GMT
EXPOSE 8300
# Sat, 12 Feb 2022 01:51:41 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 12 Feb 2022 01:51:41 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 12 Feb 2022 01:51:42 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 12 Feb 2022 01:51:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Feb 2022 01:51:43 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f6f3c9568b47c4bf44b4099672264efbf0dcbbbde4863686d69734b848d7ff`  
		Last Modified: Sat, 12 Feb 2022 01:53:35 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57af4e673ca60e6ec30cf030ea2e3b2c24a94a130f4968c84f74032ef3dc2f3`  
		Last Modified: Sat, 12 Feb 2022 01:53:54 GMT  
		Size: 35.6 MB (35579077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:154c36b13f758b324e17d809a7adbdf33b67e159b245e4b28fbcb33d75bb19c1`  
		Last Modified: Sat, 12 Feb 2022 01:53:35 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff8f832057f753e41d4ab053e1e5b0729f0758f618cbafb539edc33465fe3b6`  
		Last Modified: Sat, 12 Feb 2022 01:53:35 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6635806208ab7c02bcf738f7f96e45b0de027117964965ec9da5d4448e2df1`  
		Last Modified: Sat, 12 Feb 2022 01:53:35 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:003be37312a0ee2537a271b4ef2b36e6b89892e50653b4e3ed8eb2c1cd8e34a3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38179861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3365225d1b2f36bbcd210b7b3a577202deb80bd065ca0b065da292d42c768549`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:40:38 GMT
ARG CONSUL_VERSION=1.9.14
# Fri, 14 Jan 2022 18:40:39 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.14 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 14 Jan 2022 18:40:40 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 14 Jan 2022 18:40:41 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 14 Jan 2022 18:40:52 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 14 Jan 2022 18:40:52 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 14 Jan 2022 18:40:53 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 14 Jan 2022 18:40:54 GMT
VOLUME [/consul/data]
# Fri, 14 Jan 2022 18:40:55 GMT
EXPOSE 8300
# Fri, 14 Jan 2022 18:40:56 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 14 Jan 2022 18:40:57 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 14 Jan 2022 18:40:59 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 14 Jan 2022 18:40:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:41:00 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7439133698bbbd600cf9d81057f5df91f92892e449e5bd2f672c09d8417570`  
		Last Modified: Fri, 14 Jan 2022 18:41:56 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1a738821d02cc4713eb5a0e06e1285d353b0e78a1fc422f9f12ab52831bc7f`  
		Last Modified: Fri, 14 Jan 2022 18:42:01 GMT  
		Size: 35.5 MB (35456907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b10520793f292d10f5862e10d4349f4b5e8dac2f667c397c9e74989a6984f6`  
		Last Modified: Fri, 14 Jan 2022 18:41:56 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675f8d76a61da0e0ac8d8516c3b1b941c8c3caca512633169db378da41690d17`  
		Last Modified: Fri, 14 Jan 2022 18:41:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e45719eb90d072234e25c87caf9254d85daccc866886c4cb9f96929370a8ea`  
		Last Modified: Fri, 14 Jan 2022 18:41:56 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; 386

```console
$ docker pull consul@sha256:ce64644d31515aaa842ab6622af9938ff5ec55435f5ce5400cfcf9d2366655c8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39514404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3db905419e5e28d054293da6b934f8d1948c822dc557baf57e9faf156fb33d43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Sat, 12 Feb 2022 01:42:21 GMT
ARG CONSUL_VERSION=1.9.15
# Sat, 12 Feb 2022 01:42:21 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.15 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 12 Feb 2022 01:42:22 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 12 Feb 2022 01:42:23 GMT
# ARGS: CONSUL_VERSION=1.9.15
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 12 Feb 2022 01:42:51 GMT
# ARGS: CONSUL_VERSION=1.9.15
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 12 Feb 2022 01:42:52 GMT
# ARGS: CONSUL_VERSION=1.9.15
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 12 Feb 2022 01:42:53 GMT
# ARGS: CONSUL_VERSION=1.9.15
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 12 Feb 2022 01:42:54 GMT
VOLUME [/consul/data]
# Sat, 12 Feb 2022 01:42:54 GMT
EXPOSE 8300
# Sat, 12 Feb 2022 01:42:54 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 12 Feb 2022 01:42:54 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 12 Feb 2022 01:42:55 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 12 Feb 2022 01:42:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Feb 2022 01:42:55 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6dacf6bfcd05ebee4b7814c1e2458230bc530ec3032332b864478262b32709b`  
		Last Modified: Sat, 12 Feb 2022 01:44:06 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c2f315c27b3d7dfb65ae29709d1eca3816562f0f1dace9d6e1035d5804a76c`  
		Last Modified: Sat, 12 Feb 2022 01:44:12 GMT  
		Size: 36.7 MB (36682221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a900872b2300734d9ce3cef3365280fe46505ac36583d43ca032ca78b2430fcf`  
		Last Modified: Sat, 12 Feb 2022 01:44:06 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c153625bb4bef08683d407250abd66ba10f71d027c761158eb362657287591`  
		Last Modified: Sat, 12 Feb 2022 01:44:07 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39cfa48ca2fd0f3bc310d77e51d7fd852609e549dd9368534c6231e3ecc176cc`  
		Last Modified: Sat, 12 Feb 2022 01:44:06 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9.15`

```console
$ docker pull consul@sha256:7690a177c856959d4ae030d1b21a6cdc86cbc8e4db572900886a90ca3b01e26f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; arm variant v6
	-	linux; 386

### `consul:1.9.15` - linux; arm variant v6

```console
$ docker pull consul@sha256:114d0fa7fbf8364b43de2be40dd4fe7f85019156dbbc8e57e268c0ce10d7d6d8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38215792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308a6fa2bf51e81b458920abbbb8a09dc28a0e9a56ad9c3c8a74c6090675e8ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Sat, 12 Feb 2022 01:51:11 GMT
ARG CONSUL_VERSION=1.9.15
# Sat, 12 Feb 2022 01:51:12 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.15 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 12 Feb 2022 01:51:12 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 12 Feb 2022 01:51:14 GMT
# ARGS: CONSUL_VERSION=1.9.15
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 12 Feb 2022 01:51:36 GMT
# ARGS: CONSUL_VERSION=1.9.15
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 12 Feb 2022 01:51:38 GMT
# ARGS: CONSUL_VERSION=1.9.15
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 12 Feb 2022 01:51:39 GMT
# ARGS: CONSUL_VERSION=1.9.15
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 12 Feb 2022 01:51:40 GMT
VOLUME [/consul/data]
# Sat, 12 Feb 2022 01:51:40 GMT
EXPOSE 8300
# Sat, 12 Feb 2022 01:51:41 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 12 Feb 2022 01:51:41 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 12 Feb 2022 01:51:42 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 12 Feb 2022 01:51:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Feb 2022 01:51:43 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f6f3c9568b47c4bf44b4099672264efbf0dcbbbde4863686d69734b848d7ff`  
		Last Modified: Sat, 12 Feb 2022 01:53:35 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57af4e673ca60e6ec30cf030ea2e3b2c24a94a130f4968c84f74032ef3dc2f3`  
		Last Modified: Sat, 12 Feb 2022 01:53:54 GMT  
		Size: 35.6 MB (35579077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:154c36b13f758b324e17d809a7adbdf33b67e159b245e4b28fbcb33d75bb19c1`  
		Last Modified: Sat, 12 Feb 2022 01:53:35 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff8f832057f753e41d4ab053e1e5b0729f0758f618cbafb539edc33465fe3b6`  
		Last Modified: Sat, 12 Feb 2022 01:53:35 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6635806208ab7c02bcf738f7f96e45b0de027117964965ec9da5d4448e2df1`  
		Last Modified: Sat, 12 Feb 2022 01:53:35 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.15` - linux; 386

```console
$ docker pull consul@sha256:ce64644d31515aaa842ab6622af9938ff5ec55435f5ce5400cfcf9d2366655c8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39514404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3db905419e5e28d054293da6b934f8d1948c822dc557baf57e9faf156fb33d43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Sat, 12 Feb 2022 01:42:21 GMT
ARG CONSUL_VERSION=1.9.15
# Sat, 12 Feb 2022 01:42:21 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.15 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 12 Feb 2022 01:42:22 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 12 Feb 2022 01:42:23 GMT
# ARGS: CONSUL_VERSION=1.9.15
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 12 Feb 2022 01:42:51 GMT
# ARGS: CONSUL_VERSION=1.9.15
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 12 Feb 2022 01:42:52 GMT
# ARGS: CONSUL_VERSION=1.9.15
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 12 Feb 2022 01:42:53 GMT
# ARGS: CONSUL_VERSION=1.9.15
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 12 Feb 2022 01:42:54 GMT
VOLUME [/consul/data]
# Sat, 12 Feb 2022 01:42:54 GMT
EXPOSE 8300
# Sat, 12 Feb 2022 01:42:54 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 12 Feb 2022 01:42:54 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 12 Feb 2022 01:42:55 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 12 Feb 2022 01:42:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Feb 2022 01:42:55 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6dacf6bfcd05ebee4b7814c1e2458230bc530ec3032332b864478262b32709b`  
		Last Modified: Sat, 12 Feb 2022 01:44:06 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c2f315c27b3d7dfb65ae29709d1eca3816562f0f1dace9d6e1035d5804a76c`  
		Last Modified: Sat, 12 Feb 2022 01:44:12 GMT  
		Size: 36.7 MB (36682221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a900872b2300734d9ce3cef3365280fe46505ac36583d43ca032ca78b2430fcf`  
		Last Modified: Sat, 12 Feb 2022 01:44:06 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c153625bb4bef08683d407250abd66ba10f71d027c761158eb362657287591`  
		Last Modified: Sat, 12 Feb 2022 01:44:07 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39cfa48ca2fd0f3bc310d77e51d7fd852609e549dd9368534c6231e3ecc176cc`  
		Last Modified: Sat, 12 Feb 2022 01:44:06 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:latest`

```console
$ docker pull consul@sha256:14973ad1d1164a23196ab4860df88ed2845584c8b84cc63462cc40002ea885ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:latest` - linux; amd64

```console
$ docker pull consul@sha256:0ddc0dfddad8ff2b8ea64923383d4a84ddba21864b85a2a39b28f09b1d18c6a2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43912305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5cebfabb812332fce28693fbc088cfbb79e55dd2d338af0cfcaa9e4fc569cbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:19:31 GMT
ARG CONSUL_VERSION=1.11.2
# Fri, 14 Jan 2022 18:19:31 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 14 Jan 2022 18:19:31 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 14 Jan 2022 18:19:32 GMT
# ARGS: CONSUL_VERSION=1.11.2
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 14 Jan 2022 18:19:47 GMT
# ARGS: CONSUL_VERSION=1.11.2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 14 Jan 2022 18:19:48 GMT
# ARGS: CONSUL_VERSION=1.11.2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 14 Jan 2022 18:19:49 GMT
# ARGS: CONSUL_VERSION=1.11.2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 14 Jan 2022 18:19:49 GMT
VOLUME [/consul/data]
# Fri, 14 Jan 2022 18:19:49 GMT
EXPOSE 8300
# Fri, 14 Jan 2022 18:19:49 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 14 Jan 2022 18:19:50 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 14 Jan 2022 18:19:50 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 14 Jan 2022 18:19:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:19:50 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8172e279c1c8f35c79da13d439f1ce449c70895f6f918c8641f26978a051cbc`  
		Last Modified: Fri, 14 Jan 2022 18:21:29 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a0277f92f8d6f6e6698de8e5bebe73eda01da0b19d25fcb7d2599b4082668a`  
		Last Modified: Fri, 14 Jan 2022 18:21:37 GMT  
		Size: 41.1 MB (41086508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4994383046332c8f84b52a6efe15f1adb4c79a81f429f8dde7b0f778e9ae698`  
		Last Modified: Fri, 14 Jan 2022 18:21:29 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04bf5ee831d9822e74be0b1aea3215bee1e25cbc8d5d1e311bc8238d0cb03d36`  
		Last Modified: Fri, 14 Jan 2022 18:21:30 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2ee0a4e8fce601328442d907bc0ae97b9abc1db1792545dc2dcc58160941fe`  
		Last Modified: Fri, 14 Jan 2022 18:21:31 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm variant v6

```console
$ docker pull consul@sha256:dbbfd2b35c83bf48da8b50ffad63773357b3e694f66cb06caa93f08534708838
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41682452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c03b367769374b1a71345ab0c2186a0c83919bd442e8e118be0262d6984b46f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Sat, 12 Feb 2022 01:49:33 GMT
ARG CONSUL_VERSION=1.11.3
# Sat, 12 Feb 2022 01:49:33 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 12 Feb 2022 01:49:34 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 12 Feb 2022 01:49:35 GMT
# ARGS: CONSUL_VERSION=1.11.3
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 12 Feb 2022 01:50:00 GMT
# ARGS: CONSUL_VERSION=1.11.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 12 Feb 2022 01:50:02 GMT
# ARGS: CONSUL_VERSION=1.11.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 12 Feb 2022 01:50:04 GMT
# ARGS: CONSUL_VERSION=1.11.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 12 Feb 2022 01:50:04 GMT
VOLUME [/consul/data]
# Sat, 12 Feb 2022 01:50:05 GMT
EXPOSE 8300
# Sat, 12 Feb 2022 01:50:06 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 12 Feb 2022 01:50:06 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 12 Feb 2022 01:50:07 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 12 Feb 2022 01:50:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Feb 2022 01:50:08 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87008e907ff201560ab56249dd1fe2e0f38bef1f5607ba09eaf4426e29bc28b3`  
		Last Modified: Sat, 12 Feb 2022 01:52:26 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17fa1c0968f07bbcf8466495b357c19a158f4899674e2893740d832c54bf55d`  
		Last Modified: Sat, 12 Feb 2022 01:52:47 GMT  
		Size: 39.0 MB (39045731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f7c3cf0aa9b8598143005b4a18a66a01deddf3a6d8bd68a8a894980a623ce1`  
		Last Modified: Sat, 12 Feb 2022 01:52:26 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8f3ed270d044d28bb625f443e8feb3f47f4c0778a862389d185897088151f0`  
		Last Modified: Sat, 12 Feb 2022 01:52:26 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c2d53002a37c745be8236d738a0c2f947f0f12facb6237a5550a407466983d`  
		Last Modified: Sat, 12 Feb 2022 01:52:26 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:7df6609e86fb72a0f623ff21519798b5f06597cd77e79d3dde53c86eedbdecfb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41520118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6665c9735fea0297e8e98b868bada7f411f257b6f80dbdbfba7202bedc77f4ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:39:34 GMT
ARG CONSUL_VERSION=1.11.2
# Fri, 14 Jan 2022 18:39:35 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 14 Jan 2022 18:39:36 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 14 Jan 2022 18:39:37 GMT
# ARGS: CONSUL_VERSION=1.11.2
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 14 Jan 2022 18:39:53 GMT
# ARGS: CONSUL_VERSION=1.11.2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 14 Jan 2022 18:39:54 GMT
# ARGS: CONSUL_VERSION=1.11.2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 14 Jan 2022 18:39:55 GMT
# ARGS: CONSUL_VERSION=1.11.2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 14 Jan 2022 18:39:56 GMT
VOLUME [/consul/data]
# Fri, 14 Jan 2022 18:39:57 GMT
EXPOSE 8300
# Fri, 14 Jan 2022 18:39:58 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 14 Jan 2022 18:39:59 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 14 Jan 2022 18:40:01 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 14 Jan 2022 18:40:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:40:02 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c038088c0871b6cf21d44268e04b69630960f81ea50cbac71923dd4d755f14a`  
		Last Modified: Fri, 14 Jan 2022 18:41:20 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177d0d5d31460160d580ecbb087e91a8c604280bf9cd67fa71e6eb71c1187226`  
		Last Modified: Fri, 14 Jan 2022 18:41:26 GMT  
		Size: 38.8 MB (38797162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ead2c6b0b970b32503ce0c0a48cf2eaeb73b73b5ddb6e983a920a5fd981674`  
		Last Modified: Fri, 14 Jan 2022 18:41:20 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3181d6b79134cda51bfa818e966e88da033a76fbacfee2814c19f7114eea5f9a`  
		Last Modified: Fri, 14 Jan 2022 18:41:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c8e41024fb0d850e8d0342ab7a1fc601fe7f969b25025568ee70f7c751ca62`  
		Last Modified: Fri, 14 Jan 2022 18:41:20 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; 386

```console
$ docker pull consul@sha256:1304773a9fe880a58e228887819f227f1e3702246c34602a5a5a2ca7bce3d0d5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.7 MB (42735297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa0b311cd86f249cb811d35a57cffe14cf609863798aa111922ab2918842ab4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Sat, 12 Feb 2022 01:38:37 GMT
ARG CONSUL_VERSION=1.11.3
# Sat, 12 Feb 2022 01:38:37 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 12 Feb 2022 01:38:37 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 12 Feb 2022 01:38:39 GMT
# ARGS: CONSUL_VERSION=1.11.3
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 12 Feb 2022 01:41:10 GMT
# ARGS: CONSUL_VERSION=1.11.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 12 Feb 2022 01:41:11 GMT
# ARGS: CONSUL_VERSION=1.11.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 12 Feb 2022 01:41:12 GMT
# ARGS: CONSUL_VERSION=1.11.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 12 Feb 2022 01:41:12 GMT
VOLUME [/consul/data]
# Sat, 12 Feb 2022 01:41:13 GMT
EXPOSE 8300
# Sat, 12 Feb 2022 01:41:13 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 12 Feb 2022 01:41:13 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 12 Feb 2022 01:41:13 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 12 Feb 2022 01:41:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Feb 2022 01:41:14 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fbd61929fc21fd52ad4759e0e3d437b2e1aa30ad7e8d4ae6daf652e6ae8403b`  
		Last Modified: Sat, 12 Feb 2022 01:43:21 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bad2d753f0541317860d8bc2f2962125b4f4eea60f19a31633d666e38c8418`  
		Last Modified: Sat, 12 Feb 2022 01:43:27 GMT  
		Size: 39.9 MB (39903112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbc31b349a8590c9fb6b4cdd492db6d8ee0c2a1633f71d9862dfb7102c66342`  
		Last Modified: Sat, 12 Feb 2022 01:43:21 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ffe2fca8726b330c2452bad3261605b912b590481a82c00ae8ec3da02f9e72`  
		Last Modified: Sat, 12 Feb 2022 01:43:21 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea127a71de44806c1cf6109eae7118a56eed39379cef7fd64c5fb96a9c84c37d`  
		Last Modified: Sat, 12 Feb 2022 01:43:21 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
