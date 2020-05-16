<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:4.8.0.9`](#aerospike4809)
-	[`aerospike:4.9.0.7`](#aerospike4907)
-	[`aerospike:5.0.0.3`](#aerospike5003)
-	[`aerospike:latest`](#aerospikelatest)

## `aerospike:4.8.0.9`

```console
$ docker pull aerospike@sha256:6e1b75dfc2895f2d42c1f558b3a1bba7d46ac3ee24f42eeb7ba75d108044c854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:4.8.0.9` - linux; amd64

```console
$ docker pull aerospike@sha256:ad867f1ba41904a4e2e9934d0ca3c603450490928106ae32b48198f60782ee83
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51852804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:724739865e3319f782c68b7865a381fdee53f9a8c9862bed94a7bca2452edb15`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Fri, 15 May 2020 06:33:44 GMT
ADD file:ff87497c2a2fce1d776e432139030782373ac1549522a8366694786b45387306 in / 
# Fri, 15 May 2020 06:33:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 18:02:39 GMT
ENV AEROSPIKE_VERSION=4.8.0.9
# Fri, 15 May 2020 18:02:39 GMT
ENV AEROSPIKE_SHA256=3af1b8c97d73d05054582c8941d435bea55b7ead9b04d2df42f1e9990ab7e0c3
# Fri, 15 May 2020 18:02:56 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Fri, 15 May 2020 18:02:56 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Fri, 15 May 2020 18:02:56 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Fri, 15 May 2020 18:02:56 GMT
VOLUME [/opt/aerospike/data]
# Fri, 15 May 2020 18:02:56 GMT
EXPOSE 3000 3001 3002 3003
# Fri, 15 May 2020 18:02:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 May 2020 18:02:57 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:e62d08fa1eb18131b4109c7cbece97f4f7e37d6ea09845a21beb3a899d0c963d`  
		Last Modified: Fri, 15 May 2020 06:40:45 GMT  
		Size: 22.5 MB (22519887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54c9e0a0eb0f37ea0c57e87fa793ee69cbf6aa0e017305c081aa56f5d711aca`  
		Last Modified: Fri, 15 May 2020 18:03:44 GMT  
		Size: 29.3 MB (29330866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e132a4a8b95ea20303011bf6a6de40a791f949ec168cdbe700b7a863d31e6a6b`  
		Last Modified: Fri, 15 May 2020 18:03:37 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7662a0f44eac7d054f02f0fdb0fd60a55478e5b0e47c9575897e3a076732e8`  
		Last Modified: Fri, 15 May 2020 18:03:38 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:4.9.0.7`

```console
$ docker pull aerospike@sha256:135d516f8d6508bc5b3b5293e0003b8736f2dac5d84f4df78c445891ebcbb984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:4.9.0.7` - linux; amd64

```console
$ docker pull aerospike@sha256:260c5306d9d5961bdebfa30ddc2fc819c58fe47d024b89b0a663d14ae989c1da
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53201589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:475a63ab82870856af22648cab2e3b6551a159d100158ff3c9b7fd7c3438d44d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Fri, 15 May 2020 06:33:44 GMT
ADD file:ff87497c2a2fce1d776e432139030782373ac1549522a8366694786b45387306 in / 
# Fri, 15 May 2020 06:33:44 GMT
CMD ["bash"]
# Sat, 16 May 2020 09:59:29 GMT
ENV AEROSPIKE_VERSION=4.9.0.7
# Sat, 16 May 2020 09:59:29 GMT
ENV AEROSPIKE_SHA256=b0b900ffe201577307e838111c22507f3033c684051fc9963e8ec29eb9a1e7fb
# Sat, 16 May 2020 09:59:46 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Sat, 16 May 2020 09:59:47 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Sat, 16 May 2020 09:59:47 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Sat, 16 May 2020 09:59:47 GMT
VOLUME [/opt/aerospike/data]
# Sat, 16 May 2020 09:59:47 GMT
EXPOSE 3000 3001 3002 3003
# Sat, 16 May 2020 09:59:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 May 2020 09:59:48 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:e62d08fa1eb18131b4109c7cbece97f4f7e37d6ea09845a21beb3a899d0c963d`  
		Last Modified: Fri, 15 May 2020 06:40:45 GMT  
		Size: 22.5 MB (22519887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b6f569bec34084f4511bef874ebc6b4488f287f6c69e7260bbd7a83719b775`  
		Last Modified: Sat, 16 May 2020 10:00:29 GMT  
		Size: 30.7 MB (30679650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09615548fc25ca98dad5c4903138bd00764ce655939853ec2826b5d3828713fb`  
		Last Modified: Sat, 16 May 2020 10:00:23 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890247bc6fa2ea6e49c3e6c07a3494f38fe0a98ce0b2f0578c1d303cf1a3e34f`  
		Last Modified: Sat, 16 May 2020 10:00:23 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:5.0.0.3`

```console
$ docker pull aerospike@sha256:2d6e80246e17e3dc12a9fd115e903e343e3c9650bf8b337947233f0f531dfbac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.0.0.3` - linux; amd64

```console
$ docker pull aerospike@sha256:373d7c130166ba64e4ed0a1f48328bcced9db0b63e5298e7b7f21968ba66e98f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53089989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ec378e8545a6416e27ed38f0747abb7a5a053981fcb783de2e381f917ac3c3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Fri, 15 May 2020 06:33:44 GMT
ADD file:ff87497c2a2fce1d776e432139030782373ac1549522a8366694786b45387306 in / 
# Fri, 15 May 2020 06:33:44 GMT
CMD ["bash"]
# Sat, 16 May 2020 09:59:54 GMT
ENV AEROSPIKE_VERSION=5.0.0.3
# Sat, 16 May 2020 09:59:54 GMT
ENV AEROSPIKE_SHA256=024ebdd12d0088450a910d1eaa05685d03bf5762cafd4752fc59409a4534dc15
# Sat, 16 May 2020 10:00:11 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Sat, 16 May 2020 10:00:12 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Sat, 16 May 2020 10:00:12 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Sat, 16 May 2020 10:00:12 GMT
VOLUME [/opt/aerospike/data]
# Sat, 16 May 2020 10:00:12 GMT
EXPOSE 3000 3001 3002 3003
# Sat, 16 May 2020 10:00:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 May 2020 10:00:12 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:e62d08fa1eb18131b4109c7cbece97f4f7e37d6ea09845a21beb3a899d0c963d`  
		Last Modified: Fri, 15 May 2020 06:40:45 GMT  
		Size: 22.5 MB (22519887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3803b6657925020d950deb15c3e46603aba89e31dfe8a0930447c29e9d446c3e`  
		Last Modified: Sat, 16 May 2020 10:00:38 GMT  
		Size: 30.6 MB (30568049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5471d43ff27912d2be7280e4f85aed131d00a004c0ea4e6cbfd5c6303c27c7`  
		Last Modified: Sat, 16 May 2020 10:00:33 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520388c565fca8f3a80c46b5e1abbf085af875a08d2f168b31dcd4b3ae7cf500`  
		Last Modified: Sat, 16 May 2020 10:00:33 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:latest`

```console
$ docker pull aerospike@sha256:2d6e80246e17e3dc12a9fd115e903e343e3c9650bf8b337947233f0f531dfbac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:latest` - linux; amd64

```console
$ docker pull aerospike@sha256:373d7c130166ba64e4ed0a1f48328bcced9db0b63e5298e7b7f21968ba66e98f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53089989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ec378e8545a6416e27ed38f0747abb7a5a053981fcb783de2e381f917ac3c3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Fri, 15 May 2020 06:33:44 GMT
ADD file:ff87497c2a2fce1d776e432139030782373ac1549522a8366694786b45387306 in / 
# Fri, 15 May 2020 06:33:44 GMT
CMD ["bash"]
# Sat, 16 May 2020 09:59:54 GMT
ENV AEROSPIKE_VERSION=5.0.0.3
# Sat, 16 May 2020 09:59:54 GMT
ENV AEROSPIKE_SHA256=024ebdd12d0088450a910d1eaa05685d03bf5762cafd4752fc59409a4534dc15
# Sat, 16 May 2020 10:00:11 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Sat, 16 May 2020 10:00:12 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Sat, 16 May 2020 10:00:12 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Sat, 16 May 2020 10:00:12 GMT
VOLUME [/opt/aerospike/data]
# Sat, 16 May 2020 10:00:12 GMT
EXPOSE 3000 3001 3002 3003
# Sat, 16 May 2020 10:00:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 May 2020 10:00:12 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:e62d08fa1eb18131b4109c7cbece97f4f7e37d6ea09845a21beb3a899d0c963d`  
		Last Modified: Fri, 15 May 2020 06:40:45 GMT  
		Size: 22.5 MB (22519887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3803b6657925020d950deb15c3e46603aba89e31dfe8a0930447c29e9d446c3e`  
		Last Modified: Sat, 16 May 2020 10:00:38 GMT  
		Size: 30.6 MB (30568049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5471d43ff27912d2be7280e4f85aed131d00a004c0ea4e6cbfd5c6303c27c7`  
		Last Modified: Sat, 16 May 2020 10:00:33 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520388c565fca8f3a80c46b5e1abbf085af875a08d2f168b31dcd4b3ae7cf500`  
		Last Modified: Sat, 16 May 2020 10:00:33 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
