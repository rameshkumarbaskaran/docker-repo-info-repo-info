<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:5.3.0.14`](#aerospike53014)
-	[`aerospike:5.4.0.9`](#aerospike5409)
-	[`aerospike:5.5.0.7`](#aerospike5507)
-	[`aerospike:latest`](#aerospikelatest)

## `aerospike:5.3.0.14`

```console
$ docker pull aerospike@sha256:c6a51455c30641cfeab79cf88ab133632d70b7134720dbde812bf3e9e7c5690b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.3.0.14` - linux; amd64

```console
$ docker pull aerospike@sha256:2f1523baf3b9a9588980c726e70d919ef3fc1eef5a37fd2c7419c64065112959
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74716658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060ea8606831eee0a117c163031deb66a4bb5f333fe6036e03ceefe5e05e8813`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:55 GMT
ADD file:65a51da79ba9e2993b794078e3e24554bff59ac80185f12845c1426c7173f06f in / 
# Tue, 30 Mar 2021 21:50:55 GMT
CMD ["bash"]
# Thu, 01 Apr 2021 21:08:14 GMT
ENV AEROSPIKE_VERSION=5.3.0.14
# Thu, 01 Apr 2021 21:08:14 GMT
ENV AEROSPIKE_SHA256=9a0d4f167d89a307822ed66f80da8b6feedb869c058baa1d0eab1891207999d5
# Thu, 01 Apr 2021 21:08:35 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Thu, 01 Apr 2021 21:08:35 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Thu, 01 Apr 2021 21:08:36 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Thu, 01 Apr 2021 21:08:36 GMT
EXPOSE 3000 3001 3002 3003
# Thu, 01 Apr 2021 21:08:36 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Thu, 01 Apr 2021 21:08:36 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:23a3602cd30cf5ce6da03e18c28bbbfdc12ae98f182462de8c55785a8d982431`  
		Last Modified: Tue, 30 Mar 2021 21:57:04 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4610a1e5a23471984f31e631dcd160289fd28582c15f18d4d118f61082cccd5f`  
		Last Modified: Thu, 01 Apr 2021 21:09:46 GMT  
		Size: 52.2 MB (52186338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e430c8fa327399f697e4d1d7a3d5395a06634a51ca29e4a9409d5770bd4ed35e`  
		Last Modified: Thu, 01 Apr 2021 21:09:38 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6b7e6cda3f775d87be91b89ca89af07691c1f24e5d5a31a283d0d148e7307e`  
		Last Modified: Thu, 01 Apr 2021 21:09:38 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:5.4.0.9`

```console
$ docker pull aerospike@sha256:09673514075f00bb710935a9f2b2d92c0f8a3dbf6f7eaafbee4a1a6c25f02fb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.4.0.9` - linux; amd64

```console
$ docker pull aerospike@sha256:5372a760e466e8cb4110993436e638ec2526ad1e9dd47ed3a2770b2914452245
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74738886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46a2611aef6ae0e4ccbf57922c26f068937cd68c71923139d3ec4670893c1756`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:55 GMT
ADD file:65a51da79ba9e2993b794078e3e24554bff59ac80185f12845c1426c7173f06f in / 
# Tue, 30 Mar 2021 21:50:55 GMT
CMD ["bash"]
# Thu, 01 Apr 2021 21:08:40 GMT
ENV AEROSPIKE_VERSION=5.4.0.9
# Thu, 01 Apr 2021 21:08:40 GMT
ENV AEROSPIKE_SHA256=6262abe20f3ade81beecbc6b46766e0d63fb8c31c0ec1e20f543ff023f9479a3
# Thu, 01 Apr 2021 21:08:59 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Thu, 01 Apr 2021 21:08:59 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Thu, 01 Apr 2021 21:09:00 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Thu, 01 Apr 2021 21:09:00 GMT
EXPOSE 3000 3001 3002 3003
# Thu, 01 Apr 2021 21:09:00 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Thu, 01 Apr 2021 21:09:00 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:23a3602cd30cf5ce6da03e18c28bbbfdc12ae98f182462de8c55785a8d982431`  
		Last Modified: Tue, 30 Mar 2021 21:57:04 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bead85dd3edd34cae8682e9e4bb24fde570347a31dbcb14824af9c633e7c403`  
		Last Modified: Thu, 01 Apr 2021 21:10:07 GMT  
		Size: 52.2 MB (52208568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c29d1b9578b723b7587f623b9e68a4ddf7436fffa03bf6953f9f90c3113a59`  
		Last Modified: Thu, 01 Apr 2021 21:09:55 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4551231051ac609ebf6216ef81f858b6a27f48fa185bb9e13376e50345326a4`  
		Last Modified: Thu, 01 Apr 2021 21:09:55 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:5.5.0.7`

```console
$ docker pull aerospike@sha256:04fc9501086e7e9c18ac64a90a4ebb6cbf23c77727fbdc25a457d9430136e281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.5.0.7` - linux; amd64

```console
$ docker pull aerospike@sha256:bf29911f6816a54e7170fa6e169c59664816aa028edaeb55ada3f338853f1de3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74781897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0dc2c5e2848459108ce93d7d155ea1a4bee4ac89f9600c26c1361087701c0b0`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:55 GMT
ADD file:65a51da79ba9e2993b794078e3e24554bff59ac80185f12845c1426c7173f06f in / 
# Tue, 30 Mar 2021 21:50:55 GMT
CMD ["bash"]
# Thu, 01 Apr 2021 21:09:05 GMT
ENV AEROSPIKE_VERSION=5.5.0.7
# Thu, 01 Apr 2021 21:09:06 GMT
ENV AEROSPIKE_SHA256=43cc7c0b135fa8a0186a8ce9b5f923660e59e3ef8ec32a742a5b533c1d3caaa3
# Thu, 01 Apr 2021 21:09:24 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Thu, 01 Apr 2021 21:09:25 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Thu, 01 Apr 2021 21:09:25 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Thu, 01 Apr 2021 21:09:25 GMT
EXPOSE 3000 3001 3002 3003
# Thu, 01 Apr 2021 21:09:26 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Thu, 01 Apr 2021 21:09:26 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:23a3602cd30cf5ce6da03e18c28bbbfdc12ae98f182462de8c55785a8d982431`  
		Last Modified: Tue, 30 Mar 2021 21:57:04 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf56e3c1a85e85f87133b7dfde7e4e114373ff7799b9cdd4dc820880a685b50`  
		Last Modified: Thu, 01 Apr 2021 21:10:24 GMT  
		Size: 52.3 MB (52251580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85edc666eeea96e55b0d2ef37c1c18396dcc08325d1f03b957de6755114823e`  
		Last Modified: Thu, 01 Apr 2021 21:10:16 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f9cf26727af2799808e437adb62db46c95b62c3bd983bc877bce31a489dd94`  
		Last Modified: Thu, 01 Apr 2021 21:10:18 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:latest`

```console
$ docker pull aerospike@sha256:04fc9501086e7e9c18ac64a90a4ebb6cbf23c77727fbdc25a457d9430136e281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:latest` - linux; amd64

```console
$ docker pull aerospike@sha256:bf29911f6816a54e7170fa6e169c59664816aa028edaeb55ada3f338853f1de3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74781897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0dc2c5e2848459108ce93d7d155ea1a4bee4ac89f9600c26c1361087701c0b0`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:55 GMT
ADD file:65a51da79ba9e2993b794078e3e24554bff59ac80185f12845c1426c7173f06f in / 
# Tue, 30 Mar 2021 21:50:55 GMT
CMD ["bash"]
# Thu, 01 Apr 2021 21:09:05 GMT
ENV AEROSPIKE_VERSION=5.5.0.7
# Thu, 01 Apr 2021 21:09:06 GMT
ENV AEROSPIKE_SHA256=43cc7c0b135fa8a0186a8ce9b5f923660e59e3ef8ec32a742a5b533c1d3caaa3
# Thu, 01 Apr 2021 21:09:24 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Thu, 01 Apr 2021 21:09:25 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Thu, 01 Apr 2021 21:09:25 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Thu, 01 Apr 2021 21:09:25 GMT
EXPOSE 3000 3001 3002 3003
# Thu, 01 Apr 2021 21:09:26 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Thu, 01 Apr 2021 21:09:26 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:23a3602cd30cf5ce6da03e18c28bbbfdc12ae98f182462de8c55785a8d982431`  
		Last Modified: Tue, 30 Mar 2021 21:57:04 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf56e3c1a85e85f87133b7dfde7e4e114373ff7799b9cdd4dc820880a685b50`  
		Last Modified: Thu, 01 Apr 2021 21:10:24 GMT  
		Size: 52.3 MB (52251580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85edc666eeea96e55b0d2ef37c1c18396dcc08325d1f03b957de6755114823e`  
		Last Modified: Thu, 01 Apr 2021 21:10:16 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f9cf26727af2799808e437adb62db46c95b62c3bd983bc877bce31a489dd94`  
		Last Modified: Thu, 01 Apr 2021 21:10:18 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
