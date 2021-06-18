## `couchbase:enterprise-6.0.5`

```console
$ docker pull couchbase@sha256:c01323a9d9957cd87b6929110951a5a618f1662ae616269827f507eb4eb1073f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise-6.0.5` - linux; amd64

```console
$ docker pull couchbase@sha256:7c1f755f5f07e887dea165a97f226741611cd4ed0095531fa95114c5eeb0b38b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.1 MB (466117231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81c0474bf3d11d1efe347b4b57351ed149e20ea5f4291271dddeb0774ebd24f`
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
# Thu, 17 Jun 2021 23:56:06 GMT
ARG CB_VERSION=6.0.5
# Thu, 17 Jun 2021 23:56:06 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5
# Thu, 17 Jun 2021 23:56:06 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb
# Thu, 17 Jun 2021 23:56:06 GMT
ARG CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d
# Thu, 17 Jun 2021 23:56:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 17 Jun 2021 23:56:08 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 17 Jun 2021 23:57:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:57:05 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 17 Jun 2021 23:57:05 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 17 Jun 2021 23:57:06 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 17 Jun 2021 23:57:06 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 17 Jun 2021 23:57:07 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 17 Jun 2021 23:57:08 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 17 Jun 2021 23:57:09 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 17 Jun 2021 23:57:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Jun 2021 23:57:09 GMT
CMD ["couchbase-server"]
# Thu, 17 Jun 2021 23:57:09 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 17 Jun 2021 23:57:09 GMT
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
	-	`sha256:87889e99590a57a085f0ba827e2e71ce446e1a7f25644e6e8dece30666168683`  
		Last Modified: Fri, 18 Jun 2021 00:13:20 GMT  
		Size: 2.0 KB (1965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0564e1f57129e8716d24e67b4b2da2e87bd15ff09657998302ed32aa8ffc2e`  
		Last Modified: Fri, 18 Jun 2021 00:14:01 GMT  
		Size: 423.4 MB (423363109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe026f25a08cadf247eb0e3c071c316b77aaf96bd3285a8b0228737ade2a3b33`  
		Last Modified: Fri, 18 Jun 2021 00:13:20 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635016263f92d3a529516650e130c94d2bb254dbc01a542b29b1c3865ab70bf0`  
		Last Modified: Fri, 18 Jun 2021 00:13:20 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac6861274e63654ea9e7faef482e735dc9f967527284dc1fc0c2a16ca90b52b`  
		Last Modified: Fri, 18 Jun 2021 00:13:17 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe77e1429ab397b87e005aba082a0bc1642c611e3cca230b93c209047dc4fbc`  
		Last Modified: Fri, 18 Jun 2021 00:13:17 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4afd3c4adc77f24f67a05b779db5ecfa1428569910125e02f406244ecc9400e`  
		Last Modified: Fri, 18 Jun 2021 00:13:18 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051769b56ed3e3c77709dbbf85a5d2684be22f76488386c7dcd8de8a039992d6`  
		Last Modified: Fri, 18 Jun 2021 00:13:18 GMT  
		Size: 125.6 KB (125557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c685da4ede59d964d2de05bccc245bb082f20a1174ddafb4463a2eae4f9429`  
		Last Modified: Fri, 18 Jun 2021 00:13:17 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
