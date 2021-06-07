<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:6.8.16`](#kibana6816)
-	[`kibana:7.13.1`](#kibana7131)

## `kibana:6.8.16`

```console
$ docker pull kibana@sha256:d5b770e77b109cc53b1dd698c8692d00266bd03a51a6103de7547a9ebd67879b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kibana:6.8.16` - linux; amd64

```console
$ docker pull kibana@sha256:75e366ba999347b59bf4828318a9067f86d3e310d2cce63749f954cdc9015b41
```

-	Docker Version: 20.10.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314277631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:660db354c9a6e2d1ebd6d3351f08b460ca119d708eba560f70033a9fae564777`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Fri, 21 May 2021 20:16:10 GMT
EXPOSE 5601
# Fri, 21 May 2021 20:16:53 GMT
RUN yum update -y && yum install -y fontconfig freetype && yum clean all
# Fri, 21 May 2021 20:17:13 GMT
COPY --chown=1000:0dir:58f4d8f397cd42d79333acc4d874d4af4b0daf6eb406b891ad314f85c2bf7217 in /usr/share/kibana 
# Fri, 21 May 2021 20:17:15 GMT
WORKDIR /usr/share/kibana
# Fri, 21 May 2021 20:17:17 GMT
RUN ln -s /usr/share/kibana /opt/kibana
# Fri, 21 May 2021 20:17:17 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 21 May 2021 20:17:17 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 May 2021 20:17:17 GMT
COPY --chown=1000:0file:60b6181f28c99b362092ea6139b6d4112ddd0bef32d52563c33b26bdc2b51318 in /usr/share/kibana/config/kibana.yml 
# Fri, 21 May 2021 20:17:18 GMT
COPY --chown=1000:0file:7d472d1939e23e2f10e7c5fd1e9166eefd646214aa0d8a1c09d92af71c9cbd87 in /usr/local/bin/ 
# Fri, 21 May 2021 20:17:19 GMT
RUN chmod g+ws /usr/share/kibana && find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \;
# Fri, 21 May 2021 20:17:20 GMT
RUN groupadd --gid 1000 kibana && useradd --uid 1000 --gid 1000 --home-dir /usr/share/kibana --no-create-home kibana
# Fri, 21 May 2021 20:17:20 GMT
USER kibana
# Fri, 21 May 2021 20:17:20 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.label-schema.name=kibana org.label-schema.version=6.8.16 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.license=Elastic License license=Elastic License
# Fri, 21 May 2021 20:17:20 GMT
CMD ["/usr/local/bin/kibana-docker"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e54279e1f3b678ed0ecb7b22179ebde197f0c63a5d27bdc61eadb74868ea1a5`  
		Last Modified: Tue, 25 May 2021 12:53:44 GMT  
		Size: 51.1 MB (51074850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee0978b56b2f2ade80e76ab193501899df339ab41906c9666294daea77527ae`  
		Last Modified: Tue, 25 May 2021 12:54:00 GMT  
		Size: 187.1 MB (187100867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0060e6d28e159cc9e24d569d7da7771fad69e1d27db00575dab6fd8fe897ff9a`  
		Last Modified: Tue, 25 May 2021 12:53:34 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df3f49b2dacf9752d86f6435ec98a390e5e72326829a4149958be5faa6ee6be`  
		Last Modified: Tue, 25 May 2021 12:53:32 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e7974142180fb550caf935fdf5760d7567479617f4dcb112818faf5f0d2ca4`  
		Last Modified: Tue, 25 May 2021 12:53:32 GMT  
		Size: 2.3 KB (2264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986401b2de155f9e97cca29a9db1cf39c0a335cc4c552057cf6c3215d8f7180f`  
		Last Modified: Tue, 25 May 2021 12:53:31 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea96f665a87c76e7742652ccbe79d723a4fdfd844646a8f62e89f9268bbc960`  
		Last Modified: Tue, 25 May 2021 12:53:28 GMT  
		Size: 1.8 KB (1819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kibana:7.13.1`

```console
$ docker pull kibana@sha256:298a8520298f229f4be784f8fb204976b4e5215b89968f82bc45a469c00933ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kibana:7.13.1` - linux; amd64

```console
$ docker pull kibana@sha256:7a30e66eb455454d04d7566dcda0c62659e4986c13c0cad4a8be0bf1d94deb84
```

-	Docker Version: 20.10.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.9 MB (432941985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9e323cd5f35127ecb650c2ed65af0cf0a954ec21ff9323278c4dd3fcadc3fa6`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 08 Dec 2020 00:22:52 GMT
ADD file:bd7a2aed6ede423b719ceb2f723e4ecdfa662b28639c8429731c878e86fb138b in / 
# Tue, 08 Dec 2020 00:22:52 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201204
# Tue, 08 Dec 2020 00:22:53 GMT
CMD ["/bin/bash"]
# Fri, 28 May 2021 17:39:50 GMT
EXPOSE 5601
# Fri, 28 May 2021 17:40:15 GMT
RUN for iter in {1..10}; do       yum update --setopt=tsflags=nodocs -y &&       yum install --setopt=tsflags=nodocs -y         fontconfig freetype shadow-utils nss  &&       yum clean all && exit_code=0 && break || exit_code=$? && echo "yum error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code)
# Fri, 28 May 2021 17:40:17 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini
# Fri, 28 May 2021 17:40:18 GMT
RUN mkdir /usr/share/fonts/local
# Fri, 28 May 2021 17:40:20 GMT
RUN curl -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc
# Fri, 28 May 2021 17:40:20 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c -
# Fri, 28 May 2021 17:40:21 GMT
RUN fc-cache -v
# Fri, 28 May 2021 17:40:48 GMT
COPY --chown=1000:0dir:24e84840d13dea8a952d664d8d6eb3d2f7408b38a5d00c2e12fa6bbac41e6bae in /usr/share/kibana 
# Fri, 28 May 2021 17:41:08 GMT
WORKDIR /usr/share/kibana
# Fri, 28 May 2021 17:41:09 GMT
RUN ln -s /usr/share/kibana /opt/kibana
# Fri, 28 May 2021 17:41:09 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 28 May 2021 17:41:09 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 May 2021 17:41:09 GMT
COPY --chown=1000:0file:eb11f9e933d42eab464a137c84e7f78cfe8f1f641eabf0e5b851a4bef6ea8419 in /usr/share/kibana/config/kibana.yml 
# Fri, 28 May 2021 17:41:09 GMT
COPY --chown=1000:0file:2ad2d462f1afd1e3067945c2c68939f5f1f2cc80e376132b2be85a5979eee38b in /usr/local/bin/ 
# Fri, 28 May 2021 17:41:11 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \;
# Fri, 28 May 2021 17:41:12 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} +
# Fri, 28 May 2021 17:41:13 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana
# Fri, 28 May 2021 17:41:13 GMT
LABEL org.label-schema.build-date=2021-05-28T16:34:19.370Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=9b177ae95979d96cf172517a3c6e469bbbda07ed org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.13.1 org.opencontainers.image.created=2021-05-28T16:34:19.370Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=9b177ae95979d96cf172517a3c6e469bbbda07ed org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.13.1
# Fri, 28 May 2021 17:41:13 GMT
USER kibana
# Fri, 28 May 2021 17:41:14 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Fri, 28 May 2021 17:41:14 GMT
CMD ["/usr/local/bin/kibana-docker"]
```

-	Layers:
	-	`sha256:7a0437f04f83f084b7ed68ad9c4a4947e12fc4e1b006b38129bac89114ec3621`  
		Last Modified: Tue, 08 Dec 2020 00:23:32 GMT  
		Size: 75.2 MB (75181999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad86619e7d57dda2b236e48740450bd4247ecc5b8a83d3151e21b879b615ee09`  
		Last Modified: Wed, 02 Jun 2021 15:21:45 GMT  
		Size: 36.3 MB (36338218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d8788349442048630f44ac7230d3eaa8d1a5e4a99b9bacb334b3c42a109c66`  
		Last Modified: Wed, 02 Jun 2021 15:21:37 GMT  
		Size: 9.5 KB (9535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91eabec78fb07b2fb3a7bdebca15422ead5f390964b7d536d34f0714ad23cdc9`  
		Last Modified: Wed, 02 Jun 2021 15:21:34 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e62c391a545cea4a61101f376390d6949d35cf6a3e6f920b789fe6a046b24d`  
		Last Modified: Wed, 02 Jun 2021 15:21:36 GMT  
		Size: 16.5 MB (16460497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac93ee666950e5142b61d28fe3bfdceed245fa6a1f239b2852b9f50de9989c2`  
		Last Modified: Wed, 02 Jun 2021 15:21:33 GMT  
		Size: 8.3 KB (8271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bff7778ee7bf4b70f1ee761783ac8df6f62adda1c071071c7aa34a5e93a0955`  
		Last Modified: Wed, 02 Jun 2021 15:22:20 GMT  
		Size: 304.7 MB (304740415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91fe0b94def993756ffff96410068b216798bd02ab6b6432282b1ac4f055b9eb`  
		Last Modified: Wed, 02 Jun 2021 15:21:34 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d82c54038391033cf748c5462e5bfbafab2b7597679ecfbb4c4ad06696c1a1`  
		Last Modified: Wed, 02 Jun 2021 15:21:30 GMT  
		Size: 377.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec27fd7d553448e7a341941acc25de200b80ef298bdecb04e9882f04a9e805d`  
		Last Modified: Wed, 02 Jun 2021 15:21:30 GMT  
		Size: 3.7 KB (3728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd56ea18f687838a4181a6c1fde5a89c752bc300a67a1d1e811fa46747455836`  
		Last Modified: Wed, 02 Jun 2021 15:21:30 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368acde48564498233d724bf9421d393e95b40e33d330f729735aa03355693a0`  
		Last Modified: Wed, 02 Jun 2021 15:21:30 GMT  
		Size: 196.4 KB (196391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f721eb02ef785cc12f1d7bdbc0a3b8c02ed6c568d9f13cc418acfeb67bb768fe`  
		Last Modified: Wed, 02 Jun 2021 15:21:30 GMT  
		Size: 1.8 KB (1847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kibana:7.13.1` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:b365ceadf9e0be71ff75b339c3df027dae6ad8519e6dabfe9e0ef3d1ccbf2e5f
```

-	Docker Version: 20.10.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.0 MB (446967436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae9450c8714871e1c2b645663a0c045e7d43c53e067a10a6f16a3b5a9bd6451`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 07 Dec 2020 23:42:06 GMT
ADD file:edd6e1253ec7bbb67b5a28d40c7d28b34a443c2cfa327bebf55c8b0b19484bf9 in / 
# Mon, 07 Dec 2020 23:42:09 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201204
# Mon, 07 Dec 2020 23:42:10 GMT
CMD ["/bin/bash"]
# Fri, 28 May 2021 18:45:02 GMT
EXPOSE 5601
# Fri, 28 May 2021 18:45:44 GMT
RUN for iter in {1..10}; do       yum update --setopt=tsflags=nodocs -y &&       yum install --setopt=tsflags=nodocs -y         fontconfig freetype shadow-utils nss  &&       yum clean all && exit_code=0 && break || exit_code=$? && echo "yum error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code)
# Fri, 28 May 2021 18:45:45 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini
# Fri, 28 May 2021 18:45:46 GMT
RUN mkdir /usr/share/fonts/local
# Fri, 28 May 2021 18:45:48 GMT
RUN curl -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc
# Fri, 28 May 2021 18:45:49 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c -
# Fri, 28 May 2021 18:45:50 GMT
RUN fc-cache -v
# Fri, 28 May 2021 18:46:17 GMT
COPY --chown=1000:0dir:a030b763671efb3ef7ef38e7aefc6c218ed608201a0525bb41576397fdbf6886 in /usr/share/kibana 
# Fri, 28 May 2021 18:46:19 GMT
WORKDIR /usr/share/kibana
# Fri, 28 May 2021 18:46:20 GMT
RUN ln -s /usr/share/kibana /opt/kibana
# Fri, 28 May 2021 18:46:20 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 28 May 2021 18:46:20 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 May 2021 18:46:20 GMT
COPY --chown=1000:0file:eb11f9e933d42eab464a137c84e7f78cfe8f1f641eabf0e5b851a4bef6ea8419 in /usr/share/kibana/config/kibana.yml 
# Fri, 28 May 2021 18:46:20 GMT
COPY --chown=1000:0file:2ad2d462f1afd1e3067945c2c68939f5f1f2cc80e376132b2be85a5979eee38b in /usr/local/bin/ 
# Fri, 28 May 2021 18:46:22 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \;
# Fri, 28 May 2021 18:46:24 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} +
# Fri, 28 May 2021 18:46:24 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana
# Fri, 28 May 2021 18:46:24 GMT
LABEL org.label-schema.build-date=2021-05-28T18:41:06.391Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=9b177ae95979d96cf172517a3c6e469bbbda07ed org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.13.1 org.opencontainers.image.created=2021-05-28T18:41:06.391Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=9b177ae95979d96cf172517a3c6e469bbbda07ed org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.13.1
# Fri, 28 May 2021 18:46:25 GMT
USER kibana
# Fri, 28 May 2021 18:46:25 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Fri, 28 May 2021 18:46:25 GMT
CMD ["/usr/local/bin/kibana-docker"]
```

-	Layers:
	-	`sha256:333cbcae3fb80b9a46084ae4caea81a84aafda9700fb646ab89206d0cfe213fd`  
		Last Modified: Mon, 07 Dec 2020 23:42:49 GMT  
		Size: 75.6 MB (75613064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a9c972f874391722d6892d14c7cb0b3914e7fe9d69bc3bffb601495ce1f378`  
		Last Modified: Mon, 07 Jun 2021 17:41:03 GMT  
		Size: 35.5 MB (35548976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5fe8a55523a77e0efb42adaa6b52034df03044b193dd7d17987999eae4dc17c`  
		Last Modified: Mon, 07 Jun 2021 17:40:57 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6c2abe1c4091a0111dc0bb334ae6a7450ffa07d4fdafb6a14748f8432a31e1`  
		Last Modified: Mon, 07 Jun 2021 17:40:54 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5317381a3593318ed93c77b2b90add6cbfcba86d5c087a2fda0cdc7bbf8f16`  
		Last Modified: Mon, 07 Jun 2021 17:40:55 GMT  
		Size: 16.5 MB (16460475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0069921c75ebdf85a1263dc6f9dacbb5b76bf7bb09449e8be6d3d9c872a1cba5`  
		Last Modified: Mon, 07 Jun 2021 17:40:54 GMT  
		Size: 8.3 KB (8308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5079af43f63f0b4d1de9aa5bda316402b377daf8fe83758bdb2fa7e91b82cc6e`  
		Last Modified: Mon, 07 Jun 2021 17:41:40 GMT  
		Size: 319.1 MB (319123623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258d8f5c2ec877cf1c2db690213b95a739c05804c0a0f266c8eda0ed7da075e0`  
		Last Modified: Mon, 07 Jun 2021 17:40:53 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42848b29e778101ddf040d193a80165a8a612e0e6f3b444a009d6b27ac7ce5b`  
		Last Modified: Mon, 07 Jun 2021 17:40:51 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c46af82f75c06dc816592f63b234853ff737cb59879c449212d9d82850d0715`  
		Last Modified: Mon, 07 Jun 2021 17:40:51 GMT  
		Size: 3.7 KB (3728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e53c9c2340984c4b95f421469fc5f5238a37d111fac0f00c86ccec23a51e6cc`  
		Last Modified: Mon, 07 Jun 2021 17:40:51 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8d250ba48df3a41280640fd19b268f26778004260acb9ebf6fe2212f47b350`  
		Last Modified: Mon, 07 Jun 2021 17:40:51 GMT  
		Size: 197.2 KB (197225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc0c716c62354c6938beae07eae632265ab64253392aadde244ba2ce62f3bbc`  
		Last Modified: Mon, 07 Jun 2021 17:40:51 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
