## `telegraf:latest`

```console
$ docker pull telegraf@sha256:25b79aaba027ed9dffe336f3f6313b146151fd84aafdf2d8496143cd354540b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:a7cd5ce39fe3285b2fcb40b84919d9556319d5caceab5945e7fca1fb1316938f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115488527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870ee38129f8445492e28f0bcab38e1b212de617e813dac5645ab81f510dd435`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 12 May 2021 01:21:03 GMT
ADD file:1a1eae7a82c66d673971436ce2605e97d107e2934b7cdec876c64923ae6f4f85 in / 
# Wed, 12 May 2021 01:21:03 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:55:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 01:55:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 13 May 2021 01:53:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Thu, 13 May 2021 01:53:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Mon, 24 May 2021 19:45:45 GMT
ENV TELEGRAF_VERSION=1.18.3
# Mon, 24 May 2021 19:45:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Mon, 24 May 2021 19:45:50 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 24 May 2021 19:45:51 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Mon, 24 May 2021 19:45:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 May 2021 19:45:51 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d960726af2bec62a87ceb07182f7b94c47be03909077e23d8226658f80b47f87`  
		Last Modified: Wed, 12 May 2021 01:26:49 GMT  
		Size: 50.4 MB (50433242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d62473a22dec9ffef056b2017968a9dc484c8f836fb6d79f46980b309e9138`  
		Last Modified: Wed, 12 May 2021 02:04:42 GMT  
		Size: 7.8 MB (7832938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8962bc0fad55b13afedfeb6ad5cb06fd065461cf3e1ae4e7aeae5eeb17b179df`  
		Last Modified: Wed, 12 May 2021 02:04:42 GMT  
		Size: 10.0 MB (9997157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a673b7ce359ffba067166d571714630151228ab4091c835a238a9f7a115fdb2e`  
		Last Modified: Thu, 13 May 2021 01:54:21 GMT  
		Size: 17.4 MB (17414412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b810804dad08ec7b108bac304d8ed669a376f34ba6f13f02cdc33ddbb7ba5687`  
		Last Modified: Thu, 13 May 2021 01:54:18 GMT  
		Size: 2.9 KB (2898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e979ae447c6193b2ba6c1d636d4096abe6b0c02e6bfc9e8042a6b5f8a9773bd4`  
		Last Modified: Mon, 24 May 2021 19:46:31 GMT  
		Size: 29.8 MB (29807698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0fe315ae1e3a6df546cd07b837168e37d47d0c1e9dbc144d3e2d9c2d570ea88`  
		Last Modified: Mon, 24 May 2021 19:46:24 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:db787a8846687067a470a1983f0a79e76c9683aed34760f547ddbabcda6ac7eb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.1 MB (106102084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02172fa9044d5ff1bcee04cfb3dfb8af9d7978313d1bbc6ac4df7a77003a3585`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 12 May 2021 01:02:10 GMT
ADD file:51a0472692adf18117444dc1f35d6eb3b4d6d672f28a7f6631f9d5d269b0b85d in / 
# Wed, 12 May 2021 01:02:15 GMT
CMD ["bash"]
# Wed, 12 May 2021 03:44:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 03:44:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 May 2021 15:03:53 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 26 May 2021 15:03:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 26 May 2021 15:04:21 GMT
ENV TELEGRAF_VERSION=1.18.3
# Wed, 26 May 2021 15:04:26 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 26 May 2021 15:04:26 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 26 May 2021 15:04:27 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 26 May 2021 15:04:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 May 2021 15:04:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:89475607b1df9fc7eec7efe2fa845738a16cee3e92c1bb864c1f5a93b8303bc6`  
		Last Modified: Wed, 12 May 2021 01:18:49 GMT  
		Size: 45.9 MB (45916922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60b392acef5d5734279504aa16b720c25b67a3e59b224c69c0cc9ac9772919f`  
		Last Modified: Wed, 12 May 2021 04:01:04 GMT  
		Size: 7.1 MB (7124103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf29c9b0911c9aaa2561392012c561157f1029b7078a0f62be5c13b4a8711f6`  
		Last Modified: Wed, 12 May 2021 04:01:04 GMT  
		Size: 9.3 MB (9343805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7d00033bb71d7df4f22c6cab29f1c4951974bb39e09843ce54c4e3c3d242df`  
		Last Modified: Wed, 26 May 2021 15:05:06 GMT  
		Size: 16.2 MB (16159124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8058a7359beab800f59c22cf547acc48b3f6a4db91012ed17636a3c8bfca94a`  
		Last Modified: Wed, 26 May 2021 15:05:02 GMT  
		Size: 2.9 KB (2896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab7a1ff1c7216c66b8a170b9f733d4fadeb2ce7d069a3cc6a8d4ab59f8e20dc`  
		Last Modified: Wed, 26 May 2021 15:05:46 GMT  
		Size: 27.6 MB (27555049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17f3b423dff932e8c6a0b4d3fe32e22d9a52111c5cace337f994f3c991fc4f1`  
		Last Modified: Wed, 26 May 2021 15:05:39 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:3a321ed3cab8af4adbfe966cd0674b6e7929b097a12c41fcb4fbd3525452bfb0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 MB (111150844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de6e019a868bf4dac9e823aeba7cd6b18143ed3cd1e6c7845969157e20c856c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 12 May 2021 00:50:48 GMT
ADD file:ff9983cd659b3fc32ddfbbdeda76a971afd7d399e6d8b98faea3a9ead0e598f6 in / 
# Wed, 12 May 2021 00:50:52 GMT
CMD ["bash"]
# Thu, 27 May 2021 20:51:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 20:51:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 28 May 2021 12:27:52 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 28 May 2021 12:27:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 28 May 2021 12:28:09 GMT
ENV TELEGRAF_VERSION=1.18.3
# Fri, 28 May 2021 12:28:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 28 May 2021 12:28:12 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 28 May 2021 12:28:13 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Fri, 28 May 2021 12:28:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 May 2021 12:28:13 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c54d9402d498e45ed396b5b6fe836f55e4ccadbad745decda3e9f83d880bc677`  
		Last Modified: Wed, 12 May 2021 01:01:40 GMT  
		Size: 49.2 MB (49225351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8aff564b222789ed2823b88e0f1a69ac00cbcbf9349acb8a363d5ef9724182`  
		Last Modified: Thu, 27 May 2021 21:05:15 GMT  
		Size: 7.7 MB (7694906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e893e0778bb86166fb6799aec4e4ac337c4f10172386c8ae9cf3c787331d7d`  
		Last Modified: Thu, 27 May 2021 21:05:15 GMT  
		Size: 10.0 MB (9984325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9951068a79a194185c06d1629e86141479762b05f1b56ced254860652dcb88c`  
		Last Modified: Fri, 28 May 2021 12:28:40 GMT  
		Size: 17.3 MB (17269460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b2634dc9eba2ee633ea11b836d5eb38d000b8c2a7ace1c354ec8979fa7257f`  
		Last Modified: Fri, 28 May 2021 12:28:37 GMT  
		Size: 2.9 KB (2908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a570dc095ebd88b276729e8db6c04cbec2b6690ff52bf838201ab493844b21`  
		Last Modified: Fri, 28 May 2021 12:29:14 GMT  
		Size: 27.0 MB (26973710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21e52615ab06e8f50768b5dc5790f21bf440a55a4e4030940bfbe47b4daaeaa`  
		Last Modified: Fri, 28 May 2021 12:29:09 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
