<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.18`](#telegraf118)
-	[`telegraf:1.18-alpine`](#telegraf118-alpine)
-	[`telegraf:1.18.3`](#telegraf1183)
-	[`telegraf:1.18.3-alpine`](#telegraf1183-alpine)
-	[`telegraf:1.19`](#telegraf119)
-	[`telegraf:1.19-alpine`](#telegraf119-alpine)
-	[`telegraf:1.19.3`](#telegraf1193)
-	[`telegraf:1.19.3-alpine`](#telegraf1193-alpine)
-	[`telegraf:1.20`](#telegraf120)
-	[`telegraf:1.20-alpine`](#telegraf120-alpine)
-	[`telegraf:1.20.3`](#telegraf1203)
-	[`telegraf:1.20.3-alpine`](#telegraf1203-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.18`

```console
$ docker pull telegraf@sha256:57ad25f6a0fbd6cf80120c6c0901da0a58635c4096f40c968e4e3fb67218479a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.18` - linux; amd64

```console
$ docker pull telegraf@sha256:44213547012e7a3e9672d108ed686363ac7c9a0ecfe0726afa94567d0f17c116
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115493967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62279e4f127449aaa8fe76e3781e914fca4eec180edf60e890449fcfeb654986`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Oct 2021 01:20:53 GMT
ADD file:98c256057b79b141aea9a806a4538cf6c3f340d7e3b0d6e8c363699333f3406b in / 
# Tue, 12 Oct 2021 01:20:53 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:44:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 15:44:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Oct 2021 10:25:38 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 10:25:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 13 Oct 2021 10:25:46 GMT
ENV TELEGRAF_VERSION=1.18.3
# Wed, 13 Oct 2021 10:26:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 13 Oct 2021 10:26:08 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 03 Nov 2021 19:44:00 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Wed, 03 Nov 2021 19:44:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Nov 2021 19:44:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:07471e81507f7cf1100827f10c60c3c0422d1222430e34e527d97ec72b14a193`  
		Last Modified: Tue, 12 Oct 2021 01:26:26 GMT  
		Size: 50.4 MB (50436692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6cef1aa2170c001b320769bf8b018ed82d2c94a673e3010ea1ffe152e107419`  
		Last Modified: Tue, 12 Oct 2021 15:54:16 GMT  
		Size: 7.8 MB (7833862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a51f13be8e69cfc526b671d0bbf621b985b0932acd1523050e2995777b5926`  
		Last Modified: Tue, 12 Oct 2021 15:54:17 GMT  
		Size: 10.0 MB (9997204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91a466291d423e3faad6a8be6ae82e4a4d0550acb67989ac71c98f900e74d41`  
		Last Modified: Wed, 13 Oct 2021 10:26:55 GMT  
		Size: 17.4 MB (17415387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77934da0dce5bef46b239a3871787c2962a08cf1c8b1e629282f0c617b46426`  
		Last Modified: Wed, 13 Oct 2021 10:26:52 GMT  
		Size: 2.9 KB (2906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3dc5b173c6a2c70c8525fe530dc15fba03195a14a25a922d13d3a4907d3bb79`  
		Last Modified: Wed, 13 Oct 2021 10:26:58 GMT  
		Size: 29.8 MB (29807686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0d24a34134ee88961300aafa7bb159a5a6aa430b16c7f286cad2dbed31c531`  
		Last Modified: Wed, 03 Nov 2021 19:45:11 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.18` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:fb197fd325f2dfa4092fbb85cbdc103e5bb39f8c385492f27aaa1fbc38b6758a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.1 MB (106106557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b12441c1e85b0c520dd0d0ecf3affddbe71afb0cd0a340670e06835d79dc1e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Oct 2021 01:29:06 GMT
ADD file:b1857dc4fe4fbc4af220829cc6af7169c4555d3f63a3a304db6fa0146b1d5539 in / 
# Tue, 12 Oct 2021 01:29:08 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 18:39:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 18:39:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Oct 2021 15:31:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 15:31:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 13 Oct 2021 15:31:08 GMT
ENV TELEGRAF_VERSION=1.18.3
# Wed, 13 Oct 2021 15:31:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 13 Oct 2021 15:31:19 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 03 Nov 2021 19:51:25 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Wed, 03 Nov 2021 19:51:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Nov 2021 19:51:25 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:139a906e9407e96c50669130c30fe8fba2681b14aa838a3e52f8753b566ef1c8`  
		Last Modified: Tue, 12 Oct 2021 01:45:13 GMT  
		Size: 45.9 MB (45917899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3907051e2154d5bd4ad15141b8938bc09674039787512494a99b93fd4ebc088d`  
		Last Modified: Tue, 12 Oct 2021 19:00:49 GMT  
		Size: 7.1 MB (7125242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8651d4793d5f4d465002213d2d462c964aaf8665a87d5f9cc0de7384f10eeb10`  
		Last Modified: Tue, 12 Oct 2021 19:00:49 GMT  
		Size: 9.3 MB (9343819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e659684a04aace7b984a69bccde2a720cb53304f8905d65b9068605177b2a4b6`  
		Last Modified: Wed, 13 Oct 2021 15:33:06 GMT  
		Size: 16.2 MB (16161376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc86d346babddcb58c40b9188fc289d120a16518eed1782662459497e55f179`  
		Last Modified: Wed, 13 Oct 2021 15:32:54 GMT  
		Size: 2.9 KB (2905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9e892c3ebef241bd086d8580d87fe9e607dcddc9648567b441ee73ee6c8ec9`  
		Last Modified: Wed, 13 Oct 2021 15:33:13 GMT  
		Size: 27.6 MB (27555085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd675778b8ee5eb6339575dbbd2be62cb621719964333cf5372fd498eb10dae3`  
		Last Modified: Wed, 03 Nov 2021 19:52:33 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.18` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:aeab86e3c491d7715fd64aab1ad49afb6e6a2a026ce4516daa0a5cb574cf0aec
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110720532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b29ac4e935dd9c53901da67719ffd8704e692afa99b46725da57cbfe17917a3a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:27 GMT
ADD file:c7e9e884b1494f96e33e9d9a892b51367af8943edb282c4101cc99ea78a7753f in / 
# Wed, 17 Nov 2021 02:40:28 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 13:28:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 13:28:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 20:42:06 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 20:42:09 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 17 Nov 2021 20:42:09 GMT
ENV TELEGRAF_VERSION=1.18.3
# Wed, 17 Nov 2021 20:42:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 17 Nov 2021 20:42:14 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 17 Nov 2021 20:42:16 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Wed, 17 Nov 2021 20:42:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Nov 2021 20:42:17 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:626979e62c56e192812e818d52b82f063d9f9514b1b7bae14e534e4a7c98117a`  
		Last Modified: Wed, 17 Nov 2021 02:47:40 GMT  
		Size: 49.2 MB (49222990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134a528370d5dcbf5b6ba2d8c20f576504448e8f2d1debb5d2a4950a38a3ff2d`  
		Last Modified: Wed, 17 Nov 2021 13:37:44 GMT  
		Size: 7.7 MB (7695161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e12e3364b52ad043d8e79f750863ed4ca2878c4fdf45ded974508febc55fdd`  
		Last Modified: Wed, 17 Nov 2021 13:37:44 GMT  
		Size: 9.8 MB (9767133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be62c7c66899dfefa611452ca6b38510228e4e1661d1ec078d90733f59865bcb`  
		Last Modified: Wed, 17 Nov 2021 20:43:17 GMT  
		Size: 17.1 MB (17059007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ea9240a1fea313b800d353f9288154cce52bcb21b3cfabfc7bf0f861090de7`  
		Last Modified: Wed, 17 Nov 2021 20:43:14 GMT  
		Size: 2.9 KB (2875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0fb281bd28751a405ca94a5c5833bfeb1e064273d98cdea2fe33d46357306e`  
		Last Modified: Wed, 17 Nov 2021 20:43:20 GMT  
		Size: 27.0 MB (26973134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af547a1dd71283c2176bbeebcb1b624d9fd04aac867632b7ff44a26f383a1f69`  
		Last Modified: Wed, 17 Nov 2021 20:43:14 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.18-alpine`

```console
$ docker pull telegraf@sha256:6aa02585a82331defaba9fa2d482579de674adda7a608a3f4a449089fd03c22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:1.18-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:7036acf1cb6af49f02c4109ce8bb3a5938a17a9563ba3bd2ac8805ff7590e37c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 MB (35862269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b2815ff14c8ac1315ff16b32175e996f8f78d14d9e50860c8830372a871e52`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Nov 2021 07:20:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec &&     update-ca-certificates
# Sat, 13 Nov 2021 07:20:28 GMT
ENV TELEGRAF_VERSION=1.18.3
# Sat, 13 Nov 2021 07:20:43 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 13 Nov 2021 07:20:44 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 13 Nov 2021 07:20:44 GMT
COPY file:4071aa7d94da140b944f5aaf032330509821a974e13349f4a3682e3368362128 in /entrypoint.sh 
# Sat, 13 Nov 2021 07:20:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 13 Nov 2021 07:20:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc79f199b43e46c5dfea12dfa8b92b7811e74b4d3812ff99c8368e4d2af803e7`  
		Last Modified: Fri, 12 Nov 2021 21:56:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ae06dab0a6b50d3f23d332a8c326fd227bd58abc651b7033038337f97e077f`  
		Last Modified: Sat, 13 Nov 2021 07:21:57 GMT  
		Size: 3.4 MB (3371612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4b4cb0834236816551000b761fd652c542d20937310c681a0bd1a8c9e0c82c`  
		Last Modified: Sat, 13 Nov 2021 07:22:03 GMT  
		Size: 29.7 MB (29667313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ef8c5df072c949c20c7b8fc003a502452dce57577a3c495f513cf155ad4357`  
		Last Modified: Sat, 13 Nov 2021 07:21:56 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.18.3`

```console
$ docker pull telegraf@sha256:57ad25f6a0fbd6cf80120c6c0901da0a58635c4096f40c968e4e3fb67218479a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.18.3` - linux; amd64

```console
$ docker pull telegraf@sha256:44213547012e7a3e9672d108ed686363ac7c9a0ecfe0726afa94567d0f17c116
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115493967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62279e4f127449aaa8fe76e3781e914fca4eec180edf60e890449fcfeb654986`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Oct 2021 01:20:53 GMT
ADD file:98c256057b79b141aea9a806a4538cf6c3f340d7e3b0d6e8c363699333f3406b in / 
# Tue, 12 Oct 2021 01:20:53 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:44:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 15:44:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Oct 2021 10:25:38 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 10:25:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 13 Oct 2021 10:25:46 GMT
ENV TELEGRAF_VERSION=1.18.3
# Wed, 13 Oct 2021 10:26:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 13 Oct 2021 10:26:08 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 03 Nov 2021 19:44:00 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Wed, 03 Nov 2021 19:44:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Nov 2021 19:44:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:07471e81507f7cf1100827f10c60c3c0422d1222430e34e527d97ec72b14a193`  
		Last Modified: Tue, 12 Oct 2021 01:26:26 GMT  
		Size: 50.4 MB (50436692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6cef1aa2170c001b320769bf8b018ed82d2c94a673e3010ea1ffe152e107419`  
		Last Modified: Tue, 12 Oct 2021 15:54:16 GMT  
		Size: 7.8 MB (7833862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a51f13be8e69cfc526b671d0bbf621b985b0932acd1523050e2995777b5926`  
		Last Modified: Tue, 12 Oct 2021 15:54:17 GMT  
		Size: 10.0 MB (9997204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91a466291d423e3faad6a8be6ae82e4a4d0550acb67989ac71c98f900e74d41`  
		Last Modified: Wed, 13 Oct 2021 10:26:55 GMT  
		Size: 17.4 MB (17415387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77934da0dce5bef46b239a3871787c2962a08cf1c8b1e629282f0c617b46426`  
		Last Modified: Wed, 13 Oct 2021 10:26:52 GMT  
		Size: 2.9 KB (2906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3dc5b173c6a2c70c8525fe530dc15fba03195a14a25a922d13d3a4907d3bb79`  
		Last Modified: Wed, 13 Oct 2021 10:26:58 GMT  
		Size: 29.8 MB (29807686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0d24a34134ee88961300aafa7bb159a5a6aa430b16c7f286cad2dbed31c531`  
		Last Modified: Wed, 03 Nov 2021 19:45:11 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.18.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:fb197fd325f2dfa4092fbb85cbdc103e5bb39f8c385492f27aaa1fbc38b6758a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.1 MB (106106557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b12441c1e85b0c520dd0d0ecf3affddbe71afb0cd0a340670e06835d79dc1e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Oct 2021 01:29:06 GMT
ADD file:b1857dc4fe4fbc4af220829cc6af7169c4555d3f63a3a304db6fa0146b1d5539 in / 
# Tue, 12 Oct 2021 01:29:08 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 18:39:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 18:39:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Oct 2021 15:31:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 15:31:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 13 Oct 2021 15:31:08 GMT
ENV TELEGRAF_VERSION=1.18.3
# Wed, 13 Oct 2021 15:31:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 13 Oct 2021 15:31:19 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 03 Nov 2021 19:51:25 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Wed, 03 Nov 2021 19:51:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Nov 2021 19:51:25 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:139a906e9407e96c50669130c30fe8fba2681b14aa838a3e52f8753b566ef1c8`  
		Last Modified: Tue, 12 Oct 2021 01:45:13 GMT  
		Size: 45.9 MB (45917899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3907051e2154d5bd4ad15141b8938bc09674039787512494a99b93fd4ebc088d`  
		Last Modified: Tue, 12 Oct 2021 19:00:49 GMT  
		Size: 7.1 MB (7125242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8651d4793d5f4d465002213d2d462c964aaf8665a87d5f9cc0de7384f10eeb10`  
		Last Modified: Tue, 12 Oct 2021 19:00:49 GMT  
		Size: 9.3 MB (9343819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e659684a04aace7b984a69bccde2a720cb53304f8905d65b9068605177b2a4b6`  
		Last Modified: Wed, 13 Oct 2021 15:33:06 GMT  
		Size: 16.2 MB (16161376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc86d346babddcb58c40b9188fc289d120a16518eed1782662459497e55f179`  
		Last Modified: Wed, 13 Oct 2021 15:32:54 GMT  
		Size: 2.9 KB (2905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9e892c3ebef241bd086d8580d87fe9e607dcddc9648567b441ee73ee6c8ec9`  
		Last Modified: Wed, 13 Oct 2021 15:33:13 GMT  
		Size: 27.6 MB (27555085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd675778b8ee5eb6339575dbbd2be62cb621719964333cf5372fd498eb10dae3`  
		Last Modified: Wed, 03 Nov 2021 19:52:33 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.18.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:aeab86e3c491d7715fd64aab1ad49afb6e6a2a026ce4516daa0a5cb574cf0aec
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110720532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b29ac4e935dd9c53901da67719ffd8704e692afa99b46725da57cbfe17917a3a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:27 GMT
ADD file:c7e9e884b1494f96e33e9d9a892b51367af8943edb282c4101cc99ea78a7753f in / 
# Wed, 17 Nov 2021 02:40:28 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 13:28:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 13:28:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 20:42:06 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 20:42:09 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 17 Nov 2021 20:42:09 GMT
ENV TELEGRAF_VERSION=1.18.3
# Wed, 17 Nov 2021 20:42:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 17 Nov 2021 20:42:14 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 17 Nov 2021 20:42:16 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Wed, 17 Nov 2021 20:42:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Nov 2021 20:42:17 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:626979e62c56e192812e818d52b82f063d9f9514b1b7bae14e534e4a7c98117a`  
		Last Modified: Wed, 17 Nov 2021 02:47:40 GMT  
		Size: 49.2 MB (49222990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134a528370d5dcbf5b6ba2d8c20f576504448e8f2d1debb5d2a4950a38a3ff2d`  
		Last Modified: Wed, 17 Nov 2021 13:37:44 GMT  
		Size: 7.7 MB (7695161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e12e3364b52ad043d8e79f750863ed4ca2878c4fdf45ded974508febc55fdd`  
		Last Modified: Wed, 17 Nov 2021 13:37:44 GMT  
		Size: 9.8 MB (9767133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be62c7c66899dfefa611452ca6b38510228e4e1661d1ec078d90733f59865bcb`  
		Last Modified: Wed, 17 Nov 2021 20:43:17 GMT  
		Size: 17.1 MB (17059007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ea9240a1fea313b800d353f9288154cce52bcb21b3cfabfc7bf0f861090de7`  
		Last Modified: Wed, 17 Nov 2021 20:43:14 GMT  
		Size: 2.9 KB (2875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0fb281bd28751a405ca94a5c5833bfeb1e064273d98cdea2fe33d46357306e`  
		Last Modified: Wed, 17 Nov 2021 20:43:20 GMT  
		Size: 27.0 MB (26973134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af547a1dd71283c2176bbeebcb1b624d9fd04aac867632b7ff44a26f383a1f69`  
		Last Modified: Wed, 17 Nov 2021 20:43:14 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.18.3-alpine`

```console
$ docker pull telegraf@sha256:6aa02585a82331defaba9fa2d482579de674adda7a608a3f4a449089fd03c22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:1.18.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:7036acf1cb6af49f02c4109ce8bb3a5938a17a9563ba3bd2ac8805ff7590e37c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 MB (35862269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b2815ff14c8ac1315ff16b32175e996f8f78d14d9e50860c8830372a871e52`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Nov 2021 07:20:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec &&     update-ca-certificates
# Sat, 13 Nov 2021 07:20:28 GMT
ENV TELEGRAF_VERSION=1.18.3
# Sat, 13 Nov 2021 07:20:43 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 13 Nov 2021 07:20:44 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 13 Nov 2021 07:20:44 GMT
COPY file:4071aa7d94da140b944f5aaf032330509821a974e13349f4a3682e3368362128 in /entrypoint.sh 
# Sat, 13 Nov 2021 07:20:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 13 Nov 2021 07:20:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc79f199b43e46c5dfea12dfa8b92b7811e74b4d3812ff99c8368e4d2af803e7`  
		Last Modified: Fri, 12 Nov 2021 21:56:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ae06dab0a6b50d3f23d332a8c326fd227bd58abc651b7033038337f97e077f`  
		Last Modified: Sat, 13 Nov 2021 07:21:57 GMT  
		Size: 3.4 MB (3371612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4b4cb0834236816551000b761fd652c542d20937310c681a0bd1a8c9e0c82c`  
		Last Modified: Sat, 13 Nov 2021 07:22:03 GMT  
		Size: 29.7 MB (29667313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ef8c5df072c949c20c7b8fc003a502452dce57577a3c495f513cf155ad4357`  
		Last Modified: Sat, 13 Nov 2021 07:21:56 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.19`

```console
$ docker pull telegraf@sha256:80bf00afc51f273b989d1d46e2b0ab5bb98503ec67e14268c785e90e9d570bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.19` - linux; amd64

```console
$ docker pull telegraf@sha256:0af14261f48e251040ac25922c02c4aa89693a7a28f1008e5795533d5fe1a821
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.9 MB (119874115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a02b7a8847f7c592ef4f2193784a8cf0b5349246299ba00440c1983f1341d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Oct 2021 01:20:53 GMT
ADD file:98c256057b79b141aea9a806a4538cf6c3f340d7e3b0d6e8c363699333f3406b in / 
# Tue, 12 Oct 2021 01:20:53 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:44:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 15:44:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Oct 2021 10:25:38 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 10:25:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 13 Oct 2021 10:26:13 GMT
ENV TELEGRAF_VERSION=1.19.3
# Wed, 13 Oct 2021 10:26:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 13 Oct 2021 10:26:19 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 03 Nov 2021 19:44:22 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Wed, 03 Nov 2021 19:44:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Nov 2021 19:44:23 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:07471e81507f7cf1100827f10c60c3c0422d1222430e34e527d97ec72b14a193`  
		Last Modified: Tue, 12 Oct 2021 01:26:26 GMT  
		Size: 50.4 MB (50436692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6cef1aa2170c001b320769bf8b018ed82d2c94a673e3010ea1ffe152e107419`  
		Last Modified: Tue, 12 Oct 2021 15:54:16 GMT  
		Size: 7.8 MB (7833862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a51f13be8e69cfc526b671d0bbf621b985b0932acd1523050e2995777b5926`  
		Last Modified: Tue, 12 Oct 2021 15:54:17 GMT  
		Size: 10.0 MB (9997204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91a466291d423e3faad6a8be6ae82e4a4d0550acb67989ac71c98f900e74d41`  
		Last Modified: Wed, 13 Oct 2021 10:26:55 GMT  
		Size: 17.4 MB (17415387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77934da0dce5bef46b239a3871787c2962a08cf1c8b1e629282f0c617b46426`  
		Last Modified: Wed, 13 Oct 2021 10:26:52 GMT  
		Size: 2.9 KB (2906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740ee4b64760022ecef81a94e508ebef6be4908cf720ddf4638226c3a4e18f01`  
		Last Modified: Wed, 13 Oct 2021 10:27:15 GMT  
		Size: 34.2 MB (34187833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017df2efa91fcb8917ec99f6f28405d5693a4c3a58509ad79e47a0598dce1443`  
		Last Modified: Wed, 03 Nov 2021 19:45:41 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.19` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:f025d777fd600f1763f219c31ae3d2acfa76505ccc3e6398ecabbaef1c169c5a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110246039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a310c800f2799c9b5029c3e85c3af7411a8a7dd1f9d630ee6cfe1591b90f09a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Oct 2021 01:29:06 GMT
ADD file:b1857dc4fe4fbc4af220829cc6af7169c4555d3f63a3a304db6fa0146b1d5539 in / 
# Tue, 12 Oct 2021 01:29:08 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 18:39:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 18:39:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Oct 2021 15:31:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 15:31:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 13 Oct 2021 15:31:32 GMT
ENV TELEGRAF_VERSION=1.19.3
# Wed, 13 Oct 2021 15:31:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 13 Oct 2021 15:31:44 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 03 Nov 2021 19:51:37 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Wed, 03 Nov 2021 19:51:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Nov 2021 19:51:38 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:139a906e9407e96c50669130c30fe8fba2681b14aa838a3e52f8753b566ef1c8`  
		Last Modified: Tue, 12 Oct 2021 01:45:13 GMT  
		Size: 45.9 MB (45917899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3907051e2154d5bd4ad15141b8938bc09674039787512494a99b93fd4ebc088d`  
		Last Modified: Tue, 12 Oct 2021 19:00:49 GMT  
		Size: 7.1 MB (7125242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8651d4793d5f4d465002213d2d462c964aaf8665a87d5f9cc0de7384f10eeb10`  
		Last Modified: Tue, 12 Oct 2021 19:00:49 GMT  
		Size: 9.3 MB (9343819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e659684a04aace7b984a69bccde2a720cb53304f8905d65b9068605177b2a4b6`  
		Last Modified: Wed, 13 Oct 2021 15:33:06 GMT  
		Size: 16.2 MB (16161376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc86d346babddcb58c40b9188fc289d120a16518eed1782662459497e55f179`  
		Last Modified: Wed, 13 Oct 2021 15:32:54 GMT  
		Size: 2.9 KB (2905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f9213a7b1180f7eb074ebc32c7adc9824c55705bacd59a5e64ceacc7720b3b`  
		Last Modified: Wed, 13 Oct 2021 15:33:47 GMT  
		Size: 31.7 MB (31694568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9989f04451b58ce865558163f9caaa26bafe2c7bb4a8dd0878fe1e27bb708f1b`  
		Last Modified: Wed, 03 Nov 2021 19:52:45 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.19` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6e4d11665765a9162f3e9af94e89ae8beeb2b581384a23bc72fbb2e17456738c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114713909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a957c2c51d6eca1bd0a378dbddcaac651fcbffaa49eaeec64ffa48f551bd7e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:27 GMT
ADD file:c7e9e884b1494f96e33e9d9a892b51367af8943edb282c4101cc99ea78a7753f in / 
# Wed, 17 Nov 2021 02:40:28 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 13:28:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 13:28:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 20:42:06 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 20:42:09 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 17 Nov 2021 20:42:24 GMT
ENV TELEGRAF_VERSION=1.19.3
# Wed, 17 Nov 2021 20:42:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 17 Nov 2021 20:42:30 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 17 Nov 2021 20:42:31 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Wed, 17 Nov 2021 20:42:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Nov 2021 20:42:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:626979e62c56e192812e818d52b82f063d9f9514b1b7bae14e534e4a7c98117a`  
		Last Modified: Wed, 17 Nov 2021 02:47:40 GMT  
		Size: 49.2 MB (49222990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134a528370d5dcbf5b6ba2d8c20f576504448e8f2d1debb5d2a4950a38a3ff2d`  
		Last Modified: Wed, 17 Nov 2021 13:37:44 GMT  
		Size: 7.7 MB (7695161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e12e3364b52ad043d8e79f750863ed4ca2878c4fdf45ded974508febc55fdd`  
		Last Modified: Wed, 17 Nov 2021 13:37:44 GMT  
		Size: 9.8 MB (9767133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be62c7c66899dfefa611452ca6b38510228e4e1661d1ec078d90733f59865bcb`  
		Last Modified: Wed, 17 Nov 2021 20:43:17 GMT  
		Size: 17.1 MB (17059007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ea9240a1fea313b800d353f9288154cce52bcb21b3cfabfc7bf0f861090de7`  
		Last Modified: Wed, 17 Nov 2021 20:43:14 GMT  
		Size: 2.9 KB (2875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb4fa8ccc7f74251b0b5e98750230eeac799bcfb5de5d01baf66fa5bf650699`  
		Last Modified: Wed, 17 Nov 2021 20:43:36 GMT  
		Size: 31.0 MB (30966512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9006db8c7aee266f0d94bd9643267132f4633a6434f7ad31d02cffd459cc659`  
		Last Modified: Wed, 17 Nov 2021 20:43:30 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.19-alpine`

```console
$ docker pull telegraf@sha256:9e391c4169ccb91b1001061dae70fac58ab82165f4079e7ec039e9d84a4b5ca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:1.19-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:627ea1f7f074a431873307fdba4c402fd567078bcc892dd9db37c5b26628f8c0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40241320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b97513bb4d721e5e1acbe529575e7db4451fc351934ce3ddee001d8183371b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Nov 2021 07:20:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec &&     update-ca-certificates
# Sat, 13 Nov 2021 07:20:51 GMT
ENV TELEGRAF_VERSION=1.19.3
# Sat, 13 Nov 2021 07:21:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 13 Nov 2021 07:21:05 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 13 Nov 2021 07:21:05 GMT
COPY file:4071aa7d94da140b944f5aaf032330509821a974e13349f4a3682e3368362128 in /entrypoint.sh 
# Sat, 13 Nov 2021 07:21:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 13 Nov 2021 07:21:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc79f199b43e46c5dfea12dfa8b92b7811e74b4d3812ff99c8368e4d2af803e7`  
		Last Modified: Fri, 12 Nov 2021 21:56:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ae06dab0a6b50d3f23d332a8c326fd227bd58abc651b7033038337f97e077f`  
		Last Modified: Sat, 13 Nov 2021 07:21:57 GMT  
		Size: 3.4 MB (3371612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269b03bad908f1f612f0e6e5f1618e234a49ac3fcf23cd4f579ae4e09117ac49`  
		Last Modified: Sat, 13 Nov 2021 07:22:22 GMT  
		Size: 34.0 MB (34046365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63e1ff47e2021e70246af4383776e6845936e12e0337f4540c023f664bbe5bd`  
		Last Modified: Sat, 13 Nov 2021 07:22:14 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.19.3`

```console
$ docker pull telegraf@sha256:80bf00afc51f273b989d1d46e2b0ab5bb98503ec67e14268c785e90e9d570bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.19.3` - linux; amd64

```console
$ docker pull telegraf@sha256:0af14261f48e251040ac25922c02c4aa89693a7a28f1008e5795533d5fe1a821
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.9 MB (119874115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a02b7a8847f7c592ef4f2193784a8cf0b5349246299ba00440c1983f1341d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Oct 2021 01:20:53 GMT
ADD file:98c256057b79b141aea9a806a4538cf6c3f340d7e3b0d6e8c363699333f3406b in / 
# Tue, 12 Oct 2021 01:20:53 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:44:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 15:44:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Oct 2021 10:25:38 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 10:25:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 13 Oct 2021 10:26:13 GMT
ENV TELEGRAF_VERSION=1.19.3
# Wed, 13 Oct 2021 10:26:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 13 Oct 2021 10:26:19 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 03 Nov 2021 19:44:22 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Wed, 03 Nov 2021 19:44:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Nov 2021 19:44:23 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:07471e81507f7cf1100827f10c60c3c0422d1222430e34e527d97ec72b14a193`  
		Last Modified: Tue, 12 Oct 2021 01:26:26 GMT  
		Size: 50.4 MB (50436692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6cef1aa2170c001b320769bf8b018ed82d2c94a673e3010ea1ffe152e107419`  
		Last Modified: Tue, 12 Oct 2021 15:54:16 GMT  
		Size: 7.8 MB (7833862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a51f13be8e69cfc526b671d0bbf621b985b0932acd1523050e2995777b5926`  
		Last Modified: Tue, 12 Oct 2021 15:54:17 GMT  
		Size: 10.0 MB (9997204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91a466291d423e3faad6a8be6ae82e4a4d0550acb67989ac71c98f900e74d41`  
		Last Modified: Wed, 13 Oct 2021 10:26:55 GMT  
		Size: 17.4 MB (17415387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77934da0dce5bef46b239a3871787c2962a08cf1c8b1e629282f0c617b46426`  
		Last Modified: Wed, 13 Oct 2021 10:26:52 GMT  
		Size: 2.9 KB (2906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740ee4b64760022ecef81a94e508ebef6be4908cf720ddf4638226c3a4e18f01`  
		Last Modified: Wed, 13 Oct 2021 10:27:15 GMT  
		Size: 34.2 MB (34187833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017df2efa91fcb8917ec99f6f28405d5693a4c3a58509ad79e47a0598dce1443`  
		Last Modified: Wed, 03 Nov 2021 19:45:41 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.19.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:f025d777fd600f1763f219c31ae3d2acfa76505ccc3e6398ecabbaef1c169c5a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110246039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a310c800f2799c9b5029c3e85c3af7411a8a7dd1f9d630ee6cfe1591b90f09a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Oct 2021 01:29:06 GMT
ADD file:b1857dc4fe4fbc4af220829cc6af7169c4555d3f63a3a304db6fa0146b1d5539 in / 
# Tue, 12 Oct 2021 01:29:08 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 18:39:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 18:39:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Oct 2021 15:31:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 15:31:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 13 Oct 2021 15:31:32 GMT
ENV TELEGRAF_VERSION=1.19.3
# Wed, 13 Oct 2021 15:31:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 13 Oct 2021 15:31:44 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 03 Nov 2021 19:51:37 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Wed, 03 Nov 2021 19:51:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Nov 2021 19:51:38 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:139a906e9407e96c50669130c30fe8fba2681b14aa838a3e52f8753b566ef1c8`  
		Last Modified: Tue, 12 Oct 2021 01:45:13 GMT  
		Size: 45.9 MB (45917899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3907051e2154d5bd4ad15141b8938bc09674039787512494a99b93fd4ebc088d`  
		Last Modified: Tue, 12 Oct 2021 19:00:49 GMT  
		Size: 7.1 MB (7125242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8651d4793d5f4d465002213d2d462c964aaf8665a87d5f9cc0de7384f10eeb10`  
		Last Modified: Tue, 12 Oct 2021 19:00:49 GMT  
		Size: 9.3 MB (9343819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e659684a04aace7b984a69bccde2a720cb53304f8905d65b9068605177b2a4b6`  
		Last Modified: Wed, 13 Oct 2021 15:33:06 GMT  
		Size: 16.2 MB (16161376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc86d346babddcb58c40b9188fc289d120a16518eed1782662459497e55f179`  
		Last Modified: Wed, 13 Oct 2021 15:32:54 GMT  
		Size: 2.9 KB (2905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f9213a7b1180f7eb074ebc32c7adc9824c55705bacd59a5e64ceacc7720b3b`  
		Last Modified: Wed, 13 Oct 2021 15:33:47 GMT  
		Size: 31.7 MB (31694568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9989f04451b58ce865558163f9caaa26bafe2c7bb4a8dd0878fe1e27bb708f1b`  
		Last Modified: Wed, 03 Nov 2021 19:52:45 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.19.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6e4d11665765a9162f3e9af94e89ae8beeb2b581384a23bc72fbb2e17456738c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114713909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a957c2c51d6eca1bd0a378dbddcaac651fcbffaa49eaeec64ffa48f551bd7e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:27 GMT
ADD file:c7e9e884b1494f96e33e9d9a892b51367af8943edb282c4101cc99ea78a7753f in / 
# Wed, 17 Nov 2021 02:40:28 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 13:28:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 13:28:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 20:42:06 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 20:42:09 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 17 Nov 2021 20:42:24 GMT
ENV TELEGRAF_VERSION=1.19.3
# Wed, 17 Nov 2021 20:42:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 17 Nov 2021 20:42:30 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 17 Nov 2021 20:42:31 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Wed, 17 Nov 2021 20:42:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Nov 2021 20:42:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:626979e62c56e192812e818d52b82f063d9f9514b1b7bae14e534e4a7c98117a`  
		Last Modified: Wed, 17 Nov 2021 02:47:40 GMT  
		Size: 49.2 MB (49222990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134a528370d5dcbf5b6ba2d8c20f576504448e8f2d1debb5d2a4950a38a3ff2d`  
		Last Modified: Wed, 17 Nov 2021 13:37:44 GMT  
		Size: 7.7 MB (7695161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e12e3364b52ad043d8e79f750863ed4ca2878c4fdf45ded974508febc55fdd`  
		Last Modified: Wed, 17 Nov 2021 13:37:44 GMT  
		Size: 9.8 MB (9767133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be62c7c66899dfefa611452ca6b38510228e4e1661d1ec078d90733f59865bcb`  
		Last Modified: Wed, 17 Nov 2021 20:43:17 GMT  
		Size: 17.1 MB (17059007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ea9240a1fea313b800d353f9288154cce52bcb21b3cfabfc7bf0f861090de7`  
		Last Modified: Wed, 17 Nov 2021 20:43:14 GMT  
		Size: 2.9 KB (2875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb4fa8ccc7f74251b0b5e98750230eeac799bcfb5de5d01baf66fa5bf650699`  
		Last Modified: Wed, 17 Nov 2021 20:43:36 GMT  
		Size: 31.0 MB (30966512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9006db8c7aee266f0d94bd9643267132f4633a6434f7ad31d02cffd459cc659`  
		Last Modified: Wed, 17 Nov 2021 20:43:30 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.19.3-alpine`

```console
$ docker pull telegraf@sha256:9e391c4169ccb91b1001061dae70fac58ab82165f4079e7ec039e9d84a4b5ca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:1.19.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:627ea1f7f074a431873307fdba4c402fd567078bcc892dd9db37c5b26628f8c0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40241320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b97513bb4d721e5e1acbe529575e7db4451fc351934ce3ddee001d8183371b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Nov 2021 07:20:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec &&     update-ca-certificates
# Sat, 13 Nov 2021 07:20:51 GMT
ENV TELEGRAF_VERSION=1.19.3
# Sat, 13 Nov 2021 07:21:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 13 Nov 2021 07:21:05 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 13 Nov 2021 07:21:05 GMT
COPY file:4071aa7d94da140b944f5aaf032330509821a974e13349f4a3682e3368362128 in /entrypoint.sh 
# Sat, 13 Nov 2021 07:21:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 13 Nov 2021 07:21:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc79f199b43e46c5dfea12dfa8b92b7811e74b4d3812ff99c8368e4d2af803e7`  
		Last Modified: Fri, 12 Nov 2021 21:56:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ae06dab0a6b50d3f23d332a8c326fd227bd58abc651b7033038337f97e077f`  
		Last Modified: Sat, 13 Nov 2021 07:21:57 GMT  
		Size: 3.4 MB (3371612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269b03bad908f1f612f0e6e5f1618e234a49ac3fcf23cd4f579ae4e09117ac49`  
		Last Modified: Sat, 13 Nov 2021 07:22:22 GMT  
		Size: 34.0 MB (34046365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63e1ff47e2021e70246af4383776e6845936e12e0337f4540c023f664bbe5bd`  
		Last Modified: Sat, 13 Nov 2021 07:22:14 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.20`

```console
$ docker pull telegraf@sha256:879ccdec91a2575c540c6b1990bd8bdc30441cfafdb19826600a7e639c3da898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.20` - linux; amd64

```console
$ docker pull telegraf@sha256:210d82542b241a9d68c3f93b3b8549ed35d09c1f1eed4d6067971031361dbed7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121294336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c905645a69ca67570c85da3008b46b7f23bc59847c17189dff073cbf542dffb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Oct 2021 01:20:53 GMT
ADD file:98c256057b79b141aea9a806a4538cf6c3f340d7e3b0d6e8c363699333f3406b in / 
# Tue, 12 Oct 2021 01:20:53 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:44:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 15:44:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Oct 2021 10:25:38 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 10:25:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 29 Oct 2021 01:31:43 GMT
ENV TELEGRAF_VERSION=1.20.3
# Fri, 29 Oct 2021 01:31:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 29 Oct 2021 01:31:48 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 03 Nov 2021 19:44:38 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Wed, 03 Nov 2021 19:44:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Nov 2021 19:44:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:07471e81507f7cf1100827f10c60c3c0422d1222430e34e527d97ec72b14a193`  
		Last Modified: Tue, 12 Oct 2021 01:26:26 GMT  
		Size: 50.4 MB (50436692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6cef1aa2170c001b320769bf8b018ed82d2c94a673e3010ea1ffe152e107419`  
		Last Modified: Tue, 12 Oct 2021 15:54:16 GMT  
		Size: 7.8 MB (7833862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a51f13be8e69cfc526b671d0bbf621b985b0932acd1523050e2995777b5926`  
		Last Modified: Tue, 12 Oct 2021 15:54:17 GMT  
		Size: 10.0 MB (9997204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91a466291d423e3faad6a8be6ae82e4a4d0550acb67989ac71c98f900e74d41`  
		Last Modified: Wed, 13 Oct 2021 10:26:55 GMT  
		Size: 17.4 MB (17415387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77934da0dce5bef46b239a3871787c2962a08cf1c8b1e629282f0c617b46426`  
		Last Modified: Wed, 13 Oct 2021 10:26:52 GMT  
		Size: 2.9 KB (2906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9bb9c78b7fc1c3d2d301570d7a073caa789bd48f29617a234431b3937566893`  
		Last Modified: Fri, 29 Oct 2021 01:33:18 GMT  
		Size: 35.6 MB (35608054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f86ea74520d5c38238db95f3d83fc8da214f7a35f2cfef7399ea3b2944df12`  
		Last Modified: Wed, 03 Nov 2021 19:46:07 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.20` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:fedd44d5aad17fa7b3ad65a823d2881ad75014b2d295dc49ce175c370811ec16
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111628087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ba02837fbe7cada0a9244a77c1ddf35335f1e0a5c217af935a9eff4f7b7f69`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Oct 2021 01:29:06 GMT
ADD file:b1857dc4fe4fbc4af220829cc6af7169c4555d3f63a3a304db6fa0146b1d5539 in / 
# Tue, 12 Oct 2021 01:29:08 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 18:39:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 18:39:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Oct 2021 15:31:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 15:31:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 29 Oct 2021 02:06:56 GMT
ENV TELEGRAF_VERSION=1.20.3
# Fri, 29 Oct 2021 02:07:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 29 Oct 2021 02:07:09 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 03 Nov 2021 19:51:49 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Wed, 03 Nov 2021 19:51:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Nov 2021 19:51:50 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:139a906e9407e96c50669130c30fe8fba2681b14aa838a3e52f8753b566ef1c8`  
		Last Modified: Tue, 12 Oct 2021 01:45:13 GMT  
		Size: 45.9 MB (45917899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3907051e2154d5bd4ad15141b8938bc09674039787512494a99b93fd4ebc088d`  
		Last Modified: Tue, 12 Oct 2021 19:00:49 GMT  
		Size: 7.1 MB (7125242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8651d4793d5f4d465002213d2d462c964aaf8665a87d5f9cc0de7384f10eeb10`  
		Last Modified: Tue, 12 Oct 2021 19:00:49 GMT  
		Size: 9.3 MB (9343819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e659684a04aace7b984a69bccde2a720cb53304f8905d65b9068605177b2a4b6`  
		Last Modified: Wed, 13 Oct 2021 15:33:06 GMT  
		Size: 16.2 MB (16161376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc86d346babddcb58c40b9188fc289d120a16518eed1782662459497e55f179`  
		Last Modified: Wed, 13 Oct 2021 15:32:54 GMT  
		Size: 2.9 KB (2905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:addd4dfa7b430b02958aab120dc5d6dd3133c1b1f527269a956ba4078dd4998a`  
		Last Modified: Fri, 29 Oct 2021 02:08:41 GMT  
		Size: 33.1 MB (33076615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2b4bc4eec6033093c06cf1bbeed8bd8ad73d8db305ce297557af064b7aaf22`  
		Last Modified: Wed, 03 Nov 2021 19:52:56 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.20` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:59deb3510f567d7f1cd90aa511cff2b0abf9db2cdd0e1b4db6080b21488d6932
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.1 MB (116091267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec99cb94cc34397b9783c8ee0f16d8185ee216fa2cdccaf9361fc23b7cd01e54`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:27 GMT
ADD file:c7e9e884b1494f96e33e9d9a892b51367af8943edb282c4101cc99ea78a7753f in / 
# Wed, 17 Nov 2021 02:40:28 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 13:28:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 13:28:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 20:42:06 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 20:42:09 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 17 Nov 2021 20:42:38 GMT
ENV TELEGRAF_VERSION=1.20.3
# Wed, 17 Nov 2021 20:42:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 17 Nov 2021 20:42:48 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 17 Nov 2021 20:42:50 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Wed, 17 Nov 2021 20:42:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Nov 2021 20:42:51 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:626979e62c56e192812e818d52b82f063d9f9514b1b7bae14e534e4a7c98117a`  
		Last Modified: Wed, 17 Nov 2021 02:47:40 GMT  
		Size: 49.2 MB (49222990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134a528370d5dcbf5b6ba2d8c20f576504448e8f2d1debb5d2a4950a38a3ff2d`  
		Last Modified: Wed, 17 Nov 2021 13:37:44 GMT  
		Size: 7.7 MB (7695161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e12e3364b52ad043d8e79f750863ed4ca2878c4fdf45ded974508febc55fdd`  
		Last Modified: Wed, 17 Nov 2021 13:37:44 GMT  
		Size: 9.8 MB (9767133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be62c7c66899dfefa611452ca6b38510228e4e1661d1ec078d90733f59865bcb`  
		Last Modified: Wed, 17 Nov 2021 20:43:17 GMT  
		Size: 17.1 MB (17059007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ea9240a1fea313b800d353f9288154cce52bcb21b3cfabfc7bf0f861090de7`  
		Last Modified: Wed, 17 Nov 2021 20:43:14 GMT  
		Size: 2.9 KB (2875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b99ce1f5cf7a1e9e2a732004677c1cb2ececf45b1deb897dcb743554459076d`  
		Last Modified: Wed, 17 Nov 2021 20:43:52 GMT  
		Size: 32.3 MB (32343870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2613b76c3ec562d8153bf6a6a7985c744b76bcc06f5b20984803e3671449d2b`  
		Last Modified: Wed, 17 Nov 2021 20:43:46 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.20-alpine`

```console
$ docker pull telegraf@sha256:5e790d293cae2a28d93616b2f4e8c6f56234695e0a44c5483f15eb573e60d109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:1.20-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:3417e40207742c08f4306388b77c9b8721a84ea552b24e6e431bea125bf061f0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41654254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:175fd87d6f202e027ceb6b08499d4b3ab64fc106f454f57d4a1f03058a21d879`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Nov 2021 07:20:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec &&     update-ca-certificates
# Sat, 13 Nov 2021 07:21:14 GMT
ENV TELEGRAF_VERSION=1.20.3
# Sat, 13 Nov 2021 07:21:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 13 Nov 2021 07:21:25 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 13 Nov 2021 07:21:26 GMT
COPY file:4071aa7d94da140b944f5aaf032330509821a974e13349f4a3682e3368362128 in /entrypoint.sh 
# Sat, 13 Nov 2021 07:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 13 Nov 2021 07:21:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc79f199b43e46c5dfea12dfa8b92b7811e74b4d3812ff99c8368e4d2af803e7`  
		Last Modified: Fri, 12 Nov 2021 21:56:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ae06dab0a6b50d3f23d332a8c326fd227bd58abc651b7033038337f97e077f`  
		Last Modified: Sat, 13 Nov 2021 07:21:57 GMT  
		Size: 3.4 MB (3371612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d660f5f1a799f2942df0a7bb82ed8a90a17875f585ef37d3b746373dd8e7ed`  
		Last Modified: Sat, 13 Nov 2021 07:22:50 GMT  
		Size: 35.5 MB (35459298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2525a4a2008c02719c91dd3c1cd24c97f88dc40b60c2eb7a0d853df3499d324`  
		Last Modified: Sat, 13 Nov 2021 07:22:44 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.20.3`

```console
$ docker pull telegraf@sha256:879ccdec91a2575c540c6b1990bd8bdc30441cfafdb19826600a7e639c3da898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.20.3` - linux; amd64

```console
$ docker pull telegraf@sha256:210d82542b241a9d68c3f93b3b8549ed35d09c1f1eed4d6067971031361dbed7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121294336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c905645a69ca67570c85da3008b46b7f23bc59847c17189dff073cbf542dffb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Oct 2021 01:20:53 GMT
ADD file:98c256057b79b141aea9a806a4538cf6c3f340d7e3b0d6e8c363699333f3406b in / 
# Tue, 12 Oct 2021 01:20:53 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:44:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 15:44:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Oct 2021 10:25:38 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 10:25:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 29 Oct 2021 01:31:43 GMT
ENV TELEGRAF_VERSION=1.20.3
# Fri, 29 Oct 2021 01:31:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 29 Oct 2021 01:31:48 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 03 Nov 2021 19:44:38 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Wed, 03 Nov 2021 19:44:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Nov 2021 19:44:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:07471e81507f7cf1100827f10c60c3c0422d1222430e34e527d97ec72b14a193`  
		Last Modified: Tue, 12 Oct 2021 01:26:26 GMT  
		Size: 50.4 MB (50436692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6cef1aa2170c001b320769bf8b018ed82d2c94a673e3010ea1ffe152e107419`  
		Last Modified: Tue, 12 Oct 2021 15:54:16 GMT  
		Size: 7.8 MB (7833862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a51f13be8e69cfc526b671d0bbf621b985b0932acd1523050e2995777b5926`  
		Last Modified: Tue, 12 Oct 2021 15:54:17 GMT  
		Size: 10.0 MB (9997204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91a466291d423e3faad6a8be6ae82e4a4d0550acb67989ac71c98f900e74d41`  
		Last Modified: Wed, 13 Oct 2021 10:26:55 GMT  
		Size: 17.4 MB (17415387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77934da0dce5bef46b239a3871787c2962a08cf1c8b1e629282f0c617b46426`  
		Last Modified: Wed, 13 Oct 2021 10:26:52 GMT  
		Size: 2.9 KB (2906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9bb9c78b7fc1c3d2d301570d7a073caa789bd48f29617a234431b3937566893`  
		Last Modified: Fri, 29 Oct 2021 01:33:18 GMT  
		Size: 35.6 MB (35608054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f86ea74520d5c38238db95f3d83fc8da214f7a35f2cfef7399ea3b2944df12`  
		Last Modified: Wed, 03 Nov 2021 19:46:07 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.20.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:fedd44d5aad17fa7b3ad65a823d2881ad75014b2d295dc49ce175c370811ec16
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111628087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ba02837fbe7cada0a9244a77c1ddf35335f1e0a5c217af935a9eff4f7b7f69`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Oct 2021 01:29:06 GMT
ADD file:b1857dc4fe4fbc4af220829cc6af7169c4555d3f63a3a304db6fa0146b1d5539 in / 
# Tue, 12 Oct 2021 01:29:08 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 18:39:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 18:39:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Oct 2021 15:31:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 15:31:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 29 Oct 2021 02:06:56 GMT
ENV TELEGRAF_VERSION=1.20.3
# Fri, 29 Oct 2021 02:07:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 29 Oct 2021 02:07:09 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 03 Nov 2021 19:51:49 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Wed, 03 Nov 2021 19:51:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Nov 2021 19:51:50 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:139a906e9407e96c50669130c30fe8fba2681b14aa838a3e52f8753b566ef1c8`  
		Last Modified: Tue, 12 Oct 2021 01:45:13 GMT  
		Size: 45.9 MB (45917899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3907051e2154d5bd4ad15141b8938bc09674039787512494a99b93fd4ebc088d`  
		Last Modified: Tue, 12 Oct 2021 19:00:49 GMT  
		Size: 7.1 MB (7125242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8651d4793d5f4d465002213d2d462c964aaf8665a87d5f9cc0de7384f10eeb10`  
		Last Modified: Tue, 12 Oct 2021 19:00:49 GMT  
		Size: 9.3 MB (9343819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e659684a04aace7b984a69bccde2a720cb53304f8905d65b9068605177b2a4b6`  
		Last Modified: Wed, 13 Oct 2021 15:33:06 GMT  
		Size: 16.2 MB (16161376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc86d346babddcb58c40b9188fc289d120a16518eed1782662459497e55f179`  
		Last Modified: Wed, 13 Oct 2021 15:32:54 GMT  
		Size: 2.9 KB (2905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:addd4dfa7b430b02958aab120dc5d6dd3133c1b1f527269a956ba4078dd4998a`  
		Last Modified: Fri, 29 Oct 2021 02:08:41 GMT  
		Size: 33.1 MB (33076615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2b4bc4eec6033093c06cf1bbeed8bd8ad73d8db305ce297557af064b7aaf22`  
		Last Modified: Wed, 03 Nov 2021 19:52:56 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.20.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:59deb3510f567d7f1cd90aa511cff2b0abf9db2cdd0e1b4db6080b21488d6932
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.1 MB (116091267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec99cb94cc34397b9783c8ee0f16d8185ee216fa2cdccaf9361fc23b7cd01e54`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:27 GMT
ADD file:c7e9e884b1494f96e33e9d9a892b51367af8943edb282c4101cc99ea78a7753f in / 
# Wed, 17 Nov 2021 02:40:28 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 13:28:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 13:28:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 20:42:06 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 20:42:09 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 17 Nov 2021 20:42:38 GMT
ENV TELEGRAF_VERSION=1.20.3
# Wed, 17 Nov 2021 20:42:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 17 Nov 2021 20:42:48 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 17 Nov 2021 20:42:50 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Wed, 17 Nov 2021 20:42:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Nov 2021 20:42:51 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:626979e62c56e192812e818d52b82f063d9f9514b1b7bae14e534e4a7c98117a`  
		Last Modified: Wed, 17 Nov 2021 02:47:40 GMT  
		Size: 49.2 MB (49222990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134a528370d5dcbf5b6ba2d8c20f576504448e8f2d1debb5d2a4950a38a3ff2d`  
		Last Modified: Wed, 17 Nov 2021 13:37:44 GMT  
		Size: 7.7 MB (7695161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e12e3364b52ad043d8e79f750863ed4ca2878c4fdf45ded974508febc55fdd`  
		Last Modified: Wed, 17 Nov 2021 13:37:44 GMT  
		Size: 9.8 MB (9767133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be62c7c66899dfefa611452ca6b38510228e4e1661d1ec078d90733f59865bcb`  
		Last Modified: Wed, 17 Nov 2021 20:43:17 GMT  
		Size: 17.1 MB (17059007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ea9240a1fea313b800d353f9288154cce52bcb21b3cfabfc7bf0f861090de7`  
		Last Modified: Wed, 17 Nov 2021 20:43:14 GMT  
		Size: 2.9 KB (2875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b99ce1f5cf7a1e9e2a732004677c1cb2ececf45b1deb897dcb743554459076d`  
		Last Modified: Wed, 17 Nov 2021 20:43:52 GMT  
		Size: 32.3 MB (32343870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2613b76c3ec562d8153bf6a6a7985c744b76bcc06f5b20984803e3671449d2b`  
		Last Modified: Wed, 17 Nov 2021 20:43:46 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.20.3-alpine`

```console
$ docker pull telegraf@sha256:5e790d293cae2a28d93616b2f4e8c6f56234695e0a44c5483f15eb573e60d109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:1.20.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:3417e40207742c08f4306388b77c9b8721a84ea552b24e6e431bea125bf061f0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41654254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:175fd87d6f202e027ceb6b08499d4b3ab64fc106f454f57d4a1f03058a21d879`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Nov 2021 07:20:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec &&     update-ca-certificates
# Sat, 13 Nov 2021 07:21:14 GMT
ENV TELEGRAF_VERSION=1.20.3
# Sat, 13 Nov 2021 07:21:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 13 Nov 2021 07:21:25 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 13 Nov 2021 07:21:26 GMT
COPY file:4071aa7d94da140b944f5aaf032330509821a974e13349f4a3682e3368362128 in /entrypoint.sh 
# Sat, 13 Nov 2021 07:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 13 Nov 2021 07:21:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc79f199b43e46c5dfea12dfa8b92b7811e74b4d3812ff99c8368e4d2af803e7`  
		Last Modified: Fri, 12 Nov 2021 21:56:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ae06dab0a6b50d3f23d332a8c326fd227bd58abc651b7033038337f97e077f`  
		Last Modified: Sat, 13 Nov 2021 07:21:57 GMT  
		Size: 3.4 MB (3371612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d660f5f1a799f2942df0a7bb82ed8a90a17875f585ef37d3b746373dd8e7ed`  
		Last Modified: Sat, 13 Nov 2021 07:22:50 GMT  
		Size: 35.5 MB (35459298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2525a4a2008c02719c91dd3c1cd24c97f88dc40b60c2eb7a0d853df3499d324`  
		Last Modified: Sat, 13 Nov 2021 07:22:44 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:5e790d293cae2a28d93616b2f4e8c6f56234695e0a44c5483f15eb573e60d109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:3417e40207742c08f4306388b77c9b8721a84ea552b24e6e431bea125bf061f0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41654254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:175fd87d6f202e027ceb6b08499d4b3ab64fc106f454f57d4a1f03058a21d879`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Nov 2021 07:20:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec &&     update-ca-certificates
# Sat, 13 Nov 2021 07:21:14 GMT
ENV TELEGRAF_VERSION=1.20.3
# Sat, 13 Nov 2021 07:21:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 13 Nov 2021 07:21:25 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 13 Nov 2021 07:21:26 GMT
COPY file:4071aa7d94da140b944f5aaf032330509821a974e13349f4a3682e3368362128 in /entrypoint.sh 
# Sat, 13 Nov 2021 07:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 13 Nov 2021 07:21:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc79f199b43e46c5dfea12dfa8b92b7811e74b4d3812ff99c8368e4d2af803e7`  
		Last Modified: Fri, 12 Nov 2021 21:56:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ae06dab0a6b50d3f23d332a8c326fd227bd58abc651b7033038337f97e077f`  
		Last Modified: Sat, 13 Nov 2021 07:21:57 GMT  
		Size: 3.4 MB (3371612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d660f5f1a799f2942df0a7bb82ed8a90a17875f585ef37d3b746373dd8e7ed`  
		Last Modified: Sat, 13 Nov 2021 07:22:50 GMT  
		Size: 35.5 MB (35459298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2525a4a2008c02719c91dd3c1cd24c97f88dc40b60c2eb7a0d853df3499d324`  
		Last Modified: Sat, 13 Nov 2021 07:22:44 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:879ccdec91a2575c540c6b1990bd8bdc30441cfafdb19826600a7e639c3da898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:210d82542b241a9d68c3f93b3b8549ed35d09c1f1eed4d6067971031361dbed7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121294336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c905645a69ca67570c85da3008b46b7f23bc59847c17189dff073cbf542dffb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Oct 2021 01:20:53 GMT
ADD file:98c256057b79b141aea9a806a4538cf6c3f340d7e3b0d6e8c363699333f3406b in / 
# Tue, 12 Oct 2021 01:20:53 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:44:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 15:44:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Oct 2021 10:25:38 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 10:25:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 29 Oct 2021 01:31:43 GMT
ENV TELEGRAF_VERSION=1.20.3
# Fri, 29 Oct 2021 01:31:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 29 Oct 2021 01:31:48 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 03 Nov 2021 19:44:38 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Wed, 03 Nov 2021 19:44:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Nov 2021 19:44:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:07471e81507f7cf1100827f10c60c3c0422d1222430e34e527d97ec72b14a193`  
		Last Modified: Tue, 12 Oct 2021 01:26:26 GMT  
		Size: 50.4 MB (50436692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6cef1aa2170c001b320769bf8b018ed82d2c94a673e3010ea1ffe152e107419`  
		Last Modified: Tue, 12 Oct 2021 15:54:16 GMT  
		Size: 7.8 MB (7833862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a51f13be8e69cfc526b671d0bbf621b985b0932acd1523050e2995777b5926`  
		Last Modified: Tue, 12 Oct 2021 15:54:17 GMT  
		Size: 10.0 MB (9997204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91a466291d423e3faad6a8be6ae82e4a4d0550acb67989ac71c98f900e74d41`  
		Last Modified: Wed, 13 Oct 2021 10:26:55 GMT  
		Size: 17.4 MB (17415387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77934da0dce5bef46b239a3871787c2962a08cf1c8b1e629282f0c617b46426`  
		Last Modified: Wed, 13 Oct 2021 10:26:52 GMT  
		Size: 2.9 KB (2906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9bb9c78b7fc1c3d2d301570d7a073caa789bd48f29617a234431b3937566893`  
		Last Modified: Fri, 29 Oct 2021 01:33:18 GMT  
		Size: 35.6 MB (35608054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f86ea74520d5c38238db95f3d83fc8da214f7a35f2cfef7399ea3b2944df12`  
		Last Modified: Wed, 03 Nov 2021 19:46:07 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:fedd44d5aad17fa7b3ad65a823d2881ad75014b2d295dc49ce175c370811ec16
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111628087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ba02837fbe7cada0a9244a77c1ddf35335f1e0a5c217af935a9eff4f7b7f69`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Oct 2021 01:29:06 GMT
ADD file:b1857dc4fe4fbc4af220829cc6af7169c4555d3f63a3a304db6fa0146b1d5539 in / 
# Tue, 12 Oct 2021 01:29:08 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 18:39:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 18:39:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Oct 2021 15:31:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 15:31:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 29 Oct 2021 02:06:56 GMT
ENV TELEGRAF_VERSION=1.20.3
# Fri, 29 Oct 2021 02:07:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 29 Oct 2021 02:07:09 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 03 Nov 2021 19:51:49 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Wed, 03 Nov 2021 19:51:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Nov 2021 19:51:50 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:139a906e9407e96c50669130c30fe8fba2681b14aa838a3e52f8753b566ef1c8`  
		Last Modified: Tue, 12 Oct 2021 01:45:13 GMT  
		Size: 45.9 MB (45917899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3907051e2154d5bd4ad15141b8938bc09674039787512494a99b93fd4ebc088d`  
		Last Modified: Tue, 12 Oct 2021 19:00:49 GMT  
		Size: 7.1 MB (7125242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8651d4793d5f4d465002213d2d462c964aaf8665a87d5f9cc0de7384f10eeb10`  
		Last Modified: Tue, 12 Oct 2021 19:00:49 GMT  
		Size: 9.3 MB (9343819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e659684a04aace7b984a69bccde2a720cb53304f8905d65b9068605177b2a4b6`  
		Last Modified: Wed, 13 Oct 2021 15:33:06 GMT  
		Size: 16.2 MB (16161376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc86d346babddcb58c40b9188fc289d120a16518eed1782662459497e55f179`  
		Last Modified: Wed, 13 Oct 2021 15:32:54 GMT  
		Size: 2.9 KB (2905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:addd4dfa7b430b02958aab120dc5d6dd3133c1b1f527269a956ba4078dd4998a`  
		Last Modified: Fri, 29 Oct 2021 02:08:41 GMT  
		Size: 33.1 MB (33076615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2b4bc4eec6033093c06cf1bbeed8bd8ad73d8db305ce297557af064b7aaf22`  
		Last Modified: Wed, 03 Nov 2021 19:52:56 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:59deb3510f567d7f1cd90aa511cff2b0abf9db2cdd0e1b4db6080b21488d6932
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.1 MB (116091267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec99cb94cc34397b9783c8ee0f16d8185ee216fa2cdccaf9361fc23b7cd01e54`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:27 GMT
ADD file:c7e9e884b1494f96e33e9d9a892b51367af8943edb282c4101cc99ea78a7753f in / 
# Wed, 17 Nov 2021 02:40:28 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 13:28:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 13:28:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 20:42:06 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 20:42:09 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 17 Nov 2021 20:42:38 GMT
ENV TELEGRAF_VERSION=1.20.3
# Wed, 17 Nov 2021 20:42:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 17 Nov 2021 20:42:48 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 17 Nov 2021 20:42:50 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Wed, 17 Nov 2021 20:42:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Nov 2021 20:42:51 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:626979e62c56e192812e818d52b82f063d9f9514b1b7bae14e534e4a7c98117a`  
		Last Modified: Wed, 17 Nov 2021 02:47:40 GMT  
		Size: 49.2 MB (49222990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134a528370d5dcbf5b6ba2d8c20f576504448e8f2d1debb5d2a4950a38a3ff2d`  
		Last Modified: Wed, 17 Nov 2021 13:37:44 GMT  
		Size: 7.7 MB (7695161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e12e3364b52ad043d8e79f750863ed4ca2878c4fdf45ded974508febc55fdd`  
		Last Modified: Wed, 17 Nov 2021 13:37:44 GMT  
		Size: 9.8 MB (9767133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be62c7c66899dfefa611452ca6b38510228e4e1661d1ec078d90733f59865bcb`  
		Last Modified: Wed, 17 Nov 2021 20:43:17 GMT  
		Size: 17.1 MB (17059007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ea9240a1fea313b800d353f9288154cce52bcb21b3cfabfc7bf0f861090de7`  
		Last Modified: Wed, 17 Nov 2021 20:43:14 GMT  
		Size: 2.9 KB (2875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b99ce1f5cf7a1e9e2a732004677c1cb2ececf45b1deb897dcb743554459076d`  
		Last Modified: Wed, 17 Nov 2021 20:43:52 GMT  
		Size: 32.3 MB (32343870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2613b76c3ec562d8153bf6a6a7985c744b76bcc06f5b20984803e3671449d2b`  
		Last Modified: Wed, 17 Nov 2021 20:43:46 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
