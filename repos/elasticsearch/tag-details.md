<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:6.8.10`](#elasticsearch6810)
-	[`elasticsearch:7.8.0`](#elasticsearch780)

## `elasticsearch:6.8.10`

```console
$ docker pull elasticsearch@sha256:95d624106abc6d41340a736e2086d1d7b13d8334bee9a1c987f36fb0f9e6c16a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `elasticsearch:6.8.10` - linux; amd64

```console
$ docker pull elasticsearch@sha256:6c36fa585104d28d3a9e53c799a4e20058445476cadb3b3d3e789d3793eed10a
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.7 MB (462714490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa00077159cd4b5ac8cca1e84ec2c5d187d4395d459a661e2a901f0426c013f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 05 May 2020 21:20:06 GMT
ADD file:38e2d2a1a0cd8694bd5086f257fdf7504f0c2481bf4f746c9bd1c8d9f3f6430d in / 
# Tue, 05 May 2020 21:20:06 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200504 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-05-04 00:00:00+01:00
# Tue, 05 May 2020 21:20:07 GMT
CMD ["/bin/bash"]
# Thu, 28 May 2020 14:57:45 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 May 2020 14:57:45 GMT
ENV JAVA_HOME=/opt/jdk-14.0.1+7
# Thu, 28 May 2020 14:57:51 GMT
COPY dir:170319d0c30c0291abfea65bce51d4fa7bfdeba3e2278bcdd7c345f06cc9303d in /opt/jdk-14.0.1+7 
# Thu, 28 May 2020 14:58:06 GMT
RUN for iter in {1..10}; do yum update  --setopt=tsflags=nodocs -y &&     yum install -y  --setopt=tsflags=nodocs nc unzip wget which &&     yum clean all && exit_code=0 && break || exit_code=\$? && echo "yum error: retry $iter in 10s" && sleep 10; done;     (exit $exit_code)
# Thu, 28 May 2020 14:58:09 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chmod 0775 /usr/share/elasticsearch &&     chgrp 0 /usr/share/elasticsearch
# Thu, 28 May 2020 14:58:10 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 28 May 2020 14:58:15 GMT
COPY --chown=1000:0dir:e0d48488cb486bbdd0f929f36bd9589d20684922bb1d507041500d6bb0d91a72 in /usr/share/elasticsearch 
# Thu, 28 May 2020 14:58:16 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 May 2020 14:58:16 GMT
COPY --chown=1000:0file:08193f849fc25f29db1438eff6d5c9fe1d63237aeb07a3e0009e8ba554f97c31 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 28 May 2020 14:58:18 GMT
RUN chgrp 0 /usr/local/bin/docker-entrypoint.sh &&     chmod g=u /etc/passwd &&     chmod 0775 /usr/local/bin/docker-entrypoint.sh
# Thu, 28 May 2020 14:58:18 GMT
EXPOSE 9200 9300
# Thu, 28 May 2020 14:58:18 GMT
LABEL org.label-schema.build-date=2020-05-28T14:47:19.882936Z org.label-schema.license=Elastic-License org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=537cb22e7ffb62ee541e1af1881d18e3a78e6133 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=6.8.10 org.opencontainers.image.created=2020-05-28T14:47:19.882936Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License org.opencontainers.image.revision=537cb22e7ffb62ee541e1af1881d18e3a78e6133 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=6.8.10
# Thu, 28 May 2020 14:58:18 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 28 May 2020 14:58:19 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:524b0c1e57f8ee5fee01a1decba2f301c324a6513ca3551021264e3aa7341ebc`  
		Last Modified: Tue, 05 May 2020 21:23:14 GMT  
		Size: 75.9 MB (75880141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf34341d86d3d59e99d027d4fc69731cf8cb9b71d90381af2fc707e97e1fb1b`  
		Last Modified: Wed, 03 Jun 2020 14:50:57 GMT  
		Size: 211.9 MB (211934763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:551de3bae6fbdc0ce3dd44e4b669368ea613081815c1cb977dd924d5a960123a`  
		Last Modified: Wed, 03 Jun 2020 14:50:36 GMT  
		Size: 23.9 MB (23934482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68cc3405237863a7d97735ee56d391c4260ed50caacde466cd099943f32fdbd6`  
		Last Modified: Wed, 03 Jun 2020 14:50:32 GMT  
		Size: 2.3 KB (2276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bab9bbf7644c2c0fb4ee67a14e690f56316325c9196683a20338ca0f9451032`  
		Last Modified: Wed, 03 Jun 2020 14:50:51 GMT  
		Size: 151.0 MB (150958368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52184024c46082b666e5c1e775619ca7a297d8a50afe259ce32d329e19541b84`  
		Last Modified: Wed, 03 Jun 2020 14:50:32 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80935e4ae0b9ed4a2ca533a27c8363587b2e4c0421001dc9f2459829108ae265`  
		Last Modified: Wed, 03 Jun 2020 14:50:32 GMT  
		Size: 2.4 KB (2400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `elasticsearch:7.8.0`

```console
$ docker pull elasticsearch@sha256:945f80960f2ad1bd4b88bd07a9ba160d22d4285bbc8a720d052379006d5d57a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `elasticsearch:7.8.0` - linux; amd64

```console
$ docker pull elasticsearch@sha256:4a65567332214e36b3ad7fcb0c4f00d87f16edba57d0c4f2c7938b6014041ca3
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.9 MB (420949077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121454ddad72df47aa5726e7634dc16f5ed764b08b90aed848a48d625fde4d8b`
-	Entrypoint: `["\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 05 May 2020 21:20:06 GMT
ADD file:38e2d2a1a0cd8694bd5086f257fdf7504f0c2481bf4f746c9bd1c8d9f3f6430d in / 
# Tue, 05 May 2020 21:20:06 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200504 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-05-04 00:00:00+01:00
# Tue, 05 May 2020 21:20:07 GMT
CMD ["/bin/bash"]
# Sun, 14 Jun 2020 19:39:50 GMT
ENV ELASTIC_CONTAINER=true
# Sun, 14 Jun 2020 19:39:50 GMT
COPY file:df9158ae8b9b283e8ea5bd72d1e344c08dea733e283f9f0941833f467466323c in /tini 
# Sun, 14 Jun 2020 19:40:09 GMT
RUN for iter in {1..10}; do yum update --setopt=tsflags=nodocs -y &&     yum install --setopt=tsflags=nodocs -y nc shadow-utils zip unzip &&     yum clean all && exit_code=0 && break || exit_code=$? && echo "yum error: retry $iter in 10s" && sleep 10; done;     (exit $exit_code)
# Sun, 14 Jun 2020 19:40:10 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chmod 0775 /usr/share/elasticsearch &&     chgrp 0 /usr/share/elasticsearch
# Sun, 14 Jun 2020 19:40:10 GMT
WORKDIR /usr/share/elasticsearch
# Sun, 14 Jun 2020 19:40:22 GMT
COPY --chown=1000:0dir:c2fba1dee7a6041253b333e3a27e60f1f855853e7b839cbf37fe0a599ce00793 in /usr/share/elasticsearch 
# Sun, 14 Jun 2020 19:40:23 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts /usr/share/elasticsearch/jdk/lib/security/cacerts
# Sun, 14 Jun 2020 19:40:23 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 14 Jun 2020 19:40:24 GMT
COPY file:d964df1452418918baf1d29ee20df18c9648ca6c9d51764640fca470bd9a9366 in /usr/local/bin/docker-entrypoint.sh 
# Sun, 14 Jun 2020 19:40:25 GMT
RUN chmod g=u /etc/passwd &&     chmod 0775 /usr/local/bin/docker-entrypoint.sh
# Sun, 14 Jun 2020 19:40:26 GMT
RUN find / -xdev -perm -4000 -exec chmod ug-s {} +
# Sun, 14 Jun 2020 19:40:26 GMT
EXPOSE 9200 9300
# Sun, 14 Jun 2020 19:40:26 GMT
LABEL org.label-schema.build-date=2020-06-14T19:35:50.234439Z org.label-schema.license=Elastic-License org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=757314695644ea9a1dc2fecd26d1a43856725e65 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.8.0 org.opencontainers.image.created=2020-06-14T19:35:50.234439Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License org.opencontainers.image.revision=757314695644ea9a1dc2fecd26d1a43856725e65 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.8.0
# Sun, 14 Jun 2020 19:40:26 GMT
ENTRYPOINT ["/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Sun, 14 Jun 2020 19:40:26 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:524b0c1e57f8ee5fee01a1decba2f301c324a6513ca3551021264e3aa7341ebc`  
		Last Modified: Tue, 05 May 2020 21:23:14 GMT  
		Size: 75.9 MB (75880141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a096b8f20be15fbba037cdd0cb24101af40e9f74fb5cf3031a350d13aced548`  
		Last Modified: Thu, 18 Jun 2020 19:46:40 GMT  
		Size: 9.5 KB (9462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd8117fbfec5c22d8b96bd9c71111ca298bfcf2518932aee9300b5d2529a289`  
		Last Modified: Thu, 18 Jun 2020 19:46:45 GMT  
		Size: 24.0 MB (23985066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:335891dbdd0eb7f9bfddf1d8b15f73ef408abd9a637692aa3b7f6bc0591ca869`  
		Last Modified: Thu, 18 Jun 2020 19:46:40 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfce820717b417ccf8c29f3ceb2cfe8f776469ba5c824efd24a04c2caa452888`  
		Last Modified: Thu, 18 Jun 2020 19:47:11 GMT  
		Size: 320.9 MB (320867443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d3459719f7f8c21b7c7cb612d66d2d07b5170258e7c1be5c8ad06bd2b0f9ce`  
		Last Modified: Thu, 18 Jun 2020 19:46:39 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e79822fece3572e24b83984043214778659bb2d89ab716cf5f863dc0bcd2afa`  
		Last Modified: Thu, 18 Jun 2020 19:46:39 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f80b981dd6a20a8e704856a66cfcb1db267f75951d49e227b448f9ac760dc2b`  
		Last Modified: Thu, 18 Jun 2020 19:46:39 GMT  
		Size: 2.1 KB (2067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f8a08da0ba9eef419fde5105d98d48ecfac86b0970d4940ae1d12d57f7bf56`  
		Last Modified: Thu, 18 Jun 2020 19:46:39 GMT  
		Size: 200.6 KB (200612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elasticsearch:7.8.0` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:4a7bc78dc22de5e73a435382028fdb18b2028352919015b42d3aa6e9e014920e
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **646.6 MB (646599873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9522ad0a773f16d4a81de35c478bedecae5e668fab3011d39a3b85eb8f6f973e`
-	Entrypoint: `["\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 05 May 2020 21:41:25 GMT
ADD file:d64254c17612e9076d442240e4e567c0467ab6c4ca282ba5553f602805ad89ac in / 
# Tue, 05 May 2020 21:41:30 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200504 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-05-04 00:00:00+01:00
# Tue, 05 May 2020 21:41:31 GMT
CMD ["/bin/bash"]
# Sun, 14 Jun 2020 22:41:39 GMT
ENV ELASTIC_CONTAINER=true
# Sun, 14 Jun 2020 22:41:39 GMT
COPY file:71bfd2daffa1277e243209a08921f2609e22adbf82217ed08c071eb3a2ddca8a in /tini 
# Sun, 14 Jun 2020 22:42:31 GMT
RUN for iter in {1..10}; do yum update --setopt=tsflags=nodocs -y &&     yum install --setopt=tsflags=nodocs -y nc shadow-utils zip unzip &&     yum clean all && exit_code=0 && break || exit_code=$? && echo "yum error: retry $iter in 10s" && sleep 10; done;     (exit $exit_code)
# Sun, 14 Jun 2020 22:42:35 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chmod 0775 /usr/share/elasticsearch &&     chgrp 0 /usr/share/elasticsearch
# Sun, 14 Jun 2020 22:42:35 GMT
WORKDIR /usr/share/elasticsearch
# Sun, 14 Jun 2020 22:42:37 GMT
COPY --chown=1000:0dir:659e6fe31c32a1d0941c144c4cb0456843c8adaf8d76ee0c26c33bf7a7fffec5 in /usr/share/elasticsearch 
# Sun, 14 Jun 2020 22:42:45 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts /usr/share/elasticsearch/jdk/lib/security/cacerts
# Sun, 14 Jun 2020 22:42:45 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 14 Jun 2020 22:42:45 GMT
COPY file:d964df1452418918baf1d29ee20df18c9648ca6c9d51764640fca470bd9a9366 in /usr/local/bin/docker-entrypoint.sh 
# Sun, 14 Jun 2020 22:42:46 GMT
RUN chmod g=u /etc/passwd &&     chmod 0775 /usr/local/bin/docker-entrypoint.sh
# Sun, 14 Jun 2020 22:42:47 GMT
RUN find / -xdev -perm -4000 -exec chmod ug-s {} +
# Sun, 14 Jun 2020 22:42:47 GMT
EXPOSE 9200 9300
# Sun, 14 Jun 2020 22:42:47 GMT
LABEL org.label-schema.build-date=2020-06-14T22:39:12.009735Z org.label-schema.license=Elastic-License org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=757314695644ea9a1dc2fecd26d1a43856725e65 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.8.0 org.opencontainers.image.created=2020-06-14T22:39:12.009735Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License org.opencontainers.image.revision=757314695644ea9a1dc2fecd26d1a43856725e65 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.8.0
# Sun, 14 Jun 2020 22:42:48 GMT
ENTRYPOINT ["/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Sun, 14 Jun 2020 22:42:48 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:ae60b79047f8473e02511e923f461b869b62d2bf110b9fa282656e9f0128932d`  
		Last Modified: Tue, 05 May 2020 21:42:11 GMT  
		Size: 104.6 MB (104555376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7045b895c5ed80fdd5cea557b7ef7cdd57dca946cbeae64e51ef78438ee3ed09`  
		Last Modified: Thu, 18 Jun 2020 21:47:31 GMT  
		Size: 9.0 KB (9037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396c5afd8c56a4d0ab4ba3d0a3d8a56f5f2b331b1e211e0ed84a23f85baace78`  
		Last Modified: Thu, 18 Jun 2020 21:48:10 GMT  
		Size: 223.9 MB (223921898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748e538016955c2c58fcedcc30ed2c53d4a940520d846d9b19784dc7f679d4ee`  
		Last Modified: Thu, 18 Jun 2020 21:47:31 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ab8b9fd19a6ee0263933c7bdb8d996c045fb16dff54296d70cc8852500bed3`  
		Last Modified: Thu, 18 Jun 2020 21:48:14 GMT  
		Size: 317.9 MB (317890812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64847ece58a510f0b2b5d81fc931bc3ab0b0013c54f71cc91edfcb3ccfe1ac13`  
		Last Modified: Thu, 18 Jun 2020 21:47:29 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6090b0f571c2c1af39d00c0ec3d428d03fe11cd866b414fc81d03654f826fa3`  
		Last Modified: Thu, 18 Jun 2020 21:47:29 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d51c4c733b8652ca2ca654210f344e3958b156fc40e86b30c513f4eeeea6634`  
		Last Modified: Thu, 18 Jun 2020 21:47:29 GMT  
		Size: 2.1 KB (2064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8cfbc8fa09218491498526a78b3cb155867f017e5417588c9f591bcb47d803`  
		Last Modified: Thu, 18 Jun 2020 21:47:29 GMT  
		Size: 216.4 KB (216374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
