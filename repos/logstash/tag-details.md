<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:6.8.14`](#logstash6814)
-	[`logstash:7.11.1`](#logstash7111)

## `logstash:6.8.14`

```console
$ docker pull logstash@sha256:8cd91a724e750a80de456cce10eb0529d3cb1573c7c2f1964e13ceffcf8145ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `logstash:6.8.14` - linux; amd64

```console
$ docker pull logstash@sha256:9c5cc1c0daadc0bdb83960273a04dfdee1a2ee08f7440638731886fdfcb14b22
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.8 MB (368781995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12a44c3f695aaccbe72672546b40c5d902fd5454fb1883816de15cbe8794c29`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Tue, 02 Feb 2021 21:34:38 GMT
RUN yum update -y && yum install -y java-1.8.0-openjdk-devel which &&     yum clean all
# Tue, 02 Feb 2021 21:34:41 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home-dir /usr/share/logstash --no-create-home       logstash
# Tue, 02 Feb 2021 21:35:05 GMT
RUN curl -Lo - http://localhost:8000/logstash-6.8.14.tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-6.8.14 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Tue, 02 Feb 2021 21:35:05 GMT
WORKDIR /usr/share/logstash
# Tue, 02 Feb 2021 21:35:05 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Feb 2021 21:35:05 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Feb 2021 21:35:06 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Tue, 02 Feb 2021 21:35:06 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Tue, 02 Feb 2021 21:35:08 GMT
ADD file:2ef21d4766eab3ac48ed3847c8b8d05554f1fd0b39061cba66c9ac93240087fa in config/ 
# Tue, 02 Feb 2021 21:35:08 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Tue, 02 Feb 2021 21:35:10 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Tue, 02 Feb 2021 21:35:11 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 02 Feb 2021 21:35:11 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Tue, 02 Feb 2021 21:35:13 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Tue, 02 Feb 2021 21:35:13 GMT
USER 1000
# Tue, 02 Feb 2021 21:35:14 GMT
ADD file:c92f9dee23c3c5a04a654972a270462e21648cf6cc8c61ea9ea9b75e6f2d6089 in /usr/local/bin/ 
# Tue, 02 Feb 2021 21:35:14 GMT
EXPOSE 5044 9600
# Tue, 02 Feb 2021 21:35:14 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.label-schema.name=logstash org.label-schema.version=6.8.14 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash license=Elastic License
# Tue, 02 Feb 2021 21:35:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0351288d07ffaea4de95b44bcc7f101d605b3616bede8071427a4c1150ac51`  
		Last Modified: Wed, 10 Feb 2021 15:39:35 GMT  
		Size: 114.1 MB (114083737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7212ff6312ad18126a3f07e143127673ff168394d18c8e81b297bb2dd52bac3a`  
		Last Modified: Wed, 10 Feb 2021 15:39:16 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec4493ebf2f2d55be3969c5520e9ea89e61ad8b505fb8136ea2b16653306a7d9`  
		Last Modified: Wed, 10 Feb 2021 15:39:31 GMT  
		Size: 177.6 MB (177589706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a39609a827ff52a27e6d5dafdc78f0f2d1436e9fbc16debec2a966c9b32800`  
		Last Modified: Wed, 10 Feb 2021 15:39:14 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9c6f67847bce379f389b0a091b5e0931245ad0780182f45e88c076e3721a03`  
		Last Modified: Wed, 10 Feb 2021 15:39:13 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3776714e0a9abf6d1cf3d58e9f786be10ba899436db84f9702d8b138541b3018`  
		Last Modified: Wed, 10 Feb 2021 15:39:11 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c5f5f7d50891e35b4feb6a633a445a474adbb4f61294ca1d67d1cad99766a2`  
		Last Modified: Wed, 10 Feb 2021 15:39:11 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b320b5cbea88a89005928495d5b1db1ff0e57b78d616c1600a3436670fb1e7`  
		Last Modified: Wed, 10 Feb 2021 15:39:10 GMT  
		Size: 2.7 KB (2681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daefa3452ab51257366ad938b2a59c94dc0c9b783f2513e73e7383dea3a59105`  
		Last Modified: Wed, 10 Feb 2021 15:39:07 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daefa3452ab51257366ad938b2a59c94dc0c9b783f2513e73e7383dea3a59105`  
		Last Modified: Wed, 10 Feb 2021 15:39:07 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7295e170d49a0937298761ed848b4e73122d30685833e8bf126f435eac66f3`  
		Last Modified: Wed, 10 Feb 2021 15:39:07 GMT  
		Size: 1.0 MB (1004512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `logstash:7.11.1`

```console
$ docker pull logstash@sha256:4652c54d92b4c4ad3c99cfc1fa3d1cf6718b0f507abdbd334090c776af2cbd35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `logstash:7.11.1` - linux; amd64

```console
$ docker pull logstash@sha256:4968ab086cab801efc1c2796ace2c3c17755290ebc33b3a2c2de118e983c2dfc
```

-	Docker Version: 20.10.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **489.6 MB (489593148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abbebd2b69435c4b5b16e10b2d825264643a6b2600c46e6cd8ecf6570afe34f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Mon, 15 Feb 2021 13:47:08 GMT
RUN yum update -y && yum install -y procps findutils tar gzip which shadow-utils &&     yum clean all
# Mon, 15 Feb 2021 13:47:09 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home-dir /usr/share/logstash --no-create-home       logstash
# Mon, 15 Feb 2021 13:47:32 GMT
RUN curl -Lo - http://localhost:8000/logstash-7.11.1-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.11.1 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Mon, 15 Feb 2021 13:47:35 GMT
WORKDIR /usr/share/logstash
# Mon, 15 Feb 2021 13:47:36 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 15 Feb 2021 13:47:36 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Feb 2021 13:47:36 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Mon, 15 Feb 2021 13:47:36 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Mon, 15 Feb 2021 13:47:36 GMT
ADD file:4f39d77a8986c28d67e673d4691e69ca9c175574128b0819977c2d1bb0d6e950 in config/ 
# Mon, 15 Feb 2021 13:47:37 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Mon, 15 Feb 2021 13:47:37 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Mon, 15 Feb 2021 13:47:37 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Mon, 15 Feb 2021 13:47:37 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Mon, 15 Feb 2021 13:47:38 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Mon, 15 Feb 2021 13:47:38 GMT
USER 1000
# Mon, 15 Feb 2021 13:47:38 GMT
ADD file:4fc35f1873d25f5258bad3492de23d09cc33fd409639a119015123b4adae1db5 in /usr/local/bin/ 
# Mon, 15 Feb 2021 13:47:38 GMT
EXPOSE 5044 9600
# Mon, 15 Feb 2021 13:47:38 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.11.1 org.opencontainers.image.version=7.11.1 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2021-02-15T12:39:59Z org.opencontainers.image.created=2021-02-15T12:39:59Z
# Mon, 15 Feb 2021 13:47:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6f3a917408d1ac78e595182e2c0757eb1809758685cabde589a458a53d3df9`  
		Last Modified: Wed, 17 Feb 2021 14:58:10 GMT  
		Size: 45.3 MB (45273386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45bbbb99e18619810ffcea3c95dfc23b28de1306e5bfa3d5761d49216070100a`  
		Last Modified: Wed, 17 Feb 2021 14:58:01 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e32424e5bf74d278fcc05b0664c887afc1123d48312e9d25d9222a6bf00ab2c`  
		Last Modified: Wed, 17 Feb 2021 14:58:31 GMT  
		Size: 367.2 MB (367210961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4592f7516b5ca10eac54066af6acebd6e4301dbf7f22c485bbd6266c1923ec4e`  
		Last Modified: Wed, 17 Feb 2021 14:57:59 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:547858ea47838e7887e55cfeea60ec5e401703a59f96fc6274048790ec39e2ea`  
		Last Modified: Wed, 17 Feb 2021 14:57:58 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe91cd73f56c9da5a4e2b25179e18472aa9631e3679d9ffb7b3e336b9baed27b`  
		Last Modified: Wed, 17 Feb 2021 14:57:56 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5532534d4b2145a6f66d4337f41b0850afaa0b7827ecca669e9fbd203cac113`  
		Last Modified: Wed, 17 Feb 2021 14:57:56 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0adc40743566bc047ba5dd107f43b8962434c77230c90a28b29e4170c22d5507`  
		Last Modified: Wed, 17 Feb 2021 14:57:54 GMT  
		Size: 2.8 KB (2757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3831b23aeb0c02c0d90fef3fd4e94b37fe29f0f77efb44b9d39918c2e350a633`  
		Last Modified: Wed, 17 Feb 2021 14:57:53 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3831b23aeb0c02c0d90fef3fd4e94b37fe29f0f77efb44b9d39918c2e350a633`  
		Last Modified: Wed, 17 Feb 2021 14:57:53 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073224b21e696b36ec3a3dc201824484ac3c9cb2fa7200dcfefda28915b37b24`  
		Last Modified: Wed, 17 Feb 2021 14:57:52 GMT  
		Size: 1.0 MB (1004615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
