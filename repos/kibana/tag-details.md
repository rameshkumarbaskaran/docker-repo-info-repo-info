<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:6.8.23`](#kibana6823)
-	[`kibana:7.17.6`](#kibana7176)
-	[`kibana:8.4.2`](#kibana842)

## `kibana:6.8.23`

```console
$ docker pull kibana@sha256:dd123d133fa7e995f83eef23df6aad30c589711e6171fee8db63097a7706eae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kibana:6.8.23` - linux; amd64

```console
$ docker pull kibana@sha256:adb468810c34ccc141f01ea79135d5a2f48d09890ecd08ce59ec94444f0a09f1
```

-	Docker Version: 20.10.10
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.8 MB (325750637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e174261beaec7ef8b8fc7e3df6b62b87e442f3451d408e7fe4525b151a061ebd`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Thu, 06 Jan 2022 22:40:29 GMT
EXPOSE 5601
# Thu, 06 Jan 2022 22:41:30 GMT
RUN yum update -y && yum install -y fontconfig freetype && yum clean all
# Thu, 06 Jan 2022 22:42:25 GMT
COPY --chown=1000:0dir:91d1ac171c4ceb98ce1764191b4bde36072fa18167199a2214eb559670a34b06 in /usr/share/kibana 
# Thu, 06 Jan 2022 22:42:28 GMT
WORKDIR /usr/share/kibana
# Thu, 06 Jan 2022 22:42:29 GMT
RUN ln -s /usr/share/kibana /opt/kibana
# Thu, 06 Jan 2022 22:42:30 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 06 Jan 2022 22:42:30 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jan 2022 22:42:31 GMT
COPY --chown=1000:0file:60b6181f28c99b362092ea6139b6d4112ddd0bef32d52563c33b26bdc2b51318 in /usr/share/kibana/config/kibana.yml 
# Thu, 06 Jan 2022 22:42:31 GMT
COPY --chown=1000:0file:7d472d1939e23e2f10e7c5fd1e9166eefd646214aa0d8a1c09d92af71c9cbd87 in /usr/local/bin/ 
# Thu, 06 Jan 2022 22:42:34 GMT
RUN chmod g+ws /usr/share/kibana && find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \;
# Thu, 06 Jan 2022 22:42:39 GMT
RUN groupadd --gid 1000 kibana && useradd --uid 1000 --gid 1000 --home-dir /usr/share/kibana --no-create-home kibana
# Thu, 06 Jan 2022 22:42:39 GMT
USER kibana
# Thu, 06 Jan 2022 22:42:40 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.label-schema.name=kibana org.label-schema.version=6.8.23 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.license=Elastic License license=Elastic License
# Thu, 06 Jan 2022 22:42:41 GMT
CMD ["/usr/local/bin/kibana-docker"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842e4249e10492c4ab35d3e76f93cad922781f7d61752e1b4b3ca25636b5c56f`  
		Last Modified: Thu, 13 Jan 2022 16:11:43 GMT  
		Size: 61.0 MB (61010271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f4609300d658bf52b006741f5590abdf93d8d575e0ddf04ce5be28e82b50a4`  
		Last Modified: Thu, 13 Jan 2022 16:11:58 GMT  
		Size: 188.6 MB (188638449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:784cf3007996898653e12b85f6cf71597349b95377a60e1c57d40aaf682ddc3e`  
		Last Modified: Thu, 13 Jan 2022 16:11:32 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e291dafdd6a7112a1b18f88f42cbef2225094f58f18d2f364d0d34006b69e1`  
		Last Modified: Thu, 13 Jan 2022 16:11:30 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c90f666fc9fbd62181b8b51f391386e0a1a137451605b6f0a105171abe51380`  
		Last Modified: Thu, 13 Jan 2022 16:11:29 GMT  
		Size: 2.3 KB (2264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8abc3a9f73c2948571140a610a8c9f79b87c33bcbfdf320cd0f6e5d9fbe944`  
		Last Modified: Thu, 13 Jan 2022 16:11:29 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73634fb3f49af52529a1b025a3cebf50531fdbcbdb3876b7b00908dfe9dc0a85`  
		Last Modified: Thu, 13 Jan 2022 16:11:29 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kibana:7.17.6`

```console
$ docker pull kibana@sha256:ae5a501355903443b6cc7ff4a3af2dd76ba73f986d0612014b8370cd04bb6da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kibana:7.17.6` - linux; amd64

```console
$ docker pull kibana@sha256:a031b02cd029ce22abed498362f4ebbcd63cc8fc7bc364e95de7ceeb5eb1dfb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325453183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4239c3f5bd3d17a8a64cde246ea36e3329effe834ac38e3151f9279ec4fff004`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Mon, 22 Aug 2022 11:31:20 GMT
RUN EXPOSE map[5601/tcp:{}]
# Mon, 22 Aug 2022 11:31:20 GMT
RUN RUN /bin/sh -c for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Mon, 22 Aug 2022 11:31:21 GMT
RUN RUN /bin/sh -c set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Mon, 22 Aug 2022 11:31:21 GMT
RUN RUN /bin/sh -c mkdir /usr/share/fonts/local # buildkit
# Mon, 22 Aug 2022 11:31:22 GMT
RUN RUN /bin/sh -c curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Mon, 22 Aug 2022 11:31:23 GMT
RUN RUN /bin/sh -c echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Mon, 22 Aug 2022 11:31:23 GMT
RUN RUN /bin/sh -c fc-cache -v # buildkit
# Mon, 22 Aug 2022 11:32:25 GMT
RUN COPY /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 22 Aug 2022 11:32:25 GMT
RUN WORKDIR /usr/share/kibana
# Mon, 22 Aug 2022 11:32:25 GMT
RUN RUN /bin/sh -c ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 22 Aug 2022 11:32:25 GMT
RUN ENV ELASTIC_CONTAINER=true
# Mon, 22 Aug 2022 11:32:25 GMT
RUN ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Aug 2022 11:32:26 GMT
RUN COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 22 Aug 2022 11:32:26 GMT
RUN COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 22 Aug 2022 11:32:26 GMT
RUN RUN /bin/sh -c chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 22 Aug 2022 11:32:27 GMT
RUN RUN /bin/sh -c find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 22 Aug 2022 11:32:27 GMT
RUN RUN /bin/sh -c groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 22 Aug 2022 11:32:27 GMT
RUN LABEL org.label-schema.build-date=2022-08-22T11:05:33.075Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=d2647b053b769d4517fbb14ce37765808a1b6e0c org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.6 org.opencontainers.image.created=2022-08-22T11:05:33.075Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=d2647b053b769d4517fbb14ce37765808a1b6e0c org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.6
# Mon, 22 Aug 2022 11:32:27 GMT
RUN ENTRYPOINT ["/bin/tini" "--"]
# Mon, 22 Aug 2022 11:32:27 GMT
RUN CMD ["/usr/local/bin/kibana-docker"]
# Mon, 22 Aug 2022 11:32:27 GMT
RUN USER kibana
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4909e7eae242ddcd04ea4cac57905cde860307c129f881473a17640f26c77c22`  
		Last Modified: Wed, 24 Aug 2022 23:34:31 GMT  
		Size: 11.4 MB (11402602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe40d6fb24c0886259a755e922a95303529eb029e1832db71f8a14982cfba201`  
		Last Modified: Wed, 24 Aug 2022 23:34:29 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcaf4a9c0882e6eb369888122a32f1f3ff9c9c17fe4d43d5115afcd3be4d69b`  
		Last Modified: Wed, 24 Aug 2022 23:34:27 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:338bcf0d330658b4a5060ae46689eb526ad90811fe9fe3a5dad5f423052b025c`  
		Last Modified: Wed, 24 Aug 2022 23:34:28 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af5505a20feb5f0627a99c2f926ba87c2c8de93c16ad5ce60b2fb05fde4e38e`  
		Last Modified: Wed, 24 Aug 2022 23:34:27 GMT  
		Size: 5.3 KB (5288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe77eb249d6ffdbb9ace2b8c472e6601e48fa6eae4b6c3e6ab4a52560ff4d4d0`  
		Last Modified: Wed, 24 Aug 2022 23:34:58 GMT  
		Size: 268.8 MB (268805804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25728b71e5a44fc7a4e2eded91557b5d50399f103c7d69bb69c4d711242bc7b`  
		Last Modified: Wed, 24 Aug 2022 23:34:26 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35830107ab914645b77f72703837b4845d46e2ea9e789ecd0e2a785aff4715f1`  
		Last Modified: Wed, 24 Aug 2022 23:34:24 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1209f693487452a4793e8fcab07dd4e8d085bd70ba07bc66e042cf4ad7be65`  
		Last Modified: Wed, 24 Aug 2022 23:34:24 GMT  
		Size: 4.5 KB (4509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb27ec66f047fd0c1c30851d2089ce1dedb11fc081f75efd80c5a1026a583a9`  
		Last Modified: Wed, 24 Aug 2022 23:34:24 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6216454c4b6e809c3de959f46e320085ee49f81831ffbf88f3dacd31f32d1da1`  
		Last Modified: Wed, 24 Aug 2022 23:34:24 GMT  
		Size: 189.4 KB (189390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9baec0471caba7ed8badff4bb66852efdf363c69411b328a0e2cf26ea0b1971d`  
		Last Modified: Wed, 24 Aug 2022 23:34:24 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kibana:7.17.6` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:009a1aac9f56bd44888ab033a9f7c59845aefa182ca764877ab45009a25fc5f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.5 MB (338517103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10b0941d8c060d54a324a9dcb750eedc6f6e5fe7d247160e6dffd84d924ff77c`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Mon, 22 Aug 2022 11:34:32 GMT
RUN EXPOSE map[5601/tcp:{}]
# Mon, 22 Aug 2022 11:34:32 GMT
RUN RUN /bin/sh -c for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Mon, 22 Aug 2022 11:34:34 GMT
RUN RUN /bin/sh -c set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Mon, 22 Aug 2022 11:34:34 GMT
RUN RUN /bin/sh -c mkdir /usr/share/fonts/local # buildkit
# Mon, 22 Aug 2022 11:34:38 GMT
RUN RUN /bin/sh -c curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Mon, 22 Aug 2022 11:34:38 GMT
RUN RUN /bin/sh -c echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Mon, 22 Aug 2022 11:34:39 GMT
RUN RUN /bin/sh -c fc-cache -v # buildkit
# Mon, 22 Aug 2022 11:35:40 GMT
RUN COPY /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 22 Aug 2022 11:35:40 GMT
RUN WORKDIR /usr/share/kibana
# Mon, 22 Aug 2022 11:35:41 GMT
RUN RUN /bin/sh -c ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 22 Aug 2022 11:35:41 GMT
RUN ENV ELASTIC_CONTAINER=true
# Mon, 22 Aug 2022 11:35:41 GMT
RUN ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Aug 2022 11:35:41 GMT
RUN COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 22 Aug 2022 11:35:41 GMT
RUN COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 22 Aug 2022 11:35:41 GMT
RUN RUN /bin/sh -c chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 22 Aug 2022 11:35:42 GMT
RUN RUN /bin/sh -c find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 22 Aug 2022 11:35:43 GMT
RUN RUN /bin/sh -c groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 22 Aug 2022 11:35:43 GMT
RUN LABEL org.label-schema.build-date=2022-08-22T11:05:33.075Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=d2647b053b769d4517fbb14ce37765808a1b6e0c org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.6 org.opencontainers.image.created=2022-08-22T11:05:33.075Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=d2647b053b769d4517fbb14ce37765808a1b6e0c org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.6
# Mon, 22 Aug 2022 11:35:43 GMT
RUN ENTRYPOINT ["/bin/tini" "--"]
# Mon, 22 Aug 2022 11:35:43 GMT
RUN CMD ["/usr/local/bin/kibana-docker"]
# Mon, 22 Aug 2022 11:35:43 GMT
RUN USER kibana
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd40621629c438532eea92191837d0b33bf9a9723296a3ba24bc5d2c65f5206b`  
		Last Modified: Thu, 25 Aug 2022 02:10:43 GMT  
		Size: 11.2 MB (11235723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffa1dada9fbb499bbaee1ea95ea74e7d3d22d7b0083708ea9b238c47ed9e67e`  
		Last Modified: Thu, 25 Aug 2022 02:10:41 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47665c1ab65b80afa553144f99db53f5674e6944231ff774bf86edfb5d48fadf`  
		Last Modified: Thu, 25 Aug 2022 02:10:39 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d302b8066a42a7de4b005648be9cfa2f9fbed4fedd4231d6b4390f6fc01c93f1`  
		Last Modified: Thu, 25 Aug 2022 02:10:40 GMT  
		Size: 16.5 MB (16460486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2f75aefff3d84203de2b23fb7c8d77eb2ae9317ee0cf9b939f7e658f6a0e98`  
		Last Modified: Thu, 25 Aug 2022 02:10:38 GMT  
		Size: 5.3 KB (5295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f5af82b89cea04c1b92ca87f916b546dd42a2c8a09e25016575601be6fbf12`  
		Last Modified: Thu, 25 Aug 2022 02:11:14 GMT  
		Size: 283.4 MB (283423810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a1ca11cb812a2cecfbffd7bcab0ee97dff1b936273aa486ff0627afabaa6a9`  
		Last Modified: Thu, 25 Aug 2022 02:10:38 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be289adf6ffa9e50dd4e9a9e1d04f0ce3f3ad3f9163dfd549c025458750faa0`  
		Last Modified: Thu, 25 Aug 2022 02:10:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983daadcd4e22eb300b6d99c7087d1c6f00d10a3e9965a02d5d870427e9f98da`  
		Last Modified: Thu, 25 Aug 2022 02:10:36 GMT  
		Size: 4.5 KB (4508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43daa7054f14326442b8e1880957a36ad9255b3cd0cfc2d12198b14f0e7af20`  
		Last Modified: Thu, 25 Aug 2022 02:10:36 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e57cde9f2bfc25283f648cae139da69a696537aa26288a3ea8f34b0b82e23f4`  
		Last Modified: Thu, 25 Aug 2022 02:10:36 GMT  
		Size: 183.4 KB (183396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c001dea654d707e36e6a5180ad98399546b091c076ad6e5dbdc93e67cb13ba`  
		Last Modified: Thu, 25 Aug 2022 02:10:36 GMT  
		Size: 1.8 KB (1826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kibana:8.4.2`

```console
$ docker pull kibana@sha256:8117be633ad6c81a49edbbf08ced1c816b06cbd3de6f37f4bfbc6a981b3b9271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kibana:8.4.2` - linux; amd64

```console
$ docker pull kibana@sha256:65fe04abaec63b4aee3dd0459f2d6c2d0611aa805794fc18f2571cc732afead6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.6 MB (341582023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27aaced3f6e886f76dcc8fa985a4dbf805eb215f09fa2de2155d63b913216910`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Wed, 14 Sep 2022 11:36:24 GMT
RUN EXPOSE map[5601/tcp:{}]
# Wed, 14 Sep 2022 11:36:24 GMT
RUN RUN /bin/sh -c for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Wed, 14 Sep 2022 11:36:26 GMT
RUN RUN /bin/sh -c set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Wed, 14 Sep 2022 11:36:26 GMT
RUN RUN /bin/sh -c mkdir /usr/share/fonts/local # buildkit
# Wed, 14 Sep 2022 11:36:27 GMT
RUN RUN /bin/sh -c curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Wed, 14 Sep 2022 11:36:27 GMT
RUN RUN /bin/sh -c echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Wed, 14 Sep 2022 11:36:27 GMT
RUN RUN /bin/sh -c fc-cache -v # buildkit
# Wed, 14 Sep 2022 11:37:34 GMT
RUN COPY /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 14 Sep 2022 11:37:34 GMT
RUN WORKDIR /usr/share/kibana
# Wed, 14 Sep 2022 11:37:34 GMT
RUN RUN /bin/sh -c ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 14 Sep 2022 11:37:34 GMT
RUN ENV ELASTIC_CONTAINER=true
# Wed, 14 Sep 2022 11:37:34 GMT
RUN ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Sep 2022 11:37:34 GMT
RUN COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 14 Sep 2022 11:37:34 GMT
RUN COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 14 Sep 2022 11:37:35 GMT
RUN RUN /bin/sh -c chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 14 Sep 2022 11:37:36 GMT
RUN RUN /bin/sh -c find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 14 Sep 2022 11:37:36 GMT
RUN RUN /bin/sh -c groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 14 Sep 2022 11:37:36 GMT
RUN LABEL org.label-schema.build-date=2022-09-14T11:08:53.223Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=d34da2c98a97aac80c2b9e8ab197c76cc149574e org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.4.2 org.opencontainers.image.created=2022-09-14T11:08:53.223Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=d34da2c98a97aac80c2b9e8ab197c76cc149574e org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.4.2
# Wed, 14 Sep 2022 11:37:36 GMT
RUN ENTRYPOINT ["/bin/tini" "--"]
# Wed, 14 Sep 2022 11:37:36 GMT
RUN CMD ["/usr/local/bin/kibana-docker"]
# Wed, 14 Sep 2022 11:37:36 GMT
RUN USER kibana
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0ff12fea0fc6c1c65bb947ec47782d37daaca81cc963b8db1ff7db9dde320c`  
		Last Modified: Tue, 20 Sep 2022 23:58:15 GMT  
		Size: 10.5 MB (10514040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec96ed351ee856b3c19f8ab139861d0f7bf6e41e916cede3c21b7c84e634532`  
		Last Modified: Tue, 20 Sep 2022 23:58:13 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e65e225f988e108f0e4f00a14c66de3d3ab30c8c5dd5cc36fd127675cc338f`  
		Last Modified: Tue, 20 Sep 2022 23:58:13 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14552ba69d4e5abd1f4c997b5164041ab7cf9ad755f8ca751d190c407cf0a08f`  
		Last Modified: Tue, 20 Sep 2022 23:58:13 GMT  
		Size: 16.5 MB (16460478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f11238260b37c68ac066734cd5a0a699607da5909ef5f665330299d651456a`  
		Last Modified: Tue, 20 Sep 2022 23:58:11 GMT  
		Size: 5.3 KB (5299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22cc075d452eccbeb5ca4db08f220cad2f3318a9b23ba0b32178f1fefd4dfadd`  
		Last Modified: Tue, 20 Sep 2022 23:58:44 GMT  
		Size: 285.8 MB (285823250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca273074c14630c74e9e9c1ac0abc57221eee74caeb85968f986929300297f14`  
		Last Modified: Tue, 20 Sep 2022 23:58:11 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef7df02653a48311e6efafac663d6f812b3577cc076e208972dd1b597079ef38`  
		Last Modified: Tue, 20 Sep 2022 23:58:09 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b675254c1f6df016380187832387cf3a19b090470a82c295b1408d71d5736c4`  
		Last Modified: Tue, 20 Sep 2022 23:58:08 GMT  
		Size: 4.4 KB (4375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2bc8f61ac6a1ae84835009080f9fd52c8a75c22cbb45bfa3574e723fe85ca0`  
		Last Modified: Tue, 20 Sep 2022 23:58:09 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f259cb8b1501d1cda140dea6590f4ae3ddd50a1c982e045223db3c115fb76c5`  
		Last Modified: Tue, 20 Sep 2022 23:58:09 GMT  
		Size: 189.4 KB (189393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c8a8349acf2e184dc6be1548e4aa3997daaae6d144073c3eba4f1e86a9d6d8`  
		Last Modified: Tue, 20 Sep 2022 23:58:11 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kibana:8.4.2` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:cc96acb99e613fb0909d9b0752b4dcb431f03389c5fcaf25e3ae5a3f5213b2ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.7 MB (354681939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:647acd59aa815ad3e34c49dafb05e67a7e7cb088e47662e1cb6f21090d08c1e0`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:42 GMT
ADD file:78c56cf572dbf860290780b955a94dc4de09bd3b8d64b6a83aee51afb349129a in / 
# Fri, 02 Sep 2022 00:57:43 GMT
CMD ["bash"]
# Wed, 14 Sep 2022 11:39:35 GMT
RUN EXPOSE map[5601/tcp:{}]
# Wed, 14 Sep 2022 11:39:35 GMT
RUN RUN /bin/sh -c for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Wed, 14 Sep 2022 11:39:37 GMT
RUN RUN /bin/sh -c set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Wed, 14 Sep 2022 11:39:37 GMT
RUN RUN /bin/sh -c mkdir /usr/share/fonts/local # buildkit
# Wed, 14 Sep 2022 11:39:40 GMT
RUN RUN /bin/sh -c curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Wed, 14 Sep 2022 11:39:41 GMT
RUN RUN /bin/sh -c echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Wed, 14 Sep 2022 11:39:41 GMT
RUN RUN /bin/sh -c fc-cache -v # buildkit
# Wed, 14 Sep 2022 11:40:45 GMT
RUN COPY /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 14 Sep 2022 11:40:45 GMT
RUN WORKDIR /usr/share/kibana
# Wed, 14 Sep 2022 11:40:45 GMT
RUN RUN /bin/sh -c ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 14 Sep 2022 11:40:45 GMT
RUN ENV ELASTIC_CONTAINER=true
# Wed, 14 Sep 2022 11:40:45 GMT
RUN ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Sep 2022 11:40:45 GMT
RUN COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 14 Sep 2022 11:40:45 GMT
RUN COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 14 Sep 2022 11:40:46 GMT
RUN RUN /bin/sh -c chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 14 Sep 2022 11:40:47 GMT
RUN RUN /bin/sh -c find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 14 Sep 2022 11:40:47 GMT
RUN RUN /bin/sh -c groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 14 Sep 2022 11:40:47 GMT
RUN LABEL org.label-schema.build-date=2022-09-14T11:08:53.223Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=d34da2c98a97aac80c2b9e8ab197c76cc149574e org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.4.2 org.opencontainers.image.created=2022-09-14T11:08:53.223Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=d34da2c98a97aac80c2b9e8ab197c76cc149574e org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.4.2
# Wed, 14 Sep 2022 11:40:47 GMT
RUN ENTRYPOINT ["/bin/tini" "--"]
# Wed, 14 Sep 2022 11:40:47 GMT
RUN CMD ["/usr/local/bin/kibana-docker"]
# Wed, 14 Sep 2022 11:40:47 GMT
RUN USER kibana
```

-	Layers:
	-	`sha256:7a9f619ee5e9c87f19eed59abef41d53eb0694f492da010ee069ff26e7b4ff3f`  
		Last Modified: Fri, 02 Sep 2022 00:59:23 GMT  
		Size: 27.2 MB (27191817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6bbf86952d1356f396278f7b6700870f8b9db7558637b0c23874cbdea3a56b`  
		Last Modified: Wed, 21 Sep 2022 00:30:40 GMT  
		Size: 10.4 MB (10380995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a7a152bb7d83bd7a8325bffa2f02e5ea762d268dc51ac4d25a355e361940bb`  
		Last Modified: Wed, 21 Sep 2022 00:30:39 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c6d9e33d11017c7fac77f16270ff7e18d8526c702021b5a713fba8d00a8750`  
		Last Modified: Wed, 21 Sep 2022 00:30:36 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d51d1f83e43c498446ca6f9df7e08b33290537bc9efe16c5ea42e86e118787`  
		Last Modified: Wed, 21 Sep 2022 00:30:38 GMT  
		Size: 16.5 MB (16460490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93b5e79e07a0e19b73ab5559fff73614e463b33cbede4322be9ae1107fa8e46`  
		Last Modified: Wed, 21 Sep 2022 00:30:36 GMT  
		Size: 5.3 KB (5299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3fdb6f5b227e29c907a946a3f116497d99e50987f01457782ef4ce49b88f3e`  
		Last Modified: Wed, 21 Sep 2022 00:31:14 GMT  
		Size: 300.4 MB (300443491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510b40bd0beab4028cf4965d9544ae4f52debbe2e4ed9154286def79f682d53a`  
		Last Modified: Wed, 21 Sep 2022 00:30:36 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd1788fac5b52f70af4ae9eb87a44dd0ea998e2d0696ee85fbc4331100b158f`  
		Last Modified: Wed, 21 Sep 2022 00:30:34 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946941124da0e5067d2ba9f493b2b537c5e89147ff6669eb8eb57e1470c0b0bb`  
		Last Modified: Wed, 21 Sep 2022 00:30:33 GMT  
		Size: 4.4 KB (4380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba8a303c511f0dfe35cb8b80ef57077c8dee147b90b53f2c3a818363c596c9e`  
		Last Modified: Wed, 21 Sep 2022 00:30:34 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:166df296f457228e6c834b5957c531bc8bf4cd331995b63620c44d4fab7c4b08`  
		Last Modified: Wed, 21 Sep 2022 00:30:34 GMT  
		Size: 183.4 KB (183394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae7a8dae4b23a6506c8c7cabb5ee89423a72ecb0aeed7f9af2343d47199f9d8`  
		Last Modified: Wed, 21 Sep 2022 00:30:34 GMT  
		Size: 1.8 KB (1824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
