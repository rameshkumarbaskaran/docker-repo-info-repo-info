## `notary:signer-0.6.1-2`

```console
$ docker pull notary@sha256:107c3695bdcf4f0816d2134babf1ee8fb073c6c2f2194e7f4f9ecd0a719e5973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `notary:signer-0.6.1-2` - linux; amd64

```console
$ docker pull notary@sha256:5a597b68b254bf6117fbb7b0985cb52a0c0e86d17f91a3e2f68b82a5e60ed6c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7690874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1b0c0a51a29722cfcf864a2d028631e0853919ca0fc059237081377ad639a0`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--help"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:46 GMT
ADD file:a2ef39a587aac85256b55bee81f17d73aaa7154b2a32a31527c7803fb889f2e7 in / 
# Tue, 29 Mar 2022 00:19:46 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 15:56:36 GMT
ENV TAG=v0.6.1
# Tue, 29 Mar 2022 15:56:36 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Tue, 29 Mar 2022 15:56:55 GMT
ENV INSTALLDIR=/notary/signer
# Tue, 29 Mar 2022 15:56:56 GMT
EXPOSE 4444
# Tue, 29 Mar 2022 15:56:56 GMT
EXPOSE 7899
# Tue, 29 Mar 2022 15:56:56 GMT
WORKDIR /notary/signer
# Tue, 29 Mar 2022 15:57:10 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --help
# Tue, 29 Mar 2022 15:57:10 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Tue, 29 Mar 2022 15:57:10 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Tue, 29 Mar 2022 15:57:11 GMT
RUN adduser -D -H -g "" notary
# Tue, 29 Mar 2022 15:57:11 GMT
USER notary
# Tue, 29 Mar 2022 15:57:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Tue, 29 Mar 2022 15:57:11 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 29 Mar 2022 15:57:11 GMT
CMD ["notary-signer" "--help"]
```

-	Layers:
	-	`sha256:b9c05db88786fd3c89b78787631257301391f898c03ba50553b556630046a741`  
		Last Modified: Tue, 29 Mar 2022 00:20:43 GMT  
		Size: 2.8 MB (2819223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb1082d1643807ceaeb8e590f3432e78d20f6f87149b4b38ea6990bce6a906f`  
		Last Modified: Tue, 29 Mar 2022 15:57:33 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b54f98c8f2aaa0488352c699dc96fbe5687447f43efe4f1e38e3bbc65fd3f4b`  
		Last Modified: Tue, 29 Mar 2022 15:57:34 GMT  
		Size: 4.9 MB (4869596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc364a837c60fc420eaa9f49d15469346627cbed5c2a05c01288d87976ee4233`  
		Last Modified: Tue, 29 Mar 2022 15:57:33 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a7dffcbe64d230591ae8b8763c1ab40e881c5a3d02554bcd52c3e8a6fedf63`  
		Last Modified: Tue, 29 Mar 2022 15:57:33 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7005a3d5fd6b1e09b7b2ef641c2e305005d980afab194064bf4f42963325eb04`  
		Last Modified: Tue, 29 Mar 2022 15:57:33 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.6.1-2` - linux; arm variant v6

```console
$ docker pull notary@sha256:d1631ce42d7d46f07ac750643100dc17dc17377fb2b0a2e21068bbb716731a9c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7182333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f0120661b76e9d5a482d47dcffc5546d01455ae2458c46befada9e3f2fcf08a`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--help"]`

```dockerfile
# Mon, 04 Apr 2022 23:50:07 GMT
ADD file:9e96de1fefc4e9efba26e76103eca5f1495f00a66a8d8207d493fa9eabed19c0 in / 
# Mon, 04 Apr 2022 23:50:07 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:41:44 GMT
ENV TAG=v0.6.1
# Tue, 05 Apr 2022 06:41:45 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Tue, 05 Apr 2022 06:42:25 GMT
ENV INSTALLDIR=/notary/signer
# Tue, 05 Apr 2022 06:42:25 GMT
EXPOSE 4444
# Tue, 05 Apr 2022 06:42:26 GMT
EXPOSE 7899
# Tue, 05 Apr 2022 06:42:26 GMT
WORKDIR /notary/signer
# Tue, 05 Apr 2022 06:42:49 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --help
# Tue, 05 Apr 2022 06:42:50 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Tue, 05 Apr 2022 06:42:50 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Tue, 05 Apr 2022 06:42:52 GMT
RUN adduser -D -H -g "" notary
# Tue, 05 Apr 2022 06:42:52 GMT
USER notary
# Tue, 05 Apr 2022 06:42:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Tue, 05 Apr 2022 06:42:53 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 05 Apr 2022 06:42:53 GMT
CMD ["notary-signer" "--help"]
```

-	Layers:
	-	`sha256:83a39d5693a8029bb5246b7d72205357bcd5d8306489b586abf44bc8659dfc1e`  
		Last Modified: Mon, 04 Apr 2022 23:51:58 GMT  
		Size: 2.6 MB (2625144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a6edf6e31f19499935c3a76441187fcd92466739f87b8ea2583089574efa13`  
		Last Modified: Tue, 05 Apr 2022 06:43:37 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b3a89b1d6bec2d87129fa631facb69d2cefd43a3bdd7953ee43fd5490c87a5`  
		Last Modified: Tue, 05 Apr 2022 06:43:40 GMT  
		Size: 4.6 MB (4555132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d676f849034fec3a503bafc9bc46ab26e65a6910f1cdc7bbfbff56e607614ab`  
		Last Modified: Tue, 05 Apr 2022 06:43:37 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59df2725d042919c5b6b9846a0750838d7ca1f5fcfa3664a91ed3aa598fbc99`  
		Last Modified: Tue, 05 Apr 2022 06:43:37 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a9357ddb4523a1181e8ce7cb7dd6ba669ae79bededc06ef673085779140af3`  
		Last Modified: Tue, 05 Apr 2022 06:43:37 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.6.1-2` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:5dbf103c67811b30038b3b8dfdbbae4583755f2273a6f11df29f89601b4c3a3e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7178687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02eb0ad8e2cbe3ea5fb8f00624eb2c54b9df96819474aa54fb6570dbfd92626e`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--help"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:46 GMT
ADD file:535e6f58c2cf7520c1824c8a290dc38c5519485470ed49587748a27c0113d586 in / 
# Mon, 04 Apr 2022 23:39:46 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:20:06 GMT
ENV TAG=v0.6.1
# Tue, 05 Apr 2022 04:20:07 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Tue, 05 Apr 2022 04:20:37 GMT
ENV INSTALLDIR=/notary/signer
# Tue, 05 Apr 2022 04:20:38 GMT
EXPOSE 4444
# Tue, 05 Apr 2022 04:20:39 GMT
EXPOSE 7899
# Tue, 05 Apr 2022 04:20:40 GMT
WORKDIR /notary/signer
# Tue, 05 Apr 2022 04:20:50 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --help
# Tue, 05 Apr 2022 04:20:52 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Tue, 05 Apr 2022 04:20:53 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Tue, 05 Apr 2022 04:20:53 GMT
RUN adduser -D -H -g "" notary
# Tue, 05 Apr 2022 04:20:54 GMT
USER notary
# Tue, 05 Apr 2022 04:20:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Tue, 05 Apr 2022 04:20:56 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 05 Apr 2022 04:20:57 GMT
CMD ["notary-signer" "--help"]
```

-	Layers:
	-	`sha256:edd30f0f17040c7b292e0960fa771cf3ea45f994d7a2577a14fe02ae7ce727e9`  
		Last Modified: Mon, 04 Apr 2022 23:40:51 GMT  
		Size: 2.7 MB (2720895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6469eb955e2ff78803a49c305daee9f8c7d822f4dad3ef5e7a038762c5481ef6`  
		Last Modified: Tue, 05 Apr 2022 04:21:27 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d6490184b518304c9183e97b397c747c44b61d6f7fbbff25b4cb9a085a65e6`  
		Last Modified: Tue, 05 Apr 2022 04:21:27 GMT  
		Size: 4.5 MB (4455769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b93c98b085b6c25682339ea64ff49350b11739eaa962cf834feebf8af0e113`  
		Last Modified: Tue, 05 Apr 2022 04:21:27 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abecf4b5d027264415cd1c595cace4c7b11fd6c3ef56d1b5ba8403194af017fa`  
		Last Modified: Tue, 05 Apr 2022 04:21:27 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d88c446898ad5ead0c9dbb7ffe0f3e84bc4cd0106185a42fb36d14ad28c2be`  
		Last Modified: Tue, 05 Apr 2022 04:21:27 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.6.1-2` - linux; 386

```console
$ docker pull notary@sha256:c517416d0b0dbc3c15ffaf46105076e75637a3b09a480093871692adb85e808e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213048bd3ff08817186da1bc64b37e2e3bcfc0ba88265511ea161de9575b070b`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--help"]`

```dockerfile
# Mon, 04 Apr 2022 23:38:38 GMT
ADD file:caa278dc5cc6257518d542227fef491a89b0b4a7fc4dcb87632c2b786b65752a in / 
# Mon, 04 Apr 2022 23:38:38 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:16:38 GMT
ENV TAG=v0.6.1
# Tue, 05 Apr 2022 04:16:39 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Tue, 05 Apr 2022 04:17:09 GMT
ENV INSTALLDIR=/notary/signer
# Tue, 05 Apr 2022 04:17:10 GMT
EXPOSE 4444
# Tue, 05 Apr 2022 04:17:11 GMT
EXPOSE 7899
# Tue, 05 Apr 2022 04:17:12 GMT
WORKDIR /notary/signer
# Tue, 05 Apr 2022 04:17:24 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --help
# Tue, 05 Apr 2022 04:17:26 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Tue, 05 Apr 2022 04:17:27 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Tue, 05 Apr 2022 04:17:27 GMT
RUN adduser -D -H -g "" notary
# Tue, 05 Apr 2022 04:17:28 GMT
USER notary
# Tue, 05 Apr 2022 04:17:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Tue, 05 Apr 2022 04:17:30 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 05 Apr 2022 04:17:31 GMT
CMD ["notary-signer" "--help"]
```

-	Layers:
	-	`sha256:54c95c2f58283907ca735a3fe8d3ac4a49a63dc20092eb6fddd7bad2429e3f67`  
		Last Modified: Mon, 04 Apr 2022 23:39:46 GMT  
		Size: 2.8 MB (2820530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200ef45146319efcdecd60d517a8c61a2089c481a8449dcce89a92d1f04fc978`  
		Last Modified: Tue, 05 Apr 2022 04:18:01 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b0bfadc04bb02930de67b428075c382c95951ce913e2ddd7e8462bf02c18b6`  
		Last Modified: Tue, 05 Apr 2022 04:18:02 GMT  
		Size: 4.6 MB (4613397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a7a5dd0a2be99efa7a91689ab5526eea77055eb0de94e8d7a176728d183126`  
		Last Modified: Tue, 05 Apr 2022 04:18:01 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af15ea7412390861f7d24856cf33145bfd8880cc705b75818e4192cdcf807fb1`  
		Last Modified: Tue, 05 Apr 2022 04:18:01 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8fa97a166eed333075e1b99395c5888757006665f8eda4991a90a1637160b1`  
		Last Modified: Tue, 05 Apr 2022 04:18:01 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.6.1-2` - linux; ppc64le

```console
$ docker pull notary@sha256:28d32bbc4575f6f5b205f3c8d731c9c7fe4f5d18539add28757e9da27d57e65c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7154680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1b5007de5cc8d26eacefb2bbd7fc47b0d52ad52826d8183409a33bc26f9aec`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--help"]`

```dockerfile
# Tue, 29 Mar 2022 00:17:21 GMT
ADD file:0f301305d95e2e1e0580ec71f76edab57a1c18ed0adba5d09708b587ec19e622 in / 
# Tue, 29 Mar 2022 00:17:25 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 12:40:53 GMT
ENV TAG=v0.6.1
# Tue, 29 Mar 2022 12:40:54 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Tue, 29 Mar 2022 12:42:06 GMT
ENV INSTALLDIR=/notary/signer
# Tue, 29 Mar 2022 12:42:09 GMT
EXPOSE 4444
# Tue, 29 Mar 2022 12:42:12 GMT
EXPOSE 7899
# Tue, 29 Mar 2022 12:42:15 GMT
WORKDIR /notary/signer
# Tue, 29 Mar 2022 12:42:39 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --help
# Tue, 29 Mar 2022 12:42:40 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Tue, 29 Mar 2022 12:42:42 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Tue, 29 Mar 2022 12:42:50 GMT
RUN adduser -D -H -g "" notary
# Tue, 29 Mar 2022 12:42:59 GMT
USER notary
# Tue, 29 Mar 2022 12:43:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Tue, 29 Mar 2022 12:43:09 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 29 Mar 2022 12:43:13 GMT
CMD ["notary-signer" "--help"]
```

-	Layers:
	-	`sha256:77fcf2c0cc10658b5d6b4e43a75682b8bebbdc2e47895412dd1241c0422b8368`  
		Last Modified: Tue, 29 Mar 2022 00:18:56 GMT  
		Size: 2.8 MB (2814846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cacff4a4ed250261b3768bbfc9708d3da1b5331717d25f86c4c0928e2609079`  
		Last Modified: Tue, 29 Mar 2022 12:43:53 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222b02a3c69a5071e2847e33f670374acb913d4475da9ba50a6783ba1d451b25`  
		Last Modified: Tue, 29 Mar 2022 12:43:54 GMT  
		Size: 4.3 MB (4337776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295ab1754665b939a567857c6fbcf38d773ba83562ac53546e1e3246c54cd41a`  
		Last Modified: Tue, 29 Mar 2022 12:43:53 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542bb77cdd69cc247f93a9cdef415bbd42df299d501c84c773cb89c00c8d133c`  
		Last Modified: Tue, 29 Mar 2022 12:43:53 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7634254911f718d0571952c1c88cdbcf08b66ce4a7266e150a10dda53d468bed`  
		Last Modified: Tue, 29 Mar 2022 12:43:53 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.6.1-2` - linux; s390x

```console
$ docker pull notary@sha256:84879e97cc7abfa76e42bd92d5d987f618dcf1679091c9b6e2922e53afd0f70d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7313763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74ab04d2464b2a7b73bde2a36faa51916a3790e99232336d1ee332a76cae7f1e`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--help"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:55 GMT
ADD file:0f7653032bb9c65a5643cc31ad93fca7bd018ca0466a2d1c4ccadc5db00ad0f0 in / 
# Mon, 04 Apr 2022 23:41:55 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:09:32 GMT
ENV TAG=v0.6.1
# Tue, 05 Apr 2022 04:09:32 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Tue, 05 Apr 2022 04:09:53 GMT
ENV INSTALLDIR=/notary/signer
# Tue, 05 Apr 2022 04:09:53 GMT
EXPOSE 4444
# Tue, 05 Apr 2022 04:09:54 GMT
EXPOSE 7899
# Tue, 05 Apr 2022 04:09:54 GMT
WORKDIR /notary/signer
# Tue, 05 Apr 2022 04:10:04 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --help
# Tue, 05 Apr 2022 04:10:05 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Tue, 05 Apr 2022 04:10:05 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Tue, 05 Apr 2022 04:10:06 GMT
RUN adduser -D -H -g "" notary
# Tue, 05 Apr 2022 04:10:06 GMT
USER notary
# Tue, 05 Apr 2022 04:10:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Tue, 05 Apr 2022 04:10:06 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 05 Apr 2022 04:10:06 GMT
CMD ["notary-signer" "--help"]
```

-	Layers:
	-	`sha256:22b3eb8fdd3cabd13718400a1a4d1e75330e6e512d556cdd902359adeb0b014a`  
		Last Modified: Mon, 04 Apr 2022 23:42:54 GMT  
		Size: 2.6 MB (2605058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5cfceb0623aa4b77376a2b0943c3f6ad639bb23399311c58f149db56acb6d1`  
		Last Modified: Tue, 05 Apr 2022 04:10:31 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a23bb6474155371d7265c465752a84b037ab18d0b42c89829b8f7882da58f0`  
		Last Modified: Tue, 05 Apr 2022 04:10:32 GMT  
		Size: 4.7 MB (4706646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d732b0ce88d1b86635ede17c577fd772ea20c726d4fce09af29d5c1946abeea`  
		Last Modified: Tue, 05 Apr 2022 04:10:31 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd809709510a90d3548f93ff9a1cdc757565859ef825247e106c24c0755277aa`  
		Last Modified: Tue, 05 Apr 2022 04:10:31 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a18a490d4f9aec625e87d72f9df174b123b33a2197cae2d329bc4835baed09`  
		Last Modified: Tue, 05 Apr 2022 04:10:31 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
