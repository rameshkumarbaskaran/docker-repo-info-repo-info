<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.6`](#chronograf16)
-	[`chronograf:1.6-alpine`](#chronograf16-alpine)
-	[`chronograf:1.6.2`](#chronograf162)
-	[`chronograf:1.6.2-alpine`](#chronograf162-alpine)
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
-	[`chronograf:1.9.0`](#chronograf190)
-	[`chronograf:1.9.0-alpine`](#chronograf190-alpine)
-	[`chronograf:alpine`](#chronografalpine)
-	[`chronograf:latest`](#chronograflatest)

## `chronograf:1.6`

```console
$ docker pull chronograf@sha256:3f0c413746e25716b8d7e02a1c31dc41b36f0cd86d6d952e327b0c546cf00f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6` - linux; amd64

```console
$ docker pull chronograf@sha256:977bf442f8956232bcdef7f9944cbcdfdffee1507a056977c622b1e4da81992e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49357207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0304b2d00e52dbe6cc49a27d94d7706e35db72bf4e9263d7eb7af3cfac190628`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Sep 2021 01:23:46 GMT
ADD file:b8ae56829d548d5bff373622e23d0352bb9d313f09d8fea76dc1892b16c768c8 in / 
# Fri, 03 Sep 2021 01:23:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 03:26:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 03:26:52 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Fri, 03 Sep 2021 03:27:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Sep 2021 03:27:06 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Sep 2021 03:27:06 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Sep 2021 03:27:06 GMT
EXPOSE 8888
# Fri, 03 Sep 2021 03:27:07 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Sep 2021 03:27:07 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Sep 2021 03:27:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 03:27:08 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:442547fc262c2ebd1e2d44ea04cb011b78ec62cc2314c8c71c68ba31ae002cdb`  
		Last Modified: Fri, 03 Sep 2021 01:32:07 GMT  
		Size: 22.5 MB (22527429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be12855d82625381afbb3ee75d1d8895188661b935409594e5f2dd05563ef11a`  
		Last Modified: Fri, 03 Sep 2021 03:29:31 GMT  
		Size: 6.8 MB (6760224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8d76f4d679099bd79919021e0a3f85a7f6b7bf328bf787980bf0416b4677ee`  
		Last Modified: Fri, 03 Sep 2021 03:29:35 GMT  
		Size: 20.0 MB (20045165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e53bf0f6e4539abbfb17519c5dbe417195590373064ffd61d1919027f18f4c2`  
		Last Modified: Fri, 03 Sep 2021 03:29:29 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47fe21898815ad6ee13b4107ede93be21cf40312958e8ff8622b5e45452bee5a`  
		Last Modified: Fri, 03 Sep 2021 03:29:29 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8fd7e28f409539ff51e51b4e69e39818024e4de40dc3fefe1ef992f85fb3eb`  
		Last Modified: Fri, 03 Sep 2021 03:29:29 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d33f2016d96c512839131152bb8eb80d2f25925cade13598fbf7eb73eba92a3b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43940168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d71feca0d8b5cc6f3f107b403a7cee658f8a630561937b9ea8c170f375d83dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Sep 2021 01:05:16 GMT
ADD file:425f8ae3b1354b9858904edb027190b58b65692a710cb50a4d463ac554f853a6 in / 
# Fri, 03 Sep 2021 01:05:17 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 02:45:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 02:45:29 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Fri, 03 Sep 2021 02:45:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Sep 2021 02:45:50 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Sep 2021 02:45:50 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Sep 2021 02:45:51 GMT
EXPOSE 8888
# Fri, 03 Sep 2021 02:45:51 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Sep 2021 02:45:52 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Sep 2021 02:45:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 02:45:53 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0c15a1a8c9dffe5dfe059b37d14b92f1eb4ea47f16ae7bf66bf62f34a7510dd6`  
		Last Modified: Fri, 03 Sep 2021 01:22:37 GMT  
		Size: 19.3 MB (19316099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb41f6e44cc2adc7b1da1ef11c2a061b83d79ad3aec2895b90e80a08e2eeb1be`  
		Last Modified: Fri, 03 Sep 2021 02:49:09 GMT  
		Size: 5.8 MB (5779569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39329e39739f246799f8332fb275aeed7d3e76d7d163cb3d6e741356538bb00`  
		Last Modified: Fri, 03 Sep 2021 02:49:24 GMT  
		Size: 18.8 MB (18820116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9a24630aba0f68d5d975a50879cc35da631f2c4077368219555053519c8975`  
		Last Modified: Fri, 03 Sep 2021 02:49:07 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e30ec87c35d229130ff0dab13773ed349331993cac16a3f49a3cf0da5c9b3e`  
		Last Modified: Fri, 03 Sep 2021 02:49:07 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca92eca14d4951fbe4ff33b1a13d7f2e8331c7b47c1e6ba95b705c10130c7f5`  
		Last Modified: Fri, 03 Sep 2021 02:49:07 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:bf0af71b4df2e397f050a320ad6f280854703666de7a8962881f4277f5016209
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45423135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4c1717ce3e1102495e688027fd933de3defb882b26dfdc527fd5b15e814fa5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Sep 2021 00:42:48 GMT
ADD file:f45934b05bd47c443a0ac02ba0771c25002763d29eb9f8ae723980605ff6f091 in / 
# Fri, 03 Sep 2021 00:42:48 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 04:05:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 04:05:14 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Fri, 03 Sep 2021 04:05:22 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Sep 2021 04:05:22 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Sep 2021 04:05:22 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Sep 2021 04:05:22 GMT
EXPOSE 8888
# Fri, 03 Sep 2021 04:05:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Sep 2021 04:05:23 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Sep 2021 04:05:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 04:05:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bafcab9e99462b57e2818f0017c17049cc46e69473e9d80342344f7116f32e83`  
		Last Modified: Fri, 03 Sep 2021 00:53:26 GMT  
		Size: 20.4 MB (20389506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4762f07e63310ce400f753c3ac76f40f5fd9ce8bb5ea00be953918b761d0bece`  
		Last Modified: Fri, 03 Sep 2021 04:07:00 GMT  
		Size: 6.0 MB (6047465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d987e28d9f5e0cab026c523f5e29ab90b519d74547574630a672a96d08fbf060`  
		Last Modified: Fri, 03 Sep 2021 04:07:02 GMT  
		Size: 19.0 MB (18961777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8dd843aadd14e891bf80fcc3bcc11641b387b671a895559f12e1a2096d3594`  
		Last Modified: Fri, 03 Sep 2021 04:06:58 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39c2bb8ac5b2266b2701eda5ded984e042aa6051f818777baff0693ca718807`  
		Last Modified: Fri, 03 Sep 2021 04:06:59 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92647d50e843014dd422b7b32ab14e45c8849ea110e1feb762369921fe6b7d6`  
		Last Modified: Fri, 03 Sep 2021 04:06:59 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6-alpine`

```console
$ docker pull chronograf@sha256:a3dea9fd70283af740db184d94417ee4c3fc1375532175d597122c325b664c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.6-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b14ee1822937fb01816a97288646858f187d0f02f9fd6eeeb448b30d07b2617c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14843918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c622c45336d64ee0a6e08ce97bc55bf23712e39ca3061372e2000223e9cf6a5c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:23:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:23:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 01 Sep 2021 00:23:43 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Wed, 01 Sep 2021 00:23:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 01 Sep 2021 00:23:52 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Wed, 01 Sep 2021 00:23:52 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 01 Sep 2021 00:23:53 GMT
EXPOSE 8888
# Wed, 01 Sep 2021 00:23:53 GMT
VOLUME [/var/lib/chronograf]
# Wed, 01 Sep 2021 00:23:53 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 01 Sep 2021 00:23:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 00:23:54 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69cd3502d3b453e253ea48e4ff56f5af4e25895a1bfa5e84cda59eaefce23be`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7087df4b29e442773e368f72aa50cd7765fd6e6b43879c83880b0038e62b9077`  
		Last Modified: Wed, 01 Sep 2021 00:25:29 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62726903f0c0c59223b83affe0ace7300a908ba6fcea73b6c79ae3a146d2b5af`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 11.7 MB (11736770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff4336cfd351b47edce706376e043d71589101d40dce396d37efca10babe80d`  
		Last Modified: Wed, 01 Sep 2021 00:25:28 GMT  
		Size: 12.3 KB (12273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbbb150a469535e39e060b4b33bcad3378c611bded830e04ccb39c1942fb50de`  
		Last Modified: Wed, 01 Sep 2021 00:25:28 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3550bbef48514edb6130449969746fb016808bb6c02b3e838ac98278f8869df1`  
		Last Modified: Wed, 01 Sep 2021 00:25:28 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6.2`

```console
$ docker pull chronograf@sha256:3f0c413746e25716b8d7e02a1c31dc41b36f0cd86d6d952e327b0c546cf00f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6.2` - linux; amd64

```console
$ docker pull chronograf@sha256:977bf442f8956232bcdef7f9944cbcdfdffee1507a056977c622b1e4da81992e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49357207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0304b2d00e52dbe6cc49a27d94d7706e35db72bf4e9263d7eb7af3cfac190628`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Sep 2021 01:23:46 GMT
ADD file:b8ae56829d548d5bff373622e23d0352bb9d313f09d8fea76dc1892b16c768c8 in / 
# Fri, 03 Sep 2021 01:23:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 03:26:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 03:26:52 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Fri, 03 Sep 2021 03:27:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Sep 2021 03:27:06 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Sep 2021 03:27:06 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Sep 2021 03:27:06 GMT
EXPOSE 8888
# Fri, 03 Sep 2021 03:27:07 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Sep 2021 03:27:07 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Sep 2021 03:27:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 03:27:08 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:442547fc262c2ebd1e2d44ea04cb011b78ec62cc2314c8c71c68ba31ae002cdb`  
		Last Modified: Fri, 03 Sep 2021 01:32:07 GMT  
		Size: 22.5 MB (22527429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be12855d82625381afbb3ee75d1d8895188661b935409594e5f2dd05563ef11a`  
		Last Modified: Fri, 03 Sep 2021 03:29:31 GMT  
		Size: 6.8 MB (6760224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8d76f4d679099bd79919021e0a3f85a7f6b7bf328bf787980bf0416b4677ee`  
		Last Modified: Fri, 03 Sep 2021 03:29:35 GMT  
		Size: 20.0 MB (20045165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e53bf0f6e4539abbfb17519c5dbe417195590373064ffd61d1919027f18f4c2`  
		Last Modified: Fri, 03 Sep 2021 03:29:29 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47fe21898815ad6ee13b4107ede93be21cf40312958e8ff8622b5e45452bee5a`  
		Last Modified: Fri, 03 Sep 2021 03:29:29 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8fd7e28f409539ff51e51b4e69e39818024e4de40dc3fefe1ef992f85fb3eb`  
		Last Modified: Fri, 03 Sep 2021 03:29:29 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d33f2016d96c512839131152bb8eb80d2f25925cade13598fbf7eb73eba92a3b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43940168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d71feca0d8b5cc6f3f107b403a7cee658f8a630561937b9ea8c170f375d83dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Sep 2021 01:05:16 GMT
ADD file:425f8ae3b1354b9858904edb027190b58b65692a710cb50a4d463ac554f853a6 in / 
# Fri, 03 Sep 2021 01:05:17 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 02:45:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 02:45:29 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Fri, 03 Sep 2021 02:45:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Sep 2021 02:45:50 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Sep 2021 02:45:50 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Sep 2021 02:45:51 GMT
EXPOSE 8888
# Fri, 03 Sep 2021 02:45:51 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Sep 2021 02:45:52 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Sep 2021 02:45:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 02:45:53 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0c15a1a8c9dffe5dfe059b37d14b92f1eb4ea47f16ae7bf66bf62f34a7510dd6`  
		Last Modified: Fri, 03 Sep 2021 01:22:37 GMT  
		Size: 19.3 MB (19316099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb41f6e44cc2adc7b1da1ef11c2a061b83d79ad3aec2895b90e80a08e2eeb1be`  
		Last Modified: Fri, 03 Sep 2021 02:49:09 GMT  
		Size: 5.8 MB (5779569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39329e39739f246799f8332fb275aeed7d3e76d7d163cb3d6e741356538bb00`  
		Last Modified: Fri, 03 Sep 2021 02:49:24 GMT  
		Size: 18.8 MB (18820116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9a24630aba0f68d5d975a50879cc35da631f2c4077368219555053519c8975`  
		Last Modified: Fri, 03 Sep 2021 02:49:07 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e30ec87c35d229130ff0dab13773ed349331993cac16a3f49a3cf0da5c9b3e`  
		Last Modified: Fri, 03 Sep 2021 02:49:07 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca92eca14d4951fbe4ff33b1a13d7f2e8331c7b47c1e6ba95b705c10130c7f5`  
		Last Modified: Fri, 03 Sep 2021 02:49:07 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:bf0af71b4df2e397f050a320ad6f280854703666de7a8962881f4277f5016209
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45423135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4c1717ce3e1102495e688027fd933de3defb882b26dfdc527fd5b15e814fa5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Sep 2021 00:42:48 GMT
ADD file:f45934b05bd47c443a0ac02ba0771c25002763d29eb9f8ae723980605ff6f091 in / 
# Fri, 03 Sep 2021 00:42:48 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 04:05:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 04:05:14 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Fri, 03 Sep 2021 04:05:22 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Sep 2021 04:05:22 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Sep 2021 04:05:22 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Sep 2021 04:05:22 GMT
EXPOSE 8888
# Fri, 03 Sep 2021 04:05:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Sep 2021 04:05:23 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Sep 2021 04:05:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 04:05:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bafcab9e99462b57e2818f0017c17049cc46e69473e9d80342344f7116f32e83`  
		Last Modified: Fri, 03 Sep 2021 00:53:26 GMT  
		Size: 20.4 MB (20389506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4762f07e63310ce400f753c3ac76f40f5fd9ce8bb5ea00be953918b761d0bece`  
		Last Modified: Fri, 03 Sep 2021 04:07:00 GMT  
		Size: 6.0 MB (6047465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d987e28d9f5e0cab026c523f5e29ab90b519d74547574630a672a96d08fbf060`  
		Last Modified: Fri, 03 Sep 2021 04:07:02 GMT  
		Size: 19.0 MB (18961777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8dd843aadd14e891bf80fcc3bcc11641b387b671a895559f12e1a2096d3594`  
		Last Modified: Fri, 03 Sep 2021 04:06:58 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39c2bb8ac5b2266b2701eda5ded984e042aa6051f818777baff0693ca718807`  
		Last Modified: Fri, 03 Sep 2021 04:06:59 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92647d50e843014dd422b7b32ab14e45c8849ea110e1feb762369921fe6b7d6`  
		Last Modified: Fri, 03 Sep 2021 04:06:59 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6.2-alpine`

```console
$ docker pull chronograf@sha256:a3dea9fd70283af740db184d94417ee4c3fc1375532175d597122c325b664c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.6.2-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b14ee1822937fb01816a97288646858f187d0f02f9fd6eeeb448b30d07b2617c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14843918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c622c45336d64ee0a6e08ce97bc55bf23712e39ca3061372e2000223e9cf6a5c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:23:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:23:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 01 Sep 2021 00:23:43 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Wed, 01 Sep 2021 00:23:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 01 Sep 2021 00:23:52 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Wed, 01 Sep 2021 00:23:52 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 01 Sep 2021 00:23:53 GMT
EXPOSE 8888
# Wed, 01 Sep 2021 00:23:53 GMT
VOLUME [/var/lib/chronograf]
# Wed, 01 Sep 2021 00:23:53 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 01 Sep 2021 00:23:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 00:23:54 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69cd3502d3b453e253ea48e4ff56f5af4e25895a1bfa5e84cda59eaefce23be`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7087df4b29e442773e368f72aa50cd7765fd6e6b43879c83880b0038e62b9077`  
		Last Modified: Wed, 01 Sep 2021 00:25:29 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62726903f0c0c59223b83affe0ace7300a908ba6fcea73b6c79ae3a146d2b5af`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 11.7 MB (11736770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff4336cfd351b47edce706376e043d71589101d40dce396d37efca10babe80d`  
		Last Modified: Wed, 01 Sep 2021 00:25:28 GMT  
		Size: 12.3 KB (12273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbbb150a469535e39e060b4b33bcad3378c611bded830e04ccb39c1942fb50de`  
		Last Modified: Wed, 01 Sep 2021 00:25:28 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3550bbef48514edb6130449969746fb016808bb6c02b3e838ac98278f8869df1`  
		Last Modified: Wed, 01 Sep 2021 00:25:28 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:ae1f8709715318753d2d7d97e173d7175da346fe87b083a0a518e673bd334d8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7` - linux; amd64

```console
$ docker pull chronograf@sha256:9af3956d36aee2db91c332f3abfb98ad9bcf667574221f1bac07198cf7be5be3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65385736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de7a0dc6f1f909d06fbf5a7b5ff4f7e576a54eb078a61211329ca638d5b89dbf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Sep 2021 01:23:46 GMT
ADD file:b8ae56829d548d5bff373622e23d0352bb9d313f09d8fea76dc1892b16c768c8 in / 
# Fri, 03 Sep 2021 01:23:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 03:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 03:27:35 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 03 Sep 2021 03:27:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Sep 2021 03:27:58 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Sep 2021 03:27:59 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Sep 2021 03:27:59 GMT
EXPOSE 8888
# Fri, 03 Sep 2021 03:27:59 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Sep 2021 03:28:00 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Sep 2021 03:28:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 03:28:00 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:442547fc262c2ebd1e2d44ea04cb011b78ec62cc2314c8c71c68ba31ae002cdb`  
		Last Modified: Fri, 03 Sep 2021 01:32:07 GMT  
		Size: 22.5 MB (22527429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b34137b4359ce6da7c1b1d549bb749a382f7b288e61cb416bcfaa15f1ab61e2`  
		Last Modified: Fri, 03 Sep 2021 03:29:48 GMT  
		Size: 4.5 MB (4506022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2206f800d94743de5740396210ded4ccc715b54caad9e04d75be6fbfb81e920`  
		Last Modified: Fri, 03 Sep 2021 03:29:54 GMT  
		Size: 38.3 MB (38327902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcf366f61dd5a6e3f29db0644b50af2577a4ae82aedee25ce1f3e226a690f84`  
		Last Modified: Fri, 03 Sep 2021 03:29:46 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61d08d81dfc4c1d79f5c47eb08afaf69ad12a183ffa975bd5ed0f2cc7d52473`  
		Last Modified: Fri, 03 Sep 2021 03:29:47 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd771aee2786b84f0e966a0184c6b3dfc508ec18f3910446724672a4e5a3cbd`  
		Last Modified: Fri, 03 Sep 2021 03:29:46 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:8b3b18fc16ecc98e1bf91daaa69ba32719b5c6aea8f1816553ba941399eac678
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59002534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bcd89da09295d29aeddbf3b845afd96a58b115fbcb4aaeb3f1e9b4126500260`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Sep 2021 01:05:16 GMT
ADD file:425f8ae3b1354b9858904edb027190b58b65692a710cb50a4d463ac554f853a6 in / 
# Fri, 03 Sep 2021 01:05:17 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 02:46:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 02:46:19 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 03 Sep 2021 02:46:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Sep 2021 02:46:53 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Sep 2021 02:46:53 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Sep 2021 02:46:54 GMT
EXPOSE 8888
# Fri, 03 Sep 2021 02:46:54 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Sep 2021 02:46:55 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Sep 2021 02:46:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 02:46:56 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0c15a1a8c9dffe5dfe059b37d14b92f1eb4ea47f16ae7bf66bf62f34a7510dd6`  
		Last Modified: Fri, 03 Sep 2021 01:22:37 GMT  
		Size: 19.3 MB (19316099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72feb6c10261bcd9f265aa351af235fc6d6eb3473fad71a9579edc13f7328fa2`  
		Last Modified: Fri, 03 Sep 2021 02:49:40 GMT  
		Size: 3.9 MB (3879487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ddcfdb344e67d03f1b7a9cd328a06cbeca291255d3be23eace2601350070fa8`  
		Last Modified: Fri, 03 Sep 2021 02:49:56 GMT  
		Size: 35.8 MB (35782561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066675693109c82818a2b7cd4bd8a8e696b01141184fe0ee98354c45b0fbc140`  
		Last Modified: Fri, 03 Sep 2021 02:49:38 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4e25e7194766392fd80eed393de68cd1e2fb01396ecb0a421dbb046e1fc947`  
		Last Modified: Fri, 03 Sep 2021 02:49:38 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7170ad340de1bfc4912904c7dedb7f2308b8593444f2c0503a68b16faffdfa7b`  
		Last Modified: Fri, 03 Sep 2021 02:49:38 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:b4de3a1e320ac08817b4882160c4a6e2f33bbb06555edf5e655d6e0fa61e6e2b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60482004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3d3495eda72aa6f41a8c219f335db9ba6745e0809588b4f801d45294bee512`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Sep 2021 00:42:48 GMT
ADD file:f45934b05bd47c443a0ac02ba0771c25002763d29eb9f8ae723980605ff6f091 in / 
# Fri, 03 Sep 2021 00:42:48 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 04:05:43 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 04:05:43 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 03 Sep 2021 04:05:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Sep 2021 04:05:54 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Sep 2021 04:05:54 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Sep 2021 04:05:55 GMT
EXPOSE 8888
# Fri, 03 Sep 2021 04:05:55 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Sep 2021 04:05:55 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Sep 2021 04:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 04:05:55 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bafcab9e99462b57e2818f0017c17049cc46e69473e9d80342344f7116f32e83`  
		Last Modified: Fri, 03 Sep 2021 00:53:26 GMT  
		Size: 20.4 MB (20389506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f429787bc9369e2a73687002bd6f3a4db08dfae9c2fb518c14b3868aa3bd03`  
		Last Modified: Fri, 03 Sep 2021 04:07:14 GMT  
		Size: 4.1 MB (4082099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa00853a7dcb6f3d2c511647513db31ccb10e00dbbe49a189e21547d06b69221`  
		Last Modified: Fri, 03 Sep 2021 04:07:18 GMT  
		Size: 36.0 MB (35986014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a49fe8878086a54e507534702012ef4844946a683b06abc1929698d0f2a4cd4`  
		Last Modified: Fri, 03 Sep 2021 04:07:13 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7264941c5b0fb8e39d98bc920ca64fe4fba001c1c81c0c79c1a2cbd3ad84095e`  
		Last Modified: Fri, 03 Sep 2021 04:07:13 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571e3f3624058fae1fd839cc495825a03c6722fe872f0f92cf3e88200089f85b`  
		Last Modified: Fri, 03 Sep 2021 04:07:13 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:9b177c70e25de297b100d46ba7eb922ac167a8e65f698480e2785b1886cb94a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:c3a41e489e87268456b3ac8beea5f7c2a516dc7d43af6f7066be8b9675492d70
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22662384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a94fa13b711dbb3a88df7489d3353cc6e4777a37a87a0788d36cef2fdc64c95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:23:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:23:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 01 Sep 2021 00:24:02 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 01 Sep 2021 00:24:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 01 Sep 2021 00:24:14 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 01 Sep 2021 00:24:15 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 01 Sep 2021 00:24:15 GMT
EXPOSE 8888
# Wed, 01 Sep 2021 00:24:15 GMT
VOLUME [/var/lib/chronograf]
# Wed, 01 Sep 2021 00:24:16 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 01 Sep 2021 00:24:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 00:24:16 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69cd3502d3b453e253ea48e4ff56f5af4e25895a1bfa5e84cda59eaefce23be`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7087df4b29e442773e368f72aa50cd7765fd6e6b43879c83880b0038e62b9077`  
		Last Modified: Wed, 01 Sep 2021 00:25:29 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a1ffa92682ef14beba92c11f3c21d02b50a70f56f234ab814e604f678b2b31`  
		Last Modified: Wed, 01 Sep 2021 00:25:49 GMT  
		Size: 19.6 MB (19555249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37dbb12c4afee159bb53c97f3d0cb65034efe2713363365b1f7f5f7affb916fe`  
		Last Modified: Wed, 01 Sep 2021 00:25:43 GMT  
		Size: 12.3 KB (12265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344ba26fb8530e7520df76f60ae8b3f9e317561d15deea2b4738f5c3e4b47e11`  
		Last Modified: Wed, 01 Sep 2021 00:25:43 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9b8b115b6329338ab5fea52358a641fbb017ecd917613643e4cbce6b3f081f`  
		Last Modified: Wed, 01 Sep 2021 00:25:43 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:ae1f8709715318753d2d7d97e173d7175da346fe87b083a0a518e673bd334d8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7.17` - linux; amd64

```console
$ docker pull chronograf@sha256:9af3956d36aee2db91c332f3abfb98ad9bcf667574221f1bac07198cf7be5be3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65385736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de7a0dc6f1f909d06fbf5a7b5ff4f7e576a54eb078a61211329ca638d5b89dbf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Sep 2021 01:23:46 GMT
ADD file:b8ae56829d548d5bff373622e23d0352bb9d313f09d8fea76dc1892b16c768c8 in / 
# Fri, 03 Sep 2021 01:23:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 03:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 03:27:35 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 03 Sep 2021 03:27:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Sep 2021 03:27:58 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Sep 2021 03:27:59 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Sep 2021 03:27:59 GMT
EXPOSE 8888
# Fri, 03 Sep 2021 03:27:59 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Sep 2021 03:28:00 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Sep 2021 03:28:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 03:28:00 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:442547fc262c2ebd1e2d44ea04cb011b78ec62cc2314c8c71c68ba31ae002cdb`  
		Last Modified: Fri, 03 Sep 2021 01:32:07 GMT  
		Size: 22.5 MB (22527429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b34137b4359ce6da7c1b1d549bb749a382f7b288e61cb416bcfaa15f1ab61e2`  
		Last Modified: Fri, 03 Sep 2021 03:29:48 GMT  
		Size: 4.5 MB (4506022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2206f800d94743de5740396210ded4ccc715b54caad9e04d75be6fbfb81e920`  
		Last Modified: Fri, 03 Sep 2021 03:29:54 GMT  
		Size: 38.3 MB (38327902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcf366f61dd5a6e3f29db0644b50af2577a4ae82aedee25ce1f3e226a690f84`  
		Last Modified: Fri, 03 Sep 2021 03:29:46 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61d08d81dfc4c1d79f5c47eb08afaf69ad12a183ffa975bd5ed0f2cc7d52473`  
		Last Modified: Fri, 03 Sep 2021 03:29:47 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd771aee2786b84f0e966a0184c6b3dfc508ec18f3910446724672a4e5a3cbd`  
		Last Modified: Fri, 03 Sep 2021 03:29:46 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:8b3b18fc16ecc98e1bf91daaa69ba32719b5c6aea8f1816553ba941399eac678
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59002534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bcd89da09295d29aeddbf3b845afd96a58b115fbcb4aaeb3f1e9b4126500260`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Sep 2021 01:05:16 GMT
ADD file:425f8ae3b1354b9858904edb027190b58b65692a710cb50a4d463ac554f853a6 in / 
# Fri, 03 Sep 2021 01:05:17 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 02:46:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 02:46:19 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 03 Sep 2021 02:46:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Sep 2021 02:46:53 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Sep 2021 02:46:53 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Sep 2021 02:46:54 GMT
EXPOSE 8888
# Fri, 03 Sep 2021 02:46:54 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Sep 2021 02:46:55 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Sep 2021 02:46:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 02:46:56 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0c15a1a8c9dffe5dfe059b37d14b92f1eb4ea47f16ae7bf66bf62f34a7510dd6`  
		Last Modified: Fri, 03 Sep 2021 01:22:37 GMT  
		Size: 19.3 MB (19316099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72feb6c10261bcd9f265aa351af235fc6d6eb3473fad71a9579edc13f7328fa2`  
		Last Modified: Fri, 03 Sep 2021 02:49:40 GMT  
		Size: 3.9 MB (3879487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ddcfdb344e67d03f1b7a9cd328a06cbeca291255d3be23eace2601350070fa8`  
		Last Modified: Fri, 03 Sep 2021 02:49:56 GMT  
		Size: 35.8 MB (35782561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066675693109c82818a2b7cd4bd8a8e696b01141184fe0ee98354c45b0fbc140`  
		Last Modified: Fri, 03 Sep 2021 02:49:38 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4e25e7194766392fd80eed393de68cd1e2fb01396ecb0a421dbb046e1fc947`  
		Last Modified: Fri, 03 Sep 2021 02:49:38 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7170ad340de1bfc4912904c7dedb7f2308b8593444f2c0503a68b16faffdfa7b`  
		Last Modified: Fri, 03 Sep 2021 02:49:38 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:b4de3a1e320ac08817b4882160c4a6e2f33bbb06555edf5e655d6e0fa61e6e2b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60482004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3d3495eda72aa6f41a8c219f335db9ba6745e0809588b4f801d45294bee512`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Sep 2021 00:42:48 GMT
ADD file:f45934b05bd47c443a0ac02ba0771c25002763d29eb9f8ae723980605ff6f091 in / 
# Fri, 03 Sep 2021 00:42:48 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 04:05:43 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 04:05:43 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 03 Sep 2021 04:05:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Sep 2021 04:05:54 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Sep 2021 04:05:54 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Sep 2021 04:05:55 GMT
EXPOSE 8888
# Fri, 03 Sep 2021 04:05:55 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Sep 2021 04:05:55 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Sep 2021 04:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 04:05:55 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bafcab9e99462b57e2818f0017c17049cc46e69473e9d80342344f7116f32e83`  
		Last Modified: Fri, 03 Sep 2021 00:53:26 GMT  
		Size: 20.4 MB (20389506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f429787bc9369e2a73687002bd6f3a4db08dfae9c2fb518c14b3868aa3bd03`  
		Last Modified: Fri, 03 Sep 2021 04:07:14 GMT  
		Size: 4.1 MB (4082099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa00853a7dcb6f3d2c511647513db31ccb10e00dbbe49a189e21547d06b69221`  
		Last Modified: Fri, 03 Sep 2021 04:07:18 GMT  
		Size: 36.0 MB (35986014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a49fe8878086a54e507534702012ef4844946a683b06abc1929698d0f2a4cd4`  
		Last Modified: Fri, 03 Sep 2021 04:07:13 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7264941c5b0fb8e39d98bc920ca64fe4fba001c1c81c0c79c1a2cbd3ad84095e`  
		Last Modified: Fri, 03 Sep 2021 04:07:13 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571e3f3624058fae1fd839cc495825a03c6722fe872f0f92cf3e88200089f85b`  
		Last Modified: Fri, 03 Sep 2021 04:07:13 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:9b177c70e25de297b100d46ba7eb922ac167a8e65f698480e2785b1886cb94a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:c3a41e489e87268456b3ac8beea5f7c2a516dc7d43af6f7066be8b9675492d70
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22662384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a94fa13b711dbb3a88df7489d3353cc6e4777a37a87a0788d36cef2fdc64c95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:23:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:23:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 01 Sep 2021 00:24:02 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 01 Sep 2021 00:24:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 01 Sep 2021 00:24:14 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 01 Sep 2021 00:24:15 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 01 Sep 2021 00:24:15 GMT
EXPOSE 8888
# Wed, 01 Sep 2021 00:24:15 GMT
VOLUME [/var/lib/chronograf]
# Wed, 01 Sep 2021 00:24:16 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 01 Sep 2021 00:24:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 00:24:16 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69cd3502d3b453e253ea48e4ff56f5af4e25895a1bfa5e84cda59eaefce23be`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7087df4b29e442773e368f72aa50cd7765fd6e6b43879c83880b0038e62b9077`  
		Last Modified: Wed, 01 Sep 2021 00:25:29 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a1ffa92682ef14beba92c11f3c21d02b50a70f56f234ab814e604f678b2b31`  
		Last Modified: Wed, 01 Sep 2021 00:25:49 GMT  
		Size: 19.6 MB (19555249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37dbb12c4afee159bb53c97f3d0cb65034efe2713363365b1f7f5f7affb916fe`  
		Last Modified: Wed, 01 Sep 2021 00:25:43 GMT  
		Size: 12.3 KB (12265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344ba26fb8530e7520df76f60ae8b3f9e317561d15deea2b4738f5c3e4b47e11`  
		Last Modified: Wed, 01 Sep 2021 00:25:43 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9b8b115b6329338ab5fea52358a641fbb017ecd917613643e4cbce6b3f081f`  
		Last Modified: Wed, 01 Sep 2021 00:25:43 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:85fbd188947f50e0805b8f7dd82067faac6dba6999fa320459aba6e9f4f2eea7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8` - linux; amd64

```console
$ docker pull chronograf@sha256:2edc5de9b854517ec3ddaadd3397ec015c6a3ca2c81d135363c52cc7bda5ba4a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66238318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094849e07aeb07247bf7def7a4be41c4e6275a7defd3b7727c916ba7c5c734e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Sep 2021 01:23:46 GMT
ADD file:b8ae56829d548d5bff373622e23d0352bb9d313f09d8fea76dc1892b16c768c8 in / 
# Fri, 03 Sep 2021 01:23:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 03:26:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 03:28:15 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 03 Sep 2021 03:28:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Sep 2021 03:28:27 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Sep 2021 03:28:28 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Sep 2021 03:28:28 GMT
EXPOSE 8888
# Fri, 03 Sep 2021 03:28:28 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Sep 2021 03:28:29 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Sep 2021 03:28:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 03:28:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:442547fc262c2ebd1e2d44ea04cb011b78ec62cc2314c8c71c68ba31ae002cdb`  
		Last Modified: Fri, 03 Sep 2021 01:32:07 GMT  
		Size: 22.5 MB (22527429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be12855d82625381afbb3ee75d1d8895188661b935409594e5f2dd05563ef11a`  
		Last Modified: Fri, 03 Sep 2021 03:29:31 GMT  
		Size: 6.8 MB (6760224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae8a5484ed24ba4bc8a0140d7aa8a5d0acc2733577c289e191db0aa190f96c4`  
		Last Modified: Fri, 03 Sep 2021 03:30:14 GMT  
		Size: 36.9 MB (36926288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527b042cd48abfcde2b52c5bb1940e734d0b99d22d6100f7a66bce8625ca5930`  
		Last Modified: Fri, 03 Sep 2021 03:30:06 GMT  
		Size: 12.2 KB (12238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709f4ec0ce083159d4a0ebbc50b121e1d54749ae0b80990fc21feab5dd217483`  
		Last Modified: Fri, 03 Sep 2021 03:30:06 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe7d68b1ea4801cf2f779dd3c0e34f346a66d0130e64fc24ebdc3c104172ad8`  
		Last Modified: Fri, 03 Sep 2021 03:30:07 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:68f4eea3e9539c8bb88a29f1a805b2ba18bc9e7c78d75549abc0c2ea1471f5a8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59630013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bde18e3cc4aea138619ed10c2da36aca91ec660823f6310027e0fdcd0e8b155`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Sep 2021 01:05:16 GMT
ADD file:425f8ae3b1354b9858904edb027190b58b65692a710cb50a4d463ac554f853a6 in / 
# Fri, 03 Sep 2021 01:05:17 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 02:45:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 02:47:10 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 03 Sep 2021 02:47:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Sep 2021 02:47:31 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Sep 2021 02:47:32 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Sep 2021 02:47:32 GMT
EXPOSE 8888
# Fri, 03 Sep 2021 02:47:33 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Sep 2021 02:47:34 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Sep 2021 02:47:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 02:47:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0c15a1a8c9dffe5dfe059b37d14b92f1eb4ea47f16ae7bf66bf62f34a7510dd6`  
		Last Modified: Fri, 03 Sep 2021 01:22:37 GMT  
		Size: 19.3 MB (19316099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb41f6e44cc2adc7b1da1ef11c2a061b83d79ad3aec2895b90e80a08e2eeb1be`  
		Last Modified: Fri, 03 Sep 2021 02:49:09 GMT  
		Size: 5.8 MB (5779569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad6b722e467f0d32ff6afcf74dd4ef6cdc90463d5e905ce2af68184bc1d88d4`  
		Last Modified: Fri, 03 Sep 2021 02:50:27 GMT  
		Size: 34.5 MB (34509957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e7d7c2fb7650aa3c5cd510ca927a393170e7e92b4272f51ad20a5e068655534`  
		Last Modified: Fri, 03 Sep 2021 02:50:09 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1606dfd7c0e45badcae83cbb33a057aa34259593d16c77a0547f91bd6ff1f7d`  
		Last Modified: Fri, 03 Sep 2021 02:50:09 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfece565b9d738d7e39eea024c0ee291784e9bf6cd4211dd0a6ffb1dbf3c4455`  
		Last Modified: Fri, 03 Sep 2021 02:50:09 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:fd16d4921ddc1bd222b58e0cd64b16dab8d02e94aa6a900deef570c759f2030f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60893528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52bb6899a82a465b87dd7a70d38f5c4242f3c44db2bb9996f40a7fbf6eaef78a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Sep 2021 00:42:48 GMT
ADD file:f45934b05bd47c443a0ac02ba0771c25002763d29eb9f8ae723980605ff6f091 in / 
# Fri, 03 Sep 2021 00:42:48 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 04:05:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 04:06:04 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 03 Sep 2021 04:06:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Sep 2021 04:06:12 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Sep 2021 04:06:12 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Sep 2021 04:06:13 GMT
EXPOSE 8888
# Fri, 03 Sep 2021 04:06:13 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Sep 2021 04:06:13 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Sep 2021 04:06:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 04:06:13 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bafcab9e99462b57e2818f0017c17049cc46e69473e9d80342344f7116f32e83`  
		Last Modified: Fri, 03 Sep 2021 00:53:26 GMT  
		Size: 20.4 MB (20389506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4762f07e63310ce400f753c3ac76f40f5fd9ce8bb5ea00be953918b761d0bece`  
		Last Modified: Fri, 03 Sep 2021 04:07:00 GMT  
		Size: 6.0 MB (6047465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e0452c8fda613606c9db3835a5424a70a9892f04168838bd50513a7588cb0e`  
		Last Modified: Fri, 03 Sep 2021 04:07:35 GMT  
		Size: 34.4 MB (34432177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3727362fea4fd67d20d6846e93c46829e41d47318199151ab6b1a5aad376b49`  
		Last Modified: Fri, 03 Sep 2021 04:07:31 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b28e4291e77c49d359b0ad85218c89411dda6b91085a5ddea83f1e2a7e5408`  
		Last Modified: Fri, 03 Sep 2021 04:07:30 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7cd707987ab021f9a7543e7db7ea84ca5678e89b594a3d2fa488c537f40c737`  
		Last Modified: Fri, 03 Sep 2021 04:07:30 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:30f63fa8f9214eb152af97cd85908e510c913d81f80a49b9c232ea42c281b9d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:7c4dd500f22766f0a514d9a2d1d13c944e2aaeb5be7f2be304ae8ef21ec9bead
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22311020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419075de283e08462528ab9737dd9a32b8e4150dc96635bda486afb9571f2905`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:23:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:23:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 01 Sep 2021 00:24:24 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 01 Sep 2021 00:24:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 01 Sep 2021 00:24:31 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 01 Sep 2021 00:24:32 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 01 Sep 2021 00:24:32 GMT
EXPOSE 8888
# Wed, 01 Sep 2021 00:24:33 GMT
VOLUME [/var/lib/chronograf]
# Wed, 01 Sep 2021 00:24:33 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 01 Sep 2021 00:24:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 00:24:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69cd3502d3b453e253ea48e4ff56f5af4e25895a1bfa5e84cda59eaefce23be`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7087df4b29e442773e368f72aa50cd7765fd6e6b43879c83880b0038e62b9077`  
		Last Modified: Wed, 01 Sep 2021 00:25:29 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9dd2619092db5ca6cb874052a71c03376efbdde1ef7f45ffd85cfa8282b9fd`  
		Last Modified: Wed, 01 Sep 2021 00:26:04 GMT  
		Size: 19.2 MB (19203889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e799830d16117d477b1f2c4fa56db3520d04b1100e2330e4e4f5458ff89e0968`  
		Last Modified: Wed, 01 Sep 2021 00:26:00 GMT  
		Size: 12.3 KB (12259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c610504f400b831a31045e828f0250e107de5ad4786642d241b0b70d2e5f744`  
		Last Modified: Wed, 01 Sep 2021 00:26:00 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996e4d82939f361d8f0003173b864e68be9fe64e83e3f4cabba3aafe8ef39f01`  
		Last Modified: Wed, 01 Sep 2021 00:26:00 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:85fbd188947f50e0805b8f7dd82067faac6dba6999fa320459aba6e9f4f2eea7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8.10` - linux; amd64

```console
$ docker pull chronograf@sha256:2edc5de9b854517ec3ddaadd3397ec015c6a3ca2c81d135363c52cc7bda5ba4a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66238318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094849e07aeb07247bf7def7a4be41c4e6275a7defd3b7727c916ba7c5c734e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Sep 2021 01:23:46 GMT
ADD file:b8ae56829d548d5bff373622e23d0352bb9d313f09d8fea76dc1892b16c768c8 in / 
# Fri, 03 Sep 2021 01:23:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 03:26:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 03:28:15 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 03 Sep 2021 03:28:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Sep 2021 03:28:27 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Sep 2021 03:28:28 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Sep 2021 03:28:28 GMT
EXPOSE 8888
# Fri, 03 Sep 2021 03:28:28 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Sep 2021 03:28:29 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Sep 2021 03:28:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 03:28:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:442547fc262c2ebd1e2d44ea04cb011b78ec62cc2314c8c71c68ba31ae002cdb`  
		Last Modified: Fri, 03 Sep 2021 01:32:07 GMT  
		Size: 22.5 MB (22527429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be12855d82625381afbb3ee75d1d8895188661b935409594e5f2dd05563ef11a`  
		Last Modified: Fri, 03 Sep 2021 03:29:31 GMT  
		Size: 6.8 MB (6760224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae8a5484ed24ba4bc8a0140d7aa8a5d0acc2733577c289e191db0aa190f96c4`  
		Last Modified: Fri, 03 Sep 2021 03:30:14 GMT  
		Size: 36.9 MB (36926288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527b042cd48abfcde2b52c5bb1940e734d0b99d22d6100f7a66bce8625ca5930`  
		Last Modified: Fri, 03 Sep 2021 03:30:06 GMT  
		Size: 12.2 KB (12238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709f4ec0ce083159d4a0ebbc50b121e1d54749ae0b80990fc21feab5dd217483`  
		Last Modified: Fri, 03 Sep 2021 03:30:06 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe7d68b1ea4801cf2f779dd3c0e34f346a66d0130e64fc24ebdc3c104172ad8`  
		Last Modified: Fri, 03 Sep 2021 03:30:07 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:68f4eea3e9539c8bb88a29f1a805b2ba18bc9e7c78d75549abc0c2ea1471f5a8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59630013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bde18e3cc4aea138619ed10c2da36aca91ec660823f6310027e0fdcd0e8b155`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Sep 2021 01:05:16 GMT
ADD file:425f8ae3b1354b9858904edb027190b58b65692a710cb50a4d463ac554f853a6 in / 
# Fri, 03 Sep 2021 01:05:17 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 02:45:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 02:47:10 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 03 Sep 2021 02:47:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Sep 2021 02:47:31 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Sep 2021 02:47:32 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Sep 2021 02:47:32 GMT
EXPOSE 8888
# Fri, 03 Sep 2021 02:47:33 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Sep 2021 02:47:34 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Sep 2021 02:47:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 02:47:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0c15a1a8c9dffe5dfe059b37d14b92f1eb4ea47f16ae7bf66bf62f34a7510dd6`  
		Last Modified: Fri, 03 Sep 2021 01:22:37 GMT  
		Size: 19.3 MB (19316099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb41f6e44cc2adc7b1da1ef11c2a061b83d79ad3aec2895b90e80a08e2eeb1be`  
		Last Modified: Fri, 03 Sep 2021 02:49:09 GMT  
		Size: 5.8 MB (5779569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad6b722e467f0d32ff6afcf74dd4ef6cdc90463d5e905ce2af68184bc1d88d4`  
		Last Modified: Fri, 03 Sep 2021 02:50:27 GMT  
		Size: 34.5 MB (34509957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e7d7c2fb7650aa3c5cd510ca927a393170e7e92b4272f51ad20a5e068655534`  
		Last Modified: Fri, 03 Sep 2021 02:50:09 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1606dfd7c0e45badcae83cbb33a057aa34259593d16c77a0547f91bd6ff1f7d`  
		Last Modified: Fri, 03 Sep 2021 02:50:09 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfece565b9d738d7e39eea024c0ee291784e9bf6cd4211dd0a6ffb1dbf3c4455`  
		Last Modified: Fri, 03 Sep 2021 02:50:09 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:fd16d4921ddc1bd222b58e0cd64b16dab8d02e94aa6a900deef570c759f2030f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60893528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52bb6899a82a465b87dd7a70d38f5c4242f3c44db2bb9996f40a7fbf6eaef78a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Sep 2021 00:42:48 GMT
ADD file:f45934b05bd47c443a0ac02ba0771c25002763d29eb9f8ae723980605ff6f091 in / 
# Fri, 03 Sep 2021 00:42:48 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 04:05:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 04:06:04 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 03 Sep 2021 04:06:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Sep 2021 04:06:12 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Sep 2021 04:06:12 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Sep 2021 04:06:13 GMT
EXPOSE 8888
# Fri, 03 Sep 2021 04:06:13 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Sep 2021 04:06:13 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Sep 2021 04:06:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 04:06:13 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bafcab9e99462b57e2818f0017c17049cc46e69473e9d80342344f7116f32e83`  
		Last Modified: Fri, 03 Sep 2021 00:53:26 GMT  
		Size: 20.4 MB (20389506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4762f07e63310ce400f753c3ac76f40f5fd9ce8bb5ea00be953918b761d0bece`  
		Last Modified: Fri, 03 Sep 2021 04:07:00 GMT  
		Size: 6.0 MB (6047465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e0452c8fda613606c9db3835a5424a70a9892f04168838bd50513a7588cb0e`  
		Last Modified: Fri, 03 Sep 2021 04:07:35 GMT  
		Size: 34.4 MB (34432177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3727362fea4fd67d20d6846e93c46829e41d47318199151ab6b1a5aad376b49`  
		Last Modified: Fri, 03 Sep 2021 04:07:31 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b28e4291e77c49d359b0ad85218c89411dda6b91085a5ddea83f1e2a7e5408`  
		Last Modified: Fri, 03 Sep 2021 04:07:30 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7cd707987ab021f9a7543e7db7ea84ca5678e89b594a3d2fa488c537f40c737`  
		Last Modified: Fri, 03 Sep 2021 04:07:30 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:30f63fa8f9214eb152af97cd85908e510c913d81f80a49b9c232ea42c281b9d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:7c4dd500f22766f0a514d9a2d1d13c944e2aaeb5be7f2be304ae8ef21ec9bead
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22311020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419075de283e08462528ab9737dd9a32b8e4150dc96635bda486afb9571f2905`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:23:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:23:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 01 Sep 2021 00:24:24 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 01 Sep 2021 00:24:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 01 Sep 2021 00:24:31 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 01 Sep 2021 00:24:32 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 01 Sep 2021 00:24:32 GMT
EXPOSE 8888
# Wed, 01 Sep 2021 00:24:33 GMT
VOLUME [/var/lib/chronograf]
# Wed, 01 Sep 2021 00:24:33 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 01 Sep 2021 00:24:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 00:24:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69cd3502d3b453e253ea48e4ff56f5af4e25895a1bfa5e84cda59eaefce23be`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7087df4b29e442773e368f72aa50cd7765fd6e6b43879c83880b0038e62b9077`  
		Last Modified: Wed, 01 Sep 2021 00:25:29 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9dd2619092db5ca6cb874052a71c03376efbdde1ef7f45ffd85cfa8282b9fd`  
		Last Modified: Wed, 01 Sep 2021 00:26:04 GMT  
		Size: 19.2 MB (19203889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e799830d16117d477b1f2c4fa56db3520d04b1100e2330e4e4f5458ff89e0968`  
		Last Modified: Wed, 01 Sep 2021 00:26:00 GMT  
		Size: 12.3 KB (12259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c610504f400b831a31045e828f0250e107de5ad4786642d241b0b70d2e5f744`  
		Last Modified: Wed, 01 Sep 2021 00:26:00 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996e4d82939f361d8f0003173b864e68be9fe64e83e3f4cabba3aafe8ef39f01`  
		Last Modified: Wed, 01 Sep 2021 00:26:00 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:f8624d9e096596676ad8404eb9ae906278c950ed767d7d447291137851fa28d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9` - linux; amd64

```console
$ docker pull chronograf@sha256:130d51b2cd929156eaf436780e13977ae08061f32d0d1249249d2611b9f3d7a0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66757112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7188b868360ee863ce24c3cc7135e27947600d5ee91b3ba90a2c310d4104310`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Sep 2021 01:23:46 GMT
ADD file:b8ae56829d548d5bff373622e23d0352bb9d313f09d8fea76dc1892b16c768c8 in / 
# Fri, 03 Sep 2021 01:23:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 03:26:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 03:28:37 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Fri, 03 Sep 2021 03:28:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Sep 2021 03:28:50 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Sep 2021 03:28:51 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Sep 2021 03:28:51 GMT
EXPOSE 8888
# Fri, 03 Sep 2021 03:28:51 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Sep 2021 03:28:52 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Sep 2021 03:28:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 03:28:52 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:442547fc262c2ebd1e2d44ea04cb011b78ec62cc2314c8c71c68ba31ae002cdb`  
		Last Modified: Fri, 03 Sep 2021 01:32:07 GMT  
		Size: 22.5 MB (22527429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be12855d82625381afbb3ee75d1d8895188661b935409594e5f2dd05563ef11a`  
		Last Modified: Fri, 03 Sep 2021 03:29:31 GMT  
		Size: 6.8 MB (6760224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b572e62b2166b25f7213794bcd3db35172b1638d9127443248d54edbfb30c13`  
		Last Modified: Fri, 03 Sep 2021 03:30:34 GMT  
		Size: 37.4 MB (37445072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7778486801cde48570ea55e7b77e122f90acce71b9a2181625f4282ada3049e`  
		Last Modified: Fri, 03 Sep 2021 03:30:27 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93cfe01f527db200d370fd2e9bc4814339b73091c38b0f772a68f1614c67f86`  
		Last Modified: Fri, 03 Sep 2021 03:30:27 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca6357eeef5b1b405cf5806007e4a03ef222b059e6610d8195ba4860e288252`  
		Last Modified: Fri, 03 Sep 2021 03:30:27 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:609775e3045917416f254d596222e113bebabf264680c6289ed7bb84e1aa0439
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60284183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52137975532be06a48c3ceeedbf2bbd2b4f12a58bc040cdc385b36cc3204c55`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Sep 2021 01:05:16 GMT
ADD file:425f8ae3b1354b9858904edb027190b58b65692a710cb50a4d463ac554f853a6 in / 
# Fri, 03 Sep 2021 01:05:17 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 02:45:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 02:47:46 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Fri, 03 Sep 2021 02:48:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Sep 2021 02:48:07 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Sep 2021 02:48:07 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Sep 2021 02:48:08 GMT
EXPOSE 8888
# Fri, 03 Sep 2021 02:48:08 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Sep 2021 02:48:09 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Sep 2021 02:48:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 02:48:10 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0c15a1a8c9dffe5dfe059b37d14b92f1eb4ea47f16ae7bf66bf62f34a7510dd6`  
		Last Modified: Fri, 03 Sep 2021 01:22:37 GMT  
		Size: 19.3 MB (19316099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb41f6e44cc2adc7b1da1ef11c2a061b83d79ad3aec2895b90e80a08e2eeb1be`  
		Last Modified: Fri, 03 Sep 2021 02:49:09 GMT  
		Size: 5.8 MB (5779569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a8e857ff2824613b74370561a6f3ed4cf43acb1c72b8ec0604c75892f459cb`  
		Last Modified: Fri, 03 Sep 2021 02:50:58 GMT  
		Size: 35.2 MB (35164135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736406488d5a7638a24ee9cf3f2cdefca5302b6c28f12d1ef089bd41c153f2a2`  
		Last Modified: Fri, 03 Sep 2021 02:50:40 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b3a3fb52efb0b155e1a83b168f969aab6e53eb9a512ed6c6d16150b6d5bbc`  
		Last Modified: Fri, 03 Sep 2021 02:50:40 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af17a3f630e3db6735c25b8a73919284e41ae7925693423395adcd53097c8b7`  
		Last Modified: Fri, 03 Sep 2021 02:50:40 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:c4e899753e5aa493160dfcaedc21472514b9e2e48f2d9cbbf7e22c2289707598
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61522804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18efb5253ba6c691027e337be16361081f31d9f3beb2e248005c410e6a7c3a90`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Sep 2021 00:42:48 GMT
ADD file:f45934b05bd47c443a0ac02ba0771c25002763d29eb9f8ae723980605ff6f091 in / 
# Fri, 03 Sep 2021 00:42:48 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 04:05:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 04:06:18 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Fri, 03 Sep 2021 04:06:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Sep 2021 04:06:28 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Sep 2021 04:06:28 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Sep 2021 04:06:28 GMT
EXPOSE 8888
# Fri, 03 Sep 2021 04:06:29 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Sep 2021 04:06:29 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Sep 2021 04:06:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 04:06:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bafcab9e99462b57e2818f0017c17049cc46e69473e9d80342344f7116f32e83`  
		Last Modified: Fri, 03 Sep 2021 00:53:26 GMT  
		Size: 20.4 MB (20389506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4762f07e63310ce400f753c3ac76f40f5fd9ce8bb5ea00be953918b761d0bece`  
		Last Modified: Fri, 03 Sep 2021 04:07:00 GMT  
		Size: 6.0 MB (6047465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fd47d7e8163acc736aac2cdb3a5ed4c79160c4611204bce8a391bfdc38b6d2`  
		Last Modified: Fri, 03 Sep 2021 04:07:53 GMT  
		Size: 35.1 MB (35061449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0977d89435325ae2f9ed33725f627acc58be92e87a840f01c55cedd6a9bd79a`  
		Last Modified: Fri, 03 Sep 2021 04:07:48 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8ce9bc9abb44e4da5bfb96c4f57f99cdbb3b77ff4df81d08ba1a218be83a56`  
		Last Modified: Fri, 03 Sep 2021 04:07:48 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259f8de2028849873a65bdd23449d6c79ad90a95a07698355dfbb919370f5c63`  
		Last Modified: Fri, 03 Sep 2021 04:07:48 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:bdb38dbf0d72892a4685b69391c89a1716a2465b0d52f79bd859a846f982c702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:44ddcc13955fcee6ada98e17e24ee8f695a9823b3c3e999e5d315c9a3bb0aa8e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22689227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f86636178ef7f0961c639954f1607c343f7ed49e2749304818d81e8d9aaec58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:23:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:23:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 01 Sep 2021 00:24:42 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Wed, 01 Sep 2021 00:24:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 01 Sep 2021 00:24:49 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 01 Sep 2021 00:24:49 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 01 Sep 2021 00:24:50 GMT
EXPOSE 8888
# Wed, 01 Sep 2021 00:24:50 GMT
VOLUME [/var/lib/chronograf]
# Wed, 01 Sep 2021 00:24:51 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 01 Sep 2021 00:24:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 00:24:51 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69cd3502d3b453e253ea48e4ff56f5af4e25895a1bfa5e84cda59eaefce23be`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7087df4b29e442773e368f72aa50cd7765fd6e6b43879c83880b0038e62b9077`  
		Last Modified: Wed, 01 Sep 2021 00:25:29 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0062288c23918a5c405390da5fe197e453d3162f22d5e04c4e80c771bfb7dbb`  
		Last Modified: Wed, 01 Sep 2021 00:26:19 GMT  
		Size: 19.6 MB (19582082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56af5fa9abf70534bf74916985c59602805aaec20e843a8fb80451dc2b4aa6b`  
		Last Modified: Wed, 01 Sep 2021 00:26:15 GMT  
		Size: 12.3 KB (12269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bad79cf9294c71cb171d84b1b435766c73b488c2eaf98668e8fb24c098ec8e0`  
		Last Modified: Wed, 01 Sep 2021 00:26:15 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80584912177323f577d098fda53486bc0f440c26efb41dd2951ee13af7a0f369`  
		Last Modified: Wed, 01 Sep 2021 00:26:15 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.0`

```console
$ docker pull chronograf@sha256:f8624d9e096596676ad8404eb9ae906278c950ed767d7d447291137851fa28d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9.0` - linux; amd64

```console
$ docker pull chronograf@sha256:130d51b2cd929156eaf436780e13977ae08061f32d0d1249249d2611b9f3d7a0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66757112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7188b868360ee863ce24c3cc7135e27947600d5ee91b3ba90a2c310d4104310`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Sep 2021 01:23:46 GMT
ADD file:b8ae56829d548d5bff373622e23d0352bb9d313f09d8fea76dc1892b16c768c8 in / 
# Fri, 03 Sep 2021 01:23:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 03:26:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 03:28:37 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Fri, 03 Sep 2021 03:28:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Sep 2021 03:28:50 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Sep 2021 03:28:51 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Sep 2021 03:28:51 GMT
EXPOSE 8888
# Fri, 03 Sep 2021 03:28:51 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Sep 2021 03:28:52 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Sep 2021 03:28:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 03:28:52 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:442547fc262c2ebd1e2d44ea04cb011b78ec62cc2314c8c71c68ba31ae002cdb`  
		Last Modified: Fri, 03 Sep 2021 01:32:07 GMT  
		Size: 22.5 MB (22527429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be12855d82625381afbb3ee75d1d8895188661b935409594e5f2dd05563ef11a`  
		Last Modified: Fri, 03 Sep 2021 03:29:31 GMT  
		Size: 6.8 MB (6760224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b572e62b2166b25f7213794bcd3db35172b1638d9127443248d54edbfb30c13`  
		Last Modified: Fri, 03 Sep 2021 03:30:34 GMT  
		Size: 37.4 MB (37445072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7778486801cde48570ea55e7b77e122f90acce71b9a2181625f4282ada3049e`  
		Last Modified: Fri, 03 Sep 2021 03:30:27 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93cfe01f527db200d370fd2e9bc4814339b73091c38b0f772a68f1614c67f86`  
		Last Modified: Fri, 03 Sep 2021 03:30:27 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca6357eeef5b1b405cf5806007e4a03ef222b059e6610d8195ba4860e288252`  
		Last Modified: Fri, 03 Sep 2021 03:30:27 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.0` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:609775e3045917416f254d596222e113bebabf264680c6289ed7bb84e1aa0439
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60284183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52137975532be06a48c3ceeedbf2bbd2b4f12a58bc040cdc385b36cc3204c55`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Sep 2021 01:05:16 GMT
ADD file:425f8ae3b1354b9858904edb027190b58b65692a710cb50a4d463ac554f853a6 in / 
# Fri, 03 Sep 2021 01:05:17 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 02:45:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 02:47:46 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Fri, 03 Sep 2021 02:48:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Sep 2021 02:48:07 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Sep 2021 02:48:07 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Sep 2021 02:48:08 GMT
EXPOSE 8888
# Fri, 03 Sep 2021 02:48:08 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Sep 2021 02:48:09 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Sep 2021 02:48:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 02:48:10 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0c15a1a8c9dffe5dfe059b37d14b92f1eb4ea47f16ae7bf66bf62f34a7510dd6`  
		Last Modified: Fri, 03 Sep 2021 01:22:37 GMT  
		Size: 19.3 MB (19316099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb41f6e44cc2adc7b1da1ef11c2a061b83d79ad3aec2895b90e80a08e2eeb1be`  
		Last Modified: Fri, 03 Sep 2021 02:49:09 GMT  
		Size: 5.8 MB (5779569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a8e857ff2824613b74370561a6f3ed4cf43acb1c72b8ec0604c75892f459cb`  
		Last Modified: Fri, 03 Sep 2021 02:50:58 GMT  
		Size: 35.2 MB (35164135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736406488d5a7638a24ee9cf3f2cdefca5302b6c28f12d1ef089bd41c153f2a2`  
		Last Modified: Fri, 03 Sep 2021 02:50:40 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b3a3fb52efb0b155e1a83b168f969aab6e53eb9a512ed6c6d16150b6d5bbc`  
		Last Modified: Fri, 03 Sep 2021 02:50:40 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af17a3f630e3db6735c25b8a73919284e41ae7925693423395adcd53097c8b7`  
		Last Modified: Fri, 03 Sep 2021 02:50:40 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.0` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:c4e899753e5aa493160dfcaedc21472514b9e2e48f2d9cbbf7e22c2289707598
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61522804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18efb5253ba6c691027e337be16361081f31d9f3beb2e248005c410e6a7c3a90`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Sep 2021 00:42:48 GMT
ADD file:f45934b05bd47c443a0ac02ba0771c25002763d29eb9f8ae723980605ff6f091 in / 
# Fri, 03 Sep 2021 00:42:48 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 04:05:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 04:06:18 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Fri, 03 Sep 2021 04:06:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Sep 2021 04:06:28 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Sep 2021 04:06:28 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Sep 2021 04:06:28 GMT
EXPOSE 8888
# Fri, 03 Sep 2021 04:06:29 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Sep 2021 04:06:29 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Sep 2021 04:06:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 04:06:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bafcab9e99462b57e2818f0017c17049cc46e69473e9d80342344f7116f32e83`  
		Last Modified: Fri, 03 Sep 2021 00:53:26 GMT  
		Size: 20.4 MB (20389506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4762f07e63310ce400f753c3ac76f40f5fd9ce8bb5ea00be953918b761d0bece`  
		Last Modified: Fri, 03 Sep 2021 04:07:00 GMT  
		Size: 6.0 MB (6047465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fd47d7e8163acc736aac2cdb3a5ed4c79160c4611204bce8a391bfdc38b6d2`  
		Last Modified: Fri, 03 Sep 2021 04:07:53 GMT  
		Size: 35.1 MB (35061449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0977d89435325ae2f9ed33725f627acc58be92e87a840f01c55cedd6a9bd79a`  
		Last Modified: Fri, 03 Sep 2021 04:07:48 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8ce9bc9abb44e4da5bfb96c4f57f99cdbb3b77ff4df81d08ba1a218be83a56`  
		Last Modified: Fri, 03 Sep 2021 04:07:48 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259f8de2028849873a65bdd23449d6c79ad90a95a07698355dfbb919370f5c63`  
		Last Modified: Fri, 03 Sep 2021 04:07:48 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.0-alpine`

```console
$ docker pull chronograf@sha256:bdb38dbf0d72892a4685b69391c89a1716a2465b0d52f79bd859a846f982c702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9.0-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:44ddcc13955fcee6ada98e17e24ee8f695a9823b3c3e999e5d315c9a3bb0aa8e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22689227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f86636178ef7f0961c639954f1607c343f7ed49e2749304818d81e8d9aaec58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:23:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:23:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 01 Sep 2021 00:24:42 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Wed, 01 Sep 2021 00:24:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 01 Sep 2021 00:24:49 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 01 Sep 2021 00:24:49 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 01 Sep 2021 00:24:50 GMT
EXPOSE 8888
# Wed, 01 Sep 2021 00:24:50 GMT
VOLUME [/var/lib/chronograf]
# Wed, 01 Sep 2021 00:24:51 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 01 Sep 2021 00:24:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 00:24:51 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69cd3502d3b453e253ea48e4ff56f5af4e25895a1bfa5e84cda59eaefce23be`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7087df4b29e442773e368f72aa50cd7765fd6e6b43879c83880b0038e62b9077`  
		Last Modified: Wed, 01 Sep 2021 00:25:29 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0062288c23918a5c405390da5fe197e453d3162f22d5e04c4e80c771bfb7dbb`  
		Last Modified: Wed, 01 Sep 2021 00:26:19 GMT  
		Size: 19.6 MB (19582082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56af5fa9abf70534bf74916985c59602805aaec20e843a8fb80451dc2b4aa6b`  
		Last Modified: Wed, 01 Sep 2021 00:26:15 GMT  
		Size: 12.3 KB (12269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bad79cf9294c71cb171d84b1b435766c73b488c2eaf98668e8fb24c098ec8e0`  
		Last Modified: Wed, 01 Sep 2021 00:26:15 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80584912177323f577d098fda53486bc0f440c26efb41dd2951ee13af7a0f369`  
		Last Modified: Wed, 01 Sep 2021 00:26:15 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:bdb38dbf0d72892a4685b69391c89a1716a2465b0d52f79bd859a846f982c702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:44ddcc13955fcee6ada98e17e24ee8f695a9823b3c3e999e5d315c9a3bb0aa8e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22689227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f86636178ef7f0961c639954f1607c343f7ed49e2749304818d81e8d9aaec58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:23:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:23:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 01 Sep 2021 00:24:42 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Wed, 01 Sep 2021 00:24:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 01 Sep 2021 00:24:49 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 01 Sep 2021 00:24:49 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 01 Sep 2021 00:24:50 GMT
EXPOSE 8888
# Wed, 01 Sep 2021 00:24:50 GMT
VOLUME [/var/lib/chronograf]
# Wed, 01 Sep 2021 00:24:51 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 01 Sep 2021 00:24:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 00:24:51 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69cd3502d3b453e253ea48e4ff56f5af4e25895a1bfa5e84cda59eaefce23be`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7087df4b29e442773e368f72aa50cd7765fd6e6b43879c83880b0038e62b9077`  
		Last Modified: Wed, 01 Sep 2021 00:25:29 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0062288c23918a5c405390da5fe197e453d3162f22d5e04c4e80c771bfb7dbb`  
		Last Modified: Wed, 01 Sep 2021 00:26:19 GMT  
		Size: 19.6 MB (19582082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56af5fa9abf70534bf74916985c59602805aaec20e843a8fb80451dc2b4aa6b`  
		Last Modified: Wed, 01 Sep 2021 00:26:15 GMT  
		Size: 12.3 KB (12269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bad79cf9294c71cb171d84b1b435766c73b488c2eaf98668e8fb24c098ec8e0`  
		Last Modified: Wed, 01 Sep 2021 00:26:15 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80584912177323f577d098fda53486bc0f440c26efb41dd2951ee13af7a0f369`  
		Last Modified: Wed, 01 Sep 2021 00:26:15 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:f8624d9e096596676ad8404eb9ae906278c950ed767d7d447291137851fa28d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:130d51b2cd929156eaf436780e13977ae08061f32d0d1249249d2611b9f3d7a0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66757112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7188b868360ee863ce24c3cc7135e27947600d5ee91b3ba90a2c310d4104310`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Sep 2021 01:23:46 GMT
ADD file:b8ae56829d548d5bff373622e23d0352bb9d313f09d8fea76dc1892b16c768c8 in / 
# Fri, 03 Sep 2021 01:23:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 03:26:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 03:28:37 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Fri, 03 Sep 2021 03:28:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Sep 2021 03:28:50 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Sep 2021 03:28:51 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Sep 2021 03:28:51 GMT
EXPOSE 8888
# Fri, 03 Sep 2021 03:28:51 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Sep 2021 03:28:52 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Sep 2021 03:28:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 03:28:52 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:442547fc262c2ebd1e2d44ea04cb011b78ec62cc2314c8c71c68ba31ae002cdb`  
		Last Modified: Fri, 03 Sep 2021 01:32:07 GMT  
		Size: 22.5 MB (22527429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be12855d82625381afbb3ee75d1d8895188661b935409594e5f2dd05563ef11a`  
		Last Modified: Fri, 03 Sep 2021 03:29:31 GMT  
		Size: 6.8 MB (6760224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b572e62b2166b25f7213794bcd3db35172b1638d9127443248d54edbfb30c13`  
		Last Modified: Fri, 03 Sep 2021 03:30:34 GMT  
		Size: 37.4 MB (37445072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7778486801cde48570ea55e7b77e122f90acce71b9a2181625f4282ada3049e`  
		Last Modified: Fri, 03 Sep 2021 03:30:27 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93cfe01f527db200d370fd2e9bc4814339b73091c38b0f772a68f1614c67f86`  
		Last Modified: Fri, 03 Sep 2021 03:30:27 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca6357eeef5b1b405cf5806007e4a03ef222b059e6610d8195ba4860e288252`  
		Last Modified: Fri, 03 Sep 2021 03:30:27 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:609775e3045917416f254d596222e113bebabf264680c6289ed7bb84e1aa0439
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60284183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52137975532be06a48c3ceeedbf2bbd2b4f12a58bc040cdc385b36cc3204c55`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Sep 2021 01:05:16 GMT
ADD file:425f8ae3b1354b9858904edb027190b58b65692a710cb50a4d463ac554f853a6 in / 
# Fri, 03 Sep 2021 01:05:17 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 02:45:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 02:47:46 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Fri, 03 Sep 2021 02:48:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Sep 2021 02:48:07 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Sep 2021 02:48:07 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Sep 2021 02:48:08 GMT
EXPOSE 8888
# Fri, 03 Sep 2021 02:48:08 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Sep 2021 02:48:09 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Sep 2021 02:48:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 02:48:10 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0c15a1a8c9dffe5dfe059b37d14b92f1eb4ea47f16ae7bf66bf62f34a7510dd6`  
		Last Modified: Fri, 03 Sep 2021 01:22:37 GMT  
		Size: 19.3 MB (19316099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb41f6e44cc2adc7b1da1ef11c2a061b83d79ad3aec2895b90e80a08e2eeb1be`  
		Last Modified: Fri, 03 Sep 2021 02:49:09 GMT  
		Size: 5.8 MB (5779569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a8e857ff2824613b74370561a6f3ed4cf43acb1c72b8ec0604c75892f459cb`  
		Last Modified: Fri, 03 Sep 2021 02:50:58 GMT  
		Size: 35.2 MB (35164135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736406488d5a7638a24ee9cf3f2cdefca5302b6c28f12d1ef089bd41c153f2a2`  
		Last Modified: Fri, 03 Sep 2021 02:50:40 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b3a3fb52efb0b155e1a83b168f969aab6e53eb9a512ed6c6d16150b6d5bbc`  
		Last Modified: Fri, 03 Sep 2021 02:50:40 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af17a3f630e3db6735c25b8a73919284e41ae7925693423395adcd53097c8b7`  
		Last Modified: Fri, 03 Sep 2021 02:50:40 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:c4e899753e5aa493160dfcaedc21472514b9e2e48f2d9cbbf7e22c2289707598
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61522804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18efb5253ba6c691027e337be16361081f31d9f3beb2e248005c410e6a7c3a90`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Sep 2021 00:42:48 GMT
ADD file:f45934b05bd47c443a0ac02ba0771c25002763d29eb9f8ae723980605ff6f091 in / 
# Fri, 03 Sep 2021 00:42:48 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 04:05:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 04:06:18 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Fri, 03 Sep 2021 04:06:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Sep 2021 04:06:28 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Sep 2021 04:06:28 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Sep 2021 04:06:28 GMT
EXPOSE 8888
# Fri, 03 Sep 2021 04:06:29 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Sep 2021 04:06:29 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Sep 2021 04:06:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 04:06:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bafcab9e99462b57e2818f0017c17049cc46e69473e9d80342344f7116f32e83`  
		Last Modified: Fri, 03 Sep 2021 00:53:26 GMT  
		Size: 20.4 MB (20389506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4762f07e63310ce400f753c3ac76f40f5fd9ce8bb5ea00be953918b761d0bece`  
		Last Modified: Fri, 03 Sep 2021 04:07:00 GMT  
		Size: 6.0 MB (6047465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fd47d7e8163acc736aac2cdb3a5ed4c79160c4611204bce8a391bfdc38b6d2`  
		Last Modified: Fri, 03 Sep 2021 04:07:53 GMT  
		Size: 35.1 MB (35061449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0977d89435325ae2f9ed33725f627acc58be92e87a840f01c55cedd6a9bd79a`  
		Last Modified: Fri, 03 Sep 2021 04:07:48 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8ce9bc9abb44e4da5bfb96c4f57f99cdbb3b77ff4df81d08ba1a218be83a56`  
		Last Modified: Fri, 03 Sep 2021 04:07:48 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259f8de2028849873a65bdd23449d6c79ad90a95a07698355dfbb919370f5c63`  
		Last Modified: Fri, 03 Sep 2021 04:07:48 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
