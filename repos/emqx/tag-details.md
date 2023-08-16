<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:5`](#emqx5)
-	[`emqx:5.0`](#emqx50)
-	[`emqx:5.0.26`](#emqx5026)
-	[`emqx:5.1`](#emqx51)
-	[`emqx:5.1.5-build.3`](#emqx515-build3)
-	[`emqx:latest`](#emqxlatest)

## `emqx:5`

```console
$ docker pull emqx@sha256:476bcff71dbf6ae1ffd338d24fec301e2101dad26e205a8058e171319de069a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5` - linux; amd64

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

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:d8d318d722cab61c54a582a4d51faf98595739b0486067fa105106ee7b350f72
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92826997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914726878dfc44bb0847599bd5e1a0b0364404d1213d9ad1b589efd3398cb8f7`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 02:04:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 02:04:03 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 16 Aug 2023 02:04:14 GMT
ENV EMQX_VERSION=5.1.5-build.3
# Wed, 16 Aug 2023 02:04:14 GMT
ENV AMD64_SHA256=0266cccf61389a49ce1462f21d1e645919d54a04ab158f43245407d6df1fcaf0
# Wed, 16 Aug 2023 02:04:15 GMT
ENV ARM64_SHA256=9e92914b65f7110ca26dd57c9374cd8ed9e3384b9280659360bf507cffc1f082
# Wed, 16 Aug 2023 02:04:15 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 16 Aug 2023 02:04:20 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Wed, 16 Aug 2023 02:04:20 GMT
WORKDIR /opt/emqx
# Wed, 16 Aug 2023 02:04:21 GMT
USER emqx
# Wed, 16 Aug 2023 02:04:21 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 16 Aug 2023 02:04:21 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 16 Aug 2023 02:04:21 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 16 Aug 2023 02:04:21 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 16 Aug 2023 02:04:21 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf9935b6a5db89f92b605f7f0b0af22fb4cea1dcb2fce17fd4394f0b276031a`  
		Last Modified: Wed, 16 Aug 2023 02:04:31 GMT  
		Size: 3.0 MB (3002946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8af255dcc47cd844d6dc7e8fbb203f8650232883ccaa219fb0b5853b69a5a75`  
		Last Modified: Wed, 16 Aug 2023 02:04:30 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e33f97101f8c937743b0ae143802231d013c7c7e5bfb5e8b99cf84fc8513a76`  
		Last Modified: Wed, 16 Aug 2023 02:04:48 GMT  
		Size: 59.8 MB (59756222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f67c7a703b62fd449e1a388004f165ae294913a6df7e9e795c925b582f7c446`  
		Last Modified: Wed, 16 Aug 2023 02:04:43 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.0`

```console
$ docker pull emqx@sha256:b7f6af40051d9a6ee18d9d0e58f6602b5644a0462e9202a65a9646ddb354e777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.0` - linux; amd64

```console
$ docker pull emqx@sha256:fc52de5e495b2127918496f4279ce1175fa131ce3dd3f104ee6589565a02dd34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101982317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1dd67ffa630f220137ee6f5f73b65717f8a54256a8e063c705ffcfc115aed6c`
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
# Fri, 28 Jul 2023 01:00:13 GMT
ENV EMQX_VERSION=5.0.26
# Fri, 28 Jul 2023 01:00:13 GMT
ENV AMD64_SHA256=00f954065fe7fd2f678f2e561578234240cc2cace49fb5cbb5aa7fb450825ffa
# Fri, 28 Jul 2023 01:00:13 GMT
ENV ARM64_SHA256=0b013f0b900e687c1ef3ed73bd6fef268b5492d12a3083ffd0d75c8e3935b4ae
# Fri, 28 Jul 2023 01:00:13 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 28 Jul 2023 01:00:19 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Fri, 28 Jul 2023 01:00:20 GMT
WORKDIR /opt/emqx
# Fri, 28 Jul 2023 01:00:20 GMT
USER emqx
# Fri, 28 Jul 2023 01:00:20 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 28 Jul 2023 01:00:20 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Fri, 28 Jul 2023 01:00:20 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Fri, 28 Jul 2023 01:00:20 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 01:00:20 GMT
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
	-	`sha256:6788aa6e14f2bb644a8ea6308bc63a5293c7100c1cf56c89d166f0fbafc7f452`  
		Last Modified: Fri, 28 Jul 2023 01:01:11 GMT  
		Size: 67.6 MB (67571870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0def11967b7af57de71d52d148a123356502d2957e2fa39a551edd11526ae9dc`  
		Last Modified: Fri, 28 Jul 2023 01:01:02 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.0` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:a16517d504734871297cd6bc22f0218c447b38ba186708e30c1b4b13fdb8515d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93060156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a39b7d91dd1c3865cdab2db949ef618aa84b51270dcef9f322596b174b670b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 02:04:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 02:04:03 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 16 Aug 2023 02:04:03 GMT
ENV EMQX_VERSION=5.0.26
# Wed, 16 Aug 2023 02:04:03 GMT
ENV AMD64_SHA256=00f954065fe7fd2f678f2e561578234240cc2cace49fb5cbb5aa7fb450825ffa
# Wed, 16 Aug 2023 02:04:03 GMT
ENV ARM64_SHA256=0b013f0b900e687c1ef3ed73bd6fef268b5492d12a3083ffd0d75c8e3935b4ae
# Wed, 16 Aug 2023 02:04:04 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 16 Aug 2023 02:04:10 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 16 Aug 2023 02:04:10 GMT
WORKDIR /opt/emqx
# Wed, 16 Aug 2023 02:04:10 GMT
USER emqx
# Wed, 16 Aug 2023 02:04:11 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 16 Aug 2023 02:04:11 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 16 Aug 2023 02:04:11 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 16 Aug 2023 02:04:11 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 16 Aug 2023 02:04:11 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf9935b6a5db89f92b605f7f0b0af22fb4cea1dcb2fce17fd4394f0b276031a`  
		Last Modified: Wed, 16 Aug 2023 02:04:31 GMT  
		Size: 3.0 MB (3002946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8af255dcc47cd844d6dc7e8fbb203f8650232883ccaa219fb0b5853b69a5a75`  
		Last Modified: Wed, 16 Aug 2023 02:04:30 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c8d6f86cad7962e873b954b5638499c5b7e4457159d0032cfa7d552e606910`  
		Last Modified: Wed, 16 Aug 2023 02:04:36 GMT  
		Size: 60.0 MB (59989381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57bc415c236d3beef60d59da5052c2daaec999f2f81a314d56ae98182d5d19b`  
		Last Modified: Wed, 16 Aug 2023 02:04:30 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.0.26`

```console
$ docker pull emqx@sha256:b7f6af40051d9a6ee18d9d0e58f6602b5644a0462e9202a65a9646ddb354e777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.0.26` - linux; amd64

```console
$ docker pull emqx@sha256:fc52de5e495b2127918496f4279ce1175fa131ce3dd3f104ee6589565a02dd34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101982317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1dd67ffa630f220137ee6f5f73b65717f8a54256a8e063c705ffcfc115aed6c`
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
# Fri, 28 Jul 2023 01:00:13 GMT
ENV EMQX_VERSION=5.0.26
# Fri, 28 Jul 2023 01:00:13 GMT
ENV AMD64_SHA256=00f954065fe7fd2f678f2e561578234240cc2cace49fb5cbb5aa7fb450825ffa
# Fri, 28 Jul 2023 01:00:13 GMT
ENV ARM64_SHA256=0b013f0b900e687c1ef3ed73bd6fef268b5492d12a3083ffd0d75c8e3935b4ae
# Fri, 28 Jul 2023 01:00:13 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 28 Jul 2023 01:00:19 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Fri, 28 Jul 2023 01:00:20 GMT
WORKDIR /opt/emqx
# Fri, 28 Jul 2023 01:00:20 GMT
USER emqx
# Fri, 28 Jul 2023 01:00:20 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 28 Jul 2023 01:00:20 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Fri, 28 Jul 2023 01:00:20 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Fri, 28 Jul 2023 01:00:20 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 01:00:20 GMT
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
	-	`sha256:6788aa6e14f2bb644a8ea6308bc63a5293c7100c1cf56c89d166f0fbafc7f452`  
		Last Modified: Fri, 28 Jul 2023 01:01:11 GMT  
		Size: 67.6 MB (67571870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0def11967b7af57de71d52d148a123356502d2957e2fa39a551edd11526ae9dc`  
		Last Modified: Fri, 28 Jul 2023 01:01:02 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.0.26` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:a16517d504734871297cd6bc22f0218c447b38ba186708e30c1b4b13fdb8515d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93060156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a39b7d91dd1c3865cdab2db949ef618aa84b51270dcef9f322596b174b670b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 02:04:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 02:04:03 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 16 Aug 2023 02:04:03 GMT
ENV EMQX_VERSION=5.0.26
# Wed, 16 Aug 2023 02:04:03 GMT
ENV AMD64_SHA256=00f954065fe7fd2f678f2e561578234240cc2cace49fb5cbb5aa7fb450825ffa
# Wed, 16 Aug 2023 02:04:03 GMT
ENV ARM64_SHA256=0b013f0b900e687c1ef3ed73bd6fef268b5492d12a3083ffd0d75c8e3935b4ae
# Wed, 16 Aug 2023 02:04:04 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 16 Aug 2023 02:04:10 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 16 Aug 2023 02:04:10 GMT
WORKDIR /opt/emqx
# Wed, 16 Aug 2023 02:04:10 GMT
USER emqx
# Wed, 16 Aug 2023 02:04:11 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 16 Aug 2023 02:04:11 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 16 Aug 2023 02:04:11 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 16 Aug 2023 02:04:11 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 16 Aug 2023 02:04:11 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf9935b6a5db89f92b605f7f0b0af22fb4cea1dcb2fce17fd4394f0b276031a`  
		Last Modified: Wed, 16 Aug 2023 02:04:31 GMT  
		Size: 3.0 MB (3002946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8af255dcc47cd844d6dc7e8fbb203f8650232883ccaa219fb0b5853b69a5a75`  
		Last Modified: Wed, 16 Aug 2023 02:04:30 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c8d6f86cad7962e873b954b5638499c5b7e4457159d0032cfa7d552e606910`  
		Last Modified: Wed, 16 Aug 2023 02:04:36 GMT  
		Size: 60.0 MB (59989381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57bc415c236d3beef60d59da5052c2daaec999f2f81a314d56ae98182d5d19b`  
		Last Modified: Wed, 16 Aug 2023 02:04:30 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.1`

```console
$ docker pull emqx@sha256:476bcff71dbf6ae1ffd338d24fec301e2101dad26e205a8058e171319de069a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.1` - linux; amd64

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

### `emqx:5.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:d8d318d722cab61c54a582a4d51faf98595739b0486067fa105106ee7b350f72
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92826997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914726878dfc44bb0847599bd5e1a0b0364404d1213d9ad1b589efd3398cb8f7`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 02:04:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 02:04:03 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 16 Aug 2023 02:04:14 GMT
ENV EMQX_VERSION=5.1.5-build.3
# Wed, 16 Aug 2023 02:04:14 GMT
ENV AMD64_SHA256=0266cccf61389a49ce1462f21d1e645919d54a04ab158f43245407d6df1fcaf0
# Wed, 16 Aug 2023 02:04:15 GMT
ENV ARM64_SHA256=9e92914b65f7110ca26dd57c9374cd8ed9e3384b9280659360bf507cffc1f082
# Wed, 16 Aug 2023 02:04:15 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 16 Aug 2023 02:04:20 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Wed, 16 Aug 2023 02:04:20 GMT
WORKDIR /opt/emqx
# Wed, 16 Aug 2023 02:04:21 GMT
USER emqx
# Wed, 16 Aug 2023 02:04:21 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 16 Aug 2023 02:04:21 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 16 Aug 2023 02:04:21 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 16 Aug 2023 02:04:21 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 16 Aug 2023 02:04:21 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf9935b6a5db89f92b605f7f0b0af22fb4cea1dcb2fce17fd4394f0b276031a`  
		Last Modified: Wed, 16 Aug 2023 02:04:31 GMT  
		Size: 3.0 MB (3002946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8af255dcc47cd844d6dc7e8fbb203f8650232883ccaa219fb0b5853b69a5a75`  
		Last Modified: Wed, 16 Aug 2023 02:04:30 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e33f97101f8c937743b0ae143802231d013c7c7e5bfb5e8b99cf84fc8513a76`  
		Last Modified: Wed, 16 Aug 2023 02:04:48 GMT  
		Size: 59.8 MB (59756222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f67c7a703b62fd449e1a388004f165ae294913a6df7e9e795c925b582f7c446`  
		Last Modified: Wed, 16 Aug 2023 02:04:43 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.1.5-build.3`

```console
$ docker pull emqx@sha256:476bcff71dbf6ae1ffd338d24fec301e2101dad26e205a8058e171319de069a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.1.5-build.3` - linux; amd64

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

### `emqx:5.1.5-build.3` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:d8d318d722cab61c54a582a4d51faf98595739b0486067fa105106ee7b350f72
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92826997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914726878dfc44bb0847599bd5e1a0b0364404d1213d9ad1b589efd3398cb8f7`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 02:04:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 02:04:03 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 16 Aug 2023 02:04:14 GMT
ENV EMQX_VERSION=5.1.5-build.3
# Wed, 16 Aug 2023 02:04:14 GMT
ENV AMD64_SHA256=0266cccf61389a49ce1462f21d1e645919d54a04ab158f43245407d6df1fcaf0
# Wed, 16 Aug 2023 02:04:15 GMT
ENV ARM64_SHA256=9e92914b65f7110ca26dd57c9374cd8ed9e3384b9280659360bf507cffc1f082
# Wed, 16 Aug 2023 02:04:15 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 16 Aug 2023 02:04:20 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Wed, 16 Aug 2023 02:04:20 GMT
WORKDIR /opt/emqx
# Wed, 16 Aug 2023 02:04:21 GMT
USER emqx
# Wed, 16 Aug 2023 02:04:21 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 16 Aug 2023 02:04:21 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 16 Aug 2023 02:04:21 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 16 Aug 2023 02:04:21 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 16 Aug 2023 02:04:21 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf9935b6a5db89f92b605f7f0b0af22fb4cea1dcb2fce17fd4394f0b276031a`  
		Last Modified: Wed, 16 Aug 2023 02:04:31 GMT  
		Size: 3.0 MB (3002946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8af255dcc47cd844d6dc7e8fbb203f8650232883ccaa219fb0b5853b69a5a75`  
		Last Modified: Wed, 16 Aug 2023 02:04:30 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e33f97101f8c937743b0ae143802231d013c7c7e5bfb5e8b99cf84fc8513a76`  
		Last Modified: Wed, 16 Aug 2023 02:04:48 GMT  
		Size: 59.8 MB (59756222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f67c7a703b62fd449e1a388004f165ae294913a6df7e9e795c925b582f7c446`  
		Last Modified: Wed, 16 Aug 2023 02:04:43 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:latest`

```console
$ docker pull emqx@sha256:476bcff71dbf6ae1ffd338d24fec301e2101dad26e205a8058e171319de069a2
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
$ docker pull emqx@sha256:d8d318d722cab61c54a582a4d51faf98595739b0486067fa105106ee7b350f72
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92826997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914726878dfc44bb0847599bd5e1a0b0364404d1213d9ad1b589efd3398cb8f7`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 02:04:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 02:04:03 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 16 Aug 2023 02:04:14 GMT
ENV EMQX_VERSION=5.1.5-build.3
# Wed, 16 Aug 2023 02:04:14 GMT
ENV AMD64_SHA256=0266cccf61389a49ce1462f21d1e645919d54a04ab158f43245407d6df1fcaf0
# Wed, 16 Aug 2023 02:04:15 GMT
ENV ARM64_SHA256=9e92914b65f7110ca26dd57c9374cd8ed9e3384b9280659360bf507cffc1f082
# Wed, 16 Aug 2023 02:04:15 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 16 Aug 2023 02:04:20 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Wed, 16 Aug 2023 02:04:20 GMT
WORKDIR /opt/emqx
# Wed, 16 Aug 2023 02:04:21 GMT
USER emqx
# Wed, 16 Aug 2023 02:04:21 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 16 Aug 2023 02:04:21 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 16 Aug 2023 02:04:21 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 16 Aug 2023 02:04:21 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 16 Aug 2023 02:04:21 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf9935b6a5db89f92b605f7f0b0af22fb4cea1dcb2fce17fd4394f0b276031a`  
		Last Modified: Wed, 16 Aug 2023 02:04:31 GMT  
		Size: 3.0 MB (3002946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8af255dcc47cd844d6dc7e8fbb203f8650232883ccaa219fb0b5853b69a5a75`  
		Last Modified: Wed, 16 Aug 2023 02:04:30 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e33f97101f8c937743b0ae143802231d013c7c7e5bfb5e8b99cf84fc8513a76`  
		Last Modified: Wed, 16 Aug 2023 02:04:48 GMT  
		Size: 59.8 MB (59756222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f67c7a703b62fd449e1a388004f165ae294913a6df7e9e795c925b582f7c446`  
		Last Modified: Wed, 16 Aug 2023 02:04:43 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
