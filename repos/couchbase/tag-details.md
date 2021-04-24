<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchbase`

-	[`couchbase:6.0.5`](#couchbase605)
-	[`couchbase:6.6.2`](#couchbase662)
-	[`couchbase:7.0.0-beta`](#couchbase700-beta)
-	[`couchbase:community`](#couchbasecommunity)
-	[`couchbase:community-6.6.0`](#couchbasecommunity-660)
-	[`couchbase:community-7.0.0-beta`](#couchbasecommunity-700-beta)
-	[`couchbase:enterprise`](#couchbaseenterprise)
-	[`couchbase:enterprise-6.0.5`](#couchbaseenterprise-605)
-	[`couchbase:enterprise-6.6.2`](#couchbaseenterprise-662)
-	[`couchbase:enterprise-7.0.0-beta`](#couchbaseenterprise-700-beta)
-	[`couchbase:latest`](#couchbaselatest)

## `couchbase:6.0.5`

```console
$ docker pull couchbase@sha256:7b96e89ef0f60866c705b9661f01417a3ce2ddcfd625c974faec81d091220702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:6.0.5` - linux; amd64

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

## `couchbase:6.6.2`

```console
$ docker pull couchbase@sha256:8751c72e9a5250c711e40d609f5f91bc59570ce154f0b255f4eab45af335eeaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:6.6.2` - linux; amd64

```console
$ docker pull couchbase@sha256:caa5da5b014b06b18bf23b028a73807517a85d9f8de61034d7c72d7b1b68d056
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.9 MB (549932596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af423ed32e366e7cf4554784c3863bf39b5546caa9bd673f2a3dc688d0ec432`
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
# Fri, 23 Apr 2021 23:12:01 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 23 Apr 2021 23:12:02 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Fri, 23 Apr 2021 23:12:02 GMT
ARG CB_VERSION=6.6.2
# Fri, 23 Apr 2021 23:12:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2
# Fri, 23 Apr 2021 23:12:02 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb
# Fri, 23 Apr 2021 23:12:03 GMT
ARG CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901
# Fri, 23 Apr 2021 23:12:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 23 Apr 2021 23:12:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901 CB_VERSION=6.6.2
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 23 Apr 2021 23:12:57 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901 CB_VERSION=6.6.2
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Fri, 23 Apr 2021 23:13:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901 CB_VERSION=6.6.2
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 23 Apr 2021 23:13:02 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 23 Apr 2021 23:13:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901 CB_VERSION=6.6.2
RUN chown -R couchbase:couchbase /etc/service
# Fri, 23 Apr 2021 23:13:03 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 23 Apr 2021 23:13:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901 CB_VERSION=6.6.2
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 23 Apr 2021 23:13:05 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901 CB_VERSION=6.6.2
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 23 Apr 2021 23:13:06 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 23 Apr 2021 23:13:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 23 Apr 2021 23:13:06 GMT
CMD ["couchbase-server"]
# Fri, 23 Apr 2021 23:13:06 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 23 Apr 2021 23:13:06 GMT
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
	-	`sha256:c40c513b90a3a5bcb7f5f15dc2a983554305d585d944578130e03108493148bc`  
		Last Modified: Fri, 23 Apr 2021 23:18:43 GMT  
		Size: 5.8 MB (5833752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1f453513ef950ec91beaded0343dcdbf032b28aa40e82b0acd0bfbcfca7229`  
		Last Modified: Fri, 23 Apr 2021 23:18:41 GMT  
		Size: 2.1 KB (2079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49fb83af01f8a94d408a24781f1c77890ce3fff5d62f1512dd0a5eded95c0482`  
		Last Modified: Fri, 23 Apr 2021 23:19:57 GMT  
		Size: 497.7 MB (497720349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6b306fdf033c4070487ea46043c7884bb67f35f6125808b47834fa4771912a`  
		Last Modified: Fri, 23 Apr 2021 23:18:41 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76df32a98f35e01a703925c7202ec8d663c6c84dfd0f0bf2d25501f241d26ff4`  
		Last Modified: Fri, 23 Apr 2021 23:18:41 GMT  
		Size: 433.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c397fed50d7adaeabe853c0644f5bf1b8b9aee9a73744bf4c3f3446eb4de4d`  
		Last Modified: Fri, 23 Apr 2021 23:18:38 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a74dc1fcdd9c1c06dacbe6b522838b16947af175dee4a9fc91acfa7e0fc264`  
		Last Modified: Fri, 23 Apr 2021 23:18:38 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61efea708740e1b858be2d6d65018fb662bf7d0eca6e5db534dff9f46d702661`  
		Last Modified: Fri, 23 Apr 2021 23:18:38 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4638d2c9b6424e8f36a00e4f1f5fc4cad815c39f3c12d1f94d9b29dc799e6f`  
		Last Modified: Fri, 23 Apr 2021 23:18:38 GMT  
		Size: 118.1 KB (118073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b028c8df2f893a44004f4e0c22630c0d9ff7563ff8669b49ab53762a29f842a`  
		Last Modified: Fri, 23 Apr 2021 23:18:38 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:7.0.0-beta`

```console
$ docker pull couchbase@sha256:aed5d206af89ea11245e4bf268b116bc2bf565e8afd2eafbf7df58fc7d1cf861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:7.0.0-beta` - linux; amd64

```console
$ docker pull couchbase@sha256:1b6a19d2130ef5aa61c71bc9bed27e626237e0df166c7b68529f5ca0efa98517
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **625.8 MB (625802616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b5ac5f99b3cfc54e9590951f971845df4a155f1391dbc7b8cdfed15eece26a3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:34 GMT
ADD file:5c44a80f547b7d68b550b0e64aef898b361666857abf9a5c8f3f8d0567b8e8e4 in / 
# Fri, 23 Apr 2021 22:21:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:37 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:09:02 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Fri, 23 Apr 2021 23:09:21 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 23 Apr 2021 23:09:22 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Fri, 23 Apr 2021 23:09:22 GMT
ARG CB_VERSION=7.0.0-beta
# Fri, 23 Apr 2021 23:09:23 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta
# Fri, 23 Apr 2021 23:09:23 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb
# Fri, 23 Apr 2021 23:09:23 GMT
ARG CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6
# Fri, 23 Apr 2021 23:09:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 23 Apr 2021 23:09:24 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6 CB_VERSION=7.0.0-beta
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 23 Apr 2021 23:10:25 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6 CB_VERSION=7.0.0-beta
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Fri, 23 Apr 2021 23:10:30 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6 CB_VERSION=7.0.0-beta
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 23 Apr 2021 23:10:30 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 23 Apr 2021 23:10:31 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6 CB_VERSION=7.0.0-beta
RUN chown -R couchbase:couchbase /etc/service
# Fri, 23 Apr 2021 23:10:31 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 23 Apr 2021 23:10:32 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6 CB_VERSION=7.0.0-beta
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 23 Apr 2021 23:10:33 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6 CB_VERSION=7.0.0-beta
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 23 Apr 2021 23:10:34 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 23 Apr 2021 23:10:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 23 Apr 2021 23:10:34 GMT
CMD ["couchbase-server"]
# Fri, 23 Apr 2021 23:10:34 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 23 Apr 2021 23:10:34 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:345e3491a907bb7c6f1bdddcf4a94284b8b6ddd77eb7d93f09432b17b20f2bbe`  
		Last Modified: Fri, 16 Apr 2021 15:20:19 GMT  
		Size: 28.5 MB (28539626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57671312ef6fdbecf340e5fed0fb0863350cd806c92b1fdd7978adbd02afc5c3`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9250ddb7d0fa6d13302c7c3e6a0aa40390e42424caed1e5289077ee4054709`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7936dfaada24f79bafe7aa3445a7d6cc71d2accb0dd3bc9edefb0fa557ebea99`  
		Last Modified: Fri, 23 Apr 2021 23:16:03 GMT  
		Size: 6.3 MB (6273226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa99224a9ececc210521261656e3641be6a69810d5fae3dc0e1d7ec28b3dfc34`  
		Last Modified: Fri, 23 Apr 2021 23:15:57 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4643d4da00876529596c8ef491faa1ecaaef06076d337327a42dcd469cfe26a`  
		Last Modified: Fri, 23 Apr 2021 23:15:57 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed03712a6d2286ba67f1ad6f3126f1c9cde5995d93ec20486bcfaa6b69773f4`  
		Last Modified: Fri, 23 Apr 2021 23:17:18 GMT  
		Size: 590.9 MB (590858600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100edec8d6dec14756fb5f17efb144b9722989552b47e08561a818f3aed7275d`  
		Last Modified: Fri, 23 Apr 2021 23:15:57 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a88af01b1d7cf6f40473508e357e6d593686d2f4f90d131707c493b8a4fe45a`  
		Last Modified: Fri, 23 Apr 2021 23:15:57 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030143abd5793c25bc4e60d5b2fd399c0f55e6e48979b76703ad7aaf97f48583`  
		Last Modified: Fri, 23 Apr 2021 23:15:54 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb1f4857061863a6cb3696690c7c5e7608ff350b957f1996ca6ad432fee196b`  
		Last Modified: Fri, 23 Apr 2021 23:15:54 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a1f8d283e1c9bdf449cbcf3dd8dcbfa58f1c01a91dd34f01c56611fbe4fd502`  
		Last Modified: Fri, 23 Apr 2021 23:15:54 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b404b6274af16d841bb26a2a6fc508fa2a651895a548be86156a0ef0f597a18`  
		Last Modified: Fri, 23 Apr 2021 23:15:54 GMT  
		Size: 125.9 KB (125890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fddba050fadc5cc505c5536d6392b318385b12867bbefe7bd344926e58f19955`  
		Last Modified: Fri, 23 Apr 2021 23:15:54 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community`

```console
$ docker pull couchbase@sha256:d4c28a6d645289f0c85806571305a4c2075654c6d8ef06d10ff71f49f3232242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:community` - linux; amd64

```console
$ docker pull couchbase@sha256:f7272f5b77380fe8a62cc8c5973b1bf0d16e9fa05f6ac09feba9eea876146181
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.8 MB (371784638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c620e2675fd51fec05e730679714d2a9aefef1d6d9a6a22423f0a39a49c20a1`
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
# Fri, 23 Apr 2021 23:12:01 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 23 Apr 2021 23:12:02 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Fri, 23 Apr 2021 23:13:23 GMT
ARG CB_VERSION=6.6.0
# Fri, 23 Apr 2021 23:13:23 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0
# Fri, 23 Apr 2021 23:13:23 GMT
ARG CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb
# Fri, 23 Apr 2021 23:13:24 GMT
ARG CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e
# Fri, 23 Apr 2021 23:13:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 23 Apr 2021 23:13:25 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e CB_VERSION=6.6.0
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 23 Apr 2021 23:14:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e CB_VERSION=6.6.0
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Fri, 23 Apr 2021 23:14:05 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e CB_VERSION=6.6.0
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 23 Apr 2021 23:14:05 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 23 Apr 2021 23:14:07 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e CB_VERSION=6.6.0
RUN chown -R couchbase:couchbase /etc/service
# Fri, 23 Apr 2021 23:14:07 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 23 Apr 2021 23:14:08 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e CB_VERSION=6.6.0
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 23 Apr 2021 23:14:09 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e CB_VERSION=6.6.0
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 23 Apr 2021 23:14:09 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 23 Apr 2021 23:14:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 23 Apr 2021 23:14:10 GMT
CMD ["couchbase-server"]
# Fri, 23 Apr 2021 23:14:10 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 23 Apr 2021 23:14:10 GMT
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
	-	`sha256:c40c513b90a3a5bcb7f5f15dc2a983554305d585d944578130e03108493148bc`  
		Last Modified: Fri, 23 Apr 2021 23:18:43 GMT  
		Size: 5.8 MB (5833752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e71050d3c5a966db9ecc6b47d00497be9653126f5a68fa3bba239777645d9cd`  
		Last Modified: Fri, 23 Apr 2021 23:20:23 GMT  
		Size: 2.1 KB (2076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:277f962a6fd2888cecb621e1f65ddfa3bcff8d9e1ada3868ea971e15a0ccc95d`  
		Last Modified: Fri, 23 Apr 2021 23:21:00 GMT  
		Size: 319.6 MB (319572391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360e22a797af328303ed9330893654904b2de46fb14095d509dc6d641e7c2d70`  
		Last Modified: Fri, 23 Apr 2021 23:20:20 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6ed95631df30774f65adf8186ca57e5917c7a6971f80ee7a30309ae760a61bf`  
		Last Modified: Fri, 23 Apr 2021 23:20:20 GMT  
		Size: 433.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3648db6783cceb36aebbccecd78c25b389b92c37a06ddd9bcf321c963664ad52`  
		Last Modified: Fri, 23 Apr 2021 23:20:20 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95faa32d637551df83d7e37490362422bc3fe3f96b807f7cdd22a1dbd8e532e`  
		Last Modified: Fri, 23 Apr 2021 23:20:20 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e72b9534929ec3aa6c2f8c8a758f8de389cfb9519463ee37c158a87950d8295`  
		Last Modified: Fri, 23 Apr 2021 23:20:17 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c421270be8bf2f15635de7df8ce025e5d5ee58874ec810f8d0fbeaa5b0020244`  
		Last Modified: Fri, 23 Apr 2021 23:20:17 GMT  
		Size: 118.1 KB (118074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee07800f881b4331b170827f3410222a3c9a2848e16ebb799b3cf98a0b98d853`  
		Last Modified: Fri, 23 Apr 2021 23:20:17 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community-6.6.0`

```console
$ docker pull couchbase@sha256:d4c28a6d645289f0c85806571305a4c2075654c6d8ef06d10ff71f49f3232242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:community-6.6.0` - linux; amd64

```console
$ docker pull couchbase@sha256:f7272f5b77380fe8a62cc8c5973b1bf0d16e9fa05f6ac09feba9eea876146181
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.8 MB (371784638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c620e2675fd51fec05e730679714d2a9aefef1d6d9a6a22423f0a39a49c20a1`
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
# Fri, 23 Apr 2021 23:12:01 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 23 Apr 2021 23:12:02 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Fri, 23 Apr 2021 23:13:23 GMT
ARG CB_VERSION=6.6.0
# Fri, 23 Apr 2021 23:13:23 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0
# Fri, 23 Apr 2021 23:13:23 GMT
ARG CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb
# Fri, 23 Apr 2021 23:13:24 GMT
ARG CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e
# Fri, 23 Apr 2021 23:13:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 23 Apr 2021 23:13:25 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e CB_VERSION=6.6.0
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 23 Apr 2021 23:14:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e CB_VERSION=6.6.0
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Fri, 23 Apr 2021 23:14:05 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e CB_VERSION=6.6.0
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 23 Apr 2021 23:14:05 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 23 Apr 2021 23:14:07 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e CB_VERSION=6.6.0
RUN chown -R couchbase:couchbase /etc/service
# Fri, 23 Apr 2021 23:14:07 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 23 Apr 2021 23:14:08 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e CB_VERSION=6.6.0
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 23 Apr 2021 23:14:09 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e CB_VERSION=6.6.0
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 23 Apr 2021 23:14:09 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 23 Apr 2021 23:14:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 23 Apr 2021 23:14:10 GMT
CMD ["couchbase-server"]
# Fri, 23 Apr 2021 23:14:10 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 23 Apr 2021 23:14:10 GMT
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
	-	`sha256:c40c513b90a3a5bcb7f5f15dc2a983554305d585d944578130e03108493148bc`  
		Last Modified: Fri, 23 Apr 2021 23:18:43 GMT  
		Size: 5.8 MB (5833752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e71050d3c5a966db9ecc6b47d00497be9653126f5a68fa3bba239777645d9cd`  
		Last Modified: Fri, 23 Apr 2021 23:20:23 GMT  
		Size: 2.1 KB (2076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:277f962a6fd2888cecb621e1f65ddfa3bcff8d9e1ada3868ea971e15a0ccc95d`  
		Last Modified: Fri, 23 Apr 2021 23:21:00 GMT  
		Size: 319.6 MB (319572391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360e22a797af328303ed9330893654904b2de46fb14095d509dc6d641e7c2d70`  
		Last Modified: Fri, 23 Apr 2021 23:20:20 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6ed95631df30774f65adf8186ca57e5917c7a6971f80ee7a30309ae760a61bf`  
		Last Modified: Fri, 23 Apr 2021 23:20:20 GMT  
		Size: 433.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3648db6783cceb36aebbccecd78c25b389b92c37a06ddd9bcf321c963664ad52`  
		Last Modified: Fri, 23 Apr 2021 23:20:20 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95faa32d637551df83d7e37490362422bc3fe3f96b807f7cdd22a1dbd8e532e`  
		Last Modified: Fri, 23 Apr 2021 23:20:20 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e72b9534929ec3aa6c2f8c8a758f8de389cfb9519463ee37c158a87950d8295`  
		Last Modified: Fri, 23 Apr 2021 23:20:17 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c421270be8bf2f15635de7df8ce025e5d5ee58874ec810f8d0fbeaa5b0020244`  
		Last Modified: Fri, 23 Apr 2021 23:20:17 GMT  
		Size: 118.1 KB (118074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee07800f881b4331b170827f3410222a3c9a2848e16ebb799b3cf98a0b98d853`  
		Last Modified: Fri, 23 Apr 2021 23:20:17 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community-7.0.0-beta`

```console
$ docker pull couchbase@sha256:51991eb3d0683c616ccd0f851a24824172932593416f293c60d2fc4994295fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:community-7.0.0-beta` - linux; amd64

```console
$ docker pull couchbase@sha256:d389e970f8bacc02b0b5c4dbbab9fbdd27a84196599f1d9cfa5eae1dbcf604ee
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.7 MB (431739527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbbe9e529f7d187a702a9c03daa9272ab84311b7084813a176795682cd720ea5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:34 GMT
ADD file:5c44a80f547b7d68b550b0e64aef898b361666857abf9a5c8f3f8d0567b8e8e4 in / 
# Fri, 23 Apr 2021 22:21:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:37 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:09:02 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Fri, 23 Apr 2021 23:09:21 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 23 Apr 2021 23:09:22 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Fri, 23 Apr 2021 23:09:22 GMT
ARG CB_VERSION=7.0.0-beta
# Fri, 23 Apr 2021 23:09:23 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta
# Fri, 23 Apr 2021 23:10:43 GMT
ARG CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb
# Fri, 23 Apr 2021 23:10:43 GMT
ARG CB_SHA256=51e843e9d2b5ef746353d79c044f17e4f9be0866673bd6fda01da27a0edf9fc9
# Fri, 23 Apr 2021 23:10:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 23 Apr 2021 23:10:44 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=51e843e9d2b5ef746353d79c044f17e4f9be0866673bd6fda01da27a0edf9fc9 CB_VERSION=7.0.0-beta
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 23 Apr 2021 23:11:30 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=51e843e9d2b5ef746353d79c044f17e4f9be0866673bd6fda01da27a0edf9fc9 CB_VERSION=7.0.0-beta
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Fri, 23 Apr 2021 23:11:34 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=51e843e9d2b5ef746353d79c044f17e4f9be0866673bd6fda01da27a0edf9fc9 CB_VERSION=7.0.0-beta
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 23 Apr 2021 23:11:34 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 23 Apr 2021 23:11:35 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=51e843e9d2b5ef746353d79c044f17e4f9be0866673bd6fda01da27a0edf9fc9 CB_VERSION=7.0.0-beta
RUN chown -R couchbase:couchbase /etc/service
# Fri, 23 Apr 2021 23:11:35 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 23 Apr 2021 23:11:36 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=51e843e9d2b5ef746353d79c044f17e4f9be0866673bd6fda01da27a0edf9fc9 CB_VERSION=7.0.0-beta
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 23 Apr 2021 23:11:37 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=51e843e9d2b5ef746353d79c044f17e4f9be0866673bd6fda01da27a0edf9fc9 CB_VERSION=7.0.0-beta
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 23 Apr 2021 23:11:37 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 23 Apr 2021 23:11:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 23 Apr 2021 23:11:38 GMT
CMD ["couchbase-server"]
# Fri, 23 Apr 2021 23:11:38 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 23 Apr 2021 23:11:38 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:345e3491a907bb7c6f1bdddcf4a94284b8b6ddd77eb7d93f09432b17b20f2bbe`  
		Last Modified: Fri, 16 Apr 2021 15:20:19 GMT  
		Size: 28.5 MB (28539626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57671312ef6fdbecf340e5fed0fb0863350cd806c92b1fdd7978adbd02afc5c3`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9250ddb7d0fa6d13302c7c3e6a0aa40390e42424caed1e5289077ee4054709`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7936dfaada24f79bafe7aa3445a7d6cc71d2accb0dd3bc9edefb0fa557ebea99`  
		Last Modified: Fri, 23 Apr 2021 23:16:03 GMT  
		Size: 6.3 MB (6273226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa99224a9ececc210521261656e3641be6a69810d5fae3dc0e1d7ec28b3dfc34`  
		Last Modified: Fri, 23 Apr 2021 23:15:57 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aaf535e1b8ae8e167aa59f1f99c1ea96b069b1139cf31ac6e27afddbb36e1c5`  
		Last Modified: Fri, 23 Apr 2021 23:17:35 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2ba326669bc73839ea36011c6df730e90bcda0da455e533d5bf14722d2d261`  
		Last Modified: Fri, 23 Apr 2021 23:18:29 GMT  
		Size: 396.8 MB (396795514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ec5675dff9faa3dffd9bbbafd2d94e308538bbe6f3d04d4707b1dc12b75be5`  
		Last Modified: Fri, 23 Apr 2021 23:17:35 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f9927c81ac34e46e91d14609af80e96753debb02fdf9967c9640e089bbf51e`  
		Last Modified: Fri, 23 Apr 2021 23:17:34 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec646a7b3dfde0e85b7beffa9f477615d7536bcdef316ebcbd5aa48d203145f4`  
		Last Modified: Fri, 23 Apr 2021 23:17:32 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1e3a06ddb8fefd5811e61fdb4e4bd5ef4ffd37826ff249dd2df76c8b19af6c`  
		Last Modified: Fri, 23 Apr 2021 23:17:32 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e047066a24290ea4238d6aba5f68a7e26bdf452c21b933d96ff60fa498faa16f`  
		Last Modified: Fri, 23 Apr 2021 23:17:32 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05638d1a9bc19353cfb6339c4ef687baf8bde544aa01a9ec1eeeeda9c41e872`  
		Last Modified: Fri, 23 Apr 2021 23:17:32 GMT  
		Size: 125.9 KB (125882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8419ec211353eb04cf844121e7ca1527d77807ca3d3ee1b83ababbb4f860bc`  
		Last Modified: Fri, 23 Apr 2021 23:17:32 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise`

```console
$ docker pull couchbase@sha256:8751c72e9a5250c711e40d609f5f91bc59570ce154f0b255f4eab45af335eeaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise` - linux; amd64

```console
$ docker pull couchbase@sha256:caa5da5b014b06b18bf23b028a73807517a85d9f8de61034d7c72d7b1b68d056
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.9 MB (549932596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af423ed32e366e7cf4554784c3863bf39b5546caa9bd673f2a3dc688d0ec432`
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
# Fri, 23 Apr 2021 23:12:01 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 23 Apr 2021 23:12:02 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Fri, 23 Apr 2021 23:12:02 GMT
ARG CB_VERSION=6.6.2
# Fri, 23 Apr 2021 23:12:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2
# Fri, 23 Apr 2021 23:12:02 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb
# Fri, 23 Apr 2021 23:12:03 GMT
ARG CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901
# Fri, 23 Apr 2021 23:12:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 23 Apr 2021 23:12:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901 CB_VERSION=6.6.2
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 23 Apr 2021 23:12:57 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901 CB_VERSION=6.6.2
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Fri, 23 Apr 2021 23:13:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901 CB_VERSION=6.6.2
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 23 Apr 2021 23:13:02 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 23 Apr 2021 23:13:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901 CB_VERSION=6.6.2
RUN chown -R couchbase:couchbase /etc/service
# Fri, 23 Apr 2021 23:13:03 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 23 Apr 2021 23:13:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901 CB_VERSION=6.6.2
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 23 Apr 2021 23:13:05 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901 CB_VERSION=6.6.2
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 23 Apr 2021 23:13:06 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 23 Apr 2021 23:13:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 23 Apr 2021 23:13:06 GMT
CMD ["couchbase-server"]
# Fri, 23 Apr 2021 23:13:06 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 23 Apr 2021 23:13:06 GMT
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
	-	`sha256:c40c513b90a3a5bcb7f5f15dc2a983554305d585d944578130e03108493148bc`  
		Last Modified: Fri, 23 Apr 2021 23:18:43 GMT  
		Size: 5.8 MB (5833752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1f453513ef950ec91beaded0343dcdbf032b28aa40e82b0acd0bfbcfca7229`  
		Last Modified: Fri, 23 Apr 2021 23:18:41 GMT  
		Size: 2.1 KB (2079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49fb83af01f8a94d408a24781f1c77890ce3fff5d62f1512dd0a5eded95c0482`  
		Last Modified: Fri, 23 Apr 2021 23:19:57 GMT  
		Size: 497.7 MB (497720349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6b306fdf033c4070487ea46043c7884bb67f35f6125808b47834fa4771912a`  
		Last Modified: Fri, 23 Apr 2021 23:18:41 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76df32a98f35e01a703925c7202ec8d663c6c84dfd0f0bf2d25501f241d26ff4`  
		Last Modified: Fri, 23 Apr 2021 23:18:41 GMT  
		Size: 433.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c397fed50d7adaeabe853c0644f5bf1b8b9aee9a73744bf4c3f3446eb4de4d`  
		Last Modified: Fri, 23 Apr 2021 23:18:38 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a74dc1fcdd9c1c06dacbe6b522838b16947af175dee4a9fc91acfa7e0fc264`  
		Last Modified: Fri, 23 Apr 2021 23:18:38 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61efea708740e1b858be2d6d65018fb662bf7d0eca6e5db534dff9f46d702661`  
		Last Modified: Fri, 23 Apr 2021 23:18:38 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4638d2c9b6424e8f36a00e4f1f5fc4cad815c39f3c12d1f94d9b29dc799e6f`  
		Last Modified: Fri, 23 Apr 2021 23:18:38 GMT  
		Size: 118.1 KB (118073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b028c8df2f893a44004f4e0c22630c0d9ff7563ff8669b49ab53762a29f842a`  
		Last Modified: Fri, 23 Apr 2021 23:18:38 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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

## `couchbase:enterprise-6.6.2`

```console
$ docker pull couchbase@sha256:8751c72e9a5250c711e40d609f5f91bc59570ce154f0b255f4eab45af335eeaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise-6.6.2` - linux; amd64

```console
$ docker pull couchbase@sha256:caa5da5b014b06b18bf23b028a73807517a85d9f8de61034d7c72d7b1b68d056
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.9 MB (549932596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af423ed32e366e7cf4554784c3863bf39b5546caa9bd673f2a3dc688d0ec432`
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
# Fri, 23 Apr 2021 23:12:01 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 23 Apr 2021 23:12:02 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Fri, 23 Apr 2021 23:12:02 GMT
ARG CB_VERSION=6.6.2
# Fri, 23 Apr 2021 23:12:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2
# Fri, 23 Apr 2021 23:12:02 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb
# Fri, 23 Apr 2021 23:12:03 GMT
ARG CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901
# Fri, 23 Apr 2021 23:12:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 23 Apr 2021 23:12:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901 CB_VERSION=6.6.2
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 23 Apr 2021 23:12:57 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901 CB_VERSION=6.6.2
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Fri, 23 Apr 2021 23:13:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901 CB_VERSION=6.6.2
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 23 Apr 2021 23:13:02 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 23 Apr 2021 23:13:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901 CB_VERSION=6.6.2
RUN chown -R couchbase:couchbase /etc/service
# Fri, 23 Apr 2021 23:13:03 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 23 Apr 2021 23:13:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901 CB_VERSION=6.6.2
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 23 Apr 2021 23:13:05 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901 CB_VERSION=6.6.2
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 23 Apr 2021 23:13:06 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 23 Apr 2021 23:13:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 23 Apr 2021 23:13:06 GMT
CMD ["couchbase-server"]
# Fri, 23 Apr 2021 23:13:06 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 23 Apr 2021 23:13:06 GMT
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
	-	`sha256:c40c513b90a3a5bcb7f5f15dc2a983554305d585d944578130e03108493148bc`  
		Last Modified: Fri, 23 Apr 2021 23:18:43 GMT  
		Size: 5.8 MB (5833752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1f453513ef950ec91beaded0343dcdbf032b28aa40e82b0acd0bfbcfca7229`  
		Last Modified: Fri, 23 Apr 2021 23:18:41 GMT  
		Size: 2.1 KB (2079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49fb83af01f8a94d408a24781f1c77890ce3fff5d62f1512dd0a5eded95c0482`  
		Last Modified: Fri, 23 Apr 2021 23:19:57 GMT  
		Size: 497.7 MB (497720349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6b306fdf033c4070487ea46043c7884bb67f35f6125808b47834fa4771912a`  
		Last Modified: Fri, 23 Apr 2021 23:18:41 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76df32a98f35e01a703925c7202ec8d663c6c84dfd0f0bf2d25501f241d26ff4`  
		Last Modified: Fri, 23 Apr 2021 23:18:41 GMT  
		Size: 433.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c397fed50d7adaeabe853c0644f5bf1b8b9aee9a73744bf4c3f3446eb4de4d`  
		Last Modified: Fri, 23 Apr 2021 23:18:38 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a74dc1fcdd9c1c06dacbe6b522838b16947af175dee4a9fc91acfa7e0fc264`  
		Last Modified: Fri, 23 Apr 2021 23:18:38 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61efea708740e1b858be2d6d65018fb662bf7d0eca6e5db534dff9f46d702661`  
		Last Modified: Fri, 23 Apr 2021 23:18:38 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4638d2c9b6424e8f36a00e4f1f5fc4cad815c39f3c12d1f94d9b29dc799e6f`  
		Last Modified: Fri, 23 Apr 2021 23:18:38 GMT  
		Size: 118.1 KB (118073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b028c8df2f893a44004f4e0c22630c0d9ff7563ff8669b49ab53762a29f842a`  
		Last Modified: Fri, 23 Apr 2021 23:18:38 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-7.0.0-beta`

```console
$ docker pull couchbase@sha256:aed5d206af89ea11245e4bf268b116bc2bf565e8afd2eafbf7df58fc7d1cf861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise-7.0.0-beta` - linux; amd64

```console
$ docker pull couchbase@sha256:1b6a19d2130ef5aa61c71bc9bed27e626237e0df166c7b68529f5ca0efa98517
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **625.8 MB (625802616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b5ac5f99b3cfc54e9590951f971845df4a155f1391dbc7b8cdfed15eece26a3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:34 GMT
ADD file:5c44a80f547b7d68b550b0e64aef898b361666857abf9a5c8f3f8d0567b8e8e4 in / 
# Fri, 23 Apr 2021 22:21:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:37 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:09:02 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Fri, 23 Apr 2021 23:09:21 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 23 Apr 2021 23:09:22 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Fri, 23 Apr 2021 23:09:22 GMT
ARG CB_VERSION=7.0.0-beta
# Fri, 23 Apr 2021 23:09:23 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta
# Fri, 23 Apr 2021 23:09:23 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb
# Fri, 23 Apr 2021 23:09:23 GMT
ARG CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6
# Fri, 23 Apr 2021 23:09:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 23 Apr 2021 23:09:24 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6 CB_VERSION=7.0.0-beta
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 23 Apr 2021 23:10:25 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6 CB_VERSION=7.0.0-beta
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Fri, 23 Apr 2021 23:10:30 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6 CB_VERSION=7.0.0-beta
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 23 Apr 2021 23:10:30 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 23 Apr 2021 23:10:31 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6 CB_VERSION=7.0.0-beta
RUN chown -R couchbase:couchbase /etc/service
# Fri, 23 Apr 2021 23:10:31 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 23 Apr 2021 23:10:32 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6 CB_VERSION=7.0.0-beta
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 23 Apr 2021 23:10:33 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6 CB_VERSION=7.0.0-beta
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 23 Apr 2021 23:10:34 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 23 Apr 2021 23:10:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 23 Apr 2021 23:10:34 GMT
CMD ["couchbase-server"]
# Fri, 23 Apr 2021 23:10:34 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 23 Apr 2021 23:10:34 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:345e3491a907bb7c6f1bdddcf4a94284b8b6ddd77eb7d93f09432b17b20f2bbe`  
		Last Modified: Fri, 16 Apr 2021 15:20:19 GMT  
		Size: 28.5 MB (28539626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57671312ef6fdbecf340e5fed0fb0863350cd806c92b1fdd7978adbd02afc5c3`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9250ddb7d0fa6d13302c7c3e6a0aa40390e42424caed1e5289077ee4054709`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7936dfaada24f79bafe7aa3445a7d6cc71d2accb0dd3bc9edefb0fa557ebea99`  
		Last Modified: Fri, 23 Apr 2021 23:16:03 GMT  
		Size: 6.3 MB (6273226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa99224a9ececc210521261656e3641be6a69810d5fae3dc0e1d7ec28b3dfc34`  
		Last Modified: Fri, 23 Apr 2021 23:15:57 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4643d4da00876529596c8ef491faa1ecaaef06076d337327a42dcd469cfe26a`  
		Last Modified: Fri, 23 Apr 2021 23:15:57 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed03712a6d2286ba67f1ad6f3126f1c9cde5995d93ec20486bcfaa6b69773f4`  
		Last Modified: Fri, 23 Apr 2021 23:17:18 GMT  
		Size: 590.9 MB (590858600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100edec8d6dec14756fb5f17efb144b9722989552b47e08561a818f3aed7275d`  
		Last Modified: Fri, 23 Apr 2021 23:15:57 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a88af01b1d7cf6f40473508e357e6d593686d2f4f90d131707c493b8a4fe45a`  
		Last Modified: Fri, 23 Apr 2021 23:15:57 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030143abd5793c25bc4e60d5b2fd399c0f55e6e48979b76703ad7aaf97f48583`  
		Last Modified: Fri, 23 Apr 2021 23:15:54 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb1f4857061863a6cb3696690c7c5e7608ff350b957f1996ca6ad432fee196b`  
		Last Modified: Fri, 23 Apr 2021 23:15:54 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a1f8d283e1c9bdf449cbcf3dd8dcbfa58f1c01a91dd34f01c56611fbe4fd502`  
		Last Modified: Fri, 23 Apr 2021 23:15:54 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b404b6274af16d841bb26a2a6fc508fa2a651895a548be86156a0ef0f597a18`  
		Last Modified: Fri, 23 Apr 2021 23:15:54 GMT  
		Size: 125.9 KB (125890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fddba050fadc5cc505c5536d6392b318385b12867bbefe7bd344926e58f19955`  
		Last Modified: Fri, 23 Apr 2021 23:15:54 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:latest`

```console
$ docker pull couchbase@sha256:8751c72e9a5250c711e40d609f5f91bc59570ce154f0b255f4eab45af335eeaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:latest` - linux; amd64

```console
$ docker pull couchbase@sha256:caa5da5b014b06b18bf23b028a73807517a85d9f8de61034d7c72d7b1b68d056
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.9 MB (549932596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af423ed32e366e7cf4554784c3863bf39b5546caa9bd673f2a3dc688d0ec432`
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
# Fri, 23 Apr 2021 23:12:01 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 23 Apr 2021 23:12:02 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Fri, 23 Apr 2021 23:12:02 GMT
ARG CB_VERSION=6.6.2
# Fri, 23 Apr 2021 23:12:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2
# Fri, 23 Apr 2021 23:12:02 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb
# Fri, 23 Apr 2021 23:12:03 GMT
ARG CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901
# Fri, 23 Apr 2021 23:12:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 23 Apr 2021 23:12:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901 CB_VERSION=6.6.2
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 23 Apr 2021 23:12:57 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901 CB_VERSION=6.6.2
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Fri, 23 Apr 2021 23:13:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901 CB_VERSION=6.6.2
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 23 Apr 2021 23:13:02 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 23 Apr 2021 23:13:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901 CB_VERSION=6.6.2
RUN chown -R couchbase:couchbase /etc/service
# Fri, 23 Apr 2021 23:13:03 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 23 Apr 2021 23:13:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901 CB_VERSION=6.6.2
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 23 Apr 2021 23:13:05 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901 CB_VERSION=6.6.2
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 23 Apr 2021 23:13:06 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 23 Apr 2021 23:13:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 23 Apr 2021 23:13:06 GMT
CMD ["couchbase-server"]
# Fri, 23 Apr 2021 23:13:06 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 23 Apr 2021 23:13:06 GMT
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
	-	`sha256:c40c513b90a3a5bcb7f5f15dc2a983554305d585d944578130e03108493148bc`  
		Last Modified: Fri, 23 Apr 2021 23:18:43 GMT  
		Size: 5.8 MB (5833752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1f453513ef950ec91beaded0343dcdbf032b28aa40e82b0acd0bfbcfca7229`  
		Last Modified: Fri, 23 Apr 2021 23:18:41 GMT  
		Size: 2.1 KB (2079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49fb83af01f8a94d408a24781f1c77890ce3fff5d62f1512dd0a5eded95c0482`  
		Last Modified: Fri, 23 Apr 2021 23:19:57 GMT  
		Size: 497.7 MB (497720349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6b306fdf033c4070487ea46043c7884bb67f35f6125808b47834fa4771912a`  
		Last Modified: Fri, 23 Apr 2021 23:18:41 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76df32a98f35e01a703925c7202ec8d663c6c84dfd0f0bf2d25501f241d26ff4`  
		Last Modified: Fri, 23 Apr 2021 23:18:41 GMT  
		Size: 433.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c397fed50d7adaeabe853c0644f5bf1b8b9aee9a73744bf4c3f3446eb4de4d`  
		Last Modified: Fri, 23 Apr 2021 23:18:38 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a74dc1fcdd9c1c06dacbe6b522838b16947af175dee4a9fc91acfa7e0fc264`  
		Last Modified: Fri, 23 Apr 2021 23:18:38 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61efea708740e1b858be2d6d65018fb662bf7d0eca6e5db534dff9f46d702661`  
		Last Modified: Fri, 23 Apr 2021 23:18:38 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4638d2c9b6424e8f36a00e4f1f5fc4cad815c39f3c12d1f94d9b29dc799e6f`  
		Last Modified: Fri, 23 Apr 2021 23:18:38 GMT  
		Size: 118.1 KB (118073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b028c8df2f893a44004f4e0c22630c0d9ff7563ff8669b49ab53762a29f842a`  
		Last Modified: Fri, 23 Apr 2021 23:18:38 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
