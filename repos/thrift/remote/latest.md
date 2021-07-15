## `thrift:latest`

```console
$ docker pull thrift@sha256:7cb2f20b73e2459e4ddb29261d2ac7d4919b57ce7af6bc9070391ac467de8177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `thrift:latest` - linux; amd64

```console
$ docker pull thrift@sha256:3c5976c992de963f421ec5e3b914a6e68ec7ae3fa5df942f9abf2bd7b32a5ad8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43743109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aafa2d18f771f1554a69470b8075be1ddb2c767f65c6315869e463548a4dd24`
-	Default Command: `["thrift"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:15 GMT
ADD file:7274ece1917848683250bbeda9eacf6eb7510481cbaa177880e3a60b4133e35b in / 
# Tue, 13 Jul 2021 22:29:15 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 03:28:55 GMT
ENV THRIFT_VERSION=v0.12.0
# Wed, 14 Jul 2021 03:32:56 GMT
RUN buildDeps=" 		automake 		bison 		curl 		flex 		g++ 		libboost-dev 		libboost-filesystem-dev 		libboost-program-options-dev 		libboost-system-dev 		libboost-test-dev 		libevent-dev 		libssl-dev 		libtool 		make 		pkg-config 	"; 	apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& curl -k -sSL "https://github.com/apache/thrift/archive/${THRIFT_VERSION}.tar.gz" -o thrift.tar.gz 	&& mkdir -p /usr/src/thrift 	&& tar zxf thrift.tar.gz -C /usr/src/thrift --strip-components=1 	&& rm thrift.tar.gz 	&& cd /usr/src/thrift 	&& ./bootstrap.sh 	&& ./configure --disable-libs 	&& make 	&& make install 	&& cd / 	&& rm -rf /usr/src/thrift 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/cache/apt/* 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /tmp/* 	&& rm -rf /var/tmp/*
# Wed, 14 Jul 2021 03:32:56 GMT
CMD ["thrift"]
```

-	Layers:
	-	`sha256:e7ae86ffe2df0787131a4c49ace1b018fd38d62929b007d86bdd1f825e56a852`  
		Last Modified: Tue, 13 Jul 2021 22:31:03 GMT  
		Size: 26.7 MB (26706145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ad653376105cd82823d8bce467c8af3844d4f7204bc6ec2b451eddeafa523c`  
		Last Modified: Wed, 14 Jul 2021 03:33:18 GMT  
		Size: 17.0 MB (17036964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
