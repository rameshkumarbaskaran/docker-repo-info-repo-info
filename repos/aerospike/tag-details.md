<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:4.7.0.12`](#aerospike47012)
-	[`aerospike:4.8.0.8`](#aerospike4808)
-	[`aerospike:4.9.0.3`](#aerospike4903)
-	[`aerospike:latest`](#aerospikelatest)

## `aerospike:4.7.0.12`

```console
$ docker pull aerospike@sha256:ba2381650fecd678192971f8e3e2cd7a0da6e2d22f5e1ceef4d28ba62ff1d893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:4.7.0.12` - linux; amd64

```console
$ docker pull aerospike@sha256:2b52d5b194024ef296c5acd0040452c58e6ee8f7bd8a1de00181a3857ef147c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51769772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98932242e8c335fd35ffd6dc476fcb7622b6d05f0d49508e382566c0b14f1236`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 31 Mar 2020 01:24:08 GMT
ADD file:e077f4d014ea0869fc4b3d5a3e6b3c8b792a97a8b4a328f33a994369225ff222 in / 
# Tue, 31 Mar 2020 01:24:08 GMT
CMD ["bash"]
# Mon, 06 Apr 2020 20:19:54 GMT
ENV AEROSPIKE_VERSION=4.7.0.12
# Mon, 06 Apr 2020 20:19:54 GMT
ENV AEROSPIKE_SHA256=9169014025e376cf53cdd7440cad18f1dffe02feaa3abd697383a7678870efe8
# Mon, 06 Apr 2020 20:20:10 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Mon, 06 Apr 2020 20:20:10 GMT
COPY file:b2afebdf574a22640dc0687630172a267f2dc7857e8cd93254039deab3b62213 in /etc/aerospike/aerospike.template.conf 
# Mon, 06 Apr 2020 20:20:11 GMT
COPY file:688bc1b7dea55c1dc5575a99640936049823d07bac5c920bbace2369fbb27428 in /entrypoint.sh 
# Mon, 06 Apr 2020 20:20:11 GMT
VOLUME [/opt/aerospike/data]
# Mon, 06 Apr 2020 20:20:11 GMT
EXPOSE 3000 3001 3002 3003
# Mon, 06 Apr 2020 20:20:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Apr 2020 20:20:11 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:48839397421a64189661c2b86a34eb515d09a28204587a2b06b59df9f6e2d786`  
		Last Modified: Tue, 31 Mar 2020 01:29:28 GMT  
		Size: 22.5 MB (22513374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8eabfb5467e067c4d6aaa9fa92b7f3959870ede017f53466c2337544dbff547`  
		Last Modified: Mon, 06 Apr 2020 20:21:00 GMT  
		Size: 29.3 MB (29254380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e574a99b8b5abf9cee6c9938e14915685fe9f13e5a64ce123504d9a6d034c11a`  
		Last Modified: Mon, 06 Apr 2020 20:20:53 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d391642ed04e4c6b581833435df9f4b7c85a3c941d1fd13b3d9512d1c417cb4e`  
		Last Modified: Mon, 06 Apr 2020 20:20:53 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:4.8.0.8`

```console
$ docker pull aerospike@sha256:35b760bff9e667957cfa8cf84a708054a369edb01c6c026aefd54f395f7c31d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:4.8.0.8` - linux; amd64

```console
$ docker pull aerospike@sha256:fa7148002aa3462b955fdd02b24a8bec666a362610991821ab9fc7c4ae1941d2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51846274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa12f3b4547044802cb4b1d2da2d5f9b3cedb53c8d7972ea3dfd4e59d63ff7db`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 31 Mar 2020 01:24:08 GMT
ADD file:e077f4d014ea0869fc4b3d5a3e6b3c8b792a97a8b4a328f33a994369225ff222 in / 
# Tue, 31 Mar 2020 01:24:08 GMT
CMD ["bash"]
# Mon, 06 Apr 2020 20:20:18 GMT
ENV AEROSPIKE_VERSION=4.8.0.8
# Mon, 06 Apr 2020 20:20:18 GMT
ENV AEROSPIKE_SHA256=0239bb572069d4c803a5f558a4118c2dc7374ca539804fbc39a8d79101cf4e9e
# Mon, 06 Apr 2020 20:20:34 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Mon, 06 Apr 2020 20:20:34 GMT
COPY file:b2afebdf574a22640dc0687630172a267f2dc7857e8cd93254039deab3b62213 in /etc/aerospike/aerospike.template.conf 
# Mon, 06 Apr 2020 20:20:35 GMT
COPY file:688bc1b7dea55c1dc5575a99640936049823d07bac5c920bbace2369fbb27428 in /entrypoint.sh 
# Mon, 06 Apr 2020 20:20:35 GMT
VOLUME [/opt/aerospike/data]
# Mon, 06 Apr 2020 20:20:35 GMT
EXPOSE 3000 3001 3002 3003
# Mon, 06 Apr 2020 20:20:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Apr 2020 20:20:35 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:48839397421a64189661c2b86a34eb515d09a28204587a2b06b59df9f6e2d786`  
		Last Modified: Tue, 31 Mar 2020 01:29:28 GMT  
		Size: 22.5 MB (22513374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0507a6f2f524418c20cb5c52ca79a4ac9f3be0bb19451cf85b47702ab0903a8a`  
		Last Modified: Mon, 06 Apr 2020 20:21:08 GMT  
		Size: 29.3 MB (29330884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7edbd6426c9989b8a3350590a8d4c692aad4640fcba9191dd3293c311d4dda6`  
		Last Modified: Mon, 06 Apr 2020 20:21:03 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec4fc6a2dd147c52fe9fc71a32d142b2827d23832929a523e46cf000eaa484e`  
		Last Modified: Mon, 06 Apr 2020 20:21:03 GMT  
		Size: 883.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:4.9.0.3`

```console
$ docker pull aerospike@sha256:1c3cd90dfa8f12470743d1ab641d70c2052b62d5d2bc58049007e104c6b2c86c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:4.9.0.3` - linux; amd64

```console
$ docker pull aerospike@sha256:efce6e2675e95058e6931c7f2b683972455a875f80faa4667212e692bcaba6b0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53186704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4a0b12fdad420cc1bd82126a72345ca9d52db59ead9b18f10be20ec82db41e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 31 Mar 2020 01:24:08 GMT
ADD file:e077f4d014ea0869fc4b3d5a3e6b3c8b792a97a8b4a328f33a994369225ff222 in / 
# Tue, 31 Mar 2020 01:24:08 GMT
CMD ["bash"]
# Thu, 09 Apr 2020 23:19:31 GMT
ENV AEROSPIKE_VERSION=4.9.0.3
# Thu, 09 Apr 2020 23:19:31 GMT
ENV AEROSPIKE_SHA256=25247f67b4be624d46892dd1a66d945fafe1500107dd6cbf386dbc57e8816fb1
# Thu, 09 Apr 2020 23:19:48 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Thu, 09 Apr 2020 23:19:48 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Thu, 09 Apr 2020 23:19:48 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Thu, 09 Apr 2020 23:19:49 GMT
VOLUME [/opt/aerospike/data]
# Thu, 09 Apr 2020 23:19:49 GMT
EXPOSE 3000 3001 3002 3003
# Thu, 09 Apr 2020 23:19:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Apr 2020 23:19:49 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:48839397421a64189661c2b86a34eb515d09a28204587a2b06b59df9f6e2d786`  
		Last Modified: Tue, 31 Mar 2020 01:29:28 GMT  
		Size: 22.5 MB (22513374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9004eabd75801c3bae71075f0c59d359fd3f8b964e65a4f9c62a8df9ad49d5b1`  
		Last Modified: Thu, 09 Apr 2020 23:20:05 GMT  
		Size: 30.7 MB (30671276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ba11442efceabdd1004f7bacbac60b3db8428470f2e7b0a941a5fcc905790b`  
		Last Modified: Thu, 09 Apr 2020 23:20:00 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65391cd73ac1d78cc2231f411758c89e3f1b9aec2ebfa8b1d6d537a70da84a9f`  
		Last Modified: Thu, 09 Apr 2020 23:20:00 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:latest`

```console
$ docker pull aerospike@sha256:1c3cd90dfa8f12470743d1ab641d70c2052b62d5d2bc58049007e104c6b2c86c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:latest` - linux; amd64

```console
$ docker pull aerospike@sha256:efce6e2675e95058e6931c7f2b683972455a875f80faa4667212e692bcaba6b0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53186704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4a0b12fdad420cc1bd82126a72345ca9d52db59ead9b18f10be20ec82db41e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 31 Mar 2020 01:24:08 GMT
ADD file:e077f4d014ea0869fc4b3d5a3e6b3c8b792a97a8b4a328f33a994369225ff222 in / 
# Tue, 31 Mar 2020 01:24:08 GMT
CMD ["bash"]
# Thu, 09 Apr 2020 23:19:31 GMT
ENV AEROSPIKE_VERSION=4.9.0.3
# Thu, 09 Apr 2020 23:19:31 GMT
ENV AEROSPIKE_SHA256=25247f67b4be624d46892dd1a66d945fafe1500107dd6cbf386dbc57e8816fb1
# Thu, 09 Apr 2020 23:19:48 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Thu, 09 Apr 2020 23:19:48 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Thu, 09 Apr 2020 23:19:48 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Thu, 09 Apr 2020 23:19:49 GMT
VOLUME [/opt/aerospike/data]
# Thu, 09 Apr 2020 23:19:49 GMT
EXPOSE 3000 3001 3002 3003
# Thu, 09 Apr 2020 23:19:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Apr 2020 23:19:49 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:48839397421a64189661c2b86a34eb515d09a28204587a2b06b59df9f6e2d786`  
		Last Modified: Tue, 31 Mar 2020 01:29:28 GMT  
		Size: 22.5 MB (22513374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9004eabd75801c3bae71075f0c59d359fd3f8b964e65a4f9c62a8df9ad49d5b1`  
		Last Modified: Thu, 09 Apr 2020 23:20:05 GMT  
		Size: 30.7 MB (30671276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ba11442efceabdd1004f7bacbac60b3db8428470f2e7b0a941a5fcc905790b`  
		Last Modified: Thu, 09 Apr 2020 23:20:00 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65391cd73ac1d78cc2231f411758c89e3f1b9aec2ebfa8b1d6d537a70da84a9f`  
		Last Modified: Thu, 09 Apr 2020 23:20:00 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
