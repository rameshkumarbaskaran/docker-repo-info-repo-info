<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:4.9.0.11`](#aerospike49011)
-	[`aerospike:5.0.0.11`](#aerospike50011)
-	[`aerospike:5.1.0.6`](#aerospike5106)
-	[`aerospike:latest`](#aerospikelatest)

## `aerospike:4.9.0.11`

```console
$ docker pull aerospike@sha256:3ed94d365a3cebeda4e132a8cb5764d137ebd959e7b74219a4f02c02ff5b23a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:4.9.0.11` - linux; amd64

```console
$ docker pull aerospike@sha256:cfbcfc121b4fe4e221d82c1cf744bc8e9579a0b56a1be040d8bb6fd6938e8ce5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53212810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b229d5a4e94a0793f49dc38025c3a6dc6a07c79a83b06d270cb8b56b7f653e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:37 GMT
ADD file:83fbd2352bbac612c7a954e19abd295607cea4482c556c225308e0241b58e2bf in / 
# Thu, 10 Sep 2020 00:30:37 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:54:54 GMT
ENV AEROSPIKE_VERSION=4.9.0.11
# Thu, 10 Sep 2020 00:54:54 GMT
ENV AEROSPIKE_SHA256=6e53582b74800b5e93224ed34f30d2c8a3c191c7d27284070347fc7d8bb13fec
# Thu, 10 Sep 2020 00:55:18 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Thu, 10 Sep 2020 00:55:18 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Thu, 10 Sep 2020 00:55:19 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Thu, 10 Sep 2020 00:55:19 GMT
VOLUME [/opt/aerospike/data]
# Thu, 10 Sep 2020 00:55:19 GMT
EXPOSE 3000 3001 3002 3003
# Thu, 10 Sep 2020 00:55:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Sep 2020 00:55:20 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:abb454610128b028301ee40af387d31111a1e699e4ea424fd53186ff77067402`  
		Last Modified: Thu, 10 Sep 2020 00:37:40 GMT  
		Size: 22.5 MB (22522274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf31fccca46dc9a3a17f3afacaef597e601fce2b419fbbd284f0cf1f852c0aa`  
		Last Modified: Thu, 10 Sep 2020 00:56:35 GMT  
		Size: 30.7 MB (30688485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b169934483a3b2ef764743e24bc75d78eae54aaa7dd8c3d90d8c691c9ec359d8`  
		Last Modified: Thu, 10 Sep 2020 00:56:27 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc43c27fa8eced6c237933301a3850fd8a8a8933dd88719b0419e17b0c78bcfb`  
		Last Modified: Thu, 10 Sep 2020 00:56:27 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:5.0.0.11`

```console
$ docker pull aerospike@sha256:4b3deef6af93ccbc2e7642136beaefb3a21d4350dd1c1b5514121a7fe7d64647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.0.0.11` - linux; amd64

```console
$ docker pull aerospike@sha256:4ab38e4eeca91449330a40bbceec0657ccb1650275a5dedc3d194806f3dd3e95
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58576012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5423ddcccfc6daf22208e5bffdb452245342d1ddf4f529f4f0dd8c76a434e60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:37 GMT
ADD file:83fbd2352bbac612c7a954e19abd295607cea4482c556c225308e0241b58e2bf in / 
# Thu, 10 Sep 2020 00:30:37 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:54:19 GMT
ENV AEROSPIKE_VERSION=5.0.0.11
# Thu, 10 Sep 2020 00:54:19 GMT
ENV AEROSPIKE_SHA256=1df0eb6d966397572a5a350c72d76013eb7357c8d9614730a8e2b560c85d793a
# Thu, 10 Sep 2020 00:54:44 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Thu, 10 Sep 2020 00:54:45 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Thu, 10 Sep 2020 00:54:45 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Thu, 10 Sep 2020 00:54:46 GMT
VOLUME [/opt/aerospike/data]
# Thu, 10 Sep 2020 00:54:46 GMT
EXPOSE 3000 3001 3002 3003
# Thu, 10 Sep 2020 00:54:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Sep 2020 00:54:47 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:abb454610128b028301ee40af387d31111a1e699e4ea424fd53186ff77067402`  
		Last Modified: Thu, 10 Sep 2020 00:37:40 GMT  
		Size: 22.5 MB (22522274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c028e0144e24c80312e8795adb5f8b8832cd00bdde4659f45fb56bb3c8e487e`  
		Last Modified: Thu, 10 Sep 2020 00:56:23 GMT  
		Size: 36.1 MB (36051685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c3d872d399722d5de287755a68affd96eee77d8a302a3ceae5ea755744fd2e9`  
		Last Modified: Thu, 10 Sep 2020 00:56:15 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b0fec3e7bc60d47db5f54b32e11cc863ee51341c3ff54b03d90523fd517847`  
		Last Modified: Thu, 10 Sep 2020 00:56:15 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:5.1.0.6`

```console
$ docker pull aerospike@sha256:543645a77f4b53126e55f5a38188543e60bf993bbbbe6fa019132ed81852393a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.1.0.6` - linux; amd64

```console
$ docker pull aerospike@sha256:e973759b54ebb3499910e70f38b06ab1f46f848346bd2e50d5591b9dc1e1bbfc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (66025934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a9db1ae18281a52e7266307b073444b1a8c8eaa5a256de66ccd4d59bda4376`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:37 GMT
ADD file:83fbd2352bbac612c7a954e19abd295607cea4482c556c225308e0241b58e2bf in / 
# Thu, 10 Sep 2020 00:30:37 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:55:29 GMT
ENV AEROSPIKE_VERSION=5.1.0.6
# Thu, 10 Sep 2020 00:55:30 GMT
ENV AEROSPIKE_SHA256=64d39a81286de648592add8a4de3037c4141d55a135dfeddfa4b3c6534c297e7
# Thu, 10 Sep 2020 00:55:59 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Thu, 10 Sep 2020 00:56:00 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Thu, 10 Sep 2020 00:56:00 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Thu, 10 Sep 2020 00:56:00 GMT
VOLUME [/opt/aerospike/data]
# Thu, 10 Sep 2020 00:56:00 GMT
EXPOSE 3000 3001 3002 3003
# Thu, 10 Sep 2020 00:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Sep 2020 00:56:01 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:abb454610128b028301ee40af387d31111a1e699e4ea424fd53186ff77067402`  
		Last Modified: Thu, 10 Sep 2020 00:37:40 GMT  
		Size: 22.5 MB (22522274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e53d3cfb98de2eeedb7ef1e1c02db6b0c4a44abe56802cd991a7709350d64b9b`  
		Last Modified: Thu, 10 Sep 2020 00:56:47 GMT  
		Size: 43.5 MB (43501605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5aa4529669138b39187a737ae7aeef35616058aafaa999645dc080a9c893031`  
		Last Modified: Thu, 10 Sep 2020 00:56:39 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988d9b724bf04e46082c36fc348a21ae566913d72065b2d70c5f5136da82f599`  
		Last Modified: Thu, 10 Sep 2020 00:56:40 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:latest`

```console
$ docker pull aerospike@sha256:543645a77f4b53126e55f5a38188543e60bf993bbbbe6fa019132ed81852393a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:latest` - linux; amd64

```console
$ docker pull aerospike@sha256:e973759b54ebb3499910e70f38b06ab1f46f848346bd2e50d5591b9dc1e1bbfc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (66025934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a9db1ae18281a52e7266307b073444b1a8c8eaa5a256de66ccd4d59bda4376`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:37 GMT
ADD file:83fbd2352bbac612c7a954e19abd295607cea4482c556c225308e0241b58e2bf in / 
# Thu, 10 Sep 2020 00:30:37 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:55:29 GMT
ENV AEROSPIKE_VERSION=5.1.0.6
# Thu, 10 Sep 2020 00:55:30 GMT
ENV AEROSPIKE_SHA256=64d39a81286de648592add8a4de3037c4141d55a135dfeddfa4b3c6534c297e7
# Thu, 10 Sep 2020 00:55:59 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Thu, 10 Sep 2020 00:56:00 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Thu, 10 Sep 2020 00:56:00 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Thu, 10 Sep 2020 00:56:00 GMT
VOLUME [/opt/aerospike/data]
# Thu, 10 Sep 2020 00:56:00 GMT
EXPOSE 3000 3001 3002 3003
# Thu, 10 Sep 2020 00:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Sep 2020 00:56:01 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:abb454610128b028301ee40af387d31111a1e699e4ea424fd53186ff77067402`  
		Last Modified: Thu, 10 Sep 2020 00:37:40 GMT  
		Size: 22.5 MB (22522274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e53d3cfb98de2eeedb7ef1e1c02db6b0c4a44abe56802cd991a7709350d64b9b`  
		Last Modified: Thu, 10 Sep 2020 00:56:47 GMT  
		Size: 43.5 MB (43501605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5aa4529669138b39187a737ae7aeef35616058aafaa999645dc080a9c893031`  
		Last Modified: Thu, 10 Sep 2020 00:56:39 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988d9b724bf04e46082c36fc348a21ae566913d72065b2d70c5f5136da82f599`  
		Last Modified: Thu, 10 Sep 2020 00:56:40 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
