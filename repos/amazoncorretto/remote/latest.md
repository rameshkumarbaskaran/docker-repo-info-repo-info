## `amazoncorretto:latest`

```console
$ docker pull amazoncorretto@sha256:fa6ef84992f7b7c363043ce994e0cdfc7be319c5ed27b3a5d6495995daa2d977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:latest` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f855bfef99645840f48dc0bdc1a84417bde006e6eaf2c8346ba933668417ad05
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.1 MB (183099536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d5e55b2b7d507b8e522ac1c0b1a312b4fcd52f53e5550e9beba6ddf99ec090`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2020 00:19:43 GMT
ADD file:21f17d9ead4aa13446f2144c5042f6f83bc7dc26163bdc2ea6de306b67154747 in / 
# Fri, 10 Jan 2020 00:19:44 GMT
CMD ["/bin/bash"]
# Fri, 10 Jan 2020 00:40:30 GMT
ARG rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_232.b09-1.x86_64.rpm
# Fri, 10 Jan 2020 00:40:31 GMT
ARG path_x64=https://d3pxv6yz143wms.cloudfront.net/8.232.09.1
# Fri, 10 Jan 2020 00:40:31 GMT
ARG key_x64=E8EB406377AD2B9E9A4765D19CB3BC6FF6C9FC19
# Fri, 10 Jan 2020 00:40:31 GMT
ARG rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_232.b09-1.aarch64.rpm
# Fri, 10 Jan 2020 00:40:31 GMT
ARG path_aarch64=https://d3pxv6yz143wms.cloudfront.net/8.232.09.1
# Fri, 10 Jan 2020 00:40:31 GMT
ARG key_aarch64=E8EB406377AD2B9E9A4765D19CB3BC6FF6C9FC19
# Fri, 10 Jan 2020 00:40:52 GMT
# ARGS: key_aarch64=E8EB406377AD2B9E9A4765D19CB3BC6FF6C9FC19 key_x64=E8EB406377AD2B9E9A4765D19CB3BC6FF6C9FC19 path_aarch64=https://d3pxv6yz143wms.cloudfront.net/8.232.09.1 path_x64=https://d3pxv6yz143wms.cloudfront.net/8.232.09.1 rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_232.b09-1.aarch64.rpm rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_232.b09-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Fri, 10 Jan 2020 00:40:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:67e0556e0c29917bdaa234432962153167e628b99444a27333976b499590d8c9`  
		Last Modified: Fri, 10 Jan 2020 00:20:43 GMT  
		Size: 61.6 MB (61552853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958dc053a014ea0286ce7c210872de2b8f6cbc490e81f49bc5341ca50cae3d57`  
		Last Modified: Fri, 10 Jan 2020 00:41:57 GMT  
		Size: 121.5 MB (121546683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:latest` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0c14f445e1c65ba8eafd8cc67f2e88de3ec57575e64b3d20d9d31e8c26902dab
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167773049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc6d6784499f1e52945355886712e36c0f369dae5da98bb26a66bfa5d9acc02`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Jan 2020 23:45:53 GMT
ADD file:add3cf2f51e227816df93be763f4c623b743cf37786e5c11118149dbfaa4ad67 in / 
# Thu, 09 Jan 2020 23:45:57 GMT
CMD ["/bin/bash"]
# Fri, 10 Jan 2020 00:24:21 GMT
ARG rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_232.b09-1.x86_64.rpm
# Fri, 10 Jan 2020 00:24:22 GMT
ARG path_x64=https://d3pxv6yz143wms.cloudfront.net/8.232.09.1
# Fri, 10 Jan 2020 00:24:22 GMT
ARG key_x64=E8EB406377AD2B9E9A4765D19CB3BC6FF6C9FC19
# Fri, 10 Jan 2020 00:24:23 GMT
ARG rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_232.b09-1.aarch64.rpm
# Fri, 10 Jan 2020 00:24:24 GMT
ARG path_aarch64=https://d3pxv6yz143wms.cloudfront.net/8.232.09.1
# Fri, 10 Jan 2020 00:24:24 GMT
ARG key_aarch64=E8EB406377AD2B9E9A4765D19CB3BC6FF6C9FC19
# Fri, 10 Jan 2020 00:24:51 GMT
# ARGS: key_aarch64=E8EB406377AD2B9E9A4765D19CB3BC6FF6C9FC19 key_x64=E8EB406377AD2B9E9A4765D19CB3BC6FF6C9FC19 path_aarch64=https://d3pxv6yz143wms.cloudfront.net/8.232.09.1 path_x64=https://d3pxv6yz143wms.cloudfront.net/8.232.09.1 rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_232.b09-1.aarch64.rpm rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_232.b09-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Fri, 10 Jan 2020 00:24:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:9606ab06f949f5879fcb558b6c4a487afd285954e409f8741df95b27c6e0c5b2`  
		Last Modified: Thu, 09 Jan 2020 23:46:50 GMT  
		Size: 62.8 MB (62796733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a50eae34777174875c769f2ad6ed222cb5a02e9fec1225e68789601b180f8ff`  
		Last Modified: Fri, 10 Jan 2020 00:28:01 GMT  
		Size: 105.0 MB (104976316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
