## `couchbase:enterprise-7.0.0-beta`

```console
$ docker pull couchbase@sha256:69db6d2cac0812e2e85f7f88c9df8f9008ac10296c4f356741c3767956ad1bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise-7.0.0-beta` - linux; amd64

```console
$ docker pull couchbase@sha256:aeca39250c2452d98706e52aa74551223e508307f5a95476d9746379f7438aaa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.1 MB (628084604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7a2faac4b4fa261d77e6a640b90fbc9719b163f7c784dd3b2f3eddfcb69e780`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Thu, 17 Jun 2021 23:49:37 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 17 Jun 2021 23:50:08 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata man     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:50:09 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Thu, 17 Jun 2021 23:50:09 GMT
ARG CB_VERSION=7.0.0-beta
# Thu, 17 Jun 2021 23:50:09 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta
# Thu, 17 Jun 2021 23:50:09 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb
# Thu, 17 Jun 2021 23:50:10 GMT
ARG CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6
# Thu, 17 Jun 2021 23:50:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 17 Jun 2021 23:50:11 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6 CB_VERSION=7.0.0-beta
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 17 Jun 2021 23:51:13 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6 CB_VERSION=7.0.0-beta
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:51:18 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6 CB_VERSION=7.0.0-beta
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 17 Jun 2021 23:51:18 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 17 Jun 2021 23:51:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6 CB_VERSION=7.0.0-beta
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 17 Jun 2021 23:51:19 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 17 Jun 2021 23:51:20 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6 CB_VERSION=7.0.0-beta
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 17 Jun 2021 23:51:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6 CB_VERSION=7.0.0-beta
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 17 Jun 2021 23:51:22 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 17 Jun 2021 23:51:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Jun 2021 23:51:22 GMT
CMD ["couchbase-server"]
# Thu, 17 Jun 2021 23:51:22 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 17 Jun 2021 23:51:22 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ea62ac22b460984a57032ad72ec95bf050b1340f4eb25afd54c1aed65b631c`  
		Last Modified: Fri, 18 Jun 2021 00:08:49 GMT  
		Size: 8.3 MB (8286917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c73cba5232eb8ed25020437adc96fd1779f00a5c2ed2ba2382b3ec228ab48b9`  
		Last Modified: Fri, 18 Jun 2021 00:08:44 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0f8937c6ee760ce96d311add15db77fd7fc154e09110970dcb7172b3326966`  
		Last Modified: Fri, 18 Jun 2021 00:08:44 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800fd1cd26a5a9021417137ad0466a01bf48dc5ce205a4c39155876f2a0a45a4`  
		Last Modified: Fri, 18 Jun 2021 00:09:50 GMT  
		Size: 591.1 MB (591113742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cddc4475e9d23b540d7ad7eadf0788c667591a0aebb68abca6873bebc9d25b10`  
		Last Modified: Fri, 18 Jun 2021 00:08:43 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b4c966359bd878649225d94e21bc5d9a041690083387bea49e1f48afb4e47a`  
		Last Modified: Fri, 18 Jun 2021 00:08:43 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f111047edbe8626b9ec5a73e4cf2bde9768f01fabf1d99c6a7265ed62ecfe2`  
		Last Modified: Fri, 18 Jun 2021 00:08:41 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d415610107ee18d1266a073f4bbaa2672ead83287c581bf64069f9f2c22cca38`  
		Last Modified: Fri, 18 Jun 2021 00:08:41 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfb2409bf2794a3ff6605a79670d95c5d84696691688d37c0ee391f4c15a6d3`  
		Last Modified: Fri, 18 Jun 2021 00:08:41 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696d6f9063781d2fe925e3429ea2732f1727d80c145e24869e826f72f0c8a6c0`  
		Last Modified: Fri, 18 Jun 2021 00:08:42 GMT  
		Size: 125.9 KB (125890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b06d1f9385c1b8e646d10b4f38a834be1eaec775f14b3d29d9c6c9ba564a26e8`  
		Last Modified: Fri, 18 Jun 2021 00:08:41 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
