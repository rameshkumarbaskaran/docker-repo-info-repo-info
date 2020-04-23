## `telegraf:latest`

```console
$ docker pull telegraf@sha256:26eb919f9baea00d3b2cb3e6d44d9e53a95bf51716cfff3896d9bcc599096f5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:9bbd43a63a509632402d3371e55b0618659520338aad2e54541ccda03ed9f793
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 MB (97902074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90b865dcac2acb58e72dd07b89210842086d84fa13395bee8c18e27edd0a411`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:22 GMT
ADD file:9f6f0c8b90de3204ad5db95d10d8aa76b42454def6ac811c888ad4e274292c9c in / 
# Thu, 16 Apr 2020 03:27:22 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 04:12:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 04:12:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 17 Apr 2020 00:27:34 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 00:27:37 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 17 Apr 2020 00:28:02 GMT
ENV TELEGRAF_VERSION=1.14.1
# Fri, 17 Apr 2020 00:28:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 17 Apr 2020 00:28:06 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 17 Apr 2020 00:28:06 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Fri, 17 Apr 2020 00:28:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2020 00:28:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:7568c21980bd8003ca9d23a218302c6386aac91e069cc0c0be6bedf45476f056`  
		Last Modified: Thu, 16 Apr 2020 03:34:47 GMT  
		Size: 45.4 MB (45375910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9f2207c812b2530bc06352aa57cf50244726c52db6ff775ca9f9a76d6ea880`  
		Last Modified: Thu, 16 Apr 2020 04:20:21 GMT  
		Size: 10.8 MB (10797394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe350d2b14088b19ffff7a1c6683f0949fb0161e6ab87011a24e21e5d7fed4e`  
		Last Modified: Thu, 16 Apr 2020 04:20:19 GMT  
		Size: 4.3 MB (4340188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf38072f953130145014cafc3ae8a51015cb501cb8442527cb6e39f788e5ecc5`  
		Last Modified: Fri, 17 Apr 2020 00:28:27 GMT  
		Size: 16.0 MB (15964841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4200b5befcebaf2a662d891e97da5b77304254f7ed15ab5610170ce7c3a0ca7b`  
		Last Modified: Fri, 17 Apr 2020 00:28:23 GMT  
		Size: 2.8 KB (2775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c11b074a950b4910f7420d349256fa297f0b55bb7e804bc1d6a0d9c9a0ff2af8`  
		Last Modified: Fri, 17 Apr 2020 00:28:52 GMT  
		Size: 21.4 MB (21420782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff66d8fa2a61cebe099750838e689e0c5a98d81769767aef578a6ddf5d4ad85e`  
		Last Modified: Fri, 17 Apr 2020 00:28:46 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:a7dce1f73a4da00e5059a834d09b489f773418656e38dcf2b3024cde452e5841
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90490056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d4e06057f2b37d4fb30349bd239d8e707a953144ee243986eacd6c0ebdf198`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 23 Apr 2020 01:07:13 GMT
ADD file:af00fcaffcce2a55b74d080d33cbc9ce5bcf91faf659b887f508c06803fa64bd in / 
# Thu, 23 Apr 2020 01:07:15 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 04:23:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:23:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 19:45:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 19:45:49 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 23 Apr 2020 19:46:29 GMT
ENV TELEGRAF_VERSION=1.14.1
# Thu, 23 Apr 2020 19:46:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 23 Apr 2020 19:46:39 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 23 Apr 2020 19:46:40 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Thu, 23 Apr 2020 19:46:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 19:46:41 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4168e46f368afa15fa660f5197fb2946df81a85078c82e37a76d2610fb3999f1`  
		Last Modified: Thu, 23 Apr 2020 01:14:13 GMT  
		Size: 42.1 MB (42101192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9bc0e3bfcb00266e5034f08dae24b7862a41a069b0db0c68beb50e66983e602`  
		Last Modified: Thu, 23 Apr 2020 04:34:11 GMT  
		Size: 9.5 MB (9498287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3461f3bce5656c429f5d3faee144de5778a7f01ecd08241211c4badd34a7197b`  
		Last Modified: Thu, 23 Apr 2020 04:34:09 GMT  
		Size: 3.9 MB (3918722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c89366892b85101189243eb93a0a4a9fdbc21b615fc8d3aa603e1b2b6f1695c`  
		Last Modified: Thu, 23 Apr 2020 19:46:59 GMT  
		Size: 14.8 MB (14839164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74aa6be8071a1d0d4fcd5cda97ee3af0b63b759316ed4b27885d63e494e4958`  
		Last Modified: Thu, 23 Apr 2020 19:46:53 GMT  
		Size: 2.8 KB (2801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1668ff82c5768d9f7c77063b65d5396a641115f6052533b927c89becb2b030f3`  
		Last Modified: Thu, 23 Apr 2020 19:47:31 GMT  
		Size: 20.1 MB (20129704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3fde1a42a7bcfa704a405e3f4790ad507244e487583b74dff427d0d7be7f860`  
		Last Modified: Thu, 23 Apr 2020 19:47:23 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:c42079779f2b6623b147ad7f41326e0bc7292ec6cd43f14df931736d1db6841c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92257045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88dcd62822224da442369e04a093110325b70846b16a88872a6e3acbbcf47d13`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 16 Apr 2020 02:44:49 GMT
ADD file:6d09304a2db2752e78b9ce9610594102dc756aa4cd210f85bbfa21105c7dd88f in / 
# Thu, 16 Apr 2020 02:44:52 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:21:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 03:21:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Apr 2020 23:25:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 23:25:41 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 16 Apr 2020 23:26:10 GMT
ENV TELEGRAF_VERSION=1.14.1
# Thu, 16 Apr 2020 23:26:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 16 Apr 2020 23:26:15 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 16 Apr 2020 23:26:15 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Thu, 16 Apr 2020 23:26:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 23:26:16 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:65d54b492d599e7c785a582a0f70195e1f09f0886e54cb7788f1021f383eb4ed`  
		Last Modified: Thu, 16 Apr 2020 02:51:10 GMT  
		Size: 43.2 MB (43159230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be35cdee43e0bbb89c0867d201ff274ba25b6ea9bfe7f8f0c1d1d6de36ab08a`  
		Last Modified: Thu, 16 Apr 2020 03:30:52 GMT  
		Size: 9.7 MB (9748442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b803ac2c0e69edab9b8db20bee0f9dfc0191a7975c94d4d2ea0088d5a1759be8`  
		Last Modified: Thu, 16 Apr 2020 03:30:51 GMT  
		Size: 4.1 MB (4094379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ce3353b1907451b19cdc2a106a2de3347447827f244ab72e3fc38749527923`  
		Last Modified: Thu, 16 Apr 2020 23:26:34 GMT  
		Size: 15.5 MB (15530133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70de808a3c5a0b9f18177c664db6bda85e6e9debdb6e73cc062e24176a3bc06a`  
		Last Modified: Thu, 16 Apr 2020 23:26:29 GMT  
		Size: 2.8 KB (2801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ac280ece10758707d6b5c91fea437aa76d19fcbf721e48d8ef155de80a6f82`  
		Last Modified: Thu, 16 Apr 2020 23:26:59 GMT  
		Size: 19.7 MB (19721875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89dc1e315468c63e16eef723a049be1ec1925f95e0cde49033fc0edc953e9404`  
		Last Modified: Thu, 16 Apr 2020 23:26:52 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
