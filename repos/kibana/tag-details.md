<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:6.8.23`](#kibana6823)
-	[`kibana:7.17.4`](#kibana7174)
-	[`kibana:8.2.2`](#kibana822)

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

## `kibana:7.17.4`

```console
$ docker pull kibana@sha256:13572cada04ff3730aa7cb6ebc0e0f28e0ae7b4a3a4304fff5104e011b2cba05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kibana:7.17.4` - linux; amd64

```console
$ docker pull kibana@sha256:ce193e81c4212965be645422bde5e81215c169c7985c3dbabbe88349d6396f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334261169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86967a98433b104af475683ab9a52609298e1650b395cceb479dde052056ccf6`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Fri, 29 Apr 2022 23:20:59 GMT
ADD file:7009ad0ee0bbe5ed7f381792e07347e260e6896aeee0d80597808065120fa96b in / 
# Fri, 29 Apr 2022 23:20:59 GMT
CMD ["bash"]
# Wed, 18 May 2022 11:34:27 GMT
RUN EXPOSE map[5601/tcp:{}]
# Wed, 18 May 2022 11:34:27 GMT
RUN RUN /bin/sh -c for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Wed, 18 May 2022 11:34:28 GMT
RUN RUN /bin/sh -c set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Wed, 18 May 2022 11:34:29 GMT
RUN RUN /bin/sh -c mkdir /usr/share/fonts/local # buildkit
# Wed, 18 May 2022 11:34:29 GMT
RUN RUN /bin/sh -c curl -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Wed, 18 May 2022 11:34:30 GMT
RUN RUN /bin/sh -c echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Wed, 18 May 2022 11:34:30 GMT
RUN RUN /bin/sh -c fc-cache -v # buildkit
# Wed, 18 May 2022 11:35:28 GMT
RUN COPY /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 18 May 2022 11:35:28 GMT
RUN WORKDIR /usr/share/kibana
# Wed, 18 May 2022 11:35:28 GMT
RUN RUN /bin/sh -c ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 18 May 2022 11:35:28 GMT
RUN ENV ELASTIC_CONTAINER=true
# Wed, 18 May 2022 11:35:28 GMT
RUN ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 May 2022 11:35:28 GMT
RUN COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 18 May 2022 11:35:28 GMT
RUN COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 18 May 2022 11:35:29 GMT
RUN RUN /bin/sh -c chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 18 May 2022 11:35:29 GMT
RUN RUN /bin/sh -c find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 18 May 2022 11:35:30 GMT
RUN RUN /bin/sh -c groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 18 May 2022 11:35:30 GMT
RUN LABEL org.label-schema.build-date=2022-05-18T11:08:55.145Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=a408358a8fc5671f5eb7985678a1733684441b37 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.4 org.opencontainers.image.created=2022-05-18T11:08:55.145Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=a408358a8fc5671f5eb7985678a1733684441b37 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.4
# Wed, 18 May 2022 11:35:30 GMT
RUN ENTRYPOINT ["/bin/tini" "--"]
# Wed, 18 May 2022 11:35:30 GMT
RUN CMD ["/usr/local/bin/kibana-docker"]
# Wed, 18 May 2022 11:35:30 GMT
RUN USER kibana
```

-	Layers:
	-	`sha256:d5fd17ec1767521cf97f61568096bfc9a7cd9c2d149576a7b43930c5a97062b0`  
		Last Modified: Thu, 28 Apr 2022 03:03:21 GMT  
		Size: 28.6 MB (28566230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895745324f08b79d14681990f0904d2ef4ec6a915e9a24f75ec6a466339c4657`  
		Last Modified: Wed, 25 May 2022 17:23:55 GMT  
		Size: 20.4 MB (20353871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870e4a4d58fd2630596dd2708fe4b4f1ce8569f4324e673a15d6ae67f2e0a4af`  
		Last Modified: Wed, 25 May 2022 17:23:52 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994a3c1a490e635fc3a5cb733b5ac7847a3c6d8bb68fb8023aaea79ef20d75af`  
		Last Modified: Wed, 25 May 2022 17:23:50 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ce515a8091927b2eeff897a2379ac9e1f41cdb6216ec2330117da5c2626c93`  
		Last Modified: Wed, 25 May 2022 17:23:51 GMT  
		Size: 16.5 MB (16460477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77156eca877c4fb6ce017f148257f7627b3769859e4f8e2e0b67ec15bb73ca5a`  
		Last Modified: Wed, 25 May 2022 17:23:50 GMT  
		Size: 5.3 KB (5295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf02bccac78791a35d232c0fd9eac4f3933e3d4f5a4b0d601a2994a68df15cd`  
		Last Modified: Wed, 25 May 2022 17:24:21 GMT  
		Size: 268.7 MB (268668864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a2ae4c00a5f29540c1f28204030f1930a71de10e009184ec3b6df025ba437c`  
		Last Modified: Wed, 25 May 2022 17:23:50 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1111db6cec977561ad1043ae70c9a4be0aeaf885de414455cf59864af575fe08`  
		Last Modified: Wed, 25 May 2022 17:23:47 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bbbc44af66de7ccafc955f45a3df6f43a79615711258c5c7fc3d73da6db13e3`  
		Last Modified: Wed, 25 May 2022 17:23:47 GMT  
		Size: 4.5 KB (4505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee0ccbb5da171a6314ecf836383eb2c6b763a239a7680d1283bdcfc4af8c238`  
		Last Modified: Wed, 25 May 2022 17:23:47 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad4da5ac21b61a772786e6551aca42ee2a3b45c9879914157136a9c4986b4cb`  
		Last Modified: Wed, 25 May 2022 17:23:47 GMT  
		Size: 189.4 KB (189393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e021f342c39d3e1f11627f3d9c2b0f46c63d71c10848f73c29c187fef4f02a1d`  
		Last Modified: Wed, 25 May 2022 17:23:47 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kibana:7.17.4` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:e13b3c29fe5b570cee3721c8928f1c42f79ccd35c6cef3ab2f7c3e97eb6f2c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.2 MB (346160845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0cb4cc865b80fccce0f8549fef4c4677c8208d77c069b6465ffa35de45297f3`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Wed, 18 May 2022 11:37:41 GMT
RUN EXPOSE map[5601/tcp:{}]
# Wed, 18 May 2022 11:37:41 GMT
RUN RUN /bin/sh -c for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Wed, 18 May 2022 11:37:42 GMT
RUN RUN /bin/sh -c set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Wed, 18 May 2022 11:37:43 GMT
RUN RUN /bin/sh -c mkdir /usr/share/fonts/local # buildkit
# Wed, 18 May 2022 11:37:45 GMT
RUN RUN /bin/sh -c curl -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Wed, 18 May 2022 11:37:46 GMT
RUN RUN /bin/sh -c echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Wed, 18 May 2022 11:37:46 GMT
RUN RUN /bin/sh -c fc-cache -v # buildkit
# Wed, 18 May 2022 11:38:29 GMT
RUN COPY /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 18 May 2022 11:38:29 GMT
RUN WORKDIR /usr/share/kibana
# Wed, 18 May 2022 11:38:29 GMT
RUN RUN /bin/sh -c ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 18 May 2022 11:38:29 GMT
RUN ENV ELASTIC_CONTAINER=true
# Wed, 18 May 2022 11:38:29 GMT
RUN ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 May 2022 11:38:29 GMT
RUN COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 18 May 2022 11:38:30 GMT
RUN COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 18 May 2022 11:38:30 GMT
RUN RUN /bin/sh -c chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 18 May 2022 11:38:31 GMT
RUN RUN /bin/sh -c find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 18 May 2022 11:38:32 GMT
RUN RUN /bin/sh -c groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 18 May 2022 11:38:32 GMT
RUN LABEL org.label-schema.build-date=2022-05-18T11:08:55.145Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=a408358a8fc5671f5eb7985678a1733684441b37 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.4 org.opencontainers.image.created=2022-05-18T11:08:55.145Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=a408358a8fc5671f5eb7985678a1733684441b37 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.4
# Wed, 18 May 2022 11:38:32 GMT
RUN ENTRYPOINT ["/bin/tini" "--"]
# Wed, 18 May 2022 11:38:32 GMT
RUN CMD ["/usr/local/bin/kibana-docker"]
# Wed, 18 May 2022 11:38:32 GMT
RUN USER kibana
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc67de5f2caa39c6b84b7b4f075cc4e6b50f90d3ee10603274331320e50e415`  
		Last Modified: Wed, 25 May 2022 18:09:50 GMT  
		Size: 19.1 MB (19050929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ebd06202c616734365059ed22b2c9666a3e72e47b66617c058c7daed5a3d388`  
		Last Modified: Wed, 25 May 2022 18:09:48 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94837e1901a9cca9606d9b1fd70bad0d4581782e2a53da34334329cdbb887b4e`  
		Last Modified: Wed, 25 May 2022 18:09:45 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e8fade51954b5bb89ba6555a130d432f47ed73a29eac6a290083d5085da6cc`  
		Last Modified: Wed, 25 May 2022 18:09:47 GMT  
		Size: 16.5 MB (16460496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69502a7cd4a1c226d770c3f3d882f15cff088fd7753bb9e39d5b8fb3b842bdf`  
		Last Modified: Wed, 25 May 2022 18:09:45 GMT  
		Size: 5.3 KB (5288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea5f794788c4f7b6e3dc5daef7289ee36589520c2f86d012aab0c94e19283d2`  
		Last Modified: Wed, 25 May 2022 18:10:21 GMT  
		Size: 283.3 MB (283274736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1cb955ac88290090ac5f4129c02eaf3d6b0ccb05cc8727824754c951d1391e7`  
		Last Modified: Wed, 25 May 2022 18:09:45 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c814e4b8d09abaa078d9a817a2d7bc1eeedfd4fdea5a998d5b04bd5ccaa39395`  
		Last Modified: Wed, 25 May 2022 18:09:43 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e934e26457f998cc997a96c330bc94165f1567a6d12e71c9d79f21ff2e90bc7a`  
		Last Modified: Wed, 25 May 2022 18:09:42 GMT  
		Size: 4.5 KB (4506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ffa79e81356d4335d7c8b38afccffcfdfe5945cb2441c04e2ee9e46f751ae1`  
		Last Modified: Wed, 25 May 2022 18:09:42 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf2abae2911c5d66b7807f23a6c289b4dca6eba0dd293678ee91dd8a91fa502`  
		Last Modified: Wed, 25 May 2022 18:09:42 GMT  
		Size: 183.4 KB (183395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c129c85ffaaec772155440777196e630942e867a6b65a0ad121dbd966ac9f60f`  
		Last Modified: Wed, 25 May 2022 18:09:42 GMT  
		Size: 1.8 KB (1825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kibana:8.2.2`

**does not exist** (yet?)
