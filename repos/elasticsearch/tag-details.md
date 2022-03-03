<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:6.8.23`](#elasticsearch6823)
-	[`elasticsearch:7.17.1`](#elasticsearch7171)
-	[`elasticsearch:8.0.1`](#elasticsearch801)

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

## `elasticsearch:8.0.1`

```console
$ docker pull elasticsearch@sha256:082149d7e8b395ac569d3a019afc4169dfb7d8edf9e7d4fa83463e60d64387a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `elasticsearch:8.0.1` - linux; amd64

```console
$ docker pull elasticsearch@sha256:b47f60d6b907fe7861fdb2c3babf29370e60692a37f1c66b2d0628d9f1515b4d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.6 MB (561604594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:620a7a6cd2941f072151a9372e6ad2eb64b49fdb55b0aee30ea5a60e40d5722e`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Thu, 24 Feb 2022 18:27:46 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip vim-tiny zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code
# Thu, 24 Feb 2022 18:27:47 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch
# Thu, 24 Feb 2022 18:27:47 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 24 Feb 2022 18:27:48 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 24 Feb 2022 18:28:03 GMT
COPY --chown=0:0dir:73859350387e23fc302818f39f21fa026eab12401f4f869c4dfe3ef7cf6e561e in /usr/share/elasticsearch 
# Thu, 24 Feb 2022 18:28:06 GMT
COPY --chown=0:0file:fcc427e6b1b34164533c7d80cf8bba68e6f09d5c7d442ca055586359d7076e62 in /bin/tini 
# Thu, 24 Feb 2022 18:28:06 GMT
COPY --chown=0:0dir:b581b730e5b7ee3ec0eabb697a9ee0c5d9c3c7f14aa330f554a9bb2db8474887 in /usr/local/cloudflare-zlib 
# Thu, 24 Feb 2022 18:28:06 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Feb 2022 18:28:06 GMT
ENV ES_ZLIB_PATH=/usr/local/cloudflare-zlib/lib
# Thu, 24 Feb 2022 18:28:06 GMT
COPY file:bd241387dbc1b05c0872607dd207d3a5b10dfd812f1441a5b215a7e5436fca23 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 24 Feb 2022 18:28:07 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins
# Thu, 24 Feb 2022 18:28:07 GMT
COPY file:12a03e8b4b92c72f58aeb5fcc5d8c6ce94ffb52fa4e13b04e23229fa535fedc0 in /etc/ca-certificates/update.d/docker-openjdk 
# Thu, 24 Feb 2022 18:28:08 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk
# Thu, 24 Feb 2022 18:28:08 GMT
EXPOSE 9200 9300
# Thu, 24 Feb 2022 18:28:08 GMT
LABEL org.label-schema.build-date=2022-02-24T18:24:19.354479987Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=801d9ccc7c2ee0f2cb121bbe22ab5af77a902372 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.0.1 org.opencontainers.image.created=2022-02-24T18:24:19.354479987Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=801d9ccc7c2ee0f2cb121bbe22ab5af77a902372 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.0.1
# Thu, 24 Feb 2022 18:28:08 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 24 Feb 2022 18:28:09 GMT
CMD ["eswrapper"]
# Thu, 24 Feb 2022 18:28:09 GMT
USER elasticsearch:root
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa6ee3d1d353e9b5705abf4940c33c7b81f963c3a9ae89434c34b3bfafb500c`  
		Last Modified: Tue, 01 Mar 2022 22:21:07 GMT  
		Size: 10.8 MB (10813984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee77a467357a7d29fcc04f70b171571ee106bd0f5f84e35d52a1d6457f46ab2`  
		Last Modified: Tue, 01 Mar 2022 22:20:47 GMT  
		Size: 4.4 KB (4365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed37073fede39bbfaf7bfed6caae1a06ba2462fddc2bc4e7d2dec77aa3234a38`  
		Last Modified: Tue, 01 Mar 2022 22:24:54 GMT  
		Size: 521.8 MB (521767543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fec01ec4c6368f7295b6079447cb6edd02d7b6fd1ba1a74d586596aa2dc36cb`  
		Last Modified: Tue, 01 Mar 2022 22:20:46 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3214bd9155e3b8b97086fbc19b0c7d88987b771467b2a46c3a582008ff4b50e3`  
		Last Modified: Tue, 01 Mar 2022 22:20:46 GMT  
		Size: 147.2 KB (147239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd1758cb2069b41a2ee80ba77c5ac22bd9ca9ada1815840779876af027359160`  
		Last Modified: Tue, 01 Mar 2022 22:20:40 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237a8fb47f091ecdb6d01a60b86c7f382b7e0cd73a21d80644d6961d6dd8596a`  
		Last Modified: Tue, 01 Mar 2022 22:20:41 GMT  
		Size: 191.8 KB (191850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b78956907a4566830d018416a428fb469c85a242dc522f1c549eb71b5ededa`  
		Last Modified: Tue, 01 Mar 2022 22:20:40 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d912a940cb8534b589e6cca64ec8930d80460cba464fed218801259927f54d67`  
		Last Modified: Tue, 01 Mar 2022 22:20:41 GMT  
		Size: 103.9 KB (103867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elasticsearch:8.0.1` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:d5868c47687560a1dfaa726ffca724455495dc63fe8e38af9bd7aaeb9be504d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.7 MB (367739546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19fb2049f96a66d5cfbb77ddaf6285924cc9650c1b06eb3a1bd9372dbbf8781`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Thu, 24 Feb 2022 18:29:08 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip vim-tiny zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code
# Thu, 24 Feb 2022 18:29:09 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch
# Thu, 24 Feb 2022 18:29:09 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 24 Feb 2022 18:29:09 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 24 Feb 2022 18:29:14 GMT
COPY --chown=0:0dir:99cd4b574333b78bccd199c960203b58b1f3d809cef6d239d7690e43a075dca4 in /usr/share/elasticsearch 
# Thu, 24 Feb 2022 18:29:18 GMT
COPY --chown=0:0file:caaa172ee884dfa2de4269dce2215a63f709c6ea183f02cb82e252b7753b9772 in /bin/tini 
# Thu, 24 Feb 2022 18:29:18 GMT
COPY --chown=0:0dir:dc66ad287e412767e7bc0881fa0de8bd5a657165824323af7b04dd18841bea5d in /usr/local/cloudflare-zlib 
# Thu, 24 Feb 2022 18:29:18 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Feb 2022 18:29:18 GMT
ENV ES_ZLIB_PATH=/usr/local/cloudflare-zlib/lib
# Thu, 24 Feb 2022 18:29:18 GMT
COPY file:bd241387dbc1b05c0872607dd207d3a5b10dfd812f1441a5b215a7e5436fca23 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 24 Feb 2022 18:29:19 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins
# Thu, 24 Feb 2022 18:29:19 GMT
COPY file:12a03e8b4b92c72f58aeb5fcc5d8c6ce94ffb52fa4e13b04e23229fa535fedc0 in /etc/ca-certificates/update.d/docker-openjdk 
# Thu, 24 Feb 2022 18:29:20 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk
# Thu, 24 Feb 2022 18:29:20 GMT
EXPOSE 9200 9300
# Thu, 24 Feb 2022 18:29:20 GMT
LABEL org.label-schema.build-date=2022-02-24T18:26:34.083501191Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=801d9ccc7c2ee0f2cb121bbe22ab5af77a902372 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.0.1 org.opencontainers.image.created=2022-02-24T18:26:34.083501191Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=801d9ccc7c2ee0f2cb121bbe22ab5af77a902372 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.0.1
# Thu, 24 Feb 2022 18:29:20 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 24 Feb 2022 18:29:20 GMT
CMD ["eswrapper"]
# Thu, 24 Feb 2022 18:29:21 GMT
USER elasticsearch:root
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4baea966fe5d732ff91a809f0291fc35d71f30c1b1156c64fe279d9d475595`  
		Last Modified: Wed, 02 Mar 2022 16:02:21 GMT  
		Size: 10.6 MB (10595924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad600f207f0d8ede1a1df6ccbfc58e8ed7bb4ec6e2f1d112582fb2f874de953`  
		Last Modified: Wed, 02 Mar 2022 16:02:19 GMT  
		Size: 4.4 KB (4376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ab22ff13b74f8002dd6ba72a6b3ec3aa85f2c0ca39d92acf5cc5fbc0ada913`  
		Last Modified: Wed, 02 Mar 2022 16:02:53 GMT  
		Size: 329.5 MB (329518745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6108e92eb048f17d843e3e5bd710e196978396f882308a98ba3de1ebf6c8658c`  
		Last Modified: Wed, 02 Mar 2022 16:02:21 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9887092e87a05f5961ab1f49e7ea5a486c0672bf682de7dcae7aa1146ddfc219`  
		Last Modified: Wed, 02 Mar 2022 16:02:14 GMT  
		Size: 149.9 KB (149910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b425c18e8a45f0d3261204d308be614c514d3de7365fb27e15147e928beb72`  
		Last Modified: Wed, 02 Mar 2022 16:02:14 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c654d88fa9c3f0ce6e105dfc81f935fb694da8408e0cc2ec41e71705c792e3e`  
		Last Modified: Wed, 02 Mar 2022 16:02:14 GMT  
		Size: 185.9 KB (185871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7672bebc2213312193b7f3e122fe1dc0a11f53fb44fcc1709ef59e78609bf4c`  
		Last Modified: Wed, 02 Mar 2022 16:02:14 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613270a60f0ed2ce0a6c8a136b0cc547b7a59ebf1e5234110ea8af214faccef3`  
		Last Modified: Wed, 02 Mar 2022 16:02:14 GMT  
		Size: 103.9 KB (103867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
