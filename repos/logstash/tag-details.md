<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.10`](#logstash71710)
-	[`logstash:8.8.0`](#logstash880)

## `logstash:7.17.10`

```console
$ docker pull logstash@sha256:b390f7c524a5334348bc431b56993d306e4ef39056a633ddb739ed8fdb544114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `logstash:7.17.10` - linux; amd64

```console
$ docker pull logstash@sha256:80b5d261476927e9e09130b0ad4873c51417f22b5ecffe9b844faf9d433dc10c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.1 MB (440112781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fe6f316b8af000c27f86f25363ca89f21322f24b0e4f641f7fe5e04c0695d60`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Thu, 20 Apr 2023 15:56:56 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Thu, 20 Apr 2023 15:56:56 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Thu, 20 Apr 2023 15:57:13 GMT
RUN curl -Lo - http://localhost:8000/logstash-7.17.10-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.10 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 20 Apr 2023 15:57:13 GMT
WORKDIR /usr/share/logstash
# Thu, 20 Apr 2023 15:57:13 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 20 Apr 2023 15:57:13 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Apr 2023 15:57:13 GMT
ADD config/pipelines.yml config/pipelines.yml # buildkit
# Thu, 20 Apr 2023 15:57:13 GMT
ADD config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 20 Apr 2023 15:57:13 GMT
ADD config/log4j2.properties config/ # buildkit
# Thu, 20 Apr 2023 15:57:13 GMT
ADD pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 20 Apr 2023 15:57:13 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 20 Apr 2023 15:57:13 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 20 Apr 2023 15:57:13 GMT
ADD env2yaml/env2yaml /usr/local/bin/ # buildkit
# Thu, 20 Apr 2023 15:57:13 GMT
ADD bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Apr 2023 15:57:13 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 20 Apr 2023 15:57:13 GMT
USER 1000
# Thu, 20 Apr 2023 15:57:13 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 20 Apr 2023 15:57:13 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.10 org.opencontainers.image.version=7.17.10 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2023-04-20T15:42:08+00:00 org.opencontainers.image.created=2023-04-20T15:42:08+00:00
# Thu, 20 Apr 2023 15:57:13 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76aaa905f86d653743feb6301d1a26dff3a36c740ea710314f4ccd741d88226b`  
		Last Modified: Wed, 03 May 2023 04:26:55 GMT  
		Size: 42.5 MB (42467673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cef93bd367a0e8d050d8fe10ceeef5691333f2588f23c444428eaa6235ebfbf`  
		Last Modified: Wed, 03 May 2023 04:26:50 GMT  
		Size: 1.8 KB (1825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb63215e1981a79f73698097f3abafe4b1ef0558f389fe9dd8f79209cdc807bc`  
		Last Modified: Wed, 03 May 2023 04:27:15 GMT  
		Size: 367.3 MB (367250139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9331e3fc1964b7151733ee48c8031e71387ebb7e3cfc12567a62d977e20020a3`  
		Last Modified: Wed, 03 May 2023 04:26:49 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc1ee29d5b3ad7134e3dfc9f40c818f513208a681ea763226027cacc1b87ba1`  
		Last Modified: Wed, 03 May 2023 04:26:49 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c817d3a2ac5d2bdbb8611b2192576a1d4067c977056c4a1c0d5cbcdb3a693ed3`  
		Last Modified: Wed, 03 May 2023 04:26:47 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c443921cb7da864f6a30173ee2d22c7da85690722429347ba716ba501cefd2a`  
		Last Modified: Wed, 03 May 2023 04:26:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4a537afb20c3d4c2ab0d7e5fd3c57e80ae924747264d42e6060ec07d7a710cd`  
		Last Modified: Wed, 03 May 2023 04:26:47 GMT  
		Size: 2.9 KB (2850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7e764a3aecd07528e8da82967842ee173d755f64dfd2bbc4e6cfc5438d1801d`  
		Last Modified: Wed, 03 May 2023 04:26:48 GMT  
		Size: 1.8 MB (1809287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ecefeedb20aca94bc5fabb9da2a8bd4b96dfe650f9eed9957e4277e2c6c84e`  
		Last Modified: Wed, 03 May 2023 04:26:47 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ecefeedb20aca94bc5fabb9da2a8bd4b96dfe650f9eed9957e4277e2c6c84e`  
		Last Modified: Wed, 03 May 2023 04:26:47 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `logstash:7.17.10` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:c5fddc691f01644abb2458d947dda15670c0bc7eb3dcecd76929164e63035a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.1 MB (428108876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1aca257c77c5816e7ac4ecaf50ffae3cda57f348dac8f7a4c97c0dee97953a2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:50 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:59 GMT
ADD file:0150fa02321f8be160e90ff64583d263fe651b5d418ab65f05ba604449ab47c6 in / 
# Thu, 13 Apr 2023 13:10:00 GMT
CMD ["/bin/bash"]
# Thu, 20 Apr 2023 15:56:47 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Thu, 20 Apr 2023 15:56:47 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Thu, 20 Apr 2023 15:57:00 GMT
RUN curl -Lo - http://localhost:8000/logstash-7.17.10-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.10 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 20 Apr 2023 15:57:00 GMT
WORKDIR /usr/share/logstash
# Thu, 20 Apr 2023 15:57:00 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 20 Apr 2023 15:57:00 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Apr 2023 15:57:00 GMT
ADD config/pipelines.yml config/pipelines.yml # buildkit
# Thu, 20 Apr 2023 15:57:00 GMT
ADD config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 20 Apr 2023 15:57:00 GMT
ADD config/log4j2.properties config/ # buildkit
# Thu, 20 Apr 2023 15:57:00 GMT
ADD pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 20 Apr 2023 15:57:00 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 20 Apr 2023 15:57:00 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 20 Apr 2023 15:57:00 GMT
ADD env2yaml/env2yaml /usr/local/bin/ # buildkit
# Thu, 20 Apr 2023 15:57:00 GMT
ADD bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Apr 2023 15:57:00 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 20 Apr 2023 15:57:00 GMT
USER 1000
# Thu, 20 Apr 2023 15:57:00 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 20 Apr 2023 15:57:00 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.10 org.opencontainers.image.version=7.17.10 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2023-04-20T15:43:51+00:00 org.opencontainers.image.created=2023-04-20T15:43:51+00:00
# Thu, 20 Apr 2023 15:57:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:2378679266ac5157323158b6e52e7a884e559db5217037e57992e47a1667d525`  
		Last Modified: Fri, 14 Apr 2023 07:39:20 GMT  
		Size: 27.2 MB (27196396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df146c1c3fdeefbf2c8499aba2e532c39356e14630bc4d0800c704c8ae9c239`  
		Last Modified: Wed, 03 May 2023 03:45:51 GMT  
		Size: 35.2 MB (35192502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3e2d4e6e72b4be71db7399fd03ec4846eaf96070eb4ee12b7d585ec32484e6`  
		Last Modified: Wed, 03 May 2023 03:45:48 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bda4e20a465e10b98ca6f2051b81363fb407484af53012181f80e5ee515568b`  
		Last Modified: Wed, 03 May 2023 03:46:08 GMT  
		Size: 364.0 MB (364023654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95c90cfa68731e409f58cf9413cd14d352c799691c4e3350932b48a1728de8e`  
		Last Modified: Wed, 03 May 2023 03:45:47 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e27628d91aa2602189ff17407206d2deb1ff8000c9c96cbbde0d363a2c3ff7`  
		Last Modified: Wed, 03 May 2023 03:45:47 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75024a673d419b30010aa065f9cf7a394e6a6bc41c69e4c64d66499be68a741`  
		Last Modified: Wed, 03 May 2023 03:45:45 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6e12f434639053c3e159dcd1969589f973158963e08ca610e7aadfd7794d72`  
		Last Modified: Wed, 03 May 2023 03:45:45 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:124287526a1bf4df21260945ea7007f4f8a79dc5e9e00241230ea5a87d3c0262`  
		Last Modified: Wed, 03 May 2023 03:45:45 GMT  
		Size: 2.9 KB (2851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea4b9ceb2ccb6eee733f6df7d88df3e300facfc1e4a2c21944ac73e77244ea2`  
		Last Modified: Wed, 03 May 2023 03:45:46 GMT  
		Size: 1.7 MB (1689166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ceb4ffb8e47010f2205563ab97aeb34220207f6f3d523d2b0e8810d556d0d0`  
		Last Modified: Wed, 03 May 2023 03:45:45 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ceb4ffb8e47010f2205563ab97aeb34220207f6f3d523d2b0e8810d556d0d0`  
		Last Modified: Wed, 03 May 2023 03:45:45 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `logstash:8.8.0`

```console
$ docker pull logstash@sha256:05a7e83e7c9ccca557e3c2f5d18780a7903dfc3ec025aa74a3286b3be5608c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `logstash:8.8.0` - linux; amd64

```console
$ docker pull logstash@sha256:43bb81067a4737e33145bd3f757bd52a481c68dd8c6cc12341b6e1f5b059375c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.1 MB (410051128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dae3dd8a33763e557457af3fd4558a5265e7f68cef7eba0a54604b505b17d65`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Wed, 26 Apr 2023 16:21:37 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Wed, 26 Apr 2023 16:21:38 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Wed, 26 Apr 2023 16:21:53 GMT
RUN curl -Lo - http://localhost:8000/logstash-8.8.0-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.8.0 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt && find /usr/share/logstash -type d -exec chmod g+s {} \; && ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 26 Apr 2023 16:21:53 GMT
WORKDIR /usr/share/logstash
# Wed, 26 Apr 2023 16:21:53 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 26 Apr 2023 16:21:53 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Apr 2023 16:21:53 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Wed, 26 Apr 2023 16:21:53 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Wed, 26 Apr 2023 16:21:53 GMT
COPY config/log4j2.properties config/ # buildkit
# Wed, 26 Apr 2023 16:21:53 GMT
COPY config/log4j2.file.properties config/ # buildkit
# Wed, 26 Apr 2023 16:21:53 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Wed, 26 Apr 2023 16:21:53 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Wed, 26 Apr 2023 16:21:53 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 26 Apr 2023 16:21:53 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Wed, 26 Apr 2023 16:21:53 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 26 Apr 2023 16:21:53 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Wed, 26 Apr 2023 16:21:53 GMT
USER 1000
# Wed, 26 Apr 2023 16:21:53 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 26 Apr 2023 16:21:53 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.8.0 org.opencontainers.image.version=8.8.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2023-04-26T16:00:27+00:00 org.opencontainers.image.created=2023-04-26T16:00:27+00:00
# Wed, 26 Apr 2023 16:21:53 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794aac5945003bce239830a6cde476da66d9c1e190a2df3b45206b9986e690a7`  
		Last Modified: Thu, 25 May 2023 20:00:14 GMT  
		Size: 42.6 MB (42570122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d5ecdaf046da294406d993aa025295dc6103bc6e955b0f0c3c9fa4151399e7`  
		Last Modified: Thu, 25 May 2023 20:00:01 GMT  
		Size: 1.8 KB (1826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d7a89fc9d585bc42c9124ea5dfafef7d6bb76208aa02c97988ec6f94e81962`  
		Last Modified: Thu, 25 May 2023 20:01:28 GMT  
		Size: 337.1 MB (337083282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4108a888b9796262ba137229a044c2a0317b2238ba47d8ecc7e27e46eff58ade`  
		Last Modified: Thu, 25 May 2023 20:00:00 GMT  
		Size: 377.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e3c7aed267e87d8b1517c16b1754aa9a6f19d1b817763822c7581ec3804957`  
		Last Modified: Thu, 25 May 2023 20:00:00 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42964ddc371fc18120fb91ba832397044ddaba9243cb22ab3f4f1913c6c2c7bf`  
		Last Modified: Thu, 25 May 2023 20:00:00 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75048390fe8c733d2d72262bd7b443e21dd6a5f02f43e871ea7d1558315176fc`  
		Last Modified: Thu, 25 May 2023 19:59:58 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a153a65944deed18f2b8e27581268b7a1abfe1df78b1450f3b8084ddba4e2cdd`  
		Last Modified: Thu, 25 May 2023 19:59:58 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366917ea16800060a09709c5c7073da0414cd4361fc5c31e98550a96cc475f46`  
		Last Modified: Thu, 25 May 2023 19:59:58 GMT  
		Size: 3.7 KB (3660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e364811e59b038c3bfc29511553299557843868ac79c9508ff8a7a06a812c9c4`  
		Last Modified: Thu, 25 May 2023 19:59:58 GMT  
		Size: 1.8 MB (1809445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349ec387f91f41db44e889294e3805a2a6ebfa816311eb7147bbf630a70e14cb`  
		Last Modified: Thu, 25 May 2023 19:59:58 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349ec387f91f41db44e889294e3805a2a6ebfa816311eb7147bbf630a70e14cb`  
		Last Modified: Thu, 25 May 2023 19:59:58 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `logstash:8.8.0` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:2aa0d22f149edf53625c8ad03e0d60d4f581e410df283a957492dd75f9325c0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.0 MB (400020541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd60026e4606cca67fc9737a8cd8a9727abf0b1e3097d8f78f3b79b40b507002`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:50 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:59 GMT
ADD file:0150fa02321f8be160e90ff64583d263fe651b5d418ab65f05ba604449ab47c6 in / 
# Thu, 13 Apr 2023 13:10:00 GMT
CMD ["/bin/bash"]
# Wed, 26 Apr 2023 16:16:39 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Wed, 26 Apr 2023 16:16:39 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Wed, 26 Apr 2023 16:16:48 GMT
RUN curl -Lo - http://localhost:8000/logstash-8.8.0-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.8.0 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt && find /usr/share/logstash -type d -exec chmod g+s {} \; && ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 26 Apr 2023 16:16:48 GMT
WORKDIR /usr/share/logstash
# Wed, 26 Apr 2023 16:16:48 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 26 Apr 2023 16:16:48 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Apr 2023 16:16:48 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Wed, 26 Apr 2023 16:16:48 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Wed, 26 Apr 2023 16:16:48 GMT
COPY config/log4j2.properties config/ # buildkit
# Wed, 26 Apr 2023 16:16:48 GMT
COPY config/log4j2.file.properties config/ # buildkit
# Wed, 26 Apr 2023 16:16:48 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Wed, 26 Apr 2023 16:16:48 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Wed, 26 Apr 2023 16:16:48 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 26 Apr 2023 16:16:48 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Wed, 26 Apr 2023 16:16:48 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 26 Apr 2023 16:16:48 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Wed, 26 Apr 2023 16:16:48 GMT
USER 1000
# Wed, 26 Apr 2023 16:16:48 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 26 Apr 2023 16:16:48 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.8.0 org.opencontainers.image.version=8.8.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2023-04-26T16:02:23+00:00 org.opencontainers.image.created=2023-04-26T16:02:23+00:00
# Wed, 26 Apr 2023 16:16:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:2378679266ac5157323158b6e52e7a884e559db5217037e57992e47a1667d525`  
		Last Modified: Fri, 14 Apr 2023 07:39:20 GMT  
		Size: 27.2 MB (27196396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cecd9d4b883ad703df51a98547baae533536a8b34adfbe62f8446a736380d45`  
		Last Modified: Tue, 06 Jun 2023 22:42:21 GMT  
		Size: 35.2 MB (35231408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f82db401b81a2b61a5628c0fd6002f673fca8efc7cdba00be80b87f04e8fd`  
		Last Modified: Tue, 06 Jun 2023 22:42:17 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915d6c6d32a7981b86f48204e0372d73e4e5bc5f9e0ba8074de42b9f05695827`  
		Last Modified: Tue, 06 Jun 2023 22:42:37 GMT  
		Size: 335.9 MB (335893482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dda8dfa9e6259e1184884cdda83940cdb8309c7dfc9ae5458f19e7dd0a0a989`  
		Last Modified: Tue, 06 Jun 2023 22:42:16 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd91e1506abd64276c5151bba2f577aa76f80c5ba709bb7c62ee7e3a7c67977`  
		Last Modified: Tue, 06 Jun 2023 22:42:16 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc893fa9cdede0ded7cd8c901803e72127e3e5ec866c51d66c2c47f55e84246c`  
		Last Modified: Tue, 06 Jun 2023 22:42:16 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f8a54e9a8db1e88b5c2ebaea44918515b3b0dcd962c288400c96dfab58afcc`  
		Last Modified: Tue, 06 Jun 2023 22:42:14 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda942b7d6c7cc11a05663296c598b4bcc5ccf7af45e3bed7fe7100910fcbb64`  
		Last Modified: Tue, 06 Jun 2023 22:42:14 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edfc8877fd02108702ac4294592091486c4aeef20b91700f1405dd8b75ad87ac`  
		Last Modified: Tue, 06 Jun 2023 22:42:14 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b984da5ae2c04101aa8be039be27d3951f277a69ec57286c0c816e519fea3e66`  
		Last Modified: Tue, 06 Jun 2023 22:42:14 GMT  
		Size: 1.7 MB (1689517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217456c8132f100d0b05625719c3a2453d78e2f8ed6d297881ea4111d7cda15a`  
		Last Modified: Tue, 06 Jun 2023 22:42:14 GMT  
		Size: 715.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217456c8132f100d0b05625719c3a2453d78e2f8ed6d297881ea4111d7cda15a`  
		Last Modified: Tue, 06 Jun 2023 22:42:14 GMT  
		Size: 715.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
