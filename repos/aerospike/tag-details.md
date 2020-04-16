<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:4.7.0.12`](#aerospike47012)
-	[`aerospike:4.8.0.8`](#aerospike4808)
-	[`aerospike:4.9.0.3`](#aerospike4903)
-	[`aerospike:latest`](#aerospikelatest)

## `aerospike:4.7.0.12`

```console
$ docker pull aerospike@sha256:2bdbd182fe40abd463a327d751329ad9f6ae3d3829525fd23d5d185eb7a2de51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:4.7.0.12` - linux; amd64

```console
$ docker pull aerospike@sha256:977a978ce3689c4123c7827a2f8c12326680f4750f1f6b1d64c60bbfffad513c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51769883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e961a9c77e1f8c0acc2cde67a0c5d9e20399c3549b7ededf2c0e456fa12a8612`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 04:21:46 GMT
ENV AEROSPIKE_VERSION=4.7.0.12
# Thu, 16 Apr 2020 04:21:46 GMT
ENV AEROSPIKE_SHA256=9169014025e376cf53cdd7440cad18f1dffe02feaa3abd697383a7678870efe8
# Thu, 16 Apr 2020 04:22:04 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Thu, 16 Apr 2020 04:22:04 GMT
COPY file:b2afebdf574a22640dc0687630172a267f2dc7857e8cd93254039deab3b62213 in /etc/aerospike/aerospike.template.conf 
# Thu, 16 Apr 2020 04:22:05 GMT
COPY file:688bc1b7dea55c1dc5575a99640936049823d07bac5c920bbace2369fbb27428 in /entrypoint.sh 
# Thu, 16 Apr 2020 04:22:05 GMT
VOLUME [/opt/aerospike/data]
# Thu, 16 Apr 2020 04:22:05 GMT
EXPOSE 3000 3001 3002 3003
# Thu, 16 Apr 2020 04:22:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 04:22:05 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f3dcd8d55ef50482e6457a645e5a592e51e66fe3218ef6207022a869dc29b8`  
		Last Modified: Thu, 16 Apr 2020 04:23:21 GMT  
		Size: 29.3 MB (29254388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef873c7b2fbcf5ee7bea439b735cad4209c9bb47bc7b13e566afb97d7744c57a`  
		Last Modified: Thu, 16 Apr 2020 04:23:05 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a10afea013429c929a9ea94cf5f6d37c3c343d4179abde24af6a6d07333f1cc3`  
		Last Modified: Thu, 16 Apr 2020 04:23:05 GMT  
		Size: 884.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:4.8.0.8`

```console
$ docker pull aerospike@sha256:d76a91f39a81edcfad96e7f4e5db2ba3b6fad14b70d25ff77831032e674c9afb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:4.8.0.8` - linux; amd64

```console
$ docker pull aerospike@sha256:243a741af89fd0f6c69b9e04217b84f2bdf569775663277570ddc4b601ba9752
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51846420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3f626a9b9587ac601b69e06098d17b0619bbe44272d672ba07167a08ec00df6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 04:22:11 GMT
ENV AEROSPIKE_VERSION=4.8.0.8
# Thu, 16 Apr 2020 04:22:11 GMT
ENV AEROSPIKE_SHA256=0239bb572069d4c803a5f558a4118c2dc7374ca539804fbc39a8d79101cf4e9e
# Thu, 16 Apr 2020 04:22:29 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Thu, 16 Apr 2020 04:22:30 GMT
COPY file:b2afebdf574a22640dc0687630172a267f2dc7857e8cd93254039deab3b62213 in /etc/aerospike/aerospike.template.conf 
# Thu, 16 Apr 2020 04:22:30 GMT
COPY file:688bc1b7dea55c1dc5575a99640936049823d07bac5c920bbace2369fbb27428 in /entrypoint.sh 
# Thu, 16 Apr 2020 04:22:30 GMT
VOLUME [/opt/aerospike/data]
# Thu, 16 Apr 2020 04:22:30 GMT
EXPOSE 3000 3001 3002 3003
# Thu, 16 Apr 2020 04:22:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 04:22:31 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cfb257286a96190cc73da13ba206953f40cbb6d9386aa5f2144126017a3b75`  
		Last Modified: Thu, 16 Apr 2020 04:23:33 GMT  
		Size: 29.3 MB (29330923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760937d190179afa9cea90a2089808c55601c0645c7221cb79a322af02235436`  
		Last Modified: Thu, 16 Apr 2020 04:23:25 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc2de25f59a78bab09b28f2abe3345f2e5848f34822364f2b03966feb05bf93`  
		Last Modified: Thu, 16 Apr 2020 04:23:25 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:4.9.0.3`

```console
$ docker pull aerospike@sha256:b6b40e3568816258ef9175d06093a59337bdbe18751d519b49556888234907c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:4.9.0.3` - linux; amd64

```console
$ docker pull aerospike@sha256:7915bb4e46d2e279b0a5cb2951ba21679b2a6c5aa9311a0d5072fc808da474cc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53186870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aad73c3f9e20bb385f374b4caf7742e3d7db82a4f38ef8e1b3404f89f2f2c03`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 04:22:36 GMT
ENV AEROSPIKE_VERSION=4.9.0.3
# Thu, 16 Apr 2020 04:22:36 GMT
ENV AEROSPIKE_SHA256=25247f67b4be624d46892dd1a66d945fafe1500107dd6cbf386dbc57e8816fb1
# Thu, 16 Apr 2020 04:22:54 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Thu, 16 Apr 2020 04:22:55 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Thu, 16 Apr 2020 04:22:55 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Thu, 16 Apr 2020 04:22:55 GMT
VOLUME [/opt/aerospike/data]
# Thu, 16 Apr 2020 04:22:55 GMT
EXPOSE 3000 3001 3002 3003
# Thu, 16 Apr 2020 04:22:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 04:22:56 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554195f11b8034f38d7be796bc6da3828644dee8d6d21c2496bc7a97b879f19f`  
		Last Modified: Thu, 16 Apr 2020 04:23:46 GMT  
		Size: 30.7 MB (30671339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcbb76112010ae06b66e51300b5b5f7696818f9d577b0eba13fab9cda7855d3`  
		Last Modified: Thu, 16 Apr 2020 04:23:38 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:badeb8f0ff3666a75a9425028bde0ac1b2a7d2103185722efe7627c308c35dd0`  
		Last Modified: Thu, 16 Apr 2020 04:23:38 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:latest`

```console
$ docker pull aerospike@sha256:b6b40e3568816258ef9175d06093a59337bdbe18751d519b49556888234907c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:latest` - linux; amd64

```console
$ docker pull aerospike@sha256:7915bb4e46d2e279b0a5cb2951ba21679b2a6c5aa9311a0d5072fc808da474cc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53186870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aad73c3f9e20bb385f374b4caf7742e3d7db82a4f38ef8e1b3404f89f2f2c03`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 04:22:36 GMT
ENV AEROSPIKE_VERSION=4.9.0.3
# Thu, 16 Apr 2020 04:22:36 GMT
ENV AEROSPIKE_SHA256=25247f67b4be624d46892dd1a66d945fafe1500107dd6cbf386dbc57e8816fb1
# Thu, 16 Apr 2020 04:22:54 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Thu, 16 Apr 2020 04:22:55 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Thu, 16 Apr 2020 04:22:55 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Thu, 16 Apr 2020 04:22:55 GMT
VOLUME [/opt/aerospike/data]
# Thu, 16 Apr 2020 04:22:55 GMT
EXPOSE 3000 3001 3002 3003
# Thu, 16 Apr 2020 04:22:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 04:22:56 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554195f11b8034f38d7be796bc6da3828644dee8d6d21c2496bc7a97b879f19f`  
		Last Modified: Thu, 16 Apr 2020 04:23:46 GMT  
		Size: 30.7 MB (30671339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcbb76112010ae06b66e51300b5b5f7696818f9d577b0eba13fab9cda7855d3`  
		Last Modified: Thu, 16 Apr 2020 04:23:38 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:badeb8f0ff3666a75a9425028bde0ac1b2a7d2103185722efe7627c308c35dd0`  
		Last Modified: Thu, 16 Apr 2020 04:23:38 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
