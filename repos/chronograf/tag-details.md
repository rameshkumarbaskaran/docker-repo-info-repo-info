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
-	[`chronograf:1.8.8`](#chronograf188)
-	[`chronograf:1.8.8-alpine`](#chronograf188-alpine)
-	[`chronograf:1.8-alpine`](#chronograf18-alpine)
-	[`chronograf:alpine`](#chronografalpine)
-	[`chronograf:latest`](#chronograflatest)

## `chronograf:1.6`

```console
$ docker pull chronograf@sha256:33d34326164182325d1ce6f9842a1f2de1a9138d45d43233994fd7fe36398ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6` - linux; amd64

```console
$ docker pull chronograf@sha256:15d69f88c78fc993e239344a667d867a16cf3036fa85bb9c0ef0978d6350f73f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49339213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc24ccb5be15bf65bde27ae4676d1113a0ca2bdfce97c1e16fc68c83e4bab4d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:30 GMT
ADD file:da0c935ddc86ca9e44bdd5f61b46c7b43a115ee4bc356324265a7ad6323f61ae in / 
# Tue, 09 Feb 2021 02:23:30 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 02:46:21 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Feb 2021 02:46:21 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 09 Feb 2021 02:46:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 09 Feb 2021 02:46:30 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 09 Feb 2021 02:46:31 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 09 Feb 2021 02:46:31 GMT
EXPOSE 8888
# Tue, 09 Feb 2021 02:46:31 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Feb 2021 02:46:31 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 09 Feb 2021 02:46:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 02:46:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:cae7303ade7f17f84fe86b2a44880e9725cf7d6dcd17f79485360712b6af6dcd`  
		Last Modified: Tue, 09 Feb 2021 02:29:36 GMT  
		Size: 22.5 MB (22528600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603c713cc31395a01337edc5ae784741dda2d7aefb303bb93f7577486b1d1bbe`  
		Last Modified: Tue, 09 Feb 2021 02:47:56 GMT  
		Size: 6.7 MB (6742606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb264800cecf8165052770994afd137d006aca9ea58eb935e938faaf37456785`  
		Last Modified: Tue, 09 Feb 2021 02:47:58 GMT  
		Size: 20.0 MB (20043609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad14277e20368ba850ae45ad74343b73253d0b2e09955b70547cea209e15bc9`  
		Last Modified: Tue, 09 Feb 2021 02:47:53 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e230d3bd4c856bf3fd0f2235b0fb0b77a153d617f6a49a43a974aa2bae66485c`  
		Last Modified: Tue, 09 Feb 2021 02:47:53 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee67c6ec7750a2447c2f9b027624c9aa158255f2f6ebed9f0eab3044b4a887f`  
		Last Modified: Tue, 09 Feb 2021 02:47:53 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:51afefa3ee387a5866fadc8f87bb3857b66d4c3693f2f2cb825e0a17c89adceb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43921926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6c1689df7c8b64ddf8575ee8e992d4a4d500242289b008e9d9fdb9779e29ce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Feb 2021 03:05:17 GMT
ADD file:42ae9de4db7ca66ccb0a5bc0291a00b2b1ad3c62e6e2d6bad1f99c693e981676 in / 
# Tue, 09 Feb 2021 03:05:19 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:43:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Feb 2021 06:43:13 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 09 Feb 2021 06:43:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 09 Feb 2021 06:43:31 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 09 Feb 2021 06:43:32 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 09 Feb 2021 06:43:33 GMT
EXPOSE 8888
# Tue, 09 Feb 2021 06:43:34 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Feb 2021 06:43:34 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 09 Feb 2021 06:43:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 06:43:36 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ebe5f2b760402bf53dfee026659ac0188dc5418dfde6839893f442bbfe23e42f`  
		Last Modified: Tue, 09 Feb 2021 03:13:48 GMT  
		Size: 19.3 MB (19316094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2a61da9a3e077953d6f78e9f324764fa0ee1dca73300f2c2e9453fc6ea84b5`  
		Last Modified: Tue, 09 Feb 2021 06:45:34 GMT  
		Size: 5.8 MB (5764950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362653119746d22f0a3ae780de8a1a9586414263556781619ecff0562ce2ce14`  
		Last Modified: Tue, 09 Feb 2021 06:45:39 GMT  
		Size: 18.8 MB (18816484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c7d332156a97145a3eeb49833504f062a765f8a22b3ca059c6a5f6fd8f762b`  
		Last Modified: Tue, 09 Feb 2021 06:45:33 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5873c8ef39ae6212d18663ab4464804c34c36d3dfd72d95b1abd325a3035c677`  
		Last Modified: Tue, 09 Feb 2021 06:45:33 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2c7faf1a28a8e2bc1fc5ccc9406cb725f22adfeaf082d1d3c0121e61be1448`  
		Last Modified: Tue, 09 Feb 2021 06:45:33 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:01be822b7493fdefdb31df8567ea281109692b8294f0811865deed3697665cbe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45400388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3decb9b5aee14ca5d09e6573ee01e398a359543365c58b48862b88a274983a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Feb 2021 02:43:38 GMT
ADD file:ec0f3f5aad51202b992acbfa7ec19738608d022983bc1918d7d9eecdd35e4800 in / 
# Tue, 09 Feb 2021 02:43:40 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:28:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Feb 2021 04:28:55 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 09 Feb 2021 04:29:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 09 Feb 2021 04:29:09 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 09 Feb 2021 04:29:10 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 09 Feb 2021 04:29:11 GMT
EXPOSE 8888
# Tue, 09 Feb 2021 04:29:12 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Feb 2021 04:29:13 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 09 Feb 2021 04:29:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 04:29:14 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b373a42fa9174db1e441a19411c9622d41f6db219878945ed0cb256efa32c8a6`  
		Last Modified: Tue, 09 Feb 2021 02:50:08 GMT  
		Size: 20.4 MB (20389427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b4b210d138fd2393967f174396ed44ec8cbf98472a90f6928614b79905e1c7`  
		Last Modified: Tue, 09 Feb 2021 04:31:00 GMT  
		Size: 6.0 MB (6028114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92463e9a64f743107a35bac7cfcedc0470f56389efb30c60810b31b7474d418`  
		Last Modified: Tue, 09 Feb 2021 04:31:04 GMT  
		Size: 19.0 MB (18958459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56eb95e3ddaeefa987c0beedb2b0ed5644c5fd82be58396027e8fdb0bb9499cc`  
		Last Modified: Tue, 09 Feb 2021 04:30:58 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc12ab819f226c9f8e8bc5caa63d917b2801e29fafac3d4273b943c56018701`  
		Last Modified: Tue, 09 Feb 2021 04:30:58 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec61cd44099f0548fdb0ee56ca7b5004eb7c68d7fbc0313990476590501f455`  
		Last Modified: Tue, 09 Feb 2021 04:30:58 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6.2`

```console
$ docker pull chronograf@sha256:33d34326164182325d1ce6f9842a1f2de1a9138d45d43233994fd7fe36398ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6.2` - linux; amd64

```console
$ docker pull chronograf@sha256:15d69f88c78fc993e239344a667d867a16cf3036fa85bb9c0ef0978d6350f73f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49339213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc24ccb5be15bf65bde27ae4676d1113a0ca2bdfce97c1e16fc68c83e4bab4d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:30 GMT
ADD file:da0c935ddc86ca9e44bdd5f61b46c7b43a115ee4bc356324265a7ad6323f61ae in / 
# Tue, 09 Feb 2021 02:23:30 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 02:46:21 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Feb 2021 02:46:21 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 09 Feb 2021 02:46:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 09 Feb 2021 02:46:30 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 09 Feb 2021 02:46:31 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 09 Feb 2021 02:46:31 GMT
EXPOSE 8888
# Tue, 09 Feb 2021 02:46:31 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Feb 2021 02:46:31 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 09 Feb 2021 02:46:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 02:46:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:cae7303ade7f17f84fe86b2a44880e9725cf7d6dcd17f79485360712b6af6dcd`  
		Last Modified: Tue, 09 Feb 2021 02:29:36 GMT  
		Size: 22.5 MB (22528600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603c713cc31395a01337edc5ae784741dda2d7aefb303bb93f7577486b1d1bbe`  
		Last Modified: Tue, 09 Feb 2021 02:47:56 GMT  
		Size: 6.7 MB (6742606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb264800cecf8165052770994afd137d006aca9ea58eb935e938faaf37456785`  
		Last Modified: Tue, 09 Feb 2021 02:47:58 GMT  
		Size: 20.0 MB (20043609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad14277e20368ba850ae45ad74343b73253d0b2e09955b70547cea209e15bc9`  
		Last Modified: Tue, 09 Feb 2021 02:47:53 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e230d3bd4c856bf3fd0f2235b0fb0b77a153d617f6a49a43a974aa2bae66485c`  
		Last Modified: Tue, 09 Feb 2021 02:47:53 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee67c6ec7750a2447c2f9b027624c9aa158255f2f6ebed9f0eab3044b4a887f`  
		Last Modified: Tue, 09 Feb 2021 02:47:53 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:51afefa3ee387a5866fadc8f87bb3857b66d4c3693f2f2cb825e0a17c89adceb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43921926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6c1689df7c8b64ddf8575ee8e992d4a4d500242289b008e9d9fdb9779e29ce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Feb 2021 03:05:17 GMT
ADD file:42ae9de4db7ca66ccb0a5bc0291a00b2b1ad3c62e6e2d6bad1f99c693e981676 in / 
# Tue, 09 Feb 2021 03:05:19 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:43:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Feb 2021 06:43:13 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 09 Feb 2021 06:43:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 09 Feb 2021 06:43:31 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 09 Feb 2021 06:43:32 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 09 Feb 2021 06:43:33 GMT
EXPOSE 8888
# Tue, 09 Feb 2021 06:43:34 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Feb 2021 06:43:34 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 09 Feb 2021 06:43:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 06:43:36 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ebe5f2b760402bf53dfee026659ac0188dc5418dfde6839893f442bbfe23e42f`  
		Last Modified: Tue, 09 Feb 2021 03:13:48 GMT  
		Size: 19.3 MB (19316094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2a61da9a3e077953d6f78e9f324764fa0ee1dca73300f2c2e9453fc6ea84b5`  
		Last Modified: Tue, 09 Feb 2021 06:45:34 GMT  
		Size: 5.8 MB (5764950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362653119746d22f0a3ae780de8a1a9586414263556781619ecff0562ce2ce14`  
		Last Modified: Tue, 09 Feb 2021 06:45:39 GMT  
		Size: 18.8 MB (18816484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c7d332156a97145a3eeb49833504f062a765f8a22b3ca059c6a5f6fd8f762b`  
		Last Modified: Tue, 09 Feb 2021 06:45:33 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5873c8ef39ae6212d18663ab4464804c34c36d3dfd72d95b1abd325a3035c677`  
		Last Modified: Tue, 09 Feb 2021 06:45:33 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2c7faf1a28a8e2bc1fc5ccc9406cb725f22adfeaf082d1d3c0121e61be1448`  
		Last Modified: Tue, 09 Feb 2021 06:45:33 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:01be822b7493fdefdb31df8567ea281109692b8294f0811865deed3697665cbe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45400388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3decb9b5aee14ca5d09e6573ee01e398a359543365c58b48862b88a274983a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Feb 2021 02:43:38 GMT
ADD file:ec0f3f5aad51202b992acbfa7ec19738608d022983bc1918d7d9eecdd35e4800 in / 
# Tue, 09 Feb 2021 02:43:40 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:28:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Feb 2021 04:28:55 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 09 Feb 2021 04:29:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 09 Feb 2021 04:29:09 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 09 Feb 2021 04:29:10 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 09 Feb 2021 04:29:11 GMT
EXPOSE 8888
# Tue, 09 Feb 2021 04:29:12 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Feb 2021 04:29:13 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 09 Feb 2021 04:29:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 04:29:14 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b373a42fa9174db1e441a19411c9622d41f6db219878945ed0cb256efa32c8a6`  
		Last Modified: Tue, 09 Feb 2021 02:50:08 GMT  
		Size: 20.4 MB (20389427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b4b210d138fd2393967f174396ed44ec8cbf98472a90f6928614b79905e1c7`  
		Last Modified: Tue, 09 Feb 2021 04:31:00 GMT  
		Size: 6.0 MB (6028114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92463e9a64f743107a35bac7cfcedc0470f56389efb30c60810b31b7474d418`  
		Last Modified: Tue, 09 Feb 2021 04:31:04 GMT  
		Size: 19.0 MB (18958459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56eb95e3ddaeefa987c0beedb2b0ed5644c5fd82be58396027e8fdb0bb9499cc`  
		Last Modified: Tue, 09 Feb 2021 04:30:58 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc12ab819f226c9f8e8bc5caa63d917b2801e29fafac3d4273b943c56018701`  
		Last Modified: Tue, 09 Feb 2021 04:30:58 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec61cd44099f0548fdb0ee56ca7b5004eb7c68d7fbc0313990476590501f455`  
		Last Modified: Tue, 09 Feb 2021 04:30:58 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6.2-alpine`

```console
$ docker pull chronograf@sha256:6fda6b99cadedc8655f35b38712108cd65664a536b571db2308b21e51f237a13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:1.6.2-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:ec7e087f6d478830e1d35c47a71cf58e2567022e3f633b2f5b7a660d39459905
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14841678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8ffca3cd675931823b47f083cf6270b54dcf4b3e70829cb08e366165afebe52`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:21:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:59:21 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 24 Feb 2021 20:59:22 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Wed, 24 Feb 2021 20:59:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 24 Feb 2021 20:59:27 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Wed, 24 Feb 2021 20:59:28 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 24 Feb 2021 20:59:28 GMT
EXPOSE 8888
# Wed, 24 Feb 2021 20:59:28 GMT
VOLUME [/var/lib/chronograf]
# Wed, 24 Feb 2021 20:59:29 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 24 Feb 2021 20:59:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 20:59:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c3c544bdbd838411be7288d5c8bd23d77b89d00730ce0fa218fd7fd1694b04`  
		Last Modified: Wed, 24 Feb 2021 20:24:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b4c4e91c477308692065de267dedc098ac76d0b4d02f27d7d3ff2d2ff35287`  
		Last Modified: Wed, 24 Feb 2021 21:00:31 GMT  
		Size: 280.9 KB (280902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d904a73f6db40a28dd790c598c29db39b3b0ea0f49d5984c0fa8b199a00fa6`  
		Last Modified: Wed, 24 Feb 2021 21:00:34 GMT  
		Size: 11.7 MB (11736767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dfc883f38a5a6a504f2da1e0f287396b12a9b88228f571c2b78de3bd459116`  
		Last Modified: Wed, 24 Feb 2021 21:00:31 GMT  
		Size: 12.2 KB (12234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534ceababa7b61740f9a2691f0c133115973053e29d016d46d5e81c0622abe3e`  
		Last Modified: Wed, 24 Feb 2021 21:00:31 GMT  
		Size: 11.9 KB (11891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14260646b7f675642359885c49827737deb081acd3a59cfd9385764d823bc183`  
		Last Modified: Wed, 24 Feb 2021 21:00:31 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6-alpine`

```console
$ docker pull chronograf@sha256:6fda6b99cadedc8655f35b38712108cd65664a536b571db2308b21e51f237a13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:1.6-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:ec7e087f6d478830e1d35c47a71cf58e2567022e3f633b2f5b7a660d39459905
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14841678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8ffca3cd675931823b47f083cf6270b54dcf4b3e70829cb08e366165afebe52`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:21:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:59:21 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 24 Feb 2021 20:59:22 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Wed, 24 Feb 2021 20:59:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 24 Feb 2021 20:59:27 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Wed, 24 Feb 2021 20:59:28 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 24 Feb 2021 20:59:28 GMT
EXPOSE 8888
# Wed, 24 Feb 2021 20:59:28 GMT
VOLUME [/var/lib/chronograf]
# Wed, 24 Feb 2021 20:59:29 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 24 Feb 2021 20:59:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 20:59:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c3c544bdbd838411be7288d5c8bd23d77b89d00730ce0fa218fd7fd1694b04`  
		Last Modified: Wed, 24 Feb 2021 20:24:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b4c4e91c477308692065de267dedc098ac76d0b4d02f27d7d3ff2d2ff35287`  
		Last Modified: Wed, 24 Feb 2021 21:00:31 GMT  
		Size: 280.9 KB (280902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d904a73f6db40a28dd790c598c29db39b3b0ea0f49d5984c0fa8b199a00fa6`  
		Last Modified: Wed, 24 Feb 2021 21:00:34 GMT  
		Size: 11.7 MB (11736767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dfc883f38a5a6a504f2da1e0f287396b12a9b88228f571c2b78de3bd459116`  
		Last Modified: Wed, 24 Feb 2021 21:00:31 GMT  
		Size: 12.2 KB (12234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534ceababa7b61740f9a2691f0c133115973053e29d016d46d5e81c0622abe3e`  
		Last Modified: Wed, 24 Feb 2021 21:00:31 GMT  
		Size: 11.9 KB (11891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14260646b7f675642359885c49827737deb081acd3a59cfd9385764d823bc183`  
		Last Modified: Wed, 24 Feb 2021 21:00:31 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:f40ff5a23a27dd5609a0eb8f4f79acb3a2cc67d52ae7c283c1b440c6fc9b10fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7` - linux; amd64

```console
$ docker pull chronograf@sha256:922cb1501665af987f94a25294737445d1e750cfa3f8eaabf2c331be1d54e6d5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65367021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68daff9cf85806cd4af73110736d39c50ee36742dc4d63a14fb2fda186a72cb3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:30 GMT
ADD file:da0c935ddc86ca9e44bdd5f61b46c7b43a115ee4bc356324265a7ad6323f61ae in / 
# Tue, 09 Feb 2021 02:23:30 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 02:46:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Feb 2021 02:46:52 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 09 Feb 2021 02:47:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 09 Feb 2021 02:47:05 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 09 Feb 2021 02:47:05 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 09 Feb 2021 02:47:05 GMT
EXPOSE 8888
# Tue, 09 Feb 2021 02:47:06 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Feb 2021 02:47:06 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 09 Feb 2021 02:47:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 02:47:06 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:cae7303ade7f17f84fe86b2a44880e9725cf7d6dcd17f79485360712b6af6dcd`  
		Last Modified: Tue, 09 Feb 2021 02:29:36 GMT  
		Size: 22.5 MB (22528600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4311468ad10eee51ca97c75df7615a5d0af76d156b6824a7dfb244b8694016a2`  
		Last Modified: Tue, 09 Feb 2021 02:48:08 GMT  
		Size: 4.5 MB (4504899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da961c36214e89fbf909b0c9fb9a969ec955522bcb12630f37000ea4fde1777`  
		Last Modified: Tue, 09 Feb 2021 02:48:22 GMT  
		Size: 38.3 MB (38309126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750f9108344712250c9e2212694c183c2a1ab46aa21d48358cf9d5fd13ce2960`  
		Last Modified: Tue, 09 Feb 2021 02:48:07 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815008e187db7862ee0c7be568d20df2ef54553814a42b16b8355e95d5c8d896`  
		Last Modified: Tue, 09 Feb 2021 02:48:07 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3755893fcd8e74505c6b1ac0f7b0d69ac72d8cf813930d4bee368b9199a6be`  
		Last Modified: Tue, 09 Feb 2021 02:48:10 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:b5c54c1665446d4e599eeaff8d043dda96a0a56678b92b0b643e77d61b5247f3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58972504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d469b1fc7af1ee8bd9fcff4334667ef1cd02fdc8dc871af068dadf17d7e9ed5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Feb 2021 03:05:17 GMT
ADD file:42ae9de4db7ca66ccb0a5bc0291a00b2b1ad3c62e6e2d6bad1f99c693e981676 in / 
# Tue, 09 Feb 2021 03:05:19 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:44:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Feb 2021 06:44:08 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 09 Feb 2021 06:44:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 09 Feb 2021 06:44:33 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 09 Feb 2021 06:44:34 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 09 Feb 2021 06:44:35 GMT
EXPOSE 8888
# Tue, 09 Feb 2021 06:44:36 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Feb 2021 06:44:37 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 09 Feb 2021 06:44:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 06:44:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ebe5f2b760402bf53dfee026659ac0188dc5418dfde6839893f442bbfe23e42f`  
		Last Modified: Tue, 09 Feb 2021 03:13:48 GMT  
		Size: 19.3 MB (19316094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e417074f111ce77543576d26852c6eca0cc51db7060c127735ed5a0e031c8279`  
		Last Modified: Tue, 09 Feb 2021 06:45:49 GMT  
		Size: 3.9 MB (3879583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17eb4664e03d648317a9bac27e16eb0a136e0b52b90915f0ad4be2328b2aebbf`  
		Last Modified: Tue, 09 Feb 2021 06:45:57 GMT  
		Size: 35.8 MB (35752431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf4d71aa21408fc662eadab25f703c03b128c9ee1a01fbf21a41ad4649820a1d`  
		Last Modified: Tue, 09 Feb 2021 06:45:47 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dfb077e845608616c58ddf0a123b6ad3eb570b9cf3b905d4a75a390a3f5d19f`  
		Last Modified: Tue, 09 Feb 2021 06:45:47 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22017253e3fdcc9889a66efd516cff81e6ddf8ffa08b362ff0bae7d00ecee58e`  
		Last Modified: Tue, 09 Feb 2021 06:45:47 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:3fe817594497ba687c2c1e536381b429784146e989519d4c49aa9ec613d6bd7e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60457732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cf446bcaf7b66b3e70ecefcf89d426013ae7c91f98fb26cb84d3f127c7744e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Feb 2021 02:43:38 GMT
ADD file:ec0f3f5aad51202b992acbfa7ec19738608d022983bc1918d7d9eecdd35e4800 in / 
# Tue, 09 Feb 2021 02:43:40 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:29:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Feb 2021 04:29:40 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 09 Feb 2021 04:30:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 09 Feb 2021 04:30:01 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 09 Feb 2021 04:30:02 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 09 Feb 2021 04:30:03 GMT
EXPOSE 8888
# Tue, 09 Feb 2021 04:30:04 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Feb 2021 04:30:05 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 09 Feb 2021 04:30:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 04:30:07 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b373a42fa9174db1e441a19411c9622d41f6db219878945ed0cb256efa32c8a6`  
		Last Modified: Tue, 09 Feb 2021 02:50:08 GMT  
		Size: 20.4 MB (20389427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f91f32ad810e3079afdb3990c2c5ea83a15f72ef79ce69080270a9d31808669`  
		Last Modified: Tue, 09 Feb 2021 04:31:13 GMT  
		Size: 4.1 MB (4082249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b58ac22f8956909038475f6de337b94e8c5515c3af8b2e002f64c573e6e39fe`  
		Last Modified: Tue, 09 Feb 2021 04:31:21 GMT  
		Size: 36.0 MB (35961660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2af3f87c317846b7282ade6031f461325b19d98ebd130777821ade96277a7e`  
		Last Modified: Tue, 09 Feb 2021 04:31:13 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9f2202400c8c35fbb38c5af4a2374c5001e193477d61489db80655e5c8f0ff`  
		Last Modified: Tue, 09 Feb 2021 04:31:13 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbda7d2fb58e598338ffad6c22fb43c0b845ae194e2513624332d8fe8ad0a50`  
		Last Modified: Tue, 09 Feb 2021 04:31:12 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:f40ff5a23a27dd5609a0eb8f4f79acb3a2cc67d52ae7c283c1b440c6fc9b10fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7.17` - linux; amd64

```console
$ docker pull chronograf@sha256:922cb1501665af987f94a25294737445d1e750cfa3f8eaabf2c331be1d54e6d5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65367021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68daff9cf85806cd4af73110736d39c50ee36742dc4d63a14fb2fda186a72cb3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:30 GMT
ADD file:da0c935ddc86ca9e44bdd5f61b46c7b43a115ee4bc356324265a7ad6323f61ae in / 
# Tue, 09 Feb 2021 02:23:30 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 02:46:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Feb 2021 02:46:52 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 09 Feb 2021 02:47:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 09 Feb 2021 02:47:05 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 09 Feb 2021 02:47:05 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 09 Feb 2021 02:47:05 GMT
EXPOSE 8888
# Tue, 09 Feb 2021 02:47:06 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Feb 2021 02:47:06 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 09 Feb 2021 02:47:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 02:47:06 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:cae7303ade7f17f84fe86b2a44880e9725cf7d6dcd17f79485360712b6af6dcd`  
		Last Modified: Tue, 09 Feb 2021 02:29:36 GMT  
		Size: 22.5 MB (22528600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4311468ad10eee51ca97c75df7615a5d0af76d156b6824a7dfb244b8694016a2`  
		Last Modified: Tue, 09 Feb 2021 02:48:08 GMT  
		Size: 4.5 MB (4504899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da961c36214e89fbf909b0c9fb9a969ec955522bcb12630f37000ea4fde1777`  
		Last Modified: Tue, 09 Feb 2021 02:48:22 GMT  
		Size: 38.3 MB (38309126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750f9108344712250c9e2212694c183c2a1ab46aa21d48358cf9d5fd13ce2960`  
		Last Modified: Tue, 09 Feb 2021 02:48:07 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815008e187db7862ee0c7be568d20df2ef54553814a42b16b8355e95d5c8d896`  
		Last Modified: Tue, 09 Feb 2021 02:48:07 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3755893fcd8e74505c6b1ac0f7b0d69ac72d8cf813930d4bee368b9199a6be`  
		Last Modified: Tue, 09 Feb 2021 02:48:10 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:b5c54c1665446d4e599eeaff8d043dda96a0a56678b92b0b643e77d61b5247f3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58972504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d469b1fc7af1ee8bd9fcff4334667ef1cd02fdc8dc871af068dadf17d7e9ed5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Feb 2021 03:05:17 GMT
ADD file:42ae9de4db7ca66ccb0a5bc0291a00b2b1ad3c62e6e2d6bad1f99c693e981676 in / 
# Tue, 09 Feb 2021 03:05:19 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:44:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Feb 2021 06:44:08 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 09 Feb 2021 06:44:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 09 Feb 2021 06:44:33 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 09 Feb 2021 06:44:34 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 09 Feb 2021 06:44:35 GMT
EXPOSE 8888
# Tue, 09 Feb 2021 06:44:36 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Feb 2021 06:44:37 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 09 Feb 2021 06:44:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 06:44:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ebe5f2b760402bf53dfee026659ac0188dc5418dfde6839893f442bbfe23e42f`  
		Last Modified: Tue, 09 Feb 2021 03:13:48 GMT  
		Size: 19.3 MB (19316094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e417074f111ce77543576d26852c6eca0cc51db7060c127735ed5a0e031c8279`  
		Last Modified: Tue, 09 Feb 2021 06:45:49 GMT  
		Size: 3.9 MB (3879583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17eb4664e03d648317a9bac27e16eb0a136e0b52b90915f0ad4be2328b2aebbf`  
		Last Modified: Tue, 09 Feb 2021 06:45:57 GMT  
		Size: 35.8 MB (35752431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf4d71aa21408fc662eadab25f703c03b128c9ee1a01fbf21a41ad4649820a1d`  
		Last Modified: Tue, 09 Feb 2021 06:45:47 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dfb077e845608616c58ddf0a123b6ad3eb570b9cf3b905d4a75a390a3f5d19f`  
		Last Modified: Tue, 09 Feb 2021 06:45:47 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22017253e3fdcc9889a66efd516cff81e6ddf8ffa08b362ff0bae7d00ecee58e`  
		Last Modified: Tue, 09 Feb 2021 06:45:47 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:3fe817594497ba687c2c1e536381b429784146e989519d4c49aa9ec613d6bd7e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60457732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cf446bcaf7b66b3e70ecefcf89d426013ae7c91f98fb26cb84d3f127c7744e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Feb 2021 02:43:38 GMT
ADD file:ec0f3f5aad51202b992acbfa7ec19738608d022983bc1918d7d9eecdd35e4800 in / 
# Tue, 09 Feb 2021 02:43:40 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:29:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Feb 2021 04:29:40 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 09 Feb 2021 04:30:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 09 Feb 2021 04:30:01 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 09 Feb 2021 04:30:02 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 09 Feb 2021 04:30:03 GMT
EXPOSE 8888
# Tue, 09 Feb 2021 04:30:04 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Feb 2021 04:30:05 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 09 Feb 2021 04:30:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 04:30:07 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b373a42fa9174db1e441a19411c9622d41f6db219878945ed0cb256efa32c8a6`  
		Last Modified: Tue, 09 Feb 2021 02:50:08 GMT  
		Size: 20.4 MB (20389427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f91f32ad810e3079afdb3990c2c5ea83a15f72ef79ce69080270a9d31808669`  
		Last Modified: Tue, 09 Feb 2021 04:31:13 GMT  
		Size: 4.1 MB (4082249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b58ac22f8956909038475f6de337b94e8c5515c3af8b2e002f64c573e6e39fe`  
		Last Modified: Tue, 09 Feb 2021 04:31:21 GMT  
		Size: 36.0 MB (35961660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2af3f87c317846b7282ade6031f461325b19d98ebd130777821ade96277a7e`  
		Last Modified: Tue, 09 Feb 2021 04:31:13 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9f2202400c8c35fbb38c5af4a2374c5001e193477d61489db80655e5c8f0ff`  
		Last Modified: Tue, 09 Feb 2021 04:31:13 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbda7d2fb58e598338ffad6c22fb43c0b845ae194e2513624332d8fe8ad0a50`  
		Last Modified: Tue, 09 Feb 2021 04:31:12 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:29daf559b19979a3f6b515e5b64f85da41d8563de84f729b5cca2f29e81cb6d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:601a3e61a39ac1064fe8579fd8a76d2eb2045c0ddde6403accc6a97f9994405c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22660183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ac2fe7bc7e6b44d2fc2315ec60043d12e20db731d2f9689b25782dea5a7824`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:21:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:59:21 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 24 Feb 2021 20:59:42 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 24 Feb 2021 20:59:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 24 Feb 2021 20:59:49 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 24 Feb 2021 20:59:49 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 24 Feb 2021 20:59:50 GMT
EXPOSE 8888
# Wed, 24 Feb 2021 20:59:50 GMT
VOLUME [/var/lib/chronograf]
# Wed, 24 Feb 2021 20:59:51 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 24 Feb 2021 20:59:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 20:59:51 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c3c544bdbd838411be7288d5c8bd23d77b89d00730ce0fa218fd7fd1694b04`  
		Last Modified: Wed, 24 Feb 2021 20:24:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b4c4e91c477308692065de267dedc098ac76d0b4d02f27d7d3ff2d2ff35287`  
		Last Modified: Wed, 24 Feb 2021 21:00:31 GMT  
		Size: 280.9 KB (280902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8086d591ea21a7d2053a3ac2e4b09bcd061fa7db0a52cc88cf77e9f67a88a4a`  
		Last Modified: Wed, 24 Feb 2021 21:00:46 GMT  
		Size: 19.6 MB (19555264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69e38797301448c5c356b09bb03912342bec1eb9a4fd13af45be3ad907e36e4`  
		Last Modified: Wed, 24 Feb 2021 21:00:41 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df45ac8ca8c63a3e1dbcb7850d713547d263bd8b520831ea6af92602631b7fe`  
		Last Modified: Wed, 24 Feb 2021 21:00:41 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e197b7c1436e0215a31f5bba3fb2622516cd72e67021512d9e6f4254d7a511`  
		Last Modified: Wed, 24 Feb 2021 21:00:41 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:29daf559b19979a3f6b515e5b64f85da41d8563de84f729b5cca2f29e81cb6d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:601a3e61a39ac1064fe8579fd8a76d2eb2045c0ddde6403accc6a97f9994405c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22660183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ac2fe7bc7e6b44d2fc2315ec60043d12e20db731d2f9689b25782dea5a7824`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:21:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:59:21 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 24 Feb 2021 20:59:42 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 24 Feb 2021 20:59:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 24 Feb 2021 20:59:49 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 24 Feb 2021 20:59:49 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 24 Feb 2021 20:59:50 GMT
EXPOSE 8888
# Wed, 24 Feb 2021 20:59:50 GMT
VOLUME [/var/lib/chronograf]
# Wed, 24 Feb 2021 20:59:51 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 24 Feb 2021 20:59:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 20:59:51 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c3c544bdbd838411be7288d5c8bd23d77b89d00730ce0fa218fd7fd1694b04`  
		Last Modified: Wed, 24 Feb 2021 20:24:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b4c4e91c477308692065de267dedc098ac76d0b4d02f27d7d3ff2d2ff35287`  
		Last Modified: Wed, 24 Feb 2021 21:00:31 GMT  
		Size: 280.9 KB (280902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8086d591ea21a7d2053a3ac2e4b09bcd061fa7db0a52cc88cf77e9f67a88a4a`  
		Last Modified: Wed, 24 Feb 2021 21:00:46 GMT  
		Size: 19.6 MB (19555264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69e38797301448c5c356b09bb03912342bec1eb9a4fd13af45be3ad907e36e4`  
		Last Modified: Wed, 24 Feb 2021 21:00:41 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df45ac8ca8c63a3e1dbcb7850d713547d263bd8b520831ea6af92602631b7fe`  
		Last Modified: Wed, 24 Feb 2021 21:00:41 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e197b7c1436e0215a31f5bba3fb2622516cd72e67021512d9e6f4254d7a511`  
		Last Modified: Wed, 24 Feb 2021 21:00:41 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:36337a26f42df73c273f15841e64b1b898f1223f1aa158c10bebf668785a9d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8` - linux; amd64

```console
$ docker pull chronograf@sha256:6bbfbbd73180964dbe313647223e80ee0e165ae05015db86639ba20f0f78931d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70424385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d0154a00f46e5c1657d665aa2fc18c9c0242b2db7f64caa4e6658ed6b4ef60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:30 GMT
ADD file:da0c935ddc86ca9e44bdd5f61b46c7b43a115ee4bc356324265a7ad6323f61ae in / 
# Tue, 09 Feb 2021 02:23:30 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 02:46:21 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Feb 2021 02:47:17 GMT
ENV CHRONOGRAF_VERSION=1.8.8
# Tue, 09 Feb 2021 02:47:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 09 Feb 2021 02:47:27 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 09 Feb 2021 02:47:27 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 09 Feb 2021 02:47:28 GMT
EXPOSE 8888
# Tue, 09 Feb 2021 02:47:28 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Feb 2021 02:47:28 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 09 Feb 2021 02:47:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 02:47:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:cae7303ade7f17f84fe86b2a44880e9725cf7d6dcd17f79485360712b6af6dcd`  
		Last Modified: Tue, 09 Feb 2021 02:29:36 GMT  
		Size: 22.5 MB (22528600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603c713cc31395a01337edc5ae784741dda2d7aefb303bb93f7577486b1d1bbe`  
		Last Modified: Tue, 09 Feb 2021 02:47:56 GMT  
		Size: 6.7 MB (6742606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63600abc06b0687e4b24afa150d2da557c51a85b33e91502d51071591e5e6d82`  
		Last Modified: Tue, 09 Feb 2021 02:48:34 GMT  
		Size: 41.1 MB (41128782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3b434ef96cd8f4643d0c998ec73edb0b44c26d4e31cd5bca7c5f29b9400a0d`  
		Last Modified: Tue, 09 Feb 2021 02:48:27 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8145a040da7204ae6decb8f85b3096c06ade1972f6b6d4ab0496b789a24ce2`  
		Last Modified: Tue, 09 Feb 2021 02:48:27 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391ffb32b78cc26585c3ddd4ecc5590a8961c93e839ed73b88da29e4ad507ee7`  
		Last Modified: Tue, 09 Feb 2021 02:48:27 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:4bd93b3e7a1947354ca40608ba8679b477b93627fd704564f8844ec6583ae0ab
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63839627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31720bcd6ff8befefc1ba22809f3f7384cadcf9aac801b8e42422eba6027788b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Feb 2021 03:05:17 GMT
ADD file:42ae9de4db7ca66ccb0a5bc0291a00b2b1ad3c62e6e2d6bad1f99c693e981676 in / 
# Tue, 09 Feb 2021 03:05:19 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:43:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Feb 2021 06:44:47 GMT
ENV CHRONOGRAF_VERSION=1.8.8
# Tue, 09 Feb 2021 06:45:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 09 Feb 2021 06:45:08 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 09 Feb 2021 06:45:09 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 09 Feb 2021 06:45:10 GMT
EXPOSE 8888
# Tue, 09 Feb 2021 06:45:11 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Feb 2021 06:45:13 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 09 Feb 2021 06:45:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 06:45:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ebe5f2b760402bf53dfee026659ac0188dc5418dfde6839893f442bbfe23e42f`  
		Last Modified: Tue, 09 Feb 2021 03:13:48 GMT  
		Size: 19.3 MB (19316094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2a61da9a3e077953d6f78e9f324764fa0ee1dca73300f2c2e9453fc6ea84b5`  
		Last Modified: Tue, 09 Feb 2021 06:45:34 GMT  
		Size: 5.8 MB (5764950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37a1d6ec067d7ad885ae39385325d7b4d962e44a9606ac244f28cf7e0ef1c20`  
		Last Modified: Tue, 09 Feb 2021 06:46:18 GMT  
		Size: 38.7 MB (38734189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94bf3287fbb0eceb91a3df640fac834a6269be6dd059d7d74a2eaa6c45520d9`  
		Last Modified: Tue, 09 Feb 2021 06:46:05 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01f4f97106955daa8a8383b91693e231660a91e456c56c3c0eb30856c6d2d4a`  
		Last Modified: Tue, 09 Feb 2021 06:46:05 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd788b08bcc284b72a7696f72bfbabb0b3c44967caa6daaa71b425e112cc3a1`  
		Last Modified: Tue, 09 Feb 2021 06:46:05 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:7f130666c6361906f40355f639d52098ddfb14057bc887b3fb0624dc46f071cc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64944267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2a6436ea35a9248cd7a1fab7947bda22ebd1b384802f92f4381c3a4ab5995b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Feb 2021 02:43:38 GMT
ADD file:ec0f3f5aad51202b992acbfa7ec19738608d022983bc1918d7d9eecdd35e4800 in / 
# Tue, 09 Feb 2021 02:43:40 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:28:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Feb 2021 04:30:15 GMT
ENV CHRONOGRAF_VERSION=1.8.8
# Tue, 09 Feb 2021 04:30:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 09 Feb 2021 04:30:30 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 09 Feb 2021 04:30:30 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 09 Feb 2021 04:30:31 GMT
EXPOSE 8888
# Tue, 09 Feb 2021 04:30:32 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Feb 2021 04:30:32 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 09 Feb 2021 04:30:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 04:30:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b373a42fa9174db1e441a19411c9622d41f6db219878945ed0cb256efa32c8a6`  
		Last Modified: Tue, 09 Feb 2021 02:50:08 GMT  
		Size: 20.4 MB (20389427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b4b210d138fd2393967f174396ed44ec8cbf98472a90f6928614b79905e1c7`  
		Last Modified: Tue, 09 Feb 2021 04:31:00 GMT  
		Size: 6.0 MB (6028114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97054239d5610218f0d05723d441a14db8468a06c13285a97f969709773d4178`  
		Last Modified: Tue, 09 Feb 2021 04:31:38 GMT  
		Size: 38.5 MB (38502341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f43bc65242ba82f02506f64d85701f9c77545eb0b27c358b4485d6904721ad`  
		Last Modified: Tue, 09 Feb 2021 04:31:29 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7adfc4f590d599d4ffcc7b0942e21ba4bf06a0e9406b85dd3984a80066badaa0`  
		Last Modified: Tue, 09 Feb 2021 04:31:29 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa90b76c984b1fd857a54f0cf52b49a189c1e0989ba0d5daba83447beb7041e2`  
		Last Modified: Tue, 09 Feb 2021 04:31:29 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.8`

```console
$ docker pull chronograf@sha256:36337a26f42df73c273f15841e64b1b898f1223f1aa158c10bebf668785a9d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8.8` - linux; amd64

```console
$ docker pull chronograf@sha256:6bbfbbd73180964dbe313647223e80ee0e165ae05015db86639ba20f0f78931d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70424385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d0154a00f46e5c1657d665aa2fc18c9c0242b2db7f64caa4e6658ed6b4ef60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:30 GMT
ADD file:da0c935ddc86ca9e44bdd5f61b46c7b43a115ee4bc356324265a7ad6323f61ae in / 
# Tue, 09 Feb 2021 02:23:30 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 02:46:21 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Feb 2021 02:47:17 GMT
ENV CHRONOGRAF_VERSION=1.8.8
# Tue, 09 Feb 2021 02:47:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 09 Feb 2021 02:47:27 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 09 Feb 2021 02:47:27 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 09 Feb 2021 02:47:28 GMT
EXPOSE 8888
# Tue, 09 Feb 2021 02:47:28 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Feb 2021 02:47:28 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 09 Feb 2021 02:47:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 02:47:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:cae7303ade7f17f84fe86b2a44880e9725cf7d6dcd17f79485360712b6af6dcd`  
		Last Modified: Tue, 09 Feb 2021 02:29:36 GMT  
		Size: 22.5 MB (22528600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603c713cc31395a01337edc5ae784741dda2d7aefb303bb93f7577486b1d1bbe`  
		Last Modified: Tue, 09 Feb 2021 02:47:56 GMT  
		Size: 6.7 MB (6742606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63600abc06b0687e4b24afa150d2da557c51a85b33e91502d51071591e5e6d82`  
		Last Modified: Tue, 09 Feb 2021 02:48:34 GMT  
		Size: 41.1 MB (41128782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3b434ef96cd8f4643d0c998ec73edb0b44c26d4e31cd5bca7c5f29b9400a0d`  
		Last Modified: Tue, 09 Feb 2021 02:48:27 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8145a040da7204ae6decb8f85b3096c06ade1972f6b6d4ab0496b789a24ce2`  
		Last Modified: Tue, 09 Feb 2021 02:48:27 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391ffb32b78cc26585c3ddd4ecc5590a8961c93e839ed73b88da29e4ad507ee7`  
		Last Modified: Tue, 09 Feb 2021 02:48:27 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:4bd93b3e7a1947354ca40608ba8679b477b93627fd704564f8844ec6583ae0ab
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63839627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31720bcd6ff8befefc1ba22809f3f7384cadcf9aac801b8e42422eba6027788b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Feb 2021 03:05:17 GMT
ADD file:42ae9de4db7ca66ccb0a5bc0291a00b2b1ad3c62e6e2d6bad1f99c693e981676 in / 
# Tue, 09 Feb 2021 03:05:19 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:43:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Feb 2021 06:44:47 GMT
ENV CHRONOGRAF_VERSION=1.8.8
# Tue, 09 Feb 2021 06:45:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 09 Feb 2021 06:45:08 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 09 Feb 2021 06:45:09 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 09 Feb 2021 06:45:10 GMT
EXPOSE 8888
# Tue, 09 Feb 2021 06:45:11 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Feb 2021 06:45:13 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 09 Feb 2021 06:45:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 06:45:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ebe5f2b760402bf53dfee026659ac0188dc5418dfde6839893f442bbfe23e42f`  
		Last Modified: Tue, 09 Feb 2021 03:13:48 GMT  
		Size: 19.3 MB (19316094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2a61da9a3e077953d6f78e9f324764fa0ee1dca73300f2c2e9453fc6ea84b5`  
		Last Modified: Tue, 09 Feb 2021 06:45:34 GMT  
		Size: 5.8 MB (5764950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37a1d6ec067d7ad885ae39385325d7b4d962e44a9606ac244f28cf7e0ef1c20`  
		Last Modified: Tue, 09 Feb 2021 06:46:18 GMT  
		Size: 38.7 MB (38734189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94bf3287fbb0eceb91a3df640fac834a6269be6dd059d7d74a2eaa6c45520d9`  
		Last Modified: Tue, 09 Feb 2021 06:46:05 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01f4f97106955daa8a8383b91693e231660a91e456c56c3c0eb30856c6d2d4a`  
		Last Modified: Tue, 09 Feb 2021 06:46:05 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd788b08bcc284b72a7696f72bfbabb0b3c44967caa6daaa71b425e112cc3a1`  
		Last Modified: Tue, 09 Feb 2021 06:46:05 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:7f130666c6361906f40355f639d52098ddfb14057bc887b3fb0624dc46f071cc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64944267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2a6436ea35a9248cd7a1fab7947bda22ebd1b384802f92f4381c3a4ab5995b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Feb 2021 02:43:38 GMT
ADD file:ec0f3f5aad51202b992acbfa7ec19738608d022983bc1918d7d9eecdd35e4800 in / 
# Tue, 09 Feb 2021 02:43:40 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:28:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Feb 2021 04:30:15 GMT
ENV CHRONOGRAF_VERSION=1.8.8
# Tue, 09 Feb 2021 04:30:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 09 Feb 2021 04:30:30 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 09 Feb 2021 04:30:30 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 09 Feb 2021 04:30:31 GMT
EXPOSE 8888
# Tue, 09 Feb 2021 04:30:32 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Feb 2021 04:30:32 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 09 Feb 2021 04:30:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 04:30:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b373a42fa9174db1e441a19411c9622d41f6db219878945ed0cb256efa32c8a6`  
		Last Modified: Tue, 09 Feb 2021 02:50:08 GMT  
		Size: 20.4 MB (20389427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b4b210d138fd2393967f174396ed44ec8cbf98472a90f6928614b79905e1c7`  
		Last Modified: Tue, 09 Feb 2021 04:31:00 GMT  
		Size: 6.0 MB (6028114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97054239d5610218f0d05723d441a14db8468a06c13285a97f969709773d4178`  
		Last Modified: Tue, 09 Feb 2021 04:31:38 GMT  
		Size: 38.5 MB (38502341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f43bc65242ba82f02506f64d85701f9c77545eb0b27c358b4485d6904721ad`  
		Last Modified: Tue, 09 Feb 2021 04:31:29 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7adfc4f590d599d4ffcc7b0942e21ba4bf06a0e9406b85dd3984a80066badaa0`  
		Last Modified: Tue, 09 Feb 2021 04:31:29 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa90b76c984b1fd857a54f0cf52b49a189c1e0989ba0d5daba83447beb7041e2`  
		Last Modified: Tue, 09 Feb 2021 04:31:29 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.8-alpine`

```console
$ docker pull chronograf@sha256:189b99c39ec40fb2e81f8a2b66dcf9be042ff8b11a77dfd85a7cf29638fe0f1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:1.8.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:66430ad6ccc59e8f4ec6147fdb4b96a50b621facc07bb7ea14751af7e165e64d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 MB (25350554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c25bedeb7151ac704e5948b19e5785ebebeffecf9f9aeda0ffb2e4b034b8ab52`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:21:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:59:21 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 24 Feb 2021 21:00:03 GMT
ENV CHRONOGRAF_VERSION=1.8.8
# Wed, 24 Feb 2021 21:00:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 24 Feb 2021 21:00:07 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 24 Feb 2021 21:00:07 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 24 Feb 2021 21:00:08 GMT
EXPOSE 8888
# Wed, 24 Feb 2021 21:00:08 GMT
VOLUME [/var/lib/chronograf]
# Wed, 24 Feb 2021 21:00:08 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 24 Feb 2021 21:00:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 21:00:08 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c3c544bdbd838411be7288d5c8bd23d77b89d00730ce0fa218fd7fd1694b04`  
		Last Modified: Wed, 24 Feb 2021 20:24:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b4c4e91c477308692065de267dedc098ac76d0b4d02f27d7d3ff2d2ff35287`  
		Last Modified: Wed, 24 Feb 2021 21:00:31 GMT  
		Size: 280.9 KB (280902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feb2b2d5ddaaa88b1ce85a5f4ea1b1389c45995b6245f97001b0f6a7549b32cb`  
		Last Modified: Wed, 24 Feb 2021 21:00:58 GMT  
		Size: 22.2 MB (22245636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fb8ee86b2f01be5e469ebd670fa79929d578c0c6892d5d33e72f2e70eb486d`  
		Last Modified: Wed, 24 Feb 2021 21:00:54 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9fd1ff815227f707200b859b6f803e6ed4cb31fd9a1e6b0a6aa5c5bdda101f6`  
		Last Modified: Wed, 24 Feb 2021 21:00:52 GMT  
		Size: 11.9 KB (11894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ad7c51807f76958809e44f1a1e7b92a6097c900f61e758399311e6526ecf3c`  
		Last Modified: Wed, 24 Feb 2021 21:00:52 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:189b99c39ec40fb2e81f8a2b66dcf9be042ff8b11a77dfd85a7cf29638fe0f1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:66430ad6ccc59e8f4ec6147fdb4b96a50b621facc07bb7ea14751af7e165e64d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 MB (25350554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c25bedeb7151ac704e5948b19e5785ebebeffecf9f9aeda0ffb2e4b034b8ab52`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:21:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:59:21 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 24 Feb 2021 21:00:03 GMT
ENV CHRONOGRAF_VERSION=1.8.8
# Wed, 24 Feb 2021 21:00:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 24 Feb 2021 21:00:07 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 24 Feb 2021 21:00:07 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 24 Feb 2021 21:00:08 GMT
EXPOSE 8888
# Wed, 24 Feb 2021 21:00:08 GMT
VOLUME [/var/lib/chronograf]
# Wed, 24 Feb 2021 21:00:08 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 24 Feb 2021 21:00:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 21:00:08 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c3c544bdbd838411be7288d5c8bd23d77b89d00730ce0fa218fd7fd1694b04`  
		Last Modified: Wed, 24 Feb 2021 20:24:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b4c4e91c477308692065de267dedc098ac76d0b4d02f27d7d3ff2d2ff35287`  
		Last Modified: Wed, 24 Feb 2021 21:00:31 GMT  
		Size: 280.9 KB (280902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feb2b2d5ddaaa88b1ce85a5f4ea1b1389c45995b6245f97001b0f6a7549b32cb`  
		Last Modified: Wed, 24 Feb 2021 21:00:58 GMT  
		Size: 22.2 MB (22245636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fb8ee86b2f01be5e469ebd670fa79929d578c0c6892d5d33e72f2e70eb486d`  
		Last Modified: Wed, 24 Feb 2021 21:00:54 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9fd1ff815227f707200b859b6f803e6ed4cb31fd9a1e6b0a6aa5c5bdda101f6`  
		Last Modified: Wed, 24 Feb 2021 21:00:52 GMT  
		Size: 11.9 KB (11894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ad7c51807f76958809e44f1a1e7b92a6097c900f61e758399311e6526ecf3c`  
		Last Modified: Wed, 24 Feb 2021 21:00:52 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:189b99c39ec40fb2e81f8a2b66dcf9be042ff8b11a77dfd85a7cf29638fe0f1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:66430ad6ccc59e8f4ec6147fdb4b96a50b621facc07bb7ea14751af7e165e64d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 MB (25350554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c25bedeb7151ac704e5948b19e5785ebebeffecf9f9aeda0ffb2e4b034b8ab52`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:21:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:59:21 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 24 Feb 2021 21:00:03 GMT
ENV CHRONOGRAF_VERSION=1.8.8
# Wed, 24 Feb 2021 21:00:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 24 Feb 2021 21:00:07 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 24 Feb 2021 21:00:07 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 24 Feb 2021 21:00:08 GMT
EXPOSE 8888
# Wed, 24 Feb 2021 21:00:08 GMT
VOLUME [/var/lib/chronograf]
# Wed, 24 Feb 2021 21:00:08 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 24 Feb 2021 21:00:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 21:00:08 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c3c544bdbd838411be7288d5c8bd23d77b89d00730ce0fa218fd7fd1694b04`  
		Last Modified: Wed, 24 Feb 2021 20:24:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b4c4e91c477308692065de267dedc098ac76d0b4d02f27d7d3ff2d2ff35287`  
		Last Modified: Wed, 24 Feb 2021 21:00:31 GMT  
		Size: 280.9 KB (280902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feb2b2d5ddaaa88b1ce85a5f4ea1b1389c45995b6245f97001b0f6a7549b32cb`  
		Last Modified: Wed, 24 Feb 2021 21:00:58 GMT  
		Size: 22.2 MB (22245636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fb8ee86b2f01be5e469ebd670fa79929d578c0c6892d5d33e72f2e70eb486d`  
		Last Modified: Wed, 24 Feb 2021 21:00:54 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9fd1ff815227f707200b859b6f803e6ed4cb31fd9a1e6b0a6aa5c5bdda101f6`  
		Last Modified: Wed, 24 Feb 2021 21:00:52 GMT  
		Size: 11.9 KB (11894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ad7c51807f76958809e44f1a1e7b92a6097c900f61e758399311e6526ecf3c`  
		Last Modified: Wed, 24 Feb 2021 21:00:52 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:36337a26f42df73c273f15841e64b1b898f1223f1aa158c10bebf668785a9d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:6bbfbbd73180964dbe313647223e80ee0e165ae05015db86639ba20f0f78931d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70424385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d0154a00f46e5c1657d665aa2fc18c9c0242b2db7f64caa4e6658ed6b4ef60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:30 GMT
ADD file:da0c935ddc86ca9e44bdd5f61b46c7b43a115ee4bc356324265a7ad6323f61ae in / 
# Tue, 09 Feb 2021 02:23:30 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 02:46:21 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Feb 2021 02:47:17 GMT
ENV CHRONOGRAF_VERSION=1.8.8
# Tue, 09 Feb 2021 02:47:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 09 Feb 2021 02:47:27 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 09 Feb 2021 02:47:27 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 09 Feb 2021 02:47:28 GMT
EXPOSE 8888
# Tue, 09 Feb 2021 02:47:28 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Feb 2021 02:47:28 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 09 Feb 2021 02:47:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 02:47:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:cae7303ade7f17f84fe86b2a44880e9725cf7d6dcd17f79485360712b6af6dcd`  
		Last Modified: Tue, 09 Feb 2021 02:29:36 GMT  
		Size: 22.5 MB (22528600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603c713cc31395a01337edc5ae784741dda2d7aefb303bb93f7577486b1d1bbe`  
		Last Modified: Tue, 09 Feb 2021 02:47:56 GMT  
		Size: 6.7 MB (6742606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63600abc06b0687e4b24afa150d2da557c51a85b33e91502d51071591e5e6d82`  
		Last Modified: Tue, 09 Feb 2021 02:48:34 GMT  
		Size: 41.1 MB (41128782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3b434ef96cd8f4643d0c998ec73edb0b44c26d4e31cd5bca7c5f29b9400a0d`  
		Last Modified: Tue, 09 Feb 2021 02:48:27 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8145a040da7204ae6decb8f85b3096c06ade1972f6b6d4ab0496b789a24ce2`  
		Last Modified: Tue, 09 Feb 2021 02:48:27 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391ffb32b78cc26585c3ddd4ecc5590a8961c93e839ed73b88da29e4ad507ee7`  
		Last Modified: Tue, 09 Feb 2021 02:48:27 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:4bd93b3e7a1947354ca40608ba8679b477b93627fd704564f8844ec6583ae0ab
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63839627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31720bcd6ff8befefc1ba22809f3f7384cadcf9aac801b8e42422eba6027788b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Feb 2021 03:05:17 GMT
ADD file:42ae9de4db7ca66ccb0a5bc0291a00b2b1ad3c62e6e2d6bad1f99c693e981676 in / 
# Tue, 09 Feb 2021 03:05:19 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:43:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Feb 2021 06:44:47 GMT
ENV CHRONOGRAF_VERSION=1.8.8
# Tue, 09 Feb 2021 06:45:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 09 Feb 2021 06:45:08 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 09 Feb 2021 06:45:09 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 09 Feb 2021 06:45:10 GMT
EXPOSE 8888
# Tue, 09 Feb 2021 06:45:11 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Feb 2021 06:45:13 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 09 Feb 2021 06:45:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 06:45:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ebe5f2b760402bf53dfee026659ac0188dc5418dfde6839893f442bbfe23e42f`  
		Last Modified: Tue, 09 Feb 2021 03:13:48 GMT  
		Size: 19.3 MB (19316094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2a61da9a3e077953d6f78e9f324764fa0ee1dca73300f2c2e9453fc6ea84b5`  
		Last Modified: Tue, 09 Feb 2021 06:45:34 GMT  
		Size: 5.8 MB (5764950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37a1d6ec067d7ad885ae39385325d7b4d962e44a9606ac244f28cf7e0ef1c20`  
		Last Modified: Tue, 09 Feb 2021 06:46:18 GMT  
		Size: 38.7 MB (38734189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94bf3287fbb0eceb91a3df640fac834a6269be6dd059d7d74a2eaa6c45520d9`  
		Last Modified: Tue, 09 Feb 2021 06:46:05 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01f4f97106955daa8a8383b91693e231660a91e456c56c3c0eb30856c6d2d4a`  
		Last Modified: Tue, 09 Feb 2021 06:46:05 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd788b08bcc284b72a7696f72bfbabb0b3c44967caa6daaa71b425e112cc3a1`  
		Last Modified: Tue, 09 Feb 2021 06:46:05 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:7f130666c6361906f40355f639d52098ddfb14057bc887b3fb0624dc46f071cc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64944267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2a6436ea35a9248cd7a1fab7947bda22ebd1b384802f92f4381c3a4ab5995b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Feb 2021 02:43:38 GMT
ADD file:ec0f3f5aad51202b992acbfa7ec19738608d022983bc1918d7d9eecdd35e4800 in / 
# Tue, 09 Feb 2021 02:43:40 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:28:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Feb 2021 04:30:15 GMT
ENV CHRONOGRAF_VERSION=1.8.8
# Tue, 09 Feb 2021 04:30:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 09 Feb 2021 04:30:30 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 09 Feb 2021 04:30:30 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 09 Feb 2021 04:30:31 GMT
EXPOSE 8888
# Tue, 09 Feb 2021 04:30:32 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Feb 2021 04:30:32 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 09 Feb 2021 04:30:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 04:30:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b373a42fa9174db1e441a19411c9622d41f6db219878945ed0cb256efa32c8a6`  
		Last Modified: Tue, 09 Feb 2021 02:50:08 GMT  
		Size: 20.4 MB (20389427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b4b210d138fd2393967f174396ed44ec8cbf98472a90f6928614b79905e1c7`  
		Last Modified: Tue, 09 Feb 2021 04:31:00 GMT  
		Size: 6.0 MB (6028114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97054239d5610218f0d05723d441a14db8468a06c13285a97f969709773d4178`  
		Last Modified: Tue, 09 Feb 2021 04:31:38 GMT  
		Size: 38.5 MB (38502341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f43bc65242ba82f02506f64d85701f9c77545eb0b27c358b4485d6904721ad`  
		Last Modified: Tue, 09 Feb 2021 04:31:29 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7adfc4f590d599d4ffcc7b0942e21ba4bf06a0e9406b85dd3984a80066badaa0`  
		Last Modified: Tue, 09 Feb 2021 04:31:29 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa90b76c984b1fd857a54f0cf52b49a189c1e0989ba0d5daba83447beb7041e2`  
		Last Modified: Tue, 09 Feb 2021 04:31:29 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
