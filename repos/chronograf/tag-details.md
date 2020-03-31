<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.6`](#chronograf16)
-	[`chronograf:1.6.2`](#chronograf162)
-	[`chronograf:1.6.2-alpine`](#chronograf162-alpine)
-	[`chronograf:1.6-alpine`](#chronograf16-alpine)
-	[`chronograf:1.7`](#chronograf17)
-	[`chronograf:1.7.17`](#chronograf1717)
-	[`chronograf:1.7.17-alpine`](#chronograf1717-alpine)
-	[`chronograf:1.7-alpine`](#chronograf17-alpine)
-	[`chronograf:1.8`](#chronograf18)
-	[`chronograf:1.8.0`](#chronograf180)
-	[`chronograf:1.8.0-alpine`](#chronograf180-alpine)
-	[`chronograf:1.8-alpine`](#chronograf18-alpine)
-	[`chronograf:alpine`](#chronografalpine)
-	[`chronograf:latest`](#chronograflatest)

## `chronograf:1.6`

```console
$ docker pull chronograf@sha256:d9fd95854280a1b110ada403ec0dc3bc2f846405f6e4b1aa6563fd9a90ba0dde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6` - linux; amd64

```console
$ docker pull chronograf@sha256:417297866df1a63ce2b018c8647dbfe30862ffa6a58fe12728071129da9d4862
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49141003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b540701ddcc513c3151997d926e43737aa7840c6faa4c97f935a4bea2f1f6a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Mar 2020 01:24:08 GMT
ADD file:e077f4d014ea0869fc4b3d5a3e6b3c8b792a97a8b4a328f33a994369225ff222 in / 
# Tue, 31 Mar 2020 01:24:08 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:14:07 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 31 Mar 2020 02:14:08 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 31 Mar 2020 02:14:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 31 Mar 2020 02:14:19 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 31 Mar 2020 02:14:19 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 31 Mar 2020 02:14:20 GMT
EXPOSE 8888
# Tue, 31 Mar 2020 02:14:20 GMT
VOLUME [/var/lib/chronograf]
# Tue, 31 Mar 2020 02:14:20 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 31 Mar 2020 02:14:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 02:14:20 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:48839397421a64189661c2b86a34eb515d09a28204587a2b06b59df9f6e2d786`  
		Last Modified: Tue, 31 Mar 2020 01:29:28 GMT  
		Size: 22.5 MB (22513374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81baf4e0f31a6b328af5e7b3caddce5fafac0d7d004f39543cb688781902a627`  
		Last Modified: Tue, 31 Mar 2020 02:15:25 GMT  
		Size: 4.5 MB (4503537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8df52b096fdb92d54a56dd3f43e381dfc2e28d0c9acefb4810ff14e467fdc19`  
		Last Modified: Tue, 31 Mar 2020 02:15:29 GMT  
		Size: 22.1 MB (22099694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5644f26ef6529d7c6082976df4260cd1ac060b7a51507117b34804561e77e541`  
		Last Modified: Tue, 31 Mar 2020 02:15:24 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69116c153156aa311f0d14cfa733fc4f4a48428e30359330597e9107a02c7c61`  
		Last Modified: Tue, 31 Mar 2020 02:15:24 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c49ac133aaaa2a8421f37ec90da0f2ecb23ec049482db7aba4cc92683a023d`  
		Last Modified: Tue, 31 Mar 2020 02:15:24 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:ae63c72bacdc92d2891025a940c5846be420cd20999603afc0b9bc13c97dcaf9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43725358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f78bf7736604625294c7a65dbbaec0f8fd2f8f0dba64467e5c494cc20d52102`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 26 Feb 2020 01:01:21 GMT
ADD file:01536f0f2d25f5114e68606280b1a495c4b930ffdd782678b7e8828aef822c14 in / 
# Wed, 26 Feb 2020 01:01:26 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:29:13 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 26 Feb 2020 01:29:53 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Wed, 26 Feb 2020 01:30:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 26 Feb 2020 01:30:13 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 26 Feb 2020 01:30:14 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 26 Feb 2020 01:30:15 GMT
EXPOSE 8888
# Wed, 26 Feb 2020 01:30:17 GMT
VOLUME [/var/lib/chronograf]
# Wed, 26 Feb 2020 01:30:18 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 26 Feb 2020 01:30:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Feb 2020 01:30:20 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0e67f89df0287dbfef2de6d9322fee00ab623a93704fcb288963b8d51d7dfffe`  
		Last Modified: Wed, 26 Feb 2020 01:11:47 GMT  
		Size: 19.3 MB (19298348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15634d01c3f3a1bece118d96c09deb143bac89f0f8ab71aeb0c0629360a460f`  
		Last Modified: Wed, 26 Feb 2020 01:31:40 GMT  
		Size: 3.9 MB (3877306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e906e120466647231c285fa27ecc9be8cb19cc75e83d19b391b7608eefdc7b`  
		Last Modified: Wed, 26 Feb 2020 01:31:59 GMT  
		Size: 20.5 MB (20525314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17684c03781763995f92c0e11531b5558c0617cd50f0805164c039c65b52b1e0`  
		Last Modified: Wed, 26 Feb 2020 01:31:53 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a64f781b9ec1c0723ef52a1692d9c90643ba3f9af2828c0ad1985e3cfc0642`  
		Last Modified: Wed, 26 Feb 2020 01:31:53 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c7efdc3589128a06d0a9388f60c3141f9a94e1e93f5bd80558f39316adf279`  
		Last Modified: Wed, 26 Feb 2020 01:31:53 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:7173b34d6eee29870dbb286c337de20cc7e4f0d9e3aff35536e2ad94ee4db0b0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45208580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfc176aa969158749c9c685e3b3f5b34d19bb4792f9ed44d31fd88b1deeb780c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 26 Feb 2020 00:50:58 GMT
ADD file:9a0fcb77e697946112f14ff0a4dfe61aa0be45f648262b8e0be116e289964e4d in / 
# Wed, 26 Feb 2020 00:51:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 04:10:29 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 26 Feb 2020 04:11:01 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Wed, 26 Feb 2020 04:11:21 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 26 Feb 2020 04:11:22 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 26 Feb 2020 04:11:22 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 26 Feb 2020 04:11:23 GMT
EXPOSE 8888
# Wed, 26 Feb 2020 04:11:24 GMT
VOLUME [/var/lib/chronograf]
# Wed, 26 Feb 2020 04:11:24 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 26 Feb 2020 04:11:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Feb 2020 04:11:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:81610314811e98d4dba43f609b410f2d09dbcd135dc4cd4d8293fec3644dbea8`  
		Last Modified: Wed, 26 Feb 2020 00:58:54 GMT  
		Size: 20.4 MB (20369979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f797dde9809216bf453cb02c743c00da5fed52ec53e5d746f9a7cfdb99720f`  
		Last Modified: Wed, 26 Feb 2020 04:12:22 GMT  
		Size: 4.1 MB (4080742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2378b44fa08285f9f6686d3e53b45afb6dbbed4c81d41ba811560d4e5eb1152`  
		Last Modified: Wed, 26 Feb 2020 04:12:42 GMT  
		Size: 20.7 MB (20733458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2bf4be9df591c56977ce6d8f013fb4304d0508b066ef299fc8e3543c57b745`  
		Last Modified: Wed, 26 Feb 2020 04:12:35 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a96c8ed531f5e471cecb1e286801bae331cb1aea35105264cdf0d43c1e9a07`  
		Last Modified: Wed, 26 Feb 2020 04:12:35 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2c86410b156355eff8190317b1b055b074860a1285a3eaf941217d3845556f`  
		Last Modified: Wed, 26 Feb 2020 04:12:35 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6.2`

```console
$ docker pull chronograf@sha256:d9fd95854280a1b110ada403ec0dc3bc2f846405f6e4b1aa6563fd9a90ba0dde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6.2` - linux; amd64

```console
$ docker pull chronograf@sha256:417297866df1a63ce2b018c8647dbfe30862ffa6a58fe12728071129da9d4862
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49141003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b540701ddcc513c3151997d926e43737aa7840c6faa4c97f935a4bea2f1f6a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Mar 2020 01:24:08 GMT
ADD file:e077f4d014ea0869fc4b3d5a3e6b3c8b792a97a8b4a328f33a994369225ff222 in / 
# Tue, 31 Mar 2020 01:24:08 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:14:07 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 31 Mar 2020 02:14:08 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 31 Mar 2020 02:14:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 31 Mar 2020 02:14:19 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 31 Mar 2020 02:14:19 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 31 Mar 2020 02:14:20 GMT
EXPOSE 8888
# Tue, 31 Mar 2020 02:14:20 GMT
VOLUME [/var/lib/chronograf]
# Tue, 31 Mar 2020 02:14:20 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 31 Mar 2020 02:14:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 02:14:20 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:48839397421a64189661c2b86a34eb515d09a28204587a2b06b59df9f6e2d786`  
		Last Modified: Tue, 31 Mar 2020 01:29:28 GMT  
		Size: 22.5 MB (22513374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81baf4e0f31a6b328af5e7b3caddce5fafac0d7d004f39543cb688781902a627`  
		Last Modified: Tue, 31 Mar 2020 02:15:25 GMT  
		Size: 4.5 MB (4503537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8df52b096fdb92d54a56dd3f43e381dfc2e28d0c9acefb4810ff14e467fdc19`  
		Last Modified: Tue, 31 Mar 2020 02:15:29 GMT  
		Size: 22.1 MB (22099694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5644f26ef6529d7c6082976df4260cd1ac060b7a51507117b34804561e77e541`  
		Last Modified: Tue, 31 Mar 2020 02:15:24 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69116c153156aa311f0d14cfa733fc4f4a48428e30359330597e9107a02c7c61`  
		Last Modified: Tue, 31 Mar 2020 02:15:24 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c49ac133aaaa2a8421f37ec90da0f2ecb23ec049482db7aba4cc92683a023d`  
		Last Modified: Tue, 31 Mar 2020 02:15:24 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:ae63c72bacdc92d2891025a940c5846be420cd20999603afc0b9bc13c97dcaf9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43725358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f78bf7736604625294c7a65dbbaec0f8fd2f8f0dba64467e5c494cc20d52102`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 26 Feb 2020 01:01:21 GMT
ADD file:01536f0f2d25f5114e68606280b1a495c4b930ffdd782678b7e8828aef822c14 in / 
# Wed, 26 Feb 2020 01:01:26 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:29:13 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 26 Feb 2020 01:29:53 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Wed, 26 Feb 2020 01:30:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 26 Feb 2020 01:30:13 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 26 Feb 2020 01:30:14 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 26 Feb 2020 01:30:15 GMT
EXPOSE 8888
# Wed, 26 Feb 2020 01:30:17 GMT
VOLUME [/var/lib/chronograf]
# Wed, 26 Feb 2020 01:30:18 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 26 Feb 2020 01:30:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Feb 2020 01:30:20 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0e67f89df0287dbfef2de6d9322fee00ab623a93704fcb288963b8d51d7dfffe`  
		Last Modified: Wed, 26 Feb 2020 01:11:47 GMT  
		Size: 19.3 MB (19298348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15634d01c3f3a1bece118d96c09deb143bac89f0f8ab71aeb0c0629360a460f`  
		Last Modified: Wed, 26 Feb 2020 01:31:40 GMT  
		Size: 3.9 MB (3877306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e906e120466647231c285fa27ecc9be8cb19cc75e83d19b391b7608eefdc7b`  
		Last Modified: Wed, 26 Feb 2020 01:31:59 GMT  
		Size: 20.5 MB (20525314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17684c03781763995f92c0e11531b5558c0617cd50f0805164c039c65b52b1e0`  
		Last Modified: Wed, 26 Feb 2020 01:31:53 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a64f781b9ec1c0723ef52a1692d9c90643ba3f9af2828c0ad1985e3cfc0642`  
		Last Modified: Wed, 26 Feb 2020 01:31:53 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c7efdc3589128a06d0a9388f60c3141f9a94e1e93f5bd80558f39316adf279`  
		Last Modified: Wed, 26 Feb 2020 01:31:53 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:7173b34d6eee29870dbb286c337de20cc7e4f0d9e3aff35536e2ad94ee4db0b0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45208580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfc176aa969158749c9c685e3b3f5b34d19bb4792f9ed44d31fd88b1deeb780c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 26 Feb 2020 00:50:58 GMT
ADD file:9a0fcb77e697946112f14ff0a4dfe61aa0be45f648262b8e0be116e289964e4d in / 
# Wed, 26 Feb 2020 00:51:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 04:10:29 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 26 Feb 2020 04:11:01 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Wed, 26 Feb 2020 04:11:21 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 26 Feb 2020 04:11:22 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 26 Feb 2020 04:11:22 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 26 Feb 2020 04:11:23 GMT
EXPOSE 8888
# Wed, 26 Feb 2020 04:11:24 GMT
VOLUME [/var/lib/chronograf]
# Wed, 26 Feb 2020 04:11:24 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 26 Feb 2020 04:11:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Feb 2020 04:11:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:81610314811e98d4dba43f609b410f2d09dbcd135dc4cd4d8293fec3644dbea8`  
		Last Modified: Wed, 26 Feb 2020 00:58:54 GMT  
		Size: 20.4 MB (20369979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f797dde9809216bf453cb02c743c00da5fed52ec53e5d746f9a7cfdb99720f`  
		Last Modified: Wed, 26 Feb 2020 04:12:22 GMT  
		Size: 4.1 MB (4080742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2378b44fa08285f9f6686d3e53b45afb6dbbed4c81d41ba811560d4e5eb1152`  
		Last Modified: Wed, 26 Feb 2020 04:12:42 GMT  
		Size: 20.7 MB (20733458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2bf4be9df591c56977ce6d8f013fb4304d0508b066ef299fc8e3543c57b745`  
		Last Modified: Wed, 26 Feb 2020 04:12:35 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a96c8ed531f5e471cecb1e286801bae331cb1aea35105264cdf0d43c1e9a07`  
		Last Modified: Wed, 26 Feb 2020 04:12:35 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2c86410b156355eff8190317b1b055b074860a1285a3eaf941217d3845556f`  
		Last Modified: Wed, 26 Feb 2020 04:12:35 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6.2-alpine`

```console
$ docker pull chronograf@sha256:28a1724975f0d3d915fdd4437bb6dff1248fcba149af3263baacda8d0df53103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:1.6.2-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:ad1c476ad7bceefac0abce84dddcc784f382d48a39c1e7ace47011c45ffca72e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14827436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbd72c4a0ca324fa58904b89a1e3f7961c0c6f06d9fce279d56816a91dd9cc6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:32:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 24 Jan 2020 06:18:20 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Fri, 24 Jan 2020 06:18:24 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 24 Jan 2020 06:18:24 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Fri, 24 Jan 2020 06:18:24 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 24 Jan 2020 06:18:24 GMT
EXPOSE 8888
# Fri, 24 Jan 2020 06:18:25 GMT
VOLUME [/var/lib/chronograf]
# Fri, 24 Jan 2020 06:18:25 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 24 Jan 2020 06:18:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2020 06:18:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60cabf7ae254f2fa160de4e52dde588a8ed9490a15fc92b06cc1c47b680ccdf4`  
		Last Modified: Thu, 23 Jan 2020 19:33:23 GMT  
		Size: 301.9 KB (301878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408f862d3a925084a8f20da4818facc02b5136b1c64af46aab594da9a00e6e2a`  
		Last Modified: Fri, 24 Jan 2020 06:19:15 GMT  
		Size: 11.7 MB (11736857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef248f2678020f581052347921213393abe2aef3bb16189ea7eb4feb23c7e819`  
		Last Modified: Fri, 24 Jan 2020 06:19:07 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d0e4328be0f0ee7718f9879334e0abb572bb8941d9baa29140bccb00388dc7`  
		Last Modified: Fri, 24 Jan 2020 06:19:07 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0a0208ae33af327fb36eae423d4e90cabd9596b9d9b9f0b007ef0da70d8a78`  
		Last Modified: Fri, 24 Jan 2020 06:19:07 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6-alpine`

```console
$ docker pull chronograf@sha256:28a1724975f0d3d915fdd4437bb6dff1248fcba149af3263baacda8d0df53103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:1.6-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:ad1c476ad7bceefac0abce84dddcc784f382d48a39c1e7ace47011c45ffca72e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14827436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbd72c4a0ca324fa58904b89a1e3f7961c0c6f06d9fce279d56816a91dd9cc6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:32:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 24 Jan 2020 06:18:20 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Fri, 24 Jan 2020 06:18:24 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 24 Jan 2020 06:18:24 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Fri, 24 Jan 2020 06:18:24 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 24 Jan 2020 06:18:24 GMT
EXPOSE 8888
# Fri, 24 Jan 2020 06:18:25 GMT
VOLUME [/var/lib/chronograf]
# Fri, 24 Jan 2020 06:18:25 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 24 Jan 2020 06:18:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2020 06:18:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60cabf7ae254f2fa160de4e52dde588a8ed9490a15fc92b06cc1c47b680ccdf4`  
		Last Modified: Thu, 23 Jan 2020 19:33:23 GMT  
		Size: 301.9 KB (301878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408f862d3a925084a8f20da4818facc02b5136b1c64af46aab594da9a00e6e2a`  
		Last Modified: Fri, 24 Jan 2020 06:19:15 GMT  
		Size: 11.7 MB (11736857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef248f2678020f581052347921213393abe2aef3bb16189ea7eb4feb23c7e819`  
		Last Modified: Fri, 24 Jan 2020 06:19:07 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d0e4328be0f0ee7718f9879334e0abb572bb8941d9baa29140bccb00388dc7`  
		Last Modified: Fri, 24 Jan 2020 06:19:07 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0a0208ae33af327fb36eae423d4e90cabd9596b9d9b9f0b007ef0da70d8a78`  
		Last Modified: Fri, 24 Jan 2020 06:19:07 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:ccaa26c4d32ba587d7be54d9e6dee531f129139b18e8443b8f606b84048c5173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7` - linux; amd64

```console
$ docker pull chronograf@sha256:ab6a89aa5223b9fa94338bd205c34ed9fa0e4e3f6ecfe34e093c92bdaabd17a7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65385921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1e166dbbe81821b2a1835014601274bd0953b13e4c7c741793719874e6700ea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Mar 2020 01:24:08 GMT
ADD file:e077f4d014ea0869fc4b3d5a3e6b3c8b792a97a8b4a328f33a994369225ff222 in / 
# Tue, 31 Mar 2020 01:24:08 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:14:07 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 31 Mar 2020 02:14:30 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 31 Mar 2020 02:14:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 31 Mar 2020 02:14:43 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 31 Mar 2020 02:14:43 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 31 Mar 2020 02:14:43 GMT
EXPOSE 8888
# Tue, 31 Mar 2020 02:14:44 GMT
VOLUME [/var/lib/chronograf]
# Tue, 31 Mar 2020 02:14:44 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 31 Mar 2020 02:14:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 02:14:45 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:48839397421a64189661c2b86a34eb515d09a28204587a2b06b59df9f6e2d786`  
		Last Modified: Tue, 31 Mar 2020 01:29:28 GMT  
		Size: 22.5 MB (22513374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81baf4e0f31a6b328af5e7b3caddce5fafac0d7d004f39543cb688781902a627`  
		Last Modified: Tue, 31 Mar 2020 02:15:25 GMT  
		Size: 4.5 MB (4503537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af24628b57022658ca850475251289ddcd867760a654a7ad301d034c49457d4`  
		Last Modified: Tue, 31 Mar 2020 02:15:41 GMT  
		Size: 38.3 MB (38344616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6003ba1dc6d810bbb4dd217ca6581d7262bcb49be624dc96647c6cb902f607d`  
		Last Modified: Tue, 31 Mar 2020 02:15:33 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0262ebbb2867e34db13ca3bc910f7841798a8cbd2201e5b8e2e031f70993cc8`  
		Last Modified: Tue, 31 Mar 2020 02:15:33 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad21333833cbe3ba646c39e3a79b8f1206b590c3fd6ca912ec25854f1a65609`  
		Last Modified: Tue, 31 Mar 2020 02:15:33 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:115e64359059067dab7c4a1141a57f6fc365a6b77a666c7b9e5348ee6e4cc1d7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59002669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1493500dfed914b043ff70d7c79da69cfe82047b7a2b2565a7df56c0e781aabf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 26 Feb 2020 01:01:21 GMT
ADD file:01536f0f2d25f5114e68606280b1a495c4b930ffdd782678b7e8828aef822c14 in / 
# Wed, 26 Feb 2020 01:01:26 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:29:13 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 28 Feb 2020 01:02:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 28 Feb 2020 01:02:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Feb 2020 01:03:00 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 28 Feb 2020 01:03:01 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 28 Feb 2020 01:03:02 GMT
EXPOSE 8888
# Fri, 28 Feb 2020 01:03:02 GMT
VOLUME [/var/lib/chronograf]
# Fri, 28 Feb 2020 01:03:03 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 28 Feb 2020 01:03:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Feb 2020 01:03:05 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0e67f89df0287dbfef2de6d9322fee00ab623a93704fcb288963b8d51d7dfffe`  
		Last Modified: Wed, 26 Feb 2020 01:11:47 GMT  
		Size: 19.3 MB (19298348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15634d01c3f3a1bece118d96c09deb143bac89f0f8ab71aeb0c0629360a460f`  
		Last Modified: Wed, 26 Feb 2020 01:31:40 GMT  
		Size: 3.9 MB (3877306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e747a9b31b04e12c936e0a5dd85bdbf90d46f78c78aac7b00f0ba2804aeaae`  
		Last Modified: Fri, 28 Feb 2020 01:04:07 GMT  
		Size: 35.8 MB (35802615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7da366d25bd108d2f7f1e003adc82baa4b2df6fdff619e2b1713fce3275d1a`  
		Last Modified: Fri, 28 Feb 2020 01:03:57 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5235582746865da4a387d815ba0069a539e4f78b58f70d9746a2116ac98f525b`  
		Last Modified: Fri, 28 Feb 2020 01:03:57 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c9aa46914d3a3a9f36945b3786b4a2cbc5d19eeb712e02c38777a6ea66291f`  
		Last Modified: Fri, 28 Feb 2020 01:03:57 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:770d12a821f397fb27ba5a0624c086d1362ebe083a2df51a36fad93907968c84
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60480993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23e266c34bc9fdcc424c92a6076211202767db762ae448d5abddd57e346dc64d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 26 Feb 2020 00:50:58 GMT
ADD file:9a0fcb77e697946112f14ff0a4dfe61aa0be45f648262b8e0be116e289964e4d in / 
# Wed, 26 Feb 2020 00:51:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 04:10:29 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 28 Feb 2020 01:39:42 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 28 Feb 2020 01:40:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Feb 2020 01:40:07 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 28 Feb 2020 01:40:07 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 28 Feb 2020 01:40:08 GMT
EXPOSE 8888
# Fri, 28 Feb 2020 01:40:09 GMT
VOLUME [/var/lib/chronograf]
# Fri, 28 Feb 2020 01:40:09 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 28 Feb 2020 01:40:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Feb 2020 01:40:11 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:81610314811e98d4dba43f609b410f2d09dbcd135dc4cd4d8293fec3644dbea8`  
		Last Modified: Wed, 26 Feb 2020 00:58:54 GMT  
		Size: 20.4 MB (20369979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f797dde9809216bf453cb02c743c00da5fed52ec53e5d746f9a7cfdb99720f`  
		Last Modified: Wed, 26 Feb 2020 04:12:22 GMT  
		Size: 4.1 MB (4080742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e161d5d8b139e72fcf01761486637006b5e7a401baacee55c1e2f7078e34e9`  
		Last Modified: Fri, 28 Feb 2020 01:41:22 GMT  
		Size: 36.0 MB (36005875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4fe5c0754980b22306b079c214cd85a833612d350e03dba5acd75b2afedf83`  
		Last Modified: Fri, 28 Feb 2020 01:41:14 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23947fc34a37bbadba6ff85943fdabdbcbf89f9413d568b5aaf0374e2b2ca63e`  
		Last Modified: Fri, 28 Feb 2020 01:41:14 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a622dc0ede088f8fb0a8cf2dd8413d1572708705778accfba7d6ac2640dc408`  
		Last Modified: Fri, 28 Feb 2020 01:41:14 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:ccaa26c4d32ba587d7be54d9e6dee531f129139b18e8443b8f606b84048c5173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7.17` - linux; amd64

```console
$ docker pull chronograf@sha256:ab6a89aa5223b9fa94338bd205c34ed9fa0e4e3f6ecfe34e093c92bdaabd17a7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65385921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1e166dbbe81821b2a1835014601274bd0953b13e4c7c741793719874e6700ea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Mar 2020 01:24:08 GMT
ADD file:e077f4d014ea0869fc4b3d5a3e6b3c8b792a97a8b4a328f33a994369225ff222 in / 
# Tue, 31 Mar 2020 01:24:08 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:14:07 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 31 Mar 2020 02:14:30 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 31 Mar 2020 02:14:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 31 Mar 2020 02:14:43 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 31 Mar 2020 02:14:43 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 31 Mar 2020 02:14:43 GMT
EXPOSE 8888
# Tue, 31 Mar 2020 02:14:44 GMT
VOLUME [/var/lib/chronograf]
# Tue, 31 Mar 2020 02:14:44 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 31 Mar 2020 02:14:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 02:14:45 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:48839397421a64189661c2b86a34eb515d09a28204587a2b06b59df9f6e2d786`  
		Last Modified: Tue, 31 Mar 2020 01:29:28 GMT  
		Size: 22.5 MB (22513374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81baf4e0f31a6b328af5e7b3caddce5fafac0d7d004f39543cb688781902a627`  
		Last Modified: Tue, 31 Mar 2020 02:15:25 GMT  
		Size: 4.5 MB (4503537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af24628b57022658ca850475251289ddcd867760a654a7ad301d034c49457d4`  
		Last Modified: Tue, 31 Mar 2020 02:15:41 GMT  
		Size: 38.3 MB (38344616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6003ba1dc6d810bbb4dd217ca6581d7262bcb49be624dc96647c6cb902f607d`  
		Last Modified: Tue, 31 Mar 2020 02:15:33 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0262ebbb2867e34db13ca3bc910f7841798a8cbd2201e5b8e2e031f70993cc8`  
		Last Modified: Tue, 31 Mar 2020 02:15:33 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad21333833cbe3ba646c39e3a79b8f1206b590c3fd6ca912ec25854f1a65609`  
		Last Modified: Tue, 31 Mar 2020 02:15:33 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:115e64359059067dab7c4a1141a57f6fc365a6b77a666c7b9e5348ee6e4cc1d7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59002669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1493500dfed914b043ff70d7c79da69cfe82047b7a2b2565a7df56c0e781aabf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 26 Feb 2020 01:01:21 GMT
ADD file:01536f0f2d25f5114e68606280b1a495c4b930ffdd782678b7e8828aef822c14 in / 
# Wed, 26 Feb 2020 01:01:26 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:29:13 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 28 Feb 2020 01:02:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 28 Feb 2020 01:02:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Feb 2020 01:03:00 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 28 Feb 2020 01:03:01 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 28 Feb 2020 01:03:02 GMT
EXPOSE 8888
# Fri, 28 Feb 2020 01:03:02 GMT
VOLUME [/var/lib/chronograf]
# Fri, 28 Feb 2020 01:03:03 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 28 Feb 2020 01:03:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Feb 2020 01:03:05 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0e67f89df0287dbfef2de6d9322fee00ab623a93704fcb288963b8d51d7dfffe`  
		Last Modified: Wed, 26 Feb 2020 01:11:47 GMT  
		Size: 19.3 MB (19298348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15634d01c3f3a1bece118d96c09deb143bac89f0f8ab71aeb0c0629360a460f`  
		Last Modified: Wed, 26 Feb 2020 01:31:40 GMT  
		Size: 3.9 MB (3877306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e747a9b31b04e12c936e0a5dd85bdbf90d46f78c78aac7b00f0ba2804aeaae`  
		Last Modified: Fri, 28 Feb 2020 01:04:07 GMT  
		Size: 35.8 MB (35802615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7da366d25bd108d2f7f1e003adc82baa4b2df6fdff619e2b1713fce3275d1a`  
		Last Modified: Fri, 28 Feb 2020 01:03:57 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5235582746865da4a387d815ba0069a539e4f78b58f70d9746a2116ac98f525b`  
		Last Modified: Fri, 28 Feb 2020 01:03:57 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c9aa46914d3a3a9f36945b3786b4a2cbc5d19eeb712e02c38777a6ea66291f`  
		Last Modified: Fri, 28 Feb 2020 01:03:57 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:770d12a821f397fb27ba5a0624c086d1362ebe083a2df51a36fad93907968c84
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60480993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23e266c34bc9fdcc424c92a6076211202767db762ae448d5abddd57e346dc64d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 26 Feb 2020 00:50:58 GMT
ADD file:9a0fcb77e697946112f14ff0a4dfe61aa0be45f648262b8e0be116e289964e4d in / 
# Wed, 26 Feb 2020 00:51:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 04:10:29 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 28 Feb 2020 01:39:42 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 28 Feb 2020 01:40:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Feb 2020 01:40:07 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 28 Feb 2020 01:40:07 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 28 Feb 2020 01:40:08 GMT
EXPOSE 8888
# Fri, 28 Feb 2020 01:40:09 GMT
VOLUME [/var/lib/chronograf]
# Fri, 28 Feb 2020 01:40:09 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 28 Feb 2020 01:40:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Feb 2020 01:40:11 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:81610314811e98d4dba43f609b410f2d09dbcd135dc4cd4d8293fec3644dbea8`  
		Last Modified: Wed, 26 Feb 2020 00:58:54 GMT  
		Size: 20.4 MB (20369979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f797dde9809216bf453cb02c743c00da5fed52ec53e5d746f9a7cfdb99720f`  
		Last Modified: Wed, 26 Feb 2020 04:12:22 GMT  
		Size: 4.1 MB (4080742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e161d5d8b139e72fcf01761486637006b5e7a401baacee55c1e2f7078e34e9`  
		Last Modified: Fri, 28 Feb 2020 01:41:22 GMT  
		Size: 36.0 MB (36005875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4fe5c0754980b22306b079c214cd85a833612d350e03dba5acd75b2afedf83`  
		Last Modified: Fri, 28 Feb 2020 01:41:14 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23947fc34a37bbadba6ff85943fdabdbcbf89f9413d568b5aaf0374e2b2ca63e`  
		Last Modified: Fri, 28 Feb 2020 01:41:14 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a622dc0ede088f8fb0a8cf2dd8413d1572708705778accfba7d6ac2640dc408`  
		Last Modified: Fri, 28 Feb 2020 01:41:14 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:603a28fbc24ccbbc748b5ef9ae256684655b38e51c977f8ff4748cc45063d606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:5aef0feb9cb4e13ecf586b7f36185a09ea49724aed8463aac2c7478efa65da84
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22646053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f3c8ac4a93b15f8cf55859c56bd622883f64656febdb24c32368f49e7e13c2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:32:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 28 Feb 2020 01:19:55 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 28 Feb 2020 01:19:59 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 28 Feb 2020 01:19:59 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 28 Feb 2020 01:19:59 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 28 Feb 2020 01:19:59 GMT
EXPOSE 8888
# Fri, 28 Feb 2020 01:19:59 GMT
VOLUME [/var/lib/chronograf]
# Fri, 28 Feb 2020 01:20:00 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 28 Feb 2020 01:20:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Feb 2020 01:20:00 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60cabf7ae254f2fa160de4e52dde588a8ed9490a15fc92b06cc1c47b680ccdf4`  
		Last Modified: Thu, 23 Jan 2020 19:33:23 GMT  
		Size: 301.9 KB (301878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773e9f2acb0e8580a073d46848380cc422fb3f89788c8e0a79acf14f1acd6698`  
		Last Modified: Fri, 28 Feb 2020 01:20:58 GMT  
		Size: 19.6 MB (19555471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8a51e891a34ce42971a645e39720d571f1dad0d9ca1773236a563dae8e442e`  
		Last Modified: Fri, 28 Feb 2020 01:20:54 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393452f1b7a4bc9c29e87d2e72e91c1bde1eab6db814437cee99870bc503cf03`  
		Last Modified: Fri, 28 Feb 2020 01:20:54 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3c9db7086e9040b708e0bc5847745d94ebe7554c262fcefaee821157572878`  
		Last Modified: Fri, 28 Feb 2020 01:20:54 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:603a28fbc24ccbbc748b5ef9ae256684655b38e51c977f8ff4748cc45063d606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:5aef0feb9cb4e13ecf586b7f36185a09ea49724aed8463aac2c7478efa65da84
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22646053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f3c8ac4a93b15f8cf55859c56bd622883f64656febdb24c32368f49e7e13c2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:32:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 28 Feb 2020 01:19:55 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 28 Feb 2020 01:19:59 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 28 Feb 2020 01:19:59 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 28 Feb 2020 01:19:59 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 28 Feb 2020 01:19:59 GMT
EXPOSE 8888
# Fri, 28 Feb 2020 01:19:59 GMT
VOLUME [/var/lib/chronograf]
# Fri, 28 Feb 2020 01:20:00 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 28 Feb 2020 01:20:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Feb 2020 01:20:00 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60cabf7ae254f2fa160de4e52dde588a8ed9490a15fc92b06cc1c47b680ccdf4`  
		Last Modified: Thu, 23 Jan 2020 19:33:23 GMT  
		Size: 301.9 KB (301878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773e9f2acb0e8580a073d46848380cc422fb3f89788c8e0a79acf14f1acd6698`  
		Last Modified: Fri, 28 Feb 2020 01:20:58 GMT  
		Size: 19.6 MB (19555471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8a51e891a34ce42971a645e39720d571f1dad0d9ca1773236a563dae8e442e`  
		Last Modified: Fri, 28 Feb 2020 01:20:54 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393452f1b7a4bc9c29e87d2e72e91c1bde1eab6db814437cee99870bc503cf03`  
		Last Modified: Fri, 28 Feb 2020 01:20:54 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3c9db7086e9040b708e0bc5847745d94ebe7554c262fcefaee821157572878`  
		Last Modified: Fri, 28 Feb 2020 01:20:54 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:91f6b8b507ae9690722ba293b58b135157d9943032b27d59cc85a31e57d8709d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8` - linux; amd64

```console
$ docker pull chronograf@sha256:ee58e795c5793875734abe224e715ed99c7bd878e52491c7545614b42dc55bb0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68562627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8660afa1fb9554fcf37e5e23bb9a6b5374a97f33090eb8d6d932b42b8ece95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Mar 2020 01:24:08 GMT
ADD file:e077f4d014ea0869fc4b3d5a3e6b3c8b792a97a8b4a328f33a994369225ff222 in / 
# Tue, 31 Mar 2020 01:24:08 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:14:07 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 31 Mar 2020 02:14:54 GMT
ENV CHRONOGRAF_VERSION=1.8.0
# Tue, 31 Mar 2020 02:15:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 31 Mar 2020 02:15:06 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 31 Mar 2020 02:15:07 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 31 Mar 2020 02:15:07 GMT
EXPOSE 8888
# Tue, 31 Mar 2020 02:15:08 GMT
VOLUME [/var/lib/chronograf]
# Tue, 31 Mar 2020 02:15:08 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 31 Mar 2020 02:15:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 02:15:09 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:48839397421a64189661c2b86a34eb515d09a28204587a2b06b59df9f6e2d786`  
		Last Modified: Tue, 31 Mar 2020 01:29:28 GMT  
		Size: 22.5 MB (22513374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81baf4e0f31a6b328af5e7b3caddce5fafac0d7d004f39543cb688781902a627`  
		Last Modified: Tue, 31 Mar 2020 02:15:25 GMT  
		Size: 4.5 MB (4503537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1010cae62da9c3e75893e81a12b3970b643c0072d3d6f27f24c0ee082ab541c1`  
		Last Modified: Tue, 31 Mar 2020 02:15:54 GMT  
		Size: 41.5 MB (41521316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55facb6775467a5147e9474689c702a1d923117e89c0fc627a153dcedfe441e`  
		Last Modified: Tue, 31 Mar 2020 02:15:46 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb97379dd1e5901a33c2f0d1f591614fa0f8e4b4298653f18cdff323ac93ac8`  
		Last Modified: Tue, 31 Mar 2020 02:15:46 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c4af759bec5886156f18d9b38207b5394f288d74d9a04ac2f6d9919d4a3537`  
		Last Modified: Tue, 31 Mar 2020 02:15:46 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:bf9a855735ceb7733e1e6bf6c8b2dcde555b59d320b5d46f6ae25fa3e06da5f6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61979493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc82010da74c060152e94a4ef5f62decb4792637d7e46faffa40b01a78171320`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 26 Feb 2020 01:01:21 GMT
ADD file:01536f0f2d25f5114e68606280b1a495c4b930ffdd782678b7e8828aef822c14 in / 
# Wed, 26 Feb 2020 01:01:26 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:29:13 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 28 Feb 2020 01:03:11 GMT
ENV CHRONOGRAF_VERSION=1.8.0
# Fri, 28 Feb 2020 01:03:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Feb 2020 01:03:39 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 28 Feb 2020 01:03:40 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 28 Feb 2020 01:03:40 GMT
EXPOSE 8888
# Fri, 28 Feb 2020 01:03:41 GMT
VOLUME [/var/lib/chronograf]
# Fri, 28 Feb 2020 01:03:42 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 28 Feb 2020 01:03:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Feb 2020 01:03:43 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0e67f89df0287dbfef2de6d9322fee00ab623a93704fcb288963b8d51d7dfffe`  
		Last Modified: Wed, 26 Feb 2020 01:11:47 GMT  
		Size: 19.3 MB (19298348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15634d01c3f3a1bece118d96c09deb143bac89f0f8ab71aeb0c0629360a460f`  
		Last Modified: Wed, 26 Feb 2020 01:31:40 GMT  
		Size: 3.9 MB (3877306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3240a3a7b219ecf570076b612a7d5aac06fc710fda3f8b166a3cc399d17105`  
		Last Modified: Fri, 28 Feb 2020 01:04:26 GMT  
		Size: 38.8 MB (38779447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ce217f1ce08e8bbd6bcbf1801e7f4fced07b2987011d044993543ebc600124`  
		Last Modified: Fri, 28 Feb 2020 01:04:14 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c004f6223ca0d5c2200f5b8b1af677da199902d40ed86883385f7d895780ee29`  
		Last Modified: Fri, 28 Feb 2020 01:04:15 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff433bb8cee205aa10e5c92076debbeb7b21d28a3c03641819aaeb8bcb5ffaea`  
		Last Modified: Fri, 28 Feb 2020 01:04:14 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:95b6f9a482a886f7f2fe526f89d354352dc4e4c38cf3ba9110cbfb2db2f13673
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63163830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544b844fd5358a434ca76d6395371cf4915db5cd7199e5cadd8f742aa39d0170`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 26 Feb 2020 00:50:58 GMT
ADD file:9a0fcb77e697946112f14ff0a4dfe61aa0be45f648262b8e0be116e289964e4d in / 
# Wed, 26 Feb 2020 00:51:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 04:10:29 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 28 Feb 2020 01:40:17 GMT
ENV CHRONOGRAF_VERSION=1.8.0
# Fri, 28 Feb 2020 01:40:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Feb 2020 01:40:43 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 28 Feb 2020 01:40:45 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 28 Feb 2020 01:40:48 GMT
EXPOSE 8888
# Fri, 28 Feb 2020 01:40:51 GMT
VOLUME [/var/lib/chronograf]
# Fri, 28 Feb 2020 01:40:53 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 28 Feb 2020 01:40:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Feb 2020 01:40:57 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:81610314811e98d4dba43f609b410f2d09dbcd135dc4cd4d8293fec3644dbea8`  
		Last Modified: Wed, 26 Feb 2020 00:58:54 GMT  
		Size: 20.4 MB (20369979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f797dde9809216bf453cb02c743c00da5fed52ec53e5d746f9a7cfdb99720f`  
		Last Modified: Wed, 26 Feb 2020 04:12:22 GMT  
		Size: 4.1 MB (4080742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48780f7890892dae31b3d1274dfc8aff3c5c34ad58ae0f0bf5e1afbb238741a`  
		Last Modified: Fri, 28 Feb 2020 01:41:39 GMT  
		Size: 38.7 MB (38688710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dee94acf4498804a9d5a261e4df1ffe38798a5ff04352873de9764dfc5ffd23`  
		Last Modified: Fri, 28 Feb 2020 01:41:29 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788706574837e9824494df99fc75fda33d7f4e909002ca901bf7cb56a480e811`  
		Last Modified: Fri, 28 Feb 2020 01:41:29 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1311dfcdba68ef5487fbe417ac6484b4efb1fb3f285c268700a86549ae4345`  
		Last Modified: Fri, 28 Feb 2020 01:41:29 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.0`

```console
$ docker pull chronograf@sha256:91f6b8b507ae9690722ba293b58b135157d9943032b27d59cc85a31e57d8709d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8.0` - linux; amd64

```console
$ docker pull chronograf@sha256:ee58e795c5793875734abe224e715ed99c7bd878e52491c7545614b42dc55bb0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68562627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8660afa1fb9554fcf37e5e23bb9a6b5374a97f33090eb8d6d932b42b8ece95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Mar 2020 01:24:08 GMT
ADD file:e077f4d014ea0869fc4b3d5a3e6b3c8b792a97a8b4a328f33a994369225ff222 in / 
# Tue, 31 Mar 2020 01:24:08 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:14:07 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 31 Mar 2020 02:14:54 GMT
ENV CHRONOGRAF_VERSION=1.8.0
# Tue, 31 Mar 2020 02:15:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 31 Mar 2020 02:15:06 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 31 Mar 2020 02:15:07 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 31 Mar 2020 02:15:07 GMT
EXPOSE 8888
# Tue, 31 Mar 2020 02:15:08 GMT
VOLUME [/var/lib/chronograf]
# Tue, 31 Mar 2020 02:15:08 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 31 Mar 2020 02:15:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 02:15:09 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:48839397421a64189661c2b86a34eb515d09a28204587a2b06b59df9f6e2d786`  
		Last Modified: Tue, 31 Mar 2020 01:29:28 GMT  
		Size: 22.5 MB (22513374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81baf4e0f31a6b328af5e7b3caddce5fafac0d7d004f39543cb688781902a627`  
		Last Modified: Tue, 31 Mar 2020 02:15:25 GMT  
		Size: 4.5 MB (4503537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1010cae62da9c3e75893e81a12b3970b643c0072d3d6f27f24c0ee082ab541c1`  
		Last Modified: Tue, 31 Mar 2020 02:15:54 GMT  
		Size: 41.5 MB (41521316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55facb6775467a5147e9474689c702a1d923117e89c0fc627a153dcedfe441e`  
		Last Modified: Tue, 31 Mar 2020 02:15:46 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb97379dd1e5901a33c2f0d1f591614fa0f8e4b4298653f18cdff323ac93ac8`  
		Last Modified: Tue, 31 Mar 2020 02:15:46 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c4af759bec5886156f18d9b38207b5394f288d74d9a04ac2f6d9919d4a3537`  
		Last Modified: Tue, 31 Mar 2020 02:15:46 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.0` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:bf9a855735ceb7733e1e6bf6c8b2dcde555b59d320b5d46f6ae25fa3e06da5f6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61979493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc82010da74c060152e94a4ef5f62decb4792637d7e46faffa40b01a78171320`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 26 Feb 2020 01:01:21 GMT
ADD file:01536f0f2d25f5114e68606280b1a495c4b930ffdd782678b7e8828aef822c14 in / 
# Wed, 26 Feb 2020 01:01:26 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:29:13 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 28 Feb 2020 01:03:11 GMT
ENV CHRONOGRAF_VERSION=1.8.0
# Fri, 28 Feb 2020 01:03:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Feb 2020 01:03:39 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 28 Feb 2020 01:03:40 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 28 Feb 2020 01:03:40 GMT
EXPOSE 8888
# Fri, 28 Feb 2020 01:03:41 GMT
VOLUME [/var/lib/chronograf]
# Fri, 28 Feb 2020 01:03:42 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 28 Feb 2020 01:03:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Feb 2020 01:03:43 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0e67f89df0287dbfef2de6d9322fee00ab623a93704fcb288963b8d51d7dfffe`  
		Last Modified: Wed, 26 Feb 2020 01:11:47 GMT  
		Size: 19.3 MB (19298348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15634d01c3f3a1bece118d96c09deb143bac89f0f8ab71aeb0c0629360a460f`  
		Last Modified: Wed, 26 Feb 2020 01:31:40 GMT  
		Size: 3.9 MB (3877306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3240a3a7b219ecf570076b612a7d5aac06fc710fda3f8b166a3cc399d17105`  
		Last Modified: Fri, 28 Feb 2020 01:04:26 GMT  
		Size: 38.8 MB (38779447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ce217f1ce08e8bbd6bcbf1801e7f4fced07b2987011d044993543ebc600124`  
		Last Modified: Fri, 28 Feb 2020 01:04:14 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c004f6223ca0d5c2200f5b8b1af677da199902d40ed86883385f7d895780ee29`  
		Last Modified: Fri, 28 Feb 2020 01:04:15 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff433bb8cee205aa10e5c92076debbeb7b21d28a3c03641819aaeb8bcb5ffaea`  
		Last Modified: Fri, 28 Feb 2020 01:04:14 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.0` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:95b6f9a482a886f7f2fe526f89d354352dc4e4c38cf3ba9110cbfb2db2f13673
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63163830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544b844fd5358a434ca76d6395371cf4915db5cd7199e5cadd8f742aa39d0170`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 26 Feb 2020 00:50:58 GMT
ADD file:9a0fcb77e697946112f14ff0a4dfe61aa0be45f648262b8e0be116e289964e4d in / 
# Wed, 26 Feb 2020 00:51:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 04:10:29 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 28 Feb 2020 01:40:17 GMT
ENV CHRONOGRAF_VERSION=1.8.0
# Fri, 28 Feb 2020 01:40:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Feb 2020 01:40:43 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 28 Feb 2020 01:40:45 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 28 Feb 2020 01:40:48 GMT
EXPOSE 8888
# Fri, 28 Feb 2020 01:40:51 GMT
VOLUME [/var/lib/chronograf]
# Fri, 28 Feb 2020 01:40:53 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 28 Feb 2020 01:40:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Feb 2020 01:40:57 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:81610314811e98d4dba43f609b410f2d09dbcd135dc4cd4d8293fec3644dbea8`  
		Last Modified: Wed, 26 Feb 2020 00:58:54 GMT  
		Size: 20.4 MB (20369979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f797dde9809216bf453cb02c743c00da5fed52ec53e5d746f9a7cfdb99720f`  
		Last Modified: Wed, 26 Feb 2020 04:12:22 GMT  
		Size: 4.1 MB (4080742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48780f7890892dae31b3d1274dfc8aff3c5c34ad58ae0f0bf5e1afbb238741a`  
		Last Modified: Fri, 28 Feb 2020 01:41:39 GMT  
		Size: 38.7 MB (38688710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dee94acf4498804a9d5a261e4df1ffe38798a5ff04352873de9764dfc5ffd23`  
		Last Modified: Fri, 28 Feb 2020 01:41:29 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788706574837e9824494df99fc75fda33d7f4e909002ca901bf7cb56a480e811`  
		Last Modified: Fri, 28 Feb 2020 01:41:29 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1311dfcdba68ef5487fbe417ac6484b4efb1fb3f285c268700a86549ae4345`  
		Last Modified: Fri, 28 Feb 2020 01:41:29 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.0-alpine`

```console
$ docker pull chronograf@sha256:965e84f44180a5b5bc3aff80df38a02237529af663850a57e12505638136159a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:1.8.0-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b444d339638432a3ee33d1276962ad5326faa98ad1945d6aee6f0c2e133e75d4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24405566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc82c4eea801811fa75c31876b1bdeda04a703c6dbe27d4d026976ac02426b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:32:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 28 Feb 2020 01:20:22 GMT
ENV CHRONOGRAF_VERSION=1.8.0
# Fri, 28 Feb 2020 01:20:26 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 28 Feb 2020 01:20:26 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 28 Feb 2020 01:20:26 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 28 Feb 2020 01:20:27 GMT
EXPOSE 8888
# Fri, 28 Feb 2020 01:20:27 GMT
VOLUME [/var/lib/chronograf]
# Fri, 28 Feb 2020 01:20:27 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 28 Feb 2020 01:20:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Feb 2020 01:20:27 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60cabf7ae254f2fa160de4e52dde588a8ed9490a15fc92b06cc1c47b680ccdf4`  
		Last Modified: Thu, 23 Jan 2020 19:33:23 GMT  
		Size: 301.9 KB (301878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de03209d1eabb87355d5bad11e704eb79429856335af3b782993335ffe77a184`  
		Last Modified: Fri, 28 Feb 2020 01:21:17 GMT  
		Size: 21.3 MB (21314991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68527375afc827b163a4b88284416760be086681967d7463f2d9a8cd156a56c9`  
		Last Modified: Fri, 28 Feb 2020 01:21:13 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f18124e5aa1574304597a7b8042f2f9acc5034915266c31c48c3996b8e64c0c`  
		Last Modified: Fri, 28 Feb 2020 01:21:13 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37306532cc0f9a5c5bafbb526e79215d4e16d13029e1de3d9e92952627467d74`  
		Last Modified: Fri, 28 Feb 2020 01:21:13 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:965e84f44180a5b5bc3aff80df38a02237529af663850a57e12505638136159a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b444d339638432a3ee33d1276962ad5326faa98ad1945d6aee6f0c2e133e75d4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24405566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc82c4eea801811fa75c31876b1bdeda04a703c6dbe27d4d026976ac02426b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:32:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 28 Feb 2020 01:20:22 GMT
ENV CHRONOGRAF_VERSION=1.8.0
# Fri, 28 Feb 2020 01:20:26 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 28 Feb 2020 01:20:26 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 28 Feb 2020 01:20:26 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 28 Feb 2020 01:20:27 GMT
EXPOSE 8888
# Fri, 28 Feb 2020 01:20:27 GMT
VOLUME [/var/lib/chronograf]
# Fri, 28 Feb 2020 01:20:27 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 28 Feb 2020 01:20:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Feb 2020 01:20:27 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60cabf7ae254f2fa160de4e52dde588a8ed9490a15fc92b06cc1c47b680ccdf4`  
		Last Modified: Thu, 23 Jan 2020 19:33:23 GMT  
		Size: 301.9 KB (301878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de03209d1eabb87355d5bad11e704eb79429856335af3b782993335ffe77a184`  
		Last Modified: Fri, 28 Feb 2020 01:21:17 GMT  
		Size: 21.3 MB (21314991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68527375afc827b163a4b88284416760be086681967d7463f2d9a8cd156a56c9`  
		Last Modified: Fri, 28 Feb 2020 01:21:13 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f18124e5aa1574304597a7b8042f2f9acc5034915266c31c48c3996b8e64c0c`  
		Last Modified: Fri, 28 Feb 2020 01:21:13 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37306532cc0f9a5c5bafbb526e79215d4e16d13029e1de3d9e92952627467d74`  
		Last Modified: Fri, 28 Feb 2020 01:21:13 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:965e84f44180a5b5bc3aff80df38a02237529af663850a57e12505638136159a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b444d339638432a3ee33d1276962ad5326faa98ad1945d6aee6f0c2e133e75d4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24405566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc82c4eea801811fa75c31876b1bdeda04a703c6dbe27d4d026976ac02426b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:32:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 28 Feb 2020 01:20:22 GMT
ENV CHRONOGRAF_VERSION=1.8.0
# Fri, 28 Feb 2020 01:20:26 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 28 Feb 2020 01:20:26 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 28 Feb 2020 01:20:26 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 28 Feb 2020 01:20:27 GMT
EXPOSE 8888
# Fri, 28 Feb 2020 01:20:27 GMT
VOLUME [/var/lib/chronograf]
# Fri, 28 Feb 2020 01:20:27 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 28 Feb 2020 01:20:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Feb 2020 01:20:27 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60cabf7ae254f2fa160de4e52dde588a8ed9490a15fc92b06cc1c47b680ccdf4`  
		Last Modified: Thu, 23 Jan 2020 19:33:23 GMT  
		Size: 301.9 KB (301878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de03209d1eabb87355d5bad11e704eb79429856335af3b782993335ffe77a184`  
		Last Modified: Fri, 28 Feb 2020 01:21:17 GMT  
		Size: 21.3 MB (21314991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68527375afc827b163a4b88284416760be086681967d7463f2d9a8cd156a56c9`  
		Last Modified: Fri, 28 Feb 2020 01:21:13 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f18124e5aa1574304597a7b8042f2f9acc5034915266c31c48c3996b8e64c0c`  
		Last Modified: Fri, 28 Feb 2020 01:21:13 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37306532cc0f9a5c5bafbb526e79215d4e16d13029e1de3d9e92952627467d74`  
		Last Modified: Fri, 28 Feb 2020 01:21:13 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:91f6b8b507ae9690722ba293b58b135157d9943032b27d59cc85a31e57d8709d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:ee58e795c5793875734abe224e715ed99c7bd878e52491c7545614b42dc55bb0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68562627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8660afa1fb9554fcf37e5e23bb9a6b5374a97f33090eb8d6d932b42b8ece95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Mar 2020 01:24:08 GMT
ADD file:e077f4d014ea0869fc4b3d5a3e6b3c8b792a97a8b4a328f33a994369225ff222 in / 
# Tue, 31 Mar 2020 01:24:08 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:14:07 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 31 Mar 2020 02:14:54 GMT
ENV CHRONOGRAF_VERSION=1.8.0
# Tue, 31 Mar 2020 02:15:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 31 Mar 2020 02:15:06 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 31 Mar 2020 02:15:07 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 31 Mar 2020 02:15:07 GMT
EXPOSE 8888
# Tue, 31 Mar 2020 02:15:08 GMT
VOLUME [/var/lib/chronograf]
# Tue, 31 Mar 2020 02:15:08 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 31 Mar 2020 02:15:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 02:15:09 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:48839397421a64189661c2b86a34eb515d09a28204587a2b06b59df9f6e2d786`  
		Last Modified: Tue, 31 Mar 2020 01:29:28 GMT  
		Size: 22.5 MB (22513374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81baf4e0f31a6b328af5e7b3caddce5fafac0d7d004f39543cb688781902a627`  
		Last Modified: Tue, 31 Mar 2020 02:15:25 GMT  
		Size: 4.5 MB (4503537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1010cae62da9c3e75893e81a12b3970b643c0072d3d6f27f24c0ee082ab541c1`  
		Last Modified: Tue, 31 Mar 2020 02:15:54 GMT  
		Size: 41.5 MB (41521316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55facb6775467a5147e9474689c702a1d923117e89c0fc627a153dcedfe441e`  
		Last Modified: Tue, 31 Mar 2020 02:15:46 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb97379dd1e5901a33c2f0d1f591614fa0f8e4b4298653f18cdff323ac93ac8`  
		Last Modified: Tue, 31 Mar 2020 02:15:46 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c4af759bec5886156f18d9b38207b5394f288d74d9a04ac2f6d9919d4a3537`  
		Last Modified: Tue, 31 Mar 2020 02:15:46 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:bf9a855735ceb7733e1e6bf6c8b2dcde555b59d320b5d46f6ae25fa3e06da5f6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61979493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc82010da74c060152e94a4ef5f62decb4792637d7e46faffa40b01a78171320`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 26 Feb 2020 01:01:21 GMT
ADD file:01536f0f2d25f5114e68606280b1a495c4b930ffdd782678b7e8828aef822c14 in / 
# Wed, 26 Feb 2020 01:01:26 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:29:13 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 28 Feb 2020 01:03:11 GMT
ENV CHRONOGRAF_VERSION=1.8.0
# Fri, 28 Feb 2020 01:03:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Feb 2020 01:03:39 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 28 Feb 2020 01:03:40 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 28 Feb 2020 01:03:40 GMT
EXPOSE 8888
# Fri, 28 Feb 2020 01:03:41 GMT
VOLUME [/var/lib/chronograf]
# Fri, 28 Feb 2020 01:03:42 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 28 Feb 2020 01:03:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Feb 2020 01:03:43 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0e67f89df0287dbfef2de6d9322fee00ab623a93704fcb288963b8d51d7dfffe`  
		Last Modified: Wed, 26 Feb 2020 01:11:47 GMT  
		Size: 19.3 MB (19298348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15634d01c3f3a1bece118d96c09deb143bac89f0f8ab71aeb0c0629360a460f`  
		Last Modified: Wed, 26 Feb 2020 01:31:40 GMT  
		Size: 3.9 MB (3877306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3240a3a7b219ecf570076b612a7d5aac06fc710fda3f8b166a3cc399d17105`  
		Last Modified: Fri, 28 Feb 2020 01:04:26 GMT  
		Size: 38.8 MB (38779447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ce217f1ce08e8bbd6bcbf1801e7f4fced07b2987011d044993543ebc600124`  
		Last Modified: Fri, 28 Feb 2020 01:04:14 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c004f6223ca0d5c2200f5b8b1af677da199902d40ed86883385f7d895780ee29`  
		Last Modified: Fri, 28 Feb 2020 01:04:15 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff433bb8cee205aa10e5c92076debbeb7b21d28a3c03641819aaeb8bcb5ffaea`  
		Last Modified: Fri, 28 Feb 2020 01:04:14 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:95b6f9a482a886f7f2fe526f89d354352dc4e4c38cf3ba9110cbfb2db2f13673
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63163830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544b844fd5358a434ca76d6395371cf4915db5cd7199e5cadd8f742aa39d0170`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 26 Feb 2020 00:50:58 GMT
ADD file:9a0fcb77e697946112f14ff0a4dfe61aa0be45f648262b8e0be116e289964e4d in / 
# Wed, 26 Feb 2020 00:51:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 04:10:29 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 28 Feb 2020 01:40:17 GMT
ENV CHRONOGRAF_VERSION=1.8.0
# Fri, 28 Feb 2020 01:40:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Feb 2020 01:40:43 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 28 Feb 2020 01:40:45 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 28 Feb 2020 01:40:48 GMT
EXPOSE 8888
# Fri, 28 Feb 2020 01:40:51 GMT
VOLUME [/var/lib/chronograf]
# Fri, 28 Feb 2020 01:40:53 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 28 Feb 2020 01:40:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Feb 2020 01:40:57 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:81610314811e98d4dba43f609b410f2d09dbcd135dc4cd4d8293fec3644dbea8`  
		Last Modified: Wed, 26 Feb 2020 00:58:54 GMT  
		Size: 20.4 MB (20369979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f797dde9809216bf453cb02c743c00da5fed52ec53e5d746f9a7cfdb99720f`  
		Last Modified: Wed, 26 Feb 2020 04:12:22 GMT  
		Size: 4.1 MB (4080742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48780f7890892dae31b3d1274dfc8aff3c5c34ad58ae0f0bf5e1afbb238741a`  
		Last Modified: Fri, 28 Feb 2020 01:41:39 GMT  
		Size: 38.7 MB (38688710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dee94acf4498804a9d5a261e4df1ffe38798a5ff04352873de9764dfc5ffd23`  
		Last Modified: Fri, 28 Feb 2020 01:41:29 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788706574837e9824494df99fc75fda33d7f4e909002ca901bf7cb56a480e811`  
		Last Modified: Fri, 28 Feb 2020 01:41:29 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1311dfcdba68ef5487fbe417ac6484b4efb1fb3f285c268700a86549ae4345`  
		Last Modified: Fri, 28 Feb 2020 01:41:29 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
