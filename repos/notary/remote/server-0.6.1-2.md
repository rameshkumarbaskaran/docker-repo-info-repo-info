## `notary:server-0.6.1-2`

```console
$ docker pull notary@sha256:128f0f6fbce2d7a41c5345047e0ccb115c3d208911d54c91f71133e5bdfe3302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `notary:server-0.6.1-2` - linux; amd64

```console
$ docker pull notary@sha256:d535dadc7d2d8841dda325c81f2e9c6086c8cbfa7efce29a1b1374cdfde5716b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8217094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd331b6bf58d626685ea779170d7068842d45a0e235255438d0ae2419e4f75e`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--help"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 05:00:28 GMT
ENV TAG=v0.6.1
# Sat, 13 Nov 2021 05:00:28 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Sat, 13 Nov 2021 05:00:29 GMT
ENV INSTALLDIR=/notary/server
# Sat, 13 Nov 2021 05:00:29 GMT
EXPOSE 4443
# Sat, 13 Nov 2021 05:00:29 GMT
WORKDIR /notary/server
# Sat, 13 Nov 2021 05:00:48 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --help
# Sat, 13 Nov 2021 05:00:48 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Sat, 13 Nov 2021 05:00:48 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Sat, 13 Nov 2021 05:00:49 GMT
RUN adduser -D -H -g "" notary
# Sat, 13 Nov 2021 05:00:49 GMT
USER notary
# Sat, 13 Nov 2021 05:00:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Sat, 13 Nov 2021 05:00:50 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 13 Nov 2021 05:00:50 GMT
CMD ["notary-server" "--help"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a682a6397a941af9449bcacf0def7e602e8a083237c295435ab7f23319bf48ce`  
		Last Modified: Sat, 13 Nov 2021 05:01:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad293d2af1d9f6d59d05e2faac555e23b03b1dd1ab3e2c670fe4134f0f7e0c4`  
		Last Modified: Sat, 13 Nov 2021 05:01:48 GMT  
		Size: 5.4 MB (5392552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:395e36133ceb3a874bc5b9a4544c62968dae233d5ef9767e7523e0083f70158b`  
		Last Modified: Sat, 13 Nov 2021 05:01:47 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f24c53beaf929d6ad7befec6e6a1c9dedd27ef1bf4efd358c09be8d9d05241`  
		Last Modified: Sat, 13 Nov 2021 05:01:47 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769e1c22d7bf557580730448a2f6588d03eeba36c36fc3555f89645382384123`  
		Last Modified: Sat, 13 Nov 2021 05:01:47 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.6.1-2` - linux; arm variant v6

```console
$ docker pull notary@sha256:3d50a0803150a8c0d0fec2bd5086d810f0af6bcf73650dbbef5295eb1a157c71
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7679222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4004f00af6cb1567ffc64f047d7a11ff705bf46304107e0ca7e44732eda43bfd`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--help"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 03:01:40 GMT
ENV TAG=v0.6.1
# Sat, 13 Nov 2021 03:01:41 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Sat, 13 Nov 2021 03:01:41 GMT
ENV INSTALLDIR=/notary/server
# Sat, 13 Nov 2021 03:01:41 GMT
EXPOSE 4443
# Sat, 13 Nov 2021 03:01:42 GMT
WORKDIR /notary/server
# Sat, 13 Nov 2021 03:02:05 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --help
# Sat, 13 Nov 2021 03:02:05 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Sat, 13 Nov 2021 03:02:06 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Sat, 13 Nov 2021 03:02:07 GMT
RUN adduser -D -H -g "" notary
# Sat, 13 Nov 2021 03:02:08 GMT
USER notary
# Sat, 13 Nov 2021 03:02:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Sat, 13 Nov 2021 03:02:09 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 13 Nov 2021 03:02:09 GMT
CMD ["notary-server" "--help"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8812f75a7ee365f4ae9d8cd8673e885beec24150580e3cc6e44abd612cc4f8b`  
		Last Modified: Sat, 13 Nov 2021 03:03:19 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a5e56551da19d648d8658fa7f2f9ea44949a90049cecbd310c6c837c71fd05`  
		Last Modified: Sat, 13 Nov 2021 03:03:22 GMT  
		Size: 5.0 MB (5043759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc759be07b4dbb74b22d6a253450e4ff415f447cb9095751ce6f9b79274161e`  
		Last Modified: Sat, 13 Nov 2021 03:03:19 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626ed4e5bd3e8e40ced4f1cbf45ff9c155753fc3cc586c4ccdd7a3e416a34011`  
		Last Modified: Sat, 13 Nov 2021 03:03:19 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167ae3a1506d283b95e6ed34ed69a3345f50edbeb4380daa876e2bcb3e9135b8`  
		Last Modified: Sat, 13 Nov 2021 03:03:19 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.6.1-2` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:d058307a78633e4174d099f514df79346330a16b65e66a2bcbc379bb9aebe3a4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7661057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211ff0cf0466d36bd9d0821396297d9a04d95012678e1d45f4e236b1a9c18c50`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--help"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 00:13:38 GMT
ENV TAG=v0.6.1
# Sat, 13 Nov 2021 00:13:39 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Sat, 13 Nov 2021 00:13:40 GMT
ENV INSTALLDIR=/notary/server
# Sat, 13 Nov 2021 00:13:41 GMT
EXPOSE 4443
# Sat, 13 Nov 2021 00:13:42 GMT
WORKDIR /notary/server
# Sat, 13 Nov 2021 00:13:56 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --help
# Sat, 13 Nov 2021 00:13:58 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Sat, 13 Nov 2021 00:13:59 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Sat, 13 Nov 2021 00:13:59 GMT
RUN adduser -D -H -g "" notary
# Sat, 13 Nov 2021 00:14:00 GMT
USER notary
# Sat, 13 Nov 2021 00:14:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Sat, 13 Nov 2021 00:14:02 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 13 Nov 2021 00:14:03 GMT
CMD ["notary-server" "--help"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5b871c3959ef05d38d452bf8f6b740ec4dd926fe08ebb5f0768bb34b849e0f`  
		Last Modified: Sat, 13 Nov 2021 00:14:53 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ffaaeba98ef041f585bd32bec6651174bc246de87abb1a5d8735b8feb82af34`  
		Last Modified: Sat, 13 Nov 2021 00:14:54 GMT  
		Size: 4.9 MB (4939333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce603624efa4750d223cca7ddeddce867dd69b49e8ea51239c729ec607aac79`  
		Last Modified: Sat, 13 Nov 2021 00:14:53 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb556b8eb36fef7fb085be5678af95f78d8e6569281e4e5fe2faf028efcce02`  
		Last Modified: Sat, 13 Nov 2021 00:14:53 GMT  
		Size: 377.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ebd9966df2aa85787057ee1da91e8cd549d165d9b4745d50dacfc94db2e95f8`  
		Last Modified: Sat, 13 Nov 2021 00:14:53 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.6.1-2` - linux; 386

```console
$ docker pull notary@sha256:5f6c46b7d93cda49c33d61ae20a23ce8a10f44ef972b626c3f4151b085d2ca9f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7933457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20c10c9a0fd758ec0f35a2b2fe9bd991e817e22fcf66a21714a16cb33bd34530`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--help"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 04:13:15 GMT
ENV TAG=v0.6.1
# Sat, 13 Nov 2021 04:13:15 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Sat, 13 Nov 2021 04:13:16 GMT
ENV INSTALLDIR=/notary/server
# Sat, 13 Nov 2021 04:13:16 GMT
EXPOSE 4443
# Sat, 13 Nov 2021 04:13:16 GMT
WORKDIR /notary/server
# Sat, 13 Nov 2021 04:13:38 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --help
# Sat, 13 Nov 2021 04:13:38 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Sat, 13 Nov 2021 04:13:39 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Sat, 13 Nov 2021 04:13:39 GMT
RUN adduser -D -H -g "" notary
# Sat, 13 Nov 2021 04:13:40 GMT
USER notary
# Sat, 13 Nov 2021 04:13:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Sat, 13 Nov 2021 04:13:40 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 13 Nov 2021 04:13:40 GMT
CMD ["notary-server" "--help"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946423cdb165b5d7db7b5c37a6cbce6122a28c0037a7302d5083683d713471f2`  
		Last Modified: Sat, 13 Nov 2021 04:14:48 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4766aa546a7cb2aac16fa3dc25c82a356d12188fab6ee4e819961254daa3b7f0`  
		Last Modified: Sat, 13 Nov 2021 04:14:50 GMT  
		Size: 5.1 MB (5102528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eda60881b52a0109fa0c2f91eed00b2c46c3211007c29411d5f3ff3f578e728`  
		Last Modified: Sat, 13 Nov 2021 04:14:48 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0225c8939ee1b563213fe8a1a11e288f6e88316755a4042f3c23e19a0c85d938`  
		Last Modified: Sat, 13 Nov 2021 04:14:48 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b486712b1e88e555c008e6cdec9d8b4412d6a05be1c2fb0946e9608b6a4ef532`  
		Last Modified: Sat, 13 Nov 2021 04:14:48 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.6.1-2` - linux; ppc64le

```console
$ docker pull notary@sha256:591133743c62baefe42c3ca0caf5344e1b6fe85f1b639d7430a8023b5e5e2eec
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7631526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:463c8b5fbe4605f4a54cdae771e88ca43ff191f34c3a36c9b9650da4a638795a`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--help"]`

```dockerfile
# Fri, 12 Nov 2021 21:18:25 GMT
ADD file:f7216323de17450e653f77c86d2c1e2e8ec01e1133e93f29c515761b3e9d8f7d in / 
# Fri, 12 Nov 2021 21:18:28 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 02:54:59 GMT
ENV TAG=v0.6.1
# Sat, 13 Nov 2021 02:55:04 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Sat, 13 Nov 2021 02:55:08 GMT
ENV INSTALLDIR=/notary/server
# Sat, 13 Nov 2021 02:55:12 GMT
EXPOSE 4443
# Sat, 13 Nov 2021 02:55:16 GMT
WORKDIR /notary/server
# Sat, 13 Nov 2021 02:55:48 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --help
# Sat, 13 Nov 2021 02:55:49 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Sat, 13 Nov 2021 02:55:52 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Sat, 13 Nov 2021 02:56:07 GMT
RUN adduser -D -H -g "" notary
# Sat, 13 Nov 2021 02:56:09 GMT
USER notary
# Sat, 13 Nov 2021 02:56:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Sat, 13 Nov 2021 02:56:24 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 13 Nov 2021 02:56:30 GMT
CMD ["notary-server" "--help"]
```

-	Layers:
	-	`sha256:6729720a3e6b58511df148134bb67d786ad90f9fce1c02ba5bbfd31f33055fbe`  
		Last Modified: Fri, 12 Nov 2021 21:19:49 GMT  
		Size: 2.8 MB (2820517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7720c64aa431e9e025cf75fea965ee8b140a4ea0b9bd71c0f9e681b00cac62e6`  
		Last Modified: Sat, 13 Nov 2021 02:58:59 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bddcbbe020016693346cc418b7a4397900e146f84f9549f1c0a1b0abbd8f289`  
		Last Modified: Sat, 13 Nov 2021 02:59:01 GMT  
		Size: 4.8 MB (4808882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973381dc92e0c8d03acbebcc8f335bc832397ae1da44b9d3c1252c23ec3866cf`  
		Last Modified: Sat, 13 Nov 2021 02:59:00 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b56fbb03e78fca78e3474eb528898dab1d68b4ae7a7907fa2fa0d06fa56d1a14`  
		Last Modified: Sat, 13 Nov 2021 02:59:00 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f6fd46529589e707f125abff69536c2cb6c3704a1bb959c488d4370bc0bfdd`  
		Last Modified: Sat, 13 Nov 2021 02:58:59 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.6.1-2` - linux; s390x

```console
$ docker pull notary@sha256:6c43379addb89d560e7cab01d84855b22bd2c82e5cc2e36801f14838c700c279
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7825095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b18dc5db474643b19fdf62273306c35c1c45ff86f4b82d08c468f41e646f5f6`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--help"]`

```dockerfile
# Fri, 12 Nov 2021 16:41:44 GMT
ADD file:637f327c9b07758709ef7dbc42eb472c888d221acde89b1c3775553864334d5c in / 
# Fri, 12 Nov 2021 16:41:44 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 19:28:05 GMT
ENV TAG=v0.6.1
# Fri, 12 Nov 2021 19:28:05 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Fri, 12 Nov 2021 19:28:05 GMT
ENV INSTALLDIR=/notary/server
# Fri, 12 Nov 2021 19:28:05 GMT
EXPOSE 4443
# Fri, 12 Nov 2021 19:28:05 GMT
WORKDIR /notary/server
# Fri, 12 Nov 2021 19:28:17 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --help
# Fri, 12 Nov 2021 19:28:17 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Fri, 12 Nov 2021 19:28:17 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Fri, 12 Nov 2021 19:28:18 GMT
RUN adduser -D -H -g "" notary
# Fri, 12 Nov 2021 19:28:18 GMT
USER notary
# Fri, 12 Nov 2021 19:28:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Fri, 12 Nov 2021 19:28:18 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 12 Nov 2021 19:28:18 GMT
CMD ["notary-server" "--help"]
```

-	Layers:
	-	`sha256:b872f056719bde6e6722091afb2a3376d720c69c142b91ac352050080dd79615`  
		Last Modified: Fri, 12 Nov 2021 16:42:54 GMT  
		Size: 2.6 MB (2611155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f678c2054f7f61ec9de39904e129a2cdf5fc3d5426a7baabba2759476f19e7`  
		Last Modified: Fri, 12 Nov 2021 19:28:55 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56fdd4ef13b2fa79ee53546c4ea6f6818eb1734907894e05ea859c2dbfb980a`  
		Last Modified: Fri, 12 Nov 2021 19:28:55 GMT  
		Size: 5.2 MB (5211824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b738a8c0c4be5e7dfd345c86d78a0d2d197ca1b75fce8c9c2f0f1d33a38b4e8`  
		Last Modified: Fri, 12 Nov 2021 19:28:55 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71170955a75304f163bcc48c4dbe43164ee6f1a17c33a38f711459b475b96a1b`  
		Last Modified: Fri, 12 Nov 2021 19:28:55 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8145397afd5cfbb2a1082fddeaf7f0f58ed97c7017183595e5391fe76c7c55e`  
		Last Modified: Fri, 12 Nov 2021 19:28:55 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
