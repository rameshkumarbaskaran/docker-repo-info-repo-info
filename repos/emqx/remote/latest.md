## `emqx:latest`

```console
$ docker pull emqx@sha256:b579027f9338f4e4884c3df7325dbb5a3512a42726563539ed2b2f766f4768da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:8f6588ec839454e85c7088ebca582e9c79931c0a0e2be5de0785b926e356697f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124852615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e49fad68276031992915c490219747f207413b6ea562c7275628261449c812`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:59:59 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 01:59:59 GMT
ENV EMQX_VERSION=4.4.4
# Wed, 05 Oct 2022 01:59:59 GMT
ENV OTP=otp24.1.5-3
# Wed, 05 Oct 2022 02:00:03 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 05 Oct 2022 02:00:10 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 05 Oct 2022 02:00:10 GMT
WORKDIR /opt/emqx
# Wed, 05 Oct 2022 02:00:10 GMT
USER emqx
# Wed, 05 Oct 2022 02:00:10 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 05 Oct 2022 02:00:10 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 05 Oct 2022 02:00:10 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 05 Oct 2022 02:00:11 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 02:00:11 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe095a4000e416a4a962d9e528d50c8497d6f447edeb1dca129322f95aa5e8c`  
		Last Modified: Wed, 05 Oct 2022 02:00:38 GMT  
		Size: 2.6 MB (2569549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ca5365971083f2523aace68964b85626fc613bac6ce0ecae9295ba93ea831a`  
		Last Modified: Wed, 05 Oct 2022 02:00:43 GMT  
		Size: 45.4 MB (45424513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2ffbd0d4cd94ef8244a6bfb9c4f097fa8085cf516b3661e9cb27d34d60e8e3`  
		Last Modified: Wed, 05 Oct 2022 02:00:43 GMT  
		Size: 45.4 MB (45437342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953f151a9c84e239b25e7c4076d976eb601c1a16aefb2bd7490036184be0f971`  
		Last Modified: Wed, 05 Oct 2022 02:00:38 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:cd4145dc7a3e5b6419dc4f7df1ac35999469ffc613ccfeb4402e64a709115d6d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110033511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:262b1fa4217f1bbadbe5d83379ddb4f55744afa84619dd6dc1fff205e060c8a2`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 03:24:14 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:24:14 GMT
ENV EMQX_VERSION=4.4.4
# Wed, 05 Oct 2022 03:24:15 GMT
ENV OTP=otp24.1.5-3
# Wed, 05 Oct 2022 03:24:19 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 05 Oct 2022 03:24:21 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 05 Oct 2022 03:24:21 GMT
WORKDIR /opt/emqx
# Wed, 05 Oct 2022 03:24:22 GMT
USER emqx
# Wed, 05 Oct 2022 03:24:23 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 05 Oct 2022 03:24:24 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 05 Oct 2022 03:24:26 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 05 Oct 2022 03:24:26 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 03:24:27 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75a1f5842b76ca0e80f51010d3a1751158f2fc5fe23e1379771d0eaa6699578`  
		Last Modified: Wed, 05 Oct 2022 03:25:05 GMT  
		Size: 2.4 MB (2353586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57e83ab7e0975fc6638b0b73b6a4c987acb1d1d95e0f8e1add7128836462d10`  
		Last Modified: Wed, 05 Oct 2022 03:25:10 GMT  
		Size: 38.8 MB (38806775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7121b78d29f52bb06f1b85015074e8c415262eac1bf16060359de7f43a76cf28`  
		Last Modified: Wed, 05 Oct 2022 03:25:09 GMT  
		Size: 38.8 MB (38807649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5587cdfa385c41c68799ea99e489a5bf6927d31ebd5206f070b0423466c790bf`  
		Last Modified: Wed, 05 Oct 2022 03:25:05 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
