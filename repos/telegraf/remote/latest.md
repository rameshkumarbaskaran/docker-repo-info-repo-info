## `telegraf:latest`

```console
$ docker pull telegraf@sha256:603160cd6f4936ed4914437c91027abe0a77e8166191f0c7403014c49419546a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:cc43a1e734b27b8f76992888ef40c1b6770d716af45083494683b0f45bd0c48d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.3 MB (134296629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf0e9f35af354b67ccddf5073e75bf91bcf5d476d9952aa39807ad7b43b745da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:42 GMT
ADD file:26702ba2c3e94cb21cdb3c550cf01cf848823d160f3417b559116d4c718e5df0 in / 
# Tue, 25 Oct 2022 01:43:42 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 09:23:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:23:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Oct 2022 05:04:28 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 05:04:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 02 Nov 2022 17:21:29 GMT
ENV TELEGRAF_VERSION=1.24.3
# Wed, 02 Nov 2022 17:21:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 02 Nov 2022 17:21:35 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 02 Nov 2022 17:21:35 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 02 Nov 2022 17:21:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Nov 2022 17:21:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:17c9e6141fdb3387e5a1c07d4f9b6a05ac1498e96029fa3ea55470d4504f7770`  
		Last Modified: Tue, 25 Oct 2022 01:47:28 GMT  
		Size: 55.0 MB (55046332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4a4c6caea8801bb0b7377e10220a914da403bc93fa79663cbf2dcf1800b6f1`  
		Last Modified: Tue, 25 Oct 2022 09:47:36 GMT  
		Size: 5.2 MB (5164775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4edced8587e6c18412817019074f5e04a8ede4e2fc89d06af13df3f80d78a70d`  
		Last Modified: Tue, 25 Oct 2022 09:47:36 GMT  
		Size: 10.9 MB (10877322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351dbe0337c2dc42d06f34ca09fd880237614b4b994e56fc4c685e2bbe24a3e8`  
		Last Modified: Wed, 26 Oct 2022 05:05:19 GMT  
		Size: 18.8 MB (18760466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b698d0487ff3ce144a0979269d7e6cb907a6128452ba4a69346c5dceb9251a0`  
		Last Modified: Wed, 26 Oct 2022 05:05:15 GMT  
		Size: 2.9 KB (2902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f08581c18604c1799caf0bc3328cd9083e9de7c523bca67ad9f991a3d18a0e47`  
		Last Modified: Wed, 02 Nov 2022 17:22:19 GMT  
		Size: 44.4 MB (44444490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a870e65bbcdbc3ecd5bb40ec604422000968d303af280eeceb6e1dc4c849e6`  
		Last Modified: Wed, 02 Nov 2022 17:22:11 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:e691720430aef359c1cc637ebccb155c030a981139f2c0062316ebf29aa994a4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124314696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb896f88374da07ed062c7d4243ee0cae3e344d423e10e7415509f2b1c228d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Nov 2022 03:43:06 GMT
ADD file:b9aa70e61b1fbe181b8c48785afc4ef75e7b075b3bc2bc6c329b8397f141efdb in / 
# Tue, 15 Nov 2022 03:43:07 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 12:18:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 12:18:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 15 Nov 2022 19:59:43 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 19:59:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 15 Nov 2022 20:00:10 GMT
ENV TELEGRAF_VERSION=1.24.3
# Tue, 15 Nov 2022 20:00:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 15 Nov 2022 20:00:16 GMT
EXPOSE 8092/udp 8094 8125/udp
# Tue, 15 Nov 2022 20:00:16 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Tue, 15 Nov 2022 20:00:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 15 Nov 2022 20:00:16 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ee6e2ee12efd45cd8105de9bf53619cb3c28867c3974dc5e0137fc0efeb0f577`  
		Last Modified: Tue, 15 Nov 2022 03:49:41 GMT  
		Size: 50.2 MB (50206360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e57b390d8cdf8398d64b2fe40ea3ba6adaff3fd6f221428b28eab7babf88f4`  
		Last Modified: Tue, 15 Nov 2022 12:28:30 GMT  
		Size: 4.9 MB (4932799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6e3dceb24a7026a68b789a939899dc5b68bdfd8bef46052a5a176eca4c76b2`  
		Last Modified: Tue, 15 Nov 2022 12:28:31 GMT  
		Size: 10.2 MB (10218556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a09dc2ad5d15708c33af827818a7920afcc85c714ad1e377cbce9a7f0f286f`  
		Last Modified: Tue, 15 Nov 2022 20:00:53 GMT  
		Size: 17.5 MB (17463030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef14a56e15e24420180503745c2e9604ad396f53801ed3f4ab7d28ab86318d28`  
		Last Modified: Tue, 15 Nov 2022 20:00:49 GMT  
		Size: 2.9 KB (2860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce6b2a62a12113478c54fa1330edb0ee3bd18a3886d43809ce02d63f98b7e30`  
		Last Modified: Tue, 15 Nov 2022 20:01:35 GMT  
		Size: 41.5 MB (41490749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c90376fed5e270fdb1c763a8fa2b0bc5af5d9f2310ae1e1e2edae1b919f855d`  
		Last Modified: Tue, 15 Nov 2022 20:01:27 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:2df43d7d647fc9b0ef00555b324b764714e224a16d0c5525df19ff3171026e26
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 MB (128612700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748da2f4f3cd09f194aea841fb8f61be26171e357b35913055551eae35bb98a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 25 Oct 2022 05:45:55 GMT
ADD file:b16745ece8ef84c028d7e9ac4bf026ac64f885d4170bfcc9d435f237144a1b99 in / 
# Tue, 25 Oct 2022 05:45:56 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:58:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Oct 2022 09:48:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 09:48:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 02 Nov 2022 17:49:49 GMT
ENV TELEGRAF_VERSION=1.24.3
# Wed, 02 Nov 2022 17:49:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 02 Nov 2022 17:49:54 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 02 Nov 2022 17:49:54 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 02 Nov 2022 17:49:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Nov 2022 17:49:55 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8e1d92e7d04d2a9a9880cb45dc3c32c2805912cd86abed96d0ada3ff28748205`  
		Last Modified: Tue, 25 Oct 2022 05:48:40 GMT  
		Size: 53.7 MB (53701966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66eadbf427bb41b3e329a95935c65b09c6d3b7a9c2fa8e08417e497df02ed996`  
		Last Modified: Tue, 25 Oct 2022 08:30:22 GMT  
		Size: 5.2 MB (5151506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9731f4e3bc3680179c10cece663cf0cfe0488918d6795406f4b76f07b787de`  
		Last Modified: Tue, 25 Oct 2022 08:30:22 GMT  
		Size: 10.9 MB (10874174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c72ea8b63e6f16d43f4d9af4c4c9a85eb32f68ef197070617899ae1176d417`  
		Last Modified: Wed, 26 Oct 2022 09:49:35 GMT  
		Size: 18.6 MB (18599385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04c29547de93132c9eb465c23c293e46309e2a89380d99f318ef96001ad9bf2f`  
		Last Modified: Wed, 26 Oct 2022 09:49:32 GMT  
		Size: 2.9 KB (2896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8de0d58d9d05a2d9d7d6b7b4e43e73eb7d1b2ae3e8345abec9fe936f7c88d0e`  
		Last Modified: Wed, 02 Nov 2022 17:50:17 GMT  
		Size: 40.3 MB (40282429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1b41b4645eae202e89701f7bd690e5cc900c37914141f23c3e24969c0c2bc2`  
		Last Modified: Wed, 02 Nov 2022 17:50:12 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
