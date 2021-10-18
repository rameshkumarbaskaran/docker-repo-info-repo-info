<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:6.8.20`](#logstash6820)
-	[`logstash:7.14.2`](#logstash7142)

## `logstash:6.8.20`

```console
$ docker pull logstash@sha256:930ee70fea7e557e936afca04d5ccfa5f6500e2f4d0ae2223290792c11d76cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `logstash:6.8.20` - linux; amd64

```console
$ docker pull logstash@sha256:940eaaaab88a1a345191a714a12c59a2a60b4ecad91ec6bb7512781653d37fe7
```

-	Docker Version: 20.10.9
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.6 MB (387618098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ad8c8e0738d6b73b5a0ce2fcf7bd7587735f8154579a1b0fc0ef5001128426`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Thu, 07 Oct 2021 21:09:31 GMT
RUN yum update -y && yum install -y java-1.8.0-openjdk-devel-1.8.0.282.b08 java-1.8.0-openjdk-headless-1.8.0.282.b08 which &&     yum clean all
# Thu, 07 Oct 2021 21:09:34 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home-dir /usr/share/logstash --no-create-home       logstash
# Thu, 07 Oct 2021 21:09:51 GMT
RUN curl -Lo - http://localhost:8000/logstash-6.8.20.tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-6.8.20 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Thu, 07 Oct 2021 21:09:53 GMT
WORKDIR /usr/share/logstash
# Thu, 07 Oct 2021 21:09:53 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 07 Oct 2021 21:09:53 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Oct 2021 21:09:53 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Thu, 07 Oct 2021 21:09:53 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Thu, 07 Oct 2021 21:09:53 GMT
ADD file:2ef21d4766eab3ac48ed3847c8b8d05554f1fd0b39061cba66c9ac93240087fa in config/ 
# Thu, 07 Oct 2021 21:09:54 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Thu, 07 Oct 2021 21:09:54 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Thu, 07 Oct 2021 21:09:54 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 07 Oct 2021 21:09:54 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Thu, 07 Oct 2021 21:09:55 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Thu, 07 Oct 2021 21:09:55 GMT
USER 1000
# Thu, 07 Oct 2021 21:09:55 GMT
ADD file:c571f1340b3840928052ac69357eca598068bd1a752b377b661e4a526205c25b in /usr/local/bin/ 
# Thu, 07 Oct 2021 21:09:55 GMT
EXPOSE 5044 9600
# Thu, 07 Oct 2021 21:09:55 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.label-schema.name=logstash org.label-schema.version=6.8.20 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash license=Elastic License
# Thu, 07 Oct 2021 21:09:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f845d959f7a000ccdd444e3f747f12b926b6fe6bcced60f5bfb44bfb51be85`  
		Last Modified: Thu, 14 Oct 2021 14:14:08 GMT  
		Size: 130.0 MB (130034901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e2d5941a02a9c25ee7d7c53a3406ec837b1c783ab857877f25a70a4980a9dd`  
		Last Modified: Thu, 14 Oct 2021 14:13:54 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a1b1ad4ae879f9a1ffe2f3f5d1b6519f45b7f06f991e02540f41b3e9a668de`  
		Last Modified: Thu, 14 Oct 2021 14:14:05 GMT  
		Size: 179.8 MB (179815573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8894f89da33ccb66b6c5ba220c9db337703eaa6066fefc32518c6474ce035c1`  
		Last Modified: Thu, 14 Oct 2021 14:13:51 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ff9ace86c633a84e75f2da8c02e21ab9b2ee10dc6c388d33c8ff38afc623c2`  
		Last Modified: Thu, 14 Oct 2021 14:13:51 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31d2fb714ae3d471fa8ded079dd626f4fbdf279d3624b6b0b0d186ab79ac191`  
		Last Modified: Thu, 14 Oct 2021 14:13:51 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37627b266c4172583d0111a0166531e70312e25f0f8cff517711236e79821f24`  
		Last Modified: Thu, 14 Oct 2021 14:13:49 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704b9db70829fd31d7c64eb7c1f7e684db9cd22621e7f62c05e2abfa57587010`  
		Last Modified: Thu, 14 Oct 2021 14:13:48 GMT  
		Size: 2.7 KB (2680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3d0810a54972298734fbf0276a7bc3412aaa41af527490145bb8bec109cb7e`  
		Last Modified: Thu, 14 Oct 2021 14:13:48 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3d0810a54972298734fbf0276a7bc3412aaa41af527490145bb8bec109cb7e`  
		Last Modified: Thu, 14 Oct 2021 14:13:48 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c6e711d4a1fda74a879de38afd3f1255071b6b751e7f4302ed1becd575092df`  
		Last Modified: Thu, 14 Oct 2021 14:13:48 GMT  
		Size: 1.7 MB (1663555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `logstash:7.14.2`

```console
$ docker pull logstash@sha256:1011c200e673cb39eaa0efebc182d7bdfe87c4dbc256be8fea6ed5e13c8830cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `logstash:7.14.2` - linux; amd64

```console
$ docker pull logstash@sha256:b59f0d885ff1d21b8f9181cbf482d79b05df9c8359a33baafc6c400d96a8eab6
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.7 MB (490709716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec391466d53d1cb83d677cf7c388f86a1c466e168c3a866bbd2b7e3bae5fb73`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 10:17:19 GMT
RUN for iter in {1..10}; do yum update -y &&     yum install -y procps findutils tar gzip which shadow-utils &&     yum clean all && yum clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     yum clean all && yum clean metadata && sleep 10; done;     (exit $exit_code)
# Wed, 15 Sep 2021 10:17:20 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home-dir /usr/share/logstash --no-create-home       logstash
# Wed, 15 Sep 2021 10:17:42 GMT
RUN curl -Lo - http://localhost:8000/logstash-7.14.2-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.14.2 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Wed, 15 Sep 2021 10:17:45 GMT
WORKDIR /usr/share/logstash
# Wed, 15 Sep 2021 10:17:46 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 15 Sep 2021 10:17:46 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Sep 2021 10:17:46 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Wed, 15 Sep 2021 10:17:46 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Wed, 15 Sep 2021 10:17:46 GMT
ADD file:4f39d77a8986c28d67e673d4691e69ca9c175574128b0819977c2d1bb0d6e950 in config/ 
# Wed, 15 Sep 2021 10:17:46 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Wed, 15 Sep 2021 10:17:47 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Wed, 15 Sep 2021 10:17:47 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 15 Sep 2021 10:17:47 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Wed, 15 Sep 2021 10:17:47 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Wed, 15 Sep 2021 10:17:48 GMT
USER 1000
# Wed, 15 Sep 2021 10:17:48 GMT
ADD file:4fc35f1873d25f5258bad3492de23d09cc33fd409639a119015123b4adae1db5 in /usr/local/bin/ 
# Wed, 15 Sep 2021 10:17:48 GMT
EXPOSE 5044 9600
# Wed, 15 Sep 2021 10:17:48 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.14.2 org.opencontainers.image.version=7.14.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2021-09-15T09:11:59Z org.opencontainers.image.created=2021-09-15T09:11:59Z
# Wed, 15 Sep 2021 10:17:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341d542d42647545f8ed3744722523a4e4ce7fa69f686987dca7613e19fc34bd`  
		Last Modified: Tue, 21 Sep 2021 18:12:21 GMT  
		Size: 47.6 MB (47621399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969426769529848901123b6f31fb7526d7ade77919fa219bbc392acf742fa438`  
		Last Modified: Tue, 21 Sep 2021 18:12:04 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0a79d05d4b05a590a5cbbdd4fdb8b4c6512113f6a4a4b94f412c640765094b`  
		Last Modified: Tue, 21 Sep 2021 18:14:29 GMT  
		Size: 366.0 MB (365979511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6c6a11518d29664cefa7e931dccc8a093ba39eeda6ee666d4d20f5097c1e710`  
		Last Modified: Tue, 21 Sep 2021 18:12:02 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec271ad38cba26442b9b5b272e1d887ec6a40edd9aafbaa86cebabf4bb84c3c`  
		Last Modified: Tue, 21 Sep 2021 18:12:02 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c6a3ec61eb5563c753c1b18d869ca7a1c299e4394f83c584086396d69ef516`  
		Last Modified: Tue, 21 Sep 2021 18:12:01 GMT  
		Size: 480.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852d1b0171ae83f68b78088700cb94a2977250a80487c717057dc935ecda69e6`  
		Last Modified: Tue, 21 Sep 2021 18:12:01 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061ae22a77f3d3c31dc96746ce5abf67c6b1041d1616b57cd5e4d634d6729f97`  
		Last Modified: Tue, 21 Sep 2021 18:12:01 GMT  
		Size: 2.8 KB (2762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa0e293ef7733f9d79f7ae6e925d36b112ff6495500db5d7915c90cdf90ca1a`  
		Last Modified: Tue, 21 Sep 2021 18:11:58 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa0e293ef7733f9d79f7ae6e925d36b112ff6495500db5d7915c90cdf90ca1a`  
		Last Modified: Tue, 21 Sep 2021 18:11:58 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95809ca5c24410e477ec9b7f638795608045bd953c54549f6538b7eb026332f`  
		Last Modified: Tue, 21 Sep 2021 18:11:59 GMT  
		Size: 1.0 MB (1004616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `logstash:7.14.2` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:7195fd71b71c9c9de683b00553edd6bacb673ecbc8a35c515bd98de907889144
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **792.5 MB (792484424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43730223b07416294a17fae1af73c324c9a3a40eedec0fe42f1aca5ba9162e2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Sat, 14 Nov 2020 00:40:26 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Sat, 14 Nov 2020 00:40:31 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:40:32 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 09:29:28 GMT
RUN for iter in {1..10}; do yum install -y http://mirror.centos.org/centos/7/updates/x86_64/Packages/bind-license-9.11.4-26.P2.el7_9.5.noarch.rpm &&     yum clean all &&     yum clean metadata &&     exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     yum clean all &&     yum clean metadata && sleep 10; done;     (exit $exit_code)
# Wed, 15 Sep 2021 09:30:54 GMT
RUN for iter in {1..10}; do yum update -y &&     yum install -y procps findutils tar gzip which shadow-utils &&     yum clean all && yum clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     yum clean all && yum clean metadata && sleep 10; done;     (exit $exit_code)
# Wed, 15 Sep 2021 09:30:57 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home-dir /usr/share/logstash --no-create-home       logstash
# Wed, 15 Sep 2021 09:31:17 GMT
RUN curl -Lo - http://localhost:8000/logstash-7.14.2-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.14.2 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Wed, 15 Sep 2021 09:31:18 GMT
WORKDIR /usr/share/logstash
# Wed, 15 Sep 2021 09:31:18 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 15 Sep 2021 09:31:18 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Sep 2021 09:31:18 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Wed, 15 Sep 2021 09:31:18 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Wed, 15 Sep 2021 09:31:19 GMT
ADD file:4f39d77a8986c28d67e673d4691e69ca9c175574128b0819977c2d1bb0d6e950 in config/ 
# Wed, 15 Sep 2021 09:31:19 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Wed, 15 Sep 2021 09:31:19 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Wed, 15 Sep 2021 09:31:19 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 15 Sep 2021 09:31:19 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Wed, 15 Sep 2021 09:31:20 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Wed, 15 Sep 2021 09:31:20 GMT
USER 1000
# Wed, 15 Sep 2021 09:31:20 GMT
ADD file:90dad4802ee0da80c7e83b3633edb3846df70b484fed5615c56683a9e4c1fad0 in /usr/local/bin/ 
# Wed, 15 Sep 2021 09:31:20 GMT
EXPOSE 5044 9600
# Wed, 15 Sep 2021 09:31:20 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.14.2 org.opencontainers.image.version=7.14.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2021-09-15T09:11:33+00:00 org.opencontainers.image.created=2021-09-15T09:11:33+00:00
# Wed, 15 Sep 2021 09:31:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c387bbb72973255b78448df4d65242fae8a0f1c44a2126954eb0f05ddec90bc9`  
		Last Modified: Fri, 15 Oct 2021 18:42:39 GMT  
		Size: 6.3 MB (6297499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37407e18a956f28aa8dab0ec53f3ecda2789ddc1d9e92d8ed57f5311039f4f88`  
		Last Modified: Fri, 15 Oct 2021 18:43:09 GMT  
		Size: 314.2 MB (314186775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb63195a4b29b78e62282d5db9edb8dcf23e8fd822bca8b625db13b6c3cda8a`  
		Last Modified: Fri, 15 Oct 2021 18:42:36 GMT  
		Size: 1.8 KB (1827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6816808ce02b1f841074165e9eeba8390ba4af126c05e1a64ee57c45719a245`  
		Last Modified: Fri, 15 Oct 2021 18:43:11 GMT  
		Size: 362.7 MB (362674020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b586949e5e8450fabae31ddc9f814fddd1642f531a658d5339f838ebd4f2b8e`  
		Last Modified: Fri, 15 Oct 2021 18:42:36 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1aaca8319a1d853895b1bf1cd9dc9d51013ea4cea8ac24504f175cfa21e2e8b`  
		Last Modified: Fri, 15 Oct 2021 18:42:35 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02507812dfa847ad89c0aeb8c4b0182e008e74ebc2fbbe0804e94354c17d2ce3`  
		Last Modified: Fri, 15 Oct 2021 18:42:33 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f5009ab26b388695462c3e186e77e85da6cdcdd119fd8eac5e8fab77ad94df`  
		Last Modified: Fri, 15 Oct 2021 18:42:33 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61540ddb06ceedb516aa268118bbde86c6fba9a182680615a6a38e0571ee8fec`  
		Last Modified: Fri, 15 Oct 2021 18:42:33 GMT  
		Size: 2.8 KB (2756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1148e3141b4614de3f264c1133a559780c5ffaf518e561e1db9ec98af1bb6b8`  
		Last Modified: Fri, 15 Oct 2021 18:42:33 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1148e3141b4614de3f264c1133a559780c5ffaf518e561e1db9ec98af1bb6b8`  
		Last Modified: Fri, 15 Oct 2021 18:42:33 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01f94f2cd40da9b4178f7f6454adf23c92290fa8a9dfa1483d7e27db2f7c51b`  
		Last Modified: Fri, 15 Oct 2021 18:42:34 GMT  
		Size: 944.2 KB (944169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
