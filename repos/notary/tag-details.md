<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `notary`

-	[`notary:server`](#notaryserver)
-	[`notary:server-0.7.0`](#notaryserver-070)
-	[`notary:signer`](#notarysigner)
-	[`notary:signer-0.7.0`](#notarysigner-070)

## `notary:server`

```console
$ docker pull notary@sha256:608cb19ca39574e864814bc93803377c0b80a62d4cec21f816fcfd231b52f96f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `notary:server` - linux; amd64

```console
$ docker pull notary@sha256:25c1e9902b24aae5d1896fefb12c9e9c4e251cc5354bfe4b6d5ac9af8f5ac2a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7957652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6e2132ffa74b527c2ca855206f142b7eff158eede414d29a2d4780deba40ec`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-server ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-server --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./server-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb7a9f71fb77cab089a6afa3b9f0312d3860ccdd693b8918edba3e976cfe4a9`  
		Last Modified: Wed, 09 Aug 2023 01:27:35 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9cb729c92ea79d82f432354b3486145b87240c401211b1edf50af69f9b6b54`  
		Last Modified: Wed, 09 Aug 2023 01:27:35 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc725f9de63eb8c57bff9ef8759bdf195d16c140509db456b9b9c4de0afb1d34`  
		Last Modified: Wed, 09 Aug 2023 01:27:35 GMT  
		Size: 5.1 MB (5147835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b51941863c3f63becac9c1a3d115ad7cee7f1a16fb6b620d35316111a07e5e5`  
		Last Modified: Wed, 09 Aug 2023 01:27:36 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b36e2706b0ef942da6fba2c0528192b65e450d55cfda45a7783480f2d00c469`  
		Last Modified: Wed, 09 Aug 2023 01:27:36 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:server` - unknown; unknown

```console
$ docker pull notary@sha256:396cb803ed04b2af189ba2658dbbaa8bdc50739a95242b3a9e3488a206a206bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 KB (131753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16ac33ca492a85b61dc13582d8140b21401ccda39cca1ea87784b3c9d3b3109`

```dockerfile
```

-	Layers:
	-	`sha256:2a0ad06c6ed45043042938d752e6271c238583c3513b0570e46417670b717e5d`  
		Last Modified: Wed, 09 Aug 2023 01:27:35 GMT  
		Size: 112.5 KB (112513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc895df850296e5cc26f5f6d002356f735ab23e140f82daa52e9eb13ecfad280`  
		Last Modified: Wed, 09 Aug 2023 01:27:35 GMT  
		Size: 19.2 KB (19240 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:server` - linux; arm variant v6

```console
$ docker pull notary@sha256:6e8bfe3906aa1d8df858fedb86df50c8929f340bec233eecb2b9fc1a3a1b372c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7511249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:092a594d3d7141d38477de785ff80987f9be2d185aaedcce3e0c3250f90730f9`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:321b24cc0fbd39caa2d7672a740d2cd2030ba99cab16f50c22db9955bd99350b in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-server ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-server --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./server-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:dffa980f71c953938bb194a457aa62e7f1885137331eef8bf7f9403c075f711c`  
		Last Modified: Mon, 07 Aug 2023 19:50:02 GMT  
		Size: 2.6 MB (2615553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253ae7f8eb52a8ea4fe35dad1a51da8e2507ed4a7de0e040345c7f1778fa3728`  
		Last Modified: Mon, 07 Aug 2023 22:58:38 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72255fa7488becd327879a87fb05f982b3f53af4b97cdb2194f25beea2d1b41e`  
		Last Modified: Mon, 07 Aug 2023 22:58:38 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d0e62fb7740d86658ba5c16a040fe749e2d555ba760003e42151ebb0693ce5`  
		Last Modified: Mon, 07 Aug 2023 22:58:39 GMT  
		Size: 4.9 MB (4893567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617b4a0f26a7a047066943504031862ddce8766b7d29f5e2b3ef46209605afaa`  
		Last Modified: Mon, 07 Aug 2023 22:58:38 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81a7366f32b9d9a19fb73ed36f1d2ba7151f7ca0d88269869654851ad496cac`  
		Last Modified: Mon, 07 Aug 2023 22:58:38 GMT  
		Size: 376.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:d147a2dd70b2bc88049efd0032dd9cc20e01aa0833db2bc1702b2775dab2baaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7444608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f672acd668849ed1cfdb5c5e3040dd835e50b024d9491c53c6136d9cddeaa3ee`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:cf85500a1f5b87a88587b279c8b8018eebeb3092f402b7e2cc4ad3873e078580 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-server ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-server --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./server-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:bdb2de7ba06c3a4e10b98f439a8c70afd63eee492c2ddc32342331a8e9ef4ff7`  
		Last Modified: Mon, 07 Aug 2023 19:40:08 GMT  
		Size: 2.7 MB (2708023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202c4dd0f102d31afdf745598c8b608887eb3b4142b5fbb8619d8b431ab3d348`  
		Last Modified: Mon, 07 Aug 2023 22:45:27 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565afe3e3634f553e5e4798c9171e212127f00b3c23c93faa1eb17c3027fad79`  
		Last Modified: Mon, 07 Aug 2023 22:45:27 GMT  
		Size: 118.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6128cc3d34da4edf1351e0397480921013481a869739484a9b6366c2a03448`  
		Last Modified: Mon, 07 Aug 2023 22:45:27 GMT  
		Size: 4.7 MB (4734458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73788bca9233077876bfb7ad08ab7e664745b8945cc9734482694a0be8bbd5e4`  
		Last Modified: Mon, 07 Aug 2023 22:45:28 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad868bcf088e64171900901ed63038b26bb0c717b90d360356dce16d10e14ee`  
		Last Modified: Mon, 07 Aug 2023 22:45:28 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:server` - unknown; unknown

```console
$ docker pull notary@sha256:7477d6f6d1f1ee16a7438db8a317f070ba5ee42856203c7e30e3d5fdb9d26831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 KB (131099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7670e90ab99336561b98da07281dd5b929f251c5a9410088a2513f4a97f77776`

```dockerfile
```

-	Layers:
	-	`sha256:7f2db81d358b5d674541354c82bea5d03e60fdaf2cbfdfdd1fc5270c719cf0dc`  
		Last Modified: Mon, 07 Aug 2023 22:45:26 GMT  
		Size: 112.5 KB (112508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb8d7756dfe0a4b3b1034a0bfef4ac485cd34a16982e7b522abd0eb9035008ce`  
		Last Modified: Mon, 07 Aug 2023 22:45:26 GMT  
		Size: 18.6 KB (18591 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:server` - linux; 386

```console
$ docker pull notary@sha256:200c9cc2c149ab6067ca7731def2577f967819bf3985b2e06f93f410c6dc255f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7763475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1aa537109a2eba4a85e319194e4de4c88348b109544fe4da77ea7dff474304e`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:c06b4f6991638e506d4d0a4d70c4a78ba30b971767802af4c6b837cdf59d4303 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-server ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-server --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./server-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:be0d19c155de823c6b37eaaba7cdec9085e8f1e39b1dd5982a19acb6c8c97cc5`  
		Last Modified: Mon, 07 Aug 2023 19:39:20 GMT  
		Size: 2.8 MB (2810553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c231aba312fc8b9cb8ca18c6e0c451685d9ea439576822cf44491b0db63626`  
		Last Modified: Wed, 09 Aug 2023 01:27:51 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3722d61e2e95eadc1eb50ae11c3271f07abc6aed04e9a545eca6dd9bc2b10619`  
		Last Modified: Wed, 09 Aug 2023 01:27:51 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae315b0c389520132048d5cfa817b30e84121504b2bbf6863e8df98e01fcc75`  
		Last Modified: Wed, 09 Aug 2023 01:27:51 GMT  
		Size: 5.0 MB (4950788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7623b1494b5d3a0ef5a78f9b324d3a228bac685f65a64ae0791d4a012edb27f1`  
		Last Modified: Wed, 09 Aug 2023 01:27:51 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0da033f619f1251d0658e23e9e10ddb77bc66101ce2de84621d36b3135b140f`  
		Last Modified: Wed, 09 Aug 2023 01:27:52 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:server` - unknown; unknown

```console
$ docker pull notary@sha256:6f4fae6afa7cfe418b902be1d93a81dfbe2e6b468788f90ea7c4cd211b213c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe73c6d0fb55b8c50b06fdd36661f333f73f2ba2c3f9707a0ed7283640ffa27a`

```dockerfile
```

-	Layers:
	-	`sha256:0ced58b11b722d777f6b5b6d7fcfd5a7001b703bb95faf8d396ae5b77b0c8c7d`  
		Last Modified: Wed, 09 Aug 2023 01:27:51 GMT  
		Size: 19.0 KB (18986 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:server` - linux; ppc64le

```console
$ docker pull notary@sha256:45ca8fd4de3a1b8c6981d7237f9158a14fc29ec22d2d67510f40fe775a2a8faf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7443614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af28e6b9b522a35047a4261ae895a906716441751c1a9176f9190c582373947`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:b30c2945bf4c873440b2e390c7120f16abe08ec41b10c2fb248b9b1a7ad223fa in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-server ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-server --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./server-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:cc1a557f8d111cc8c11359cd168abb441e150c9dc42a046349c5e51132461a47`  
		Last Modified: Mon, 07 Aug 2023 20:17:53 GMT  
		Size: 2.8 MB (2802326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4d9f67868be443e2c2f090de7caea30272fbfa297b89c353c3ad9a3047b1b6`  
		Last Modified: Tue, 08 Aug 2023 01:08:52 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a142ff761db1df086e666a3b69b35cd4106e93592f900cc3b76d2d76b1399f`  
		Last Modified: Tue, 08 Aug 2023 01:08:51 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23852e81f7d884e270dc9bda64a0a19667821e912203466850d3487407ab148e`  
		Last Modified: Tue, 08 Aug 2023 01:08:52 GMT  
		Size: 4.6 MB (4639154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5494c8e99bfc8addd3828ed280ef3c9c3217d35aeb79e08acda6ec04c1d59cd1`  
		Last Modified: Tue, 08 Aug 2023 01:08:53 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d6c9532ca0f0dab6d785d1823407632bb7512b524b8d12c75ccca39b02d357`  
		Last Modified: Tue, 08 Aug 2023 01:08:53 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:server` - unknown; unknown

```console
$ docker pull notary@sha256:d1fb1aad865534d7c9d3566b083fc8ddda2011f05cda2c1f324aca2610d4f74e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.7 KB (129658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06831e0701a211bf080e17fac7a7f847ff085bd6f78ab144fe54154ec8b1cd42`

```dockerfile
```

-	Layers:
	-	`sha256:6e489af8319856f95d152d089b630904d98de7ca0ec332cfb5ebe99d0c5d07c7`  
		Last Modified: Tue, 08 Aug 2023 01:08:52 GMT  
		Size: 111.0 KB (111037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4b40f82604a7b5b336f5c78d151441e55a091350857b2f2c23e9e31ca1ea655`  
		Last Modified: Tue, 08 Aug 2023 01:08:52 GMT  
		Size: 18.6 KB (18621 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:server` - linux; s390x

```console
$ docker pull notary@sha256:d1e72c424482060b7779d9776023874287d059644af495a94f9bf7d30493830f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7570354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5547bc15c32a972261ced143dc05c99cabc078586b07defc03eae161bf6cf804`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:39bfe995aa06bc953f4887751caefaa4576f3dfe63f0020b8989bb8b0a09c28f in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-server ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-server --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./server-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:e5761c1ed80af1ea48f655cdeb0fa9a89fe7d3903985d9ea08286e940a4f30dd`  
		Last Modified: Mon, 07 Aug 2023 19:42:55 GMT  
		Size: 2.6 MB (2591728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f55e3cbca2287bf936764f7cf3d3b0b4e12e954928cb0652b427c0f83cf162c`  
		Last Modified: Tue, 08 Aug 2023 05:26:46 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e593822092e94f68a1e55cc1042d360e1c590ab8447d859122cc25a9456787`  
		Last Modified: Tue, 08 Aug 2023 05:26:46 GMT  
		Size: 117.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf217811d8edc379710881aceac7ba3e7175bd8336398e8a11b3788234625b6`  
		Last Modified: Tue, 08 Aug 2023 05:26:46 GMT  
		Size: 5.0 MB (4976495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483c151497f6252ea96df4ac234160917d6911427d6798c993e6a9a427268439`  
		Last Modified: Tue, 08 Aug 2023 05:26:47 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b2097a71fe86b39696fea28da91125bc63c807b7bc6f41c05e9e0dc5d822c8`  
		Last Modified: Tue, 08 Aug 2023 05:26:47 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:server` - unknown; unknown

```console
$ docker pull notary@sha256:fb77e4dd3502ffc5c54c1cb0591edbed7380639afd707853add98178dd0dc275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 KB (129571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dec5c91ed119d8fb3bb1c8a96e4dafa5ea1dff3ef9b63cf0f8ae727054f21079`

```dockerfile
```

-	Layers:
	-	`sha256:972ad4fcfc8a5ed75d3268d0c7ea754f81e48e9497c5890c15174e715a0d8b8f`  
		Last Modified: Tue, 08 Aug 2023 05:26:46 GMT  
		Size: 111.0 KB (110986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3946524db89d6bde663b41e48a85762a20c6e1963750f78fc04b86adf78fef00`  
		Last Modified: Tue, 08 Aug 2023 05:26:46 GMT  
		Size: 18.6 KB (18585 bytes)  
		MIME: application/vnd.in-toto+json

## `notary:server-0.7.0`

```console
$ docker pull notary@sha256:608cb19ca39574e864814bc93803377c0b80a62d4cec21f816fcfd231b52f96f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `notary:server-0.7.0` - linux; amd64

```console
$ docker pull notary@sha256:25c1e9902b24aae5d1896fefb12c9e9c4e251cc5354bfe4b6d5ac9af8f5ac2a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7957652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6e2132ffa74b527c2ca855206f142b7eff158eede414d29a2d4780deba40ec`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-server ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-server --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./server-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb7a9f71fb77cab089a6afa3b9f0312d3860ccdd693b8918edba3e976cfe4a9`  
		Last Modified: Wed, 09 Aug 2023 01:27:35 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9cb729c92ea79d82f432354b3486145b87240c401211b1edf50af69f9b6b54`  
		Last Modified: Wed, 09 Aug 2023 01:27:35 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc725f9de63eb8c57bff9ef8759bdf195d16c140509db456b9b9c4de0afb1d34`  
		Last Modified: Wed, 09 Aug 2023 01:27:35 GMT  
		Size: 5.1 MB (5147835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b51941863c3f63becac9c1a3d115ad7cee7f1a16fb6b620d35316111a07e5e5`  
		Last Modified: Wed, 09 Aug 2023 01:27:36 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b36e2706b0ef942da6fba2c0528192b65e450d55cfda45a7783480f2d00c469`  
		Last Modified: Wed, 09 Aug 2023 01:27:36 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:server-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:396cb803ed04b2af189ba2658dbbaa8bdc50739a95242b3a9e3488a206a206bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 KB (131753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16ac33ca492a85b61dc13582d8140b21401ccda39cca1ea87784b3c9d3b3109`

```dockerfile
```

-	Layers:
	-	`sha256:2a0ad06c6ed45043042938d752e6271c238583c3513b0570e46417670b717e5d`  
		Last Modified: Wed, 09 Aug 2023 01:27:35 GMT  
		Size: 112.5 KB (112513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc895df850296e5cc26f5f6d002356f735ab23e140f82daa52e9eb13ecfad280`  
		Last Modified: Wed, 09 Aug 2023 01:27:35 GMT  
		Size: 19.2 KB (19240 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:server-0.7.0` - linux; arm variant v6

```console
$ docker pull notary@sha256:6e8bfe3906aa1d8df858fedb86df50c8929f340bec233eecb2b9fc1a3a1b372c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7511249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:092a594d3d7141d38477de785ff80987f9be2d185aaedcce3e0c3250f90730f9`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:321b24cc0fbd39caa2d7672a740d2cd2030ba99cab16f50c22db9955bd99350b in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-server ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-server --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./server-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:dffa980f71c953938bb194a457aa62e7f1885137331eef8bf7f9403c075f711c`  
		Last Modified: Mon, 07 Aug 2023 19:50:02 GMT  
		Size: 2.6 MB (2615553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253ae7f8eb52a8ea4fe35dad1a51da8e2507ed4a7de0e040345c7f1778fa3728`  
		Last Modified: Mon, 07 Aug 2023 22:58:38 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72255fa7488becd327879a87fb05f982b3f53af4b97cdb2194f25beea2d1b41e`  
		Last Modified: Mon, 07 Aug 2023 22:58:38 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d0e62fb7740d86658ba5c16a040fe749e2d555ba760003e42151ebb0693ce5`  
		Last Modified: Mon, 07 Aug 2023 22:58:39 GMT  
		Size: 4.9 MB (4893567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617b4a0f26a7a047066943504031862ddce8766b7d29f5e2b3ef46209605afaa`  
		Last Modified: Mon, 07 Aug 2023 22:58:38 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81a7366f32b9d9a19fb73ed36f1d2ba7151f7ca0d88269869654851ad496cac`  
		Last Modified: Mon, 07 Aug 2023 22:58:38 GMT  
		Size: 376.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.7.0` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:d147a2dd70b2bc88049efd0032dd9cc20e01aa0833db2bc1702b2775dab2baaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7444608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f672acd668849ed1cfdb5c5e3040dd835e50b024d9491c53c6136d9cddeaa3ee`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:cf85500a1f5b87a88587b279c8b8018eebeb3092f402b7e2cc4ad3873e078580 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-server ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-server --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./server-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:bdb2de7ba06c3a4e10b98f439a8c70afd63eee492c2ddc32342331a8e9ef4ff7`  
		Last Modified: Mon, 07 Aug 2023 19:40:08 GMT  
		Size: 2.7 MB (2708023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202c4dd0f102d31afdf745598c8b608887eb3b4142b5fbb8619d8b431ab3d348`  
		Last Modified: Mon, 07 Aug 2023 22:45:27 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565afe3e3634f553e5e4798c9171e212127f00b3c23c93faa1eb17c3027fad79`  
		Last Modified: Mon, 07 Aug 2023 22:45:27 GMT  
		Size: 118.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6128cc3d34da4edf1351e0397480921013481a869739484a9b6366c2a03448`  
		Last Modified: Mon, 07 Aug 2023 22:45:27 GMT  
		Size: 4.7 MB (4734458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73788bca9233077876bfb7ad08ab7e664745b8945cc9734482694a0be8bbd5e4`  
		Last Modified: Mon, 07 Aug 2023 22:45:28 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad868bcf088e64171900901ed63038b26bb0c717b90d360356dce16d10e14ee`  
		Last Modified: Mon, 07 Aug 2023 22:45:28 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:server-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:7477d6f6d1f1ee16a7438db8a317f070ba5ee42856203c7e30e3d5fdb9d26831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 KB (131099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7670e90ab99336561b98da07281dd5b929f251c5a9410088a2513f4a97f77776`

```dockerfile
```

-	Layers:
	-	`sha256:7f2db81d358b5d674541354c82bea5d03e60fdaf2cbfdfdd1fc5270c719cf0dc`  
		Last Modified: Mon, 07 Aug 2023 22:45:26 GMT  
		Size: 112.5 KB (112508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb8d7756dfe0a4b3b1034a0bfef4ac485cd34a16982e7b522abd0eb9035008ce`  
		Last Modified: Mon, 07 Aug 2023 22:45:26 GMT  
		Size: 18.6 KB (18591 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:server-0.7.0` - linux; 386

```console
$ docker pull notary@sha256:200c9cc2c149ab6067ca7731def2577f967819bf3985b2e06f93f410c6dc255f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7763475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1aa537109a2eba4a85e319194e4de4c88348b109544fe4da77ea7dff474304e`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:c06b4f6991638e506d4d0a4d70c4a78ba30b971767802af4c6b837cdf59d4303 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-server ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-server --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./server-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:be0d19c155de823c6b37eaaba7cdec9085e8f1e39b1dd5982a19acb6c8c97cc5`  
		Last Modified: Mon, 07 Aug 2023 19:39:20 GMT  
		Size: 2.8 MB (2810553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c231aba312fc8b9cb8ca18c6e0c451685d9ea439576822cf44491b0db63626`  
		Last Modified: Wed, 09 Aug 2023 01:27:51 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3722d61e2e95eadc1eb50ae11c3271f07abc6aed04e9a545eca6dd9bc2b10619`  
		Last Modified: Wed, 09 Aug 2023 01:27:51 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae315b0c389520132048d5cfa817b30e84121504b2bbf6863e8df98e01fcc75`  
		Last Modified: Wed, 09 Aug 2023 01:27:51 GMT  
		Size: 5.0 MB (4950788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7623b1494b5d3a0ef5a78f9b324d3a228bac685f65a64ae0791d4a012edb27f1`  
		Last Modified: Wed, 09 Aug 2023 01:27:51 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0da033f619f1251d0658e23e9e10ddb77bc66101ce2de84621d36b3135b140f`  
		Last Modified: Wed, 09 Aug 2023 01:27:52 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:server-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:6f4fae6afa7cfe418b902be1d93a81dfbe2e6b468788f90ea7c4cd211b213c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe73c6d0fb55b8c50b06fdd36661f333f73f2ba2c3f9707a0ed7283640ffa27a`

```dockerfile
```

-	Layers:
	-	`sha256:0ced58b11b722d777f6b5b6d7fcfd5a7001b703bb95faf8d396ae5b77b0c8c7d`  
		Last Modified: Wed, 09 Aug 2023 01:27:51 GMT  
		Size: 19.0 KB (18986 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:server-0.7.0` - linux; ppc64le

```console
$ docker pull notary@sha256:45ca8fd4de3a1b8c6981d7237f9158a14fc29ec22d2d67510f40fe775a2a8faf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7443614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af28e6b9b522a35047a4261ae895a906716441751c1a9176f9190c582373947`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:b30c2945bf4c873440b2e390c7120f16abe08ec41b10c2fb248b9b1a7ad223fa in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-server ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-server --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./server-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:cc1a557f8d111cc8c11359cd168abb441e150c9dc42a046349c5e51132461a47`  
		Last Modified: Mon, 07 Aug 2023 20:17:53 GMT  
		Size: 2.8 MB (2802326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4d9f67868be443e2c2f090de7caea30272fbfa297b89c353c3ad9a3047b1b6`  
		Last Modified: Tue, 08 Aug 2023 01:08:52 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a142ff761db1df086e666a3b69b35cd4106e93592f900cc3b76d2d76b1399f`  
		Last Modified: Tue, 08 Aug 2023 01:08:51 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23852e81f7d884e270dc9bda64a0a19667821e912203466850d3487407ab148e`  
		Last Modified: Tue, 08 Aug 2023 01:08:52 GMT  
		Size: 4.6 MB (4639154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5494c8e99bfc8addd3828ed280ef3c9c3217d35aeb79e08acda6ec04c1d59cd1`  
		Last Modified: Tue, 08 Aug 2023 01:08:53 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d6c9532ca0f0dab6d785d1823407632bb7512b524b8d12c75ccca39b02d357`  
		Last Modified: Tue, 08 Aug 2023 01:08:53 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:server-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:d1fb1aad865534d7c9d3566b083fc8ddda2011f05cda2c1f324aca2610d4f74e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.7 KB (129658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06831e0701a211bf080e17fac7a7f847ff085bd6f78ab144fe54154ec8b1cd42`

```dockerfile
```

-	Layers:
	-	`sha256:6e489af8319856f95d152d089b630904d98de7ca0ec332cfb5ebe99d0c5d07c7`  
		Last Modified: Tue, 08 Aug 2023 01:08:52 GMT  
		Size: 111.0 KB (111037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4b40f82604a7b5b336f5c78d151441e55a091350857b2f2c23e9e31ca1ea655`  
		Last Modified: Tue, 08 Aug 2023 01:08:52 GMT  
		Size: 18.6 KB (18621 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:server-0.7.0` - linux; s390x

```console
$ docker pull notary@sha256:d1e72c424482060b7779d9776023874287d059644af495a94f9bf7d30493830f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7570354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5547bc15c32a972261ced143dc05c99cabc078586b07defc03eae161bf6cf804`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:39bfe995aa06bc953f4887751caefaa4576f3dfe63f0020b8989bb8b0a09c28f in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-server ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-server --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./server-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:e5761c1ed80af1ea48f655cdeb0fa9a89fe7d3903985d9ea08286e940a4f30dd`  
		Last Modified: Mon, 07 Aug 2023 19:42:55 GMT  
		Size: 2.6 MB (2591728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f55e3cbca2287bf936764f7cf3d3b0b4e12e954928cb0652b427c0f83cf162c`  
		Last Modified: Tue, 08 Aug 2023 05:26:46 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e593822092e94f68a1e55cc1042d360e1c590ab8447d859122cc25a9456787`  
		Last Modified: Tue, 08 Aug 2023 05:26:46 GMT  
		Size: 117.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf217811d8edc379710881aceac7ba3e7175bd8336398e8a11b3788234625b6`  
		Last Modified: Tue, 08 Aug 2023 05:26:46 GMT  
		Size: 5.0 MB (4976495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483c151497f6252ea96df4ac234160917d6911427d6798c993e6a9a427268439`  
		Last Modified: Tue, 08 Aug 2023 05:26:47 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b2097a71fe86b39696fea28da91125bc63c807b7bc6f41c05e9e0dc5d822c8`  
		Last Modified: Tue, 08 Aug 2023 05:26:47 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:server-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:fb77e4dd3502ffc5c54c1cb0591edbed7380639afd707853add98178dd0dc275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 KB (129571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dec5c91ed119d8fb3bb1c8a96e4dafa5ea1dff3ef9b63cf0f8ae727054f21079`

```dockerfile
```

-	Layers:
	-	`sha256:972ad4fcfc8a5ed75d3268d0c7ea754f81e48e9497c5890c15174e715a0d8b8f`  
		Last Modified: Tue, 08 Aug 2023 05:26:46 GMT  
		Size: 111.0 KB (110986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3946524db89d6bde663b41e48a85762a20c6e1963750f78fc04b86adf78fef00`  
		Last Modified: Tue, 08 Aug 2023 05:26:46 GMT  
		Size: 18.6 KB (18585 bytes)  
		MIME: application/vnd.in-toto+json

## `notary:signer`

```console
$ docker pull notary@sha256:25a6df0c5a31b1fa7308d3162355ec82acf2a699d7187119a3d5e43caea30a86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `notary:signer` - linux; amd64

```console
$ docker pull notary@sha256:040eb3d8263ae51e2eae515270d60af57d9572d27f43fe0d8fe66dce8481a399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7572850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:133820e48f36d1b218f99f09963e3f0b8b7768b40f261e15176f3b67a8b46c50`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a5b0d3d73e0aad458a4701fbe7d1c9c05855820109107fa38c29e7f1d8988f`  
		Last Modified: Wed, 09 Aug 2023 01:27:40 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0718e9b7fb5da11be6b1b7b342bfddcfc195818b87b5eeb5a11b58fc701cb9c`  
		Last Modified: Wed, 09 Aug 2023 01:27:40 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007b8b4bca6cf0cdc1e3450c4f8125136d59adfef23b427a23b12ca71dfb1d88`  
		Last Modified: Wed, 09 Aug 2023 01:27:40 GMT  
		Size: 4.8 MB (4763097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151f421d0f558f0b21b409187f99be356cbe7222406b9590bc8bcb5482deff96`  
		Last Modified: Wed, 09 Aug 2023 01:27:40 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab80b2297f56dca5b843b06cf0dc11e86fedef3b962ca6d6783d850644e73647`  
		Last Modified: Wed, 09 Aug 2023 01:27:41 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer` - unknown; unknown

```console
$ docker pull notary@sha256:db30b6efa9a499de8bbf8e13b30c748193b6e07c92de049be4aabed8238acd7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 KB (125624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5750904a8c4c60a3f6f59a06ba54b26b65d6a6068a98ed56cd5bdcc316f60d`

```dockerfile
```

-	Layers:
	-	`sha256:ffac4743df0aa717f66518797c27711bc0a610818b6553cae7511a84ca224140`  
		Last Modified: Wed, 09 Aug 2023 01:27:40 GMT  
		Size: 106.4 KB (106368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43235a6b1d5c02ffa4f6272989680cbc42bfffa2a81d17a2d6c50e01dc31bdcc`  
		Last Modified: Wed, 09 Aug 2023 01:27:40 GMT  
		Size: 19.3 KB (19256 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:signer` - linux; arm variant v6

```console
$ docker pull notary@sha256:5fdb9009bee2a9102d0fd29a4113f4c29cc9b74d654186e4e13ffcecbc722e4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7143721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aec235975a04dc5580e5f759fa174a5efd4d835df2818c236805808532a5f9b`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:321b24cc0fbd39caa2d7672a740d2cd2030ba99cab16f50c22db9955bd99350b in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:dffa980f71c953938bb194a457aa62e7f1885137331eef8bf7f9403c075f711c`  
		Last Modified: Mon, 07 Aug 2023 19:50:02 GMT  
		Size: 2.6 MB (2615553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253ae7f8eb52a8ea4fe35dad1a51da8e2507ed4a7de0e040345c7f1778fa3728`  
		Last Modified: Mon, 07 Aug 2023 22:58:38 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe858dda9ac67d7da225bf0e7cbb97c3d8168347d4bdd73f887f4add26a7e7e3`  
		Last Modified: Mon, 07 Aug 2023 22:58:59 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbc8c04719ae3263711caaa86e777271ef591ecad80813f9fafeae903fd0db3`  
		Last Modified: Mon, 07 Aug 2023 22:59:00 GMT  
		Size: 4.5 MB (4526096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0fc61eff27830763478c3589a62d809f4e27a7f2767f8740c55c4f92be583c`  
		Last Modified: Mon, 07 Aug 2023 22:58:59 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609ae2997199f3151e09c1705027e568d72f65008e6466cc501661f3e76cd7ca`  
		Last Modified: Mon, 07 Aug 2023 22:58:59 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:d0b2157e191e4ba482b1840f736d0d5f8e03e69cd939e2997b53bf9bb70cb016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7103175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69eec41fd3d6cf59d8bb581a10497f7417bffab2b543059ee887a590df99b84`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:cf85500a1f5b87a88587b279c8b8018eebeb3092f402b7e2cc4ad3873e078580 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:bdb2de7ba06c3a4e10b98f439a8c70afd63eee492c2ddc32342331a8e9ef4ff7`  
		Last Modified: Mon, 07 Aug 2023 19:40:08 GMT  
		Size: 2.7 MB (2708023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202c4dd0f102d31afdf745598c8b608887eb3b4142b5fbb8619d8b431ab3d348`  
		Last Modified: Mon, 07 Aug 2023 22:45:27 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f88739c04bec4884bc40c7d216e4e9211441e2d033c5861f631bb0925b478fa`  
		Last Modified: Mon, 07 Aug 2023 22:45:46 GMT  
		Size: 118.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f13b4a5fcaf14870b0afd1801c5ea0380125660000fd5e65bc19c7ae8dee6d`  
		Last Modified: Mon, 07 Aug 2023 22:45:46 GMT  
		Size: 4.4 MB (4393084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b200dfa82abb58b4aa87e1cda3b731e8020c5ca1217d041b2c3c0284514c9c4`  
		Last Modified: Mon, 07 Aug 2023 22:45:46 GMT  
		Size: 356.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da7244fcfdb45e21dcac9ea3d397ec3d43317799fbc86f16ec39bc6827ade69`  
		Last Modified: Mon, 07 Aug 2023 22:45:46 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer` - unknown; unknown

```console
$ docker pull notary@sha256:6c3721c3e50f6202d878e10a2084ef28f9f3e205b64bf9549b7b5eb1bd2aa40f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 KB (124804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e1ccd32f74833463693ebc8f513b1e076841b47242ed0ff7481e1c3b010d1ac`

```dockerfile
```

-	Layers:
	-	`sha256:b3358f066f0c59b3ce8b89133689b71d9a03801c8e7aaf284eb6a30657fd6d0e`  
		Last Modified: Mon, 07 Aug 2023 22:45:46 GMT  
		Size: 106.4 KB (106363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63d590c84f36fc4d06f8d219aa0fd62cdc1c10edb805b91bee4729064b1aa73f`  
		Last Modified: Mon, 07 Aug 2023 22:45:46 GMT  
		Size: 18.4 KB (18441 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:signer` - linux; 386

```console
$ docker pull notary@sha256:cae566acd384c12acc56915a5e0e283f0152d349fd17bb67dd433fb3537bac5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7391648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc1b53618908ecfdb960d930c2febb9ba2a263827e05e7a3a9b1667451120a13`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:c06b4f6991638e506d4d0a4d70c4a78ba30b971767802af4c6b837cdf59d4303 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:be0d19c155de823c6b37eaaba7cdec9085e8f1e39b1dd5982a19acb6c8c97cc5`  
		Last Modified: Mon, 07 Aug 2023 19:39:20 GMT  
		Size: 2.8 MB (2810553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fa9de7917724356fc9e5ac0a36feaf4921e583aebcdf915c77b9e5fe049e34`  
		Last Modified: Wed, 09 Aug 2023 01:27:42 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ca1b5e04b1fc9f11a05435096a7f30af90cef32873e1e3d7ff57d5aa0515f9`  
		Last Modified: Wed, 09 Aug 2023 01:27:42 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbfbca84a1999316d9a6bc89a8b46d7b20b432addf17d144be762e4a7076309`  
		Last Modified: Wed, 09 Aug 2023 01:27:43 GMT  
		Size: 4.6 MB (4579026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759ef7dbd2a1a6c0af05d324ab96cb82d79201020e9c89d883d4967c3b006204`  
		Last Modified: Wed, 09 Aug 2023 01:27:43 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112eb3e886f111b07f002de740e51083cefd74d62bdc059ac1f288b3f6ae77f3`  
		Last Modified: Wed, 09 Aug 2023 01:27:43 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer` - unknown; unknown

```console
$ docker pull notary@sha256:b560387955bb1feb2878824ee2cbee4034ce43264f027d353c671fdbb7960bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a58af98b79aa31d01cec762b88008925cfea4720c6b682d774e4409f9bc2a80b`

```dockerfile
```

-	Layers:
	-	`sha256:c0e1b64cee3ec971d50c9c7068b68407f9fdad38b53027b4caa5b18204feed5c`  
		Last Modified: Wed, 09 Aug 2023 01:27:42 GMT  
		Size: 19.0 KB (19002 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:signer` - linux; ppc64le

```console
$ docker pull notary@sha256:8e2d7e9e0b6f610e145fe2763452f0fa6bf2753d2ea1fad370b3bcc10a0c4f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7101376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4371a66e28772fd7bd0f365e7c22523f8110639edde31c01d2e15b05b73380a9`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:b30c2945bf4c873440b2e390c7120f16abe08ec41b10c2fb248b9b1a7ad223fa in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:cc1a557f8d111cc8c11359cd168abb441e150c9dc42a046349c5e51132461a47`  
		Last Modified: Mon, 07 Aug 2023 20:17:53 GMT  
		Size: 2.8 MB (2802326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4d9f67868be443e2c2f090de7caea30272fbfa297b89c353c3ad9a3047b1b6`  
		Last Modified: Tue, 08 Aug 2023 01:08:52 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6bd11e750564a61a33996fb08fc38ada593f7823ecaccb23125be14e4bf09f`  
		Last Modified: Tue, 08 Aug 2023 01:39:25 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c573b997a055b49ebb28df708ccd35e322e96c34fbd6fe31b349be82ceb426`  
		Last Modified: Tue, 08 Aug 2023 01:39:26 GMT  
		Size: 4.3 MB (4296977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31213f0f3061baad77fce782c27b0f9752d96d5efb9d05256f12d3b867d6a009`  
		Last Modified: Tue, 08 Aug 2023 01:39:26 GMT  
		Size: 356.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05359a8b732c0eabd34a61042fbb4826c60251cd3227746cf8ac7ef7ff2f411d`  
		Last Modified: Tue, 08 Aug 2023 01:39:26 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer` - unknown; unknown

```console
$ docker pull notary@sha256:da86de469b4076950283f4ec3a37f5d629d66c28d1dcdd8fd568801777ed5d1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 KB (123360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa96a89b691cad5f90ca1b1126ae1461f287c21e227a070ba22012d6a0f5a362`

```dockerfile
```

-	Layers:
	-	`sha256:bb10678cdbed709be4f4c2adc53c78cdf5c5f8f8feb4d43440cd0519cbe32e5f`  
		Last Modified: Tue, 08 Aug 2023 01:39:25 GMT  
		Size: 104.9 KB (104890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7af8755352d387b3465e24338fea942f94faa6ee3972521e2c8defa2fe016633`  
		Last Modified: Tue, 08 Aug 2023 01:39:25 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:signer` - linux; s390x

```console
$ docker pull notary@sha256:319f21d2ddd35d20943a31dded0fad5d24a3afb0985abfa0a709c8e676a772f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7200499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421fdca38a4b1ebe2321e27db10001ec12a1597aa5b5f378a76b284e96d0513c`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:39bfe995aa06bc953f4887751caefaa4576f3dfe63f0020b8989bb8b0a09c28f in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:e5761c1ed80af1ea48f655cdeb0fa9a89fe7d3903985d9ea08286e940a4f30dd`  
		Last Modified: Mon, 07 Aug 2023 19:42:55 GMT  
		Size: 2.6 MB (2591728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f55e3cbca2287bf936764f7cf3d3b0b4e12e954928cb0652b427c0f83cf162c`  
		Last Modified: Tue, 08 Aug 2023 05:26:46 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0675d7212e30a1beebba53fe2bb273bb1b10a0a3bfecec0797d9f9f49f235635`  
		Last Modified: Tue, 08 Aug 2023 05:30:24 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e10cf9585fd55e6c66f374ba49ab100672415130008c82ab7e57f9e9546e044`  
		Last Modified: Tue, 08 Aug 2023 05:30:25 GMT  
		Size: 4.6 MB (4606700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950ca5e57e3b0a0e35bf3b1b98dc81ee770fef5cea6b1d28c9c3e3684817c80b`  
		Last Modified: Tue, 08 Aug 2023 05:30:24 GMT  
		Size: 357.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91afc82a44ac77e18bcdebfc2c102118f68cb968b983168e0eaada234ddf83e1`  
		Last Modified: Tue, 08 Aug 2023 05:30:24 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer` - unknown; unknown

```console
$ docker pull notary@sha256:6271446d12272feba6b979eddbfca08d906c11004b16c66b3d8562dffef4ca4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 KB (123267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51e10e3eb7477768c03f32c168686936654c4cecb6b0e4ecc216a0bb9a566e49`

```dockerfile
```

-	Layers:
	-	`sha256:ef528497f39c68399e33b89c2d85906594801be0d64aec598abbd7dcac60eba5`  
		Last Modified: Tue, 08 Aug 2023 05:30:24 GMT  
		Size: 104.8 KB (104833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8f3422f9679d5025f202fc44217a7fd91207439c2aac3aaa1815195eb15fa57`  
		Last Modified: Tue, 08 Aug 2023 05:30:24 GMT  
		Size: 18.4 KB (18434 bytes)  
		MIME: application/vnd.in-toto+json

## `notary:signer-0.7.0`

```console
$ docker pull notary@sha256:25a6df0c5a31b1fa7308d3162355ec82acf2a699d7187119a3d5e43caea30a86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `notary:signer-0.7.0` - linux; amd64

```console
$ docker pull notary@sha256:040eb3d8263ae51e2eae515270d60af57d9572d27f43fe0d8fe66dce8481a399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7572850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:133820e48f36d1b218f99f09963e3f0b8b7768b40f261e15176f3b67a8b46c50`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a5b0d3d73e0aad458a4701fbe7d1c9c05855820109107fa38c29e7f1d8988f`  
		Last Modified: Wed, 09 Aug 2023 01:27:40 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0718e9b7fb5da11be6b1b7b342bfddcfc195818b87b5eeb5a11b58fc701cb9c`  
		Last Modified: Wed, 09 Aug 2023 01:27:40 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007b8b4bca6cf0cdc1e3450c4f8125136d59adfef23b427a23b12ca71dfb1d88`  
		Last Modified: Wed, 09 Aug 2023 01:27:40 GMT  
		Size: 4.8 MB (4763097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151f421d0f558f0b21b409187f99be356cbe7222406b9590bc8bcb5482deff96`  
		Last Modified: Wed, 09 Aug 2023 01:27:40 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab80b2297f56dca5b843b06cf0dc11e86fedef3b962ca6d6783d850644e73647`  
		Last Modified: Wed, 09 Aug 2023 01:27:41 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:db30b6efa9a499de8bbf8e13b30c748193b6e07c92de049be4aabed8238acd7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 KB (125624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5750904a8c4c60a3f6f59a06ba54b26b65d6a6068a98ed56cd5bdcc316f60d`

```dockerfile
```

-	Layers:
	-	`sha256:ffac4743df0aa717f66518797c27711bc0a610818b6553cae7511a84ca224140`  
		Last Modified: Wed, 09 Aug 2023 01:27:40 GMT  
		Size: 106.4 KB (106368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43235a6b1d5c02ffa4f6272989680cbc42bfffa2a81d17a2d6c50e01dc31bdcc`  
		Last Modified: Wed, 09 Aug 2023 01:27:40 GMT  
		Size: 19.3 KB (19256 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:signer-0.7.0` - linux; arm variant v6

```console
$ docker pull notary@sha256:5fdb9009bee2a9102d0fd29a4113f4c29cc9b74d654186e4e13ffcecbc722e4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7143721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aec235975a04dc5580e5f759fa174a5efd4d835df2818c236805808532a5f9b`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:321b24cc0fbd39caa2d7672a740d2cd2030ba99cab16f50c22db9955bd99350b in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:dffa980f71c953938bb194a457aa62e7f1885137331eef8bf7f9403c075f711c`  
		Last Modified: Mon, 07 Aug 2023 19:50:02 GMT  
		Size: 2.6 MB (2615553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253ae7f8eb52a8ea4fe35dad1a51da8e2507ed4a7de0e040345c7f1778fa3728`  
		Last Modified: Mon, 07 Aug 2023 22:58:38 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe858dda9ac67d7da225bf0e7cbb97c3d8168347d4bdd73f887f4add26a7e7e3`  
		Last Modified: Mon, 07 Aug 2023 22:58:59 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbc8c04719ae3263711caaa86e777271ef591ecad80813f9fafeae903fd0db3`  
		Last Modified: Mon, 07 Aug 2023 22:59:00 GMT  
		Size: 4.5 MB (4526096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0fc61eff27830763478c3589a62d809f4e27a7f2767f8740c55c4f92be583c`  
		Last Modified: Mon, 07 Aug 2023 22:58:59 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609ae2997199f3151e09c1705027e568d72f65008e6466cc501661f3e76cd7ca`  
		Last Modified: Mon, 07 Aug 2023 22:58:59 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:d0b2157e191e4ba482b1840f736d0d5f8e03e69cd939e2997b53bf9bb70cb016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7103175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69eec41fd3d6cf59d8bb581a10497f7417bffab2b543059ee887a590df99b84`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:cf85500a1f5b87a88587b279c8b8018eebeb3092f402b7e2cc4ad3873e078580 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:bdb2de7ba06c3a4e10b98f439a8c70afd63eee492c2ddc32342331a8e9ef4ff7`  
		Last Modified: Mon, 07 Aug 2023 19:40:08 GMT  
		Size: 2.7 MB (2708023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202c4dd0f102d31afdf745598c8b608887eb3b4142b5fbb8619d8b431ab3d348`  
		Last Modified: Mon, 07 Aug 2023 22:45:27 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f88739c04bec4884bc40c7d216e4e9211441e2d033c5861f631bb0925b478fa`  
		Last Modified: Mon, 07 Aug 2023 22:45:46 GMT  
		Size: 118.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f13b4a5fcaf14870b0afd1801c5ea0380125660000fd5e65bc19c7ae8dee6d`  
		Last Modified: Mon, 07 Aug 2023 22:45:46 GMT  
		Size: 4.4 MB (4393084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b200dfa82abb58b4aa87e1cda3b731e8020c5ca1217d041b2c3c0284514c9c4`  
		Last Modified: Mon, 07 Aug 2023 22:45:46 GMT  
		Size: 356.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da7244fcfdb45e21dcac9ea3d397ec3d43317799fbc86f16ec39bc6827ade69`  
		Last Modified: Mon, 07 Aug 2023 22:45:46 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:6c3721c3e50f6202d878e10a2084ef28f9f3e205b64bf9549b7b5eb1bd2aa40f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 KB (124804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e1ccd32f74833463693ebc8f513b1e076841b47242ed0ff7481e1c3b010d1ac`

```dockerfile
```

-	Layers:
	-	`sha256:b3358f066f0c59b3ce8b89133689b71d9a03801c8e7aaf284eb6a30657fd6d0e`  
		Last Modified: Mon, 07 Aug 2023 22:45:46 GMT  
		Size: 106.4 KB (106363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63d590c84f36fc4d06f8d219aa0fd62cdc1c10edb805b91bee4729064b1aa73f`  
		Last Modified: Mon, 07 Aug 2023 22:45:46 GMT  
		Size: 18.4 KB (18441 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:signer-0.7.0` - linux; 386

```console
$ docker pull notary@sha256:cae566acd384c12acc56915a5e0e283f0152d349fd17bb67dd433fb3537bac5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7391648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc1b53618908ecfdb960d930c2febb9ba2a263827e05e7a3a9b1667451120a13`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:c06b4f6991638e506d4d0a4d70c4a78ba30b971767802af4c6b837cdf59d4303 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:be0d19c155de823c6b37eaaba7cdec9085e8f1e39b1dd5982a19acb6c8c97cc5`  
		Last Modified: Mon, 07 Aug 2023 19:39:20 GMT  
		Size: 2.8 MB (2810553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fa9de7917724356fc9e5ac0a36feaf4921e583aebcdf915c77b9e5fe049e34`  
		Last Modified: Wed, 09 Aug 2023 01:27:42 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ca1b5e04b1fc9f11a05435096a7f30af90cef32873e1e3d7ff57d5aa0515f9`  
		Last Modified: Wed, 09 Aug 2023 01:27:42 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbfbca84a1999316d9a6bc89a8b46d7b20b432addf17d144be762e4a7076309`  
		Last Modified: Wed, 09 Aug 2023 01:27:43 GMT  
		Size: 4.6 MB (4579026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759ef7dbd2a1a6c0af05d324ab96cb82d79201020e9c89d883d4967c3b006204`  
		Last Modified: Wed, 09 Aug 2023 01:27:43 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112eb3e886f111b07f002de740e51083cefd74d62bdc059ac1f288b3f6ae77f3`  
		Last Modified: Wed, 09 Aug 2023 01:27:43 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:b560387955bb1feb2878824ee2cbee4034ce43264f027d353c671fdbb7960bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a58af98b79aa31d01cec762b88008925cfea4720c6b682d774e4409f9bc2a80b`

```dockerfile
```

-	Layers:
	-	`sha256:c0e1b64cee3ec971d50c9c7068b68407f9fdad38b53027b4caa5b18204feed5c`  
		Last Modified: Wed, 09 Aug 2023 01:27:42 GMT  
		Size: 19.0 KB (19002 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:signer-0.7.0` - linux; ppc64le

```console
$ docker pull notary@sha256:8e2d7e9e0b6f610e145fe2763452f0fa6bf2753d2ea1fad370b3bcc10a0c4f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7101376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4371a66e28772fd7bd0f365e7c22523f8110639edde31c01d2e15b05b73380a9`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:b30c2945bf4c873440b2e390c7120f16abe08ec41b10c2fb248b9b1a7ad223fa in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:cc1a557f8d111cc8c11359cd168abb441e150c9dc42a046349c5e51132461a47`  
		Last Modified: Mon, 07 Aug 2023 20:17:53 GMT  
		Size: 2.8 MB (2802326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4d9f67868be443e2c2f090de7caea30272fbfa297b89c353c3ad9a3047b1b6`  
		Last Modified: Tue, 08 Aug 2023 01:08:52 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6bd11e750564a61a33996fb08fc38ada593f7823ecaccb23125be14e4bf09f`  
		Last Modified: Tue, 08 Aug 2023 01:39:25 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c573b997a055b49ebb28df708ccd35e322e96c34fbd6fe31b349be82ceb426`  
		Last Modified: Tue, 08 Aug 2023 01:39:26 GMT  
		Size: 4.3 MB (4296977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31213f0f3061baad77fce782c27b0f9752d96d5efb9d05256f12d3b867d6a009`  
		Last Modified: Tue, 08 Aug 2023 01:39:26 GMT  
		Size: 356.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05359a8b732c0eabd34a61042fbb4826c60251cd3227746cf8ac7ef7ff2f411d`  
		Last Modified: Tue, 08 Aug 2023 01:39:26 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:da86de469b4076950283f4ec3a37f5d629d66c28d1dcdd8fd568801777ed5d1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 KB (123360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa96a89b691cad5f90ca1b1126ae1461f287c21e227a070ba22012d6a0f5a362`

```dockerfile
```

-	Layers:
	-	`sha256:bb10678cdbed709be4f4c2adc53c78cdf5c5f8f8feb4d43440cd0519cbe32e5f`  
		Last Modified: Tue, 08 Aug 2023 01:39:25 GMT  
		Size: 104.9 KB (104890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7af8755352d387b3465e24338fea942f94faa6ee3972521e2c8defa2fe016633`  
		Last Modified: Tue, 08 Aug 2023 01:39:25 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:signer-0.7.0` - linux; s390x

```console
$ docker pull notary@sha256:319f21d2ddd35d20943a31dded0fad5d24a3afb0985abfa0a709c8e676a772f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7200499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421fdca38a4b1ebe2321e27db10001ec12a1597aa5b5f378a76b284e96d0513c`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:39bfe995aa06bc953f4887751caefaa4576f3dfe63f0020b8989bb8b0a09c28f in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:e5761c1ed80af1ea48f655cdeb0fa9a89fe7d3903985d9ea08286e940a4f30dd`  
		Last Modified: Mon, 07 Aug 2023 19:42:55 GMT  
		Size: 2.6 MB (2591728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f55e3cbca2287bf936764f7cf3d3b0b4e12e954928cb0652b427c0f83cf162c`  
		Last Modified: Tue, 08 Aug 2023 05:26:46 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0675d7212e30a1beebba53fe2bb273bb1b10a0a3bfecec0797d9f9f49f235635`  
		Last Modified: Tue, 08 Aug 2023 05:30:24 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e10cf9585fd55e6c66f374ba49ab100672415130008c82ab7e57f9e9546e044`  
		Last Modified: Tue, 08 Aug 2023 05:30:25 GMT  
		Size: 4.6 MB (4606700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950ca5e57e3b0a0e35bf3b1b98dc81ee770fef5cea6b1d28c9c3e3684817c80b`  
		Last Modified: Tue, 08 Aug 2023 05:30:24 GMT  
		Size: 357.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91afc82a44ac77e18bcdebfc2c102118f68cb968b983168e0eaada234ddf83e1`  
		Last Modified: Tue, 08 Aug 2023 05:30:24 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:6271446d12272feba6b979eddbfca08d906c11004b16c66b3d8562dffef4ca4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 KB (123267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51e10e3eb7477768c03f32c168686936654c4cecb6b0e4ecc216a0bb9a566e49`

```dockerfile
```

-	Layers:
	-	`sha256:ef528497f39c68399e33b89c2d85906594801be0d64aec598abbd7dcac60eba5`  
		Last Modified: Tue, 08 Aug 2023 05:30:24 GMT  
		Size: 104.8 KB (104833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8f3422f9679d5025f202fc44217a7fd91207439c2aac3aaa1815195eb15fa57`  
		Last Modified: Tue, 08 Aug 2023 05:30:24 GMT  
		Size: 18.4 KB (18434 bytes)  
		MIME: application/vnd.in-toto+json
