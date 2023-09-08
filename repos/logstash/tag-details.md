<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.13`](#logstash71713)
-	[`logstash:8.9.2`](#logstash892)

## `logstash:7.17.13`

```console
$ docker pull logstash@sha256:205e6bb80eda3e0912a1475eeae8c41fae17dab73337dcd4a2501ff2cb977005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `logstash:7.17.13` - linux; amd64

```console
$ docker pull logstash@sha256:596d903402966164334d38373e48ba5f85c91dce03523c4d9f95569af0ce19ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.8 MB (441833995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b3073bfb3bf20c65e02792c748368d9ec1d518cca99b23d7fc1de517fddda74`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:43 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:45 GMT
ADD file:233702cd816c07bc9fed02881b11fb3bdcaee41f3ce3ec1c9f0c4a060b155d5b in / 
# Tue, 01 Aug 2023 06:16:46 GMT
CMD ["/bin/bash"]
# Tue, 29 Aug 2023 12:47:46 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 29 Aug 2023 12:47:46 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Tue, 29 Aug 2023 12:48:03 GMT
RUN curl -Lo - http://localhost:8000/logstash-7.17.13-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.13 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 29 Aug 2023 12:48:03 GMT
WORKDIR /usr/share/logstash
# Tue, 29 Aug 2023 12:48:04 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 29 Aug 2023 12:48:04 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Aug 2023 12:48:04 GMT
ADD config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 29 Aug 2023 12:48:04 GMT
ADD config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 29 Aug 2023 12:48:04 GMT
ADD config/log4j2.properties config/ # buildkit
# Tue, 29 Aug 2023 12:48:04 GMT
ADD pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 29 Aug 2023 12:48:04 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 29 Aug 2023 12:48:04 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 29 Aug 2023 12:48:04 GMT
ADD env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 29 Aug 2023 12:48:04 GMT
ADD bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 29 Aug 2023 12:48:04 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 29 Aug 2023 12:48:04 GMT
USER 1000
# Tue, 29 Aug 2023 12:48:04 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 29 Aug 2023 12:48:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.13 org.opencontainers.image.version=7.17.13 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2023-08-29T12:32:19+00:00 org.opencontainers.image.created=2023-08-29T12:32:19+00:00
# Tue, 29 Aug 2023 12:48:04 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:7007490126efaae58924972668256aaeb4858e6c4537eb4257e1978719b958c7`  
		Last Modified: Tue, 01 Aug 2023 08:35:40 GMT  
		Size: 28.6 MB (28580671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83fe34beff15fcddc19b3d739827897fd04abef4f951770b1640e696d1999291`  
		Last Modified: Fri, 08 Sep 2023 05:26:59 GMT  
		Size: 44.6 MB (44555715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103dfd3d5810a1a1db0cc61af270e109fec70ab1b181fb6f169dcf3ef5be4ac0`  
		Last Modified: Fri, 08 Sep 2023 05:26:54 GMT  
		Size: 1.8 KB (1830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2fabf29352f45b1742ab868f6dc02275b86ec162604933a727c532ea03eed77`  
		Last Modified: Fri, 08 Sep 2023 05:27:20 GMT  
		Size: 366.8 MB (366844936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33474fbbc276e9940864c002c09ff2224b0a39915e6dcf9f035da422ca6a29a`  
		Last Modified: Fri, 08 Sep 2023 05:26:54 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bef82fffd525f24fc964a08df0aeb2e185021675e7cfc9400465e8dca51b680`  
		Last Modified: Fri, 08 Sep 2023 05:26:53 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c608f9d9880413bbc2757cab40c2e7376637fd78946dfa2a49b1453654834e93`  
		Last Modified: Fri, 08 Sep 2023 05:26:51 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86698dc5df38888031dcb159d78a75392eb5a2823024aa50e1c0f17e4bd38965`  
		Last Modified: Fri, 08 Sep 2023 05:26:51 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb509c99c0c97e6a8fecaae5878f01076c872024de433e7dc4e02fbe91824f6`  
		Last Modified: Fri, 08 Sep 2023 05:26:51 GMT  
		Size: 2.9 KB (2853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f376629b40d26d3407539bbfb92f950917666b8c59025fecfc3b663a25574bc3`  
		Last Modified: Fri, 08 Sep 2023 05:26:52 GMT  
		Size: 1.8 MB (1845554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33276697c3a28d89f01299c7d291853f9a97833630fe6174c5a4a0d670862b5e`  
		Last Modified: Fri, 08 Sep 2023 05:26:52 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33276697c3a28d89f01299c7d291853f9a97833630fe6174c5a4a0d670862b5e`  
		Last Modified: Fri, 08 Sep 2023 05:26:52 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull logstash@sha256:3bd927946cd7f302c529625327306fe64c6a8904bf4f23f6a596259969499b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `logstash:8.9.2` - linux; amd64

```console
$ docker pull logstash@sha256:cd76e90caa44cff36bb1a704e4d9433940ef9df28eaaa4e717cc8cc3bc31d188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.2 MB (424223666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13e133ae1d4db2e42fa887ea1eb07aebfcb39c82fcb29830c4f5229b85bafaad`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:43 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:45 GMT
ADD file:233702cd816c07bc9fed02881b11fb3bdcaee41f3ce3ec1c9f0c4a060b155d5b in / 
# Tue, 01 Aug 2023 06:16:46 GMT
CMD ["/bin/bash"]
# Wed, 30 Aug 2023 13:40:55 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Wed, 30 Aug 2023 13:40:55 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Wed, 30 Aug 2023 13:41:11 GMT
RUN curl -Lo - http://localhost:8000/logstash-8.9.2-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.9.2 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt && find /usr/share/logstash -type d -exec chmod g+s {} \; && ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 30 Aug 2023 13:41:11 GMT
WORKDIR /usr/share/logstash
# Wed, 30 Aug 2023 13:41:11 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 30 Aug 2023 13:41:11 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Aug 2023 13:41:11 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Wed, 30 Aug 2023 13:41:11 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Wed, 30 Aug 2023 13:41:11 GMT
COPY config/log4j2.properties config/ # buildkit
# Wed, 30 Aug 2023 13:41:11 GMT
COPY config/log4j2.file.properties config/ # buildkit
# Wed, 30 Aug 2023 13:41:11 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Wed, 30 Aug 2023 13:41:11 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Wed, 30 Aug 2023 13:41:11 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 30 Aug 2023 13:41:11 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Wed, 30 Aug 2023 13:41:11 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 30 Aug 2023 13:41:11 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Wed, 30 Aug 2023 13:41:11 GMT
USER 1000
# Wed, 30 Aug 2023 13:41:11 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 30 Aug 2023 13:41:11 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.9.2 org.opencontainers.image.version=8.9.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2023-08-30T13:23:56+00:00 org.opencontainers.image.created=2023-08-30T13:23:56+00:00
# Wed, 30 Aug 2023 13:41:11 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:7007490126efaae58924972668256aaeb4858e6c4537eb4257e1978719b958c7`  
		Last Modified: Tue, 01 Aug 2023 08:35:40 GMT  
		Size: 28.6 MB (28580671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330be7caba6b0b5a029a9cfeaa3633eacf6989ff1f2d8195f8cab9c336dd6a21`  
		Last Modified: Fri, 08 Sep 2023 05:26:26 GMT  
		Size: 44.6 MB (44576132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d2cf1e23bd148bb0cd1d31b555a89165ade177056d4ba483cfe5c64c366bb52`  
		Last Modified: Fri, 08 Sep 2023 05:26:20 GMT  
		Size: 1.8 KB (1829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74fe8dfccbf12142cd068ef9b22f6ce30e8c705cc58e1d2c7c1076d67087af2`  
		Last Modified: Fri, 08 Sep 2023 05:26:45 GMT  
		Size: 349.2 MB (349211398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc554d068a400d5b6955d12de9618c6ea423a66916fd901f16702da9cf2558ed`  
		Last Modified: Fri, 08 Sep 2023 05:26:19 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b4faa71c131adb6ceae7eca5c9112a13ee2475ca351441da7e2a3a6c03ef22f`  
		Last Modified: Fri, 08 Sep 2023 05:26:19 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3712d23b90f7beb23038383616037094459e5d1572e9ded9bc168301a84908bd`  
		Last Modified: Fri, 08 Sep 2023 05:26:19 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ffd6cfcb57a8e83ecf80c28059949a3ca7841d8f06237e7183ec230811fc25`  
		Last Modified: Fri, 08 Sep 2023 05:26:17 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72fdcf246be80c187186090755053492913be8add04e6a4b911c4b12e2dac346`  
		Last Modified: Fri, 08 Sep 2023 05:26:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd91aa4e2a547869025a196f240ce61716788b1e284449e2a54d44919e094883`  
		Last Modified: Fri, 08 Sep 2023 05:26:17 GMT  
		Size: 3.7 KB (3662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39b8f8de96669d97cf63e4049e188d14e5e6f66e524e1affbdb9e9766cad3fb`  
		Last Modified: Fri, 08 Sep 2023 05:26:17 GMT  
		Size: 1.8 MB (1845753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250e0de95453fffa0bf953da66c70c29032543dc29a77584c63b29b98d529978`  
		Last Modified: Fri, 08 Sep 2023 05:26:17 GMT  
		Size: 713.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250e0de95453fffa0bf953da66c70c29032543dc29a77584c63b29b98d529978`  
		Last Modified: Fri, 08 Sep 2023 05:26:17 GMT  
		Size: 713.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
