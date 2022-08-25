<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:6.8.23`](#elasticsearch6823)
-	[`elasticsearch:7.17.6`](#elasticsearch7176)
-	[`elasticsearch:8.4.0`](#elasticsearch840)

## `elasticsearch:6.8.23`

```console
$ docker pull elasticsearch@sha256:deda76957c8cacc5dbf0d535fd14fe365f37d839813099bc32f26390a5e232dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `elasticsearch:6.8.23` - linux; amd64

```console
$ docker pull elasticsearch@sha256:71d4f7d890b90d277a1677d53f100139dcb39a34e9aac1138bfbf272c878a9cf
```

-	Docker Version: 20.10.10
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.7 MB (492666994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a2652c5f453b2f21ac32f841a6ed1897097741d69a1a4cc1947f58fae0d04b4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Thu, 06 Jan 2022 21:35:20 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 06 Jan 2022 21:35:21 GMT
ENV JAVA_HOME=/opt/jdk-15.0.1+9
# Thu, 06 Jan 2022 21:35:26 GMT
COPY dir:8d79ae5f21bb18379c0d92b3d252f4730fec22a4509252ec794212b8f72bd7af in /opt/jdk-15.0.1+9 
# Thu, 06 Jan 2022 21:36:34 GMT
RUN for iter in {1..10}; do yum update  --setopt=tsflags=nodocs -y &&     yum install -y  --setopt=tsflags=nodocs nc unzip wget which &&     yum clean all && exit_code=0 && break || exit_code=\$? && echo "yum error: retry $iter in 10s" && sleep 10; done;     (exit $exit_code)
# Thu, 06 Jan 2022 21:36:38 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chmod 0775 /usr/share/elasticsearch &&     chgrp 0 /usr/share/elasticsearch
# Thu, 06 Jan 2022 21:36:38 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 06 Jan 2022 21:36:42 GMT
COPY --chown=1000:0dir:b97ce01feda46ea896b080aa40faf3a7efc9341727b688e691ee0eac86058c3a in /usr/share/elasticsearch 
# Thu, 06 Jan 2022 21:36:43 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jan 2022 21:36:44 GMT
COPY --chown=1000:0file:08193f849fc25f29db1438eff6d5c9fe1d63237aeb07a3e0009e8ba554f97c31 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 06 Jan 2022 21:36:45 GMT
RUN chgrp 0 /usr/local/bin/docker-entrypoint.sh &&     chmod g=u /etc/passwd &&     chmod 0775 /usr/local/bin/docker-entrypoint.sh
# Thu, 06 Jan 2022 21:36:46 GMT
EXPOSE 9200 9300
# Thu, 06 Jan 2022 21:36:46 GMT
LABEL org.label-schema.build-date=2022-01-06T21:30:50.087716Z org.label-schema.license=Elastic-License org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=4f67856884ff580d8b48a858411b8c17cb0f8cdb org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=6.8.23 org.opencontainers.image.created=2022-01-06T21:30:50.087716Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License org.opencontainers.image.revision=4f67856884ff580d8b48a858411b8c17cb0f8cdb org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=6.8.23
# Thu, 06 Jan 2022 21:36:46 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 06 Jan 2022 21:36:46 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d2262411d0f2af035c2e0f0c62814960b3e7d77eecab02eba9f97819d00d2e`  
		Last Modified: Thu, 13 Jan 2022 16:11:26 GMT  
		Size: 207.7 MB (207657716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:affa3bfe04943870deba40892398c3fc9d08da9825ea7953984632c74e4994bd`  
		Last Modified: Thu, 13 Jan 2022 16:11:18 GMT  
		Size: 58.2 MB (58240591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e780d91c9f56dc0a05ae8916a4e8d6738cf94ed5cf924534d41236da5fb38f`  
		Last Modified: Thu, 13 Jan 2022 16:11:06 GMT  
		Size: 2.3 KB (2315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2471af457050139c5057c781433abadb769786df91ecbe6ed2a59b5f85e50369`  
		Last Modified: Thu, 13 Jan 2022 16:11:20 GMT  
		Size: 150.7 MB (150664745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca890dfc68d05cdbdd9a7f528fbe8707c05d71e8c0c985307da6797ad204eb49`  
		Last Modified: Thu, 13 Jan 2022 16:11:05 GMT  
		Size: 2.1 KB (2065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd85b0b895822b5794063d98df42deeb3f0110f505b79fff7abc26f54f70a9c5`  
		Last Modified: Thu, 13 Jan 2022 16:11:05 GMT  
		Size: 2.4 KB (2405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `elasticsearch:7.17.6`

```console
$ docker pull elasticsearch@sha256:2889c7e071357eb2c7e7e1577961c67ba3336239fedf8d9a0d289fe1aab032ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `elasticsearch:7.17.6` - linux; amd64

```console
$ docker pull elasticsearch@sha256:46584db983c753d7ea74169eeffa83eefef54e49c4bfeb63b2ee243f3a3ec690
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.2 MB (347150274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fad10241ffd65d817ed0ddfaf6e87eee1f7dc2a7db33db1047835560ea71fda`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 15:08:24 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code
# Tue, 23 Aug 2022 15:08:25 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch
# Tue, 23 Aug 2022 15:08:25 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 23 Aug 2022 15:08:26 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 23 Aug 2022 15:08:34 GMT
COPY --chown=0:0dir:968aeb02bc3cf00dd536456d0cd1935c740040c9a93bcd93dfa0c0bbe958b24e in /usr/share/elasticsearch 
# Tue, 23 Aug 2022 15:08:36 GMT
COPY --chown=0:0file:fcc427e6b1b34164533c7d80cf8bba68e6f09d5c7d442ca055586359d7076e62 in /bin/tini 
# Tue, 23 Aug 2022 15:08:36 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Aug 2022 15:08:36 GMT
COPY file:35bdfc6ad8079cb9cab605169a09ebfe8ce26cd4a9e4120efe12f418073a9bfb in /usr/local/bin/docker-entrypoint.sh 
# Tue, 23 Aug 2022 15:08:37 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins
# Tue, 23 Aug 2022 15:08:37 GMT
COPY file:12a03e8b4b92c72f58aeb5fcc5d8c6ce94ffb52fa4e13b04e23229fa535fedc0 in /etc/ca-certificates/update.d/docker-openjdk 
# Tue, 23 Aug 2022 15:08:38 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk
# Tue, 23 Aug 2022 15:08:38 GMT
EXPOSE 9200 9300
# Tue, 23 Aug 2022 15:08:39 GMT
LABEL org.label-schema.build-date=2022-08-23T15:05:47.781551968Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=f65e9d338dc1d07b642e14a27f338990148ee5b6 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.6 org.opencontainers.image.created=2022-08-23T15:05:47.781551968Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=f65e9d338dc1d07b642e14a27f338990148ee5b6 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.6
# Tue, 23 Aug 2022 15:08:39 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 15:08:39 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa839ec4bcfe97e29e4d933e680f58fc0aa906a457482fe50b63c1ed73e687e`  
		Last Modified: Wed, 24 Aug 2022 17:23:50 GMT  
		Size: 8.4 MB (8378011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d59e7399c06529654b9c7f6ba6659aa136a02649b0bbe8a273caf2c205e55e7d`  
		Last Modified: Wed, 24 Aug 2022 17:23:49 GMT  
		Size: 4.3 KB (4339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa821b5c79a03569a25c35635e3f41a5efc8a886a9c9b52abbba7cd632b9488`  
		Last Modified: Wed, 24 Aug 2022 17:24:13 GMT  
		Size: 309.9 MB (309888856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b43de0011f568946d3e1b8716f2810637a8762e51b77836e5af3d0c41c542e8`  
		Last Modified: Wed, 24 Aug 2022 17:23:48 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e32e747aeac36975116540d4c70c70419e62620b782533ebf6f0e3cbfbbc1d`  
		Last Modified: Wed, 24 Aug 2022 17:23:46 GMT  
		Size: 2.0 KB (1984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df7bf99d869b6f5b9562a889c0bfb2d775e6967167520aa2cc29770933e0807`  
		Last Modified: Wed, 24 Aug 2022 17:23:46 GMT  
		Size: 192.1 KB (192132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c29c988ba5741f0270b97d3ef45c839c2086989e10b515eac1060fe678297b0`  
		Last Modified: Wed, 24 Aug 2022 17:23:46 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c547bc2077a7c0ff0c4f356c17182852d4135eb4c94405a3acc7324c16a6c625`  
		Last Modified: Wed, 24 Aug 2022 17:23:46 GMT  
		Size: 102.4 KB (102419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `elasticsearch:8.4.0`

```console
$ docker pull elasticsearch@sha256:08ad2e8d392a19bcb5dccc788af0dc02c873cb520f87832594e2d6a94a3e6eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `elasticsearch:8.4.0` - linux; amd64

```console
$ docker pull elasticsearch@sha256:f919f9d97aa008faad8669135357bd5de5c3f59cc42c410027f3b18c8adf0419
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.2 MB (610204890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a76b82015e09ef0b39c2c39296bb0a15b41de1ed0196d803ed093b87e63107`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Fri, 19 Aug 2022 22:40:05 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code
# Fri, 19 Aug 2022 22:40:06 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch
# Fri, 19 Aug 2022 22:40:06 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 19 Aug 2022 22:40:06 GMT
WORKDIR /usr/share/elasticsearch
# Fri, 19 Aug 2022 22:40:21 GMT
COPY --chown=0:0dir:f2e7d9904c41dfeb6a321646b60c1552a9008da5922e7112a8d95fe671270750 in /usr/share/elasticsearch 
# Fri, 19 Aug 2022 22:40:25 GMT
COPY --chown=0:0file:fcc427e6b1b34164533c7d80cf8bba68e6f09d5c7d442ca055586359d7076e62 in /bin/tini 
# Fri, 19 Aug 2022 22:40:25 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Aug 2022 22:40:25 GMT
COPY file:480ac78aea3a6b2b78f3489c03400c7b30d7129a2955fcf04b47c6666f033929 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 19 Aug 2022 22:40:26 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins
# Fri, 19 Aug 2022 22:40:26 GMT
COPY file:12a03e8b4b92c72f58aeb5fcc5d8c6ce94ffb52fa4e13b04e23229fa535fedc0 in /etc/ca-certificates/update.d/docker-openjdk 
# Fri, 19 Aug 2022 22:40:27 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk
# Fri, 19 Aug 2022 22:40:27 GMT
EXPOSE 9200 9300
# Fri, 19 Aug 2022 22:40:27 GMT
LABEL org.label-schema.build-date=2022-08-19T22:37:22.116074826Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=f56126089ca4db89b631901ad7cce0a8e10e2fe5 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.4.0 org.opencontainers.image.created=2022-08-19T22:37:22.116074826Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=f56126089ca4db89b631901ad7cce0a8e10e2fe5 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.4.0
# Fri, 19 Aug 2022 22:40:27 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Fri, 19 Aug 2022 22:40:28 GMT
CMD ["eswrapper"]
# Fri, 19 Aug 2022 22:40:28 GMT
USER elasticsearch:root
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6ee62b119192dfe0498aab9cae334d0d68043b7a2a4d0c637746a14ced4d7f`  
		Last Modified: Wed, 24 Aug 2022 23:22:54 GMT  
		Size: 8.4 MB (8377901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:089d376a9a77a4af8c57995aa06588995e154765ec5c0783fcda84272f888760`  
		Last Modified: Wed, 24 Aug 2022 23:22:52 GMT  
		Size: 4.3 KB (4339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a10427b036629197dc232427f5e4abca6316bbf23cf7c0b3994743f420497e2b`  
		Last Modified: Wed, 24 Aug 2022 23:23:45 GMT  
		Size: 572.9 MB (572944116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d32917a7d03e5eff6d20dfd3251ab01e6921f615daeba4aa5c9aa0cdfc323d8`  
		Last Modified: Wed, 24 Aug 2022 23:22:50 GMT  
		Size: 9.5 KB (9524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40487250cae6f1f8e48edea1cac102db0742931b23ef61f26cb99c5bd7b5fbf`  
		Last Modified: Wed, 24 Aug 2022 23:22:50 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ee73aa106552e6cf872c9150f94e781734c32ee7046f5881ce61e8645a420a`  
		Last Modified: Wed, 24 Aug 2022 23:22:50 GMT  
		Size: 191.9 KB (191869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145ea5ec7dd6c1a077e34380a78bc1e0b5edbffb44242342463eb111f5c2cb57`  
		Last Modified: Wed, 24 Aug 2022 23:22:50 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c8865142e518055894becfe36a46bd5ca97afd168dfc8d64dd3875d8d1a01d`  
		Last Modified: Wed, 24 Aug 2022 23:22:53 GMT  
		Size: 102.4 KB (102416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
