<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:6.8.22`](#logstash6822)
-	[`logstash:7.16.2`](#logstash7162)

## `logstash:6.8.22`

```console
$ docker pull logstash@sha256:4936d1bcbe649e02ac67d051f70f090ef86f9d7cb5c351885685132d8c61d629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `logstash:6.8.22` - linux; amd64

```console
$ docker pull logstash@sha256:a3b7b0372838490d6efec704feea15524a77a1d1e7e84a0fa9a3b7dcd6442d59
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.2 MB (396165436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89419abca70fbd51a2df9fa99dbff91bc2a60c78ec7baf2478d5170627353d35`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Sun, 19 Dec 2021 00:08:26 GMT
RUN yum update -y && yum install -y java-1.8.0-openjdk-devel-1.8.0.282.b08 java-1.8.0-openjdk-headless-1.8.0.282.b08 which &&     yum clean all
# Sun, 19 Dec 2021 00:08:29 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home-dir /usr/share/logstash --no-create-home       logstash
# Sun, 19 Dec 2021 00:08:45 GMT
RUN curl -Lo - http://localhost:8000/logstash-6.8.22.tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-6.8.22 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Sun, 19 Dec 2021 00:08:47 GMT
WORKDIR /usr/share/logstash
# Sun, 19 Dec 2021 00:08:47 GMT
ENV ELASTIC_CONTAINER=true
# Sun, 19 Dec 2021 00:08:47 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 19 Dec 2021 00:08:47 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Sun, 19 Dec 2021 00:08:47 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Sun, 19 Dec 2021 00:08:47 GMT
ADD file:2ef21d4766eab3ac48ed3847c8b8d05554f1fd0b39061cba66c9ac93240087fa in config/ 
# Sun, 19 Dec 2021 00:08:48 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Sun, 19 Dec 2021 00:08:48 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Sun, 19 Dec 2021 00:08:48 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Sun, 19 Dec 2021 00:08:48 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Sun, 19 Dec 2021 00:08:49 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Sun, 19 Dec 2021 00:08:49 GMT
USER 1000
# Sun, 19 Dec 2021 00:08:49 GMT
ADD file:c571f1340b3840928052ac69357eca598068bd1a752b377b661e4a526205c25b in /usr/local/bin/ 
# Sun, 19 Dec 2021 00:08:49 GMT
EXPOSE 5044 9600
# Sun, 19 Dec 2021 00:08:49 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.label-schema.name=logstash org.label-schema.version=6.8.22 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash license=Elastic License
# Sun, 19 Dec 2021 00:08:49 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb3374f70910dc0549792b498598d66090072e569405f9a072b8825febbd2c0`  
		Last Modified: Sun, 19 Dec 2021 20:55:06 GMT  
		Size: 139.1 MB (139127023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99bc3d6f254a174d215a17e43a9009ea7b1dd8e6b9b26de0fcb39a5f33f6fe3`  
		Last Modified: Sun, 19 Dec 2021 20:54:53 GMT  
		Size: 1.8 KB (1819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3c9a99156763e5f01a0f8bc7fd60cf1e47378970ddfffa34bea1d1bc4c4256`  
		Last Modified: Sun, 19 Dec 2021 20:55:04 GMT  
		Size: 179.3 MB (179270793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c14bb4bc9be586ddc845da00aed59614c717aae4239c558d182044485a344d`  
		Last Modified: Sun, 19 Dec 2021 20:54:51 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e023c3b14598e5191001b96ed30b0539c4c50d663f9ef60fc6d993719a4853`  
		Last Modified: Sun, 19 Dec 2021 20:54:51 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e846f38396767b33f540f3a53c8c13f950126e7ca640b0ee3cecd25b6ab3650`  
		Last Modified: Sun, 19 Dec 2021 20:54:51 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd4a173375e2353eae38ba75df862e89e4cc1c114f0eaf0ddd72e18a6863fe5`  
		Last Modified: Sun, 19 Dec 2021 20:54:48 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cad91305a2b897e7b5bf834500abec9b81b79abf26d1594fade1b8f40384756`  
		Last Modified: Sun, 19 Dec 2021 20:54:48 GMT  
		Size: 2.7 KB (2682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39fc156a2ccdb91be0ff765efb9b57cb7e58f060dc4d750222f623af78e47d9f`  
		Last Modified: Sun, 19 Dec 2021 20:54:47 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39fc156a2ccdb91be0ff765efb9b57cb7e58f060dc4d750222f623af78e47d9f`  
		Last Modified: Sun, 19 Dec 2021 20:54:47 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7c366e236fee9eda27257bbdfc7bc993536336df86cd26ea1ab7c22d50dcd8`  
		Last Modified: Sun, 19 Dec 2021 20:54:47 GMT  
		Size: 1.7 MB (1663550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `logstash:7.16.2`

```console
$ docker pull logstash@sha256:a2be462b1f23aafda215bd5c96fb53c8f8e4f6161e237f06efd45e64e6d064b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `logstash:7.16.2` - linux; amd64

```console
$ docker pull logstash@sha256:a3f0ea205881847c0f72c07dd4e8cc49246f34c6cbefae35c3719f81552d812b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **503.6 MB (503572394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e5a301659d9e11e129c0f35c01074c10f32bfcc9c6f2312e567ee417b2eab7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Sat, 18 Dec 2021 21:00:10 GMT
RUN for iter in {1..10}; do yum update -y &&     yum install -y procps findutils tar gzip which shadow-utils &&     yum clean all && yum clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     yum clean all && yum clean metadata && sleep 10; done;     (exit $exit_code)
# Sat, 18 Dec 2021 21:00:11 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home-dir /usr/share/logstash --no-create-home       logstash
# Sat, 18 Dec 2021 21:00:34 GMT
RUN curl -Lo - http://localhost:8000/logstash-7.16.2-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.16.2 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Sat, 18 Dec 2021 21:00:37 GMT
WORKDIR /usr/share/logstash
# Sat, 18 Dec 2021 21:00:38 GMT
ENV ELASTIC_CONTAINER=true
# Sat, 18 Dec 2021 21:00:38 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Dec 2021 21:00:38 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Sat, 18 Dec 2021 21:00:38 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Sat, 18 Dec 2021 21:00:38 GMT
ADD file:4f39d77a8986c28d67e673d4691e69ca9c175574128b0819977c2d1bb0d6e950 in config/ 
# Sat, 18 Dec 2021 21:00:38 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Sat, 18 Dec 2021 21:00:39 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Sat, 18 Dec 2021 21:00:39 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Sat, 18 Dec 2021 21:00:39 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Sat, 18 Dec 2021 21:00:39 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Sat, 18 Dec 2021 21:00:39 GMT
USER 1000
# Sat, 18 Dec 2021 21:00:40 GMT
ADD file:bc2ff40ec3323fe4b7e3cc88ed3e05a6716f206361909a69b57058b5e140a579 in /usr/local/bin/ 
# Sat, 18 Dec 2021 21:00:40 GMT
EXPOSE 5044 9600
# Sat, 18 Dec 2021 21:00:40 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.16.2 org.opencontainers.image.version=7.16.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2021-12-18T19:42:46Z org.opencontainers.image.created=2021-12-18T19:42:46Z
# Sat, 18 Dec 2021 21:00:40 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c3ca6198004d7d0d22f52a714b46b2becfb3cb1c820e7b06a51ef1a0a30c1d`  
		Last Modified: Sun, 19 Dec 2021 18:59:38 GMT  
		Size: 57.6 MB (57552151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0d86179cf0d09b58a8093003b49db72ed5e3f029262833fc1ec2d013e4d9b1`  
		Last Modified: Sun, 19 Dec 2021 18:59:03 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab45c17c796165b66753c4104e78a0909bb300d2d5de054b9ae604cbd9795ad`  
		Last Modified: Sun, 19 Dec 2021 19:00:50 GMT  
		Size: 368.3 MB (368252233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f07a7dad20c90aaca53787c306b14f577d5924a81fd053caccec13b5915460`  
		Last Modified: Sun, 19 Dec 2021 18:58:59 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688f479e228d22c5419ea0921c877cac4a621f2481f65a2ad912e80a5c90ae56`  
		Last Modified: Sun, 19 Dec 2021 18:58:58 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54982bc6eed794b07f5951b0385364abf30b67b0fb8131ccdf6aa1470aaeb1b`  
		Last Modified: Sun, 19 Dec 2021 18:58:57 GMT  
		Size: 480.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:490e23f550b176b71fa9997b1eaa86d3a904128542e1834fa9d25a92c5cc0d9a`  
		Last Modified: Sun, 19 Dec 2021 18:58:57 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ce1a615e064c1e46891f50bcbb46ddd6b0644d34aca7e9f3414c671649d2dc`  
		Last Modified: Sun, 19 Dec 2021 18:58:56 GMT  
		Size: 2.8 KB (2812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb11b460dfc6a01b1132b9bb461b68874a447c665e4360a398057c140f3330d`  
		Last Modified: Sun, 19 Dec 2021 18:58:52 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb11b460dfc6a01b1132b9bb461b68874a447c665e4360a398057c140f3330d`  
		Last Modified: Sun, 19 Dec 2021 18:58:52 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165ca4b8efa51c509f5d516ad65dba89c98fec7e9c1b1099fba83d54fc9d436f`  
		Last Modified: Sun, 19 Dec 2021 18:58:54 GMT  
		Size: 1.7 MB (1663764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `logstash:7.16.2` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:c2350fb6b74b694615e628764b338a2885ea55d7cfdd4344feb1e5ed41b7f12f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **805.3 MB (805303628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c8401c9eb71c92ee9955ec8fd7b69062d2704b3f148fcbe0ad9f15909a9acba`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Sat, 18 Dec 2021 20:05:57 GMT
RUN for iter in {1..10}; do yum install -y http://mirror.centos.org/centos/7/updates/x86_64/Packages/bind-license-9.11.4-26.P2.el7_9.5.noarch.rpm &&     yum clean all &&     yum clean metadata &&     exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     yum clean all &&     yum clean metadata && sleep 10; done;     (exit $exit_code)
# Sat, 18 Dec 2021 20:07:29 GMT
RUN for iter in {1..10}; do yum update -y &&     yum install -y procps findutils tar gzip which shadow-utils &&     yum clean all && yum clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     yum clean all && yum clean metadata && sleep 10; done;     (exit $exit_code)
# Sat, 18 Dec 2021 20:07:32 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home-dir /usr/share/logstash --no-create-home       logstash
# Sat, 18 Dec 2021 20:07:52 GMT
RUN curl -Lo - http://localhost:8000/logstash-7.16.2-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.16.2 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Sat, 18 Dec 2021 20:07:54 GMT
WORKDIR /usr/share/logstash
# Sat, 18 Dec 2021 20:07:54 GMT
ENV ELASTIC_CONTAINER=true
# Sat, 18 Dec 2021 20:07:54 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Dec 2021 20:07:55 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Sat, 18 Dec 2021 20:07:55 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Sat, 18 Dec 2021 20:07:55 GMT
ADD file:4f39d77a8986c28d67e673d4691e69ca9c175574128b0819977c2d1bb0d6e950 in config/ 
# Sat, 18 Dec 2021 20:07:55 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Sat, 18 Dec 2021 20:07:55 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Sat, 18 Dec 2021 20:07:55 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Sat, 18 Dec 2021 20:07:55 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Sat, 18 Dec 2021 20:07:56 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Sat, 18 Dec 2021 20:07:56 GMT
USER 1000
# Sat, 18 Dec 2021 20:07:56 GMT
ADD file:86be8b3554008b0941aee895258eda0ddb8a6aa71aaa83d0b5f7ef3c5ef5697e in /usr/local/bin/ 
# Sat, 18 Dec 2021 20:07:56 GMT
EXPOSE 5044 9600
# Sat, 18 Dec 2021 20:07:56 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.16.2 org.opencontainers.image.version=7.16.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2021-12-18T19:44:11+00:00 org.opencontainers.image.created=2021-12-18T19:44:11+00:00
# Sat, 18 Dec 2021 20:07:56 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e22c994e04d185cbe3bde1cd97f5c58be03fa5ff598703efe48c22af35a969`  
		Last Modified: Mon, 20 Dec 2021 13:28:27 GMT  
		Size: 6.3 MB (6297485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63127af4085917c51829ff5302f0e32394478d8a2705e46f576136605a115faf`  
		Last Modified: Mon, 20 Dec 2021 13:42:54 GMT  
		Size: 324.1 MB (324128749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9869f71e582fbf67895471266f86193ffd212d2bd37e52e010d1d0a5b3473bd3`  
		Last Modified: Mon, 20 Dec 2021 13:28:04 GMT  
		Size: 1.8 KB (1826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2f0934cfacddcd9b6f026c05b99da617f70630cb1c245203333b9260ccbcfc`  
		Last Modified: Tue, 21 Dec 2021 00:43:36 GMT  
		Size: 365.0 MB (364965262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:954001ff78ecbc1ce0c8171c671775923bd0d1e8eeb43f6f2fc58379e38ac5d4`  
		Last Modified: Tue, 21 Dec 2021 00:43:01 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c5a03b4e9a22c18cdd96db77cea38691b078284c6403cd6850bb0bb82d2118`  
		Last Modified: Tue, 21 Dec 2021 00:43:01 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387f22b6368abfa49396004477c66df935ef4462022a5c00f299081fbd688aea`  
		Last Modified: Tue, 21 Dec 2021 00:42:59 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aad3adf94a954c6ce1bddf7c75a3d161cd74b74281b10de46738067c0821494`  
		Last Modified: Tue, 21 Dec 2021 00:42:59 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8f18c19168272ff7e91a136bdf26bff872807cbb6cc57f7a8b0f32f9b0216d`  
		Last Modified: Tue, 21 Dec 2021 00:42:59 GMT  
		Size: 2.8 KB (2809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f73b191a52af8bdbd4839f691121a36922895be0b2eedb4f3c0af763819be04`  
		Last Modified: Tue, 21 Dec 2021 00:42:59 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f73b191a52af8bdbd4839f691121a36922895be0b2eedb4f3c0af763819be04`  
		Last Modified: Tue, 21 Dec 2021 00:42:59 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d995ae082094dda286de735eb5243a7cf719b8586143eb269bbde629a77a2d71`  
		Last Modified: Tue, 21 Dec 2021 00:42:59 GMT  
		Size: 1.5 MB (1530120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
