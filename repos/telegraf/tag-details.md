<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.15`](#telegraf115)
-	[`telegraf:1.15-alpine`](#telegraf115-alpine)
-	[`telegraf:1.15.4`](#telegraf1154)
-	[`telegraf:1.15.4-alpine`](#telegraf1154-alpine)
-	[`telegraf:1.16`](#telegraf116)
-	[`telegraf:1.16-alpine`](#telegraf116-alpine)
-	[`telegraf:1.16.3`](#telegraf1163)
-	[`telegraf:1.16.3-alpine`](#telegraf1163-alpine)
-	[`telegraf:1.17`](#telegraf117)
-	[`telegraf:1.17-alpine`](#telegraf117-alpine)
-	[`telegraf:1.17.3`](#telegraf1173)
-	[`telegraf:1.17.3-alpine`](#telegraf1173-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.15`

```console
$ docker pull telegraf@sha256:961cc096173f8a41e46b3d4aed3015e3d6b0779e9662746f6654b78bab3b9d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.15` - linux; amd64

```console
$ docker pull telegraf@sha256:1f5b470dc3a3917e880f2fdc07acb43b54996301c1f0c5f9435685989475d0c3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107312717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd4697244abef2ae0d3d6fa0c6cf8fdd2e68726a85f4515d10a66cbd1f47986a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:40 GMT
ADD file:8f75f11b2bd2d50e5912359ae750de06a7b49506df3756c19baf4cc63d900c4f in / 
# Tue, 09 Feb 2021 02:20:40 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:35:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:35:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 05:12:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Feb 2021 05:12:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 05:12:16 GMT
ENV TELEGRAF_VERSION=1.15.4
# Wed, 10 Feb 2021 05:12:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 10 Feb 2021 05:12:20 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 10 Feb 2021 05:12:20 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 10 Feb 2021 05:12:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 05:12:21 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0ecb575e629cd60aa802266a3bc6847dcf4073aa2a6d7d43f717dd61e7b90e0b`  
		Last Modified: Tue, 09 Feb 2021 02:26:22 GMT  
		Size: 50.4 MB (50400198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7467d1831b6947c294d92ee957902c3cd448b17c5ac2103ca5e79d15afb317c3`  
		Last Modified: Tue, 09 Feb 2021 04:46:00 GMT  
		Size: 7.8 MB (7830684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feab2c490a3cea21cc051ff29c33cc9857418edfa1be9966124b18abe1d5ae16`  
		Last Modified: Tue, 09 Feb 2021 04:46:00 GMT  
		Size: 10.0 MB (9996459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bb12ccec32f30558bc0672fb2db77bd29642b4ed86fe3dc5d886e36ab7cdef`  
		Last Modified: Wed, 10 Feb 2021 05:13:12 GMT  
		Size: 17.4 MB (17412680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8771be66e2d28a682acd9b2229052524b4a4466779459c8f48e09fe644611bea`  
		Last Modified: Wed, 10 Feb 2021 05:13:08 GMT  
		Size: 2.9 KB (2870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b726ba860a55431e44319e503390ef41b57feb9673baffbc43946ce384e665f2`  
		Last Modified: Wed, 10 Feb 2021 05:13:13 GMT  
		Size: 21.7 MB (21669640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c331fe039547981e9e0de04b26ef9d59fb66bc025d0d2bcacd002731aa038874`  
		Last Modified: Wed, 10 Feb 2021 05:13:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.15` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:def7def0574067a8eb0cb780f9862abf7a9c5e73e04ca90512064f48120e32c9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98905640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f74fd54604a29e9cc1bce1580c3bde6843b071fffb83a91cce20420c293bb529`
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
# Fri, 12 Mar 2021 20:12:06 GMT
ENV TELEGRAF_VERSION=1.15.4
# Fri, 12 Mar 2021 20:12:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 12 Mar 2021 20:12:14 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 12 Mar 2021 20:12:14 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Fri, 12 Mar 2021 20:12:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 20:12:16 GMT
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
	-	`sha256:58fcad762fcda15aa7210bdd20ad6a6b86e5a7c6c06daa230e3c2e83cad1ec37`  
		Last Modified: Fri, 12 Mar 2021 20:13:14 GMT  
		Size: 20.4 MB (20407930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7de3e50c015557103e31732f4ccfb237e23e0d92ce3c4ca79f68758d69ab48`  
		Last Modified: Fri, 12 Mar 2021 20:13:07 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.15` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:00c68fbd3e34b929a63247a4b1699146eaee2153c3b6edc9dff91cd683d300a5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104165688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5181bd078d23c4bbf3fc61228c776c45373cbbfc57776c4182f98355dcbdd4fc`
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
# Fri, 12 Mar 2021 23:38:01 GMT
ENV TELEGRAF_VERSION=1.15.4
# Fri, 12 Mar 2021 23:38:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 12 Mar 2021 23:38:07 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 12 Mar 2021 23:38:08 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Fri, 12 Mar 2021 23:38:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 23:38:10 GMT
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
	-	`sha256:ceea5ffbb829257848853297a08cfc07129f0bf636d1b5d7f8b5095903837e36`  
		Last Modified: Fri, 12 Mar 2021 23:39:14 GMT  
		Size: 20.0 MB (20018541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4004ca839cef7e761f418a9b0fde159f195cfece1196f91b0b70aad16f5311d7`  
		Last Modified: Fri, 12 Mar 2021 23:39:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.15-alpine`

```console
$ docker pull telegraf@sha256:c9f4415eec780410a23910cd50f1299ca9c54bc1c5a0fce915f79cf72660bd93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.15-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:2feeb44e793423cc0f355fd101a548996919101223f8c7cea5347a20a3d20720
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 MB (27695177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ab3b9556e28dd391f18a4faa5155c7dcdbed432a2835ebdc9b56b0ecf5bc33`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 06:58:12 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 18 Feb 2021 06:58:14 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Thu, 18 Feb 2021 06:58:14 GMT
ENV TELEGRAF_VERSION=1.15.4
# Thu, 18 Feb 2021 06:58:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 18 Feb 2021 06:58:18 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 18 Feb 2021 06:58:19 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Thu, 18 Feb 2021 06:58:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Feb 2021 06:58:19 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a566023623516b301d90728ad0e1530d806f4443c0a6991f786c0f6d2c9104`  
		Last Modified: Thu, 18 Feb 2021 06:58:53 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d38ad2952582880c3b13cabd7234784ddc0661dc0ce269dfda323d528a6f72b`  
		Last Modified: Thu, 18 Feb 2021 06:58:54 GMT  
		Size: 3.3 MB (3342420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bef1f8ecf9e2d0f70fc5ff14f72fb5354bdfc55ca71ec8bcc02f711f152d415`  
		Last Modified: Thu, 18 Feb 2021 06:58:57 GMT  
		Size: 21.5 MB (21540768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0049460c07c1970d28933c3b91772ddb31a06f04a9a3402c2ad990e376a8b25c`  
		Last Modified: Thu, 18 Feb 2021 06:58:53 GMT  
		Size: 180.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.15.4`

```console
$ docker pull telegraf@sha256:961cc096173f8a41e46b3d4aed3015e3d6b0779e9662746f6654b78bab3b9d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.15.4` - linux; amd64

```console
$ docker pull telegraf@sha256:1f5b470dc3a3917e880f2fdc07acb43b54996301c1f0c5f9435685989475d0c3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107312717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd4697244abef2ae0d3d6fa0c6cf8fdd2e68726a85f4515d10a66cbd1f47986a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:40 GMT
ADD file:8f75f11b2bd2d50e5912359ae750de06a7b49506df3756c19baf4cc63d900c4f in / 
# Tue, 09 Feb 2021 02:20:40 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:35:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:35:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 05:12:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Feb 2021 05:12:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 05:12:16 GMT
ENV TELEGRAF_VERSION=1.15.4
# Wed, 10 Feb 2021 05:12:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 10 Feb 2021 05:12:20 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 10 Feb 2021 05:12:20 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 10 Feb 2021 05:12:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 05:12:21 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0ecb575e629cd60aa802266a3bc6847dcf4073aa2a6d7d43f717dd61e7b90e0b`  
		Last Modified: Tue, 09 Feb 2021 02:26:22 GMT  
		Size: 50.4 MB (50400198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7467d1831b6947c294d92ee957902c3cd448b17c5ac2103ca5e79d15afb317c3`  
		Last Modified: Tue, 09 Feb 2021 04:46:00 GMT  
		Size: 7.8 MB (7830684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feab2c490a3cea21cc051ff29c33cc9857418edfa1be9966124b18abe1d5ae16`  
		Last Modified: Tue, 09 Feb 2021 04:46:00 GMT  
		Size: 10.0 MB (9996459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bb12ccec32f30558bc0672fb2db77bd29642b4ed86fe3dc5d886e36ab7cdef`  
		Last Modified: Wed, 10 Feb 2021 05:13:12 GMT  
		Size: 17.4 MB (17412680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8771be66e2d28a682acd9b2229052524b4a4466779459c8f48e09fe644611bea`  
		Last Modified: Wed, 10 Feb 2021 05:13:08 GMT  
		Size: 2.9 KB (2870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b726ba860a55431e44319e503390ef41b57feb9673baffbc43946ce384e665f2`  
		Last Modified: Wed, 10 Feb 2021 05:13:13 GMT  
		Size: 21.7 MB (21669640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c331fe039547981e9e0de04b26ef9d59fb66bc025d0d2bcacd002731aa038874`  
		Last Modified: Wed, 10 Feb 2021 05:13:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.15.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:def7def0574067a8eb0cb780f9862abf7a9c5e73e04ca90512064f48120e32c9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98905640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f74fd54604a29e9cc1bce1580c3bde6843b071fffb83a91cce20420c293bb529`
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
# Fri, 12 Mar 2021 20:12:06 GMT
ENV TELEGRAF_VERSION=1.15.4
# Fri, 12 Mar 2021 20:12:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 12 Mar 2021 20:12:14 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 12 Mar 2021 20:12:14 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Fri, 12 Mar 2021 20:12:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 20:12:16 GMT
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
	-	`sha256:58fcad762fcda15aa7210bdd20ad6a6b86e5a7c6c06daa230e3c2e83cad1ec37`  
		Last Modified: Fri, 12 Mar 2021 20:13:14 GMT  
		Size: 20.4 MB (20407930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7de3e50c015557103e31732f4ccfb237e23e0d92ce3c4ca79f68758d69ab48`  
		Last Modified: Fri, 12 Mar 2021 20:13:07 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.15.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:00c68fbd3e34b929a63247a4b1699146eaee2153c3b6edc9dff91cd683d300a5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104165688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5181bd078d23c4bbf3fc61228c776c45373cbbfc57776c4182f98355dcbdd4fc`
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
# Fri, 12 Mar 2021 23:38:01 GMT
ENV TELEGRAF_VERSION=1.15.4
# Fri, 12 Mar 2021 23:38:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 12 Mar 2021 23:38:07 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 12 Mar 2021 23:38:08 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Fri, 12 Mar 2021 23:38:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 23:38:10 GMT
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
	-	`sha256:ceea5ffbb829257848853297a08cfc07129f0bf636d1b5d7f8b5095903837e36`  
		Last Modified: Fri, 12 Mar 2021 23:39:14 GMT  
		Size: 20.0 MB (20018541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4004ca839cef7e761f418a9b0fde159f195cfece1196f91b0b70aad16f5311d7`  
		Last Modified: Fri, 12 Mar 2021 23:39:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.15.4-alpine`

```console
$ docker pull telegraf@sha256:c9f4415eec780410a23910cd50f1299ca9c54bc1c5a0fce915f79cf72660bd93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.15.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:2feeb44e793423cc0f355fd101a548996919101223f8c7cea5347a20a3d20720
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 MB (27695177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ab3b9556e28dd391f18a4faa5155c7dcdbed432a2835ebdc9b56b0ecf5bc33`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 06:58:12 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 18 Feb 2021 06:58:14 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Thu, 18 Feb 2021 06:58:14 GMT
ENV TELEGRAF_VERSION=1.15.4
# Thu, 18 Feb 2021 06:58:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 18 Feb 2021 06:58:18 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 18 Feb 2021 06:58:19 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Thu, 18 Feb 2021 06:58:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Feb 2021 06:58:19 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a566023623516b301d90728ad0e1530d806f4443c0a6991f786c0f6d2c9104`  
		Last Modified: Thu, 18 Feb 2021 06:58:53 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d38ad2952582880c3b13cabd7234784ddc0661dc0ce269dfda323d528a6f72b`  
		Last Modified: Thu, 18 Feb 2021 06:58:54 GMT  
		Size: 3.3 MB (3342420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bef1f8ecf9e2d0f70fc5ff14f72fb5354bdfc55ca71ec8bcc02f711f152d415`  
		Last Modified: Thu, 18 Feb 2021 06:58:57 GMT  
		Size: 21.5 MB (21540768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0049460c07c1970d28933c3b91772ddb31a06f04a9a3402c2ad990e376a8b25c`  
		Last Modified: Thu, 18 Feb 2021 06:58:53 GMT  
		Size: 180.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.16`

```console
$ docker pull telegraf@sha256:103058c925ab37649692e5dc919f649cbc1918447b15869fa9ba41f95d6d7b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.16` - linux; amd64

```console
$ docker pull telegraf@sha256:3b5cc15c3d9c224efeba10eace2103ce177206c06cdacef40676264805de2a2d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.0 MB (108000321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160d28f5dc42ff89a13edbf2ccbb4077dde793b9e4b356b4a82579a76ed02ad8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:40 GMT
ADD file:8f75f11b2bd2d50e5912359ae750de06a7b49506df3756c19baf4cc63d900c4f in / 
# Tue, 09 Feb 2021 02:20:40 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:35:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:35:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 05:12:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Feb 2021 05:12:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 05:12:30 GMT
ENV TELEGRAF_VERSION=1.16.3
# Wed, 10 Feb 2021 05:12:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 10 Feb 2021 05:12:34 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 10 Feb 2021 05:12:34 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 10 Feb 2021 05:12:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 05:12:34 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0ecb575e629cd60aa802266a3bc6847dcf4073aa2a6d7d43f717dd61e7b90e0b`  
		Last Modified: Tue, 09 Feb 2021 02:26:22 GMT  
		Size: 50.4 MB (50400198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7467d1831b6947c294d92ee957902c3cd448b17c5ac2103ca5e79d15afb317c3`  
		Last Modified: Tue, 09 Feb 2021 04:46:00 GMT  
		Size: 7.8 MB (7830684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feab2c490a3cea21cc051ff29c33cc9857418edfa1be9966124b18abe1d5ae16`  
		Last Modified: Tue, 09 Feb 2021 04:46:00 GMT  
		Size: 10.0 MB (9996459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bb12ccec32f30558bc0672fb2db77bd29642b4ed86fe3dc5d886e36ab7cdef`  
		Last Modified: Wed, 10 Feb 2021 05:13:12 GMT  
		Size: 17.4 MB (17412680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8771be66e2d28a682acd9b2229052524b4a4466779459c8f48e09fe644611bea`  
		Last Modified: Wed, 10 Feb 2021 05:13:08 GMT  
		Size: 2.9 KB (2870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e43c8d6a07cc76251d4e9524397c074d22e2920c682230e91cbd0805e43331ba`  
		Last Modified: Wed, 10 Feb 2021 05:13:34 GMT  
		Size: 22.4 MB (22357244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1426615b59b84b0daabe1e2d2f93a48fbc9f0acce2c3481663e2aa7dc09a0e6b`  
		Last Modified: Wed, 10 Feb 2021 05:13:19 GMT  
		Size: 186.0 B  
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
$ docker pull telegraf@sha256:6cb8c1212f1adbdf9dc4ae7a9717fabc977b5b54079acb5a62362c909987b0ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.16-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:77814e5cd2c0d77593a6845d4cba2cf657be795f37703fb345e9ff6f50777c45
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 MB (28314612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b7d692287836f0c628c2628ce7666d0ef770f9a903c15dae5a64ad6c2bf8ca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:21:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 25 Feb 2021 03:10:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Thu, 25 Feb 2021 03:10:27 GMT
ENV TELEGRAF_VERSION=1.16.3
# Thu, 25 Feb 2021 03:10:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 25 Feb 2021 03:10:34 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 25 Feb 2021 03:10:34 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Thu, 25 Feb 2021 03:10:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Feb 2021 03:10:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c3c544bdbd838411be7288d5c8bd23d77b89d00730ce0fa218fd7fd1694b04`  
		Last Modified: Wed, 24 Feb 2021 20:24:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82161b50eed987332d980ae30c61690586264cf2cd8f62d601819cc06ac1154b`  
		Last Modified: Thu, 25 Feb 2021 03:11:21 GMT  
		Size: 3.3 MB (3300351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc22fa71707e30e7ef4f448eb532e1f97aa6f0c556403e1da716a48c0925b827`  
		Last Modified: Thu, 25 Feb 2021 03:11:27 GMT  
		Size: 22.2 MB (22214433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93dba41f824283fc67df7cc443f4a816ae9e14b43ec5907eb9991854f58b73f4`  
		Last Modified: Thu, 25 Feb 2021 03:11:20 GMT  
		Size: 181.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.16.3`

```console
$ docker pull telegraf@sha256:103058c925ab37649692e5dc919f649cbc1918447b15869fa9ba41f95d6d7b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.16.3` - linux; amd64

```console
$ docker pull telegraf@sha256:3b5cc15c3d9c224efeba10eace2103ce177206c06cdacef40676264805de2a2d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.0 MB (108000321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160d28f5dc42ff89a13edbf2ccbb4077dde793b9e4b356b4a82579a76ed02ad8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:40 GMT
ADD file:8f75f11b2bd2d50e5912359ae750de06a7b49506df3756c19baf4cc63d900c4f in / 
# Tue, 09 Feb 2021 02:20:40 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:35:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:35:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 05:12:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Feb 2021 05:12:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 05:12:30 GMT
ENV TELEGRAF_VERSION=1.16.3
# Wed, 10 Feb 2021 05:12:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 10 Feb 2021 05:12:34 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 10 Feb 2021 05:12:34 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 10 Feb 2021 05:12:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 05:12:34 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0ecb575e629cd60aa802266a3bc6847dcf4073aa2a6d7d43f717dd61e7b90e0b`  
		Last Modified: Tue, 09 Feb 2021 02:26:22 GMT  
		Size: 50.4 MB (50400198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7467d1831b6947c294d92ee957902c3cd448b17c5ac2103ca5e79d15afb317c3`  
		Last Modified: Tue, 09 Feb 2021 04:46:00 GMT  
		Size: 7.8 MB (7830684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feab2c490a3cea21cc051ff29c33cc9857418edfa1be9966124b18abe1d5ae16`  
		Last Modified: Tue, 09 Feb 2021 04:46:00 GMT  
		Size: 10.0 MB (9996459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bb12ccec32f30558bc0672fb2db77bd29642b4ed86fe3dc5d886e36ab7cdef`  
		Last Modified: Wed, 10 Feb 2021 05:13:12 GMT  
		Size: 17.4 MB (17412680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8771be66e2d28a682acd9b2229052524b4a4466779459c8f48e09fe644611bea`  
		Last Modified: Wed, 10 Feb 2021 05:13:08 GMT  
		Size: 2.9 KB (2870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e43c8d6a07cc76251d4e9524397c074d22e2920c682230e91cbd0805e43331ba`  
		Last Modified: Wed, 10 Feb 2021 05:13:34 GMT  
		Size: 22.4 MB (22357244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1426615b59b84b0daabe1e2d2f93a48fbc9f0acce2c3481663e2aa7dc09a0e6b`  
		Last Modified: Wed, 10 Feb 2021 05:13:19 GMT  
		Size: 186.0 B  
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
$ docker pull telegraf@sha256:6cb8c1212f1adbdf9dc4ae7a9717fabc977b5b54079acb5a62362c909987b0ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.16.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:77814e5cd2c0d77593a6845d4cba2cf657be795f37703fb345e9ff6f50777c45
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 MB (28314612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b7d692287836f0c628c2628ce7666d0ef770f9a903c15dae5a64ad6c2bf8ca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:21:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 25 Feb 2021 03:10:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Thu, 25 Feb 2021 03:10:27 GMT
ENV TELEGRAF_VERSION=1.16.3
# Thu, 25 Feb 2021 03:10:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 25 Feb 2021 03:10:34 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 25 Feb 2021 03:10:34 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Thu, 25 Feb 2021 03:10:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Feb 2021 03:10:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c3c544bdbd838411be7288d5c8bd23d77b89d00730ce0fa218fd7fd1694b04`  
		Last Modified: Wed, 24 Feb 2021 20:24:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82161b50eed987332d980ae30c61690586264cf2cd8f62d601819cc06ac1154b`  
		Last Modified: Thu, 25 Feb 2021 03:11:21 GMT  
		Size: 3.3 MB (3300351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc22fa71707e30e7ef4f448eb532e1f97aa6f0c556403e1da716a48c0925b827`  
		Last Modified: Thu, 25 Feb 2021 03:11:27 GMT  
		Size: 22.2 MB (22214433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93dba41f824283fc67df7cc443f4a816ae9e14b43ec5907eb9991854f58b73f4`  
		Last Modified: Thu, 25 Feb 2021 03:11:20 GMT  
		Size: 181.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.17`

```console
$ docker pull telegraf@sha256:4517161678cffcf965ebb2a9b9ff92956a7a78da32f825f6378823aacf4faa7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.17` - linux; amd64

```console
$ docker pull telegraf@sha256:dddfec9e9cdf8bdd2cac2025e1828ace6f39c0f9e1076faa1427e11f34b096a4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.6 MB (108601776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13d3af8fedb4c47f3ee7d210483b2f8f1db049a40b7d56736eb083ebde70b22`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:40 GMT
ADD file:8f75f11b2bd2d50e5912359ae750de06a7b49506df3756c19baf4cc63d900c4f in / 
# Tue, 09 Feb 2021 02:20:40 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:35:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:35:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 05:12:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Feb 2021 05:12:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 24 Feb 2021 18:47:43 GMT
ENV TELEGRAF_VERSION=1.17.3
# Wed, 24 Feb 2021 18:47:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 24 Feb 2021 18:47:47 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 24 Feb 2021 18:47:47 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 24 Feb 2021 18:47:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 18:47:47 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0ecb575e629cd60aa802266a3bc6847dcf4073aa2a6d7d43f717dd61e7b90e0b`  
		Last Modified: Tue, 09 Feb 2021 02:26:22 GMT  
		Size: 50.4 MB (50400198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7467d1831b6947c294d92ee957902c3cd448b17c5ac2103ca5e79d15afb317c3`  
		Last Modified: Tue, 09 Feb 2021 04:46:00 GMT  
		Size: 7.8 MB (7830684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feab2c490a3cea21cc051ff29c33cc9857418edfa1be9966124b18abe1d5ae16`  
		Last Modified: Tue, 09 Feb 2021 04:46:00 GMT  
		Size: 10.0 MB (9996459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bb12ccec32f30558bc0672fb2db77bd29642b4ed86fe3dc5d886e36ab7cdef`  
		Last Modified: Wed, 10 Feb 2021 05:13:12 GMT  
		Size: 17.4 MB (17412680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8771be66e2d28a682acd9b2229052524b4a4466779459c8f48e09fe644611bea`  
		Last Modified: Wed, 10 Feb 2021 05:13:08 GMT  
		Size: 2.9 KB (2870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3b9183e2d25d6bd23609f5394de713bf5a4a666ac75cd215c6b65e4ba786b5`  
		Last Modified: Wed, 24 Feb 2021 18:48:26 GMT  
		Size: 23.0 MB (22958700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f58677597ef6b7ae6393b2a07569ed37ad242b0f511bb0b185307776492c34`  
		Last Modified: Wed, 24 Feb 2021 18:48:21 GMT  
		Size: 185.0 B  
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
$ docker pull telegraf@sha256:0e0c1b0929fa460b92cb9ebe48c21fff8655d12c5afc7df0b0168883109dc27e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.17-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:b211eff1365b465c20cb5d53d33474ee1cdd3dcf2bee6b748c228c00ea7b16ce
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28921159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2543a379287e378b03dac2d8befcb34c5d3d8b6eaa973ea234d1b641ac139982`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:21:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 25 Feb 2021 03:10:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Thu, 25 Feb 2021 03:10:47 GMT
ENV TELEGRAF_VERSION=1.17.3
# Thu, 25 Feb 2021 03:10:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 25 Feb 2021 03:10:52 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 25 Feb 2021 03:10:53 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Thu, 25 Feb 2021 03:10:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Feb 2021 03:10:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c3c544bdbd838411be7288d5c8bd23d77b89d00730ce0fa218fd7fd1694b04`  
		Last Modified: Wed, 24 Feb 2021 20:24:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82161b50eed987332d980ae30c61690586264cf2cd8f62d601819cc06ac1154b`  
		Last Modified: Thu, 25 Feb 2021 03:11:21 GMT  
		Size: 3.3 MB (3300351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fde0bc6809561cec22c96436399e0fe7b643a3a1b61cbe0015bf17ed5f48ec4`  
		Last Modified: Thu, 25 Feb 2021 03:11:43 GMT  
		Size: 22.8 MB (22820979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b41c521a3b98aa1e4f31420abc5950fae51cc04d9fb6fa90344622eb5d4811a`  
		Last Modified: Thu, 25 Feb 2021 03:11:36 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.17.3`

```console
$ docker pull telegraf@sha256:4517161678cffcf965ebb2a9b9ff92956a7a78da32f825f6378823aacf4faa7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.17.3` - linux; amd64

```console
$ docker pull telegraf@sha256:dddfec9e9cdf8bdd2cac2025e1828ace6f39c0f9e1076faa1427e11f34b096a4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.6 MB (108601776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13d3af8fedb4c47f3ee7d210483b2f8f1db049a40b7d56736eb083ebde70b22`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:40 GMT
ADD file:8f75f11b2bd2d50e5912359ae750de06a7b49506df3756c19baf4cc63d900c4f in / 
# Tue, 09 Feb 2021 02:20:40 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:35:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:35:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 05:12:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Feb 2021 05:12:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 24 Feb 2021 18:47:43 GMT
ENV TELEGRAF_VERSION=1.17.3
# Wed, 24 Feb 2021 18:47:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 24 Feb 2021 18:47:47 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 24 Feb 2021 18:47:47 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 24 Feb 2021 18:47:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 18:47:47 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0ecb575e629cd60aa802266a3bc6847dcf4073aa2a6d7d43f717dd61e7b90e0b`  
		Last Modified: Tue, 09 Feb 2021 02:26:22 GMT  
		Size: 50.4 MB (50400198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7467d1831b6947c294d92ee957902c3cd448b17c5ac2103ca5e79d15afb317c3`  
		Last Modified: Tue, 09 Feb 2021 04:46:00 GMT  
		Size: 7.8 MB (7830684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feab2c490a3cea21cc051ff29c33cc9857418edfa1be9966124b18abe1d5ae16`  
		Last Modified: Tue, 09 Feb 2021 04:46:00 GMT  
		Size: 10.0 MB (9996459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bb12ccec32f30558bc0672fb2db77bd29642b4ed86fe3dc5d886e36ab7cdef`  
		Last Modified: Wed, 10 Feb 2021 05:13:12 GMT  
		Size: 17.4 MB (17412680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8771be66e2d28a682acd9b2229052524b4a4466779459c8f48e09fe644611bea`  
		Last Modified: Wed, 10 Feb 2021 05:13:08 GMT  
		Size: 2.9 KB (2870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3b9183e2d25d6bd23609f5394de713bf5a4a666ac75cd215c6b65e4ba786b5`  
		Last Modified: Wed, 24 Feb 2021 18:48:26 GMT  
		Size: 23.0 MB (22958700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f58677597ef6b7ae6393b2a07569ed37ad242b0f511bb0b185307776492c34`  
		Last Modified: Wed, 24 Feb 2021 18:48:21 GMT  
		Size: 185.0 B  
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
$ docker pull telegraf@sha256:0e0c1b0929fa460b92cb9ebe48c21fff8655d12c5afc7df0b0168883109dc27e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.17.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:b211eff1365b465c20cb5d53d33474ee1cdd3dcf2bee6b748c228c00ea7b16ce
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28921159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2543a379287e378b03dac2d8befcb34c5d3d8b6eaa973ea234d1b641ac139982`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:21:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 25 Feb 2021 03:10:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Thu, 25 Feb 2021 03:10:47 GMT
ENV TELEGRAF_VERSION=1.17.3
# Thu, 25 Feb 2021 03:10:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 25 Feb 2021 03:10:52 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 25 Feb 2021 03:10:53 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Thu, 25 Feb 2021 03:10:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Feb 2021 03:10:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c3c544bdbd838411be7288d5c8bd23d77b89d00730ce0fa218fd7fd1694b04`  
		Last Modified: Wed, 24 Feb 2021 20:24:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82161b50eed987332d980ae30c61690586264cf2cd8f62d601819cc06ac1154b`  
		Last Modified: Thu, 25 Feb 2021 03:11:21 GMT  
		Size: 3.3 MB (3300351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fde0bc6809561cec22c96436399e0fe7b643a3a1b61cbe0015bf17ed5f48ec4`  
		Last Modified: Thu, 25 Feb 2021 03:11:43 GMT  
		Size: 22.8 MB (22820979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b41c521a3b98aa1e4f31420abc5950fae51cc04d9fb6fa90344622eb5d4811a`  
		Last Modified: Thu, 25 Feb 2021 03:11:36 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:0e0c1b0929fa460b92cb9ebe48c21fff8655d12c5afc7df0b0168883109dc27e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:b211eff1365b465c20cb5d53d33474ee1cdd3dcf2bee6b748c228c00ea7b16ce
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28921159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2543a379287e378b03dac2d8befcb34c5d3d8b6eaa973ea234d1b641ac139982`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:21:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 25 Feb 2021 03:10:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Thu, 25 Feb 2021 03:10:47 GMT
ENV TELEGRAF_VERSION=1.17.3
# Thu, 25 Feb 2021 03:10:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 25 Feb 2021 03:10:52 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 25 Feb 2021 03:10:53 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Thu, 25 Feb 2021 03:10:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Feb 2021 03:10:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c3c544bdbd838411be7288d5c8bd23d77b89d00730ce0fa218fd7fd1694b04`  
		Last Modified: Wed, 24 Feb 2021 20:24:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82161b50eed987332d980ae30c61690586264cf2cd8f62d601819cc06ac1154b`  
		Last Modified: Thu, 25 Feb 2021 03:11:21 GMT  
		Size: 3.3 MB (3300351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fde0bc6809561cec22c96436399e0fe7b643a3a1b61cbe0015bf17ed5f48ec4`  
		Last Modified: Thu, 25 Feb 2021 03:11:43 GMT  
		Size: 22.8 MB (22820979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b41c521a3b98aa1e4f31420abc5950fae51cc04d9fb6fa90344622eb5d4811a`  
		Last Modified: Thu, 25 Feb 2021 03:11:36 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:4517161678cffcf965ebb2a9b9ff92956a7a78da32f825f6378823aacf4faa7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:dddfec9e9cdf8bdd2cac2025e1828ace6f39c0f9e1076faa1427e11f34b096a4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.6 MB (108601776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13d3af8fedb4c47f3ee7d210483b2f8f1db049a40b7d56736eb083ebde70b22`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:40 GMT
ADD file:8f75f11b2bd2d50e5912359ae750de06a7b49506df3756c19baf4cc63d900c4f in / 
# Tue, 09 Feb 2021 02:20:40 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:35:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:35:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 05:12:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Feb 2021 05:12:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 24 Feb 2021 18:47:43 GMT
ENV TELEGRAF_VERSION=1.17.3
# Wed, 24 Feb 2021 18:47:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 24 Feb 2021 18:47:47 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 24 Feb 2021 18:47:47 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 24 Feb 2021 18:47:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 18:47:47 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0ecb575e629cd60aa802266a3bc6847dcf4073aa2a6d7d43f717dd61e7b90e0b`  
		Last Modified: Tue, 09 Feb 2021 02:26:22 GMT  
		Size: 50.4 MB (50400198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7467d1831b6947c294d92ee957902c3cd448b17c5ac2103ca5e79d15afb317c3`  
		Last Modified: Tue, 09 Feb 2021 04:46:00 GMT  
		Size: 7.8 MB (7830684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feab2c490a3cea21cc051ff29c33cc9857418edfa1be9966124b18abe1d5ae16`  
		Last Modified: Tue, 09 Feb 2021 04:46:00 GMT  
		Size: 10.0 MB (9996459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bb12ccec32f30558bc0672fb2db77bd29642b4ed86fe3dc5d886e36ab7cdef`  
		Last Modified: Wed, 10 Feb 2021 05:13:12 GMT  
		Size: 17.4 MB (17412680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8771be66e2d28a682acd9b2229052524b4a4466779459c8f48e09fe644611bea`  
		Last Modified: Wed, 10 Feb 2021 05:13:08 GMT  
		Size: 2.9 KB (2870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3b9183e2d25d6bd23609f5394de713bf5a4a666ac75cd215c6b65e4ba786b5`  
		Last Modified: Wed, 24 Feb 2021 18:48:26 GMT  
		Size: 23.0 MB (22958700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f58677597ef6b7ae6393b2a07569ed37ad242b0f511bb0b185307776492c34`  
		Last Modified: Wed, 24 Feb 2021 18:48:21 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm variant v7

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

### `telegraf:latest` - linux; arm64 variant v8

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
