## `couchbase:enterprise-6.0.5`

```console
$ docker pull couchbase@sha256:7b96e89ef0f60866c705b9661f01417a3ce2ddcfd625c974faec81d091220702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise-6.0.5` - linux; amd64

```console
$ docker pull couchbase@sha256:e106120e1aa09931a9835c86aed98f61863ccb78c879d992fa7f70245b91d799
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **481.3 MB (481321606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:601bd23b57feafbd57152c34d7f04021402b6e8668fd18f26e7d031383571543`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 23 Apr 2021 22:22:16 GMT
ADD file:34f9c325bb2e6ad9f9a062ce9a0237fab0c04aea83f31b8548ea0ae532255be0 in / 
# Fri, 23 Apr 2021 22:22:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:22:18 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:22:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:22:19 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:11:43 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Fri, 23 Apr 2021 23:14:26 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 23 Apr 2021 23:14:27 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Fri, 23 Apr 2021 23:14:28 GMT
ARG CB_VERSION=6.0.5
# Fri, 23 Apr 2021 23:14:28 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5
# Fri, 23 Apr 2021 23:14:28 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu16.04_amd64.deb
# Fri, 23 Apr 2021 23:14:28 GMT
ARG CB_SHA256=3227bd9bf04affeea6c567a9e87cde585d2d49e5548b95204ffbda7dea8d451a
# Fri, 23 Apr 2021 23:14:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 23 Apr 2021 23:14:30 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=3227bd9bf04affeea6c567a9e87cde585d2d49e5548b95204ffbda7dea8d451a CB_VERSION=6.0.5
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 23 Apr 2021 23:15:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=3227bd9bf04affeea6c567a9e87cde585d2d49e5548b95204ffbda7dea8d451a CB_VERSION=6.0.5
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Fri, 23 Apr 2021 23:15:22 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=3227bd9bf04affeea6c567a9e87cde585d2d49e5548b95204ffbda7dea8d451a CB_VERSION=6.0.5
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 23 Apr 2021 23:15:23 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 23 Apr 2021 23:15:24 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=3227bd9bf04affeea6c567a9e87cde585d2d49e5548b95204ffbda7dea8d451a CB_VERSION=6.0.5
RUN chown -R couchbase:couchbase /etc/service
# Fri, 23 Apr 2021 23:15:24 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 23 Apr 2021 23:15:25 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=3227bd9bf04affeea6c567a9e87cde585d2d49e5548b95204ffbda7dea8d451a CB_VERSION=6.0.5
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 23 Apr 2021 23:15:26 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=3227bd9bf04affeea6c567a9e87cde585d2d49e5548b95204ffbda7dea8d451a CB_VERSION=6.0.5
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 23 Apr 2021 23:15:27 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 23 Apr 2021 23:15:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 23 Apr 2021 23:15:27 GMT
CMD ["couchbase-server"]
# Fri, 23 Apr 2021 23:15:27 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 23 Apr 2021 23:15:27 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:92473f7ef45574f608989888a6cfc8187d3a1425e3a63f974434acab03fed068`  
		Last Modified: Sat, 17 Apr 2021 15:20:07 GMT  
		Size: 46.3 MB (46254451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb52bde70123ac7f3a1b88fee95e74f4bdcdbd81917a91a35b56a52ec7671947`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64788f86be3fd71809b5de602deff9445f3de18d2f44a49d0a053dfc9a2008ae`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f6d5f2e001ababe3ddac4731d9c33121e1148ef32a87a83a5b470cb401abef`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c803522fd7ce3caeee80a2f3560697378ef0efcef40e8f0ecd7e7d4c201ef52d`  
		Last Modified: Fri, 23 Apr 2021 23:21:19 GMT  
		Size: 14.3 MB (14298604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96adf41055f8d226fa05769703b147487f1706d86ca0b679aca2b054d5da6ce`  
		Last Modified: Fri, 23 Apr 2021 23:21:15 GMT  
		Size: 2.1 KB (2076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df65a523c006ddac01880d748c8e96f10c574c55d25825627baaf73706ceb75f`  
		Last Modified: Fri, 23 Apr 2021 23:21:59 GMT  
		Size: 420.6 MB (420641974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e562d5a94ff2aca64d86f93e24e56161649bda8578c162946ea1f8099ff65e`  
		Last Modified: Fri, 23 Apr 2021 23:21:15 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770e55bdb2dfeec5e7ed1eea854e2a80d2d67300c92216d87b64613056d2195a`  
		Last Modified: Fri, 23 Apr 2021 23:21:15 GMT  
		Size: 434.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4404f385bad081b72f90d0593bb625007a4a1ac3380283649c4600b6c8a8ce2b`  
		Last Modified: Fri, 23 Apr 2021 23:21:12 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ee964919e6237d0d81bdff28971be6b30156defa74636f0af7369250174851`  
		Last Modified: Fri, 23 Apr 2021 23:21:12 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0857822d3c707682f9af4a94cb09d220f3b09930b0bca18634293aced638182`  
		Last Modified: Fri, 23 Apr 2021 23:21:12 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7063b6fef97b7f687317a181524d6b7f548ec693aa292bf1ece8368674b1f4`  
		Last Modified: Fri, 23 Apr 2021 23:21:13 GMT  
		Size: 120.6 KB (120602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874d396c99b7a51d9b5bc5112545d5ede1e548d4b115fca9f4ad6bffd5776d75`  
		Last Modified: Fri, 23 Apr 2021 23:21:12 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
