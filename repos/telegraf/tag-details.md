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
$ docker pull telegraf@sha256:17dc93794ed1d696bbcbf456c0cd3e21584b424f680e597cd2be9fd87d375c2e
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
$ docker pull telegraf@sha256:7441f3c7a3bcba647d7439f325ace4def9276b8ae8b68cd9365b2ea480b89722
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110720292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:186d2b9d3fb60e572ccf8254e6595cb62d7fc6145623bf0a2858d6e4ee1f27fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Oct 2021 01:41:28 GMT
ADD file:aed1709ccba6a81b9726b228fad7b81bcf4c16bafe723981ad37076322d78986 in / 
# Tue, 12 Oct 2021 01:41:29 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:59:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:59:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 16 Oct 2021 11:51:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 11:51:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 16 Oct 2021 11:51:08 GMT
ENV TELEGRAF_VERSION=1.18.3
# Sat, 16 Oct 2021 11:51:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Sat, 16 Oct 2021 11:51:13 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 29 Oct 2021 00:21:34 GMT
USER telegraf
# Fri, 29 Oct 2021 00:21:36 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Fri, 29 Oct 2021 00:21:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Oct 2021 00:21:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2ff6d7a9e7d73e4a01b9417518d18c001728c45fa8109ed8f55aaa50e7981482`  
		Last Modified: Tue, 12 Oct 2021 01:48:38 GMT  
		Size: 49.2 MB (49222756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7324ea4098419bc5fa2ac5a138522230bf12cef3996d1740dd00f9d4737d004`  
		Last Modified: Sat, 16 Oct 2021 03:15:37 GMT  
		Size: 7.7 MB (7695063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e213c33a07316d84d829be685bd3b02e1e2bc135f7748c932050e6ed6a3a0d3`  
		Last Modified: Sat, 16 Oct 2021 03:15:37 GMT  
		Size: 9.8 MB (9767289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195fcb7c5d1eb571a72b8f9d97c3baa030a716aa837f3e8228435b153a518cca`  
		Last Modified: Sat, 16 Oct 2021 11:52:14 GMT  
		Size: 17.1 MB (17058985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb3a6b78fdf159f9ca6b70db784a6eafd05eb4f5f46555df56c6d48d032c608`  
		Last Modified: Sat, 16 Oct 2021 11:52:11 GMT  
		Size: 2.9 KB (2879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e882748fd14001237e38063bb3983a9ad85c8a53ec3b58b5a091f8315d8224`  
		Last Modified: Sat, 16 Oct 2021 11:52:16 GMT  
		Size: 27.0 MB (26973134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d041509eed212b98d7d081cbf77a223d47a124888b95be315c89e39c1db40564`  
		Last Modified: Fri, 29 Oct 2021 00:22:22 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.18-alpine`

```console
$ docker pull telegraf@sha256:eac5ea08c9684bb31517a5b3b34996de974878c06c130a023c5c552cd156bb1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:1.18-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:02f8c4674423686b2d2d57a5fa5d93acf4b86dfe4cb544c97cdddbd20abfd02e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 MB (35851581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84998ed9f7c55e217804303b6cfd5722e7cfe120ab2dc9e67bff0c1038c1e60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Thu, 16 Sep 2021 21:20:06 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 03 Nov 2021 19:44:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec &&     update-ca-certificates
# Wed, 03 Nov 2021 19:44:05 GMT
ENV TELEGRAF_VERSION=1.18.3
# Wed, 03 Nov 2021 19:44:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Wed, 03 Nov 2021 19:44:19 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 03 Nov 2021 19:44:20 GMT
COPY file:4071aa7d94da140b944f5aaf032330509821a974e13349f4a3682e3368362128 in /entrypoint.sh 
# Wed, 03 Nov 2021 19:44:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Nov 2021 19:44:20 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8cf55ffd68f3512245522356168367182cfdaeb0a0d11bbd5328472d4c0761`  
		Last Modified: Thu, 16 Sep 2021 21:24:04 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc5969994ddff3cc06380d4484d56d3001e9b843686d9d8e2df71ab1a5bfb87`  
		Last Modified: Wed, 03 Nov 2021 19:45:21 GMT  
		Size: 3.4 MB (3371089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816681438b86ea7e280b27f389706ceb370d5ff9cd4445bde7c95569122d533d`  
		Last Modified: Wed, 03 Nov 2021 19:45:25 GMT  
		Size: 29.7 MB (29665686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12aaf691b637c9d5ba317c59cab5139b116b125c096a4c893ed45bb6405b6fa8`  
		Last Modified: Wed, 03 Nov 2021 19:45:20 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.18.3`

```console
$ docker pull telegraf@sha256:17dc93794ed1d696bbcbf456c0cd3e21584b424f680e597cd2be9fd87d375c2e
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
$ docker pull telegraf@sha256:7441f3c7a3bcba647d7439f325ace4def9276b8ae8b68cd9365b2ea480b89722
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110720292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:186d2b9d3fb60e572ccf8254e6595cb62d7fc6145623bf0a2858d6e4ee1f27fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Oct 2021 01:41:28 GMT
ADD file:aed1709ccba6a81b9726b228fad7b81bcf4c16bafe723981ad37076322d78986 in / 
# Tue, 12 Oct 2021 01:41:29 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:59:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:59:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 16 Oct 2021 11:51:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 11:51:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 16 Oct 2021 11:51:08 GMT
ENV TELEGRAF_VERSION=1.18.3
# Sat, 16 Oct 2021 11:51:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Sat, 16 Oct 2021 11:51:13 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 29 Oct 2021 00:21:34 GMT
USER telegraf
# Fri, 29 Oct 2021 00:21:36 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Fri, 29 Oct 2021 00:21:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Oct 2021 00:21:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2ff6d7a9e7d73e4a01b9417518d18c001728c45fa8109ed8f55aaa50e7981482`  
		Last Modified: Tue, 12 Oct 2021 01:48:38 GMT  
		Size: 49.2 MB (49222756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7324ea4098419bc5fa2ac5a138522230bf12cef3996d1740dd00f9d4737d004`  
		Last Modified: Sat, 16 Oct 2021 03:15:37 GMT  
		Size: 7.7 MB (7695063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e213c33a07316d84d829be685bd3b02e1e2bc135f7748c932050e6ed6a3a0d3`  
		Last Modified: Sat, 16 Oct 2021 03:15:37 GMT  
		Size: 9.8 MB (9767289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195fcb7c5d1eb571a72b8f9d97c3baa030a716aa837f3e8228435b153a518cca`  
		Last Modified: Sat, 16 Oct 2021 11:52:14 GMT  
		Size: 17.1 MB (17058985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb3a6b78fdf159f9ca6b70db784a6eafd05eb4f5f46555df56c6d48d032c608`  
		Last Modified: Sat, 16 Oct 2021 11:52:11 GMT  
		Size: 2.9 KB (2879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e882748fd14001237e38063bb3983a9ad85c8a53ec3b58b5a091f8315d8224`  
		Last Modified: Sat, 16 Oct 2021 11:52:16 GMT  
		Size: 27.0 MB (26973134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d041509eed212b98d7d081cbf77a223d47a124888b95be315c89e39c1db40564`  
		Last Modified: Fri, 29 Oct 2021 00:22:22 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.18.3-alpine`

```console
$ docker pull telegraf@sha256:eac5ea08c9684bb31517a5b3b34996de974878c06c130a023c5c552cd156bb1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:1.18.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:02f8c4674423686b2d2d57a5fa5d93acf4b86dfe4cb544c97cdddbd20abfd02e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 MB (35851581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84998ed9f7c55e217804303b6cfd5722e7cfe120ab2dc9e67bff0c1038c1e60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Thu, 16 Sep 2021 21:20:06 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 03 Nov 2021 19:44:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec &&     update-ca-certificates
# Wed, 03 Nov 2021 19:44:05 GMT
ENV TELEGRAF_VERSION=1.18.3
# Wed, 03 Nov 2021 19:44:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Wed, 03 Nov 2021 19:44:19 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 03 Nov 2021 19:44:20 GMT
COPY file:4071aa7d94da140b944f5aaf032330509821a974e13349f4a3682e3368362128 in /entrypoint.sh 
# Wed, 03 Nov 2021 19:44:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Nov 2021 19:44:20 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8cf55ffd68f3512245522356168367182cfdaeb0a0d11bbd5328472d4c0761`  
		Last Modified: Thu, 16 Sep 2021 21:24:04 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc5969994ddff3cc06380d4484d56d3001e9b843686d9d8e2df71ab1a5bfb87`  
		Last Modified: Wed, 03 Nov 2021 19:45:21 GMT  
		Size: 3.4 MB (3371089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816681438b86ea7e280b27f389706ceb370d5ff9cd4445bde7c95569122d533d`  
		Last Modified: Wed, 03 Nov 2021 19:45:25 GMT  
		Size: 29.7 MB (29665686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12aaf691b637c9d5ba317c59cab5139b116b125c096a4c893ed45bb6405b6fa8`  
		Last Modified: Wed, 03 Nov 2021 19:45:20 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.19`

```console
$ docker pull telegraf@sha256:d31a9577e8fda7058b1bc00743ce82588cae2fbf05d70ffb207dbc1bf697780e
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
$ docker pull telegraf@sha256:e84d22992263e08a81ab5bb01c7b7fdb96a5bafd74e1deedd584abc2db3377ee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114713620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f03fb12daca69d0cd68465bf49ff19ae85772d94a5ca07eb5ba858be637b14`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Oct 2021 01:41:28 GMT
ADD file:aed1709ccba6a81b9726b228fad7b81bcf4c16bafe723981ad37076322d78986 in / 
# Tue, 12 Oct 2021 01:41:29 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:59:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:59:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 16 Oct 2021 11:51:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 11:51:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 16 Oct 2021 11:51:23 GMT
ENV TELEGRAF_VERSION=1.19.3
# Sat, 16 Oct 2021 11:51:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Sat, 16 Oct 2021 11:51:27 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 29 Oct 2021 00:21:42 GMT
USER telegraf
# Fri, 29 Oct 2021 00:21:44 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Fri, 29 Oct 2021 00:21:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Oct 2021 00:21:45 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2ff6d7a9e7d73e4a01b9417518d18c001728c45fa8109ed8f55aaa50e7981482`  
		Last Modified: Tue, 12 Oct 2021 01:48:38 GMT  
		Size: 49.2 MB (49222756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7324ea4098419bc5fa2ac5a138522230bf12cef3996d1740dd00f9d4737d004`  
		Last Modified: Sat, 16 Oct 2021 03:15:37 GMT  
		Size: 7.7 MB (7695063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e213c33a07316d84d829be685bd3b02e1e2bc135f7748c932050e6ed6a3a0d3`  
		Last Modified: Sat, 16 Oct 2021 03:15:37 GMT  
		Size: 9.8 MB (9767289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195fcb7c5d1eb571a72b8f9d97c3baa030a716aa837f3e8228435b153a518cca`  
		Last Modified: Sat, 16 Oct 2021 11:52:14 GMT  
		Size: 17.1 MB (17058985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb3a6b78fdf159f9ca6b70db784a6eafd05eb4f5f46555df56c6d48d032c608`  
		Last Modified: Sat, 16 Oct 2021 11:52:11 GMT  
		Size: 2.9 KB (2879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d521ff76d5175010c3864c432ab662004079fd9bd5b37d02ddae4899af4c0e`  
		Last Modified: Sat, 16 Oct 2021 11:52:32 GMT  
		Size: 31.0 MB (30966464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee8a9e5cd179ad4693b9e8c13196f5e1a0b3d38738788903898659398fb730f`  
		Last Modified: Fri, 29 Oct 2021 00:22:32 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.19-alpine`

```console
$ docker pull telegraf@sha256:8050f9c50d29badd65df08a573865728936ae4915516860eb01224b437a63639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:1.19-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:48d9e2455559384bfdb8292ea16e8784fad05c078d1a97b20e2fac3f76c72b4a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40231257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42f4fc29c84140ab896e980723eabb1e03d33d87fedc8d37ed0459a36cd4fb71`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Thu, 16 Sep 2021 21:20:06 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 03 Nov 2021 19:44:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec &&     update-ca-certificates
# Wed, 03 Nov 2021 19:44:25 GMT
ENV TELEGRAF_VERSION=1.19.3
# Wed, 03 Nov 2021 19:44:34 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Wed, 03 Nov 2021 19:44:35 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 03 Nov 2021 19:44:35 GMT
COPY file:4071aa7d94da140b944f5aaf032330509821a974e13349f4a3682e3368362128 in /entrypoint.sh 
# Wed, 03 Nov 2021 19:44:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Nov 2021 19:44:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8cf55ffd68f3512245522356168367182cfdaeb0a0d11bbd5328472d4c0761`  
		Last Modified: Thu, 16 Sep 2021 21:24:04 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc5969994ddff3cc06380d4484d56d3001e9b843686d9d8e2df71ab1a5bfb87`  
		Last Modified: Wed, 03 Nov 2021 19:45:21 GMT  
		Size: 3.4 MB (3371089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c674d9f6917a59dccf7fe51db5e6875ee47435636af3a4fe3f03603e2c9dc1`  
		Last Modified: Wed, 03 Nov 2021 19:45:57 GMT  
		Size: 34.0 MB (34045362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e835e1bef96a0bd9c6e50bc12dd87a3d7811901165945e7c16edf407c00c21b3`  
		Last Modified: Wed, 03 Nov 2021 19:45:51 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.19.3`

```console
$ docker pull telegraf@sha256:d31a9577e8fda7058b1bc00743ce82588cae2fbf05d70ffb207dbc1bf697780e
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
$ docker pull telegraf@sha256:e84d22992263e08a81ab5bb01c7b7fdb96a5bafd74e1deedd584abc2db3377ee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114713620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f03fb12daca69d0cd68465bf49ff19ae85772d94a5ca07eb5ba858be637b14`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Oct 2021 01:41:28 GMT
ADD file:aed1709ccba6a81b9726b228fad7b81bcf4c16bafe723981ad37076322d78986 in / 
# Tue, 12 Oct 2021 01:41:29 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:59:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:59:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 16 Oct 2021 11:51:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 11:51:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 16 Oct 2021 11:51:23 GMT
ENV TELEGRAF_VERSION=1.19.3
# Sat, 16 Oct 2021 11:51:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Sat, 16 Oct 2021 11:51:27 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 29 Oct 2021 00:21:42 GMT
USER telegraf
# Fri, 29 Oct 2021 00:21:44 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Fri, 29 Oct 2021 00:21:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Oct 2021 00:21:45 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2ff6d7a9e7d73e4a01b9417518d18c001728c45fa8109ed8f55aaa50e7981482`  
		Last Modified: Tue, 12 Oct 2021 01:48:38 GMT  
		Size: 49.2 MB (49222756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7324ea4098419bc5fa2ac5a138522230bf12cef3996d1740dd00f9d4737d004`  
		Last Modified: Sat, 16 Oct 2021 03:15:37 GMT  
		Size: 7.7 MB (7695063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e213c33a07316d84d829be685bd3b02e1e2bc135f7748c932050e6ed6a3a0d3`  
		Last Modified: Sat, 16 Oct 2021 03:15:37 GMT  
		Size: 9.8 MB (9767289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195fcb7c5d1eb571a72b8f9d97c3baa030a716aa837f3e8228435b153a518cca`  
		Last Modified: Sat, 16 Oct 2021 11:52:14 GMT  
		Size: 17.1 MB (17058985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb3a6b78fdf159f9ca6b70db784a6eafd05eb4f5f46555df56c6d48d032c608`  
		Last Modified: Sat, 16 Oct 2021 11:52:11 GMT  
		Size: 2.9 KB (2879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d521ff76d5175010c3864c432ab662004079fd9bd5b37d02ddae4899af4c0e`  
		Last Modified: Sat, 16 Oct 2021 11:52:32 GMT  
		Size: 31.0 MB (30966464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee8a9e5cd179ad4693b9e8c13196f5e1a0b3d38738788903898659398fb730f`  
		Last Modified: Fri, 29 Oct 2021 00:22:32 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.19.3-alpine`

```console
$ docker pull telegraf@sha256:8050f9c50d29badd65df08a573865728936ae4915516860eb01224b437a63639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:1.19.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:48d9e2455559384bfdb8292ea16e8784fad05c078d1a97b20e2fac3f76c72b4a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40231257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42f4fc29c84140ab896e980723eabb1e03d33d87fedc8d37ed0459a36cd4fb71`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Thu, 16 Sep 2021 21:20:06 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 03 Nov 2021 19:44:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec &&     update-ca-certificates
# Wed, 03 Nov 2021 19:44:25 GMT
ENV TELEGRAF_VERSION=1.19.3
# Wed, 03 Nov 2021 19:44:34 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Wed, 03 Nov 2021 19:44:35 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 03 Nov 2021 19:44:35 GMT
COPY file:4071aa7d94da140b944f5aaf032330509821a974e13349f4a3682e3368362128 in /entrypoint.sh 
# Wed, 03 Nov 2021 19:44:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Nov 2021 19:44:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8cf55ffd68f3512245522356168367182cfdaeb0a0d11bbd5328472d4c0761`  
		Last Modified: Thu, 16 Sep 2021 21:24:04 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc5969994ddff3cc06380d4484d56d3001e9b843686d9d8e2df71ab1a5bfb87`  
		Last Modified: Wed, 03 Nov 2021 19:45:21 GMT  
		Size: 3.4 MB (3371089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c674d9f6917a59dccf7fe51db5e6875ee47435636af3a4fe3f03603e2c9dc1`  
		Last Modified: Wed, 03 Nov 2021 19:45:57 GMT  
		Size: 34.0 MB (34045362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e835e1bef96a0bd9c6e50bc12dd87a3d7811901165945e7c16edf407c00c21b3`  
		Last Modified: Wed, 03 Nov 2021 19:45:51 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.20`

```console
$ docker pull telegraf@sha256:5208e79b72d3e1ed0b26325c9cb095b06da4c0df5503a2d9ff599bd1b51fc4cd
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
$ docker pull telegraf@sha256:b2d9ec92df08d3289dc7ce34a23c99cee81babd6b14221b8c2081a902ca482f0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.1 MB (116091043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d5b89d2ea8910d1b417d8139f5e6cbd14b8b193c8a3b16b0aff853d29911fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Oct 2021 01:41:28 GMT
ADD file:aed1709ccba6a81b9726b228fad7b81bcf4c16bafe723981ad37076322d78986 in / 
# Tue, 12 Oct 2021 01:41:29 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:59:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:59:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 16 Oct 2021 11:51:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 11:51:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 29 Oct 2021 00:21:51 GMT
ENV TELEGRAF_VERSION=1.20.3
# Fri, 29 Oct 2021 00:21:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 29 Oct 2021 00:21:56 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 29 Oct 2021 00:21:56 GMT
USER telegraf
# Fri, 29 Oct 2021 00:21:58 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Fri, 29 Oct 2021 00:21:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Oct 2021 00:21:59 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2ff6d7a9e7d73e4a01b9417518d18c001728c45fa8109ed8f55aaa50e7981482`  
		Last Modified: Tue, 12 Oct 2021 01:48:38 GMT  
		Size: 49.2 MB (49222756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7324ea4098419bc5fa2ac5a138522230bf12cef3996d1740dd00f9d4737d004`  
		Last Modified: Sat, 16 Oct 2021 03:15:37 GMT  
		Size: 7.7 MB (7695063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e213c33a07316d84d829be685bd3b02e1e2bc135f7748c932050e6ed6a3a0d3`  
		Last Modified: Sat, 16 Oct 2021 03:15:37 GMT  
		Size: 9.8 MB (9767289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195fcb7c5d1eb571a72b8f9d97c3baa030a716aa837f3e8228435b153a518cca`  
		Last Modified: Sat, 16 Oct 2021 11:52:14 GMT  
		Size: 17.1 MB (17058985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb3a6b78fdf159f9ca6b70db784a6eafd05eb4f5f46555df56c6d48d032c608`  
		Last Modified: Sat, 16 Oct 2021 11:52:11 GMT  
		Size: 2.9 KB (2879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342f7a018d235e2e6656d33f5fbdfb3a6af6c6940ef24f0b757e11e5869d7093`  
		Last Modified: Fri, 29 Oct 2021 00:22:49 GMT  
		Size: 32.3 MB (32343886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3db21a4c96c7933ddd45a2e501c529a0442c4902084502082d927893041b97`  
		Last Modified: Fri, 29 Oct 2021 00:22:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.20-alpine`

```console
$ docker pull telegraf@sha256:314108cc28917dd404d9f5f925a79ad058a5db1a6fcdfa7b7bfe6771235e5eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:1.20-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:93d6455dbb278143a257d82437c05cb956a3fd9a6bebf5b18f4b0149f5494641
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41645259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc99b10f752475d0b5baf65182c32a2caea4bac1657d72b47b84a218ab782bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Thu, 16 Sep 2021 21:20:06 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 03 Nov 2021 19:44:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec &&     update-ca-certificates
# Wed, 03 Nov 2021 19:44:41 GMT
ENV TELEGRAF_VERSION=1.20.3
# Wed, 03 Nov 2021 19:44:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Wed, 03 Nov 2021 19:44:50 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 03 Nov 2021 19:44:50 GMT
COPY file:4071aa7d94da140b944f5aaf032330509821a974e13349f4a3682e3368362128 in /entrypoint.sh 
# Wed, 03 Nov 2021 19:44:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Nov 2021 19:44:50 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8cf55ffd68f3512245522356168367182cfdaeb0a0d11bbd5328472d4c0761`  
		Last Modified: Thu, 16 Sep 2021 21:24:04 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc5969994ddff3cc06380d4484d56d3001e9b843686d9d8e2df71ab1a5bfb87`  
		Last Modified: Wed, 03 Nov 2021 19:45:21 GMT  
		Size: 3.4 MB (3371089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3f6d84ea81248992b415c62942686816e6f3afa27c6bfc47d8d4fdfcbd5b50`  
		Last Modified: Wed, 03 Nov 2021 19:46:25 GMT  
		Size: 35.5 MB (35459363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc2ae9653b2fdf734ac5e280179840f825a6d5d86db796fec9daf63e3e30de9`  
		Last Modified: Wed, 03 Nov 2021 19:46:19 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.20.3`

```console
$ docker pull telegraf@sha256:5208e79b72d3e1ed0b26325c9cb095b06da4c0df5503a2d9ff599bd1b51fc4cd
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
$ docker pull telegraf@sha256:b2d9ec92df08d3289dc7ce34a23c99cee81babd6b14221b8c2081a902ca482f0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.1 MB (116091043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d5b89d2ea8910d1b417d8139f5e6cbd14b8b193c8a3b16b0aff853d29911fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Oct 2021 01:41:28 GMT
ADD file:aed1709ccba6a81b9726b228fad7b81bcf4c16bafe723981ad37076322d78986 in / 
# Tue, 12 Oct 2021 01:41:29 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:59:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:59:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 16 Oct 2021 11:51:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 11:51:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 29 Oct 2021 00:21:51 GMT
ENV TELEGRAF_VERSION=1.20.3
# Fri, 29 Oct 2021 00:21:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 29 Oct 2021 00:21:56 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 29 Oct 2021 00:21:56 GMT
USER telegraf
# Fri, 29 Oct 2021 00:21:58 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Fri, 29 Oct 2021 00:21:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Oct 2021 00:21:59 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2ff6d7a9e7d73e4a01b9417518d18c001728c45fa8109ed8f55aaa50e7981482`  
		Last Modified: Tue, 12 Oct 2021 01:48:38 GMT  
		Size: 49.2 MB (49222756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7324ea4098419bc5fa2ac5a138522230bf12cef3996d1740dd00f9d4737d004`  
		Last Modified: Sat, 16 Oct 2021 03:15:37 GMT  
		Size: 7.7 MB (7695063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e213c33a07316d84d829be685bd3b02e1e2bc135f7748c932050e6ed6a3a0d3`  
		Last Modified: Sat, 16 Oct 2021 03:15:37 GMT  
		Size: 9.8 MB (9767289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195fcb7c5d1eb571a72b8f9d97c3baa030a716aa837f3e8228435b153a518cca`  
		Last Modified: Sat, 16 Oct 2021 11:52:14 GMT  
		Size: 17.1 MB (17058985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb3a6b78fdf159f9ca6b70db784a6eafd05eb4f5f46555df56c6d48d032c608`  
		Last Modified: Sat, 16 Oct 2021 11:52:11 GMT  
		Size: 2.9 KB (2879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342f7a018d235e2e6656d33f5fbdfb3a6af6c6940ef24f0b757e11e5869d7093`  
		Last Modified: Fri, 29 Oct 2021 00:22:49 GMT  
		Size: 32.3 MB (32343886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3db21a4c96c7933ddd45a2e501c529a0442c4902084502082d927893041b97`  
		Last Modified: Fri, 29 Oct 2021 00:22:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.20.3-alpine`

```console
$ docker pull telegraf@sha256:314108cc28917dd404d9f5f925a79ad058a5db1a6fcdfa7b7bfe6771235e5eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:1.20.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:93d6455dbb278143a257d82437c05cb956a3fd9a6bebf5b18f4b0149f5494641
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41645259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc99b10f752475d0b5baf65182c32a2caea4bac1657d72b47b84a218ab782bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Thu, 16 Sep 2021 21:20:06 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 03 Nov 2021 19:44:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec &&     update-ca-certificates
# Wed, 03 Nov 2021 19:44:41 GMT
ENV TELEGRAF_VERSION=1.20.3
# Wed, 03 Nov 2021 19:44:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Wed, 03 Nov 2021 19:44:50 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 03 Nov 2021 19:44:50 GMT
COPY file:4071aa7d94da140b944f5aaf032330509821a974e13349f4a3682e3368362128 in /entrypoint.sh 
# Wed, 03 Nov 2021 19:44:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Nov 2021 19:44:50 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8cf55ffd68f3512245522356168367182cfdaeb0a0d11bbd5328472d4c0761`  
		Last Modified: Thu, 16 Sep 2021 21:24:04 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc5969994ddff3cc06380d4484d56d3001e9b843686d9d8e2df71ab1a5bfb87`  
		Last Modified: Wed, 03 Nov 2021 19:45:21 GMT  
		Size: 3.4 MB (3371089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3f6d84ea81248992b415c62942686816e6f3afa27c6bfc47d8d4fdfcbd5b50`  
		Last Modified: Wed, 03 Nov 2021 19:46:25 GMT  
		Size: 35.5 MB (35459363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc2ae9653b2fdf734ac5e280179840f825a6d5d86db796fec9daf63e3e30de9`  
		Last Modified: Wed, 03 Nov 2021 19:46:19 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:314108cc28917dd404d9f5f925a79ad058a5db1a6fcdfa7b7bfe6771235e5eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:93d6455dbb278143a257d82437c05cb956a3fd9a6bebf5b18f4b0149f5494641
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41645259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc99b10f752475d0b5baf65182c32a2caea4bac1657d72b47b84a218ab782bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Thu, 16 Sep 2021 21:20:06 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 03 Nov 2021 19:44:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec &&     update-ca-certificates
# Wed, 03 Nov 2021 19:44:41 GMT
ENV TELEGRAF_VERSION=1.20.3
# Wed, 03 Nov 2021 19:44:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Wed, 03 Nov 2021 19:44:50 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 03 Nov 2021 19:44:50 GMT
COPY file:4071aa7d94da140b944f5aaf032330509821a974e13349f4a3682e3368362128 in /entrypoint.sh 
# Wed, 03 Nov 2021 19:44:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Nov 2021 19:44:50 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8cf55ffd68f3512245522356168367182cfdaeb0a0d11bbd5328472d4c0761`  
		Last Modified: Thu, 16 Sep 2021 21:24:04 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc5969994ddff3cc06380d4484d56d3001e9b843686d9d8e2df71ab1a5bfb87`  
		Last Modified: Wed, 03 Nov 2021 19:45:21 GMT  
		Size: 3.4 MB (3371089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3f6d84ea81248992b415c62942686816e6f3afa27c6bfc47d8d4fdfcbd5b50`  
		Last Modified: Wed, 03 Nov 2021 19:46:25 GMT  
		Size: 35.5 MB (35459363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc2ae9653b2fdf734ac5e280179840f825a6d5d86db796fec9daf63e3e30de9`  
		Last Modified: Wed, 03 Nov 2021 19:46:19 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:5208e79b72d3e1ed0b26325c9cb095b06da4c0df5503a2d9ff599bd1b51fc4cd
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
$ docker pull telegraf@sha256:b2d9ec92df08d3289dc7ce34a23c99cee81babd6b14221b8c2081a902ca482f0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.1 MB (116091043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d5b89d2ea8910d1b417d8139f5e6cbd14b8b193c8a3b16b0aff853d29911fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Oct 2021 01:41:28 GMT
ADD file:aed1709ccba6a81b9726b228fad7b81bcf4c16bafe723981ad37076322d78986 in / 
# Tue, 12 Oct 2021 01:41:29 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:59:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:59:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 16 Oct 2021 11:51:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 11:51:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 29 Oct 2021 00:21:51 GMT
ENV TELEGRAF_VERSION=1.20.3
# Fri, 29 Oct 2021 00:21:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 29 Oct 2021 00:21:56 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 29 Oct 2021 00:21:56 GMT
USER telegraf
# Fri, 29 Oct 2021 00:21:58 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Fri, 29 Oct 2021 00:21:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Oct 2021 00:21:59 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2ff6d7a9e7d73e4a01b9417518d18c001728c45fa8109ed8f55aaa50e7981482`  
		Last Modified: Tue, 12 Oct 2021 01:48:38 GMT  
		Size: 49.2 MB (49222756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7324ea4098419bc5fa2ac5a138522230bf12cef3996d1740dd00f9d4737d004`  
		Last Modified: Sat, 16 Oct 2021 03:15:37 GMT  
		Size: 7.7 MB (7695063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e213c33a07316d84d829be685bd3b02e1e2bc135f7748c932050e6ed6a3a0d3`  
		Last Modified: Sat, 16 Oct 2021 03:15:37 GMT  
		Size: 9.8 MB (9767289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195fcb7c5d1eb571a72b8f9d97c3baa030a716aa837f3e8228435b153a518cca`  
		Last Modified: Sat, 16 Oct 2021 11:52:14 GMT  
		Size: 17.1 MB (17058985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb3a6b78fdf159f9ca6b70db784a6eafd05eb4f5f46555df56c6d48d032c608`  
		Last Modified: Sat, 16 Oct 2021 11:52:11 GMT  
		Size: 2.9 KB (2879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342f7a018d235e2e6656d33f5fbdfb3a6af6c6940ef24f0b757e11e5869d7093`  
		Last Modified: Fri, 29 Oct 2021 00:22:49 GMT  
		Size: 32.3 MB (32343886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3db21a4c96c7933ddd45a2e501c529a0442c4902084502082d927893041b97`  
		Last Modified: Fri, 29 Oct 2021 00:22:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
