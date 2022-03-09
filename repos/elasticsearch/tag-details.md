<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:6.8.23`](#elasticsearch6823)
-	[`elasticsearch:7.17.1`](#elasticsearch7171)
-	[`elasticsearch:8.1.0`](#elasticsearch810)

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

## `elasticsearch:7.17.1`

```console
$ docker pull elasticsearch@sha256:c236219f85e1982aa1aad3e183ea899d834b0a5bbc3bf1c00c216a0b8353c9a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `elasticsearch:7.17.1` - linux; amd64

```console
$ docker pull elasticsearch@sha256:ddbf16b215a91f4bcc83103d54bf053056168ca38b4420d2fdc47dd02bdf6267
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.9 MB (352854012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:515ab4fba87016cef98f367ff9c845b7e54b6d1595e6f5053d53b831a3641d91`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Thu, 24 Feb 2022 09:31:55 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip vim-tiny zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code
# Thu, 24 Feb 2022 09:31:56 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch
# Thu, 24 Feb 2022 09:31:56 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 24 Feb 2022 09:31:57 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 24 Feb 2022 09:32:03 GMT
COPY --chown=0:0dir:fd1bd7ac9db6f8aa3263365284f77d46ba33b7d246c5c8ec7cd506968e6ff35c in /usr/share/elasticsearch 
# Thu, 24 Feb 2022 09:32:07 GMT
COPY --chown=0:0file:fcc427e6b1b34164533c7d80cf8bba68e6f09d5c7d442ca055586359d7076e62 in /bin/tini 
# Thu, 24 Feb 2022 09:32:07 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Feb 2022 09:32:07 GMT
COPY file:35bdfc6ad8079cb9cab605169a09ebfe8ce26cd4a9e4120efe12f418073a9bfb in /usr/local/bin/docker-entrypoint.sh 
# Thu, 24 Feb 2022 09:32:08 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins
# Thu, 24 Feb 2022 09:32:08 GMT
COPY file:12a03e8b4b92c72f58aeb5fcc5d8c6ce94ffb52fa4e13b04e23229fa535fedc0 in /etc/ca-certificates/update.d/docker-openjdk 
# Thu, 24 Feb 2022 09:32:09 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk
# Thu, 24 Feb 2022 09:32:09 GMT
EXPOSE 9200 9300
# Thu, 24 Feb 2022 09:32:09 GMT
LABEL org.label-schema.build-date=2022-02-24T09:29:39.346656497Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=e5acb99f822233d62d6444ce45a4543dc1c8059a org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.1 org.opencontainers.image.created=2022-02-24T09:29:39.346656497Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=e5acb99f822233d62d6444ce45a4543dc1c8059a org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.1
# Thu, 24 Feb 2022 09:32:09 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 24 Feb 2022 09:32:09 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c13ab4dd35a39bf156da4a7659edf05439002d24aa7d7bebf1603e2b16d9534`  
		Last Modified: Tue, 01 Mar 2022 04:50:17 GMT  
		Size: 10.8 MB (10813947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257cfc4bd62dd01191ed769141f0358adaaf2e3d8c91ee5bd03ea83cf1aec2ab`  
		Last Modified: Tue, 01 Mar 2022 04:50:14 GMT  
		Size: 4.4 KB (4361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b78bb352a8f1e8565e11e7b19230f2fcf7cea1b7bbf807d0fb26258747681d`  
		Last Modified: Tue, 01 Mar 2022 04:50:41 GMT  
		Size: 313.2 MB (313163696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:712cf7eaa835918cdbb668f93a846df5b45ccce95ccdc8fc599d2bdcd73dec1c`  
		Last Modified: Tue, 01 Mar 2022 04:50:14 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb23c52cd0070b2b8f4ba95268d3fb93c42cadeee84add81fbabc114fc436b6`  
		Last Modified: Tue, 01 Mar 2022 04:50:13 GMT  
		Size: 2.0 KB (1981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b752828c33545d099b1e52623d4c6959384d25bda9493e3a5ba6046024cbea19`  
		Last Modified: Tue, 01 Mar 2022 04:50:13 GMT  
		Size: 192.1 KB (192122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1ac86b3d6e2bb47d2de1254e8e3557836e1130385405fa3bcb424dcdba8dd6`  
		Last Modified: Tue, 01 Mar 2022 04:50:13 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e68b6b8003db7088720db95cb4fe45e45951bbfab20637b887dfe04dc755f11`  
		Last Modified: Tue, 01 Mar 2022 04:50:13 GMT  
		Size: 103.9 KB (103870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elasticsearch:7.17.1` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:3585800c475cfb38a9e8c05819ba0f93cca2bf329c869c39f6574c1a58970036
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.8 MB (347753466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1345c4a1ed1b57cf76af9b7abacbfb46fc2dae97a0ffba886a72a10dce82a770`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Thu, 24 Feb 2022 09:33:45 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip vim-tiny zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code
# Thu, 24 Feb 2022 09:33:46 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch
# Thu, 24 Feb 2022 09:33:46 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 24 Feb 2022 09:33:46 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 24 Feb 2022 09:33:50 GMT
COPY --chown=0:0dir:dd8cdf57fe959a026ef07ca59b94c4de04285758a1fd90c0583c4e0e047402f9 in /usr/share/elasticsearch 
# Thu, 24 Feb 2022 09:33:54 GMT
COPY --chown=0:0file:caaa172ee884dfa2de4269dce2215a63f709c6ea183f02cb82e252b7753b9772 in /bin/tini 
# Thu, 24 Feb 2022 09:33:54 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Feb 2022 09:33:55 GMT
COPY file:35bdfc6ad8079cb9cab605169a09ebfe8ce26cd4a9e4120efe12f418073a9bfb in /usr/local/bin/docker-entrypoint.sh 
# Thu, 24 Feb 2022 09:33:55 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins
# Thu, 24 Feb 2022 09:33:56 GMT
COPY file:12a03e8b4b92c72f58aeb5fcc5d8c6ce94ffb52fa4e13b04e23229fa535fedc0 in /etc/ca-certificates/update.d/docker-openjdk 
# Thu, 24 Feb 2022 09:33:56 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk
# Thu, 24 Feb 2022 09:33:56 GMT
EXPOSE 9200 9300
# Thu, 24 Feb 2022 09:33:56 GMT
LABEL org.label-schema.build-date=2022-02-24T09:31:44.848757160Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=e5acb99f822233d62d6444ce45a4543dc1c8059a org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.1 org.opencontainers.image.created=2022-02-24T09:31:44.848757160Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=e5acb99f822233d62d6444ce45a4543dc1c8059a org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.1
# Thu, 24 Feb 2022 09:33:57 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 24 Feb 2022 09:33:57 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe7bf9d67731dd96e850413a33ddf87a0b6e1d1f844be879d7122ad052443c2`  
		Last Modified: Wed, 02 Mar 2022 16:03:13 GMT  
		Size: 10.6 MB (10596088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56749365c1edd3f562d755b342a91f70ceba499e64aa2d51f8748160b8002515`  
		Last Modified: Wed, 02 Mar 2022 16:03:04 GMT  
		Size: 4.4 KB (4377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f8929cade0c81a6c7a092b392260363db00a5b10c1a815c66af25a35154717`  
		Last Modified: Wed, 02 Mar 2022 16:03:35 GMT  
		Size: 309.7 MB (309681842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df3eb5f0a2a1c02f2e8b1d56f36193e6ac904c59ef5511c8d574123d87b8575`  
		Last Modified: Wed, 02 Mar 2022 16:03:01 GMT  
		Size: 9.1 KB (9095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3abe89c77be0a772ec32fe82783230bc32fb53ff1e6fdd4a34f6954627a9115b`  
		Last Modified: Wed, 02 Mar 2022 16:03:01 GMT  
		Size: 2.0 KB (1983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef46a25d412500cdc14b1fac6cdd6dfbd5fde1e034963ffea60c3ed098d6004`  
		Last Modified: Wed, 02 Mar 2022 16:03:01 GMT  
		Size: 186.2 KB (186163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533f73c6eb0e834985aa6ef71858d72be0f0a564cd43686e30a19b7fabe1d437`  
		Last Modified: Wed, 02 Mar 2022 16:03:01 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52209a05e2157ece6366861e1545256d0773adafe46a1eb9243ca26e384d9f3`  
		Last Modified: Wed, 02 Mar 2022 16:03:01 GMT  
		Size: 103.9 KB (103870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `elasticsearch:8.1.0`

```console
$ docker pull elasticsearch@sha256:600949aed8caa919d500a5d87995c8d9c9aa80bc7961fb8d355761146a05a470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `elasticsearch:8.1.0` - linux; amd64

```console
$ docker pull elasticsearch@sha256:cb74057b1647351b128a4417510c6ce398d8e5d5db16be2bc305fbafaf2f4a87
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **568.6 MB (568584459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9fc6ca9dc521df575db04077c5967e122def8f9b7f2dfe15219b83029fe019b`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 17:52:18 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip vim-tiny zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code
# Thu, 03 Mar 2022 17:52:19 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch
# Thu, 03 Mar 2022 17:52:19 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 03 Mar 2022 17:52:19 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 03 Mar 2022 17:52:34 GMT
COPY --chown=0:0dir:452d1d481f6b03019aaa34aac78338656ebd31ed404474bbbbcab293db1c4d7b in /usr/share/elasticsearch 
# Thu, 03 Mar 2022 17:52:38 GMT
COPY --chown=0:0file:fcc427e6b1b34164533c7d80cf8bba68e6f09d5c7d442ca055586359d7076e62 in /bin/tini 
# Thu, 03 Mar 2022 17:52:38 GMT
COPY --chown=0:0dir:b581b730e5b7ee3ec0eabb697a9ee0c5d9c3c7f14aa330f554a9bb2db8474887 in /usr/local/cloudflare-zlib 
# Thu, 03 Mar 2022 17:52:38 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 17:52:38 GMT
ENV ES_ZLIB_PATH=/usr/local/cloudflare-zlib/lib
# Thu, 03 Mar 2022 17:52:38 GMT
COPY file:bd241387dbc1b05c0872607dd207d3a5b10dfd812f1441a5b215a7e5436fca23 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 03 Mar 2022 17:52:39 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins
# Thu, 03 Mar 2022 17:52:39 GMT
COPY file:12a03e8b4b92c72f58aeb5fcc5d8c6ce94ffb52fa4e13b04e23229fa535fedc0 in /etc/ca-certificates/update.d/docker-openjdk 
# Thu, 03 Mar 2022 17:52:40 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk
# Thu, 03 Mar 2022 17:52:40 GMT
EXPOSE 9200 9300
# Thu, 03 Mar 2022 17:52:40 GMT
LABEL org.label-schema.build-date=2022-03-03T17:48:45.112302284Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=3700f7679f7d95e36da0b43762189bab189bc53a org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.1.0 org.opencontainers.image.created=2022-03-03T17:48:45.112302284Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=3700f7679f7d95e36da0b43762189bab189bc53a org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.1.0
# Thu, 03 Mar 2022 17:52:40 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 03 Mar 2022 17:52:40 GMT
CMD ["eswrapper"]
# Thu, 03 Mar 2022 17:52:41 GMT
USER elasticsearch:root
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff2ab324559139e278188844978c46e8c91af47270dc75e691d0e907b78acb2`  
		Last Modified: Tue, 08 Mar 2022 21:24:05 GMT  
		Size: 17.4 MB (17390373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ed3593db2433454400c92d4a7c910c527aa1837c6f893adffe5c31a81518a1`  
		Last Modified: Tue, 08 Mar 2022 21:24:02 GMT  
		Size: 4.4 KB (4370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818e9e5e96bb0ac3ae473bb6558a01e65181e2125573c5c0e9cd2b2b8c156a6d`  
		Last Modified: Tue, 08 Mar 2022 21:24:57 GMT  
		Size: 522.2 MB (522171015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffdad5b7c035610df49891b1e911940f1b4553c9dc9b4c496f33dcd48ac784c`  
		Last Modified: Tue, 08 Mar 2022 21:24:02 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75c21c9d887f3d1d89c33727c1cb3cd1733ba7f008e7a163c75f79cdd8e87f7`  
		Last Modified: Tue, 08 Mar 2022 21:24:02 GMT  
		Size: 147.2 KB (147243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de9ee659811fbaeca358e2ce018246bf725c492d80cf866e098996aab2953f7`  
		Last Modified: Tue, 08 Mar 2022 21:23:59 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e251a8179c68d530ba5a4699f472187644d7101ed9d3274eb4d2b6d8e01eea1e`  
		Last Modified: Tue, 08 Mar 2022 21:23:59 GMT  
		Size: 191.8 KB (191844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4fd8fa609a599a6ed7dd64edafdab1049c18cf19b2e6815de9e651ea367ce8`  
		Last Modified: Tue, 08 Mar 2022 21:24:00 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac1c98ec28bf3b5c1693f8e3fde1270b651c6dabd5b348ae66d759d85c9f23f`  
		Last Modified: Tue, 08 Mar 2022 21:23:59 GMT  
		Size: 103.9 KB (103867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elasticsearch:8.1.0` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:56bfbba13046c12da036054f4d3629afaa660e98e89a11ab36d14cf582f1fa44
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.6 MB (373624122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4209cb2b912e46b16c52956623d21ccd8c03a485ee8f42cc7f020b1485dd5cf7`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 17:53:10 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip vim-tiny zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code
# Thu, 03 Mar 2022 17:53:11 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch
# Thu, 03 Mar 2022 17:53:11 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 03 Mar 2022 17:53:11 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 03 Mar 2022 17:53:15 GMT
COPY --chown=0:0dir:4134d222abe4c9edb8be038b4e7c0dfb49ca9b78da7867faeb3dedfdce5d7233 in /usr/share/elasticsearch 
# Thu, 03 Mar 2022 17:53:20 GMT
COPY --chown=0:0file:caaa172ee884dfa2de4269dce2215a63f709c6ea183f02cb82e252b7753b9772 in /bin/tini 
# Thu, 03 Mar 2022 17:53:20 GMT
COPY --chown=0:0dir:dc66ad287e412767e7bc0881fa0de8bd5a657165824323af7b04dd18841bea5d in /usr/local/cloudflare-zlib 
# Thu, 03 Mar 2022 17:53:20 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 17:53:20 GMT
ENV ES_ZLIB_PATH=/usr/local/cloudflare-zlib/lib
# Thu, 03 Mar 2022 17:53:20 GMT
COPY file:bd241387dbc1b05c0872607dd207d3a5b10dfd812f1441a5b215a7e5436fca23 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 03 Mar 2022 17:53:21 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins
# Thu, 03 Mar 2022 17:53:21 GMT
COPY file:12a03e8b4b92c72f58aeb5fcc5d8c6ce94ffb52fa4e13b04e23229fa535fedc0 in /etc/ca-certificates/update.d/docker-openjdk 
# Thu, 03 Mar 2022 17:53:22 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk
# Thu, 03 Mar 2022 17:53:22 GMT
EXPOSE 9200 9300
# Thu, 03 Mar 2022 17:53:22 GMT
LABEL org.label-schema.build-date=2022-03-03T17:50:13.963430103Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=3700f7679f7d95e36da0b43762189bab189bc53a org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.1.0 org.opencontainers.image.created=2022-03-03T17:50:13.963430103Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=3700f7679f7d95e36da0b43762189bab189bc53a org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.1.0
# Thu, 03 Mar 2022 17:53:22 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 03 Mar 2022 17:53:22 GMT
CMD ["eswrapper"]
# Thu, 03 Mar 2022 17:53:22 GMT
USER elasticsearch:root
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:926bd648e1f65c79a6572f53b7e86e85840079c58c69b26e89a73f0e2c6c323f`  
		Last Modified: Wed, 09 Mar 2022 21:40:09 GMT  
		Size: 16.1 MB (16099850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e7c02bd096ad3dfb95b89f6e72e1df3cdbc05df14d148f283c6d464a655f3b`  
		Last Modified: Wed, 09 Mar 2022 21:40:07 GMT  
		Size: 4.4 KB (4381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc1865270af037cdd40f5f955ade858e7e579147bfa90af8b50b6b92f5bfba0f`  
		Last Modified: Wed, 09 Mar 2022 21:40:38 GMT  
		Size: 329.9 MB (329899379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:169a1f705cb3cc507113a40d2de63ab4bbec4f009e73e3ff5327cb1870b0462a`  
		Last Modified: Wed, 09 Mar 2022 21:40:06 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d228fca1e8f5437047cf1f881ea7babbf238bc25f2016858bbffbb6ba93b78f`  
		Last Modified: Wed, 09 Mar 2022 21:40:04 GMT  
		Size: 149.9 KB (149909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd1741c3648a19321ed1fee9baacb8bf80237d2c5c02695c493d7e91fa3588be`  
		Last Modified: Wed, 09 Mar 2022 21:40:04 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a29eb6bdc419baba5dd5950f870154ef0d5b0a37e8408a986cb519d2762891`  
		Last Modified: Wed, 09 Mar 2022 21:40:04 GMT  
		Size: 185.9 KB (185880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43dacc103a2a2d078b01fa8a8b03cfbbe303a603f589fd2c9733445b236ce40d`  
		Last Modified: Wed, 09 Mar 2022 21:40:04 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f91cada41207f17cb411a0aec95d280798ae808de30eb2f163a9452d8fef6e`  
		Last Modified: Wed, 09 Mar 2022 21:40:04 GMT  
		Size: 103.9 KB (103869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
