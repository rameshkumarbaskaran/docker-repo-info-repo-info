<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.13`](#logstash71713)
-	[`logstash:8.9.2`](#logstash892)

## `logstash:7.17.13`

```console
$ docker pull logstash@sha256:496ff1f2432cd3ab94ae0477e075fa40cd340d8e41190fa1a2adcf60b874d96a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `logstash:7.17.13` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:1e261ec63ea1fc57eecd742dbf537ad158ac8aa354127d98f65f45acedfbea73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.6 MB (428591171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba2b287b529218992f257de967e4f2ab6b39bfc63b61369bcaded88854b6ca61`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:56 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:21:03 GMT
ADD file:ef6e767091d76c1461d099d5bc7a18c526ec80834cf87280803ab6480192f766 in / 
# Tue, 01 Aug 2023 06:21:03 GMT
CMD ["/bin/bash"]
# Tue, 29 Aug 2023 12:45:15 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 29 Aug 2023 12:45:15 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Tue, 29 Aug 2023 12:45:26 GMT
RUN curl -Lo - http://localhost:8000/logstash-7.17.13-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.13 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 29 Aug 2023 12:45:26 GMT
WORKDIR /usr/share/logstash
# Tue, 29 Aug 2023 12:45:26 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 29 Aug 2023 12:45:26 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Aug 2023 12:45:26 GMT
ADD config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 29 Aug 2023 12:45:26 GMT
ADD config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 29 Aug 2023 12:45:26 GMT
ADD config/log4j2.properties config/ # buildkit
# Tue, 29 Aug 2023 12:45:26 GMT
ADD pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 29 Aug 2023 12:45:26 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 29 Aug 2023 12:45:26 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 29 Aug 2023 12:45:26 GMT
ADD env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 29 Aug 2023 12:45:26 GMT
ADD bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 29 Aug 2023 12:45:27 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 29 Aug 2023 12:45:27 GMT
USER 1000
# Tue, 29 Aug 2023 12:45:27 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 29 Aug 2023 12:45:27 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.13 org.opencontainers.image.version=7.17.13 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2023-08-29T12:32:29+00:00 org.opencontainers.image.created=2023-08-29T12:32:29+00:00
# Tue, 29 Aug 2023 12:45:27 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:edab87ea811e56041127f5e9eb4115fb62cb96d0e6a14056e0d2dbf51a945a22`  
		Last Modified: Wed, 02 Aug 2023 04:28:23 GMT  
		Size: 27.2 MB (27200587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5ea6c0a6e78fd90fa1c399208e0f14c1921366555f78829413d37a36715b0e`  
		Last Modified: Thu, 07 Sep 2023 23:43:38 GMT  
		Size: 36.1 MB (36069997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb4bcf9489e2909161fa9daf039479bdbcad05922bb7ab0f11a9d9876bfb641`  
		Last Modified: Thu, 07 Sep 2023 23:43:35 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56aadfb7bd16702a7aaf82f3ae1da7fb5259fd33ff0a7132b4c5db676be3d628`  
		Last Modified: Thu, 07 Sep 2023 23:43:55 GMT  
		Size: 363.6 MB (363581868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbf37db6582af9148061e2ce65bba0e0570141b5e9c6097402e72b2abefb3eb`  
		Last Modified: Thu, 07 Sep 2023 23:43:35 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753a71f4582f6a21100aa94ba6cc4fa8d8ef221a0743dcf7f7dc6bcd4424ae58`  
		Last Modified: Thu, 07 Sep 2023 23:43:35 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544f798f8ae4be9a4eb881952c7978cb109c48d695a8b85cbda153ef4b9cc5fd`  
		Last Modified: Thu, 07 Sep 2023 23:43:32 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55608cfd1a69a72cc44c8a84d40e76e1718803d8a1aa5726e3a6d16a918e78fa`  
		Last Modified: Thu, 07 Sep 2023 23:43:33 GMT  
		Size: 301.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cbcfe6d2d95a111def3e77a6f0c9f9497513c76973e11bcb0c5bba3f1aeed2`  
		Last Modified: Thu, 07 Sep 2023 23:43:32 GMT  
		Size: 2.9 KB (2850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa6cbec40cff015c83ea9f462dbb1a41ac918a6b32acd9792e4ea83394f54bd`  
		Last Modified: Thu, 07 Sep 2023 23:43:33 GMT  
		Size: 1.7 MB (1731585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044af80824dae93e4d4b92b40e843a968924c023b1ccb29a435e67849d0c0ee6`  
		Last Modified: Thu, 07 Sep 2023 23:43:33 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044af80824dae93e4d4b92b40e843a968924c023b1ccb29a435e67849d0c0ee6`  
		Last Modified: Thu, 07 Sep 2023 23:43:33 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `logstash:8.9.2`

```console
$ docker pull logstash@sha256:978b0c062a5d552f85ee1f0185749deaf6d4ad56ec496c94fe621b48c4e822c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `logstash:8.9.2` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:7befc1edaf5bc47909b4fc68bafda52866ddf6834b8b1672fc038b2b3f2d1572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.0 MB (413023716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:572cc3da6377aaae3510942b644e908acfff952f3cdfbddc9e93680cfb8cb980`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:56 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:21:03 GMT
ADD file:ef6e767091d76c1461d099d5bc7a18c526ec80834cf87280803ab6480192f766 in / 
# Tue, 01 Aug 2023 06:21:03 GMT
CMD ["/bin/bash"]
# Wed, 30 Aug 2023 13:44:55 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Wed, 30 Aug 2023 13:44:55 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Wed, 30 Aug 2023 13:45:06 GMT
RUN curl -Lo - http://localhost:8000/logstash-8.9.2-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.9.2 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt && find /usr/share/logstash -type d -exec chmod g+s {} \; && ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 30 Aug 2023 13:45:06 GMT
WORKDIR /usr/share/logstash
# Wed, 30 Aug 2023 13:45:06 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 30 Aug 2023 13:45:06 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Aug 2023 13:45:06 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Wed, 30 Aug 2023 13:45:06 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Wed, 30 Aug 2023 13:45:06 GMT
COPY config/log4j2.properties config/ # buildkit
# Wed, 30 Aug 2023 13:45:06 GMT
COPY config/log4j2.file.properties config/ # buildkit
# Wed, 30 Aug 2023 13:45:06 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Wed, 30 Aug 2023 13:45:06 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Wed, 30 Aug 2023 13:45:06 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 30 Aug 2023 13:45:07 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Wed, 30 Aug 2023 13:45:07 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 30 Aug 2023 13:45:07 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Wed, 30 Aug 2023 13:45:07 GMT
USER 1000
# Wed, 30 Aug 2023 13:45:07 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 30 Aug 2023 13:45:07 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.9.2 org.opencontainers.image.version=8.9.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2023-08-30T13:29:42+00:00 org.opencontainers.image.created=2023-08-30T13:29:42+00:00
# Wed, 30 Aug 2023 13:45:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:edab87ea811e56041127f5e9eb4115fb62cb96d0e6a14056e0d2dbf51a945a22`  
		Last Modified: Wed, 02 Aug 2023 04:28:23 GMT  
		Size: 27.2 MB (27200587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226ce5181c3617bc0e34c36143d45fdc7a1665fef5e4540077f2082d2a34554e`  
		Last Modified: Thu, 07 Sep 2023 23:43:08 GMT  
		Size: 36.1 MB (36076374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f2b8b3910bba93263efff5f0545100b939b220905105b612afb632b3ade800`  
		Last Modified: Thu, 07 Sep 2023 23:43:03 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b0693ac66a165d2ef14f13df9ffbdc420b1e37cdfc0781edf92b3fdc398396`  
		Last Modified: Thu, 07 Sep 2023 23:43:26 GMT  
		Size: 348.0 MB (348005261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8db424188430766f5e2e6f3e0c5c914c0f555c0541f151eb8a4ac067bfe1427`  
		Last Modified: Thu, 07 Sep 2023 23:43:02 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aeefd7b529460e02ebaada08320b46b2c167a439d37229fe6d7c2b578518a85`  
		Last Modified: Thu, 07 Sep 2023 23:43:02 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bcb94cc7070f520c4eb3b69734cbf80032844b40fedbef8238bb0696a82bcde`  
		Last Modified: Thu, 07 Sep 2023 23:43:02 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6fcef79aeec95db9af120c663144c6860962baceaad3b932ae329eb98a6d2e`  
		Last Modified: Thu, 07 Sep 2023 23:43:00 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcdcf69d708cfe5525a093be6889b5af37df2b492ebbe8e92123f95b13c47ee0`  
		Last Modified: Thu, 07 Sep 2023 23:43:00 GMT  
		Size: 300.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7e2b8d2092e883e4a97fef4100ca43aaef778e7bfd57790d8bce419f27f273`  
		Last Modified: Thu, 07 Sep 2023 23:43:00 GMT  
		Size: 3.7 KB (3658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24123b9c9c9e90068444696c96600774ab6399b8f2e40703f56f6cb28e04a77`  
		Last Modified: Thu, 07 Sep 2023 23:43:01 GMT  
		Size: 1.7 MB (1731755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65354c96861346a49503163d6c008489b3f8f2af3d19fb3cfaa05a5e0d218cf`  
		Last Modified: Thu, 07 Sep 2023 23:43:00 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65354c96861346a49503163d6c008489b3f8f2af3d19fb3cfaa05a5e0d218cf`  
		Last Modified: Thu, 07 Sep 2023 23:43:00 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
