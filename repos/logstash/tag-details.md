<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:6.8.15`](#logstash6815)
-	[`logstash:7.12.0`](#logstash7120)

## `logstash:6.8.15`

```console
$ docker pull logstash@sha256:de1c899e9acd7ebf22f35ed85dd052be62b4c298ba6b8c4359a31edb9005b095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `logstash:6.8.15` - linux; amd64

```console
$ docker pull logstash@sha256:2163988cb6afed70b3fc4fdd3dadbb1b9df3cff724ae35a54606ea8e4ca4f81c
```

-	Docker Version: 20.10.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.6 MB (381577474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5562e14c18c34ff1dfc4e535670dd8093cf6bc349b9246acbc3dfca071bc873`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Thu, 18 Mar 2021 05:32:57 GMT
RUN yum update -y && yum install -y java-1.8.0-openjdk-devel which &&     yum clean all
# Thu, 18 Mar 2021 05:32:59 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home-dir /usr/share/logstash --no-create-home       logstash
# Thu, 18 Mar 2021 05:33:15 GMT
RUN curl -Lo - http://localhost:8000/logstash-6.8.15.tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-6.8.15 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Thu, 18 Mar 2021 05:33:17 GMT
WORKDIR /usr/share/logstash
# Thu, 18 Mar 2021 05:33:17 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Mar 2021 05:33:17 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Mar 2021 05:33:17 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Thu, 18 Mar 2021 05:33:18 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Thu, 18 Mar 2021 05:33:18 GMT
ADD file:2ef21d4766eab3ac48ed3847c8b8d05554f1fd0b39061cba66c9ac93240087fa in config/ 
# Thu, 18 Mar 2021 05:33:18 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Thu, 18 Mar 2021 05:33:18 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Thu, 18 Mar 2021 05:33:18 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 18 Mar 2021 05:33:19 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Thu, 18 Mar 2021 05:33:19 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Thu, 18 Mar 2021 05:33:19 GMT
USER 1000
# Thu, 18 Mar 2021 05:33:19 GMT
ADD file:c92f9dee23c3c5a04a654972a270462e21648cf6cc8c61ea9ea9b75e6f2d6089 in /usr/local/bin/ 
# Thu, 18 Mar 2021 05:33:20 GMT
EXPOSE 5044 9600
# Thu, 18 Mar 2021 05:33:20 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.label-schema.name=logstash org.label-schema.version=6.8.15 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash license=Elastic License
# Thu, 18 Mar 2021 05:33:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4dee90a7b63b1c1b646b0595e0eecbe473413e4b0858036bda0b5735f69a9d`  
		Last Modified: Tue, 23 Mar 2021 13:51:14 GMT  
		Size: 126.9 MB (126877497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93cdcdbddec4fda1d2f3d425b9deb2e9e4b730e8e7e97eb080cb8990866819a`  
		Last Modified: Tue, 23 Mar 2021 13:50:53 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963ffe6f1798cba728667afbe2a241f07f4c4a69c801a35b7812ce58232bb1b0`  
		Last Modified: Tue, 23 Mar 2021 13:51:09 GMT  
		Size: 177.6 MB (177591402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf23a9986a41e43c928a36f702d76389fd1477177530eff671f3e9d1be76b8d`  
		Last Modified: Tue, 23 Mar 2021 13:50:51 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb0ba9e7a929ae61489c2d449bac840775c7fd154cceea8db91d978d496a734`  
		Last Modified: Tue, 23 Mar 2021 13:50:50 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e224c39806ee179fae6bad0eb4113de0718784d85911b44bf97fb8b2e4ae806`  
		Last Modified: Tue, 23 Mar 2021 13:50:50 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74b6876f613409145b976516c001b7269261fb0ac87b3b57d836e82dcf94978`  
		Last Modified: Tue, 23 Mar 2021 13:50:48 GMT  
		Size: 305.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e30fdfdca719b5e482adcd26c672c64f0afe28e253879d4f02dca0f0f6d8f0`  
		Last Modified: Tue, 23 Mar 2021 13:50:48 GMT  
		Size: 2.7 KB (2675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b8bd053e3bbb8b363a2a435e5212bd33b9345f76374ad76b1ccedf46ee7e25f`  
		Last Modified: Tue, 23 Mar 2021 13:50:47 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b8bd053e3bbb8b363a2a435e5212bd33b9345f76374ad76b1ccedf46ee7e25f`  
		Last Modified: Tue, 23 Mar 2021 13:50:47 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085c1a83f4dc4d172d49e19ce89363c6feafd25500bb3216621178d994fd14e8`  
		Last Modified: Tue, 23 Mar 2021 13:50:46 GMT  
		Size: 1.0 MB (1004511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `logstash:7.12.0`

```console
$ docker pull logstash@sha256:9529ed3a4339fbafd4893d67151ac47811d55c8ac961089ee0f73927b8b56cea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `logstash:7.12.0` - linux; amd64

```console
$ docker pull logstash@sha256:9288ce0d309fdf4a28be513c9c62f4701427bb63556802c5264a51aaab6eb1c4
```

-	Docker Version: 20.10.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.5 MB (493462595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c283394286f55a3815d5c4c1b083bcfe14c237bdd29525f013aad0e0664209f8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Thu, 18 Mar 2021 06:23:51 GMT
RUN yum update -y && yum install -y procps findutils tar gzip which shadow-utils &&     yum clean all
# Thu, 18 Mar 2021 06:23:53 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home-dir /usr/share/logstash --no-create-home       logstash
# Thu, 18 Mar 2021 06:24:17 GMT
RUN curl -Lo - http://localhost:8000/logstash-7.12.0-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.12.0 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Thu, 18 Mar 2021 06:24:20 GMT
WORKDIR /usr/share/logstash
# Thu, 18 Mar 2021 06:24:21 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Mar 2021 06:24:21 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Mar 2021 06:24:21 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Thu, 18 Mar 2021 06:24:21 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Thu, 18 Mar 2021 06:24:22 GMT
ADD file:4f39d77a8986c28d67e673d4691e69ca9c175574128b0819977c2d1bb0d6e950 in config/ 
# Thu, 18 Mar 2021 06:24:22 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Thu, 18 Mar 2021 06:24:22 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Thu, 18 Mar 2021 06:24:22 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 18 Mar 2021 06:24:23 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Thu, 18 Mar 2021 06:24:23 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Thu, 18 Mar 2021 06:24:23 GMT
USER 1000
# Thu, 18 Mar 2021 06:24:23 GMT
ADD file:4fc35f1873d25f5258bad3492de23d09cc33fd409639a119015123b4adae1db5 in /usr/local/bin/ 
# Thu, 18 Mar 2021 06:24:24 GMT
EXPOSE 5044 9600
# Thu, 18 Mar 2021 06:24:24 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.12.0 org.opencontainers.image.version=7.12.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2021-03-18T05:13:33Z org.opencontainers.image.created=2021-03-18T05:13:33Z
# Thu, 18 Mar 2021 06:24:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa48cd88e6f7d55d8702cf2a4dd77f7ac1c559cb24b83bc475152c0dbbf4e5b`  
		Last Modified: Wed, 24 Mar 2021 04:36:34 GMT  
		Size: 45.3 MB (45272129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542ba1a206c180c0d86b669c0f568413c8f988d0257f151cd671f4e9f60b8da0`  
		Last Modified: Wed, 24 Mar 2021 04:36:11 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdfc1de001e401d4c12c4f02f19779864d6d65b3319fdbe2adc270d377e44a27`  
		Last Modified: Wed, 24 Mar 2021 04:38:58 GMT  
		Size: 371.1 MB (371081658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2fa217ed3757405a60e7992cb48718a8b02a036749df95998422b0c7b7a117`  
		Last Modified: Wed, 24 Mar 2021 04:36:05 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45467d7711d8ff825d6140ca10e61d61522c7d8e872ffada3576b7ba8527be7`  
		Last Modified: Wed, 24 Mar 2021 04:36:04 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd12e8564c4e4ec03ba9c1edc523f61b6a041851b3839b000e57d2e62740dccf`  
		Last Modified: Wed, 24 Mar 2021 04:36:03 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a42fb850ead823e484e20bc0e18cfb57a758a341c2bd4f345c6ced49bb2fa8`  
		Last Modified: Wed, 24 Mar 2021 04:35:57 GMT  
		Size: 305.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b799d16e97cd73783ed8c8421cdf34cf4aaa4e05e4b67c5ebe56b4e497c60d`  
		Last Modified: Wed, 24 Mar 2021 04:35:59 GMT  
		Size: 2.8 KB (2766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdcabc1b2593a97a22c6a725beb8dac8d6bf7116a663de6076361ad99434ae0`  
		Last Modified: Wed, 24 Mar 2021 04:35:55 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdcabc1b2593a97a22c6a725beb8dac8d6bf7116a663de6076361ad99434ae0`  
		Last Modified: Wed, 24 Mar 2021 04:35:55 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a980ed74ac983bb475eaa9e70e4e2058350a1bb7c29f837d84366b09751021a`  
		Last Modified: Wed, 24 Mar 2021 04:35:57 GMT  
		Size: 1.0 MB (1004617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
