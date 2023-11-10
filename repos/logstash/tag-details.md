<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.14`](#logstash71714)
-	[`logstash:8.11.0`](#logstash8110)

## `logstash:7.17.14`

```console
$ docker pull logstash@sha256:d2367a6a6c85437d32639d685f7e679b29193fc69db69f2aa90d18e4205c026f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:7.17.14` - linux; amd64

```console
$ docker pull logstash@sha256:0ba85183b62e05bdbabe4bf3725f600e7bb0ff68b54322d49b0b0b7a3e684395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.0 MB (484042137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52cc476a69e28cc52f1693e993d2d80e029dfb0ff4f6bbd1b7601083e66abbb9`
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
# Wed, 04 Oct 2023 20:57:59 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Wed, 04 Oct 2023 20:57:59 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Wed, 04 Oct 2023 20:58:16 GMT
RUN curl -Lo - http://localhost:8000/logstash-7.17.14-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.14 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 04 Oct 2023 20:58:16 GMT
WORKDIR /usr/share/logstash
# Wed, 04 Oct 2023 20:58:16 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 04 Oct 2023 20:58:16 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Oct 2023 20:58:16 GMT
ADD config/pipelines.yml config/pipelines.yml # buildkit
# Wed, 04 Oct 2023 20:58:16 GMT
ADD config/logstash-full.yml config/logstash.yml # buildkit
# Wed, 04 Oct 2023 20:58:16 GMT
ADD config/log4j2.properties config/ # buildkit
# Wed, 04 Oct 2023 20:58:17 GMT
ADD pipeline/default.conf pipeline/logstash.conf # buildkit
# Wed, 04 Oct 2023 20:58:17 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Wed, 04 Oct 2023 20:58:17 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 04 Oct 2023 20:58:17 GMT
ADD env2yaml/env2yaml /usr/local/bin/ # buildkit
# Wed, 04 Oct 2023 20:58:17 GMT
ADD bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 04 Oct 2023 20:58:17 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Wed, 04 Oct 2023 20:58:17 GMT
USER 1000
# Wed, 04 Oct 2023 20:58:17 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 04 Oct 2023 20:58:17 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.14 org.opencontainers.image.version=7.17.14 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2023-10-04T20:42:06+00:00 org.opencontainers.image.created=2023-10-04T20:42:06+00:00
# Wed, 04 Oct 2023 20:58:17 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:f9175e7b73a4b948b4c5db289cbeeb1d8511aee675255978036e76ffeda560be`  
		Last Modified: Mon, 07 Aug 2023 21:55:17 GMT  
		Size: 31.8 MB (31795971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ec421020aa3caacaf2f6c765aff7a09fe5f0f46925887dfbf9b0f8be02a701`  
		Last Modified: Tue, 10 Oct 2023 09:01:48 GMT  
		Size: 55.1 MB (55099341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9377db22fae0c73fa1ad49f54f119d0af9635377230d74debad16f601db5c3`  
		Last Modified: Tue, 10 Oct 2023 09:01:42 GMT  
		Size: 2.0 KB (2033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac893d2dc651c92524e1d9a7be17e90480effbdafbe59bef2043891add31afab`  
		Last Modified: Tue, 10 Oct 2023 09:02:00 GMT  
		Size: 395.2 MB (395191608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89732bc7504122601f40269fc9ddfb70982e633ea9caf641ae45736f2846b004`  
		Last Modified: Sat, 26 Jan 2019 16:40:00 GMT  
		Size: 39.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cbe589daa5cdf42911ab29b8acd8d29ff286ba87f74f0a6b77408efcfbb851`  
		Last Modified: Tue, 10 Oct 2023 09:01:42 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fe6748f2a57270e864de842cacaad9faa1a083ecb1583ba6b1de4c8fb345b9`  
		Last Modified: Tue, 10 Oct 2023 09:01:44 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c491fd6f3d4f48075331cff1fff8595fd5d03902d543d6122b7a4e91c167f04d`  
		Last Modified: Tue, 10 Oct 2023 09:01:44 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b7b37e11b17023df829e2a1469e4686f53694f5d4962cf45da6e3fa19972b6`  
		Last Modified: Tue, 10 Oct 2023 09:01:45 GMT  
		Size: 299.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d4edea7c9d40b0ef944bd23b87140c3f48090476af2e8c22f9cd48cc2ab760`  
		Last Modified: Tue, 10 Oct 2023 09:01:45 GMT  
		Size: 3.0 KB (3012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31fd30867e6504170171427b4e00e391bf87f47500ea7e8024352fb3141e219`  
		Last Modified: Tue, 10 Oct 2023 09:01:47 GMT  
		Size: 1.9 MB (1947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897800aac07a2f34941b94dcb21eb88ceaf802a7c691845f773a3022c95e7f79`  
		Last Modified: Tue, 10 Oct 2023 09:01:47 GMT  
		Size: 512.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897800aac07a2f34941b94dcb21eb88ceaf802a7c691845f773a3022c95e7f79`  
		Last Modified: Tue, 10 Oct 2023 09:01:47 GMT  
		Size: 512.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.14` - unknown; unknown

```console
$ docker pull logstash@sha256:5276ae9c8b10b8334ffcd09743631d6c897eddfcb7e118d42b02931ab29e6fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2683591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919141c893321e487d3d0102e08bbf435f3883856b5f11f13d0770e4af19f339`

```dockerfile
```

-	Layers:
	-	`sha256:5f4ce92e1e2961865201e6e2e4797459a07034f85efe6ef78c90dee85b134339`  
		Last Modified: Thu, 09 Nov 2023 22:20:03 GMT  
		Size: 2.7 MB (2675654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e41a1f91168c90209d04bc212898b99068eb59bbcffbcee33e905fa34361f289`  
		Last Modified: Thu, 09 Nov 2023 22:20:03 GMT  
		Size: 7.9 KB (7937 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:7.17.14` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:1cdc4fc57b300e828aa7bb18e6242008232ef0378bf4c9962fbf322d0ac96c54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **467.6 MB (467648976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:990771c6a2acef0968703c8d385f5137604b5df68897b27512cc4bee6101daac`
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
# Wed, 04 Oct 2023 20:39:28 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Wed, 04 Oct 2023 20:39:28 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Wed, 04 Oct 2023 20:39:40 GMT
RUN curl -Lo - http://localhost:8000/logstash-7.17.14-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.14 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 04 Oct 2023 20:39:40 GMT
WORKDIR /usr/share/logstash
# Wed, 04 Oct 2023 20:39:40 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 04 Oct 2023 20:39:40 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Oct 2023 20:39:40 GMT
ADD config/pipelines.yml config/pipelines.yml # buildkit
# Wed, 04 Oct 2023 20:39:40 GMT
ADD config/logstash-full.yml config/logstash.yml # buildkit
# Wed, 04 Oct 2023 20:39:40 GMT
ADD config/log4j2.properties config/ # buildkit
# Wed, 04 Oct 2023 20:39:40 GMT
ADD pipeline/default.conf pipeline/logstash.conf # buildkit
# Wed, 04 Oct 2023 20:39:40 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Wed, 04 Oct 2023 20:39:40 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 04 Oct 2023 20:39:41 GMT
ADD env2yaml/env2yaml /usr/local/bin/ # buildkit
# Wed, 04 Oct 2023 20:39:41 GMT
ADD bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 04 Oct 2023 20:39:41 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Wed, 04 Oct 2023 20:39:41 GMT
USER 1000
# Wed, 04 Oct 2023 20:39:41 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 04 Oct 2023 20:39:41 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.14 org.opencontainers.image.version=7.17.14 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2023-10-04T20:26:30+00:00 org.opencontainers.image.created=2023-10-04T20:26:30+00:00
# Wed, 04 Oct 2023 20:39:41 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:e61e4aa6ecf06d84f177710ed7a16ba36429af08286de7aa5a485fdcedaac1f7`  
		Last Modified: Thu, 17 Aug 2023 10:22:08 GMT  
		Size: 29.9 MB (29915840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7740039ed6f7a724d659eb8e8ec4b18e62f9fb18d53528e8f64d2bebbcca8cc8`  
		Last Modified: Tue, 10 Oct 2023 09:01:46 GMT  
		Size: 44.6 MB (44567335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb28d6a3567dcb4a7196bfba87e5f0d2262718974630a8f0db7b2bcccf94f44`  
		Last Modified: Tue, 10 Oct 2023 09:01:42 GMT  
		Size: 2.0 KB (2038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef71cfa7a8b5e78ee842cf9571fba6bc01f75a813af5a94f841a27d41ba02101`  
		Last Modified: Tue, 10 Oct 2023 09:02:01 GMT  
		Size: 391.3 MB (391323667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89732bc7504122601f40269fc9ddfb70982e633ea9caf641ae45736f2846b004`  
		Last Modified: Sat, 26 Jan 2019 16:40:00 GMT  
		Size: 39.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e49c8143abedb8332b1975afc12f1ec092112ae4a1721d6830b9bc40d7c50e`  
		Last Modified: Tue, 10 Oct 2023 09:01:43 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a4723641dcdb69e3903b2232c2a47827ad61b6bf7fa76130396d168c2b46fc`  
		Last Modified: Tue, 10 Oct 2023 09:01:44 GMT  
		Size: 295.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4211064df7a2885095219397bdd15bc04bb080783731263ea2372090064155f7`  
		Last Modified: Tue, 10 Oct 2023 09:01:44 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebadaeb0483416c43a2ffb0f52d0870182affdc07d3d6fdd2a468471b7bed5a1`  
		Last Modified: Tue, 10 Oct 2023 09:01:45 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9afea1d03ba7c849bffb3611e45c79fdc7bf8ad3c4fb231a52366f6d779685`  
		Last Modified: Tue, 10 Oct 2023 09:01:46 GMT  
		Size: 3.0 KB (3006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c347060ceac511d239e1859713dcf01afcdc88479d336a3a2afab27c34e7c0d`  
		Last Modified: Tue, 10 Oct 2023 09:01:47 GMT  
		Size: 1.8 MB (1834536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4639d6dbf38d40472328815e2849af724430abf4d7d1fde67c67ea8ba879dec3`  
		Last Modified: Tue, 10 Oct 2023 09:01:47 GMT  
		Size: 512.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4639d6dbf38d40472328815e2849af724430abf4d7d1fde67c67ea8ba879dec3`  
		Last Modified: Tue, 10 Oct 2023 09:01:47 GMT  
		Size: 512.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.14` - unknown; unknown

```console
$ docker pull logstash@sha256:71dc9051f87f1df0f71bd9804fff5df4c7cc702795b6907c663cc5d4db1cb87a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2683916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a92672b435073652eb9ecd28e5bb2d3f06b54d61c37291d1c1114831f3a577cc`

```dockerfile
```

-	Layers:
	-	`sha256:3274502a52af9c841bbf85ebc64e18b7333be84a46f3e6c153bc05de6ee7ffb6`  
		Last Modified: Thu, 09 Nov 2023 22:34:08 GMT  
		Size: 2.7 MB (2675974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:722f2e67f66e9b7b27b9f431a614db0124eb0bef39716dc7ce380308824693af`  
		Last Modified: Thu, 09 Nov 2023 22:34:06 GMT  
		Size: 7.9 KB (7942 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.11.0`

```console
$ docker pull logstash@sha256:72baab8f903a2371a4afbe150df59bc251ab8e42074617e6d3ed81dd91eb5dab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `logstash:8.11.0` - linux; amd64

```console
$ docker pull logstash@sha256:447397b1a0bd0df1123029ce734f958288007da15f630c83b278d27743c7b07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.2 MB (460218938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15eae9bea4118e3e76039e6bd62d973e1f7f56f530f991ec8bd3b8f69689966`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 03 Oct 2023 10:45:50 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:45:51 GMT
ADD file:4809da414c2d478b4d991cbdaa2df457f2b3d07d0ff6cf673f09a66f90833e81 in / 
# Tue, 03 Oct 2023 10:45:52 GMT
CMD ["/bin/bash"]
# Tue, 31 Oct 2023 13:12:09 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 31 Oct 2023 13:12:09 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Tue, 31 Oct 2023 13:12:19 GMT
RUN curl -Lo - http://localhost:8000/logstash-8.11.0-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.11.0 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt && find /usr/share/logstash -type d -exec chmod g+s {} \; && ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 31 Oct 2023 13:12:19 GMT
WORKDIR /usr/share/logstash
# Tue, 31 Oct 2023 13:12:19 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 31 Oct 2023 13:12:19 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 13:12:19 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 31 Oct 2023 13:12:19 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 31 Oct 2023 13:12:19 GMT
COPY config/log4j2.properties config/ # buildkit
# Tue, 31 Oct 2023 13:12:19 GMT
COPY config/log4j2.file.properties config/ # buildkit
# Tue, 31 Oct 2023 13:12:19 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 31 Oct 2023 13:12:19 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 31 Oct 2023 13:12:19 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 31 Oct 2023 13:12:19 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 31 Oct 2023 13:12:19 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 31 Oct 2023 13:12:20 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 31 Oct 2023 13:12:20 GMT
USER 1000
# Tue, 31 Oct 2023 13:12:20 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 31 Oct 2023 13:12:20 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.11.0 org.opencontainers.image.version=8.11.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2023-10-31T12:59:21+00:00 org.opencontainers.image.created=2023-10-31T12:59:21+00:00
# Tue, 31 Oct 2023 13:12:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:70db4e7a2af7f73b7cef95301fc20fbedcfe68e5fb874e2cfba0b5ae41a066ca`  
		Last Modified: Wed, 25 Oct 2023 11:40:40 GMT  
		Size: 31.8 MB (31790746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7936218db4b70dd23796ce4fe898a2e041ec2d9022f4bd6b59b58522e1985377`  
		Last Modified: Tue, 07 Nov 2023 14:58:36 GMT  
		Size: 48.3 MB (48286490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263e567d19dbd3779f54850ca80f3e6423c1b3bf2bdb0429b4eb82bba9fe0e97`  
		Last Modified: Tue, 07 Nov 2023 14:58:33 GMT  
		Size: 2.0 KB (2042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfe6910cf9efe0108c488957253d0a762a37f8db75319b460ec2344a12a368e`  
		Last Modified: Tue, 07 Nov 2023 14:58:52 GMT  
		Size: 378.2 MB (378182143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89732bc7504122601f40269fc9ddfb70982e633ea9caf641ae45736f2846b004`  
		Last Modified: Sat, 26 Jan 2019 16:40:00 GMT  
		Size: 39.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a36fb6d96eb35be859a71c47abd3a56394e1ec5eaccf98bcf81be4f15e9daf`  
		Last Modified: Tue, 07 Nov 2023 14:58:35 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66618343ece5ffd3283b5b329cb09e0481073bda580ad536bf5afd8818be47f7`  
		Last Modified: Tue, 07 Nov 2023 14:58:36 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b94dc2376aa522e60b2b55828978b9120eec421717a3daa71bcd1ebdb2aef8`  
		Last Modified: Tue, 07 Nov 2023 14:58:38 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5459c40c1d14c87b892dca2582996809b25bd4177ac9bc828dcb9d26c0d7b1de`  
		Last Modified: Tue, 07 Nov 2023 14:58:38 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad679ecf5633519e41b37dd522545f986abc95ac5fb14fda95a4dd42d4f3e74`  
		Last Modified: Tue, 07 Nov 2023 14:58:39 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99aa053891847f6c0e7e9dd8c7e2d828e2599bfeba14d85b29c3bea86a969c0`  
		Last Modified: Tue, 07 Nov 2023 14:58:40 GMT  
		Size: 4.1 KB (4125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aeb165680f2ce9c483845ac7ff9e67b29e86e0faec150808b3f0fcd7c4d4dc9`  
		Last Modified: Tue, 07 Nov 2023 14:58:40 GMT  
		Size: 1.9 MB (1948684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0c3b53426634c4ccab4f24974a192599f17d0b9056e8699fb4958feb8ae9b7`  
		Last Modified: Tue, 07 Nov 2023 14:58:40 GMT  
		Size: 743.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0c3b53426634c4ccab4f24974a192599f17d0b9056e8699fb4958feb8ae9b7`  
		Last Modified: Tue, 07 Nov 2023 14:58:40 GMT  
		Size: 743.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.11.0` - unknown; unknown

```console
$ docker pull logstash@sha256:b0da99594e408c75a661d24ec7eebeb64ddcfb40aa2c68d7846947998c8e68ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2814206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e68d4231e6650afa59c83a8b1b379ffd5b1330cdde7a9057a8a55f167d7c07`

```dockerfile
```

-	Layers:
	-	`sha256:290aed7fcd77feebc832ecfa862580f3fc22e227c8621f0d82281d1fad8c53fb`  
		Last Modified: Thu, 09 Nov 2023 22:19:45 GMT  
		Size: 2.8 MB (2805952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83310186eef58979d480ba7a8f71106de61adb36ab5840cf83d22d14da4baaf0`  
		Last Modified: Thu, 09 Nov 2023 22:19:45 GMT  
		Size: 8.3 KB (8254 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.11.0` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:5e45ebf81ff2a2ecc3443b7d04927bf80c063c0e60e992c8fb681afe5ec25534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.0 MB (414990646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48615bafa582943667b5fd94db20a45d2ac1d8c940da19e83737eb80f7e3e7a2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 03 Oct 2023 11:04:09 GMT
ARG RELEASE
# Tue, 03 Oct 2023 11:04:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 11:04:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 11:04:10 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 11:04:16 GMT
ADD file:f70cc2610ea8fcd25e6e9ae727eb9345d5b7198102f6a6d8e458ab8f99efefc3 in / 
# Tue, 03 Oct 2023 11:04:17 GMT
CMD ["/bin/bash"]
# Tue, 31 Oct 2023 13:16:57 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 31 Oct 2023 13:16:57 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Tue, 31 Oct 2023 13:17:10 GMT
RUN curl -Lo - http://localhost:8000/logstash-8.11.0-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.11.0 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt && find /usr/share/logstash -type d -exec chmod g+s {} \; && ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 31 Oct 2023 13:17:10 GMT
WORKDIR /usr/share/logstash
# Tue, 31 Oct 2023 13:17:10 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 31 Oct 2023 13:17:10 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 13:17:10 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 31 Oct 2023 13:17:10 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 31 Oct 2023 13:17:10 GMT
COPY config/log4j2.properties config/ # buildkit
# Tue, 31 Oct 2023 13:17:10 GMT
COPY config/log4j2.file.properties config/ # buildkit
# Tue, 31 Oct 2023 13:17:10 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 31 Oct 2023 13:17:10 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 31 Oct 2023 13:17:10 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 31 Oct 2023 13:17:10 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 31 Oct 2023 13:17:10 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 31 Oct 2023 13:17:11 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 31 Oct 2023 13:17:11 GMT
USER 1000
# Tue, 31 Oct 2023 13:17:11 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 31 Oct 2023 13:17:11 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.11.0 org.opencontainers.image.version=8.11.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2023-10-31T13:01:31+00:00 org.opencontainers.image.created=2023-10-31T13:01:31+00:00
# Tue, 31 Oct 2023 13:17:11 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:6cba4020c0a193cd551ed8edf368670967e3546345b52c4ec66cb0931436e9b9`  
		Last Modified: Thu, 05 Oct 2023 12:12:17 GMT  
		Size: 27.2 MB (27199503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19397d8b86f4f79467b24765398bfd29243be689fb63c24639f082326abffb3`  
		Last Modified: Tue, 07 Nov 2023 23:46:43 GMT  
		Size: 36.5 MB (36523118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4907c53a2a95774b4dabb4ba94d4db5845b743ab62d675b337a4cf01219aa123`  
		Last Modified: Tue, 07 Nov 2023 23:46:39 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:becfdd5d1d2692015d7e0b17fb3c68df7e03d6139d4aa20bc07f029d54e3f62d`  
		Last Modified: Tue, 07 Nov 2023 23:46:58 GMT  
		Size: 349.5 MB (349526712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab0fb2b7fb1bee88c5bfbf616a62e69a6c5f344f476c2669ddb1e9f2d22f716`  
		Last Modified: Tue, 07 Nov 2023 23:46:39 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8affec6045259b98bdab39e796e580d1a1051c480fa43cff2023a96045e8d3eb`  
		Last Modified: Tue, 07 Nov 2023 23:46:37 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80dd691087de1e52ab450bd17c46470dec82bd5dbad5e4bd6d13e89adbd99644`  
		Last Modified: Tue, 07 Nov 2023 23:46:37 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2e5bf3526f1faae7e8fd5ea7a769bec2ecb475463b6f325e48225f78c3f613`  
		Last Modified: Tue, 07 Nov 2023 23:46:36 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b02d0197dcd6596874010bfe8a348bcb869369f825e1c027e11281b2ef98ac5`  
		Last Modified: Tue, 07 Nov 2023 23:46:35 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6059852ae6585d855f5e74b4baff4438a5f6cd5dec8f654e826863e8bc2e297a`  
		Last Modified: Tue, 07 Nov 2023 23:46:35 GMT  
		Size: 3.7 KB (3657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bab966623401f91962bbf5fa072e4a2a3554d28f5b3ec0a096eea19aa919493`  
		Last Modified: Tue, 07 Nov 2023 23:46:36 GMT  
		Size: 1.7 MB (1731597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d4d6c5957f0c8c82f80830787acff043033eea3c4578a0a38d1270ff4b730d`  
		Last Modified: Tue, 07 Nov 2023 23:46:35 GMT  
		Size: 713.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d4d6c5957f0c8c82f80830787acff043033eea3c4578a0a38d1270ff4b730d`  
		Last Modified: Tue, 07 Nov 2023 23:46:35 GMT  
		Size: 713.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
