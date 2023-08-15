## `emqx:latest`

```console
$ docker pull emqx@sha256:0eaea1871100fde78d9a02f3f70a07bdbda92f915144638ab0f2461c0d74628a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:83a4b62cbf0ea2f2550f66c27bf269bcd77e609d42961385dd1af952e25f4603
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102509562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dd7f30618b6cd0cf7b13f76ca61c93f232a9f02963cfa57e9d8dc38f238e68c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:00:12 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:00:13 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 15 Aug 2023 19:19:38 GMT
ENV EMQX_VERSION=5.1.5-build.3
# Tue, 15 Aug 2023 19:19:38 GMT
ENV AMD64_SHA256=0266cccf61389a49ce1462f21d1e645919d54a04ab158f43245407d6df1fcaf0
# Tue, 15 Aug 2023 19:19:39 GMT
ENV ARM64_SHA256=9e92914b65f7110ca26dd57c9374cd8ed9e3384b9280659360bf507cffc1f082
# Tue, 15 Aug 2023 19:19:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 15 Aug 2023 19:19:46 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 15 Aug 2023 19:19:47 GMT
WORKDIR /opt/emqx
# Tue, 15 Aug 2023 19:19:47 GMT
USER emqx
# Tue, 15 Aug 2023 19:19:47 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 15 Aug 2023 19:19:47 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 15 Aug 2023 19:19:47 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 15 Aug 2023 19:19:47 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 15 Aug 2023 19:19:47 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aae0cd767678d99b5128cb9f0b9f0d533d60f80be20eeda6f6530c35a813613`  
		Last Modified: Fri, 28 Jul 2023 01:01:03 GMT  
		Size: 3.0 MB (2987830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bde007415e9cca4e319dea3b886b7d723309116b3ba73372e0de710d2b6b068`  
		Last Modified: Fri, 28 Jul 2023 01:01:02 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d9caee15444c5b631f9f50e0ea049c45591344aeeaa8ed104eec66be5bcafc`  
		Last Modified: Tue, 15 Aug 2023 19:20:10 GMT  
		Size: 68.1 MB (68099115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0a701e9535530d23d7ce64a657de0a3dcc8e363b1c833b9d5036a1bbab3d6f`  
		Last Modified: Tue, 15 Aug 2023 19:20:02 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:571b01a607d8a35308cf66833f78fbfa961244a319c6ad4b7683f2bde85ad44c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92827010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1027f7dd1d77fa089bfeb402c30e855c47097f9fe9079590b2ffc12e076929ed`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:15 GMT
ADD file:085ecd2f941de953afe5513a41a37412d72cbafd982de581ebd2309b3772b51e in / 
# Thu, 27 Jul 2023 23:43:15 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:59:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:59:21 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 15 Aug 2023 19:39:30 GMT
ENV EMQX_VERSION=5.1.5-build.3
# Tue, 15 Aug 2023 19:39:30 GMT
ENV AMD64_SHA256=0266cccf61389a49ce1462f21d1e645919d54a04ab158f43245407d6df1fcaf0
# Tue, 15 Aug 2023 19:39:30 GMT
ENV ARM64_SHA256=9e92914b65f7110ca26dd57c9374cd8ed9e3384b9280659360bf507cffc1f082
# Tue, 15 Aug 2023 19:39:30 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 15 Aug 2023 19:39:37 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 15 Aug 2023 19:39:38 GMT
WORKDIR /opt/emqx
# Tue, 15 Aug 2023 19:39:38 GMT
USER emqx
# Tue, 15 Aug 2023 19:39:38 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 15 Aug 2023 19:39:38 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 15 Aug 2023 19:39:38 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 15 Aug 2023 19:39:38 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 15 Aug 2023 19:39:38 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:795b5d192ab1819e75375fead3f2f931bd86046e3308224944f16a5ec3b97424`  
		Last Modified: Thu, 27 Jul 2023 23:47:14 GMT  
		Size: 30.1 MB (30062831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf0f15215e9823dbfc2d709d9ca85f9fdb46f7665c3621f3699f4bed019d389`  
		Last Modified: Fri, 28 Jul 2023 02:00:04 GMT  
		Size: 3.0 MB (3002976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8e62bd45d0ac350812046fdc53fe9edeb5523a9bad244ef297b7eda7e76e15`  
		Last Modified: Fri, 28 Jul 2023 02:00:03 GMT  
		Size: 4.1 KB (4117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a43a49720f5a58d6f0679c62cf1e10a832389719b9a53b7b89f8b083e23a52`  
		Last Modified: Tue, 15 Aug 2023 19:39:53 GMT  
		Size: 59.8 MB (59756183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aff06bf5175c6851bdd06cd2ffb6ab3fca26429adc5cd4ca6179fa669964fc9`  
		Last Modified: Tue, 15 Aug 2023 19:39:48 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
