<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:4.8.0.11`](#aerospike48011)
-	[`aerospike:4.9.0.8`](#aerospike4908)
-	[`aerospike:5.0.0.4`](#aerospike5004)
-	[`aerospike:latest`](#aerospikelatest)

## `aerospike:4.8.0.11`

```console
$ docker pull aerospike@sha256:1654c43985d3b57f0e83af3207d26e44c10ede72e0e79cd44258b84421fa21a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:4.8.0.11` - linux; amd64

```console
$ docker pull aerospike@sha256:bd67bb87be648ac2dd332bca7878c8473b78cb84154342cf58ba767829aa8e7e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51851926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f1aed234410b11680b293dd4132060152cca18480e667953ac11e1b06afd343`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:03:48 GMT
ENV AEROSPIKE_VERSION=4.8.0.11
# Tue, 09 Jun 2020 02:03:49 GMT
ENV AEROSPIKE_SHA256=534f3ceb2da1e3914a62dff0cb4f876f7eacb9f30d029389dea1723387744aa3
# Tue, 09 Jun 2020 02:04:05 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Tue, 09 Jun 2020 02:04:05 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Tue, 09 Jun 2020 02:04:06 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Tue, 09 Jun 2020 02:04:06 GMT
VOLUME [/opt/aerospike/data]
# Tue, 09 Jun 2020 02:04:06 GMT
EXPOSE 3000 3001 3002 3003
# Tue, 09 Jun 2020 02:04:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2020 02:04:06 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0949cbee0718ec6d0a280976ef9a40e179a4062bfcf46437488be11bdaed5d06`  
		Last Modified: Tue, 09 Jun 2020 02:05:04 GMT  
		Size: 29.3 MB (29330274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43239f6561699aa03342f6fc3575fba005740a21dc0b0b4309fb147022ebda72`  
		Last Modified: Tue, 09 Jun 2020 02:04:59 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e528a2687f3d295fca3e2529e2693652675c275962ca7499c54006935e0d4df`  
		Last Modified: Tue, 09 Jun 2020 02:04:59 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:4.9.0.8`

```console
$ docker pull aerospike@sha256:3033a8cbdf0abea9470a5a2c111afa86d7e7d5f797b9681978af3d67929de238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:4.9.0.8` - linux; amd64

```console
$ docker pull aerospike@sha256:ba196732c484e9c9691e791dfba31ae297a80df7272b79b1c08925e600a2fb2c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53201544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a227ec8a1f9a067555e8ca41af81001f82582e2563e83b642f566f5a28c607c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:04:10 GMT
ENV AEROSPIKE_VERSION=4.9.0.8
# Tue, 09 Jun 2020 02:04:10 GMT
ENV AEROSPIKE_SHA256=dc41beb743ddc495c4c202897df8fc5000e764b659697beeb231e70f71005016
# Tue, 09 Jun 2020 02:04:27 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Tue, 09 Jun 2020 02:04:27 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Tue, 09 Jun 2020 02:04:27 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Tue, 09 Jun 2020 02:04:27 GMT
VOLUME [/opt/aerospike/data]
# Tue, 09 Jun 2020 02:04:27 GMT
EXPOSE 3000 3001 3002 3003
# Tue, 09 Jun 2020 02:04:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2020 02:04:28 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298d15f17a3552dbf6f326c25e997c962354e42d2b55edd72261c0fac34a4f24`  
		Last Modified: Tue, 09 Jun 2020 02:05:14 GMT  
		Size: 30.7 MB (30679889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee648759663a71326069609a14b2197c2f72dc40fa8bd8b383cc9c4d56a003d3`  
		Last Modified: Tue, 09 Jun 2020 02:05:08 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0242b721cfa1fbc23c5e29fca4536dddefa2c63ea23b7160527bf591991238d3`  
		Last Modified: Tue, 09 Jun 2020 02:05:08 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:5.0.0.4`

```console
$ docker pull aerospike@sha256:91cb9f29893778cc7fd057e9bf886bb71628d31d2ffccd8689ecb8f4e6e4e02b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.0.0.4` - linux; amd64

```console
$ docker pull aerospike@sha256:b10369efe4af266c63474d889dd9167c3075bac3a8de4f67a7f3a402ee0c9fab
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53089904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a7074862faf8d5a97a415a48e557460e49e028d13d2c6853b2abdb613a10f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:04:32 GMT
ENV AEROSPIKE_VERSION=5.0.0.4
# Tue, 09 Jun 2020 02:04:32 GMT
ENV AEROSPIKE_SHA256=30638676e17a5918fcc91a5e1b93eec95823a465d1c68bdf8574241d5e68ea61
# Tue, 09 Jun 2020 02:04:48 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Tue, 09 Jun 2020 02:04:48 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Tue, 09 Jun 2020 02:04:49 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Tue, 09 Jun 2020 02:04:49 GMT
VOLUME [/opt/aerospike/data]
# Tue, 09 Jun 2020 02:04:49 GMT
EXPOSE 3000 3001 3002 3003
# Tue, 09 Jun 2020 02:04:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2020 02:04:49 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7491f76e61c609a91b8f60978235d5db989ed1953e1e70d6b8ff1474cab0c1`  
		Last Modified: Tue, 09 Jun 2020 02:05:23 GMT  
		Size: 30.6 MB (30568251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c450f1531aa2cae488b301f21b68fa3a975c48b2946cb060393888f03c16a3`  
		Last Modified: Tue, 09 Jun 2020 02:05:17 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec091a552d089f05ae2c6f48a602750ba2f3af0d7b8f6439e3c94e2eca35c07b`  
		Last Modified: Tue, 09 Jun 2020 02:05:17 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:latest`

```console
$ docker pull aerospike@sha256:91cb9f29893778cc7fd057e9bf886bb71628d31d2ffccd8689ecb8f4e6e4e02b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:latest` - linux; amd64

```console
$ docker pull aerospike@sha256:b10369efe4af266c63474d889dd9167c3075bac3a8de4f67a7f3a402ee0c9fab
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53089904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a7074862faf8d5a97a415a48e557460e49e028d13d2c6853b2abdb613a10f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:04:32 GMT
ENV AEROSPIKE_VERSION=5.0.0.4
# Tue, 09 Jun 2020 02:04:32 GMT
ENV AEROSPIKE_SHA256=30638676e17a5918fcc91a5e1b93eec95823a465d1c68bdf8574241d5e68ea61
# Tue, 09 Jun 2020 02:04:48 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Tue, 09 Jun 2020 02:04:48 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Tue, 09 Jun 2020 02:04:49 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Tue, 09 Jun 2020 02:04:49 GMT
VOLUME [/opt/aerospike/data]
# Tue, 09 Jun 2020 02:04:49 GMT
EXPOSE 3000 3001 3002 3003
# Tue, 09 Jun 2020 02:04:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2020 02:04:49 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7491f76e61c609a91b8f60978235d5db989ed1953e1e70d6b8ff1474cab0c1`  
		Last Modified: Tue, 09 Jun 2020 02:05:23 GMT  
		Size: 30.6 MB (30568251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c450f1531aa2cae488b301f21b68fa3a975c48b2946cb060393888f03c16a3`  
		Last Modified: Tue, 09 Jun 2020 02:05:17 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec091a552d089f05ae2c6f48a602750ba2f3af0d7b8f6439e3c94e2eca35c07b`  
		Last Modified: Tue, 09 Jun 2020 02:05:17 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
