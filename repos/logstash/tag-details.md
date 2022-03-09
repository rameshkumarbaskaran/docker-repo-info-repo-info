<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:6.8.23`](#logstash6823)
-	[`logstash:7.17.1`](#logstash7171)
-	[`logstash:8.1.0`](#logstash810)

## `logstash:6.8.23`

```console
$ docker pull logstash@sha256:53d822de31e74c91dcb623abf0d0bfd95192ee571e695e39ea4fe2af626c9232
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `logstash:6.8.23` - linux; amd64

```console
$ docker pull logstash@sha256:347be947d25fad34bcb808af6884c9f7c06a3d9a1f9599d036bb4d05bd2a46a8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.6 MB (395596751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e03e2750214e21b7f3a5a7b5cf55db2adb0aad5eb897eb03e77e05b2e6a1ebb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Thu, 06 Jan 2022 20:50:28 GMT
RUN yum update -y && yum install -y java-1.8.0-openjdk-devel-1.8.0.282.b08 java-1.8.0-openjdk-headless-1.8.0.282.b08 which &&     yum clean all
# Thu, 06 Jan 2022 20:50:30 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home-dir /usr/share/logstash --no-create-home       logstash
# Thu, 06 Jan 2022 20:50:46 GMT
RUN curl -Lo - http://localhost:8000/logstash-6.8.23.tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-6.8.23 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Thu, 06 Jan 2022 20:50:48 GMT
WORKDIR /usr/share/logstash
# Thu, 06 Jan 2022 20:50:48 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 06 Jan 2022 20:50:48 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jan 2022 20:50:49 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Thu, 06 Jan 2022 20:50:49 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Thu, 06 Jan 2022 20:50:49 GMT
ADD file:2ef21d4766eab3ac48ed3847c8b8d05554f1fd0b39061cba66c9ac93240087fa in config/ 
# Thu, 06 Jan 2022 20:50:49 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Thu, 06 Jan 2022 20:50:49 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Thu, 06 Jan 2022 20:50:50 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 06 Jan 2022 20:50:50 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Thu, 06 Jan 2022 20:50:50 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Thu, 06 Jan 2022 20:50:50 GMT
USER 1000
# Thu, 06 Jan 2022 20:50:50 GMT
ADD file:c571f1340b3840928052ac69357eca598068bd1a752b377b661e4a526205c25b in /usr/local/bin/ 
# Thu, 06 Jan 2022 20:50:51 GMT
EXPOSE 5044 9600
# Thu, 06 Jan 2022 20:50:51 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.label-schema.name=logstash org.label-schema.version=6.8.23 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash license=Elastic License
# Thu, 06 Jan 2022 20:50:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b1fb6f60b9250e42308ecf6503a441f9fc10b2e603a46e8767f9646555f43d`  
		Last Modified: Thu, 13 Jan 2022 16:12:17 GMT  
		Size: 139.1 MB (139127934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab13d3e354e35c347031eddca0d4bb20209d98ace9d3223a8358de9120fc72b`  
		Last Modified: Thu, 13 Jan 2022 16:11:56 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5ffc479f94b8a50d1647f4dfce26f0045e4fcb2055db4859ddcc840208bb96`  
		Last Modified: Thu, 13 Jan 2022 16:12:10 GMT  
		Size: 178.7 MB (178701203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88d374d1955f1098a61ca9fee227fce373072d7b9379399153efe94b7a0774f`  
		Last Modified: Thu, 13 Jan 2022 16:11:53 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07700abd6d6ac998267b237b6308c2722005f4b43601aadf6fe67b2ff92a4d3`  
		Last Modified: Thu, 13 Jan 2022 16:11:53 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a109f862359a4f53f5f8b0c2c48138454070d95f9b003bd4332b725f466223`  
		Last Modified: Thu, 13 Jan 2022 16:11:53 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8800e09be38effb116e9b61cbfe8810b2c48c0a08af461cbfd3e58d52bf84f`  
		Last Modified: Thu, 13 Jan 2022 16:11:50 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2282ae509684254b6426aa0880f79c8147ebf07313803f64519567c602654a`  
		Last Modified: Thu, 13 Jan 2022 16:11:50 GMT  
		Size: 2.7 KB (2676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b4125dcde9ccc2725f69e8f367f96efe05fc158888dad1fb7d3502c268f7e0`  
		Last Modified: Thu, 13 Jan 2022 16:11:50 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b4125dcde9ccc2725f69e8f367f96efe05fc158888dad1fb7d3502c268f7e0`  
		Last Modified: Thu, 13 Jan 2022 16:11:50 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963fece8ba60aee91b52cdf69bf5b3548119d5efb180f0c3ccb045831ac1cd18`  
		Last Modified: Thu, 13 Jan 2022 16:11:49 GMT  
		Size: 1.7 MB (1663550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `logstash:7.17.1`

```console
$ docker pull logstash@sha256:78f68b476a2f727cd8cef12610f4e7b7dd8434ba8cf45758326cfc1f299beb43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `logstash:7.17.1` - linux; amd64

```console
$ docker pull logstash@sha256:4b00f23786ab028a8a6803b06ccfa9c6e233c8952c1c2022f7a3d6074c5898d4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.9 MB (436913412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6867cdc686066dd4a5fe0df50513348df1a40067604770a465ef76d92b1ff8f2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 23 Feb 2022 23:40:34 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y &&     apt-get upgrade -y &&     apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code)
# Wed, 23 Feb 2022 23:40:35 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home /usr/share/logstash --no-create-home       logstash
# Wed, 23 Feb 2022 23:41:01 GMT
RUN curl -Lo - http://localhost:8000/logstash-7.17.1-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.1 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Wed, 23 Feb 2022 23:41:04 GMT
WORKDIR /usr/share/logstash
# Wed, 23 Feb 2022 23:41:04 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 23 Feb 2022 23:41:05 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Feb 2022 23:41:05 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Wed, 23 Feb 2022 23:41:05 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Wed, 23 Feb 2022 23:41:05 GMT
ADD file:4f39d77a8986c28d67e673d4691e69ca9c175574128b0819977c2d1bb0d6e950 in config/ 
# Wed, 23 Feb 2022 23:41:05 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Wed, 23 Feb 2022 23:41:06 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Wed, 23 Feb 2022 23:41:06 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 23 Feb 2022 23:41:06 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Wed, 23 Feb 2022 23:41:06 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Wed, 23 Feb 2022 23:41:06 GMT
USER 1000
# Wed, 23 Feb 2022 23:41:07 GMT
ADD file:bc2ff40ec3323fe4b7e3cc88ed3e05a6716f206361909a69b57058b5e140a579 in /usr/local/bin/ 
# Wed, 23 Feb 2022 23:41:07 GMT
EXPOSE 5044 9600
# Wed, 23 Feb 2022 23:41:07 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.1 org.opencontainers.image.version=7.17.1 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2022-02-23T22:23:10Z org.opencontainers.image.created=2022-02-23T22:23:10Z
# Wed, 23 Feb 2022 23:41:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:869740cab373cb4e24b08037aa862b56a8c5798f98d2f1e1bbe8aaaa0c9f20cd`  
		Last Modified: Tue, 01 Mar 2022 04:00:42 GMT  
		Size: 39.7 MB (39711775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9501681a4236f95934d8988ebf8de67eb9608d0e164a73dc3e45eb469cca26b2`  
		Last Modified: Tue, 01 Mar 2022 04:00:34 GMT  
		Size: 1.8 KB (1827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2a6f0d667162bc2833de08b283b82c48d86f0fda65cd4c4bed56fe7d2d2e1c`  
		Last Modified: Tue, 01 Mar 2022 04:01:19 GMT  
		Size: 367.0 MB (366966688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8500ce3174d2858f8109d9b2509929f6117fe71d74ac19e1e2ca5ceb218111b9`  
		Last Modified: Tue, 01 Mar 2022 04:00:32 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd9f510e031005b78892fb89ec4eb5970b61c25afdfc2a059db391207798ffc8`  
		Last Modified: Tue, 01 Mar 2022 04:00:30 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad19b15dcc5292d2c554994c454ac46d5316928135b1145f21a4aefa72921a80`  
		Last Modified: Tue, 01 Mar 2022 04:00:29 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066f96dfc588192827ff8b2ef25b67258fecd5bf56582d9b6586f986d1815ae0`  
		Last Modified: Tue, 01 Mar 2022 04:00:28 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d0d1c896fadd28d3fcb48a46a02f27ad0ef1c65d37e7765fb9d43579959d63`  
		Last Modified: Tue, 01 Mar 2022 04:00:27 GMT  
		Size: 2.8 KB (2810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5029db52cc072a1a4651e3f524b28194b9c9f0675873e871c817f4b27b55fd2c`  
		Last Modified: Tue, 01 Mar 2022 04:00:25 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5029db52cc072a1a4651e3f524b28194b9c9f0675873e871c817f4b27b55fd2c`  
		Last Modified: Tue, 01 Mar 2022 04:00:25 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dcf0a9df4e11f0a7c5ac5e7a9f1ea07db6ac6aca35b917acaa00de9db39696f`  
		Last Modified: Tue, 01 Mar 2022 04:00:24 GMT  
		Size: 1.7 MB (1663767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `logstash:7.17.1` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:7e837d6b07f0432af31084919fe240135a38ef118e026c3a15b9c50924880bf4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.9 MB (427874582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469f6b4baaeb29fa98b1feed6dc42760cb72b012ac62055f6a4ff1edb52ff932`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 23 Feb 2022 22:45:54 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y &&     apt-get upgrade -y &&     apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code)
# Wed, 23 Feb 2022 22:45:55 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home /usr/share/logstash --no-create-home       logstash
# Wed, 23 Feb 2022 22:46:13 GMT
RUN curl -Lo - http://localhost:8000/logstash-7.17.1-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.1 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Wed, 23 Feb 2022 22:46:15 GMT
WORKDIR /usr/share/logstash
# Wed, 23 Feb 2022 22:46:15 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 23 Feb 2022 22:46:15 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Feb 2022 22:46:15 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Wed, 23 Feb 2022 22:46:16 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Wed, 23 Feb 2022 22:46:16 GMT
ADD file:4f39d77a8986c28d67e673d4691e69ca9c175574128b0819977c2d1bb0d6e950 in config/ 
# Wed, 23 Feb 2022 22:46:16 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Wed, 23 Feb 2022 22:46:16 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Wed, 23 Feb 2022 22:46:16 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 23 Feb 2022 22:46:16 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Wed, 23 Feb 2022 22:46:17 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Wed, 23 Feb 2022 22:46:17 GMT
USER 1000
# Wed, 23 Feb 2022 22:46:17 GMT
ADD file:86be8b3554008b0941aee895258eda0ddb8a6aa71aaa83d0b5f7ef3c5ef5697e in /usr/local/bin/ 
# Wed, 23 Feb 2022 22:46:17 GMT
EXPOSE 5044 9600
# Wed, 23 Feb 2022 22:46:17 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.1 org.opencontainers.image.version=7.17.1 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2022-02-23T22:24:19+00:00 org.opencontainers.image.created=2022-02-23T22:24:19+00:00
# Wed, 23 Feb 2022 22:46:17 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd90f70abb904972921dab34007ebc18d299a6ba7f61614bbc4a8262914c55c0`  
		Last Modified: Wed, 02 Mar 2022 16:05:39 GMT  
		Size: 35.5 MB (35489080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54f644c418c77e329fe7402ea9ce1e343c5ace85588c22a11ab786b7bbb82f5`  
		Last Modified: Wed, 02 Mar 2022 16:05:34 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255a48aeca3553f1ba342bf05e450e1b3d58724993310ef366cfed2aadc61b3a`  
		Last Modified: Wed, 02 Mar 2022 16:06:12 GMT  
		Size: 363.7 MB (363678673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc176bb1a33dcaedebb24862544ba21c7be693ccdb8e203079cd1d89af3fbe8`  
		Last Modified: Wed, 02 Mar 2022 16:05:34 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ee2535495bf3ee0e0ca58c3d22e50cfcd8705ae562fb5c33d3bd7cbad18893`  
		Last Modified: Wed, 02 Mar 2022 16:05:34 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d209b999c4ad404147321b650460e9365c604912130ff42144a89ce71a7ee7f`  
		Last Modified: Wed, 02 Mar 2022 16:05:32 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18719dde5e053f719721a6d33325ac202289b2f71f8618eb9cd774f5fbbfb82`  
		Last Modified: Wed, 02 Mar 2022 16:05:32 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f29dd1f46359873e13c72fba512072393470bb5cebc33b7b5d23b8df4042b7`  
		Last Modified: Wed, 02 Mar 2022 16:05:32 GMT  
		Size: 2.8 KB (2806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e55890d1d23225e60c44d0f84d2336f484a479cdb03764e3bf5626029fac0d`  
		Last Modified: Wed, 02 Mar 2022 16:05:31 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e55890d1d23225e60c44d0f84d2336f484a479cdb03764e3bf5626029fac0d`  
		Last Modified: Wed, 02 Mar 2022 16:05:31 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c042766f2e06ae9b45012bafa9b78212c08ac630767a1e97efd9e0bc94d487b9`  
		Last Modified: Wed, 02 Mar 2022 16:05:32 GMT  
		Size: 1.5 MB (1530117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `logstash:8.1.0`

```console
$ docker pull logstash@sha256:1e40d09ce8dbfc3c4bebe976a4a06544ff198e2193e377a3ca31f92678cf165e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `logstash:8.1.0` - linux; amd64

```console
$ docker pull logstash@sha256:0b464418a1eb5abb2e45bd1a6dbfb4349a4994e1713912459333a343c67062c5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.9 MB (424868451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:937d7a90c1119cc0ee34b466e9d0918119a1e4c23e8774eb4f6d4a0478c2f5b7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 15:48:38 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y &&     apt-get upgrade -y &&     apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code)
# Thu, 03 Mar 2022 15:48:39 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home /usr/share/logstash --no-create-home       logstash
# Thu, 03 Mar 2022 15:49:05 GMT
RUN curl -Lo - http://localhost:8000/logstash-8.1.0-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.1.0 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Thu, 03 Mar 2022 15:49:08 GMT
WORKDIR /usr/share/logstash
# Thu, 03 Mar 2022 15:49:08 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 03 Mar 2022 15:49:08 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 15:49:09 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Thu, 03 Mar 2022 15:49:09 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Thu, 03 Mar 2022 15:49:09 GMT
ADD file:4f39d77a8986c28d67e673d4691e69ca9c175574128b0819977c2d1bb0d6e950 in config/ 
# Thu, 03 Mar 2022 15:49:09 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Thu, 03 Mar 2022 15:49:09 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Thu, 03 Mar 2022 15:49:10 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 03 Mar 2022 15:49:10 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Thu, 03 Mar 2022 15:49:10 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Thu, 03 Mar 2022 15:49:10 GMT
USER 1000
# Thu, 03 Mar 2022 15:49:10 GMT
ADD file:74f1240397564c8006436b57526b98f8b3e9fcbad9cb9f7c905c223de143c5f3 in /usr/local/bin/ 
# Thu, 03 Mar 2022 15:49:10 GMT
EXPOSE 5044 9600
# Thu, 03 Mar 2022 15:49:11 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.1.0 org.opencontainers.image.version=8.1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2022-03-03T14:22:37Z org.opencontainers.image.created=2022-03-03T14:22:37Z
# Thu, 03 Mar 2022 15:49:11 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094b7c0396dbee76c47f39488684ad5d2d79b5f3d09a5eec6035a0fe4ff4b458`  
		Last Modified: Wed, 09 Mar 2022 21:21:52 GMT  
		Size: 46.3 MB (46334809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf744fd2fd861a974ca1f91283c4500e3bf4a44a114a1dd90b11b74cc99421a`  
		Last Modified: Wed, 09 Mar 2022 21:21:46 GMT  
		Size: 1.8 KB (1827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2fc31ccb2d9241bcc59337bb25e994220fce9d1588e2f0a9604e620e198a5a9`  
		Last Modified: Wed, 09 Mar 2022 21:22:13 GMT  
		Size: 348.3 MB (348298607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64302cb0600ae5829a47de957c2e56f0a694fbf875c89175e5234d1e36ec8140`  
		Last Modified: Wed, 09 Mar 2022 21:21:46 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd975acaf0584dd5d98b16f155a2eddb9660ef2415ccc968aec5706b1400352a`  
		Last Modified: Wed, 09 Mar 2022 21:21:45 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd514d03a628d4ea88ecbadd46228e320045d0ca518d35f7c7fa4d63a9887e35`  
		Last Modified: Wed, 09 Mar 2022 21:21:43 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92ff80c5d5e71f1e78c7e3e5d27e6ed89e72e625ad4f77f76c0cc52dc82a1c5`  
		Last Modified: Wed, 09 Mar 2022 21:21:43 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:513163dd6ced1b2c5202f7aa174895797ba608fa25373048074f15e33ac2bb7d`  
		Last Modified: Wed, 09 Mar 2022 21:21:43 GMT  
		Size: 2.8 KB (2833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec23a5db0f79bf305a423733903a56d79d94fa0205d4da9c9de902f1f76863c`  
		Last Modified: Wed, 09 Mar 2022 21:21:43 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec23a5db0f79bf305a423733903a56d79d94fa0205d4da9c9de902f1f76863c`  
		Last Modified: Wed, 09 Mar 2022 21:21:43 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6055aef0a8f1017c9dec5b74c72606d139639a7b5dcefbbd840dce618cd7cd0`  
		Last Modified: Wed, 09 Mar 2022 21:21:44 GMT  
		Size: 1.7 MB (1663832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `logstash:8.1.0` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:58fcb80f6e47c64ababc664c3c8dea601df48424b088525c594e3fb339033571
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.7 MB (414746810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76b21d88364405ea184a9b8ff8bf9adfba586aab5f77dc1df86fdf4ca0adfc6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 14:48:52 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y &&     apt-get upgrade -y &&     apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code)
# Thu, 03 Mar 2022 14:48:52 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home /usr/share/logstash --no-create-home       logstash
# Thu, 03 Mar 2022 14:49:13 GMT
RUN curl -Lo - http://localhost:8000/logstash-8.1.0-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.1.0 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Thu, 03 Mar 2022 14:49:15 GMT
WORKDIR /usr/share/logstash
# Thu, 03 Mar 2022 14:49:15 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 03 Mar 2022 14:49:15 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 14:49:15 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Thu, 03 Mar 2022 14:49:15 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Thu, 03 Mar 2022 14:49:15 GMT
ADD file:4f39d77a8986c28d67e673d4691e69ca9c175574128b0819977c2d1bb0d6e950 in config/ 
# Thu, 03 Mar 2022 14:49:16 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Thu, 03 Mar 2022 14:49:16 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Thu, 03 Mar 2022 14:49:16 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 03 Mar 2022 14:49:16 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Thu, 03 Mar 2022 14:49:16 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Thu, 03 Mar 2022 14:49:16 GMT
USER 1000
# Thu, 03 Mar 2022 14:49:17 GMT
ADD file:945c6fce9a9e80bbe91b66f2c2535aba760ab72a0b46cff684339f8e5b553444 in /usr/local/bin/ 
# Thu, 03 Mar 2022 14:49:17 GMT
EXPOSE 5044 9600
# Thu, 03 Mar 2022 14:49:17 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.1.0 org.opencontainers.image.version=8.1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2022-03-03T14:23:52+00:00 org.opencontainers.image.created=2022-03-03T14:23:52+00:00
# Thu, 03 Mar 2022 14:49:17 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a3e463ee04cf723193c4a4469accef70b437977f5a3b0361028415c1dde441`  
		Last Modified: Wed, 09 Mar 2022 21:43:14 GMT  
		Size: 41.0 MB (41026210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ced2d35e8f7bc894c8574fc6f86699b0edc96223418c941b537346c8b4d659`  
		Last Modified: Wed, 09 Mar 2022 21:43:09 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114217ca478e092d3a9fb10feb4628fa5ced75639b79f7c61742f24ae1c5fff5`  
		Last Modified: Wed, 09 Mar 2022 21:43:39 GMT  
		Size: 345.0 MB (345013766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f795506ce280decc01a1ba02a4b0d44c907f4a6ca31c267619607865e4e333e`  
		Last Modified: Wed, 09 Mar 2022 21:43:09 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15b5a0c8c75e17d98c84519364dee235326b81a2f5eb0ccabf93180840f8d72`  
		Last Modified: Wed, 09 Mar 2022 21:43:08 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfed04dd2b7c1a2a56446ca050ba6f856a16fa0a7ef239f07663dd602cd1315`  
		Last Modified: Wed, 09 Mar 2022 21:43:06 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca73bb6d131fd73bf0fd9bc08cf0cd91e5b85fd5343715c09a478863b89d451`  
		Last Modified: Wed, 09 Mar 2022 21:43:06 GMT  
		Size: 305.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae189185d9f16f3b46216c9a5aa7bb5ddfbccab042ebcf138b86476a57d3471`  
		Last Modified: Wed, 09 Mar 2022 21:43:06 GMT  
		Size: 2.8 KB (2831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9696e84647aae492df3f2521e0a9b7dc92cf5e1c68ccde57e6d26f1898149d5`  
		Last Modified: Wed, 09 Mar 2022 21:43:06 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9696e84647aae492df3f2521e0a9b7dc92cf5e1c68ccde57e6d26f1898149d5`  
		Last Modified: Wed, 09 Mar 2022 21:43:06 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ba215abb0b3c4f7c6944c80214f46c802b2395361492b8620791be3033700c`  
		Last Modified: Wed, 09 Mar 2022 21:43:06 GMT  
		Size: 1.5 MB (1530085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
