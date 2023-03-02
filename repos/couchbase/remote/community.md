## `couchbase:community`

```console
$ docker pull couchbase@sha256:ccfed27bf26b937fd372fe8e661ad7b1de74e3768f8b2ddbf65e717584b5b304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:community` - linux; amd64

```console
$ docker pull couchbase@sha256:c9f4154e895e8574268027d046fe7f12a9a59ff9a7365b90854f19d1c124e4cb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.6 MB (346597781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39220a3e298986d8513e334800e17c4585c93882a28b810d92c5fc1c0c7994e9`
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
# Wed, 01 Feb 2023 18:26:42 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1
# Wed, 01 Feb 2023 18:26:42 GMT
ARG CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb
# Wed, 01 Feb 2023 18:26:42 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 01 Feb 2023 18:26:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 01 Feb 2023 18:26:43 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 01 Feb 2023 18:27:18 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=275a0bb41d81920e9948fc05f736eef753179f698a04609eb8fe617d0fe55b8b            ;;          'amd64')            CB_SHA256=2fa47dc00f6d85aad5298149bb52450cc98c2c1e18eb54ab8ed45346c24a9403            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Wed, 01 Feb 2023 18:27:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 01 Feb 2023 18:27:21 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Wed, 01 Feb 2023 18:27:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Wed, 01 Feb 2023 18:27:21 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 01 Feb 2023 18:27:22 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 01 Feb 2023 18:27:23 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Wed, 01 Feb 2023 18:27:23 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Wed, 01 Feb 2023 18:27:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Feb 2023 18:27:23 GMT
CMD ["couchbase-server"]
# Wed, 01 Feb 2023 18:27:23 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Wed, 01 Feb 2023 18:27:23 GMT
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
	-	`sha256:9104ac5883bac220a5f574ba7966f482cea80896107af366ff3070096269b6d8`  
		Last Modified: Wed, 01 Feb 2023 18:32:16 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5badd907bdc9e401e76b24e9f00dae2ce8a147ba07a3318b7db146c942e634`  
		Last Modified: Wed, 01 Feb 2023 18:32:54 GMT  
		Size: 311.8 MB (311799081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24350a0cac3b682c873ae27c1e4e99a3a230d8f463d6fc41c789afabb9e253d9`  
		Last Modified: Wed, 01 Feb 2023 18:32:16 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ae8adb8b33072989ccd8b1bb270ce6dc12ac81b9bbcd9297cb9b16ebcb67ce`  
		Last Modified: Wed, 01 Feb 2023 18:32:14 GMT  
		Size: 744.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c46fc231003be1da0d19984c4d4bf1cfc24878eded7c73c8029c2bc643dbe657`  
		Last Modified: Wed, 01 Feb 2023 18:32:15 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8449d72ddff01b8dc6be535e0cd417fd17845f9562e0371190882071d997235b`  
		Last Modified: Wed, 01 Feb 2023 18:32:15 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaea83304a41aaa60679eb036b0aa0052a0e345e8732f4f98f0ba110e3d63626`  
		Last Modified: Wed, 01 Feb 2023 18:32:14 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97fad92e762b2a92e079e8c6da1631613fb22d047a081feddbac24d190eedc20`  
		Last Modified: Wed, 01 Feb 2023 18:32:15 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:community` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:440efff5952b786ef8f2d4ed59edf26b629d05c82a6f54b86f641b1030e7db22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.3 MB (327266970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8786890f47a6ab029f214845a44ffc8a8e44e2d711484ec85696bf999f47811d`
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
# Thu, 02 Mar 2023 02:41:20 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1
# Thu, 02 Mar 2023 02:41:20 GMT
ARG CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb
# Thu, 02 Mar 2023 02:41:20 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 02 Mar 2023 02:41:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 02 Mar 2023 02:41:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 02 Mar 2023 02:41:53 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=275a0bb41d81920e9948fc05f736eef753179f698a04609eb8fe617d0fe55b8b            ;;          'amd64')            CB_SHA256=2fa47dc00f6d85aad5298149bb52450cc98c2c1e18eb54ab8ed45346c24a9403            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 02 Mar 2023 02:41:59 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 02 Mar 2023 02:41:59 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 02 Mar 2023 02:42:00 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 02 Mar 2023 02:42:00 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 02 Mar 2023 02:42:00 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 02 Mar 2023 02:42:01 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 02 Mar 2023 02:42:01 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Thu, 02 Mar 2023 02:42:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Mar 2023 02:42:01 GMT
CMD ["couchbase-server"]
# Thu, 02 Mar 2023 02:42:01 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 02 Mar 2023 02:42:01 GMT
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
	-	`sha256:513c35875e493bdff62ae8f7b641422236d84835e44288c73c06b766ecb36a88`  
		Last Modified: Thu, 02 Mar 2023 02:43:13 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2219b45c9688ab1aaff8e5c935f45eb799158e5cef70bd8e3d73753516eaa33e`  
		Last Modified: Thu, 02 Mar 2023 02:43:40 GMT  
		Size: 294.0 MB (294024677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d644680c905d18925ca26abe3af750716593a0f4f46adcd4b81eb2a4a1e4a26d`  
		Last Modified: Thu, 02 Mar 2023 02:43:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a978297d23fb352712a340acf440390d986fc7cd77a1dc69ac8afcb384251257`  
		Last Modified: Thu, 02 Mar 2023 02:43:11 GMT  
		Size: 737.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec574fe950a4063621631a9e4efbf9fb8eeb891c1f569cccc2012f03ccf1b1f`  
		Last Modified: Thu, 02 Mar 2023 02:43:11 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e67843acdce830f9058557d263e5879acf0e0e384a33ffae7fe598894d1ac4`  
		Last Modified: Thu, 02 Mar 2023 02:43:11 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc198758a44849f8a09ad61f324c4f4078c9e8d378569f36ec38b9e10a3049b9`  
		Last Modified: Thu, 02 Mar 2023 02:43:11 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9fa898ba252d30cbb7fd359745ff2a1f586264a35a11a32f843bdf14c6b13c`  
		Last Modified: Thu, 02 Mar 2023 02:43:11 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
