<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.11`](#telegraf111)
-	[`telegraf:1.11.5`](#telegraf1115)
-	[`telegraf:1.11.5-alpine`](#telegraf1115-alpine)
-	[`telegraf:1.11-alpine`](#telegraf111-alpine)
-	[`telegraf:1.12`](#telegraf112)
-	[`telegraf:1.12.6`](#telegraf1126)
-	[`telegraf:1.12.6-alpine`](#telegraf1126-alpine)
-	[`telegraf:1.12-alpine`](#telegraf112-alpine)
-	[`telegraf:1.13`](#telegraf113)
-	[`telegraf:1.13.4`](#telegraf1134)
-	[`telegraf:1.13.4-alpine`](#telegraf1134-alpine)
-	[`telegraf:1.13-alpine`](#telegraf113-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.11`

```console
$ docker pull telegraf@sha256:5015c47866d9eb9b873895a03a49f3c4954b543e1b0c4064dcf1cc6571c9a7cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.11` - linux; amd64

```console
$ docker pull telegraf@sha256:abca7567ca713a2bee87ba09fa843964fbd4581fab3a1e030e9dd1b096a44158
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96881174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cf8b23e00034ccbe169e58c57db2bd91f5035338023a07f44cba6ddc800aea8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 26 Feb 2020 00:41:14 GMT
ADD file:08c5ab7c53526da155d6be40a9795fc08afc9f47bd333c096e90185fe9fab2b1 in / 
# Wed, 26 Feb 2020 00:41:14 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:17:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:17:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 27 Feb 2020 03:46:55 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Thu, 27 Feb 2020 03:46:58 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 03:46:58 GMT
ENV TELEGRAF_VERSION=1.11.5
# Thu, 27 Feb 2020 03:47:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 27 Feb 2020 03:47:01 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 27 Feb 2020 03:47:01 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Thu, 27 Feb 2020 03:47:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Feb 2020 03:47:02 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c0c53f743a403d45480d026864d9611d6eb898e897d60c13ae854ad453d462a4`  
		Last Modified: Wed, 26 Feb 2020 00:47:05 GMT  
		Size: 45.4 MB (45375932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66997431d390aecfd02e57222c9b5752d314a4508de82c9b43c66812c3434ed4`  
		Last Modified: Wed, 26 Feb 2020 01:23:37 GMT  
		Size: 10.8 MB (10797283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea865e2909f355d736daef9076ecda63b3075c6267b858d9eaaf2e3966fc0d2`  
		Last Modified: Wed, 26 Feb 2020 01:23:36 GMT  
		Size: 4.3 MB (4340193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c88bc97a5eac56e184580f940a4f029efc2a5833a63f5e3b388235eba13c2a8`  
		Last Modified: Thu, 27 Feb 2020 03:47:46 GMT  
		Size: 16.0 MB (15964515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be22d8f1978c9458f25db77f824eaf5082ba3e987122c82d9735e424cc9c1e8e`  
		Last Modified: Thu, 27 Feb 2020 03:47:42 GMT  
		Size: 2.8 KB (2774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651cdafe710f41e9076f6aa0890043a16ef0ee7833e26b8ed644967e4d1712fc`  
		Last Modified: Thu, 27 Feb 2020 03:47:47 GMT  
		Size: 20.4 MB (20400290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ce65214475583ade3e22b75dcb76d275d434179e8cb862d4e52c3131ae17bb`  
		Last Modified: Thu, 27 Feb 2020 03:47:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.11` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:1f976af21e1443dad88c0eeb2e476890cc3d5fedf6a32bcc15362f64517b5f65
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89622472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7214dcd7db9acaf706b8d521b29c0a353f0b34974ff590bb4c71aa497c7c875`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 26 Feb 2020 00:59:40 GMT
ADD file:6497e2f777f4487d9221931005a8b4b81c021442a769b581e223cf30c81ff553 in / 
# Wed, 26 Feb 2020 00:59:53 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 02:27:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 02:27:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 22:39:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 22:39:36 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 26 Feb 2020 22:39:37 GMT
ENV TELEGRAF_VERSION=1.11.5
# Wed, 26 Feb 2020 22:39:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 26 Feb 2020 22:39:43 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 26 Feb 2020 22:39:43 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 26 Feb 2020 22:39:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Feb 2020 22:39:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2478a2ed882cb5fbb5e4e92c9f580da9ca52f5fc78b8bb439ecbf3ac18023caa`  
		Last Modified: Wed, 26 Feb 2020 01:11:29 GMT  
		Size: 42.1 MB (42100335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c541086e0dffa72464d4077dcc60504a1c08a73ecec554c159269786ba08fed`  
		Last Modified: Wed, 26 Feb 2020 02:37:24 GMT  
		Size: 9.5 MB (9498391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf0f97b070f73118badb36d21af3459f8317d4ac6d45aec680092cc962f1c47`  
		Last Modified: Wed, 26 Feb 2020 02:37:23 GMT  
		Size: 3.9 MB (3918781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72b82e5ea1ce74c629ee54374affe651a03b088d27ce98d02cc0362c5c97ddb`  
		Last Modified: Wed, 26 Feb 2020 22:40:29 GMT  
		Size: 14.8 MB (14839243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f886a9cb8cf01cad24d98ebeb20ae5ab165501700d0d9ce52baa216e62cf7828`  
		Last Modified: Wed, 26 Feb 2020 22:40:24 GMT  
		Size: 2.8 KB (2801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b95331375bddcec348e463be5f876c6ebae4cd478d04736bbf43f23c3d9efd`  
		Last Modified: Wed, 26 Feb 2020 22:40:30 GMT  
		Size: 19.3 MB (19262736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3986e6257bd049dfdb7ec26e98b173297c6255bff7ceaa5194be87e48e8f514d`  
		Last Modified: Wed, 26 Feb 2020 22:40:24 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.11` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:f69dbde6ec4d7f20536e4325a02bb4c72264de302ac3c9d463adf5c0557cac29
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91387872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4457ba11a7d7152e3c485c922b3ab4b57cfa7b2c1a077b7463008dc061b84059`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 26 Feb 2020 00:50:03 GMT
ADD file:c82c7dc82c2eb3b50218c35e1b848f707b134d2df957f57125408f69aaeb9b96 in / 
# Wed, 26 Feb 2020 00:50:15 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 03:59:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 03:59:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 23:09:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 23:09:49 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 26 Feb 2020 23:09:50 GMT
ENV TELEGRAF_VERSION=1.11.5
# Wed, 26 Feb 2020 23:09:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 26 Feb 2020 23:09:55 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 26 Feb 2020 23:09:56 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 26 Feb 2020 23:09:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Feb 2020 23:09:57 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:668c278237ef972312df4979c8fb1a927b38db5da09f094ae4fcc84a061dedf8`  
		Last Modified: Wed, 26 Feb 2020 00:58:30 GMT  
		Size: 43.2 MB (43158146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b41cac09012800692bd13a1238260bfb293c18c7864536c494809f2983ad770`  
		Last Modified: Wed, 26 Feb 2020 04:08:32 GMT  
		Size: 9.7 MB (9748511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094b353938273b0bbc576a8a80a232614ca2d9bfe48769641eee7055f3db6a5e`  
		Last Modified: Wed, 26 Feb 2020 04:08:31 GMT  
		Size: 4.1 MB (4094435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a6e84d4e14247280f0fd1fbd5a82033129b5135c2099807933ac0fac69a92a`  
		Last Modified: Wed, 26 Feb 2020 23:10:46 GMT  
		Size: 15.5 MB (15530092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a4677cafd0a8d9f616e558c61fdcea352bf03a6cb4b548e0fc1a44d8582b9c`  
		Last Modified: Wed, 26 Feb 2020 23:10:41 GMT  
		Size: 2.8 KB (2800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8222beed1ba6324945b9d1a38f2459123042943b9cd422f41203772c0aa571bc`  
		Last Modified: Wed, 26 Feb 2020 23:10:48 GMT  
		Size: 18.9 MB (18853705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03abc687ddd37f0b211b95c5b69e530663e27893937551d8a63ebd198bd6ac9`  
		Last Modified: Wed, 26 Feb 2020 23:10:41 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.11.5`

```console
$ docker pull telegraf@sha256:5015c47866d9eb9b873895a03a49f3c4954b543e1b0c4064dcf1cc6571c9a7cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.11.5` - linux; amd64

```console
$ docker pull telegraf@sha256:abca7567ca713a2bee87ba09fa843964fbd4581fab3a1e030e9dd1b096a44158
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96881174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cf8b23e00034ccbe169e58c57db2bd91f5035338023a07f44cba6ddc800aea8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 26 Feb 2020 00:41:14 GMT
ADD file:08c5ab7c53526da155d6be40a9795fc08afc9f47bd333c096e90185fe9fab2b1 in / 
# Wed, 26 Feb 2020 00:41:14 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:17:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:17:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 27 Feb 2020 03:46:55 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Thu, 27 Feb 2020 03:46:58 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 03:46:58 GMT
ENV TELEGRAF_VERSION=1.11.5
# Thu, 27 Feb 2020 03:47:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 27 Feb 2020 03:47:01 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 27 Feb 2020 03:47:01 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Thu, 27 Feb 2020 03:47:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Feb 2020 03:47:02 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c0c53f743a403d45480d026864d9611d6eb898e897d60c13ae854ad453d462a4`  
		Last Modified: Wed, 26 Feb 2020 00:47:05 GMT  
		Size: 45.4 MB (45375932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66997431d390aecfd02e57222c9b5752d314a4508de82c9b43c66812c3434ed4`  
		Last Modified: Wed, 26 Feb 2020 01:23:37 GMT  
		Size: 10.8 MB (10797283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea865e2909f355d736daef9076ecda63b3075c6267b858d9eaaf2e3966fc0d2`  
		Last Modified: Wed, 26 Feb 2020 01:23:36 GMT  
		Size: 4.3 MB (4340193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c88bc97a5eac56e184580f940a4f029efc2a5833a63f5e3b388235eba13c2a8`  
		Last Modified: Thu, 27 Feb 2020 03:47:46 GMT  
		Size: 16.0 MB (15964515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be22d8f1978c9458f25db77f824eaf5082ba3e987122c82d9735e424cc9c1e8e`  
		Last Modified: Thu, 27 Feb 2020 03:47:42 GMT  
		Size: 2.8 KB (2774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651cdafe710f41e9076f6aa0890043a16ef0ee7833e26b8ed644967e4d1712fc`  
		Last Modified: Thu, 27 Feb 2020 03:47:47 GMT  
		Size: 20.4 MB (20400290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ce65214475583ade3e22b75dcb76d275d434179e8cb862d4e52c3131ae17bb`  
		Last Modified: Thu, 27 Feb 2020 03:47:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.11.5` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:1f976af21e1443dad88c0eeb2e476890cc3d5fedf6a32bcc15362f64517b5f65
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89622472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7214dcd7db9acaf706b8d521b29c0a353f0b34974ff590bb4c71aa497c7c875`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 26 Feb 2020 00:59:40 GMT
ADD file:6497e2f777f4487d9221931005a8b4b81c021442a769b581e223cf30c81ff553 in / 
# Wed, 26 Feb 2020 00:59:53 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 02:27:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 02:27:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 22:39:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 22:39:36 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 26 Feb 2020 22:39:37 GMT
ENV TELEGRAF_VERSION=1.11.5
# Wed, 26 Feb 2020 22:39:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 26 Feb 2020 22:39:43 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 26 Feb 2020 22:39:43 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 26 Feb 2020 22:39:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Feb 2020 22:39:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2478a2ed882cb5fbb5e4e92c9f580da9ca52f5fc78b8bb439ecbf3ac18023caa`  
		Last Modified: Wed, 26 Feb 2020 01:11:29 GMT  
		Size: 42.1 MB (42100335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c541086e0dffa72464d4077dcc60504a1c08a73ecec554c159269786ba08fed`  
		Last Modified: Wed, 26 Feb 2020 02:37:24 GMT  
		Size: 9.5 MB (9498391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf0f97b070f73118badb36d21af3459f8317d4ac6d45aec680092cc962f1c47`  
		Last Modified: Wed, 26 Feb 2020 02:37:23 GMT  
		Size: 3.9 MB (3918781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72b82e5ea1ce74c629ee54374affe651a03b088d27ce98d02cc0362c5c97ddb`  
		Last Modified: Wed, 26 Feb 2020 22:40:29 GMT  
		Size: 14.8 MB (14839243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f886a9cb8cf01cad24d98ebeb20ae5ab165501700d0d9ce52baa216e62cf7828`  
		Last Modified: Wed, 26 Feb 2020 22:40:24 GMT  
		Size: 2.8 KB (2801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b95331375bddcec348e463be5f876c6ebae4cd478d04736bbf43f23c3d9efd`  
		Last Modified: Wed, 26 Feb 2020 22:40:30 GMT  
		Size: 19.3 MB (19262736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3986e6257bd049dfdb7ec26e98b173297c6255bff7ceaa5194be87e48e8f514d`  
		Last Modified: Wed, 26 Feb 2020 22:40:24 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.11.5` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:f69dbde6ec4d7f20536e4325a02bb4c72264de302ac3c9d463adf5c0557cac29
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91387872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4457ba11a7d7152e3c485c922b3ab4b57cfa7b2c1a077b7463008dc061b84059`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 26 Feb 2020 00:50:03 GMT
ADD file:c82c7dc82c2eb3b50218c35e1b848f707b134d2df957f57125408f69aaeb9b96 in / 
# Wed, 26 Feb 2020 00:50:15 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 03:59:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 03:59:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 23:09:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 23:09:49 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 26 Feb 2020 23:09:50 GMT
ENV TELEGRAF_VERSION=1.11.5
# Wed, 26 Feb 2020 23:09:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 26 Feb 2020 23:09:55 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 26 Feb 2020 23:09:56 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 26 Feb 2020 23:09:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Feb 2020 23:09:57 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:668c278237ef972312df4979c8fb1a927b38db5da09f094ae4fcc84a061dedf8`  
		Last Modified: Wed, 26 Feb 2020 00:58:30 GMT  
		Size: 43.2 MB (43158146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b41cac09012800692bd13a1238260bfb293c18c7864536c494809f2983ad770`  
		Last Modified: Wed, 26 Feb 2020 04:08:32 GMT  
		Size: 9.7 MB (9748511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094b353938273b0bbc576a8a80a232614ca2d9bfe48769641eee7055f3db6a5e`  
		Last Modified: Wed, 26 Feb 2020 04:08:31 GMT  
		Size: 4.1 MB (4094435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a6e84d4e14247280f0fd1fbd5a82033129b5135c2099807933ac0fac69a92a`  
		Last Modified: Wed, 26 Feb 2020 23:10:46 GMT  
		Size: 15.5 MB (15530092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a4677cafd0a8d9f616e558c61fdcea352bf03a6cb4b548e0fc1a44d8582b9c`  
		Last Modified: Wed, 26 Feb 2020 23:10:41 GMT  
		Size: 2.8 KB (2800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8222beed1ba6324945b9d1a38f2459123042943b9cd422f41203772c0aa571bc`  
		Last Modified: Wed, 26 Feb 2020 23:10:48 GMT  
		Size: 18.9 MB (18853705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03abc687ddd37f0b211b95c5b69e530663e27893937551d8a63ebd198bd6ac9`  
		Last Modified: Wed, 26 Feb 2020 23:10:41 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.11.5-alpine`

```console
$ docker pull telegraf@sha256:e8f44f2bb35b063d2450e36e7784f78373c3e4500fcc2fffe6319debf3ea6115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.11.5-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:ce32c9b35e1b1e088ed45c0e68ab1fd21ab03279433316e34372a0543e707be1
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26876416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5f1249ce324386bb0b1e553338e68f53090e01551dde52155a9d47d4c67df7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Jan 2020 06:15:43 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Fri, 24 Jan 2020 06:15:43 GMT
ENV TELEGRAF_VERSION=1.11.5
# Fri, 24 Jan 2020 06:15:47 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/telegraf.conf /etc/telegraf/ &&     chmod +x /usr/src/telegraf*/* &&     cp -a /usr/src/telegraf*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 24 Jan 2020 06:15:47 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 24 Jan 2020 06:15:47 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Fri, 24 Jan 2020 06:15:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2020 06:15:47 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444cfcaf178343a9f58fc894ab2f74510cab12f8a33ca82fe7fa41ef18e72b2c`  
		Last Modified: Fri, 24 Jan 2020 06:16:26 GMT  
		Size: 3.7 MB (3721327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7762a2bb8b583bd2361ede93c28381b740d4d29c004cb2562edf4559d1c8b1d4`  
		Last Modified: Fri, 24 Jan 2020 06:16:30 GMT  
		Size: 20.4 MB (20390577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7789f28ac82b3c1abe5ed4384ef6289a6f12ff2765f11b6fd42903d3ec7e2661`  
		Last Modified: Fri, 24 Jan 2020 06:16:24 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.11-alpine`

```console
$ docker pull telegraf@sha256:e8f44f2bb35b063d2450e36e7784f78373c3e4500fcc2fffe6319debf3ea6115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.11-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:ce32c9b35e1b1e088ed45c0e68ab1fd21ab03279433316e34372a0543e707be1
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26876416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5f1249ce324386bb0b1e553338e68f53090e01551dde52155a9d47d4c67df7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Jan 2020 06:15:43 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Fri, 24 Jan 2020 06:15:43 GMT
ENV TELEGRAF_VERSION=1.11.5
# Fri, 24 Jan 2020 06:15:47 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/telegraf.conf /etc/telegraf/ &&     chmod +x /usr/src/telegraf*/* &&     cp -a /usr/src/telegraf*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 24 Jan 2020 06:15:47 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 24 Jan 2020 06:15:47 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Fri, 24 Jan 2020 06:15:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2020 06:15:47 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444cfcaf178343a9f58fc894ab2f74510cab12f8a33ca82fe7fa41ef18e72b2c`  
		Last Modified: Fri, 24 Jan 2020 06:16:26 GMT  
		Size: 3.7 MB (3721327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7762a2bb8b583bd2361ede93c28381b740d4d29c004cb2562edf4559d1c8b1d4`  
		Last Modified: Fri, 24 Jan 2020 06:16:30 GMT  
		Size: 20.4 MB (20390577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7789f28ac82b3c1abe5ed4384ef6289a6f12ff2765f11b6fd42903d3ec7e2661`  
		Last Modified: Fri, 24 Jan 2020 06:16:24 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.12`

```console
$ docker pull telegraf@sha256:ac00e93410eb8df63096a28e86ba960becbc3a71152dcb8c90c51188795ff113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.12` - linux; amd64

```console
$ docker pull telegraf@sha256:b0db54773ac1297b72018c64c2e87735303b71316d161b91196391d4e6cb698c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.8 MB (97849446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b628fde51704600239126ca22f4c5105a5081aba3b5c15b75a0042a8472d392`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 26 Feb 2020 00:41:14 GMT
ADD file:08c5ab7c53526da155d6be40a9795fc08afc9f47bd333c096e90185fe9fab2b1 in / 
# Wed, 26 Feb 2020 00:41:14 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:17:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:17:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 27 Feb 2020 03:46:55 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Thu, 27 Feb 2020 03:46:58 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 03:47:11 GMT
ENV TELEGRAF_VERSION=1.12.6
# Thu, 27 Feb 2020 03:47:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 27 Feb 2020 03:47:14 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 27 Feb 2020 03:47:14 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Thu, 27 Feb 2020 03:47:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Feb 2020 03:47:14 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c0c53f743a403d45480d026864d9611d6eb898e897d60c13ae854ad453d462a4`  
		Last Modified: Wed, 26 Feb 2020 00:47:05 GMT  
		Size: 45.4 MB (45375932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66997431d390aecfd02e57222c9b5752d314a4508de82c9b43c66812c3434ed4`  
		Last Modified: Wed, 26 Feb 2020 01:23:37 GMT  
		Size: 10.8 MB (10797283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea865e2909f355d736daef9076ecda63b3075c6267b858d9eaaf2e3966fc0d2`  
		Last Modified: Wed, 26 Feb 2020 01:23:36 GMT  
		Size: 4.3 MB (4340193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c88bc97a5eac56e184580f940a4f029efc2a5833a63f5e3b388235eba13c2a8`  
		Last Modified: Thu, 27 Feb 2020 03:47:46 GMT  
		Size: 16.0 MB (15964515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be22d8f1978c9458f25db77f824eaf5082ba3e987122c82d9735e424cc9c1e8e`  
		Last Modified: Thu, 27 Feb 2020 03:47:42 GMT  
		Size: 2.8 KB (2774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8456008d93ab63760acee4267ab143e9fdffd5fb80bb95c3edeb44dc3cf5232`  
		Last Modified: Thu, 27 Feb 2020 03:47:56 GMT  
		Size: 21.4 MB (21368563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61dd9445ae2cbc65ea94e771d0df8515f95a8986c415ce36107d593f26e5f5f5`  
		Last Modified: Thu, 27 Feb 2020 03:47:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.12` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:eb72d8aa8f24c60d82063fc2838ad19592d6725ba9d91851e562293545883f0b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90521046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354943fb8ddc34ac1ea1d36d92cdc21c2c408358412aedf268c43c01f6dc4f3f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 26 Feb 2020 00:59:40 GMT
ADD file:6497e2f777f4487d9221931005a8b4b81c021442a769b581e223cf30c81ff553 in / 
# Wed, 26 Feb 2020 00:59:53 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 02:27:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 02:27:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 22:39:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 22:39:36 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 26 Feb 2020 22:39:50 GMT
ENV TELEGRAF_VERSION=1.12.6
# Wed, 26 Feb 2020 22:39:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 26 Feb 2020 22:39:56 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 26 Feb 2020 22:39:56 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 26 Feb 2020 22:39:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Feb 2020 22:39:57 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2478a2ed882cb5fbb5e4e92c9f580da9ca52f5fc78b8bb439ecbf3ac18023caa`  
		Last Modified: Wed, 26 Feb 2020 01:11:29 GMT  
		Size: 42.1 MB (42100335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c541086e0dffa72464d4077dcc60504a1c08a73ecec554c159269786ba08fed`  
		Last Modified: Wed, 26 Feb 2020 02:37:24 GMT  
		Size: 9.5 MB (9498391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf0f97b070f73118badb36d21af3459f8317d4ac6d45aec680092cc962f1c47`  
		Last Modified: Wed, 26 Feb 2020 02:37:23 GMT  
		Size: 3.9 MB (3918781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72b82e5ea1ce74c629ee54374affe651a03b088d27ce98d02cc0362c5c97ddb`  
		Last Modified: Wed, 26 Feb 2020 22:40:29 GMT  
		Size: 14.8 MB (14839243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f886a9cb8cf01cad24d98ebeb20ae5ab165501700d0d9ce52baa216e62cf7828`  
		Last Modified: Wed, 26 Feb 2020 22:40:24 GMT  
		Size: 2.8 KB (2801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67379ec4d838f3d5c8936abc4340a0ccdce300fe8debe22319079429ea5378b`  
		Last Modified: Wed, 26 Feb 2020 22:40:43 GMT  
		Size: 20.2 MB (20161311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603179329faa9fb5c8e35f6e381b9c1a4ac71d8379c809c01e59c6107c130095`  
		Last Modified: Wed, 26 Feb 2020 22:40:36 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.12` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:5d256068a6adeeaf5c1736b8a20f4467008cd25878f163a3065285acffa95449
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92266689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df9f9dd06539a9a3d025fd858a8e46b5710400bc27b30b240cd55c140c06926`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 26 Feb 2020 00:50:03 GMT
ADD file:c82c7dc82c2eb3b50218c35e1b848f707b134d2df957f57125408f69aaeb9b96 in / 
# Wed, 26 Feb 2020 00:50:15 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 03:59:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 03:59:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 23:09:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 23:09:49 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 26 Feb 2020 23:10:07 GMT
ENV TELEGRAF_VERSION=1.12.6
# Wed, 26 Feb 2020 23:10:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 26 Feb 2020 23:10:13 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 26 Feb 2020 23:10:13 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 26 Feb 2020 23:10:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Feb 2020 23:10:15 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:668c278237ef972312df4979c8fb1a927b38db5da09f094ae4fcc84a061dedf8`  
		Last Modified: Wed, 26 Feb 2020 00:58:30 GMT  
		Size: 43.2 MB (43158146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b41cac09012800692bd13a1238260bfb293c18c7864536c494809f2983ad770`  
		Last Modified: Wed, 26 Feb 2020 04:08:32 GMT  
		Size: 9.7 MB (9748511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094b353938273b0bbc576a8a80a232614ca2d9bfe48769641eee7055f3db6a5e`  
		Last Modified: Wed, 26 Feb 2020 04:08:31 GMT  
		Size: 4.1 MB (4094435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a6e84d4e14247280f0fd1fbd5a82033129b5135c2099807933ac0fac69a92a`  
		Last Modified: Wed, 26 Feb 2020 23:10:46 GMT  
		Size: 15.5 MB (15530092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a4677cafd0a8d9f616e558c61fdcea352bf03a6cb4b548e0fc1a44d8582b9c`  
		Last Modified: Wed, 26 Feb 2020 23:10:41 GMT  
		Size: 2.8 KB (2800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5fc86f0b9402e62a151ac18801f321b5f38f9ce0f9c4c22fb5f15fc4947bcbe`  
		Last Modified: Wed, 26 Feb 2020 23:11:04 GMT  
		Size: 19.7 MB (19732520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea2fba39bd7466740de97b1a032ede5a5ad8eb48f592a26db7ae2e9d0d7fd1d`  
		Last Modified: Wed, 26 Feb 2020 23:10:54 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.12.6`

```console
$ docker pull telegraf@sha256:ac00e93410eb8df63096a28e86ba960becbc3a71152dcb8c90c51188795ff113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.12.6` - linux; amd64

```console
$ docker pull telegraf@sha256:b0db54773ac1297b72018c64c2e87735303b71316d161b91196391d4e6cb698c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.8 MB (97849446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b628fde51704600239126ca22f4c5105a5081aba3b5c15b75a0042a8472d392`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 26 Feb 2020 00:41:14 GMT
ADD file:08c5ab7c53526da155d6be40a9795fc08afc9f47bd333c096e90185fe9fab2b1 in / 
# Wed, 26 Feb 2020 00:41:14 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:17:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:17:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 27 Feb 2020 03:46:55 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Thu, 27 Feb 2020 03:46:58 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 03:47:11 GMT
ENV TELEGRAF_VERSION=1.12.6
# Thu, 27 Feb 2020 03:47:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 27 Feb 2020 03:47:14 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 27 Feb 2020 03:47:14 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Thu, 27 Feb 2020 03:47:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Feb 2020 03:47:14 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c0c53f743a403d45480d026864d9611d6eb898e897d60c13ae854ad453d462a4`  
		Last Modified: Wed, 26 Feb 2020 00:47:05 GMT  
		Size: 45.4 MB (45375932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66997431d390aecfd02e57222c9b5752d314a4508de82c9b43c66812c3434ed4`  
		Last Modified: Wed, 26 Feb 2020 01:23:37 GMT  
		Size: 10.8 MB (10797283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea865e2909f355d736daef9076ecda63b3075c6267b858d9eaaf2e3966fc0d2`  
		Last Modified: Wed, 26 Feb 2020 01:23:36 GMT  
		Size: 4.3 MB (4340193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c88bc97a5eac56e184580f940a4f029efc2a5833a63f5e3b388235eba13c2a8`  
		Last Modified: Thu, 27 Feb 2020 03:47:46 GMT  
		Size: 16.0 MB (15964515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be22d8f1978c9458f25db77f824eaf5082ba3e987122c82d9735e424cc9c1e8e`  
		Last Modified: Thu, 27 Feb 2020 03:47:42 GMT  
		Size: 2.8 KB (2774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8456008d93ab63760acee4267ab143e9fdffd5fb80bb95c3edeb44dc3cf5232`  
		Last Modified: Thu, 27 Feb 2020 03:47:56 GMT  
		Size: 21.4 MB (21368563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61dd9445ae2cbc65ea94e771d0df8515f95a8986c415ce36107d593f26e5f5f5`  
		Last Modified: Thu, 27 Feb 2020 03:47:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.12.6` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:eb72d8aa8f24c60d82063fc2838ad19592d6725ba9d91851e562293545883f0b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90521046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354943fb8ddc34ac1ea1d36d92cdc21c2c408358412aedf268c43c01f6dc4f3f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 26 Feb 2020 00:59:40 GMT
ADD file:6497e2f777f4487d9221931005a8b4b81c021442a769b581e223cf30c81ff553 in / 
# Wed, 26 Feb 2020 00:59:53 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 02:27:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 02:27:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 22:39:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 22:39:36 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 26 Feb 2020 22:39:50 GMT
ENV TELEGRAF_VERSION=1.12.6
# Wed, 26 Feb 2020 22:39:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 26 Feb 2020 22:39:56 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 26 Feb 2020 22:39:56 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 26 Feb 2020 22:39:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Feb 2020 22:39:57 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2478a2ed882cb5fbb5e4e92c9f580da9ca52f5fc78b8bb439ecbf3ac18023caa`  
		Last Modified: Wed, 26 Feb 2020 01:11:29 GMT  
		Size: 42.1 MB (42100335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c541086e0dffa72464d4077dcc60504a1c08a73ecec554c159269786ba08fed`  
		Last Modified: Wed, 26 Feb 2020 02:37:24 GMT  
		Size: 9.5 MB (9498391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf0f97b070f73118badb36d21af3459f8317d4ac6d45aec680092cc962f1c47`  
		Last Modified: Wed, 26 Feb 2020 02:37:23 GMT  
		Size: 3.9 MB (3918781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72b82e5ea1ce74c629ee54374affe651a03b088d27ce98d02cc0362c5c97ddb`  
		Last Modified: Wed, 26 Feb 2020 22:40:29 GMT  
		Size: 14.8 MB (14839243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f886a9cb8cf01cad24d98ebeb20ae5ab165501700d0d9ce52baa216e62cf7828`  
		Last Modified: Wed, 26 Feb 2020 22:40:24 GMT  
		Size: 2.8 KB (2801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67379ec4d838f3d5c8936abc4340a0ccdce300fe8debe22319079429ea5378b`  
		Last Modified: Wed, 26 Feb 2020 22:40:43 GMT  
		Size: 20.2 MB (20161311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603179329faa9fb5c8e35f6e381b9c1a4ac71d8379c809c01e59c6107c130095`  
		Last Modified: Wed, 26 Feb 2020 22:40:36 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.12.6` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:5d256068a6adeeaf5c1736b8a20f4467008cd25878f163a3065285acffa95449
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92266689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df9f9dd06539a9a3d025fd858a8e46b5710400bc27b30b240cd55c140c06926`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 26 Feb 2020 00:50:03 GMT
ADD file:c82c7dc82c2eb3b50218c35e1b848f707b134d2df957f57125408f69aaeb9b96 in / 
# Wed, 26 Feb 2020 00:50:15 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 03:59:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 03:59:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 23:09:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 23:09:49 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 26 Feb 2020 23:10:07 GMT
ENV TELEGRAF_VERSION=1.12.6
# Wed, 26 Feb 2020 23:10:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 26 Feb 2020 23:10:13 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 26 Feb 2020 23:10:13 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 26 Feb 2020 23:10:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Feb 2020 23:10:15 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:668c278237ef972312df4979c8fb1a927b38db5da09f094ae4fcc84a061dedf8`  
		Last Modified: Wed, 26 Feb 2020 00:58:30 GMT  
		Size: 43.2 MB (43158146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b41cac09012800692bd13a1238260bfb293c18c7864536c494809f2983ad770`  
		Last Modified: Wed, 26 Feb 2020 04:08:32 GMT  
		Size: 9.7 MB (9748511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094b353938273b0bbc576a8a80a232614ca2d9bfe48769641eee7055f3db6a5e`  
		Last Modified: Wed, 26 Feb 2020 04:08:31 GMT  
		Size: 4.1 MB (4094435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a6e84d4e14247280f0fd1fbd5a82033129b5135c2099807933ac0fac69a92a`  
		Last Modified: Wed, 26 Feb 2020 23:10:46 GMT  
		Size: 15.5 MB (15530092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a4677cafd0a8d9f616e558c61fdcea352bf03a6cb4b548e0fc1a44d8582b9c`  
		Last Modified: Wed, 26 Feb 2020 23:10:41 GMT  
		Size: 2.8 KB (2800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5fc86f0b9402e62a151ac18801f321b5f38f9ce0f9c4c22fb5f15fc4947bcbe`  
		Last Modified: Wed, 26 Feb 2020 23:11:04 GMT  
		Size: 19.7 MB (19732520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea2fba39bd7466740de97b1a032ede5a5ad8eb48f592a26db7ae2e9d0d7fd1d`  
		Last Modified: Wed, 26 Feb 2020 23:10:54 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.12.6-alpine`

```console
$ docker pull telegraf@sha256:1ede048f390fbc0b6d15263f4148ef83dd36971d10b61f868cf7602776cc00cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.12.6-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:67e4bb84ae45303faf654018db5835111cfc0071e37bfb16609e649a5a3d7631
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.8 MB (27846105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcfaa9bae9ca7bb859b07a33c80cf1e7a5e6482750782932f52bd7c7b8f53bd1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Jan 2020 06:15:43 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Fri, 24 Jan 2020 06:15:55 GMT
ENV TELEGRAF_VERSION=1.12.6
# Fri, 24 Jan 2020 06:15:58 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/telegraf.conf /etc/telegraf/ &&     chmod +x /usr/src/telegraf*/* &&     cp -a /usr/src/telegraf*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 24 Jan 2020 06:15:59 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 24 Jan 2020 06:15:59 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Fri, 24 Jan 2020 06:15:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2020 06:15:59 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444cfcaf178343a9f58fc894ab2f74510cab12f8a33ca82fe7fa41ef18e72b2c`  
		Last Modified: Fri, 24 Jan 2020 06:16:26 GMT  
		Size: 3.7 MB (3721327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44db90b4a631f7b5bef5a6b9efc6ca7968289f5c8d1d3ac6e22e50a7924d7b2e`  
		Last Modified: Fri, 24 Jan 2020 06:16:46 GMT  
		Size: 21.4 MB (21360266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81f5a834d4204ed812dcb03d57c6275ad1cdb20f93e1caf6cfbcc2d96068f1c`  
		Last Modified: Fri, 24 Jan 2020 06:16:36 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.12-alpine`

```console
$ docker pull telegraf@sha256:1ede048f390fbc0b6d15263f4148ef83dd36971d10b61f868cf7602776cc00cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.12-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:67e4bb84ae45303faf654018db5835111cfc0071e37bfb16609e649a5a3d7631
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.8 MB (27846105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcfaa9bae9ca7bb859b07a33c80cf1e7a5e6482750782932f52bd7c7b8f53bd1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Jan 2020 06:15:43 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Fri, 24 Jan 2020 06:15:55 GMT
ENV TELEGRAF_VERSION=1.12.6
# Fri, 24 Jan 2020 06:15:58 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/telegraf.conf /etc/telegraf/ &&     chmod +x /usr/src/telegraf*/* &&     cp -a /usr/src/telegraf*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 24 Jan 2020 06:15:59 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 24 Jan 2020 06:15:59 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Fri, 24 Jan 2020 06:15:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2020 06:15:59 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444cfcaf178343a9f58fc894ab2f74510cab12f8a33ca82fe7fa41ef18e72b2c`  
		Last Modified: Fri, 24 Jan 2020 06:16:26 GMT  
		Size: 3.7 MB (3721327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44db90b4a631f7b5bef5a6b9efc6ca7968289f5c8d1d3ac6e22e50a7924d7b2e`  
		Last Modified: Fri, 24 Jan 2020 06:16:46 GMT  
		Size: 21.4 MB (21360266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81f5a834d4204ed812dcb03d57c6275ad1cdb20f93e1caf6cfbcc2d96068f1c`  
		Last Modified: Fri, 24 Jan 2020 06:16:36 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.13`

```console
$ docker pull telegraf@sha256:f703aab1f042adc5ce7bc2b6301ca904e49e01a0a30bf3d65ae881d22a4a910d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.13` - linux; amd64

```console
$ docker pull telegraf@sha256:614e580dc9609b5229c3ce4e06200333e9c9e40f245fabd753b61a7d9e6d13cc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.8 MB (96792682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d2b3c9f8e62b0a9eedc98271f448331a7a719b09920170ffa048776e9963c1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 26 Feb 2020 00:41:14 GMT
ADD file:08c5ab7c53526da155d6be40a9795fc08afc9f47bd333c096e90185fe9fab2b1 in / 
# Wed, 26 Feb 2020 00:41:14 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:17:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:17:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 27 Feb 2020 03:46:55 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Thu, 27 Feb 2020 03:46:58 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 03:47:22 GMT
ENV TELEGRAF_VERSION=1.13.4
# Thu, 27 Feb 2020 03:47:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 27 Feb 2020 03:47:25 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 27 Feb 2020 03:47:25 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Thu, 27 Feb 2020 03:47:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Feb 2020 03:47:25 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c0c53f743a403d45480d026864d9611d6eb898e897d60c13ae854ad453d462a4`  
		Last Modified: Wed, 26 Feb 2020 00:47:05 GMT  
		Size: 45.4 MB (45375932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66997431d390aecfd02e57222c9b5752d314a4508de82c9b43c66812c3434ed4`  
		Last Modified: Wed, 26 Feb 2020 01:23:37 GMT  
		Size: 10.8 MB (10797283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea865e2909f355d736daef9076ecda63b3075c6267b858d9eaaf2e3966fc0d2`  
		Last Modified: Wed, 26 Feb 2020 01:23:36 GMT  
		Size: 4.3 MB (4340193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c88bc97a5eac56e184580f940a4f029efc2a5833a63f5e3b388235eba13c2a8`  
		Last Modified: Thu, 27 Feb 2020 03:47:46 GMT  
		Size: 16.0 MB (15964515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be22d8f1978c9458f25db77f824eaf5082ba3e987122c82d9735e424cc9c1e8e`  
		Last Modified: Thu, 27 Feb 2020 03:47:42 GMT  
		Size: 2.8 KB (2774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6820dac3acd3370a5e496a503ba225f6c0f8caf82c6306193b4c6c88541abbe2`  
		Last Modified: Thu, 27 Feb 2020 03:48:04 GMT  
		Size: 20.3 MB (20311799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a207582c6a918f4bd0d3d536df15cab06b6edf4dd10c713c1bd309afe97c2ffa`  
		Last Modified: Thu, 27 Feb 2020 03:48:00 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.13` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:65f30761d5948daa71c88a80d5a1786fdb6e3ce3ccaeb08a6bf0a06444afed62
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89412813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2cd96a4d551283616c961b9bc0bb9b41dd32fafda5a87acb8477f82a22a84a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 26 Feb 2020 00:59:40 GMT
ADD file:6497e2f777f4487d9221931005a8b4b81c021442a769b581e223cf30c81ff553 in / 
# Wed, 26 Feb 2020 00:59:53 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 02:27:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 02:27:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 22:39:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 22:39:36 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 26 Feb 2020 22:40:04 GMT
ENV TELEGRAF_VERSION=1.13.4
# Wed, 26 Feb 2020 22:40:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 26 Feb 2020 22:40:11 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 26 Feb 2020 22:40:12 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 26 Feb 2020 22:40:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Feb 2020 22:40:13 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2478a2ed882cb5fbb5e4e92c9f580da9ca52f5fc78b8bb439ecbf3ac18023caa`  
		Last Modified: Wed, 26 Feb 2020 01:11:29 GMT  
		Size: 42.1 MB (42100335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c541086e0dffa72464d4077dcc60504a1c08a73ecec554c159269786ba08fed`  
		Last Modified: Wed, 26 Feb 2020 02:37:24 GMT  
		Size: 9.5 MB (9498391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf0f97b070f73118badb36d21af3459f8317d4ac6d45aec680092cc962f1c47`  
		Last Modified: Wed, 26 Feb 2020 02:37:23 GMT  
		Size: 3.9 MB (3918781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72b82e5ea1ce74c629ee54374affe651a03b088d27ce98d02cc0362c5c97ddb`  
		Last Modified: Wed, 26 Feb 2020 22:40:29 GMT  
		Size: 14.8 MB (14839243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f886a9cb8cf01cad24d98ebeb20ae5ab165501700d0d9ce52baa216e62cf7828`  
		Last Modified: Wed, 26 Feb 2020 22:40:24 GMT  
		Size: 2.8 KB (2801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1860f427099bac8326130f0978697226ebd0674622131cdb90e62c20e20604`  
		Last Modified: Wed, 26 Feb 2020 22:40:55 GMT  
		Size: 19.1 MB (19053079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7778d6135d773d5f8564f4c6e76f47318c37e1e4a2b8a867621f7830517d900`  
		Last Modified: Wed, 26 Feb 2020 22:40:49 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.13` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:7da1f6fdd88d7f22d193f147a4a66b50a81de758d4fdbb50a018033e0a936790
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91239475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5cc4ced1fcbb6d806ea116bfe7a700b8a63b43f3a5b3793970560c54ade63c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 26 Feb 2020 00:50:03 GMT
ADD file:c82c7dc82c2eb3b50218c35e1b848f707b134d2df957f57125408f69aaeb9b96 in / 
# Wed, 26 Feb 2020 00:50:15 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 03:59:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 03:59:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 23:09:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 23:09:49 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 26 Feb 2020 23:10:22 GMT
ENV TELEGRAF_VERSION=1.13.4
# Wed, 26 Feb 2020 23:10:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 26 Feb 2020 23:10:28 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 26 Feb 2020 23:10:29 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 26 Feb 2020 23:10:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Feb 2020 23:10:30 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:668c278237ef972312df4979c8fb1a927b38db5da09f094ae4fcc84a061dedf8`  
		Last Modified: Wed, 26 Feb 2020 00:58:30 GMT  
		Size: 43.2 MB (43158146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b41cac09012800692bd13a1238260bfb293c18c7864536c494809f2983ad770`  
		Last Modified: Wed, 26 Feb 2020 04:08:32 GMT  
		Size: 9.7 MB (9748511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094b353938273b0bbc576a8a80a232614ca2d9bfe48769641eee7055f3db6a5e`  
		Last Modified: Wed, 26 Feb 2020 04:08:31 GMT  
		Size: 4.1 MB (4094435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a6e84d4e14247280f0fd1fbd5a82033129b5135c2099807933ac0fac69a92a`  
		Last Modified: Wed, 26 Feb 2020 23:10:46 GMT  
		Size: 15.5 MB (15530092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a4677cafd0a8d9f616e558c61fdcea352bf03a6cb4b548e0fc1a44d8582b9c`  
		Last Modified: Wed, 26 Feb 2020 23:10:41 GMT  
		Size: 2.8 KB (2800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952b58a00ad8d9ab3e1453c25829c5d38ece278e7b1c5e0050a8a2ef52b4d604`  
		Last Modified: Wed, 26 Feb 2020 23:11:15 GMT  
		Size: 18.7 MB (18705306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4897baeb8078eeb8ac62c508927c8411ec2e32029e78112f9ae6155a9e0b7c7f`  
		Last Modified: Wed, 26 Feb 2020 23:11:09 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.13.4`

```console
$ docker pull telegraf@sha256:f703aab1f042adc5ce7bc2b6301ca904e49e01a0a30bf3d65ae881d22a4a910d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.13.4` - linux; amd64

```console
$ docker pull telegraf@sha256:614e580dc9609b5229c3ce4e06200333e9c9e40f245fabd753b61a7d9e6d13cc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.8 MB (96792682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d2b3c9f8e62b0a9eedc98271f448331a7a719b09920170ffa048776e9963c1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 26 Feb 2020 00:41:14 GMT
ADD file:08c5ab7c53526da155d6be40a9795fc08afc9f47bd333c096e90185fe9fab2b1 in / 
# Wed, 26 Feb 2020 00:41:14 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:17:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:17:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 27 Feb 2020 03:46:55 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Thu, 27 Feb 2020 03:46:58 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 03:47:22 GMT
ENV TELEGRAF_VERSION=1.13.4
# Thu, 27 Feb 2020 03:47:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 27 Feb 2020 03:47:25 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 27 Feb 2020 03:47:25 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Thu, 27 Feb 2020 03:47:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Feb 2020 03:47:25 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c0c53f743a403d45480d026864d9611d6eb898e897d60c13ae854ad453d462a4`  
		Last Modified: Wed, 26 Feb 2020 00:47:05 GMT  
		Size: 45.4 MB (45375932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66997431d390aecfd02e57222c9b5752d314a4508de82c9b43c66812c3434ed4`  
		Last Modified: Wed, 26 Feb 2020 01:23:37 GMT  
		Size: 10.8 MB (10797283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea865e2909f355d736daef9076ecda63b3075c6267b858d9eaaf2e3966fc0d2`  
		Last Modified: Wed, 26 Feb 2020 01:23:36 GMT  
		Size: 4.3 MB (4340193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c88bc97a5eac56e184580f940a4f029efc2a5833a63f5e3b388235eba13c2a8`  
		Last Modified: Thu, 27 Feb 2020 03:47:46 GMT  
		Size: 16.0 MB (15964515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be22d8f1978c9458f25db77f824eaf5082ba3e987122c82d9735e424cc9c1e8e`  
		Last Modified: Thu, 27 Feb 2020 03:47:42 GMT  
		Size: 2.8 KB (2774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6820dac3acd3370a5e496a503ba225f6c0f8caf82c6306193b4c6c88541abbe2`  
		Last Modified: Thu, 27 Feb 2020 03:48:04 GMT  
		Size: 20.3 MB (20311799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a207582c6a918f4bd0d3d536df15cab06b6edf4dd10c713c1bd309afe97c2ffa`  
		Last Modified: Thu, 27 Feb 2020 03:48:00 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.13.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:65f30761d5948daa71c88a80d5a1786fdb6e3ce3ccaeb08a6bf0a06444afed62
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89412813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2cd96a4d551283616c961b9bc0bb9b41dd32fafda5a87acb8477f82a22a84a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 26 Feb 2020 00:59:40 GMT
ADD file:6497e2f777f4487d9221931005a8b4b81c021442a769b581e223cf30c81ff553 in / 
# Wed, 26 Feb 2020 00:59:53 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 02:27:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 02:27:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 22:39:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 22:39:36 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 26 Feb 2020 22:40:04 GMT
ENV TELEGRAF_VERSION=1.13.4
# Wed, 26 Feb 2020 22:40:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 26 Feb 2020 22:40:11 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 26 Feb 2020 22:40:12 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 26 Feb 2020 22:40:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Feb 2020 22:40:13 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2478a2ed882cb5fbb5e4e92c9f580da9ca52f5fc78b8bb439ecbf3ac18023caa`  
		Last Modified: Wed, 26 Feb 2020 01:11:29 GMT  
		Size: 42.1 MB (42100335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c541086e0dffa72464d4077dcc60504a1c08a73ecec554c159269786ba08fed`  
		Last Modified: Wed, 26 Feb 2020 02:37:24 GMT  
		Size: 9.5 MB (9498391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf0f97b070f73118badb36d21af3459f8317d4ac6d45aec680092cc962f1c47`  
		Last Modified: Wed, 26 Feb 2020 02:37:23 GMT  
		Size: 3.9 MB (3918781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72b82e5ea1ce74c629ee54374affe651a03b088d27ce98d02cc0362c5c97ddb`  
		Last Modified: Wed, 26 Feb 2020 22:40:29 GMT  
		Size: 14.8 MB (14839243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f886a9cb8cf01cad24d98ebeb20ae5ab165501700d0d9ce52baa216e62cf7828`  
		Last Modified: Wed, 26 Feb 2020 22:40:24 GMT  
		Size: 2.8 KB (2801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1860f427099bac8326130f0978697226ebd0674622131cdb90e62c20e20604`  
		Last Modified: Wed, 26 Feb 2020 22:40:55 GMT  
		Size: 19.1 MB (19053079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7778d6135d773d5f8564f4c6e76f47318c37e1e4a2b8a867621f7830517d900`  
		Last Modified: Wed, 26 Feb 2020 22:40:49 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.13.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:7da1f6fdd88d7f22d193f147a4a66b50a81de758d4fdbb50a018033e0a936790
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91239475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5cc4ced1fcbb6d806ea116bfe7a700b8a63b43f3a5b3793970560c54ade63c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 26 Feb 2020 00:50:03 GMT
ADD file:c82c7dc82c2eb3b50218c35e1b848f707b134d2df957f57125408f69aaeb9b96 in / 
# Wed, 26 Feb 2020 00:50:15 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 03:59:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 03:59:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 23:09:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 23:09:49 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 26 Feb 2020 23:10:22 GMT
ENV TELEGRAF_VERSION=1.13.4
# Wed, 26 Feb 2020 23:10:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 26 Feb 2020 23:10:28 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 26 Feb 2020 23:10:29 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 26 Feb 2020 23:10:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Feb 2020 23:10:30 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:668c278237ef972312df4979c8fb1a927b38db5da09f094ae4fcc84a061dedf8`  
		Last Modified: Wed, 26 Feb 2020 00:58:30 GMT  
		Size: 43.2 MB (43158146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b41cac09012800692bd13a1238260bfb293c18c7864536c494809f2983ad770`  
		Last Modified: Wed, 26 Feb 2020 04:08:32 GMT  
		Size: 9.7 MB (9748511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094b353938273b0bbc576a8a80a232614ca2d9bfe48769641eee7055f3db6a5e`  
		Last Modified: Wed, 26 Feb 2020 04:08:31 GMT  
		Size: 4.1 MB (4094435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a6e84d4e14247280f0fd1fbd5a82033129b5135c2099807933ac0fac69a92a`  
		Last Modified: Wed, 26 Feb 2020 23:10:46 GMT  
		Size: 15.5 MB (15530092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a4677cafd0a8d9f616e558c61fdcea352bf03a6cb4b548e0fc1a44d8582b9c`  
		Last Modified: Wed, 26 Feb 2020 23:10:41 GMT  
		Size: 2.8 KB (2800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952b58a00ad8d9ab3e1453c25829c5d38ece278e7b1c5e0050a8a2ef52b4d604`  
		Last Modified: Wed, 26 Feb 2020 23:11:15 GMT  
		Size: 18.7 MB (18705306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4897baeb8078eeb8ac62c508927c8411ec2e32029e78112f9ae6155a9e0b7c7f`  
		Last Modified: Wed, 26 Feb 2020 23:11:09 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.13.4-alpine`

```console
$ docker pull telegraf@sha256:bd63e7af47b34ccfbddc9607a68e61c0186f02c74ee1fc482c31cd9c26c74ffc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.13.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:490e2976a5890ae6474fe36cb44764c81f17215396647c0ddae09b04e47a30b6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26777408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5440ed763a603d8965759563ecf59281169c67ad0640578b8bb81123e8dd1d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Jan 2020 06:15:43 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Thu, 27 Feb 2020 03:47:29 GMT
ENV TELEGRAF_VERSION=1.13.4
# Thu, 27 Feb 2020 03:47:32 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/telegraf.conf /etc/telegraf/ &&     chmod +x /usr/src/telegraf*/* &&     cp -a /usr/src/telegraf*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 27 Feb 2020 03:47:33 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 27 Feb 2020 03:47:33 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Thu, 27 Feb 2020 03:47:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Feb 2020 03:47:33 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444cfcaf178343a9f58fc894ab2f74510cab12f8a33ca82fe7fa41ef18e72b2c`  
		Last Modified: Fri, 24 Jan 2020 06:16:26 GMT  
		Size: 3.7 MB (3721327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6eb1ed95a028b91e83773b6afbead3ea7c35227247ebdbae26fbb3c13acd150`  
		Last Modified: Thu, 27 Feb 2020 03:48:12 GMT  
		Size: 20.3 MB (20291570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f14913fd99d7f8dc176036e10c9673445241818e3139d8a616f4d1ca043159`  
		Last Modified: Thu, 27 Feb 2020 03:48:08 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.13-alpine`

```console
$ docker pull telegraf@sha256:bd63e7af47b34ccfbddc9607a68e61c0186f02c74ee1fc482c31cd9c26c74ffc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.13-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:490e2976a5890ae6474fe36cb44764c81f17215396647c0ddae09b04e47a30b6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26777408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5440ed763a603d8965759563ecf59281169c67ad0640578b8bb81123e8dd1d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Jan 2020 06:15:43 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Thu, 27 Feb 2020 03:47:29 GMT
ENV TELEGRAF_VERSION=1.13.4
# Thu, 27 Feb 2020 03:47:32 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/telegraf.conf /etc/telegraf/ &&     chmod +x /usr/src/telegraf*/* &&     cp -a /usr/src/telegraf*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 27 Feb 2020 03:47:33 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 27 Feb 2020 03:47:33 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Thu, 27 Feb 2020 03:47:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Feb 2020 03:47:33 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444cfcaf178343a9f58fc894ab2f74510cab12f8a33ca82fe7fa41ef18e72b2c`  
		Last Modified: Fri, 24 Jan 2020 06:16:26 GMT  
		Size: 3.7 MB (3721327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6eb1ed95a028b91e83773b6afbead3ea7c35227247ebdbae26fbb3c13acd150`  
		Last Modified: Thu, 27 Feb 2020 03:48:12 GMT  
		Size: 20.3 MB (20291570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f14913fd99d7f8dc176036e10c9673445241818e3139d8a616f4d1ca043159`  
		Last Modified: Thu, 27 Feb 2020 03:48:08 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:bd63e7af47b34ccfbddc9607a68e61c0186f02c74ee1fc482c31cd9c26c74ffc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:490e2976a5890ae6474fe36cb44764c81f17215396647c0ddae09b04e47a30b6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26777408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5440ed763a603d8965759563ecf59281169c67ad0640578b8bb81123e8dd1d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Jan 2020 06:15:43 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Thu, 27 Feb 2020 03:47:29 GMT
ENV TELEGRAF_VERSION=1.13.4
# Thu, 27 Feb 2020 03:47:32 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/telegraf.conf /etc/telegraf/ &&     chmod +x /usr/src/telegraf*/* &&     cp -a /usr/src/telegraf*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 27 Feb 2020 03:47:33 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 27 Feb 2020 03:47:33 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Thu, 27 Feb 2020 03:47:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Feb 2020 03:47:33 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444cfcaf178343a9f58fc894ab2f74510cab12f8a33ca82fe7fa41ef18e72b2c`  
		Last Modified: Fri, 24 Jan 2020 06:16:26 GMT  
		Size: 3.7 MB (3721327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6eb1ed95a028b91e83773b6afbead3ea7c35227247ebdbae26fbb3c13acd150`  
		Last Modified: Thu, 27 Feb 2020 03:48:12 GMT  
		Size: 20.3 MB (20291570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f14913fd99d7f8dc176036e10c9673445241818e3139d8a616f4d1ca043159`  
		Last Modified: Thu, 27 Feb 2020 03:48:08 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:f703aab1f042adc5ce7bc2b6301ca904e49e01a0a30bf3d65ae881d22a4a910d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:614e580dc9609b5229c3ce4e06200333e9c9e40f245fabd753b61a7d9e6d13cc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.8 MB (96792682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d2b3c9f8e62b0a9eedc98271f448331a7a719b09920170ffa048776e9963c1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 26 Feb 2020 00:41:14 GMT
ADD file:08c5ab7c53526da155d6be40a9795fc08afc9f47bd333c096e90185fe9fab2b1 in / 
# Wed, 26 Feb 2020 00:41:14 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:17:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:17:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 27 Feb 2020 03:46:55 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Thu, 27 Feb 2020 03:46:58 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 03:47:22 GMT
ENV TELEGRAF_VERSION=1.13.4
# Thu, 27 Feb 2020 03:47:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 27 Feb 2020 03:47:25 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 27 Feb 2020 03:47:25 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Thu, 27 Feb 2020 03:47:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Feb 2020 03:47:25 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c0c53f743a403d45480d026864d9611d6eb898e897d60c13ae854ad453d462a4`  
		Last Modified: Wed, 26 Feb 2020 00:47:05 GMT  
		Size: 45.4 MB (45375932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66997431d390aecfd02e57222c9b5752d314a4508de82c9b43c66812c3434ed4`  
		Last Modified: Wed, 26 Feb 2020 01:23:37 GMT  
		Size: 10.8 MB (10797283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea865e2909f355d736daef9076ecda63b3075c6267b858d9eaaf2e3966fc0d2`  
		Last Modified: Wed, 26 Feb 2020 01:23:36 GMT  
		Size: 4.3 MB (4340193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c88bc97a5eac56e184580f940a4f029efc2a5833a63f5e3b388235eba13c2a8`  
		Last Modified: Thu, 27 Feb 2020 03:47:46 GMT  
		Size: 16.0 MB (15964515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be22d8f1978c9458f25db77f824eaf5082ba3e987122c82d9735e424cc9c1e8e`  
		Last Modified: Thu, 27 Feb 2020 03:47:42 GMT  
		Size: 2.8 KB (2774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6820dac3acd3370a5e496a503ba225f6c0f8caf82c6306193b4c6c88541abbe2`  
		Last Modified: Thu, 27 Feb 2020 03:48:04 GMT  
		Size: 20.3 MB (20311799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a207582c6a918f4bd0d3d536df15cab06b6edf4dd10c713c1bd309afe97c2ffa`  
		Last Modified: Thu, 27 Feb 2020 03:48:00 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:65f30761d5948daa71c88a80d5a1786fdb6e3ce3ccaeb08a6bf0a06444afed62
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89412813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2cd96a4d551283616c961b9bc0bb9b41dd32fafda5a87acb8477f82a22a84a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 26 Feb 2020 00:59:40 GMT
ADD file:6497e2f777f4487d9221931005a8b4b81c021442a769b581e223cf30c81ff553 in / 
# Wed, 26 Feb 2020 00:59:53 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 02:27:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 02:27:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 22:39:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 22:39:36 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 26 Feb 2020 22:40:04 GMT
ENV TELEGRAF_VERSION=1.13.4
# Wed, 26 Feb 2020 22:40:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 26 Feb 2020 22:40:11 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 26 Feb 2020 22:40:12 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 26 Feb 2020 22:40:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Feb 2020 22:40:13 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2478a2ed882cb5fbb5e4e92c9f580da9ca52f5fc78b8bb439ecbf3ac18023caa`  
		Last Modified: Wed, 26 Feb 2020 01:11:29 GMT  
		Size: 42.1 MB (42100335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c541086e0dffa72464d4077dcc60504a1c08a73ecec554c159269786ba08fed`  
		Last Modified: Wed, 26 Feb 2020 02:37:24 GMT  
		Size: 9.5 MB (9498391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf0f97b070f73118badb36d21af3459f8317d4ac6d45aec680092cc962f1c47`  
		Last Modified: Wed, 26 Feb 2020 02:37:23 GMT  
		Size: 3.9 MB (3918781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72b82e5ea1ce74c629ee54374affe651a03b088d27ce98d02cc0362c5c97ddb`  
		Last Modified: Wed, 26 Feb 2020 22:40:29 GMT  
		Size: 14.8 MB (14839243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f886a9cb8cf01cad24d98ebeb20ae5ab165501700d0d9ce52baa216e62cf7828`  
		Last Modified: Wed, 26 Feb 2020 22:40:24 GMT  
		Size: 2.8 KB (2801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1860f427099bac8326130f0978697226ebd0674622131cdb90e62c20e20604`  
		Last Modified: Wed, 26 Feb 2020 22:40:55 GMT  
		Size: 19.1 MB (19053079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7778d6135d773d5f8564f4c6e76f47318c37e1e4a2b8a867621f7830517d900`  
		Last Modified: Wed, 26 Feb 2020 22:40:49 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:7da1f6fdd88d7f22d193f147a4a66b50a81de758d4fdbb50a018033e0a936790
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91239475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5cc4ced1fcbb6d806ea116bfe7a700b8a63b43f3a5b3793970560c54ade63c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 26 Feb 2020 00:50:03 GMT
ADD file:c82c7dc82c2eb3b50218c35e1b848f707b134d2df957f57125408f69aaeb9b96 in / 
# Wed, 26 Feb 2020 00:50:15 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 03:59:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 03:59:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 23:09:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 23:09:49 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 26 Feb 2020 23:10:22 GMT
ENV TELEGRAF_VERSION=1.13.4
# Wed, 26 Feb 2020 23:10:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 26 Feb 2020 23:10:28 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 26 Feb 2020 23:10:29 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 26 Feb 2020 23:10:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Feb 2020 23:10:30 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:668c278237ef972312df4979c8fb1a927b38db5da09f094ae4fcc84a061dedf8`  
		Last Modified: Wed, 26 Feb 2020 00:58:30 GMT  
		Size: 43.2 MB (43158146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b41cac09012800692bd13a1238260bfb293c18c7864536c494809f2983ad770`  
		Last Modified: Wed, 26 Feb 2020 04:08:32 GMT  
		Size: 9.7 MB (9748511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094b353938273b0bbc576a8a80a232614ca2d9bfe48769641eee7055f3db6a5e`  
		Last Modified: Wed, 26 Feb 2020 04:08:31 GMT  
		Size: 4.1 MB (4094435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a6e84d4e14247280f0fd1fbd5a82033129b5135c2099807933ac0fac69a92a`  
		Last Modified: Wed, 26 Feb 2020 23:10:46 GMT  
		Size: 15.5 MB (15530092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a4677cafd0a8d9f616e558c61fdcea352bf03a6cb4b548e0fc1a44d8582b9c`  
		Last Modified: Wed, 26 Feb 2020 23:10:41 GMT  
		Size: 2.8 KB (2800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952b58a00ad8d9ab3e1453c25829c5d38ece278e7b1c5e0050a8a2ef52b4d604`  
		Last Modified: Wed, 26 Feb 2020 23:11:15 GMT  
		Size: 18.7 MB (18705306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4897baeb8078eeb8ac62c508927c8411ec2e32029e78112f9ae6155a9e0b7c7f`  
		Last Modified: Wed, 26 Feb 2020 23:11:09 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
