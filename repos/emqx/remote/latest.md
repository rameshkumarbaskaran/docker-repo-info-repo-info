## `emqx:latest`

```console
$ docker pull emqx@sha256:e16fb01aa65825dae3d9b99e5b777386f7c4677c980b23134476eaef547681c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:af67b05efd940d20f7045f890108598695e5432d25844412ac412d2889eeaa5f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.2 MB (164249699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638f3c40783e63508fbe1577dd48615bbbcbacb458793a33bbc80c48810e06c5`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 04:04:14 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:04:15 GMT
ENV EMQX_VERSION=5.0.11
# Tue, 06 Dec 2022 04:04:15 GMT
ENV AMD64_SHA256=68609fcc1d74be917f9c28c57c14daabccee22361af91b6e98812a35300a1c80
# Tue, 06 Dec 2022 04:04:15 GMT
ENV ARM64_SHA256=f7c7417951beb490ed3a7347b3879db8e9e80ea214c9ef942e777c7136681d31
# Tue, 06 Dec 2022 04:04:15 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 06 Dec 2022 04:04:21 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 06 Dec 2022 04:04:22 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 06 Dec 2022 04:04:22 GMT
WORKDIR /opt/emqx
# Tue, 06 Dec 2022 04:04:28 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 06 Dec 2022 04:04:29 GMT
USER emqx
# Tue, 06 Dec 2022 04:04:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 06 Dec 2022 04:04:29 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 06 Dec 2022 04:04:29 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 04:04:29 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29e5e20fa16580fcb41964870e6c9d3d48072cc1abdbe98fe1645a15c65e9ec`  
		Last Modified: Tue, 06 Dec 2022 04:05:16 GMT  
		Size: 3.0 MB (2988935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22dd9348a5687efee9dadf933fdf1c581bf1533143eb3ce58748acb88502529`  
		Last Modified: Tue, 06 Dec 2022 04:05:24 GMT  
		Size: 64.9 MB (64920995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd74f9c9e7272821472794e054fec92054af29b0a2e630254ff8f3a33fdb09f`  
		Last Modified: Tue, 06 Dec 2022 04:05:15 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2cc6b1ce2d96ed9a20aeaf174adb300c68487487d4a97d95ffb692f30dafae7`  
		Last Modified: Tue, 06 Dec 2022 04:05:24 GMT  
		Size: 64.9 MB (64926015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:36847cbc801d37eafe836c7486f7069e618b168054494a17e6b9108a02c80d06
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.8 MB (147767210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d2c84148e688bdd6a324207d0535c831a0a169d9ac580388ab9659e4f6df89`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Wed, 30 Nov 2022 01:52:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Nov 2022 01:52:58 GMT
ENV EMQX_VERSION=5.0.11
# Wed, 30 Nov 2022 01:52:58 GMT
ENV AMD64_SHA256=68609fcc1d74be917f9c28c57c14daabccee22361af91b6e98812a35300a1c80
# Wed, 30 Nov 2022 01:52:58 GMT
ENV ARM64_SHA256=f7c7417951beb490ed3a7347b3879db8e9e80ea214c9ef942e777c7136681d31
# Wed, 30 Nov 2022 01:52:58 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 30 Nov 2022 01:53:02 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Wed, 30 Nov 2022 01:53:03 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 30 Nov 2022 01:53:03 GMT
WORKDIR /opt/emqx
# Wed, 30 Nov 2022 01:53:08 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 30 Nov 2022 01:53:08 GMT
USER emqx
# Wed, 30 Nov 2022 01:53:08 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 30 Nov 2022 01:53:08 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 30 Nov 2022 01:53:08 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 30 Nov 2022 01:53:08 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779afb6670c886761cbd92232fabbfb5460051f084cda020112fd649fd64c9e9`  
		Last Modified: Wed, 30 Nov 2022 01:53:54 GMT  
		Size: 3.0 MB (3004113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950c27ff169ec58514bc5b2f6c9432b3c603c0f3c9d900e0f87cf167e7e8216e`  
		Last Modified: Wed, 30 Nov 2022 01:53:59 GMT  
		Size: 57.3 MB (57348503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554dd3630b90df5cd7b76d935f8ca60310032deeb91f91555ace233382d57c09`  
		Last Modified: Wed, 30 Nov 2022 01:53:53 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d390a44da3d80a16d371b5d4fa0e9de4b35bc149a4fcb8c8c13309aa6c6cee`  
		Last Modified: Wed, 30 Nov 2022 01:53:59 GMT  
		Size: 57.4 MB (57353085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
