<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.16`](#telegraf116)
-	[`telegraf:1.16-alpine`](#telegraf116-alpine)
-	[`telegraf:1.16.3`](#telegraf1163)
-	[`telegraf:1.16.3-alpine`](#telegraf1163-alpine)
-	[`telegraf:1.17`](#telegraf117)
-	[`telegraf:1.17-alpine`](#telegraf117-alpine)
-	[`telegraf:1.17.3`](#telegraf1173)
-	[`telegraf:1.17.3-alpine`](#telegraf1173-alpine)
-	[`telegraf:1.18`](#telegraf118)
-	[`telegraf:1.18-alpine`](#telegraf118-alpine)
-	[`telegraf:1.18.0`](#telegraf1180)
-	[`telegraf:1.18.0-alpine`](#telegraf1180-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.16`

```console
$ docker pull telegraf@sha256:46519028cccc85b24917c31ebe3ff7f12c106513bab00cde97053d2b7027fe83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.16` - linux; amd64

```console
$ docker pull telegraf@sha256:69ff9fc7832b11ee75c3d194bc427c97d38bc476dee2a567dcc7df5a17ad2832
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.0 MB (108004704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e73f0d76da4595fefd0323074d374bccf8b3bf56a6e4a288f4712f1d0acee79`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:27 GMT
ADD file:575bf0d00d72810609a4118728923f11625b43de536352fe69a341086e4ebfd1 in / 
# Fri, 12 Mar 2021 02:20:28 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:49:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:49:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 13 Mar 2021 04:21:53 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Sat, 13 Mar 2021 04:21:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 13 Mar 2021 04:22:16 GMT
ENV TELEGRAF_VERSION=1.16.3
# Sat, 13 Mar 2021 04:22:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Sat, 13 Mar 2021 04:22:19 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 13 Mar 2021 04:22:19 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Sat, 13 Mar 2021 04:22:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 13 Mar 2021 04:22:20 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e22122b926a1a853d61887fa35c3fe53e05ee7dc0f2f488936dc9838bd0e230d`  
		Last Modified: Fri, 12 Mar 2021 02:25:38 GMT  
		Size: 50.4 MB (50400353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29e09ae83733d697508e34827538cc0129b8719b85db943041c5d37287bcb81`  
		Last Modified: Fri, 12 Mar 2021 03:19:09 GMT  
		Size: 7.8 MB (7832474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e319e3daef68c36099bf3b534377a78d373f67bde3d156119c2463f5fe133ac5`  
		Last Modified: Fri, 12 Mar 2021 03:19:09 GMT  
		Size: 10.0 MB (9997147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78656f24469046aafcacf134dd6459f23b9332602a90a66a866ad5e65040fe4d`  
		Last Modified: Sat, 13 Mar 2021 04:23:18 GMT  
		Size: 17.4 MB (17414412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb405ad31ae4d29bd8710887a1e3837a2c576d4f3c53e14313c94282fa7ff86`  
		Last Modified: Sat, 13 Mar 2021 04:23:14 GMT  
		Size: 2.9 KB (2897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c01d42ab387b0c43c5d6a3ada3a3eff396c5d68eb90e444a1909ed156477ecd`  
		Last Modified: Sat, 13 Mar 2021 04:23:50 GMT  
		Size: 22.4 MB (22357237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e40937cecef302f740fd2c458a35adba0d6d95045802a9a1e47104c58a22340`  
		Last Modified: Sat, 13 Mar 2021 04:23:44 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.16` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:eef1919dbecbd86cdf81c6c4c70b858eb515423925cab1030b90ba70e40e2c3b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99387772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071a4477fe909d14a6390515921735781165e5879e57bca5bc632daa20cefa8b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 12 Mar 2021 01:59:39 GMT
ADD file:7a272c0a2bf029fde32186ff5d55a8ef335d159da9770327eedf010bd6e6c42d in / 
# Fri, 12 Mar 2021 01:59:44 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 03:32:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 03:32:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 20:12:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 20:12:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 12 Mar 2021 20:12:24 GMT
ENV TELEGRAF_VERSION=1.16.3
# Fri, 12 Mar 2021 20:12:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 12 Mar 2021 20:12:30 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 12 Mar 2021 20:12:31 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Fri, 12 Mar 2021 20:12:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 20:12:33 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:199f83f6a2f5a375b8f94d3025f9bbdaca75f4ca46ad0aab2061c331588fa662`  
		Last Modified: Fri, 12 Mar 2021 02:10:00 GMT  
		Size: 45.9 MB (45868120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d535c087e97eba956c56d41b509048f3f9283744c2b2ef7fabbb6a75fe7d3c`  
		Last Modified: Fri, 12 Mar 2021 03:47:04 GMT  
		Size: 7.1 MB (7123778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7cfc4c570eb98f73a8ab1d871e36ff43492038fa4c0279c70ccff1797447d2b`  
		Last Modified: Fri, 12 Mar 2021 03:47:04 GMT  
		Size: 9.3 MB (9343577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5bf068baebd708e3761ed06f179f64325dccfa420b559b02ebc09bae2c0fda`  
		Last Modified: Fri, 12 Mar 2021 20:13:13 GMT  
		Size: 16.2 MB (16159151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3c1f8007e854e0bd2b8c67586814d6cbb8f27c595193f97f169d521f6c1ab4`  
		Last Modified: Fri, 12 Mar 2021 20:13:07 GMT  
		Size: 2.9 KB (2898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a4a6243bd5056db242128a66e7c3b21eab857f74c5021ed4ceb021b681aa78`  
		Last Modified: Fri, 12 Mar 2021 20:13:28 GMT  
		Size: 20.9 MB (20890063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40fddb4b5bfd5ffc9cb56ed4589d1f1ab42a3c16198911fe2a68c1e1bfd722c`  
		Last Modified: Fri, 12 Mar 2021 20:13:21 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.16` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:8e1fb0dc5d172506b6fac1fc8b3bd2185dab22dc8300a8dc53f764647db4fbdf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104641505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19aec1c07898d0f439f6e9da6e9a7c318b56ebe780fbe62b2db30d454555ec35`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 12 Mar 2021 01:53:16 GMT
ADD file:b2e2cca51e131b97e6a7e02af893c7f9b1f7a491b3d5fdaafa80409ed248a706 in / 
# Fri, 12 Mar 2021 01:53:20 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:29:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:29:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 23:37:57 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 23:38:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 12 Mar 2021 23:38:22 GMT
ENV TELEGRAF_VERSION=1.16.3
# Fri, 12 Mar 2021 23:38:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 12 Mar 2021 23:38:33 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 12 Mar 2021 23:38:35 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Fri, 12 Mar 2021 23:38:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 23:38:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e9742a63e95a88f8685c4f23a73f7dd15e4039ac1862ce5753c53406a5f7c04a`  
		Last Modified: Fri, 12 Mar 2021 02:01:14 GMT  
		Size: 49.2 MB (49195763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90273c85fdda8648cee9282aa7b01faf0ec1f45451931985b3504c37cf1ac3e6`  
		Last Modified: Fri, 12 Mar 2021 02:43:30 GMT  
		Size: 7.7 MB (7694407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685f873e984153af9a44cf556c7679b430b9c557d901c7d476725134f28754e7`  
		Last Modified: Fri, 12 Mar 2021 02:43:30 GMT  
		Size: 10.0 MB (9984339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67be13eac316a9bb534db0eeff7686c2ec2ba9e0e02d4544b9d206c7275ed54`  
		Last Modified: Fri, 12 Mar 2021 23:39:13 GMT  
		Size: 17.3 MB (17269554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682c14900e4723e4a455cc93b301b78b3177a23356e5d5b7a424a39c0ceb3ea9`  
		Last Modified: Fri, 12 Mar 2021 23:39:08 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637cac2704406cad0d1fc2c17c2dd416cb648619da56e0a36d341b8cf7b1e3f9`  
		Last Modified: Fri, 12 Mar 2021 23:39:32 GMT  
		Size: 20.5 MB (20494359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832bd51da166654b1f517edbc82a52b8961c334bf3ca17171a53f978345f8ca9`  
		Last Modified: Fri, 12 Mar 2021 23:39:26 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.16-alpine`

```console
$ docker pull telegraf@sha256:5d4bcb2eac33f3cf1d1469ed4cfbad2570b444b7eb7aa6b73f3b2abb9960273c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.16-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:8706e0fab623055407a6fc0932ef6a906d9590a4b2a1ed2811b51c654bb4f9cf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 MB (28314743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7fd3363208ec323b5f17118403b6d74c7eda15c6dda9a77b45613660c6f6f2a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Fri, 12 Mar 2021 03:37:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Mar 2021 04:22:25 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Sat, 13 Mar 2021 04:22:25 GMT
ENV TELEGRAF_VERSION=1.16.3
# Sat, 13 Mar 2021 04:22:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 13 Mar 2021 04:22:31 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 13 Mar 2021 04:22:31 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Sat, 13 Mar 2021 04:22:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 13 Mar 2021 04:22:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bab45d475695400229b7b704d7c3a4a6f326f0eb1299894f67d202fbaf5a331`  
		Last Modified: Fri, 12 Mar 2021 03:39:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646312e5d4a840c82a7cb31726398ff761aef46aa9c78a9b689d1e1d4615c3b6`  
		Last Modified: Sat, 13 Mar 2021 04:24:01 GMT  
		Size: 3.3 MB (3300514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdda767aa1389ed7e955f4e37c1429559f6b063abebc24956bbf43b089b2e915`  
		Last Modified: Sat, 13 Mar 2021 04:24:05 GMT  
		Size: 22.2 MB (22214398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f90d9e5e2006bd02b388d5ef6d71889de6552357d024e13adcded3bbd219b96`  
		Last Modified: Sat, 13 Mar 2021 04:24:00 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.16.3`

```console
$ docker pull telegraf@sha256:46519028cccc85b24917c31ebe3ff7f12c106513bab00cde97053d2b7027fe83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.16.3` - linux; amd64

```console
$ docker pull telegraf@sha256:69ff9fc7832b11ee75c3d194bc427c97d38bc476dee2a567dcc7df5a17ad2832
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.0 MB (108004704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e73f0d76da4595fefd0323074d374bccf8b3bf56a6e4a288f4712f1d0acee79`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:27 GMT
ADD file:575bf0d00d72810609a4118728923f11625b43de536352fe69a341086e4ebfd1 in / 
# Fri, 12 Mar 2021 02:20:28 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:49:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:49:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 13 Mar 2021 04:21:53 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Sat, 13 Mar 2021 04:21:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 13 Mar 2021 04:22:16 GMT
ENV TELEGRAF_VERSION=1.16.3
# Sat, 13 Mar 2021 04:22:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Sat, 13 Mar 2021 04:22:19 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 13 Mar 2021 04:22:19 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Sat, 13 Mar 2021 04:22:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 13 Mar 2021 04:22:20 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e22122b926a1a853d61887fa35c3fe53e05ee7dc0f2f488936dc9838bd0e230d`  
		Last Modified: Fri, 12 Mar 2021 02:25:38 GMT  
		Size: 50.4 MB (50400353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29e09ae83733d697508e34827538cc0129b8719b85db943041c5d37287bcb81`  
		Last Modified: Fri, 12 Mar 2021 03:19:09 GMT  
		Size: 7.8 MB (7832474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e319e3daef68c36099bf3b534377a78d373f67bde3d156119c2463f5fe133ac5`  
		Last Modified: Fri, 12 Mar 2021 03:19:09 GMT  
		Size: 10.0 MB (9997147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78656f24469046aafcacf134dd6459f23b9332602a90a66a866ad5e65040fe4d`  
		Last Modified: Sat, 13 Mar 2021 04:23:18 GMT  
		Size: 17.4 MB (17414412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb405ad31ae4d29bd8710887a1e3837a2c576d4f3c53e14313c94282fa7ff86`  
		Last Modified: Sat, 13 Mar 2021 04:23:14 GMT  
		Size: 2.9 KB (2897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c01d42ab387b0c43c5d6a3ada3a3eff396c5d68eb90e444a1909ed156477ecd`  
		Last Modified: Sat, 13 Mar 2021 04:23:50 GMT  
		Size: 22.4 MB (22357237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e40937cecef302f740fd2c458a35adba0d6d95045802a9a1e47104c58a22340`  
		Last Modified: Sat, 13 Mar 2021 04:23:44 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.16.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:eef1919dbecbd86cdf81c6c4c70b858eb515423925cab1030b90ba70e40e2c3b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99387772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071a4477fe909d14a6390515921735781165e5879e57bca5bc632daa20cefa8b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 12 Mar 2021 01:59:39 GMT
ADD file:7a272c0a2bf029fde32186ff5d55a8ef335d159da9770327eedf010bd6e6c42d in / 
# Fri, 12 Mar 2021 01:59:44 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 03:32:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 03:32:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 20:12:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 20:12:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 12 Mar 2021 20:12:24 GMT
ENV TELEGRAF_VERSION=1.16.3
# Fri, 12 Mar 2021 20:12:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 12 Mar 2021 20:12:30 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 12 Mar 2021 20:12:31 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Fri, 12 Mar 2021 20:12:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 20:12:33 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:199f83f6a2f5a375b8f94d3025f9bbdaca75f4ca46ad0aab2061c331588fa662`  
		Last Modified: Fri, 12 Mar 2021 02:10:00 GMT  
		Size: 45.9 MB (45868120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d535c087e97eba956c56d41b509048f3f9283744c2b2ef7fabbb6a75fe7d3c`  
		Last Modified: Fri, 12 Mar 2021 03:47:04 GMT  
		Size: 7.1 MB (7123778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7cfc4c570eb98f73a8ab1d871e36ff43492038fa4c0279c70ccff1797447d2b`  
		Last Modified: Fri, 12 Mar 2021 03:47:04 GMT  
		Size: 9.3 MB (9343577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5bf068baebd708e3761ed06f179f64325dccfa420b559b02ebc09bae2c0fda`  
		Last Modified: Fri, 12 Mar 2021 20:13:13 GMT  
		Size: 16.2 MB (16159151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3c1f8007e854e0bd2b8c67586814d6cbb8f27c595193f97f169d521f6c1ab4`  
		Last Modified: Fri, 12 Mar 2021 20:13:07 GMT  
		Size: 2.9 KB (2898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a4a6243bd5056db242128a66e7c3b21eab857f74c5021ed4ceb021b681aa78`  
		Last Modified: Fri, 12 Mar 2021 20:13:28 GMT  
		Size: 20.9 MB (20890063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40fddb4b5bfd5ffc9cb56ed4589d1f1ab42a3c16198911fe2a68c1e1bfd722c`  
		Last Modified: Fri, 12 Mar 2021 20:13:21 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.16.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:8e1fb0dc5d172506b6fac1fc8b3bd2185dab22dc8300a8dc53f764647db4fbdf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104641505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19aec1c07898d0f439f6e9da6e9a7c318b56ebe780fbe62b2db30d454555ec35`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 12 Mar 2021 01:53:16 GMT
ADD file:b2e2cca51e131b97e6a7e02af893c7f9b1f7a491b3d5fdaafa80409ed248a706 in / 
# Fri, 12 Mar 2021 01:53:20 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:29:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:29:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 23:37:57 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 23:38:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 12 Mar 2021 23:38:22 GMT
ENV TELEGRAF_VERSION=1.16.3
# Fri, 12 Mar 2021 23:38:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 12 Mar 2021 23:38:33 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 12 Mar 2021 23:38:35 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Fri, 12 Mar 2021 23:38:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 23:38:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e9742a63e95a88f8685c4f23a73f7dd15e4039ac1862ce5753c53406a5f7c04a`  
		Last Modified: Fri, 12 Mar 2021 02:01:14 GMT  
		Size: 49.2 MB (49195763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90273c85fdda8648cee9282aa7b01faf0ec1f45451931985b3504c37cf1ac3e6`  
		Last Modified: Fri, 12 Mar 2021 02:43:30 GMT  
		Size: 7.7 MB (7694407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685f873e984153af9a44cf556c7679b430b9c557d901c7d476725134f28754e7`  
		Last Modified: Fri, 12 Mar 2021 02:43:30 GMT  
		Size: 10.0 MB (9984339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67be13eac316a9bb534db0eeff7686c2ec2ba9e0e02d4544b9d206c7275ed54`  
		Last Modified: Fri, 12 Mar 2021 23:39:13 GMT  
		Size: 17.3 MB (17269554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682c14900e4723e4a455cc93b301b78b3177a23356e5d5b7a424a39c0ceb3ea9`  
		Last Modified: Fri, 12 Mar 2021 23:39:08 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637cac2704406cad0d1fc2c17c2dd416cb648619da56e0a36d341b8cf7b1e3f9`  
		Last Modified: Fri, 12 Mar 2021 23:39:32 GMT  
		Size: 20.5 MB (20494359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832bd51da166654b1f517edbc82a52b8961c334bf3ca17171a53f978345f8ca9`  
		Last Modified: Fri, 12 Mar 2021 23:39:26 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.16.3-alpine`

```console
$ docker pull telegraf@sha256:5d4bcb2eac33f3cf1d1469ed4cfbad2570b444b7eb7aa6b73f3b2abb9960273c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.16.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:8706e0fab623055407a6fc0932ef6a906d9590a4b2a1ed2811b51c654bb4f9cf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 MB (28314743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7fd3363208ec323b5f17118403b6d74c7eda15c6dda9a77b45613660c6f6f2a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Fri, 12 Mar 2021 03:37:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Mar 2021 04:22:25 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Sat, 13 Mar 2021 04:22:25 GMT
ENV TELEGRAF_VERSION=1.16.3
# Sat, 13 Mar 2021 04:22:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 13 Mar 2021 04:22:31 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 13 Mar 2021 04:22:31 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Sat, 13 Mar 2021 04:22:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 13 Mar 2021 04:22:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bab45d475695400229b7b704d7c3a4a6f326f0eb1299894f67d202fbaf5a331`  
		Last Modified: Fri, 12 Mar 2021 03:39:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646312e5d4a840c82a7cb31726398ff761aef46aa9c78a9b689d1e1d4615c3b6`  
		Last Modified: Sat, 13 Mar 2021 04:24:01 GMT  
		Size: 3.3 MB (3300514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdda767aa1389ed7e955f4e37c1429559f6b063abebc24956bbf43b089b2e915`  
		Last Modified: Sat, 13 Mar 2021 04:24:05 GMT  
		Size: 22.2 MB (22214398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f90d9e5e2006bd02b388d5ef6d71889de6552357d024e13adcded3bbd219b96`  
		Last Modified: Sat, 13 Mar 2021 04:24:00 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.17`

```console
$ docker pull telegraf@sha256:80551afb26482363bac6f17d9c1da57aefa2d0e5443d87ad6ec4e79c9c75bca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.17` - linux; amd64

```console
$ docker pull telegraf@sha256:a2e6c6d5452cdc92726266f112ac3159ddd0546d29c46322ad176e8844369a4c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.6 MB (108606317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6dbb36abe4fa49b3920eb1b492e1ceaf9d8bf8446aed091f93e33f16d466fb9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:27 GMT
ADD file:575bf0d00d72810609a4118728923f11625b43de536352fe69a341086e4ebfd1 in / 
# Fri, 12 Mar 2021 02:20:28 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:49:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:49:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 13 Mar 2021 04:21:53 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Sat, 13 Mar 2021 04:21:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 13 Mar 2021 04:22:35 GMT
ENV TELEGRAF_VERSION=1.17.3
# Sat, 13 Mar 2021 04:22:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Sat, 13 Mar 2021 04:22:38 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 13 Mar 2021 04:22:38 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Sat, 13 Mar 2021 04:22:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 13 Mar 2021 04:22:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e22122b926a1a853d61887fa35c3fe53e05ee7dc0f2f488936dc9838bd0e230d`  
		Last Modified: Fri, 12 Mar 2021 02:25:38 GMT  
		Size: 50.4 MB (50400353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29e09ae83733d697508e34827538cc0129b8719b85db943041c5d37287bcb81`  
		Last Modified: Fri, 12 Mar 2021 03:19:09 GMT  
		Size: 7.8 MB (7832474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e319e3daef68c36099bf3b534377a78d373f67bde3d156119c2463f5fe133ac5`  
		Last Modified: Fri, 12 Mar 2021 03:19:09 GMT  
		Size: 10.0 MB (9997147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78656f24469046aafcacf134dd6459f23b9332602a90a66a866ad5e65040fe4d`  
		Last Modified: Sat, 13 Mar 2021 04:23:18 GMT  
		Size: 17.4 MB (17414412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb405ad31ae4d29bd8710887a1e3837a2c576d4f3c53e14313c94282fa7ff86`  
		Last Modified: Sat, 13 Mar 2021 04:23:14 GMT  
		Size: 2.9 KB (2897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90d1346a633f7ce1b175356432fe501fae451e63f735e93a6206fee5c51688b`  
		Last Modified: Sat, 13 Mar 2021 04:24:25 GMT  
		Size: 23.0 MB (22958852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c1ed4b20ccee9a4f361a7157c833959e2d757aab87982272fd199890a27ab0`  
		Last Modified: Sat, 13 Mar 2021 04:24:16 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.17` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:263dd467b4162bafbfeda58537abf7bea1ac2dfdbef1797dbecab4c8e476deb7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.0 MB (99956323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7389058e26423a70d53419877b10adb0e7ff879d9c4affc60f132f64bda6c456`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 12 Mar 2021 01:59:39 GMT
ADD file:7a272c0a2bf029fde32186ff5d55a8ef335d159da9770327eedf010bd6e6c42d in / 
# Fri, 12 Mar 2021 01:59:44 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 03:32:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 03:32:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 20:12:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 20:12:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 12 Mar 2021 20:12:41 GMT
ENV TELEGRAF_VERSION=1.17.3
# Fri, 12 Mar 2021 20:12:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 12 Mar 2021 20:12:49 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 12 Mar 2021 20:12:49 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Fri, 12 Mar 2021 20:12:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 20:12:52 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:199f83f6a2f5a375b8f94d3025f9bbdaca75f4ca46ad0aab2061c331588fa662`  
		Last Modified: Fri, 12 Mar 2021 02:10:00 GMT  
		Size: 45.9 MB (45868120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d535c087e97eba956c56d41b509048f3f9283744c2b2ef7fabbb6a75fe7d3c`  
		Last Modified: Fri, 12 Mar 2021 03:47:04 GMT  
		Size: 7.1 MB (7123778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7cfc4c570eb98f73a8ab1d871e36ff43492038fa4c0279c70ccff1797447d2b`  
		Last Modified: Fri, 12 Mar 2021 03:47:04 GMT  
		Size: 9.3 MB (9343577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5bf068baebd708e3761ed06f179f64325dccfa420b559b02ebc09bae2c0fda`  
		Last Modified: Fri, 12 Mar 2021 20:13:13 GMT  
		Size: 16.2 MB (16159151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3c1f8007e854e0bd2b8c67586814d6cbb8f27c595193f97f169d521f6c1ab4`  
		Last Modified: Fri, 12 Mar 2021 20:13:07 GMT  
		Size: 2.9 KB (2898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7630478e0515fa11599fd72dd7b6d2a1bfa011d70a49e27235498852083fc0`  
		Last Modified: Fri, 12 Mar 2021 20:13:41 GMT  
		Size: 21.5 MB (21458614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a8c477efdfaf28423896e5993790ac972447c1ac46e8de9c8ac7a25a7df140`  
		Last Modified: Fri, 12 Mar 2021 20:13:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.17` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:31eb33b32fe96db75c8a453569f2dfd117e81e2cd8cdf1cf7f5094184ee4005f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105198867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d9bf8b621ad202c01db78d7ce4ab40def93747632bba3201e2d488905dc236`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 12 Mar 2021 01:53:16 GMT
ADD file:b2e2cca51e131b97e6a7e02af893c7f9b1f7a491b3d5fdaafa80409ed248a706 in / 
# Fri, 12 Mar 2021 01:53:20 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:29:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:29:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 23:37:57 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 23:38:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 12 Mar 2021 23:38:43 GMT
ENV TELEGRAF_VERSION=1.17.3
# Fri, 12 Mar 2021 23:38:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 12 Mar 2021 23:38:50 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 12 Mar 2021 23:38:51 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Fri, 12 Mar 2021 23:38:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 23:38:52 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e9742a63e95a88f8685c4f23a73f7dd15e4039ac1862ce5753c53406a5f7c04a`  
		Last Modified: Fri, 12 Mar 2021 02:01:14 GMT  
		Size: 49.2 MB (49195763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90273c85fdda8648cee9282aa7b01faf0ec1f45451931985b3504c37cf1ac3e6`  
		Last Modified: Fri, 12 Mar 2021 02:43:30 GMT  
		Size: 7.7 MB (7694407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685f873e984153af9a44cf556c7679b430b9c557d901c7d476725134f28754e7`  
		Last Modified: Fri, 12 Mar 2021 02:43:30 GMT  
		Size: 10.0 MB (9984339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67be13eac316a9bb534db0eeff7686c2ec2ba9e0e02d4544b9d206c7275ed54`  
		Last Modified: Fri, 12 Mar 2021 23:39:13 GMT  
		Size: 17.3 MB (17269554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682c14900e4723e4a455cc93b301b78b3177a23356e5d5b7a424a39c0ceb3ea9`  
		Last Modified: Fri, 12 Mar 2021 23:39:08 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707ab646b5c4ccc1f7b6971b38ef5247f5a4d0e19264e980e49e6f15d79c164a`  
		Last Modified: Fri, 12 Mar 2021 23:39:44 GMT  
		Size: 21.1 MB (21051722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d515b3cdba841f30e13c7f0b0d1a74fefcd1cba504538af82b67aa81fe58fb10`  
		Last Modified: Fri, 12 Mar 2021 23:39:38 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.17-alpine`

```console
$ docker pull telegraf@sha256:e38aa684ed3e8f8236d5820701238e5737adaf3707df46cb19c2f96b2986f40c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.17-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:bc3a75f0184a9ed5f0488c2b3a1fd6a8bacfefb20e1ba7fd1ebddf9fc6fbcd51
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28921279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5919a2c3ba0682c9880189c23669d8cc5f4b12b0cb48e6239bbc8b01911b04ec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Fri, 12 Mar 2021 03:37:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Mar 2021 04:22:25 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Sat, 13 Mar 2021 04:22:42 GMT
ENV TELEGRAF_VERSION=1.17.3
# Sat, 13 Mar 2021 04:22:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 13 Mar 2021 04:22:51 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 13 Mar 2021 04:22:51 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Sat, 13 Mar 2021 04:22:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 13 Mar 2021 04:22:51 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bab45d475695400229b7b704d7c3a4a6f326f0eb1299894f67d202fbaf5a331`  
		Last Modified: Fri, 12 Mar 2021 03:39:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646312e5d4a840c82a7cb31726398ff761aef46aa9c78a9b689d1e1d4615c3b6`  
		Last Modified: Sat, 13 Mar 2021 04:24:01 GMT  
		Size: 3.3 MB (3300514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e2264b39335e3e2c8ec6c02f8cb5c585add6cbdb198d454f56e4547cab35cd`  
		Last Modified: Sat, 13 Mar 2021 04:24:43 GMT  
		Size: 22.8 MB (22820935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13aaeb1f6df15757368e85d1419153daf1f43d5114743349c6f0dd27a01fcb6`  
		Last Modified: Sat, 13 Mar 2021 04:24:38 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.17.3`

```console
$ docker pull telegraf@sha256:80551afb26482363bac6f17d9c1da57aefa2d0e5443d87ad6ec4e79c9c75bca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.17.3` - linux; amd64

```console
$ docker pull telegraf@sha256:a2e6c6d5452cdc92726266f112ac3159ddd0546d29c46322ad176e8844369a4c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.6 MB (108606317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6dbb36abe4fa49b3920eb1b492e1ceaf9d8bf8446aed091f93e33f16d466fb9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:27 GMT
ADD file:575bf0d00d72810609a4118728923f11625b43de536352fe69a341086e4ebfd1 in / 
# Fri, 12 Mar 2021 02:20:28 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:49:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:49:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 13 Mar 2021 04:21:53 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Sat, 13 Mar 2021 04:21:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 13 Mar 2021 04:22:35 GMT
ENV TELEGRAF_VERSION=1.17.3
# Sat, 13 Mar 2021 04:22:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Sat, 13 Mar 2021 04:22:38 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 13 Mar 2021 04:22:38 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Sat, 13 Mar 2021 04:22:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 13 Mar 2021 04:22:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e22122b926a1a853d61887fa35c3fe53e05ee7dc0f2f488936dc9838bd0e230d`  
		Last Modified: Fri, 12 Mar 2021 02:25:38 GMT  
		Size: 50.4 MB (50400353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29e09ae83733d697508e34827538cc0129b8719b85db943041c5d37287bcb81`  
		Last Modified: Fri, 12 Mar 2021 03:19:09 GMT  
		Size: 7.8 MB (7832474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e319e3daef68c36099bf3b534377a78d373f67bde3d156119c2463f5fe133ac5`  
		Last Modified: Fri, 12 Mar 2021 03:19:09 GMT  
		Size: 10.0 MB (9997147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78656f24469046aafcacf134dd6459f23b9332602a90a66a866ad5e65040fe4d`  
		Last Modified: Sat, 13 Mar 2021 04:23:18 GMT  
		Size: 17.4 MB (17414412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb405ad31ae4d29bd8710887a1e3837a2c576d4f3c53e14313c94282fa7ff86`  
		Last Modified: Sat, 13 Mar 2021 04:23:14 GMT  
		Size: 2.9 KB (2897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90d1346a633f7ce1b175356432fe501fae451e63f735e93a6206fee5c51688b`  
		Last Modified: Sat, 13 Mar 2021 04:24:25 GMT  
		Size: 23.0 MB (22958852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c1ed4b20ccee9a4f361a7157c833959e2d757aab87982272fd199890a27ab0`  
		Last Modified: Sat, 13 Mar 2021 04:24:16 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.17.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:263dd467b4162bafbfeda58537abf7bea1ac2dfdbef1797dbecab4c8e476deb7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.0 MB (99956323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7389058e26423a70d53419877b10adb0e7ff879d9c4affc60f132f64bda6c456`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 12 Mar 2021 01:59:39 GMT
ADD file:7a272c0a2bf029fde32186ff5d55a8ef335d159da9770327eedf010bd6e6c42d in / 
# Fri, 12 Mar 2021 01:59:44 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 03:32:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 03:32:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 20:12:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 20:12:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 12 Mar 2021 20:12:41 GMT
ENV TELEGRAF_VERSION=1.17.3
# Fri, 12 Mar 2021 20:12:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 12 Mar 2021 20:12:49 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 12 Mar 2021 20:12:49 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Fri, 12 Mar 2021 20:12:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 20:12:52 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:199f83f6a2f5a375b8f94d3025f9bbdaca75f4ca46ad0aab2061c331588fa662`  
		Last Modified: Fri, 12 Mar 2021 02:10:00 GMT  
		Size: 45.9 MB (45868120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d535c087e97eba956c56d41b509048f3f9283744c2b2ef7fabbb6a75fe7d3c`  
		Last Modified: Fri, 12 Mar 2021 03:47:04 GMT  
		Size: 7.1 MB (7123778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7cfc4c570eb98f73a8ab1d871e36ff43492038fa4c0279c70ccff1797447d2b`  
		Last Modified: Fri, 12 Mar 2021 03:47:04 GMT  
		Size: 9.3 MB (9343577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5bf068baebd708e3761ed06f179f64325dccfa420b559b02ebc09bae2c0fda`  
		Last Modified: Fri, 12 Mar 2021 20:13:13 GMT  
		Size: 16.2 MB (16159151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3c1f8007e854e0bd2b8c67586814d6cbb8f27c595193f97f169d521f6c1ab4`  
		Last Modified: Fri, 12 Mar 2021 20:13:07 GMT  
		Size: 2.9 KB (2898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7630478e0515fa11599fd72dd7b6d2a1bfa011d70a49e27235498852083fc0`  
		Last Modified: Fri, 12 Mar 2021 20:13:41 GMT  
		Size: 21.5 MB (21458614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a8c477efdfaf28423896e5993790ac972447c1ac46e8de9c8ac7a25a7df140`  
		Last Modified: Fri, 12 Mar 2021 20:13:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.17.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:31eb33b32fe96db75c8a453569f2dfd117e81e2cd8cdf1cf7f5094184ee4005f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105198867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d9bf8b621ad202c01db78d7ce4ab40def93747632bba3201e2d488905dc236`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 12 Mar 2021 01:53:16 GMT
ADD file:b2e2cca51e131b97e6a7e02af893c7f9b1f7a491b3d5fdaafa80409ed248a706 in / 
# Fri, 12 Mar 2021 01:53:20 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:29:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:29:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 23:37:57 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 23:38:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 12 Mar 2021 23:38:43 GMT
ENV TELEGRAF_VERSION=1.17.3
# Fri, 12 Mar 2021 23:38:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 12 Mar 2021 23:38:50 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 12 Mar 2021 23:38:51 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Fri, 12 Mar 2021 23:38:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 23:38:52 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e9742a63e95a88f8685c4f23a73f7dd15e4039ac1862ce5753c53406a5f7c04a`  
		Last Modified: Fri, 12 Mar 2021 02:01:14 GMT  
		Size: 49.2 MB (49195763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90273c85fdda8648cee9282aa7b01faf0ec1f45451931985b3504c37cf1ac3e6`  
		Last Modified: Fri, 12 Mar 2021 02:43:30 GMT  
		Size: 7.7 MB (7694407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685f873e984153af9a44cf556c7679b430b9c557d901c7d476725134f28754e7`  
		Last Modified: Fri, 12 Mar 2021 02:43:30 GMT  
		Size: 10.0 MB (9984339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67be13eac316a9bb534db0eeff7686c2ec2ba9e0e02d4544b9d206c7275ed54`  
		Last Modified: Fri, 12 Mar 2021 23:39:13 GMT  
		Size: 17.3 MB (17269554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682c14900e4723e4a455cc93b301b78b3177a23356e5d5b7a424a39c0ceb3ea9`  
		Last Modified: Fri, 12 Mar 2021 23:39:08 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707ab646b5c4ccc1f7b6971b38ef5247f5a4d0e19264e980e49e6f15d79c164a`  
		Last Modified: Fri, 12 Mar 2021 23:39:44 GMT  
		Size: 21.1 MB (21051722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d515b3cdba841f30e13c7f0b0d1a74fefcd1cba504538af82b67aa81fe58fb10`  
		Last Modified: Fri, 12 Mar 2021 23:39:38 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.17.3-alpine`

```console
$ docker pull telegraf@sha256:e38aa684ed3e8f8236d5820701238e5737adaf3707df46cb19c2f96b2986f40c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.17.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:bc3a75f0184a9ed5f0488c2b3a1fd6a8bacfefb20e1ba7fd1ebddf9fc6fbcd51
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28921279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5919a2c3ba0682c9880189c23669d8cc5f4b12b0cb48e6239bbc8b01911b04ec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Fri, 12 Mar 2021 03:37:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Mar 2021 04:22:25 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Sat, 13 Mar 2021 04:22:42 GMT
ENV TELEGRAF_VERSION=1.17.3
# Sat, 13 Mar 2021 04:22:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 13 Mar 2021 04:22:51 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 13 Mar 2021 04:22:51 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Sat, 13 Mar 2021 04:22:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 13 Mar 2021 04:22:51 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bab45d475695400229b7b704d7c3a4a6f326f0eb1299894f67d202fbaf5a331`  
		Last Modified: Fri, 12 Mar 2021 03:39:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646312e5d4a840c82a7cb31726398ff761aef46aa9c78a9b689d1e1d4615c3b6`  
		Last Modified: Sat, 13 Mar 2021 04:24:01 GMT  
		Size: 3.3 MB (3300514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e2264b39335e3e2c8ec6c02f8cb5c585add6cbdb198d454f56e4547cab35cd`  
		Last Modified: Sat, 13 Mar 2021 04:24:43 GMT  
		Size: 22.8 MB (22820935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13aaeb1f6df15757368e85d1419153daf1f43d5114743349c6f0dd27a01fcb6`  
		Last Modified: Sat, 13 Mar 2021 04:24:38 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.18`

```console
$ docker pull telegraf@sha256:f70b6208076ea423adbf560419fbf02e54d5d139f18b832c05916d82d045a8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.18` - linux; amd64

```console
$ docker pull telegraf@sha256:460a896574533bf2974b952d9f1b817adccb42bba82dd35415f225fa97a965e0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 MB (111343492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6fcc27083d05669cf5233e865588e1bbeef1df6f97828918f080e97092e7079`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:27 GMT
ADD file:575bf0d00d72810609a4118728923f11625b43de536352fe69a341086e4ebfd1 in / 
# Fri, 12 Mar 2021 02:20:28 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:49:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:49:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 13 Mar 2021 04:21:53 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Sat, 13 Mar 2021 04:21:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 18 Mar 2021 01:28:30 GMT
ENV TELEGRAF_VERSION=1.18.0
# Thu, 18 Mar 2021 01:28:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 18 Mar 2021 01:28:36 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 18 Mar 2021 01:28:36 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Thu, 18 Mar 2021 01:28:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Mar 2021 01:28:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e22122b926a1a853d61887fa35c3fe53e05ee7dc0f2f488936dc9838bd0e230d`  
		Last Modified: Fri, 12 Mar 2021 02:25:38 GMT  
		Size: 50.4 MB (50400353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29e09ae83733d697508e34827538cc0129b8719b85db943041c5d37287bcb81`  
		Last Modified: Fri, 12 Mar 2021 03:19:09 GMT  
		Size: 7.8 MB (7832474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e319e3daef68c36099bf3b534377a78d373f67bde3d156119c2463f5fe133ac5`  
		Last Modified: Fri, 12 Mar 2021 03:19:09 GMT  
		Size: 10.0 MB (9997147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78656f24469046aafcacf134dd6459f23b9332602a90a66a866ad5e65040fe4d`  
		Last Modified: Sat, 13 Mar 2021 04:23:18 GMT  
		Size: 17.4 MB (17414412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb405ad31ae4d29bd8710887a1e3837a2c576d4f3c53e14313c94282fa7ff86`  
		Last Modified: Sat, 13 Mar 2021 04:23:14 GMT  
		Size: 2.9 KB (2897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813d826ac3831059bd29266b49495022b5a40f498501661b2ac757520c263f87`  
		Last Modified: Thu, 18 Mar 2021 01:29:15 GMT  
		Size: 25.7 MB (25696025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fa2dfd32cd8435a93001130e6aa2db89de174c5384895bf57aabcaa86652837`  
		Last Modified: Thu, 18 Mar 2021 01:29:10 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.18` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:7ef2475e0eacb99af604e039a53548c15109b8798d47bb614a5afb78f3003343
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102268008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5f3a2a08dfba5132a6485b89906b596a4fa08d679362979a214bbfd66320ec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 12 Mar 2021 01:59:39 GMT
ADD file:7a272c0a2bf029fde32186ff5d55a8ef335d159da9770327eedf010bd6e6c42d in / 
# Fri, 12 Mar 2021 01:59:44 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 03:32:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 03:32:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 20:12:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 20:12:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 18 Mar 2021 01:34:29 GMT
ENV TELEGRAF_VERSION=1.18.0
# Thu, 18 Mar 2021 01:34:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 18 Mar 2021 01:34:39 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 18 Mar 2021 01:34:40 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Thu, 18 Mar 2021 01:34:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Mar 2021 01:34:41 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:199f83f6a2f5a375b8f94d3025f9bbdaca75f4ca46ad0aab2061c331588fa662`  
		Last Modified: Fri, 12 Mar 2021 02:10:00 GMT  
		Size: 45.9 MB (45868120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d535c087e97eba956c56d41b509048f3f9283744c2b2ef7fabbb6a75fe7d3c`  
		Last Modified: Fri, 12 Mar 2021 03:47:04 GMT  
		Size: 7.1 MB (7123778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7cfc4c570eb98f73a8ab1d871e36ff43492038fa4c0279c70ccff1797447d2b`  
		Last Modified: Fri, 12 Mar 2021 03:47:04 GMT  
		Size: 9.3 MB (9343577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5bf068baebd708e3761ed06f179f64325dccfa420b559b02ebc09bae2c0fda`  
		Last Modified: Fri, 12 Mar 2021 20:13:13 GMT  
		Size: 16.2 MB (16159151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3c1f8007e854e0bd2b8c67586814d6cbb8f27c595193f97f169d521f6c1ab4`  
		Last Modified: Fri, 12 Mar 2021 20:13:07 GMT  
		Size: 2.9 KB (2898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdebf22157b930dc142d349b3d9d0bdb01689c4330805561299122beacd09c1d`  
		Last Modified: Thu, 18 Mar 2021 01:35:05 GMT  
		Size: 23.8 MB (23770298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e9e19177f7edc69e6c5f8fb9f196c7d7ee8d53360e772358f3397e07097845`  
		Last Modified: Thu, 18 Mar 2021 01:34:58 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.18` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:f8b6443f353d552229d60f21029920481c300caa3373f17f4f1aeba3058e5216
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107468820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da8eb2b8831351096fa670ef2d79e910d3a0f69204d4bc8ed55e529e4bfc9b8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 12 Mar 2021 01:53:16 GMT
ADD file:b2e2cca51e131b97e6a7e02af893c7f9b1f7a491b3d5fdaafa80409ed248a706 in / 
# Fri, 12 Mar 2021 01:53:20 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:29:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:29:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 23:37:57 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 23:38:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 18 Mar 2021 00:43:55 GMT
ENV TELEGRAF_VERSION=1.18.0
# Thu, 18 Mar 2021 00:44:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 18 Mar 2021 00:44:02 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 18 Mar 2021 00:44:03 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Thu, 18 Mar 2021 00:44:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Mar 2021 00:44:05 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e9742a63e95a88f8685c4f23a73f7dd15e4039ac1862ce5753c53406a5f7c04a`  
		Last Modified: Fri, 12 Mar 2021 02:01:14 GMT  
		Size: 49.2 MB (49195763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90273c85fdda8648cee9282aa7b01faf0ec1f45451931985b3504c37cf1ac3e6`  
		Last Modified: Fri, 12 Mar 2021 02:43:30 GMT  
		Size: 7.7 MB (7694407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685f873e984153af9a44cf556c7679b430b9c557d901c7d476725134f28754e7`  
		Last Modified: Fri, 12 Mar 2021 02:43:30 GMT  
		Size: 10.0 MB (9984339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67be13eac316a9bb534db0eeff7686c2ec2ba9e0e02d4544b9d206c7275ed54`  
		Last Modified: Fri, 12 Mar 2021 23:39:13 GMT  
		Size: 17.3 MB (17269554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682c14900e4723e4a455cc93b301b78b3177a23356e5d5b7a424a39c0ceb3ea9`  
		Last Modified: Fri, 12 Mar 2021 23:39:08 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409e8cf09d9bc47d94eb274af655865f409ad7e76241135143d60e1dd1825e52`  
		Last Modified: Thu, 18 Mar 2021 00:44:27 GMT  
		Size: 23.3 MB (23321673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf2ac6f41541a2d5f434116d398da3dbce49fbb7597c3df642805ebbe9ce7d0`  
		Last Modified: Thu, 18 Mar 2021 00:44:21 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.18-alpine`

```console
$ docker pull telegraf@sha256:653a0541f6c5441368e29a380133084be82c76730888ba215906a4d95f4be371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.18-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:f531a8156e240100b96ce545279c8252605508997b5f47ca07d9cbf383646e53
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31650529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd00f7d807e254e4a597dc282d284a94f864dad009ce088212c4ca6ca4c1c44a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Fri, 12 Mar 2021 03:37:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Mar 2021 04:22:25 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Thu, 18 Mar 2021 01:28:40 GMT
ENV TELEGRAF_VERSION=1.18.0
# Thu, 18 Mar 2021 01:28:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 18 Mar 2021 01:28:46 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 18 Mar 2021 01:28:46 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Thu, 18 Mar 2021 01:28:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Mar 2021 01:28:47 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bab45d475695400229b7b704d7c3a4a6f326f0eb1299894f67d202fbaf5a331`  
		Last Modified: Fri, 12 Mar 2021 03:39:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646312e5d4a840c82a7cb31726398ff761aef46aa9c78a9b689d1e1d4615c3b6`  
		Last Modified: Sat, 13 Mar 2021 04:24:01 GMT  
		Size: 3.3 MB (3300514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5b79bd03cb610ba763616a29788fb8df3abc7e8439d7dfabad1ae3bea68adc`  
		Last Modified: Thu, 18 Mar 2021 01:29:34 GMT  
		Size: 25.6 MB (25550183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7919ed643eaadd136a06348e935048f42a81e6af7eef5dc042aa99a42730f67e`  
		Last Modified: Thu, 18 Mar 2021 01:29:28 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.18.0`

```console
$ docker pull telegraf@sha256:f70b6208076ea423adbf560419fbf02e54d5d139f18b832c05916d82d045a8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.18.0` - linux; amd64

```console
$ docker pull telegraf@sha256:460a896574533bf2974b952d9f1b817adccb42bba82dd35415f225fa97a965e0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 MB (111343492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6fcc27083d05669cf5233e865588e1bbeef1df6f97828918f080e97092e7079`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:27 GMT
ADD file:575bf0d00d72810609a4118728923f11625b43de536352fe69a341086e4ebfd1 in / 
# Fri, 12 Mar 2021 02:20:28 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:49:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:49:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 13 Mar 2021 04:21:53 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Sat, 13 Mar 2021 04:21:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 18 Mar 2021 01:28:30 GMT
ENV TELEGRAF_VERSION=1.18.0
# Thu, 18 Mar 2021 01:28:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 18 Mar 2021 01:28:36 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 18 Mar 2021 01:28:36 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Thu, 18 Mar 2021 01:28:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Mar 2021 01:28:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e22122b926a1a853d61887fa35c3fe53e05ee7dc0f2f488936dc9838bd0e230d`  
		Last Modified: Fri, 12 Mar 2021 02:25:38 GMT  
		Size: 50.4 MB (50400353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29e09ae83733d697508e34827538cc0129b8719b85db943041c5d37287bcb81`  
		Last Modified: Fri, 12 Mar 2021 03:19:09 GMT  
		Size: 7.8 MB (7832474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e319e3daef68c36099bf3b534377a78d373f67bde3d156119c2463f5fe133ac5`  
		Last Modified: Fri, 12 Mar 2021 03:19:09 GMT  
		Size: 10.0 MB (9997147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78656f24469046aafcacf134dd6459f23b9332602a90a66a866ad5e65040fe4d`  
		Last Modified: Sat, 13 Mar 2021 04:23:18 GMT  
		Size: 17.4 MB (17414412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb405ad31ae4d29bd8710887a1e3837a2c576d4f3c53e14313c94282fa7ff86`  
		Last Modified: Sat, 13 Mar 2021 04:23:14 GMT  
		Size: 2.9 KB (2897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813d826ac3831059bd29266b49495022b5a40f498501661b2ac757520c263f87`  
		Last Modified: Thu, 18 Mar 2021 01:29:15 GMT  
		Size: 25.7 MB (25696025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fa2dfd32cd8435a93001130e6aa2db89de174c5384895bf57aabcaa86652837`  
		Last Modified: Thu, 18 Mar 2021 01:29:10 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.18.0` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:7ef2475e0eacb99af604e039a53548c15109b8798d47bb614a5afb78f3003343
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102268008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5f3a2a08dfba5132a6485b89906b596a4fa08d679362979a214bbfd66320ec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 12 Mar 2021 01:59:39 GMT
ADD file:7a272c0a2bf029fde32186ff5d55a8ef335d159da9770327eedf010bd6e6c42d in / 
# Fri, 12 Mar 2021 01:59:44 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 03:32:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 03:32:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 20:12:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 20:12:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 18 Mar 2021 01:34:29 GMT
ENV TELEGRAF_VERSION=1.18.0
# Thu, 18 Mar 2021 01:34:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 18 Mar 2021 01:34:39 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 18 Mar 2021 01:34:40 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Thu, 18 Mar 2021 01:34:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Mar 2021 01:34:41 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:199f83f6a2f5a375b8f94d3025f9bbdaca75f4ca46ad0aab2061c331588fa662`  
		Last Modified: Fri, 12 Mar 2021 02:10:00 GMT  
		Size: 45.9 MB (45868120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d535c087e97eba956c56d41b509048f3f9283744c2b2ef7fabbb6a75fe7d3c`  
		Last Modified: Fri, 12 Mar 2021 03:47:04 GMT  
		Size: 7.1 MB (7123778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7cfc4c570eb98f73a8ab1d871e36ff43492038fa4c0279c70ccff1797447d2b`  
		Last Modified: Fri, 12 Mar 2021 03:47:04 GMT  
		Size: 9.3 MB (9343577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5bf068baebd708e3761ed06f179f64325dccfa420b559b02ebc09bae2c0fda`  
		Last Modified: Fri, 12 Mar 2021 20:13:13 GMT  
		Size: 16.2 MB (16159151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3c1f8007e854e0bd2b8c67586814d6cbb8f27c595193f97f169d521f6c1ab4`  
		Last Modified: Fri, 12 Mar 2021 20:13:07 GMT  
		Size: 2.9 KB (2898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdebf22157b930dc142d349b3d9d0bdb01689c4330805561299122beacd09c1d`  
		Last Modified: Thu, 18 Mar 2021 01:35:05 GMT  
		Size: 23.8 MB (23770298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e9e19177f7edc69e6c5f8fb9f196c7d7ee8d53360e772358f3397e07097845`  
		Last Modified: Thu, 18 Mar 2021 01:34:58 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.18.0` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:f8b6443f353d552229d60f21029920481c300caa3373f17f4f1aeba3058e5216
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107468820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da8eb2b8831351096fa670ef2d79e910d3a0f69204d4bc8ed55e529e4bfc9b8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 12 Mar 2021 01:53:16 GMT
ADD file:b2e2cca51e131b97e6a7e02af893c7f9b1f7a491b3d5fdaafa80409ed248a706 in / 
# Fri, 12 Mar 2021 01:53:20 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:29:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:29:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 23:37:57 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 23:38:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 18 Mar 2021 00:43:55 GMT
ENV TELEGRAF_VERSION=1.18.0
# Thu, 18 Mar 2021 00:44:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 18 Mar 2021 00:44:02 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 18 Mar 2021 00:44:03 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Thu, 18 Mar 2021 00:44:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Mar 2021 00:44:05 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e9742a63e95a88f8685c4f23a73f7dd15e4039ac1862ce5753c53406a5f7c04a`  
		Last Modified: Fri, 12 Mar 2021 02:01:14 GMT  
		Size: 49.2 MB (49195763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90273c85fdda8648cee9282aa7b01faf0ec1f45451931985b3504c37cf1ac3e6`  
		Last Modified: Fri, 12 Mar 2021 02:43:30 GMT  
		Size: 7.7 MB (7694407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685f873e984153af9a44cf556c7679b430b9c557d901c7d476725134f28754e7`  
		Last Modified: Fri, 12 Mar 2021 02:43:30 GMT  
		Size: 10.0 MB (9984339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67be13eac316a9bb534db0eeff7686c2ec2ba9e0e02d4544b9d206c7275ed54`  
		Last Modified: Fri, 12 Mar 2021 23:39:13 GMT  
		Size: 17.3 MB (17269554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682c14900e4723e4a455cc93b301b78b3177a23356e5d5b7a424a39c0ceb3ea9`  
		Last Modified: Fri, 12 Mar 2021 23:39:08 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409e8cf09d9bc47d94eb274af655865f409ad7e76241135143d60e1dd1825e52`  
		Last Modified: Thu, 18 Mar 2021 00:44:27 GMT  
		Size: 23.3 MB (23321673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf2ac6f41541a2d5f434116d398da3dbce49fbb7597c3df642805ebbe9ce7d0`  
		Last Modified: Thu, 18 Mar 2021 00:44:21 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.18.0-alpine`

```console
$ docker pull telegraf@sha256:653a0541f6c5441368e29a380133084be82c76730888ba215906a4d95f4be371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.18.0-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:f531a8156e240100b96ce545279c8252605508997b5f47ca07d9cbf383646e53
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31650529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd00f7d807e254e4a597dc282d284a94f864dad009ce088212c4ca6ca4c1c44a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Fri, 12 Mar 2021 03:37:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Mar 2021 04:22:25 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Thu, 18 Mar 2021 01:28:40 GMT
ENV TELEGRAF_VERSION=1.18.0
# Thu, 18 Mar 2021 01:28:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 18 Mar 2021 01:28:46 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 18 Mar 2021 01:28:46 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Thu, 18 Mar 2021 01:28:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Mar 2021 01:28:47 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bab45d475695400229b7b704d7c3a4a6f326f0eb1299894f67d202fbaf5a331`  
		Last Modified: Fri, 12 Mar 2021 03:39:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646312e5d4a840c82a7cb31726398ff761aef46aa9c78a9b689d1e1d4615c3b6`  
		Last Modified: Sat, 13 Mar 2021 04:24:01 GMT  
		Size: 3.3 MB (3300514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5b79bd03cb610ba763616a29788fb8df3abc7e8439d7dfabad1ae3bea68adc`  
		Last Modified: Thu, 18 Mar 2021 01:29:34 GMT  
		Size: 25.6 MB (25550183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7919ed643eaadd136a06348e935048f42a81e6af7eef5dc042aa99a42730f67e`  
		Last Modified: Thu, 18 Mar 2021 01:29:28 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:653a0541f6c5441368e29a380133084be82c76730888ba215906a4d95f4be371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:f531a8156e240100b96ce545279c8252605508997b5f47ca07d9cbf383646e53
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31650529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd00f7d807e254e4a597dc282d284a94f864dad009ce088212c4ca6ca4c1c44a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Fri, 12 Mar 2021 03:37:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Mar 2021 04:22:25 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Thu, 18 Mar 2021 01:28:40 GMT
ENV TELEGRAF_VERSION=1.18.0
# Thu, 18 Mar 2021 01:28:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 18 Mar 2021 01:28:46 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 18 Mar 2021 01:28:46 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Thu, 18 Mar 2021 01:28:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Mar 2021 01:28:47 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bab45d475695400229b7b704d7c3a4a6f326f0eb1299894f67d202fbaf5a331`  
		Last Modified: Fri, 12 Mar 2021 03:39:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646312e5d4a840c82a7cb31726398ff761aef46aa9c78a9b689d1e1d4615c3b6`  
		Last Modified: Sat, 13 Mar 2021 04:24:01 GMT  
		Size: 3.3 MB (3300514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5b79bd03cb610ba763616a29788fb8df3abc7e8439d7dfabad1ae3bea68adc`  
		Last Modified: Thu, 18 Mar 2021 01:29:34 GMT  
		Size: 25.6 MB (25550183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7919ed643eaadd136a06348e935048f42a81e6af7eef5dc042aa99a42730f67e`  
		Last Modified: Thu, 18 Mar 2021 01:29:28 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:f70b6208076ea423adbf560419fbf02e54d5d139f18b832c05916d82d045a8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:460a896574533bf2974b952d9f1b817adccb42bba82dd35415f225fa97a965e0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 MB (111343492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6fcc27083d05669cf5233e865588e1bbeef1df6f97828918f080e97092e7079`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:27 GMT
ADD file:575bf0d00d72810609a4118728923f11625b43de536352fe69a341086e4ebfd1 in / 
# Fri, 12 Mar 2021 02:20:28 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:49:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:49:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 13 Mar 2021 04:21:53 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Sat, 13 Mar 2021 04:21:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 18 Mar 2021 01:28:30 GMT
ENV TELEGRAF_VERSION=1.18.0
# Thu, 18 Mar 2021 01:28:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 18 Mar 2021 01:28:36 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 18 Mar 2021 01:28:36 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Thu, 18 Mar 2021 01:28:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Mar 2021 01:28:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e22122b926a1a853d61887fa35c3fe53e05ee7dc0f2f488936dc9838bd0e230d`  
		Last Modified: Fri, 12 Mar 2021 02:25:38 GMT  
		Size: 50.4 MB (50400353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29e09ae83733d697508e34827538cc0129b8719b85db943041c5d37287bcb81`  
		Last Modified: Fri, 12 Mar 2021 03:19:09 GMT  
		Size: 7.8 MB (7832474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e319e3daef68c36099bf3b534377a78d373f67bde3d156119c2463f5fe133ac5`  
		Last Modified: Fri, 12 Mar 2021 03:19:09 GMT  
		Size: 10.0 MB (9997147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78656f24469046aafcacf134dd6459f23b9332602a90a66a866ad5e65040fe4d`  
		Last Modified: Sat, 13 Mar 2021 04:23:18 GMT  
		Size: 17.4 MB (17414412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb405ad31ae4d29bd8710887a1e3837a2c576d4f3c53e14313c94282fa7ff86`  
		Last Modified: Sat, 13 Mar 2021 04:23:14 GMT  
		Size: 2.9 KB (2897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813d826ac3831059bd29266b49495022b5a40f498501661b2ac757520c263f87`  
		Last Modified: Thu, 18 Mar 2021 01:29:15 GMT  
		Size: 25.7 MB (25696025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fa2dfd32cd8435a93001130e6aa2db89de174c5384895bf57aabcaa86652837`  
		Last Modified: Thu, 18 Mar 2021 01:29:10 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:7ef2475e0eacb99af604e039a53548c15109b8798d47bb614a5afb78f3003343
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102268008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5f3a2a08dfba5132a6485b89906b596a4fa08d679362979a214bbfd66320ec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 12 Mar 2021 01:59:39 GMT
ADD file:7a272c0a2bf029fde32186ff5d55a8ef335d159da9770327eedf010bd6e6c42d in / 
# Fri, 12 Mar 2021 01:59:44 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 03:32:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 03:32:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 20:12:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 20:12:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 18 Mar 2021 01:34:29 GMT
ENV TELEGRAF_VERSION=1.18.0
# Thu, 18 Mar 2021 01:34:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 18 Mar 2021 01:34:39 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 18 Mar 2021 01:34:40 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Thu, 18 Mar 2021 01:34:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Mar 2021 01:34:41 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:199f83f6a2f5a375b8f94d3025f9bbdaca75f4ca46ad0aab2061c331588fa662`  
		Last Modified: Fri, 12 Mar 2021 02:10:00 GMT  
		Size: 45.9 MB (45868120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d535c087e97eba956c56d41b509048f3f9283744c2b2ef7fabbb6a75fe7d3c`  
		Last Modified: Fri, 12 Mar 2021 03:47:04 GMT  
		Size: 7.1 MB (7123778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7cfc4c570eb98f73a8ab1d871e36ff43492038fa4c0279c70ccff1797447d2b`  
		Last Modified: Fri, 12 Mar 2021 03:47:04 GMT  
		Size: 9.3 MB (9343577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5bf068baebd708e3761ed06f179f64325dccfa420b559b02ebc09bae2c0fda`  
		Last Modified: Fri, 12 Mar 2021 20:13:13 GMT  
		Size: 16.2 MB (16159151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3c1f8007e854e0bd2b8c67586814d6cbb8f27c595193f97f169d521f6c1ab4`  
		Last Modified: Fri, 12 Mar 2021 20:13:07 GMT  
		Size: 2.9 KB (2898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdebf22157b930dc142d349b3d9d0bdb01689c4330805561299122beacd09c1d`  
		Last Modified: Thu, 18 Mar 2021 01:35:05 GMT  
		Size: 23.8 MB (23770298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e9e19177f7edc69e6c5f8fb9f196c7d7ee8d53360e772358f3397e07097845`  
		Last Modified: Thu, 18 Mar 2021 01:34:58 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:f8b6443f353d552229d60f21029920481c300caa3373f17f4f1aeba3058e5216
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107468820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da8eb2b8831351096fa670ef2d79e910d3a0f69204d4bc8ed55e529e4bfc9b8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 12 Mar 2021 01:53:16 GMT
ADD file:b2e2cca51e131b97e6a7e02af893c7f9b1f7a491b3d5fdaafa80409ed248a706 in / 
# Fri, 12 Mar 2021 01:53:20 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:29:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:29:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 23:37:57 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 23:38:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 18 Mar 2021 00:43:55 GMT
ENV TELEGRAF_VERSION=1.18.0
# Thu, 18 Mar 2021 00:44:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 18 Mar 2021 00:44:02 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 18 Mar 2021 00:44:03 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Thu, 18 Mar 2021 00:44:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Mar 2021 00:44:05 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e9742a63e95a88f8685c4f23a73f7dd15e4039ac1862ce5753c53406a5f7c04a`  
		Last Modified: Fri, 12 Mar 2021 02:01:14 GMT  
		Size: 49.2 MB (49195763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90273c85fdda8648cee9282aa7b01faf0ec1f45451931985b3504c37cf1ac3e6`  
		Last Modified: Fri, 12 Mar 2021 02:43:30 GMT  
		Size: 7.7 MB (7694407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685f873e984153af9a44cf556c7679b430b9c557d901c7d476725134f28754e7`  
		Last Modified: Fri, 12 Mar 2021 02:43:30 GMT  
		Size: 10.0 MB (9984339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67be13eac316a9bb534db0eeff7686c2ec2ba9e0e02d4544b9d206c7275ed54`  
		Last Modified: Fri, 12 Mar 2021 23:39:13 GMT  
		Size: 17.3 MB (17269554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682c14900e4723e4a455cc93b301b78b3177a23356e5d5b7a424a39c0ceb3ea9`  
		Last Modified: Fri, 12 Mar 2021 23:39:08 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409e8cf09d9bc47d94eb274af655865f409ad7e76241135143d60e1dd1825e52`  
		Last Modified: Thu, 18 Mar 2021 00:44:27 GMT  
		Size: 23.3 MB (23321673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf2ac6f41541a2d5f434116d398da3dbce49fbb7597c3df642805ebbe9ce7d0`  
		Last Modified: Thu, 18 Mar 2021 00:44:21 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
