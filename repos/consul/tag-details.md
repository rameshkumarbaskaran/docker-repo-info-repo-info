<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `consul`

-	[`consul:1.10`](#consul110)
-	[`consul:1.10.5`](#consul1105)
-	[`consul:1.11.0-beta`](#consul1110-beta)
-	[`consul:1.11.0-beta3`](#consul1110-beta3)
-	[`consul:1.8`](#consul18)
-	[`consul:1.8.18`](#consul1818)
-	[`consul:1.9`](#consul19)
-	[`consul:1.9.12`](#consul1912)
-	[`consul:latest`](#consullatest)

## `consul:1.10`

```console
$ docker pull consul@sha256:e4be41d10951d8adfba93d2d1a92dba879a7c5668fa88ab16593d880e4574e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.10` - linux; amd64

```console
$ docker pull consul@sha256:4475b8159e056762094fddccfc4ee04cb2fa27168ab1e2fe5602fc0321797573
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43681368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3539c821b8d51285cccc20d1146f06adcf4eb7462ac74f89c0e29e324cb3e7aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 20:20:45 GMT
ARG CONSUL_VERSION=1.10.5
# Tue, 14 Dec 2021 20:20:45 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.5 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 20:20:45 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 20:20:46 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 20:20:52 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 20:20:54 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 20:20:54 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 20:20:55 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 20:20:55 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 20:20:55 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 20:20:55 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 20:20:55 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 20:20:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 20:20:56 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a31878686a1a40acb3733831b5a7977a1dd15481c4fa1b284f0b2ec7c7d368`  
		Last Modified: Tue, 14 Dec 2021 20:21:42 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8a9b91a9748569616113217fd3037a4404d3e6fed1b00b3fd776da6bf88430`  
		Last Modified: Tue, 14 Dec 2021 20:21:48 GMT  
		Size: 40.9 MB (40855570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44901b3a103ad21cb27e4943d04146ec890159259fd545231fc8edb6b4de44f`  
		Last Modified: Tue, 14 Dec 2021 20:21:42 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964fca1b89e646eeea82bd99676942a41d53336385078346d0d0cb55e52c8f7f`  
		Last Modified: Tue, 14 Dec 2021 20:21:42 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06001403e520ac36329d871362a618fca50e6758455ef4788e34d656a3ab2db4`  
		Last Modified: Tue, 14 Dec 2021 20:21:42 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10` - linux; arm variant v6

```console
$ docker pull consul@sha256:26f6c9499d42f73064f17b21d437bafc9fa61a3bf57bc7a7bc7540531d95eb3f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41747103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a429113e2ccc547f1ee16878d329fac41000ab084f7b6b11471fd7dafe758982`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 19:49:42 GMT
ARG CONSUL_VERSION=1.10.5
# Tue, 14 Dec 2021 19:49:42 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.5 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 19:49:43 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 19:49:44 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 19:49:59 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 19:50:01 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 19:50:02 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 19:50:03 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 19:50:03 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 19:50:03 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 19:50:04 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 19:50:04 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 19:50:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 19:50:05 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8738eec68152c08f93f0bc71941e91f6fe264b9630c9caba638107049fa1bc4`  
		Last Modified: Tue, 14 Dec 2021 19:52:08 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cfdb687b1dc02c4107c9139d0f53c12cbf3277b217201770d9ae8b2885b88c`  
		Last Modified: Tue, 14 Dec 2021 19:52:28 GMT  
		Size: 39.1 MB (39110381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47fa8e27beaff857f03fc8210cf70f6fabe906382ed2c0339765cadee8c6cbe`  
		Last Modified: Tue, 14 Dec 2021 19:52:08 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c210f4cc2d698fd83ed20044938c48fa52e2cf08e9dfa365e7934863cfe3e94`  
		Last Modified: Tue, 14 Dec 2021 19:52:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f007675b8db5768f9232d3d0f90275fc72f85204b03e85393dd52bd7ee68f7c0`  
		Last Modified: Tue, 14 Dec 2021 19:52:08 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:56ab516709703801f86014f2c8c01444507fd43032564c5f805d2cad08fe4747
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41699391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50953a41d2fdcad5e29f0cd8a6a1a6a4f6e5ef655e077cf6adbf4ab0cff93221`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 20:42:07 GMT
ARG CONSUL_VERSION=1.10.5
# Tue, 14 Dec 2021 20:42:08 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.5 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 20:42:09 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 20:42:10 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 20:42:21 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 20:42:22 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 20:42:23 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 20:42:24 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 20:42:25 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 20:42:26 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 20:42:27 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 20:42:29 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 20:42:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 20:42:30 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a2c1bd6c357bc002e6a58e4dba209c567c829b5c3d67a98785cc945075c119`  
		Last Modified: Tue, 14 Dec 2021 20:43:44 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeffb4866022338f09341cba456bc786d9a24021b9def25d3c52dfc1b44fc06f`  
		Last Modified: Tue, 14 Dec 2021 20:43:49 GMT  
		Size: 39.0 MB (38976434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00761f25345de261175f4c5295c54ca88591886261a2d8b6df4349fc125c02ee`  
		Last Modified: Tue, 14 Dec 2021 20:43:44 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef726733fba0795bb822948e4c778b0905a5817dece0dab82e9c748f348bd6a`  
		Last Modified: Tue, 14 Dec 2021 20:43:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e926b3c440264449b5bdd90f02c671539c8a02a514fb4c0b00b77b8ee8715c04`  
		Last Modified: Tue, 14 Dec 2021 20:43:44 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10` - linux; 386

```console
$ docker pull consul@sha256:4f528d2bec02d5a9bd173c1853d1977b0cbc62deba36c3a0c749a750d75208b6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43063020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b8d0dfb97fd1d3e95de17901bec6860d509acc08a8df1e1f2d8b5533b27826`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 20:38:28 GMT
ARG CONSUL_VERSION=1.10.5
# Tue, 14 Dec 2021 20:38:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.5 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 20:38:29 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 20:38:30 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 20:38:38 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 20:38:39 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 20:38:40 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 20:38:41 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 20:38:41 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 20:38:41 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 20:38:41 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 20:38:42 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 20:38:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 20:38:42 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c775a942206ecfd17cfc4806f59ef3add5887dd9bd84253e7df754248313fb`  
		Last Modified: Tue, 14 Dec 2021 20:39:46 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38feef64f936ed8a2a9497c4e414fb4bea21d20ce99b0fdaadfb333895526b8e`  
		Last Modified: Tue, 14 Dec 2021 20:39:52 GMT  
		Size: 40.2 MB (40230838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a916f75ced95121585c99f1bdd61d718b2f36035c24eec0145be385d1b57bfa6`  
		Last Modified: Tue, 14 Dec 2021 20:39:46 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f64d8c3662188233d828bfd67724f06d0e8c34fa06b283f0ade188c81f5d16`  
		Last Modified: Tue, 14 Dec 2021 20:39:46 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d01e24ff602a70f89473df922920c3b2f1f19e3eed68efe936ff140ce0a159c`  
		Last Modified: Tue, 14 Dec 2021 20:39:46 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.10.5`

```console
$ docker pull consul@sha256:e4be41d10951d8adfba93d2d1a92dba879a7c5668fa88ab16593d880e4574e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.10.5` - linux; amd64

```console
$ docker pull consul@sha256:4475b8159e056762094fddccfc4ee04cb2fa27168ab1e2fe5602fc0321797573
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43681368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3539c821b8d51285cccc20d1146f06adcf4eb7462ac74f89c0e29e324cb3e7aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 20:20:45 GMT
ARG CONSUL_VERSION=1.10.5
# Tue, 14 Dec 2021 20:20:45 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.5 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 20:20:45 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 20:20:46 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 20:20:52 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 20:20:54 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 20:20:54 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 20:20:55 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 20:20:55 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 20:20:55 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 20:20:55 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 20:20:55 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 20:20:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 20:20:56 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a31878686a1a40acb3733831b5a7977a1dd15481c4fa1b284f0b2ec7c7d368`  
		Last Modified: Tue, 14 Dec 2021 20:21:42 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8a9b91a9748569616113217fd3037a4404d3e6fed1b00b3fd776da6bf88430`  
		Last Modified: Tue, 14 Dec 2021 20:21:48 GMT  
		Size: 40.9 MB (40855570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44901b3a103ad21cb27e4943d04146ec890159259fd545231fc8edb6b4de44f`  
		Last Modified: Tue, 14 Dec 2021 20:21:42 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964fca1b89e646eeea82bd99676942a41d53336385078346d0d0cb55e52c8f7f`  
		Last Modified: Tue, 14 Dec 2021 20:21:42 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06001403e520ac36329d871362a618fca50e6758455ef4788e34d656a3ab2db4`  
		Last Modified: Tue, 14 Dec 2021 20:21:42 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.5` - linux; arm variant v6

```console
$ docker pull consul@sha256:26f6c9499d42f73064f17b21d437bafc9fa61a3bf57bc7a7bc7540531d95eb3f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41747103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a429113e2ccc547f1ee16878d329fac41000ab084f7b6b11471fd7dafe758982`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 19:49:42 GMT
ARG CONSUL_VERSION=1.10.5
# Tue, 14 Dec 2021 19:49:42 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.5 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 19:49:43 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 19:49:44 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 19:49:59 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 19:50:01 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 19:50:02 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 19:50:03 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 19:50:03 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 19:50:03 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 19:50:04 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 19:50:04 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 19:50:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 19:50:05 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8738eec68152c08f93f0bc71941e91f6fe264b9630c9caba638107049fa1bc4`  
		Last Modified: Tue, 14 Dec 2021 19:52:08 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cfdb687b1dc02c4107c9139d0f53c12cbf3277b217201770d9ae8b2885b88c`  
		Last Modified: Tue, 14 Dec 2021 19:52:28 GMT  
		Size: 39.1 MB (39110381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47fa8e27beaff857f03fc8210cf70f6fabe906382ed2c0339765cadee8c6cbe`  
		Last Modified: Tue, 14 Dec 2021 19:52:08 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c210f4cc2d698fd83ed20044938c48fa52e2cf08e9dfa365e7934863cfe3e94`  
		Last Modified: Tue, 14 Dec 2021 19:52:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f007675b8db5768f9232d3d0f90275fc72f85204b03e85393dd52bd7ee68f7c0`  
		Last Modified: Tue, 14 Dec 2021 19:52:08 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.5` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:56ab516709703801f86014f2c8c01444507fd43032564c5f805d2cad08fe4747
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41699391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50953a41d2fdcad5e29f0cd8a6a1a6a4f6e5ef655e077cf6adbf4ab0cff93221`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 20:42:07 GMT
ARG CONSUL_VERSION=1.10.5
# Tue, 14 Dec 2021 20:42:08 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.5 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 20:42:09 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 20:42:10 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 20:42:21 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 20:42:22 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 20:42:23 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 20:42:24 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 20:42:25 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 20:42:26 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 20:42:27 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 20:42:29 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 20:42:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 20:42:30 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a2c1bd6c357bc002e6a58e4dba209c567c829b5c3d67a98785cc945075c119`  
		Last Modified: Tue, 14 Dec 2021 20:43:44 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeffb4866022338f09341cba456bc786d9a24021b9def25d3c52dfc1b44fc06f`  
		Last Modified: Tue, 14 Dec 2021 20:43:49 GMT  
		Size: 39.0 MB (38976434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00761f25345de261175f4c5295c54ca88591886261a2d8b6df4349fc125c02ee`  
		Last Modified: Tue, 14 Dec 2021 20:43:44 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef726733fba0795bb822948e4c778b0905a5817dece0dab82e9c748f348bd6a`  
		Last Modified: Tue, 14 Dec 2021 20:43:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e926b3c440264449b5bdd90f02c671539c8a02a514fb4c0b00b77b8ee8715c04`  
		Last Modified: Tue, 14 Dec 2021 20:43:44 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.5` - linux; 386

```console
$ docker pull consul@sha256:4f528d2bec02d5a9bd173c1853d1977b0cbc62deba36c3a0c749a750d75208b6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43063020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b8d0dfb97fd1d3e95de17901bec6860d509acc08a8df1e1f2d8b5533b27826`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 20:38:28 GMT
ARG CONSUL_VERSION=1.10.5
# Tue, 14 Dec 2021 20:38:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.5 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 20:38:29 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 20:38:30 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 20:38:38 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 20:38:39 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 20:38:40 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 20:38:41 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 20:38:41 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 20:38:41 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 20:38:41 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 20:38:42 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 20:38:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 20:38:42 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c775a942206ecfd17cfc4806f59ef3add5887dd9bd84253e7df754248313fb`  
		Last Modified: Tue, 14 Dec 2021 20:39:46 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38feef64f936ed8a2a9497c4e414fb4bea21d20ce99b0fdaadfb333895526b8e`  
		Last Modified: Tue, 14 Dec 2021 20:39:52 GMT  
		Size: 40.2 MB (40230838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a916f75ced95121585c99f1bdd61d718b2f36035c24eec0145be385d1b57bfa6`  
		Last Modified: Tue, 14 Dec 2021 20:39:46 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f64d8c3662188233d828bfd67724f06d0e8c34fa06b283f0ade188c81f5d16`  
		Last Modified: Tue, 14 Dec 2021 20:39:46 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d01e24ff602a70f89473df922920c3b2f1f19e3eed68efe936ff140ce0a159c`  
		Last Modified: Tue, 14 Dec 2021 20:39:46 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.11.0-beta`

```console
$ docker pull consul@sha256:b65caa85b885338a6a5ff8f11b5588ccc32f6534329b4ba39191f5d4292d2331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.11.0-beta` - linux; amd64

```console
$ docker pull consul@sha256:52a71ee874601c8950aa28629a35e099bb0dc24847bc0b5d14d13f14cd584360
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43783223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0829aee119e4fdb501973904e56a18ca62c1069d2710b110bb38eabe5249c4a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Tue, 23 Nov 2021 19:19:18 GMT
ARG CONSUL_VERSION=1.11.0-beta3
# Tue, 23 Nov 2021 19:19:18 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.0-beta3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 23 Nov 2021 19:19:18 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 23 Nov 2021 19:19:19 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta3
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 23 Nov 2021 19:19:33 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 23 Nov 2021 19:19:34 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 23 Nov 2021 19:19:35 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 23 Nov 2021 19:19:35 GMT
VOLUME [/consul/data]
# Tue, 23 Nov 2021 19:19:35 GMT
EXPOSE 8300
# Tue, 23 Nov 2021 19:19:36 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 23 Nov 2021 19:19:36 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 23 Nov 2021 19:19:36 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 23 Nov 2021 19:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Nov 2021 19:19:36 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73381c19459765aa22ca5dd0ee5491588020084ecccbddd026ad50ddf056fea5`  
		Last Modified: Tue, 23 Nov 2021 19:20:00 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d17f77e4418b6299e2e1b6b625de81198d2554ea630e8b017af09596ca7465`  
		Last Modified: Tue, 23 Nov 2021 19:20:05 GMT  
		Size: 41.0 MB (40957427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3916d11a8424c9d4f67814e94fd4865297a0fcaf338a8af0d22f9adb8b8f8fce`  
		Last Modified: Tue, 23 Nov 2021 19:20:00 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcf5f99182864f19cdca74347c7c5521f56fc3405125776c327b5688ed5d4ed`  
		Last Modified: Tue, 23 Nov 2021 19:20:00 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905c58ec0ca6ec64894e4aa2aa439d0172207e08be634fee1d4af21b098906ad`  
		Last Modified: Tue, 23 Nov 2021 19:20:00 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11.0-beta` - linux; arm variant v6

```console
$ docker pull consul@sha256:0024e041bcf0aefa04ebe1677b6ad4787787565359e7fb971f7e5fd1c8861191
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41551086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c584a46c47f66ea85020652500bde0e9fad1e9bf0c87a469932d1ec5c98e7f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Tue, 23 Nov 2021 18:49:59 GMT
ARG CONSUL_VERSION=1.11.0-beta3
# Tue, 23 Nov 2021 18:50:00 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.0-beta3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 23 Nov 2021 18:50:00 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 23 Nov 2021 18:50:02 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta3
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 23 Nov 2021 18:50:18 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 23 Nov 2021 18:50:20 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 23 Nov 2021 18:50:21 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 23 Nov 2021 18:50:22 GMT
VOLUME [/consul/data]
# Tue, 23 Nov 2021 18:50:22 GMT
EXPOSE 8300
# Tue, 23 Nov 2021 18:50:23 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 23 Nov 2021 18:50:23 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 23 Nov 2021 18:50:23 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 23 Nov 2021 18:50:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Nov 2021 18:50:24 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ef87264a077c1ecf85fc3a91c5871c49bd30a2ede423401d27fbd8fc6e0d9d`  
		Last Modified: Tue, 23 Nov 2021 18:51:55 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993f03b632272b8c52cebe8fcf9bd308c9c33092e59969822199abc39056dff5`  
		Last Modified: Tue, 23 Nov 2021 18:52:17 GMT  
		Size: 38.9 MB (38914368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859261bff8af64bf1dd074c0db6f66600549a8f0c62916a992a5c22b22f89131`  
		Last Modified: Tue, 23 Nov 2021 18:51:55 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa94cd9ccec3a706f8de8b229a651068dd7a46d684045588d6d8a26fcbc81f40`  
		Last Modified: Tue, 23 Nov 2021 18:51:55 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6047fddf3c992c47996add1b8f01edf00e9d65ba72628a1011ff74e7651e7ac7`  
		Last Modified: Tue, 23 Nov 2021 18:51:56 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11.0-beta` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:2526d50f45d5b1b0eef62c4d3f8bc832b1f21ff1963626a6af80d3579f7234dc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41372190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc21ac26013d490dcb7afd843193b8b68f5b46f4f0bd557f54660fa5da81cb61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Tue, 23 Nov 2021 19:39:23 GMT
ARG CONSUL_VERSION=1.11.0-beta3
# Tue, 23 Nov 2021 19:39:23 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.0-beta3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 23 Nov 2021 19:39:24 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 23 Nov 2021 19:39:25 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta3
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 23 Nov 2021 19:39:38 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 23 Nov 2021 19:39:38 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 23 Nov 2021 19:39:39 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 23 Nov 2021 19:39:40 GMT
VOLUME [/consul/data]
# Tue, 23 Nov 2021 19:39:41 GMT
EXPOSE 8300
# Tue, 23 Nov 2021 19:39:42 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 23 Nov 2021 19:39:43 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 23 Nov 2021 19:39:45 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 23 Nov 2021 19:39:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Nov 2021 19:39:46 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d1ae6c8bcb01b3d601117d2d945d49de0f1b217d29602cd187ae26cee50719`  
		Last Modified: Tue, 23 Nov 2021 19:40:26 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ad6d2e338b5ce664e8890aa919ccd3f6567de48903fe4c71e5d20060a5e0e6`  
		Last Modified: Tue, 23 Nov 2021 19:40:31 GMT  
		Size: 38.6 MB (38649236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c572704fba3032e705c8b61b416877cd7dda2a72997d246c665c97f7bdc4cd24`  
		Last Modified: Tue, 23 Nov 2021 19:40:26 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593c975c48d9650222de382f136a74107f7c6c5c97e2d320c1511433b2a1837e`  
		Last Modified: Tue, 23 Nov 2021 19:40:26 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d3aab2b512665d530fd135f83f267afcf1b1961d0ba64b9c0b3149aa6f70aec`  
		Last Modified: Tue, 23 Nov 2021 19:40:26 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11.0-beta` - linux; 386

```console
$ docker pull consul@sha256:9b717ed38d9d78a3411a23a76f73ec75d08717456042b4e43d8fe8f33e9c6492
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42604671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf90f45c09a1ce18c47c11acbfa96deeacad20c61db2da0880c3d5ac11169e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Tue, 23 Nov 2021 19:38:22 GMT
ARG CONSUL_VERSION=1.11.0-beta3
# Tue, 23 Nov 2021 19:38:23 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.0-beta3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 23 Nov 2021 19:38:23 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 23 Nov 2021 19:38:24 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta3
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 23 Nov 2021 19:38:40 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 23 Nov 2021 19:38:41 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 23 Nov 2021 19:38:42 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 23 Nov 2021 19:38:43 GMT
VOLUME [/consul/data]
# Tue, 23 Nov 2021 19:38:43 GMT
EXPOSE 8300
# Tue, 23 Nov 2021 19:38:43 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 23 Nov 2021 19:38:43 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 23 Nov 2021 19:38:44 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 23 Nov 2021 19:38:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Nov 2021 19:38:44 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61fe9dda4d6ab5d7c90434d71d7a564ab47164e3884d0d0183d97298220b3f4a`  
		Last Modified: Tue, 23 Nov 2021 19:39:25 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444468b267e25ec9f9f22813ed20f5ebb77f06a599f02e8bf03b7a382640aae5`  
		Last Modified: Tue, 23 Nov 2021 19:39:31 GMT  
		Size: 39.8 MB (39772491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136215fa8a89d261b79549ad123d9d89174e378887da6f9ef6698876de4753d3`  
		Last Modified: Tue, 23 Nov 2021 19:39:25 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e978ec332e47545959cfd85eccf817a1753bfe558642403b7e918a94372c1e3f`  
		Last Modified: Tue, 23 Nov 2021 19:39:25 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66521b03ff59815b8d220297fd5e7871811706aec776a78d3e1b137b5d4fa2b4`  
		Last Modified: Tue, 23 Nov 2021 19:39:25 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.11.0-beta3`

```console
$ docker pull consul@sha256:b65caa85b885338a6a5ff8f11b5588ccc32f6534329b4ba39191f5d4292d2331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.11.0-beta3` - linux; amd64

```console
$ docker pull consul@sha256:52a71ee874601c8950aa28629a35e099bb0dc24847bc0b5d14d13f14cd584360
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43783223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0829aee119e4fdb501973904e56a18ca62c1069d2710b110bb38eabe5249c4a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Tue, 23 Nov 2021 19:19:18 GMT
ARG CONSUL_VERSION=1.11.0-beta3
# Tue, 23 Nov 2021 19:19:18 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.0-beta3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 23 Nov 2021 19:19:18 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 23 Nov 2021 19:19:19 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta3
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 23 Nov 2021 19:19:33 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 23 Nov 2021 19:19:34 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 23 Nov 2021 19:19:35 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 23 Nov 2021 19:19:35 GMT
VOLUME [/consul/data]
# Tue, 23 Nov 2021 19:19:35 GMT
EXPOSE 8300
# Tue, 23 Nov 2021 19:19:36 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 23 Nov 2021 19:19:36 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 23 Nov 2021 19:19:36 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 23 Nov 2021 19:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Nov 2021 19:19:36 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73381c19459765aa22ca5dd0ee5491588020084ecccbddd026ad50ddf056fea5`  
		Last Modified: Tue, 23 Nov 2021 19:20:00 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d17f77e4418b6299e2e1b6b625de81198d2554ea630e8b017af09596ca7465`  
		Last Modified: Tue, 23 Nov 2021 19:20:05 GMT  
		Size: 41.0 MB (40957427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3916d11a8424c9d4f67814e94fd4865297a0fcaf338a8af0d22f9adb8b8f8fce`  
		Last Modified: Tue, 23 Nov 2021 19:20:00 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcf5f99182864f19cdca74347c7c5521f56fc3405125776c327b5688ed5d4ed`  
		Last Modified: Tue, 23 Nov 2021 19:20:00 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905c58ec0ca6ec64894e4aa2aa439d0172207e08be634fee1d4af21b098906ad`  
		Last Modified: Tue, 23 Nov 2021 19:20:00 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11.0-beta3` - linux; arm variant v6

```console
$ docker pull consul@sha256:0024e041bcf0aefa04ebe1677b6ad4787787565359e7fb971f7e5fd1c8861191
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41551086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c584a46c47f66ea85020652500bde0e9fad1e9bf0c87a469932d1ec5c98e7f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Tue, 23 Nov 2021 18:49:59 GMT
ARG CONSUL_VERSION=1.11.0-beta3
# Tue, 23 Nov 2021 18:50:00 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.0-beta3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 23 Nov 2021 18:50:00 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 23 Nov 2021 18:50:02 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta3
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 23 Nov 2021 18:50:18 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 23 Nov 2021 18:50:20 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 23 Nov 2021 18:50:21 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 23 Nov 2021 18:50:22 GMT
VOLUME [/consul/data]
# Tue, 23 Nov 2021 18:50:22 GMT
EXPOSE 8300
# Tue, 23 Nov 2021 18:50:23 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 23 Nov 2021 18:50:23 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 23 Nov 2021 18:50:23 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 23 Nov 2021 18:50:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Nov 2021 18:50:24 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ef87264a077c1ecf85fc3a91c5871c49bd30a2ede423401d27fbd8fc6e0d9d`  
		Last Modified: Tue, 23 Nov 2021 18:51:55 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993f03b632272b8c52cebe8fcf9bd308c9c33092e59969822199abc39056dff5`  
		Last Modified: Tue, 23 Nov 2021 18:52:17 GMT  
		Size: 38.9 MB (38914368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859261bff8af64bf1dd074c0db6f66600549a8f0c62916a992a5c22b22f89131`  
		Last Modified: Tue, 23 Nov 2021 18:51:55 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa94cd9ccec3a706f8de8b229a651068dd7a46d684045588d6d8a26fcbc81f40`  
		Last Modified: Tue, 23 Nov 2021 18:51:55 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6047fddf3c992c47996add1b8f01edf00e9d65ba72628a1011ff74e7651e7ac7`  
		Last Modified: Tue, 23 Nov 2021 18:51:56 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11.0-beta3` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:2526d50f45d5b1b0eef62c4d3f8bc832b1f21ff1963626a6af80d3579f7234dc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41372190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc21ac26013d490dcb7afd843193b8b68f5b46f4f0bd557f54660fa5da81cb61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Tue, 23 Nov 2021 19:39:23 GMT
ARG CONSUL_VERSION=1.11.0-beta3
# Tue, 23 Nov 2021 19:39:23 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.0-beta3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 23 Nov 2021 19:39:24 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 23 Nov 2021 19:39:25 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta3
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 23 Nov 2021 19:39:38 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 23 Nov 2021 19:39:38 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 23 Nov 2021 19:39:39 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 23 Nov 2021 19:39:40 GMT
VOLUME [/consul/data]
# Tue, 23 Nov 2021 19:39:41 GMT
EXPOSE 8300
# Tue, 23 Nov 2021 19:39:42 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 23 Nov 2021 19:39:43 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 23 Nov 2021 19:39:45 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 23 Nov 2021 19:39:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Nov 2021 19:39:46 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d1ae6c8bcb01b3d601117d2d945d49de0f1b217d29602cd187ae26cee50719`  
		Last Modified: Tue, 23 Nov 2021 19:40:26 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ad6d2e338b5ce664e8890aa919ccd3f6567de48903fe4c71e5d20060a5e0e6`  
		Last Modified: Tue, 23 Nov 2021 19:40:31 GMT  
		Size: 38.6 MB (38649236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c572704fba3032e705c8b61b416877cd7dda2a72997d246c665c97f7bdc4cd24`  
		Last Modified: Tue, 23 Nov 2021 19:40:26 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593c975c48d9650222de382f136a74107f7c6c5c97e2d320c1511433b2a1837e`  
		Last Modified: Tue, 23 Nov 2021 19:40:26 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d3aab2b512665d530fd135f83f267afcf1b1961d0ba64b9c0b3149aa6f70aec`  
		Last Modified: Tue, 23 Nov 2021 19:40:26 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11.0-beta3` - linux; 386

```console
$ docker pull consul@sha256:9b717ed38d9d78a3411a23a76f73ec75d08717456042b4e43d8fe8f33e9c6492
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42604671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf90f45c09a1ce18c47c11acbfa96deeacad20c61db2da0880c3d5ac11169e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Tue, 23 Nov 2021 19:38:22 GMT
ARG CONSUL_VERSION=1.11.0-beta3
# Tue, 23 Nov 2021 19:38:23 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.0-beta3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 23 Nov 2021 19:38:23 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 23 Nov 2021 19:38:24 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta3
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 23 Nov 2021 19:38:40 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 23 Nov 2021 19:38:41 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 23 Nov 2021 19:38:42 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 23 Nov 2021 19:38:43 GMT
VOLUME [/consul/data]
# Tue, 23 Nov 2021 19:38:43 GMT
EXPOSE 8300
# Tue, 23 Nov 2021 19:38:43 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 23 Nov 2021 19:38:43 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 23 Nov 2021 19:38:44 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 23 Nov 2021 19:38:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Nov 2021 19:38:44 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61fe9dda4d6ab5d7c90434d71d7a564ab47164e3884d0d0183d97298220b3f4a`  
		Last Modified: Tue, 23 Nov 2021 19:39:25 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444468b267e25ec9f9f22813ed20f5ebb77f06a599f02e8bf03b7a382640aae5`  
		Last Modified: Tue, 23 Nov 2021 19:39:31 GMT  
		Size: 39.8 MB (39772491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136215fa8a89d261b79549ad123d9d89174e378887da6f9ef6698876de4753d3`  
		Last Modified: Tue, 23 Nov 2021 19:39:25 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e978ec332e47545959cfd85eccf817a1753bfe558642403b7e918a94372c1e3f`  
		Last Modified: Tue, 23 Nov 2021 19:39:25 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66521b03ff59815b8d220297fd5e7871811706aec776a78d3e1b137b5d4fa2b4`  
		Last Modified: Tue, 23 Nov 2021 19:39:25 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.8`

```console
$ docker pull consul@sha256:eea4e23addc159be441d9b627b98be3f90f1bfe1c437483960c90789321fa86a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.8` - linux; amd64

```console
$ docker pull consul@sha256:0237ef3dd1ed19526b2d564146f48eb6a2d374dc2ae6107bd8039e4e8dcd524b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39625462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d58024b657ac960ba60220f06bfec72fbffae469435c142529e08a9d5404b21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 20:21:14 GMT
ARG CONSUL_VERSION=1.8.18
# Tue, 14 Dec 2021 20:21:15 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.8.18 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 20:21:15 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 20:21:16 GMT
# ARGS: CONSUL_VERSION=1.8.18
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 20:21:21 GMT
# ARGS: CONSUL_VERSION=1.8.18
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 20:21:22 GMT
# ARGS: CONSUL_VERSION=1.8.18
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 20:21:23 GMT
# ARGS: CONSUL_VERSION=1.8.18
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 20:21:23 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 20:21:24 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 20:21:24 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 20:21:24 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 20:21:24 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 20:21:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 20:21:25 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4225e222515a56c2592f391917f8a8cfcf2ea17e324648324ecb80d2f7b9eaea`  
		Last Modified: Tue, 14 Dec 2021 20:22:26 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19738c4da42f24187b6fd0fb85173db3d542b4d115f4db2c2bd9bf4b08f2bf5f`  
		Last Modified: Tue, 14 Dec 2021 20:22:31 GMT  
		Size: 36.8 MB (36799664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9faef3ee9faa025bbaf6595740414ab02e5a77b0c1b14aa09a2f9da1ad0f2e05`  
		Last Modified: Tue, 14 Dec 2021 20:22:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe43cf4ae3b0b75a15a4432f6f77db29d48b910b0d20324236f57f91737195d7`  
		Last Modified: Tue, 14 Dec 2021 20:22:26 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d38c5aefb781292ea8c44979be412147c2e5c37bd35aa21b05169321d9de3969`  
		Last Modified: Tue, 14 Dec 2021 20:22:26 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; arm variant v6

```console
$ docker pull consul@sha256:ca16e9de52bc42274036b93ac1ba22d40c13ff112e0b543daea085dd24c93dca
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 MB (37761971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d9056f4944f3248dd5ed2afe60f3e262d63db8bce97334fa6c463ac390e452`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 19:50:51 GMT
ARG CONSUL_VERSION=1.8.18
# Tue, 14 Dec 2021 19:50:51 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.8.18 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 19:50:51 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 19:50:53 GMT
# ARGS: CONSUL_VERSION=1.8.18
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 19:51:04 GMT
# ARGS: CONSUL_VERSION=1.8.18
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 19:51:06 GMT
# ARGS: CONSUL_VERSION=1.8.18
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 19:51:08 GMT
# ARGS: CONSUL_VERSION=1.8.18
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 19:51:08 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 19:51:09 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 19:51:09 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 19:51:09 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 19:51:10 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 19:51:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 19:51:11 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdf34b7336fc2c298b5bce3f469a542abfdb046db17f73f75514da048d308d3`  
		Last Modified: Tue, 14 Dec 2021 19:53:19 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d3971a463e11d15d7ceef6b01505899a6602902908124023055181f6c32d4e`  
		Last Modified: Tue, 14 Dec 2021 19:53:37 GMT  
		Size: 35.1 MB (35125255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8a409be9e64f07ac679bf7f6f2b53b0e2d417b228ee817bb55e2295219302a`  
		Last Modified: Tue, 14 Dec 2021 19:53:19 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe3c149b532390a0f5e86a021a8946a4a67bb5b286998cce46e03ac8d2aeea0`  
		Last Modified: Tue, 14 Dec 2021 19:53:19 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23bbb98ea46c7b6cd22340d6e6781b6667f594f68820f63b0ced4c69b70e627`  
		Last Modified: Tue, 14 Dec 2021 19:53:19 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:43de21f8618c69393453d6f0d5adc8c11bb6527e4646e51732f58511d86b8940
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37688845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a779498809a7599d2126d6fedfa6beff1bd0d2cdb98a322e95e4603645d67ab6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 20:43:01 GMT
ARG CONSUL_VERSION=1.8.18
# Tue, 14 Dec 2021 20:43:02 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.8.18 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 20:43:03 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 20:43:04 GMT
# ARGS: CONSUL_VERSION=1.8.18
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 20:43:10 GMT
# ARGS: CONSUL_VERSION=1.8.18
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 20:43:11 GMT
# ARGS: CONSUL_VERSION=1.8.18
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 20:43:12 GMT
# ARGS: CONSUL_VERSION=1.8.18
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 20:43:13 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 20:43:14 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 20:43:15 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 20:43:16 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 20:43:18 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 20:43:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 20:43:19 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15918c156e8d4a8918b371f8458f3b32f206e28c5e82f548114e96c728d8601`  
		Last Modified: Tue, 14 Dec 2021 20:44:19 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01bc308c4ae01f355551310bf1c2832c03257ccb692bbfbd45c99257c6c7b70e`  
		Last Modified: Tue, 14 Dec 2021 20:44:24 GMT  
		Size: 35.0 MB (34965890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6addae3d45d9e0a1ad29fa78f4133c51e91c8dc755ae9f358f36f132452298`  
		Last Modified: Tue, 14 Dec 2021 20:44:19 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ceb155592186725faaa460527d57d978b3f01d34ab71800a6d945ef93ddf902`  
		Last Modified: Tue, 14 Dec 2021 20:44:19 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1405987d2fb255abee4a6ee1c518f9d0ab8d31bfec9dea66ebea76f9dab5f0dd`  
		Last Modified: Tue, 14 Dec 2021 20:44:19 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; 386

```console
$ docker pull consul@sha256:1385a4d401eb93f5f9574c33a1e44469d3009e15bf81f6280d254890b62c6cf8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (39019485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3186ece8260bb2b4469e81ee5d577217b31b0306d36c97a0d2c1783bcd2cacab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 20:39:06 GMT
ARG CONSUL_VERSION=1.8.18
# Tue, 14 Dec 2021 20:39:06 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.8.18 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 20:39:06 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 20:39:07 GMT
# ARGS: CONSUL_VERSION=1.8.18
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 20:39:15 GMT
# ARGS: CONSUL_VERSION=1.8.18
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 20:39:16 GMT
# ARGS: CONSUL_VERSION=1.8.18
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 20:39:17 GMT
# ARGS: CONSUL_VERSION=1.8.18
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 20:39:18 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 20:39:18 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 20:39:18 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 20:39:18 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 20:39:19 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 20:39:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 20:39:19 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88d2131fa6612db0bb58a99bb2ea76a55a14a1d062b50ea1fcf666b446c78ae`  
		Last Modified: Tue, 14 Dec 2021 20:40:25 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601c65b117486f6aa9ca666a5cb3f379e2dc97cd8081b217b69328278e5c7d41`  
		Last Modified: Tue, 14 Dec 2021 20:40:31 GMT  
		Size: 36.2 MB (36187302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31747c33dac45d4a153e19f11afbdbeb7fae7608c8a4f339f2dbb304f3dbf073`  
		Last Modified: Tue, 14 Dec 2021 20:40:25 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cd5ac009e9b91138a496dacb1e3c223ca898dd3441db87e85d843ee5e3b82e`  
		Last Modified: Tue, 14 Dec 2021 20:40:25 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a2fbe27afe68e7d13d4c99919fe5939d8730c3006ca62c4bde1df8cc97e4f2`  
		Last Modified: Tue, 14 Dec 2021 20:40:25 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.8.18`

```console
$ docker pull consul@sha256:eea4e23addc159be441d9b627b98be3f90f1bfe1c437483960c90789321fa86a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.8.18` - linux; amd64

```console
$ docker pull consul@sha256:0237ef3dd1ed19526b2d564146f48eb6a2d374dc2ae6107bd8039e4e8dcd524b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39625462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d58024b657ac960ba60220f06bfec72fbffae469435c142529e08a9d5404b21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 20:21:14 GMT
ARG CONSUL_VERSION=1.8.18
# Tue, 14 Dec 2021 20:21:15 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.8.18 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 20:21:15 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 20:21:16 GMT
# ARGS: CONSUL_VERSION=1.8.18
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 20:21:21 GMT
# ARGS: CONSUL_VERSION=1.8.18
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 20:21:22 GMT
# ARGS: CONSUL_VERSION=1.8.18
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 20:21:23 GMT
# ARGS: CONSUL_VERSION=1.8.18
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 20:21:23 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 20:21:24 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 20:21:24 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 20:21:24 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 20:21:24 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 20:21:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 20:21:25 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4225e222515a56c2592f391917f8a8cfcf2ea17e324648324ecb80d2f7b9eaea`  
		Last Modified: Tue, 14 Dec 2021 20:22:26 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19738c4da42f24187b6fd0fb85173db3d542b4d115f4db2c2bd9bf4b08f2bf5f`  
		Last Modified: Tue, 14 Dec 2021 20:22:31 GMT  
		Size: 36.8 MB (36799664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9faef3ee9faa025bbaf6595740414ab02e5a77b0c1b14aa09a2f9da1ad0f2e05`  
		Last Modified: Tue, 14 Dec 2021 20:22:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe43cf4ae3b0b75a15a4432f6f77db29d48b910b0d20324236f57f91737195d7`  
		Last Modified: Tue, 14 Dec 2021 20:22:26 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d38c5aefb781292ea8c44979be412147c2e5c37bd35aa21b05169321d9de3969`  
		Last Modified: Tue, 14 Dec 2021 20:22:26 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.18` - linux; arm variant v6

```console
$ docker pull consul@sha256:ca16e9de52bc42274036b93ac1ba22d40c13ff112e0b543daea085dd24c93dca
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 MB (37761971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d9056f4944f3248dd5ed2afe60f3e262d63db8bce97334fa6c463ac390e452`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 19:50:51 GMT
ARG CONSUL_VERSION=1.8.18
# Tue, 14 Dec 2021 19:50:51 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.8.18 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 19:50:51 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 19:50:53 GMT
# ARGS: CONSUL_VERSION=1.8.18
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 19:51:04 GMT
# ARGS: CONSUL_VERSION=1.8.18
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 19:51:06 GMT
# ARGS: CONSUL_VERSION=1.8.18
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 19:51:08 GMT
# ARGS: CONSUL_VERSION=1.8.18
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 19:51:08 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 19:51:09 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 19:51:09 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 19:51:09 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 19:51:10 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 19:51:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 19:51:11 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdf34b7336fc2c298b5bce3f469a542abfdb046db17f73f75514da048d308d3`  
		Last Modified: Tue, 14 Dec 2021 19:53:19 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d3971a463e11d15d7ceef6b01505899a6602902908124023055181f6c32d4e`  
		Last Modified: Tue, 14 Dec 2021 19:53:37 GMT  
		Size: 35.1 MB (35125255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8a409be9e64f07ac679bf7f6f2b53b0e2d417b228ee817bb55e2295219302a`  
		Last Modified: Tue, 14 Dec 2021 19:53:19 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe3c149b532390a0f5e86a021a8946a4a67bb5b286998cce46e03ac8d2aeea0`  
		Last Modified: Tue, 14 Dec 2021 19:53:19 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23bbb98ea46c7b6cd22340d6e6781b6667f594f68820f63b0ced4c69b70e627`  
		Last Modified: Tue, 14 Dec 2021 19:53:19 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.18` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:43de21f8618c69393453d6f0d5adc8c11bb6527e4646e51732f58511d86b8940
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37688845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a779498809a7599d2126d6fedfa6beff1bd0d2cdb98a322e95e4603645d67ab6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 20:43:01 GMT
ARG CONSUL_VERSION=1.8.18
# Tue, 14 Dec 2021 20:43:02 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.8.18 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 20:43:03 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 20:43:04 GMT
# ARGS: CONSUL_VERSION=1.8.18
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 20:43:10 GMT
# ARGS: CONSUL_VERSION=1.8.18
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 20:43:11 GMT
# ARGS: CONSUL_VERSION=1.8.18
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 20:43:12 GMT
# ARGS: CONSUL_VERSION=1.8.18
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 20:43:13 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 20:43:14 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 20:43:15 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 20:43:16 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 20:43:18 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 20:43:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 20:43:19 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15918c156e8d4a8918b371f8458f3b32f206e28c5e82f548114e96c728d8601`  
		Last Modified: Tue, 14 Dec 2021 20:44:19 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01bc308c4ae01f355551310bf1c2832c03257ccb692bbfbd45c99257c6c7b70e`  
		Last Modified: Tue, 14 Dec 2021 20:44:24 GMT  
		Size: 35.0 MB (34965890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6addae3d45d9e0a1ad29fa78f4133c51e91c8dc755ae9f358f36f132452298`  
		Last Modified: Tue, 14 Dec 2021 20:44:19 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ceb155592186725faaa460527d57d978b3f01d34ab71800a6d945ef93ddf902`  
		Last Modified: Tue, 14 Dec 2021 20:44:19 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1405987d2fb255abee4a6ee1c518f9d0ab8d31bfec9dea66ebea76f9dab5f0dd`  
		Last Modified: Tue, 14 Dec 2021 20:44:19 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.18` - linux; 386

```console
$ docker pull consul@sha256:1385a4d401eb93f5f9574c33a1e44469d3009e15bf81f6280d254890b62c6cf8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (39019485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3186ece8260bb2b4469e81ee5d577217b31b0306d36c97a0d2c1783bcd2cacab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 20:39:06 GMT
ARG CONSUL_VERSION=1.8.18
# Tue, 14 Dec 2021 20:39:06 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.8.18 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 20:39:06 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 20:39:07 GMT
# ARGS: CONSUL_VERSION=1.8.18
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 20:39:15 GMT
# ARGS: CONSUL_VERSION=1.8.18
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 20:39:16 GMT
# ARGS: CONSUL_VERSION=1.8.18
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 20:39:17 GMT
# ARGS: CONSUL_VERSION=1.8.18
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 20:39:18 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 20:39:18 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 20:39:18 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 20:39:18 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 20:39:19 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 20:39:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 20:39:19 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88d2131fa6612db0bb58a99bb2ea76a55a14a1d062b50ea1fcf666b446c78ae`  
		Last Modified: Tue, 14 Dec 2021 20:40:25 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601c65b117486f6aa9ca666a5cb3f379e2dc97cd8081b217b69328278e5c7d41`  
		Last Modified: Tue, 14 Dec 2021 20:40:31 GMT  
		Size: 36.2 MB (36187302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31747c33dac45d4a153e19f11afbdbeb7fae7608c8a4f339f2dbb304f3dbf073`  
		Last Modified: Tue, 14 Dec 2021 20:40:25 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cd5ac009e9b91138a496dacb1e3c223ca898dd3441db87e85d843ee5e3b82e`  
		Last Modified: Tue, 14 Dec 2021 20:40:25 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a2fbe27afe68e7d13d4c99919fe5939d8730c3006ca62c4bde1df8cc97e4f2`  
		Last Modified: Tue, 14 Dec 2021 20:40:25 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9`

```console
$ docker pull consul@sha256:c1401ff3cb72322e72983eb837c0655445f418dfd52842ea50d32d1de9220fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.9` - linux; amd64

```console
$ docker pull consul@sha256:414000fc660049d2566f607e1bb5138e74e3d2bb2ad4f073495418ba35917531
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46347283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b1b850029f6abff01847817129e319da7f85e22ff6ce3ee8452d8d22def883`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 20:20:58 GMT
ARG CONSUL_VERSION=1.9.12
# Tue, 14 Dec 2021 20:20:58 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.12 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 20:20:59 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 20:20:59 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 20:21:07 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 20:21:08 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 20:21:09 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 20:21:09 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 20:21:09 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 20:21:09 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 20:21:09 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 20:21:10 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 20:21:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 20:21:10 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:757ae26b350794d2fa7287fb89434cbe0b66fafab1d8ba1bd6b5b7406d0ae111`  
		Last Modified: Tue, 14 Dec 2021 20:22:00 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4ba7257335ed3cc6d28ec7be06c9965df9d90cd1821024371221a0b315425d`  
		Last Modified: Tue, 14 Dec 2021 20:22:06 GMT  
		Size: 43.5 MB (43521487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e034957fd950b917007c48bd9777c799d472a17116b5a6a4305e83cb22c2144`  
		Last Modified: Tue, 14 Dec 2021 20:22:00 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ddc88c68c55accb56303e9bb0bbe718f3aeff268b447260af5502b8b30d49d7`  
		Last Modified: Tue, 14 Dec 2021 20:22:00 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64b78141e0daaf4545c9403bcf81891f8b5456e2c00e3eee3ae5ce73908552c`  
		Last Modified: Tue, 14 Dec 2021 20:22:00 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; arm variant v6

```console
$ docker pull consul@sha256:a7105c62cfb3f0e40ba51cb4a7a51d909694a6cc218213e8e5e88839743b9f22
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43630043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ebf8bd2a2f91043ea2800786b2704e71df2576168d75614baedccb327857e20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 19:50:18 GMT
ARG CONSUL_VERSION=1.9.12
# Tue, 14 Dec 2021 19:50:18 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.12 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 19:50:19 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 19:50:20 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 19:50:33 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 19:50:35 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 19:50:36 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 19:50:37 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 19:50:37 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 19:50:38 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 19:50:38 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 19:50:39 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 19:50:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 19:50:39 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738aaaed04bbd7697fdeaa9d74a8accd8958ed8179919906c5b737f6f836cbe0`  
		Last Modified: Tue, 14 Dec 2021 19:52:44 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11aa60632f4b82d88ecbc5d28163c03404c0266707d9b231ffad298fa1bae3f0`  
		Last Modified: Tue, 14 Dec 2021 19:53:06 GMT  
		Size: 41.0 MB (40993320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d7330cf0a1f14d749ce5047705ee3383d1b9cecd6031edcfaa1dfebf3d5954c`  
		Last Modified: Tue, 14 Dec 2021 19:52:44 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d426972319eebc1a0fe09d30b557863794f1d16a309451e35c4b7ca3c8e2d6`  
		Last Modified: Tue, 14 Dec 2021 19:52:44 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5c5118bab9327394112ea78c084e7e160abcdf72c22555468f9e8eac0f2fcc`  
		Last Modified: Tue, 14 Dec 2021 19:52:44 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:25ca83fd0b136d9f122c03d25f63f42e08395e49dbb7a2649bf7c23f6b324dcb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43917815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ed12ef44ef801c92388227129b79c623b47bba97f0d109dc940cf95c14c621`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 20:42:38 GMT
ARG CONSUL_VERSION=1.9.12
# Tue, 14 Dec 2021 20:42:39 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.12 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 20:42:40 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 20:42:41 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 20:42:48 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 20:42:48 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 20:42:49 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 20:42:50 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 20:42:51 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 20:42:52 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 20:42:53 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 20:42:55 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 20:42:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 20:42:56 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08fd8ec1ab1ca61fd03e0b39e52ba153f0052bf13c3466094a6a26779fed8c2`  
		Last Modified: Tue, 14 Dec 2021 20:44:03 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3bf82943d743f743e3f356b5bc9a5ff3cde6f0e3e1e3d203f4a4f91757c91f`  
		Last Modified: Tue, 14 Dec 2021 20:44:08 GMT  
		Size: 41.2 MB (41194864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a999ae667c9bcb8227f07b7c61c9aae978a328cd3256003672bf1cf0d8bf05d`  
		Last Modified: Tue, 14 Dec 2021 20:44:03 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1d6502de310c0cd222ce8b76b1de977e73bb28d465f44ea9db4adbb69e723a`  
		Last Modified: Tue, 14 Dec 2021 20:44:03 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbc67176a0724ecdb3bfebf97423fa213a6275c6b7514cc0b90baa6aad1bed`  
		Last Modified: Tue, 14 Dec 2021 20:44:03 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; 386

```console
$ docker pull consul@sha256:5bb412b4e60ea4b1890b4a54b91a8a1f627380965c1ad965944ec31a641e3caa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45728780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3860d9bbc588dc8f7010b7bfcb80a248dc155327801cfb06aba563ca8645e1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 20:38:48 GMT
ARG CONSUL_VERSION=1.9.12
# Tue, 14 Dec 2021 20:38:49 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.12 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 20:38:49 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 20:38:50 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 20:38:57 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 20:38:58 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 20:38:59 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 20:38:59 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 20:39:00 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 20:39:00 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 20:39:00 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 20:39:01 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 20:39:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 20:39:01 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d99b58bd55e9a552c1b5df8ad17486a4dfea641ded9190dc2068da8a525944`  
		Last Modified: Tue, 14 Dec 2021 20:40:07 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0842f2031276fce7ab6cc94d8215180a1c6535ca04883da838937d62f0af9f`  
		Last Modified: Tue, 14 Dec 2021 20:40:14 GMT  
		Size: 42.9 MB (42896600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc80f747f1b2611b42db8f51d5fefea94c70103585b856281b5bed1d23c3af26`  
		Last Modified: Tue, 14 Dec 2021 20:40:07 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6507305b927578884055029b7d8729ece2610479e23564e6e864dc86f502b08`  
		Last Modified: Tue, 14 Dec 2021 20:40:07 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3450ca70d07687f9dd9db2509f7490bdb3f0e1ed3c13b416f1dbec8acaece95`  
		Last Modified: Tue, 14 Dec 2021 20:40:07 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9.12`

```console
$ docker pull consul@sha256:c1401ff3cb72322e72983eb837c0655445f418dfd52842ea50d32d1de9220fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.9.12` - linux; amd64

```console
$ docker pull consul@sha256:414000fc660049d2566f607e1bb5138e74e3d2bb2ad4f073495418ba35917531
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46347283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b1b850029f6abff01847817129e319da7f85e22ff6ce3ee8452d8d22def883`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 20:20:58 GMT
ARG CONSUL_VERSION=1.9.12
# Tue, 14 Dec 2021 20:20:58 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.12 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 20:20:59 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 20:20:59 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 20:21:07 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 20:21:08 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 20:21:09 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 20:21:09 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 20:21:09 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 20:21:09 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 20:21:09 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 20:21:10 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 20:21:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 20:21:10 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:757ae26b350794d2fa7287fb89434cbe0b66fafab1d8ba1bd6b5b7406d0ae111`  
		Last Modified: Tue, 14 Dec 2021 20:22:00 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4ba7257335ed3cc6d28ec7be06c9965df9d90cd1821024371221a0b315425d`  
		Last Modified: Tue, 14 Dec 2021 20:22:06 GMT  
		Size: 43.5 MB (43521487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e034957fd950b917007c48bd9777c799d472a17116b5a6a4305e83cb22c2144`  
		Last Modified: Tue, 14 Dec 2021 20:22:00 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ddc88c68c55accb56303e9bb0bbe718f3aeff268b447260af5502b8b30d49d7`  
		Last Modified: Tue, 14 Dec 2021 20:22:00 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64b78141e0daaf4545c9403bcf81891f8b5456e2c00e3eee3ae5ce73908552c`  
		Last Modified: Tue, 14 Dec 2021 20:22:00 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.12` - linux; arm variant v6

```console
$ docker pull consul@sha256:a7105c62cfb3f0e40ba51cb4a7a51d909694a6cc218213e8e5e88839743b9f22
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43630043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ebf8bd2a2f91043ea2800786b2704e71df2576168d75614baedccb327857e20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 19:50:18 GMT
ARG CONSUL_VERSION=1.9.12
# Tue, 14 Dec 2021 19:50:18 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.12 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 19:50:19 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 19:50:20 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 19:50:33 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 19:50:35 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 19:50:36 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 19:50:37 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 19:50:37 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 19:50:38 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 19:50:38 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 19:50:39 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 19:50:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 19:50:39 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738aaaed04bbd7697fdeaa9d74a8accd8958ed8179919906c5b737f6f836cbe0`  
		Last Modified: Tue, 14 Dec 2021 19:52:44 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11aa60632f4b82d88ecbc5d28163c03404c0266707d9b231ffad298fa1bae3f0`  
		Last Modified: Tue, 14 Dec 2021 19:53:06 GMT  
		Size: 41.0 MB (40993320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d7330cf0a1f14d749ce5047705ee3383d1b9cecd6031edcfaa1dfebf3d5954c`  
		Last Modified: Tue, 14 Dec 2021 19:52:44 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d426972319eebc1a0fe09d30b557863794f1d16a309451e35c4b7ca3c8e2d6`  
		Last Modified: Tue, 14 Dec 2021 19:52:44 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5c5118bab9327394112ea78c084e7e160abcdf72c22555468f9e8eac0f2fcc`  
		Last Modified: Tue, 14 Dec 2021 19:52:44 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.12` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:25ca83fd0b136d9f122c03d25f63f42e08395e49dbb7a2649bf7c23f6b324dcb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43917815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ed12ef44ef801c92388227129b79c623b47bba97f0d109dc940cf95c14c621`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 20:42:38 GMT
ARG CONSUL_VERSION=1.9.12
# Tue, 14 Dec 2021 20:42:39 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.12 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 20:42:40 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 20:42:41 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 20:42:48 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 20:42:48 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 20:42:49 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 20:42:50 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 20:42:51 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 20:42:52 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 20:42:53 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 20:42:55 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 20:42:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 20:42:56 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08fd8ec1ab1ca61fd03e0b39e52ba153f0052bf13c3466094a6a26779fed8c2`  
		Last Modified: Tue, 14 Dec 2021 20:44:03 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3bf82943d743f743e3f356b5bc9a5ff3cde6f0e3e1e3d203f4a4f91757c91f`  
		Last Modified: Tue, 14 Dec 2021 20:44:08 GMT  
		Size: 41.2 MB (41194864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a999ae667c9bcb8227f07b7c61c9aae978a328cd3256003672bf1cf0d8bf05d`  
		Last Modified: Tue, 14 Dec 2021 20:44:03 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1d6502de310c0cd222ce8b76b1de977e73bb28d465f44ea9db4adbb69e723a`  
		Last Modified: Tue, 14 Dec 2021 20:44:03 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbc67176a0724ecdb3bfebf97423fa213a6275c6b7514cc0b90baa6aad1bed`  
		Last Modified: Tue, 14 Dec 2021 20:44:03 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.12` - linux; 386

```console
$ docker pull consul@sha256:5bb412b4e60ea4b1890b4a54b91a8a1f627380965c1ad965944ec31a641e3caa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45728780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3860d9bbc588dc8f7010b7bfcb80a248dc155327801cfb06aba563ca8645e1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 20:38:48 GMT
ARG CONSUL_VERSION=1.9.12
# Tue, 14 Dec 2021 20:38:49 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.12 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 20:38:49 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 20:38:50 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 20:38:57 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 20:38:58 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 20:38:59 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 20:38:59 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 20:39:00 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 20:39:00 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 20:39:00 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 20:39:01 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 20:39:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 20:39:01 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d99b58bd55e9a552c1b5df8ad17486a4dfea641ded9190dc2068da8a525944`  
		Last Modified: Tue, 14 Dec 2021 20:40:07 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0842f2031276fce7ab6cc94d8215180a1c6535ca04883da838937d62f0af9f`  
		Last Modified: Tue, 14 Dec 2021 20:40:14 GMT  
		Size: 42.9 MB (42896600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc80f747f1b2611b42db8f51d5fefea94c70103585b856281b5bed1d23c3af26`  
		Last Modified: Tue, 14 Dec 2021 20:40:07 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6507305b927578884055029b7d8729ece2610479e23564e6e864dc86f502b08`  
		Last Modified: Tue, 14 Dec 2021 20:40:07 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3450ca70d07687f9dd9db2509f7490bdb3f0e1ed3c13b416f1dbec8acaece95`  
		Last Modified: Tue, 14 Dec 2021 20:40:07 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:latest`

```console
$ docker pull consul@sha256:e4be41d10951d8adfba93d2d1a92dba879a7c5668fa88ab16593d880e4574e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:latest` - linux; amd64

```console
$ docker pull consul@sha256:4475b8159e056762094fddccfc4ee04cb2fa27168ab1e2fe5602fc0321797573
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43681368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3539c821b8d51285cccc20d1146f06adcf4eb7462ac74f89c0e29e324cb3e7aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 20:20:45 GMT
ARG CONSUL_VERSION=1.10.5
# Tue, 14 Dec 2021 20:20:45 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.5 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 20:20:45 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 20:20:46 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 20:20:52 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 20:20:54 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 20:20:54 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 20:20:55 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 20:20:55 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 20:20:55 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 20:20:55 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 20:20:55 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 20:20:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 20:20:56 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a31878686a1a40acb3733831b5a7977a1dd15481c4fa1b284f0b2ec7c7d368`  
		Last Modified: Tue, 14 Dec 2021 20:21:42 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8a9b91a9748569616113217fd3037a4404d3e6fed1b00b3fd776da6bf88430`  
		Last Modified: Tue, 14 Dec 2021 20:21:48 GMT  
		Size: 40.9 MB (40855570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44901b3a103ad21cb27e4943d04146ec890159259fd545231fc8edb6b4de44f`  
		Last Modified: Tue, 14 Dec 2021 20:21:42 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964fca1b89e646eeea82bd99676942a41d53336385078346d0d0cb55e52c8f7f`  
		Last Modified: Tue, 14 Dec 2021 20:21:42 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06001403e520ac36329d871362a618fca50e6758455ef4788e34d656a3ab2db4`  
		Last Modified: Tue, 14 Dec 2021 20:21:42 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm variant v6

```console
$ docker pull consul@sha256:26f6c9499d42f73064f17b21d437bafc9fa61a3bf57bc7a7bc7540531d95eb3f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41747103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a429113e2ccc547f1ee16878d329fac41000ab084f7b6b11471fd7dafe758982`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 19:49:42 GMT
ARG CONSUL_VERSION=1.10.5
# Tue, 14 Dec 2021 19:49:42 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.5 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 19:49:43 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 19:49:44 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 19:49:59 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 19:50:01 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 19:50:02 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 19:50:03 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 19:50:03 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 19:50:03 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 19:50:04 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 19:50:04 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 19:50:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 19:50:05 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8738eec68152c08f93f0bc71941e91f6fe264b9630c9caba638107049fa1bc4`  
		Last Modified: Tue, 14 Dec 2021 19:52:08 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cfdb687b1dc02c4107c9139d0f53c12cbf3277b217201770d9ae8b2885b88c`  
		Last Modified: Tue, 14 Dec 2021 19:52:28 GMT  
		Size: 39.1 MB (39110381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47fa8e27beaff857f03fc8210cf70f6fabe906382ed2c0339765cadee8c6cbe`  
		Last Modified: Tue, 14 Dec 2021 19:52:08 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c210f4cc2d698fd83ed20044938c48fa52e2cf08e9dfa365e7934863cfe3e94`  
		Last Modified: Tue, 14 Dec 2021 19:52:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f007675b8db5768f9232d3d0f90275fc72f85204b03e85393dd52bd7ee68f7c0`  
		Last Modified: Tue, 14 Dec 2021 19:52:08 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:56ab516709703801f86014f2c8c01444507fd43032564c5f805d2cad08fe4747
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41699391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50953a41d2fdcad5e29f0cd8a6a1a6a4f6e5ef655e077cf6adbf4ab0cff93221`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 20:42:07 GMT
ARG CONSUL_VERSION=1.10.5
# Tue, 14 Dec 2021 20:42:08 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.5 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 20:42:09 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 20:42:10 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 20:42:21 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 20:42:22 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 20:42:23 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 20:42:24 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 20:42:25 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 20:42:26 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 20:42:27 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 20:42:29 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 20:42:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 20:42:30 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a2c1bd6c357bc002e6a58e4dba209c567c829b5c3d67a98785cc945075c119`  
		Last Modified: Tue, 14 Dec 2021 20:43:44 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeffb4866022338f09341cba456bc786d9a24021b9def25d3c52dfc1b44fc06f`  
		Last Modified: Tue, 14 Dec 2021 20:43:49 GMT  
		Size: 39.0 MB (38976434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00761f25345de261175f4c5295c54ca88591886261a2d8b6df4349fc125c02ee`  
		Last Modified: Tue, 14 Dec 2021 20:43:44 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef726733fba0795bb822948e4c778b0905a5817dece0dab82e9c748f348bd6a`  
		Last Modified: Tue, 14 Dec 2021 20:43:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e926b3c440264449b5bdd90f02c671539c8a02a514fb4c0b00b77b8ee8715c04`  
		Last Modified: Tue, 14 Dec 2021 20:43:44 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; 386

```console
$ docker pull consul@sha256:4f528d2bec02d5a9bd173c1853d1977b0cbc62deba36c3a0c749a750d75208b6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43063020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b8d0dfb97fd1d3e95de17901bec6860d509acc08a8df1e1f2d8b5533b27826`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 20:38:28 GMT
ARG CONSUL_VERSION=1.10.5
# Tue, 14 Dec 2021 20:38:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.5 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 20:38:29 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 20:38:30 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 20:38:38 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 20:38:39 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 20:38:40 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 20:38:41 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 20:38:41 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 20:38:41 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 20:38:41 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 20:38:42 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 20:38:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 20:38:42 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c775a942206ecfd17cfc4806f59ef3add5887dd9bd84253e7df754248313fb`  
		Last Modified: Tue, 14 Dec 2021 20:39:46 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38feef64f936ed8a2a9497c4e414fb4bea21d20ce99b0fdaadfb333895526b8e`  
		Last Modified: Tue, 14 Dec 2021 20:39:52 GMT  
		Size: 40.2 MB (40230838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a916f75ced95121585c99f1bdd61d718b2f36035c24eec0145be385d1b57bfa6`  
		Last Modified: Tue, 14 Dec 2021 20:39:46 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f64d8c3662188233d828bfd67724f06d0e8c34fa06b283f0ade188c81f5d16`  
		Last Modified: Tue, 14 Dec 2021 20:39:46 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d01e24ff602a70f89473df922920c3b2f1f19e3eed68efe936ff140ce0a159c`  
		Last Modified: Tue, 14 Dec 2021 20:39:46 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
