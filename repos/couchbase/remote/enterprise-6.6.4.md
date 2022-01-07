## `couchbase:enterprise-6.6.4`

```console
$ docker pull couchbase@sha256:3775640593dd86e6682ff63de4a2e38941b7258753fc0f66d8db2ae0e0ebf707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:enterprise-6.6.4` - linux; amd64

```console
$ docker pull couchbase@sha256:fdad5c35d221a25172dabeae1c9bcc613e10430817f2bd751ef0b1b384223d0f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.7 MB (561688730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820e0d5e5d4fd9cabdfce500318b7e20b77374619b596cd32cf3254cae0cec31`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:29 GMT
ADD file:122ad323412c2e70b3138d8eb62648c4692989de91be1ffb6b4bf086c8311b62 in / 
# Fri, 07 Jan 2022 02:25:30 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:47:48 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 07 Jan 2022 02:48:14 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 07 Jan 2022 02:51:19 GMT
ARG CB_VERSION=6.6.4
# Fri, 07 Jan 2022 02:51:20 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.4
# Fri, 07 Jan 2022 02:51:20 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.6.4-ubuntu20.04_amd64.deb
# Fri, 07 Jan 2022 02:51:20 GMT
ARG CB_SHA256=97cb0aec5a4f7e3d2c3e2017546ac0adb41478c6e5bc1dcefd06cc9f5926f6db
# Fri, 07 Jan 2022 02:51:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 07 Jan 2022 02:51:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.4-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.4 CB_SHA256=97cb0aec5a4f7e3d2c3e2017546ac0adb41478c6e5bc1dcefd06cc9f5926f6db CB_VERSION=6.6.4
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 07 Jan 2022 02:52:26 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.4-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.4 CB_SHA256=97cb0aec5a4f7e3d2c3e2017546ac0adb41478c6e5bc1dcefd06cc9f5926f6db CB_VERSION=6.6.4
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 07 Jan 2022 02:52:28 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.4-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.4 CB_SHA256=97cb0aec5a4f7e3d2c3e2017546ac0adb41478c6e5bc1dcefd06cc9f5926f6db CB_VERSION=6.6.4
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 07 Jan 2022 02:52:28 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Fri, 07 Jan 2022 02:52:29 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.4-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.4 CB_SHA256=97cb0aec5a4f7e3d2c3e2017546ac0adb41478c6e5bc1dcefd06cc9f5926f6db CB_VERSION=6.6.4
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 07 Jan 2022 02:52:29 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 07 Jan 2022 02:52:30 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.4-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.4 CB_SHA256=97cb0aec5a4f7e3d2c3e2017546ac0adb41478c6e5bc1dcefd06cc9f5926f6db CB_VERSION=6.6.4
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 07 Jan 2022 02:52:37 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.4-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.4 CB_SHA256=97cb0aec5a4f7e3d2c3e2017546ac0adb41478c6e5bc1dcefd06cc9f5926f6db CB_VERSION=6.6.4
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             apt-get update;             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get purge -y chrpath;             apt-get autoremove;             apt-get clean;         fi
# Fri, 07 Jan 2022 02:52:38 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Fri, 07 Jan 2022 02:52:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Jan 2022 02:52:38 GMT
CMD ["couchbase-server"]
# Fri, 07 Jan 2022 02:52:38 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 07 Jan 2022 02:52:39 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:ea362f368469f909a95f9a6e54ebe0121ce0a8e3c30583dd9c5fb35b14544dec`  
		Last Modified: Thu, 06 Jan 2022 15:07:12 GMT  
		Size: 28.6 MB (28566425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66cfcdf8838abf002a7e0a2b3f6a8a41688c07a1055f77fedce22a3c62c05b4`  
		Last Modified: Fri, 07 Jan 2022 02:56:20 GMT  
		Size: 6.3 MB (6252170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16199ea3a03efa6bc813742048c124777c44a880011c4f02f0ab2ed64655366`  
		Last Modified: Fri, 07 Jan 2022 02:58:50 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3335e980a3591f1d6a88a0e5987986c06e05d58c7b593480950e9e62c88131f`  
		Last Modified: Fri, 07 Jan 2022 02:59:42 GMT  
		Size: 503.0 MB (502991689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5eb14c1807736bf2b4ab827e9fd460dcaaabf182af700421592b7d13df3732`  
		Last Modified: Fri, 07 Jan 2022 02:58:50 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1d5b3d1205d51ec426512339929f89cf3f366b3730b33776992f14567234f10`  
		Last Modified: Fri, 07 Jan 2022 02:58:50 GMT  
		Size: 744.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2b217981de2a462d4dcc62538fc1a1f3c1cbf3b6f6729768fd39c08fb18c97`  
		Last Modified: Fri, 07 Jan 2022 02:58:48 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3235e9bac99058de6ff914ba35a22351a4a572b341552845bf65ec3abc12abde`  
		Last Modified: Fri, 07 Jan 2022 02:58:48 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc9220de1c0106fba54832851747dffad049287f03d3b12c7fa7ecff5461beb`  
		Last Modified: Fri, 07 Jan 2022 02:58:48 GMT  
		Size: 215.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4163898a45897dd974d3ae811621a9c97b0f6df6dfd4a13ad3e14f1ee967b9a6`  
		Last Modified: Fri, 07 Jan 2022 02:58:50 GMT  
		Size: 23.9 MB (23874079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719891fd4435444301cfc8b2b9cfa85be519b0014494181a0996b1f43600d323`  
		Last Modified: Fri, 07 Jan 2022 02:58:48 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
