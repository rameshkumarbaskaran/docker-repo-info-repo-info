## `couchbase:latest`

```console
$ docker pull couchbase@sha256:88db0ccb60ac5d6ec29164dab749c4c696ac534be7743a66b57d5a3878ee33c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:latest` - linux; amd64

```console
$ docker pull couchbase@sha256:27442f3b0200d77b37168f5687f30e2a999947ef0a5db598c4750e97fb92e3d2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.3 MB (600285393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ec1dd33ec9082d8c2d7e9a150579b5193c1f6d18df628b4decf3bec9209055`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 01 Feb 2023 11:42:37 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:42:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:42:39 GMT
ADD file:8b180a9b4497de0c6e131d6b48cf5c69a885379e63033ab9639d1655991e626c in / 
# Wed, 01 Feb 2023 11:42:39 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 18:25:04 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 01 Feb 2023 18:25:04 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 01 Feb 2023 18:25:04 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 01 Feb 2023 18:25:27 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Wed, 01 Feb 2023 18:25:28 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.3
# Wed, 01 Feb 2023 18:25:28 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.1.3-linux_@@ARCH@@.deb
# Wed, 01 Feb 2023 18:25:28 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 01 Feb 2023 18:25:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 01 Feb 2023 18:25:29 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 01 Feb 2023 18:26:26 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=bdc1ffbd5a0eca07a554856a92eb0b5930b457c1d13fca9a2a93ef91a5d88156            ;;          'amd64')            CB_SHA256=bd8c808771cb46e563c173f60e0723c32351a6453f6ece2d4fa440e0d2dcdfd3            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Wed, 01 Feb 2023 18:26:31 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 01 Feb 2023 18:26:31 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Wed, 01 Feb 2023 18:26:31 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Wed, 01 Feb 2023 18:26:31 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 01 Feb 2023 18:26:32 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 01 Feb 2023 18:26:33 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Wed, 01 Feb 2023 18:26:33 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Wed, 01 Feb 2023 18:26:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Feb 2023 18:26:33 GMT
CMD ["couchbase-server"]
# Wed, 01 Feb 2023 18:26:33 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Wed, 01 Feb 2023 18:26:33 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:7608715873ec5c02d370e963aa9b19a149023ce218887221d93fe671b3abbf58`  
		Last Modified: Thu, 26 Jan 2023 17:04:53 GMT  
		Size: 28.6 MB (28577884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b4cf586c4b7a57fc5e73b3aa283d12081f9bd7606b6b60d897f2783e6efa0d`  
		Last Modified: Wed, 01 Feb 2023 18:31:06 GMT  
		Size: 6.2 MB (6216449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2820c7121f0a09d4a6b11881f09b95cacc3cbebc82f73aff1f996202193ce0`  
		Last Modified: Wed, 01 Feb 2023 18:31:05 GMT  
		Size: 1.8 KB (1831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5db5dca17b86b88c0c7cf2b23d43c1ed0561f66106e0b0a955667da1dc1401`  
		Last Modified: Wed, 01 Feb 2023 18:32:01 GMT  
		Size: 565.5 MB (565486707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d11bb0b33cc4ea595033a41004eeea233f267374a44a5dc97bd226bcb64e0d8`  
		Last Modified: Wed, 01 Feb 2023 18:31:05 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a801c20d9d04c9fffd9c9584e4383bf75463ec98280eb032175223dfb87f1980`  
		Last Modified: Wed, 01 Feb 2023 18:31:03 GMT  
		Size: 739.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2988e82038abb9d711b27510974291e14223e2834c95c920ce5938a6e7a2c2c`  
		Last Modified: Wed, 01 Feb 2023 18:31:03 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35420a0cd22388f3cc77425bfc3f5d128433747095ebac6d391c01742be295c`  
		Last Modified: Wed, 01 Feb 2023 18:31:03 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9bea392911ee85dcff4c4d9224495188208fa48c7c4022a52c08b7788dad184`  
		Last Modified: Wed, 01 Feb 2023 18:31:03 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe9dae4957e5be3f0645755f477cb900b50908d1d7587c4ff46ab294f41d8e4`  
		Last Modified: Wed, 01 Feb 2023 18:31:03 GMT  
		Size: 866.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:latest` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:c333865404800137a086cdcd45d489e3b6d760caa39013259c9738cb5bdbddfd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.4 MB (574398490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b58bad804f0017c75f6305262c411945ceb7551ebba40c4cba08b86313c3e7a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 02:39:57 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 02 Mar 2023 02:39:57 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 02 Mar 2023 02:39:57 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 02 Mar 2023 02:40:16 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Thu, 02 Mar 2023 02:40:17 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.3
# Thu, 02 Mar 2023 02:40:17 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.1.3-linux_@@ARCH@@.deb
# Thu, 02 Mar 2023 02:40:17 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 02 Mar 2023 02:40:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 02 Mar 2023 02:40:17 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 02 Mar 2023 02:41:07 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=bdc1ffbd5a0eca07a554856a92eb0b5930b457c1d13fca9a2a93ef91a5d88156            ;;          'amd64')            CB_SHA256=bd8c808771cb46e563c173f60e0723c32351a6453f6ece2d4fa440e0d2dcdfd3            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 02 Mar 2023 02:41:16 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 02 Mar 2023 02:41:16 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 02 Mar 2023 02:41:17 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 02 Mar 2023 02:41:17 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 02 Mar 2023 02:41:17 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 02 Mar 2023 02:41:17 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 02 Mar 2023 02:41:18 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Thu, 02 Mar 2023 02:41:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Mar 2023 02:41:18 GMT
CMD ["couchbase-server"]
# Thu, 02 Mar 2023 02:41:18 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Thu, 02 Mar 2023 02:41:18 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbdfa26235b63626dd91aab79323328c46ba411941b8d974a5b265cd558297e`  
		Last Modified: Thu, 02 Mar 2023 02:42:20 GMT  
		Size: 6.0 MB (6043418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44876af4cc6075d743d09d0b900e248afbc79aef356d76a3e6fe266fef0c3115`  
		Last Modified: Thu, 02 Mar 2023 02:42:19 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c14aedc03bfb796a48c5c908c4572917eea057fedb80808779b424983f05be`  
		Last Modified: Thu, 02 Mar 2023 02:42:56 GMT  
		Size: 541.2 MB (541156198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9655e15d917231584089e31a623fb8c919e9d44ada53b7bfd34f871e945fdf`  
		Last Modified: Thu, 02 Mar 2023 02:42:18 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca558e35df7ed35c4b2d39d7fe9f53605dbfb7536892252653ed116d4cc2d8e5`  
		Last Modified: Thu, 02 Mar 2023 02:42:17 GMT  
		Size: 738.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19af2c032a23b1dce6647e08a1f6fece635710b2b21422cc70d7411669f94cba`  
		Last Modified: Thu, 02 Mar 2023 02:42:17 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393f2b3f67b6d071e81815575792aa6178570d9341d2884657e92ee56e401fd1`  
		Last Modified: Thu, 02 Mar 2023 02:42:17 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca029d7a7e337b0ffb2830a4acbe4bb9d5f5b22e04038c33f7cfe8392f1e154`  
		Last Modified: Thu, 02 Mar 2023 02:42:17 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76a578ca28a2e8bac1dc729e557225d4bd9d3f969abc0f94e27c8f260ae19a2`  
		Last Modified: Thu, 02 Mar 2023 02:42:17 GMT  
		Size: 864.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
