<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:6.8.20`](#elasticsearch6820)
-	[`elasticsearch:7.14.2`](#elasticsearch7142)

## `elasticsearch:6.8.20`

```console
$ docker pull elasticsearch@sha256:70889ef6ff6ab6df8ade85428e47dabc7fa114e33e540333e4b0829af46468f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `elasticsearch:6.8.20` - linux; amd64

```console
$ docker pull elasticsearch@sha256:703d0ee684ec16cf8f923ebafd02e0b0c81d16a6f654f670a3efdbd7e4cba4a3
```

-	Docker Version: 20.10.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.0 MB (483040639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ac76565a15d27de702318cc19e3195d22701b79477c8766c79cf312b0394bf`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Thu, 07 Oct 2021 22:04:43 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 07 Oct 2021 22:04:43 GMT
ENV JAVA_HOME=/opt/jdk-15.0.1+9
# Thu, 07 Oct 2021 22:04:48 GMT
COPY dir:8d79ae5f21bb18379c0d92b3d252f4730fec22a4509252ec794212b8f72bd7af in /opt/jdk-15.0.1+9 
# Thu, 07 Oct 2021 22:05:37 GMT
RUN for iter in {1..10}; do yum update  --setopt=tsflags=nodocs -y &&     yum install -y  --setopt=tsflags=nodocs nc unzip wget which &&     yum clean all && exit_code=0 && break || exit_code=\$? && echo "yum error: retry $iter in 10s" && sleep 10; done;     (exit $exit_code)
# Thu, 07 Oct 2021 22:05:39 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chmod 0775 /usr/share/elasticsearch &&     chgrp 0 /usr/share/elasticsearch
# Thu, 07 Oct 2021 22:05:39 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 07 Oct 2021 22:05:44 GMT
COPY --chown=1000:0dir:ffb6642bc44428e21004f343f678b841a4fd48fdceaf5f9a17c6aead48dfad5a in /usr/share/elasticsearch 
# Thu, 07 Oct 2021 22:05:44 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Oct 2021 22:05:44 GMT
COPY --chown=1000:0file:08193f849fc25f29db1438eff6d5c9fe1d63237aeb07a3e0009e8ba554f97c31 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 07 Oct 2021 22:05:45 GMT
RUN chgrp 0 /usr/local/bin/docker-entrypoint.sh &&     chmod g=u /etc/passwd &&     chmod 0775 /usr/local/bin/docker-entrypoint.sh
# Thu, 07 Oct 2021 22:05:45 GMT
EXPOSE 9200 9300
# Thu, 07 Oct 2021 22:05:46 GMT
LABEL org.label-schema.build-date=2021-10-07T22:00:24.085009Z org.label-schema.license=Elastic-License org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c859302dcfa51ee10915348ce467453130ed8b97 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=6.8.20 org.opencontainers.image.created=2021-10-07T22:00:24.085009Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License org.opencontainers.image.revision=c859302dcfa51ee10915348ce467453130ed8b97 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=6.8.20
# Thu, 07 Oct 2021 22:05:46 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 07 Oct 2021 22:05:46 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24a4cc54c7c368727fe395785960f69a0dbe1fe8fca5bdbbe0c8d45a8dc51d8`  
		Last Modified: Thu, 14 Oct 2021 14:13:31 GMT  
		Size: 207.7 MB (207657728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6df3adfb8f398060c16b9e9ee78862e7deae89bf64ba501e709c71e595b402`  
		Last Modified: Thu, 14 Oct 2021 14:13:23 GMT  
		Size: 49.1 MB (49138569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75da569075e87317d63fa7e45b18ced12bb07fda73169ddfeb1bc913062980c`  
		Last Modified: Thu, 14 Oct 2021 14:13:15 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787abc13b0c35727891900ef2d218b89343dcb84e9dd8e4d85083ea690f83d76`  
		Last Modified: Thu, 14 Oct 2021 14:13:25 GMT  
		Size: 150.1 MB (150140409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9392e421ee4302715968c11bfaf914be2f375d258027cf632e6987e9303e5888`  
		Last Modified: Thu, 14 Oct 2021 14:13:14 GMT  
		Size: 2.1 KB (2064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ce69fc8e63b9df5f043722782f8e8158015660c7ab54a1b174ce81653acea5`  
		Last Modified: Thu, 14 Oct 2021 14:13:14 GMT  
		Size: 2.4 KB (2400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `elasticsearch:7.14.2`

```console
$ docker pull elasticsearch@sha256:f05ab7f4d2aa5040813a0ea4eb76fa99bb31459937a4539efe2f2c2dbb2109fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `elasticsearch:7.14.2` - linux; amd64

```console
$ docker pull elasticsearch@sha256:55a0901f558968fb615d25032fdbeb9c6dd112d8ead05b830b1da4326e2f482b
```

-	Docker Version: 20.10.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.9 MB (512930458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2abd5342ace0faddbf87836d7d1fbb201dada20a6ca09a3dbf3cb6f4637f45fb`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 08 Dec 2020 00:22:52 GMT
ADD file:bd7a2aed6ede423b719ceb2f723e4ecdfa662b28639c8429731c878e86fb138b in / 
# Tue, 08 Dec 2020 00:22:52 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201204
# Tue, 08 Dec 2020 00:22:53 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 10:27:15 GMT
RUN for iter in {1..10}; do       yum update --setopt=tsflags=nodocs -y &&       yum install --setopt=tsflags=nodocs -y       nc shadow-utils zip unzip  &&       yum clean all &&       exit_code=0 && break ||         exit_code=$? && echo "yum error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code
# Wed, 15 Sep 2021 10:27:17 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chmod 0775 /usr/share/elasticsearch &&     chown -R 1000:0 /usr/share/elasticsearch
# Wed, 15 Sep 2021 10:27:17 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 15 Sep 2021 10:27:18 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 15 Sep 2021 10:27:28 GMT
COPY --chown=1000:0dir:9ed02511fe970e8199c325aec043fe7fe9812efad45c3dd336ab6f8962140577 in /usr/share/elasticsearch 
# Wed, 15 Sep 2021 10:27:29 GMT
COPY --chown=0:0file:cbfbfe828617d3c65a10427a333f66d6d0b1b1aaea532739bba4696579b6cb19 in /bin/tini 
# Wed, 15 Sep 2021 10:27:30 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Sep 2021 10:27:30 GMT
COPY file:35bdfc6ad8079cb9cab605169a09ebfe8ce26cd4a9e4120efe12f418073a9bfb in /usr/local/bin/docker-entrypoint.sh 
# Wed, 15 Sep 2021 10:27:32 GMT
RUN chmod g=u /etc/passwd &&     chmod 0775 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     ln -sf /etc/pki/ca-trust/extracted/java/cacerts /usr/share/elasticsearch/jdk/lib/security/cacerts
# Wed, 15 Sep 2021 10:27:32 GMT
EXPOSE 9200 9300
# Wed, 15 Sep 2021 10:27:33 GMT
LABEL org.label-schema.build-date=2021-09-15T10:18:09.722761972Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=6bc13727ce758c0e943c3c21653b3da82f627f75 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.14.2 org.opencontainers.image.created=2021-09-15T10:18:09.722761972Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=6bc13727ce758c0e943c3c21653b3da82f627f75 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.14.2
# Wed, 15 Sep 2021 10:27:34 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 15 Sep 2021 10:27:34 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:7a0437f04f83f084b7ed68ad9c4a4947e12fc4e1b006b38129bac89114ec3621`  
		Last Modified: Tue, 08 Dec 2020 00:23:32 GMT  
		Size: 75.2 MB (75181999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600da26e6cb4578cad8923b843a3c1728e20dda2ac672510332fc3473d617927`  
		Last Modified: Tue, 21 Sep 2021 18:24:08 GMT  
		Size: 91.8 MB (91793214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b994055406c50e80fa6bf671d5ffee21976d2debf09d1086d9550c5ec3f41b2`  
		Last Modified: Tue, 21 Sep 2021 18:23:45 GMT  
		Size: 2.4 KB (2391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637f4d51200f9f2c2cd7c27d9aa9f51a5b9bcfb06883ee7305cbaf02371cbb83`  
		Last Modified: Tue, 21 Sep 2021 18:24:28 GMT  
		Size: 345.7 MB (345741648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfea77848c675146487eded896837273011579b0cd8f2ef718b9813709acdd62`  
		Last Modified: Tue, 21 Sep 2021 18:23:44 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d228b386cd631767458e17d9db8c7dcc454bc61c6364408ce6c64e213d7e0d`  
		Last Modified: Tue, 21 Sep 2021 18:23:41 GMT  
		Size: 2.0 KB (1982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d5caaa4668ef2fd6cd43858cc6cf4a7b579d48a26228b02a1f558f8516f096`  
		Last Modified: Tue, 21 Sep 2021 18:23:42 GMT  
		Size: 199.7 KB (199687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elasticsearch:7.14.2` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:8f99dc1f4a95a4f440de70556125bc0fdb4ab9ccdfa67538186b3da01059b7dd
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.6 MB (510604148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86bdd490aebb31ec8728f5f55e1c8906cfb3aaa0b1bcaeaf15f951579b8d6af3`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 07 Dec 2020 23:42:06 GMT
ADD file:edd6e1253ec7bbb67b5a28d40c7d28b34a443c2cfa327bebf55c8b0b19484bf9 in / 
# Mon, 07 Dec 2020 23:42:09 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201204
# Mon, 07 Dec 2020 23:42:10 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 11:22:50 GMT
RUN for iter in {1..10}; do       yum update --setopt=tsflags=nodocs -y &&       yum install --setopt=tsflags=nodocs -y       nc shadow-utils zip unzip  &&       yum clean all &&       exit_code=0 && break ||         exit_code=$? && echo "yum error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code
# Wed, 15 Sep 2021 11:22:52 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chmod 0775 /usr/share/elasticsearch &&     chown -R 1000:0 /usr/share/elasticsearch
# Wed, 15 Sep 2021 11:22:52 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 15 Sep 2021 11:22:52 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 15 Sep 2021 11:23:07 GMT
COPY --chown=1000:0dir:76770c6ad4d50207aebc54eeafd7b09cad509815bc72f6d052487a0882fa6ae6 in /usr/share/elasticsearch 
# Wed, 15 Sep 2021 11:23:08 GMT
COPY --chown=0:0file:1d48586bd42e8cf29bed9d4feee798b5c536660cc7b115750f0cd4f7bd33c311 in /bin/tini 
# Wed, 15 Sep 2021 11:23:08 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Sep 2021 11:23:09 GMT
COPY file:35bdfc6ad8079cb9cab605169a09ebfe8ce26cd4a9e4120efe12f418073a9bfb in /usr/local/bin/docker-entrypoint.sh 
# Wed, 15 Sep 2021 11:23:11 GMT
RUN chmod g=u /etc/passwd &&     chmod 0775 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     ln -sf /etc/pki/ca-trust/extracted/java/cacerts /usr/share/elasticsearch/jdk/lib/security/cacerts
# Wed, 15 Sep 2021 11:23:11 GMT
EXPOSE 9200 9300
# Wed, 15 Sep 2021 11:23:11 GMT
LABEL org.label-schema.build-date=2021-09-15T11:18:15.075101818Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=6bc13727ce758c0e943c3c21653b3da82f627f75 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.14.2 org.opencontainers.image.created=2021-09-15T11:18:15.075101818Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=6bc13727ce758c0e943c3c21653b3da82f627f75 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.14.2
# Wed, 15 Sep 2021 11:23:11 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 15 Sep 2021 11:23:11 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:333cbcae3fb80b9a46084ae4caea81a84aafda9700fb646ab89206d0cfe213fd`  
		Last Modified: Mon, 07 Dec 2020 23:42:49 GMT  
		Size: 75.6 MB (75613064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa00907024c66456f751b7d67ed3a2ae7acf4202c0753693d99c2b782a9eec3`  
		Last Modified: Fri, 15 Oct 2021 18:40:12 GMT  
		Size: 91.7 MB (91746387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d68e84eef78a65e75130cdaf29095feb3dd007452846ae11d24d4507c00ba6c`  
		Last Modified: Fri, 15 Oct 2021 18:39:55 GMT  
		Size: 2.4 KB (2393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756ca6399aa1ed8073e2f344663729cb67c815af988f21ac363a94498cfdfd08`  
		Last Modified: Fri, 15 Oct 2021 18:41:37 GMT  
		Size: 343.0 MB (343030869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:689d68c97e57712ae92b5527e0590f4cc734c02495c4c5424f010d20186d01ee`  
		Last Modified: Fri, 15 Oct 2021 18:39:55 GMT  
		Size: 9.1 KB (9109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43919fab8263045383c7197a3ecdb46fb3df5cd389c3461e76209a2cad2f2dd9`  
		Last Modified: Fri, 15 Oct 2021 18:39:55 GMT  
		Size: 2.0 KB (1981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2ce3a977efd7a5f39b186d11e1fe84f7d7d9a4dc14fa304fe3c66cf8d6c109`  
		Last Modified: Fri, 15 Oct 2021 18:39:55 GMT  
		Size: 200.3 KB (200345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
