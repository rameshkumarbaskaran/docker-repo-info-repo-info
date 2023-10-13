<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.6`](#kapacitor16)
-	[`kapacitor:1.6-alpine`](#kapacitor16-alpine)
-	[`kapacitor:1.6.6`](#kapacitor166)
-	[`kapacitor:1.6.6-alpine`](#kapacitor166-alpine)
-	[`kapacitor:1.7`](#kapacitor17)
-	[`kapacitor:1.7-alpine`](#kapacitor17-alpine)
-	[`kapacitor:1.7.0`](#kapacitor170)
-	[`kapacitor:1.7.0-alpine`](#kapacitor170-alpine)
-	[`kapacitor:alpine`](#kapacitoralpine)
-	[`kapacitor:latest`](#kapacitorlatest)

## `kapacitor:1.6`

```console
$ docker pull kapacitor@sha256:a98fd1934497ff181534e0468319affad296ec597a9a759aad0a37fe565358d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:1.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:64177fde33c3487c7c06305cce1a73c55b1855534083acc835846b70409e4c9f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.2 MB (135245806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be0bdc4c43c6d5fc29fdf570074bbf6c77a7402d50a9ea842b306f8250b0666`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 07:15:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 15:30:21 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 13 Oct 2023 15:30:21 GMT
ENV KAPACITOR_VERSION=1.6.6
# Fri, 13 Oct 2023 15:30:30 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 13 Oct 2023 15:30:30 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 13 Oct 2023 15:30:30 GMT
EXPOSE 9092
# Fri, 13 Oct 2023 15:30:30 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 13 Oct 2023 15:30:30 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 13 Oct 2023 15:30:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Oct 2023 15:30:30 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:43f89b94cd7df92a2f7e565b8fb1b7f502eff2cd225508cbd7ea2d36a9a3a601`  
		Last Modified: Thu, 05 Oct 2023 08:42:10 GMT  
		Size: 30.4 MB (30439111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c42c1a5016fb63983b7331918ba3251a006a305a7155f887c55ba0310f14ebe4`  
		Last Modified: Fri, 13 Oct 2023 07:26:26 GMT  
		Size: 7.1 MB (7119810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30239ad5e5d9331355af6421fa6c366b9f628dc79e8975c56206b99c1e540649`  
		Last Modified: Fri, 13 Oct 2023 15:31:04 GMT  
		Size: 32.0 MB (32014006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eecafba812a5df786d75c865dbb62c9bb138a7e2e3e2af65195b95faa4e41e1d`  
		Last Modified: Fri, 13 Oct 2023 15:31:08 GMT  
		Size: 65.7 MB (65672425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfebf2e5917fe7e0aa17fb02cb4f6dd873412ebcad9a73897967fdd177906c3`  
		Last Modified: Fri, 13 Oct 2023 15:31:00 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e755ceaa5480c6fface437072f7648e695473a47edcf0c9d059a6065b31431ff`  
		Last Modified: Fri, 13 Oct 2023 15:31:00 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:5d91bd5f62525d173a715c9c65b176c07a057b2ef185165ff50aeb55a362e849
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126942827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7906ff2dbdf09f2d7455dc54386eb30798e67eadfb47f0daa55cde48782f3e52`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 02:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 07:54:48 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 13 Oct 2023 07:54:48 GMT
ENV KAPACITOR_VERSION=1.6.6
# Fri, 13 Oct 2023 07:54:54 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 13 Oct 2023 07:54:55 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 13 Oct 2023 07:54:55 GMT
EXPOSE 9092
# Fri, 13 Oct 2023 07:54:55 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 13 Oct 2023 07:54:55 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 13 Oct 2023 07:54:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Oct 2023 07:54:55 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab98684ba3fe8f55da444be42c97a55fce3f516fbef08145bd1ee5686d63f30`  
		Last Modified: Fri, 13 Oct 2023 02:44:09 GMT  
		Size: 7.1 MB (7066736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffde288acdecd99ce55666c8df894c13e86912225e79ecfe6f13b5a92ced69af`  
		Last Modified: Fri, 13 Oct 2023 07:55:16 GMT  
		Size: 29.8 MB (29813095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c558fbf2f6dee23ffaf2645bdaba830dffba218997487a16702cf22362e2b57`  
		Last Modified: Fri, 13 Oct 2023 07:55:18 GMT  
		Size: 61.7 MB (61670599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04896a5ff0cac5767ecc623ef1ebd0cf27d10e0d8b3a1c5e2173b1540794a172`  
		Last Modified: Fri, 13 Oct 2023 07:55:13 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf5f2a19c4bb19ef54a520e5d50d75cf9abfdb665fd4cc74dca4135ca9585bc`  
		Last Modified: Fri, 13 Oct 2023 07:55:13 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.6-alpine`

```console
$ docker pull kapacitor@sha256:649a97fc6725f8320bc780e9559dadcbbae8b97e1bbed5d859e193b35f276b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:7b7418906094f3e66553c595956ece066860539debed2172bd0e97ccaf6b03ca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68673465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c0ab4b2e7a3e604797ddf2015c7b97fcdee7df4948f525dd75b3b8bebc96e8a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:31 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 07 Aug 2023 19:20:31 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 02:06:43 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 09 Aug 2023 02:06:44 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 09 Aug 2023 02:06:44 GMT
ENV KAPACITOR_VERSION=1.6.6
# Wed, 09 Aug 2023 02:06:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 09 Aug 2023 02:06:52 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 09 Aug 2023 02:06:52 GMT
EXPOSE 9092
# Wed, 09 Aug 2023 02:06:52 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 09 Aug 2023 02:06:52 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Wed, 09 Aug 2023 02:06:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 09 Aug 2023 02:06:53 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61398f0c26e32fcf30f1436e94600012d7b35bbf04bb4a0cf0304cf2d8ae065f`  
		Last Modified: Wed, 09 Aug 2023 02:07:08 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc02a84aa2e93219dad782abd5562f8d465bed2fb7769681d5c6a42a87db231`  
		Last Modified: Wed, 09 Aug 2023 02:07:08 GMT  
		Size: 284.9 KB (284895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2687f33019eea09dc53b5214c7b87d0c9bcb9a3898ad6ee9f316d7865c71c673`  
		Last Modified: Wed, 09 Aug 2023 02:07:16 GMT  
		Size: 65.6 MB (65580154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b00ae2bb82d25948398d6dcea1533849cc768d89ad5a61cd6ecf685c217b2fb`  
		Last Modified: Wed, 09 Aug 2023 02:07:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedb4317a123bd4dc6bb77c19a0f1ce1410a13a8926df49193aab5f9aecb78e3`  
		Last Modified: Wed, 09 Aug 2023 02:07:08 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.6.6`

```console
$ docker pull kapacitor@sha256:a98fd1934497ff181534e0468319affad296ec597a9a759aad0a37fe565358d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:1.6.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:64177fde33c3487c7c06305cce1a73c55b1855534083acc835846b70409e4c9f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.2 MB (135245806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be0bdc4c43c6d5fc29fdf570074bbf6c77a7402d50a9ea842b306f8250b0666`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 07:15:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 15:30:21 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 13 Oct 2023 15:30:21 GMT
ENV KAPACITOR_VERSION=1.6.6
# Fri, 13 Oct 2023 15:30:30 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 13 Oct 2023 15:30:30 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 13 Oct 2023 15:30:30 GMT
EXPOSE 9092
# Fri, 13 Oct 2023 15:30:30 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 13 Oct 2023 15:30:30 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 13 Oct 2023 15:30:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Oct 2023 15:30:30 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:43f89b94cd7df92a2f7e565b8fb1b7f502eff2cd225508cbd7ea2d36a9a3a601`  
		Last Modified: Thu, 05 Oct 2023 08:42:10 GMT  
		Size: 30.4 MB (30439111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c42c1a5016fb63983b7331918ba3251a006a305a7155f887c55ba0310f14ebe4`  
		Last Modified: Fri, 13 Oct 2023 07:26:26 GMT  
		Size: 7.1 MB (7119810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30239ad5e5d9331355af6421fa6c366b9f628dc79e8975c56206b99c1e540649`  
		Last Modified: Fri, 13 Oct 2023 15:31:04 GMT  
		Size: 32.0 MB (32014006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eecafba812a5df786d75c865dbb62c9bb138a7e2e3e2af65195b95faa4e41e1d`  
		Last Modified: Fri, 13 Oct 2023 15:31:08 GMT  
		Size: 65.7 MB (65672425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfebf2e5917fe7e0aa17fb02cb4f6dd873412ebcad9a73897967fdd177906c3`  
		Last Modified: Fri, 13 Oct 2023 15:31:00 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e755ceaa5480c6fface437072f7648e695473a47edcf0c9d059a6065b31431ff`  
		Last Modified: Fri, 13 Oct 2023 15:31:00 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.6.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:5d91bd5f62525d173a715c9c65b176c07a057b2ef185165ff50aeb55a362e849
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126942827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7906ff2dbdf09f2d7455dc54386eb30798e67eadfb47f0daa55cde48782f3e52`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 02:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 07:54:48 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 13 Oct 2023 07:54:48 GMT
ENV KAPACITOR_VERSION=1.6.6
# Fri, 13 Oct 2023 07:54:54 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 13 Oct 2023 07:54:55 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 13 Oct 2023 07:54:55 GMT
EXPOSE 9092
# Fri, 13 Oct 2023 07:54:55 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 13 Oct 2023 07:54:55 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 13 Oct 2023 07:54:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Oct 2023 07:54:55 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab98684ba3fe8f55da444be42c97a55fce3f516fbef08145bd1ee5686d63f30`  
		Last Modified: Fri, 13 Oct 2023 02:44:09 GMT  
		Size: 7.1 MB (7066736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffde288acdecd99ce55666c8df894c13e86912225e79ecfe6f13b5a92ced69af`  
		Last Modified: Fri, 13 Oct 2023 07:55:16 GMT  
		Size: 29.8 MB (29813095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c558fbf2f6dee23ffaf2645bdaba830dffba218997487a16702cf22362e2b57`  
		Last Modified: Fri, 13 Oct 2023 07:55:18 GMT  
		Size: 61.7 MB (61670599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04896a5ff0cac5767ecc623ef1ebd0cf27d10e0d8b3a1c5e2173b1540794a172`  
		Last Modified: Fri, 13 Oct 2023 07:55:13 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf5f2a19c4bb19ef54a520e5d50d75cf9abfdb665fd4cc74dca4135ca9585bc`  
		Last Modified: Fri, 13 Oct 2023 07:55:13 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.6.6-alpine`

```console
$ docker pull kapacitor@sha256:649a97fc6725f8320bc780e9559dadcbbae8b97e1bbed5d859e193b35f276b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.6.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:7b7418906094f3e66553c595956ece066860539debed2172bd0e97ccaf6b03ca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68673465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c0ab4b2e7a3e604797ddf2015c7b97fcdee7df4948f525dd75b3b8bebc96e8a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:31 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 07 Aug 2023 19:20:31 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 02:06:43 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 09 Aug 2023 02:06:44 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 09 Aug 2023 02:06:44 GMT
ENV KAPACITOR_VERSION=1.6.6
# Wed, 09 Aug 2023 02:06:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 09 Aug 2023 02:06:52 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 09 Aug 2023 02:06:52 GMT
EXPOSE 9092
# Wed, 09 Aug 2023 02:06:52 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 09 Aug 2023 02:06:52 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Wed, 09 Aug 2023 02:06:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 09 Aug 2023 02:06:53 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61398f0c26e32fcf30f1436e94600012d7b35bbf04bb4a0cf0304cf2d8ae065f`  
		Last Modified: Wed, 09 Aug 2023 02:07:08 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc02a84aa2e93219dad782abd5562f8d465bed2fb7769681d5c6a42a87db231`  
		Last Modified: Wed, 09 Aug 2023 02:07:08 GMT  
		Size: 284.9 KB (284895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2687f33019eea09dc53b5214c7b87d0c9bcb9a3898ad6ee9f316d7865c71c673`  
		Last Modified: Wed, 09 Aug 2023 02:07:16 GMT  
		Size: 65.6 MB (65580154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b00ae2bb82d25948398d6dcea1533849cc768d89ad5a61cd6ecf685c217b2fb`  
		Last Modified: Wed, 09 Aug 2023 02:07:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedb4317a123bd4dc6bb77c19a0f1ce1410a13a8926df49193aab5f9aecb78e3`  
		Last Modified: Wed, 09 Aug 2023 02:07:08 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.7`

```console
$ docker pull kapacitor@sha256:dbf049f06c1a0008c105311aecae08ce26b481511f8a025bb9f7cb7fc869516e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:1.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:432ddacdf835d7ceaea9eaa97baa66acfeeeaf1dea0ceacd43c5299caeacdb1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136293092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f4b7658b1aa344e91c9e5ef008ba5cd19d0e77d80e8089bfeb4d0e27a694f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 07:15:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 15:30:21 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 13 Oct 2023 15:30:37 GMT
ENV KAPACITOR_VERSION=1.7.0
# Fri, 13 Oct 2023 15:30:44 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 13 Oct 2023 15:30:44 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 13 Oct 2023 15:30:45 GMT
EXPOSE 9092
# Fri, 13 Oct 2023 15:30:45 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 13 Oct 2023 15:30:45 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 13 Oct 2023 15:30:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Oct 2023 15:30:45 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:43f89b94cd7df92a2f7e565b8fb1b7f502eff2cd225508cbd7ea2d36a9a3a601`  
		Last Modified: Thu, 05 Oct 2023 08:42:10 GMT  
		Size: 30.4 MB (30439111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c42c1a5016fb63983b7331918ba3251a006a305a7155f887c55ba0310f14ebe4`  
		Last Modified: Fri, 13 Oct 2023 07:26:26 GMT  
		Size: 7.1 MB (7119810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30239ad5e5d9331355af6421fa6c366b9f628dc79e8975c56206b99c1e540649`  
		Last Modified: Fri, 13 Oct 2023 15:31:04 GMT  
		Size: 32.0 MB (32014006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10fea4f6b5b83222f35ca3cfa351675affb75881c74246406e492084b15405c`  
		Last Modified: Fri, 13 Oct 2023 15:31:27 GMT  
		Size: 66.7 MB (66719708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d6b914aa09603360ffafa8c5e027bada453ad7e46c2225a7b1db8fc65b7e47`  
		Last Modified: Fri, 13 Oct 2023 15:31:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770a41cc49a4c5c3be56c6fa5d18ec937a669f009d199d4f0a21b86d6dc60b79`  
		Last Modified: Fri, 13 Oct 2023 15:31:18 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:9e6622ef801b5a4d95ea622e0774991fd822ff46adb1ef99c62131a1db6e232d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127552472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0351bd7f54af348451f3b697f32965cb8f04ac8eac10e1a976a6ad2a57763182`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 02:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 07:54:48 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 13 Oct 2023 07:54:58 GMT
ENV KAPACITOR_VERSION=1.7.0
# Fri, 13 Oct 2023 07:55:03 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 13 Oct 2023 07:55:03 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 13 Oct 2023 07:55:03 GMT
EXPOSE 9092
# Fri, 13 Oct 2023 07:55:03 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 13 Oct 2023 07:55:04 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 13 Oct 2023 07:55:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Oct 2023 07:55:04 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab98684ba3fe8f55da444be42c97a55fce3f516fbef08145bd1ee5686d63f30`  
		Last Modified: Fri, 13 Oct 2023 02:44:09 GMT  
		Size: 7.1 MB (7066736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffde288acdecd99ce55666c8df894c13e86912225e79ecfe6f13b5a92ced69af`  
		Last Modified: Fri, 13 Oct 2023 07:55:16 GMT  
		Size: 29.8 MB (29813095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf445c00d132d9b03742d0a9d2b5166dee4b3320b5ec5aca70b07e8774999fd9`  
		Last Modified: Fri, 13 Oct 2023 07:55:34 GMT  
		Size: 62.3 MB (62280247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3378e1b187d480d30f9ac4d5f883df90697f5fffad4565b8af2c5683781db636`  
		Last Modified: Fri, 13 Oct 2023 07:55:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400f43a8af0c6fb7bba3d6ddf4381ec0b313af65498721d0300e2f46077d0887`  
		Last Modified: Fri, 13 Oct 2023 07:55:27 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.7-alpine`

```console
$ docker pull kapacitor@sha256:0f1c393a6e3fa11feae973703969333e1d506439ca4de5d55848832ef69912a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.7-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:33a8f10c30c5e5f62585eeac00d1cc0715d9a41bc964378366fea3f7d0a13173
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70331993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3853cbb605f2244f62acfb55c54ff149c71bd053238ab42b74a2a09f744bcce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 28 Sep 2023 23:22:11 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 28 Sep 2023 23:22:11 GMT
ENV KAPACITOR_VERSION=1.7.0
# Thu, 28 Sep 2023 23:22:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 28 Sep 2023 23:22:20 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 28 Sep 2023 23:22:20 GMT
EXPOSE 9092
# Thu, 28 Sep 2023 23:22:20 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 28 Sep 2023 23:22:20 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Thu, 28 Sep 2023 23:22:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 Sep 2023 23:22:21 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3779175f54086809f96dd5b117ed71f84dd847e86676070c520eaf459fa4e08a`  
		Last Modified: Thu, 28 Sep 2023 23:22:36 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877f6d483e0e31120bd02f44a884174729150927274ce02af767e9f420bf1086`  
		Last Modified: Thu, 28 Sep 2023 23:22:36 GMT  
		Size: 284.7 KB (284699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8a5dcd1f5f2dd9ebf473eb0cc6efa928dcbe492ff45e983de648f06ae6dd14`  
		Last Modified: Thu, 28 Sep 2023 23:22:44 GMT  
		Size: 66.6 MB (66644596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d72cc490ab8065bdc237bcc304fbd0ea8ba3d4afbfcb2fcad365f374a2a6fab`  
		Last Modified: Thu, 28 Sep 2023 23:22:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485d09f60f4ac443b6c1c9c30ca7004906aad8263902298d5dd7dd9dca37d8e8`  
		Last Modified: Thu, 28 Sep 2023 23:22:36 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.7.0`

```console
$ docker pull kapacitor@sha256:dbf049f06c1a0008c105311aecae08ce26b481511f8a025bb9f7cb7fc869516e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:1.7.0` - linux; amd64

```console
$ docker pull kapacitor@sha256:432ddacdf835d7ceaea9eaa97baa66acfeeeaf1dea0ceacd43c5299caeacdb1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136293092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f4b7658b1aa344e91c9e5ef008ba5cd19d0e77d80e8089bfeb4d0e27a694f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 07:15:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 15:30:21 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 13 Oct 2023 15:30:37 GMT
ENV KAPACITOR_VERSION=1.7.0
# Fri, 13 Oct 2023 15:30:44 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 13 Oct 2023 15:30:44 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 13 Oct 2023 15:30:45 GMT
EXPOSE 9092
# Fri, 13 Oct 2023 15:30:45 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 13 Oct 2023 15:30:45 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 13 Oct 2023 15:30:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Oct 2023 15:30:45 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:43f89b94cd7df92a2f7e565b8fb1b7f502eff2cd225508cbd7ea2d36a9a3a601`  
		Last Modified: Thu, 05 Oct 2023 08:42:10 GMT  
		Size: 30.4 MB (30439111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c42c1a5016fb63983b7331918ba3251a006a305a7155f887c55ba0310f14ebe4`  
		Last Modified: Fri, 13 Oct 2023 07:26:26 GMT  
		Size: 7.1 MB (7119810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30239ad5e5d9331355af6421fa6c366b9f628dc79e8975c56206b99c1e540649`  
		Last Modified: Fri, 13 Oct 2023 15:31:04 GMT  
		Size: 32.0 MB (32014006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10fea4f6b5b83222f35ca3cfa351675affb75881c74246406e492084b15405c`  
		Last Modified: Fri, 13 Oct 2023 15:31:27 GMT  
		Size: 66.7 MB (66719708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d6b914aa09603360ffafa8c5e027bada453ad7e46c2225a7b1db8fc65b7e47`  
		Last Modified: Fri, 13 Oct 2023 15:31:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770a41cc49a4c5c3be56c6fa5d18ec937a669f009d199d4f0a21b86d6dc60b79`  
		Last Modified: Fri, 13 Oct 2023 15:31:18 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.7.0` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:9e6622ef801b5a4d95ea622e0774991fd822ff46adb1ef99c62131a1db6e232d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127552472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0351bd7f54af348451f3b697f32965cb8f04ac8eac10e1a976a6ad2a57763182`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 02:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 07:54:48 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 13 Oct 2023 07:54:58 GMT
ENV KAPACITOR_VERSION=1.7.0
# Fri, 13 Oct 2023 07:55:03 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 13 Oct 2023 07:55:03 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 13 Oct 2023 07:55:03 GMT
EXPOSE 9092
# Fri, 13 Oct 2023 07:55:03 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 13 Oct 2023 07:55:04 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 13 Oct 2023 07:55:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Oct 2023 07:55:04 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab98684ba3fe8f55da444be42c97a55fce3f516fbef08145bd1ee5686d63f30`  
		Last Modified: Fri, 13 Oct 2023 02:44:09 GMT  
		Size: 7.1 MB (7066736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffde288acdecd99ce55666c8df894c13e86912225e79ecfe6f13b5a92ced69af`  
		Last Modified: Fri, 13 Oct 2023 07:55:16 GMT  
		Size: 29.8 MB (29813095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf445c00d132d9b03742d0a9d2b5166dee4b3320b5ec5aca70b07e8774999fd9`  
		Last Modified: Fri, 13 Oct 2023 07:55:34 GMT  
		Size: 62.3 MB (62280247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3378e1b187d480d30f9ac4d5f883df90697f5fffad4565b8af2c5683781db636`  
		Last Modified: Fri, 13 Oct 2023 07:55:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400f43a8af0c6fb7bba3d6ddf4381ec0b313af65498721d0300e2f46077d0887`  
		Last Modified: Fri, 13 Oct 2023 07:55:27 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.7.0-alpine`

```console
$ docker pull kapacitor@sha256:0f1c393a6e3fa11feae973703969333e1d506439ca4de5d55848832ef69912a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.7.0-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:33a8f10c30c5e5f62585eeac00d1cc0715d9a41bc964378366fea3f7d0a13173
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70331993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3853cbb605f2244f62acfb55c54ff149c71bd053238ab42b74a2a09f744bcce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 28 Sep 2023 23:22:11 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 28 Sep 2023 23:22:11 GMT
ENV KAPACITOR_VERSION=1.7.0
# Thu, 28 Sep 2023 23:22:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 28 Sep 2023 23:22:20 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 28 Sep 2023 23:22:20 GMT
EXPOSE 9092
# Thu, 28 Sep 2023 23:22:20 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 28 Sep 2023 23:22:20 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Thu, 28 Sep 2023 23:22:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 Sep 2023 23:22:21 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3779175f54086809f96dd5b117ed71f84dd847e86676070c520eaf459fa4e08a`  
		Last Modified: Thu, 28 Sep 2023 23:22:36 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877f6d483e0e31120bd02f44a884174729150927274ce02af767e9f420bf1086`  
		Last Modified: Thu, 28 Sep 2023 23:22:36 GMT  
		Size: 284.7 KB (284699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8a5dcd1f5f2dd9ebf473eb0cc6efa928dcbe492ff45e983de648f06ae6dd14`  
		Last Modified: Thu, 28 Sep 2023 23:22:44 GMT  
		Size: 66.6 MB (66644596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d72cc490ab8065bdc237bcc304fbd0ea8ba3d4afbfcb2fcad365f374a2a6fab`  
		Last Modified: Thu, 28 Sep 2023 23:22:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485d09f60f4ac443b6c1c9c30ca7004906aad8263902298d5dd7dd9dca37d8e8`  
		Last Modified: Thu, 28 Sep 2023 23:22:36 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:0f1c393a6e3fa11feae973703969333e1d506439ca4de5d55848832ef69912a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:33a8f10c30c5e5f62585eeac00d1cc0715d9a41bc964378366fea3f7d0a13173
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70331993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3853cbb605f2244f62acfb55c54ff149c71bd053238ab42b74a2a09f744bcce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 28 Sep 2023 23:22:11 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 28 Sep 2023 23:22:11 GMT
ENV KAPACITOR_VERSION=1.7.0
# Thu, 28 Sep 2023 23:22:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 28 Sep 2023 23:22:20 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 28 Sep 2023 23:22:20 GMT
EXPOSE 9092
# Thu, 28 Sep 2023 23:22:20 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 28 Sep 2023 23:22:20 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Thu, 28 Sep 2023 23:22:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 Sep 2023 23:22:21 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3779175f54086809f96dd5b117ed71f84dd847e86676070c520eaf459fa4e08a`  
		Last Modified: Thu, 28 Sep 2023 23:22:36 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877f6d483e0e31120bd02f44a884174729150927274ce02af767e9f420bf1086`  
		Last Modified: Thu, 28 Sep 2023 23:22:36 GMT  
		Size: 284.7 KB (284699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8a5dcd1f5f2dd9ebf473eb0cc6efa928dcbe492ff45e983de648f06ae6dd14`  
		Last Modified: Thu, 28 Sep 2023 23:22:44 GMT  
		Size: 66.6 MB (66644596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d72cc490ab8065bdc237bcc304fbd0ea8ba3d4afbfcb2fcad365f374a2a6fab`  
		Last Modified: Thu, 28 Sep 2023 23:22:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485d09f60f4ac443b6c1c9c30ca7004906aad8263902298d5dd7dd9dca37d8e8`  
		Last Modified: Thu, 28 Sep 2023 23:22:36 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:dbf049f06c1a0008c105311aecae08ce26b481511f8a025bb9f7cb7fc869516e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:432ddacdf835d7ceaea9eaa97baa66acfeeeaf1dea0ceacd43c5299caeacdb1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136293092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f4b7658b1aa344e91c9e5ef008ba5cd19d0e77d80e8089bfeb4d0e27a694f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 07:15:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 15:30:21 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 13 Oct 2023 15:30:37 GMT
ENV KAPACITOR_VERSION=1.7.0
# Fri, 13 Oct 2023 15:30:44 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 13 Oct 2023 15:30:44 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 13 Oct 2023 15:30:45 GMT
EXPOSE 9092
# Fri, 13 Oct 2023 15:30:45 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 13 Oct 2023 15:30:45 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 13 Oct 2023 15:30:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Oct 2023 15:30:45 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:43f89b94cd7df92a2f7e565b8fb1b7f502eff2cd225508cbd7ea2d36a9a3a601`  
		Last Modified: Thu, 05 Oct 2023 08:42:10 GMT  
		Size: 30.4 MB (30439111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c42c1a5016fb63983b7331918ba3251a006a305a7155f887c55ba0310f14ebe4`  
		Last Modified: Fri, 13 Oct 2023 07:26:26 GMT  
		Size: 7.1 MB (7119810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30239ad5e5d9331355af6421fa6c366b9f628dc79e8975c56206b99c1e540649`  
		Last Modified: Fri, 13 Oct 2023 15:31:04 GMT  
		Size: 32.0 MB (32014006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10fea4f6b5b83222f35ca3cfa351675affb75881c74246406e492084b15405c`  
		Last Modified: Fri, 13 Oct 2023 15:31:27 GMT  
		Size: 66.7 MB (66719708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d6b914aa09603360ffafa8c5e027bada453ad7e46c2225a7b1db8fc65b7e47`  
		Last Modified: Fri, 13 Oct 2023 15:31:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770a41cc49a4c5c3be56c6fa5d18ec937a669f009d199d4f0a21b86d6dc60b79`  
		Last Modified: Fri, 13 Oct 2023 15:31:18 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:9e6622ef801b5a4d95ea622e0774991fd822ff46adb1ef99c62131a1db6e232d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127552472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0351bd7f54af348451f3b697f32965cb8f04ac8eac10e1a976a6ad2a57763182`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 02:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 07:54:48 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 13 Oct 2023 07:54:58 GMT
ENV KAPACITOR_VERSION=1.7.0
# Fri, 13 Oct 2023 07:55:03 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 13 Oct 2023 07:55:03 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 13 Oct 2023 07:55:03 GMT
EXPOSE 9092
# Fri, 13 Oct 2023 07:55:03 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 13 Oct 2023 07:55:04 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 13 Oct 2023 07:55:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Oct 2023 07:55:04 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab98684ba3fe8f55da444be42c97a55fce3f516fbef08145bd1ee5686d63f30`  
		Last Modified: Fri, 13 Oct 2023 02:44:09 GMT  
		Size: 7.1 MB (7066736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffde288acdecd99ce55666c8df894c13e86912225e79ecfe6f13b5a92ced69af`  
		Last Modified: Fri, 13 Oct 2023 07:55:16 GMT  
		Size: 29.8 MB (29813095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf445c00d132d9b03742d0a9d2b5166dee4b3320b5ec5aca70b07e8774999fd9`  
		Last Modified: Fri, 13 Oct 2023 07:55:34 GMT  
		Size: 62.3 MB (62280247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3378e1b187d480d30f9ac4d5f883df90697f5fffad4565b8af2c5683781db636`  
		Last Modified: Fri, 13 Oct 2023 07:55:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400f43a8af0c6fb7bba3d6ddf4381ec0b313af65498721d0300e2f46077d0887`  
		Last Modified: Fri, 13 Oct 2023 07:55:27 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
