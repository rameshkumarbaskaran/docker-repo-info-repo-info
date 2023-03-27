<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:4`](#emqx4)
-	[`emqx:4.4`](#emqx44)
-	[`emqx:4.4.16`](#emqx4416)
-	[`emqx:5`](#emqx5)
-	[`emqx:5.0`](#emqx50)
-	[`emqx:5.0.21`](#emqx5021)
-	[`emqx:latest`](#emqxlatest)

## `emqx:4`

```console
$ docker pull emqx@sha256:d0c7a636891e44bfdc8c66697fec9b5cb94675210cb090cffd732a6219ab5284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4` - linux; amd64

```console
$ docker pull emqx@sha256:b594671f1c8c001b76971e896ec29f4aea1b4ce35e471f418b7e190d66bdfe8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81272225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df18f1b36fce0936fd74b9faf314e3a01d83c037091286efb92131b581fe822`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:38:29 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 06:38:30 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Thu, 23 Mar 2023 06:38:30 GMT
ENV EMQX_VERSION=4.4.16
# Thu, 23 Mar 2023 06:38:30 GMT
ENV OTP=otp24.3.4.2-1
# Thu, 23 Mar 2023 06:38:34 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="901b76ea2bee68729b75280740ca31b1af5b358d331422d1653dc342ee830324"; fi;     if [ ${arch} = "arm64" ]; then sha256="1224f53d0ee98390c286f3bbd9af2f294c2fa4ccb79342343d803fa234165c6e"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Thu, 23 Mar 2023 06:38:34 GMT
WORKDIR /opt/emqx
# Thu, 23 Mar 2023 06:38:35 GMT
USER emqx
# Thu, 23 Mar 2023 06:38:35 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 23 Mar 2023 06:38:35 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Thu, 23 Mar 2023 06:38:35 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Thu, 23 Mar 2023 06:38:35 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 23 Mar 2023 06:38:35 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7216294cbe2d1311e293a82d22eb3f71da435b2b9bb7ad9900eaaeb14d68d2b7`  
		Last Modified: Thu, 23 Mar 2023 06:39:01 GMT  
		Size: 2.6 MB (2569460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca85a7d40cdb8392bb213cc3b9efc98bcb416df588c86b55eb174485340016cb`  
		Last Modified: Thu, 23 Mar 2023 06:39:01 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93644246d8ba201ec9c154bf77410efda76bbc02af25c4d8c89b5bef6aa7e90e`  
		Last Modified: Thu, 23 Mar 2023 06:39:05 GMT  
		Size: 47.3 MB (47286145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1172e73e519b49b8ecabc31cf1807694cf854572647611963d00191e5c03612`  
		Last Modified: Thu, 23 Mar 2023 06:39:01 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:5077868044732549104a37735bbeb9eeea04990428ec84565089b9f912a27b4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72700174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b721a7424bef3c917f99584f6ede9bdd469bf8bf89ca3187bf5fd2fa3f563f5c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:10 GMT
ADD file:83beb883b699cd442f1dbd4baf29c23f4cd15f7a5f9f120979df16a77455c69f in / 
# Thu, 23 Mar 2023 00:45:10 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:22:40 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 07:22:40 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Thu, 23 Mar 2023 07:22:40 GMT
ENV EMQX_VERSION=4.4.16
# Thu, 23 Mar 2023 07:22:40 GMT
ENV OTP=otp24.3.4.2-1
# Thu, 23 Mar 2023 07:22:44 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="901b76ea2bee68729b75280740ca31b1af5b358d331422d1653dc342ee830324"; fi;     if [ ${arch} = "arm64" ]; then sha256="1224f53d0ee98390c286f3bbd9af2f294c2fa4ccb79342343d803fa234165c6e"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Thu, 23 Mar 2023 07:22:44 GMT
WORKDIR /opt/emqx
# Thu, 23 Mar 2023 07:22:44 GMT
USER emqx
# Thu, 23 Mar 2023 07:22:45 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 23 Mar 2023 07:22:45 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Thu, 23 Mar 2023 07:22:45 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Thu, 23 Mar 2023 07:22:45 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 23 Mar 2023 07:22:45 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:fcdb9667c46b09d1c1d058681ea4a1db41e66bbc1a71d873a0c9da4f7a92947d`  
		Last Modified: Thu, 23 Mar 2023 00:48:09 GMT  
		Size: 30.1 MB (30062700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a2fca160acd6916ee9f7a44af39ca048ec3dba62c3d8276915f397320d937d`  
		Last Modified: Thu, 23 Mar 2023 07:23:07 GMT  
		Size: 2.6 MB (2559254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602fe4683989e6650cbe1071564b8e4029b4eacf0814ee226b81bfa86c6df9fe`  
		Last Modified: Thu, 23 Mar 2023 07:23:07 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4d7f2460db59baf21229445904a5c93abb98a720847d234328af163a73069b`  
		Last Modified: Thu, 23 Mar 2023 07:23:10 GMT  
		Size: 40.1 MB (40073001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b619deebd0c236156f78632f97bd2738a18a1a8edf1e4cabdeb0d403c57810db`  
		Last Modified: Thu, 23 Mar 2023 07:23:07 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4`

```console
$ docker pull emqx@sha256:d0c7a636891e44bfdc8c66697fec9b5cb94675210cb090cffd732a6219ab5284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.4` - linux; amd64

```console
$ docker pull emqx@sha256:b594671f1c8c001b76971e896ec29f4aea1b4ce35e471f418b7e190d66bdfe8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81272225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df18f1b36fce0936fd74b9faf314e3a01d83c037091286efb92131b581fe822`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:38:29 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 06:38:30 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Thu, 23 Mar 2023 06:38:30 GMT
ENV EMQX_VERSION=4.4.16
# Thu, 23 Mar 2023 06:38:30 GMT
ENV OTP=otp24.3.4.2-1
# Thu, 23 Mar 2023 06:38:34 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="901b76ea2bee68729b75280740ca31b1af5b358d331422d1653dc342ee830324"; fi;     if [ ${arch} = "arm64" ]; then sha256="1224f53d0ee98390c286f3bbd9af2f294c2fa4ccb79342343d803fa234165c6e"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Thu, 23 Mar 2023 06:38:34 GMT
WORKDIR /opt/emqx
# Thu, 23 Mar 2023 06:38:35 GMT
USER emqx
# Thu, 23 Mar 2023 06:38:35 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 23 Mar 2023 06:38:35 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Thu, 23 Mar 2023 06:38:35 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Thu, 23 Mar 2023 06:38:35 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 23 Mar 2023 06:38:35 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7216294cbe2d1311e293a82d22eb3f71da435b2b9bb7ad9900eaaeb14d68d2b7`  
		Last Modified: Thu, 23 Mar 2023 06:39:01 GMT  
		Size: 2.6 MB (2569460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca85a7d40cdb8392bb213cc3b9efc98bcb416df588c86b55eb174485340016cb`  
		Last Modified: Thu, 23 Mar 2023 06:39:01 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93644246d8ba201ec9c154bf77410efda76bbc02af25c4d8c89b5bef6aa7e90e`  
		Last Modified: Thu, 23 Mar 2023 06:39:05 GMT  
		Size: 47.3 MB (47286145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1172e73e519b49b8ecabc31cf1807694cf854572647611963d00191e5c03612`  
		Last Modified: Thu, 23 Mar 2023 06:39:01 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:5077868044732549104a37735bbeb9eeea04990428ec84565089b9f912a27b4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72700174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b721a7424bef3c917f99584f6ede9bdd469bf8bf89ca3187bf5fd2fa3f563f5c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:10 GMT
ADD file:83beb883b699cd442f1dbd4baf29c23f4cd15f7a5f9f120979df16a77455c69f in / 
# Thu, 23 Mar 2023 00:45:10 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:22:40 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 07:22:40 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Thu, 23 Mar 2023 07:22:40 GMT
ENV EMQX_VERSION=4.4.16
# Thu, 23 Mar 2023 07:22:40 GMT
ENV OTP=otp24.3.4.2-1
# Thu, 23 Mar 2023 07:22:44 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="901b76ea2bee68729b75280740ca31b1af5b358d331422d1653dc342ee830324"; fi;     if [ ${arch} = "arm64" ]; then sha256="1224f53d0ee98390c286f3bbd9af2f294c2fa4ccb79342343d803fa234165c6e"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Thu, 23 Mar 2023 07:22:44 GMT
WORKDIR /opt/emqx
# Thu, 23 Mar 2023 07:22:44 GMT
USER emqx
# Thu, 23 Mar 2023 07:22:45 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 23 Mar 2023 07:22:45 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Thu, 23 Mar 2023 07:22:45 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Thu, 23 Mar 2023 07:22:45 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 23 Mar 2023 07:22:45 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:fcdb9667c46b09d1c1d058681ea4a1db41e66bbc1a71d873a0c9da4f7a92947d`  
		Last Modified: Thu, 23 Mar 2023 00:48:09 GMT  
		Size: 30.1 MB (30062700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a2fca160acd6916ee9f7a44af39ca048ec3dba62c3d8276915f397320d937d`  
		Last Modified: Thu, 23 Mar 2023 07:23:07 GMT  
		Size: 2.6 MB (2559254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602fe4683989e6650cbe1071564b8e4029b4eacf0814ee226b81bfa86c6df9fe`  
		Last Modified: Thu, 23 Mar 2023 07:23:07 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4d7f2460db59baf21229445904a5c93abb98a720847d234328af163a73069b`  
		Last Modified: Thu, 23 Mar 2023 07:23:10 GMT  
		Size: 40.1 MB (40073001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b619deebd0c236156f78632f97bd2738a18a1a8edf1e4cabdeb0d403c57810db`  
		Last Modified: Thu, 23 Mar 2023 07:23:07 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4.16`

```console
$ docker pull emqx@sha256:d0c7a636891e44bfdc8c66697fec9b5cb94675210cb090cffd732a6219ab5284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.4.16` - linux; amd64

```console
$ docker pull emqx@sha256:b594671f1c8c001b76971e896ec29f4aea1b4ce35e471f418b7e190d66bdfe8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81272225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df18f1b36fce0936fd74b9faf314e3a01d83c037091286efb92131b581fe822`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:38:29 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 06:38:30 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Thu, 23 Mar 2023 06:38:30 GMT
ENV EMQX_VERSION=4.4.16
# Thu, 23 Mar 2023 06:38:30 GMT
ENV OTP=otp24.3.4.2-1
# Thu, 23 Mar 2023 06:38:34 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="901b76ea2bee68729b75280740ca31b1af5b358d331422d1653dc342ee830324"; fi;     if [ ${arch} = "arm64" ]; then sha256="1224f53d0ee98390c286f3bbd9af2f294c2fa4ccb79342343d803fa234165c6e"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Thu, 23 Mar 2023 06:38:34 GMT
WORKDIR /opt/emqx
# Thu, 23 Mar 2023 06:38:35 GMT
USER emqx
# Thu, 23 Mar 2023 06:38:35 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 23 Mar 2023 06:38:35 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Thu, 23 Mar 2023 06:38:35 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Thu, 23 Mar 2023 06:38:35 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 23 Mar 2023 06:38:35 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7216294cbe2d1311e293a82d22eb3f71da435b2b9bb7ad9900eaaeb14d68d2b7`  
		Last Modified: Thu, 23 Mar 2023 06:39:01 GMT  
		Size: 2.6 MB (2569460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca85a7d40cdb8392bb213cc3b9efc98bcb416df588c86b55eb174485340016cb`  
		Last Modified: Thu, 23 Mar 2023 06:39:01 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93644246d8ba201ec9c154bf77410efda76bbc02af25c4d8c89b5bef6aa7e90e`  
		Last Modified: Thu, 23 Mar 2023 06:39:05 GMT  
		Size: 47.3 MB (47286145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1172e73e519b49b8ecabc31cf1807694cf854572647611963d00191e5c03612`  
		Last Modified: Thu, 23 Mar 2023 06:39:01 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.4.16` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:5077868044732549104a37735bbeb9eeea04990428ec84565089b9f912a27b4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72700174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b721a7424bef3c917f99584f6ede9bdd469bf8bf89ca3187bf5fd2fa3f563f5c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:10 GMT
ADD file:83beb883b699cd442f1dbd4baf29c23f4cd15f7a5f9f120979df16a77455c69f in / 
# Thu, 23 Mar 2023 00:45:10 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:22:40 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 07:22:40 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Thu, 23 Mar 2023 07:22:40 GMT
ENV EMQX_VERSION=4.4.16
# Thu, 23 Mar 2023 07:22:40 GMT
ENV OTP=otp24.3.4.2-1
# Thu, 23 Mar 2023 07:22:44 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="901b76ea2bee68729b75280740ca31b1af5b358d331422d1653dc342ee830324"; fi;     if [ ${arch} = "arm64" ]; then sha256="1224f53d0ee98390c286f3bbd9af2f294c2fa4ccb79342343d803fa234165c6e"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Thu, 23 Mar 2023 07:22:44 GMT
WORKDIR /opt/emqx
# Thu, 23 Mar 2023 07:22:44 GMT
USER emqx
# Thu, 23 Mar 2023 07:22:45 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 23 Mar 2023 07:22:45 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Thu, 23 Mar 2023 07:22:45 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Thu, 23 Mar 2023 07:22:45 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 23 Mar 2023 07:22:45 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:fcdb9667c46b09d1c1d058681ea4a1db41e66bbc1a71d873a0c9da4f7a92947d`  
		Last Modified: Thu, 23 Mar 2023 00:48:09 GMT  
		Size: 30.1 MB (30062700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a2fca160acd6916ee9f7a44af39ca048ec3dba62c3d8276915f397320d937d`  
		Last Modified: Thu, 23 Mar 2023 07:23:07 GMT  
		Size: 2.6 MB (2559254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602fe4683989e6650cbe1071564b8e4029b4eacf0814ee226b81bfa86c6df9fe`  
		Last Modified: Thu, 23 Mar 2023 07:23:07 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4d7f2460db59baf21229445904a5c93abb98a720847d234328af163a73069b`  
		Last Modified: Thu, 23 Mar 2023 07:23:10 GMT  
		Size: 40.1 MB (40073001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b619deebd0c236156f78632f97bd2738a18a1a8edf1e4cabdeb0d403c57810db`  
		Last Modified: Thu, 23 Mar 2023 07:23:07 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5`

```console
$ docker pull emqx@sha256:bae07926c41a1dd0c66da83b063b250ad12b81aa4831c368db92d91101a2872a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:08c3ebcadd877cb22ba78856515f212dc8cb0091a2127bbd19efd4924f9dc2fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101404984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc1b082e4efacb30a112147dba1345c209014dbf83830316a72b478eeca38b8`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:38:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 06:38:44 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Mon, 27 Mar 2023 18:19:36 GMT
ENV EMQX_VERSION=5.0.21
# Mon, 27 Mar 2023 18:19:36 GMT
ENV AMD64_SHA256=d83d435bfd49fc06cf9448de12ee76d383f9919fbb4d149545ccc246c903b78e
# Mon, 27 Mar 2023 18:19:36 GMT
ENV ARM64_SHA256=29dc8a470c9d43069dbc0f640e9493a991516fa18e028930726e8a6c7e60afc6
# Mon, 27 Mar 2023 18:19:36 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 27 Mar 2023 18:19:42 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Mon, 27 Mar 2023 18:19:42 GMT
WORKDIR /opt/emqx
# Mon, 27 Mar 2023 18:19:42 GMT
USER emqx
# Mon, 27 Mar 2023 18:19:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 27 Mar 2023 18:19:42 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Mon, 27 Mar 2023 18:19:42 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Mon, 27 Mar 2023 18:19:42 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 27 Mar 2023 18:19:42 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad234a8e621d243ffc2889b413a9971003cc42ee7ba32a7ac16473122c6d6364`  
		Last Modified: Thu, 23 Mar 2023 06:39:16 GMT  
		Size: 3.0 MB (2987658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e02c887fbcfd1b399b200e621a473094afcaf8febe6e035caf150ebf9136c32`  
		Last Modified: Thu, 23 Mar 2023 06:39:15 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7488720fedff88d9c3050fc5c1c7eace8812e01a550d5f94e7321631d3edc999`  
		Last Modified: Mon, 27 Mar 2023 18:20:03 GMT  
		Size: 67.0 MB (67000911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6e93be2743506e4b3bfb33dffdfc9915d527ee6e6e5cd45bca119503e078be`  
		Last Modified: Mon, 27 Mar 2023 18:19:55 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:7671cd62ab056dba332416f95e7c720de953fdc6a54941ac9f9d3b0ba8a1d026
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92497974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad0c2a0224f67caf0201ab8f98e72acd6792b402e07ffc7636d046fec29fc99`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:10 GMT
ADD file:83beb883b699cd442f1dbd4baf29c23f4cd15f7a5f9f120979df16a77455c69f in / 
# Thu, 23 Mar 2023 00:45:10 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:22:51 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 07:22:52 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Mon, 27 Mar 2023 18:39:26 GMT
ENV EMQX_VERSION=5.0.21
# Mon, 27 Mar 2023 18:39:26 GMT
ENV AMD64_SHA256=d83d435bfd49fc06cf9448de12ee76d383f9919fbb4d149545ccc246c903b78e
# Mon, 27 Mar 2023 18:39:26 GMT
ENV ARM64_SHA256=29dc8a470c9d43069dbc0f640e9493a991516fa18e028930726e8a6c7e60afc6
# Mon, 27 Mar 2023 18:39:26 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 27 Mar 2023 18:39:32 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Mon, 27 Mar 2023 18:39:32 GMT
WORKDIR /opt/emqx
# Mon, 27 Mar 2023 18:39:32 GMT
USER emqx
# Mon, 27 Mar 2023 18:39:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 27 Mar 2023 18:39:32 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Mon, 27 Mar 2023 18:39:33 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Mon, 27 Mar 2023 18:39:33 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 27 Mar 2023 18:39:33 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:fcdb9667c46b09d1c1d058681ea4a1db41e66bbc1a71d873a0c9da4f7a92947d`  
		Last Modified: Thu, 23 Mar 2023 00:48:09 GMT  
		Size: 30.1 MB (30062700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e32acc0199b24e0cbce1256b7b9514920ac6dedaed2a2ee404a0957d036012bc`  
		Last Modified: Thu, 23 Mar 2023 07:23:22 GMT  
		Size: 3.0 MB (3002755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a325419b9b6ebe9519e9bc7472f523d98e68e6d85caf8a71f9faca4312e840`  
		Last Modified: Thu, 23 Mar 2023 07:23:22 GMT  
		Size: 4.1 KB (4112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c49cef7f4e6ffd2282ec337c80569467f5de5a3c7c2b1ffd0f08d417bd3d9c`  
		Last Modified: Mon, 27 Mar 2023 18:39:48 GMT  
		Size: 59.4 MB (59427505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29cf7f61f4a88bc9f8e7ffa790fb4ed0fe9a7c10d791de441ef057ee2205e87f`  
		Last Modified: Mon, 27 Mar 2023 18:39:42 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.0`

```console
$ docker pull emqx@sha256:bae07926c41a1dd0c66da83b063b250ad12b81aa4831c368db92d91101a2872a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.0` - linux; amd64

```console
$ docker pull emqx@sha256:08c3ebcadd877cb22ba78856515f212dc8cb0091a2127bbd19efd4924f9dc2fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101404984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc1b082e4efacb30a112147dba1345c209014dbf83830316a72b478eeca38b8`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:38:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 06:38:44 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Mon, 27 Mar 2023 18:19:36 GMT
ENV EMQX_VERSION=5.0.21
# Mon, 27 Mar 2023 18:19:36 GMT
ENV AMD64_SHA256=d83d435bfd49fc06cf9448de12ee76d383f9919fbb4d149545ccc246c903b78e
# Mon, 27 Mar 2023 18:19:36 GMT
ENV ARM64_SHA256=29dc8a470c9d43069dbc0f640e9493a991516fa18e028930726e8a6c7e60afc6
# Mon, 27 Mar 2023 18:19:36 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 27 Mar 2023 18:19:42 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Mon, 27 Mar 2023 18:19:42 GMT
WORKDIR /opt/emqx
# Mon, 27 Mar 2023 18:19:42 GMT
USER emqx
# Mon, 27 Mar 2023 18:19:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 27 Mar 2023 18:19:42 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Mon, 27 Mar 2023 18:19:42 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Mon, 27 Mar 2023 18:19:42 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 27 Mar 2023 18:19:42 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad234a8e621d243ffc2889b413a9971003cc42ee7ba32a7ac16473122c6d6364`  
		Last Modified: Thu, 23 Mar 2023 06:39:16 GMT  
		Size: 3.0 MB (2987658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e02c887fbcfd1b399b200e621a473094afcaf8febe6e035caf150ebf9136c32`  
		Last Modified: Thu, 23 Mar 2023 06:39:15 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7488720fedff88d9c3050fc5c1c7eace8812e01a550d5f94e7321631d3edc999`  
		Last Modified: Mon, 27 Mar 2023 18:20:03 GMT  
		Size: 67.0 MB (67000911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6e93be2743506e4b3bfb33dffdfc9915d527ee6e6e5cd45bca119503e078be`  
		Last Modified: Mon, 27 Mar 2023 18:19:55 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.0` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:7671cd62ab056dba332416f95e7c720de953fdc6a54941ac9f9d3b0ba8a1d026
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92497974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad0c2a0224f67caf0201ab8f98e72acd6792b402e07ffc7636d046fec29fc99`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:10 GMT
ADD file:83beb883b699cd442f1dbd4baf29c23f4cd15f7a5f9f120979df16a77455c69f in / 
# Thu, 23 Mar 2023 00:45:10 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:22:51 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 07:22:52 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Mon, 27 Mar 2023 18:39:26 GMT
ENV EMQX_VERSION=5.0.21
# Mon, 27 Mar 2023 18:39:26 GMT
ENV AMD64_SHA256=d83d435bfd49fc06cf9448de12ee76d383f9919fbb4d149545ccc246c903b78e
# Mon, 27 Mar 2023 18:39:26 GMT
ENV ARM64_SHA256=29dc8a470c9d43069dbc0f640e9493a991516fa18e028930726e8a6c7e60afc6
# Mon, 27 Mar 2023 18:39:26 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 27 Mar 2023 18:39:32 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Mon, 27 Mar 2023 18:39:32 GMT
WORKDIR /opt/emqx
# Mon, 27 Mar 2023 18:39:32 GMT
USER emqx
# Mon, 27 Mar 2023 18:39:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 27 Mar 2023 18:39:32 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Mon, 27 Mar 2023 18:39:33 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Mon, 27 Mar 2023 18:39:33 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 27 Mar 2023 18:39:33 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:fcdb9667c46b09d1c1d058681ea4a1db41e66bbc1a71d873a0c9da4f7a92947d`  
		Last Modified: Thu, 23 Mar 2023 00:48:09 GMT  
		Size: 30.1 MB (30062700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e32acc0199b24e0cbce1256b7b9514920ac6dedaed2a2ee404a0957d036012bc`  
		Last Modified: Thu, 23 Mar 2023 07:23:22 GMT  
		Size: 3.0 MB (3002755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a325419b9b6ebe9519e9bc7472f523d98e68e6d85caf8a71f9faca4312e840`  
		Last Modified: Thu, 23 Mar 2023 07:23:22 GMT  
		Size: 4.1 KB (4112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c49cef7f4e6ffd2282ec337c80569467f5de5a3c7c2b1ffd0f08d417bd3d9c`  
		Last Modified: Mon, 27 Mar 2023 18:39:48 GMT  
		Size: 59.4 MB (59427505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29cf7f61f4a88bc9f8e7ffa790fb4ed0fe9a7c10d791de441ef057ee2205e87f`  
		Last Modified: Mon, 27 Mar 2023 18:39:42 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.0.21`

```console
$ docker pull emqx@sha256:bae07926c41a1dd0c66da83b063b250ad12b81aa4831c368db92d91101a2872a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.0.21` - linux; amd64

```console
$ docker pull emqx@sha256:08c3ebcadd877cb22ba78856515f212dc8cb0091a2127bbd19efd4924f9dc2fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101404984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc1b082e4efacb30a112147dba1345c209014dbf83830316a72b478eeca38b8`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:38:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 06:38:44 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Mon, 27 Mar 2023 18:19:36 GMT
ENV EMQX_VERSION=5.0.21
# Mon, 27 Mar 2023 18:19:36 GMT
ENV AMD64_SHA256=d83d435bfd49fc06cf9448de12ee76d383f9919fbb4d149545ccc246c903b78e
# Mon, 27 Mar 2023 18:19:36 GMT
ENV ARM64_SHA256=29dc8a470c9d43069dbc0f640e9493a991516fa18e028930726e8a6c7e60afc6
# Mon, 27 Mar 2023 18:19:36 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 27 Mar 2023 18:19:42 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Mon, 27 Mar 2023 18:19:42 GMT
WORKDIR /opt/emqx
# Mon, 27 Mar 2023 18:19:42 GMT
USER emqx
# Mon, 27 Mar 2023 18:19:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 27 Mar 2023 18:19:42 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Mon, 27 Mar 2023 18:19:42 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Mon, 27 Mar 2023 18:19:42 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 27 Mar 2023 18:19:42 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad234a8e621d243ffc2889b413a9971003cc42ee7ba32a7ac16473122c6d6364`  
		Last Modified: Thu, 23 Mar 2023 06:39:16 GMT  
		Size: 3.0 MB (2987658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e02c887fbcfd1b399b200e621a473094afcaf8febe6e035caf150ebf9136c32`  
		Last Modified: Thu, 23 Mar 2023 06:39:15 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7488720fedff88d9c3050fc5c1c7eace8812e01a550d5f94e7321631d3edc999`  
		Last Modified: Mon, 27 Mar 2023 18:20:03 GMT  
		Size: 67.0 MB (67000911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6e93be2743506e4b3bfb33dffdfc9915d527ee6e6e5cd45bca119503e078be`  
		Last Modified: Mon, 27 Mar 2023 18:19:55 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.0.21` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:7671cd62ab056dba332416f95e7c720de953fdc6a54941ac9f9d3b0ba8a1d026
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92497974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad0c2a0224f67caf0201ab8f98e72acd6792b402e07ffc7636d046fec29fc99`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:10 GMT
ADD file:83beb883b699cd442f1dbd4baf29c23f4cd15f7a5f9f120979df16a77455c69f in / 
# Thu, 23 Mar 2023 00:45:10 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:22:51 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 07:22:52 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Mon, 27 Mar 2023 18:39:26 GMT
ENV EMQX_VERSION=5.0.21
# Mon, 27 Mar 2023 18:39:26 GMT
ENV AMD64_SHA256=d83d435bfd49fc06cf9448de12ee76d383f9919fbb4d149545ccc246c903b78e
# Mon, 27 Mar 2023 18:39:26 GMT
ENV ARM64_SHA256=29dc8a470c9d43069dbc0f640e9493a991516fa18e028930726e8a6c7e60afc6
# Mon, 27 Mar 2023 18:39:26 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 27 Mar 2023 18:39:32 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Mon, 27 Mar 2023 18:39:32 GMT
WORKDIR /opt/emqx
# Mon, 27 Mar 2023 18:39:32 GMT
USER emqx
# Mon, 27 Mar 2023 18:39:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 27 Mar 2023 18:39:32 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Mon, 27 Mar 2023 18:39:33 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Mon, 27 Mar 2023 18:39:33 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 27 Mar 2023 18:39:33 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:fcdb9667c46b09d1c1d058681ea4a1db41e66bbc1a71d873a0c9da4f7a92947d`  
		Last Modified: Thu, 23 Mar 2023 00:48:09 GMT  
		Size: 30.1 MB (30062700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e32acc0199b24e0cbce1256b7b9514920ac6dedaed2a2ee404a0957d036012bc`  
		Last Modified: Thu, 23 Mar 2023 07:23:22 GMT  
		Size: 3.0 MB (3002755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a325419b9b6ebe9519e9bc7472f523d98e68e6d85caf8a71f9faca4312e840`  
		Last Modified: Thu, 23 Mar 2023 07:23:22 GMT  
		Size: 4.1 KB (4112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c49cef7f4e6ffd2282ec337c80569467f5de5a3c7c2b1ffd0f08d417bd3d9c`  
		Last Modified: Mon, 27 Mar 2023 18:39:48 GMT  
		Size: 59.4 MB (59427505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29cf7f61f4a88bc9f8e7ffa790fb4ed0fe9a7c10d791de441ef057ee2205e87f`  
		Last Modified: Mon, 27 Mar 2023 18:39:42 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:latest`

```console
$ docker pull emqx@sha256:bae07926c41a1dd0c66da83b063b250ad12b81aa4831c368db92d91101a2872a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:08c3ebcadd877cb22ba78856515f212dc8cb0091a2127bbd19efd4924f9dc2fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101404984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc1b082e4efacb30a112147dba1345c209014dbf83830316a72b478eeca38b8`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:38:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 06:38:44 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Mon, 27 Mar 2023 18:19:36 GMT
ENV EMQX_VERSION=5.0.21
# Mon, 27 Mar 2023 18:19:36 GMT
ENV AMD64_SHA256=d83d435bfd49fc06cf9448de12ee76d383f9919fbb4d149545ccc246c903b78e
# Mon, 27 Mar 2023 18:19:36 GMT
ENV ARM64_SHA256=29dc8a470c9d43069dbc0f640e9493a991516fa18e028930726e8a6c7e60afc6
# Mon, 27 Mar 2023 18:19:36 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 27 Mar 2023 18:19:42 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Mon, 27 Mar 2023 18:19:42 GMT
WORKDIR /opt/emqx
# Mon, 27 Mar 2023 18:19:42 GMT
USER emqx
# Mon, 27 Mar 2023 18:19:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 27 Mar 2023 18:19:42 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Mon, 27 Mar 2023 18:19:42 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Mon, 27 Mar 2023 18:19:42 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 27 Mar 2023 18:19:42 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad234a8e621d243ffc2889b413a9971003cc42ee7ba32a7ac16473122c6d6364`  
		Last Modified: Thu, 23 Mar 2023 06:39:16 GMT  
		Size: 3.0 MB (2987658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e02c887fbcfd1b399b200e621a473094afcaf8febe6e035caf150ebf9136c32`  
		Last Modified: Thu, 23 Mar 2023 06:39:15 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7488720fedff88d9c3050fc5c1c7eace8812e01a550d5f94e7321631d3edc999`  
		Last Modified: Mon, 27 Mar 2023 18:20:03 GMT  
		Size: 67.0 MB (67000911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6e93be2743506e4b3bfb33dffdfc9915d527ee6e6e5cd45bca119503e078be`  
		Last Modified: Mon, 27 Mar 2023 18:19:55 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:7671cd62ab056dba332416f95e7c720de953fdc6a54941ac9f9d3b0ba8a1d026
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92497974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad0c2a0224f67caf0201ab8f98e72acd6792b402e07ffc7636d046fec29fc99`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:10 GMT
ADD file:83beb883b699cd442f1dbd4baf29c23f4cd15f7a5f9f120979df16a77455c69f in / 
# Thu, 23 Mar 2023 00:45:10 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:22:51 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 07:22:52 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Mon, 27 Mar 2023 18:39:26 GMT
ENV EMQX_VERSION=5.0.21
# Mon, 27 Mar 2023 18:39:26 GMT
ENV AMD64_SHA256=d83d435bfd49fc06cf9448de12ee76d383f9919fbb4d149545ccc246c903b78e
# Mon, 27 Mar 2023 18:39:26 GMT
ENV ARM64_SHA256=29dc8a470c9d43069dbc0f640e9493a991516fa18e028930726e8a6c7e60afc6
# Mon, 27 Mar 2023 18:39:26 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 27 Mar 2023 18:39:32 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Mon, 27 Mar 2023 18:39:32 GMT
WORKDIR /opt/emqx
# Mon, 27 Mar 2023 18:39:32 GMT
USER emqx
# Mon, 27 Mar 2023 18:39:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 27 Mar 2023 18:39:32 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Mon, 27 Mar 2023 18:39:33 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Mon, 27 Mar 2023 18:39:33 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 27 Mar 2023 18:39:33 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:fcdb9667c46b09d1c1d058681ea4a1db41e66bbc1a71d873a0c9da4f7a92947d`  
		Last Modified: Thu, 23 Mar 2023 00:48:09 GMT  
		Size: 30.1 MB (30062700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e32acc0199b24e0cbce1256b7b9514920ac6dedaed2a2ee404a0957d036012bc`  
		Last Modified: Thu, 23 Mar 2023 07:23:22 GMT  
		Size: 3.0 MB (3002755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a325419b9b6ebe9519e9bc7472f523d98e68e6d85caf8a71f9faca4312e840`  
		Last Modified: Thu, 23 Mar 2023 07:23:22 GMT  
		Size: 4.1 KB (4112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c49cef7f4e6ffd2282ec337c80569467f5de5a3c7c2b1ffd0f08d417bd3d9c`  
		Last Modified: Mon, 27 Mar 2023 18:39:48 GMT  
		Size: 59.4 MB (59427505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29cf7f61f4a88bc9f8e7ffa790fb4ed0fe9a7c10d791de441ef057ee2205e87f`  
		Last Modified: Mon, 27 Mar 2023 18:39:42 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
