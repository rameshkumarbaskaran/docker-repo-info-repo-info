## `couchbase:community-7.1.1`

```console
$ docker pull couchbase@sha256:7ce7bb3f7f3dff035dc885a8096a9f5d3440a95deb2a97b1f7bb11f114f1a751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:community-7.1.1` - linux; amd64

```console
$ docker pull couchbase@sha256:b12f3769b9b191a8ce97afa2e7c0d27cebc36a7a12f22ccf57167b140871abf0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.7 MB (346670583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f9f5c90b4c2fa28bb2d4f8f78fe66707071b6425e05c195d9f5e50c25466b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 05 Jun 2023 17:08:57 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:08:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:08:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:08:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Jun 2023 17:08:58 GMT
ADD file:655d373cb551d0dd5d7867f88a4f98908dc3f16190986f693e88c423e6f21b8d in / 
# Mon, 05 Jun 2023 17:08:58 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 01:58:57 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 16 Jun 2023 01:58:57 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 16 Jun 2023 01:58:57 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 16 Jun 2023 01:59:25 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Fri, 16 Jun 2023 02:03:13 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1
# Fri, 16 Jun 2023 02:03:13 GMT
ARG CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb
# Fri, 16 Jun 2023 02:03:13 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 16 Jun 2023 02:03:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 16 Jun 2023 02:03:14 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 16 Jun 2023 02:03:54 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=275a0bb41d81920e9948fc05f736eef753179f698a04609eb8fe617d0fe55b8b            ;;          'amd64')            CB_SHA256=2fa47dc00f6d85aad5298149bb52450cc98c2c1e18eb54ab8ed45346c24a9403            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Fri, 16 Jun 2023 02:03:56 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 16 Jun 2023 02:03:56 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Fri, 16 Jun 2023 02:03:57 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 16 Jun 2023 02:03:57 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 16 Jun 2023 02:03:58 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 16 Jun 2023 02:03:58 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Fri, 16 Jun 2023 02:03:58 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Fri, 16 Jun 2023 02:03:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Jun 2023 02:03:58 GMT
CMD ["couchbase-server"]
# Fri, 16 Jun 2023 02:03:58 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 16 Jun 2023 02:03:59 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:f0412dfb1aaea4892c13dab6f771bcd79641a4bdcb521ce881f5dcfc0df9a7a5`  
		Last Modified: Tue, 06 Jun 2023 09:20:27 GMT  
		Size: 28.6 MB (28580519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6415ade50a8971f892e9c651c561cf94f9aa5d1d59773d9bfcb7c41680c6fe81`  
		Last Modified: Fri, 16 Jun 2023 02:08:02 GMT  
		Size: 6.3 MB (6285956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d975eae37e05a1e067c18e15e7853d00d84f825151aa79d1ca0a0acc337761`  
		Last Modified: Fri, 16 Jun 2023 02:11:05 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308e0c15db12698895a8fe96a9d70018fbc8a46419f1282ceae8f5447d07e039`  
		Last Modified: Fri, 16 Jun 2023 02:11:40 GMT  
		Size: 311.8 MB (311799736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:310d95d09835ccd047e338263c45b1d3898390e69a92609f9ea79599fc8f650a`  
		Last Modified: Fri, 16 Jun 2023 02:11:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7427c3ae8b34640c7479b06e5671896b9324c0ab43ac6f03be2a18fda43ea8`  
		Last Modified: Fri, 16 Jun 2023 02:11:03 GMT  
		Size: 745.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f10a7bd6ef65534abf7e16092c2ac59f05e5f770a6c45f2703262b563337e8`  
		Last Modified: Fri, 16 Jun 2023 02:11:03 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd83caff1bafcac9ddc8f6b18484811c17ec9019a84c621bbb81148efed605d1`  
		Last Modified: Fri, 16 Jun 2023 02:11:03 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23bc495fc6d62ed47c114043c0977fd9fec9094b9987f2a8cd135da9e0f64ba8`  
		Last Modified: Fri, 16 Jun 2023 02:11:03 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f80caee774fd3e0d8a5e393310077637657eea144b2ccebcdf02430cc88fd5`  
		Last Modified: Fri, 16 Jun 2023 02:11:03 GMT  
		Size: 867.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:community-7.1.1` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:b7b43952a73567110f08b7a7da8a4f9118d2f9887481abd8ede558474a873f30
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.3 MB (327338874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2782a69d7f0589c8425896ad43951f76be91c5f05c31231e877a59f2b69b895`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:41:11 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 04 Jul 2023 15:41:11 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 04 Jul 2023 15:41:12 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 04 Jul 2023 15:41:30 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Tue, 04 Jul 2023 15:45:00 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1
# Tue, 04 Jul 2023 15:45:00 GMT
ARG CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb
# Tue, 04 Jul 2023 15:45:00 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 04 Jul 2023 15:45:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 04 Jul 2023 15:45:01 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 04 Jul 2023 15:45:31 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=275a0bb41d81920e9948fc05f736eef753179f698a04609eb8fe617d0fe55b8b            ;;          'amd64')            CB_SHA256=2fa47dc00f6d85aad5298149bb52450cc98c2c1e18eb54ab8ed45346c24a9403            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Tue, 04 Jul 2023 15:45:37 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 04 Jul 2023 15:45:37 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Tue, 04 Jul 2023 15:45:38 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Tue, 04 Jul 2023 15:45:38 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 04 Jul 2023 15:45:38 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 04 Jul 2023 15:45:39 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Tue, 04 Jul 2023 15:45:39 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Tue, 04 Jul 2023 15:45:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Jul 2023 15:45:39 GMT
CMD ["couchbase-server"]
# Tue, 04 Jul 2023 15:45:39 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Tue, 04 Jul 2023 15:45:39 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda9a6210867ab86522abf879d7f6960e90ba3a4e2a7eb0c684bd4e5b1305a61`  
		Last Modified: Tue, 04 Jul 2023 15:46:00 GMT  
		Size: 6.1 MB (6109787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c2947c691fb640b82f82638c9ddc2cf7f6bd79eb7b980cf5d5112f5f5db89e`  
		Last Modified: Tue, 04 Jul 2023 15:48:21 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cfbc7f39271cd65d00269926b1b7446ad62d3b09e977df6c3897531801fe76e`  
		Last Modified: Tue, 04 Jul 2023 15:48:46 GMT  
		Size: 294.0 MB (294026383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627deed16fc8939af94a5d5d3f0fcaf93fc9ba6e9f4da50f58aa1e38d3663b44`  
		Last Modified: Tue, 04 Jul 2023 15:48:21 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20cb4f24eb542d75cc8a4975b30bdd869f23545ceccd890aa3afdd93494f6a18`  
		Last Modified: Tue, 04 Jul 2023 15:48:19 GMT  
		Size: 745.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f00c4ba37b83d322d40220c2544947a8afa85dc89641547c93b47143a27738b`  
		Last Modified: Tue, 04 Jul 2023 15:48:19 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3144b40e11e59c937b606eb56c79ceaf602ff0d01ce9d78c7ec2057072206a3`  
		Last Modified: Tue, 04 Jul 2023 15:48:19 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c1f769d4f349e36eabd43d1ebb2dd7952d28f3d6ec0146c35c62d3bcfb4e01`  
		Last Modified: Tue, 04 Jul 2023 15:48:19 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b48b802bf3ddc58207a782547396ea853e474e4f62e235397660881e63be709d`  
		Last Modified: Tue, 04 Jul 2023 15:48:19 GMT  
		Size: 867.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
