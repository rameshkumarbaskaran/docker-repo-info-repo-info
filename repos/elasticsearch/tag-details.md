<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:6.8.7`](#elasticsearch687)
-	[`elasticsearch:7.6.1`](#elasticsearch761)

## `elasticsearch:6.8.7`

```console
$ docker pull elasticsearch@sha256:ec7dd7cc7da5d7f6d9bde3e827b6528bcd96f1132986e730b694d1ade4ff534a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `elasticsearch:6.8.7` - linux; amd64

```console
$ docker pull elasticsearch@sha256:f58bcad2b9405084e9a9a928a700c051b92bc8abe4f5271b41ea0ba4d897fed7
```

-	Docker Version: 19.03.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.0 MB (465999423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cdc9986c313cb90ffc63842963b3d461aef42d9e6791fb8f8979002e42e1770`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Wed, 26 Feb 2020 14:42:15 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 26 Feb 2020 14:42:16 GMT
ENV JAVA_HOME=/opt/jdk-13.0.2+8
# Wed, 26 Feb 2020 14:42:24 GMT
COPY dir:c7c79974d85e29bb31c6146bbec28f47f27379ef4cc0a27af31ffdf76a8bd503 in /opt/jdk-13.0.2+8 
# Wed, 26 Feb 2020 14:43:02 GMT
RUN for iter in {1..10}; do yum update  --setopt=tsflags=nodocs -y &&     yum install -y  --setopt=tsflags=nodocs nc unzip wget which &&     yum clean all && exit_code=0 && break || exit_code=\$? && echo "yum error: retry $iter in 10s" && sleep 10; done;     (exit $exit_code)
# Wed, 26 Feb 2020 14:43:06 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chmod 0775 /usr/share/elasticsearch &&     chgrp 0 /usr/share/elasticsearch
# Wed, 26 Feb 2020 14:43:07 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 26 Feb 2020 14:43:13 GMT
COPY --chown=1000:0dir:2adb2db14bf110aa4f9df9f12957998c1e1fa724e2f97cc4850aca72d83b8edf in /usr/share/elasticsearch 
# Wed, 26 Feb 2020 14:43:14 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 14:43:14 GMT
COPY --chown=1000:0file:08193f849fc25f29db1438eff6d5c9fe1d63237aeb07a3e0009e8ba554f97c31 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 26 Feb 2020 14:43:17 GMT
RUN chgrp 0 /usr/local/bin/docker-entrypoint.sh &&     chmod g=u /etc/passwd &&     chmod 0775 /usr/local/bin/docker-entrypoint.sh
# Wed, 26 Feb 2020 14:43:17 GMT
EXPOSE 9200 9300
# Wed, 26 Feb 2020 14:43:18 GMT
LABEL org.label-schema.build-date=2020-02-26T14:38:01.193138Z org.label-schema.license=Elastic-License org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c63e621eaba638f77ebb10e03f7637688eb0a726 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=6.8.7 org.opencontainers.image.created=2020-02-26T14:38:01.193138Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License org.opencontainers.image.revision=c63e621eaba638f77ebb10e03f7637688eb0a726 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=6.8.7
# Wed, 26 Feb 2020 14:43:19 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Wed, 26 Feb 2020 14:43:21 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf190bd12b7b74671037b955882a868a98a5740d2d13c19c08b1932f7f863875`  
		Last Modified: Wed, 04 Mar 2020 22:09:20 GMT  
		Size: 208.4 MB (208435530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f29a357a380ffb0dd6fd0a2b216a5dae8ad8fbf90b9f883d3ae939c92e87380`  
		Last Modified: Wed, 04 Mar 2020 22:08:58 GMT  
		Size: 30.8 MB (30826541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72133ff33327e82a39e42b5db8685eaf05ed03199a5c712fe8e812294c851e44`  
		Last Modified: Wed, 04 Mar 2020 22:08:52 GMT  
		Size: 2.3 KB (2331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c64bf4688499b11caa1f2a82b63a4a53c8746b6fc40edbf7eb3680e02679f10d`  
		Last Modified: Wed, 04 Mar 2020 22:09:18 GMT  
		Size: 150.9 MB (150949810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0af0c6ae269fe877996a3ca115339d9896af13f645e0e57a71efe295c7614a4`  
		Last Modified: Wed, 04 Mar 2020 22:08:52 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9524fedcb544869dbae5aab7d087333012d365eb0a4e734793a05f483cbdd07e`  
		Last Modified: Wed, 04 Mar 2020 22:08:52 GMT  
		Size: 2.4 KB (2418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `elasticsearch:7.6.1`

```console
$ docker pull elasticsearch@sha256:e779a3f3e2b5ec085c44055e61ac908f42c8c174628219d22ad405d9fe7e10fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `elasticsearch:7.6.1` - linux; amd64

```console
$ docker pull elasticsearch@sha256:76e9a781357ded86dcddaed0cfe3ee9b7fb412101ed251f7a9e3581548810bd7
```

-	Docker Version: 19.03.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.8 MB (404767986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41072cdeebc50e080607ef04258a348a1d627b63cfb3034ff3885a5f5e067624`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Sat, 29 Feb 2020 00:19:15 GMT
ENV ELASTIC_CONTAINER=true
# Sat, 29 Feb 2020 00:20:01 GMT
RUN for iter in {1..10}; do yum update --setopt=tsflags=nodocs -y &&     yum install --setopt=tsflags=nodocs -y nc shadow-utils zip unzip &&     yum clean all && exit_code=0 && break || exit_code=$? && echo "yum error: retry $iter in 10s" && sleep 10; done;     (exit $exit_code)
# Sat, 29 Feb 2020 00:20:02 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chmod 0775 /usr/share/elasticsearch &&     chgrp 0 /usr/share/elasticsearch
# Sat, 29 Feb 2020 00:20:02 GMT
WORKDIR /usr/share/elasticsearch
# Sat, 29 Feb 2020 00:20:12 GMT
COPY --chown=1000:0dir:0c72cbebb8883ad9924e5f0aaf040c91ec785db7fa1cc3368be3770f723e98d5 in /usr/share/elasticsearch 
# Sat, 29 Feb 2020 00:20:13 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts /usr/share/elasticsearch/jdk/lib/security/cacerts
# Sat, 29 Feb 2020 00:20:14 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 29 Feb 2020 00:20:14 GMT
COPY --chown=1000:0file:4e194e0f53ce77fff91bb999402cbd943658f591ee80ee538c1d145b9e464be4 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 29 Feb 2020 00:20:15 GMT
RUN chgrp 0 /usr/local/bin/docker-entrypoint.sh &&     chmod g=u /etc/passwd &&     chmod 0775 /usr/local/bin/docker-entrypoint.sh
# Sat, 29 Feb 2020 00:20:15 GMT
EXPOSE 9200 9300
# Sat, 29 Feb 2020 00:20:15 GMT
LABEL org.label-schema.build-date=2020-02-29T00:15:25.529771Z org.label-schema.license=Elastic-License org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=aa751e09be0a5072e8570670309b1f12348f023b org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.6.1 org.opencontainers.image.created=2020-02-29T00:15:25.529771Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License org.opencontainers.image.revision=aa751e09be0a5072e8570670309b1f12348f023b org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.6.1
# Sat, 29 Feb 2020 00:20:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Sat, 29 Feb 2020 00:20:16 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1836a70f10a6b47ef6d1fe5cd28dd71944f74c2d2ef39fb73ad80c4b3adbaa7`  
		Last Modified: Wed, 04 Mar 2020 19:43:28 GMT  
		Size: 30.9 MB (30858131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20af6116b6bdbd08955ecb57b6706aab95e917ae4dddbcea9159e2fc3362f593`  
		Last Modified: Wed, 04 Mar 2020 19:43:19 GMT  
		Size: 2.3 KB (2336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c1a145d9e83e3add5ee1b99ca88a1e55b7b17148f05ea1a955782a435c515b`  
		Last Modified: Wed, 04 Mar 2020 19:44:15 GMT  
		Size: 298.1 MB (298122936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992cc3ebce9bd550325456e56ae93a9c50bb373927a1ac1ae24a5638578a0b5b`  
		Last Modified: Wed, 04 Mar 2020 19:43:15 GMT  
		Size: 293.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c986d28790533411f611a1f8edda725e232ed9ea26dafa5f2486dde00a5f245a`  
		Last Modified: Wed, 04 Mar 2020 19:43:15 GMT  
		Size: 1.6 KB (1621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662a6b9facf4e20ad14bec871c5478272a358924864f752c1265a5dc326c5398`  
		Last Modified: Wed, 04 Mar 2020 19:43:15 GMT  
		Size: 2.0 KB (1957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
