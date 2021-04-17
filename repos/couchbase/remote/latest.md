## `couchbase:latest`

```console
$ docker pull couchbase@sha256:21ee325b15534b7b64c93ce9f4f1dbdcc3e4508b626046a9b3af13439dbd323e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:latest` - linux; amd64

```console
$ docker pull couchbase@sha256:e3e12663a9c5407a6a5a41b1be6f51d34519f3f8b6028f3044b7f5ef06d35ce8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.6 MB (549640673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d71133afbb312869005649d2e66cb2eb94890f8adeeb180ddcc4ab93c9831a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:52 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 25 Mar 2021 22:33:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:54 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 25 Mar 2021 22:33:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:55 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 10:21:26 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Fri, 26 Mar 2021 10:21:52 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 26 Mar 2021 10:21:53 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Fri, 16 Apr 2021 21:22:31 GMT
ARG CB_VERSION=6.6.2
# Fri, 16 Apr 2021 21:22:31 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2
# Fri, 16 Apr 2021 21:22:31 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb
# Fri, 16 Apr 2021 21:22:31 GMT
ARG CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901
# Fri, 16 Apr 2021 21:22:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 16 Apr 2021 21:22:33 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901 CB_VERSION=6.6.2
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 16 Apr 2021 21:23:16 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901 CB_VERSION=6.6.2
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Fri, 16 Apr 2021 21:23:20 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901 CB_VERSION=6.6.2
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 16 Apr 2021 21:23:21 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 16 Apr 2021 21:23:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901 CB_VERSION=6.6.2
RUN chown -R couchbase:couchbase /etc/service
# Fri, 16 Apr 2021 21:23:22 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 16 Apr 2021 21:23:23 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901 CB_VERSION=6.6.2
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 16 Apr 2021 21:23:24 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901 CB_VERSION=6.6.2
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 16 Apr 2021 21:23:24 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 16 Apr 2021 21:23:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Apr 2021 21:23:24 GMT
CMD ["couchbase-server"]
# Fri, 16 Apr 2021 21:23:24 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 16 Apr 2021 21:23:24 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1de0f9cdfc1f9f595acd2ea8724ea92a509d64a6936f0e645c65b504e7e4bc6`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee6ca703b866ac2b74b6129d2db331936292f899e8e3a794474fdf81343605`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39e2761d3d4971e78914857af4c6bd9989873b53426cf2fef3e76983b166fa2`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9325ab665c8be8e5ece555680f3b6c687043d93890fcc988a71846a0d0a23afd`  
		Last Modified: Fri, 26 Mar 2021 10:28:08 GMT  
		Size: 5.8 MB (5834025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7abcf66ff05add3d148151e2ae63c331b6541d78dc6b7cd24ca373224752e2a1`  
		Last Modified: Fri, 16 Apr 2021 21:23:56 GMT  
		Size: 2.1 KB (2079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebe838941d4a6ad12ff03131657f6de49c24af06b33ffc93241cb09b972d1326`  
		Last Modified: Fri, 16 Apr 2021 21:24:48 GMT  
		Size: 497.7 MB (497720259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f022646853e41ce158f96769237ed31e5db89cbb203865cc38a72f8477837454`  
		Last Modified: Fri, 16 Apr 2021 21:23:56 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05645457d8af33d284fe21d13d389c2860773512522b55363275c1f321e5329`  
		Last Modified: Fri, 16 Apr 2021 21:23:55 GMT  
		Size: 433.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe73e613ae88192fb93331527a4d2aabc2e2943fb678cd6648008f4ea036a9b9`  
		Last Modified: Fri, 16 Apr 2021 21:23:54 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1eb311f673c586da0a9027362a83337bc2aa0ffe97f964e6ca9b375bd4e596b`  
		Last Modified: Fri, 16 Apr 2021 21:23:53 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ca42c7882a8422cd13500fccac2bd6e24628d970dfde5c402df310b59b24b8`  
		Last Modified: Fri, 16 Apr 2021 21:23:52 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159da761c1ead54326fe30fbf0297e8e184060f1d757ac9a4300e4a0b946e29b`  
		Last Modified: Fri, 16 Apr 2021 21:23:52 GMT  
		Size: 118.1 KB (118072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47425dd40311e4bb8d5dc6a9a2a591388edc6c65fdd53dafd850e8315436f99c`  
		Last Modified: Fri, 16 Apr 2021 21:23:52 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
