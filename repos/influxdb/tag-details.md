<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `influxdb`

-	[`influxdb:1.7`](#influxdb17)
-	[`influxdb:1.7.10`](#influxdb1710)
-	[`influxdb:1.7.10-alpine`](#influxdb1710-alpine)
-	[`influxdb:1.7.10-data`](#influxdb1710-data)
-	[`influxdb:1.7.10-data-alpine`](#influxdb1710-data-alpine)
-	[`influxdb:1.7.10-meta`](#influxdb1710-meta)
-	[`influxdb:1.7.10-meta-alpine`](#influxdb1710-meta-alpine)
-	[`influxdb:1.7-alpine`](#influxdb17-alpine)
-	[`influxdb:1.7-data`](#influxdb17-data)
-	[`influxdb:1.7-data-alpine`](#influxdb17-data-alpine)
-	[`influxdb:1.7-meta`](#influxdb17-meta)
-	[`influxdb:1.7-meta-alpine`](#influxdb17-meta-alpine)
-	[`influxdb:1.8`](#influxdb18)
-	[`influxdb:1.8.1`](#influxdb181)
-	[`influxdb:1.8.1-alpine`](#influxdb181-alpine)
-	[`influxdb:1.8.1-data`](#influxdb181-data)
-	[`influxdb:1.8.1-data-alpine`](#influxdb181-data-alpine)
-	[`influxdb:1.8.1-meta`](#influxdb181-meta)
-	[`influxdb:1.8.1-meta-alpine`](#influxdb181-meta-alpine)
-	[`influxdb:1.8-alpine`](#influxdb18-alpine)
-	[`influxdb:1.8-data`](#influxdb18-data)
-	[`influxdb:1.8-data-alpine`](#influxdb18-data-alpine)
-	[`influxdb:1.8-meta`](#influxdb18-meta)
-	[`influxdb:1.8-meta-alpine`](#influxdb18-meta-alpine)
-	[`influxdb:alpine`](#influxdbalpine)
-	[`influxdb:data`](#influxdbdata)
-	[`influxdb:data-alpine`](#influxdbdata-alpine)
-	[`influxdb:latest`](#influxdblatest)
-	[`influxdb:meta`](#influxdbmeta)
-	[`influxdb:meta-alpine`](#influxdbmeta-alpine)

## `influxdb:1.7`

```console
$ docker pull influxdb@sha256:bba86c742adc1ab27d115fbfc35e9d749579849f80c7c00eaf0afe7578378421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.7` - linux; amd64

```console
$ docker pull influxdb@sha256:b6b1f6ddc53b0b2eb54ba8db7fbb5125f9798d8a708695d55e51069a3bde6eed
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124561187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0fd32adbe245274693d56040019439e4d9069b17d79f0111d4682ede2bc4d28`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 22 Jul 2020 02:06:48 GMT
ADD file:f98fe3d719ea765cb59da025d506d0bbd6db7a842b6b63c58c8d4d65b51bdb1f in / 
# Wed, 22 Jul 2020 02:06:48 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:11:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:11:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 23:31:14 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 22 Jul 2020 23:31:14 GMT
ENV INFLUXDB_VERSION=1.7.10
# Wed, 22 Jul 2020 23:31:22 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 22 Jul 2020 23:31:22 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 22 Jul 2020 23:31:22 GMT
EXPOSE 8086
# Wed, 22 Jul 2020 23:31:23 GMT
VOLUME [/var/lib/influxdb]
# Wed, 22 Jul 2020 23:31:23 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 22 Jul 2020 23:31:23 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 22 Jul 2020 23:31:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jul 2020 23:31:23 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:7e6d8ed603557d9bf077a9ace4ee506501970a4938b9a704f040ad15f22bd4e8`  
		Last Modified: Wed, 22 Jul 2020 02:12:13 GMT  
		Size: 45.4 MB (45369674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43421f771d04c7019cae6594c2b95ad92d692750fc57d201b5108c1bef2d095e`  
		Last Modified: Wed, 22 Jul 2020 03:19:27 GMT  
		Size: 10.8 MB (10750266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36327c39ae4245e3dcfa5b77a55cff18b6d81f2b4ca1b0e107da95ecd6b225f`  
		Last Modified: Wed, 22 Jul 2020 03:19:26 GMT  
		Size: 4.3 MB (4339838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a444ea13ca5c9a75f3861a3ed19ef97219c52e6a9609a61e75c76d1d9b5f675`  
		Last Modified: Wed, 22 Jul 2020 23:33:09 GMT  
		Size: 2.8 KB (2773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a0450828b903c85ece7538bb617d9e83732fe715f39588eb42bb876e006849`  
		Last Modified: Wed, 22 Jul 2020 23:33:19 GMT  
		Size: 64.1 MB (64096920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e14bf7c248570b58a4af25e24d664782aaf50ba624fb26127a6d4e029659b4e5`  
		Last Modified: Wed, 22 Jul 2020 23:33:09 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8327189bfa49a8e1174796310b53e0f7786841e97c0b416f21f9263f71aa7dc6`  
		Last Modified: Wed, 22 Jul 2020 23:33:09 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6cbd262585b1d3f2667c367fb2dd25080bd5e62eba2bad458bc9cf14739ec1`  
		Last Modified: Wed, 22 Jul 2020 23:33:09 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:79dcc74c7c58e16c8029fa74c4dca416fda9e6190b1ba3549ad05d64c5e4fe5a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.1 MB (116113826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b80c588545102aefd7ad8a8ff874f8cb398624ff1b542f0075cc6717758966`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 04 Aug 2020 05:01:04 GMT
ADD file:0ba6f3203fb10e66124d03088d234e92fc908c572ec7eed268e866623a383a7d in / 
# Tue, 04 Aug 2020 05:01:07 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 08:16:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 08:16:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 04:21:30 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 05 Aug 2020 04:21:31 GMT
ENV INFLUXDB_VERSION=1.7.10
# Wed, 05 Aug 2020 04:21:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 05 Aug 2020 04:21:45 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 05 Aug 2020 04:21:45 GMT
EXPOSE 8086
# Wed, 05 Aug 2020 04:21:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 05 Aug 2020 04:21:48 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 05 Aug 2020 04:21:49 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 05 Aug 2020 04:21:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Aug 2020 04:21:50 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:323178d00ec2c5eb5ffb9cb696a52eaf8683dcf2eb605c742da2953556f06e37`  
		Last Modified: Tue, 04 Aug 2020 05:08:40 GMT  
		Size: 42.1 MB (42111382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b4e15a79453f6ae10815d79c8f4590aef2f1ac2979c192ff7f1ed0fbf04e60`  
		Last Modified: Tue, 04 Aug 2020 08:30:43 GMT  
		Size: 9.4 MB (9443881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf9cb1ef704caf3af8a2ed43dc12884b4f74ac867ce95f60bd8996f51fde770`  
		Last Modified: Tue, 04 Aug 2020 08:30:41 GMT  
		Size: 3.9 MB (3918490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ad1ae0455f086a984fe5ca80430d33819b38c31587c5972ddc6aedd904cbf6`  
		Last Modified: Wed, 05 Aug 2020 04:22:33 GMT  
		Size: 2.8 KB (2806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1267d806e70c298ed68589d4672a3cccc8a093edd6b7a8385c28559abf8e58cd`  
		Last Modified: Wed, 05 Aug 2020 04:22:50 GMT  
		Size: 60.6 MB (60635553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ae7de07ea51a6b197afd534c050863711d4b45bd82a9334cb4de6e5c56a75c`  
		Last Modified: Wed, 05 Aug 2020 04:22:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab345706f1299dfeda06e2a332cdbc1927091fd4b8764e4e23db8dcf152dcb69`  
		Last Modified: Wed, 05 Aug 2020 04:22:33 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d39539457854df0b0b36b1db9790dd70f972da884ef0c6988cde051c25214ec`  
		Last Modified: Wed, 05 Aug 2020 04:22:33 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:42e6b269758d654376936144da3e8ae7eebd7b5ea8fded9ab616b9c7b6469cfa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 MB (117098893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0f883f619093062c36f6b219de2bbc006b130d1d939f624737471dd0952ab1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 04 Aug 2020 06:59:38 GMT
ADD file:0a7a65de4c9dc6ea7f7ac97362a47b82a02a45ecab668ddc84cfd011dad26d33 in / 
# Tue, 04 Aug 2020 06:59:41 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 11:16:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 11:16:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 07:16:40 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 05 Aug 2020 07:16:40 GMT
ENV INFLUXDB_VERSION=1.7.10
# Wed, 05 Aug 2020 07:16:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 05 Aug 2020 07:16:51 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 05 Aug 2020 07:16:52 GMT
EXPOSE 8086
# Wed, 05 Aug 2020 07:16:53 GMT
VOLUME [/var/lib/influxdb]
# Wed, 05 Aug 2020 07:16:54 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 05 Aug 2020 07:16:55 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 05 Aug 2020 07:16:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Aug 2020 07:16:58 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:708f9b01fc1a5dff70f7d40443ac7dd0ee1d0ae93202b6f305f4e3627cea7d22`  
		Last Modified: Tue, 04 Aug 2020 07:06:12 GMT  
		Size: 43.2 MB (43171643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06dc3a0299d558e9f611edd56658d792af018276662c8c30d86476a05c18b00b`  
		Last Modified: Tue, 04 Aug 2020 11:26:22 GMT  
		Size: 9.7 MB (9700890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7feaa2634e51f929e9ca86765cd5579cdf0809084c80d6787166627ca2aed6d4`  
		Last Modified: Tue, 04 Aug 2020 11:26:21 GMT  
		Size: 4.1 MB (4094122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691da85e3888bd2ba9b2a633be8705530081b5fde5f1bfe36535d5a56097f227`  
		Last Modified: Wed, 05 Aug 2020 07:17:36 GMT  
		Size: 2.8 KB (2803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a660ee63c1c953f1c11182f99cf4fe4a5bab347a42ab0d2f5239973be91e489`  
		Last Modified: Wed, 05 Aug 2020 07:17:52 GMT  
		Size: 60.1 MB (60127717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54305954dbb5193e67e13d2f4e8d273657dc2a4d49f6c003897eb461795401a6`  
		Last Modified: Wed, 05 Aug 2020 07:17:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561cd249002586daae6fbc84652f496351a18315d32dbe6f500eab0525ce7a6e`  
		Last Modified: Wed, 05 Aug 2020 07:17:36 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89cab6405998177b1e9ec67a48284330b603148810a76df0a500f9c5bf3d7829`  
		Last Modified: Wed, 05 Aug 2020 07:17:36 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10`

```console
$ docker pull influxdb@sha256:bba86c742adc1ab27d115fbfc35e9d749579849f80c7c00eaf0afe7578378421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.7.10` - linux; amd64

```console
$ docker pull influxdb@sha256:b6b1f6ddc53b0b2eb54ba8db7fbb5125f9798d8a708695d55e51069a3bde6eed
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124561187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0fd32adbe245274693d56040019439e4d9069b17d79f0111d4682ede2bc4d28`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 22 Jul 2020 02:06:48 GMT
ADD file:f98fe3d719ea765cb59da025d506d0bbd6db7a842b6b63c58c8d4d65b51bdb1f in / 
# Wed, 22 Jul 2020 02:06:48 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:11:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:11:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 23:31:14 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 22 Jul 2020 23:31:14 GMT
ENV INFLUXDB_VERSION=1.7.10
# Wed, 22 Jul 2020 23:31:22 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 22 Jul 2020 23:31:22 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 22 Jul 2020 23:31:22 GMT
EXPOSE 8086
# Wed, 22 Jul 2020 23:31:23 GMT
VOLUME [/var/lib/influxdb]
# Wed, 22 Jul 2020 23:31:23 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 22 Jul 2020 23:31:23 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 22 Jul 2020 23:31:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jul 2020 23:31:23 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:7e6d8ed603557d9bf077a9ace4ee506501970a4938b9a704f040ad15f22bd4e8`  
		Last Modified: Wed, 22 Jul 2020 02:12:13 GMT  
		Size: 45.4 MB (45369674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43421f771d04c7019cae6594c2b95ad92d692750fc57d201b5108c1bef2d095e`  
		Last Modified: Wed, 22 Jul 2020 03:19:27 GMT  
		Size: 10.8 MB (10750266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36327c39ae4245e3dcfa5b77a55cff18b6d81f2b4ca1b0e107da95ecd6b225f`  
		Last Modified: Wed, 22 Jul 2020 03:19:26 GMT  
		Size: 4.3 MB (4339838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a444ea13ca5c9a75f3861a3ed19ef97219c52e6a9609a61e75c76d1d9b5f675`  
		Last Modified: Wed, 22 Jul 2020 23:33:09 GMT  
		Size: 2.8 KB (2773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a0450828b903c85ece7538bb617d9e83732fe715f39588eb42bb876e006849`  
		Last Modified: Wed, 22 Jul 2020 23:33:19 GMT  
		Size: 64.1 MB (64096920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e14bf7c248570b58a4af25e24d664782aaf50ba624fb26127a6d4e029659b4e5`  
		Last Modified: Wed, 22 Jul 2020 23:33:09 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8327189bfa49a8e1174796310b53e0f7786841e97c0b416f21f9263f71aa7dc6`  
		Last Modified: Wed, 22 Jul 2020 23:33:09 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6cbd262585b1d3f2667c367fb2dd25080bd5e62eba2bad458bc9cf14739ec1`  
		Last Modified: Wed, 22 Jul 2020 23:33:09 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7.10` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:79dcc74c7c58e16c8029fa74c4dca416fda9e6190b1ba3549ad05d64c5e4fe5a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.1 MB (116113826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b80c588545102aefd7ad8a8ff874f8cb398624ff1b542f0075cc6717758966`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 04 Aug 2020 05:01:04 GMT
ADD file:0ba6f3203fb10e66124d03088d234e92fc908c572ec7eed268e866623a383a7d in / 
# Tue, 04 Aug 2020 05:01:07 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 08:16:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 08:16:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 04:21:30 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 05 Aug 2020 04:21:31 GMT
ENV INFLUXDB_VERSION=1.7.10
# Wed, 05 Aug 2020 04:21:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 05 Aug 2020 04:21:45 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 05 Aug 2020 04:21:45 GMT
EXPOSE 8086
# Wed, 05 Aug 2020 04:21:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 05 Aug 2020 04:21:48 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 05 Aug 2020 04:21:49 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 05 Aug 2020 04:21:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Aug 2020 04:21:50 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:323178d00ec2c5eb5ffb9cb696a52eaf8683dcf2eb605c742da2953556f06e37`  
		Last Modified: Tue, 04 Aug 2020 05:08:40 GMT  
		Size: 42.1 MB (42111382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b4e15a79453f6ae10815d79c8f4590aef2f1ac2979c192ff7f1ed0fbf04e60`  
		Last Modified: Tue, 04 Aug 2020 08:30:43 GMT  
		Size: 9.4 MB (9443881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf9cb1ef704caf3af8a2ed43dc12884b4f74ac867ce95f60bd8996f51fde770`  
		Last Modified: Tue, 04 Aug 2020 08:30:41 GMT  
		Size: 3.9 MB (3918490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ad1ae0455f086a984fe5ca80430d33819b38c31587c5972ddc6aedd904cbf6`  
		Last Modified: Wed, 05 Aug 2020 04:22:33 GMT  
		Size: 2.8 KB (2806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1267d806e70c298ed68589d4672a3cccc8a093edd6b7a8385c28559abf8e58cd`  
		Last Modified: Wed, 05 Aug 2020 04:22:50 GMT  
		Size: 60.6 MB (60635553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ae7de07ea51a6b197afd534c050863711d4b45bd82a9334cb4de6e5c56a75c`  
		Last Modified: Wed, 05 Aug 2020 04:22:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab345706f1299dfeda06e2a332cdbc1927091fd4b8764e4e23db8dcf152dcb69`  
		Last Modified: Wed, 05 Aug 2020 04:22:33 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d39539457854df0b0b36b1db9790dd70f972da884ef0c6988cde051c25214ec`  
		Last Modified: Wed, 05 Aug 2020 04:22:33 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7.10` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:42e6b269758d654376936144da3e8ae7eebd7b5ea8fded9ab616b9c7b6469cfa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 MB (117098893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0f883f619093062c36f6b219de2bbc006b130d1d939f624737471dd0952ab1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 04 Aug 2020 06:59:38 GMT
ADD file:0a7a65de4c9dc6ea7f7ac97362a47b82a02a45ecab668ddc84cfd011dad26d33 in / 
# Tue, 04 Aug 2020 06:59:41 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 11:16:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 11:16:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 07:16:40 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 05 Aug 2020 07:16:40 GMT
ENV INFLUXDB_VERSION=1.7.10
# Wed, 05 Aug 2020 07:16:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 05 Aug 2020 07:16:51 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 05 Aug 2020 07:16:52 GMT
EXPOSE 8086
# Wed, 05 Aug 2020 07:16:53 GMT
VOLUME [/var/lib/influxdb]
# Wed, 05 Aug 2020 07:16:54 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 05 Aug 2020 07:16:55 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 05 Aug 2020 07:16:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Aug 2020 07:16:58 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:708f9b01fc1a5dff70f7d40443ac7dd0ee1d0ae93202b6f305f4e3627cea7d22`  
		Last Modified: Tue, 04 Aug 2020 07:06:12 GMT  
		Size: 43.2 MB (43171643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06dc3a0299d558e9f611edd56658d792af018276662c8c30d86476a05c18b00b`  
		Last Modified: Tue, 04 Aug 2020 11:26:22 GMT  
		Size: 9.7 MB (9700890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7feaa2634e51f929e9ca86765cd5579cdf0809084c80d6787166627ca2aed6d4`  
		Last Modified: Tue, 04 Aug 2020 11:26:21 GMT  
		Size: 4.1 MB (4094122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691da85e3888bd2ba9b2a633be8705530081b5fde5f1bfe36535d5a56097f227`  
		Last Modified: Wed, 05 Aug 2020 07:17:36 GMT  
		Size: 2.8 KB (2803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a660ee63c1c953f1c11182f99cf4fe4a5bab347a42ab0d2f5239973be91e489`  
		Last Modified: Wed, 05 Aug 2020 07:17:52 GMT  
		Size: 60.1 MB (60127717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54305954dbb5193e67e13d2f4e8d273657dc2a4d49f6c003897eb461795401a6`  
		Last Modified: Wed, 05 Aug 2020 07:17:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561cd249002586daae6fbc84652f496351a18315d32dbe6f500eab0525ce7a6e`  
		Last Modified: Wed, 05 Aug 2020 07:17:36 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89cab6405998177b1e9ec67a48284330b603148810a76df0a500f9c5bf3d7829`  
		Last Modified: Wed, 05 Aug 2020 07:17:36 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10-alpine`

```console
$ docker pull influxdb@sha256:22222e93aa7cfeaef35d64a3b34c6c00130e62564be44d5b4af1a93bd066be95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:25b986e522bebbfaf13549edf96406da0b55af3c45f806c49813472f68579ca1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68530288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3907dabe467bcb68c89f7f56065ba5ccf90bcf3f43979819cdcddf9dd982bcd9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:15:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Apr 2020 15:28:09 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 24 Apr 2020 15:28:09 GMT
ENV INFLUXDB_VERSION=1.7.10
# Mon, 03 Aug 2020 22:33:55 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 03 Aug 2020 22:33:55 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Mon, 03 Aug 2020 22:33:55 GMT
EXPOSE 8086
# Mon, 03 Aug 2020 22:33:55 GMT
VOLUME [/var/lib/influxdb]
# Mon, 03 Aug 2020 22:33:56 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Mon, 03 Aug 2020 22:33:56 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Mon, 03 Aug 2020 22:33:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Aug 2020 22:33:56 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321996f3080d1a7516b5914e27460b495eb04950d0190554844f395e7be9c793`  
		Last Modified: Fri, 24 Apr 2020 14:16:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9984b0a697389d40ad58252364c9cbb4e4a5258602767230a8f149134746718`  
		Last Modified: Fri, 24 Apr 2020 15:30:04 GMT  
		Size: 1.9 MB (1863602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f8eb2a5c80dfdf58578d21b9a2e6644f61c2489cbad50e1cc828d5543d857f`  
		Last Modified: Mon, 03 Aug 2020 22:35:12 GMT  
		Size: 63.9 MB (63891407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952443686cebb831b75432c39ec873100199ecd72c08d0dbee13b467747bd03f`  
		Last Modified: Mon, 03 Aug 2020 22:35:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a618c35a6a0867722c75221a4579df6d3f56c4e455d164e0ce61ef4654fe07`  
		Last Modified: Mon, 03 Aug 2020 22:35:01 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ebc15cbd03b9735f84606f64540c20e4298a06517c3140af3ecb7058335ac50`  
		Last Modified: Mon, 03 Aug 2020 22:35:01 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10-data`

```console
$ docker pull influxdb@sha256:d0fe73f58cd9eabcd2a012337800364bee134669ad0773a73d61b1b138b0ed58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-data` - linux; amd64

```console
$ docker pull influxdb@sha256:9451658cfcdbf89a2f88fd48f2f0c950de572d848a213b08f38d076e35199e9e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148376608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1c3922de522d7a0a5e29255ce6788bbcbd366e443c911c9815466052b08196`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 22 Jul 2020 02:06:48 GMT
ADD file:f98fe3d719ea765cb59da025d506d0bbd6db7a842b6b63c58c8d4d65b51bdb1f in / 
# Wed, 22 Jul 2020 02:06:48 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:11:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:11:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 23:31:14 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 22 Jul 2020 23:31:32 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Wed, 22 Jul 2020 23:31:42 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 22 Jul 2020 23:31:42 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 22 Jul 2020 23:31:43 GMT
EXPOSE 8086
# Wed, 22 Jul 2020 23:31:43 GMT
VOLUME [/var/lib/influxdb]
# Wed, 22 Jul 2020 23:31:43 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 22 Jul 2020 23:31:43 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 22 Jul 2020 23:31:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jul 2020 23:31:44 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:7e6d8ed603557d9bf077a9ace4ee506501970a4938b9a704f040ad15f22bd4e8`  
		Last Modified: Wed, 22 Jul 2020 02:12:13 GMT  
		Size: 45.4 MB (45369674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43421f771d04c7019cae6594c2b95ad92d692750fc57d201b5108c1bef2d095e`  
		Last Modified: Wed, 22 Jul 2020 03:19:27 GMT  
		Size: 10.8 MB (10750266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36327c39ae4245e3dcfa5b77a55cff18b6d81f2b4ca1b0e107da95ecd6b225f`  
		Last Modified: Wed, 22 Jul 2020 03:19:26 GMT  
		Size: 4.3 MB (4339838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a444ea13ca5c9a75f3861a3ed19ef97219c52e6a9609a61e75c76d1d9b5f675`  
		Last Modified: Wed, 22 Jul 2020 23:33:09 GMT  
		Size: 2.8 KB (2773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bde1d6da31be9fed773f48c65c3d36dc6b5db36b8f1437b3062a2600a43431d`  
		Last Modified: Wed, 22 Jul 2020 23:33:37 GMT  
		Size: 87.9 MB (87912284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f88f623bb10f0e77cf3b794f34d074b0c939bf6e29f79526c56fec8ac8a0164`  
		Last Modified: Wed, 22 Jul 2020 23:33:24 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc36540bf0ad01c3d0bad85b231b1c8cfd36ac4b5d27c20abf07aa4cddbdfb16`  
		Last Modified: Wed, 22 Jul 2020 23:33:23 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5541b1246fc19c5aa207b7ec1478386a75d162ed094ca6f095af98dd6390ca54`  
		Last Modified: Wed, 22 Jul 2020 23:33:23 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10-data-alpine`

```console
$ docker pull influxdb@sha256:6f250d7b1cc13d3b798789d480d82bdf0ffea2004e44d563619b0b397b088ec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:70a708452c2a1ff2c4fe2cad36847aa83ca1b5d9b80a5ecc16579118e9b544a3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92308348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae5cbf4e52e5b3da9fbfdee13fcd1e5806ca3f8cfad3d19ef8ae5064ef6b69f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:15:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Apr 2020 15:28:09 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 24 Apr 2020 15:28:26 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Fri, 24 Apr 2020 15:28:38 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 24 Apr 2020 15:28:38 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Fri, 24 Apr 2020 15:28:38 GMT
EXPOSE 8086
# Fri, 24 Apr 2020 15:28:39 GMT
VOLUME [/var/lib/influxdb]
# Fri, 24 Apr 2020 15:28:39 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Fri, 24 Apr 2020 15:28:39 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 24 Apr 2020 15:28:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Apr 2020 15:28:39 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321996f3080d1a7516b5914e27460b495eb04950d0190554844f395e7be9c793`  
		Last Modified: Fri, 24 Apr 2020 14:16:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9984b0a697389d40ad58252364c9cbb4e4a5258602767230a8f149134746718`  
		Last Modified: Fri, 24 Apr 2020 15:30:04 GMT  
		Size: 1.9 MB (1863602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8edd32b853201f14ebc1936e706d17eb835091b987588bea9264a45758b1b81c`  
		Last Modified: Fri, 24 Apr 2020 15:30:32 GMT  
		Size: 87.7 MB (87669411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24b53788b2bbcd58690fc7ef76c7ea9c1eceff1796a093161fe8ed3de0530cd`  
		Last Modified: Fri, 24 Apr 2020 15:30:19 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232bedee238d45217ce15f43133f9f8cebe172f996e449793704111099486c52`  
		Last Modified: Fri, 24 Apr 2020 15:30:19 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06db629dfa54d5a6727c4f73b214d90437d3640cd6bde265a8b861edc687cda`  
		Last Modified: Fri, 24 Apr 2020 15:30:19 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10-meta`

```console
$ docker pull influxdb@sha256:3087a0e54daa87b2c58d60fe8f964c1d7e3854fa7aca55743ffcb377fdb6e12c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:1b72444d1633e51c2f7ad511c5d2a91a207f93de0df8c4ee6b5bf87418ad377a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83595746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744e3ccd9f3375410212c6d84d8d5cc304d0f2cdeb659736bf052cf8ef354b58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 22 Jul 2020 02:06:48 GMT
ADD file:f98fe3d719ea765cb59da025d506d0bbd6db7a842b6b63c58c8d4d65b51bdb1f in / 
# Wed, 22 Jul 2020 02:06:48 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:11:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:11:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 23:31:14 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 22 Jul 2020 23:31:32 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Wed, 22 Jul 2020 23:31:54 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 22 Jul 2020 23:31:55 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 22 Jul 2020 23:31:55 GMT
EXPOSE 8091
# Wed, 22 Jul 2020 23:31:55 GMT
VOLUME [/var/lib/influxdb]
# Wed, 22 Jul 2020 23:31:55 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 22 Jul 2020 23:31:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jul 2020 23:31:56 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:7e6d8ed603557d9bf077a9ace4ee506501970a4938b9a704f040ad15f22bd4e8`  
		Last Modified: Wed, 22 Jul 2020 02:12:13 GMT  
		Size: 45.4 MB (45369674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43421f771d04c7019cae6594c2b95ad92d692750fc57d201b5108c1bef2d095e`  
		Last Modified: Wed, 22 Jul 2020 03:19:27 GMT  
		Size: 10.8 MB (10750266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36327c39ae4245e3dcfa5b77a55cff18b6d81f2b4ca1b0e107da95ecd6b225f`  
		Last Modified: Wed, 22 Jul 2020 03:19:26 GMT  
		Size: 4.3 MB (4339838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a444ea13ca5c9a75f3861a3ed19ef97219c52e6a9609a61e75c76d1d9b5f675`  
		Last Modified: Wed, 22 Jul 2020 23:33:09 GMT  
		Size: 2.8 KB (2773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0dd4da63cbb1484366d30c43bc98fc9541b6f0292589985a03abe12d03b8be8`  
		Last Modified: Wed, 22 Jul 2020 23:33:44 GMT  
		Size: 23.1 MB (23132624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1837b8a910bccb51cb548ae83b29e4abd402100207ee58b8348a6d267745b7a2`  
		Last Modified: Wed, 22 Jul 2020 23:33:41 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a14d6f0e8daa9638c168dd03e49978b1d24ddc72bf1dffe3ffec8e7be137899`  
		Last Modified: Wed, 22 Jul 2020 23:33:41 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10-meta-alpine`

```console
$ docker pull influxdb@sha256:a9cc22461d2f36bc3794b09dc6878f51b5d34d635475c89c9bce4b3582642642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:83006300e441c3d613b679f74ceeaf2b858635500e894bfdabb0f4165e85c8e5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 MB (27703385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d488e358e094fb5a4b10c46a25792a62288d03a3912d8321d91f20fb5d9416a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:15:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Apr 2020 15:28:09 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 24 Apr 2020 15:28:26 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Fri, 24 Apr 2020 15:28:52 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 24 Apr 2020 15:28:53 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Fri, 24 Apr 2020 15:28:53 GMT
EXPOSE 8091
# Fri, 24 Apr 2020 15:28:53 GMT
VOLUME [/var/lib/influxdb]
# Fri, 24 Apr 2020 15:28:53 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Fri, 24 Apr 2020 15:28:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Apr 2020 15:28:53 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321996f3080d1a7516b5914e27460b495eb04950d0190554844f395e7be9c793`  
		Last Modified: Fri, 24 Apr 2020 14:16:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9984b0a697389d40ad58252364c9cbb4e4a5258602767230a8f149134746718`  
		Last Modified: Fri, 24 Apr 2020 15:30:04 GMT  
		Size: 1.9 MB (1863602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ff89aa062bdb7a1a80129c8bcce60d7d6dd691a149c073e74c0876616ed43a`  
		Last Modified: Fri, 24 Apr 2020 15:30:39 GMT  
		Size: 23.1 MB (23065649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3663bb55eb8ab96716ac08e09fa1c7f6d3758caa9d115dca19be9a19c507859e`  
		Last Modified: Fri, 24 Apr 2020 15:30:36 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7a9206a9f14558d5470916b3124349a4575f6ecead7a899ca34c3fcb59ef0f`  
		Last Modified: Fri, 24 Apr 2020 15:30:36 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-alpine`

```console
$ docker pull influxdb@sha256:22222e93aa7cfeaef35d64a3b34c6c00130e62564be44d5b4af1a93bd066be95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:25b986e522bebbfaf13549edf96406da0b55af3c45f806c49813472f68579ca1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68530288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3907dabe467bcb68c89f7f56065ba5ccf90bcf3f43979819cdcddf9dd982bcd9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:15:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Apr 2020 15:28:09 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 24 Apr 2020 15:28:09 GMT
ENV INFLUXDB_VERSION=1.7.10
# Mon, 03 Aug 2020 22:33:55 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 03 Aug 2020 22:33:55 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Mon, 03 Aug 2020 22:33:55 GMT
EXPOSE 8086
# Mon, 03 Aug 2020 22:33:55 GMT
VOLUME [/var/lib/influxdb]
# Mon, 03 Aug 2020 22:33:56 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Mon, 03 Aug 2020 22:33:56 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Mon, 03 Aug 2020 22:33:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Aug 2020 22:33:56 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321996f3080d1a7516b5914e27460b495eb04950d0190554844f395e7be9c793`  
		Last Modified: Fri, 24 Apr 2020 14:16:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9984b0a697389d40ad58252364c9cbb4e4a5258602767230a8f149134746718`  
		Last Modified: Fri, 24 Apr 2020 15:30:04 GMT  
		Size: 1.9 MB (1863602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f8eb2a5c80dfdf58578d21b9a2e6644f61c2489cbad50e1cc828d5543d857f`  
		Last Modified: Mon, 03 Aug 2020 22:35:12 GMT  
		Size: 63.9 MB (63891407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952443686cebb831b75432c39ec873100199ecd72c08d0dbee13b467747bd03f`  
		Last Modified: Mon, 03 Aug 2020 22:35:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a618c35a6a0867722c75221a4579df6d3f56c4e455d164e0ce61ef4654fe07`  
		Last Modified: Mon, 03 Aug 2020 22:35:01 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ebc15cbd03b9735f84606f64540c20e4298a06517c3140af3ecb7058335ac50`  
		Last Modified: Mon, 03 Aug 2020 22:35:01 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-data`

```console
$ docker pull influxdb@sha256:d0fe73f58cd9eabcd2a012337800364bee134669ad0773a73d61b1b138b0ed58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-data` - linux; amd64

```console
$ docker pull influxdb@sha256:9451658cfcdbf89a2f88fd48f2f0c950de572d848a213b08f38d076e35199e9e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148376608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1c3922de522d7a0a5e29255ce6788bbcbd366e443c911c9815466052b08196`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 22 Jul 2020 02:06:48 GMT
ADD file:f98fe3d719ea765cb59da025d506d0bbd6db7a842b6b63c58c8d4d65b51bdb1f in / 
# Wed, 22 Jul 2020 02:06:48 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:11:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:11:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 23:31:14 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 22 Jul 2020 23:31:32 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Wed, 22 Jul 2020 23:31:42 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 22 Jul 2020 23:31:42 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 22 Jul 2020 23:31:43 GMT
EXPOSE 8086
# Wed, 22 Jul 2020 23:31:43 GMT
VOLUME [/var/lib/influxdb]
# Wed, 22 Jul 2020 23:31:43 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 22 Jul 2020 23:31:43 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 22 Jul 2020 23:31:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jul 2020 23:31:44 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:7e6d8ed603557d9bf077a9ace4ee506501970a4938b9a704f040ad15f22bd4e8`  
		Last Modified: Wed, 22 Jul 2020 02:12:13 GMT  
		Size: 45.4 MB (45369674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43421f771d04c7019cae6594c2b95ad92d692750fc57d201b5108c1bef2d095e`  
		Last Modified: Wed, 22 Jul 2020 03:19:27 GMT  
		Size: 10.8 MB (10750266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36327c39ae4245e3dcfa5b77a55cff18b6d81f2b4ca1b0e107da95ecd6b225f`  
		Last Modified: Wed, 22 Jul 2020 03:19:26 GMT  
		Size: 4.3 MB (4339838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a444ea13ca5c9a75f3861a3ed19ef97219c52e6a9609a61e75c76d1d9b5f675`  
		Last Modified: Wed, 22 Jul 2020 23:33:09 GMT  
		Size: 2.8 KB (2773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bde1d6da31be9fed773f48c65c3d36dc6b5db36b8f1437b3062a2600a43431d`  
		Last Modified: Wed, 22 Jul 2020 23:33:37 GMT  
		Size: 87.9 MB (87912284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f88f623bb10f0e77cf3b794f34d074b0c939bf6e29f79526c56fec8ac8a0164`  
		Last Modified: Wed, 22 Jul 2020 23:33:24 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc36540bf0ad01c3d0bad85b231b1c8cfd36ac4b5d27c20abf07aa4cddbdfb16`  
		Last Modified: Wed, 22 Jul 2020 23:33:23 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5541b1246fc19c5aa207b7ec1478386a75d162ed094ca6f095af98dd6390ca54`  
		Last Modified: Wed, 22 Jul 2020 23:33:23 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-data-alpine`

```console
$ docker pull influxdb@sha256:6f250d7b1cc13d3b798789d480d82bdf0ffea2004e44d563619b0b397b088ec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:70a708452c2a1ff2c4fe2cad36847aa83ca1b5d9b80a5ecc16579118e9b544a3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92308348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae5cbf4e52e5b3da9fbfdee13fcd1e5806ca3f8cfad3d19ef8ae5064ef6b69f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:15:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Apr 2020 15:28:09 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 24 Apr 2020 15:28:26 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Fri, 24 Apr 2020 15:28:38 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 24 Apr 2020 15:28:38 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Fri, 24 Apr 2020 15:28:38 GMT
EXPOSE 8086
# Fri, 24 Apr 2020 15:28:39 GMT
VOLUME [/var/lib/influxdb]
# Fri, 24 Apr 2020 15:28:39 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Fri, 24 Apr 2020 15:28:39 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 24 Apr 2020 15:28:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Apr 2020 15:28:39 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321996f3080d1a7516b5914e27460b495eb04950d0190554844f395e7be9c793`  
		Last Modified: Fri, 24 Apr 2020 14:16:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9984b0a697389d40ad58252364c9cbb4e4a5258602767230a8f149134746718`  
		Last Modified: Fri, 24 Apr 2020 15:30:04 GMT  
		Size: 1.9 MB (1863602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8edd32b853201f14ebc1936e706d17eb835091b987588bea9264a45758b1b81c`  
		Last Modified: Fri, 24 Apr 2020 15:30:32 GMT  
		Size: 87.7 MB (87669411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24b53788b2bbcd58690fc7ef76c7ea9c1eceff1796a093161fe8ed3de0530cd`  
		Last Modified: Fri, 24 Apr 2020 15:30:19 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232bedee238d45217ce15f43133f9f8cebe172f996e449793704111099486c52`  
		Last Modified: Fri, 24 Apr 2020 15:30:19 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06db629dfa54d5a6727c4f73b214d90437d3640cd6bde265a8b861edc687cda`  
		Last Modified: Fri, 24 Apr 2020 15:30:19 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-meta`

```console
$ docker pull influxdb@sha256:3087a0e54daa87b2c58d60fe8f964c1d7e3854fa7aca55743ffcb377fdb6e12c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:1b72444d1633e51c2f7ad511c5d2a91a207f93de0df8c4ee6b5bf87418ad377a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83595746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744e3ccd9f3375410212c6d84d8d5cc304d0f2cdeb659736bf052cf8ef354b58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 22 Jul 2020 02:06:48 GMT
ADD file:f98fe3d719ea765cb59da025d506d0bbd6db7a842b6b63c58c8d4d65b51bdb1f in / 
# Wed, 22 Jul 2020 02:06:48 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:11:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:11:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 23:31:14 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 22 Jul 2020 23:31:32 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Wed, 22 Jul 2020 23:31:54 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 22 Jul 2020 23:31:55 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 22 Jul 2020 23:31:55 GMT
EXPOSE 8091
# Wed, 22 Jul 2020 23:31:55 GMT
VOLUME [/var/lib/influxdb]
# Wed, 22 Jul 2020 23:31:55 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 22 Jul 2020 23:31:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jul 2020 23:31:56 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:7e6d8ed603557d9bf077a9ace4ee506501970a4938b9a704f040ad15f22bd4e8`  
		Last Modified: Wed, 22 Jul 2020 02:12:13 GMT  
		Size: 45.4 MB (45369674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43421f771d04c7019cae6594c2b95ad92d692750fc57d201b5108c1bef2d095e`  
		Last Modified: Wed, 22 Jul 2020 03:19:27 GMT  
		Size: 10.8 MB (10750266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36327c39ae4245e3dcfa5b77a55cff18b6d81f2b4ca1b0e107da95ecd6b225f`  
		Last Modified: Wed, 22 Jul 2020 03:19:26 GMT  
		Size: 4.3 MB (4339838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a444ea13ca5c9a75f3861a3ed19ef97219c52e6a9609a61e75c76d1d9b5f675`  
		Last Modified: Wed, 22 Jul 2020 23:33:09 GMT  
		Size: 2.8 KB (2773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0dd4da63cbb1484366d30c43bc98fc9541b6f0292589985a03abe12d03b8be8`  
		Last Modified: Wed, 22 Jul 2020 23:33:44 GMT  
		Size: 23.1 MB (23132624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1837b8a910bccb51cb548ae83b29e4abd402100207ee58b8348a6d267745b7a2`  
		Last Modified: Wed, 22 Jul 2020 23:33:41 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a14d6f0e8daa9638c168dd03e49978b1d24ddc72bf1dffe3ffec8e7be137899`  
		Last Modified: Wed, 22 Jul 2020 23:33:41 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-meta-alpine`

```console
$ docker pull influxdb@sha256:a9cc22461d2f36bc3794b09dc6878f51b5d34d635475c89c9bce4b3582642642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:83006300e441c3d613b679f74ceeaf2b858635500e894bfdabb0f4165e85c8e5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 MB (27703385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d488e358e094fb5a4b10c46a25792a62288d03a3912d8321d91f20fb5d9416a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:15:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Apr 2020 15:28:09 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 24 Apr 2020 15:28:26 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Fri, 24 Apr 2020 15:28:52 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 24 Apr 2020 15:28:53 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Fri, 24 Apr 2020 15:28:53 GMT
EXPOSE 8091
# Fri, 24 Apr 2020 15:28:53 GMT
VOLUME [/var/lib/influxdb]
# Fri, 24 Apr 2020 15:28:53 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Fri, 24 Apr 2020 15:28:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Apr 2020 15:28:53 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321996f3080d1a7516b5914e27460b495eb04950d0190554844f395e7be9c793`  
		Last Modified: Fri, 24 Apr 2020 14:16:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9984b0a697389d40ad58252364c9cbb4e4a5258602767230a8f149134746718`  
		Last Modified: Fri, 24 Apr 2020 15:30:04 GMT  
		Size: 1.9 MB (1863602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ff89aa062bdb7a1a80129c8bcce60d7d6dd691a149c073e74c0876616ed43a`  
		Last Modified: Fri, 24 Apr 2020 15:30:39 GMT  
		Size: 23.1 MB (23065649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3663bb55eb8ab96716ac08e09fa1c7f6d3758caa9d115dca19be9a19c507859e`  
		Last Modified: Fri, 24 Apr 2020 15:30:36 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7a9206a9f14558d5470916b3124349a4575f6ecead7a899ca34c3fcb59ef0f`  
		Last Modified: Fri, 24 Apr 2020 15:30:36 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8`

```console
$ docker pull influxdb@sha256:25b7f722797bd8c61d9f3fa10a1e3a0851360aa0724fb95dcf21688270b0e531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.8` - linux; amd64

```console
$ docker pull influxdb@sha256:823c3121f18f54687c077cfd9c63aa4223cd0bca436beab16721cf82dbbd1dde
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124470930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84fa3cbe963e03e4c682e170148b423c4f753266f40719e654ce8eb973b8489`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 22 Jul 2020 02:06:48 GMT
ADD file:f98fe3d719ea765cb59da025d506d0bbd6db7a842b6b63c58c8d4d65b51bdb1f in / 
# Wed, 22 Jul 2020 02:06:48 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:11:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:11:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 23:31:14 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 22 Jul 2020 23:32:06 GMT
ENV INFLUXDB_VERSION=1.8.1
# Wed, 22 Jul 2020 23:32:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 22 Jul 2020 23:32:14 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 22 Jul 2020 23:32:15 GMT
EXPOSE 8086
# Wed, 22 Jul 2020 23:32:15 GMT
VOLUME [/var/lib/influxdb]
# Wed, 22 Jul 2020 23:32:15 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 22 Jul 2020 23:32:16 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 22 Jul 2020 23:32:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jul 2020 23:32:16 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:7e6d8ed603557d9bf077a9ace4ee506501970a4938b9a704f040ad15f22bd4e8`  
		Last Modified: Wed, 22 Jul 2020 02:12:13 GMT  
		Size: 45.4 MB (45369674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43421f771d04c7019cae6594c2b95ad92d692750fc57d201b5108c1bef2d095e`  
		Last Modified: Wed, 22 Jul 2020 03:19:27 GMT  
		Size: 10.8 MB (10750266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36327c39ae4245e3dcfa5b77a55cff18b6d81f2b4ca1b0e107da95ecd6b225f`  
		Last Modified: Wed, 22 Jul 2020 03:19:26 GMT  
		Size: 4.3 MB (4339838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a444ea13ca5c9a75f3861a3ed19ef97219c52e6a9609a61e75c76d1d9b5f675`  
		Last Modified: Wed, 22 Jul 2020 23:33:09 GMT  
		Size: 2.8 KB (2773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a2ad8b75f837c2b5520dc74eb7bc0a72d8b8e8641719f4d91eb77acaac3cf6`  
		Last Modified: Wed, 22 Jul 2020 23:33:59 GMT  
		Size: 64.0 MB (64006662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca009f9b21e567e19bf92596628eb43f3956a2ea2b8a79f54f1304892326fb20`  
		Last Modified: Wed, 22 Jul 2020 23:33:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7af9bac28586f8319a8d3db9d18de4719b5d88da4b866f9a5ac7aa21cf9c429`  
		Last Modified: Wed, 22 Jul 2020 23:33:48 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afd90f51447a444a39a512277e1b6b98ae749a1b5793377c88500cd61651688`  
		Last Modified: Wed, 22 Jul 2020 23:33:48 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:1157bb2a790ce31f68b5deb6d44691e96136e776f0ef824a4de4dab44fca27a6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115669457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca48fe485f8800ea48b91952a2df8be1abc61036733452d23f271fb38c3e87a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 04 Aug 2020 05:01:04 GMT
ADD file:0ba6f3203fb10e66124d03088d234e92fc908c572ec7eed268e866623a383a7d in / 
# Tue, 04 Aug 2020 05:01:07 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 08:16:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 08:16:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 04:21:30 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 05 Aug 2020 04:21:56 GMT
ENV INFLUXDB_VERSION=1.8.1
# Wed, 05 Aug 2020 04:22:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 05 Aug 2020 04:22:12 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 05 Aug 2020 04:22:13 GMT
EXPOSE 8086
# Wed, 05 Aug 2020 04:22:14 GMT
VOLUME [/var/lib/influxdb]
# Wed, 05 Aug 2020 04:22:16 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 05 Aug 2020 04:22:17 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 05 Aug 2020 04:22:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Aug 2020 04:22:20 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:323178d00ec2c5eb5ffb9cb696a52eaf8683dcf2eb605c742da2953556f06e37`  
		Last Modified: Tue, 04 Aug 2020 05:08:40 GMT  
		Size: 42.1 MB (42111382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b4e15a79453f6ae10815d79c8f4590aef2f1ac2979c192ff7f1ed0fbf04e60`  
		Last Modified: Tue, 04 Aug 2020 08:30:43 GMT  
		Size: 9.4 MB (9443881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf9cb1ef704caf3af8a2ed43dc12884b4f74ac867ce95f60bd8996f51fde770`  
		Last Modified: Tue, 04 Aug 2020 08:30:41 GMT  
		Size: 3.9 MB (3918490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ad1ae0455f086a984fe5ca80430d33819b38c31587c5972ddc6aedd904cbf6`  
		Last Modified: Wed, 05 Aug 2020 04:22:33 GMT  
		Size: 2.8 KB (2806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc479edc9f408861f73f237123015da94c716f59ab416a62078fc7ab0ac3971`  
		Last Modified: Wed, 05 Aug 2020 04:23:13 GMT  
		Size: 60.2 MB (60191181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacd186a6889b8c5e41c0b0208a92d0f55f6401cb522fa7e71e55dc922b234cf`  
		Last Modified: Wed, 05 Aug 2020 04:22:56 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1fdc63038b078c5450481ae63880edfcde3b6a5ea42ca5896bc6e7e37f93e0`  
		Last Modified: Wed, 05 Aug 2020 04:22:57 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d22af3197898ed08422e5d4a2d9fa52b2e82343f2e13168a54d610e949a020`  
		Last Modified: Wed, 05 Aug 2020 04:22:57 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:292af04787cffff028d2d41e5c4ea5b227acbc62eb2bb67c9ffb673e5b177d93
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116751836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad3f87612d7990058390dc9fb5bdc782051f6753ab23be256b977b8623a1744`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 04 Aug 2020 06:59:38 GMT
ADD file:0a7a65de4c9dc6ea7f7ac97362a47b82a02a45ecab668ddc84cfd011dad26d33 in / 
# Tue, 04 Aug 2020 06:59:41 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 11:16:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 11:16:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 07:16:40 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 05 Aug 2020 07:17:08 GMT
ENV INFLUXDB_VERSION=1.8.1
# Wed, 05 Aug 2020 07:17:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 05 Aug 2020 07:17:18 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 05 Aug 2020 07:17:18 GMT
EXPOSE 8086
# Wed, 05 Aug 2020 07:17:19 GMT
VOLUME [/var/lib/influxdb]
# Wed, 05 Aug 2020 07:17:20 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 05 Aug 2020 07:17:21 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 05 Aug 2020 07:17:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Aug 2020 07:17:23 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:708f9b01fc1a5dff70f7d40443ac7dd0ee1d0ae93202b6f305f4e3627cea7d22`  
		Last Modified: Tue, 04 Aug 2020 07:06:12 GMT  
		Size: 43.2 MB (43171643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06dc3a0299d558e9f611edd56658d792af018276662c8c30d86476a05c18b00b`  
		Last Modified: Tue, 04 Aug 2020 11:26:22 GMT  
		Size: 9.7 MB (9700890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7feaa2634e51f929e9ca86765cd5579cdf0809084c80d6787166627ca2aed6d4`  
		Last Modified: Tue, 04 Aug 2020 11:26:21 GMT  
		Size: 4.1 MB (4094122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691da85e3888bd2ba9b2a633be8705530081b5fde5f1bfe36535d5a56097f227`  
		Last Modified: Wed, 05 Aug 2020 07:17:36 GMT  
		Size: 2.8 KB (2803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7bd8e8c27c2ddfda4ef8731d73cf066d46aa4ff09a84d9595e4630850d8ca6b`  
		Last Modified: Wed, 05 Aug 2020 07:18:19 GMT  
		Size: 59.8 MB (59780661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb50e8c44feda4b5bcf1773af525f934697314bcc69ba061deffe2fc21efab27`  
		Last Modified: Wed, 05 Aug 2020 07:18:04 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455d8f53b784a5b76145dd669e1620768099f571ce1a57a248eb1e076eccd9e6`  
		Last Modified: Wed, 05 Aug 2020 07:18:04 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9056c827c399a558a1a6ea15ef45a5bcee6046d6bbdb2e5538772e7e04d69126`  
		Last Modified: Wed, 05 Aug 2020 07:18:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.1`

```console
$ docker pull influxdb@sha256:25b7f722797bd8c61d9f3fa10a1e3a0851360aa0724fb95dcf21688270b0e531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.8.1` - linux; amd64

```console
$ docker pull influxdb@sha256:823c3121f18f54687c077cfd9c63aa4223cd0bca436beab16721cf82dbbd1dde
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124470930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84fa3cbe963e03e4c682e170148b423c4f753266f40719e654ce8eb973b8489`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 22 Jul 2020 02:06:48 GMT
ADD file:f98fe3d719ea765cb59da025d506d0bbd6db7a842b6b63c58c8d4d65b51bdb1f in / 
# Wed, 22 Jul 2020 02:06:48 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:11:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:11:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 23:31:14 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 22 Jul 2020 23:32:06 GMT
ENV INFLUXDB_VERSION=1.8.1
# Wed, 22 Jul 2020 23:32:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 22 Jul 2020 23:32:14 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 22 Jul 2020 23:32:15 GMT
EXPOSE 8086
# Wed, 22 Jul 2020 23:32:15 GMT
VOLUME [/var/lib/influxdb]
# Wed, 22 Jul 2020 23:32:15 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 22 Jul 2020 23:32:16 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 22 Jul 2020 23:32:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jul 2020 23:32:16 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:7e6d8ed603557d9bf077a9ace4ee506501970a4938b9a704f040ad15f22bd4e8`  
		Last Modified: Wed, 22 Jul 2020 02:12:13 GMT  
		Size: 45.4 MB (45369674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43421f771d04c7019cae6594c2b95ad92d692750fc57d201b5108c1bef2d095e`  
		Last Modified: Wed, 22 Jul 2020 03:19:27 GMT  
		Size: 10.8 MB (10750266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36327c39ae4245e3dcfa5b77a55cff18b6d81f2b4ca1b0e107da95ecd6b225f`  
		Last Modified: Wed, 22 Jul 2020 03:19:26 GMT  
		Size: 4.3 MB (4339838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a444ea13ca5c9a75f3861a3ed19ef97219c52e6a9609a61e75c76d1d9b5f675`  
		Last Modified: Wed, 22 Jul 2020 23:33:09 GMT  
		Size: 2.8 KB (2773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a2ad8b75f837c2b5520dc74eb7bc0a72d8b8e8641719f4d91eb77acaac3cf6`  
		Last Modified: Wed, 22 Jul 2020 23:33:59 GMT  
		Size: 64.0 MB (64006662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca009f9b21e567e19bf92596628eb43f3956a2ea2b8a79f54f1304892326fb20`  
		Last Modified: Wed, 22 Jul 2020 23:33:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7af9bac28586f8319a8d3db9d18de4719b5d88da4b866f9a5ac7aa21cf9c429`  
		Last Modified: Wed, 22 Jul 2020 23:33:48 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afd90f51447a444a39a512277e1b6b98ae749a1b5793377c88500cd61651688`  
		Last Modified: Wed, 22 Jul 2020 23:33:48 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8.1` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:1157bb2a790ce31f68b5deb6d44691e96136e776f0ef824a4de4dab44fca27a6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115669457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca48fe485f8800ea48b91952a2df8be1abc61036733452d23f271fb38c3e87a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 04 Aug 2020 05:01:04 GMT
ADD file:0ba6f3203fb10e66124d03088d234e92fc908c572ec7eed268e866623a383a7d in / 
# Tue, 04 Aug 2020 05:01:07 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 08:16:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 08:16:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 04:21:30 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 05 Aug 2020 04:21:56 GMT
ENV INFLUXDB_VERSION=1.8.1
# Wed, 05 Aug 2020 04:22:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 05 Aug 2020 04:22:12 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 05 Aug 2020 04:22:13 GMT
EXPOSE 8086
# Wed, 05 Aug 2020 04:22:14 GMT
VOLUME [/var/lib/influxdb]
# Wed, 05 Aug 2020 04:22:16 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 05 Aug 2020 04:22:17 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 05 Aug 2020 04:22:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Aug 2020 04:22:20 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:323178d00ec2c5eb5ffb9cb696a52eaf8683dcf2eb605c742da2953556f06e37`  
		Last Modified: Tue, 04 Aug 2020 05:08:40 GMT  
		Size: 42.1 MB (42111382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b4e15a79453f6ae10815d79c8f4590aef2f1ac2979c192ff7f1ed0fbf04e60`  
		Last Modified: Tue, 04 Aug 2020 08:30:43 GMT  
		Size: 9.4 MB (9443881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf9cb1ef704caf3af8a2ed43dc12884b4f74ac867ce95f60bd8996f51fde770`  
		Last Modified: Tue, 04 Aug 2020 08:30:41 GMT  
		Size: 3.9 MB (3918490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ad1ae0455f086a984fe5ca80430d33819b38c31587c5972ddc6aedd904cbf6`  
		Last Modified: Wed, 05 Aug 2020 04:22:33 GMT  
		Size: 2.8 KB (2806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc479edc9f408861f73f237123015da94c716f59ab416a62078fc7ab0ac3971`  
		Last Modified: Wed, 05 Aug 2020 04:23:13 GMT  
		Size: 60.2 MB (60191181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacd186a6889b8c5e41c0b0208a92d0f55f6401cb522fa7e71e55dc922b234cf`  
		Last Modified: Wed, 05 Aug 2020 04:22:56 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1fdc63038b078c5450481ae63880edfcde3b6a5ea42ca5896bc6e7e37f93e0`  
		Last Modified: Wed, 05 Aug 2020 04:22:57 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d22af3197898ed08422e5d4a2d9fa52b2e82343f2e13168a54d610e949a020`  
		Last Modified: Wed, 05 Aug 2020 04:22:57 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8.1` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:292af04787cffff028d2d41e5c4ea5b227acbc62eb2bb67c9ffb673e5b177d93
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116751836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad3f87612d7990058390dc9fb5bdc782051f6753ab23be256b977b8623a1744`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 04 Aug 2020 06:59:38 GMT
ADD file:0a7a65de4c9dc6ea7f7ac97362a47b82a02a45ecab668ddc84cfd011dad26d33 in / 
# Tue, 04 Aug 2020 06:59:41 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 11:16:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 11:16:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 07:16:40 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 05 Aug 2020 07:17:08 GMT
ENV INFLUXDB_VERSION=1.8.1
# Wed, 05 Aug 2020 07:17:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 05 Aug 2020 07:17:18 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 05 Aug 2020 07:17:18 GMT
EXPOSE 8086
# Wed, 05 Aug 2020 07:17:19 GMT
VOLUME [/var/lib/influxdb]
# Wed, 05 Aug 2020 07:17:20 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 05 Aug 2020 07:17:21 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 05 Aug 2020 07:17:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Aug 2020 07:17:23 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:708f9b01fc1a5dff70f7d40443ac7dd0ee1d0ae93202b6f305f4e3627cea7d22`  
		Last Modified: Tue, 04 Aug 2020 07:06:12 GMT  
		Size: 43.2 MB (43171643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06dc3a0299d558e9f611edd56658d792af018276662c8c30d86476a05c18b00b`  
		Last Modified: Tue, 04 Aug 2020 11:26:22 GMT  
		Size: 9.7 MB (9700890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7feaa2634e51f929e9ca86765cd5579cdf0809084c80d6787166627ca2aed6d4`  
		Last Modified: Tue, 04 Aug 2020 11:26:21 GMT  
		Size: 4.1 MB (4094122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691da85e3888bd2ba9b2a633be8705530081b5fde5f1bfe36535d5a56097f227`  
		Last Modified: Wed, 05 Aug 2020 07:17:36 GMT  
		Size: 2.8 KB (2803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7bd8e8c27c2ddfda4ef8731d73cf066d46aa4ff09a84d9595e4630850d8ca6b`  
		Last Modified: Wed, 05 Aug 2020 07:18:19 GMT  
		Size: 59.8 MB (59780661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb50e8c44feda4b5bcf1773af525f934697314bcc69ba061deffe2fc21efab27`  
		Last Modified: Wed, 05 Aug 2020 07:18:04 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455d8f53b784a5b76145dd669e1620768099f571ce1a57a248eb1e076eccd9e6`  
		Last Modified: Wed, 05 Aug 2020 07:18:04 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9056c827c399a558a1a6ea15ef45a5bcee6046d6bbdb2e5538772e7e04d69126`  
		Last Modified: Wed, 05 Aug 2020 07:18:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.1-alpine`

```console
$ docker pull influxdb@sha256:32dbb22a7a1f0d3be2a034cc7aac0bd43d68066b4375d0d2c8f745072df9f438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.1-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:39d0ca6f1278d2e38eb40f92fff6111b181dfa3d07e98181249113350e005974
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68430025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a3d14e43adecbd4ae14a5ab30bf9b0ab7edfeaa1ddb6b94224cdad972b8d98`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:15:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Apr 2020 15:28:09 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 15 Jul 2020 00:20:41 GMT
ENV INFLUXDB_VERSION=1.8.1
# Mon, 03 Aug 2020 22:34:28 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 03 Aug 2020 22:34:29 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Mon, 03 Aug 2020 22:34:29 GMT
EXPOSE 8086
# Mon, 03 Aug 2020 22:34:29 GMT
VOLUME [/var/lib/influxdb]
# Mon, 03 Aug 2020 22:34:29 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Mon, 03 Aug 2020 22:34:29 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Mon, 03 Aug 2020 22:34:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Aug 2020 22:34:30 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321996f3080d1a7516b5914e27460b495eb04950d0190554844f395e7be9c793`  
		Last Modified: Fri, 24 Apr 2020 14:16:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9984b0a697389d40ad58252364c9cbb4e4a5258602767230a8f149134746718`  
		Last Modified: Fri, 24 Apr 2020 15:30:04 GMT  
		Size: 1.9 MB (1863602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac116993ab18e3e4368870163f4aa9a16213584178dca11b2f8176feb7e0f88`  
		Last Modified: Mon, 03 Aug 2020 22:35:31 GMT  
		Size: 63.8 MB (63791146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a5fc5379a9b5202ac0c9eb6cecb4989f866ab37ed15fb0fe720dbd241d6286`  
		Last Modified: Mon, 03 Aug 2020 22:35:21 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f48eac3660df184b7a56993e71edd267a8538148b294500bcd92d8021db376`  
		Last Modified: Mon, 03 Aug 2020 22:35:21 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e23b94f7fd3e8b623c5b780e09385cd870cfb847c31db816af592e9738463e9`  
		Last Modified: Mon, 03 Aug 2020 22:35:22 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.1-data`

```console
$ docker pull influxdb@sha256:87876650ef61c12cb9fd595ece5da2d7bc2f3e91fb15aec1325d51630782be55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.1-data` - linux; amd64

```console
$ docker pull influxdb@sha256:69e0b29f1088758f24dba1b7cdbbb3863a405bf826bd87106097e9f0c7d52642
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126206997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29985b6bdcb6ad7157e1d47388dcbe6336dd518336aad056f1f803493114c9d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 22 Jul 2020 02:06:48 GMT
ADD file:f98fe3d719ea765cb59da025d506d0bbd6db7a842b6b63c58c8d4d65b51bdb1f in / 
# Wed, 22 Jul 2020 02:06:48 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:11:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:11:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 23:31:14 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 22 Jul 2020 23:32:26 GMT
ENV INFLUXDB_VERSION=1.8.1-c1.8.1
# Wed, 22 Jul 2020 23:32:35 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 22 Jul 2020 23:32:35 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 22 Jul 2020 23:32:36 GMT
EXPOSE 8086
# Wed, 22 Jul 2020 23:32:36 GMT
VOLUME [/var/lib/influxdb]
# Wed, 22 Jul 2020 23:32:36 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 22 Jul 2020 23:32:37 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 22 Jul 2020 23:32:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jul 2020 23:32:37 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:7e6d8ed603557d9bf077a9ace4ee506501970a4938b9a704f040ad15f22bd4e8`  
		Last Modified: Wed, 22 Jul 2020 02:12:13 GMT  
		Size: 45.4 MB (45369674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43421f771d04c7019cae6594c2b95ad92d692750fc57d201b5108c1bef2d095e`  
		Last Modified: Wed, 22 Jul 2020 03:19:27 GMT  
		Size: 10.8 MB (10750266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36327c39ae4245e3dcfa5b77a55cff18b6d81f2b4ca1b0e107da95ecd6b225f`  
		Last Modified: Wed, 22 Jul 2020 03:19:26 GMT  
		Size: 4.3 MB (4339838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a444ea13ca5c9a75f3861a3ed19ef97219c52e6a9609a61e75c76d1d9b5f675`  
		Last Modified: Wed, 22 Jul 2020 23:33:09 GMT  
		Size: 2.8 KB (2773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd31833684a1451a391b9784af01b46a092e7d31e837314d3891a80f133a366`  
		Last Modified: Wed, 22 Jul 2020 23:34:14 GMT  
		Size: 65.7 MB (65742671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e35a0a8bca0a8581baa01045695af0b07e22cc4445080971b22763cd8993b99`  
		Last Modified: Wed, 22 Jul 2020 23:34:04 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d726d81514b6e2ab4d3d904dff6f61118378932319154f47dc14bb0f7bb361b3`  
		Last Modified: Wed, 22 Jul 2020 23:34:04 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4463301aa241b67a61dcb23ba6a6e696767bb20ba3e5adf1f95753ac2c207a2`  
		Last Modified: Wed, 22 Jul 2020 23:34:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.1-data-alpine`

```console
$ docker pull influxdb@sha256:fc6d916dc0e8e0dc8e35dd8b569f2e672af9219fbd63c0daa34637c4cba6f4ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.1-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e42328040adac22e4e7895c654eb37235277b08ad61fa38799731cb0100ba62e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70173301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0423dd66da6accc89eb4214f453956f19c3ba6c0e44b7af1f7df3c2368bfd88b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:15:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Apr 2020 15:28:09 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 15 Jul 2020 00:21:11 GMT
ENV INFLUXDB_VERSION=1.8.1-c1.8.1
# Wed, 15 Jul 2020 00:21:18 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 15 Jul 2020 00:21:18 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 15 Jul 2020 00:21:19 GMT
EXPOSE 8086
# Wed, 15 Jul 2020 00:21:19 GMT
VOLUME [/var/lib/influxdb]
# Wed, 15 Jul 2020 00:21:19 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 15 Jul 2020 00:21:19 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 15 Jul 2020 00:21:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Jul 2020 00:21:20 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321996f3080d1a7516b5914e27460b495eb04950d0190554844f395e7be9c793`  
		Last Modified: Fri, 24 Apr 2020 14:16:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9984b0a697389d40ad58252364c9cbb4e4a5258602767230a8f149134746718`  
		Last Modified: Fri, 24 Apr 2020 15:30:04 GMT  
		Size: 1.9 MB (1863602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ff18872a887bf990e02501bbd33e315b94ae545b55f4d285bbeeb610a7ef72`  
		Last Modified: Wed, 15 Jul 2020 00:22:48 GMT  
		Size: 65.5 MB (65534361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf3a27e97265ff02cd0fccbfc01f3147517b9a3c7375960675e9bfb38c60765`  
		Last Modified: Wed, 15 Jul 2020 00:22:38 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a027b0bd7f86077fd5e75a3da497d00f3c332d33a0d33500d72111e2e31c2b9a`  
		Last Modified: Wed, 15 Jul 2020 00:22:38 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aef61dc5578ad7509620181765e9f485bc80ca56b3a7de05a9780eaabe870ef5`  
		Last Modified: Wed, 15 Jul 2020 00:22:38 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.1-meta`

```console
$ docker pull influxdb@sha256:56b6c97b7b7e7ae369fec326fcbccdcb79d1684f58c1128a9269f0071529b11e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.1-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:3b7daf523f84f3b9b7c268489e26b83b0bb1dc3e3470ca26104c21fc0568e31e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83313189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de16b4d435b8cd79d99c8ebe19bc2c8ecc29cc4aada2b986549e67398e64dc3c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 22 Jul 2020 02:06:48 GMT
ADD file:f98fe3d719ea765cb59da025d506d0bbd6db7a842b6b63c58c8d4d65b51bdb1f in / 
# Wed, 22 Jul 2020 02:06:48 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:11:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:11:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 23:31:14 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 22 Jul 2020 23:32:26 GMT
ENV INFLUXDB_VERSION=1.8.1-c1.8.1
# Wed, 22 Jul 2020 23:32:50 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 22 Jul 2020 23:32:50 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 22 Jul 2020 23:32:50 GMT
EXPOSE 8091
# Wed, 22 Jul 2020 23:32:50 GMT
VOLUME [/var/lib/influxdb]
# Wed, 22 Jul 2020 23:32:50 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 22 Jul 2020 23:32:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jul 2020 23:32:51 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:7e6d8ed603557d9bf077a9ace4ee506501970a4938b9a704f040ad15f22bd4e8`  
		Last Modified: Wed, 22 Jul 2020 02:12:13 GMT  
		Size: 45.4 MB (45369674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43421f771d04c7019cae6594c2b95ad92d692750fc57d201b5108c1bef2d095e`  
		Last Modified: Wed, 22 Jul 2020 03:19:27 GMT  
		Size: 10.8 MB (10750266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36327c39ae4245e3dcfa5b77a55cff18b6d81f2b4ca1b0e107da95ecd6b225f`  
		Last Modified: Wed, 22 Jul 2020 03:19:26 GMT  
		Size: 4.3 MB (4339838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a444ea13ca5c9a75f3861a3ed19ef97219c52e6a9609a61e75c76d1d9b5f675`  
		Last Modified: Wed, 22 Jul 2020 23:33:09 GMT  
		Size: 2.8 KB (2773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde41dcf0953b874343229adfeba55b703ec06e5c2c112288d37bd91ad3f8482`  
		Last Modified: Wed, 22 Jul 2020 23:34:23 GMT  
		Size: 22.9 MB (22850067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3355947ab4213205e7afd41a64fbbc384bca75d5911f38a35cf4164bf9b517b3`  
		Last Modified: Wed, 22 Jul 2020 23:34:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fce8214204a0ac00ca7d5af4a03f8f3e60bc341b44cfb83a8ac4b59c1623a7b`  
		Last Modified: Wed, 22 Jul 2020 23:34:20 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.1-meta-alpine`

```console
$ docker pull influxdb@sha256:0a813f65fb1796551a2257c939249c7f96982aab9e6f9c2eb1d9921076dacb65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.1-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:77cc1bfc119bf95903193bfad60caf3f4794d430cce0fa72c64fee94c3596330
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27414327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a72d95c5c9755d533cce3e75c96e7d39c8ffabba678cbff2aee013a874b1fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:15:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Apr 2020 15:28:09 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 15 Jul 2020 00:21:11 GMT
ENV INFLUXDB_VERSION=1.8.1-c1.8.1
# Wed, 15 Jul 2020 00:21:35 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 15 Jul 2020 00:21:36 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 15 Jul 2020 00:21:36 GMT
EXPOSE 8091
# Wed, 15 Jul 2020 00:21:36 GMT
VOLUME [/var/lib/influxdb]
# Wed, 15 Jul 2020 00:21:36 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 15 Jul 2020 00:21:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Jul 2020 00:21:37 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321996f3080d1a7516b5914e27460b495eb04950d0190554844f395e7be9c793`  
		Last Modified: Fri, 24 Apr 2020 14:16:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9984b0a697389d40ad58252364c9cbb4e4a5258602767230a8f149134746718`  
		Last Modified: Fri, 24 Apr 2020 15:30:04 GMT  
		Size: 1.9 MB (1863602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c12adea02bd50fa5aa1d04ea28e0994f0f789be746b3904caf21a329098c0ab`  
		Last Modified: Wed, 15 Jul 2020 00:23:10 GMT  
		Size: 22.8 MB (22776590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c28078b0904b5df388e2cf2bd487bf90616eea5ed1978a24a13efd120b549f`  
		Last Modified: Wed, 15 Jul 2020 00:23:03 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ecbc2075fb01004f36eda9fab53dd86582c46ee3b552ad2a9269f1f5831f58`  
		Last Modified: Wed, 15 Jul 2020 00:23:06 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-alpine`

```console
$ docker pull influxdb@sha256:32dbb22a7a1f0d3be2a034cc7aac0bd43d68066b4375d0d2c8f745072df9f438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:39d0ca6f1278d2e38eb40f92fff6111b181dfa3d07e98181249113350e005974
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68430025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a3d14e43adecbd4ae14a5ab30bf9b0ab7edfeaa1ddb6b94224cdad972b8d98`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:15:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Apr 2020 15:28:09 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 15 Jul 2020 00:20:41 GMT
ENV INFLUXDB_VERSION=1.8.1
# Mon, 03 Aug 2020 22:34:28 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 03 Aug 2020 22:34:29 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Mon, 03 Aug 2020 22:34:29 GMT
EXPOSE 8086
# Mon, 03 Aug 2020 22:34:29 GMT
VOLUME [/var/lib/influxdb]
# Mon, 03 Aug 2020 22:34:29 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Mon, 03 Aug 2020 22:34:29 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Mon, 03 Aug 2020 22:34:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Aug 2020 22:34:30 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321996f3080d1a7516b5914e27460b495eb04950d0190554844f395e7be9c793`  
		Last Modified: Fri, 24 Apr 2020 14:16:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9984b0a697389d40ad58252364c9cbb4e4a5258602767230a8f149134746718`  
		Last Modified: Fri, 24 Apr 2020 15:30:04 GMT  
		Size: 1.9 MB (1863602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac116993ab18e3e4368870163f4aa9a16213584178dca11b2f8176feb7e0f88`  
		Last Modified: Mon, 03 Aug 2020 22:35:31 GMT  
		Size: 63.8 MB (63791146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a5fc5379a9b5202ac0c9eb6cecb4989f866ab37ed15fb0fe720dbd241d6286`  
		Last Modified: Mon, 03 Aug 2020 22:35:21 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f48eac3660df184b7a56993e71edd267a8538148b294500bcd92d8021db376`  
		Last Modified: Mon, 03 Aug 2020 22:35:21 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e23b94f7fd3e8b623c5b780e09385cd870cfb847c31db816af592e9738463e9`  
		Last Modified: Mon, 03 Aug 2020 22:35:22 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-data`

```console
$ docker pull influxdb@sha256:87876650ef61c12cb9fd595ece5da2d7bc2f3e91fb15aec1325d51630782be55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-data` - linux; amd64

```console
$ docker pull influxdb@sha256:69e0b29f1088758f24dba1b7cdbbb3863a405bf826bd87106097e9f0c7d52642
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126206997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29985b6bdcb6ad7157e1d47388dcbe6336dd518336aad056f1f803493114c9d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 22 Jul 2020 02:06:48 GMT
ADD file:f98fe3d719ea765cb59da025d506d0bbd6db7a842b6b63c58c8d4d65b51bdb1f in / 
# Wed, 22 Jul 2020 02:06:48 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:11:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:11:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 23:31:14 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 22 Jul 2020 23:32:26 GMT
ENV INFLUXDB_VERSION=1.8.1-c1.8.1
# Wed, 22 Jul 2020 23:32:35 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 22 Jul 2020 23:32:35 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 22 Jul 2020 23:32:36 GMT
EXPOSE 8086
# Wed, 22 Jul 2020 23:32:36 GMT
VOLUME [/var/lib/influxdb]
# Wed, 22 Jul 2020 23:32:36 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 22 Jul 2020 23:32:37 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 22 Jul 2020 23:32:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jul 2020 23:32:37 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:7e6d8ed603557d9bf077a9ace4ee506501970a4938b9a704f040ad15f22bd4e8`  
		Last Modified: Wed, 22 Jul 2020 02:12:13 GMT  
		Size: 45.4 MB (45369674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43421f771d04c7019cae6594c2b95ad92d692750fc57d201b5108c1bef2d095e`  
		Last Modified: Wed, 22 Jul 2020 03:19:27 GMT  
		Size: 10.8 MB (10750266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36327c39ae4245e3dcfa5b77a55cff18b6d81f2b4ca1b0e107da95ecd6b225f`  
		Last Modified: Wed, 22 Jul 2020 03:19:26 GMT  
		Size: 4.3 MB (4339838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a444ea13ca5c9a75f3861a3ed19ef97219c52e6a9609a61e75c76d1d9b5f675`  
		Last Modified: Wed, 22 Jul 2020 23:33:09 GMT  
		Size: 2.8 KB (2773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd31833684a1451a391b9784af01b46a092e7d31e837314d3891a80f133a366`  
		Last Modified: Wed, 22 Jul 2020 23:34:14 GMT  
		Size: 65.7 MB (65742671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e35a0a8bca0a8581baa01045695af0b07e22cc4445080971b22763cd8993b99`  
		Last Modified: Wed, 22 Jul 2020 23:34:04 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d726d81514b6e2ab4d3d904dff6f61118378932319154f47dc14bb0f7bb361b3`  
		Last Modified: Wed, 22 Jul 2020 23:34:04 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4463301aa241b67a61dcb23ba6a6e696767bb20ba3e5adf1f95753ac2c207a2`  
		Last Modified: Wed, 22 Jul 2020 23:34:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-data-alpine`

```console
$ docker pull influxdb@sha256:fc6d916dc0e8e0dc8e35dd8b569f2e672af9219fbd63c0daa34637c4cba6f4ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e42328040adac22e4e7895c654eb37235277b08ad61fa38799731cb0100ba62e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70173301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0423dd66da6accc89eb4214f453956f19c3ba6c0e44b7af1f7df3c2368bfd88b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:15:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Apr 2020 15:28:09 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 15 Jul 2020 00:21:11 GMT
ENV INFLUXDB_VERSION=1.8.1-c1.8.1
# Wed, 15 Jul 2020 00:21:18 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 15 Jul 2020 00:21:18 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 15 Jul 2020 00:21:19 GMT
EXPOSE 8086
# Wed, 15 Jul 2020 00:21:19 GMT
VOLUME [/var/lib/influxdb]
# Wed, 15 Jul 2020 00:21:19 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 15 Jul 2020 00:21:19 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 15 Jul 2020 00:21:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Jul 2020 00:21:20 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321996f3080d1a7516b5914e27460b495eb04950d0190554844f395e7be9c793`  
		Last Modified: Fri, 24 Apr 2020 14:16:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9984b0a697389d40ad58252364c9cbb4e4a5258602767230a8f149134746718`  
		Last Modified: Fri, 24 Apr 2020 15:30:04 GMT  
		Size: 1.9 MB (1863602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ff18872a887bf990e02501bbd33e315b94ae545b55f4d285bbeeb610a7ef72`  
		Last Modified: Wed, 15 Jul 2020 00:22:48 GMT  
		Size: 65.5 MB (65534361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf3a27e97265ff02cd0fccbfc01f3147517b9a3c7375960675e9bfb38c60765`  
		Last Modified: Wed, 15 Jul 2020 00:22:38 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a027b0bd7f86077fd5e75a3da497d00f3c332d33a0d33500d72111e2e31c2b9a`  
		Last Modified: Wed, 15 Jul 2020 00:22:38 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aef61dc5578ad7509620181765e9f485bc80ca56b3a7de05a9780eaabe870ef5`  
		Last Modified: Wed, 15 Jul 2020 00:22:38 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-meta`

```console
$ docker pull influxdb@sha256:56b6c97b7b7e7ae369fec326fcbccdcb79d1684f58c1128a9269f0071529b11e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:3b7daf523f84f3b9b7c268489e26b83b0bb1dc3e3470ca26104c21fc0568e31e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83313189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de16b4d435b8cd79d99c8ebe19bc2c8ecc29cc4aada2b986549e67398e64dc3c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 22 Jul 2020 02:06:48 GMT
ADD file:f98fe3d719ea765cb59da025d506d0bbd6db7a842b6b63c58c8d4d65b51bdb1f in / 
# Wed, 22 Jul 2020 02:06:48 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:11:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:11:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 23:31:14 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 22 Jul 2020 23:32:26 GMT
ENV INFLUXDB_VERSION=1.8.1-c1.8.1
# Wed, 22 Jul 2020 23:32:50 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 22 Jul 2020 23:32:50 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 22 Jul 2020 23:32:50 GMT
EXPOSE 8091
# Wed, 22 Jul 2020 23:32:50 GMT
VOLUME [/var/lib/influxdb]
# Wed, 22 Jul 2020 23:32:50 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 22 Jul 2020 23:32:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jul 2020 23:32:51 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:7e6d8ed603557d9bf077a9ace4ee506501970a4938b9a704f040ad15f22bd4e8`  
		Last Modified: Wed, 22 Jul 2020 02:12:13 GMT  
		Size: 45.4 MB (45369674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43421f771d04c7019cae6594c2b95ad92d692750fc57d201b5108c1bef2d095e`  
		Last Modified: Wed, 22 Jul 2020 03:19:27 GMT  
		Size: 10.8 MB (10750266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36327c39ae4245e3dcfa5b77a55cff18b6d81f2b4ca1b0e107da95ecd6b225f`  
		Last Modified: Wed, 22 Jul 2020 03:19:26 GMT  
		Size: 4.3 MB (4339838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a444ea13ca5c9a75f3861a3ed19ef97219c52e6a9609a61e75c76d1d9b5f675`  
		Last Modified: Wed, 22 Jul 2020 23:33:09 GMT  
		Size: 2.8 KB (2773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde41dcf0953b874343229adfeba55b703ec06e5c2c112288d37bd91ad3f8482`  
		Last Modified: Wed, 22 Jul 2020 23:34:23 GMT  
		Size: 22.9 MB (22850067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3355947ab4213205e7afd41a64fbbc384bca75d5911f38a35cf4164bf9b517b3`  
		Last Modified: Wed, 22 Jul 2020 23:34:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fce8214204a0ac00ca7d5af4a03f8f3e60bc341b44cfb83a8ac4b59c1623a7b`  
		Last Modified: Wed, 22 Jul 2020 23:34:20 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-meta-alpine`

```console
$ docker pull influxdb@sha256:0a813f65fb1796551a2257c939249c7f96982aab9e6f9c2eb1d9921076dacb65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:77cc1bfc119bf95903193bfad60caf3f4794d430cce0fa72c64fee94c3596330
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27414327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a72d95c5c9755d533cce3e75c96e7d39c8ffabba678cbff2aee013a874b1fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:15:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Apr 2020 15:28:09 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 15 Jul 2020 00:21:11 GMT
ENV INFLUXDB_VERSION=1.8.1-c1.8.1
# Wed, 15 Jul 2020 00:21:35 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 15 Jul 2020 00:21:36 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 15 Jul 2020 00:21:36 GMT
EXPOSE 8091
# Wed, 15 Jul 2020 00:21:36 GMT
VOLUME [/var/lib/influxdb]
# Wed, 15 Jul 2020 00:21:36 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 15 Jul 2020 00:21:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Jul 2020 00:21:37 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321996f3080d1a7516b5914e27460b495eb04950d0190554844f395e7be9c793`  
		Last Modified: Fri, 24 Apr 2020 14:16:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9984b0a697389d40ad58252364c9cbb4e4a5258602767230a8f149134746718`  
		Last Modified: Fri, 24 Apr 2020 15:30:04 GMT  
		Size: 1.9 MB (1863602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c12adea02bd50fa5aa1d04ea28e0994f0f789be746b3904caf21a329098c0ab`  
		Last Modified: Wed, 15 Jul 2020 00:23:10 GMT  
		Size: 22.8 MB (22776590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c28078b0904b5df388e2cf2bd487bf90616eea5ed1978a24a13efd120b549f`  
		Last Modified: Wed, 15 Jul 2020 00:23:03 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ecbc2075fb01004f36eda9fab53dd86582c46ee3b552ad2a9269f1f5831f58`  
		Last Modified: Wed, 15 Jul 2020 00:23:06 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:32dbb22a7a1f0d3be2a034cc7aac0bd43d68066b4375d0d2c8f745072df9f438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:39d0ca6f1278d2e38eb40f92fff6111b181dfa3d07e98181249113350e005974
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68430025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a3d14e43adecbd4ae14a5ab30bf9b0ab7edfeaa1ddb6b94224cdad972b8d98`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:15:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Apr 2020 15:28:09 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 15 Jul 2020 00:20:41 GMT
ENV INFLUXDB_VERSION=1.8.1
# Mon, 03 Aug 2020 22:34:28 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 03 Aug 2020 22:34:29 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Mon, 03 Aug 2020 22:34:29 GMT
EXPOSE 8086
# Mon, 03 Aug 2020 22:34:29 GMT
VOLUME [/var/lib/influxdb]
# Mon, 03 Aug 2020 22:34:29 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Mon, 03 Aug 2020 22:34:29 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Mon, 03 Aug 2020 22:34:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Aug 2020 22:34:30 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321996f3080d1a7516b5914e27460b495eb04950d0190554844f395e7be9c793`  
		Last Modified: Fri, 24 Apr 2020 14:16:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9984b0a697389d40ad58252364c9cbb4e4a5258602767230a8f149134746718`  
		Last Modified: Fri, 24 Apr 2020 15:30:04 GMT  
		Size: 1.9 MB (1863602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac116993ab18e3e4368870163f4aa9a16213584178dca11b2f8176feb7e0f88`  
		Last Modified: Mon, 03 Aug 2020 22:35:31 GMT  
		Size: 63.8 MB (63791146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a5fc5379a9b5202ac0c9eb6cecb4989f866ab37ed15fb0fe720dbd241d6286`  
		Last Modified: Mon, 03 Aug 2020 22:35:21 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f48eac3660df184b7a56993e71edd267a8538148b294500bcd92d8021db376`  
		Last Modified: Mon, 03 Aug 2020 22:35:21 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e23b94f7fd3e8b623c5b780e09385cd870cfb847c31db816af592e9738463e9`  
		Last Modified: Mon, 03 Aug 2020 22:35:22 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:data`

```console
$ docker pull influxdb@sha256:87876650ef61c12cb9fd595ece5da2d7bc2f3e91fb15aec1325d51630782be55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:69e0b29f1088758f24dba1b7cdbbb3863a405bf826bd87106097e9f0c7d52642
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126206997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29985b6bdcb6ad7157e1d47388dcbe6336dd518336aad056f1f803493114c9d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 22 Jul 2020 02:06:48 GMT
ADD file:f98fe3d719ea765cb59da025d506d0bbd6db7a842b6b63c58c8d4d65b51bdb1f in / 
# Wed, 22 Jul 2020 02:06:48 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:11:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:11:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 23:31:14 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 22 Jul 2020 23:32:26 GMT
ENV INFLUXDB_VERSION=1.8.1-c1.8.1
# Wed, 22 Jul 2020 23:32:35 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 22 Jul 2020 23:32:35 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 22 Jul 2020 23:32:36 GMT
EXPOSE 8086
# Wed, 22 Jul 2020 23:32:36 GMT
VOLUME [/var/lib/influxdb]
# Wed, 22 Jul 2020 23:32:36 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 22 Jul 2020 23:32:37 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 22 Jul 2020 23:32:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jul 2020 23:32:37 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:7e6d8ed603557d9bf077a9ace4ee506501970a4938b9a704f040ad15f22bd4e8`  
		Last Modified: Wed, 22 Jul 2020 02:12:13 GMT  
		Size: 45.4 MB (45369674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43421f771d04c7019cae6594c2b95ad92d692750fc57d201b5108c1bef2d095e`  
		Last Modified: Wed, 22 Jul 2020 03:19:27 GMT  
		Size: 10.8 MB (10750266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36327c39ae4245e3dcfa5b77a55cff18b6d81f2b4ca1b0e107da95ecd6b225f`  
		Last Modified: Wed, 22 Jul 2020 03:19:26 GMT  
		Size: 4.3 MB (4339838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a444ea13ca5c9a75f3861a3ed19ef97219c52e6a9609a61e75c76d1d9b5f675`  
		Last Modified: Wed, 22 Jul 2020 23:33:09 GMT  
		Size: 2.8 KB (2773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd31833684a1451a391b9784af01b46a092e7d31e837314d3891a80f133a366`  
		Last Modified: Wed, 22 Jul 2020 23:34:14 GMT  
		Size: 65.7 MB (65742671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e35a0a8bca0a8581baa01045695af0b07e22cc4445080971b22763cd8993b99`  
		Last Modified: Wed, 22 Jul 2020 23:34:04 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d726d81514b6e2ab4d3d904dff6f61118378932319154f47dc14bb0f7bb361b3`  
		Last Modified: Wed, 22 Jul 2020 23:34:04 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4463301aa241b67a61dcb23ba6a6e696767bb20ba3e5adf1f95753ac2c207a2`  
		Last Modified: Wed, 22 Jul 2020 23:34:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:data-alpine`

```console
$ docker pull influxdb@sha256:fc6d916dc0e8e0dc8e35dd8b569f2e672af9219fbd63c0daa34637c4cba6f4ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e42328040adac22e4e7895c654eb37235277b08ad61fa38799731cb0100ba62e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70173301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0423dd66da6accc89eb4214f453956f19c3ba6c0e44b7af1f7df3c2368bfd88b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:15:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Apr 2020 15:28:09 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 15 Jul 2020 00:21:11 GMT
ENV INFLUXDB_VERSION=1.8.1-c1.8.1
# Wed, 15 Jul 2020 00:21:18 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 15 Jul 2020 00:21:18 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 15 Jul 2020 00:21:19 GMT
EXPOSE 8086
# Wed, 15 Jul 2020 00:21:19 GMT
VOLUME [/var/lib/influxdb]
# Wed, 15 Jul 2020 00:21:19 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 15 Jul 2020 00:21:19 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 15 Jul 2020 00:21:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Jul 2020 00:21:20 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321996f3080d1a7516b5914e27460b495eb04950d0190554844f395e7be9c793`  
		Last Modified: Fri, 24 Apr 2020 14:16:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9984b0a697389d40ad58252364c9cbb4e4a5258602767230a8f149134746718`  
		Last Modified: Fri, 24 Apr 2020 15:30:04 GMT  
		Size: 1.9 MB (1863602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ff18872a887bf990e02501bbd33e315b94ae545b55f4d285bbeeb610a7ef72`  
		Last Modified: Wed, 15 Jul 2020 00:22:48 GMT  
		Size: 65.5 MB (65534361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf3a27e97265ff02cd0fccbfc01f3147517b9a3c7375960675e9bfb38c60765`  
		Last Modified: Wed, 15 Jul 2020 00:22:38 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a027b0bd7f86077fd5e75a3da497d00f3c332d33a0d33500d72111e2e31c2b9a`  
		Last Modified: Wed, 15 Jul 2020 00:22:38 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aef61dc5578ad7509620181765e9f485bc80ca56b3a7de05a9780eaabe870ef5`  
		Last Modified: Wed, 15 Jul 2020 00:22:38 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:25b7f722797bd8c61d9f3fa10a1e3a0851360aa0724fb95dcf21688270b0e531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:823c3121f18f54687c077cfd9c63aa4223cd0bca436beab16721cf82dbbd1dde
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124470930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84fa3cbe963e03e4c682e170148b423c4f753266f40719e654ce8eb973b8489`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 22 Jul 2020 02:06:48 GMT
ADD file:f98fe3d719ea765cb59da025d506d0bbd6db7a842b6b63c58c8d4d65b51bdb1f in / 
# Wed, 22 Jul 2020 02:06:48 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:11:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:11:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 23:31:14 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 22 Jul 2020 23:32:06 GMT
ENV INFLUXDB_VERSION=1.8.1
# Wed, 22 Jul 2020 23:32:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 22 Jul 2020 23:32:14 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 22 Jul 2020 23:32:15 GMT
EXPOSE 8086
# Wed, 22 Jul 2020 23:32:15 GMT
VOLUME [/var/lib/influxdb]
# Wed, 22 Jul 2020 23:32:15 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 22 Jul 2020 23:32:16 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 22 Jul 2020 23:32:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jul 2020 23:32:16 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:7e6d8ed603557d9bf077a9ace4ee506501970a4938b9a704f040ad15f22bd4e8`  
		Last Modified: Wed, 22 Jul 2020 02:12:13 GMT  
		Size: 45.4 MB (45369674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43421f771d04c7019cae6594c2b95ad92d692750fc57d201b5108c1bef2d095e`  
		Last Modified: Wed, 22 Jul 2020 03:19:27 GMT  
		Size: 10.8 MB (10750266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36327c39ae4245e3dcfa5b77a55cff18b6d81f2b4ca1b0e107da95ecd6b225f`  
		Last Modified: Wed, 22 Jul 2020 03:19:26 GMT  
		Size: 4.3 MB (4339838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a444ea13ca5c9a75f3861a3ed19ef97219c52e6a9609a61e75c76d1d9b5f675`  
		Last Modified: Wed, 22 Jul 2020 23:33:09 GMT  
		Size: 2.8 KB (2773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a2ad8b75f837c2b5520dc74eb7bc0a72d8b8e8641719f4d91eb77acaac3cf6`  
		Last Modified: Wed, 22 Jul 2020 23:33:59 GMT  
		Size: 64.0 MB (64006662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca009f9b21e567e19bf92596628eb43f3956a2ea2b8a79f54f1304892326fb20`  
		Last Modified: Wed, 22 Jul 2020 23:33:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7af9bac28586f8319a8d3db9d18de4719b5d88da4b866f9a5ac7aa21cf9c429`  
		Last Modified: Wed, 22 Jul 2020 23:33:48 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afd90f51447a444a39a512277e1b6b98ae749a1b5793377c88500cd61651688`  
		Last Modified: Wed, 22 Jul 2020 23:33:48 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:latest` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:1157bb2a790ce31f68b5deb6d44691e96136e776f0ef824a4de4dab44fca27a6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115669457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca48fe485f8800ea48b91952a2df8be1abc61036733452d23f271fb38c3e87a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 04 Aug 2020 05:01:04 GMT
ADD file:0ba6f3203fb10e66124d03088d234e92fc908c572ec7eed268e866623a383a7d in / 
# Tue, 04 Aug 2020 05:01:07 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 08:16:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 08:16:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 04:21:30 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 05 Aug 2020 04:21:56 GMT
ENV INFLUXDB_VERSION=1.8.1
# Wed, 05 Aug 2020 04:22:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 05 Aug 2020 04:22:12 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 05 Aug 2020 04:22:13 GMT
EXPOSE 8086
# Wed, 05 Aug 2020 04:22:14 GMT
VOLUME [/var/lib/influxdb]
# Wed, 05 Aug 2020 04:22:16 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 05 Aug 2020 04:22:17 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 05 Aug 2020 04:22:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Aug 2020 04:22:20 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:323178d00ec2c5eb5ffb9cb696a52eaf8683dcf2eb605c742da2953556f06e37`  
		Last Modified: Tue, 04 Aug 2020 05:08:40 GMT  
		Size: 42.1 MB (42111382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b4e15a79453f6ae10815d79c8f4590aef2f1ac2979c192ff7f1ed0fbf04e60`  
		Last Modified: Tue, 04 Aug 2020 08:30:43 GMT  
		Size: 9.4 MB (9443881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf9cb1ef704caf3af8a2ed43dc12884b4f74ac867ce95f60bd8996f51fde770`  
		Last Modified: Tue, 04 Aug 2020 08:30:41 GMT  
		Size: 3.9 MB (3918490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ad1ae0455f086a984fe5ca80430d33819b38c31587c5972ddc6aedd904cbf6`  
		Last Modified: Wed, 05 Aug 2020 04:22:33 GMT  
		Size: 2.8 KB (2806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc479edc9f408861f73f237123015da94c716f59ab416a62078fc7ab0ac3971`  
		Last Modified: Wed, 05 Aug 2020 04:23:13 GMT  
		Size: 60.2 MB (60191181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacd186a6889b8c5e41c0b0208a92d0f55f6401cb522fa7e71e55dc922b234cf`  
		Last Modified: Wed, 05 Aug 2020 04:22:56 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1fdc63038b078c5450481ae63880edfcde3b6a5ea42ca5896bc6e7e37f93e0`  
		Last Modified: Wed, 05 Aug 2020 04:22:57 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d22af3197898ed08422e5d4a2d9fa52b2e82343f2e13168a54d610e949a020`  
		Last Modified: Wed, 05 Aug 2020 04:22:57 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:292af04787cffff028d2d41e5c4ea5b227acbc62eb2bb67c9ffb673e5b177d93
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116751836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad3f87612d7990058390dc9fb5bdc782051f6753ab23be256b977b8623a1744`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 04 Aug 2020 06:59:38 GMT
ADD file:0a7a65de4c9dc6ea7f7ac97362a47b82a02a45ecab668ddc84cfd011dad26d33 in / 
# Tue, 04 Aug 2020 06:59:41 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 11:16:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 11:16:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 07:16:40 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 05 Aug 2020 07:17:08 GMT
ENV INFLUXDB_VERSION=1.8.1
# Wed, 05 Aug 2020 07:17:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 05 Aug 2020 07:17:18 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 05 Aug 2020 07:17:18 GMT
EXPOSE 8086
# Wed, 05 Aug 2020 07:17:19 GMT
VOLUME [/var/lib/influxdb]
# Wed, 05 Aug 2020 07:17:20 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 05 Aug 2020 07:17:21 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 05 Aug 2020 07:17:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Aug 2020 07:17:23 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:708f9b01fc1a5dff70f7d40443ac7dd0ee1d0ae93202b6f305f4e3627cea7d22`  
		Last Modified: Tue, 04 Aug 2020 07:06:12 GMT  
		Size: 43.2 MB (43171643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06dc3a0299d558e9f611edd56658d792af018276662c8c30d86476a05c18b00b`  
		Last Modified: Tue, 04 Aug 2020 11:26:22 GMT  
		Size: 9.7 MB (9700890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7feaa2634e51f929e9ca86765cd5579cdf0809084c80d6787166627ca2aed6d4`  
		Last Modified: Tue, 04 Aug 2020 11:26:21 GMT  
		Size: 4.1 MB (4094122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691da85e3888bd2ba9b2a633be8705530081b5fde5f1bfe36535d5a56097f227`  
		Last Modified: Wed, 05 Aug 2020 07:17:36 GMT  
		Size: 2.8 KB (2803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7bd8e8c27c2ddfda4ef8731d73cf066d46aa4ff09a84d9595e4630850d8ca6b`  
		Last Modified: Wed, 05 Aug 2020 07:18:19 GMT  
		Size: 59.8 MB (59780661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb50e8c44feda4b5bcf1773af525f934697314bcc69ba061deffe2fc21efab27`  
		Last Modified: Wed, 05 Aug 2020 07:18:04 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455d8f53b784a5b76145dd669e1620768099f571ce1a57a248eb1e076eccd9e6`  
		Last Modified: Wed, 05 Aug 2020 07:18:04 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9056c827c399a558a1a6ea15ef45a5bcee6046d6bbdb2e5538772e7e04d69126`  
		Last Modified: Wed, 05 Aug 2020 07:18:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:meta`

```console
$ docker pull influxdb@sha256:56b6c97b7b7e7ae369fec326fcbccdcb79d1684f58c1128a9269f0071529b11e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:meta` - linux; amd64

```console
$ docker pull influxdb@sha256:3b7daf523f84f3b9b7c268489e26b83b0bb1dc3e3470ca26104c21fc0568e31e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83313189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de16b4d435b8cd79d99c8ebe19bc2c8ecc29cc4aada2b986549e67398e64dc3c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 22 Jul 2020 02:06:48 GMT
ADD file:f98fe3d719ea765cb59da025d506d0bbd6db7a842b6b63c58c8d4d65b51bdb1f in / 
# Wed, 22 Jul 2020 02:06:48 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:11:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:11:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 23:31:14 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 22 Jul 2020 23:32:26 GMT
ENV INFLUXDB_VERSION=1.8.1-c1.8.1
# Wed, 22 Jul 2020 23:32:50 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 22 Jul 2020 23:32:50 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 22 Jul 2020 23:32:50 GMT
EXPOSE 8091
# Wed, 22 Jul 2020 23:32:50 GMT
VOLUME [/var/lib/influxdb]
# Wed, 22 Jul 2020 23:32:50 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 22 Jul 2020 23:32:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jul 2020 23:32:51 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:7e6d8ed603557d9bf077a9ace4ee506501970a4938b9a704f040ad15f22bd4e8`  
		Last Modified: Wed, 22 Jul 2020 02:12:13 GMT  
		Size: 45.4 MB (45369674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43421f771d04c7019cae6594c2b95ad92d692750fc57d201b5108c1bef2d095e`  
		Last Modified: Wed, 22 Jul 2020 03:19:27 GMT  
		Size: 10.8 MB (10750266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36327c39ae4245e3dcfa5b77a55cff18b6d81f2b4ca1b0e107da95ecd6b225f`  
		Last Modified: Wed, 22 Jul 2020 03:19:26 GMT  
		Size: 4.3 MB (4339838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a444ea13ca5c9a75f3861a3ed19ef97219c52e6a9609a61e75c76d1d9b5f675`  
		Last Modified: Wed, 22 Jul 2020 23:33:09 GMT  
		Size: 2.8 KB (2773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde41dcf0953b874343229adfeba55b703ec06e5c2c112288d37bd91ad3f8482`  
		Last Modified: Wed, 22 Jul 2020 23:34:23 GMT  
		Size: 22.9 MB (22850067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3355947ab4213205e7afd41a64fbbc384bca75d5911f38a35cf4164bf9b517b3`  
		Last Modified: Wed, 22 Jul 2020 23:34:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fce8214204a0ac00ca7d5af4a03f8f3e60bc341b44cfb83a8ac4b59c1623a7b`  
		Last Modified: Wed, 22 Jul 2020 23:34:20 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:meta-alpine`

```console
$ docker pull influxdb@sha256:0a813f65fb1796551a2257c939249c7f96982aab9e6f9c2eb1d9921076dacb65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:77cc1bfc119bf95903193bfad60caf3f4794d430cce0fa72c64fee94c3596330
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27414327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a72d95c5c9755d533cce3e75c96e7d39c8ffabba678cbff2aee013a874b1fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:15:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Apr 2020 15:28:09 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 15 Jul 2020 00:21:11 GMT
ENV INFLUXDB_VERSION=1.8.1-c1.8.1
# Wed, 15 Jul 2020 00:21:35 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 15 Jul 2020 00:21:36 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 15 Jul 2020 00:21:36 GMT
EXPOSE 8091
# Wed, 15 Jul 2020 00:21:36 GMT
VOLUME [/var/lib/influxdb]
# Wed, 15 Jul 2020 00:21:36 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 15 Jul 2020 00:21:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Jul 2020 00:21:37 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321996f3080d1a7516b5914e27460b495eb04950d0190554844f395e7be9c793`  
		Last Modified: Fri, 24 Apr 2020 14:16:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9984b0a697389d40ad58252364c9cbb4e4a5258602767230a8f149134746718`  
		Last Modified: Fri, 24 Apr 2020 15:30:04 GMT  
		Size: 1.9 MB (1863602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c12adea02bd50fa5aa1d04ea28e0994f0f789be746b3904caf21a329098c0ab`  
		Last Modified: Wed, 15 Jul 2020 00:23:10 GMT  
		Size: 22.8 MB (22776590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c28078b0904b5df388e2cf2bd487bf90616eea5ed1978a24a13efd120b549f`  
		Last Modified: Wed, 15 Jul 2020 00:23:03 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ecbc2075fb01004f36eda9fab53dd86582c46ee3b552ad2a9269f1f5831f58`  
		Last Modified: Wed, 15 Jul 2020 00:23:06 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
