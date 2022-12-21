## `chronograf:latest`

```console
$ docker pull chronograf@sha256:945dcf98d1fcafd93a238515cad2710b78551cec1e374a73d77cdc9de42500e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:5e147cd584cc40d42a9ac5ad8b05892dd7def2826e426050d12b33f4e206288c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.2 MB (81235348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:181ca155af9072dff68e616f46ffeb6a6e86d08036194c0d3b67ca015392d45d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:47:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 21 Dec 2022 01:47:47 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Wed, 21 Dec 2022 01:47:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 21 Dec 2022 01:47:55 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 21 Dec 2022 01:47:55 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 21 Dec 2022 01:47:55 GMT
EXPOSE 8888
# Wed, 21 Dec 2022 01:47:55 GMT
VOLUME [/var/lib/chronograf]
# Wed, 21 Dec 2022 01:47:55 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 21 Dec 2022 01:47:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Dec 2022 01:47:55 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb42710022201b4041517538b3a692f1ae88a0ec8c9646567df3d05bf9b09a37`  
		Last Modified: Wed, 21 Dec 2022 01:48:36 GMT  
		Size: 5.2 MB (5226800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43185987e07d673338ff668e3ec4ad0ae414aa8764ccc819daa46e2a3b791fbd`  
		Last Modified: Wed, 21 Dec 2022 01:49:11 GMT  
		Size: 44.6 MB (44587208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451016ff8a51b54246c631725ac73043d0487c20425abb51151962ad40964c49`  
		Last Modified: Wed, 21 Dec 2022 01:49:05 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421c18610532b58e3f5a781742491c6d8d3183edbe842846cd69379ee856d3b3`  
		Last Modified: Wed, 21 Dec 2022 01:49:05 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c806cb526b4dbab7dc6d1b7cc633047bce85ee9a0622fd73bfead331185c27b4`  
		Last Modified: Wed, 21 Dec 2022 01:49:05 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:0665685551e147643926adb58a7d5ccc52603fdf0e7392236f70fad66daf1f91
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73542170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89ace42b78502d90092363b0772a4038c414bd55030ea2c01cd5ef86c90abdad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 21 Dec 2022 01:58:25 GMT
ADD file:d62015d4eb206b606ae0bc76253de55403ede851d6fae0277e76bdaed196a848 in / 
# Wed, 21 Dec 2022 01:58:26 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:42:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 21 Dec 2022 02:43:28 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Wed, 21 Dec 2022 02:43:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 21 Dec 2022 02:43:37 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 21 Dec 2022 02:43:37 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 21 Dec 2022 02:43:37 GMT
EXPOSE 8888
# Wed, 21 Dec 2022 02:43:37 GMT
VOLUME [/var/lib/chronograf]
# Wed, 21 Dec 2022 02:43:37 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 21 Dec 2022 02:43:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Dec 2022 02:43:37 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f8686edc9eb6f431c8c17a5eddc7bd38917d3b2d7835970d4fdb2ad0db464766`  
		Last Modified: Wed, 21 Dec 2022 02:05:08 GMT  
		Size: 26.6 MB (26559455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016a20fa6dc9af990e18156410fd2ebb146489aff31ebd3572a48d5e3ad402cf`  
		Last Modified: Wed, 21 Dec 2022 02:44:27 GMT  
		Size: 4.5 MB (4493656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7b4f024336f1d949eb17681b6186a6b3d02c95152448b0eb55789e9c9948166`  
		Last Modified: Wed, 21 Dec 2022 02:45:05 GMT  
		Size: 42.5 MB (42464667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:106b7f1e5290083b565b86b689a9e95014341bb28580da5fce4690a1203dec31`  
		Last Modified: Wed, 21 Dec 2022 02:44:57 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684b514b6671d11e95e75c492f7d9802b345186639fdd12d7f4654e7bdc5c244`  
		Last Modified: Wed, 21 Dec 2022 02:44:57 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f8bf00d940219cd88951a008e58692376b31204c7809d5ac93fff0c490f99b`  
		Last Modified: Wed, 21 Dec 2022 02:44:57 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:a7dd81c66b768d0345ba7ad70daa0cc83babd2d5a65e1a070d19005b3363ac98
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77896728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc644edbac968760c8fccbf14f92f650f29caaea1d64c78a864f317770c2508`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:16:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 21 Dec 2022 02:16:23 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Wed, 21 Dec 2022 02:16:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 21 Dec 2022 02:16:29 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 21 Dec 2022 02:16:30 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 21 Dec 2022 02:16:30 GMT
EXPOSE 8888
# Wed, 21 Dec 2022 02:16:30 GMT
VOLUME [/var/lib/chronograf]
# Wed, 21 Dec 2022 02:16:30 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 21 Dec 2022 02:16:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Dec 2022 02:16:30 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a54fd72505320f64d385cacc21d9f10503c09d3d6004cc6b0024c1c16c3c11`  
		Last Modified: Wed, 21 Dec 2022 02:16:59 GMT  
		Size: 5.2 MB (5210438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269a364ac9dc813f1cd6eb7134357e0510d68d966a7200e66d4362198312bfd7`  
		Last Modified: Wed, 21 Dec 2022 02:17:28 GMT  
		Size: 42.6 MB (42617115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6e18c151345cc203fcd510628be84e6e02dbc0dbb936cd36373e85ef3695a9`  
		Last Modified: Wed, 21 Dec 2022 02:17:23 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f1799d43cd51a3696fe2f26f3f17f682be36fc656186e18a6441e00ad63e26`  
		Last Modified: Wed, 21 Dec 2022 02:17:23 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56436ec89d611f253cb8515a9e2d7e8859d35d24f47fcc750d3f602466b5377e`  
		Last Modified: Wed, 21 Dec 2022 02:17:23 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
