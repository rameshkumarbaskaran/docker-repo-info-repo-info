## `couchbase:enterprise-6.0.1`

```console
$ docker pull couchbase@sha256:688008083ab940a045c49c25e0cc10054cdf39c6b4835488cd91e8834a2f0796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise-6.0.1` - linux; amd64

```console
$ docker pull couchbase@sha256:6da3a869ab10a5a1801c863a3c721298b59567eb8feb0b4d6b51beca1ad78310
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.2 MB (455204583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575336030b3c6c606cb327a4006df587a93211d7e0a0ea0a5e5090584ec38aea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 19 May 2021 19:44:30 GMT
ADD file:e05689b5b0d51a2316f8a87b1a9d6cbf90d98b19a424dbb924ee3d0b1cc17bfc in / 
# Wed, 19 May 2021 19:44:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 19:44:32 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 19:44:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 19:44:33 GMT
CMD ["/bin/bash"]
# Wed, 19 May 2021 20:37:24 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 19 May 2021 20:39:05 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata man     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 19 May 2021 20:39:06 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Wed, 19 May 2021 20:50:01 GMT
ARG CB_VERSION=6.0.1
# Wed, 19 May 2021 20:50:01 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.1
# Wed, 19 May 2021 20:50:02 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.0.1-ubuntu18.04_amd64.deb
# Wed, 19 May 2021 20:50:02 GMT
ARG CB_SHA256=68deed9ba855e2a84500ae99a787c415fc85b4d4dc1140be28ae6f56662bafea
# Wed, 19 May 2021 20:50:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 19 May 2021 20:50:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.1 CB_SHA256=68deed9ba855e2a84500ae99a787c415fc85b4d4dc1140be28ae6f56662bafea CB_VERSION=6.0.1
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 19 May 2021 20:50:58 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.1 CB_SHA256=68deed9ba855e2a84500ae99a787c415fc85b4d4dc1140be28ae6f56662bafea CB_VERSION=6.0.1
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 19 May 2021 20:51:01 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.1 CB_SHA256=68deed9ba855e2a84500ae99a787c415fc85b4d4dc1140be28ae6f56662bafea CB_VERSION=6.0.1
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 19 May 2021 20:51:01 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Wed, 19 May 2021 20:51:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.1 CB_SHA256=68deed9ba855e2a84500ae99a787c415fc85b4d4dc1140be28ae6f56662bafea CB_VERSION=6.0.1
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Wed, 19 May 2021 20:51:02 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 19 May 2021 20:51:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.1 CB_SHA256=68deed9ba855e2a84500ae99a787c415fc85b4d4dc1140be28ae6f56662bafea CB_VERSION=6.0.1
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 19 May 2021 20:51:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.1 CB_SHA256=68deed9ba855e2a84500ae99a787c415fc85b4d4dc1140be28ae6f56662bafea CB_VERSION=6.0.1
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Wed, 19 May 2021 20:51:05 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Wed, 19 May 2021 20:51:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 19 May 2021 20:51:05 GMT
CMD ["couchbase-server"]
# Wed, 19 May 2021 20:51:05 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Wed, 19 May 2021 20:51:05 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:4bbfd2c87b7524455f144a03bf387c88b6d4200e5e0df9139a9d5e79110f89ca`  
		Last Modified: Thu, 13 May 2021 14:54:04 GMT  
		Size: 26.7 MB (26696304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e110be24e168b42c1a2ddbc4a476a217b73cccdba69cdcb212b812a88f5726`  
		Last Modified: Wed, 19 May 2021 19:45:43 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889a7173dcfeb409f9d88054a97ab2445f5a799a823f719a5573365ee3662b6f`  
		Last Modified: Wed, 19 May 2021 19:45:43 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4443906eb69df93081300561a4d975a66f54f54cb8d4fabb0f5291860404b5`  
		Last Modified: Wed, 19 May 2021 20:53:52 GMT  
		Size: 15.9 MB (15923534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1810bc668c2f9196f83ab1f6a5314764eb7785985415a163f6ff2e3335aefeb9`  
		Last Modified: Wed, 19 May 2021 20:53:45 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77c45dcaabdd1c528a50694256362dcb7345043065d6ec7d4d713b3848600a08`  
		Last Modified: Wed, 19 May 2021 21:02:41 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7b6ea3727705d5b81ffdecf9f3b43037233509b627d0191be667bc32d7826a`  
		Last Modified: Wed, 19 May 2021 21:03:24 GMT  
		Size: 412.5 MB (412453646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a40749430527340641e8dbeb3d2fa994c564ac1f372dd0d318bac74864e85d`  
		Last Modified: Wed, 19 May 2021 21:02:41 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36962b3d2f7b16f3ff154645177f181c230f63f93bd1f61e1bd067c7e03d5437`  
		Last Modified: Wed, 19 May 2021 21:02:41 GMT  
		Size: 481.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fc281808d1810890e5b31162f8cfe600999ce38dabc3a892d4d01b5bc219b5`  
		Last Modified: Wed, 19 May 2021 21:02:39 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15de46d0dd0bafde30bbe625d2209e6ca14e4a55f185717c0b8ba1e1adc7b58`  
		Last Modified: Wed, 19 May 2021 21:02:39 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718431b022ad74116c18ad947d28f631caf6e8066981cfb7b6e3b49675548082`  
		Last Modified: Wed, 19 May 2021 21:02:39 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0408bf73fac8c6dc459e43af5c9800342d6ef83e038a4d4bf82ca634d6691e`  
		Last Modified: Wed, 19 May 2021 21:02:39 GMT  
		Size: 125.6 KB (125560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02ef82acb4c8e33c1ea1323a0631275b0c9f8041ddc7f2601f6fa6d75e477ed`  
		Last Modified: Wed, 19 May 2021 21:02:39 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
