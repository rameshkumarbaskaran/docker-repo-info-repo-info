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
-	[`chronograf:1.9.1`](#chronograf191)
-	[`chronograf:1.9.1-alpine`](#chronograf191-alpine)
-	[`chronograf:alpine`](#chronografalpine)
-	[`chronograf:latest`](#chronograflatest)

## `chronograf:1.6`

```console
$ docker pull chronograf@sha256:b57484c5bc6269d7846f55f499d4d859d8cb4c13ed7d374ec25b11dd51bc06cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6` - linux; amd64

```console
$ docker pull chronograf@sha256:9b6e45461a6131f427dec3561927653a30acbe6351537c3e1705be8407c3a7f9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49357279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2787aa994425d922e88d7df5d8cbaab33084fd24aec062ed91fb6a6075b24885`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:22:52 GMT
ADD file:1220579e31585dec45ca8e35874eb689018ed026a1f23b7906f791c0279671e0 in / 
# Tue, 12 Oct 2021 01:22:53 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:13:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 15:13:27 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 12 Oct 2021 15:13:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 15:13:36 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 15:13:36 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 15:13:36 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 15:13:36 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 15:13:36 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 15:13:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 15:13:37 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:eec53b8a5053c739b5b685cb372b38eea3286ab6626532bad963291f76357c5f`  
		Last Modified: Tue, 12 Oct 2021 01:29:50 GMT  
		Size: 22.5 MB (22527572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af087790cf4907eb60360fae75759db60331cfdfb749ae8593e374a3afb328f`  
		Last Modified: Tue, 12 Oct 2021 15:15:15 GMT  
		Size: 6.8 MB (6760208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66087bf7be5c579789511a21c106da28de5de4dab61cb75b514b4c737e403764`  
		Last Modified: Tue, 12 Oct 2021 15:15:17 GMT  
		Size: 20.0 MB (20045112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d39018c54114d2d1c74266bc1843a885fa863defaa88b75222c7ee282278598`  
		Last Modified: Tue, 12 Oct 2021 15:15:13 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9c0274b2fa67c68a28d02c8ec15be12be755ad04061e31050cfb1086cdf45d`  
		Last Modified: Tue, 12 Oct 2021 15:15:13 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b80da8236c0c6d1017f54ab63d7807fa4419ddf39eb0bfd3e691a845465ed51`  
		Last Modified: Tue, 12 Oct 2021 15:15:13 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:2f7ab4550c5a33718fbc57ace9e323139261d26d24f7964438b807f6aa54aa21
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43941727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3b6928c30816e270273153010070663706e2fc23d2bbf28e0aeb515c6f9cea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:34:42 GMT
ADD file:9bfcfd0aaac802b902b0e842e040a6599c461c90b73579bcacc2fbdda7ec39cb in / 
# Tue, 12 Oct 2021 01:34:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 19:38:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 19:38:55 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 12 Oct 2021 19:39:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 19:39:14 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 19:39:14 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 19:39:15 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 19:39:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 19:39:16 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 19:39:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 19:39:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a1a3620b17011bd36d6f64dfcc8fd7c4cb3da78d19a59efb1b35afcadaf3f6a8`  
		Last Modified: Tue, 12 Oct 2021 01:51:59 GMT  
		Size: 19.3 MB (19316474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bdc2f2b4d96b348e56cf5179e6a1d2f89538251124d2659dcb521c5c19e51bb`  
		Last Modified: Tue, 12 Oct 2021 19:42:36 GMT  
		Size: 5.8 MB (5780488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90062e4eca0454a6b55d5ed50bff4c7deb791c7d22de226597152334d9bb073e`  
		Last Modified: Tue, 12 Oct 2021 19:42:41 GMT  
		Size: 18.8 MB (18820372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd9dd16d2c73dd4fd0238fdc97b81a2d79b2506c51c187351cd7ac5da3c5719`  
		Last Modified: Tue, 12 Oct 2021 19:42:33 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108f35c398f2e1184fc422610949e17eca7c582e770dd0afbdfa19fd1bca1a71`  
		Last Modified: Tue, 12 Oct 2021 19:42:34 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c80b9aa5ed4f16409267c0781b4830096e20ec938021f2d257d52ea25ae9e4`  
		Last Modified: Tue, 12 Oct 2021 19:42:33 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:f3f94b901f49e9126af4b6764a613041372c241862f143f41f841842b0d02198
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45423602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d822691295a3377b2e34a1a8d951ea6f95ab88442e4e023708fce26aa0a47a7d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:43:29 GMT
ADD file:ebfc214a3da7b706f0759fd22fa991c905976d2c970b2d59d134753f7cbd5e06 in / 
# Tue, 12 Oct 2021 01:43:29 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 02:24:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 02:24:49 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 12 Oct 2021 02:24:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 02:24:57 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 02:24:57 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 02:24:57 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 02:24:57 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 02:24:57 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 02:24:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 02:24:58 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0b0a22641ad2aad782c696887c59bf05ec0b1e7aa1e07902ee51949bab802657`  
		Last Modified: Tue, 12 Oct 2021 01:52:33 GMT  
		Size: 20.4 MB (20389450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693941dd06bd7505ff4633db32f85f682bb43790f889c3700a0cc8f95a8775a`  
		Last Modified: Tue, 12 Oct 2021 02:26:22 GMT  
		Size: 6.0 MB (6047991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c80a13875d1601dda5709f1d69a00589cf3ce58b12f53fa1f724cd72014207`  
		Last Modified: Tue, 12 Oct 2021 02:26:25 GMT  
		Size: 19.0 MB (18961773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385e3003b1770a74069520dd203b4146211b03893fe9e3cb1128bbec6988f20e`  
		Last Modified: Tue, 12 Oct 2021 02:26:21 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c20fad82f79c98ea608757c45478eee61b9bd857812b095623c2765c82e5f8f`  
		Last Modified: Tue, 12 Oct 2021 02:26:21 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d145d4d4dbcb7a3f9c5ed61739d22752a3376db5bef7dd9939b863381d500426`  
		Last Modified: Tue, 12 Oct 2021 02:26:21 GMT  
		Size: 238.0 B  
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
$ docker pull chronograf@sha256:b57484c5bc6269d7846f55f499d4d859d8cb4c13ed7d374ec25b11dd51bc06cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6.2` - linux; amd64

```console
$ docker pull chronograf@sha256:9b6e45461a6131f427dec3561927653a30acbe6351537c3e1705be8407c3a7f9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49357279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2787aa994425d922e88d7df5d8cbaab33084fd24aec062ed91fb6a6075b24885`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:22:52 GMT
ADD file:1220579e31585dec45ca8e35874eb689018ed026a1f23b7906f791c0279671e0 in / 
# Tue, 12 Oct 2021 01:22:53 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:13:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 15:13:27 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 12 Oct 2021 15:13:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 15:13:36 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 15:13:36 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 15:13:36 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 15:13:36 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 15:13:36 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 15:13:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 15:13:37 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:eec53b8a5053c739b5b685cb372b38eea3286ab6626532bad963291f76357c5f`  
		Last Modified: Tue, 12 Oct 2021 01:29:50 GMT  
		Size: 22.5 MB (22527572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af087790cf4907eb60360fae75759db60331cfdfb749ae8593e374a3afb328f`  
		Last Modified: Tue, 12 Oct 2021 15:15:15 GMT  
		Size: 6.8 MB (6760208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66087bf7be5c579789511a21c106da28de5de4dab61cb75b514b4c737e403764`  
		Last Modified: Tue, 12 Oct 2021 15:15:17 GMT  
		Size: 20.0 MB (20045112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d39018c54114d2d1c74266bc1843a885fa863defaa88b75222c7ee282278598`  
		Last Modified: Tue, 12 Oct 2021 15:15:13 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9c0274b2fa67c68a28d02c8ec15be12be755ad04061e31050cfb1086cdf45d`  
		Last Modified: Tue, 12 Oct 2021 15:15:13 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b80da8236c0c6d1017f54ab63d7807fa4419ddf39eb0bfd3e691a845465ed51`  
		Last Modified: Tue, 12 Oct 2021 15:15:13 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:2f7ab4550c5a33718fbc57ace9e323139261d26d24f7964438b807f6aa54aa21
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43941727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3b6928c30816e270273153010070663706e2fc23d2bbf28e0aeb515c6f9cea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:34:42 GMT
ADD file:9bfcfd0aaac802b902b0e842e040a6599c461c90b73579bcacc2fbdda7ec39cb in / 
# Tue, 12 Oct 2021 01:34:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 19:38:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 19:38:55 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 12 Oct 2021 19:39:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 19:39:14 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 19:39:14 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 19:39:15 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 19:39:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 19:39:16 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 19:39:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 19:39:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a1a3620b17011bd36d6f64dfcc8fd7c4cb3da78d19a59efb1b35afcadaf3f6a8`  
		Last Modified: Tue, 12 Oct 2021 01:51:59 GMT  
		Size: 19.3 MB (19316474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bdc2f2b4d96b348e56cf5179e6a1d2f89538251124d2659dcb521c5c19e51bb`  
		Last Modified: Tue, 12 Oct 2021 19:42:36 GMT  
		Size: 5.8 MB (5780488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90062e4eca0454a6b55d5ed50bff4c7deb791c7d22de226597152334d9bb073e`  
		Last Modified: Tue, 12 Oct 2021 19:42:41 GMT  
		Size: 18.8 MB (18820372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd9dd16d2c73dd4fd0238fdc97b81a2d79b2506c51c187351cd7ac5da3c5719`  
		Last Modified: Tue, 12 Oct 2021 19:42:33 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108f35c398f2e1184fc422610949e17eca7c582e770dd0afbdfa19fd1bca1a71`  
		Last Modified: Tue, 12 Oct 2021 19:42:34 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c80b9aa5ed4f16409267c0781b4830096e20ec938021f2d257d52ea25ae9e4`  
		Last Modified: Tue, 12 Oct 2021 19:42:33 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:f3f94b901f49e9126af4b6764a613041372c241862f143f41f841842b0d02198
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45423602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d822691295a3377b2e34a1a8d951ea6f95ab88442e4e023708fce26aa0a47a7d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:43:29 GMT
ADD file:ebfc214a3da7b706f0759fd22fa991c905976d2c970b2d59d134753f7cbd5e06 in / 
# Tue, 12 Oct 2021 01:43:29 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 02:24:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 02:24:49 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 12 Oct 2021 02:24:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 02:24:57 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 02:24:57 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 02:24:57 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 02:24:57 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 02:24:57 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 02:24:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 02:24:58 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0b0a22641ad2aad782c696887c59bf05ec0b1e7aa1e07902ee51949bab802657`  
		Last Modified: Tue, 12 Oct 2021 01:52:33 GMT  
		Size: 20.4 MB (20389450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693941dd06bd7505ff4633db32f85f682bb43790f889c3700a0cc8f95a8775a`  
		Last Modified: Tue, 12 Oct 2021 02:26:22 GMT  
		Size: 6.0 MB (6047991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c80a13875d1601dda5709f1d69a00589cf3ce58b12f53fa1f724cd72014207`  
		Last Modified: Tue, 12 Oct 2021 02:26:25 GMT  
		Size: 19.0 MB (18961773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385e3003b1770a74069520dd203b4146211b03893fe9e3cb1128bbec6988f20e`  
		Last Modified: Tue, 12 Oct 2021 02:26:21 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c20fad82f79c98ea608757c45478eee61b9bd857812b095623c2765c82e5f8f`  
		Last Modified: Tue, 12 Oct 2021 02:26:21 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d145d4d4dbcb7a3f9c5ed61739d22752a3376db5bef7dd9939b863381d500426`  
		Last Modified: Tue, 12 Oct 2021 02:26:21 GMT  
		Size: 238.0 B  
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
$ docker pull chronograf@sha256:34516213b2b6065c2f99ef0ed8c1354558556c5ca4bbfdf66c9a46c3f9bd51ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7` - linux; amd64

```console
$ docker pull chronograf@sha256:2bd89c8e3321704209756d371908d7d67c8ff11a44742ebda71bbb55f59b2f0f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65386514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4cc46bc95e6eb6fff4e2ef999885e2a7877ae4c81faaccf2b55b85c643da3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:22:52 GMT
ADD file:1220579e31585dec45ca8e35874eb689018ed026a1f23b7906f791c0279671e0 in / 
# Tue, 12 Oct 2021 01:22:53 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:14:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 15:14:00 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 12 Oct 2021 15:14:11 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 15:14:11 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 15:14:12 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 15:14:12 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 15:14:12 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 15:14:12 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 15:14:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 15:14:13 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:eec53b8a5053c739b5b685cb372b38eea3286ab6626532bad963291f76357c5f`  
		Last Modified: Tue, 12 Oct 2021 01:29:50 GMT  
		Size: 22.5 MB (22527572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff71fee6d1c6f643c4ff577353f7241f074a2e1172c48bc55d6069c83fda780`  
		Last Modified: Tue, 12 Oct 2021 15:15:28 GMT  
		Size: 4.5 MB (4506496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc48f5a7983e6c90de97e53279aefdbcb8f04b16c695b8b3c0c8d11006a03c36`  
		Last Modified: Tue, 12 Oct 2021 15:15:33 GMT  
		Size: 38.3 MB (38328059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:631c77fffd0c1adcabc4c422f0b54c61947831f4a30ef756ab4cd8e1cc32e092`  
		Last Modified: Tue, 12 Oct 2021 15:15:27 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b08426d08ca99f1b410b47ea2acae8115f8f14ce88a2e0e8c944d9a45e5251a`  
		Last Modified: Tue, 12 Oct 2021 15:15:28 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad5dc2c1b79f0561fd3a3850dbedf5b3aadc0f829a1e252d3a62117c28b7958`  
		Last Modified: Tue, 12 Oct 2021 15:15:27 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:24c953f15124e44d5f380ab57393ba63f756b3ae00178b8c9a80b57e60da7d0b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59004035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0990e576b5aa23f88bb3470e9f41d66329abb0ea617ce2265caf4fe0a962b36e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:34:42 GMT
ADD file:9bfcfd0aaac802b902b0e842e040a6599c461c90b73579bcacc2fbdda7ec39cb in / 
# Tue, 12 Oct 2021 01:34:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 19:39:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 19:39:50 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 12 Oct 2021 19:40:21 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 19:40:22 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 19:40:23 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 19:40:24 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 19:40:24 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 19:40:25 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 19:40:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 19:40:26 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a1a3620b17011bd36d6f64dfcc8fd7c4cb3da78d19a59efb1b35afcadaf3f6a8`  
		Last Modified: Tue, 12 Oct 2021 01:51:59 GMT  
		Size: 19.3 MB (19316474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba93e163db4e24fdc0b61e5985bc4b17555fa24b26c0fe4f12f9128c2f84eaf0`  
		Last Modified: Tue, 12 Oct 2021 19:42:54 GMT  
		Size: 3.9 MB (3879899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5062c1f70209ac4f7642c34d34e5595e27b46dd3c3613e650f066bbfc95e12`  
		Last Modified: Tue, 12 Oct 2021 19:43:10 GMT  
		Size: 35.8 MB (35783266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26fb47a33ac1e78d667ef6f96865c0f0ff850f8ba7ff43cea2ed8402d499fdc6`  
		Last Modified: Tue, 12 Oct 2021 19:42:52 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843ef10a515dcd0452d9b9afd8d115f464770476846c5a040fe3bd2e6dd7b45e`  
		Last Modified: Tue, 12 Oct 2021 19:42:52 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cefacd9f6d476b458a8a581c78ccacd7d528d4615b8f9d031c4ab3032f416438`  
		Last Modified: Tue, 12 Oct 2021 19:42:52 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:adeac5d4387c7576c8579eaad716e24486db0062c58fb80ef7d8192615d5a944
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60483654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd33a9716e9e3159b09ae9cfc8740db8727600c4e5bff17fc22df6ec8dfd2a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:43:29 GMT
ADD file:ebfc214a3da7b706f0759fd22fa991c905976d2c970b2d59d134753f7cbd5e06 in / 
# Tue, 12 Oct 2021 01:43:29 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 02:25:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 02:25:14 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 12 Oct 2021 02:25:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 02:25:23 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 02:25:23 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 02:25:24 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 02:25:24 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 02:25:24 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 02:25:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 02:25:24 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0b0a22641ad2aad782c696887c59bf05ec0b1e7aa1e07902ee51949bab802657`  
		Last Modified: Tue, 12 Oct 2021 01:52:33 GMT  
		Size: 20.4 MB (20389450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f76b6a4b9313ee67027ac38a67f4f5f5af946bfcab3f702b4c663ccca1d7e5`  
		Last Modified: Tue, 12 Oct 2021 02:26:37 GMT  
		Size: 4.1 MB (4082592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca94d0146c32da4f5e1d8c0bbfb32fbc13d56a6bdeff65499ac569e504608c3`  
		Last Modified: Tue, 12 Oct 2021 02:26:41 GMT  
		Size: 36.0 MB (35987214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:392069b3957ad6611f447e44730a5f67aea67ebc67e2b5061e21cda77ea09de7`  
		Last Modified: Tue, 12 Oct 2021 02:26:36 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770e379656b239a44ddc6963f4d9225f45c07df1cc9e25297bb7bfddff3a2fd9`  
		Last Modified: Tue, 12 Oct 2021 02:26:36 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9246ed914e241e65ac16ea65cf8a04e0c8b15487a71ab33fe11ea72278f6ee`  
		Last Modified: Tue, 12 Oct 2021 02:26:36 GMT  
		Size: 237.0 B  
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
$ docker pull chronograf@sha256:34516213b2b6065c2f99ef0ed8c1354558556c5ca4bbfdf66c9a46c3f9bd51ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7.17` - linux; amd64

```console
$ docker pull chronograf@sha256:2bd89c8e3321704209756d371908d7d67c8ff11a44742ebda71bbb55f59b2f0f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65386514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4cc46bc95e6eb6fff4e2ef999885e2a7877ae4c81faaccf2b55b85c643da3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:22:52 GMT
ADD file:1220579e31585dec45ca8e35874eb689018ed026a1f23b7906f791c0279671e0 in / 
# Tue, 12 Oct 2021 01:22:53 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:14:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 15:14:00 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 12 Oct 2021 15:14:11 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 15:14:11 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 15:14:12 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 15:14:12 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 15:14:12 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 15:14:12 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 15:14:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 15:14:13 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:eec53b8a5053c739b5b685cb372b38eea3286ab6626532bad963291f76357c5f`  
		Last Modified: Tue, 12 Oct 2021 01:29:50 GMT  
		Size: 22.5 MB (22527572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff71fee6d1c6f643c4ff577353f7241f074a2e1172c48bc55d6069c83fda780`  
		Last Modified: Tue, 12 Oct 2021 15:15:28 GMT  
		Size: 4.5 MB (4506496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc48f5a7983e6c90de97e53279aefdbcb8f04b16c695b8b3c0c8d11006a03c36`  
		Last Modified: Tue, 12 Oct 2021 15:15:33 GMT  
		Size: 38.3 MB (38328059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:631c77fffd0c1adcabc4c422f0b54c61947831f4a30ef756ab4cd8e1cc32e092`  
		Last Modified: Tue, 12 Oct 2021 15:15:27 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b08426d08ca99f1b410b47ea2acae8115f8f14ce88a2e0e8c944d9a45e5251a`  
		Last Modified: Tue, 12 Oct 2021 15:15:28 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad5dc2c1b79f0561fd3a3850dbedf5b3aadc0f829a1e252d3a62117c28b7958`  
		Last Modified: Tue, 12 Oct 2021 15:15:27 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:24c953f15124e44d5f380ab57393ba63f756b3ae00178b8c9a80b57e60da7d0b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59004035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0990e576b5aa23f88bb3470e9f41d66329abb0ea617ce2265caf4fe0a962b36e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:34:42 GMT
ADD file:9bfcfd0aaac802b902b0e842e040a6599c461c90b73579bcacc2fbdda7ec39cb in / 
# Tue, 12 Oct 2021 01:34:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 19:39:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 19:39:50 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 12 Oct 2021 19:40:21 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 19:40:22 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 19:40:23 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 19:40:24 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 19:40:24 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 19:40:25 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 19:40:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 19:40:26 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a1a3620b17011bd36d6f64dfcc8fd7c4cb3da78d19a59efb1b35afcadaf3f6a8`  
		Last Modified: Tue, 12 Oct 2021 01:51:59 GMT  
		Size: 19.3 MB (19316474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba93e163db4e24fdc0b61e5985bc4b17555fa24b26c0fe4f12f9128c2f84eaf0`  
		Last Modified: Tue, 12 Oct 2021 19:42:54 GMT  
		Size: 3.9 MB (3879899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5062c1f70209ac4f7642c34d34e5595e27b46dd3c3613e650f066bbfc95e12`  
		Last Modified: Tue, 12 Oct 2021 19:43:10 GMT  
		Size: 35.8 MB (35783266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26fb47a33ac1e78d667ef6f96865c0f0ff850f8ba7ff43cea2ed8402d499fdc6`  
		Last Modified: Tue, 12 Oct 2021 19:42:52 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843ef10a515dcd0452d9b9afd8d115f464770476846c5a040fe3bd2e6dd7b45e`  
		Last Modified: Tue, 12 Oct 2021 19:42:52 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cefacd9f6d476b458a8a581c78ccacd7d528d4615b8f9d031c4ab3032f416438`  
		Last Modified: Tue, 12 Oct 2021 19:42:52 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:adeac5d4387c7576c8579eaad716e24486db0062c58fb80ef7d8192615d5a944
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60483654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd33a9716e9e3159b09ae9cfc8740db8727600c4e5bff17fc22df6ec8dfd2a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:43:29 GMT
ADD file:ebfc214a3da7b706f0759fd22fa991c905976d2c970b2d59d134753f7cbd5e06 in / 
# Tue, 12 Oct 2021 01:43:29 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 02:25:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 02:25:14 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 12 Oct 2021 02:25:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 02:25:23 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 02:25:23 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 02:25:24 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 02:25:24 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 02:25:24 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 02:25:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 02:25:24 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0b0a22641ad2aad782c696887c59bf05ec0b1e7aa1e07902ee51949bab802657`  
		Last Modified: Tue, 12 Oct 2021 01:52:33 GMT  
		Size: 20.4 MB (20389450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f76b6a4b9313ee67027ac38a67f4f5f5af946bfcab3f702b4c663ccca1d7e5`  
		Last Modified: Tue, 12 Oct 2021 02:26:37 GMT  
		Size: 4.1 MB (4082592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca94d0146c32da4f5e1d8c0bbfb32fbc13d56a6bdeff65499ac569e504608c3`  
		Last Modified: Tue, 12 Oct 2021 02:26:41 GMT  
		Size: 36.0 MB (35987214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:392069b3957ad6611f447e44730a5f67aea67ebc67e2b5061e21cda77ea09de7`  
		Last Modified: Tue, 12 Oct 2021 02:26:36 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770e379656b239a44ddc6963f4d9225f45c07df1cc9e25297bb7bfddff3a2fd9`  
		Last Modified: Tue, 12 Oct 2021 02:26:36 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9246ed914e241e65ac16ea65cf8a04e0c8b15487a71ab33fe11ea72278f6ee`  
		Last Modified: Tue, 12 Oct 2021 02:26:36 GMT  
		Size: 237.0 B  
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
$ docker pull chronograf@sha256:bc751a665c1d476a0c561104c5f6bd40677aa481470fb2d7dc558363bd93680d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8` - linux; amd64

```console
$ docker pull chronograf@sha256:28d78f7ebfd70cabe87f092c5711214b6430d593fa97ae0d07b4ca085eac0089
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66238089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5e668a013e2d920330790522771b175609cbad9cb9e1fd69f02238c5b84c54`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:22:52 GMT
ADD file:1220579e31585dec45ca8e35874eb689018ed026a1f23b7906f791c0279671e0 in / 
# Tue, 12 Oct 2021 01:22:53 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:13:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 15:14:21 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 12 Oct 2021 15:14:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 15:14:29 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 15:14:29 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 15:14:30 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 15:14:30 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 15:14:30 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 15:14:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 15:14:30 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:eec53b8a5053c739b5b685cb372b38eea3286ab6626532bad963291f76357c5f`  
		Last Modified: Tue, 12 Oct 2021 01:29:50 GMT  
		Size: 22.5 MB (22527572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af087790cf4907eb60360fae75759db60331cfdfb749ae8593e374a3afb328f`  
		Last Modified: Tue, 12 Oct 2021 15:15:15 GMT  
		Size: 6.8 MB (6760208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8953df3cc8defa8f66bec30576de86c6eae2d8b1adcf5d303730f4032ade0047`  
		Last Modified: Tue, 12 Oct 2021 15:15:49 GMT  
		Size: 36.9 MB (36925919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d22d923a6658e9d6073c1138d027503b4bd19690c1929beaa6edb6dbec4d32a`  
		Last Modified: Tue, 12 Oct 2021 15:15:43 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97056842c271762da86131f848a0cf5e2e501646a00a81b72d101895d6017ff2`  
		Last Modified: Tue, 12 Oct 2021 15:15:43 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79854fc9d1645faa1753c703bf21bf54fa0c6452b3e31fdf34058a37503372b3`  
		Last Modified: Tue, 12 Oct 2021 15:15:44 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:e605529e9949cebced87e772262e32d25cc7174b90fa331199d39d3e6d1bfdf1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59632513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9547985998cd5c863f3d75b3a9bf95979fd0aef9eafbe631993a0149d453825`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:34:42 GMT
ADD file:9bfcfd0aaac802b902b0e842e040a6599c461c90b73579bcacc2fbdda7ec39cb in / 
# Tue, 12 Oct 2021 01:34:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 19:38:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 19:40:42 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 12 Oct 2021 19:41:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 19:41:01 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 19:41:02 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 19:41:02 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 19:41:03 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 19:41:03 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 19:41:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 19:41:04 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a1a3620b17011bd36d6f64dfcc8fd7c4cb3da78d19a59efb1b35afcadaf3f6a8`  
		Last Modified: Tue, 12 Oct 2021 01:51:59 GMT  
		Size: 19.3 MB (19316474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bdc2f2b4d96b348e56cf5179e6a1d2f89538251124d2659dcb521c5c19e51bb`  
		Last Modified: Tue, 12 Oct 2021 19:42:36 GMT  
		Size: 5.8 MB (5780488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7abebde07ee5067581f728ce1049bfb321ae8aa8a50c6badf7c2d260eb793285`  
		Last Modified: Tue, 12 Oct 2021 19:43:40 GMT  
		Size: 34.5 MB (34511153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b85ed73208be7b2083812316441639b1345bfaf23d14c53d5f48e62d237bc6a`  
		Last Modified: Tue, 12 Oct 2021 19:43:21 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f255471ddc5f6979184f7e99a330c28cefb293a081ce7cdfeba51540dcd893e`  
		Last Modified: Tue, 12 Oct 2021 19:43:21 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf7931f243ffa449d28bb79868493276ea0e146b34e6e33d4d50bc5241da366`  
		Last Modified: Tue, 12 Oct 2021 19:43:21 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:ab6f87343df4ac8dff564bbf4561e54c41f76343461cab1af174cdb4ae9fc099
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60894104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2db46ffbab26315fb63c807d93c54ed1a66dbae430804cb81753faba4cb4c4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:43:29 GMT
ADD file:ebfc214a3da7b706f0759fd22fa991c905976d2c970b2d59d134753f7cbd5e06 in / 
# Tue, 12 Oct 2021 01:43:29 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 02:24:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 02:25:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 12 Oct 2021 02:25:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 02:25:39 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 02:25:39 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 02:25:39 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 02:25:40 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 02:25:40 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 02:25:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 02:25:40 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0b0a22641ad2aad782c696887c59bf05ec0b1e7aa1e07902ee51949bab802657`  
		Last Modified: Tue, 12 Oct 2021 01:52:33 GMT  
		Size: 20.4 MB (20389450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693941dd06bd7505ff4633db32f85f682bb43790f889c3700a0cc8f95a8775a`  
		Last Modified: Tue, 12 Oct 2021 02:26:22 GMT  
		Size: 6.0 MB (6047991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08264f151f4d30a4fba68d5fe51630efced126fd472dcfb44cb30ee0b000a1b`  
		Last Modified: Tue, 12 Oct 2021 02:26:58 GMT  
		Size: 34.4 MB (34432275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a037be6d9070a98b468bae7a099e5478093d677b9f944f2ae1c8cda8dc38098`  
		Last Modified: Tue, 12 Oct 2021 02:26:53 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e428abd6250e9e7fbbc22dd13bbed705111a055e1175e302203f4a361b6e83f5`  
		Last Modified: Tue, 12 Oct 2021 02:26:53 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb99c2fa13e01a038fbb1101249ed08a0ebd2d4e4daa5d6e325f55aa68e1b0d`  
		Last Modified: Tue, 12 Oct 2021 02:26:53 GMT  
		Size: 238.0 B  
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
$ docker pull chronograf@sha256:bc751a665c1d476a0c561104c5f6bd40677aa481470fb2d7dc558363bd93680d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8.10` - linux; amd64

```console
$ docker pull chronograf@sha256:28d78f7ebfd70cabe87f092c5711214b6430d593fa97ae0d07b4ca085eac0089
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66238089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5e668a013e2d920330790522771b175609cbad9cb9e1fd69f02238c5b84c54`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:22:52 GMT
ADD file:1220579e31585dec45ca8e35874eb689018ed026a1f23b7906f791c0279671e0 in / 
# Tue, 12 Oct 2021 01:22:53 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:13:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 15:14:21 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 12 Oct 2021 15:14:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 15:14:29 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 15:14:29 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 15:14:30 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 15:14:30 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 15:14:30 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 15:14:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 15:14:30 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:eec53b8a5053c739b5b685cb372b38eea3286ab6626532bad963291f76357c5f`  
		Last Modified: Tue, 12 Oct 2021 01:29:50 GMT  
		Size: 22.5 MB (22527572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af087790cf4907eb60360fae75759db60331cfdfb749ae8593e374a3afb328f`  
		Last Modified: Tue, 12 Oct 2021 15:15:15 GMT  
		Size: 6.8 MB (6760208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8953df3cc8defa8f66bec30576de86c6eae2d8b1adcf5d303730f4032ade0047`  
		Last Modified: Tue, 12 Oct 2021 15:15:49 GMT  
		Size: 36.9 MB (36925919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d22d923a6658e9d6073c1138d027503b4bd19690c1929beaa6edb6dbec4d32a`  
		Last Modified: Tue, 12 Oct 2021 15:15:43 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97056842c271762da86131f848a0cf5e2e501646a00a81b72d101895d6017ff2`  
		Last Modified: Tue, 12 Oct 2021 15:15:43 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79854fc9d1645faa1753c703bf21bf54fa0c6452b3e31fdf34058a37503372b3`  
		Last Modified: Tue, 12 Oct 2021 15:15:44 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:e605529e9949cebced87e772262e32d25cc7174b90fa331199d39d3e6d1bfdf1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59632513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9547985998cd5c863f3d75b3a9bf95979fd0aef9eafbe631993a0149d453825`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:34:42 GMT
ADD file:9bfcfd0aaac802b902b0e842e040a6599c461c90b73579bcacc2fbdda7ec39cb in / 
# Tue, 12 Oct 2021 01:34:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 19:38:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 19:40:42 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 12 Oct 2021 19:41:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 19:41:01 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 19:41:02 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 19:41:02 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 19:41:03 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 19:41:03 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 19:41:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 19:41:04 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a1a3620b17011bd36d6f64dfcc8fd7c4cb3da78d19a59efb1b35afcadaf3f6a8`  
		Last Modified: Tue, 12 Oct 2021 01:51:59 GMT  
		Size: 19.3 MB (19316474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bdc2f2b4d96b348e56cf5179e6a1d2f89538251124d2659dcb521c5c19e51bb`  
		Last Modified: Tue, 12 Oct 2021 19:42:36 GMT  
		Size: 5.8 MB (5780488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7abebde07ee5067581f728ce1049bfb321ae8aa8a50c6badf7c2d260eb793285`  
		Last Modified: Tue, 12 Oct 2021 19:43:40 GMT  
		Size: 34.5 MB (34511153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b85ed73208be7b2083812316441639b1345bfaf23d14c53d5f48e62d237bc6a`  
		Last Modified: Tue, 12 Oct 2021 19:43:21 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f255471ddc5f6979184f7e99a330c28cefb293a081ce7cdfeba51540dcd893e`  
		Last Modified: Tue, 12 Oct 2021 19:43:21 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf7931f243ffa449d28bb79868493276ea0e146b34e6e33d4d50bc5241da366`  
		Last Modified: Tue, 12 Oct 2021 19:43:21 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:ab6f87343df4ac8dff564bbf4561e54c41f76343461cab1af174cdb4ae9fc099
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60894104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2db46ffbab26315fb63c807d93c54ed1a66dbae430804cb81753faba4cb4c4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:43:29 GMT
ADD file:ebfc214a3da7b706f0759fd22fa991c905976d2c970b2d59d134753f7cbd5e06 in / 
# Tue, 12 Oct 2021 01:43:29 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 02:24:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 02:25:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 12 Oct 2021 02:25:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 02:25:39 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 02:25:39 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 02:25:39 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 02:25:40 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 02:25:40 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 02:25:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 02:25:40 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0b0a22641ad2aad782c696887c59bf05ec0b1e7aa1e07902ee51949bab802657`  
		Last Modified: Tue, 12 Oct 2021 01:52:33 GMT  
		Size: 20.4 MB (20389450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693941dd06bd7505ff4633db32f85f682bb43790f889c3700a0cc8f95a8775a`  
		Last Modified: Tue, 12 Oct 2021 02:26:22 GMT  
		Size: 6.0 MB (6047991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08264f151f4d30a4fba68d5fe51630efced126fd472dcfb44cb30ee0b000a1b`  
		Last Modified: Tue, 12 Oct 2021 02:26:58 GMT  
		Size: 34.4 MB (34432275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a037be6d9070a98b468bae7a099e5478093d677b9f944f2ae1c8cda8dc38098`  
		Last Modified: Tue, 12 Oct 2021 02:26:53 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e428abd6250e9e7fbbc22dd13bbed705111a055e1175e302203f4a361b6e83f5`  
		Last Modified: Tue, 12 Oct 2021 02:26:53 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb99c2fa13e01a038fbb1101249ed08a0ebd2d4e4daa5d6e325f55aa68e1b0d`  
		Last Modified: Tue, 12 Oct 2021 02:26:53 GMT  
		Size: 238.0 B  
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
$ docker pull chronograf@sha256:400f410e828123bc69c6ae1799ce7a8e70c4a6d059ff0473a983b8cda7c38f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9` - linux; amd64

```console
$ docker pull chronograf@sha256:aaea951b5f320fe4e7d041fe9ec9d49dbd521f05537caefe1cb31eab793c5ea9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66757613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05070621bd7952dad5f4565a7466f2ed27514d2fad47646e1c2bec97313ece70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:22:52 GMT
ADD file:1220579e31585dec45ca8e35874eb689018ed026a1f23b7906f791c0279671e0 in / 
# Tue, 12 Oct 2021 01:22:53 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:13:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 15:14:36 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Tue, 12 Oct 2021 15:14:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 15:14:44 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 15:14:45 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 15:14:45 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 15:14:45 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 15:14:45 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 15:14:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 15:14:46 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:eec53b8a5053c739b5b685cb372b38eea3286ab6626532bad963291f76357c5f`  
		Last Modified: Tue, 12 Oct 2021 01:29:50 GMT  
		Size: 22.5 MB (22527572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af087790cf4907eb60360fae75759db60331cfdfb749ae8593e374a3afb328f`  
		Last Modified: Tue, 12 Oct 2021 15:15:15 GMT  
		Size: 6.8 MB (6760208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428f39960a7f8d0006300a974ae86a69f8187f11e8598ab7917a8393b5498cbd`  
		Last Modified: Tue, 12 Oct 2021 15:16:05 GMT  
		Size: 37.4 MB (37445441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4725bf7e4c46d8c7e159ad0a2891e0fddfa77e31151155e909a15eef1bb8c316`  
		Last Modified: Tue, 12 Oct 2021 15:16:00 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2b58092a3477c6240ae4a362c9639d501b9e384bfa3654246d9ebcee892123`  
		Last Modified: Tue, 12 Oct 2021 15:16:00 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f71aad39dc5739f7a9e2f382448e46d433ea77813f54f08d637ccc536eeb6a5`  
		Last Modified: Tue, 12 Oct 2021 15:16:00 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:3fb18999dd46d064947de88c86f049f7ce677b11db15a4d4cf87c15b8b0d1321
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60400450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4aa55eda148d3b9748e46d3bc19063b771b86359c6f629fe806c3e5afb1bb58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:34:42 GMT
ADD file:9bfcfd0aaac802b902b0e842e040a6599c461c90b73579bcacc2fbdda7ec39cb in / 
# Tue, 12 Oct 2021 01:34:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 19:38:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 15 Oct 2021 22:58:13 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Fri, 15 Oct 2021 22:58:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 15 Oct 2021 22:58:34 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 15 Oct 2021 22:58:34 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 15 Oct 2021 22:58:35 GMT
EXPOSE 8888
# Fri, 15 Oct 2021 22:58:35 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Oct 2021 22:58:36 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 15 Oct 2021 22:58:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Oct 2021 22:58:36 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a1a3620b17011bd36d6f64dfcc8fd7c4cb3da78d19a59efb1b35afcadaf3f6a8`  
		Last Modified: Tue, 12 Oct 2021 01:51:59 GMT  
		Size: 19.3 MB (19316474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bdc2f2b4d96b348e56cf5179e6a1d2f89538251124d2659dcb521c5c19e51bb`  
		Last Modified: Tue, 12 Oct 2021 19:42:36 GMT  
		Size: 5.8 MB (5780488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb66a9a95b28e3a240c450633d5421211135b4312de046bce206afbb0f30edf9`  
		Last Modified: Fri, 15 Oct 2021 22:59:56 GMT  
		Size: 35.3 MB (35279095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec2c2711c3377ce218bad44c96856e245d745faa65f1687a85c49b1f8a56538`  
		Last Modified: Fri, 15 Oct 2021 22:59:37 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e65825543156a066468a039c1e306c2c2db19fc435de2dcd52973ad8a56f97d`  
		Last Modified: Fri, 15 Oct 2021 22:59:37 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8291978c4564a4ffcbd216ab5bc6155061ae9c2b94b78ea4b685708808d67891`  
		Last Modified: Fri, 15 Oct 2021 22:59:37 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:f8b10eabd6a93f7fcbc8d8acce2b60e412754a07bb95664a8b3caa800ca21c38
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61523317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc16a9b86e7c3cd6838f8aae38c005ab4d37fd1595c576151580683e74909a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:43:29 GMT
ADD file:ebfc214a3da7b706f0759fd22fa991c905976d2c970b2d59d134753f7cbd5e06 in / 
# Tue, 12 Oct 2021 01:43:29 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 02:24:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 02:25:45 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Tue, 12 Oct 2021 02:25:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 02:25:53 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 02:25:53 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 02:25:53 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 02:25:53 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 02:25:54 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 02:25:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 02:25:54 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0b0a22641ad2aad782c696887c59bf05ec0b1e7aa1e07902ee51949bab802657`  
		Last Modified: Tue, 12 Oct 2021 01:52:33 GMT  
		Size: 20.4 MB (20389450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693941dd06bd7505ff4633db32f85f682bb43790f889c3700a0cc8f95a8775a`  
		Last Modified: Tue, 12 Oct 2021 02:26:22 GMT  
		Size: 6.0 MB (6047991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc03711acce0b5e2f3e2ad7249ce4962fdd520835a1c778de663b9f2bec5f309`  
		Last Modified: Tue, 12 Oct 2021 02:27:14 GMT  
		Size: 35.1 MB (35061492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ac3e7452691d4edc39f45e7e6706d3dcf06f188bb81aa96749fe12906f31bc`  
		Last Modified: Tue, 12 Oct 2021 02:27:09 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef8988907a0a7be1f7d83a61d1aeaf02ef140108fff7f975c89339dd03e7848`  
		Last Modified: Tue, 12 Oct 2021 02:27:09 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb9b5f2079e26ff03ed792915e6a981d31ea534399c82cf9eee4a529a07ae60`  
		Last Modified: Tue, 12 Oct 2021 02:27:09 GMT  
		Size: 237.0 B  
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

## `chronograf:1.9.1`

```console
$ docker pull chronograf@sha256:3cac4b0cb4971d8f884dcc6d3e96010f00f21417f7e638fc883a37513665a7fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm variant v7

### `chronograf:1.9.1` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:3fb18999dd46d064947de88c86f049f7ce677b11db15a4d4cf87c15b8b0d1321
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60400450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4aa55eda148d3b9748e46d3bc19063b771b86359c6f629fe806c3e5afb1bb58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:34:42 GMT
ADD file:9bfcfd0aaac802b902b0e842e040a6599c461c90b73579bcacc2fbdda7ec39cb in / 
# Tue, 12 Oct 2021 01:34:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 19:38:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 15 Oct 2021 22:58:13 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Fri, 15 Oct 2021 22:58:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 15 Oct 2021 22:58:34 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 15 Oct 2021 22:58:34 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 15 Oct 2021 22:58:35 GMT
EXPOSE 8888
# Fri, 15 Oct 2021 22:58:35 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Oct 2021 22:58:36 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 15 Oct 2021 22:58:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Oct 2021 22:58:36 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a1a3620b17011bd36d6f64dfcc8fd7c4cb3da78d19a59efb1b35afcadaf3f6a8`  
		Last Modified: Tue, 12 Oct 2021 01:51:59 GMT  
		Size: 19.3 MB (19316474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bdc2f2b4d96b348e56cf5179e6a1d2f89538251124d2659dcb521c5c19e51bb`  
		Last Modified: Tue, 12 Oct 2021 19:42:36 GMT  
		Size: 5.8 MB (5780488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb66a9a95b28e3a240c450633d5421211135b4312de046bce206afbb0f30edf9`  
		Last Modified: Fri, 15 Oct 2021 22:59:56 GMT  
		Size: 35.3 MB (35279095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec2c2711c3377ce218bad44c96856e245d745faa65f1687a85c49b1f8a56538`  
		Last Modified: Fri, 15 Oct 2021 22:59:37 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e65825543156a066468a039c1e306c2c2db19fc435de2dcd52973ad8a56f97d`  
		Last Modified: Fri, 15 Oct 2021 22:59:37 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8291978c4564a4ffcbd216ab5bc6155061ae9c2b94b78ea4b685708808d67891`  
		Last Modified: Fri, 15 Oct 2021 22:59:37 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.1-alpine`

```console
$ docker pull chronograf@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

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
$ docker pull chronograf@sha256:400f410e828123bc69c6ae1799ce7a8e70c4a6d059ff0473a983b8cda7c38f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:aaea951b5f320fe4e7d041fe9ec9d49dbd521f05537caefe1cb31eab793c5ea9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66757613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05070621bd7952dad5f4565a7466f2ed27514d2fad47646e1c2bec97313ece70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:22:52 GMT
ADD file:1220579e31585dec45ca8e35874eb689018ed026a1f23b7906f791c0279671e0 in / 
# Tue, 12 Oct 2021 01:22:53 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:13:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 15:14:36 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Tue, 12 Oct 2021 15:14:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 15:14:44 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 15:14:45 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 15:14:45 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 15:14:45 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 15:14:45 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 15:14:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 15:14:46 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:eec53b8a5053c739b5b685cb372b38eea3286ab6626532bad963291f76357c5f`  
		Last Modified: Tue, 12 Oct 2021 01:29:50 GMT  
		Size: 22.5 MB (22527572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af087790cf4907eb60360fae75759db60331cfdfb749ae8593e374a3afb328f`  
		Last Modified: Tue, 12 Oct 2021 15:15:15 GMT  
		Size: 6.8 MB (6760208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428f39960a7f8d0006300a974ae86a69f8187f11e8598ab7917a8393b5498cbd`  
		Last Modified: Tue, 12 Oct 2021 15:16:05 GMT  
		Size: 37.4 MB (37445441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4725bf7e4c46d8c7e159ad0a2891e0fddfa77e31151155e909a15eef1bb8c316`  
		Last Modified: Tue, 12 Oct 2021 15:16:00 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2b58092a3477c6240ae4a362c9639d501b9e384bfa3654246d9ebcee892123`  
		Last Modified: Tue, 12 Oct 2021 15:16:00 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f71aad39dc5739f7a9e2f382448e46d433ea77813f54f08d637ccc536eeb6a5`  
		Last Modified: Tue, 12 Oct 2021 15:16:00 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:3fb18999dd46d064947de88c86f049f7ce677b11db15a4d4cf87c15b8b0d1321
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60400450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4aa55eda148d3b9748e46d3bc19063b771b86359c6f629fe806c3e5afb1bb58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:34:42 GMT
ADD file:9bfcfd0aaac802b902b0e842e040a6599c461c90b73579bcacc2fbdda7ec39cb in / 
# Tue, 12 Oct 2021 01:34:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 19:38:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 15 Oct 2021 22:58:13 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Fri, 15 Oct 2021 22:58:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 15 Oct 2021 22:58:34 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 15 Oct 2021 22:58:34 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 15 Oct 2021 22:58:35 GMT
EXPOSE 8888
# Fri, 15 Oct 2021 22:58:35 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Oct 2021 22:58:36 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 15 Oct 2021 22:58:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Oct 2021 22:58:36 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a1a3620b17011bd36d6f64dfcc8fd7c4cb3da78d19a59efb1b35afcadaf3f6a8`  
		Last Modified: Tue, 12 Oct 2021 01:51:59 GMT  
		Size: 19.3 MB (19316474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bdc2f2b4d96b348e56cf5179e6a1d2f89538251124d2659dcb521c5c19e51bb`  
		Last Modified: Tue, 12 Oct 2021 19:42:36 GMT  
		Size: 5.8 MB (5780488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb66a9a95b28e3a240c450633d5421211135b4312de046bce206afbb0f30edf9`  
		Last Modified: Fri, 15 Oct 2021 22:59:56 GMT  
		Size: 35.3 MB (35279095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec2c2711c3377ce218bad44c96856e245d745faa65f1687a85c49b1f8a56538`  
		Last Modified: Fri, 15 Oct 2021 22:59:37 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e65825543156a066468a039c1e306c2c2db19fc435de2dcd52973ad8a56f97d`  
		Last Modified: Fri, 15 Oct 2021 22:59:37 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8291978c4564a4ffcbd216ab5bc6155061ae9c2b94b78ea4b685708808d67891`  
		Last Modified: Fri, 15 Oct 2021 22:59:37 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:f8b10eabd6a93f7fcbc8d8acce2b60e412754a07bb95664a8b3caa800ca21c38
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61523317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc16a9b86e7c3cd6838f8aae38c005ab4d37fd1595c576151580683e74909a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:43:29 GMT
ADD file:ebfc214a3da7b706f0759fd22fa991c905976d2c970b2d59d134753f7cbd5e06 in / 
# Tue, 12 Oct 2021 01:43:29 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 02:24:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 02:25:45 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Tue, 12 Oct 2021 02:25:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 02:25:53 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 02:25:53 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 02:25:53 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 02:25:53 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 02:25:54 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 02:25:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 02:25:54 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0b0a22641ad2aad782c696887c59bf05ec0b1e7aa1e07902ee51949bab802657`  
		Last Modified: Tue, 12 Oct 2021 01:52:33 GMT  
		Size: 20.4 MB (20389450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693941dd06bd7505ff4633db32f85f682bb43790f889c3700a0cc8f95a8775a`  
		Last Modified: Tue, 12 Oct 2021 02:26:22 GMT  
		Size: 6.0 MB (6047991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc03711acce0b5e2f3e2ad7249ce4962fdd520835a1c778de663b9f2bec5f309`  
		Last Modified: Tue, 12 Oct 2021 02:27:14 GMT  
		Size: 35.1 MB (35061492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ac3e7452691d4edc39f45e7e6706d3dcf06f188bb81aa96749fe12906f31bc`  
		Last Modified: Tue, 12 Oct 2021 02:27:09 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef8988907a0a7be1f7d83a61d1aeaf02ef140108fff7f975c89339dd03e7848`  
		Last Modified: Tue, 12 Oct 2021 02:27:09 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb9b5f2079e26ff03ed792915e6a981d31ea534399c82cf9eee4a529a07ae60`  
		Last Modified: Tue, 12 Oct 2021 02:27:09 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
