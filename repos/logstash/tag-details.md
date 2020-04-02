<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:6.8.8`](#logstash688)
-	[`logstash:7.6.2`](#logstash762)

## `logstash:6.8.8`

```console
$ docker pull logstash@sha256:4f1b895c2eca36d25aab8141443b88c187294ae922004bef613607a0580095ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `logstash:6.8.8` - linux; amd64

```console
$ docker pull logstash@sha256:80377ab548d829357796f9d7ba585f418a959efbc53f6c5799adb6cbe7e8548e
```

-	Docker Version: 19.03.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.7 MB (367655223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f44b376ef356b02e84071eae519ecaf11af49654e281cbba2c891bc3383620`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2020 00:52:23 GMT
RUN yum update -y && yum install -y java-1.8.0-openjdk-devel which &&     yum clean all
# Thu, 19 Mar 2020 00:52:24 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home-dir /usr/share/logstash --no-create-home       logstash
# Thu, 19 Mar 2020 00:52:43 GMT
RUN curl -Lo - http://localhost:8000/logstash-6.8.8.tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-6.8.8 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Thu, 19 Mar 2020 00:52:44 GMT
WORKDIR /usr/share/logstash
# Thu, 19 Mar 2020 00:52:44 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 19 Mar 2020 00:52:45 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Mar 2020 00:52:47 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Thu, 19 Mar 2020 00:52:48 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Thu, 19 Mar 2020 00:52:49 GMT
ADD file:2ef21d4766eab3ac48ed3847c8b8d05554f1fd0b39061cba66c9ac93240087fa in config/ 
# Thu, 19 Mar 2020 00:52:50 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Thu, 19 Mar 2020 00:52:51 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Thu, 19 Mar 2020 00:52:52 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 19 Mar 2020 00:52:52 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Thu, 19 Mar 2020 00:52:56 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Thu, 19 Mar 2020 00:52:56 GMT
USER 1000
# Thu, 19 Mar 2020 00:52:56 GMT
ADD file:cebf0ff7ebe120c237a4cd02789b4d90543b551aaeb6a2e695b7ed3070e28792 in /usr/local/bin/ 
# Thu, 19 Mar 2020 00:52:57 GMT
EXPOSE 5044 9600
# Thu, 19 Mar 2020 00:52:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.label-schema.name=logstash org.label-schema.version=6.8.8 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash license=Elastic License
# Thu, 19 Mar 2020 00:52:58 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9b588e2483a7d2303de062070d502c8c2cae404c0b63708551b4feb3647734`  
		Last Modified: Tue, 31 Mar 2020 16:08:29 GMT  
		Size: 110.2 MB (110209606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5589b6d68030675a136de5c4fa128d386e4c73d239f9fbdfedb05a376a8ed19e`  
		Last Modified: Tue, 31 Mar 2020 16:08:08 GMT  
		Size: 1.9 KB (1854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffc2a7adbe168e04f0004626fca6adc18e86ab6cb18340659edb983071e8170`  
		Last Modified: Tue, 31 Mar 2020 16:08:30 GMT  
		Size: 180.7 MB (180653508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3281acf1632309a17c43b8f4a66b7248851dc69023babc502acefeb4c6978487`  
		Last Modified: Tue, 31 Mar 2020 16:08:08 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f992bc0b53dd94a58216c150e765175804fde9abb791ee5a780a9ce02d9cf6bf`  
		Last Modified: Tue, 31 Mar 2020 16:08:07 GMT  
		Size: 291.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa54e80bc9635431a115b85821f425c5a0982e6a12064ada2aeeb8d958cb839`  
		Last Modified: Tue, 31 Mar 2020 16:08:05 GMT  
		Size: 456.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d9357716d5c37ab47beb739831aa5c76285838838abcc83e9f4f2839609bad5`  
		Last Modified: Tue, 31 Mar 2020 16:08:05 GMT  
		Size: 289.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cd124c8e0c7f4c33376a59922ceee099f26feb2e742ab8dcb10d3e34563797`  
		Last Modified: Tue, 31 Mar 2020 16:08:05 GMT  
		Size: 2.7 KB (2686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c076e24078610c2fdfb778756687db030b1c917c9f6ffe822cbbc2f4d474042`  
		Last Modified: Tue, 31 Mar 2020 16:08:05 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c076e24078610c2fdfb778756687db030b1c917c9f6ffe822cbbc2f4d474042`  
		Last Modified: Tue, 31 Mar 2020 16:08:05 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8e389d9dacf789bc128e09d4de1afe55f8e181ffc02969186abf67c9422ca1`  
		Last Modified: Tue, 31 Mar 2020 16:08:05 GMT  
		Size: 1.0 MB (1004422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `logstash:7.6.2`

```console
$ docker pull logstash@sha256:c486f8945885ef3e9b32e09c9f527793ed0d0bfde84c536b5491205ccf8c882d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `logstash:7.6.2` - linux; amd64

```console
$ docker pull logstash@sha256:66e67861ca60fc583fc44b65014abb9791a70a0494461120a556a2945511c3da
```

-	Docker Version: 19.03.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.7 MB (355715101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa5b3b1e9757f45947a4a4297cc7bfad80bc7451ac3ba9f36f81d92dc244daaf`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Thu, 26 Mar 2020 09:01:46 GMT
RUN yum update -y && yum install -y java-11-openjdk-devel which &&     yum clean all
# Thu, 26 Mar 2020 09:01:49 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home-dir /usr/share/logstash --no-create-home       logstash
# Thu, 26 Mar 2020 09:02:06 GMT
RUN curl -Lo - http://localhost:8000/logstash-7.6.2.tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.6.2 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Thu, 26 Mar 2020 09:02:08 GMT
WORKDIR /usr/share/logstash
# Thu, 26 Mar 2020 09:02:08 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 26 Mar 2020 09:02:08 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Mar 2020 09:02:09 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Thu, 26 Mar 2020 09:02:10 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Thu, 26 Mar 2020 09:02:10 GMT
ADD file:67a3543613849420f3c5597cdf7f793b85362365cfa372b40a93ed03d46feadc in config/ 
# Thu, 26 Mar 2020 09:02:12 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Thu, 26 Mar 2020 09:02:16 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Thu, 26 Mar 2020 09:02:17 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 26 Mar 2020 09:02:18 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Thu, 26 Mar 2020 09:02:20 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Thu, 26 Mar 2020 09:02:20 GMT
USER 1000
# Thu, 26 Mar 2020 09:02:21 GMT
ADD file:27413a36073280132d63a9a255bb2ff3bccb55f07e11020493fefa619a65018c in /usr/local/bin/ 
# Thu, 26 Mar 2020 09:02:21 GMT
EXPOSE 5044 9600
# Thu, 26 Mar 2020 09:02:21 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.label-schema.name=logstash org.label-schema.version=7.6.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash license=Elastic License
# Thu, 26 Mar 2020 09:02:22 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5938cf5635f6d71e5c2267777a07f9eab5517a0ecb79663fbc145f9ed57c257c`  
		Last Modified: Tue, 31 Mar 2020 16:22:16 GMT  
		Size: 105.5 MB (105546208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea38a5278bc342e6f7317097a12033fbbcbc7ca4d537e5c6451520f42abdcc2f`  
		Last Modified: Tue, 31 Mar 2020 16:21:57 GMT  
		Size: 1.9 KB (1855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c96ea47db28206670f51997ab237119cbc52766061256f6d3cc38a89c2979bd`  
		Last Modified: Tue, 31 Mar 2020 16:22:17 GMT  
		Size: 173.4 MB (173376687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee9458d31f72570b32f8728d612cbd362c8e492ff143bb373a77801509a3cbc`  
		Last Modified: Tue, 31 Mar 2020 16:21:55 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d132291e0acc70d3afcdb49dd560bde83b4167a70ac39bd3537ad37e8ba594d9`  
		Last Modified: Tue, 31 Mar 2020 16:21:55 GMT  
		Size: 292.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fbe178b66676dfbb5fa68acba153942af73d08667f0ba39e353448bdc81e5fe`  
		Last Modified: Tue, 31 Mar 2020 16:21:53 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ec28449d082cd6b8693c4312bf24052fb236522227c9d431a6ffd045faaefe`  
		Last Modified: Tue, 31 Mar 2020 16:21:53 GMT  
		Size: 290.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72acc425e425e21d685dffc4ce1deb27e492b99723de0343e09bb713bfe98e97`  
		Last Modified: Tue, 31 Mar 2020 16:21:53 GMT  
		Size: 2.7 KB (2749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2532346c63bc6882ef04c1b8091f22c128b3e372e637c4de8ff08e3fa16fd2`  
		Last Modified: Tue, 31 Mar 2020 16:21:53 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2532346c63bc6882ef04c1b8091f22c128b3e372e637c4de8ff08e3fa16fd2`  
		Last Modified: Tue, 31 Mar 2020 16:21:53 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded666662d1e8996053ad12bef179e8eb2ab7306b7df38e587bf500b98f3f4a8`  
		Last Modified: Tue, 31 Mar 2020 16:21:53 GMT  
		Size: 1.0 MB (1004435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
