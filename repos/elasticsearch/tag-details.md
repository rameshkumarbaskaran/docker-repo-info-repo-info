<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:6.8.14`](#elasticsearch6814)
-	[`elasticsearch:7.11.1`](#elasticsearch7111)

## `elasticsearch:6.8.14`

```console
$ docker pull elasticsearch@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `elasticsearch:7.11.1`

```console
$ docker pull elasticsearch@sha256:f21513208473cecc1cb571586545bc264bd03ae5db086555f5d66a72578255f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm64 variant v8

### `elasticsearch:7.11.1` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:d52cda1e73d1b1915ba2d76ca1e426620c7b5d6942d9d2f432259503974ba786
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.5 MB (419450068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71e6c5051b459d1a65ab0e63a014132940cad09a37f96ac403ff34a5b3ea3f0a`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 07 Dec 2020 23:42:06 GMT
ADD file:edd6e1253ec7bbb67b5a28d40c7d28b34a443c2cfa327bebf55c8b0b19484bf9 in / 
# Mon, 07 Dec 2020 23:42:09 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201204
# Mon, 07 Dec 2020 23:42:10 GMT
CMD ["/bin/bash"]
# Mon, 15 Feb 2021 14:50:11 GMT
RUN for iter in {1..10}; do       yum update --setopt=tsflags=nodocs -y &&       yum install --setopt=tsflags=nodocs -y       nc shadow-utils zip unzip  &&       yum clean all &&       exit_code=0 && break ||         exit_code=$? && echo "yum error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code
# Mon, 15 Feb 2021 14:50:12 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chmod 0775 /usr/share/elasticsearch &&     chown -R 1000:0 /usr/share/elasticsearch
# Mon, 15 Feb 2021 14:50:12 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 15 Feb 2021 14:50:12 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 15 Feb 2021 14:50:15 GMT
COPY --chown=1000:0dir:97cba44341a47b00f5b9029bc8e45e03a527a33c41dd7549c96a75d099b0ab93 in /usr/share/elasticsearch 
# Mon, 15 Feb 2021 14:50:18 GMT
COPY --chown=0:0file:1d48586bd42e8cf29bed9d4feee798b5c536660cc7b115750f0cd4f7bd33c311 in /bin/tini 
# Mon, 15 Feb 2021 14:50:18 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Feb 2021 14:50:19 GMT
COPY file:b60644ac0fe4cb4e2bab5fb75a5f9b33fa1cb8276d88703c138a52af6bd8ea5b in /usr/local/bin/docker-entrypoint.sh 
# Mon, 15 Feb 2021 14:50:19 GMT
RUN chmod g=u /etc/passwd &&     chmod 0775 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     ln -sf /etc/pki/ca-trust/extracted/java/cacerts /usr/share/elasticsearch/jdk/lib/security/cacerts
# Mon, 15 Feb 2021 14:50:19 GMT
EXPOSE 9200 9300
# Mon, 15 Feb 2021 14:50:19 GMT
LABEL org.label-schema.build-date=2021-02-15T14:49:09.995421Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=ff17057114c2199c9c1bbecc727003a907c0db7a org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.11.1 org.opencontainers.image.created=2021-02-15T14:49:09.995421Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=ff17057114c2199c9c1bbecc727003a907c0db7a org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.11.1
# Mon, 15 Feb 2021 14:50:20 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 15 Feb 2021 14:50:20 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:333cbcae3fb80b9a46084ae4caea81a84aafda9700fb646ab89206d0cfe213fd`  
		Last Modified: Mon, 07 Dec 2020 23:42:49 GMT  
		Size: 75.6 MB (75613064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdce518068f1a5fe2f653538db01e4806e08b76f85cf3344eccb53fc0cd9ac4e`  
		Last Modified: Mon, 22 Feb 2021 15:07:10 GMT  
		Size: 21.9 MB (21881970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d5ce99b6d274717ca2db7d3d217e1f1efaa4a2411930f2df86c68a5c9fd5e9`  
		Last Modified: Mon, 22 Feb 2021 15:06:52 GMT  
		Size: 2.4 KB (2369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934fbb2d1947b6daa8a220b39011497b069686e2b782284477ae2993c2b4bf98`  
		Last Modified: Mon, 22 Feb 2021 15:07:58 GMT  
		Size: 321.7 MB (321746475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e6009fbf2e601525a456a8bc66642ec9acb483947220052b8ea8c9df876966`  
		Last Modified: Mon, 22 Feb 2021 15:06:49 GMT  
		Size: 9.1 KB (9106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d0deff3ac23d892d9d8ea41a6349fbe2403bfa8273ac2f330148197c0cfb30`  
		Last Modified: Mon, 22 Feb 2021 15:06:49 GMT  
		Size: 1.9 KB (1946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eff4af5045c3407cb1d34da755ad89d6482c46c5aea56239ac7852feed0ec90`  
		Last Modified: Mon, 22 Feb 2021 15:06:44 GMT  
		Size: 195.1 KB (195138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
