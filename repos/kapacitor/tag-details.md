<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.4`](#kapacitor14)
-	[`kapacitor:1.4-alpine`](#kapacitor14-alpine)
-	[`kapacitor:1.4.1`](#kapacitor141)
-	[`kapacitor:1.4.1-alpine`](#kapacitor141-alpine)
-	[`kapacitor:1.5`](#kapacitor15)
-	[`kapacitor:1.5-alpine`](#kapacitor15-alpine)
-	[`kapacitor:1.5.9`](#kapacitor159)
-	[`kapacitor:1.5.9-alpine`](#kapacitor159-alpine)
-	[`kapacitor:alpine`](#kapacitoralpine)
-	[`kapacitor:latest`](#kapacitorlatest)

## `kapacitor:1.4`

```console
$ docker pull kapacitor@sha256:f50a0e5d79c0cc1beafcb451d2a9274abc3d822ef549dba783ff2ac1f403bf50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.4` - linux; amd64

```console
$ docker pull kapacitor@sha256:35353c62300e33437684138b9027ecaade115778b56fef95a32f9fd810371230
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (97025971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7891f774e044dfd88e38df024eff5d89cc502e8dcabc4fff7839bff66d0a6f2d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 22 Jul 2021 00:47:05 GMT
ADD file:fc9409352ad67880b83ccf1ccd1587eb2666715eae04e4dd98fca919f1bb98d7 in / 
# Thu, 22 Jul 2021 00:47:05 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:15:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:15:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 23 Jul 2021 02:16:34 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 23 Jul 2021 02:16:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 23 Jul 2021 02:16:39 GMT
ENV KAPACITOR_VERSION=1.4.1
# Fri, 23 Jul 2021 02:16:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Fri, 23 Jul 2021 02:16:43 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 23 Jul 2021 02:16:44 GMT
EXPOSE 9092
# Fri, 23 Jul 2021 02:16:44 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 23 Jul 2021 02:16:44 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 23 Jul 2021 02:16:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 23 Jul 2021 02:16:45 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:08224db8ce18b31a78a0a26d1b344d173528e50a7067797c9df4de5d8df353e2`  
		Last Modified: Thu, 22 Jul 2021 00:52:52 GMT  
		Size: 45.4 MB (45379781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd3caf86f5b9d8f8e63437571297df5fa6d454140b9c1985c47d6ad526da824`  
		Last Modified: Thu, 22 Jul 2021 01:22:23 GMT  
		Size: 11.3 MB (11294469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c316554a558d4aa95c0be17c01e4a0366d6026a98eeba53dca5baa6091e815`  
		Last Modified: Thu, 22 Jul 2021 01:22:23 GMT  
		Size: 4.3 MB (4342387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033178e431edb303118884c90bb7a40abc832073db5b2aa6a93ca11e99081292`  
		Last Modified: Fri, 23 Jul 2021 02:17:24 GMT  
		Size: 13.3 MB (13310827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8bfef56be41c9898ef2a77ed2266db25f802666e73b37ba34276bd3992ac92`  
		Last Modified: Fri, 23 Jul 2021 02:17:21 GMT  
		Size: 2.9 KB (2851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177caa5f1d9577bfc0387d08536ba81bd653e788c7a12f897e56baf92683a1a0`  
		Last Modified: Fri, 23 Jul 2021 02:17:27 GMT  
		Size: 22.7 MB (22695201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa75329d68413701f68932ab2d5b982ff64428cddb2ade6ec960f20d8a6dd07`  
		Last Modified: Fri, 23 Jul 2021 02:17:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa11a058efd9c1a383709b2e1dd86dffab5f431ba20782da5a23d7794b0d7ea`  
		Last Modified: Fri, 23 Jul 2021 02:17:21 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:e5d973d8795201994bad7a3f3103defca258ec0f1e86a2e2c4bbedb4a3cf1c22
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90787347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9cf52625aab316ebee26e82c48f4be6a8aa506939b5ae3083fd7cbb8d740359`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 23 Jun 2021 00:23:06 GMT
ADD file:8c289b4c3c40ee076e3b3563f38ccd72dee8b2ee3122170cf1bdd417ae9e03c0 in / 
# Wed, 23 Jun 2021 00:23:08 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 05:53:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 05:53:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 24 Jun 2021 18:16:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 24 Jun 2021 18:16:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 24 Jun 2021 18:16:46 GMT
ENV KAPACITOR_VERSION=1.4.1
# Thu, 24 Jun 2021 18:16:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Thu, 24 Jun 2021 18:16:54 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 24 Jun 2021 18:16:55 GMT
EXPOSE 9092
# Thu, 24 Jun 2021 18:16:55 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 24 Jun 2021 18:16:56 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 24 Jun 2021 18:16:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Jun 2021 18:16:57 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:d2f34e8839b40d84b70d62e2c8a6909422dad9688919bf387ad4a092d38ab62f`  
		Last Modified: Wed, 23 Jun 2021 00:36:08 GMT  
		Size: 42.1 MB (42119988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327954c584e8a66a22440b9a731a29ecccc047aa5f3477d6191e1c7167a37503`  
		Last Modified: Wed, 23 Jun 2021 06:24:47 GMT  
		Size: 10.0 MB (9950929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7274a619e45e9e714e599f6ae62b529f504ec947a07a58908ad99c464907420`  
		Last Modified: Wed, 23 Jun 2021 06:24:44 GMT  
		Size: 3.9 MB (3921297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9140005b461be96a490039ca3d38495bed0e1887d0cf777ccab57b720799f5`  
		Last Modified: Thu, 24 Jun 2021 18:17:59 GMT  
		Size: 13.5 MB (13482795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4878412a3a6b956dcfffe7177f563bbac67a61b883e0a440e6e556a48aa92e60`  
		Last Modified: Thu, 24 Jun 2021 18:17:55 GMT  
		Size: 2.9 KB (2853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:399e14f511ae14335be63401d810236949da4988a1660c4526387dc64cd0ae3c`  
		Last Modified: Thu, 24 Jun 2021 18:18:12 GMT  
		Size: 21.3 MB (21309027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885027938c8e2e031f33e48a2459f7b81551a217bcd21a1cbbd6f01301c24b01`  
		Last Modified: Thu, 24 Jun 2021 18:17:54 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ae6e2e57a2b61fc694d71d531a3c24bff57e6b460cbf06ef2dc7bf8cb2467a`  
		Last Modified: Thu, 24 Jun 2021 18:17:54 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:1c0c2d8390ee5b13fc927988ac21dc9444761c3a4f650ebe797ffe5eaa6b750c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91815986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b14ce8fabda31a73486dc9264725039b488d9583fd7bcffd76b8e33e9919991b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 22 Jul 2021 00:41:26 GMT
ADD file:fab290162e6d28cbe115c866c49a1e09d955450dc9e831ccbeefe40e18cfa3a7 in / 
# Thu, 22 Jul 2021 00:41:27 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:18:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:18:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 13:28:05 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 22 Jul 2021 13:28:09 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 22 Jul 2021 13:28:10 GMT
ENV KAPACITOR_VERSION=1.4.1
# Thu, 22 Jul 2021 13:28:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Thu, 22 Jul 2021 13:28:13 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 22 Jul 2021 13:28:13 GMT
EXPOSE 9092
# Thu, 22 Jul 2021 13:28:13 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 22 Jul 2021 13:28:13 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 22 Jul 2021 13:28:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Jul 2021 13:28:14 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:28ed64be8f9ee39d8ded09482441a288852dd40c2e535b64e1f9c0271c10eb44`  
		Last Modified: Thu, 22 Jul 2021 00:48:16 GMT  
		Size: 43.2 MB (43178440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6227db87dba6bebff5c1f1a2bd2d290c25c44c23f3b974a4e99fe72b48777812`  
		Last Modified: Thu, 22 Jul 2021 01:27:41 GMT  
		Size: 10.2 MB (10214761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cffb4d8549ecf5dfe60357ee2dc98dd618c73220f26c8cd505b088085229668`  
		Last Modified: Thu, 22 Jul 2021 01:27:40 GMT  
		Size: 4.1 MB (4096559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6346e9072bed6a2f6624d105c5f466f3ad8014bfb827b52970a16068730eaf53`  
		Last Modified: Thu, 22 Jul 2021 13:28:46 GMT  
		Size: 13.0 MB (13014410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5108cf0dcc3d42daee7af1dd9c991f51426fdac7db2286bb43658e80f013dd`  
		Last Modified: Thu, 22 Jul 2021 13:28:44 GMT  
		Size: 2.9 KB (2855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14223a3bf92d4e645e052a1789d4956b238cc8553806b894b9e6b76d9010dd18`  
		Last Modified: Thu, 22 Jul 2021 13:28:48 GMT  
		Size: 21.3 MB (21308507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde4fc2ba89867dd62d4be18b7948c2b4ed6012cbb9e809c72e210327796ab8d`  
		Last Modified: Thu, 22 Jul 2021 13:28:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61cb4a864bd8ad9741d714d3be4d679e61a71f5f697f0f185061fccd61973263`  
		Last Modified: Thu, 22 Jul 2021 13:28:44 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.4-alpine`

```console
$ docker pull kapacitor@sha256:4eec10a57ca53138ee13f8da786cbd1efdcb0095ec4c0403937a687f2031d692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.4-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:ba41bfd529fcc6d4a44c8c95b673955697cc0060706eb0360997d22d00adf2a5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19680593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e52482996396462c1fb07acc470d4f932ec576479e07f5b324595d9a26af4bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:12:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:12:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 14 Apr 2021 23:05:28 GMT
ENV KAPACITOR_VERSION=1.4.1
# Wed, 14 Apr 2021 23:05:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 14 Apr 2021 23:05:33 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 14 Apr 2021 23:05:33 GMT
EXPOSE 9092
# Wed, 14 Apr 2021 23:05:33 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 14 Apr 2021 23:05:33 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Wed, 14 Apr 2021 23:05:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Apr 2021 23:05:34 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4496f95da0ff203c55ba4ff45e6cc518bfd24507a21516931244d25e8db7d14`  
		Last Modified: Wed, 14 Apr 2021 20:13:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9162e7666a3906b38fdfed2592cc2e4df967e365a3fcf17c8d6320caed7fd960`  
		Last Modified: Wed, 14 Apr 2021 20:13:33 GMT  
		Size: 280.9 KB (280875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8435439cf9eca56cecd6b004cf2ca703c19915f351aa2ca841d864c05e9800`  
		Last Modified: Wed, 14 Apr 2021 23:06:07 GMT  
		Size: 16.6 MB (16598520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef7d79ef87171299b351d79f252ba6e6aea768b48aec3627cba6ff30b251422`  
		Last Modified: Wed, 14 Apr 2021 23:06:06 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a54bcdb5b237d9277650a17fb5cd3709ffb934ac98888c87cb357b9b38130d0`  
		Last Modified: Wed, 14 Apr 2021 23:06:04 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.4.1`

```console
$ docker pull kapacitor@sha256:f50a0e5d79c0cc1beafcb451d2a9274abc3d822ef549dba783ff2ac1f403bf50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.4.1` - linux; amd64

```console
$ docker pull kapacitor@sha256:35353c62300e33437684138b9027ecaade115778b56fef95a32f9fd810371230
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (97025971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7891f774e044dfd88e38df024eff5d89cc502e8dcabc4fff7839bff66d0a6f2d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 22 Jul 2021 00:47:05 GMT
ADD file:fc9409352ad67880b83ccf1ccd1587eb2666715eae04e4dd98fca919f1bb98d7 in / 
# Thu, 22 Jul 2021 00:47:05 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:15:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:15:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 23 Jul 2021 02:16:34 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 23 Jul 2021 02:16:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 23 Jul 2021 02:16:39 GMT
ENV KAPACITOR_VERSION=1.4.1
# Fri, 23 Jul 2021 02:16:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Fri, 23 Jul 2021 02:16:43 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 23 Jul 2021 02:16:44 GMT
EXPOSE 9092
# Fri, 23 Jul 2021 02:16:44 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 23 Jul 2021 02:16:44 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 23 Jul 2021 02:16:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 23 Jul 2021 02:16:45 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:08224db8ce18b31a78a0a26d1b344d173528e50a7067797c9df4de5d8df353e2`  
		Last Modified: Thu, 22 Jul 2021 00:52:52 GMT  
		Size: 45.4 MB (45379781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd3caf86f5b9d8f8e63437571297df5fa6d454140b9c1985c47d6ad526da824`  
		Last Modified: Thu, 22 Jul 2021 01:22:23 GMT  
		Size: 11.3 MB (11294469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c316554a558d4aa95c0be17c01e4a0366d6026a98eeba53dca5baa6091e815`  
		Last Modified: Thu, 22 Jul 2021 01:22:23 GMT  
		Size: 4.3 MB (4342387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033178e431edb303118884c90bb7a40abc832073db5b2aa6a93ca11e99081292`  
		Last Modified: Fri, 23 Jul 2021 02:17:24 GMT  
		Size: 13.3 MB (13310827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8bfef56be41c9898ef2a77ed2266db25f802666e73b37ba34276bd3992ac92`  
		Last Modified: Fri, 23 Jul 2021 02:17:21 GMT  
		Size: 2.9 KB (2851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177caa5f1d9577bfc0387d08536ba81bd653e788c7a12f897e56baf92683a1a0`  
		Last Modified: Fri, 23 Jul 2021 02:17:27 GMT  
		Size: 22.7 MB (22695201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa75329d68413701f68932ab2d5b982ff64428cddb2ade6ec960f20d8a6dd07`  
		Last Modified: Fri, 23 Jul 2021 02:17:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa11a058efd9c1a383709b2e1dd86dffab5f431ba20782da5a23d7794b0d7ea`  
		Last Modified: Fri, 23 Jul 2021 02:17:21 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4.1` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:e5d973d8795201994bad7a3f3103defca258ec0f1e86a2e2c4bbedb4a3cf1c22
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90787347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9cf52625aab316ebee26e82c48f4be6a8aa506939b5ae3083fd7cbb8d740359`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 23 Jun 2021 00:23:06 GMT
ADD file:8c289b4c3c40ee076e3b3563f38ccd72dee8b2ee3122170cf1bdd417ae9e03c0 in / 
# Wed, 23 Jun 2021 00:23:08 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 05:53:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 05:53:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 24 Jun 2021 18:16:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 24 Jun 2021 18:16:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 24 Jun 2021 18:16:46 GMT
ENV KAPACITOR_VERSION=1.4.1
# Thu, 24 Jun 2021 18:16:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Thu, 24 Jun 2021 18:16:54 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 24 Jun 2021 18:16:55 GMT
EXPOSE 9092
# Thu, 24 Jun 2021 18:16:55 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 24 Jun 2021 18:16:56 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 24 Jun 2021 18:16:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Jun 2021 18:16:57 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:d2f34e8839b40d84b70d62e2c8a6909422dad9688919bf387ad4a092d38ab62f`  
		Last Modified: Wed, 23 Jun 2021 00:36:08 GMT  
		Size: 42.1 MB (42119988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327954c584e8a66a22440b9a731a29ecccc047aa5f3477d6191e1c7167a37503`  
		Last Modified: Wed, 23 Jun 2021 06:24:47 GMT  
		Size: 10.0 MB (9950929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7274a619e45e9e714e599f6ae62b529f504ec947a07a58908ad99c464907420`  
		Last Modified: Wed, 23 Jun 2021 06:24:44 GMT  
		Size: 3.9 MB (3921297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9140005b461be96a490039ca3d38495bed0e1887d0cf777ccab57b720799f5`  
		Last Modified: Thu, 24 Jun 2021 18:17:59 GMT  
		Size: 13.5 MB (13482795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4878412a3a6b956dcfffe7177f563bbac67a61b883e0a440e6e556a48aa92e60`  
		Last Modified: Thu, 24 Jun 2021 18:17:55 GMT  
		Size: 2.9 KB (2853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:399e14f511ae14335be63401d810236949da4988a1660c4526387dc64cd0ae3c`  
		Last Modified: Thu, 24 Jun 2021 18:18:12 GMT  
		Size: 21.3 MB (21309027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885027938c8e2e031f33e48a2459f7b81551a217bcd21a1cbbd6f01301c24b01`  
		Last Modified: Thu, 24 Jun 2021 18:17:54 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ae6e2e57a2b61fc694d71d531a3c24bff57e6b460cbf06ef2dc7bf8cb2467a`  
		Last Modified: Thu, 24 Jun 2021 18:17:54 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4.1` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:1c0c2d8390ee5b13fc927988ac21dc9444761c3a4f650ebe797ffe5eaa6b750c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91815986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b14ce8fabda31a73486dc9264725039b488d9583fd7bcffd76b8e33e9919991b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 22 Jul 2021 00:41:26 GMT
ADD file:fab290162e6d28cbe115c866c49a1e09d955450dc9e831ccbeefe40e18cfa3a7 in / 
# Thu, 22 Jul 2021 00:41:27 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:18:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:18:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 13:28:05 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 22 Jul 2021 13:28:09 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 22 Jul 2021 13:28:10 GMT
ENV KAPACITOR_VERSION=1.4.1
# Thu, 22 Jul 2021 13:28:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Thu, 22 Jul 2021 13:28:13 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 22 Jul 2021 13:28:13 GMT
EXPOSE 9092
# Thu, 22 Jul 2021 13:28:13 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 22 Jul 2021 13:28:13 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 22 Jul 2021 13:28:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Jul 2021 13:28:14 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:28ed64be8f9ee39d8ded09482441a288852dd40c2e535b64e1f9c0271c10eb44`  
		Last Modified: Thu, 22 Jul 2021 00:48:16 GMT  
		Size: 43.2 MB (43178440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6227db87dba6bebff5c1f1a2bd2d290c25c44c23f3b974a4e99fe72b48777812`  
		Last Modified: Thu, 22 Jul 2021 01:27:41 GMT  
		Size: 10.2 MB (10214761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cffb4d8549ecf5dfe60357ee2dc98dd618c73220f26c8cd505b088085229668`  
		Last Modified: Thu, 22 Jul 2021 01:27:40 GMT  
		Size: 4.1 MB (4096559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6346e9072bed6a2f6624d105c5f466f3ad8014bfb827b52970a16068730eaf53`  
		Last Modified: Thu, 22 Jul 2021 13:28:46 GMT  
		Size: 13.0 MB (13014410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5108cf0dcc3d42daee7af1dd9c991f51426fdac7db2286bb43658e80f013dd`  
		Last Modified: Thu, 22 Jul 2021 13:28:44 GMT  
		Size: 2.9 KB (2855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14223a3bf92d4e645e052a1789d4956b238cc8553806b894b9e6b76d9010dd18`  
		Last Modified: Thu, 22 Jul 2021 13:28:48 GMT  
		Size: 21.3 MB (21308507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde4fc2ba89867dd62d4be18b7948c2b4ed6012cbb9e809c72e210327796ab8d`  
		Last Modified: Thu, 22 Jul 2021 13:28:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61cb4a864bd8ad9741d714d3be4d679e61a71f5f697f0f185061fccd61973263`  
		Last Modified: Thu, 22 Jul 2021 13:28:44 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.4.1-alpine`

```console
$ docker pull kapacitor@sha256:4eec10a57ca53138ee13f8da786cbd1efdcb0095ec4c0403937a687f2031d692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.4.1-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:ba41bfd529fcc6d4a44c8c95b673955697cc0060706eb0360997d22d00adf2a5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19680593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e52482996396462c1fb07acc470d4f932ec576479e07f5b324595d9a26af4bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:12:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:12:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 14 Apr 2021 23:05:28 GMT
ENV KAPACITOR_VERSION=1.4.1
# Wed, 14 Apr 2021 23:05:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 14 Apr 2021 23:05:33 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 14 Apr 2021 23:05:33 GMT
EXPOSE 9092
# Wed, 14 Apr 2021 23:05:33 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 14 Apr 2021 23:05:33 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Wed, 14 Apr 2021 23:05:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Apr 2021 23:05:34 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4496f95da0ff203c55ba4ff45e6cc518bfd24507a21516931244d25e8db7d14`  
		Last Modified: Wed, 14 Apr 2021 20:13:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9162e7666a3906b38fdfed2592cc2e4df967e365a3fcf17c8d6320caed7fd960`  
		Last Modified: Wed, 14 Apr 2021 20:13:33 GMT  
		Size: 280.9 KB (280875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8435439cf9eca56cecd6b004cf2ca703c19915f351aa2ca841d864c05e9800`  
		Last Modified: Wed, 14 Apr 2021 23:06:07 GMT  
		Size: 16.6 MB (16598520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef7d79ef87171299b351d79f252ba6e6aea768b48aec3627cba6ff30b251422`  
		Last Modified: Wed, 14 Apr 2021 23:06:06 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a54bcdb5b237d9277650a17fb5cd3709ffb934ac98888c87cb357b9b38130d0`  
		Last Modified: Wed, 14 Apr 2021 23:06:04 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5`

```console
$ docker pull kapacitor@sha256:5b3c3a67676332584ddfe0c49d4f287364386061788d2ce2d86f18e6d65bec17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.5` - linux; amd64

```console
$ docker pull kapacitor@sha256:61081b5f8a050ba9fdd01305f97cb0e881f69d51a3188ef1890a9aeb4b50d8e7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111550048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26fe97eea26074deb8eea6b054e942959450074a078edd7506734b3acd1423f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 22 Jul 2021 00:47:05 GMT
ADD file:fc9409352ad67880b83ccf1ccd1587eb2666715eae04e4dd98fca919f1bb98d7 in / 
# Thu, 22 Jul 2021 00:47:05 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:15:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:15:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 23 Jul 2021 02:16:34 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 23 Jul 2021 02:16:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 23 Jul 2021 02:16:51 GMT
ENV KAPACITOR_VERSION=1.5.9
# Fri, 23 Jul 2021 02:16:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 23 Jul 2021 02:16:57 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 23 Jul 2021 02:16:57 GMT
EXPOSE 9092
# Fri, 23 Jul 2021 02:16:57 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 23 Jul 2021 02:16:58 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 23 Jul 2021 02:16:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 23 Jul 2021 02:16:58 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:08224db8ce18b31a78a0a26d1b344d173528e50a7067797c9df4de5d8df353e2`  
		Last Modified: Thu, 22 Jul 2021 00:52:52 GMT  
		Size: 45.4 MB (45379781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd3caf86f5b9d8f8e63437571297df5fa6d454140b9c1985c47d6ad526da824`  
		Last Modified: Thu, 22 Jul 2021 01:22:23 GMT  
		Size: 11.3 MB (11294469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c316554a558d4aa95c0be17c01e4a0366d6026a98eeba53dca5baa6091e815`  
		Last Modified: Thu, 22 Jul 2021 01:22:23 GMT  
		Size: 4.3 MB (4342387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033178e431edb303118884c90bb7a40abc832073db5b2aa6a93ca11e99081292`  
		Last Modified: Fri, 23 Jul 2021 02:17:24 GMT  
		Size: 13.3 MB (13310827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8bfef56be41c9898ef2a77ed2266db25f802666e73b37ba34276bd3992ac92`  
		Last Modified: Fri, 23 Jul 2021 02:17:21 GMT  
		Size: 2.9 KB (2851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f46388a9187d538c0ca826f17bec8e18a9e1bf21f9aae2232a92875b09ad3f9`  
		Last Modified: Fri, 23 Jul 2021 02:17:44 GMT  
		Size: 37.2 MB (37219277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7e1d1c86bc719fb6fb4686ed04c42a776a20746072aca32695e51041b387cd`  
		Last Modified: Fri, 23 Jul 2021 02:17:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cedd255af55ae1a9287923f014141aca6cae9f50b229201d0a8134fdb3354c`  
		Last Modified: Fri, 23 Jul 2021 02:17:38 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:d82e9b9f4d1cb9fe22767bf9d755a116663751ca013ce4683a54b2f66b773c29
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104265049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf9a3ad8d8158a85b0cde73062302984bc3099544685b3489c14e2252e6ef19`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 23 Jun 2021 00:23:06 GMT
ADD file:8c289b4c3c40ee076e3b3563f38ccd72dee8b2ee3122170cf1bdd417ae9e03c0 in / 
# Wed, 23 Jun 2021 00:23:08 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 05:53:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 05:53:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 24 Jun 2021 18:16:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 24 Jun 2021 18:16:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 24 Jun 2021 18:17:07 GMT
ENV KAPACITOR_VERSION=1.5.9
# Thu, 24 Jun 2021 18:17:16 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 24 Jun 2021 18:17:17 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 24 Jun 2021 18:17:17 GMT
EXPOSE 9092
# Thu, 24 Jun 2021 18:17:17 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 24 Jun 2021 18:17:18 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 24 Jun 2021 18:17:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Jun 2021 18:17:19 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:d2f34e8839b40d84b70d62e2c8a6909422dad9688919bf387ad4a092d38ab62f`  
		Last Modified: Wed, 23 Jun 2021 00:36:08 GMT  
		Size: 42.1 MB (42119988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327954c584e8a66a22440b9a731a29ecccc047aa5f3477d6191e1c7167a37503`  
		Last Modified: Wed, 23 Jun 2021 06:24:47 GMT  
		Size: 10.0 MB (9950929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7274a619e45e9e714e599f6ae62b529f504ec947a07a58908ad99c464907420`  
		Last Modified: Wed, 23 Jun 2021 06:24:44 GMT  
		Size: 3.9 MB (3921297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9140005b461be96a490039ca3d38495bed0e1887d0cf777ccab57b720799f5`  
		Last Modified: Thu, 24 Jun 2021 18:17:59 GMT  
		Size: 13.5 MB (13482795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4878412a3a6b956dcfffe7177f563bbac67a61b883e0a440e6e556a48aa92e60`  
		Last Modified: Thu, 24 Jun 2021 18:17:55 GMT  
		Size: 2.9 KB (2853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5a24017a148bb8b6f51369237e7cfce5ac631fa3a2bb712859724f3c8aee97`  
		Last Modified: Thu, 24 Jun 2021 18:18:43 GMT  
		Size: 34.8 MB (34786731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d56f0608a441145c647ac0115cd9869faee9c5eb75e38236eb8277ff6804f9eb`  
		Last Modified: Thu, 24 Jun 2021 18:18:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d81956a32379023eeccc1de837b9d9e6850bebb5d587c4933e1552e08d62761`  
		Last Modified: Thu, 24 Jun 2021 18:18:25 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:72c4109486cbe275b9ca2ef8e50d2e211e38fe1ce70f73e527c5839fac8419de
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105068396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad801b11ae96591268aac7953811a632a6615ffc7c92077fd3d80ddb60901ad4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 22 Jul 2021 00:41:26 GMT
ADD file:fab290162e6d28cbe115c866c49a1e09d955450dc9e831ccbeefe40e18cfa3a7 in / 
# Thu, 22 Jul 2021 00:41:27 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:18:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:18:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 13:28:05 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 22 Jul 2021 13:28:09 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 22 Jul 2021 13:28:20 GMT
ENV KAPACITOR_VERSION=1.5.9
# Thu, 22 Jul 2021 13:28:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 22 Jul 2021 13:28:23 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 22 Jul 2021 13:28:23 GMT
EXPOSE 9092
# Thu, 22 Jul 2021 13:28:24 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 22 Jul 2021 13:28:24 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 22 Jul 2021 13:28:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Jul 2021 13:28:24 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:28ed64be8f9ee39d8ded09482441a288852dd40c2e535b64e1f9c0271c10eb44`  
		Last Modified: Thu, 22 Jul 2021 00:48:16 GMT  
		Size: 43.2 MB (43178440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6227db87dba6bebff5c1f1a2bd2d290c25c44c23f3b974a4e99fe72b48777812`  
		Last Modified: Thu, 22 Jul 2021 01:27:41 GMT  
		Size: 10.2 MB (10214761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cffb4d8549ecf5dfe60357ee2dc98dd618c73220f26c8cd505b088085229668`  
		Last Modified: Thu, 22 Jul 2021 01:27:40 GMT  
		Size: 4.1 MB (4096559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6346e9072bed6a2f6624d105c5f466f3ad8014bfb827b52970a16068730eaf53`  
		Last Modified: Thu, 22 Jul 2021 13:28:46 GMT  
		Size: 13.0 MB (13014410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5108cf0dcc3d42daee7af1dd9c991f51426fdac7db2286bb43658e80f013dd`  
		Last Modified: Thu, 22 Jul 2021 13:28:44 GMT  
		Size: 2.9 KB (2855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2ac8cb046154d41e652250ff93604f8bc0717f2aa926e511591699a7e5de3b`  
		Last Modified: Thu, 22 Jul 2021 13:29:05 GMT  
		Size: 34.6 MB (34560917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcdecb78aba02fe8abaac90910701564b6f81f4c66c70964eaa3ef4297fae5e`  
		Last Modified: Thu, 22 Jul 2021 13:29:00 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59cfdcd7be9512de52c98344ab0fbf114ebc91575377be2b40222c9967351fd`  
		Last Modified: Thu, 22 Jul 2021 13:29:00 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5-alpine`

```console
$ docker pull kapacitor@sha256:6af30b7c71b361325dd37e32405ffe260a7622e252ff781cf8750274fd7cafc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.5-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:c0ce756dce7e277da60e4820cf9202224333a458faef03a5244417b437597b3f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22624130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2299dfad2371a47bc586d62a1a0e658fb221bd1e503455e166c2a3420004c432`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:12:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:12:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 14 Apr 2021 23:05:40 GMT
ENV KAPACITOR_VERSION=1.5.9
# Wed, 14 Apr 2021 23:05:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 14 Apr 2021 23:05:45 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 14 Apr 2021 23:05:45 GMT
EXPOSE 9092
# Wed, 14 Apr 2021 23:05:45 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 14 Apr 2021 23:05:45 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Wed, 14 Apr 2021 23:05:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Apr 2021 23:05:45 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4496f95da0ff203c55ba4ff45e6cc518bfd24507a21516931244d25e8db7d14`  
		Last Modified: Wed, 14 Apr 2021 20:13:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9162e7666a3906b38fdfed2592cc2e4df967e365a3fcf17c8d6320caed7fd960`  
		Last Modified: Wed, 14 Apr 2021 20:13:33 GMT  
		Size: 280.9 KB (280875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a1f5be947bda46483241414ba5ca37c67b9d35756739e5d95a3691b0dc19b8`  
		Last Modified: Wed, 14 Apr 2021 23:06:23 GMT  
		Size: 19.5 MB (19542054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8641ef767335ca62f3d100628e194d12b66b4ce8eb4c47f14990bc30097a2ac0`  
		Last Modified: Wed, 14 Apr 2021 23:06:20 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa60130307537cadab811f1a558e43af4c684353ca1acdc997f2705491d950a`  
		Last Modified: Wed, 14 Apr 2021 23:06:20 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5.9`

```console
$ docker pull kapacitor@sha256:3ebef0517a6804b74b0d83fdb27a3e0b4c7da9360fb00d16cd6183e3705c5984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.5.9` - linux; amd64

```console
$ docker pull kapacitor@sha256:61081b5f8a050ba9fdd01305f97cb0e881f69d51a3188ef1890a9aeb4b50d8e7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111550048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26fe97eea26074deb8eea6b054e942959450074a078edd7506734b3acd1423f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 22 Jul 2021 00:47:05 GMT
ADD file:fc9409352ad67880b83ccf1ccd1587eb2666715eae04e4dd98fca919f1bb98d7 in / 
# Thu, 22 Jul 2021 00:47:05 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:15:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:15:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 23 Jul 2021 02:16:34 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 23 Jul 2021 02:16:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 23 Jul 2021 02:16:51 GMT
ENV KAPACITOR_VERSION=1.5.9
# Fri, 23 Jul 2021 02:16:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 23 Jul 2021 02:16:57 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 23 Jul 2021 02:16:57 GMT
EXPOSE 9092
# Fri, 23 Jul 2021 02:16:57 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 23 Jul 2021 02:16:58 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 23 Jul 2021 02:16:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 23 Jul 2021 02:16:58 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:08224db8ce18b31a78a0a26d1b344d173528e50a7067797c9df4de5d8df353e2`  
		Last Modified: Thu, 22 Jul 2021 00:52:52 GMT  
		Size: 45.4 MB (45379781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd3caf86f5b9d8f8e63437571297df5fa6d454140b9c1985c47d6ad526da824`  
		Last Modified: Thu, 22 Jul 2021 01:22:23 GMT  
		Size: 11.3 MB (11294469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c316554a558d4aa95c0be17c01e4a0366d6026a98eeba53dca5baa6091e815`  
		Last Modified: Thu, 22 Jul 2021 01:22:23 GMT  
		Size: 4.3 MB (4342387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033178e431edb303118884c90bb7a40abc832073db5b2aa6a93ca11e99081292`  
		Last Modified: Fri, 23 Jul 2021 02:17:24 GMT  
		Size: 13.3 MB (13310827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8bfef56be41c9898ef2a77ed2266db25f802666e73b37ba34276bd3992ac92`  
		Last Modified: Fri, 23 Jul 2021 02:17:21 GMT  
		Size: 2.9 KB (2851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f46388a9187d538c0ca826f17bec8e18a9e1bf21f9aae2232a92875b09ad3f9`  
		Last Modified: Fri, 23 Jul 2021 02:17:44 GMT  
		Size: 37.2 MB (37219277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7e1d1c86bc719fb6fb4686ed04c42a776a20746072aca32695e51041b387cd`  
		Last Modified: Fri, 23 Jul 2021 02:17:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cedd255af55ae1a9287923f014141aca6cae9f50b229201d0a8134fdb3354c`  
		Last Modified: Fri, 23 Jul 2021 02:17:38 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5.9` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:0d2023b217f21f77f223ff7b748caba6b0611e8e989a4b659faee414563555cd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104271827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:874056135561911f0d9b37277d4d62d1f33a320a29a80c304e23026f92b2b83d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 22 Jul 2021 02:06:56 GMT
ADD file:544c40297b94c3ecc6561cf7bfef1cdf9763a18ce5e24b6841a1b70d0516d41d in / 
# Thu, 22 Jul 2021 02:06:57 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 04:21:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 04:22:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 23 Jul 2021 11:00:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 23 Jul 2021 11:00:34 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 23 Jul 2021 11:01:01 GMT
ENV KAPACITOR_VERSION=1.5.9
# Fri, 23 Jul 2021 11:01:09 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 23 Jul 2021 11:01:10 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 23 Jul 2021 11:01:10 GMT
EXPOSE 9092
# Fri, 23 Jul 2021 11:01:11 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 23 Jul 2021 11:01:11 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 23 Jul 2021 11:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 23 Jul 2021 11:01:12 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:b3cc5e47308fe8ded537d7ffdcaba46fcdf803cfe9878bd9264754a50eaa128b`  
		Last Modified: Thu, 22 Jul 2021 02:20:37 GMT  
		Size: 42.1 MB (42120108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf69efd3b547fe4dc472fd34a54c466b82ce51b7f04957779206b5ea0ef9160`  
		Last Modified: Thu, 22 Jul 2021 04:41:23 GMT  
		Size: 10.0 MB (9950872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7430ae4c6b93ca669cc72566a38f952b74dece32c5897c46e51a5907bd5a0c`  
		Last Modified: Thu, 22 Jul 2021 04:41:20 GMT  
		Size: 3.9 MB (3921255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d288a7a9052de99ec8f43901d57a79d2ed295f5365af74abc65676e9d1a597`  
		Last Modified: Fri, 23 Jul 2021 11:01:53 GMT  
		Size: 13.5 MB (13489598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df3480c3f7f784068324a7a0264eefbde158fee4a796d2b818ac07b85051cec`  
		Last Modified: Fri, 23 Jul 2021 11:01:49 GMT  
		Size: 2.9 KB (2853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad786f7a776faed48a2f5fe6cc4ed989f002a067a1419b112731a2a2c379c549`  
		Last Modified: Fri, 23 Jul 2021 11:02:33 GMT  
		Size: 34.8 MB (34786687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f19d7d688b3f16eee058bcfd3c28142e19f2944d9720a1fcc9aeb7de1a37fb`  
		Last Modified: Fri, 23 Jul 2021 11:02:15 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f624dcbf4cdec850d810382c22a2b3cfb9b478b42f3a632a76319d1a142be8a5`  
		Last Modified: Fri, 23 Jul 2021 11:02:15 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5.9` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:72c4109486cbe275b9ca2ef8e50d2e211e38fe1ce70f73e527c5839fac8419de
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105068396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad801b11ae96591268aac7953811a632a6615ffc7c92077fd3d80ddb60901ad4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 22 Jul 2021 00:41:26 GMT
ADD file:fab290162e6d28cbe115c866c49a1e09d955450dc9e831ccbeefe40e18cfa3a7 in / 
# Thu, 22 Jul 2021 00:41:27 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:18:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:18:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 13:28:05 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 22 Jul 2021 13:28:09 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 22 Jul 2021 13:28:20 GMT
ENV KAPACITOR_VERSION=1.5.9
# Thu, 22 Jul 2021 13:28:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 22 Jul 2021 13:28:23 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 22 Jul 2021 13:28:23 GMT
EXPOSE 9092
# Thu, 22 Jul 2021 13:28:24 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 22 Jul 2021 13:28:24 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 22 Jul 2021 13:28:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Jul 2021 13:28:24 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:28ed64be8f9ee39d8ded09482441a288852dd40c2e535b64e1f9c0271c10eb44`  
		Last Modified: Thu, 22 Jul 2021 00:48:16 GMT  
		Size: 43.2 MB (43178440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6227db87dba6bebff5c1f1a2bd2d290c25c44c23f3b974a4e99fe72b48777812`  
		Last Modified: Thu, 22 Jul 2021 01:27:41 GMT  
		Size: 10.2 MB (10214761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cffb4d8549ecf5dfe60357ee2dc98dd618c73220f26c8cd505b088085229668`  
		Last Modified: Thu, 22 Jul 2021 01:27:40 GMT  
		Size: 4.1 MB (4096559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6346e9072bed6a2f6624d105c5f466f3ad8014bfb827b52970a16068730eaf53`  
		Last Modified: Thu, 22 Jul 2021 13:28:46 GMT  
		Size: 13.0 MB (13014410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5108cf0dcc3d42daee7af1dd9c991f51426fdac7db2286bb43658e80f013dd`  
		Last Modified: Thu, 22 Jul 2021 13:28:44 GMT  
		Size: 2.9 KB (2855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2ac8cb046154d41e652250ff93604f8bc0717f2aa926e511591699a7e5de3b`  
		Last Modified: Thu, 22 Jul 2021 13:29:05 GMT  
		Size: 34.6 MB (34560917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcdecb78aba02fe8abaac90910701564b6f81f4c66c70964eaa3ef4297fae5e`  
		Last Modified: Thu, 22 Jul 2021 13:29:00 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59cfdcd7be9512de52c98344ab0fbf114ebc91575377be2b40222c9967351fd`  
		Last Modified: Thu, 22 Jul 2021 13:29:00 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5.9-alpine`

```console
$ docker pull kapacitor@sha256:6af30b7c71b361325dd37e32405ffe260a7622e252ff781cf8750274fd7cafc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.5.9-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:c0ce756dce7e277da60e4820cf9202224333a458faef03a5244417b437597b3f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22624130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2299dfad2371a47bc586d62a1a0e658fb221bd1e503455e166c2a3420004c432`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:12:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:12:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 14 Apr 2021 23:05:40 GMT
ENV KAPACITOR_VERSION=1.5.9
# Wed, 14 Apr 2021 23:05:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 14 Apr 2021 23:05:45 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 14 Apr 2021 23:05:45 GMT
EXPOSE 9092
# Wed, 14 Apr 2021 23:05:45 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 14 Apr 2021 23:05:45 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Wed, 14 Apr 2021 23:05:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Apr 2021 23:05:45 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4496f95da0ff203c55ba4ff45e6cc518bfd24507a21516931244d25e8db7d14`  
		Last Modified: Wed, 14 Apr 2021 20:13:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9162e7666a3906b38fdfed2592cc2e4df967e365a3fcf17c8d6320caed7fd960`  
		Last Modified: Wed, 14 Apr 2021 20:13:33 GMT  
		Size: 280.9 KB (280875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a1f5be947bda46483241414ba5ca37c67b9d35756739e5d95a3691b0dc19b8`  
		Last Modified: Wed, 14 Apr 2021 23:06:23 GMT  
		Size: 19.5 MB (19542054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8641ef767335ca62f3d100628e194d12b66b4ce8eb4c47f14990bc30097a2ac0`  
		Last Modified: Wed, 14 Apr 2021 23:06:20 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa60130307537cadab811f1a558e43af4c684353ca1acdc997f2705491d950a`  
		Last Modified: Wed, 14 Apr 2021 23:06:20 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:6af30b7c71b361325dd37e32405ffe260a7622e252ff781cf8750274fd7cafc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:c0ce756dce7e277da60e4820cf9202224333a458faef03a5244417b437597b3f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22624130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2299dfad2371a47bc586d62a1a0e658fb221bd1e503455e166c2a3420004c432`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:12:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:12:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 14 Apr 2021 23:05:40 GMT
ENV KAPACITOR_VERSION=1.5.9
# Wed, 14 Apr 2021 23:05:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 14 Apr 2021 23:05:45 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 14 Apr 2021 23:05:45 GMT
EXPOSE 9092
# Wed, 14 Apr 2021 23:05:45 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 14 Apr 2021 23:05:45 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Wed, 14 Apr 2021 23:05:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Apr 2021 23:05:45 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4496f95da0ff203c55ba4ff45e6cc518bfd24507a21516931244d25e8db7d14`  
		Last Modified: Wed, 14 Apr 2021 20:13:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9162e7666a3906b38fdfed2592cc2e4df967e365a3fcf17c8d6320caed7fd960`  
		Last Modified: Wed, 14 Apr 2021 20:13:33 GMT  
		Size: 280.9 KB (280875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a1f5be947bda46483241414ba5ca37c67b9d35756739e5d95a3691b0dc19b8`  
		Last Modified: Wed, 14 Apr 2021 23:06:23 GMT  
		Size: 19.5 MB (19542054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8641ef767335ca62f3d100628e194d12b66b4ce8eb4c47f14990bc30097a2ac0`  
		Last Modified: Wed, 14 Apr 2021 23:06:20 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa60130307537cadab811f1a558e43af4c684353ca1acdc997f2705491d950a`  
		Last Modified: Wed, 14 Apr 2021 23:06:20 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:3ebef0517a6804b74b0d83fdb27a3e0b4c7da9360fb00d16cd6183e3705c5984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:61081b5f8a050ba9fdd01305f97cb0e881f69d51a3188ef1890a9aeb4b50d8e7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111550048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26fe97eea26074deb8eea6b054e942959450074a078edd7506734b3acd1423f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 22 Jul 2021 00:47:05 GMT
ADD file:fc9409352ad67880b83ccf1ccd1587eb2666715eae04e4dd98fca919f1bb98d7 in / 
# Thu, 22 Jul 2021 00:47:05 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:15:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:15:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 23 Jul 2021 02:16:34 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 23 Jul 2021 02:16:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 23 Jul 2021 02:16:51 GMT
ENV KAPACITOR_VERSION=1.5.9
# Fri, 23 Jul 2021 02:16:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 23 Jul 2021 02:16:57 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 23 Jul 2021 02:16:57 GMT
EXPOSE 9092
# Fri, 23 Jul 2021 02:16:57 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 23 Jul 2021 02:16:58 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 23 Jul 2021 02:16:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 23 Jul 2021 02:16:58 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:08224db8ce18b31a78a0a26d1b344d173528e50a7067797c9df4de5d8df353e2`  
		Last Modified: Thu, 22 Jul 2021 00:52:52 GMT  
		Size: 45.4 MB (45379781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd3caf86f5b9d8f8e63437571297df5fa6d454140b9c1985c47d6ad526da824`  
		Last Modified: Thu, 22 Jul 2021 01:22:23 GMT  
		Size: 11.3 MB (11294469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c316554a558d4aa95c0be17c01e4a0366d6026a98eeba53dca5baa6091e815`  
		Last Modified: Thu, 22 Jul 2021 01:22:23 GMT  
		Size: 4.3 MB (4342387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033178e431edb303118884c90bb7a40abc832073db5b2aa6a93ca11e99081292`  
		Last Modified: Fri, 23 Jul 2021 02:17:24 GMT  
		Size: 13.3 MB (13310827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8bfef56be41c9898ef2a77ed2266db25f802666e73b37ba34276bd3992ac92`  
		Last Modified: Fri, 23 Jul 2021 02:17:21 GMT  
		Size: 2.9 KB (2851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f46388a9187d538c0ca826f17bec8e18a9e1bf21f9aae2232a92875b09ad3f9`  
		Last Modified: Fri, 23 Jul 2021 02:17:44 GMT  
		Size: 37.2 MB (37219277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7e1d1c86bc719fb6fb4686ed04c42a776a20746072aca32695e51041b387cd`  
		Last Modified: Fri, 23 Jul 2021 02:17:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cedd255af55ae1a9287923f014141aca6cae9f50b229201d0a8134fdb3354c`  
		Last Modified: Fri, 23 Jul 2021 02:17:38 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:0d2023b217f21f77f223ff7b748caba6b0611e8e989a4b659faee414563555cd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104271827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:874056135561911f0d9b37277d4d62d1f33a320a29a80c304e23026f92b2b83d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 22 Jul 2021 02:06:56 GMT
ADD file:544c40297b94c3ecc6561cf7bfef1cdf9763a18ce5e24b6841a1b70d0516d41d in / 
# Thu, 22 Jul 2021 02:06:57 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 04:21:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 04:22:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 23 Jul 2021 11:00:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 23 Jul 2021 11:00:34 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 23 Jul 2021 11:01:01 GMT
ENV KAPACITOR_VERSION=1.5.9
# Fri, 23 Jul 2021 11:01:09 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 23 Jul 2021 11:01:10 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 23 Jul 2021 11:01:10 GMT
EXPOSE 9092
# Fri, 23 Jul 2021 11:01:11 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 23 Jul 2021 11:01:11 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 23 Jul 2021 11:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 23 Jul 2021 11:01:12 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:b3cc5e47308fe8ded537d7ffdcaba46fcdf803cfe9878bd9264754a50eaa128b`  
		Last Modified: Thu, 22 Jul 2021 02:20:37 GMT  
		Size: 42.1 MB (42120108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf69efd3b547fe4dc472fd34a54c466b82ce51b7f04957779206b5ea0ef9160`  
		Last Modified: Thu, 22 Jul 2021 04:41:23 GMT  
		Size: 10.0 MB (9950872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7430ae4c6b93ca669cc72566a38f952b74dece32c5897c46e51a5907bd5a0c`  
		Last Modified: Thu, 22 Jul 2021 04:41:20 GMT  
		Size: 3.9 MB (3921255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d288a7a9052de99ec8f43901d57a79d2ed295f5365af74abc65676e9d1a597`  
		Last Modified: Fri, 23 Jul 2021 11:01:53 GMT  
		Size: 13.5 MB (13489598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df3480c3f7f784068324a7a0264eefbde158fee4a796d2b818ac07b85051cec`  
		Last Modified: Fri, 23 Jul 2021 11:01:49 GMT  
		Size: 2.9 KB (2853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad786f7a776faed48a2f5fe6cc4ed989f002a067a1419b112731a2a2c379c549`  
		Last Modified: Fri, 23 Jul 2021 11:02:33 GMT  
		Size: 34.8 MB (34786687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f19d7d688b3f16eee058bcfd3c28142e19f2944d9720a1fcc9aeb7de1a37fb`  
		Last Modified: Fri, 23 Jul 2021 11:02:15 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f624dcbf4cdec850d810382c22a2b3cfb9b478b42f3a632a76319d1a142be8a5`  
		Last Modified: Fri, 23 Jul 2021 11:02:15 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:72c4109486cbe275b9ca2ef8e50d2e211e38fe1ce70f73e527c5839fac8419de
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105068396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad801b11ae96591268aac7953811a632a6615ffc7c92077fd3d80ddb60901ad4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 22 Jul 2021 00:41:26 GMT
ADD file:fab290162e6d28cbe115c866c49a1e09d955450dc9e831ccbeefe40e18cfa3a7 in / 
# Thu, 22 Jul 2021 00:41:27 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:18:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:18:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 13:28:05 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 22 Jul 2021 13:28:09 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 22 Jul 2021 13:28:20 GMT
ENV KAPACITOR_VERSION=1.5.9
# Thu, 22 Jul 2021 13:28:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 22 Jul 2021 13:28:23 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 22 Jul 2021 13:28:23 GMT
EXPOSE 9092
# Thu, 22 Jul 2021 13:28:24 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 22 Jul 2021 13:28:24 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 22 Jul 2021 13:28:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Jul 2021 13:28:24 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:28ed64be8f9ee39d8ded09482441a288852dd40c2e535b64e1f9c0271c10eb44`  
		Last Modified: Thu, 22 Jul 2021 00:48:16 GMT  
		Size: 43.2 MB (43178440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6227db87dba6bebff5c1f1a2bd2d290c25c44c23f3b974a4e99fe72b48777812`  
		Last Modified: Thu, 22 Jul 2021 01:27:41 GMT  
		Size: 10.2 MB (10214761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cffb4d8549ecf5dfe60357ee2dc98dd618c73220f26c8cd505b088085229668`  
		Last Modified: Thu, 22 Jul 2021 01:27:40 GMT  
		Size: 4.1 MB (4096559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6346e9072bed6a2f6624d105c5f466f3ad8014bfb827b52970a16068730eaf53`  
		Last Modified: Thu, 22 Jul 2021 13:28:46 GMT  
		Size: 13.0 MB (13014410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5108cf0dcc3d42daee7af1dd9c991f51426fdac7db2286bb43658e80f013dd`  
		Last Modified: Thu, 22 Jul 2021 13:28:44 GMT  
		Size: 2.9 KB (2855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2ac8cb046154d41e652250ff93604f8bc0717f2aa926e511591699a7e5de3b`  
		Last Modified: Thu, 22 Jul 2021 13:29:05 GMT  
		Size: 34.6 MB (34560917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcdecb78aba02fe8abaac90910701564b6f81f4c66c70964eaa3ef4297fae5e`  
		Last Modified: Thu, 22 Jul 2021 13:29:00 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59cfdcd7be9512de52c98344ab0fbf114ebc91575377be2b40222c9967351fd`  
		Last Modified: Thu, 22 Jul 2021 13:29:00 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
