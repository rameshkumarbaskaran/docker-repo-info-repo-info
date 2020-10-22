<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:6.8.13`](#elasticsearch6813)
-	[`elasticsearch:7.9.3`](#elasticsearch793)

## `elasticsearch:6.8.13`

```console
$ docker pull elasticsearch@sha256:8d4e29332dc159e7c256efa131453bd62a35b6e90f32aa9ab3f76632e29372c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `elasticsearch:6.8.13` - linux; amd64

```console
$ docker pull elasticsearch@sha256:8a1fe3c94950c07fa156aec633b7fc946cd81645b8c48e306535da675a69fc6c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.8 MB (440820933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e1d4b5ee814bc6c25cb4c8a2ee7950f25ca0f7621005405484b94b40e0f976`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 10 Aug 2020 18:20:08 GMT
ADD file:61908381d3142ffba798ae9a904476d19b197ab79d0338f14bec0f76649df8d4 in / 
# Mon, 10 Aug 2020 18:20:09 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200809 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-08-09 00:00:00+01:00
# Mon, 10 Aug 2020 18:20:09 GMT
CMD ["/bin/bash"]
# Fri, 16 Oct 2020 09:18:17 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 16 Oct 2020 09:18:18 GMT
ENV JAVA_HOME=/opt/jdk-15+36
# Fri, 16 Oct 2020 09:18:24 GMT
COPY dir:d78ffb599e9e9b4589ff70ac49aaeab0c8bd3455dac60ff715fb156774755752 in /opt/jdk-15+36 
# Fri, 16 Oct 2020 09:18:34 GMT
RUN for iter in {1..10}; do yum update  --setopt=tsflags=nodocs -y &&     yum install -y  --setopt=tsflags=nodocs nc unzip wget which &&     yum clean all && exit_code=0 && break || exit_code=\$? && echo "yum error: retry $iter in 10s" && sleep 10; done;     (exit $exit_code)
# Fri, 16 Oct 2020 09:18:36 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chmod 0775 /usr/share/elasticsearch &&     chgrp 0 /usr/share/elasticsearch
# Fri, 16 Oct 2020 09:18:37 GMT
WORKDIR /usr/share/elasticsearch
# Fri, 16 Oct 2020 09:18:43 GMT
COPY --chown=1000:0dir:787d275540a0eea8d7d841a45f6cec0bfb0a080933199b53aa7a277315198546 in /usr/share/elasticsearch 
# Fri, 16 Oct 2020 09:18:43 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Oct 2020 09:18:44 GMT
COPY --chown=1000:0file:08193f849fc25f29db1438eff6d5c9fe1d63237aeb07a3e0009e8ba554f97c31 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Oct 2020 09:18:45 GMT
RUN chgrp 0 /usr/local/bin/docker-entrypoint.sh &&     chmod g=u /etc/passwd &&     chmod 0775 /usr/local/bin/docker-entrypoint.sh
# Fri, 16 Oct 2020 09:18:45 GMT
EXPOSE 9200 9300
# Fri, 16 Oct 2020 09:18:45 GMT
LABEL org.label-schema.build-date=2020-10-16T09:09:46.555371Z org.label-schema.license=Elastic-License org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=be13c699d0ab4706ec25626375b0965e3cdfa138 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=6.8.13 org.opencontainers.image.created=2020-10-16T09:09:46.555371Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License org.opencontainers.image.revision=be13c699d0ab4706ec25626375b0965e3cdfa138 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=6.8.13
# Fri, 16 Oct 2020 09:18:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Fri, 16 Oct 2020 09:18:46 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:75f829a71a1c5277a7abf55495ac8d16759691d980bf1d931795e5eb68a294c0`  
		Last Modified: Mon, 10 Aug 2020 18:21:46 GMT  
		Size: 75.9 MB (75863188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ddf21112a95c2b297c9501907ea7830e6e4a56044aa9a64628e5bc4db52e157`  
		Last Modified: Thu, 22 Oct 2020 13:53:03 GMT  
		Size: 207.6 MB (207649973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9eb3eb5dbd4f6e0f58a238f77287efcd8d0493f75a967ee0bb85560786b031f`  
		Last Modified: Thu, 22 Oct 2020 13:52:30 GMT  
		Size: 7.2 MB (7197391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec630f80209e807986f3133930339442edbade997649eb1c85c0edb0d215f1db`  
		Last Modified: Thu, 22 Oct 2020 13:52:28 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c6cedc99d3f0ee71111a79c397e76c8c0e3a5efa5ae0224dab1bdd664a9356`  
		Last Modified: Thu, 22 Oct 2020 13:52:40 GMT  
		Size: 150.1 MB (150103638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370a8f20dfc6929720417e888382d2edf8e28e28854d275f00129e7cbe9a1d14`  
		Last Modified: Thu, 22 Oct 2020 13:52:25 GMT  
		Size: 2.1 KB (2061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3feb9e7bea81267646c5a5db3fa9bd4f43cccf91081d1e8def3a4d3c5ec048a4`  
		Last Modified: Thu, 22 Oct 2020 13:52:25 GMT  
		Size: 2.4 KB (2402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `elasticsearch:7.9.3`

```console
$ docker pull elasticsearch@sha256:a13cd87cbf139fadbca64972ef2c8777222236887d303e4177c1ab7cff1b52f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `elasticsearch:7.9.3` - linux; amd64

```console
$ docker pull elasticsearch@sha256:b153829871d83cea307fcfdfb245c9981d8036847064ce89df645a49bcf8c1d9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.4 MB (391381798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ab13f928dc8aa958574d060fde595bd7715c1c2d3260446356a6a02d231e168`
-	Entrypoint: `["\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 10 Aug 2020 18:20:08 GMT
ADD file:61908381d3142ffba798ae9a904476d19b197ab79d0338f14bec0f76649df8d4 in / 
# Mon, 10 Aug 2020 18:20:09 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200809 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-08-09 00:00:00+01:00
# Mon, 10 Aug 2020 18:20:09 GMT
CMD ["/bin/bash"]
# Fri, 16 Oct 2020 10:40:21 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 16 Oct 2020 10:40:22 GMT
COPY file:df9158ae8b9b283e8ea5bd72d1e344c08dea733e283f9f0941833f467466323c in /tini 
# Fri, 16 Oct 2020 10:40:47 GMT
RUN for iter in {1..10}; do yum update --setopt=tsflags=nodocs -y &&     yum install --setopt=tsflags=nodocs -y nc shadow-utils zip unzip &&     yum clean all && exit_code=0 && break || exit_code=$? && echo "yum error: retry $iter in 10s" && sleep 10; done;     (exit $exit_code)
# Fri, 16 Oct 2020 10:40:48 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chmod 0775 /usr/share/elasticsearch &&     chgrp 0 /usr/share/elasticsearch
# Fri, 16 Oct 2020 10:40:48 GMT
WORKDIR /usr/share/elasticsearch
# Fri, 16 Oct 2020 10:41:01 GMT
COPY --chown=1000:0dir:bb3f56af31f79ace647b634b7bbf77edee9655f8d4de9dc15176282e8da544ce in /usr/share/elasticsearch 
# Fri, 16 Oct 2020 10:41:02 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts /usr/share/elasticsearch/jdk/lib/security/cacerts
# Fri, 16 Oct 2020 10:41:02 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Oct 2020 10:41:02 GMT
COPY file:d964df1452418918baf1d29ee20df18c9648ca6c9d51764640fca470bd9a9366 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Oct 2020 10:41:03 GMT
RUN chmod g=u /etc/passwd &&     chmod 0775 /usr/local/bin/docker-entrypoint.sh
# Fri, 16 Oct 2020 10:41:04 GMT
RUN find / -xdev -perm -4000 -exec chmod ug-s {} +
# Fri, 16 Oct 2020 10:41:04 GMT
EXPOSE 9200 9300
# Fri, 16 Oct 2020 10:41:05 GMT
LABEL org.label-schema.build-date=2020-10-16T10:36:16.141335Z org.label-schema.license=Elastic-License org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c4138e51121ef06a6404866cddc601906fe5c868 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.9.3 org.opencontainers.image.created=2020-10-16T10:36:16.141335Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License org.opencontainers.image.revision=c4138e51121ef06a6404866cddc601906fe5c868 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.9.3
# Fri, 16 Oct 2020 10:41:05 GMT
ENTRYPOINT ["/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Fri, 16 Oct 2020 10:41:05 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:75f829a71a1c5277a7abf55495ac8d16759691d980bf1d931795e5eb68a294c0`  
		Last Modified: Mon, 10 Aug 2020 18:21:46 GMT  
		Size: 75.9 MB (75863188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd8aabff66579d4af7fee16d78cd1da41b5cb1b061200d8679922a80040273c`  
		Last Modified: Thu, 22 Oct 2020 14:03:51 GMT  
		Size: 9.5 KB (9462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd17121b3976ef6597ade0621cffa8927c3bff995da7a653a608b5461c15dcb3`  
		Last Modified: Thu, 22 Oct 2020 14:03:52 GMT  
		Size: 7.2 MB (7239498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19cf707b4fd6d2709e0690ad6d3f9cdfdc92c3f97ca4f193c934d76db03f99e`  
		Last Modified: Thu, 22 Oct 2020 14:03:51 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ccdd8a52dc05e5935acf607b46064583fa65b40d80612891e3a35ff70acf735`  
		Last Modified: Thu, 22 Oct 2020 14:04:13 GMT  
		Size: 308.1 MB (308062691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d018d3fc07a49cc2a27cbbc76749dfd77f38684c7482b4b11c10f7a91bfb06e0`  
		Last Modified: Thu, 22 Oct 2020 14:03:47 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f1e3a1960ad99468199edd036fe3b559f10fe76fea90b83e0d853bad203eb0`  
		Last Modified: Thu, 22 Oct 2020 14:03:47 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f58f7e426faeec7f759789d0841d26ff296fcfda8d64a72e51fc4af8f3e1aea`  
		Last Modified: Thu, 22 Oct 2020 14:03:45 GMT  
		Size: 2.1 KB (2062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:817feb91b55c590cde52765064649bf5b6188541e13c499d977fe1a472893272`  
		Last Modified: Thu, 22 Oct 2020 14:03:46 GMT  
		Size: 200.6 KB (200611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elasticsearch:7.9.3` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:3f6d27fcbfd3b2fb843c72cec02be88c8887cb39f840dec536e963953f1bb6d6
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.1 MB (403121321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32bb4bf1ee4231fdea29a3d95b27317a370561bb480c4417e0f35e2989099964`
-	Entrypoint: `["\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 10 Aug 2020 18:40:15 GMT
ADD file:bd33d5894d5b88d0234cb910fde969eb9864ff572b5f9c61d7e847e0d25eab07 in / 
# Mon, 10 Aug 2020 18:40:21 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200809 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-08-09 00:00:00+01:00
# Mon, 10 Aug 2020 18:40:21 GMT
CMD ["/bin/bash"]
# Fri, 16 Oct 2020 13:36:49 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 16 Oct 2020 13:36:49 GMT
COPY file:71bfd2daffa1277e243209a08921f2609e22adbf82217ed08c071eb3a2ddca8a in /tini 
# Fri, 16 Oct 2020 13:36:54 GMT
RUN for iter in {1..10}; do yum update --setopt=tsflags=nodocs -y &&     yum install --setopt=tsflags=nodocs -y nc shadow-utils zip unzip &&     yum clean all && exit_code=0 && break || exit_code=$? && echo "yum error: retry $iter in 10s" && sleep 10; done;     (exit $exit_code)
# Fri, 16 Oct 2020 13:36:55 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chmod 0775 /usr/share/elasticsearch &&     chgrp 0 /usr/share/elasticsearch
# Fri, 16 Oct 2020 13:36:55 GMT
WORKDIR /usr/share/elasticsearch
# Fri, 16 Oct 2020 13:36:57 GMT
COPY --chown=1000:0dir:e9f587e2d5dab007eb4aa0aed7911dbfea9696223b6e6a3a0cc964c47408997b in /usr/share/elasticsearch 
# Fri, 16 Oct 2020 13:37:00 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts /usr/share/elasticsearch/jdk/lib/security/cacerts
# Fri, 16 Oct 2020 13:37:00 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Oct 2020 13:37:00 GMT
COPY file:d964df1452418918baf1d29ee20df18c9648ca6c9d51764640fca470bd9a9366 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Oct 2020 13:37:01 GMT
RUN chmod g=u /etc/passwd &&     chmod 0775 /usr/local/bin/docker-entrypoint.sh
# Fri, 16 Oct 2020 13:37:02 GMT
RUN find / -xdev -perm -4000 -exec chmod ug-s {} +
# Fri, 16 Oct 2020 13:37:02 GMT
EXPOSE 9200 9300
# Fri, 16 Oct 2020 13:37:02 GMT
LABEL org.label-schema.build-date=2020-10-16T13:34:25.304557Z org.label-schema.license=Elastic-License org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c4138e51121ef06a6404866cddc601906fe5c868 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.9.3 org.opencontainers.image.created=2020-10-16T13:34:25.304557Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License org.opencontainers.image.revision=c4138e51121ef06a6404866cddc601906fe5c868 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.9.3
# Fri, 16 Oct 2020 13:37:02 GMT
ENTRYPOINT ["/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Fri, 16 Oct 2020 13:37:02 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:9f74aa7d9ab9b412a3fcf68bb81925361c12040976f82e40aec2a10d83fb0ec6`  
		Last Modified: Mon, 10 Aug 2020 18:41:57 GMT  
		Size: 107.3 MB (107331333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787a765508d83b81a105c6a43f8fb0f67fa00b18656c04bad47047df641f9223`  
		Last Modified: Thu, 22 Oct 2020 22:40:10 GMT  
		Size: 9.0 KB (9037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab593d6f94598de2bef9440a2a06fc8cce1b96b00eae75ca699a84c570f31efc`  
		Last Modified: Thu, 22 Oct 2020 22:40:11 GMT  
		Size: 7.0 MB (6977580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d61aced22a4d6976f49c49d8bcc1e01f0d77da373df9774a6f028b9de12438d`  
		Last Modified: Thu, 22 Oct 2020 22:40:08 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dbba22529658fbadcac739581a818908f70555015aa6ba1acd9c6ed3a64e24b`  
		Last Modified: Thu, 22 Oct 2020 22:40:44 GMT  
		Size: 288.6 MB (288585974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d439482a940dc418802d2b7ff57e7e774393ae03044c2b576639b73cf5d1c8`  
		Last Modified: Thu, 22 Oct 2020 22:40:06 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f506bcb6c300559d550ec0ba529b9a0319db5f42c6c50336b089c93d49672d8b`  
		Last Modified: Thu, 22 Oct 2020 22:40:06 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fccbde717d0f6ec3ed7f4fd38591cf4afe6742e4c012e5e01b1588e53db4a132`  
		Last Modified: Thu, 22 Oct 2020 22:40:06 GMT  
		Size: 2.1 KB (2063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f396ba01a7bc6003f095a74d00858f3f8a486ceab5aad74a11fd7acf2ff06218`  
		Last Modified: Thu, 22 Oct 2020 22:40:08 GMT  
		Size: 211.0 KB (211026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
