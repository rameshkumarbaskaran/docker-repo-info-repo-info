## `couchbase:community`

```console
$ docker pull couchbase@sha256:c5a18e2523c0df3f33cf628951ca40eeeb770d18c1b6bd5c40cc306f756b2136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:community` - linux; amd64

```console
$ docker pull couchbase@sha256:ecdf66c68f0ed58f9c8ee7d9f99d4ffbd3cef85eccea1d691fc4fc946f6558fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (349044603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42453a1704198596fd5f4de8d57c88ac7f7a8d60a2460314d463e4b49de84380`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Mon, 06 Jun 2022 23:57:21 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 06 Jun 2022 23:57:21 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Mon, 06 Jun 2022 23:57:21 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 06 Jun 2022 23:57:42 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Mon, 06 Jun 2022 23:57:42 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0
# Mon, 06 Jun 2022 23:58:52 GMT
ARG CB_PACKAGE=couchbase-server-community_7.1.0-ubuntu20.04_amd64.deb
# Mon, 06 Jun 2022 23:58:52 GMT
ARG CB_SHA256=23c24973c9a9c57341bd78549dc8b07b149b3c3798bfa0968b77678c47b7f539
# Mon, 06 Jun 2022 23:58:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 06 Jun 2022 23:58:53 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=23c24973c9a9c57341bd78549dc8b07b149b3c3798bfa0968b77678c47b7f539 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Mon, 06 Jun 2022 23:59:28 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=23c24973c9a9c57341bd78549dc8b07b149b3c3798bfa0968b77678c47b7f539 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c -     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Mon, 06 Jun 2022 23:59:31 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=23c24973c9a9c57341bd78549dc8b07b149b3c3798bfa0968b77678c47b7f539 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Mon, 06 Jun 2022 23:59:31 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Mon, 06 Jun 2022 23:59:32 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=23c24973c9a9c57341bd78549dc8b07b149b3c3798bfa0968b77678c47b7f539 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Mon, 06 Jun 2022 23:59:32 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Mon, 06 Jun 2022 23:59:32 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=23c24973c9a9c57341bd78549dc8b07b149b3c3798bfa0968b77678c47b7f539 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Mon, 06 Jun 2022 23:59:33 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=23c24973c9a9c57341bd78549dc8b07b149b3c3798bfa0968b77678c47b7f539 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Mon, 06 Jun 2022 23:59:33 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Mon, 06 Jun 2022 23:59:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jun 2022 23:59:33 GMT
CMD ["couchbase-server"]
# Mon, 06 Jun 2022 23:59:34 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Mon, 06 Jun 2022 23:59:34 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b15b7718218cb8c8adc351f6e6d4b00e354a525046c18ec4d6f5bab108a1a66`  
		Last Modified: Tue, 07 Jun 2022 00:07:47 GMT  
		Size: 6.3 MB (6251734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f066d477269a208fd593affb5665c2128daf8dee05f6312fb50971cff31fb434`  
		Last Modified: Tue, 07 Jun 2022 00:09:03 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e6edf1cedda40fa9e51d92d21c021bc9a2bee9070c3c8c4205cfa04c1d5012`  
		Last Modified: Tue, 07 Jun 2022 00:09:44 GMT  
		Size: 314.2 MB (314215876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d26a3f9a09c47cb4eda07e4502823fb8bb0d880cc51f23e64e71f8bdb15b58`  
		Last Modified: Tue, 07 Jun 2022 00:09:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f464fe501c0d90ae2ab29f501a811632e9423afe0d23b1c45c78a4bc4d380d`  
		Last Modified: Tue, 07 Jun 2022 00:09:01 GMT  
		Size: 740.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2c00d03227fa4feb5e8d36d73f2797f4d75c420c798dbafbfa22105e5dc61c`  
		Last Modified: Tue, 07 Jun 2022 00:09:01 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63dcd7e1d853f91ebad23cc758a89935314030c7f598fc15f1fa307287688f51`  
		Last Modified: Tue, 07 Jun 2022 00:09:01 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aef3d656bc7708dc688b5ce04f1ebf0571df2fee448fa0cb7ba3de8c1c8d11ae`  
		Last Modified: Tue, 07 Jun 2022 00:09:01 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800d564395e484973e7b383c43913b150ef28bfb4e969c341a7cf822445c236d`  
		Last Modified: Tue, 07 Jun 2022 00:09:01 GMT  
		Size: 869.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
