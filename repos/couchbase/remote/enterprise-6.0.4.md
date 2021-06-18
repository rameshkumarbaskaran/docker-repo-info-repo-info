## `couchbase:enterprise-6.0.4`

```console
$ docker pull couchbase@sha256:768a0be972b295b8fd967c0ded61a278c1c2ef22e659c3892850f0760b12e784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise-6.0.4` - linux; amd64

```console
$ docker pull couchbase@sha256:c298a4d6d5682be40e703c3c9cb7dbd110599ae51efe2ead4d58d52df1e1f42b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **467.2 MB (467168867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df402e941db862e70dfdf9b1886f9d34477c7ec8d6de82d33bc443cdbc89386`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:22 GMT
ADD file:900f735ff138e5137cf25ddd85a32a01921ebec26d86704d24b5f12e73a832c2 in / 
# Thu, 17 Jun 2021 23:31:22 GMT
CMD ["bash"]
# Thu, 17 Jun 2021 23:53:59 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 17 Jun 2021 23:56:05 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata man     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:56:06 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Fri, 18 Jun 2021 00:02:22 GMT
ARG CB_VERSION=6.0.4
# Fri, 18 Jun 2021 00:02:22 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.4
# Fri, 18 Jun 2021 00:02:22 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.0.4-ubuntu18.04_amd64.deb
# Fri, 18 Jun 2021 00:02:23 GMT
ARG CB_SHA256=7dbe8dd074f9cabea69468ea488f9ffc19c04dab8fc2e98c937fa32704982aff
# Fri, 18 Jun 2021 00:02:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 18 Jun 2021 00:02:24 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.4-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.4 CB_SHA256=7dbe8dd074f9cabea69468ea488f9ffc19c04dab8fc2e98c937fa32704982aff CB_VERSION=6.0.4
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 18 Jun 2021 00:03:14 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.4-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.4 CB_SHA256=7dbe8dd074f9cabea69468ea488f9ffc19c04dab8fc2e98c937fa32704982aff CB_VERSION=6.0.4
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 18 Jun 2021 00:03:17 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.4-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.4 CB_SHA256=7dbe8dd074f9cabea69468ea488f9ffc19c04dab8fc2e98c937fa32704982aff CB_VERSION=6.0.4
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 18 Jun 2021 00:03:18 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 18 Jun 2021 00:03:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.4-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.4 CB_SHA256=7dbe8dd074f9cabea69468ea488f9ffc19c04dab8fc2e98c937fa32704982aff CB_VERSION=6.0.4
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 18 Jun 2021 00:03:19 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:03:20 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.4-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.4 CB_SHA256=7dbe8dd074f9cabea69468ea488f9ffc19c04dab8fc2e98c937fa32704982aff CB_VERSION=6.0.4
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 18 Jun 2021 00:03:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.4-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.4 CB_SHA256=7dbe8dd074f9cabea69468ea488f9ffc19c04dab8fc2e98c937fa32704982aff CB_VERSION=6.0.4
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 18 Jun 2021 00:03:21 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 18 Jun 2021 00:03:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Jun 2021 00:03:21 GMT
CMD ["couchbase-server"]
# Fri, 18 Jun 2021 00:03:21 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 18 Jun 2021 00:03:22 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:25fa05cd42bd8fabb25d2a6f3f8c9f7ab34637903d00fd2ed1c1d0fa980427dd`  
		Last Modified: Thu, 17 Jun 2021 23:32:41 GMT  
		Size: 26.7 MB (26700706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05bf3da53cf4b3f333e9356133c7830082e23c62dddddb71c4d2c08ea2915223`  
		Last Modified: Fri, 18 Jun 2021 00:13:27 GMT  
		Size: 15.9 MB (15923371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545dc5a4237ac749c5a107319df722d3d49b8cafcb548eede9190b28815c17e0`  
		Last Modified: Fri, 18 Jun 2021 00:13:20 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60fa8873fa27f508bb6dd4a45d6a6d2e3dd3df0352d427c3e8dbd1bdd7a44a02`  
		Last Modified: Fri, 18 Jun 2021 00:19:18 GMT  
		Size: 2.0 KB (1964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6be19648d35f5d96fc5b8658d54b3804b9876e56772f43613404cea6717d2f`  
		Last Modified: Fri, 18 Jun 2021 00:20:01 GMT  
		Size: 424.4 MB (424414734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe238b99720845cfe81c253f3ff30bc517923b0767087857f08e78015b6a8440`  
		Last Modified: Fri, 18 Jun 2021 00:19:18 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5f3795e56a5d2a85066a7952a266aefe1c67146108da953e73d1c1d6d186b6`  
		Last Modified: Fri, 18 Jun 2021 00:19:18 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528e93e00d13be7736369f280b2bf09ec30e5ae16c14b798e439353aff02a8bb`  
		Last Modified: Fri, 18 Jun 2021 00:19:16 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997293441b8ed4550205e79c87efd1f75a86ec47b8c71ef812c763610a140f2e`  
		Last Modified: Fri, 18 Jun 2021 00:19:16 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ab0ae57684cf9c26e565a4e49c80682898e7dbad4c7b870c6240fb61287022`  
		Last Modified: Fri, 18 Jun 2021 00:19:16 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c776ce0a278d5fbdfbd22508a2716779395f54ccc2a6d89eb2bb734c2967063`  
		Last Modified: Fri, 18 Jun 2021 00:19:16 GMT  
		Size: 125.6 KB (125564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49b5a158124ea31a3811965af11bd7b3b08fd14523cd846b8db56cf506ed97f`  
		Last Modified: Fri, 18 Jun 2021 00:19:16 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
