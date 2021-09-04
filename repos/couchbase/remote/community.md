## `couchbase:community`

```console
$ docker pull couchbase@sha256:63526e608090b51d3a6146618cbf0964d1dbfaf2841577b53bcd7db57c22b966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:community` - linux; amd64

```console
$ docker pull couchbase@sha256:dcc89b0820163f81859ffbc17edc4d2bfb9cef0162087e19e3543ef30fd47199
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.1 MB (422112842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9036e7373b9d28a70f893314a748a332e86ad1e108d9244b2069f4c57380cd3a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:55 GMT
ADD file:d2abf27fe2e8b0b5f4da68c018560c73e11c53098329246e3e6fe176698ef941 in / 
# Tue, 31 Aug 2021 01:20:56 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:17:15 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 31 Aug 2021 03:17:35 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 31 Aug 2021 03:17:36 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Sat, 04 Sep 2021 17:15:20 GMT
ARG CB_VERSION=7.0.1
# Sat, 04 Sep 2021 17:15:21 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.1
# Sat, 04 Sep 2021 17:16:46 GMT
ARG CB_PACKAGE=couchbase-server-community_7.0.1-ubuntu20.04_amd64.deb
# Sat, 04 Sep 2021 17:16:46 GMT
ARG CB_SHA256=1e20fbac5a10573c999f20f313f89bb1f40848f66f6eabb853731f5853c23277
# Sat, 04 Sep 2021 17:16:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Sat, 04 Sep 2021 17:16:47 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.1 CB_SHA256=1e20fbac5a10573c999f20f313f89bb1f40848f66f6eabb853731f5853c23277 CB_VERSION=7.0.1
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Sat, 04 Sep 2021 17:17:32 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.1 CB_SHA256=1e20fbac5a10573c999f20f313f89bb1f40848f66f6eabb853731f5853c23277 CB_VERSION=7.0.1
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Sat, 04 Sep 2021 17:17:36 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.1 CB_SHA256=1e20fbac5a10573c999f20f313f89bb1f40848f66f6eabb853731f5853c23277 CB_VERSION=7.0.1
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Sat, 04 Sep 2021 17:17:36 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Sat, 04 Sep 2021 17:17:37 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.1 CB_SHA256=1e20fbac5a10573c999f20f313f89bb1f40848f66f6eabb853731f5853c23277 CB_VERSION=7.0.1
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Sat, 04 Sep 2021 17:17:37 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Sat, 04 Sep 2021 17:17:38 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.1 CB_SHA256=1e20fbac5a10573c999f20f313f89bb1f40848f66f6eabb853731f5853c23277 CB_VERSION=7.0.1
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Sat, 04 Sep 2021 17:17:39 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.1 CB_SHA256=1e20fbac5a10573c999f20f313f89bb1f40848f66f6eabb853731f5853c23277 CB_VERSION=7.0.1
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Sat, 04 Sep 2021 17:17:39 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Sat, 04 Sep 2021 17:17:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 04 Sep 2021 17:17:39 GMT
CMD ["couchbase-server"]
# Sat, 04 Sep 2021 17:17:39 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Sat, 04 Sep 2021 17:17:39 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:35807b77a593c1147d13dc926a91dcc3015616ff7307cc30442c5a8e07546283`  
		Last Modified: Sat, 28 Aug 2021 03:03:19 GMT  
		Size: 28.6 MB (28570074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909a89f4ffc52b1bc0efc8b382b1da145d18cc3fe8aa349a8c93a0174473f38d`  
		Last Modified: Tue, 31 Aug 2021 03:25:11 GMT  
		Size: 6.3 MB (6265547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669f46faa4219d00fffdc48350b495c094272d77b1505e7438e9786ced31ff1f`  
		Last Modified: Tue, 31 Aug 2021 03:25:07 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fabc9cf3ccdf0f28dc0102ed0ea43f042ead7b1c9d6d5c98d00efbd54422711`  
		Last Modified: Sat, 04 Sep 2021 17:19:31 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf8164cd11694d3d8a475e69ed1fdb181ee2f7ce458581c462de19a6743dbdd`  
		Last Modified: Sat, 04 Sep 2021 17:20:17 GMT  
		Size: 387.1 MB (387146966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c52dc256d57d7b868c856042b86a4c23e55b5050b94e5bc763020adda05f416`  
		Last Modified: Sat, 04 Sep 2021 17:19:31 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3c506e84a3057fca61e9f61deb8e7fb7e2005a520e671fb05cf8525fb71474`  
		Last Modified: Sat, 04 Sep 2021 17:19:31 GMT  
		Size: 481.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbfe724518a5ea5a3533137322718f7fc9f606cc55f7ad346006de737702651b`  
		Last Modified: Sat, 04 Sep 2021 17:19:28 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bed4c7fdb9380ffaf60ac119e8e2676accf221b9d558a7abf29fde7d8bfaa1b`  
		Last Modified: Sat, 04 Sep 2021 17:19:29 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c77d677e622365fc195b811ce9ca8015fbe085ee3858bc3a3d2c18774a87e90`  
		Last Modified: Sat, 04 Sep 2021 17:19:29 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acbfb317876188f099e8cb83b4f8ac8c30c3c32c67b797a72da5ca07c9487828`  
		Last Modified: Sat, 04 Sep 2021 17:19:28 GMT  
		Size: 125.9 KB (125889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196cedc9a5ef41c3ff6e31d6c0fc3a263022d8ca22421f59f815497b64f226f1`  
		Last Modified: Sat, 04 Sep 2021 17:19:28 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
