## `couchbase:latest`

```console
$ docker pull couchbase@sha256:47ed9b19ac85b202000e8875aa8ae507c81dac77c67f757b8367522d8f1f35d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:latest` - linux; amd64

```console
$ docker pull couchbase@sha256:20251532870b6947b24c0249d8081652488af7ad45f221f015118dcd2df0db33
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.0 MB (676998066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb033a3df3d523bcf22def918aed04ea07ac0d1100bd60baf7cefec1943e6ee7`
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
# Fri, 07 Jan 2022 02:48:14 GMT
ARG CB_VERSION=7.0.3
# Fri, 07 Jan 2022 02:48:15 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3
# Fri, 07 Jan 2022 02:48:15 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb
# Fri, 07 Jan 2022 02:48:15 GMT
ARG CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c
# Fri, 07 Jan 2022 02:48:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 07 Jan 2022 02:48:16 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 07 Jan 2022 02:49:34 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 07 Jan 2022 02:49:39 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 07 Jan 2022 02:49:39 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Fri, 07 Jan 2022 02:49:40 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 07 Jan 2022 02:49:41 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 07 Jan 2022 02:49:41 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 07 Jan 2022 02:49:48 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             apt-get update;             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get purge -y chrpath;             apt-get autoremove;             apt-get clean;         fi
# Fri, 07 Jan 2022 02:49:49 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Fri, 07 Jan 2022 02:49:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Jan 2022 02:49:49 GMT
CMD ["couchbase-server"]
# Fri, 07 Jan 2022 02:49:49 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 07 Jan 2022 02:49:50 GMT
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
	-	`sha256:bcb4f8680ab88ed1d42054586110b2f7c88d44d1958461db8bc7768f41dbd77c`  
		Last Modified: Fri, 07 Jan 2022 02:56:17 GMT  
		Size: 1.8 KB (1829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1103d0911786914568c3da9a9a75f1af7bb0461c2ed7e70a18e2920a978e0bca`  
		Last Modified: Fri, 07 Jan 2022 02:57:27 GMT  
		Size: 618.3 MB (618296886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2110faa7a5b85b1938337de9103a54236c115e8e3eb81079716d9041b4003e05`  
		Last Modified: Fri, 07 Jan 2022 02:56:16 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fb9e05960f9a3f2f101ab8b046e9c1ec9e1ea75d558f014b3fa96b2110d4f8`  
		Last Modified: Fri, 07 Jan 2022 02:56:16 GMT  
		Size: 744.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4508c1d298c835756496e8819dd6a5eda3603f6598fffdb247bf6217bc698724`  
		Last Modified: Fri, 07 Jan 2022 02:56:14 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1496e727dd9652cc32a50f280e4a872cb12a0dcd8c36bfd63f4503a2a3c0aae`  
		Last Modified: Fri, 07 Jan 2022 02:56:14 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d91ce2b56d0558b11b0e82aef58a3a88a266d0e48acdb9c488593ff6f15377`  
		Last Modified: Fri, 07 Jan 2022 02:56:14 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc08238b4d72bda9a93053cd6b1dcb3dd9cc66f2a7a122fdd149f03bf1f50a4`  
		Last Modified: Fri, 07 Jan 2022 02:56:17 GMT  
		Size: 23.9 MB (23878221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2c81438f07aeea3dc1f64847b3c55fc43be24ea9d75c7bf33e92b0e758e980`  
		Last Modified: Fri, 07 Jan 2022 02:56:14 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
