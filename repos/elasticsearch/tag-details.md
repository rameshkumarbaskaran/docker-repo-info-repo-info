<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:6.8.23`](#elasticsearch6823)
-	[`elasticsearch:7.17.2`](#elasticsearch7172)
-	[`elasticsearch:8.1.2`](#elasticsearch812)

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

## `elasticsearch:7.17.2`

```console
$ docker pull elasticsearch@sha256:5b112bf382bc84c017fdd3e183c89a2c2b93ececedbc7a0dec6046bcecb70462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `elasticsearch:7.17.2` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:5312c114d426ee22556b0e00a49ac84c864de721bd12e8571537fa3b0f568288
```

-	Docker Version: 20.10.14
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.2 MB (345248084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:462cac7b5f3d52b777798e04d9c3992b53913cb0abda81a5fed0e1d8a61b825e`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Mon, 28 Mar 2022 17:39:41 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip vim-tiny zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code
# Mon, 28 Mar 2022 17:39:42 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch
# Mon, 28 Mar 2022 17:39:42 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 28 Mar 2022 17:39:42 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 28 Mar 2022 17:39:47 GMT
COPY --chown=0:0dir:6ffa12f8e3e204a1eeaaa0bb7c4f7a728017481c0bb958d952b9bed14c090176 in /usr/share/elasticsearch 
# Mon, 28 Mar 2022 17:39:50 GMT
COPY --chown=0:0file:caaa172ee884dfa2de4269dce2215a63f709c6ea183f02cb82e252b7753b9772 in /bin/tini 
# Mon, 28 Mar 2022 17:39:50 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Mar 2022 17:39:50 GMT
COPY file:35bdfc6ad8079cb9cab605169a09ebfe8ce26cd4a9e4120efe12f418073a9bfb in /usr/local/bin/docker-entrypoint.sh 
# Mon, 28 Mar 2022 17:39:51 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins
# Mon, 28 Mar 2022 17:39:51 GMT
COPY file:12a03e8b4b92c72f58aeb5fcc5d8c6ce94ffb52fa4e13b04e23229fa535fedc0 in /etc/ca-certificates/update.d/docker-openjdk 
# Mon, 28 Mar 2022 17:39:51 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk
# Mon, 28 Mar 2022 17:39:52 GMT
EXPOSE 9200 9300
# Mon, 28 Mar 2022 17:39:52 GMT
LABEL org.label-schema.build-date=2022-03-28T17:37:42.958961613Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=de7261de50d90919ae53b0eff9413fd7e5307301 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.2 org.opencontainers.image.created=2022-03-28T17:37:42.958961613Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=de7261de50d90919ae53b0eff9413fd7e5307301 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.2
# Mon, 28 Mar 2022 17:39:52 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 28 Mar 2022 17:39:52 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffec6af9705b51ed512bfbe9652df0459107561c87b227c26f7cf7dfe4968e42`  
		Last Modified: Fri, 01 Apr 2022 18:41:35 GMT  
		Size: 8.1 MB (8068239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50fa7d78637ce3edc788dee1faa3575011a1b26e8cfa2218f8198d3bb7184838`  
		Last Modified: Fri, 01 Apr 2022 18:41:34 GMT  
		Size: 4.4 KB (4374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5431b91c136cf37a3a4b480048ef2873579dd5d7c6ef664e19118ab620adfd5b`  
		Last Modified: Fri, 01 Apr 2022 18:42:01 GMT  
		Size: 309.7 MB (309704351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3958de2d62ada7eb51f84b8db36339095865eb777d33f25277e60a2c10f313`  
		Last Modified: Fri, 01 Apr 2022 18:41:31 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a11945d3132326229d336ccf8c74afe565ceb5ce5cd4e18534369e8ec60fd36f`  
		Last Modified: Fri, 01 Apr 2022 18:41:31 GMT  
		Size: 2.0 KB (1982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f9170b9ac333996802f8abf10b38c3b29de878d52ab5d4b0e0ed8f7d7e185c`  
		Last Modified: Fri, 01 Apr 2022 18:41:31 GMT  
		Size: 186.2 KB (186153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4adb97d764de7ff7c34404da77200029c9673608ca7588c9183b04692b7b0b`  
		Last Modified: Fri, 01 Apr 2022 18:41:31 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7afb0b29eae94d4e3f7b68f570dc5200e43fbfbf100bacb3967837f7fcd778`  
		Last Modified: Fri, 01 Apr 2022 18:41:31 GMT  
		Size: 103.9 KB (103864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `elasticsearch:8.1.2`

```console
$ docker pull elasticsearch@sha256:bf1c6c2aeb9fc563d9aebcfba4027907de2a1d980a1275521b3da89e861fea01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `elasticsearch:8.1.2` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:fd5c3d054b1b6baad3bee3cd6b980395f48f3165a37d13aca41d50cef541c1e3
```

-	Docker Version: 20.10.14
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.5 MB (365453748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27acfe772b57f0da522f449e7aadb6cafe6df6e8da899ad2edf72be8d42eb23d`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 00:44:29 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip vim-tiny zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code
# Wed, 30 Mar 2022 00:44:29 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch
# Wed, 30 Mar 2022 00:44:30 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 30 Mar 2022 00:44:30 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 30 Mar 2022 00:44:34 GMT
COPY --chown=0:0dir:a691657ff62f4a371e9970aa20352b585b002416249374bb89caea1c267b095d in /usr/share/elasticsearch 
# Wed, 30 Mar 2022 00:44:38 GMT
COPY --chown=0:0file:caaa172ee884dfa2de4269dce2215a63f709c6ea183f02cb82e252b7753b9772 in /bin/tini 
# Wed, 30 Mar 2022 00:44:39 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 00:44:39 GMT
COPY file:bd241387dbc1b05c0872607dd207d3a5b10dfd812f1441a5b215a7e5436fca23 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 30 Mar 2022 00:44:39 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins
# Wed, 30 Mar 2022 00:44:40 GMT
COPY file:12a03e8b4b92c72f58aeb5fcc5d8c6ce94ffb52fa4e13b04e23229fa535fedc0 in /etc/ca-certificates/update.d/docker-openjdk 
# Wed, 30 Mar 2022 00:44:40 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk
# Wed, 30 Mar 2022 00:44:40 GMT
EXPOSE 9200 9300
# Wed, 30 Mar 2022 00:44:40 GMT
LABEL org.label-schema.build-date=2022-03-30T00:42:32.034297564Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=31df9689e80bad366ac20176aa7f2371ea5eb4c1 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.1.2 org.opencontainers.image.created=2022-03-30T00:42:32.034297564Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=31df9689e80bad366ac20176aa7f2371ea5eb4c1 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.1.2
# Wed, 30 Mar 2022 00:44:41 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 30 Mar 2022 00:44:41 GMT
CMD ["eswrapper"]
# Wed, 30 Mar 2022 00:44:41 GMT
USER elasticsearch:root
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64a0d2824e0b76a9556f1fc4d97e21027f626dde8732d5c79ddcdcbe8513583`  
		Last Modified: Fri, 01 Apr 2022 18:40:55 GMT  
		Size: 8.1 MB (8068262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a4738732ca0e0547f6c6bb1f64b59b4043ffb6a45da1fc1f0f14a52d195173`  
		Last Modified: Fri, 01 Apr 2022 18:40:54 GMT  
		Size: 4.4 KB (4368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59da657d1871c33a5c12ff5f370fe4e57436f18d8c2e0f011500b8cb9920e81f`  
		Last Modified: Fri, 01 Apr 2022 18:41:23 GMT  
		Size: 329.9 MB (329910522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79e6b5fcf42bd89c6bef10c540a7797c5d4f37bac98dc234dbfc2781b1fe819`  
		Last Modified: Fri, 01 Apr 2022 18:40:51 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f611182f6b7587cbbd22ef4a0c1eab254a941d2d24d8e25fac5e6ed2ee9777`  
		Last Modified: Fri, 01 Apr 2022 18:40:51 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:263c337c293cd51708021944988380849567a97b5350941d2fa816069d39ed99`  
		Last Modified: Fri, 01 Apr 2022 18:40:51 GMT  
		Size: 185.9 KB (185883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9306ce3864bde6b64f37bddc96b98cd024e820b7a15f9ae0a5e860fab8aa919`  
		Last Modified: Fri, 01 Apr 2022 18:40:51 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283c0adef4ac223e0f8968a79a0e84f08ca96b2e4ab749476ee156944f3ab1a3`  
		Last Modified: Fri, 01 Apr 2022 18:40:51 GMT  
		Size: 103.9 KB (103869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
