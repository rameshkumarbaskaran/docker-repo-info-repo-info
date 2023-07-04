<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.10`](#chronograf110)
-	[`chronograf:1.10-alpine`](#chronograf110-alpine)
-	[`chronograf:1.10.1`](#chronograf1101)
-	[`chronograf:1.10.1-alpine`](#chronograf1101-alpine)
-	[`chronograf:1.7`](#chronograf17)
-	[`chronograf:1.7-alpine`](#chronograf17-alpine)
-	[`chronograf:1.7.17`](#chronograf1717)
-	[`chronograf:1.7.17-alpine`](#chronograf1717-alpine)
-	[`chronograf:1.8`](#chronograf18)
-	[`chronograf:1.8-alpine`](#chronograf18-alpine)
-	[`chronograf:1.8.10`](#chronograf1810)
-	[`chronograf:1.8.10-alpine`](#chronograf1810-alpine)
-	[`chronograf:1.9`](#chronograf19)
-	[`chronograf:1.9-alpine`](#chronograf19-alpine)
-	[`chronograf:1.9.4`](#chronograf194)
-	[`chronograf:1.9.4-alpine`](#chronograf194-alpine)
-	[`chronograf:alpine`](#chronografalpine)
-	[`chronograf:latest`](#chronograflatest)

## `chronograf:1.10`

```console
$ docker pull chronograf@sha256:388abdaf401707b186f9d5702858f4677eb03fd673f5a399101f12a1adc1eb18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.10` - linux; amd64

```console
$ docker pull chronograf@sha256:4c8a72a31cf1c6751c665bdb090cf7dcfdf2c4d29cc6a826c0341c1ac4e287e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82809646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30929b3c76af4d2c56658f9ad656760fa3a66bd6034fdeef441fad99114c79c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:23 GMT
ADD file:4a063d4e089ef10c6806d7042a0040078674ac2db61df02df8bbb8fa4894910a in / 
# Tue, 04 Jul 2023 01:20:23 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:18:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 04 Jul 2023 04:19:17 GMT
ENV CHRONOGRAF_VERSION=1.10.1
# Tue, 04 Jul 2023 04:19:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 04:19:24 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Jul 2023 04:19:24 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Jul 2023 04:19:24 GMT
EXPOSE 8888
# Tue, 04 Jul 2023 04:19:24 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Jul 2023 04:19:24 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Jul 2023 04:19:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Jul 2023 04:19:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9d21b12d5fab9ab82969054d72411ce627c209257df64b6057016c981e163c30`  
		Last Modified: Tue, 04 Jul 2023 01:25:43 GMT  
		Size: 31.4 MB (31417388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2442302dfe8f99302044b2f10fa8cb2af7595d343d96ac7aa33263bd2e73be1b`  
		Last Modified: Tue, 04 Jul 2023 04:20:00 GMT  
		Size: 5.2 MB (5226360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009868036e3e962809f4734cf4a0d4c68017aaf3d8bc1bdc7a4f2388de7e8388`  
		Last Modified: Tue, 04 Jul 2023 04:20:34 GMT  
		Size: 46.1 MB (46141511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18dcb6401f859ffb576f7f730b11d86414e2091c979468533f9e84c3c70c940c`  
		Last Modified: Tue, 04 Jul 2023 04:20:27 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7c6e4727dfa5750009dc64b69a2a5b1603636489dd98a085839f1c0840fee6`  
		Last Modified: Tue, 04 Jul 2023 04:20:27 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e8a3c9c5d09608504a1d10e1fcdbb69d6a907d419e03a07cb380209ee9042c`  
		Last Modified: Tue, 04 Jul 2023 04:20:27 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:e4953286da1c97d04f3520adabd5886ca34fc49832f7c7b3811566ef72f99b43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74945316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36d2a8af0d2bd908fbba430fa4096bfef6579eef605eb628ab22aac25a551da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Jul 2023 00:58:20 GMT
ADD file:c023c66ee4b7cdae5c542f2ad2dd35aef94ad24e1b3b479a16538c46013ae6a5 in / 
# Tue, 04 Jul 2023 00:58:21 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:29:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 04 Jul 2023 06:29:48 GMT
ENV CHRONOGRAF_VERSION=1.10.1
# Tue, 04 Jul 2023 06:29:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 06:29:57 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Jul 2023 06:29:58 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Jul 2023 06:29:58 GMT
EXPOSE 8888
# Tue, 04 Jul 2023 06:29:58 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Jul 2023 06:29:58 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Jul 2023 06:29:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Jul 2023 06:29:58 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d9e6a8b782e380f447723ac26499c5014f2d383b9210819b9e73e97abaf81249`  
		Last Modified: Tue, 04 Jul 2023 01:03:35 GMT  
		Size: 26.6 MB (26578754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9342e7e73f178efbc8b6ba31602b8a5dbdc8fe380c40736d6ac6584f1c87a882`  
		Last Modified: Tue, 04 Jul 2023 06:30:24 GMT  
		Size: 4.5 MB (4491824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150b89319532d6a2cd53c2cf3f59e872d7ebc002136bab645382be417b453273`  
		Last Modified: Tue, 04 Jul 2023 06:30:58 GMT  
		Size: 43.9 MB (43850353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d4f915b970c5fcc23a674b16b35ed319980a4c3afb90734ac34d8cd9626c6e`  
		Last Modified: Tue, 04 Jul 2023 06:30:49 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a6547c1db13262ae04239dbfa4010271c6116d8d2a9d2c939e2b99a66bb0a8`  
		Last Modified: Tue, 04 Jul 2023 06:30:49 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10072985771255af31224dc8881d62cce74ecf7deb1c79ee2b3d13b2090229d`  
		Last Modified: Tue, 04 Jul 2023 06:30:49 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:9db3d47e265e260f4646576487a53fc5b908d7746549ce124ec6abb27e55fcdd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79151499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2176b8533c4b733822bd23fca173d0e75bde715674bddf95e11a76d5763be75`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:59:51 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 04 Jul 2023 07:00:10 GMT
ENV CHRONOGRAF_VERSION=1.10.1
# Tue, 04 Jul 2023 07:00:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 07:00:18 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Jul 2023 07:00:18 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Jul 2023 07:00:18 GMT
EXPOSE 8888
# Tue, 04 Jul 2023 07:00:18 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Jul 2023 07:00:19 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Jul 2023 07:00:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Jul 2023 07:00:19 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d212c0049b7c205f5df3dcdb0fdd25ed0b516d7b251ba14226da58f0c65258`  
		Last Modified: Tue, 04 Jul 2023 07:00:42 GMT  
		Size: 5.2 MB (5209373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36fffa32013ecab3c37d0a13386b03d66b826c3ad16cd5b45fbaab3a8206e8b4`  
		Last Modified: Tue, 04 Jul 2023 07:01:08 GMT  
		Size: 43.9 MB (43854786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ef3094da538c8be78ada7b6b3a50b4ef69825085f668a91f46fc9a0d3d6372`  
		Last Modified: Tue, 04 Jul 2023 07:01:03 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f1ee4f678c62a1aefc8c3fa9fa67c4b7f128026022926a9c3bbc28c236f879`  
		Last Modified: Tue, 04 Jul 2023 07:01:03 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:277f3dab10842ee9d228261ac6f4584aeba94d7552087622da21f3cf7a6ece56`  
		Last Modified: Tue, 04 Jul 2023 07:01:03 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:9d62c72cebc36f428c0060313c3ef3e3377e0309711addf0170493a0620920a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:612bc34865193e974de365f3e61f464ac77ea1ad3c828c125ce158034cd22205
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 MB (31471523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d92372eb76aa713e1f80da30fab50499e9f6a9a5124e579f57eab9642694097`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:04 GMT
ADD file:828b07e74c184e7f251ed992ff195cdc50fdca345f13ff484e258851d928d950 in / 
# Wed, 14 Jun 2023 20:42:04 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 00:09:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 15 Jun 2023 04:35:00 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 15 Jun 2023 04:35:33 GMT
ENV CHRONOGRAF_VERSION=1.10.1
# Thu, 15 Jun 2023 04:35:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 15 Jun 2023 04:35:39 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 15 Jun 2023 04:35:39 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 15 Jun 2023 04:35:39 GMT
EXPOSE 8888
# Thu, 15 Jun 2023 04:35:39 GMT
VOLUME [/var/lib/chronograf]
# Thu, 15 Jun 2023 04:35:39 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Thu, 15 Jun 2023 04:35:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jun 2023 04:35:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4db1b89c0bd13344176ddce2d093b9da2ae58336823ffed2009a7ea4b62d2a95`  
		Last Modified: Wed, 14 Jun 2023 20:42:37 GMT  
		Size: 3.4 MB (3374713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2214dfdd928ecf1e62b4f8e2a9a59608a27026918bc2c56798c200b89a66607`  
		Last Modified: Thu, 15 Jun 2023 00:11:46 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd2f215a0656c3952ad3cfce3a088aa7765b3195f9e051a0a7995b2b4260c48`  
		Last Modified: Thu, 15 Jun 2023 04:35:57 GMT  
		Size: 284.9 KB (284929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de727897c91e79266c88af5c343cde0e3e5167b458a9e128d56da665c573a039`  
		Last Modified: Thu, 15 Jun 2023 04:36:38 GMT  
		Size: 27.8 MB (27787202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4d3f77996a15dce0f8e8ac9c5a89eb2d6db2ff2ef00bd3fb6c2f4efa1ec675`  
		Last Modified: Thu, 15 Jun 2023 04:36:33 GMT  
		Size: 12.3 KB (12266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0347e88c27ad598445a0a65573552937a41150af7f36b834b4d4a85d4bad794b`  
		Last Modified: Thu, 15 Jun 2023 04:36:33 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0656947d8c90443cbc4edb28052852f49a1a523a4b6e8e23bf7d0967ef2dc3bd`  
		Last Modified: Thu, 15 Jun 2023 04:36:33 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.10.1`

```console
$ docker pull chronograf@sha256:388abdaf401707b186f9d5702858f4677eb03fd673f5a399101f12a1adc1eb18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.10.1` - linux; amd64

```console
$ docker pull chronograf@sha256:4c8a72a31cf1c6751c665bdb090cf7dcfdf2c4d29cc6a826c0341c1ac4e287e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82809646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30929b3c76af4d2c56658f9ad656760fa3a66bd6034fdeef441fad99114c79c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:23 GMT
ADD file:4a063d4e089ef10c6806d7042a0040078674ac2db61df02df8bbb8fa4894910a in / 
# Tue, 04 Jul 2023 01:20:23 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:18:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 04 Jul 2023 04:19:17 GMT
ENV CHRONOGRAF_VERSION=1.10.1
# Tue, 04 Jul 2023 04:19:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 04:19:24 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Jul 2023 04:19:24 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Jul 2023 04:19:24 GMT
EXPOSE 8888
# Tue, 04 Jul 2023 04:19:24 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Jul 2023 04:19:24 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Jul 2023 04:19:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Jul 2023 04:19:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9d21b12d5fab9ab82969054d72411ce627c209257df64b6057016c981e163c30`  
		Last Modified: Tue, 04 Jul 2023 01:25:43 GMT  
		Size: 31.4 MB (31417388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2442302dfe8f99302044b2f10fa8cb2af7595d343d96ac7aa33263bd2e73be1b`  
		Last Modified: Tue, 04 Jul 2023 04:20:00 GMT  
		Size: 5.2 MB (5226360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009868036e3e962809f4734cf4a0d4c68017aaf3d8bc1bdc7a4f2388de7e8388`  
		Last Modified: Tue, 04 Jul 2023 04:20:34 GMT  
		Size: 46.1 MB (46141511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18dcb6401f859ffb576f7f730b11d86414e2091c979468533f9e84c3c70c940c`  
		Last Modified: Tue, 04 Jul 2023 04:20:27 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7c6e4727dfa5750009dc64b69a2a5b1603636489dd98a085839f1c0840fee6`  
		Last Modified: Tue, 04 Jul 2023 04:20:27 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e8a3c9c5d09608504a1d10e1fcdbb69d6a907d419e03a07cb380209ee9042c`  
		Last Modified: Tue, 04 Jul 2023 04:20:27 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10.1` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:e4953286da1c97d04f3520adabd5886ca34fc49832f7c7b3811566ef72f99b43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74945316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36d2a8af0d2bd908fbba430fa4096bfef6579eef605eb628ab22aac25a551da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Jul 2023 00:58:20 GMT
ADD file:c023c66ee4b7cdae5c542f2ad2dd35aef94ad24e1b3b479a16538c46013ae6a5 in / 
# Tue, 04 Jul 2023 00:58:21 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:29:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 04 Jul 2023 06:29:48 GMT
ENV CHRONOGRAF_VERSION=1.10.1
# Tue, 04 Jul 2023 06:29:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 06:29:57 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Jul 2023 06:29:58 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Jul 2023 06:29:58 GMT
EXPOSE 8888
# Tue, 04 Jul 2023 06:29:58 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Jul 2023 06:29:58 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Jul 2023 06:29:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Jul 2023 06:29:58 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d9e6a8b782e380f447723ac26499c5014f2d383b9210819b9e73e97abaf81249`  
		Last Modified: Tue, 04 Jul 2023 01:03:35 GMT  
		Size: 26.6 MB (26578754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9342e7e73f178efbc8b6ba31602b8a5dbdc8fe380c40736d6ac6584f1c87a882`  
		Last Modified: Tue, 04 Jul 2023 06:30:24 GMT  
		Size: 4.5 MB (4491824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150b89319532d6a2cd53c2cf3f59e872d7ebc002136bab645382be417b453273`  
		Last Modified: Tue, 04 Jul 2023 06:30:58 GMT  
		Size: 43.9 MB (43850353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d4f915b970c5fcc23a674b16b35ed319980a4c3afb90734ac34d8cd9626c6e`  
		Last Modified: Tue, 04 Jul 2023 06:30:49 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a6547c1db13262ae04239dbfa4010271c6116d8d2a9d2c939e2b99a66bb0a8`  
		Last Modified: Tue, 04 Jul 2023 06:30:49 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10072985771255af31224dc8881d62cce74ecf7deb1c79ee2b3d13b2090229d`  
		Last Modified: Tue, 04 Jul 2023 06:30:49 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10.1` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:9db3d47e265e260f4646576487a53fc5b908d7746549ce124ec6abb27e55fcdd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79151499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2176b8533c4b733822bd23fca173d0e75bde715674bddf95e11a76d5763be75`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:59:51 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 04 Jul 2023 07:00:10 GMT
ENV CHRONOGRAF_VERSION=1.10.1
# Tue, 04 Jul 2023 07:00:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 07:00:18 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Jul 2023 07:00:18 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Jul 2023 07:00:18 GMT
EXPOSE 8888
# Tue, 04 Jul 2023 07:00:18 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Jul 2023 07:00:19 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Jul 2023 07:00:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Jul 2023 07:00:19 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d212c0049b7c205f5df3dcdb0fdd25ed0b516d7b251ba14226da58f0c65258`  
		Last Modified: Tue, 04 Jul 2023 07:00:42 GMT  
		Size: 5.2 MB (5209373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36fffa32013ecab3c37d0a13386b03d66b826c3ad16cd5b45fbaab3a8206e8b4`  
		Last Modified: Tue, 04 Jul 2023 07:01:08 GMT  
		Size: 43.9 MB (43854786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ef3094da538c8be78ada7b6b3a50b4ef69825085f668a91f46fc9a0d3d6372`  
		Last Modified: Tue, 04 Jul 2023 07:01:03 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f1ee4f678c62a1aefc8c3fa9fa67c4b7f128026022926a9c3bbc28c236f879`  
		Last Modified: Tue, 04 Jul 2023 07:01:03 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:277f3dab10842ee9d228261ac6f4584aeba94d7552087622da21f3cf7a6ece56`  
		Last Modified: Tue, 04 Jul 2023 07:01:03 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.10.1-alpine`

```console
$ docker pull chronograf@sha256:9d62c72cebc36f428c0060313c3ef3e3377e0309711addf0170493a0620920a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.10.1-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:612bc34865193e974de365f3e61f464ac77ea1ad3c828c125ce158034cd22205
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 MB (31471523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d92372eb76aa713e1f80da30fab50499e9f6a9a5124e579f57eab9642694097`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:04 GMT
ADD file:828b07e74c184e7f251ed992ff195cdc50fdca345f13ff484e258851d928d950 in / 
# Wed, 14 Jun 2023 20:42:04 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 00:09:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 15 Jun 2023 04:35:00 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 15 Jun 2023 04:35:33 GMT
ENV CHRONOGRAF_VERSION=1.10.1
# Thu, 15 Jun 2023 04:35:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 15 Jun 2023 04:35:39 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 15 Jun 2023 04:35:39 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 15 Jun 2023 04:35:39 GMT
EXPOSE 8888
# Thu, 15 Jun 2023 04:35:39 GMT
VOLUME [/var/lib/chronograf]
# Thu, 15 Jun 2023 04:35:39 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Thu, 15 Jun 2023 04:35:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jun 2023 04:35:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4db1b89c0bd13344176ddce2d093b9da2ae58336823ffed2009a7ea4b62d2a95`  
		Last Modified: Wed, 14 Jun 2023 20:42:37 GMT  
		Size: 3.4 MB (3374713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2214dfdd928ecf1e62b4f8e2a9a59608a27026918bc2c56798c200b89a66607`  
		Last Modified: Thu, 15 Jun 2023 00:11:46 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd2f215a0656c3952ad3cfce3a088aa7765b3195f9e051a0a7995b2b4260c48`  
		Last Modified: Thu, 15 Jun 2023 04:35:57 GMT  
		Size: 284.9 KB (284929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de727897c91e79266c88af5c343cde0e3e5167b458a9e128d56da665c573a039`  
		Last Modified: Thu, 15 Jun 2023 04:36:38 GMT  
		Size: 27.8 MB (27787202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4d3f77996a15dce0f8e8ac9c5a89eb2d6db2ff2ef00bd3fb6c2f4efa1ec675`  
		Last Modified: Thu, 15 Jun 2023 04:36:33 GMT  
		Size: 12.3 KB (12266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0347e88c27ad598445a0a65573552937a41150af7f36b834b4d4a85d4bad794b`  
		Last Modified: Thu, 15 Jun 2023 04:36:33 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0656947d8c90443cbc4edb28052852f49a1a523a4b6e8e23bf7d0967ef2dc3bd`  
		Last Modified: Thu, 15 Jun 2023 04:36:33 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:b6788a207b612fcb5872b7b9602fc29df264b124c91fafd390ed575555caaa77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7` - linux; amd64

```console
$ docker pull chronograf@sha256:c3102c9461b097ab32f3cc9de5c2040aa694adae55ad0ad37cfba5c5a61565e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70596127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce694b906d0d7e517e4ded2c67f08a25ed031870d1f066a9d47550b4f17b5bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:23 GMT
ADD file:4a063d4e089ef10c6806d7042a0040078674ac2db61df02df8bbb8fa4894910a in / 
# Tue, 04 Jul 2023 01:20:23 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:18:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 04 Jul 2023 04:18:30 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 04 Jul 2023 04:18:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 04:18:39 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Jul 2023 04:18:39 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Jul 2023 04:18:39 GMT
EXPOSE 8888
# Tue, 04 Jul 2023 04:18:39 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Jul 2023 04:18:39 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Jul 2023 04:18:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Jul 2023 04:18:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9d21b12d5fab9ab82969054d72411ce627c209257df64b6057016c981e163c30`  
		Last Modified: Tue, 04 Jul 2023 01:25:43 GMT  
		Size: 31.4 MB (31417388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc2603c0c701dea36776169c235816328b2f92bae43270ab42e5310926f4efa`  
		Last Modified: Tue, 04 Jul 2023 04:19:45 GMT  
		Size: 4.4 MB (4416615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f4d7e03a922d610329c2a37bda571f1280064460004093c4ef5eaa3c7352c0`  
		Last Modified: Tue, 04 Jul 2023 04:19:49 GMT  
		Size: 34.7 MB (34737741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a96f2be06d0a50c183c1497555144f0ba56f80950541147a86212c1f8ca18c`  
		Last Modified: Tue, 04 Jul 2023 04:19:45 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908eaf4d7d6063e965af904cb722d15d84399c042ac0d3683c3c12de679c1cc0`  
		Last Modified: Tue, 04 Jul 2023 04:19:44 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8064acecdd5a3dcbcbb64156672a6d4adefe7716e0f603a98f4d18ee2632ddcd`  
		Last Modified: Tue, 04 Jul 2023 04:19:44 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:0bcfc060216c6c4a2cbafad8c36988726c2e0ce8895b263f594b254a1fba9814
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63419406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a320fa582f58e158d4bd73b36396cfafb130ed8c636686d6d9fbae288ac69ffa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Jul 2023 00:58:20 GMT
ADD file:c023c66ee4b7cdae5c542f2ad2dd35aef94ad24e1b3b479a16538c46013ae6a5 in / 
# Tue, 04 Jul 2023 00:58:21 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:29:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 04 Jul 2023 06:29:04 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 04 Jul 2023 06:29:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 06:29:13 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Jul 2023 06:29:13 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Jul 2023 06:29:13 GMT
EXPOSE 8888
# Tue, 04 Jul 2023 06:29:14 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Jul 2023 06:29:14 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Jul 2023 06:29:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Jul 2023 06:29:14 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d9e6a8b782e380f447723ac26499c5014f2d383b9210819b9e73e97abaf81249`  
		Last Modified: Tue, 04 Jul 2023 01:03:35 GMT  
		Size: 26.6 MB (26578754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9212b3f541dcb381fb0b9d202da62cb58532fd0eabbbb478adb826439983955`  
		Last Modified: Tue, 04 Jul 2023 06:30:12 GMT  
		Size: 3.7 MB (3719092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665f68a83b8931bd3315da97de9c95c25191e7c7b0e9c1eae9748347cc40cbc5`  
		Last Modified: Tue, 04 Jul 2023 06:30:16 GMT  
		Size: 33.1 MB (33097176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07832117fa689a26a2e8611eeffe7d3814287099df275bc6bfa489a26dafcb7`  
		Last Modified: Tue, 04 Jul 2023 06:30:11 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad44e6bd1aad602f61cd93287f0a07bf963ac1b4c2c826a11ede27e6187e174`  
		Last Modified: Tue, 04 Jul 2023 06:30:11 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1760fa14e3e4b886aa542d4cabb929faef6391d7189338a9029f81f5f8a4a8a`  
		Last Modified: Tue, 04 Jul 2023 06:30:11 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:728a583541cbb842f03b572d6f8678cc888873cce5b60edf05e4e3ebede787fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67742961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f18e60fe746da39cf6767c3075ed60066c81772ad00ed3bd1b7d7454a82eaa9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:59:34 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 04 Jul 2023 06:59:34 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 04 Jul 2023 06:59:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 06:59:42 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Jul 2023 06:59:42 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Jul 2023 06:59:42 GMT
EXPOSE 8888
# Tue, 04 Jul 2023 06:59:42 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Jul 2023 06:59:42 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Jul 2023 06:59:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Jul 2023 06:59:42 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55163e4b4957616e847c981cdeace6bdecb4e2584dbcdf7c7f6eeb47722b266`  
		Last Modified: Tue, 04 Jul 2023 07:00:31 GMT  
		Size: 4.4 MB (4418101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95cdb4cd566c19b441302be933e043ac0f60990d3b3faaf0dcf35ea1c66fce64`  
		Last Modified: Tue, 04 Jul 2023 07:00:33 GMT  
		Size: 33.2 MB (33237522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c531e14ee9c500e56580f5bc5cd7cb5a5a9125101399f829e95e73e92193b594`  
		Last Modified: Tue, 04 Jul 2023 07:00:30 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ec46e86b2774ac94ec45b2c2753e74805c4d6447ce5ab25d87f822815fb13a`  
		Last Modified: Tue, 04 Jul 2023 07:00:30 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9efcc6eb4e79dc0493bd86de296f7970cb0d9ad9253f93bfaa0543d48f14bb2c`  
		Last Modified: Tue, 04 Jul 2023 07:00:30 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:c45bc7d84366cea6b1b902851fe180efb2d3dad959a7384a275057d32f4a24e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:3eaa1c6b4d57274c2a181e92e4d32f5e3b2ce74083938b0f57c32898f90296e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23241488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2655192cf47553a9da71225d9570b0a6ed514c8963e7e8f81fceb7f0d9fd6d2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:04 GMT
ADD file:828b07e74c184e7f251ed992ff195cdc50fdca345f13ff484e258851d928d950 in / 
# Wed, 14 Jun 2023 20:42:04 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 00:09:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 15 Jun 2023 04:35:00 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 15 Jun 2023 04:35:00 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Thu, 15 Jun 2023 04:35:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 15 Jun 2023 04:35:05 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 15 Jun 2023 04:35:06 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 15 Jun 2023 04:35:06 GMT
EXPOSE 8888
# Thu, 15 Jun 2023 04:35:06 GMT
VOLUME [/var/lib/chronograf]
# Thu, 15 Jun 2023 04:35:06 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Thu, 15 Jun 2023 04:35:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jun 2023 04:35:06 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4db1b89c0bd13344176ddce2d093b9da2ae58336823ffed2009a7ea4b62d2a95`  
		Last Modified: Wed, 14 Jun 2023 20:42:37 GMT  
		Size: 3.4 MB (3374713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2214dfdd928ecf1e62b4f8e2a9a59608a27026918bc2c56798c200b89a66607`  
		Last Modified: Thu, 15 Jun 2023 00:11:46 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd2f215a0656c3952ad3cfce3a088aa7765b3195f9e051a0a7995b2b4260c48`  
		Last Modified: Thu, 15 Jun 2023 04:35:57 GMT  
		Size: 284.9 KB (284929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d939a17986882c795cafbd0e8fed626f72a6055e186f1966c9dcfc722fd9d87`  
		Last Modified: Thu, 15 Jun 2023 04:36:00 GMT  
		Size: 19.6 MB (19557178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6037df3946668958b094a0d7cb915b643b97438ba4e6d75213139f55df998970`  
		Last Modified: Thu, 15 Jun 2023 04:35:57 GMT  
		Size: 12.3 KB (12259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4628dcb858423f19f1e7df9bee5e95e129c6ad4fde51b5759f2398c9fac50be`  
		Last Modified: Thu, 15 Jun 2023 04:35:57 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f1676910e4ded7481e4fe3b71d8a329c053e23ce9c689e45a53d2b9a7cf2ea`  
		Last Modified: Thu, 15 Jun 2023 04:35:57 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:b6788a207b612fcb5872b7b9602fc29df264b124c91fafd390ed575555caaa77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7.17` - linux; amd64

```console
$ docker pull chronograf@sha256:c3102c9461b097ab32f3cc9de5c2040aa694adae55ad0ad37cfba5c5a61565e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70596127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce694b906d0d7e517e4ded2c67f08a25ed031870d1f066a9d47550b4f17b5bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:23 GMT
ADD file:4a063d4e089ef10c6806d7042a0040078674ac2db61df02df8bbb8fa4894910a in / 
# Tue, 04 Jul 2023 01:20:23 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:18:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 04 Jul 2023 04:18:30 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 04 Jul 2023 04:18:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 04:18:39 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Jul 2023 04:18:39 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Jul 2023 04:18:39 GMT
EXPOSE 8888
# Tue, 04 Jul 2023 04:18:39 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Jul 2023 04:18:39 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Jul 2023 04:18:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Jul 2023 04:18:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9d21b12d5fab9ab82969054d72411ce627c209257df64b6057016c981e163c30`  
		Last Modified: Tue, 04 Jul 2023 01:25:43 GMT  
		Size: 31.4 MB (31417388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc2603c0c701dea36776169c235816328b2f92bae43270ab42e5310926f4efa`  
		Last Modified: Tue, 04 Jul 2023 04:19:45 GMT  
		Size: 4.4 MB (4416615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f4d7e03a922d610329c2a37bda571f1280064460004093c4ef5eaa3c7352c0`  
		Last Modified: Tue, 04 Jul 2023 04:19:49 GMT  
		Size: 34.7 MB (34737741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a96f2be06d0a50c183c1497555144f0ba56f80950541147a86212c1f8ca18c`  
		Last Modified: Tue, 04 Jul 2023 04:19:45 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908eaf4d7d6063e965af904cb722d15d84399c042ac0d3683c3c12de679c1cc0`  
		Last Modified: Tue, 04 Jul 2023 04:19:44 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8064acecdd5a3dcbcbb64156672a6d4adefe7716e0f603a98f4d18ee2632ddcd`  
		Last Modified: Tue, 04 Jul 2023 04:19:44 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:0bcfc060216c6c4a2cbafad8c36988726c2e0ce8895b263f594b254a1fba9814
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63419406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a320fa582f58e158d4bd73b36396cfafb130ed8c636686d6d9fbae288ac69ffa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Jul 2023 00:58:20 GMT
ADD file:c023c66ee4b7cdae5c542f2ad2dd35aef94ad24e1b3b479a16538c46013ae6a5 in / 
# Tue, 04 Jul 2023 00:58:21 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:29:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 04 Jul 2023 06:29:04 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 04 Jul 2023 06:29:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 06:29:13 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Jul 2023 06:29:13 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Jul 2023 06:29:13 GMT
EXPOSE 8888
# Tue, 04 Jul 2023 06:29:14 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Jul 2023 06:29:14 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Jul 2023 06:29:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Jul 2023 06:29:14 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d9e6a8b782e380f447723ac26499c5014f2d383b9210819b9e73e97abaf81249`  
		Last Modified: Tue, 04 Jul 2023 01:03:35 GMT  
		Size: 26.6 MB (26578754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9212b3f541dcb381fb0b9d202da62cb58532fd0eabbbb478adb826439983955`  
		Last Modified: Tue, 04 Jul 2023 06:30:12 GMT  
		Size: 3.7 MB (3719092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665f68a83b8931bd3315da97de9c95c25191e7c7b0e9c1eae9748347cc40cbc5`  
		Last Modified: Tue, 04 Jul 2023 06:30:16 GMT  
		Size: 33.1 MB (33097176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07832117fa689a26a2e8611eeffe7d3814287099df275bc6bfa489a26dafcb7`  
		Last Modified: Tue, 04 Jul 2023 06:30:11 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad44e6bd1aad602f61cd93287f0a07bf963ac1b4c2c826a11ede27e6187e174`  
		Last Modified: Tue, 04 Jul 2023 06:30:11 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1760fa14e3e4b886aa542d4cabb929faef6391d7189338a9029f81f5f8a4a8a`  
		Last Modified: Tue, 04 Jul 2023 06:30:11 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:728a583541cbb842f03b572d6f8678cc888873cce5b60edf05e4e3ebede787fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67742961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f18e60fe746da39cf6767c3075ed60066c81772ad00ed3bd1b7d7454a82eaa9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:59:34 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 04 Jul 2023 06:59:34 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 04 Jul 2023 06:59:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 06:59:42 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Jul 2023 06:59:42 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Jul 2023 06:59:42 GMT
EXPOSE 8888
# Tue, 04 Jul 2023 06:59:42 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Jul 2023 06:59:42 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Jul 2023 06:59:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Jul 2023 06:59:42 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55163e4b4957616e847c981cdeace6bdecb4e2584dbcdf7c7f6eeb47722b266`  
		Last Modified: Tue, 04 Jul 2023 07:00:31 GMT  
		Size: 4.4 MB (4418101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95cdb4cd566c19b441302be933e043ac0f60990d3b3faaf0dcf35ea1c66fce64`  
		Last Modified: Tue, 04 Jul 2023 07:00:33 GMT  
		Size: 33.2 MB (33237522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c531e14ee9c500e56580f5bc5cd7cb5a5a9125101399f829e95e73e92193b594`  
		Last Modified: Tue, 04 Jul 2023 07:00:30 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ec46e86b2774ac94ec45b2c2753e74805c4d6447ce5ab25d87f822815fb13a`  
		Last Modified: Tue, 04 Jul 2023 07:00:30 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9efcc6eb4e79dc0493bd86de296f7970cb0d9ad9253f93bfaa0543d48f14bb2c`  
		Last Modified: Tue, 04 Jul 2023 07:00:30 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:c45bc7d84366cea6b1b902851fe180efb2d3dad959a7384a275057d32f4a24e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:3eaa1c6b4d57274c2a181e92e4d32f5e3b2ce74083938b0f57c32898f90296e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23241488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2655192cf47553a9da71225d9570b0a6ed514c8963e7e8f81fceb7f0d9fd6d2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:04 GMT
ADD file:828b07e74c184e7f251ed992ff195cdc50fdca345f13ff484e258851d928d950 in / 
# Wed, 14 Jun 2023 20:42:04 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 00:09:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 15 Jun 2023 04:35:00 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 15 Jun 2023 04:35:00 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Thu, 15 Jun 2023 04:35:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 15 Jun 2023 04:35:05 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 15 Jun 2023 04:35:06 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 15 Jun 2023 04:35:06 GMT
EXPOSE 8888
# Thu, 15 Jun 2023 04:35:06 GMT
VOLUME [/var/lib/chronograf]
# Thu, 15 Jun 2023 04:35:06 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Thu, 15 Jun 2023 04:35:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jun 2023 04:35:06 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4db1b89c0bd13344176ddce2d093b9da2ae58336823ffed2009a7ea4b62d2a95`  
		Last Modified: Wed, 14 Jun 2023 20:42:37 GMT  
		Size: 3.4 MB (3374713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2214dfdd928ecf1e62b4f8e2a9a59608a27026918bc2c56798c200b89a66607`  
		Last Modified: Thu, 15 Jun 2023 00:11:46 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd2f215a0656c3952ad3cfce3a088aa7765b3195f9e051a0a7995b2b4260c48`  
		Last Modified: Thu, 15 Jun 2023 04:35:57 GMT  
		Size: 284.9 KB (284929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d939a17986882c795cafbd0e8fed626f72a6055e186f1966c9dcfc722fd9d87`  
		Last Modified: Thu, 15 Jun 2023 04:36:00 GMT  
		Size: 19.6 MB (19557178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6037df3946668958b094a0d7cb915b643b97438ba4e6d75213139f55df998970`  
		Last Modified: Thu, 15 Jun 2023 04:35:57 GMT  
		Size: 12.3 KB (12259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4628dcb858423f19f1e7df9bee5e95e129c6ad4fde51b5759f2398c9fac50be`  
		Last Modified: Thu, 15 Jun 2023 04:35:57 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f1676910e4ded7481e4fe3b71d8a329c053e23ce9c689e45a53d2b9a7cf2ea`  
		Last Modified: Thu, 15 Jun 2023 04:35:57 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:1ea0887e1f06ca5a3ca575b107b946051707b6091a9edb232ddedd8646a39f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8` - linux; amd64

```console
$ docker pull chronograf@sha256:47fb875ec0e8ce1a13e5b1f4ea597228b51c6c3c27c5c2ccd3440c264491be74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71247223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d71cad4f6770a970ee61513b308a24d28245afd9fc1cef89d9b812ac5e71804`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:23 GMT
ADD file:4a063d4e089ef10c6806d7042a0040078674ac2db61df02df8bbb8fa4894910a in / 
# Tue, 04 Jul 2023 01:20:23 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:18:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 04 Jul 2023 04:18:53 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 04 Jul 2023 04:19:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 04:19:00 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Jul 2023 04:19:00 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Jul 2023 04:19:00 GMT
EXPOSE 8888
# Tue, 04 Jul 2023 04:19:00 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Jul 2023 04:19:00 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Jul 2023 04:19:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Jul 2023 04:19:00 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9d21b12d5fab9ab82969054d72411ce627c209257df64b6057016c981e163c30`  
		Last Modified: Tue, 04 Jul 2023 01:25:43 GMT  
		Size: 31.4 MB (31417388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2442302dfe8f99302044b2f10fa8cb2af7595d343d96ac7aa33263bd2e73be1b`  
		Last Modified: Tue, 04 Jul 2023 04:20:00 GMT  
		Size: 5.2 MB (5226360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9269842128bc0b52ce9020a379de8f6c7ca488f52e56f82d6beb5e9f014b620d`  
		Last Modified: Tue, 04 Jul 2023 04:20:03 GMT  
		Size: 34.6 MB (34579086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5240e62f6dea38b6e1f99292839cc2ad0e9ae45221a429e88576ef3c651245`  
		Last Modified: Tue, 04 Jul 2023 04:19:58 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18cc5a3b74a0739ee53e7fc7f92e0e7f8d01d93559d6f6ec8b0a25a9da6277c`  
		Last Modified: Tue, 04 Jul 2023 04:19:59 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d35d924643ba624e5664eec24a3ce2c85672d75daae2dc8b30cbcb641258b83`  
		Last Modified: Tue, 04 Jul 2023 04:19:58 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d99d37900f2f3451cea18765dcd9d3d623de747a7eb692d5021451f74a5ad9ad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63845423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac75b87539886a28cbc7d7ea3c93e1b5105fc0d1752a7c237946fda19ac49d6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Jul 2023 00:58:20 GMT
ADD file:c023c66ee4b7cdae5c542f2ad2dd35aef94ad24e1b3b479a16538c46013ae6a5 in / 
# Tue, 04 Jul 2023 00:58:21 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:29:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 04 Jul 2023 06:29:24 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 04 Jul 2023 06:29:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 06:29:33 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Jul 2023 06:29:33 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Jul 2023 06:29:33 GMT
EXPOSE 8888
# Tue, 04 Jul 2023 06:29:33 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Jul 2023 06:29:33 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Jul 2023 06:29:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Jul 2023 06:29:33 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d9e6a8b782e380f447723ac26499c5014f2d383b9210819b9e73e97abaf81249`  
		Last Modified: Tue, 04 Jul 2023 01:03:35 GMT  
		Size: 26.6 MB (26578754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9342e7e73f178efbc8b6ba31602b8a5dbdc8fe380c40736d6ac6584f1c87a882`  
		Last Modified: Tue, 04 Jul 2023 06:30:24 GMT  
		Size: 4.5 MB (4491824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda1cd7bcdea1409bc0eee7b2dd80f99a6010087e23a104de9d3934e352ca4c8`  
		Last Modified: Tue, 04 Jul 2023 06:30:28 GMT  
		Size: 32.8 MB (32750464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba7ef5aa3f6d5986d57dbb7435026e861e32d974e923a5f9c1add86c5107b2e`  
		Last Modified: Tue, 04 Jul 2023 06:30:24 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ac9cd2b3f50c3daae6fb4637fece26ef2577621a48defec19c6438c11a67b4`  
		Last Modified: Tue, 04 Jul 2023 06:30:24 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1415e0d0bdc36d1a49812053e2f908915bd8183a2de3da56a6deb282afcbf9d5`  
		Last Modified: Tue, 04 Jul 2023 06:30:24 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:9e1ce69a63af1bb30a2e25f60f753b0be7d85c49b185d27f24b4ec8ce1f95898
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67940590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a967117a9d453ba28d1bb741d160a92f42242e4d543061fe2d5c9b14f065c06c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:59:51 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 04 Jul 2023 06:59:51 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 04 Jul 2023 06:59:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 06:59:58 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Jul 2023 06:59:58 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Jul 2023 06:59:58 GMT
EXPOSE 8888
# Tue, 04 Jul 2023 06:59:58 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Jul 2023 06:59:58 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Jul 2023 06:59:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Jul 2023 06:59:58 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d212c0049b7c205f5df3dcdb0fdd25ed0b516d7b251ba14226da58f0c65258`  
		Last Modified: Tue, 04 Jul 2023 07:00:42 GMT  
		Size: 5.2 MB (5209373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ba4fd507cbfbc70cb17c5cd838aa04abcbbd8ba9ee300aa5d9aaf32b29a85b`  
		Last Modified: Tue, 04 Jul 2023 07:00:44 GMT  
		Size: 32.6 MB (32643875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9968b7776d93face1c9a86701e86afe813f53fa873aef4bb5871f49faf05e7bf`  
		Last Modified: Tue, 04 Jul 2023 07:00:41 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9000879167900beb3a6d02ebf771b881684258b07c26baa9fc8fa0d9d805709c`  
		Last Modified: Tue, 04 Jul 2023 07:00:41 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55e07df79e030c04ff5fab09e66ea265ad34f0ae172982e842b6ade2074f585d`  
		Last Modified: Tue, 04 Jul 2023 07:00:41 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:69e8bc014ccc7b13212883a21876c0c86602fd0880dfbb246ec5e977022287ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:e71099b850f644dcda89e33b77eb5041228a1deaa61179c1c32b2d08207c9bd6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22888506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c14c2b253d74665ff5424b287945be9913bdf9c7e3a2887f8fc7fda48f741cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:04 GMT
ADD file:828b07e74c184e7f251ed992ff195cdc50fdca345f13ff484e258851d928d950 in / 
# Wed, 14 Jun 2023 20:42:04 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 00:09:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 15 Jun 2023 04:35:00 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 15 Jun 2023 04:35:11 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Thu, 15 Jun 2023 04:35:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 15 Jun 2023 04:35:17 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 15 Jun 2023 04:35:17 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 15 Jun 2023 04:35:17 GMT
EXPOSE 8888
# Thu, 15 Jun 2023 04:35:17 GMT
VOLUME [/var/lib/chronograf]
# Thu, 15 Jun 2023 04:35:17 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Thu, 15 Jun 2023 04:35:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jun 2023 04:35:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4db1b89c0bd13344176ddce2d093b9da2ae58336823ffed2009a7ea4b62d2a95`  
		Last Modified: Wed, 14 Jun 2023 20:42:37 GMT  
		Size: 3.4 MB (3374713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2214dfdd928ecf1e62b4f8e2a9a59608a27026918bc2c56798c200b89a66607`  
		Last Modified: Thu, 15 Jun 2023 00:11:46 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd2f215a0656c3952ad3cfce3a088aa7765b3195f9e051a0a7995b2b4260c48`  
		Last Modified: Thu, 15 Jun 2023 04:35:57 GMT  
		Size: 284.9 KB (284929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b5039647d7dd02cb310b5dba71112e2ee3f5a9937a775a318ee674af152f7c3`  
		Last Modified: Thu, 15 Jun 2023 04:36:12 GMT  
		Size: 19.2 MB (19204182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff8ab86cdd06603524b29868cb5c948fbdbe2a2661ad331911719ae767f06a0`  
		Last Modified: Thu, 15 Jun 2023 04:36:08 GMT  
		Size: 12.3 KB (12267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e979ff46c3cf2ce097cb605de70b9907411b76d12cc403c7ab5a1143f5215820`  
		Last Modified: Thu, 15 Jun 2023 04:36:08 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ee4514cdf253fe353946dcae9a81a37f706e09d216ded1cf1c54b9336dc7e7`  
		Last Modified: Thu, 15 Jun 2023 04:36:08 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:1ea0887e1f06ca5a3ca575b107b946051707b6091a9edb232ddedd8646a39f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8.10` - linux; amd64

```console
$ docker pull chronograf@sha256:47fb875ec0e8ce1a13e5b1f4ea597228b51c6c3c27c5c2ccd3440c264491be74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71247223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d71cad4f6770a970ee61513b308a24d28245afd9fc1cef89d9b812ac5e71804`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:23 GMT
ADD file:4a063d4e089ef10c6806d7042a0040078674ac2db61df02df8bbb8fa4894910a in / 
# Tue, 04 Jul 2023 01:20:23 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:18:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 04 Jul 2023 04:18:53 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 04 Jul 2023 04:19:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 04:19:00 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Jul 2023 04:19:00 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Jul 2023 04:19:00 GMT
EXPOSE 8888
# Tue, 04 Jul 2023 04:19:00 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Jul 2023 04:19:00 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Jul 2023 04:19:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Jul 2023 04:19:00 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9d21b12d5fab9ab82969054d72411ce627c209257df64b6057016c981e163c30`  
		Last Modified: Tue, 04 Jul 2023 01:25:43 GMT  
		Size: 31.4 MB (31417388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2442302dfe8f99302044b2f10fa8cb2af7595d343d96ac7aa33263bd2e73be1b`  
		Last Modified: Tue, 04 Jul 2023 04:20:00 GMT  
		Size: 5.2 MB (5226360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9269842128bc0b52ce9020a379de8f6c7ca488f52e56f82d6beb5e9f014b620d`  
		Last Modified: Tue, 04 Jul 2023 04:20:03 GMT  
		Size: 34.6 MB (34579086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5240e62f6dea38b6e1f99292839cc2ad0e9ae45221a429e88576ef3c651245`  
		Last Modified: Tue, 04 Jul 2023 04:19:58 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18cc5a3b74a0739ee53e7fc7f92e0e7f8d01d93559d6f6ec8b0a25a9da6277c`  
		Last Modified: Tue, 04 Jul 2023 04:19:59 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d35d924643ba624e5664eec24a3ce2c85672d75daae2dc8b30cbcb641258b83`  
		Last Modified: Tue, 04 Jul 2023 04:19:58 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d99d37900f2f3451cea18765dcd9d3d623de747a7eb692d5021451f74a5ad9ad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63845423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac75b87539886a28cbc7d7ea3c93e1b5105fc0d1752a7c237946fda19ac49d6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Jul 2023 00:58:20 GMT
ADD file:c023c66ee4b7cdae5c542f2ad2dd35aef94ad24e1b3b479a16538c46013ae6a5 in / 
# Tue, 04 Jul 2023 00:58:21 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:29:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 04 Jul 2023 06:29:24 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 04 Jul 2023 06:29:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 06:29:33 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Jul 2023 06:29:33 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Jul 2023 06:29:33 GMT
EXPOSE 8888
# Tue, 04 Jul 2023 06:29:33 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Jul 2023 06:29:33 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Jul 2023 06:29:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Jul 2023 06:29:33 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d9e6a8b782e380f447723ac26499c5014f2d383b9210819b9e73e97abaf81249`  
		Last Modified: Tue, 04 Jul 2023 01:03:35 GMT  
		Size: 26.6 MB (26578754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9342e7e73f178efbc8b6ba31602b8a5dbdc8fe380c40736d6ac6584f1c87a882`  
		Last Modified: Tue, 04 Jul 2023 06:30:24 GMT  
		Size: 4.5 MB (4491824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda1cd7bcdea1409bc0eee7b2dd80f99a6010087e23a104de9d3934e352ca4c8`  
		Last Modified: Tue, 04 Jul 2023 06:30:28 GMT  
		Size: 32.8 MB (32750464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba7ef5aa3f6d5986d57dbb7435026e861e32d974e923a5f9c1add86c5107b2e`  
		Last Modified: Tue, 04 Jul 2023 06:30:24 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ac9cd2b3f50c3daae6fb4637fece26ef2577621a48defec19c6438c11a67b4`  
		Last Modified: Tue, 04 Jul 2023 06:30:24 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1415e0d0bdc36d1a49812053e2f908915bd8183a2de3da56a6deb282afcbf9d5`  
		Last Modified: Tue, 04 Jul 2023 06:30:24 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:9e1ce69a63af1bb30a2e25f60f753b0be7d85c49b185d27f24b4ec8ce1f95898
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67940590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a967117a9d453ba28d1bb741d160a92f42242e4d543061fe2d5c9b14f065c06c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:59:51 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 04 Jul 2023 06:59:51 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 04 Jul 2023 06:59:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 06:59:58 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Jul 2023 06:59:58 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Jul 2023 06:59:58 GMT
EXPOSE 8888
# Tue, 04 Jul 2023 06:59:58 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Jul 2023 06:59:58 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Jul 2023 06:59:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Jul 2023 06:59:58 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d212c0049b7c205f5df3dcdb0fdd25ed0b516d7b251ba14226da58f0c65258`  
		Last Modified: Tue, 04 Jul 2023 07:00:42 GMT  
		Size: 5.2 MB (5209373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ba4fd507cbfbc70cb17c5cd838aa04abcbbd8ba9ee300aa5d9aaf32b29a85b`  
		Last Modified: Tue, 04 Jul 2023 07:00:44 GMT  
		Size: 32.6 MB (32643875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9968b7776d93face1c9a86701e86afe813f53fa873aef4bb5871f49faf05e7bf`  
		Last Modified: Tue, 04 Jul 2023 07:00:41 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9000879167900beb3a6d02ebf771b881684258b07c26baa9fc8fa0d9d805709c`  
		Last Modified: Tue, 04 Jul 2023 07:00:41 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55e07df79e030c04ff5fab09e66ea265ad34f0ae172982e842b6ade2074f585d`  
		Last Modified: Tue, 04 Jul 2023 07:00:41 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:69e8bc014ccc7b13212883a21876c0c86602fd0880dfbb246ec5e977022287ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:e71099b850f644dcda89e33b77eb5041228a1deaa61179c1c32b2d08207c9bd6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22888506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c14c2b253d74665ff5424b287945be9913bdf9c7e3a2887f8fc7fda48f741cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:04 GMT
ADD file:828b07e74c184e7f251ed992ff195cdc50fdca345f13ff484e258851d928d950 in / 
# Wed, 14 Jun 2023 20:42:04 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 00:09:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 15 Jun 2023 04:35:00 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 15 Jun 2023 04:35:11 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Thu, 15 Jun 2023 04:35:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 15 Jun 2023 04:35:17 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 15 Jun 2023 04:35:17 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 15 Jun 2023 04:35:17 GMT
EXPOSE 8888
# Thu, 15 Jun 2023 04:35:17 GMT
VOLUME [/var/lib/chronograf]
# Thu, 15 Jun 2023 04:35:17 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Thu, 15 Jun 2023 04:35:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jun 2023 04:35:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4db1b89c0bd13344176ddce2d093b9da2ae58336823ffed2009a7ea4b62d2a95`  
		Last Modified: Wed, 14 Jun 2023 20:42:37 GMT  
		Size: 3.4 MB (3374713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2214dfdd928ecf1e62b4f8e2a9a59608a27026918bc2c56798c200b89a66607`  
		Last Modified: Thu, 15 Jun 2023 00:11:46 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd2f215a0656c3952ad3cfce3a088aa7765b3195f9e051a0a7995b2b4260c48`  
		Last Modified: Thu, 15 Jun 2023 04:35:57 GMT  
		Size: 284.9 KB (284929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b5039647d7dd02cb310b5dba71112e2ee3f5a9937a775a318ee674af152f7c3`  
		Last Modified: Thu, 15 Jun 2023 04:36:12 GMT  
		Size: 19.2 MB (19204182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff8ab86cdd06603524b29868cb5c948fbdbe2a2661ad331911719ae767f06a0`  
		Last Modified: Thu, 15 Jun 2023 04:36:08 GMT  
		Size: 12.3 KB (12267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e979ff46c3cf2ce097cb605de70b9907411b76d12cc403c7ab5a1143f5215820`  
		Last Modified: Thu, 15 Jun 2023 04:36:08 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ee4514cdf253fe353946dcae9a81a37f706e09d216ded1cf1c54b9336dc7e7`  
		Last Modified: Thu, 15 Jun 2023 04:36:08 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:25a6f9f5d4f54cabd4287ff83c8c845bb9ce4629ada12cdedc8582effccdbfd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9` - linux; amd64

```console
$ docker pull chronograf@sha256:d3aa9903808e40ec23e7946af9271bd97c1495fff4377edb773ac5a58bd4fa38
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71894735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:052ffda5d479a5372700c1fb6c786de559a7c28c53c335d6049a4ae87ddb684f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:23 GMT
ADD file:4a063d4e089ef10c6806d7042a0040078674ac2db61df02df8bbb8fa4894910a in / 
# Tue, 04 Jul 2023 01:20:23 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:18:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 04 Jul 2023 04:19:05 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 04 Jul 2023 04:19:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 04:19:12 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Jul 2023 04:19:12 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Jul 2023 04:19:12 GMT
EXPOSE 8888
# Tue, 04 Jul 2023 04:19:12 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Jul 2023 04:19:12 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Jul 2023 04:19:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Jul 2023 04:19:13 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9d21b12d5fab9ab82969054d72411ce627c209257df64b6057016c981e163c30`  
		Last Modified: Tue, 04 Jul 2023 01:25:43 GMT  
		Size: 31.4 MB (31417388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2442302dfe8f99302044b2f10fa8cb2af7595d343d96ac7aa33263bd2e73be1b`  
		Last Modified: Tue, 04 Jul 2023 04:20:00 GMT  
		Size: 5.2 MB (5226360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf3cc6deabbb718c6c64047b43b90a641652aac960683f34af898b095380e95`  
		Last Modified: Tue, 04 Jul 2023 04:20:18 GMT  
		Size: 35.2 MB (35226607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3196af2fce16cc2aae910610219e5999c96fd96477e95812a51f622c87f64a2e`  
		Last Modified: Tue, 04 Jul 2023 04:20:13 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4eee56e0ac2ff68e735b9980a7e0d5399e94274fde1768b9edfdabc76979f4`  
		Last Modified: Tue, 04 Jul 2023 04:20:13 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7c590d9c3f2994bad810ed621ad407731601891a307aff8a7193b2d72c3f0a`  
		Last Modified: Tue, 04 Jul 2023 04:20:13 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:854eeb4c534051a470d9cb297862b1a5f5b815e3d7497c2e7bcafbf3ca27cde3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64621529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025786f5a05d25b123e976c3e39a5753accfcdb01d36f4df4f4f7ca9442b19e8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Jul 2023 00:58:20 GMT
ADD file:c023c66ee4b7cdae5c542f2ad2dd35aef94ad24e1b3b479a16538c46013ae6a5 in / 
# Tue, 04 Jul 2023 00:58:21 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:29:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 04 Jul 2023 06:29:36 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 04 Jul 2023 06:29:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 06:29:45 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Jul 2023 06:29:45 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Jul 2023 06:29:45 GMT
EXPOSE 8888
# Tue, 04 Jul 2023 06:29:45 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Jul 2023 06:29:45 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Jul 2023 06:29:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Jul 2023 06:29:45 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d9e6a8b782e380f447723ac26499c5014f2d383b9210819b9e73e97abaf81249`  
		Last Modified: Tue, 04 Jul 2023 01:03:35 GMT  
		Size: 26.6 MB (26578754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9342e7e73f178efbc8b6ba31602b8a5dbdc8fe380c40736d6ac6584f1c87a882`  
		Last Modified: Tue, 04 Jul 2023 06:30:24 GMT  
		Size: 4.5 MB (4491824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b845ce68954eb07a52a4641458bc2210a97c7be70d3ab73716ad8f741a1233`  
		Last Modified: Tue, 04 Jul 2023 06:30:40 GMT  
		Size: 33.5 MB (33526568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5658ae60be51ca7327fdc1f36e1346fb837c72068a13e5d3c676b66111b6ed4`  
		Last Modified: Tue, 04 Jul 2023 06:30:36 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46b074a8d44981e1ab1cc801462dfbaa2bf343380de3b32a993a3707303e728`  
		Last Modified: Tue, 04 Jul 2023 06:30:36 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9881da08ac476c52c7359beabee335b6796d75accdfff39e666f9f9e9f8d97`  
		Last Modified: Tue, 04 Jul 2023 06:30:36 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:9a37f225cb493a42e4f375e69e5c88a5484f3f833c1975ea8a5a9ddd79704dfc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68692201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745be4eb6029b67ce86685590242717e43198be860d556d7960506a90f5d9763`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:59:51 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 04 Jul 2023 07:00:01 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 04 Jul 2023 07:00:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 07:00:08 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Jul 2023 07:00:08 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Jul 2023 07:00:08 GMT
EXPOSE 8888
# Tue, 04 Jul 2023 07:00:08 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Jul 2023 07:00:08 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Jul 2023 07:00:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Jul 2023 07:00:08 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d212c0049b7c205f5df3dcdb0fdd25ed0b516d7b251ba14226da58f0c65258`  
		Last Modified: Tue, 04 Jul 2023 07:00:42 GMT  
		Size: 5.2 MB (5209373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aaa681939b37c55f3f346b631fd43c5246aa930897a99b23bbe63fc89208e0a`  
		Last Modified: Tue, 04 Jul 2023 07:00:56 GMT  
		Size: 33.4 MB (33395491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03e753074d3a501ee2d611bedead48c86c8ab422a3832b2b54955abb16b5713`  
		Last Modified: Tue, 04 Jul 2023 07:00:52 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26fbb861d8af2a23aa6c2c44ff8d5fc6608dd794ab122ef34001cb60101c7ac`  
		Last Modified: Tue, 04 Jul 2023 07:00:52 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6735a0c3be8683ffd467d8b2e05d0ac9ac82aec6f41b5ceb2882cb513cb10109`  
		Last Modified: Tue, 04 Jul 2023 07:00:52 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:adb1ec8ffa83a784f6f8f0766c5189ef428ec67ea964f6d9eea9067dd77d0e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:89fceeaa051048e2099e7c38fe8224f18dd2462774f8bf44df6439c8fff43f48
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23356515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11eda8116721d2210f91fdff75be7847611674c8ef6a74a5d9fa0e8bb282db66`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:04 GMT
ADD file:828b07e74c184e7f251ed992ff195cdc50fdca345f13ff484e258851d928d950 in / 
# Wed, 14 Jun 2023 20:42:04 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 00:09:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 15 Jun 2023 04:35:00 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 15 Jun 2023 04:35:22 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Thu, 15 Jun 2023 04:35:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 15 Jun 2023 04:35:27 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 15 Jun 2023 04:35:27 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 15 Jun 2023 04:35:27 GMT
EXPOSE 8888
# Thu, 15 Jun 2023 04:35:27 GMT
VOLUME [/var/lib/chronograf]
# Thu, 15 Jun 2023 04:35:28 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Thu, 15 Jun 2023 04:35:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jun 2023 04:35:28 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4db1b89c0bd13344176ddce2d093b9da2ae58336823ffed2009a7ea4b62d2a95`  
		Last Modified: Wed, 14 Jun 2023 20:42:37 GMT  
		Size: 3.4 MB (3374713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2214dfdd928ecf1e62b4f8e2a9a59608a27026918bc2c56798c200b89a66607`  
		Last Modified: Thu, 15 Jun 2023 00:11:46 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd2f215a0656c3952ad3cfce3a088aa7765b3195f9e051a0a7995b2b4260c48`  
		Last Modified: Thu, 15 Jun 2023 04:35:57 GMT  
		Size: 284.9 KB (284929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc089fbd9f70a18f48551ca37ed446f30b06acd413388c7c5b3a619d5c81dd5`  
		Last Modified: Thu, 15 Jun 2023 04:36:24 GMT  
		Size: 19.7 MB (19672199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84aa2385f6a0c11646291b7a2eba18f763125735aff856a106935ce44ab5519e`  
		Last Modified: Thu, 15 Jun 2023 04:36:20 GMT  
		Size: 12.3 KB (12265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3b4e4ca4491b416a322e12a3b27dbd6067965faefd0a9a90ac93a9145f8548`  
		Last Modified: Thu, 15 Jun 2023 04:36:20 GMT  
		Size: 11.9 KB (11894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c2340f1a40772b9c155a1bec1dadb5e661b5d510f65e38e1d6bda5b770a43f`  
		Last Modified: Thu, 15 Jun 2023 04:36:20 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:25a6f9f5d4f54cabd4287ff83c8c845bb9ce4629ada12cdedc8582effccdbfd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9.4` - linux; amd64

```console
$ docker pull chronograf@sha256:d3aa9903808e40ec23e7946af9271bd97c1495fff4377edb773ac5a58bd4fa38
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71894735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:052ffda5d479a5372700c1fb6c786de559a7c28c53c335d6049a4ae87ddb684f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:23 GMT
ADD file:4a063d4e089ef10c6806d7042a0040078674ac2db61df02df8bbb8fa4894910a in / 
# Tue, 04 Jul 2023 01:20:23 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:18:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 04 Jul 2023 04:19:05 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 04 Jul 2023 04:19:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 04:19:12 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Jul 2023 04:19:12 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Jul 2023 04:19:12 GMT
EXPOSE 8888
# Tue, 04 Jul 2023 04:19:12 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Jul 2023 04:19:12 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Jul 2023 04:19:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Jul 2023 04:19:13 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9d21b12d5fab9ab82969054d72411ce627c209257df64b6057016c981e163c30`  
		Last Modified: Tue, 04 Jul 2023 01:25:43 GMT  
		Size: 31.4 MB (31417388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2442302dfe8f99302044b2f10fa8cb2af7595d343d96ac7aa33263bd2e73be1b`  
		Last Modified: Tue, 04 Jul 2023 04:20:00 GMT  
		Size: 5.2 MB (5226360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf3cc6deabbb718c6c64047b43b90a641652aac960683f34af898b095380e95`  
		Last Modified: Tue, 04 Jul 2023 04:20:18 GMT  
		Size: 35.2 MB (35226607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3196af2fce16cc2aae910610219e5999c96fd96477e95812a51f622c87f64a2e`  
		Last Modified: Tue, 04 Jul 2023 04:20:13 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4eee56e0ac2ff68e735b9980a7e0d5399e94274fde1768b9edfdabc76979f4`  
		Last Modified: Tue, 04 Jul 2023 04:20:13 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7c590d9c3f2994bad810ed621ad407731601891a307aff8a7193b2d72c3f0a`  
		Last Modified: Tue, 04 Jul 2023 04:20:13 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:854eeb4c534051a470d9cb297862b1a5f5b815e3d7497c2e7bcafbf3ca27cde3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64621529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025786f5a05d25b123e976c3e39a5753accfcdb01d36f4df4f4f7ca9442b19e8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Jul 2023 00:58:20 GMT
ADD file:c023c66ee4b7cdae5c542f2ad2dd35aef94ad24e1b3b479a16538c46013ae6a5 in / 
# Tue, 04 Jul 2023 00:58:21 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:29:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 04 Jul 2023 06:29:36 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 04 Jul 2023 06:29:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 06:29:45 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Jul 2023 06:29:45 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Jul 2023 06:29:45 GMT
EXPOSE 8888
# Tue, 04 Jul 2023 06:29:45 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Jul 2023 06:29:45 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Jul 2023 06:29:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Jul 2023 06:29:45 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d9e6a8b782e380f447723ac26499c5014f2d383b9210819b9e73e97abaf81249`  
		Last Modified: Tue, 04 Jul 2023 01:03:35 GMT  
		Size: 26.6 MB (26578754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9342e7e73f178efbc8b6ba31602b8a5dbdc8fe380c40736d6ac6584f1c87a882`  
		Last Modified: Tue, 04 Jul 2023 06:30:24 GMT  
		Size: 4.5 MB (4491824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b845ce68954eb07a52a4641458bc2210a97c7be70d3ab73716ad8f741a1233`  
		Last Modified: Tue, 04 Jul 2023 06:30:40 GMT  
		Size: 33.5 MB (33526568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5658ae60be51ca7327fdc1f36e1346fb837c72068a13e5d3c676b66111b6ed4`  
		Last Modified: Tue, 04 Jul 2023 06:30:36 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46b074a8d44981e1ab1cc801462dfbaa2bf343380de3b32a993a3707303e728`  
		Last Modified: Tue, 04 Jul 2023 06:30:36 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9881da08ac476c52c7359beabee335b6796d75accdfff39e666f9f9e9f8d97`  
		Last Modified: Tue, 04 Jul 2023 06:30:36 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:9a37f225cb493a42e4f375e69e5c88a5484f3f833c1975ea8a5a9ddd79704dfc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68692201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745be4eb6029b67ce86685590242717e43198be860d556d7960506a90f5d9763`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:59:51 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 04 Jul 2023 07:00:01 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 04 Jul 2023 07:00:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 07:00:08 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Jul 2023 07:00:08 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Jul 2023 07:00:08 GMT
EXPOSE 8888
# Tue, 04 Jul 2023 07:00:08 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Jul 2023 07:00:08 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Jul 2023 07:00:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Jul 2023 07:00:08 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d212c0049b7c205f5df3dcdb0fdd25ed0b516d7b251ba14226da58f0c65258`  
		Last Modified: Tue, 04 Jul 2023 07:00:42 GMT  
		Size: 5.2 MB (5209373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aaa681939b37c55f3f346b631fd43c5246aa930897a99b23bbe63fc89208e0a`  
		Last Modified: Tue, 04 Jul 2023 07:00:56 GMT  
		Size: 33.4 MB (33395491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03e753074d3a501ee2d611bedead48c86c8ab422a3832b2b54955abb16b5713`  
		Last Modified: Tue, 04 Jul 2023 07:00:52 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26fbb861d8af2a23aa6c2c44ff8d5fc6608dd794ab122ef34001cb60101c7ac`  
		Last Modified: Tue, 04 Jul 2023 07:00:52 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6735a0c3be8683ffd467d8b2e05d0ac9ac82aec6f41b5ceb2882cb513cb10109`  
		Last Modified: Tue, 04 Jul 2023 07:00:52 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:adb1ec8ffa83a784f6f8f0766c5189ef428ec67ea964f6d9eea9067dd77d0e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:89fceeaa051048e2099e7c38fe8224f18dd2462774f8bf44df6439c8fff43f48
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23356515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11eda8116721d2210f91fdff75be7847611674c8ef6a74a5d9fa0e8bb282db66`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:04 GMT
ADD file:828b07e74c184e7f251ed992ff195cdc50fdca345f13ff484e258851d928d950 in / 
# Wed, 14 Jun 2023 20:42:04 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 00:09:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 15 Jun 2023 04:35:00 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 15 Jun 2023 04:35:22 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Thu, 15 Jun 2023 04:35:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 15 Jun 2023 04:35:27 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 15 Jun 2023 04:35:27 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 15 Jun 2023 04:35:27 GMT
EXPOSE 8888
# Thu, 15 Jun 2023 04:35:27 GMT
VOLUME [/var/lib/chronograf]
# Thu, 15 Jun 2023 04:35:28 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Thu, 15 Jun 2023 04:35:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jun 2023 04:35:28 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4db1b89c0bd13344176ddce2d093b9da2ae58336823ffed2009a7ea4b62d2a95`  
		Last Modified: Wed, 14 Jun 2023 20:42:37 GMT  
		Size: 3.4 MB (3374713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2214dfdd928ecf1e62b4f8e2a9a59608a27026918bc2c56798c200b89a66607`  
		Last Modified: Thu, 15 Jun 2023 00:11:46 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd2f215a0656c3952ad3cfce3a088aa7765b3195f9e051a0a7995b2b4260c48`  
		Last Modified: Thu, 15 Jun 2023 04:35:57 GMT  
		Size: 284.9 KB (284929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc089fbd9f70a18f48551ca37ed446f30b06acd413388c7c5b3a619d5c81dd5`  
		Last Modified: Thu, 15 Jun 2023 04:36:24 GMT  
		Size: 19.7 MB (19672199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84aa2385f6a0c11646291b7a2eba18f763125735aff856a106935ce44ab5519e`  
		Last Modified: Thu, 15 Jun 2023 04:36:20 GMT  
		Size: 12.3 KB (12265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3b4e4ca4491b416a322e12a3b27dbd6067965faefd0a9a90ac93a9145f8548`  
		Last Modified: Thu, 15 Jun 2023 04:36:20 GMT  
		Size: 11.9 KB (11894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c2340f1a40772b9c155a1bec1dadb5e661b5d510f65e38e1d6bda5b770a43f`  
		Last Modified: Thu, 15 Jun 2023 04:36:20 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:9d62c72cebc36f428c0060313c3ef3e3377e0309711addf0170493a0620920a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:612bc34865193e974de365f3e61f464ac77ea1ad3c828c125ce158034cd22205
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 MB (31471523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d92372eb76aa713e1f80da30fab50499e9f6a9a5124e579f57eab9642694097`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:04 GMT
ADD file:828b07e74c184e7f251ed992ff195cdc50fdca345f13ff484e258851d928d950 in / 
# Wed, 14 Jun 2023 20:42:04 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 00:09:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 15 Jun 2023 04:35:00 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 15 Jun 2023 04:35:33 GMT
ENV CHRONOGRAF_VERSION=1.10.1
# Thu, 15 Jun 2023 04:35:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 15 Jun 2023 04:35:39 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 15 Jun 2023 04:35:39 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 15 Jun 2023 04:35:39 GMT
EXPOSE 8888
# Thu, 15 Jun 2023 04:35:39 GMT
VOLUME [/var/lib/chronograf]
# Thu, 15 Jun 2023 04:35:39 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Thu, 15 Jun 2023 04:35:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jun 2023 04:35:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4db1b89c0bd13344176ddce2d093b9da2ae58336823ffed2009a7ea4b62d2a95`  
		Last Modified: Wed, 14 Jun 2023 20:42:37 GMT  
		Size: 3.4 MB (3374713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2214dfdd928ecf1e62b4f8e2a9a59608a27026918bc2c56798c200b89a66607`  
		Last Modified: Thu, 15 Jun 2023 00:11:46 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd2f215a0656c3952ad3cfce3a088aa7765b3195f9e051a0a7995b2b4260c48`  
		Last Modified: Thu, 15 Jun 2023 04:35:57 GMT  
		Size: 284.9 KB (284929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de727897c91e79266c88af5c343cde0e3e5167b458a9e128d56da665c573a039`  
		Last Modified: Thu, 15 Jun 2023 04:36:38 GMT  
		Size: 27.8 MB (27787202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4d3f77996a15dce0f8e8ac9c5a89eb2d6db2ff2ef00bd3fb6c2f4efa1ec675`  
		Last Modified: Thu, 15 Jun 2023 04:36:33 GMT  
		Size: 12.3 KB (12266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0347e88c27ad598445a0a65573552937a41150af7f36b834b4d4a85d4bad794b`  
		Last Modified: Thu, 15 Jun 2023 04:36:33 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0656947d8c90443cbc4edb28052852f49a1a523a4b6e8e23bf7d0967ef2dc3bd`  
		Last Modified: Thu, 15 Jun 2023 04:36:33 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:388abdaf401707b186f9d5702858f4677eb03fd673f5a399101f12a1adc1eb18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:4c8a72a31cf1c6751c665bdb090cf7dcfdf2c4d29cc6a826c0341c1ac4e287e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82809646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30929b3c76af4d2c56658f9ad656760fa3a66bd6034fdeef441fad99114c79c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:23 GMT
ADD file:4a063d4e089ef10c6806d7042a0040078674ac2db61df02df8bbb8fa4894910a in / 
# Tue, 04 Jul 2023 01:20:23 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:18:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 04 Jul 2023 04:19:17 GMT
ENV CHRONOGRAF_VERSION=1.10.1
# Tue, 04 Jul 2023 04:19:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 04:19:24 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Jul 2023 04:19:24 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Jul 2023 04:19:24 GMT
EXPOSE 8888
# Tue, 04 Jul 2023 04:19:24 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Jul 2023 04:19:24 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Jul 2023 04:19:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Jul 2023 04:19:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9d21b12d5fab9ab82969054d72411ce627c209257df64b6057016c981e163c30`  
		Last Modified: Tue, 04 Jul 2023 01:25:43 GMT  
		Size: 31.4 MB (31417388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2442302dfe8f99302044b2f10fa8cb2af7595d343d96ac7aa33263bd2e73be1b`  
		Last Modified: Tue, 04 Jul 2023 04:20:00 GMT  
		Size: 5.2 MB (5226360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009868036e3e962809f4734cf4a0d4c68017aaf3d8bc1bdc7a4f2388de7e8388`  
		Last Modified: Tue, 04 Jul 2023 04:20:34 GMT  
		Size: 46.1 MB (46141511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18dcb6401f859ffb576f7f730b11d86414e2091c979468533f9e84c3c70c940c`  
		Last Modified: Tue, 04 Jul 2023 04:20:27 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7c6e4727dfa5750009dc64b69a2a5b1603636489dd98a085839f1c0840fee6`  
		Last Modified: Tue, 04 Jul 2023 04:20:27 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e8a3c9c5d09608504a1d10e1fcdbb69d6a907d419e03a07cb380209ee9042c`  
		Last Modified: Tue, 04 Jul 2023 04:20:27 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:e4953286da1c97d04f3520adabd5886ca34fc49832f7c7b3811566ef72f99b43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74945316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36d2a8af0d2bd908fbba430fa4096bfef6579eef605eb628ab22aac25a551da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Jul 2023 00:58:20 GMT
ADD file:c023c66ee4b7cdae5c542f2ad2dd35aef94ad24e1b3b479a16538c46013ae6a5 in / 
# Tue, 04 Jul 2023 00:58:21 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:29:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 04 Jul 2023 06:29:48 GMT
ENV CHRONOGRAF_VERSION=1.10.1
# Tue, 04 Jul 2023 06:29:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 06:29:57 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Jul 2023 06:29:58 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Jul 2023 06:29:58 GMT
EXPOSE 8888
# Tue, 04 Jul 2023 06:29:58 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Jul 2023 06:29:58 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Jul 2023 06:29:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Jul 2023 06:29:58 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d9e6a8b782e380f447723ac26499c5014f2d383b9210819b9e73e97abaf81249`  
		Last Modified: Tue, 04 Jul 2023 01:03:35 GMT  
		Size: 26.6 MB (26578754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9342e7e73f178efbc8b6ba31602b8a5dbdc8fe380c40736d6ac6584f1c87a882`  
		Last Modified: Tue, 04 Jul 2023 06:30:24 GMT  
		Size: 4.5 MB (4491824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150b89319532d6a2cd53c2cf3f59e872d7ebc002136bab645382be417b453273`  
		Last Modified: Tue, 04 Jul 2023 06:30:58 GMT  
		Size: 43.9 MB (43850353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d4f915b970c5fcc23a674b16b35ed319980a4c3afb90734ac34d8cd9626c6e`  
		Last Modified: Tue, 04 Jul 2023 06:30:49 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a6547c1db13262ae04239dbfa4010271c6116d8d2a9d2c939e2b99a66bb0a8`  
		Last Modified: Tue, 04 Jul 2023 06:30:49 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10072985771255af31224dc8881d62cce74ecf7deb1c79ee2b3d13b2090229d`  
		Last Modified: Tue, 04 Jul 2023 06:30:49 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:9db3d47e265e260f4646576487a53fc5b908d7746549ce124ec6abb27e55fcdd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79151499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2176b8533c4b733822bd23fca173d0e75bde715674bddf95e11a76d5763be75`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:59:51 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 04 Jul 2023 07:00:10 GMT
ENV CHRONOGRAF_VERSION=1.10.1
# Tue, 04 Jul 2023 07:00:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 07:00:18 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Jul 2023 07:00:18 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Jul 2023 07:00:18 GMT
EXPOSE 8888
# Tue, 04 Jul 2023 07:00:18 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Jul 2023 07:00:19 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Jul 2023 07:00:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Jul 2023 07:00:19 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d212c0049b7c205f5df3dcdb0fdd25ed0b516d7b251ba14226da58f0c65258`  
		Last Modified: Tue, 04 Jul 2023 07:00:42 GMT  
		Size: 5.2 MB (5209373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36fffa32013ecab3c37d0a13386b03d66b826c3ad16cd5b45fbaab3a8206e8b4`  
		Last Modified: Tue, 04 Jul 2023 07:01:08 GMT  
		Size: 43.9 MB (43854786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ef3094da538c8be78ada7b6b3a50b4ef69825085f668a91f46fc9a0d3d6372`  
		Last Modified: Tue, 04 Jul 2023 07:01:03 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f1ee4f678c62a1aefc8c3fa9fa67c4b7f128026022926a9c3bbc28c236f879`  
		Last Modified: Tue, 04 Jul 2023 07:01:03 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:277f3dab10842ee9d228261ac6f4584aeba94d7552087622da21f3cf7a6ece56`  
		Last Modified: Tue, 04 Jul 2023 07:01:03 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
