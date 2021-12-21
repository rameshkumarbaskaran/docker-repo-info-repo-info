<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:6.8.22`](#kibana6822)
-	[`kibana:7.16.2`](#kibana7162)

## `kibana:6.8.22`

```console
$ docker pull kibana@sha256:2b0dc7184a9c4f1dd0df031a91e458eff91a4111ce95f92f1b7cca92219f9926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kibana:6.8.22` - linux; amd64

```console
$ docker pull kibana@sha256:7276be7c8a4bdc13b25f5ffeb6f3142dfb9ef6ac28314490dda3a5ff3cc41880
```

-	Docker Version: 20.10.10
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.7 MB (325735589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7378ee20fe044c38a3ba30918b12a8bf2f4b36c927bd4fd71c205cd8471d7f2`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Sun, 19 Dec 2021 02:24:52 GMT
EXPOSE 5601
# Sun, 19 Dec 2021 02:26:30 GMT
RUN yum update -y && yum install -y fontconfig freetype && yum clean all
# Sun, 19 Dec 2021 02:27:18 GMT
COPY --chown=1000:0dir:aaf2a9b5239aef20562498cdae38a5562a296fd00e53af9f47e803244008ee87 in /usr/share/kibana 
# Sun, 19 Dec 2021 02:27:20 GMT
WORKDIR /usr/share/kibana
# Sun, 19 Dec 2021 02:27:22 GMT
RUN ln -s /usr/share/kibana /opt/kibana
# Sun, 19 Dec 2021 02:27:23 GMT
ENV ELASTIC_CONTAINER=true
# Sun, 19 Dec 2021 02:27:24 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 19 Dec 2021 02:27:24 GMT
COPY --chown=1000:0file:60b6181f28c99b362092ea6139b6d4112ddd0bef32d52563c33b26bdc2b51318 in /usr/share/kibana/config/kibana.yml 
# Sun, 19 Dec 2021 02:27:26 GMT
COPY --chown=1000:0file:7d472d1939e23e2f10e7c5fd1e9166eefd646214aa0d8a1c09d92af71c9cbd87 in /usr/local/bin/ 
# Sun, 19 Dec 2021 02:27:29 GMT
RUN chmod g+ws /usr/share/kibana && find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \;
# Sun, 19 Dec 2021 02:27:31 GMT
RUN groupadd --gid 1000 kibana && useradd --uid 1000 --gid 1000 --home-dir /usr/share/kibana --no-create-home kibana
# Sun, 19 Dec 2021 02:27:31 GMT
USER kibana
# Sun, 19 Dec 2021 02:27:32 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.label-schema.name=kibana org.label-schema.version=6.8.22 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.license=Elastic License license=Elastic License
# Sun, 19 Dec 2021 02:27:32 GMT
CMD ["/usr/local/bin/kibana-docker"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf35f5e94db4a1365ec74877a4b5a9bfd4fadf6de0b216bfc1cd3b79fdbc86af`  
		Last Modified: Sun, 19 Dec 2021 20:54:36 GMT  
		Size: 61.0 MB (60997859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9528749378acc340bd228b925f0eadb8f16f85951b9cc37876f307d1d63021f7`  
		Last Modified: Sun, 19 Dec 2021 20:54:48 GMT  
		Size: 188.6 MB (188635813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e6259f54e889e0d43ca52436ad78e649412190110dbd68092e59a6baedcdd4`  
		Last Modified: Sun, 19 Dec 2021 20:54:29 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8589653378f9af68c55a073af9c809eb845da74812106bdc9638fc2bab46d7ef`  
		Last Modified: Sun, 19 Dec 2021 20:54:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21cc3c0cd2963c0a563caf4bd98b57fc2d102cdc61fe098fb29c61a483e9663`  
		Last Modified: Sun, 19 Dec 2021 20:54:26 GMT  
		Size: 2.3 KB (2264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c231ace297b14af5a4b65b71f65d5ed156cc2151e1c3ace08cd3f4af777da1d`  
		Last Modified: Sun, 19 Dec 2021 20:54:26 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850fa3ad8b10d6098697ad4d48fec75863d11769a0288b7e50014c72fb466c19`  
		Last Modified: Sun, 19 Dec 2021 20:54:24 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kibana:7.16.2`

```console
$ docker pull kibana@sha256:cbff0e7f8200798130dc9ebca666c89d440f203272d66b007763ef554b21d0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kibana:7.16.2` - linux; amd64

```console
$ docker pull kibana@sha256:51aec3d4fa9711e712bcd0af984bfc35a6fe0cb1bcaef2f241b5c5fafbf18e4d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.6 MB (480625978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c46ec23123eb7341321e7d1b0ba9ebeb2f49a96e82ed72ccfb084b0e665f64c`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:04 GMT
ADD file:805cb5e15fb6e0bb0326ca33fd2942e068863ce2a8491bb71522c652f31fb466 in / 
# Wed, 15 Sep 2021 18:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20210915
# Wed, 15 Sep 2021 18:20:05 GMT
CMD ["/bin/bash"]
# Sat, 18 Dec 2021 20:41:13 GMT
EXPOSE 5601
# Sat, 18 Dec 2021 20:42:04 GMT
RUN for iter in {1..10}; do       yum update --setopt=tsflags=nodocs -y &&       yum install --setopt=tsflags=nodocs -y         fontconfig freetype shadow-utils nss  &&       yum clean all && exit_code=0 && break || exit_code=$? && echo "yum error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code)
# Sat, 18 Dec 2021 20:42:06 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini
# Sat, 18 Dec 2021 20:42:07 GMT
RUN mkdir /usr/share/fonts/local
# Sat, 18 Dec 2021 20:42:08 GMT
RUN curl -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc
# Sat, 18 Dec 2021 20:42:09 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c -
# Sat, 18 Dec 2021 20:42:10 GMT
RUN fc-cache -v
# Sat, 18 Dec 2021 20:42:38 GMT
COPY --chown=1000:0dir:101babb43c852f12335fb8a6950e0b84b9145812c4f60b30570034a7dd78dbbd in /usr/share/kibana 
# Sat, 18 Dec 2021 20:42:48 GMT
WORKDIR /usr/share/kibana
# Sat, 18 Dec 2021 20:42:49 GMT
RUN ln -s /usr/share/kibana /opt/kibana
# Sat, 18 Dec 2021 20:42:49 GMT
ENV ELASTIC_CONTAINER=true
# Sat, 18 Dec 2021 20:42:49 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Dec 2021 20:42:49 GMT
COPY --chown=1000:0file:6db5413736a28ead04731f52a5ef1acaa8f3ca1c1d2eaf6bb2b80d8f232794a2 in /usr/share/kibana/config/kibana.yml 
# Sat, 18 Dec 2021 20:42:49 GMT
COPY file:4b05cc4ee8dc464b192dc25102b9385329fd96ca9e48428d3b36b7d2a9e4be58 in /usr/local/bin/ 
# Sat, 18 Dec 2021 20:42:51 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \;
# Sat, 18 Dec 2021 20:42:52 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} +
# Sat, 18 Dec 2021 20:42:53 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana
# Sat, 18 Dec 2021 20:42:53 GMT
LABEL org.label-schema.build-date=2021-12-18T19:47:46.695Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=9b678a13a6a3f45286f1d21856a7536a9297f42f org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.16.2 org.opencontainers.image.created=2021-12-18T19:47:46.695Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=9b678a13a6a3f45286f1d21856a7536a9297f42f org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.16.2
# Sat, 18 Dec 2021 20:42:53 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Sat, 18 Dec 2021 20:42:53 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Sat, 18 Dec 2021 20:42:53 GMT
USER kibana
```

-	Layers:
	-	`sha256:a1d0c75327776413fa0db9ed3adcdbadedc95a662eb1d360dad82bb913f8a1d1`  
		Last Modified: Wed, 15 Sep 2021 18:21:25 GMT  
		Size: 83.5 MB (83518086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700212586d98cb48deb6be94a920c2a36e1c3bc4c27a868e9423b55825c7698a`  
		Last Modified: Sun, 19 Dec 2021 13:21:12 GMT  
		Size: 94.4 MB (94426988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013f69c97c90843a572efd852dfc271b2fe0fba5ffe0bb7bf0248ae1b0a264ad`  
		Last Modified: Sun, 19 Dec 2021 13:21:01 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c92d785e3b224ec32621da6285e1aa4e462caa0ada30af231ecab776e7ce8cb`  
		Last Modified: Sun, 19 Dec 2021 13:21:00 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efddc883940a26396b5c72d5f336555cc09ba98439e269842b605465e2a96973`  
		Last Modified: Sun, 19 Dec 2021 13:21:01 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ac9ba18fc01fb853775fa296bff08c7e85a77848f9ce7e50e07ce5780b5753`  
		Last Modified: Sun, 19 Dec 2021 13:20:58 GMT  
		Size: 8.3 KB (8258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d6c552d07814d66bb387ea797d43bcafe801eca2e1228edaef9746974fa512d`  
		Last Modified: Sun, 19 Dec 2021 13:21:28 GMT  
		Size: 286.0 MB (285998705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752fb7e12a501c96e7a8a44454bb170a806ea4111e2530581c23e2f6b948e6ec`  
		Last Modified: Sun, 19 Dec 2021 13:20:58 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be34b62839b5c619cff2665cd8230415a09c488a263e19297a240ac1a27ef1f5`  
		Last Modified: Sun, 19 Dec 2021 13:20:57 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7a37976b341bc8175abf54852729524e0accb204fee3e5dcdb1783873f2b84`  
		Last Modified: Sun, 19 Dec 2021 13:20:56 GMT  
		Size: 4.5 KB (4486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39cd3d8ea5b357a903eb6fcf561295e02b7fec6eff93210a9f7fc892a38d41f4`  
		Last Modified: Sun, 19 Dec 2021 13:20:55 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c75809c03a7d6514371956c5f2782e4c79e557ea4d1d7e33e82e0223c7ca25d`  
		Last Modified: Sun, 19 Dec 2021 13:20:55 GMT  
		Size: 196.5 KB (196451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bff35135e16628e01807188b12f625c3957fbe7142d72c491b1fabd3b7eabe`  
		Last Modified: Sun, 19 Dec 2021 13:20:55 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kibana:7.16.2` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:f4bbb4e68162da8d7b492294e5fbdb8af96fe9149b3f844445b530695327665e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.6 MB (495590403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bcb4cae919c78fe2a75fbe77f711ca3f8de0829edf9c5ce23928ee2e23a4e2f`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:41 GMT
ADD file:420712a90b0934202b326dc06b73638ab8e4603d12be2c23d67d834eb6cfc052 in / 
# Wed, 15 Sep 2021 17:39:42 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20210915
# Wed, 15 Sep 2021 17:39:42 GMT
CMD ["/bin/bash"]
# Sat, 18 Dec 2021 22:08:36 GMT
EXPOSE 5601
# Sat, 18 Dec 2021 22:09:44 GMT
RUN for iter in {1..10}; do       yum update --setopt=tsflags=nodocs -y &&       yum install --setopt=tsflags=nodocs -y         fontconfig freetype shadow-utils nss  &&       yum clean all && exit_code=0 && break || exit_code=$? && echo "yum error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code)
# Sat, 18 Dec 2021 22:09:48 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini
# Sat, 18 Dec 2021 22:09:48 GMT
RUN mkdir /usr/share/fonts/local
# Sat, 18 Dec 2021 22:09:51 GMT
RUN curl -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc
# Sat, 18 Dec 2021 22:09:52 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c -
# Sat, 18 Dec 2021 22:09:52 GMT
RUN fc-cache -v
# Sat, 18 Dec 2021 22:10:28 GMT
COPY --chown=1000:0dir:718a2dbb286ac29dec3fe8a243c2f9f57d62d3d3f3934b7b80ba3415274ca584 in /usr/share/kibana 
# Sat, 18 Dec 2021 22:10:32 GMT
WORKDIR /usr/share/kibana
# Sat, 18 Dec 2021 22:10:33 GMT
RUN ln -s /usr/share/kibana /opt/kibana
# Sat, 18 Dec 2021 22:10:33 GMT
ENV ELASTIC_CONTAINER=true
# Sat, 18 Dec 2021 22:10:33 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Dec 2021 22:10:33 GMT
COPY --chown=1000:0file:6db5413736a28ead04731f52a5ef1acaa8f3ca1c1d2eaf6bb2b80d8f232794a2 in /usr/share/kibana/config/kibana.yml 
# Sat, 18 Dec 2021 22:10:33 GMT
COPY file:4b05cc4ee8dc464b192dc25102b9385329fd96ca9e48428d3b36b7d2a9e4be58 in /usr/local/bin/ 
# Sat, 18 Dec 2021 22:10:35 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \;
# Sat, 18 Dec 2021 22:10:37 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} +
# Sat, 18 Dec 2021 22:10:37 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana
# Sat, 18 Dec 2021 22:10:38 GMT
LABEL org.label-schema.build-date=2021-12-18T22:05:22.047Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=9b678a13a6a3f45286f1d21856a7536a9297f42f org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.16.2 org.opencontainers.image.created=2021-12-18T22:05:22.047Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=9b678a13a6a3f45286f1d21856a7536a9297f42f org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.16.2
# Sat, 18 Dec 2021 22:10:38 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Sat, 18 Dec 2021 22:10:38 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Sat, 18 Dec 2021 22:10:38 GMT
USER kibana
```

-	Layers:
	-	`sha256:52f9ef134af7dd14738733e567402af86136287d9468978d044780a6435a1193`  
		Last Modified: Wed, 15 Sep 2021 17:40:42 GMT  
		Size: 83.9 MB (83941353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d829adaecdb949e43a3b99ef3339f4ac7d12e099d47a74da453d78e6d60045e`  
		Last Modified: Tue, 21 Dec 2021 00:41:45 GMT  
		Size: 94.4 MB (94358467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b147794101787503976957feb3fffd8db270796c37a316f5d05a7850280edc63`  
		Last Modified: Tue, 21 Dec 2021 00:41:30 GMT  
		Size: 9.1 KB (9094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a948fe82120e296f1917e7d9342b88a3566604248a28e906f1c40a4a926ecde5`  
		Last Modified: Tue, 21 Dec 2021 00:41:28 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa96d1fad6c1bafeab0e55c54e972f2367d8d36b23e1b8c61e6a44875ce96558`  
		Last Modified: Tue, 21 Dec 2021 00:41:30 GMT  
		Size: 16.5 MB (16460491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8fdff7556f49ae62ccc1c570fd7e72e1e946f18c346711309df38a26a4084a`  
		Last Modified: Tue, 21 Dec 2021 00:41:28 GMT  
		Size: 8.3 KB (8304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4029b7de6ab4bd2c15ab75925a8966754c37d4b22d8b4c16926b983332d42c`  
		Last Modified: Tue, 21 Dec 2021 00:42:08 GMT  
		Size: 300.6 MB (300607965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fede2c4304b2e977a4dd8cdb3775ca61217e0f4527d5d51f6f7136dd70d714a`  
		Last Modified: Tue, 21 Dec 2021 00:41:27 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f363a710f54e9dbf00dd0a5016cb6e597265f77171a0b58c8a62cbf927719ef`  
		Last Modified: Tue, 21 Dec 2021 00:41:25 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c210b27217b62c89ffea4e21bc369effabbc4eb32052c0a95aadfdc9a9e0f254`  
		Last Modified: Tue, 21 Dec 2021 00:41:25 GMT  
		Size: 4.5 KB (4488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e18d34b40ff579d6344a33b757accd4a972ea301b3498d9f6145288159b49b`  
		Last Modified: Tue, 21 Dec 2021 00:41:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c47c30ffbd5d06082539eab2ac369582cfc54e041f41ba7de6aac288b523db`  
		Last Modified: Tue, 21 Dec 2021 00:41:25 GMT  
		Size: 197.2 KB (197249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2edf0f691bad3fee4180726abadcd314c6ac76e8ceb8d9813a7430ae851fbd72`  
		Last Modified: Tue, 21 Dec 2021 00:41:25 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
