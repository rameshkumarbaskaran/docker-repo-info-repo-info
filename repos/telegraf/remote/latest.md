## `telegraf:latest`

```console
$ docker pull telegraf@sha256:8aff5a74822413552542a43adbcfb519cba234b16def8a1903f0ae4521a71071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:8c78d39af0aea1fa2202466a39402cc17a5a88d32aa9ffd539a4fe2ba823fe1a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148375707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c484ec3137fb1dbf9059cd5314369e411bf185d9477261a84457c293128cdebb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 07 Sep 2023 00:20:39 GMT
ADD file:8415eb847ca46ed1aa1695965af86f1a0f09e8859a7b3c07b2f719404b665102 in / 
# Thu, 07 Sep 2023 00:20:39 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 02:56:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 22:44:17 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 22:44:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 11 Sep 2023 19:30:47 GMT
ENV TELEGRAF_VERSION=1.28.0
# Mon, 11 Sep 2023 19:30:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Mon, 11 Sep 2023 19:30:52 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 11 Sep 2023 19:30:52 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Mon, 11 Sep 2023 19:30:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Sep 2023 19:30:52 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:012c0b3e998c1a0c0bedcf712eaaafb188580529dd026a04aa1ce13fdb39e42b`  
		Last Modified: Thu, 07 Sep 2023 00:24:59 GMT  
		Size: 49.6 MB (49557216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00046d1e755ea94fa55a700ca9a10597e4fac7c47be19d970a359b0267a51fbf`  
		Last Modified: Thu, 07 Sep 2023 03:04:41 GMT  
		Size: 24.0 MB (24030451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7deb6a885cf05af87b03dc0760c49315846a46a14e40307838388402c787ac5b`  
		Last Modified: Thu, 07 Sep 2023 22:45:17 GMT  
		Size: 19.1 MB (19143468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef685fa60eef2ecb32de1be898cc22426d5074884e2334991558e776a5be1f2c`  
		Last Modified: Thu, 07 Sep 2023 22:45:14 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c128aa5b6090fc98a90e906f8790489507219a65fedcb8641cd01dd6758a807`  
		Last Modified: Mon, 11 Sep 2023 19:31:30 GMT  
		Size: 55.6 MB (55642426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1656b801a5244ee631d0794d7542bf72e7d457ce9ae1306b477140109fbb3fdf`  
		Last Modified: Mon, 11 Sep 2023 19:31:22 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:126c14a88c826e0b22636cbc76ca4bb47eef129509b31686e0ee4b625ee82499
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136570373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9aed279a1ce0f91d37c4b40b84c778e1c551dfa8c182db2c32453d56ca596f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 07 Sep 2023 00:57:31 GMT
ADD file:33a39c01d7e209fab46b54083ee271e3bdd3d4dccc3a6e8635cbe0989c92c53e in / 
# Thu, 07 Sep 2023 00:57:33 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 01:33:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 19:33:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 19:33:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 11 Sep 2023 20:50:47 GMT
ENV TELEGRAF_VERSION=1.28.0
# Mon, 11 Sep 2023 20:51:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Mon, 11 Sep 2023 20:51:01 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 11 Sep 2023 20:51:01 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Mon, 11 Sep 2023 20:51:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Sep 2023 20:51:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4e1ef44b7a1dc38ec98ec01f961a48844fdf07e1ff182d55daae1c01406302a9`  
		Last Modified: Thu, 07 Sep 2023 01:02:04 GMT  
		Size: 45.2 MB (45233200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c71aa39a4f5a50ddeb9942b08a954d6892177b5409397b1e948e88ac7f6575a`  
		Last Modified: Thu, 07 Sep 2023 01:44:56 GMT  
		Size: 21.9 MB (21936900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7478dca3d662e96d838b4be3ec8d69a5207bc88ec0e58fc729e20efc92c6b314`  
		Last Modified: Thu, 07 Sep 2023 19:34:44 GMT  
		Size: 18.0 MB (17989213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf6e8baa84204d932b09bd493be5742abf6ac0c77352d7e55044f79ad2d06d5`  
		Last Modified: Thu, 07 Sep 2023 19:34:39 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df3208e341bba7662d466867865ef87330e81798e175afecaad3eba6d340ac3`  
		Last Modified: Mon, 11 Sep 2023 20:51:22 GMT  
		Size: 51.4 MB (51408916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea98c5c143e3cb33bf2a0412385c0dbadb858bbee9a5bcf6ad8d03499e3a6596`  
		Last Modified: Mon, 11 Sep 2023 20:51:12 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:d173d976be495a400a1555fc7c2d7cb63c20ceb8357ebdb3d4967b83c1dc422b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142612225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eedba4e6884be984fb2e708d2b718b80d0c46a589dfee949887556c920678e1d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:31 GMT
ADD file:f9dd2b1cc0ba261acd8a3e500c54f6b6e0a46131a32988bfd71cf3c6fc5a7d13 in / 
# Thu, 07 Sep 2023 00:39:32 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 06:51:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 19:38:20 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 19:38:21 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 11 Sep 2023 19:26:08 GMT
ENV TELEGRAF_VERSION=1.28.0
# Mon, 11 Sep 2023 19:26:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Mon, 11 Sep 2023 19:26:16 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 11 Sep 2023 19:26:16 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Mon, 11 Sep 2023 19:26:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Sep 2023 19:26:16 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:fa34261389f3dee2ecffe9bfe38ae7fd05a1908e98a7486354905aee0f648a6e`  
		Last Modified: Thu, 07 Sep 2023 00:42:39 GMT  
		Size: 49.6 MB (49590783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993525952a483617183655b735562fd3eee4b3a85a472e3dc3c79a258adca100`  
		Last Modified: Thu, 07 Sep 2023 06:59:20 GMT  
		Size: 23.6 MB (23570086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72451c72e989c3737872403fa80ba26c9c18121690e8fc4bf54784bb55f7618`  
		Last Modified: Thu, 07 Sep 2023 19:39:15 GMT  
		Size: 19.1 MB (19077240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8be5dd722b46de02a012c0f6aae92ffa934c2f8d52fd5485345ab0eed03a2b`  
		Last Modified: Thu, 07 Sep 2023 19:39:13 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795f426cb4e7e2b39b441a89d694efb53ef2ad5dadf6130995392bbf00a287f8`  
		Last Modified: Mon, 11 Sep 2023 19:26:56 GMT  
		Size: 50.4 MB (50371960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae94e7bd553ed095f22735d3d09458756ba07f533166c95c6587d8a27d7689aa`  
		Last Modified: Mon, 11 Sep 2023 19:26:50 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
