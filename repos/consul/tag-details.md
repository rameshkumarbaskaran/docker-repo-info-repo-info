<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `consul`

-	[`consul:1.6`](#consul16)
-	[`consul:1.6.9`](#consul169)
-	[`consul:1.7`](#consul17)
-	[`consul:1.7.8`](#consul178)
-	[`consul:1.8`](#consul18)
-	[`consul:1.8.4`](#consul184)
-	[`consul:latest`](#consullatest)

## `consul:1.6`

```console
$ docker pull consul@sha256:b82a6c65621662f4bb978d9b6721af2c42e44c2b03fe4145ee9feffec0687bfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.6` - linux; amd64

```console
$ docker pull consul@sha256:b218372f1a4f734ba18854b70aeffde0259b9c5cb870a695b6686928530c07a8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42259073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ff071ff9806fc2edca099100007ad99b1c7acafc8757c863d6512e224651db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Fri, 31 Jul 2020 18:22:03 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 12 Aug 2020 23:19:49 GMT
ENV CONSUL_VERSION=1.6.8
# Wed, 12 Aug 2020 23:19:49 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 12 Aug 2020 23:19:50 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 12 Aug 2020 23:19:54 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 12 Aug 2020 23:19:55 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 12 Aug 2020 23:19:55 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 12 Aug 2020 23:19:56 GMT
VOLUME [/consul/data]
# Wed, 12 Aug 2020 23:19:56 GMT
EXPOSE 8300
# Wed, 12 Aug 2020 23:19:56 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 12 Aug 2020 23:19:56 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 12 Aug 2020 23:19:56 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 12 Aug 2020 23:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Aug 2020 23:19:57 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1cdaf14ceed1ef9be8b478aa4905fcfb75f941c79389ac1d76bc29cec3c301`  
		Last Modified: Wed, 12 Aug 2020 23:20:32 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c333adfe037a1097c919f3ec5beb5b510afa4f528c8b5be2f2ac4f812698220`  
		Last Modified: Wed, 12 Aug 2020 23:20:40 GMT  
		Size: 39.5 MB (39458296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2912b97906f7842b1578d516222b09b92bde1fddc33786a7644debc244760b0c`  
		Last Modified: Wed, 12 Aug 2020 23:20:30 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e1c36068dc8fb356108b8e9456ef73745e054e4df0db341fc92914f5a04914`  
		Last Modified: Wed, 12 Aug 2020 23:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b05d00f70ea79d0b256ed0b1d9e10ea61b2a7a80f06b01b6adc3e81ccdc3dbe`  
		Last Modified: Wed, 12 Aug 2020 23:20:30 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.6` - linux; arm variant v6

```console
$ docker pull consul@sha256:d1b234763bc339b9a12a6b9785ed3e72e65b0a6d605bef8891fa5bcdfc49eba0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37937989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:027d81057134e497189496564bbd4c442b07d593dd9c56234c766a3758974827`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Fri, 31 Jul 2020 17:49:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 11 Sep 2020 20:50:27 GMT
ENV CONSUL_VERSION=1.6.9
# Fri, 11 Sep 2020 20:50:28 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 11 Sep 2020 20:50:31 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 11 Sep 2020 20:50:40 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 11 Sep 2020 20:50:43 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 11 Sep 2020 20:50:45 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Sep 2020 20:50:46 GMT
VOLUME [/consul/data]
# Fri, 11 Sep 2020 20:50:47 GMT
EXPOSE 8300
# Fri, 11 Sep 2020 20:50:50 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 11 Sep 2020 20:50:51 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 11 Sep 2020 20:50:51 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 11 Sep 2020 20:50:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Sep 2020 20:50:53 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b94ec3f0f3e01d39f7033e85747937598cefb6de79886a6838240a7caa0f681`  
		Last Modified: Fri, 11 Sep 2020 20:51:43 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5006ee3d86dbdcb2110b01e5c30cab655a34754ff1f55d24fd241c8c8046bcc8`  
		Last Modified: Fri, 11 Sep 2020 20:51:52 GMT  
		Size: 35.3 MB (35331410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaeb914a71dcf59c42cf45f0b1e8ae8cedb7dafe092966f06c57ca57f0ea49c6`  
		Last Modified: Fri, 11 Sep 2020 20:51:43 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed51e56effe49113c5b99cbaa51a35e7bb73d979d74f6cfb64432c7f1b6856a2`  
		Last Modified: Fri, 11 Sep 2020 20:51:43 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ead4b852bd4afca40cbf71ee888422c765f0ad6801a16989f922221ddeccd2`  
		Last Modified: Fri, 11 Sep 2020 20:51:43 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.6` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:30bf2cb26d9d8ff09c87b44c4f914192dcbd1ef61eed0c94659dfa944ab59cec
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38162371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:294ecd37947292352e701d468c80f3ed988f7dd448ead37444f6c95bc1dcf3df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Fri, 31 Jul 2020 17:42:27 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 12 Aug 2020 22:40:25 GMT
ENV CONSUL_VERSION=1.6.8
# Wed, 12 Aug 2020 22:40:25 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 12 Aug 2020 22:40:27 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 12 Aug 2020 22:40:35 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 12 Aug 2020 22:40:37 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 12 Aug 2020 22:40:46 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 12 Aug 2020 22:40:48 GMT
VOLUME [/consul/data]
# Wed, 12 Aug 2020 22:40:49 GMT
EXPOSE 8300
# Wed, 12 Aug 2020 22:40:49 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 12 Aug 2020 22:40:50 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 12 Aug 2020 22:40:51 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 12 Aug 2020 22:40:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Aug 2020 22:40:52 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b538f80385f9b48122e3da068c932a96ea5018afa3c7be79da00437414bd18cd`  
		Last Modified: Fri, 29 May 2020 21:43:57 GMT  
		Size: 2.7 MB (2707964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21d2de38027b1095b9c96fa34af3bf782183ccb38e039f9583e3f71a1fdeb2a`  
		Last Modified: Wed, 12 Aug 2020 22:41:42 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e451565ab97118d95ae810f945c4fee8af5d388592d450c46e74b7a7adc797c`  
		Last Modified: Wed, 12 Aug 2020 22:41:51 GMT  
		Size: 35.5 MB (35451112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7eefb9a969d185d8f570b9164d40639e182ff8197fa1c1eadb544a41623f62`  
		Last Modified: Wed, 12 Aug 2020 22:41:42 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491a4bbba720985e6b6355bc091bba3c672645e683d2f52bddfc7d5df725f366`  
		Last Modified: Wed, 12 Aug 2020 22:41:42 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aaa06b441fbb995cc633698b736cd88ec5184a8f983183e18fe0da9ac98060b`  
		Last Modified: Wed, 12 Aug 2020 22:41:42 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.6` - linux; 386

```console
$ docker pull consul@sha256:d14e5551bd1059106134f334837ccb3fd5435271d457f1be97ba2100c71e5432
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41086187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4fbb243d40d76b0b70545f8684bf59551947d2cbc49abc5aa7fe289ff0b2705`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 29 May 2020 21:38:33 GMT
ADD file:5624441d97aca5eeb82a582941efc3586397098b8391227a9040ebe434cc1d6b in / 
# Fri, 29 May 2020 21:38:33 GMT
CMD ["/bin/sh"]
# Fri, 31 Jul 2020 17:38:31 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 12 Aug 2020 22:38:48 GMT
ENV CONSUL_VERSION=1.6.8
# Wed, 12 Aug 2020 22:38:48 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 12 Aug 2020 22:38:49 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 12 Aug 2020 22:38:54 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 12 Aug 2020 22:38:54 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 12 Aug 2020 22:38:55 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 12 Aug 2020 22:38:55 GMT
VOLUME [/consul/data]
# Wed, 12 Aug 2020 22:38:55 GMT
EXPOSE 8300
# Wed, 12 Aug 2020 22:38:56 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 12 Aug 2020 22:38:56 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 12 Aug 2020 22:38:56 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 12 Aug 2020 22:38:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Aug 2020 22:38:56 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0625b4155e2a59f647ece47c0cd77ed3196b1f84454fa64ce80cad90e2b9b79e`  
		Last Modified: Fri, 29 May 2020 21:38:53 GMT  
		Size: 2.8 MB (2792298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e3f5b5cfcd4f4a336ad49cfaebed58b223ae207713568d44a1c5faa8bc59dc`  
		Last Modified: Wed, 12 Aug 2020 22:39:30 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f6e90b416fae9821858323a8a84e6dd9b77bdbf92bd84cf02ef0126098afc3`  
		Last Modified: Wed, 12 Aug 2020 22:39:37 GMT  
		Size: 38.3 MB (38290653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f388426c2fc856f01be5cc485a166f1320f1413f41b61f61ebc988878912a0d8`  
		Last Modified: Wed, 12 Aug 2020 22:39:29 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716320c8e70fae76d02982d36900d181086b2ebae51f0ef3ebc01f1b5c76b44c`  
		Last Modified: Wed, 12 Aug 2020 22:39:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa5dd075b219159556ad337e0f2e45d9406b1af737b953a129a24713381e529e`  
		Last Modified: Wed, 12 Aug 2020 22:39:29 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.6.9`

```console
$ docker pull consul@sha256:3d3b17ad24db3a72efcbc6476db1d72e7cff083e6959f8b294535a852d2db967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm variant v6

### `consul:1.6.9` - linux; arm variant v6

```console
$ docker pull consul@sha256:d1b234763bc339b9a12a6b9785ed3e72e65b0a6d605bef8891fa5bcdfc49eba0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37937989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:027d81057134e497189496564bbd4c442b07d593dd9c56234c766a3758974827`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Fri, 31 Jul 2020 17:49:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 11 Sep 2020 20:50:27 GMT
ENV CONSUL_VERSION=1.6.9
# Fri, 11 Sep 2020 20:50:28 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 11 Sep 2020 20:50:31 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 11 Sep 2020 20:50:40 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 11 Sep 2020 20:50:43 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 11 Sep 2020 20:50:45 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Sep 2020 20:50:46 GMT
VOLUME [/consul/data]
# Fri, 11 Sep 2020 20:50:47 GMT
EXPOSE 8300
# Fri, 11 Sep 2020 20:50:50 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 11 Sep 2020 20:50:51 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 11 Sep 2020 20:50:51 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 11 Sep 2020 20:50:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Sep 2020 20:50:53 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b94ec3f0f3e01d39f7033e85747937598cefb6de79886a6838240a7caa0f681`  
		Last Modified: Fri, 11 Sep 2020 20:51:43 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5006ee3d86dbdcb2110b01e5c30cab655a34754ff1f55d24fd241c8c8046bcc8`  
		Last Modified: Fri, 11 Sep 2020 20:51:52 GMT  
		Size: 35.3 MB (35331410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaeb914a71dcf59c42cf45f0b1e8ae8cedb7dafe092966f06c57ca57f0ea49c6`  
		Last Modified: Fri, 11 Sep 2020 20:51:43 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed51e56effe49113c5b99cbaa51a35e7bb73d979d74f6cfb64432c7f1b6856a2`  
		Last Modified: Fri, 11 Sep 2020 20:51:43 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ead4b852bd4afca40cbf71ee888422c765f0ad6801a16989f922221ddeccd2`  
		Last Modified: Fri, 11 Sep 2020 20:51:43 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.7`

```console
$ docker pull consul@sha256:60bf1026e2fe61f0f9c19780713623920b42843aa06d9a8f0fd14c9ef5d835f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.7` - linux; amd64

```console
$ docker pull consul@sha256:f072e8083af714d0bf5904d3baaf53a66da7ffb15685b5d6d4d4602412f0f9e8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43639234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd3070b7b81e1e0de45be441cfeae38bce7a83e0e08ed5693b636ca0777efde2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Fri, 31 Jul 2020 18:22:03 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 12 Aug 2020 23:19:37 GMT
ENV CONSUL_VERSION=1.7.7
# Wed, 12 Aug 2020 23:19:37 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 12 Aug 2020 23:19:38 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 12 Aug 2020 23:19:42 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 12 Aug 2020 23:19:43 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 12 Aug 2020 23:19:43 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 12 Aug 2020 23:19:44 GMT
VOLUME [/consul/data]
# Wed, 12 Aug 2020 23:19:44 GMT
EXPOSE 8300
# Wed, 12 Aug 2020 23:19:44 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 12 Aug 2020 23:19:44 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 12 Aug 2020 23:19:44 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 12 Aug 2020 23:19:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Aug 2020 23:19:45 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82536e679949e1ae83aaddc7d54e09ad6fdfd59d3b16c934c8dad419266d8f61`  
		Last Modified: Wed, 12 Aug 2020 23:20:20 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d0e794c78f5c3fd0337b4abed3a1940d9340e6bf1f3cdbcd76c1878149c7f2`  
		Last Modified: Wed, 12 Aug 2020 23:20:26 GMT  
		Size: 40.8 MB (40838459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d439c5eb4ab1a9df89a94b902058e921a5ba1119446526d98313f918fb966dcb`  
		Last Modified: Wed, 12 Aug 2020 23:20:19 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f593bfcc55903cf12a6342d6249eb603de1cb27e74d486f2806a3c51d9680ef2`  
		Last Modified: Wed, 12 Aug 2020 23:20:20 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbaee936ad1b0b84be1c74e0129dd757c5e14696ee32ccafa0d158ad4b9286cf`  
		Last Modified: Wed, 12 Aug 2020 23:20:20 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7` - linux; arm variant v6

```console
$ docker pull consul@sha256:71cba28e62ec10592039ceb72a8511b55c8f2666b39217047180e9fea9e3de81
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39303513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f5e1daef07fc68c15b6937c0599fbd72ada85bb6c790cd7b514ea700a63e59e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Fri, 31 Jul 2020 17:49:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 11 Sep 2020 20:49:56 GMT
ENV CONSUL_VERSION=1.7.8
# Fri, 11 Sep 2020 20:49:56 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 11 Sep 2020 20:49:59 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 11 Sep 2020 20:50:08 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 11 Sep 2020 20:50:11 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 11 Sep 2020 20:50:13 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Sep 2020 20:50:14 GMT
VOLUME [/consul/data]
# Fri, 11 Sep 2020 20:50:15 GMT
EXPOSE 8300
# Fri, 11 Sep 2020 20:50:16 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 11 Sep 2020 20:50:17 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 11 Sep 2020 20:50:17 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 11 Sep 2020 20:50:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Sep 2020 20:50:21 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6844b3063c1a2bd33f1ab8dc40b11e5ea7bff6199f137b4ca0aa498993b51f53`  
		Last Modified: Fri, 11 Sep 2020 20:51:27 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944802fa2b60e84bd8a4d90ab67877d67179e75fe2be2a4c0753a08919a52f50`  
		Last Modified: Fri, 11 Sep 2020 20:51:37 GMT  
		Size: 36.7 MB (36696932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ed00f247e4c41021efcf87e6cbda128e3adc528d414cf7bfba027ead33e923`  
		Last Modified: Fri, 11 Sep 2020 20:51:27 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58cb41dbdda2d745c0e2c9997f9824a322e57e9dc601e67264198a27796422ad`  
		Last Modified: Fri, 11 Sep 2020 20:51:27 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377efeb788858a4e3d8de19182644ac7282efa8311db9d1c5d8224880781c8a5`  
		Last Modified: Fri, 11 Sep 2020 20:51:27 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:e58f37814e3edca4c9e8506d4d3d064f4284c11736ef3fa7db0b2e898eb2d401
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39492176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50cc310448d89b89de288bab0310eab38866ad5c806e9b65ad9bdacb38890502`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Fri, 31 Jul 2020 17:42:27 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 12 Aug 2020 22:40:01 GMT
ENV CONSUL_VERSION=1.7.7
# Wed, 12 Aug 2020 22:40:02 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 12 Aug 2020 22:40:04 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 12 Aug 2020 22:40:11 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 12 Aug 2020 22:40:13 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 12 Aug 2020 22:40:14 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 12 Aug 2020 22:40:15 GMT
VOLUME [/consul/data]
# Wed, 12 Aug 2020 22:40:16 GMT
EXPOSE 8300
# Wed, 12 Aug 2020 22:40:16 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 12 Aug 2020 22:40:17 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 12 Aug 2020 22:40:18 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 12 Aug 2020 22:40:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Aug 2020 22:40:19 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b538f80385f9b48122e3da068c932a96ea5018afa3c7be79da00437414bd18cd`  
		Last Modified: Fri, 29 May 2020 21:43:57 GMT  
		Size: 2.7 MB (2707964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82309a3254a88c6b40cdfe5da6d458a6a06822a06932c1374a6bced31886df59`  
		Last Modified: Wed, 12 Aug 2020 22:41:25 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27475b0bc4e7292bbc75e38375d039ee8f635a994e921c08126392b6aaf2777`  
		Last Modified: Wed, 12 Aug 2020 22:41:35 GMT  
		Size: 36.8 MB (36780917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca1c13f2ece1c29eedf05c7803493867d5c09276ae54dcf65072a148c394767`  
		Last Modified: Wed, 12 Aug 2020 22:41:26 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39aab6f115119612ed11566663ead5b6da7ad645fb2a4491aa36575c85561c4d`  
		Last Modified: Wed, 12 Aug 2020 22:41:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d169ff28398649a004f688e9b4a8822569d231816a34d870cbacbe049cb18e`  
		Last Modified: Wed, 12 Aug 2020 22:41:26 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7` - linux; 386

```console
$ docker pull consul@sha256:83897a2359ca857bfa853698c761454f9b9ff8a20d5a0a39bc07570053072cd8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42414577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92570e091eb50edb6a9ee3eca386b2a749b9d274ba3c88ea592ea390b1d55ff0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 29 May 2020 21:38:33 GMT
ADD file:5624441d97aca5eeb82a582941efc3586397098b8391227a9040ebe434cc1d6b in / 
# Fri, 29 May 2020 21:38:33 GMT
CMD ["/bin/sh"]
# Fri, 31 Jul 2020 17:38:31 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 12 Aug 2020 22:38:33 GMT
ENV CONSUL_VERSION=1.7.7
# Wed, 12 Aug 2020 22:38:34 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 12 Aug 2020 22:38:34 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 12 Aug 2020 22:38:39 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 12 Aug 2020 22:38:40 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 12 Aug 2020 22:38:41 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 12 Aug 2020 22:38:41 GMT
VOLUME [/consul/data]
# Wed, 12 Aug 2020 22:38:41 GMT
EXPOSE 8300
# Wed, 12 Aug 2020 22:38:42 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 12 Aug 2020 22:38:42 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 12 Aug 2020 22:38:42 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 12 Aug 2020 22:38:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Aug 2020 22:38:42 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0625b4155e2a59f647ece47c0cd77ed3196b1f84454fa64ce80cad90e2b9b79e`  
		Last Modified: Fri, 29 May 2020 21:38:53 GMT  
		Size: 2.8 MB (2792298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414d48df1939665f473bd635ef9e09dd4940c699f59f941ef608fa6e4879e5cd`  
		Last Modified: Wed, 12 Aug 2020 22:39:18 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da52655faaef1c03bd8e30404f938e4b84f3e4acf8960b53101f4504a645f45`  
		Last Modified: Wed, 12 Aug 2020 22:39:26 GMT  
		Size: 39.6 MB (39619048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881c12b8ecb31e4a696fcd08383e1176eaecaa226be86360abd9e45f0b4a4f6c`  
		Last Modified: Wed, 12 Aug 2020 22:39:18 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b590f8503b1e6700851dcfdebaf157c5bf237771f058afd73bbc2b354017764b`  
		Last Modified: Wed, 12 Aug 2020 22:39:18 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc333115398234081062622a9384b76933a24749c673dee37ebc7e0d62747d63`  
		Last Modified: Wed, 12 Aug 2020 22:39:18 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.7.8`

```console
$ docker pull consul@sha256:c69861c3771303550c90abc4b616e68eb89ec05d50118890c5a71974f9db5670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm variant v6

### `consul:1.7.8` - linux; arm variant v6

```console
$ docker pull consul@sha256:71cba28e62ec10592039ceb72a8511b55c8f2666b39217047180e9fea9e3de81
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39303513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f5e1daef07fc68c15b6937c0599fbd72ada85bb6c790cd7b514ea700a63e59e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Fri, 31 Jul 2020 17:49:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 11 Sep 2020 20:49:56 GMT
ENV CONSUL_VERSION=1.7.8
# Fri, 11 Sep 2020 20:49:56 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 11 Sep 2020 20:49:59 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 11 Sep 2020 20:50:08 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 11 Sep 2020 20:50:11 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 11 Sep 2020 20:50:13 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Sep 2020 20:50:14 GMT
VOLUME [/consul/data]
# Fri, 11 Sep 2020 20:50:15 GMT
EXPOSE 8300
# Fri, 11 Sep 2020 20:50:16 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 11 Sep 2020 20:50:17 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 11 Sep 2020 20:50:17 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 11 Sep 2020 20:50:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Sep 2020 20:50:21 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6844b3063c1a2bd33f1ab8dc40b11e5ea7bff6199f137b4ca0aa498993b51f53`  
		Last Modified: Fri, 11 Sep 2020 20:51:27 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944802fa2b60e84bd8a4d90ab67877d67179e75fe2be2a4c0753a08919a52f50`  
		Last Modified: Fri, 11 Sep 2020 20:51:37 GMT  
		Size: 36.7 MB (36696932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ed00f247e4c41021efcf87e6cbda128e3adc528d414cf7bfba027ead33e923`  
		Last Modified: Fri, 11 Sep 2020 20:51:27 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58cb41dbdda2d745c0e2c9997f9824a322e57e9dc601e67264198a27796422ad`  
		Last Modified: Fri, 11 Sep 2020 20:51:27 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377efeb788858a4e3d8de19182644ac7282efa8311db9d1c5d8224880781c8a5`  
		Last Modified: Fri, 11 Sep 2020 20:51:27 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.8`

```console
$ docker pull consul@sha256:fc2acee26e1e4b04bc9a92a3943c285eb5c89e55a1b3dc6924ab03bd3047766e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.8` - linux; amd64

```console
$ docker pull consul@sha256:09ad16215a3109c1d4c9a5ec61f562945e9b4f1f9d6a7c4bc661bd9cb94caa73
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46720519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6adcb25542eda66a0ceac823a4f73fae620dcea0e9d56e0de5e82437cd439824`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Fri, 31 Jul 2020 18:22:03 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 12 Aug 2020 23:19:24 GMT
ENV CONSUL_VERSION=1.8.3
# Wed, 12 Aug 2020 23:19:25 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 12 Aug 2020 23:19:25 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 12 Aug 2020 23:19:30 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 12 Aug 2020 23:19:30 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 12 Aug 2020 23:19:31 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 12 Aug 2020 23:19:31 GMT
VOLUME [/consul/data]
# Wed, 12 Aug 2020 23:19:31 GMT
EXPOSE 8300
# Wed, 12 Aug 2020 23:19:32 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 12 Aug 2020 23:19:32 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 12 Aug 2020 23:19:32 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 12 Aug 2020 23:19:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Aug 2020 23:19:32 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01486d8d789a836fa0a61e9c6be4070359f9bf550e9d58b2c55aa5e9a6f2d9de`  
		Last Modified: Wed, 12 Aug 2020 23:20:08 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05331c059db9677723f134d54b199ab7c7a634ff44c91ae9bf3b44a2a38615b`  
		Last Modified: Wed, 12 Aug 2020 23:20:15 GMT  
		Size: 43.9 MB (43919745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c63443219bd9cc84874e4dd1e634c80d2163db1fb85a0a9751ca5c02d9498be`  
		Last Modified: Wed, 12 Aug 2020 23:20:08 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b49373c72e609facd8f9b654fc736fdf7810ceaa3c061ffdb0f686b06f009af`  
		Last Modified: Wed, 12 Aug 2020 23:20:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df210b14cefb03bf32f81949ae915db1c1278633d29cee4650b5c79b807f649d`  
		Last Modified: Wed, 12 Aug 2020 23:20:08 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; arm variant v6

```console
$ docker pull consul@sha256:aafaaf0a09da25bd0cb54bee1602b40cc1f7ef193138e4f6b434f76a943c0fe2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (41989701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43a86100da6105b536645f761c3b8ddceb32dcd97aa0640f33164a622dfe57e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Fri, 31 Jul 2020 17:49:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 11 Sep 2020 20:49:29 GMT
ENV CONSUL_VERSION=1.8.4
# Fri, 11 Sep 2020 20:49:29 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 11 Sep 2020 20:49:31 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 11 Sep 2020 20:49:40 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 11 Sep 2020 20:49:44 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 11 Sep 2020 20:49:46 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Sep 2020 20:49:46 GMT
VOLUME [/consul/data]
# Fri, 11 Sep 2020 20:49:47 GMT
EXPOSE 8300
# Fri, 11 Sep 2020 20:49:47 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 11 Sep 2020 20:49:48 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 11 Sep 2020 20:49:48 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 11 Sep 2020 20:49:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Sep 2020 20:49:50 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d7d80d413d641bef620f785978bda397aeadb9d40c19888f1988f929a889be`  
		Last Modified: Fri, 11 Sep 2020 20:51:09 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:132a3b58482ee0d780b5c237f45cfd9e340608f0251760e4da695f7c9c61f9e2`  
		Last Modified: Fri, 11 Sep 2020 20:51:19 GMT  
		Size: 39.4 MB (39383119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e7fc35438c3d463979d24a583bf530ce2f1d0577a22458d98d4101f6744f809`  
		Last Modified: Fri, 11 Sep 2020 20:51:08 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87522bb599e02c975c75cc6765f06913218b8a993a2af1c128f6c539df64d6d0`  
		Last Modified: Fri, 11 Sep 2020 20:51:08 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59c8f2ab204e55afa3d65f24e4a8faddc5a897301d01f6eb835b1dd22b89510`  
		Last Modified: Fri, 11 Sep 2020 20:51:08 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:639b207a298e4509204e5b2ef3471911f134eb377bfef9cc2425b04e9e0b8365
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42158653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c40c79012cc5f2c761919273e7b2d0d1fc0ab66916658780938a0319b6ef68fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Fri, 31 Jul 2020 17:42:27 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 12 Aug 2020 22:39:38 GMT
ENV CONSUL_VERSION=1.8.3
# Wed, 12 Aug 2020 22:39:38 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 12 Aug 2020 22:39:40 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 12 Aug 2020 22:39:46 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 12 Aug 2020 22:39:49 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 12 Aug 2020 22:39:50 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 12 Aug 2020 22:39:51 GMT
VOLUME [/consul/data]
# Wed, 12 Aug 2020 22:39:52 GMT
EXPOSE 8300
# Wed, 12 Aug 2020 22:39:52 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 12 Aug 2020 22:39:53 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 12 Aug 2020 22:39:54 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 12 Aug 2020 22:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Aug 2020 22:39:55 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b538f80385f9b48122e3da068c932a96ea5018afa3c7be79da00437414bd18cd`  
		Last Modified: Fri, 29 May 2020 21:43:57 GMT  
		Size: 2.7 MB (2707964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92fecd5b8617da42a08e84ceeb94f1f7d5337ce142feeaecf2f6158565975d6`  
		Last Modified: Wed, 12 Aug 2020 22:41:06 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d855b7ed22a0f596e540c83fc2192a861973363bb55a3dbe007a0b322dd6b268`  
		Last Modified: Wed, 12 Aug 2020 22:41:18 GMT  
		Size: 39.4 MB (39447392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7dff89b82fb6337045bf4109c009e9e431e0de440036e3dc1e7d69ff1db483`  
		Last Modified: Wed, 12 Aug 2020 22:41:06 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756a766e7f101cb3edf270496e5182cd60ca51460eeac41e6e378425f22c0b02`  
		Last Modified: Wed, 12 Aug 2020 22:41:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e607abf614e43fa8345b6210eb230fb524d57a366ca8cac741b1444e521c5a`  
		Last Modified: Wed, 12 Aug 2020 22:41:06 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; 386

```console
$ docker pull consul@sha256:38d06d2f0b6b7d3e09f859bf154c4e4f6a3410571bc06ba405d16ba7ae07caaa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46225694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6344752d8dea7cbf710d1703bdcffe53cc58d45f94a45261a6def4c1dcfe74c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 29 May 2020 21:38:33 GMT
ADD file:5624441d97aca5eeb82a582941efc3586397098b8391227a9040ebe434cc1d6b in / 
# Fri, 29 May 2020 21:38:33 GMT
CMD ["/bin/sh"]
# Fri, 31 Jul 2020 17:38:31 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 12 Aug 2020 22:38:19 GMT
ENV CONSUL_VERSION=1.8.3
# Wed, 12 Aug 2020 22:38:19 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 12 Aug 2020 22:38:20 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 12 Aug 2020 22:38:26 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 12 Aug 2020 22:38:26 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 12 Aug 2020 22:38:27 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 12 Aug 2020 22:38:27 GMT
VOLUME [/consul/data]
# Wed, 12 Aug 2020 22:38:28 GMT
EXPOSE 8300
# Wed, 12 Aug 2020 22:38:28 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 12 Aug 2020 22:38:28 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 12 Aug 2020 22:38:28 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 12 Aug 2020 22:38:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Aug 2020 22:38:29 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0625b4155e2a59f647ece47c0cd77ed3196b1f84454fa64ce80cad90e2b9b79e`  
		Last Modified: Fri, 29 May 2020 21:38:53 GMT  
		Size: 2.8 MB (2792298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca82cd5f49dce13a1f1e77839d956af71fad07e9d9f5ed000770828e6ecbda9`  
		Last Modified: Wed, 12 Aug 2020 22:39:05 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de204e89a6f811988c465045a2e6a35e744fb1f56fa8bf06c7bb676caf0f62e6`  
		Last Modified: Wed, 12 Aug 2020 22:39:14 GMT  
		Size: 43.4 MB (43430164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0cfbcbf3b55178a387ebb8bb7831588b4705bc4d211f8f66736982703e26ec5`  
		Last Modified: Wed, 12 Aug 2020 22:39:05 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a10959073be88c1188614bd98ad2596d4d9ea9260bdf414729ab50d09e76a820`  
		Last Modified: Wed, 12 Aug 2020 22:39:06 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfe19e68baf4d65969f77586d8dad93f36bbe97d730f4b1b4c3194957e6da20`  
		Last Modified: Wed, 12 Aug 2020 22:39:05 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.8.4`

```console
$ docker pull consul@sha256:a68f815bf13a22952e1cdd20be2d087b52493d86c99d67a9b65f259134add122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm variant v6

### `consul:1.8.4` - linux; arm variant v6

```console
$ docker pull consul@sha256:aafaaf0a09da25bd0cb54bee1602b40cc1f7ef193138e4f6b434f76a943c0fe2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (41989701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43a86100da6105b536645f761c3b8ddceb32dcd97aa0640f33164a622dfe57e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Fri, 31 Jul 2020 17:49:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 11 Sep 2020 20:49:29 GMT
ENV CONSUL_VERSION=1.8.4
# Fri, 11 Sep 2020 20:49:29 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 11 Sep 2020 20:49:31 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 11 Sep 2020 20:49:40 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 11 Sep 2020 20:49:44 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 11 Sep 2020 20:49:46 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Sep 2020 20:49:46 GMT
VOLUME [/consul/data]
# Fri, 11 Sep 2020 20:49:47 GMT
EXPOSE 8300
# Fri, 11 Sep 2020 20:49:47 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 11 Sep 2020 20:49:48 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 11 Sep 2020 20:49:48 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 11 Sep 2020 20:49:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Sep 2020 20:49:50 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d7d80d413d641bef620f785978bda397aeadb9d40c19888f1988f929a889be`  
		Last Modified: Fri, 11 Sep 2020 20:51:09 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:132a3b58482ee0d780b5c237f45cfd9e340608f0251760e4da695f7c9c61f9e2`  
		Last Modified: Fri, 11 Sep 2020 20:51:19 GMT  
		Size: 39.4 MB (39383119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e7fc35438c3d463979d24a583bf530ce2f1d0577a22458d98d4101f6744f809`  
		Last Modified: Fri, 11 Sep 2020 20:51:08 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87522bb599e02c975c75cc6765f06913218b8a993a2af1c128f6c539df64d6d0`  
		Last Modified: Fri, 11 Sep 2020 20:51:08 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59c8f2ab204e55afa3d65f24e4a8faddc5a897301d01f6eb835b1dd22b89510`  
		Last Modified: Fri, 11 Sep 2020 20:51:08 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:latest`

```console
$ docker pull consul@sha256:fc2acee26e1e4b04bc9a92a3943c285eb5c89e55a1b3dc6924ab03bd3047766e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:latest` - linux; amd64

```console
$ docker pull consul@sha256:09ad16215a3109c1d4c9a5ec61f562945e9b4f1f9d6a7c4bc661bd9cb94caa73
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46720519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6adcb25542eda66a0ceac823a4f73fae620dcea0e9d56e0de5e82437cd439824`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Fri, 31 Jul 2020 18:22:03 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 12 Aug 2020 23:19:24 GMT
ENV CONSUL_VERSION=1.8.3
# Wed, 12 Aug 2020 23:19:25 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 12 Aug 2020 23:19:25 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 12 Aug 2020 23:19:30 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 12 Aug 2020 23:19:30 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 12 Aug 2020 23:19:31 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 12 Aug 2020 23:19:31 GMT
VOLUME [/consul/data]
# Wed, 12 Aug 2020 23:19:31 GMT
EXPOSE 8300
# Wed, 12 Aug 2020 23:19:32 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 12 Aug 2020 23:19:32 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 12 Aug 2020 23:19:32 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 12 Aug 2020 23:19:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Aug 2020 23:19:32 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01486d8d789a836fa0a61e9c6be4070359f9bf550e9d58b2c55aa5e9a6f2d9de`  
		Last Modified: Wed, 12 Aug 2020 23:20:08 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05331c059db9677723f134d54b199ab7c7a634ff44c91ae9bf3b44a2a38615b`  
		Last Modified: Wed, 12 Aug 2020 23:20:15 GMT  
		Size: 43.9 MB (43919745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c63443219bd9cc84874e4dd1e634c80d2163db1fb85a0a9751ca5c02d9498be`  
		Last Modified: Wed, 12 Aug 2020 23:20:08 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b49373c72e609facd8f9b654fc736fdf7810ceaa3c061ffdb0f686b06f009af`  
		Last Modified: Wed, 12 Aug 2020 23:20:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df210b14cefb03bf32f81949ae915db1c1278633d29cee4650b5c79b807f649d`  
		Last Modified: Wed, 12 Aug 2020 23:20:08 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm variant v6

```console
$ docker pull consul@sha256:aafaaf0a09da25bd0cb54bee1602b40cc1f7ef193138e4f6b434f76a943c0fe2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (41989701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43a86100da6105b536645f761c3b8ddceb32dcd97aa0640f33164a622dfe57e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Fri, 31 Jul 2020 17:49:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 11 Sep 2020 20:49:29 GMT
ENV CONSUL_VERSION=1.8.4
# Fri, 11 Sep 2020 20:49:29 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 11 Sep 2020 20:49:31 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 11 Sep 2020 20:49:40 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 11 Sep 2020 20:49:44 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 11 Sep 2020 20:49:46 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Sep 2020 20:49:46 GMT
VOLUME [/consul/data]
# Fri, 11 Sep 2020 20:49:47 GMT
EXPOSE 8300
# Fri, 11 Sep 2020 20:49:47 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 11 Sep 2020 20:49:48 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 11 Sep 2020 20:49:48 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 11 Sep 2020 20:49:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Sep 2020 20:49:50 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d7d80d413d641bef620f785978bda397aeadb9d40c19888f1988f929a889be`  
		Last Modified: Fri, 11 Sep 2020 20:51:09 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:132a3b58482ee0d780b5c237f45cfd9e340608f0251760e4da695f7c9c61f9e2`  
		Last Modified: Fri, 11 Sep 2020 20:51:19 GMT  
		Size: 39.4 MB (39383119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e7fc35438c3d463979d24a583bf530ce2f1d0577a22458d98d4101f6744f809`  
		Last Modified: Fri, 11 Sep 2020 20:51:08 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87522bb599e02c975c75cc6765f06913218b8a993a2af1c128f6c539df64d6d0`  
		Last Modified: Fri, 11 Sep 2020 20:51:08 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59c8f2ab204e55afa3d65f24e4a8faddc5a897301d01f6eb835b1dd22b89510`  
		Last Modified: Fri, 11 Sep 2020 20:51:08 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:639b207a298e4509204e5b2ef3471911f134eb377bfef9cc2425b04e9e0b8365
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42158653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c40c79012cc5f2c761919273e7b2d0d1fc0ab66916658780938a0319b6ef68fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Fri, 31 Jul 2020 17:42:27 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 12 Aug 2020 22:39:38 GMT
ENV CONSUL_VERSION=1.8.3
# Wed, 12 Aug 2020 22:39:38 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 12 Aug 2020 22:39:40 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 12 Aug 2020 22:39:46 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 12 Aug 2020 22:39:49 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 12 Aug 2020 22:39:50 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 12 Aug 2020 22:39:51 GMT
VOLUME [/consul/data]
# Wed, 12 Aug 2020 22:39:52 GMT
EXPOSE 8300
# Wed, 12 Aug 2020 22:39:52 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 12 Aug 2020 22:39:53 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 12 Aug 2020 22:39:54 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 12 Aug 2020 22:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Aug 2020 22:39:55 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b538f80385f9b48122e3da068c932a96ea5018afa3c7be79da00437414bd18cd`  
		Last Modified: Fri, 29 May 2020 21:43:57 GMT  
		Size: 2.7 MB (2707964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92fecd5b8617da42a08e84ceeb94f1f7d5337ce142feeaecf2f6158565975d6`  
		Last Modified: Wed, 12 Aug 2020 22:41:06 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d855b7ed22a0f596e540c83fc2192a861973363bb55a3dbe007a0b322dd6b268`  
		Last Modified: Wed, 12 Aug 2020 22:41:18 GMT  
		Size: 39.4 MB (39447392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7dff89b82fb6337045bf4109c009e9e431e0de440036e3dc1e7d69ff1db483`  
		Last Modified: Wed, 12 Aug 2020 22:41:06 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756a766e7f101cb3edf270496e5182cd60ca51460eeac41e6e378425f22c0b02`  
		Last Modified: Wed, 12 Aug 2020 22:41:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e607abf614e43fa8345b6210eb230fb524d57a366ca8cac741b1444e521c5a`  
		Last Modified: Wed, 12 Aug 2020 22:41:06 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; 386

```console
$ docker pull consul@sha256:38d06d2f0b6b7d3e09f859bf154c4e4f6a3410571bc06ba405d16ba7ae07caaa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46225694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6344752d8dea7cbf710d1703bdcffe53cc58d45f94a45261a6def4c1dcfe74c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 29 May 2020 21:38:33 GMT
ADD file:5624441d97aca5eeb82a582941efc3586397098b8391227a9040ebe434cc1d6b in / 
# Fri, 29 May 2020 21:38:33 GMT
CMD ["/bin/sh"]
# Fri, 31 Jul 2020 17:38:31 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 12 Aug 2020 22:38:19 GMT
ENV CONSUL_VERSION=1.8.3
# Wed, 12 Aug 2020 22:38:19 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 12 Aug 2020 22:38:20 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 12 Aug 2020 22:38:26 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 12 Aug 2020 22:38:26 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 12 Aug 2020 22:38:27 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 12 Aug 2020 22:38:27 GMT
VOLUME [/consul/data]
# Wed, 12 Aug 2020 22:38:28 GMT
EXPOSE 8300
# Wed, 12 Aug 2020 22:38:28 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 12 Aug 2020 22:38:28 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 12 Aug 2020 22:38:28 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 12 Aug 2020 22:38:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Aug 2020 22:38:29 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0625b4155e2a59f647ece47c0cd77ed3196b1f84454fa64ce80cad90e2b9b79e`  
		Last Modified: Fri, 29 May 2020 21:38:53 GMT  
		Size: 2.8 MB (2792298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca82cd5f49dce13a1f1e77839d956af71fad07e9d9f5ed000770828e6ecbda9`  
		Last Modified: Wed, 12 Aug 2020 22:39:05 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de204e89a6f811988c465045a2e6a35e744fb1f56fa8bf06c7bb676caf0f62e6`  
		Last Modified: Wed, 12 Aug 2020 22:39:14 GMT  
		Size: 43.4 MB (43430164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0cfbcbf3b55178a387ebb8bb7831588b4705bc4d211f8f66736982703e26ec5`  
		Last Modified: Wed, 12 Aug 2020 22:39:05 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a10959073be88c1188614bd98ad2596d4d9ea9260bdf414729ab50d09e76a820`  
		Last Modified: Wed, 12 Aug 2020 22:39:06 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfe19e68baf4d65969f77586d8dad93f36bbe97d730f4b1b4c3194957e6da20`  
		Last Modified: Wed, 12 Aug 2020 22:39:05 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
