## `thrift:latest`

```console
$ docker pull thrift@sha256:ebf98d0d7eaec52bbe0d3b0b28c6a2a8e4f6c0cd43dba89b060f5d0c92ab2e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `thrift:latest` - linux; amd64

```console
$ docker pull thrift@sha256:27716a5a98c3f2ab6f693bced73d2f5477f37e0b88648dc501eed604b8a0669e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43745226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f02df5f7961cd2b6a62ef89bff487b3882dbe48747fb2298cfc05a3e60315c6d`
-	Default Command: `["thrift"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:48 GMT
ADD file:425a053fd043786e9454fb269d4c93c624550fb913a8c96d03ddd430b4e6c1c3 in / 
# Tue, 31 Aug 2021 01:20:48 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:20:34 GMT
ENV THRIFT_VERSION=v0.12.0
# Tue, 31 Aug 2021 02:25:17 GMT
RUN buildDeps=" 		automake 		bison 		curl 		flex 		g++ 		libboost-dev 		libboost-filesystem-dev 		libboost-program-options-dev 		libboost-system-dev 		libboost-test-dev 		libevent-dev 		libssl-dev 		libtool 		make 		pkg-config 	"; 	apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& curl -k -sSL "https://github.com/apache/thrift/archive/${THRIFT_VERSION}.tar.gz" -o thrift.tar.gz 	&& mkdir -p /usr/src/thrift 	&& tar zxf thrift.tar.gz -C /usr/src/thrift --strip-components=1 	&& rm thrift.tar.gz 	&& cd /usr/src/thrift 	&& ./bootstrap.sh 	&& ./configure --disable-libs 	&& make 	&& make install 	&& cd / 	&& rm -rf /usr/src/thrift 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/cache/apt/* 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /tmp/* 	&& rm -rf /var/tmp/*
# Tue, 31 Aug 2021 02:25:17 GMT
CMD ["thrift"]
```

-	Layers:
	-	`sha256:e4ca327ec0e73c737201b7a6d7b2df779a3ccf34fe9cf1b0c031e767f6464240`  
		Last Modified: Tue, 31 Aug 2021 01:22:00 GMT  
		Size: 26.7 MB (26708511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f600e1c2317daf4b252f1b30ad40bbad465ca8bbf120676434cf49c7c862006`  
		Last Modified: Tue, 31 Aug 2021 02:25:41 GMT  
		Size: 17.0 MB (17036715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
