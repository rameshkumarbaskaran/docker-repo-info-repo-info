<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.6`](#chronograf16)
-	[`chronograf:1.6-alpine`](#chronograf16-alpine)
-	[`chronograf:1.6.2`](#chronograf162)
-	[`chronograf:1.6.2-alpine`](#chronograf162-alpine)
-	[`chronograf:1.7`](#chronograf17)
-	[`chronograf:1.7-alpine`](#chronograf17-alpine)
-	[`chronograf:1.7.17`](#chronograf1717)
-	[`chronograf:1.7.17-alpine`](#chronograf1717-alpine)
-	[`chronograf:1.8`](#chronograf18)
-	[`chronograf:1.8-alpine`](#chronograf18-alpine)
-	[`chronograf:1.8.10`](#chronograf1810)
-	[`chronograf:1.8.10-alpine`](#chronograf1810-alpine)
-	[`chronograf:1.9`](#chronograf19)
-	[`chronograf:1.9-alpine`](#chronograf19-alpine)
-	[`chronograf:1.9.4`](#chronograf194)
-	[`chronograf:1.9.4-alpine`](#chronograf194-alpine)
-	[`chronograf:alpine`](#chronografalpine)
-	[`chronograf:latest`](#chronograflatest)

## `chronograf:1.6`

```console
$ docker pull chronograf@sha256:fa89f62d32264f001bb5bc5d23b520eacef0fd2a9c4394b74008a2cbdb8900eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6` - linux; amd64

```console
$ docker pull chronograf@sha256:8776b412f6dee5cf89b535ec95a0383864157a1818c0738033f09b0b02db7e5a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49398012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4e5baf49b6c22b31b2934bb301328f6ab16f8f0f303170cbb2946b5d50a6dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 May 2022 01:22:19 GMT
ADD file:d7acabc78d998195522bc84475bc7d834e451aba4eb84f813f1eeecc4b3269d7 in / 
# Sat, 28 May 2022 01:22:20 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:54:09 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 28 May 2022 02:54:09 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Sat, 28 May 2022 02:54:16 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 28 May 2022 02:54:17 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 28 May 2022 02:54:17 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 28 May 2022 02:54:17 GMT
EXPOSE 8888
# Sat, 28 May 2022 02:54:17 GMT
VOLUME [/var/lib/chronograf]
# Sat, 28 May 2022 02:54:17 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 28 May 2022 02:54:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 May 2022 02:54:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:73e8e05762864dd5f0a339ca8471e27294d125b63c8adfb278e84c105b8c842d`  
		Last Modified: Sat, 28 May 2022 01:29:04 GMT  
		Size: 22.6 MB (22567519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7662ef14e699ef68d3e9bfd3f48f778f1149a24d5c81007ae49fcb88de333f`  
		Last Modified: Sat, 28 May 2022 02:55:35 GMT  
		Size: 6.8 MB (6760408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:731ad90ebcddd0888557ea1fde09c1fec29c0bcbd126ec9bef83c1db76a6d4a8`  
		Last Modified: Sat, 28 May 2022 02:55:38 GMT  
		Size: 20.0 MB (20045688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d8766f2918a1f21a1e358ed47180fa58cad3db66abf8a299c9defb98835400`  
		Last Modified: Sat, 28 May 2022 02:55:34 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0fb8e9c6be5603768280d34eade3ee8ddc32dd6b2b138541001ae8b3c09207`  
		Last Modified: Sat, 28 May 2022 02:55:34 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddbaf7013fce7bf216263aca204256613f7682ec4c00b76261855635f08548cd`  
		Last Modified: Sat, 28 May 2022 02:55:34 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:a27c0cbaa413d31dab0a4217073f6153f8d9881ab1cb5d0dcfadd4c179098950
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43986139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e4ec0535f8f4e188f3cfda17b51b5f4165d4a48d17dd4154f318d548fba951`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 May 2022 01:05:51 GMT
ADD file:4dd5baef6913cbeaba8b4abeb9fa3860736e9c421334170bf9a435f002176781 in / 
# Sat, 28 May 2022 01:05:52 GMT
CMD ["bash"]
# Sun, 29 May 2022 10:55:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sun, 29 May 2022 10:55:49 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Sun, 29 May 2022 10:56:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sun, 29 May 2022 10:56:08 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sun, 29 May 2022 10:56:09 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sun, 29 May 2022 10:56:09 GMT
EXPOSE 8888
# Sun, 29 May 2022 10:56:10 GMT
VOLUME [/var/lib/chronograf]
# Sun, 29 May 2022 10:56:10 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sun, 29 May 2022 10:56:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 May 2022 10:56:11 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b1bc9eb7248815be774e7f369470fa41493ff76db8a85f10e545b1538909d9d7`  
		Last Modified: Sat, 28 May 2022 01:22:13 GMT  
		Size: 19.4 MB (19359814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4119ba187328a107b9db1a52f6838ddab5d6c6b8647c5dcff3fa9af4baf486a4`  
		Last Modified: Sun, 29 May 2022 10:59:28 GMT  
		Size: 5.8 MB (5780942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a2187321b4fa5f3d4fc36a89db14d30a6c14bc705ed54f11a0c70a9a7f1aaa`  
		Last Modified: Sun, 29 May 2022 10:59:38 GMT  
		Size: 18.8 MB (18820986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767d837ef6cb92e710393907f4986d32cf436f4d346b3354d230ed25ad7ca59b`  
		Last Modified: Sun, 29 May 2022 10:59:26 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4987ac849dd128de031a98b494760cff7f4d15ceecf174f939a290628f7d3ac2`  
		Last Modified: Sun, 29 May 2022 10:59:25 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b57912442eff406b610500e2193c3b5ab692f444d9775f2ecab133053dc1064`  
		Last Modified: Sun, 29 May 2022 10:59:25 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:76f58ca1bc760b6b7398e9378abdf407a7bb503bce6b6153fbcbb2889697cf6d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45457509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1afcda4ed80268c18523491c9c685000dff6e5b200de413139d2246688b6309`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 May 2022 00:43:00 GMT
ADD file:5d3acfb1c09652c954868b7e7fba2e995e5e143bd0f2b1c04a34897232913f7a in / 
# Sat, 28 May 2022 00:43:01 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:06:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 28 May 2022 02:06:18 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Sat, 28 May 2022 02:06:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 28 May 2022 02:06:28 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 28 May 2022 02:06:29 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 28 May 2022 02:06:29 GMT
EXPOSE 8888
# Sat, 28 May 2022 02:06:30 GMT
VOLUME [/var/lib/chronograf]
# Sat, 28 May 2022 02:06:32 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 28 May 2022 02:06:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 May 2022 02:06:33 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5787d8ce843947b58d50c514418ca92eca29e2110be4fe2993451d835d2d846a`  
		Last Modified: Sat, 28 May 2022 00:51:48 GMT  
		Size: 20.4 MB (20424104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625f22e207e828809833b2c489092f0299c587279c18e2b3a9ae4cd42c4f698f`  
		Last Modified: Sat, 28 May 2022 02:08:23 GMT  
		Size: 6.0 MB (6047429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9654088699162bb6f9ecfa018d753a933d681961dec7e85a1a58cd8ed5ca4f3`  
		Last Modified: Sat, 28 May 2022 02:08:25 GMT  
		Size: 19.0 MB (18961585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7837d1e3bd0fd182b2c26a1036dc5d778d8bd29544e0befd57c197b5e8db4f3`  
		Last Modified: Sat, 28 May 2022 02:08:22 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1022be7de059eb85f2c5ca7f0536081720b5feb91914658c468b45483872e0b4`  
		Last Modified: Sat, 28 May 2022 02:08:22 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0965c8230b7849520b48ed1654ce54259ef77c4e24196add7cfbb173aa3faad`  
		Last Modified: Sat, 28 May 2022 02:08:22 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6-alpine`

```console
$ docker pull chronograf@sha256:23417672f50b4d8e10c2afe16fb30256ea18d11c8b18476774bb7d582d31d80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.6-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:6f8f433011148165c541c6c2b5a4e5b6a0e17ed7a30e489da79572ffb65511b1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14852447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7955bca787a43198659959f56224c8b4bcdcec4f04756f3179ed0041b6b3c97a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:26:16 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 04:26:16 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 05 Apr 2022 04:26:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 05 Apr 2022 04:26:20 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Tue, 05 Apr 2022 04:26:20 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 05 Apr 2022 04:26:20 GMT
EXPOSE 8888
# Tue, 05 Apr 2022 04:26:20 GMT
VOLUME [/var/lib/chronograf]
# Tue, 05 Apr 2022 04:26:21 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 05 Apr 2022 04:26:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 04:26:21 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58beb826c7b7288de69f85c4476fd6f04b58ceed760dd1b9e51a7d80aeb0e471`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 271.7 KB (271678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec6a02657fcad83f14ccaebfe65596c725dc1a85062cc10c59315a08a6b4139`  
		Last Modified: Tue, 05 Apr 2022 04:27:21 GMT  
		Size: 11.7 MB (11737836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f48b6b7852557acd0c24a3412aff3571ae06abe1235cec3ae3c10d78c63a7f`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 12.3 KB (12274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216f28bcf9418aa7355c3934973e69b52e1bba48dd0e758a66049eaef57cbd96`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d36456c8c8f7725ba610682fd161c3b25b5bc41b4a3e2a9d384a197f9d65cc0`  
		Last Modified: Tue, 05 Apr 2022 04:27:19 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6.2`

```console
$ docker pull chronograf@sha256:fa89f62d32264f001bb5bc5d23b520eacef0fd2a9c4394b74008a2cbdb8900eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6.2` - linux; amd64

```console
$ docker pull chronograf@sha256:8776b412f6dee5cf89b535ec95a0383864157a1818c0738033f09b0b02db7e5a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49398012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4e5baf49b6c22b31b2934bb301328f6ab16f8f0f303170cbb2946b5d50a6dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 May 2022 01:22:19 GMT
ADD file:d7acabc78d998195522bc84475bc7d834e451aba4eb84f813f1eeecc4b3269d7 in / 
# Sat, 28 May 2022 01:22:20 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:54:09 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 28 May 2022 02:54:09 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Sat, 28 May 2022 02:54:16 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 28 May 2022 02:54:17 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 28 May 2022 02:54:17 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 28 May 2022 02:54:17 GMT
EXPOSE 8888
# Sat, 28 May 2022 02:54:17 GMT
VOLUME [/var/lib/chronograf]
# Sat, 28 May 2022 02:54:17 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 28 May 2022 02:54:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 May 2022 02:54:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:73e8e05762864dd5f0a339ca8471e27294d125b63c8adfb278e84c105b8c842d`  
		Last Modified: Sat, 28 May 2022 01:29:04 GMT  
		Size: 22.6 MB (22567519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7662ef14e699ef68d3e9bfd3f48f778f1149a24d5c81007ae49fcb88de333f`  
		Last Modified: Sat, 28 May 2022 02:55:35 GMT  
		Size: 6.8 MB (6760408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:731ad90ebcddd0888557ea1fde09c1fec29c0bcbd126ec9bef83c1db76a6d4a8`  
		Last Modified: Sat, 28 May 2022 02:55:38 GMT  
		Size: 20.0 MB (20045688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d8766f2918a1f21a1e358ed47180fa58cad3db66abf8a299c9defb98835400`  
		Last Modified: Sat, 28 May 2022 02:55:34 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0fb8e9c6be5603768280d34eade3ee8ddc32dd6b2b138541001ae8b3c09207`  
		Last Modified: Sat, 28 May 2022 02:55:34 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddbaf7013fce7bf216263aca204256613f7682ec4c00b76261855635f08548cd`  
		Last Modified: Sat, 28 May 2022 02:55:34 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:a27c0cbaa413d31dab0a4217073f6153f8d9881ab1cb5d0dcfadd4c179098950
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43986139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e4ec0535f8f4e188f3cfda17b51b5f4165d4a48d17dd4154f318d548fba951`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 May 2022 01:05:51 GMT
ADD file:4dd5baef6913cbeaba8b4abeb9fa3860736e9c421334170bf9a435f002176781 in / 
# Sat, 28 May 2022 01:05:52 GMT
CMD ["bash"]
# Sun, 29 May 2022 10:55:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sun, 29 May 2022 10:55:49 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Sun, 29 May 2022 10:56:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sun, 29 May 2022 10:56:08 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sun, 29 May 2022 10:56:09 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sun, 29 May 2022 10:56:09 GMT
EXPOSE 8888
# Sun, 29 May 2022 10:56:10 GMT
VOLUME [/var/lib/chronograf]
# Sun, 29 May 2022 10:56:10 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sun, 29 May 2022 10:56:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 May 2022 10:56:11 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b1bc9eb7248815be774e7f369470fa41493ff76db8a85f10e545b1538909d9d7`  
		Last Modified: Sat, 28 May 2022 01:22:13 GMT  
		Size: 19.4 MB (19359814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4119ba187328a107b9db1a52f6838ddab5d6c6b8647c5dcff3fa9af4baf486a4`  
		Last Modified: Sun, 29 May 2022 10:59:28 GMT  
		Size: 5.8 MB (5780942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a2187321b4fa5f3d4fc36a89db14d30a6c14bc705ed54f11a0c70a9a7f1aaa`  
		Last Modified: Sun, 29 May 2022 10:59:38 GMT  
		Size: 18.8 MB (18820986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767d837ef6cb92e710393907f4986d32cf436f4d346b3354d230ed25ad7ca59b`  
		Last Modified: Sun, 29 May 2022 10:59:26 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4987ac849dd128de031a98b494760cff7f4d15ceecf174f939a290628f7d3ac2`  
		Last Modified: Sun, 29 May 2022 10:59:25 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b57912442eff406b610500e2193c3b5ab692f444d9775f2ecab133053dc1064`  
		Last Modified: Sun, 29 May 2022 10:59:25 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:76f58ca1bc760b6b7398e9378abdf407a7bb503bce6b6153fbcbb2889697cf6d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45457509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1afcda4ed80268c18523491c9c685000dff6e5b200de413139d2246688b6309`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 May 2022 00:43:00 GMT
ADD file:5d3acfb1c09652c954868b7e7fba2e995e5e143bd0f2b1c04a34897232913f7a in / 
# Sat, 28 May 2022 00:43:01 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:06:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 28 May 2022 02:06:18 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Sat, 28 May 2022 02:06:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 28 May 2022 02:06:28 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 28 May 2022 02:06:29 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 28 May 2022 02:06:29 GMT
EXPOSE 8888
# Sat, 28 May 2022 02:06:30 GMT
VOLUME [/var/lib/chronograf]
# Sat, 28 May 2022 02:06:32 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 28 May 2022 02:06:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 May 2022 02:06:33 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5787d8ce843947b58d50c514418ca92eca29e2110be4fe2993451d835d2d846a`  
		Last Modified: Sat, 28 May 2022 00:51:48 GMT  
		Size: 20.4 MB (20424104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625f22e207e828809833b2c489092f0299c587279c18e2b3a9ae4cd42c4f698f`  
		Last Modified: Sat, 28 May 2022 02:08:23 GMT  
		Size: 6.0 MB (6047429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9654088699162bb6f9ecfa018d753a933d681961dec7e85a1a58cd8ed5ca4f3`  
		Last Modified: Sat, 28 May 2022 02:08:25 GMT  
		Size: 19.0 MB (18961585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7837d1e3bd0fd182b2c26a1036dc5d778d8bd29544e0befd57c197b5e8db4f3`  
		Last Modified: Sat, 28 May 2022 02:08:22 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1022be7de059eb85f2c5ca7f0536081720b5feb91914658c468b45483872e0b4`  
		Last Modified: Sat, 28 May 2022 02:08:22 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0965c8230b7849520b48ed1654ce54259ef77c4e24196add7cfbb173aa3faad`  
		Last Modified: Sat, 28 May 2022 02:08:22 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6.2-alpine`

```console
$ docker pull chronograf@sha256:23417672f50b4d8e10c2afe16fb30256ea18d11c8b18476774bb7d582d31d80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.6.2-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:6f8f433011148165c541c6c2b5a4e5b6a0e17ed7a30e489da79572ffb65511b1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14852447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7955bca787a43198659959f56224c8b4bcdcec4f04756f3179ed0041b6b3c97a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:26:16 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 04:26:16 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 05 Apr 2022 04:26:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 05 Apr 2022 04:26:20 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Tue, 05 Apr 2022 04:26:20 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 05 Apr 2022 04:26:20 GMT
EXPOSE 8888
# Tue, 05 Apr 2022 04:26:20 GMT
VOLUME [/var/lib/chronograf]
# Tue, 05 Apr 2022 04:26:21 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 05 Apr 2022 04:26:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 04:26:21 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58beb826c7b7288de69f85c4476fd6f04b58ceed760dd1b9e51a7d80aeb0e471`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 271.7 KB (271678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec6a02657fcad83f14ccaebfe65596c725dc1a85062cc10c59315a08a6b4139`  
		Last Modified: Tue, 05 Apr 2022 04:27:21 GMT  
		Size: 11.7 MB (11737836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f48b6b7852557acd0c24a3412aff3571ae06abe1235cec3ae3c10d78c63a7f`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 12.3 KB (12274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216f28bcf9418aa7355c3934973e69b52e1bba48dd0e758a66049eaef57cbd96`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d36456c8c8f7725ba610682fd161c3b25b5bc41b4a3e2a9d384a197f9d65cc0`  
		Last Modified: Tue, 05 Apr 2022 04:27:19 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:ffdff47d9ad590ef22d30aab1dc79f6462d8b17ad77e279ae3842c84165a79ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7` - linux; amd64

```console
$ docker pull chronograf@sha256:32a93900073a9b1190ddb923bbc3330bfd08b66cb411434c300bd2f4673d811d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65427092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79376e2eff312c91161b808dbc1cf8b6d2a0175956bb67cc6468af94704a89bf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 May 2022 01:22:19 GMT
ADD file:d7acabc78d998195522bc84475bc7d834e451aba4eb84f813f1eeecc4b3269d7 in / 
# Sat, 28 May 2022 01:22:20 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:54:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 28 May 2022 02:54:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Sat, 28 May 2022 02:54:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 28 May 2022 02:54:42 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 28 May 2022 02:54:42 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 28 May 2022 02:54:42 GMT
EXPOSE 8888
# Sat, 28 May 2022 02:54:42 GMT
VOLUME [/var/lib/chronograf]
# Sat, 28 May 2022 02:54:43 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 28 May 2022 02:54:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 May 2022 02:54:43 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:73e8e05762864dd5f0a339ca8471e27294d125b63c8adfb278e84c105b8c842d`  
		Last Modified: Sat, 28 May 2022 01:29:04 GMT  
		Size: 22.6 MB (22567519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98611c8ed04c1565c75f25cc6f9a836a256a54f6f3336b99e4fe4955e0abf0c5`  
		Last Modified: Sat, 28 May 2022 02:55:48 GMT  
		Size: 4.5 MB (4506789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82ee52431fd6486ebef86acccf7dedb20bf267f0e02c58efdd29b2a2d0336e7`  
		Last Modified: Sat, 28 May 2022 02:55:53 GMT  
		Size: 38.3 MB (38328396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9b71ebd5ce218c19e6c6595f00993b9e3a273254860b349c8a45e4e8f25c99`  
		Last Modified: Sat, 28 May 2022 02:55:47 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3e7f7e1a7dfa5652ac955a7113e4995ac4859adf0babab278c3b930696b3b5`  
		Last Modified: Sat, 28 May 2022 02:55:48 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65687aca6dbf84ab423dae24bdcf38458522edb70c2aa684bc436933153a9be9`  
		Last Modified: Sat, 28 May 2022 02:55:47 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:3ab9c3ae4dbe93d0c68b2b13a6f5f1a6693eb318c8ef96d429a0ea95931012fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59047797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:710d8146a656c6b6260367fdbfe3c7ab297bc0818936a6852aec4166c31e5753`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 May 2022 01:05:51 GMT
ADD file:4dd5baef6913cbeaba8b4abeb9fa3860736e9c421334170bf9a435f002176781 in / 
# Sat, 28 May 2022 01:05:52 GMT
CMD ["bash"]
# Sun, 29 May 2022 10:56:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sun, 29 May 2022 10:56:45 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Sun, 29 May 2022 10:57:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sun, 29 May 2022 10:57:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sun, 29 May 2022 10:57:16 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sun, 29 May 2022 10:57:17 GMT
EXPOSE 8888
# Sun, 29 May 2022 10:57:17 GMT
VOLUME [/var/lib/chronograf]
# Sun, 29 May 2022 10:57:17 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sun, 29 May 2022 10:57:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 May 2022 10:57:18 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b1bc9eb7248815be774e7f369470fa41493ff76db8a85f10e545b1538909d9d7`  
		Last Modified: Sat, 28 May 2022 01:22:13 GMT  
		Size: 19.4 MB (19359814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be570855153de9294811361809dbf8420e01f00470116c7f002ef9e8428ef71f`  
		Last Modified: Sun, 29 May 2022 10:59:51 GMT  
		Size: 3.9 MB (3880111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e9c5c6e4c4643ac7a75a35d35080940f4dde2c6372b4de4a7745bd416b32c2`  
		Last Modified: Sun, 29 May 2022 11:00:09 GMT  
		Size: 35.8 MB (35783472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50aff1f4d8cf55ec3328e89533e93a50fa6d37466aecbe52bfbd6ff8ba527d1`  
		Last Modified: Sun, 29 May 2022 10:59:49 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ebaf2e61cba1434d8eae96da6e40f1adeb21e55401ffed7af372e4bcbbb9ba`  
		Last Modified: Sun, 29 May 2022 10:59:49 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13de0aaa586114a36f64e0985b4bb3f8c2af13d6f745bea44cb13c415d2fb1b2`  
		Last Modified: Sun, 29 May 2022 10:59:49 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:332c6d6ccf18ca594582dd4d1d6444dc92220acbe877e6f833f64cdbcfd190d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60329363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b55afde15022aa61b3108116f3f7588b01b13c7b1bd452bfd00c85cb9f16a88`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 May 2022 00:43:00 GMT
ADD file:5d3acfb1c09652c954868b7e7fba2e995e5e143bd0f2b1c04a34897232913f7a in / 
# Sat, 28 May 2022 00:43:01 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:06:47 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 28 May 2022 02:06:48 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Sat, 28 May 2022 02:07:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 28 May 2022 02:07:04 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 28 May 2022 02:07:05 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 28 May 2022 02:07:05 GMT
EXPOSE 8888
# Sat, 28 May 2022 02:07:06 GMT
VOLUME [/var/lib/chronograf]
# Sat, 28 May 2022 02:07:08 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 28 May 2022 02:07:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 May 2022 02:07:09 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5787d8ce843947b58d50c514418ca92eca29e2110be4fe2993451d835d2d846a`  
		Last Modified: Sat, 28 May 2022 00:51:48 GMT  
		Size: 20.4 MB (20424104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df14918e634f11689ccd0550a9e2d468d7fa27a73b12e2088c75e4e7b3cc484d`  
		Last Modified: Sat, 28 May 2022 02:08:37 GMT  
		Size: 3.9 MB (3893953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a5a2090703fc4cebf944fd587646bf8223e3aa10edc840e46a24deead86e57`  
		Last Modified: Sat, 28 May 2022 02:08:40 GMT  
		Size: 36.0 MB (35986913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:380e4417f7f77d8c7674ef38e785fbf4a780501504ac2236fb88391100f24c3f`  
		Last Modified: Sat, 28 May 2022 02:08:36 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4536b874a72f7bab6c303526e6c9d422db9213fe9068d8be25d75a210dd8fc`  
		Last Modified: Sat, 28 May 2022 02:08:36 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e189b1314aff80643afa88a41580b75c279f9e9159d12945daed969986f947`  
		Last Modified: Sat, 28 May 2022 02:08:36 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:990421b8bc9b5dd6d472bd68efb5b165bf5f909c1b4a841756198933b14513d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:386f11aba61ccd79dd3d8105edce283d4eac402a7c92b802beb7ad89cf3136a1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22670798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7c75f57862ead544bf92efebf86f59028a171990d14514c9cc621d7807042a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:26:16 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 04:26:26 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 05 Apr 2022 04:26:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 05 Apr 2022 04:26:31 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 05 Apr 2022 04:26:31 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 05 Apr 2022 04:26:31 GMT
EXPOSE 8888
# Tue, 05 Apr 2022 04:26:32 GMT
VOLUME [/var/lib/chronograf]
# Tue, 05 Apr 2022 04:26:32 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 05 Apr 2022 04:26:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 04:26:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58beb826c7b7288de69f85c4476fd6f04b58ceed760dd1b9e51a7d80aeb0e471`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 271.7 KB (271678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8ba42ef9e34fc8eb0a6b88a3cd9242247e7029eaaed6b3d13f3f77eba9bb4f`  
		Last Modified: Tue, 05 Apr 2022 04:27:35 GMT  
		Size: 19.6 MB (19556196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e98e5f05434dd7e69e4acfb1c9682f93ab2c0d204b09dac76ccbc8fac82952`  
		Last Modified: Tue, 05 Apr 2022 04:27:32 GMT  
		Size: 12.3 KB (12264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12636f40cb960e763e7c41f0b801007ade339c74aac79418124da7df48f27a7f`  
		Last Modified: Tue, 05 Apr 2022 04:27:32 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e7c964b7b93ca840cc02a49bcee2e824dccd67e40f48c0d16b239cc3b3e2be1`  
		Last Modified: Tue, 05 Apr 2022 04:27:32 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:ffdff47d9ad590ef22d30aab1dc79f6462d8b17ad77e279ae3842c84165a79ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7.17` - linux; amd64

```console
$ docker pull chronograf@sha256:32a93900073a9b1190ddb923bbc3330bfd08b66cb411434c300bd2f4673d811d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65427092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79376e2eff312c91161b808dbc1cf8b6d2a0175956bb67cc6468af94704a89bf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 May 2022 01:22:19 GMT
ADD file:d7acabc78d998195522bc84475bc7d834e451aba4eb84f813f1eeecc4b3269d7 in / 
# Sat, 28 May 2022 01:22:20 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:54:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 28 May 2022 02:54:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Sat, 28 May 2022 02:54:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 28 May 2022 02:54:42 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 28 May 2022 02:54:42 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 28 May 2022 02:54:42 GMT
EXPOSE 8888
# Sat, 28 May 2022 02:54:42 GMT
VOLUME [/var/lib/chronograf]
# Sat, 28 May 2022 02:54:43 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 28 May 2022 02:54:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 May 2022 02:54:43 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:73e8e05762864dd5f0a339ca8471e27294d125b63c8adfb278e84c105b8c842d`  
		Last Modified: Sat, 28 May 2022 01:29:04 GMT  
		Size: 22.6 MB (22567519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98611c8ed04c1565c75f25cc6f9a836a256a54f6f3336b99e4fe4955e0abf0c5`  
		Last Modified: Sat, 28 May 2022 02:55:48 GMT  
		Size: 4.5 MB (4506789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82ee52431fd6486ebef86acccf7dedb20bf267f0e02c58efdd29b2a2d0336e7`  
		Last Modified: Sat, 28 May 2022 02:55:53 GMT  
		Size: 38.3 MB (38328396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9b71ebd5ce218c19e6c6595f00993b9e3a273254860b349c8a45e4e8f25c99`  
		Last Modified: Sat, 28 May 2022 02:55:47 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3e7f7e1a7dfa5652ac955a7113e4995ac4859adf0babab278c3b930696b3b5`  
		Last Modified: Sat, 28 May 2022 02:55:48 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65687aca6dbf84ab423dae24bdcf38458522edb70c2aa684bc436933153a9be9`  
		Last Modified: Sat, 28 May 2022 02:55:47 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:3ab9c3ae4dbe93d0c68b2b13a6f5f1a6693eb318c8ef96d429a0ea95931012fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59047797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:710d8146a656c6b6260367fdbfe3c7ab297bc0818936a6852aec4166c31e5753`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 May 2022 01:05:51 GMT
ADD file:4dd5baef6913cbeaba8b4abeb9fa3860736e9c421334170bf9a435f002176781 in / 
# Sat, 28 May 2022 01:05:52 GMT
CMD ["bash"]
# Sun, 29 May 2022 10:56:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sun, 29 May 2022 10:56:45 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Sun, 29 May 2022 10:57:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sun, 29 May 2022 10:57:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sun, 29 May 2022 10:57:16 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sun, 29 May 2022 10:57:17 GMT
EXPOSE 8888
# Sun, 29 May 2022 10:57:17 GMT
VOLUME [/var/lib/chronograf]
# Sun, 29 May 2022 10:57:17 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sun, 29 May 2022 10:57:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 May 2022 10:57:18 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b1bc9eb7248815be774e7f369470fa41493ff76db8a85f10e545b1538909d9d7`  
		Last Modified: Sat, 28 May 2022 01:22:13 GMT  
		Size: 19.4 MB (19359814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be570855153de9294811361809dbf8420e01f00470116c7f002ef9e8428ef71f`  
		Last Modified: Sun, 29 May 2022 10:59:51 GMT  
		Size: 3.9 MB (3880111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e9c5c6e4c4643ac7a75a35d35080940f4dde2c6372b4de4a7745bd416b32c2`  
		Last Modified: Sun, 29 May 2022 11:00:09 GMT  
		Size: 35.8 MB (35783472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50aff1f4d8cf55ec3328e89533e93a50fa6d37466aecbe52bfbd6ff8ba527d1`  
		Last Modified: Sun, 29 May 2022 10:59:49 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ebaf2e61cba1434d8eae96da6e40f1adeb21e55401ffed7af372e4bcbbb9ba`  
		Last Modified: Sun, 29 May 2022 10:59:49 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13de0aaa586114a36f64e0985b4bb3f8c2af13d6f745bea44cb13c415d2fb1b2`  
		Last Modified: Sun, 29 May 2022 10:59:49 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:332c6d6ccf18ca594582dd4d1d6444dc92220acbe877e6f833f64cdbcfd190d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60329363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b55afde15022aa61b3108116f3f7588b01b13c7b1bd452bfd00c85cb9f16a88`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 May 2022 00:43:00 GMT
ADD file:5d3acfb1c09652c954868b7e7fba2e995e5e143bd0f2b1c04a34897232913f7a in / 
# Sat, 28 May 2022 00:43:01 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:06:47 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 28 May 2022 02:06:48 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Sat, 28 May 2022 02:07:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 28 May 2022 02:07:04 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 28 May 2022 02:07:05 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 28 May 2022 02:07:05 GMT
EXPOSE 8888
# Sat, 28 May 2022 02:07:06 GMT
VOLUME [/var/lib/chronograf]
# Sat, 28 May 2022 02:07:08 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 28 May 2022 02:07:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 May 2022 02:07:09 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5787d8ce843947b58d50c514418ca92eca29e2110be4fe2993451d835d2d846a`  
		Last Modified: Sat, 28 May 2022 00:51:48 GMT  
		Size: 20.4 MB (20424104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df14918e634f11689ccd0550a9e2d468d7fa27a73b12e2088c75e4e7b3cc484d`  
		Last Modified: Sat, 28 May 2022 02:08:37 GMT  
		Size: 3.9 MB (3893953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a5a2090703fc4cebf944fd587646bf8223e3aa10edc840e46a24deead86e57`  
		Last Modified: Sat, 28 May 2022 02:08:40 GMT  
		Size: 36.0 MB (35986913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:380e4417f7f77d8c7674ef38e785fbf4a780501504ac2236fb88391100f24c3f`  
		Last Modified: Sat, 28 May 2022 02:08:36 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4536b874a72f7bab6c303526e6c9d422db9213fe9068d8be25d75a210dd8fc`  
		Last Modified: Sat, 28 May 2022 02:08:36 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e189b1314aff80643afa88a41580b75c279f9e9159d12945daed969986f947`  
		Last Modified: Sat, 28 May 2022 02:08:36 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:990421b8bc9b5dd6d472bd68efb5b165bf5f909c1b4a841756198933b14513d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:386f11aba61ccd79dd3d8105edce283d4eac402a7c92b802beb7ad89cf3136a1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22670798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7c75f57862ead544bf92efebf86f59028a171990d14514c9cc621d7807042a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:26:16 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 04:26:26 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 05 Apr 2022 04:26:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 05 Apr 2022 04:26:31 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 05 Apr 2022 04:26:31 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 05 Apr 2022 04:26:31 GMT
EXPOSE 8888
# Tue, 05 Apr 2022 04:26:32 GMT
VOLUME [/var/lib/chronograf]
# Tue, 05 Apr 2022 04:26:32 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 05 Apr 2022 04:26:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 04:26:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58beb826c7b7288de69f85c4476fd6f04b58ceed760dd1b9e51a7d80aeb0e471`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 271.7 KB (271678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8ba42ef9e34fc8eb0a6b88a3cd9242247e7029eaaed6b3d13f3f77eba9bb4f`  
		Last Modified: Tue, 05 Apr 2022 04:27:35 GMT  
		Size: 19.6 MB (19556196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e98e5f05434dd7e69e4acfb1c9682f93ab2c0d204b09dac76ccbc8fac82952`  
		Last Modified: Tue, 05 Apr 2022 04:27:32 GMT  
		Size: 12.3 KB (12264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12636f40cb960e763e7c41f0b801007ade339c74aac79418124da7df48f27a7f`  
		Last Modified: Tue, 05 Apr 2022 04:27:32 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e7c964b7b93ca840cc02a49bcee2e824dccd67e40f48c0d16b239cc3b3e2be1`  
		Last Modified: Tue, 05 Apr 2022 04:27:32 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:02c6e802958cff57cb5233b197646400ee7490827645aad84ea0cdc473b4e012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8` - linux; amd64

```console
$ docker pull chronograf@sha256:9ebce37f1cb3f8aa1367256397f33a175c1657673303c26323d67a7f52e87402
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66278958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd274d8f5f45fe5e7d766b561911351d1da0486e97f77b2797c6bdcd41334df`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 May 2022 01:22:19 GMT
ADD file:d7acabc78d998195522bc84475bc7d834e451aba4eb84f813f1eeecc4b3269d7 in / 
# Sat, 28 May 2022 01:22:20 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:54:09 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 28 May 2022 02:54:49 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Sat, 28 May 2022 02:54:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 28 May 2022 02:54:57 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 28 May 2022 02:54:57 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 28 May 2022 02:54:58 GMT
EXPOSE 8888
# Sat, 28 May 2022 02:54:58 GMT
VOLUME [/var/lib/chronograf]
# Sat, 28 May 2022 02:54:58 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 28 May 2022 02:54:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 May 2022 02:54:58 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:73e8e05762864dd5f0a339ca8471e27294d125b63c8adfb278e84c105b8c842d`  
		Last Modified: Sat, 28 May 2022 01:29:04 GMT  
		Size: 22.6 MB (22567519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7662ef14e699ef68d3e9bfd3f48f778f1149a24d5c81007ae49fcb88de333f`  
		Last Modified: Sat, 28 May 2022 02:55:35 GMT  
		Size: 6.8 MB (6760408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1fa322485e82966362f480aa009fcec37b8bfd09c75592bc599f46a271121e`  
		Last Modified: Sat, 28 May 2022 02:56:08 GMT  
		Size: 36.9 MB (36926645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23b636894f961ed3a7165ccea36caf923dd0830c99075981a4f8e2595db9837`  
		Last Modified: Sat, 28 May 2022 02:56:03 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e4dade2c0591441391f8fc707dcff92556641abc005799a5bdd252c99d3a23`  
		Last Modified: Sat, 28 May 2022 02:56:03 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8893c40a09bcf889be2676bd35705c946c2e025e04f81b480207474e38d645`  
		Last Modified: Sat, 28 May 2022 02:56:03 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:9ec0fca2836243cd7e7abd7d91f0465501bf87596c3b6d8482ca3cfcf18e6e7a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59677074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2a75af0bb3fb2c325af4810fa40d8d240a2668c567de0ed6b73782a5321ebb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 May 2022 01:05:51 GMT
ADD file:4dd5baef6913cbeaba8b4abeb9fa3860736e9c421334170bf9a435f002176781 in / 
# Sat, 28 May 2022 01:05:52 GMT
CMD ["bash"]
# Sun, 29 May 2022 10:55:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sun, 29 May 2022 10:57:37 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Sun, 29 May 2022 10:57:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sun, 29 May 2022 10:57:58 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sun, 29 May 2022 10:57:58 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sun, 29 May 2022 10:57:59 GMT
EXPOSE 8888
# Sun, 29 May 2022 10:57:59 GMT
VOLUME [/var/lib/chronograf]
# Sun, 29 May 2022 10:58:00 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sun, 29 May 2022 10:58:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 May 2022 10:58:01 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b1bc9eb7248815be774e7f369470fa41493ff76db8a85f10e545b1538909d9d7`  
		Last Modified: Sat, 28 May 2022 01:22:13 GMT  
		Size: 19.4 MB (19359814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4119ba187328a107b9db1a52f6838ddab5d6c6b8647c5dcff3fa9af4baf486a4`  
		Last Modified: Sun, 29 May 2022 10:59:28 GMT  
		Size: 5.8 MB (5780942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f14c826331b3b2a0e3043566e5772143c4f83fc4390794920fb3f01e3babc2`  
		Last Modified: Sun, 29 May 2022 11:00:38 GMT  
		Size: 34.5 MB (34511923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a134a1318b6432dc1727dfe33e397408cb8d0df0d46154780d048760482aec`  
		Last Modified: Sun, 29 May 2022 11:00:20 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d6ead8c2fb766463e52625a816b0ed0174a76a8be377cebf594520b8fe74edd`  
		Last Modified: Sun, 29 May 2022 11:00:20 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b75dff010c7ee6697b5b21fa5ef81c730ad02e409fe440ae8b064884fc801d`  
		Last Modified: Sun, 29 May 2022 11:00:20 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:23d4ccf233559cd021ba2588260cd2e3d73a1737a8c59ad08afe5ab030c30ebd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60927571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8807af89456190050c24361a794d52896ab5b862c89ec09ad0077bf2d15dea62`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 May 2022 00:43:00 GMT
ADD file:5d3acfb1c09652c954868b7e7fba2e995e5e143bd0f2b1c04a34897232913f7a in / 
# Sat, 28 May 2022 00:43:01 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:06:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 28 May 2022 02:07:16 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Sat, 28 May 2022 02:07:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 28 May 2022 02:07:27 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 28 May 2022 02:07:28 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 28 May 2022 02:07:28 GMT
EXPOSE 8888
# Sat, 28 May 2022 02:07:29 GMT
VOLUME [/var/lib/chronograf]
# Sat, 28 May 2022 02:07:31 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 28 May 2022 02:07:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 May 2022 02:07:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5787d8ce843947b58d50c514418ca92eca29e2110be4fe2993451d835d2d846a`  
		Last Modified: Sat, 28 May 2022 00:51:48 GMT  
		Size: 20.4 MB (20424104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625f22e207e828809833b2c489092f0299c587279c18e2b3a9ae4cd42c4f698f`  
		Last Modified: Sat, 28 May 2022 02:08:23 GMT  
		Size: 6.0 MB (6047429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ffd65e4d9beb391cdd07566713526dcf352fd2ab1401a18efd83bef58f20e6`  
		Last Modified: Sat, 28 May 2022 02:08:57 GMT  
		Size: 34.4 MB (34431642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a4795fa65588801427636ce8627f9d3a1b85741fbdf48ef63d7eca8a5f7f9e9`  
		Last Modified: Sat, 28 May 2022 02:08:52 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd06bed5a8c8a0be0b27d18233727be5bac0b008c8a86c28fd278dadf7811c5`  
		Last Modified: Sat, 28 May 2022 02:08:52 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304f07c65ba0277170bb563d3ddd9a19ee3a0a7f7ba29a4cf0531bfac0a4e882`  
		Last Modified: Sat, 28 May 2022 02:08:52 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:d3e3bbce6ab55cead013b905eba19cdd95cc418e5f2acfb421159ccc1bf8cbd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b28beb85949241c005e5be21181999ce565e4b29dd96295f7e2f7d8ff833a80a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22318581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb7b4f19d3448b5e558e8d6e7857db12751a4b8a0928e3f0fa36efaa296650b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:26:16 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 04:26:37 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 05 Apr 2022 04:26:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 05 Apr 2022 04:26:43 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 05 Apr 2022 04:26:43 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 05 Apr 2022 04:26:43 GMT
EXPOSE 8888
# Tue, 05 Apr 2022 04:26:43 GMT
VOLUME [/var/lib/chronograf]
# Tue, 05 Apr 2022 04:26:43 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 05 Apr 2022 04:26:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 04:26:43 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58beb826c7b7288de69f85c4476fd6f04b58ceed760dd1b9e51a7d80aeb0e471`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 271.7 KB (271678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e780df476439b3a8749d6d1ec5009124d7cb47b7328d520390e5c1df5e5260f7`  
		Last Modified: Tue, 05 Apr 2022 04:27:49 GMT  
		Size: 19.2 MB (19203976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770779eb24c794631aa560ebb5145f2fd7a4bf2972a43459d9321581fc47084e`  
		Last Modified: Tue, 05 Apr 2022 04:27:45 GMT  
		Size: 12.3 KB (12267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e1701788eafedc43dca0570322f1ab0c00388a8d9a882173a472e4cc23774b`  
		Last Modified: Tue, 05 Apr 2022 04:27:45 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51eec10863e13223024d57ee99337a425873b97b7b2829d8f207c267a414b201`  
		Last Modified: Tue, 05 Apr 2022 04:27:45 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:02c6e802958cff57cb5233b197646400ee7490827645aad84ea0cdc473b4e012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8.10` - linux; amd64

```console
$ docker pull chronograf@sha256:9ebce37f1cb3f8aa1367256397f33a175c1657673303c26323d67a7f52e87402
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66278958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd274d8f5f45fe5e7d766b561911351d1da0486e97f77b2797c6bdcd41334df`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 May 2022 01:22:19 GMT
ADD file:d7acabc78d998195522bc84475bc7d834e451aba4eb84f813f1eeecc4b3269d7 in / 
# Sat, 28 May 2022 01:22:20 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:54:09 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 28 May 2022 02:54:49 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Sat, 28 May 2022 02:54:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 28 May 2022 02:54:57 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 28 May 2022 02:54:57 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 28 May 2022 02:54:58 GMT
EXPOSE 8888
# Sat, 28 May 2022 02:54:58 GMT
VOLUME [/var/lib/chronograf]
# Sat, 28 May 2022 02:54:58 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 28 May 2022 02:54:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 May 2022 02:54:58 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:73e8e05762864dd5f0a339ca8471e27294d125b63c8adfb278e84c105b8c842d`  
		Last Modified: Sat, 28 May 2022 01:29:04 GMT  
		Size: 22.6 MB (22567519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7662ef14e699ef68d3e9bfd3f48f778f1149a24d5c81007ae49fcb88de333f`  
		Last Modified: Sat, 28 May 2022 02:55:35 GMT  
		Size: 6.8 MB (6760408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1fa322485e82966362f480aa009fcec37b8bfd09c75592bc599f46a271121e`  
		Last Modified: Sat, 28 May 2022 02:56:08 GMT  
		Size: 36.9 MB (36926645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23b636894f961ed3a7165ccea36caf923dd0830c99075981a4f8e2595db9837`  
		Last Modified: Sat, 28 May 2022 02:56:03 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e4dade2c0591441391f8fc707dcff92556641abc005799a5bdd252c99d3a23`  
		Last Modified: Sat, 28 May 2022 02:56:03 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8893c40a09bcf889be2676bd35705c946c2e025e04f81b480207474e38d645`  
		Last Modified: Sat, 28 May 2022 02:56:03 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:9ec0fca2836243cd7e7abd7d91f0465501bf87596c3b6d8482ca3cfcf18e6e7a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59677074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2a75af0bb3fb2c325af4810fa40d8d240a2668c567de0ed6b73782a5321ebb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 May 2022 01:05:51 GMT
ADD file:4dd5baef6913cbeaba8b4abeb9fa3860736e9c421334170bf9a435f002176781 in / 
# Sat, 28 May 2022 01:05:52 GMT
CMD ["bash"]
# Sun, 29 May 2022 10:55:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sun, 29 May 2022 10:57:37 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Sun, 29 May 2022 10:57:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sun, 29 May 2022 10:57:58 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sun, 29 May 2022 10:57:58 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sun, 29 May 2022 10:57:59 GMT
EXPOSE 8888
# Sun, 29 May 2022 10:57:59 GMT
VOLUME [/var/lib/chronograf]
# Sun, 29 May 2022 10:58:00 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sun, 29 May 2022 10:58:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 May 2022 10:58:01 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b1bc9eb7248815be774e7f369470fa41493ff76db8a85f10e545b1538909d9d7`  
		Last Modified: Sat, 28 May 2022 01:22:13 GMT  
		Size: 19.4 MB (19359814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4119ba187328a107b9db1a52f6838ddab5d6c6b8647c5dcff3fa9af4baf486a4`  
		Last Modified: Sun, 29 May 2022 10:59:28 GMT  
		Size: 5.8 MB (5780942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f14c826331b3b2a0e3043566e5772143c4f83fc4390794920fb3f01e3babc2`  
		Last Modified: Sun, 29 May 2022 11:00:38 GMT  
		Size: 34.5 MB (34511923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a134a1318b6432dc1727dfe33e397408cb8d0df0d46154780d048760482aec`  
		Last Modified: Sun, 29 May 2022 11:00:20 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d6ead8c2fb766463e52625a816b0ed0174a76a8be377cebf594520b8fe74edd`  
		Last Modified: Sun, 29 May 2022 11:00:20 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b75dff010c7ee6697b5b21fa5ef81c730ad02e409fe440ae8b064884fc801d`  
		Last Modified: Sun, 29 May 2022 11:00:20 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:23d4ccf233559cd021ba2588260cd2e3d73a1737a8c59ad08afe5ab030c30ebd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60927571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8807af89456190050c24361a794d52896ab5b862c89ec09ad0077bf2d15dea62`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 May 2022 00:43:00 GMT
ADD file:5d3acfb1c09652c954868b7e7fba2e995e5e143bd0f2b1c04a34897232913f7a in / 
# Sat, 28 May 2022 00:43:01 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:06:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 28 May 2022 02:07:16 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Sat, 28 May 2022 02:07:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 28 May 2022 02:07:27 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 28 May 2022 02:07:28 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 28 May 2022 02:07:28 GMT
EXPOSE 8888
# Sat, 28 May 2022 02:07:29 GMT
VOLUME [/var/lib/chronograf]
# Sat, 28 May 2022 02:07:31 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 28 May 2022 02:07:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 May 2022 02:07:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5787d8ce843947b58d50c514418ca92eca29e2110be4fe2993451d835d2d846a`  
		Last Modified: Sat, 28 May 2022 00:51:48 GMT  
		Size: 20.4 MB (20424104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625f22e207e828809833b2c489092f0299c587279c18e2b3a9ae4cd42c4f698f`  
		Last Modified: Sat, 28 May 2022 02:08:23 GMT  
		Size: 6.0 MB (6047429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ffd65e4d9beb391cdd07566713526dcf352fd2ab1401a18efd83bef58f20e6`  
		Last Modified: Sat, 28 May 2022 02:08:57 GMT  
		Size: 34.4 MB (34431642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a4795fa65588801427636ce8627f9d3a1b85741fbdf48ef63d7eca8a5f7f9e9`  
		Last Modified: Sat, 28 May 2022 02:08:52 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd06bed5a8c8a0be0b27d18233727be5bac0b008c8a86c28fd278dadf7811c5`  
		Last Modified: Sat, 28 May 2022 02:08:52 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304f07c65ba0277170bb563d3ddd9a19ee3a0a7f7ba29a4cf0531bfac0a4e882`  
		Last Modified: Sat, 28 May 2022 02:08:52 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:d3e3bbce6ab55cead013b905eba19cdd95cc418e5f2acfb421159ccc1bf8cbd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b28beb85949241c005e5be21181999ce565e4b29dd96295f7e2f7d8ff833a80a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22318581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb7b4f19d3448b5e558e8d6e7857db12751a4b8a0928e3f0fa36efaa296650b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:26:16 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 04:26:37 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 05 Apr 2022 04:26:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 05 Apr 2022 04:26:43 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 05 Apr 2022 04:26:43 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 05 Apr 2022 04:26:43 GMT
EXPOSE 8888
# Tue, 05 Apr 2022 04:26:43 GMT
VOLUME [/var/lib/chronograf]
# Tue, 05 Apr 2022 04:26:43 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 05 Apr 2022 04:26:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 04:26:43 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58beb826c7b7288de69f85c4476fd6f04b58ceed760dd1b9e51a7d80aeb0e471`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 271.7 KB (271678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e780df476439b3a8749d6d1ec5009124d7cb47b7328d520390e5c1df5e5260f7`  
		Last Modified: Tue, 05 Apr 2022 04:27:49 GMT  
		Size: 19.2 MB (19203976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770779eb24c794631aa560ebb5145f2fd7a4bf2972a43459d9321581fc47084e`  
		Last Modified: Tue, 05 Apr 2022 04:27:45 GMT  
		Size: 12.3 KB (12267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e1701788eafedc43dca0570322f1ab0c00388a8d9a882173a472e4cc23774b`  
		Last Modified: Tue, 05 Apr 2022 04:27:45 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51eec10863e13223024d57ee99337a425873b97b7b2829d8f207c267a414b201`  
		Last Modified: Tue, 05 Apr 2022 04:27:45 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:a23d5a50cd032df3089eb3ec783045f2000684466fe32dcc4a425553f0b594e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9` - linux; amd64

```console
$ docker pull chronograf@sha256:e1e28ae9a3a124943a2cbb441eccdf83ae4e8202fe4d466479251685dea253e8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66922759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120de2a27d8f14060d0557cae43f43fcbcbcaad06b52b1f6a583e2a6b66df466`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 May 2022 01:22:19 GMT
ADD file:d7acabc78d998195522bc84475bc7d834e451aba4eb84f813f1eeecc4b3269d7 in / 
# Sat, 28 May 2022 01:22:20 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:54:09 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 28 May 2022 02:55:03 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Sat, 28 May 2022 02:55:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 28 May 2022 02:55:10 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 28 May 2022 02:55:10 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 28 May 2022 02:55:10 GMT
EXPOSE 8888
# Sat, 28 May 2022 02:55:10 GMT
VOLUME [/var/lib/chronograf]
# Sat, 28 May 2022 02:55:10 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 28 May 2022 02:55:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 May 2022 02:55:11 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:73e8e05762864dd5f0a339ca8471e27294d125b63c8adfb278e84c105b8c842d`  
		Last Modified: Sat, 28 May 2022 01:29:04 GMT  
		Size: 22.6 MB (22567519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7662ef14e699ef68d3e9bfd3f48f778f1149a24d5c81007ae49fcb88de333f`  
		Last Modified: Sat, 28 May 2022 02:55:35 GMT  
		Size: 6.8 MB (6760408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982e608e9dddf3de0b0f4310db00ee8b0e0aab7b29a3985d08f2691766225c45`  
		Last Modified: Sat, 28 May 2022 02:56:24 GMT  
		Size: 37.6 MB (37570443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72431261ada86930e6603a517e6ed40abdcf6d808476b85fa04a8024cc85e285`  
		Last Modified: Sat, 28 May 2022 02:56:19 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd99aa97f1a1785745e7babd1e735ef7b4a4029f00cc26469a8421b7bff60a2`  
		Last Modified: Sat, 28 May 2022 02:56:19 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48e17eaea1941f134733a72b9aee9b7e3aa4a4252f2f2ab0d410c83fdc0a52c`  
		Last Modified: Sat, 28 May 2022 02:56:19 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:91792d93db64802b69b8550319078ecd42dd7af182f1fbb9a145f1d20e606743
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60456573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1891d59a62b2ba570f788d9d27aeab62f92c6563eeeb70f6ec610214c0ae07c3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 May 2022 01:05:51 GMT
ADD file:4dd5baef6913cbeaba8b4abeb9fa3860736e9c421334170bf9a435f002176781 in / 
# Sat, 28 May 2022 01:05:52 GMT
CMD ["bash"]
# Sun, 29 May 2022 10:55:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sun, 29 May 2022 10:58:13 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Sun, 29 May 2022 10:58:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sun, 29 May 2022 10:58:33 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sun, 29 May 2022 10:58:33 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sun, 29 May 2022 10:58:34 GMT
EXPOSE 8888
# Sun, 29 May 2022 10:58:34 GMT
VOLUME [/var/lib/chronograf]
# Sun, 29 May 2022 10:58:34 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sun, 29 May 2022 10:58:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 May 2022 10:58:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b1bc9eb7248815be774e7f369470fa41493ff76db8a85f10e545b1538909d9d7`  
		Last Modified: Sat, 28 May 2022 01:22:13 GMT  
		Size: 19.4 MB (19359814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4119ba187328a107b9db1a52f6838ddab5d6c6b8647c5dcff3fa9af4baf486a4`  
		Last Modified: Sun, 29 May 2022 10:59:28 GMT  
		Size: 5.8 MB (5780942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b381ef66ac88214907ef3be818d7b4dcbb3a61bccc080616900e4ed66ea8187`  
		Last Modified: Sun, 29 May 2022 11:01:08 GMT  
		Size: 35.3 MB (35291426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19bae757276901132b7c6f04689b796e75800914327608c507a8a8ea435f9482`  
		Last Modified: Sun, 29 May 2022 11:00:49 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e6e25a9bf1a83179b4080db85af01b6aae433301906a10261e0dd8748fda3e`  
		Last Modified: Sun, 29 May 2022 11:00:49 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b559a4d6864b3e1599e4207a2c01cc2014d7b5e895ee3ca48b77dbf144aedc`  
		Last Modified: Sun, 29 May 2022 11:00:49 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:54a8463f2d4d6f7e7f9a66fed383d5a8cd56ba6a7e26cc2c4da041aae0c38f2e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61669974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da170c79cc572b299e1566df2dadbf48b235dae8bdaacb6e1d3c9109b4757d60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 May 2022 00:43:00 GMT
ADD file:5d3acfb1c09652c954868b7e7fba2e995e5e143bd0f2b1c04a34897232913f7a in / 
# Sat, 28 May 2022 00:43:01 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:06:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 28 May 2022 02:07:39 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Sat, 28 May 2022 02:07:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 28 May 2022 02:07:49 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 28 May 2022 02:07:50 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 28 May 2022 02:07:50 GMT
EXPOSE 8888
# Sat, 28 May 2022 02:07:51 GMT
VOLUME [/var/lib/chronograf]
# Sat, 28 May 2022 02:07:53 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 28 May 2022 02:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 May 2022 02:07:54 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5787d8ce843947b58d50c514418ca92eca29e2110be4fe2993451d835d2d846a`  
		Last Modified: Sat, 28 May 2022 00:51:48 GMT  
		Size: 20.4 MB (20424104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625f22e207e828809833b2c489092f0299c587279c18e2b3a9ae4cd42c4f698f`  
		Last Modified: Sat, 28 May 2022 02:08:23 GMT  
		Size: 6.0 MB (6047429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bea21f6be927dcbadbae629e5fc7be9b1f791bdb07a47f4ed3b79bed64ec485`  
		Last Modified: Sat, 28 May 2022 02:09:13 GMT  
		Size: 35.2 MB (35174052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e400c64508d13d3ef643da9fdcc5ebdc2eb5863de74e96dad4bfbde7d954900`  
		Last Modified: Sat, 28 May 2022 02:09:08 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cafa953d2ec770bb9db45a190416d9127194ac76bf92a7c9266a8863df018bb3`  
		Last Modified: Sat, 28 May 2022 02:09:08 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc5048fe593aa0c34ef28fbde2ef56a945c29d72402d01cfbb11df89654dd0f`  
		Last Modified: Sat, 28 May 2022 02:09:08 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:64529a79e1f42f21063f77e88d3b17a66dd5fe12b361ba459a496564f60deae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:617112048d88886c7c56a0298d5022925bf60cea583bf42950f85da0b1543c30
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22786740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f641fefba39a03a8fb9f9a028aeeecec9f62c81b6a89da22334192b42afee733`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:26:16 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 04:26:47 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 05 Apr 2022 04:26:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 05 Apr 2022 04:26:55 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 05 Apr 2022 04:26:55 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 05 Apr 2022 04:26:55 GMT
EXPOSE 8888
# Tue, 05 Apr 2022 04:26:55 GMT
VOLUME [/var/lib/chronograf]
# Tue, 05 Apr 2022 04:26:55 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 05 Apr 2022 04:26:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 04:26:56 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58beb826c7b7288de69f85c4476fd6f04b58ceed760dd1b9e51a7d80aeb0e471`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 271.7 KB (271678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03048cd652ea5c71fdf0fb436e4b84f533bce10501e6f8f75b34a3f5499ec3bc`  
		Last Modified: Tue, 05 Apr 2022 04:28:03 GMT  
		Size: 19.7 MB (19672143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcafdf6394d7dc10583226357da386688d2d1aa89d90e9d6c3e02d059d1ff7a0`  
		Last Modified: Tue, 05 Apr 2022 04:27:59 GMT  
		Size: 12.3 KB (12263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad9df35e5b1a70215f7fa195a06d17ece074a61ec14d91da8c065c6f5426b8bc`  
		Last Modified: Tue, 05 Apr 2022 04:27:59 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eab2c8d98b5fdc4d6ed0e531c9766afacad54ccd952085aa98da4d57c5519a`  
		Last Modified: Tue, 05 Apr 2022 04:28:00 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:a23d5a50cd032df3089eb3ec783045f2000684466fe32dcc4a425553f0b594e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9.4` - linux; amd64

```console
$ docker pull chronograf@sha256:e1e28ae9a3a124943a2cbb441eccdf83ae4e8202fe4d466479251685dea253e8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66922759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120de2a27d8f14060d0557cae43f43fcbcbcaad06b52b1f6a583e2a6b66df466`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 May 2022 01:22:19 GMT
ADD file:d7acabc78d998195522bc84475bc7d834e451aba4eb84f813f1eeecc4b3269d7 in / 
# Sat, 28 May 2022 01:22:20 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:54:09 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 28 May 2022 02:55:03 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Sat, 28 May 2022 02:55:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 28 May 2022 02:55:10 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 28 May 2022 02:55:10 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 28 May 2022 02:55:10 GMT
EXPOSE 8888
# Sat, 28 May 2022 02:55:10 GMT
VOLUME [/var/lib/chronograf]
# Sat, 28 May 2022 02:55:10 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 28 May 2022 02:55:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 May 2022 02:55:11 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:73e8e05762864dd5f0a339ca8471e27294d125b63c8adfb278e84c105b8c842d`  
		Last Modified: Sat, 28 May 2022 01:29:04 GMT  
		Size: 22.6 MB (22567519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7662ef14e699ef68d3e9bfd3f48f778f1149a24d5c81007ae49fcb88de333f`  
		Last Modified: Sat, 28 May 2022 02:55:35 GMT  
		Size: 6.8 MB (6760408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982e608e9dddf3de0b0f4310db00ee8b0e0aab7b29a3985d08f2691766225c45`  
		Last Modified: Sat, 28 May 2022 02:56:24 GMT  
		Size: 37.6 MB (37570443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72431261ada86930e6603a517e6ed40abdcf6d808476b85fa04a8024cc85e285`  
		Last Modified: Sat, 28 May 2022 02:56:19 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd99aa97f1a1785745e7babd1e735ef7b4a4029f00cc26469a8421b7bff60a2`  
		Last Modified: Sat, 28 May 2022 02:56:19 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48e17eaea1941f134733a72b9aee9b7e3aa4a4252f2f2ab0d410c83fdc0a52c`  
		Last Modified: Sat, 28 May 2022 02:56:19 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:91792d93db64802b69b8550319078ecd42dd7af182f1fbb9a145f1d20e606743
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60456573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1891d59a62b2ba570f788d9d27aeab62f92c6563eeeb70f6ec610214c0ae07c3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 May 2022 01:05:51 GMT
ADD file:4dd5baef6913cbeaba8b4abeb9fa3860736e9c421334170bf9a435f002176781 in / 
# Sat, 28 May 2022 01:05:52 GMT
CMD ["bash"]
# Sun, 29 May 2022 10:55:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sun, 29 May 2022 10:58:13 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Sun, 29 May 2022 10:58:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sun, 29 May 2022 10:58:33 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sun, 29 May 2022 10:58:33 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sun, 29 May 2022 10:58:34 GMT
EXPOSE 8888
# Sun, 29 May 2022 10:58:34 GMT
VOLUME [/var/lib/chronograf]
# Sun, 29 May 2022 10:58:34 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sun, 29 May 2022 10:58:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 May 2022 10:58:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b1bc9eb7248815be774e7f369470fa41493ff76db8a85f10e545b1538909d9d7`  
		Last Modified: Sat, 28 May 2022 01:22:13 GMT  
		Size: 19.4 MB (19359814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4119ba187328a107b9db1a52f6838ddab5d6c6b8647c5dcff3fa9af4baf486a4`  
		Last Modified: Sun, 29 May 2022 10:59:28 GMT  
		Size: 5.8 MB (5780942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b381ef66ac88214907ef3be818d7b4dcbb3a61bccc080616900e4ed66ea8187`  
		Last Modified: Sun, 29 May 2022 11:01:08 GMT  
		Size: 35.3 MB (35291426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19bae757276901132b7c6f04689b796e75800914327608c507a8a8ea435f9482`  
		Last Modified: Sun, 29 May 2022 11:00:49 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e6e25a9bf1a83179b4080db85af01b6aae433301906a10261e0dd8748fda3e`  
		Last Modified: Sun, 29 May 2022 11:00:49 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b559a4d6864b3e1599e4207a2c01cc2014d7b5e895ee3ca48b77dbf144aedc`  
		Last Modified: Sun, 29 May 2022 11:00:49 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:54a8463f2d4d6f7e7f9a66fed383d5a8cd56ba6a7e26cc2c4da041aae0c38f2e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61669974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da170c79cc572b299e1566df2dadbf48b235dae8bdaacb6e1d3c9109b4757d60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 May 2022 00:43:00 GMT
ADD file:5d3acfb1c09652c954868b7e7fba2e995e5e143bd0f2b1c04a34897232913f7a in / 
# Sat, 28 May 2022 00:43:01 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:06:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 28 May 2022 02:07:39 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Sat, 28 May 2022 02:07:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 28 May 2022 02:07:49 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 28 May 2022 02:07:50 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 28 May 2022 02:07:50 GMT
EXPOSE 8888
# Sat, 28 May 2022 02:07:51 GMT
VOLUME [/var/lib/chronograf]
# Sat, 28 May 2022 02:07:53 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 28 May 2022 02:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 May 2022 02:07:54 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5787d8ce843947b58d50c514418ca92eca29e2110be4fe2993451d835d2d846a`  
		Last Modified: Sat, 28 May 2022 00:51:48 GMT  
		Size: 20.4 MB (20424104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625f22e207e828809833b2c489092f0299c587279c18e2b3a9ae4cd42c4f698f`  
		Last Modified: Sat, 28 May 2022 02:08:23 GMT  
		Size: 6.0 MB (6047429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bea21f6be927dcbadbae629e5fc7be9b1f791bdb07a47f4ed3b79bed64ec485`  
		Last Modified: Sat, 28 May 2022 02:09:13 GMT  
		Size: 35.2 MB (35174052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e400c64508d13d3ef643da9fdcc5ebdc2eb5863de74e96dad4bfbde7d954900`  
		Last Modified: Sat, 28 May 2022 02:09:08 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cafa953d2ec770bb9db45a190416d9127194ac76bf92a7c9266a8863df018bb3`  
		Last Modified: Sat, 28 May 2022 02:09:08 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc5048fe593aa0c34ef28fbde2ef56a945c29d72402d01cfbb11df89654dd0f`  
		Last Modified: Sat, 28 May 2022 02:09:08 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:64529a79e1f42f21063f77e88d3b17a66dd5fe12b361ba459a496564f60deae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:617112048d88886c7c56a0298d5022925bf60cea583bf42950f85da0b1543c30
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22786740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f641fefba39a03a8fb9f9a028aeeecec9f62c81b6a89da22334192b42afee733`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:26:16 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 04:26:47 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 05 Apr 2022 04:26:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 05 Apr 2022 04:26:55 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 05 Apr 2022 04:26:55 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 05 Apr 2022 04:26:55 GMT
EXPOSE 8888
# Tue, 05 Apr 2022 04:26:55 GMT
VOLUME [/var/lib/chronograf]
# Tue, 05 Apr 2022 04:26:55 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 05 Apr 2022 04:26:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 04:26:56 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58beb826c7b7288de69f85c4476fd6f04b58ceed760dd1b9e51a7d80aeb0e471`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 271.7 KB (271678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03048cd652ea5c71fdf0fb436e4b84f533bce10501e6f8f75b34a3f5499ec3bc`  
		Last Modified: Tue, 05 Apr 2022 04:28:03 GMT  
		Size: 19.7 MB (19672143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcafdf6394d7dc10583226357da386688d2d1aa89d90e9d6c3e02d059d1ff7a0`  
		Last Modified: Tue, 05 Apr 2022 04:27:59 GMT  
		Size: 12.3 KB (12263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad9df35e5b1a70215f7fa195a06d17ece074a61ec14d91da8c065c6f5426b8bc`  
		Last Modified: Tue, 05 Apr 2022 04:27:59 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eab2c8d98b5fdc4d6ed0e531c9766afacad54ccd952085aa98da4d57c5519a`  
		Last Modified: Tue, 05 Apr 2022 04:28:00 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:64529a79e1f42f21063f77e88d3b17a66dd5fe12b361ba459a496564f60deae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:617112048d88886c7c56a0298d5022925bf60cea583bf42950f85da0b1543c30
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22786740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f641fefba39a03a8fb9f9a028aeeecec9f62c81b6a89da22334192b42afee733`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:26:16 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 04:26:47 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 05 Apr 2022 04:26:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 05 Apr 2022 04:26:55 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 05 Apr 2022 04:26:55 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 05 Apr 2022 04:26:55 GMT
EXPOSE 8888
# Tue, 05 Apr 2022 04:26:55 GMT
VOLUME [/var/lib/chronograf]
# Tue, 05 Apr 2022 04:26:55 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 05 Apr 2022 04:26:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 04:26:56 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58beb826c7b7288de69f85c4476fd6f04b58ceed760dd1b9e51a7d80aeb0e471`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 271.7 KB (271678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03048cd652ea5c71fdf0fb436e4b84f533bce10501e6f8f75b34a3f5499ec3bc`  
		Last Modified: Tue, 05 Apr 2022 04:28:03 GMT  
		Size: 19.7 MB (19672143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcafdf6394d7dc10583226357da386688d2d1aa89d90e9d6c3e02d059d1ff7a0`  
		Last Modified: Tue, 05 Apr 2022 04:27:59 GMT  
		Size: 12.3 KB (12263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad9df35e5b1a70215f7fa195a06d17ece074a61ec14d91da8c065c6f5426b8bc`  
		Last Modified: Tue, 05 Apr 2022 04:27:59 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eab2c8d98b5fdc4d6ed0e531c9766afacad54ccd952085aa98da4d57c5519a`  
		Last Modified: Tue, 05 Apr 2022 04:28:00 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:a23d5a50cd032df3089eb3ec783045f2000684466fe32dcc4a425553f0b594e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:e1e28ae9a3a124943a2cbb441eccdf83ae4e8202fe4d466479251685dea253e8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66922759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120de2a27d8f14060d0557cae43f43fcbcbcaad06b52b1f6a583e2a6b66df466`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 May 2022 01:22:19 GMT
ADD file:d7acabc78d998195522bc84475bc7d834e451aba4eb84f813f1eeecc4b3269d7 in / 
# Sat, 28 May 2022 01:22:20 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:54:09 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 28 May 2022 02:55:03 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Sat, 28 May 2022 02:55:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 28 May 2022 02:55:10 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 28 May 2022 02:55:10 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 28 May 2022 02:55:10 GMT
EXPOSE 8888
# Sat, 28 May 2022 02:55:10 GMT
VOLUME [/var/lib/chronograf]
# Sat, 28 May 2022 02:55:10 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 28 May 2022 02:55:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 May 2022 02:55:11 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:73e8e05762864dd5f0a339ca8471e27294d125b63c8adfb278e84c105b8c842d`  
		Last Modified: Sat, 28 May 2022 01:29:04 GMT  
		Size: 22.6 MB (22567519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7662ef14e699ef68d3e9bfd3f48f778f1149a24d5c81007ae49fcb88de333f`  
		Last Modified: Sat, 28 May 2022 02:55:35 GMT  
		Size: 6.8 MB (6760408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982e608e9dddf3de0b0f4310db00ee8b0e0aab7b29a3985d08f2691766225c45`  
		Last Modified: Sat, 28 May 2022 02:56:24 GMT  
		Size: 37.6 MB (37570443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72431261ada86930e6603a517e6ed40abdcf6d808476b85fa04a8024cc85e285`  
		Last Modified: Sat, 28 May 2022 02:56:19 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd99aa97f1a1785745e7babd1e735ef7b4a4029f00cc26469a8421b7bff60a2`  
		Last Modified: Sat, 28 May 2022 02:56:19 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48e17eaea1941f134733a72b9aee9b7e3aa4a4252f2f2ab0d410c83fdc0a52c`  
		Last Modified: Sat, 28 May 2022 02:56:19 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:91792d93db64802b69b8550319078ecd42dd7af182f1fbb9a145f1d20e606743
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60456573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1891d59a62b2ba570f788d9d27aeab62f92c6563eeeb70f6ec610214c0ae07c3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 May 2022 01:05:51 GMT
ADD file:4dd5baef6913cbeaba8b4abeb9fa3860736e9c421334170bf9a435f002176781 in / 
# Sat, 28 May 2022 01:05:52 GMT
CMD ["bash"]
# Sun, 29 May 2022 10:55:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sun, 29 May 2022 10:58:13 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Sun, 29 May 2022 10:58:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sun, 29 May 2022 10:58:33 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sun, 29 May 2022 10:58:33 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sun, 29 May 2022 10:58:34 GMT
EXPOSE 8888
# Sun, 29 May 2022 10:58:34 GMT
VOLUME [/var/lib/chronograf]
# Sun, 29 May 2022 10:58:34 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sun, 29 May 2022 10:58:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 May 2022 10:58:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b1bc9eb7248815be774e7f369470fa41493ff76db8a85f10e545b1538909d9d7`  
		Last Modified: Sat, 28 May 2022 01:22:13 GMT  
		Size: 19.4 MB (19359814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4119ba187328a107b9db1a52f6838ddab5d6c6b8647c5dcff3fa9af4baf486a4`  
		Last Modified: Sun, 29 May 2022 10:59:28 GMT  
		Size: 5.8 MB (5780942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b381ef66ac88214907ef3be818d7b4dcbb3a61bccc080616900e4ed66ea8187`  
		Last Modified: Sun, 29 May 2022 11:01:08 GMT  
		Size: 35.3 MB (35291426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19bae757276901132b7c6f04689b796e75800914327608c507a8a8ea435f9482`  
		Last Modified: Sun, 29 May 2022 11:00:49 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e6e25a9bf1a83179b4080db85af01b6aae433301906a10261e0dd8748fda3e`  
		Last Modified: Sun, 29 May 2022 11:00:49 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b559a4d6864b3e1599e4207a2c01cc2014d7b5e895ee3ca48b77dbf144aedc`  
		Last Modified: Sun, 29 May 2022 11:00:49 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:54a8463f2d4d6f7e7f9a66fed383d5a8cd56ba6a7e26cc2c4da041aae0c38f2e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61669974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da170c79cc572b299e1566df2dadbf48b235dae8bdaacb6e1d3c9109b4757d60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 May 2022 00:43:00 GMT
ADD file:5d3acfb1c09652c954868b7e7fba2e995e5e143bd0f2b1c04a34897232913f7a in / 
# Sat, 28 May 2022 00:43:01 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:06:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 28 May 2022 02:07:39 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Sat, 28 May 2022 02:07:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 28 May 2022 02:07:49 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 28 May 2022 02:07:50 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 28 May 2022 02:07:50 GMT
EXPOSE 8888
# Sat, 28 May 2022 02:07:51 GMT
VOLUME [/var/lib/chronograf]
# Sat, 28 May 2022 02:07:53 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 28 May 2022 02:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 May 2022 02:07:54 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5787d8ce843947b58d50c514418ca92eca29e2110be4fe2993451d835d2d846a`  
		Last Modified: Sat, 28 May 2022 00:51:48 GMT  
		Size: 20.4 MB (20424104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625f22e207e828809833b2c489092f0299c587279c18e2b3a9ae4cd42c4f698f`  
		Last Modified: Sat, 28 May 2022 02:08:23 GMT  
		Size: 6.0 MB (6047429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bea21f6be927dcbadbae629e5fc7be9b1f791bdb07a47f4ed3b79bed64ec485`  
		Last Modified: Sat, 28 May 2022 02:09:13 GMT  
		Size: 35.2 MB (35174052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e400c64508d13d3ef643da9fdcc5ebdc2eb5863de74e96dad4bfbde7d954900`  
		Last Modified: Sat, 28 May 2022 02:09:08 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cafa953d2ec770bb9db45a190416d9127194ac76bf92a7c9266a8863df018bb3`  
		Last Modified: Sat, 28 May 2022 02:09:08 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc5048fe593aa0c34ef28fbde2ef56a945c29d72402d01cfbb11df89654dd0f`  
		Last Modified: Sat, 28 May 2022 02:09:08 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
