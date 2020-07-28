<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:6.8.11`](#logstash6811)
-	[`logstash:7.8.1`](#logstash781)

## `logstash:6.8.11`

```console
$ docker pull logstash@sha256:66098286f12b9b72a4e1d0bd4cba4aa8ecbef8d2123737e36091622383fc3ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `logstash:6.8.11` - linux; amd64

```console
$ docker pull logstash@sha256:bf1daa2505bd18cc36567af156b0ab45b5b25c71fb0d3264134146ee5680ae17
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.8 MB (358825368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c1a7d7b2b15c32873dc6bad70f84e76d10483a326ee4569ef759be442d55b99`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 05 May 2020 21:20:06 GMT
ADD file:38e2d2a1a0cd8694bd5086f257fdf7504f0c2481bf4f746c9bd1c8d9f3f6430d in / 
# Tue, 05 May 2020 21:20:06 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200504 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-05-04 00:00:00+01:00
# Tue, 05 May 2020 21:20:07 GMT
CMD ["/bin/bash"]
# Thu, 09 Jul 2020 20:43:38 GMT
RUN yum update -y && yum install -y java-1.8.0-openjdk-devel which &&     yum clean all
# Thu, 09 Jul 2020 20:43:39 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home-dir /usr/share/logstash --no-create-home       logstash
# Thu, 09 Jul 2020 20:44:02 GMT
RUN curl -Lo - http://localhost:8000/logstash-6.8.11.tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-6.8.11 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Thu, 09 Jul 2020 20:44:02 GMT
WORKDIR /usr/share/logstash
# Thu, 09 Jul 2020 20:44:02 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 09 Jul 2020 20:44:03 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Jul 2020 20:44:03 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Thu, 09 Jul 2020 20:44:05 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Thu, 09 Jul 2020 20:44:05 GMT
ADD file:2ef21d4766eab3ac48ed3847c8b8d05554f1fd0b39061cba66c9ac93240087fa in config/ 
# Thu, 09 Jul 2020 20:44:08 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Thu, 09 Jul 2020 20:44:10 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Thu, 09 Jul 2020 20:44:11 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 09 Jul 2020 20:44:11 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Thu, 09 Jul 2020 20:44:14 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Thu, 09 Jul 2020 20:44:14 GMT
USER 1000
# Thu, 09 Jul 2020 20:44:14 GMT
ADD file:571dd4a165fa42134dca8ddb671372023424aeaef9b0ed94f044c92e999f584e in /usr/local/bin/ 
# Thu, 09 Jul 2020 20:44:14 GMT
EXPOSE 5044 9600
# Thu, 09 Jul 2020 20:44:14 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.label-schema.name=logstash org.label-schema.version=6.8.11 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash license=Elastic License
# Thu, 09 Jul 2020 20:44:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:524b0c1e57f8ee5fee01a1decba2f301c324a6513ca3551021264e3aa7341ebc`  
		Last Modified: Tue, 05 May 2020 21:23:14 GMT  
		Size: 75.9 MB (75880141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5d35a3a33e607f1c85d349a8ef90a3473774c0df1323da5735ccd3648ad06c`  
		Last Modified: Mon, 27 Jul 2020 17:05:47 GMT  
		Size: 104.3 MB (104342852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43787c71b44c58b8aafa0acdc978a2d021dcfad7728c213da4dd52d47ea48e84`  
		Last Modified: Mon, 27 Jul 2020 17:05:30 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f14a8b2391d3399b9f748647ddcf1b16e8b1bd5df5ead3f6a88c0d5908c9acb`  
		Last Modified: Mon, 27 Jul 2020 17:09:20 GMT  
		Size: 177.6 MB (177590917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c176d1e99655532ceb507803bee4955e93b9c133ea0479532854176a36d2476a`  
		Last Modified: Mon, 27 Jul 2020 17:09:04 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f3f7dca40ee7a75c9164d7af74b7ad477338f3cf5d91136ff1a33abf374d76`  
		Last Modified: Mon, 27 Jul 2020 17:09:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd124032dd4c7995f2460c7c2a54b3d1a6f06578c3d489c542e4e1c650312f5b`  
		Last Modified: Mon, 27 Jul 2020 17:09:05 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:131952dd1e2c7a2bfa474e663dcc28a3a82c5441adf72415755188efdaad6676`  
		Last Modified: Mon, 27 Jul 2020 17:09:02 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e8b7b514f5a3a98f13778f5dc82a01c9e1e3fd8459ab4f920b9d5ed7410a31e`  
		Last Modified: Mon, 27 Jul 2020 17:09:02 GMT  
		Size: 2.7 KB (2681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3104c1c98d50ee37a1a2ebfab2d4e5db3f48a32c441a3bb99f46c65e20334b17`  
		Last Modified: Mon, 27 Jul 2020 17:09:02 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3104c1c98d50ee37a1a2ebfab2d4e5db3f48a32c441a3bb99f46c65e20334b17`  
		Last Modified: Mon, 27 Jul 2020 17:09:02 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faec7042c31d2e99f627e1b9832aa6ff4325fa2ec7796dfc49d0d99bb409c952`  
		Last Modified: Mon, 27 Jul 2020 17:09:02 GMT  
		Size: 1.0 MB (1004570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `logstash:7.8.1`

```console
$ docker pull logstash@sha256:f7ff8907ac010e35df8447ea8ea32ea57d07fb261316d92644f168c63cf99287
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `logstash:7.8.1` - linux; amd64

```console
$ docker pull logstash@sha256:77fd49599f5af8a0594bdac4c41d12a912ca112700c72c4953187b77048169ae
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.9 MB (336921618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc67e625d9743ceabbf6e2259b9fa7ac5d0b57e1ebc6b2169f6c0e5b694520b0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 05 May 2020 21:20:06 GMT
ADD file:38e2d2a1a0cd8694bd5086f257fdf7504f0c2481bf4f746c9bd1c8d9f3f6430d in / 
# Tue, 05 May 2020 21:20:06 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200504 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-05-04 00:00:00+01:00
# Tue, 05 May 2020 21:20:07 GMT
CMD ["/bin/bash"]
# Tue, 21 Jul 2020 19:30:30 GMT
RUN yum update -y && yum install -y java-11-openjdk-devel which &&     yum clean all
# Tue, 21 Jul 2020 19:30:32 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home-dir /usr/share/logstash --no-create-home       logstash
# Tue, 21 Jul 2020 19:30:46 GMT
RUN curl -Lo - http://localhost:8000/logstash-7.8.1.tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.8.1 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Tue, 21 Jul 2020 19:30:47 GMT
WORKDIR /usr/share/logstash
# Tue, 21 Jul 2020 19:30:47 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 21 Jul 2020 19:30:48 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jul 2020 19:30:49 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Tue, 21 Jul 2020 19:30:50 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Tue, 21 Jul 2020 19:30:52 GMT
ADD file:4f39d77a8986c28d67e673d4691e69ca9c175574128b0819977c2d1bb0d6e950 in config/ 
# Tue, 21 Jul 2020 19:30:52 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Tue, 21 Jul 2020 19:30:53 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Tue, 21 Jul 2020 19:30:54 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 21 Jul 2020 19:30:55 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Tue, 21 Jul 2020 19:30:56 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Tue, 21 Jul 2020 19:30:56 GMT
USER 1000
# Tue, 21 Jul 2020 19:30:58 GMT
ADD file:810198d06e82306d8355b16413986c5fe815f9695228538ed48fec4ac96eb43f in /usr/local/bin/ 
# Tue, 21 Jul 2020 19:30:58 GMT
EXPOSE 5044 9600
# Tue, 21 Jul 2020 19:30:59 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.label-schema.name=logstash org.label-schema.version=7.8.1 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash license=Elastic License
# Tue, 21 Jul 2020 19:30:59 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:524b0c1e57f8ee5fee01a1decba2f301c324a6513ca3551021264e3aa7341ebc`  
		Last Modified: Tue, 05 May 2020 21:23:14 GMT  
		Size: 75.9 MB (75880141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea79d464a65586f0c809818c894f15fe0fc002615d91a4440b88015ac2ec46a`  
		Last Modified: Mon, 27 Jul 2020 20:07:09 GMT  
		Size: 99.7 MB (99740731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245cfcbe00e53fd469abb749674cbf672e6482698114376937afd55942488ad7`  
		Last Modified: Mon, 27 Jul 2020 19:54:17 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4d0381588665466b3fa22cabefad92ee5bcc98445ab58d3228e22c807dee75`  
		Last Modified: Mon, 27 Jul 2020 20:11:37 GMT  
		Size: 160.3 MB (160288992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505552b55db28bec6ef98e1fe2706b076973d105c29fabf10647376d3b32ec8f`  
		Last Modified: Mon, 27 Jul 2020 19:54:15 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d440869a711be746a427e90efc0a192f0cb843e419ca5d3401545242db4169ff`  
		Last Modified: Mon, 27 Jul 2020 19:54:15 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086ef50d80ce51233f89583609793a3486931d863324552972e8231b8b296119`  
		Last Modified: Mon, 27 Jul 2020 19:54:14 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b8a22f5fe66944753e1d87e7775819afe2d0e1835a0625371ac6ab4c713c0d`  
		Last Modified: Mon, 27 Jul 2020 19:54:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aece5f411b8b8a24236660946cb14329bbed9016ce3f0ea3f7444b9ed37d420b`  
		Last Modified: Mon, 27 Jul 2020 19:54:16 GMT  
		Size: 2.8 KB (2753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f6ec9f2b6e3f16a8d3af2c07944ebc684539481bbb8202b0c937f1e11e0cac`  
		Last Modified: Mon, 27 Jul 2020 19:54:13 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f6ec9f2b6e3f16a8d3af2c07944ebc684539481bbb8202b0c937f1e11e0cac`  
		Last Modified: Mon, 27 Jul 2020 19:54:13 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03353e162ddf60b9aec43b06213cd256fefb62d4bb5c00674d62709e35570c7e`  
		Last Modified: Mon, 27 Jul 2020 19:54:12 GMT  
		Size: 1.0 MB (1004771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
