<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:6.8.13`](#logstash6813)
-	[`logstash:7.10.1`](#logstash7101)

## `logstash:6.8.13`

```console
$ docker pull logstash@sha256:40827a135885cb06ef8794fbed75d3957887676803b54ca7b23283dde9d4e6ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `logstash:6.8.13` - linux; amd64

```console
$ docker pull logstash@sha256:a407a7d7ff8fab4a3fedf6ec0bcca214d7eaaee87a3b9b69cf34e58821164dde
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.1 MB (343125627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5208112d67964df5eb839a4965ddde68820d9a2fa93600ace44175b6fa68876a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 10 Aug 2020 18:20:08 GMT
ADD file:61908381d3142ffba798ae9a904476d19b197ab79d0338f14bec0f76649df8d4 in / 
# Mon, 10 Aug 2020 18:20:09 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200809 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-08-09 00:00:00+01:00
# Mon, 10 Aug 2020 18:20:09 GMT
CMD ["/bin/bash"]
# Fri, 16 Oct 2020 10:54:00 GMT
RUN yum update -y && yum install -y java-1.8.0-openjdk-devel which &&     yum clean all
# Fri, 16 Oct 2020 10:54:03 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home-dir /usr/share/logstash --no-create-home       logstash
# Fri, 16 Oct 2020 10:54:24 GMT
RUN curl -Lo - http://localhost:8000/logstash-6.8.13.tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-6.8.13 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Fri, 16 Oct 2020 10:54:25 GMT
WORKDIR /usr/share/logstash
# Fri, 16 Oct 2020 10:54:25 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 16 Oct 2020 10:54:27 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Oct 2020 10:54:27 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Fri, 16 Oct 2020 10:54:28 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Fri, 16 Oct 2020 10:54:28 GMT
ADD file:2ef21d4766eab3ac48ed3847c8b8d05554f1fd0b39061cba66c9ac93240087fa in config/ 
# Fri, 16 Oct 2020 10:54:28 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Fri, 16 Oct 2020 10:54:30 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Fri, 16 Oct 2020 10:54:31 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Fri, 16 Oct 2020 10:54:31 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Fri, 16 Oct 2020 10:54:32 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Fri, 16 Oct 2020 10:54:32 GMT
USER 1000
# Fri, 16 Oct 2020 10:54:32 GMT
ADD file:571dd4a165fa42134dca8ddb671372023424aeaef9b0ed94f044c92e999f584e in /usr/local/bin/ 
# Fri, 16 Oct 2020 10:54:32 GMT
EXPOSE 5044 9600
# Fri, 16 Oct 2020 10:54:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.label-schema.name=logstash org.label-schema.version=6.8.13 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash license=Elastic License
# Fri, 16 Oct 2020 10:54:33 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:75f829a71a1c5277a7abf55495ac8d16759691d980bf1d931795e5eb68a294c0`  
		Last Modified: Mon, 10 Aug 2020 18:21:46 GMT  
		Size: 75.9 MB (75863188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d954755df0bb276bdf2f6f9e98afb888404cc93fc3bb1eb5619339442ba978`  
		Last Modified: Thu, 22 Oct 2020 13:54:14 GMT  
		Size: 88.7 MB (88660545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666bc8198c42f89a73824c48c2147064c0359bf2b72fb9b262b7920b22158792`  
		Last Modified: Thu, 22 Oct 2020 13:53:58 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb060f05750ac8a1e7aea69ab8f828deceb459f27f58612517de45f328fc9aa`  
		Last Modified: Thu, 22 Oct 2020 13:54:14 GMT  
		Size: 177.6 MB (177590449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5170fcd539a67569026d2a7fae5244ef60261757aaea1a9a8e46f8fdb285749a`  
		Last Modified: Thu, 22 Oct 2020 13:53:57 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d7c258fd94ec28db31d1c1d94a95b5bd72166239166cc7bc033ab99b5f1174`  
		Last Modified: Thu, 22 Oct 2020 13:53:55 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc3ec5c4a216960a2898c83e430124c4e2b59e94bfd5c70379d5e16a72cf541`  
		Last Modified: Thu, 22 Oct 2020 13:53:53 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fea6c1f9ebcca2bedc2b835949a03294b060fa080e8498442525e3fab31e812`  
		Last Modified: Thu, 22 Oct 2020 13:53:53 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be2cd5b8f9cccde1104c31c886118101777fbb170f48fccc986bab7a488ba3bb`  
		Last Modified: Thu, 22 Oct 2020 13:53:51 GMT  
		Size: 2.7 KB (2675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9754cde9522416d20e515b9b80be76f189fb660104df48e1f9a2c08970283b7`  
		Last Modified: Thu, 22 Oct 2020 13:53:49 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9754cde9522416d20e515b9b80be76f189fb660104df48e1f9a2c08970283b7`  
		Last Modified: Thu, 22 Oct 2020 13:53:49 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd1797cb5c8353f28d8e40394f0d1a140665ab67bb9f2fe26cce998331a4a0db`  
		Last Modified: Thu, 22 Oct 2020 13:53:48 GMT  
		Size: 1.0 MB (1004570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `logstash:7.10.1`

```console
$ docker pull logstash@sha256:c37e21ed82561791d095a7f9f617ea123bc255b32aa9ee61b7713cbd287749c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `logstash:7.10.1` - linux; amd64

```console
$ docker pull logstash@sha256:40e498c756691211d6a64d6332f0c19a87fc72089f69aef671227a73cabf0cb7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.6 MB (460562999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ae9aeccc0ed11f6151033337a6c5c8ec8d4a9fd83d29ff9ecb0f096786d10d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 05 Dec 2020 03:42:45 GMT
RUN yum update -y && yum install -y procps findutils tar gzip which shadow-utils &&     yum clean all
# Sat, 05 Dec 2020 03:42:47 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home-dir /usr/share/logstash --no-create-home       logstash
# Sat, 05 Dec 2020 03:43:17 GMT
RUN curl -Lo - http://localhost:8000/logstash-7.10.1-linux-x86_64.tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.10.1 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Sat, 05 Dec 2020 03:43:18 GMT
WORKDIR /usr/share/logstash
# Sat, 05 Dec 2020 03:43:18 GMT
ENV ELASTIC_CONTAINER=true
# Sat, 05 Dec 2020 03:43:18 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Dec 2020 03:43:19 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Sat, 05 Dec 2020 03:43:20 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Sat, 05 Dec 2020 03:43:22 GMT
ADD file:4f39d77a8986c28d67e673d4691e69ca9c175574128b0819977c2d1bb0d6e950 in config/ 
# Sat, 05 Dec 2020 03:43:24 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Sat, 05 Dec 2020 03:43:27 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Sat, 05 Dec 2020 03:43:27 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Sat, 05 Dec 2020 03:43:28 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Sat, 05 Dec 2020 03:43:30 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Sat, 05 Dec 2020 03:43:31 GMT
USER 1000
# Sat, 05 Dec 2020 03:43:32 GMT
ADD file:4fc35f1873d25f5258bad3492de23d09cc33fd409639a119015123b4adae1db5 in /usr/local/bin/ 
# Sat, 05 Dec 2020 03:43:33 GMT
EXPOSE 5044 9600
# Sat, 05 Dec 2020 03:43:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.10.1 org.opencontainers.image.version=7.10.1 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2020-12-05T03:00:47Z org.opencontainers.image.created=2020-12-05T03:00:47Z
# Sat, 05 Dec 2020 03:43:33 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60cd6984aa1c663ad6579dfc1ba8de6357bbbbb347c0d21f70b8c431abab3a93`  
		Last Modified: Wed, 09 Dec 2020 14:21:04 GMT  
		Size: 29.7 MB (29706553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61331f8cfbc27ff4ee6dd8b23ac81132f42faa56acfcaef12fc3c6036922abf2`  
		Last Modified: Wed, 09 Dec 2020 14:20:58 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24abc09771b6f0d22abf1ce8b28b4a8886653590d399e23a79b24b6495598dd`  
		Last Modified: Wed, 09 Dec 2020 14:21:27 GMT  
		Size: 353.7 MB (353747686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e5d9bfea4202d2b0c442b217f09190fbba21aafad00f14c9ffd1683ed78526`  
		Last Modified: Wed, 09 Dec 2020 14:20:56 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c53485a22b71f6ad127f56fd5159fca809f47bbca46a742954d83ae86edaeb`  
		Last Modified: Wed, 09 Dec 2020 14:20:54 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df9197dd971c7abc8f5a2fe17bfeb07d233d22b78e254bcf90eb30b089927fec`  
		Last Modified: Wed, 09 Dec 2020 14:20:54 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23caab6d34d96a9a9c2df991e4630b401593f9ad157d7f78163cb28f406f2b3`  
		Last Modified: Wed, 09 Dec 2020 14:20:52 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8acf0de931286ac3752d4db2f54dfed542ebf3551dd04c3beed19e2d7f15a6`  
		Last Modified: Wed, 09 Dec 2020 14:20:51 GMT  
		Size: 2.8 KB (2763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48352b37601d74d78d89096c9eda8f652f3e8a81eddd4ee31d1b7bb5cf5e04a8`  
		Last Modified: Wed, 09 Dec 2020 14:20:50 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48352b37601d74d78d89096c9eda8f652f3e8a81eddd4ee31d1b7bb5cf5e04a8`  
		Last Modified: Wed, 09 Dec 2020 14:20:50 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a51a76361bf8a7dd109f947536875d7bc39f995e0ed536f826373d34a57d1d`  
		Last Modified: Wed, 09 Dec 2020 14:20:49 GMT  
		Size: 1.0 MB (1004614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
