## `telegraf:latest`

```console
$ docker pull telegraf@sha256:832b9851dcf4981e79cc98bb68e62c20a28a12d12c03e8f8f5ecd2db4fbf7733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:1df08db5a5346628185a4711a9ac6bfbe44a716342a1650b87682a1dc55e1086
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.9 MB (107945492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7606d5ee069fcab20036c4bd521e1133ac8ca31e44f7d241f0d83a36315d6ca6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 13 Oct 2020 01:38:30 GMT
ADD file:6627ad39ea0cb9fcb212342326d14efaff51aece1fd0dc16d5bbcaa25d858622 in / 
# Tue, 13 Oct 2020 01:38:30 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:14:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:14:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 22:44:34 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 22:44:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 29 Oct 2020 01:21:08 GMT
ENV TELEGRAF_VERSION=1.16.1
# Thu, 29 Oct 2020 01:21:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 29 Oct 2020 01:21:13 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 29 Oct 2020 01:21:13 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Thu, 29 Oct 2020 01:21:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Oct 2020 01:21:13 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e4c3d3e4f7b024979a1c12daa4073f6353b2ba92d96418bc90451994927c9bff`  
		Last Modified: Tue, 13 Oct 2020 01:48:02 GMT  
		Size: 50.4 MB (50395978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101c41d0463bc77661fb3343235b16d536a92d2efb687046164d413e51bd4fc4`  
		Last Modified: Tue, 13 Oct 2020 02:28:35 GMT  
		Size: 7.8 MB (7811737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8275efcd805f9905d7def23603618236284b0be6b9e47455c638fbfb03fa9208`  
		Last Modified: Tue, 13 Oct 2020 02:28:35 GMT  
		Size: 10.0 MB (9996326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d9d3d4ee2cf178895c34ba3484e9620e7c241f8075dcf9aae610b1a33b2bef`  
		Last Modified: Tue, 13 Oct 2020 22:45:23 GMT  
		Size: 17.4 MB (17411706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe6b63091110a764935bedc335698000213e2bc4aaf334b6da2060639bf8027`  
		Last Modified: Tue, 13 Oct 2020 22:45:19 GMT  
		Size: 2.9 KB (2870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b9c2814dda25367c31ab8498fba93cb0f3c3e2522ee3ba88b27f143a6a99b3`  
		Last Modified: Thu, 29 Oct 2020 01:21:49 GMT  
		Size: 22.3 MB (22326689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a82f22e1c8d7de1fea8e3af688648419ab3a668c59f05c4307b2aea81e2dc3d5`  
		Last Modified: Thu, 29 Oct 2020 01:21:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:762d7b2590c532e59b7894e5590c7a73c1c3365cb8d98b44ff23b16ce466bf5a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.3 MB (99329165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9743ae4307caf83399a52495d073a559b5a614a63dc5f51b6146ee4691470c0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 13 Oct 2020 00:59:02 GMT
ADD file:e03270d36cef8171f1f6303860ff31bb1c0eb10642b8173bfdfef9f77fa4f89c in / 
# Tue, 13 Oct 2020 00:59:04 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 01:34:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 01:34:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 23:13:17 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 23:13:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 29 Oct 2020 01:59:21 GMT
ENV TELEGRAF_VERSION=1.16.1
# Thu, 29 Oct 2020 01:59:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 29 Oct 2020 01:59:31 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 29 Oct 2020 01:59:32 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Thu, 29 Oct 2020 01:59:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Oct 2020 01:59:33 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:5c0fdcca2cbb5e316a288f39c8c2006f45544568ea04623c036e0b1faa066bbe`  
		Last Modified: Tue, 13 Oct 2020 01:08:04 GMT  
		Size: 45.9 MB (45869258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8216e147de931a74896e75f60d0a331dd1438bc1ae4b2d4c29c8017548e8dcbd`  
		Last Modified: Tue, 13 Oct 2020 01:56:20 GMT  
		Size: 7.1 MB (7097763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf6642121709e17d1419901978da7d29b673d5f936e42ec3241b7d7157e9541`  
		Last Modified: Tue, 13 Oct 2020 01:56:20 GMT  
		Size: 9.3 MB (9343130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6a0d3562077749d37b0c9fc2fc28a538b7e7eb94ccea5e858358c15828841b`  
		Last Modified: Tue, 13 Oct 2020 23:14:38 GMT  
		Size: 16.2 MB (16158104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d734f702ca00ac70d67b7c72628aca0ab61bf44ea7d503e6050ae5e9b50d65e`  
		Last Modified: Tue, 13 Oct 2020 23:14:32 GMT  
		Size: 2.9 KB (2896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df1fff70478765d05476700346d3439ab32ba3a006db2be481c367e9419b39e`  
		Last Modified: Thu, 29 Oct 2020 01:59:52 GMT  
		Size: 20.9 MB (20857830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61064f81a239db6bd9313372ccd1cb037549438d5d6cc4271b76790582d95773`  
		Last Modified: Thu, 29 Oct 2020 01:59:45 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:162cbc5981ed6c60d17660f17d070a0dcb73105408408c3d4a1428f9420b3826
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104583720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915b2b3445e48b662836a74ab7aae6c7184dc6f307036a379f788ecd5ea03748`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 13 Oct 2020 01:40:40 GMT
ADD file:7a9016f6c75910c392bbea2cb9e146d1eba3942cdfd666a44004c79951c5d46f in / 
# Tue, 13 Oct 2020 01:40:45 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:32:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:33:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 14 Oct 2020 02:15:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 14 Oct 2020 02:15:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 29 Oct 2020 01:41:40 GMT
ENV TELEGRAF_VERSION=1.16.1
# Thu, 29 Oct 2020 01:41:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 29 Oct 2020 01:41:47 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 29 Oct 2020 01:41:47 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Thu, 29 Oct 2020 01:41:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Oct 2020 01:41:49 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:04aacb10cb67f5fa248646a0ac9f40af5a6d3b0dbef65505bb7766bed6bf4885`  
		Last Modified: Tue, 13 Oct 2020 01:47:53 GMT  
		Size: 49.2 MB (49175405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136d6e4f4b17bdbefbe60820da5f5711a26d31c075dc69bcaf9b077d7d29262d`  
		Last Modified: Tue, 13 Oct 2020 02:47:32 GMT  
		Size: 7.7 MB (7681432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28db65b8364fc73072a0d5b51199cc9c6b108b4229d92e784b92ae67898dd0bd`  
		Last Modified: Tue, 13 Oct 2020 02:47:32 GMT  
		Size: 10.0 MB (9983936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317e9a06b1254ac01a06e12efe2c55dd39f040017adf07ce8f6949dd06948ef1`  
		Last Modified: Wed, 14 Oct 2020 02:16:03 GMT  
		Size: 17.3 MB (17270065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed886e7e1546ecbc743ef4320f25c4709e68c90b33afbf9fe8cdfafc6b94449`  
		Last Modified: Wed, 14 Oct 2020 02:15:58 GMT  
		Size: 2.9 KB (2898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e658ac2f782bfa34e7f14c8f0ac7cbcb246c913ef0a28ccc90b9f22aed321c34`  
		Last Modified: Thu, 29 Oct 2020 01:42:10 GMT  
		Size: 20.5 MB (20469800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9517ccb1a7aa2c7a6ddfa90dc49c424cc05a3a5feab62895d8bc5bd1f4c593aa`  
		Last Modified: Thu, 29 Oct 2020 01:42:04 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
