<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:4.8.0.13`](#aerospike48013)
-	[`aerospike:4.9.0.10`](#aerospike49010)
-	[`aerospike:5.0.0.7`](#aerospike5007)
-	[`aerospike:latest`](#aerospikelatest)

## `aerospike:4.8.0.13`

```console
$ docker pull aerospike@sha256:9f17db6f653abf72d531fe840e4233907eca54656b63a7d8acc910188907b604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:4.8.0.13` - linux; amd64

```console
$ docker pull aerospike@sha256:79238f6276d6ed414180c50037275a27a552430acaf0652562a613cee13e5225
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51854651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19ccf6a21ab5226819abb7bc701339ea2535ebd62a00ceef1ee4db2896f79da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Fri, 19 Jun 2020 23:19:35 GMT
ENV AEROSPIKE_VERSION=4.8.0.13
# Fri, 19 Jun 2020 23:19:35 GMT
ENV AEROSPIKE_SHA256=d00cc4b5e8443cda1f32d6354c22649d9f647aed4a980c3eca133ac61c63c78f
# Fri, 19 Jun 2020 23:19:52 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Fri, 19 Jun 2020 23:19:52 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Fri, 19 Jun 2020 23:19:52 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Fri, 19 Jun 2020 23:19:52 GMT
VOLUME [/opt/aerospike/data]
# Fri, 19 Jun 2020 23:19:52 GMT
EXPOSE 3000 3001 3002 3003
# Fri, 19 Jun 2020 23:19:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Jun 2020 23:19:53 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fdbb194e00c9a20ec1f424daf0ce9badc622df7cc3e51f0a9492ff77177e879`  
		Last Modified: Fri, 19 Jun 2020 23:20:48 GMT  
		Size: 29.3 MB (29332997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87253f20be5bca3ce1526320360af6def37b2c431826c51e2f98e2e40768d983`  
		Last Modified: Fri, 19 Jun 2020 23:20:43 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1215a128ece210c2d2bcc16a376c4a7ef3e9f73e5a677e05d064eb92d3bd0e6e`  
		Last Modified: Fri, 19 Jun 2020 23:20:42 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:4.9.0.10`

```console
$ docker pull aerospike@sha256:3b95269f094754a4be3cb18681e555be149366c0d8f93e539112da23146604bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:4.9.0.10` - linux; amd64

```console
$ docker pull aerospike@sha256:aa654c722a733088a9f1e4458a83985f6a2cc104347c54b04335ae758c226a09
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53205065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f5c73232e9d509073019599e10e266014bd384e9763491d5fbf75c5128d36d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Fri, 19 Jun 2020 23:19:56 GMT
ENV AEROSPIKE_VERSION=4.9.0.10
# Fri, 19 Jun 2020 23:19:57 GMT
ENV AEROSPIKE_SHA256=e53354adc330986a7a8325a2c1624260944e7d2d54103fabced2974c82235148
# Fri, 19 Jun 2020 23:20:13 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Fri, 19 Jun 2020 23:20:13 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Fri, 19 Jun 2020 23:20:13 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Fri, 19 Jun 2020 23:20:14 GMT
VOLUME [/opt/aerospike/data]
# Fri, 19 Jun 2020 23:20:14 GMT
EXPOSE 3000 3001 3002 3003
# Fri, 19 Jun 2020 23:20:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Jun 2020 23:20:14 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28cad9175fd2c531d9dbeb6f0462f42e7a84c82084a73277a298a19d09751227`  
		Last Modified: Fri, 19 Jun 2020 23:20:56 GMT  
		Size: 30.7 MB (30683414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aadb5dec3f5950729d6d918200303e8f1d947ea35a646fc98b08dc477658a7d5`  
		Last Modified: Fri, 19 Jun 2020 23:20:51 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65bdd018d578dc0b671a6d4d0824e0dad5736b0165b40344118fa445d7c3042`  
		Last Modified: Fri, 19 Jun 2020 23:20:52 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:5.0.0.7`

```console
$ docker pull aerospike@sha256:a73a550cd5de3cd91d0583f287cfd2c143f28fb0fd3cab3362b885dcccd81067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.0.0.7` - linux; amd64

```console
$ docker pull aerospike@sha256:402fba3ec00e0ba6a1392f18705395eb6cd2f487c2efa7ef2e639977bbecf404
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53092596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcdd5a5d6a87f71b4d12d89eb876123de143faba567831afda1bcb4898c56c2e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Fri, 19 Jun 2020 23:20:18 GMT
ENV AEROSPIKE_VERSION=5.0.0.7
# Fri, 19 Jun 2020 23:20:18 GMT
ENV AEROSPIKE_SHA256=360c2246000634f1950f9e398e6c6c7d63aab0b1785eee65b2c0625a47a6baf3
# Fri, 19 Jun 2020 23:20:35 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Fri, 19 Jun 2020 23:20:35 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Fri, 19 Jun 2020 23:20:35 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Fri, 19 Jun 2020 23:20:35 GMT
VOLUME [/opt/aerospike/data]
# Fri, 19 Jun 2020 23:20:35 GMT
EXPOSE 3000 3001 3002 3003
# Fri, 19 Jun 2020 23:20:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Jun 2020 23:20:36 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808c8ee1fa99dc8285305b6839f4e199fa51685682cd9978076e6fbf887cf0cc`  
		Last Modified: Fri, 19 Jun 2020 23:21:04 GMT  
		Size: 30.6 MB (30570941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad4ae699d60bd36624e78e01bf05fa85457b792c96ca1f2bc07ee76f1108d64`  
		Last Modified: Fri, 19 Jun 2020 23:21:00 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d84b7415983070eadf904efce532d171a9d5c961a8b501271a9aaf2665e9204`  
		Last Modified: Fri, 19 Jun 2020 23:20:59 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:latest`

```console
$ docker pull aerospike@sha256:a73a550cd5de3cd91d0583f287cfd2c143f28fb0fd3cab3362b885dcccd81067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:latest` - linux; amd64

```console
$ docker pull aerospike@sha256:402fba3ec00e0ba6a1392f18705395eb6cd2f487c2efa7ef2e639977bbecf404
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53092596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcdd5a5d6a87f71b4d12d89eb876123de143faba567831afda1bcb4898c56c2e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Fri, 19 Jun 2020 23:20:18 GMT
ENV AEROSPIKE_VERSION=5.0.0.7
# Fri, 19 Jun 2020 23:20:18 GMT
ENV AEROSPIKE_SHA256=360c2246000634f1950f9e398e6c6c7d63aab0b1785eee65b2c0625a47a6baf3
# Fri, 19 Jun 2020 23:20:35 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Fri, 19 Jun 2020 23:20:35 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Fri, 19 Jun 2020 23:20:35 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Fri, 19 Jun 2020 23:20:35 GMT
VOLUME [/opt/aerospike/data]
# Fri, 19 Jun 2020 23:20:35 GMT
EXPOSE 3000 3001 3002 3003
# Fri, 19 Jun 2020 23:20:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Jun 2020 23:20:36 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808c8ee1fa99dc8285305b6839f4e199fa51685682cd9978076e6fbf887cf0cc`  
		Last Modified: Fri, 19 Jun 2020 23:21:04 GMT  
		Size: 30.6 MB (30570941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad4ae699d60bd36624e78e01bf05fa85457b792c96ca1f2bc07ee76f1108d64`  
		Last Modified: Fri, 19 Jun 2020 23:21:00 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d84b7415983070eadf904efce532d171a9d5c961a8b501271a9aaf2665e9204`  
		Last Modified: Fri, 19 Jun 2020 23:20:59 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
