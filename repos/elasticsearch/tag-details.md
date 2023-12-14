<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.16`](#elasticsearch71716)
-	[`elasticsearch:8.11.2`](#elasticsearch8112)
-	[`elasticsearch:8.11.3`](#elasticsearch8113)

## `elasticsearch:7.17.16`

```console
$ docker pull elasticsearch@sha256:d158f0bbdaefd98ec48ff59bdbdd9ed3e6e65455563eaa41001ddce40c2e6420
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:7.17.16` - linux; amd64

```console
$ docker pull elasticsearch@sha256:a2527dea759d0f89e0c28dc5bec76b088b192208e439e050f0d7386b807c617a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.6 MB (366626437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e51728c58b9d183d0e57a72b4d65600370570c965902cd24f433f4dd1664503`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 28 Nov 2023 05:17:39 GMT
ARG RELEASE
# Tue, 28 Nov 2023 05:17:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 05:17:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 05:17:39 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 28 Nov 2023 05:17:41 GMT
ADD file:9169bb1d6ef21313aed17e924538fee03d858460ae6b05e01968457dfc043bd7 in / 
# Tue, 28 Nov 2023 05:17:41 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 12:49:29 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Dec 2023 12:49:29 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Dec 2023 12:49:29 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2023 12:49:29 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Dec 2023 12:49:29 GMT
LABEL org.label-schema.build-date=2023-12-08T10:06:54.672540567Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=2b23fa076334f8d4651aeebe458a955a2ae23218 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.16 org.opencontainers.image.created=2023-12-08T10:06:54.672540567Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=2b23fa076334f8d4651aeebe458a955a2ae23218 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.16
# Tue, 12 Dec 2023 12:49:29 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Dec 2023 12:49:29 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:25ad149ed3cff49ddb57ceb4418377f63c897198de1f9de7a24506397822de3e`  
		Last Modified: Tue, 28 Nov 2023 05:37:19 GMT  
		Size: 27.5 MB (27512563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027c0bcdad627fa5974f1df4480a4921b488de4678d60affa7e9f3152f29b062`  
		Last Modified: Thu, 14 Dec 2023 18:51:43 GMT  
		Size: 14.3 MB (14340549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb90aea5c91fc8cd1126356c16cfc8099f979881ef816a227472d96f6ad3ee9`  
		Last Modified: Thu, 14 Dec 2023 18:51:42 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb828add429abf1c2303025bb49307953f3f04520cec12b80ff04d420c8c4dc`  
		Last Modified: Thu, 14 Dec 2023 18:51:49 GMT  
		Size: 324.5 MB (324455673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86716950acc2326454bab9807108e4b28b7d3b695e35672ac1e50a759b19ff0`  
		Last Modified: Thu, 14 Dec 2023 18:51:42 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6a6af76dabc224d2b9bd322582e4c56a0e093fe950a0304c3da88ec442024a`  
		Last Modified: Thu, 14 Dec 2023 18:51:43 GMT  
		Size: 2.0 KB (1979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df80efa8c9c6c00faa14dcd12bb9416c958c9fcb580ffa4b5873203ce6e32fb6`  
		Last Modified: Thu, 14 Dec 2023 18:51:43 GMT  
		Size: 192.1 KB (192144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f674f74f56a9c1cf576847df336b43a0b301cb280c792580ec8f2b67811718`  
		Last Modified: Thu, 14 Dec 2023 18:51:44 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e70437cf653659aaa61677084ce15efab7432a4f16bfeb5cdfaeec4d81b32c8`  
		Last Modified: Thu, 14 Dec 2023 18:51:44 GMT  
		Size: 109.2 KB (109249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.16` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:9e30307049fbd87558abd78ccc67b2fe32e63bbeb72a2e07b0f18b2dcbb3632e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2107526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd3e21faea4138cbe7842533016575a2eb67a4a05ab327927c92f6f924b312a`

```dockerfile
```

-	Layers:
	-	`sha256:2bd665a4014c9a5e61996f02b64d35945e9388518312fefa3da8ce2e2f0281e3`  
		Last Modified: Thu, 14 Dec 2023 18:51:42 GMT  
		Size: 2.1 MB (2069775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ad385100d683ae667ec62809e49257e0d2550e0458b6f1c870535653f15fb6c`  
		Last Modified: Thu, 14 Dec 2023 18:51:42 GMT  
		Size: 37.8 KB (37751 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:7.17.16` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:4c89c8c1bdadcd6e9ebf2c37580a61e37093cd3143e2399b00ff4bdb92c41644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.8 MB (361784660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a1e8fc8a9e6895c208a233c6adcd9fb468022ca6e66bcc98e39e2a118a1f1b`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 28 Nov 2023 05:25:16 GMT
ARG RELEASE
# Tue, 28 Nov 2023 05:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 05:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 05:25:16 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 28 Nov 2023 05:25:23 GMT
ADD file:f80c582e6edb1f05fc0cefc201be3c47d4b4c6ceb20889c434c9fdef0291cbbf in / 
# Tue, 28 Nov 2023 05:25:23 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 12:49:29 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Dec 2023 12:49:29 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Dec 2023 12:49:29 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2023 12:49:29 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Dec 2023 12:49:29 GMT
LABEL org.label-schema.build-date=2023-12-08T10:06:54.672540567Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=2b23fa076334f8d4651aeebe458a955a2ae23218 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.16 org.opencontainers.image.created=2023-12-08T10:06:54.672540567Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=2b23fa076334f8d4651aeebe458a955a2ae23218 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.16
# Tue, 12 Dec 2023 12:49:29 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Dec 2023 12:49:29 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:dae58cbd668a05adbb25fa9970bfa041b807c2c537b86caa4ab74f77cfac02df`  
		Last Modified: Tue, 28 Nov 2023 05:37:25 GMT  
		Size: 26.0 MB (25975507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cd4f99a610be444dfff1ae0c40ce13564f13e34b28c5be770e1d952eed9c6b`  
		Last Modified: Tue, 12 Dec 2023 17:49:40 GMT  
		Size: 13.1 MB (13103533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdf3ab269a14f2fe4e3711c51d1ca401e0b0ee05fbdac3182da784b5258f4b2`  
		Last Modified: Tue, 12 Dec 2023 17:49:39 GMT  
		Size: 4.3 KB (4326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba730edf31691b025ed8ba38962f964ff0563211f400a7a67684049f847fa52`  
		Last Modified: Thu, 14 Dec 2023 19:34:33 GMT  
		Size: 322.4 MB (322394350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbdfed47dee0b7d1d7dc2425b987408ba8b659b7915e4370ee54eea228fd267`  
		Last Modified: Thu, 14 Dec 2023 19:34:25 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec83c6ad1e9e66d694c8b4e9dfe08f8073086157a58d01b9575017f2ba2700f`  
		Last Modified: Thu, 14 Dec 2023 19:34:25 GMT  
		Size: 2.0 KB (1984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c098f9a5b6fbf5c278066822c12cf8badb1fe9f726072feae05dd6c877b3a7`  
		Last Modified: Thu, 14 Dec 2023 19:34:26 GMT  
		Size: 186.2 KB (186170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589c2b08fdbef037fcdfd3679d0ef2daaa6a279cbc376a7988543fa410f4fd65`  
		Last Modified: Thu, 14 Dec 2023 19:34:26 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3383cf3663bcf1d013315adb1ad351a4076d2b5b4eee9e43135166285279f82`  
		Last Modified: Thu, 14 Dec 2023 19:34:27 GMT  
		Size: 109.2 KB (109250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.16` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:90deff51fd0cfdc86d2add7ea9354c5bdab551c3c78c25fe9eca701633e923e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2107692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36432870664415139a3852e880db1283f940bae9ac56c9cc0d8c0f070cc9aa0`

```dockerfile
```

-	Layers:
	-	`sha256:9cd9dad00e234302ab5bf8e9ddcfa0b3d1be7a41df1fa8c07f109e9b0909d154`  
		Last Modified: Thu, 14 Dec 2023 19:34:26 GMT  
		Size: 2.1 MB (2070098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73ccdf9ad71f431ce3f2e4c3b68a7e75be8061b14b000acd225779fe69b6ce29`  
		Last Modified: Thu, 14 Dec 2023 19:34:25 GMT  
		Size: 37.6 KB (37594 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.11.2`

```console
$ docker pull elasticsearch@sha256:29e5dfe42efbed2f2ce169ec367a6b299c20d37e1ea8d76ed2e08ce7ec505458
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.11.2` - linux; amd64

```console
$ docker pull elasticsearch@sha256:3167a95768e947863f17e744a8d8eeb1311a8122a5802efde37a99534703fb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.1 MB (680111559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212d3d19070996ead468a0f085f93317e2f71b2950ebb30d4233806bf63ffc4b`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 28 Nov 2023 05:17:39 GMT
ARG RELEASE
# Tue, 28 Nov 2023 05:17:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 05:17:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 05:17:39 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 28 Nov 2023 05:17:41 GMT
ADD file:9169bb1d6ef21313aed17e924538fee03d858460ae6b05e01968457dfc043bd7 in / 
# Tue, 28 Nov 2023 05:17:41 GMT
CMD ["/bin/bash"]
# Thu, 07 Dec 2023 12:34:16 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 07 Dec 2023 12:34:16 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 07 Dec 2023 12:34:16 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Dec 2023 12:34:16 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 07 Dec 2023 12:34:16 GMT
LABEL org.label-schema.build-date=2023-12-05T10:03:47.729926671Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=76013fa76dcbf144c886990c6290715f5dc2ae20 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.11.2 org.opencontainers.image.created=2023-12-05T10:03:47.729926671Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=76013fa76dcbf144c886990c6290715f5dc2ae20 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.11.2
# Thu, 07 Dec 2023 12:34:16 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 07 Dec 2023 12:34:16 GMT
CMD ["eswrapper"]
# Thu, 07 Dec 2023 12:34:16 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:25ad149ed3cff49ddb57ceb4418377f63c897198de1f9de7a24506397822de3e`  
		Last Modified: Tue, 28 Nov 2023 05:37:19 GMT  
		Size: 27.5 MB (27512563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e611e6137254040d01c7676652917196284a03d1a3fc1f5a5998b56c510bff0`  
		Last Modified: Thu, 14 Dec 2023 18:52:29 GMT  
		Size: 14.3 MB (14340740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3fa29d22eddf79a7ab9996b721fbf3b94e19862b47e22f8c352aea9f9f9c74`  
		Last Modified: Thu, 14 Dec 2023 18:52:28 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d828a09df1c39c2fe7d8ab3d9fb0ef0ab41123b84b8b1a2a9584cbed37f11874`  
		Last Modified: Thu, 14 Dec 2023 18:52:43 GMT  
		Size: 637.9 MB (637941129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7e28750d8c6a2939aa46bc4d26ddc6b5746d77988bffa5127fb8fef75c1f0a`  
		Last Modified: Thu, 14 Dec 2023 18:52:28 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ae364151ff0c959a4a13b3ee92eef2ef3a7aee966490906ae7edc9004a0108`  
		Last Modified: Thu, 14 Dec 2023 18:52:30 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b434b16381677778c14b0438959dbe6a98dbe60f5d1d160c941f3613499cf1a4`  
		Last Modified: Thu, 14 Dec 2023 18:52:30 GMT  
		Size: 191.9 KB (191877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e75da5ece7dfcb7dd1a5d65ea9259a6536e80a1a21fefc29e3a877c5bead9ac`  
		Last Modified: Thu, 14 Dec 2023 18:52:31 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce0a9ce9cf1d883ba242efa14dafe21f2367ae2f2bff43b6ac035aeabcb0982`  
		Last Modified: Thu, 14 Dec 2023 18:52:32 GMT  
		Size: 109.3 KB (109252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.11.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:99998b3a675055d0752afc45bbc8e07cf86dcc5eaa2f778f5e352c39f53af03a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2376848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18286a4cd188c1ce2e822ecef4b1f90edd409256e36ec24875c3bf51867005d5`

```dockerfile
```

-	Layers:
	-	`sha256:0445cb3dde263a63944ee3f5435bb72ba036da7dee1f1edb2d834910bdee12ed`  
		Last Modified: Thu, 14 Dec 2023 18:52:29 GMT  
		Size: 2.3 MB (2339082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae72b7dde0d0804f1b25773904ed0080a54d1a7ef6f585f52400c8cf1f8186e4`  
		Last Modified: Thu, 14 Dec 2023 18:52:28 GMT  
		Size: 37.8 KB (37766 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.11.2` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:e1fd628a70d52683ee032f2d72948a1d28d16a7772ac533a60422e7a1d28f389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **456.5 MB (456537204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4596f0d2accf7be6471f0ca46abbfd31df63317435310d5f0638efa50c11fad`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 28 Nov 2023 05:25:16 GMT
ARG RELEASE
# Tue, 28 Nov 2023 05:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 05:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 05:25:16 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 28 Nov 2023 05:25:23 GMT
ADD file:f80c582e6edb1f05fc0cefc201be3c47d4b4c6ceb20889c434c9fdef0291cbbf in / 
# Tue, 28 Nov 2023 05:25:23 GMT
CMD ["/bin/bash"]
# Thu, 07 Dec 2023 12:34:16 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 07 Dec 2023 12:34:16 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 07 Dec 2023 12:34:16 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Dec 2023 12:34:16 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 07 Dec 2023 12:34:16 GMT
LABEL org.label-schema.build-date=2023-12-05T10:03:47.729926671Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=76013fa76dcbf144c886990c6290715f5dc2ae20 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.11.2 org.opencontainers.image.created=2023-12-05T10:03:47.729926671Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=76013fa76dcbf144c886990c6290715f5dc2ae20 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.11.2
# Thu, 07 Dec 2023 12:34:16 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 07 Dec 2023 12:34:16 GMT
CMD ["eswrapper"]
# Thu, 07 Dec 2023 12:34:16 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:dae58cbd668a05adbb25fa9970bfa041b807c2c537b86caa4ab74f77cfac02df`  
		Last Modified: Tue, 28 Nov 2023 05:37:25 GMT  
		Size: 26.0 MB (25975507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fad6d5c5cc520ad13dbf6a0fad6c68e44f414404e8f7cce759a1533656103b3`  
		Last Modified: Tue, 12 Dec 2023 17:48:11 GMT  
		Size: 13.1 MB (13103527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c2b9825c789c2462f62696c0513cfc91e1df500b5ea96ee546250047bb6068`  
		Last Modified: Tue, 12 Dec 2023 17:48:10 GMT  
		Size: 4.3 KB (4317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9e590e913bcc5f376cecfb8c678bfd9233dc66897a75087a7354bfdfb90a4b`  
		Last Modified: Thu, 14 Dec 2023 19:32:00 GMT  
		Size: 417.1 MB (417147432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d75909748fece91d574f65e5a1b43c6c266b0e1f869aef2963fe7ecbe981ba2`  
		Last Modified: Thu, 14 Dec 2023 19:31:49 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6141f47b5431387ffe9b52c941538a02db70aad70868f3223e9a1f18732d6334`  
		Last Modified: Thu, 14 Dec 2023 19:31:50 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c33057cf2ae8d7550d1db0d0a489d7755da1e2b5191af7ba01960af73a48a0`  
		Last Modified: Thu, 14 Dec 2023 19:31:50 GMT  
		Size: 185.9 KB (185903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44aa5f504a8211bcbdcb3eceac3bd3ecfdcb05f2057b91affc82dac5c23745d0`  
		Last Modified: Thu, 14 Dec 2023 19:31:51 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc7808036e8e94c79c132dd51e0dedc1b45783e5776f376b0185af9555097e9`  
		Last Modified: Thu, 14 Dec 2023 19:31:51 GMT  
		Size: 109.3 KB (109257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.11.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:539b48fafdb8027f2214eee6c3c726f001692ba127001bdde7f0a2aae2bdc637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb9c803a4109fa9bbff9c0e49406c3a42c641d33ab34231f9d4ef078a9556216`

```dockerfile
```

-	Layers:
	-	`sha256:dbdba262a4b7cd0f1a281d4fdbf0f36062af03fca3f27bc119fdbabe55cae08b`  
		Last Modified: Thu, 14 Dec 2023 19:31:50 GMT  
		Size: 2.3 MB (2339405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03d237023e1363c8d5ac5c1540eb9631b2b5149afc5bbb79724e2923851ee1fd`  
		Last Modified: Thu, 14 Dec 2023 19:31:49 GMT  
		Size: 37.6 KB (37610 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.11.3`

```console
$ docker pull elasticsearch@sha256:32313bf758f47f7b514f5bcb7e9d6eedebe4de5411c0c785c0352206c28ced08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.11.3` - linux; amd64

```console
$ docker pull elasticsearch@sha256:7c5a3bdb242e0dd35bad7dcb4b5f432d8bc8515564d06c04c34e9b6cb0c6aa04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.1 MB (680117617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114d814920ae8a7984e8faf81a9b87b8f26587ec21945110a053ba6983731198`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 28 Nov 2023 05:17:39 GMT
ARG RELEASE
# Tue, 28 Nov 2023 05:17:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 05:17:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 05:17:39 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 28 Nov 2023 05:17:41 GMT
ADD file:9169bb1d6ef21313aed17e924538fee03d858460ae6b05e01968457dfc043bd7 in / 
# Tue, 28 Nov 2023 05:17:41 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 13:07:20 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Dec 2023 13:07:20 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Dec 2023 13:07:20 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2023 13:07:20 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Dec 2023 13:07:20 GMT
LABEL org.label-schema.build-date=2023-12-08T11:33:53.634979452Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=64cf052f3b56b1fd4449f5454cb88aca7e739d9a org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.11.3 org.opencontainers.image.created=2023-12-08T11:33:53.634979452Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=64cf052f3b56b1fd4449f5454cb88aca7e739d9a org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.11.3
# Tue, 12 Dec 2023 13:07:20 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Dec 2023 13:07:20 GMT
CMD ["eswrapper"]
# Tue, 12 Dec 2023 13:07:20 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:25ad149ed3cff49ddb57ceb4418377f63c897198de1f9de7a24506397822de3e`  
		Last Modified: Tue, 28 Nov 2023 05:37:19 GMT  
		Size: 27.5 MB (27512563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef072f36d9834bea8a6d3909431e220489c205356288a7471f7f33a760bca5fb`  
		Last Modified: Thu, 14 Dec 2023 18:52:25 GMT  
		Size: 14.3 MB (14340666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa57d1764caf6c7973b26e2e8aa42dc9a91eb15ae6be3066934817866af94d6`  
		Last Modified: Thu, 14 Dec 2023 18:52:24 GMT  
		Size: 4.3 KB (4318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4abecb0e790720424042bdcd575c965baf0f5d64207afd0a52841b863a1e44`  
		Last Modified: Thu, 14 Dec 2023 18:52:37 GMT  
		Size: 637.9 MB (637947253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fc31cc6346e38c818795dc9a28dbff4ad31486ffc8c54673f01119191cc633`  
		Last Modified: Thu, 14 Dec 2023 18:52:25 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c66da9c173dbd4bf6ae73d8e8467391b58be7057c5aa42498105982f7efdd40`  
		Last Modified: Thu, 14 Dec 2023 18:52:25 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c206d3c7f8416eef7a954e8d3c47abb3d88f8528e8d200c325eda4eb4da1bd02`  
		Last Modified: Thu, 14 Dec 2023 18:52:26 GMT  
		Size: 191.9 KB (191883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f46301c72b4e287fa47a79c43bbace6aa48e0acaf0f1236b41c15468f420afd`  
		Last Modified: Thu, 14 Dec 2023 18:52:26 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e907a0c050ca10acc27c62009782cee08622a6b9c4f59d388832395a778780d2`  
		Last Modified: Thu, 14 Dec 2023 18:52:26 GMT  
		Size: 109.2 KB (109248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.11.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:9337b57f424ebbc5139ce5e0d635552fe56eb01b5689a6e6fa68327c73a645c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2376849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af07b3a74128e35dec0a58381239ab2d2eea849c47ce9c600cec8deb92ed19f`

```dockerfile
```

-	Layers:
	-	`sha256:3ff91380d3515d5e09ef9b5dd69d5e7d5d2eac97347e9ab17d3e67872a4adaf5`  
		Last Modified: Thu, 14 Dec 2023 18:52:25 GMT  
		Size: 2.3 MB (2339082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc7ea8991c9d5994b7467e57c28d91330e108c55939012abe3d300e4a2078607`  
		Last Modified: Thu, 14 Dec 2023 18:52:24 GMT  
		Size: 37.8 KB (37767 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.11.3` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:44398545f17b295cb016e0c50dc12efb538eab67e87fdbc2499cc0448200c480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **456.5 MB (456542578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92866351f1d21ad06cbcd8cef0251a644efbb68e4eb0c9f56f7a7b40c639628f`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 28 Nov 2023 05:25:16 GMT
ARG RELEASE
# Tue, 28 Nov 2023 05:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 05:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 05:25:16 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 28 Nov 2023 05:25:23 GMT
ADD file:f80c582e6edb1f05fc0cefc201be3c47d4b4c6ceb20889c434c9fdef0291cbbf in / 
# Tue, 28 Nov 2023 05:25:23 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 13:07:20 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Dec 2023 13:07:20 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Dec 2023 13:07:20 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2023 13:07:20 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Dec 2023 13:07:20 GMT
LABEL org.label-schema.build-date=2023-12-08T11:33:53.634979452Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=64cf052f3b56b1fd4449f5454cb88aca7e739d9a org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.11.3 org.opencontainers.image.created=2023-12-08T11:33:53.634979452Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=64cf052f3b56b1fd4449f5454cb88aca7e739d9a org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.11.3
# Tue, 12 Dec 2023 13:07:20 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Dec 2023 13:07:20 GMT
CMD ["eswrapper"]
# Tue, 12 Dec 2023 13:07:20 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:dae58cbd668a05adbb25fa9970bfa041b807c2c537b86caa4ab74f77cfac02df`  
		Last Modified: Tue, 28 Nov 2023 05:37:25 GMT  
		Size: 26.0 MB (25975507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fad6d5c5cc520ad13dbf6a0fad6c68e44f414404e8f7cce759a1533656103b3`  
		Last Modified: Tue, 12 Dec 2023 17:48:11 GMT  
		Size: 13.1 MB (13103527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c2b9825c789c2462f62696c0513cfc91e1df500b5ea96ee546250047bb6068`  
		Last Modified: Tue, 12 Dec 2023 17:48:10 GMT  
		Size: 4.3 KB (4317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715eb0de7bac9b6d554a5e26bfafdf2afa5f1449be13bd98cfd8eb8b27e539d5`  
		Last Modified: Thu, 14 Dec 2023 19:23:06 GMT  
		Size: 417.2 MB (417152807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b996c48e81a2bb33206f1ef942d24aa751f2d680ab2f60382ea5093b2af34a3`  
		Last Modified: Thu, 14 Dec 2023 19:22:57 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0edcba450a381bed3774b133f94cd449b405eaf58a3151f01ff1634849a66f`  
		Last Modified: Thu, 14 Dec 2023 19:22:57 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd5fcee8a7e50961b8a4e4c800e58543768b3bccb7f706636810e638b658b9c`  
		Last Modified: Thu, 14 Dec 2023 19:22:57 GMT  
		Size: 185.9 KB (185904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ad3ae845f052b8d52f6c6a61dfc48185e84ea0f5abbe2552e9a10ec8c8af8e`  
		Last Modified: Thu, 14 Dec 2023 19:22:58 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd48697c3d9a794bd555ab5f5f263654225c981a8eea063af5ce75c3db85c0b`  
		Last Modified: Thu, 14 Dec 2023 19:22:58 GMT  
		Size: 109.3 KB (109254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.11.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:187d5e81002c71e7a9134c6173fed78b42d1744f89202215f0d756199946ac9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789a22aaffe1ca9d0f094f4f8378b7b97572b28e198027a1fbf166eb2420fc19`

```dockerfile
```

-	Layers:
	-	`sha256:b1b2a0d17147ac7109d5fbd5fb466311422690ab34daa880fec08fcb12f02718`  
		Last Modified: Thu, 14 Dec 2023 19:22:57 GMT  
		Size: 2.3 MB (2339405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d33af2d1bdea4795e5c5c7291e68b6e0a340ceb03b6d233d6fd0693965372781`  
		Last Modified: Thu, 14 Dec 2023 19:22:57 GMT  
		Size: 37.6 KB (37610 bytes)  
		MIME: application/vnd.in-toto+json
