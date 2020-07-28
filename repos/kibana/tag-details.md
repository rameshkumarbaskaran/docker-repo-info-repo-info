<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:6.8.11`](#kibana6811)
-	[`kibana:7.8.1`](#kibana781)

## `kibana:6.8.11`

```console
$ docker pull kibana@sha256:d7483d3ffd9493b2adb8ad18b0648ef7b598dbeb3bf73057cb1f75a4b90c916c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kibana:6.8.11` - linux; amd64

```console
$ docker pull kibana@sha256:f421eddfd0eb4e5ff17dcd347aecc5a329452366fa81779a3cef2df13377cc77
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.3 MB (293295685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b83bdd97ee4713e81324b3fac44a233b12a5e0158c718f6870ebb5d73fa34e9`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 05 May 2020 21:20:06 GMT
ADD file:38e2d2a1a0cd8694bd5086f257fdf7504f0c2481bf4f746c9bd1c8d9f3f6430d in / 
# Tue, 05 May 2020 21:20:06 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200504 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-05-04 00:00:00+01:00
# Tue, 05 May 2020 21:20:07 GMT
CMD ["/bin/bash"]
# Thu, 09 Jul 2020 19:56:31 GMT
EXPOSE 5601
# Thu, 09 Jul 2020 19:57:04 GMT
RUN yum update -y && yum install -y fontconfig freetype && yum clean all
# Thu, 09 Jul 2020 19:57:55 GMT
COPY --chown=1000:0dir:b77b54be08243bf777b6255d65def2cd9c9ecf070856b76a0e1f6b9c6368650d in /usr/share/kibana 
# Thu, 09 Jul 2020 19:57:56 GMT
WORKDIR /usr/share/kibana
# Thu, 09 Jul 2020 19:57:58 GMT
RUN ln -s /usr/share/kibana /opt/kibana
# Thu, 09 Jul 2020 19:57:59 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 09 Jul 2020 19:57:59 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Jul 2020 19:57:59 GMT
COPY --chown=1000:0file:60b6181f28c99b362092ea6139b6d4112ddd0bef32d52563c33b26bdc2b51318 in /usr/share/kibana/config/kibana.yml 
# Thu, 09 Jul 2020 19:57:59 GMT
COPY --chown=1000:0file:7d472d1939e23e2f10e7c5fd1e9166eefd646214aa0d8a1c09d92af71c9cbd87 in /usr/local/bin/ 
# Thu, 09 Jul 2020 19:58:03 GMT
RUN chmod g+ws /usr/share/kibana && find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \;
# Thu, 09 Jul 2020 19:58:05 GMT
RUN groupadd --gid 1000 kibana && useradd --uid 1000 --gid 1000 --home-dir /usr/share/kibana --no-create-home kibana
# Thu, 09 Jul 2020 19:58:05 GMT
USER kibana
# Thu, 09 Jul 2020 19:58:06 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.label-schema.name=kibana org.label-schema.version=6.8.11 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.license=Elastic License license=Elastic License
# Thu, 09 Jul 2020 19:58:07 GMT
CMD ["/usr/local/bin/kibana-docker"]
```

-	Layers:
	-	`sha256:524b0c1e57f8ee5fee01a1decba2f301c324a6513ca3551021264e3aa7341ebc`  
		Last Modified: Tue, 05 May 2020 21:23:14 GMT  
		Size: 75.9 MB (75880141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80655dfbcc700a7891422b35967360aee6c5e9427eeb7b5b59178b69818da3a`  
		Last Modified: Mon, 27 Jul 2020 17:06:07 GMT  
		Size: 27.5 MB (27531780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c83a5ed1ccb2cdaccb69f8420b14f505e2a6fe929175b2149214f618bbdabad7`  
		Last Modified: Mon, 27 Jul 2020 17:10:09 GMT  
		Size: 189.9 MB (189879015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64fe1bc24a55665eeb505626612edf05b91a1a71cb916b2914ffd0686f64cfd`  
		Last Modified: Mon, 27 Jul 2020 17:09:37 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc806ab6b0a68deb67f7a61985072f294e8bdd1417517fc3a6f8bc8abe614076`  
		Last Modified: Mon, 27 Jul 2020 17:09:37 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a67753a8362153e026d2656112a40f807fc0fd9946d0d989656d0753c7fa7258`  
		Last Modified: Mon, 27 Jul 2020 17:09:37 GMT  
		Size: 2.3 KB (2261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64075ac1d8f9aae4ecef05307b878320f280728c05ae20c9e59588b81cd3a887`  
		Last Modified: Mon, 27 Jul 2020 17:09:35 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb9f2e2ea5e56beced1dbcea0696a16b56cc8c4b07e0849bd019af01333431d`  
		Last Modified: Mon, 27 Jul 2020 17:09:35 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kibana:7.8.1`

```console
$ docker pull kibana@sha256:0f1c2a8975555d80bcb16f76cf19c339477512c4fc3dcb07c227607d629ed638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kibana:7.8.1` - linux; amd64

```console
$ docker pull kibana@sha256:a1bcec7265740d8587bb80814bafb1aaab597f41ce9b2b437a0510742ed30f74
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.6 MB (444616833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22bc1dd9a48a0e5b1608a727ed860eb18492214758406db888ed01b67ab7c48e`
-	Entrypoint: `["\/usr\/local\/bin\/dumb-init","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 05 May 2020 21:20:06 GMT
ADD file:38e2d2a1a0cd8694bd5086f257fdf7504f0c2481bf4f746c9bd1c8d9f3f6430d in / 
# Tue, 05 May 2020 21:20:06 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200504 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-05-04 00:00:00+01:00
# Tue, 05 May 2020 21:20:07 GMT
CMD ["/bin/bash"]
# Tue, 21 Jul 2020 18:13:32 GMT
EXPOSE 5601
# Tue, 21 Jul 2020 18:14:10 GMT
RUN yum update -y && yum install -y fontconfig freetype shadow-utils && yum clean all
# Tue, 21 Jul 2020 18:14:19 GMT
RUN curl -L -o /usr/local/bin/dumb-init https://github.com/Yelp/dumb-init/releases/download/v1.2.2/dumb-init_1.2.2_amd64
# Tue, 21 Jul 2020 18:14:22 GMT
RUN echo "37f2c1f0372a45554f1b89924fbb134fc24c3756efaedf11e07f599494e0eff9  /usr/local/bin/dumb-init" | sha256sum -c -
# Tue, 21 Jul 2020 18:14:24 GMT
RUN chmod +x /usr/local/bin/dumb-init
# Tue, 21 Jul 2020 18:16:31 GMT
COPY --chown=1000:0dir:69c0f75eb61009adb93783ec56c0e680bbf68631e7e5e480bc0942206d28e467 in /usr/share/kibana 
# Tue, 21 Jul 2020 18:16:34 GMT
WORKDIR /usr/share/kibana
# Tue, 21 Jul 2020 18:16:35 GMT
RUN ln -s /usr/share/kibana /opt/kibana
# Tue, 21 Jul 2020 18:16:36 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 21 Jul 2020 18:16:36 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jul 2020 18:16:37 GMT
COPY --chown=1000:0file:ea1f294356f14dfc1a50e3303613e69f187589962058569d5b3282460d7f28cb in /usr/share/kibana/config/kibana.yml 
# Tue, 21 Jul 2020 18:16:37 GMT
COPY --chown=1000:0file:be27eaa94cf3ac359df3cf9e575e39c404657ad4c53e5ac0a89e8b6e5462d8e1 in /usr/local/bin/ 
# Tue, 21 Jul 2020 18:16:42 GMT
RUN chmod g+ws /usr/share/kibana && find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \;
# Tue, 21 Jul 2020 18:16:46 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} +
# Tue, 21 Jul 2020 18:16:50 GMT
RUN groupadd --gid 1000 kibana && useradd --uid 1000 --gid 1000 --home-dir /usr/share/kibana --no-create-home kibana
# Tue, 21 Jul 2020 18:16:51 GMT
USER kibana
# Tue, 21 Jul 2020 18:16:51 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.label-schema.name=kibana org.label-schema.version=7.8.1 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.license=Elastic License org.label-schema.usage=https://www.elastic.co/guide/en/kibana/index.html org.label-schema.build-date=2020-07-21T18:06:50.890Z license=Elastic License
# Tue, 21 Jul 2020 18:16:51 GMT
ENTRYPOINT ["/usr/local/bin/dumb-init" "--"]
# Tue, 21 Jul 2020 18:16:51 GMT
CMD ["/usr/local/bin/kibana-docker"]
```

-	Layers:
	-	`sha256:524b0c1e57f8ee5fee01a1decba2f301c324a6513ca3551021264e3aa7341ebc`  
		Last Modified: Tue, 05 May 2020 21:23:14 GMT  
		Size: 75.9 MB (75880141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aaca5b4b5e76ae99923c86bbee52d7d6d03ddc6be794dcbc19da9af1ce14bad`  
		Last Modified: Mon, 27 Jul 2020 21:38:45 GMT  
		Size: 27.9 MB (27875771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de3c0a7135336a6a887694f9fb000a95a7ebbdc23566a4f5ce00d081b7fc581`  
		Last Modified: Mon, 27 Jul 2020 21:38:36 GMT  
		Size: 31.7 KB (31691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfc04650be356178a6b89cbf6498ed8d71129954b6588da8853563c6b9d42051`  
		Last Modified: Mon, 27 Jul 2020 21:38:35 GMT  
		Size: 30.2 KB (30196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2844fa53159a88841583397dae267bee8ad126c7177a9f74984572f0dd8ee6`  
		Last Modified: Mon, 27 Jul 2020 23:23:48 GMT  
		Size: 340.6 MB (340592929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:933b2c17ef2d08ca1cb3f880841c6c69c1c7352a8f75c428b786affaf76b4012`  
		Last Modified: Mon, 27 Jul 2020 23:22:48 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:861d21ef358485eaf6da6dc654eeaf32b4771a9ae8d23a496e200dbc27ed1c32`  
		Last Modified: Mon, 27 Jul 2020 23:22:47 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dacdae3c06579560bcf6afbb4571bb4bee81a71f252fc12c6b731e66754aa774`  
		Last Modified: Mon, 27 Jul 2020 23:22:48 GMT  
		Size: 3.0 KB (3002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2334c2e8505935b62e53b7fc35658f938674ddcb24a74fe47eb3b1bef840e617`  
		Last Modified: Mon, 27 Jul 2020 23:22:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17854d19823013c1a86159388401e962e7240c0265bfbb56aec8e0b83bb73e7f`  
		Last Modified: Mon, 27 Jul 2020 21:38:31 GMT  
		Size: 200.6 KB (200615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17de503ad3fc5b5200cf7333ac4272478ec739c7ee3660246b779d245e0a22e7`  
		Last Modified: Mon, 27 Jul 2020 23:22:47 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
