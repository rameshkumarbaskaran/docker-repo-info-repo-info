<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:5.1.0.20`](#aerospike51020)
-	[`aerospike:5.2.0.12`](#aerospike52012)
-	[`aerospike:5.3.0.3`](#aerospike5303)
-	[`aerospike:latest`](#aerospikelatest)

## `aerospike:5.1.0.20`

```console
$ docker pull aerospike@sha256:0f14038554acb311c5f6025a9d8987df29f535d3cecf392f38f37035a7a4b05a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.1.0.20` - linux; amd64

```console
$ docker pull aerospike@sha256:6683026ef3ea713f2f333d3e9c89b8cd068a2a3f73ba8e91a423a26ea0532c7c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76358037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1071441977a3f2037eea3905062e690549ad3f0df01a6cd9473e844f21b5d29`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:58 GMT
ADD file:f03e68a10b84e2342cfffbb8cdec1117c7f5e5d0dd004072e84efb62cfdf157c in / 
# Fri, 11 Dec 2020 02:08:58 GMT
CMD ["bash"]
# Mon, 21 Dec 2020 19:19:44 GMT
ENV AEROSPIKE_VERSION=5.1.0.20
# Mon, 21 Dec 2020 19:19:45 GMT
ENV AEROSPIKE_SHA256=1cf1497c88baf917b37f0b4af380a3ce403c3ce47538c5b1d38737bfe45d1ac9
# Mon, 21 Dec 2020 19:20:07 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Mon, 21 Dec 2020 19:20:07 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Mon, 21 Dec 2020 19:20:07 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Mon, 21 Dec 2020 19:20:07 GMT
EXPOSE 3000 3001 3002 3003
# Mon, 21 Dec 2020 19:20:07 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Mon, 21 Dec 2020 19:20:08 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:e50c3c9ef5a201a24959788dcbc7ebf88d95c63e132a4d7396ce541127afd88e`  
		Last Modified: Fri, 11 Dec 2020 02:15:43 GMT  
		Size: 22.5 MB (22527860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a4c344029947c9d85399552b2ea320b0c29627430dcb6b728d0a0889b30f49`  
		Last Modified: Mon, 21 Dec 2020 19:21:27 GMT  
		Size: 53.8 MB (53828124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36592aa6712877354834516cf981e41a1b20af51dd98f669d67295bd2ac6764`  
		Last Modified: Mon, 21 Dec 2020 19:21:19 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8896e05c95ba36607ceda3da2ac013421f76bfa3d78f1a1c18d03e9bb0c1d05`  
		Last Modified: Mon, 21 Dec 2020 19:21:18 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:5.2.0.12`

```console
$ docker pull aerospike@sha256:b61a5ac51aa988520d12bec8a4e95a1fcc70d4b5a028d0fb03bdc1da2c9e4001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.2.0.12` - linux; amd64

```console
$ docker pull aerospike@sha256:e206d69f5f1431450787a349e430928a72b4b1f647f0c3441aaa5c817ba2b2cf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76275595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a115bc02b645d2cbfd768f8f63f75e12f795baaaa004e301dd8c3fa569225fce`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:58 GMT
ADD file:f03e68a10b84e2342cfffbb8cdec1117c7f5e5d0dd004072e84efb62cfdf157c in / 
# Fri, 11 Dec 2020 02:08:58 GMT
CMD ["bash"]
# Mon, 21 Dec 2020 19:20:14 GMT
ENV AEROSPIKE_VERSION=5.2.0.12
# Mon, 21 Dec 2020 19:20:14 GMT
ENV AEROSPIKE_SHA256=890c27dde115223e29cb01b65571c6d2f1d36bb8ac94c22b3244d7ad710ffbdc
# Mon, 21 Dec 2020 19:20:36 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Mon, 21 Dec 2020 19:20:36 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Mon, 21 Dec 2020 19:20:36 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Mon, 21 Dec 2020 19:20:37 GMT
EXPOSE 3000 3001 3002 3003
# Mon, 21 Dec 2020 19:20:37 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Mon, 21 Dec 2020 19:20:37 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:e50c3c9ef5a201a24959788dcbc7ebf88d95c63e132a4d7396ce541127afd88e`  
		Last Modified: Fri, 11 Dec 2020 02:15:43 GMT  
		Size: 22.5 MB (22527860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c6eff11a81dc19d983bcbcfdc570a3429283dcffe5c82931cb639f660241e0e`  
		Last Modified: Mon, 21 Dec 2020 19:21:41 GMT  
		Size: 53.7 MB (53745683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b0ddb6001e87822da4dc399acb472424c21358c741fc7af08579f46da582e4`  
		Last Modified: Mon, 21 Dec 2020 19:21:33 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38203c933a7274ad7b1b571e24d1ce29a684c08fd406f3e7ab1940f15022f93`  
		Last Modified: Mon, 21 Dec 2020 19:21:33 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:5.3.0.3`

```console
$ docker pull aerospike@sha256:8284a2c523bf9a74e306cde6e1cd7f836d1cd8f437cc62b56487125d8541aa70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.3.0.3` - linux; amd64

```console
$ docker pull aerospike@sha256:05893ce04c6e938fee4428b334abcf104a0cfcbf365a4b7274c743cc6e01eb4b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74705558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5fbc24c21b769ed55236b2519590e5624dad44b6ca063e271281d5068d6eb5`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:58 GMT
ADD file:f03e68a10b84e2342cfffbb8cdec1117c7f5e5d0dd004072e84efb62cfdf157c in / 
# Fri, 11 Dec 2020 02:08:58 GMT
CMD ["bash"]
# Mon, 21 Dec 2020 19:20:43 GMT
ENV AEROSPIKE_VERSION=5.3.0.3
# Mon, 21 Dec 2020 19:20:43 GMT
ENV AEROSPIKE_SHA256=a37fc7f70aec0976ae959b36a94ef7022e539e87f1abf20054e53742c40ed058
# Mon, 21 Dec 2020 19:21:05 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Mon, 21 Dec 2020 19:21:06 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Mon, 21 Dec 2020 19:21:06 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Mon, 21 Dec 2020 19:21:06 GMT
EXPOSE 3000 3001 3002 3003
# Mon, 21 Dec 2020 19:21:06 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Mon, 21 Dec 2020 19:21:07 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:e50c3c9ef5a201a24959788dcbc7ebf88d95c63e132a4d7396ce541127afd88e`  
		Last Modified: Fri, 11 Dec 2020 02:15:43 GMT  
		Size: 22.5 MB (22527860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b2b093203af722753fd0984eb7ca7c16450ffec4e458f65658210a6986fbed`  
		Last Modified: Mon, 21 Dec 2020 19:21:55 GMT  
		Size: 52.2 MB (52175646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79e09e28460370ed5b9a77659ec8cf9e466d31cf0b7c7b21309fd6fa9f127f4`  
		Last Modified: Mon, 21 Dec 2020 19:21:46 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846b391ceed552fc51fb95390519fcba68ca5425c862f7b427ae49f2b76746b7`  
		Last Modified: Mon, 21 Dec 2020 19:21:46 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:latest`

```console
$ docker pull aerospike@sha256:8284a2c523bf9a74e306cde6e1cd7f836d1cd8f437cc62b56487125d8541aa70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:latest` - linux; amd64

```console
$ docker pull aerospike@sha256:05893ce04c6e938fee4428b334abcf104a0cfcbf365a4b7274c743cc6e01eb4b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74705558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5fbc24c21b769ed55236b2519590e5624dad44b6ca063e271281d5068d6eb5`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:58 GMT
ADD file:f03e68a10b84e2342cfffbb8cdec1117c7f5e5d0dd004072e84efb62cfdf157c in / 
# Fri, 11 Dec 2020 02:08:58 GMT
CMD ["bash"]
# Mon, 21 Dec 2020 19:20:43 GMT
ENV AEROSPIKE_VERSION=5.3.0.3
# Mon, 21 Dec 2020 19:20:43 GMT
ENV AEROSPIKE_SHA256=a37fc7f70aec0976ae959b36a94ef7022e539e87f1abf20054e53742c40ed058
# Mon, 21 Dec 2020 19:21:05 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Mon, 21 Dec 2020 19:21:06 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Mon, 21 Dec 2020 19:21:06 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Mon, 21 Dec 2020 19:21:06 GMT
EXPOSE 3000 3001 3002 3003
# Mon, 21 Dec 2020 19:21:06 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Mon, 21 Dec 2020 19:21:07 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:e50c3c9ef5a201a24959788dcbc7ebf88d95c63e132a4d7396ce541127afd88e`  
		Last Modified: Fri, 11 Dec 2020 02:15:43 GMT  
		Size: 22.5 MB (22527860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b2b093203af722753fd0984eb7ca7c16450ffec4e458f65658210a6986fbed`  
		Last Modified: Mon, 21 Dec 2020 19:21:55 GMT  
		Size: 52.2 MB (52175646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79e09e28460370ed5b9a77659ec8cf9e466d31cf0b7c7b21309fd6fa9f127f4`  
		Last Modified: Mon, 21 Dec 2020 19:21:46 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846b391ceed552fc51fb95390519fcba68ca5425c862f7b427ae49f2b76746b7`  
		Last Modified: Mon, 21 Dec 2020 19:21:46 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
