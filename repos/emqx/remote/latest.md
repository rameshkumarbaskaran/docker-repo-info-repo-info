## `emqx:latest`

```console
$ docker pull emqx@sha256:0e09237d5596c70e9123ce5d03788ee0d9d44db564be9883aa578f6212a49100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:c8b3886cf87cec744649fd18e8af7989dc9ecc9461656eca1893830833afc2b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102509686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8b34ae5d09640705cc9c800243c4a269c13935cd8c429e9e3c193321932073`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 07:24:04 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 07:24:05 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 16 Aug 2023 07:24:19 GMT
ENV EMQX_VERSION=5.1.5-build.3
# Wed, 16 Aug 2023 07:24:20 GMT
ENV AMD64_SHA256=0266cccf61389a49ce1462f21d1e645919d54a04ab158f43245407d6df1fcaf0
# Wed, 16 Aug 2023 07:24:20 GMT
ENV ARM64_SHA256=9e92914b65f7110ca26dd57c9374cd8ed9e3384b9280659360bf507cffc1f082
# Wed, 16 Aug 2023 07:24:20 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 16 Aug 2023 07:24:27 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Wed, 16 Aug 2023 07:24:27 GMT
WORKDIR /opt/emqx
# Wed, 16 Aug 2023 07:24:27 GMT
USER emqx
# Wed, 16 Aug 2023 07:24:27 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 16 Aug 2023 07:24:27 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 16 Aug 2023 07:24:27 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 16 Aug 2023 07:24:27 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 16 Aug 2023 07:24:28 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a371b5ddcbcc897a67cc3e48b691dbdcd2c7847b68982ab2989fed94aba2ab`  
		Last Modified: Wed, 16 Aug 2023 07:24:39 GMT  
		Size: 3.0 MB (2987856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ac64eaf05d4c12a1fe03c49dfc34648d55d85f58364d6acf48973413731b3d`  
		Last Modified: Wed, 16 Aug 2023 07:24:38 GMT  
		Size: 4.1 KB (4107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2001445164695e0f17915a70ad2db3abe10ac3e79dccd273e034f6766f888345`  
		Last Modified: Wed, 16 Aug 2023 07:25:02 GMT  
		Size: 68.1 MB (68099143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429f3f38f3d63567c7bfcc6dfff8beee13f935cffd2d87c0db6f58deec3261b6`  
		Last Modified: Wed, 16 Aug 2023 07:24:55 GMT  
		Size: 902.0 B  
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
