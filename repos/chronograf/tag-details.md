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
-	[`chronograf:1.8.2`](#chronograf182)
-	[`chronograf:1.8.2-alpine`](#chronograf182-alpine)
-	[`chronograf:1.8-alpine`](#chronograf18-alpine)
-	[`chronograf:alpine`](#chronografalpine)
-	[`chronograf:latest`](#chronograflatest)

## `chronograf:1.6`

```console
$ docker pull chronograf@sha256:e15afe39289b1862bfe3cefbd879495dfddd1c9d6eed74a70b33a8bc4b259d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6` - linux; amd64

```console
$ docker pull chronograf@sha256:0da81589e0d24c2ad7e90149dd5a3b11db05f8137866ac09e80889a99700d17e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49141259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b02f81123e8fb9d9ddf8636babda58406da85ea91fbc39e17b673b53da4f2d0a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:54:36 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 16 Apr 2020 03:54:36 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Thu, 16 Apr 2020 03:54:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 16 Apr 2020 03:54:53 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 16 Apr 2020 03:54:53 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 16 Apr 2020 03:54:53 GMT
EXPOSE 8888
# Thu, 16 Apr 2020 03:54:54 GMT
VOLUME [/var/lib/chronograf]
# Thu, 16 Apr 2020 03:54:54 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 16 Apr 2020 03:54:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 03:54:55 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44df9a0f20c0a9a55f33ce1ff19dbad64f53385c2d80e54cbae2095a8d4af02`  
		Last Modified: Thu, 16 Apr 2020 03:56:19 GMT  
		Size: 4.5 MB (4503605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3a2474f0953ba3ec58dce910b469f3a1bea0d9d68f7f7b78930230d0aae01d`  
		Last Modified: Thu, 16 Apr 2020 03:56:25 GMT  
		Size: 22.1 MB (22099787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682fa7aa59a50b2fa50fe6a0e01da39dc4255449247ff202bb965eeecf05730b`  
		Last Modified: Thu, 16 Apr 2020 03:56:18 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0a14ede9a47f6e72af94778cb3f644b3a561b61315dd133cd1da01cc76a645`  
		Last Modified: Thu, 16 Apr 2020 03:56:18 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c11f56174887755ed67dbcd7c7814d8a8d6e2074debe4e681f2644947493f9`  
		Last Modified: Thu, 16 Apr 2020 03:56:18 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:7b1276d5ddd7bb18bc11b82e4d23c1cbc8ad7fb76ec52c3c79eb9239b86a84de
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43725682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2e96c81cdb92cd346f42b5245c2e1ce22a485f2861b785f706a27f16692ceb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2020 01:05:08 GMT
ADD file:e37c4728c0c89ac126542ac35e7e493425c021bfac751079c9b266821a1b4e99 in / 
# Thu, 16 Apr 2020 01:05:10 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 02:02:01 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 16 Apr 2020 02:02:02 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Thu, 16 Apr 2020 02:02:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 16 Apr 2020 02:02:28 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 16 Apr 2020 02:02:29 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 16 Apr 2020 02:02:30 GMT
EXPOSE 8888
# Thu, 16 Apr 2020 02:02:33 GMT
VOLUME [/var/lib/chronograf]
# Thu, 16 Apr 2020 02:02:34 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 16 Apr 2020 02:02:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 02:02:36 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f78d9963dfddc4747d6200353b50f6093a6e37ca82e1612fa397d64ff13e7299`  
		Last Modified: Thu, 16 Apr 2020 01:12:33 GMT  
		Size: 19.3 MB (19298546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a83ba0d6e415d0bb68db80a86f4023e0cac619036ce507dc505523c397d3975`  
		Last Modified: Thu, 16 Apr 2020 02:04:40 GMT  
		Size: 3.9 MB (3877396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3cdcf6536f90f16ba32b62c4917dd9a8b69ccc26d55be75f24d67039c5d03e`  
		Last Modified: Thu, 16 Apr 2020 02:04:47 GMT  
		Size: 20.5 MB (20525355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09969b42d9a54b541a8214b0753f801459995f71ba4169c175c245497921ed3e`  
		Last Modified: Thu, 16 Apr 2020 02:04:40 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c768c7512790ed58ea85de2fe05bab3c4a95f9a075d2eb3b17c07e81a280c06`  
		Last Modified: Thu, 16 Apr 2020 02:04:40 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492dad9d10bf3280e74f8c32f0dd57f79d3563eb70d2cb94b626dc343fb99838`  
		Last Modified: Thu, 16 Apr 2020 02:04:40 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:52bb5bcffc8daa9d2beba4195ba044a23ee61c91f0654341f7ce13737d5ac1b5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45208794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db92ceed319c50ba40ef6d1e52d471df4dbdd670f7a5633e0ca10429b1a4c565`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2020 02:45:19 GMT
ADD file:1588320d1c43714ec0353b7471f2ffd649045ca0f5f70dcb1eb064875fff9578 in / 
# Thu, 16 Apr 2020 02:45:21 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:33:04 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 16 Apr 2020 03:33:05 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Thu, 16 Apr 2020 03:33:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 16 Apr 2020 03:33:31 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 16 Apr 2020 03:33:32 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 16 Apr 2020 03:33:33 GMT
EXPOSE 8888
# Thu, 16 Apr 2020 03:33:34 GMT
VOLUME [/var/lib/chronograf]
# Thu, 16 Apr 2020 03:33:35 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 16 Apr 2020 03:33:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 03:33:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8978c87ff45d64d1663a585dcf1ed66d9e711c2e4048d83ef561da9514ef46e6`  
		Last Modified: Thu, 16 Apr 2020 02:51:32 GMT  
		Size: 20.4 MB (20370106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1f12b855cc63fdfabc47f79ca6cc4e5130d9eff6495b3185a5da6eeb8d2863`  
		Last Modified: Thu, 16 Apr 2020 03:35:11 GMT  
		Size: 4.1 MB (4080756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a51ddc37665b2883a1ccb94c1dfbfbd4e5d11e4874e70de68a10060df32961`  
		Last Modified: Thu, 16 Apr 2020 03:35:16 GMT  
		Size: 20.7 MB (20733535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280770854d52eb573393f06b27cffe9aa79930362d395fb678c35597fc4b4287`  
		Last Modified: Thu, 16 Apr 2020 03:35:10 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5e582e034542fafbe8c250912c4c5c8ab4aa7bfa648a50ace4362ed58165a9`  
		Last Modified: Thu, 16 Apr 2020 03:35:10 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b1b6cb6e179036de3f63eb18a28a337b0790ab957d3cb01196dff7c2441839a`  
		Last Modified: Thu, 16 Apr 2020 03:35:10 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6.2`

```console
$ docker pull chronograf@sha256:e15afe39289b1862bfe3cefbd879495dfddd1c9d6eed74a70b33a8bc4b259d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6.2` - linux; amd64

```console
$ docker pull chronograf@sha256:0da81589e0d24c2ad7e90149dd5a3b11db05f8137866ac09e80889a99700d17e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49141259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b02f81123e8fb9d9ddf8636babda58406da85ea91fbc39e17b673b53da4f2d0a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:54:36 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 16 Apr 2020 03:54:36 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Thu, 16 Apr 2020 03:54:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 16 Apr 2020 03:54:53 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 16 Apr 2020 03:54:53 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 16 Apr 2020 03:54:53 GMT
EXPOSE 8888
# Thu, 16 Apr 2020 03:54:54 GMT
VOLUME [/var/lib/chronograf]
# Thu, 16 Apr 2020 03:54:54 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 16 Apr 2020 03:54:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 03:54:55 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44df9a0f20c0a9a55f33ce1ff19dbad64f53385c2d80e54cbae2095a8d4af02`  
		Last Modified: Thu, 16 Apr 2020 03:56:19 GMT  
		Size: 4.5 MB (4503605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3a2474f0953ba3ec58dce910b469f3a1bea0d9d68f7f7b78930230d0aae01d`  
		Last Modified: Thu, 16 Apr 2020 03:56:25 GMT  
		Size: 22.1 MB (22099787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682fa7aa59a50b2fa50fe6a0e01da39dc4255449247ff202bb965eeecf05730b`  
		Last Modified: Thu, 16 Apr 2020 03:56:18 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0a14ede9a47f6e72af94778cb3f644b3a561b61315dd133cd1da01cc76a645`  
		Last Modified: Thu, 16 Apr 2020 03:56:18 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c11f56174887755ed67dbcd7c7814d8a8d6e2074debe4e681f2644947493f9`  
		Last Modified: Thu, 16 Apr 2020 03:56:18 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:7b1276d5ddd7bb18bc11b82e4d23c1cbc8ad7fb76ec52c3c79eb9239b86a84de
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43725682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2e96c81cdb92cd346f42b5245c2e1ce22a485f2861b785f706a27f16692ceb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2020 01:05:08 GMT
ADD file:e37c4728c0c89ac126542ac35e7e493425c021bfac751079c9b266821a1b4e99 in / 
# Thu, 16 Apr 2020 01:05:10 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 02:02:01 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 16 Apr 2020 02:02:02 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Thu, 16 Apr 2020 02:02:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 16 Apr 2020 02:02:28 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 16 Apr 2020 02:02:29 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 16 Apr 2020 02:02:30 GMT
EXPOSE 8888
# Thu, 16 Apr 2020 02:02:33 GMT
VOLUME [/var/lib/chronograf]
# Thu, 16 Apr 2020 02:02:34 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 16 Apr 2020 02:02:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 02:02:36 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f78d9963dfddc4747d6200353b50f6093a6e37ca82e1612fa397d64ff13e7299`  
		Last Modified: Thu, 16 Apr 2020 01:12:33 GMT  
		Size: 19.3 MB (19298546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a83ba0d6e415d0bb68db80a86f4023e0cac619036ce507dc505523c397d3975`  
		Last Modified: Thu, 16 Apr 2020 02:04:40 GMT  
		Size: 3.9 MB (3877396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3cdcf6536f90f16ba32b62c4917dd9a8b69ccc26d55be75f24d67039c5d03e`  
		Last Modified: Thu, 16 Apr 2020 02:04:47 GMT  
		Size: 20.5 MB (20525355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09969b42d9a54b541a8214b0753f801459995f71ba4169c175c245497921ed3e`  
		Last Modified: Thu, 16 Apr 2020 02:04:40 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c768c7512790ed58ea85de2fe05bab3c4a95f9a075d2eb3b17c07e81a280c06`  
		Last Modified: Thu, 16 Apr 2020 02:04:40 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492dad9d10bf3280e74f8c32f0dd57f79d3563eb70d2cb94b626dc343fb99838`  
		Last Modified: Thu, 16 Apr 2020 02:04:40 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:52bb5bcffc8daa9d2beba4195ba044a23ee61c91f0654341f7ce13737d5ac1b5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45208794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db92ceed319c50ba40ef6d1e52d471df4dbdd670f7a5633e0ca10429b1a4c565`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2020 02:45:19 GMT
ADD file:1588320d1c43714ec0353b7471f2ffd649045ca0f5f70dcb1eb064875fff9578 in / 
# Thu, 16 Apr 2020 02:45:21 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:33:04 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 16 Apr 2020 03:33:05 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Thu, 16 Apr 2020 03:33:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 16 Apr 2020 03:33:31 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 16 Apr 2020 03:33:32 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 16 Apr 2020 03:33:33 GMT
EXPOSE 8888
# Thu, 16 Apr 2020 03:33:34 GMT
VOLUME [/var/lib/chronograf]
# Thu, 16 Apr 2020 03:33:35 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 16 Apr 2020 03:33:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 03:33:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8978c87ff45d64d1663a585dcf1ed66d9e711c2e4048d83ef561da9514ef46e6`  
		Last Modified: Thu, 16 Apr 2020 02:51:32 GMT  
		Size: 20.4 MB (20370106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1f12b855cc63fdfabc47f79ca6cc4e5130d9eff6495b3185a5da6eeb8d2863`  
		Last Modified: Thu, 16 Apr 2020 03:35:11 GMT  
		Size: 4.1 MB (4080756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a51ddc37665b2883a1ccb94c1dfbfbd4e5d11e4874e70de68a10060df32961`  
		Last Modified: Thu, 16 Apr 2020 03:35:16 GMT  
		Size: 20.7 MB (20733535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280770854d52eb573393f06b27cffe9aa79930362d395fb678c35597fc4b4287`  
		Last Modified: Thu, 16 Apr 2020 03:35:10 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5e582e034542fafbe8c250912c4c5c8ab4aa7bfa648a50ace4362ed58165a9`  
		Last Modified: Thu, 16 Apr 2020 03:35:10 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b1b6cb6e179036de3f63eb18a28a337b0790ab957d3cb01196dff7c2441839a`  
		Last Modified: Thu, 16 Apr 2020 03:35:10 GMT  
		Size: 239.0 B  
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
$ docker pull chronograf@sha256:7d1ff3ddd5254de32f0c4a685b10da24002220f2bec3cfe6973e062f2cc84c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7` - linux; amd64

```console
$ docker pull chronograf@sha256:82bff3a34679c4120e5bfbc3d9873eb18d5e0281a16ed90f52cf2474d4608eb4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65386213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ea5b84e59362cb5ae9d6c94925c68b4745cadf231b13b226e60e50d0672d40`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:54:36 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 16 Apr 2020 03:55:03 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Thu, 16 Apr 2020 03:55:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 16 Apr 2020 03:55:21 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 16 Apr 2020 03:55:21 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 16 Apr 2020 03:55:21 GMT
EXPOSE 8888
# Thu, 16 Apr 2020 03:55:22 GMT
VOLUME [/var/lib/chronograf]
# Thu, 16 Apr 2020 03:55:22 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 16 Apr 2020 03:55:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 03:55:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44df9a0f20c0a9a55f33ce1ff19dbad64f53385c2d80e54cbae2095a8d4af02`  
		Last Modified: Thu, 16 Apr 2020 03:56:19 GMT  
		Size: 4.5 MB (4503605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44199f4cac77d05f3b40c5537dd0ac57f1d06e47ddea50024f6adf49b45b5a7`  
		Last Modified: Thu, 16 Apr 2020 03:56:39 GMT  
		Size: 38.3 MB (38344737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16315fc575aa156e16f31e9b12afa9b681d7d6d4ab02eed38aeb68655e5944e8`  
		Last Modified: Thu, 16 Apr 2020 03:56:30 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4cd6ed49d4687466c25125621e37b4c4163885536d2deec52a3b28bb6a62f97`  
		Last Modified: Thu, 16 Apr 2020 03:56:29 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5214b5f60aed4f931592db113c134e53db070ec87ccd6c44335460a8cf27ef`  
		Last Modified: Thu, 16 Apr 2020 03:56:29 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:c6d32d8c1fd5a9b085fcdcd43cc7b295936464fabae3e40b87b04d0eaa6b6238
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59003058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:721881fdbf593222ad2d1f69af7c427597132e30c5757402adf975e0c6983359`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2020 01:05:08 GMT
ADD file:e37c4728c0c89ac126542ac35e7e493425c021bfac751079c9b266821a1b4e99 in / 
# Thu, 16 Apr 2020 01:05:10 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 02:02:01 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 16 Apr 2020 02:02:54 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Thu, 16 Apr 2020 02:03:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 16 Apr 2020 02:03:26 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 16 Apr 2020 02:03:27 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 16 Apr 2020 02:03:28 GMT
EXPOSE 8888
# Thu, 16 Apr 2020 02:03:29 GMT
VOLUME [/var/lib/chronograf]
# Thu, 16 Apr 2020 02:03:30 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 16 Apr 2020 02:03:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 02:03:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f78d9963dfddc4747d6200353b50f6093a6e37ca82e1612fa397d64ff13e7299`  
		Last Modified: Thu, 16 Apr 2020 01:12:33 GMT  
		Size: 19.3 MB (19298546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a83ba0d6e415d0bb68db80a86f4023e0cac619036ce507dc505523c397d3975`  
		Last Modified: Thu, 16 Apr 2020 02:04:40 GMT  
		Size: 3.9 MB (3877396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5506d500f5aebcb5d1c8628305b1d4d6526a072813995c56b6fe10d4073a6e7d`  
		Last Modified: Thu, 16 Apr 2020 02:05:09 GMT  
		Size: 35.8 MB (35802723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914f8f57aa99afa7b946c065e71e2dad956f8e91cff10d0730d6bc1c9da663f7`  
		Last Modified: Thu, 16 Apr 2020 02:04:53 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a67d15af846b6df7e0c5abf433d571da53a63f12ff7a7b5975f9fc27dfae89e`  
		Last Modified: Thu, 16 Apr 2020 02:04:53 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3387407602baba71c2d2af369c844ed475b861091df8274a10282e550938f8b4`  
		Last Modified: Thu, 16 Apr 2020 02:04:53 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:df71381fd44afa99430afc26ec41db06b795afc63e853d962490aca7f73af1d9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60481064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2fd62fb75e7099efae09d61451284c4dae0be4b385fb99fa96347b8b52d08c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2020 02:45:19 GMT
ADD file:1588320d1c43714ec0353b7471f2ffd649045ca0f5f70dcb1eb064875fff9578 in / 
# Thu, 16 Apr 2020 02:45:21 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:33:04 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 16 Apr 2020 03:33:50 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Thu, 16 Apr 2020 03:34:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 16 Apr 2020 03:34:13 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 16 Apr 2020 03:34:14 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 16 Apr 2020 03:34:14 GMT
EXPOSE 8888
# Thu, 16 Apr 2020 03:34:15 GMT
VOLUME [/var/lib/chronograf]
# Thu, 16 Apr 2020 03:34:16 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 16 Apr 2020 03:34:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 03:34:18 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8978c87ff45d64d1663a585dcf1ed66d9e711c2e4048d83ef561da9514ef46e6`  
		Last Modified: Thu, 16 Apr 2020 02:51:32 GMT  
		Size: 20.4 MB (20370106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1f12b855cc63fdfabc47f79ca6cc4e5130d9eff6495b3185a5da6eeb8d2863`  
		Last Modified: Thu, 16 Apr 2020 03:35:11 GMT  
		Size: 4.1 MB (4080756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e7632f196b2490c6e153cfe44947774490d8a1e174ffd226a05dc6eee2f278e`  
		Last Modified: Thu, 16 Apr 2020 03:35:50 GMT  
		Size: 36.0 MB (36005818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ab8e2455db3a8941a270fb87bd2961d9924b55d7346e6e6a3c1a69c6a4dab6`  
		Last Modified: Thu, 16 Apr 2020 03:35:22 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1262d15f500c04fecc929ac9f4ec198aae2dc27d78318bd558cb9a8923660d9`  
		Last Modified: Thu, 16 Apr 2020 03:35:22 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea7971742fa16ea6b07e709b41d07cd4f929568d05e42d25ebe5cadfb7fb5a2`  
		Last Modified: Thu, 16 Apr 2020 03:35:22 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:7d1ff3ddd5254de32f0c4a685b10da24002220f2bec3cfe6973e062f2cc84c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7.17` - linux; amd64

```console
$ docker pull chronograf@sha256:82bff3a34679c4120e5bfbc3d9873eb18d5e0281a16ed90f52cf2474d4608eb4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65386213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ea5b84e59362cb5ae9d6c94925c68b4745cadf231b13b226e60e50d0672d40`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:54:36 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 16 Apr 2020 03:55:03 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Thu, 16 Apr 2020 03:55:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 16 Apr 2020 03:55:21 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 16 Apr 2020 03:55:21 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 16 Apr 2020 03:55:21 GMT
EXPOSE 8888
# Thu, 16 Apr 2020 03:55:22 GMT
VOLUME [/var/lib/chronograf]
# Thu, 16 Apr 2020 03:55:22 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 16 Apr 2020 03:55:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 03:55:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44df9a0f20c0a9a55f33ce1ff19dbad64f53385c2d80e54cbae2095a8d4af02`  
		Last Modified: Thu, 16 Apr 2020 03:56:19 GMT  
		Size: 4.5 MB (4503605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44199f4cac77d05f3b40c5537dd0ac57f1d06e47ddea50024f6adf49b45b5a7`  
		Last Modified: Thu, 16 Apr 2020 03:56:39 GMT  
		Size: 38.3 MB (38344737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16315fc575aa156e16f31e9b12afa9b681d7d6d4ab02eed38aeb68655e5944e8`  
		Last Modified: Thu, 16 Apr 2020 03:56:30 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4cd6ed49d4687466c25125621e37b4c4163885536d2deec52a3b28bb6a62f97`  
		Last Modified: Thu, 16 Apr 2020 03:56:29 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5214b5f60aed4f931592db113c134e53db070ec87ccd6c44335460a8cf27ef`  
		Last Modified: Thu, 16 Apr 2020 03:56:29 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:c6d32d8c1fd5a9b085fcdcd43cc7b295936464fabae3e40b87b04d0eaa6b6238
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59003058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:721881fdbf593222ad2d1f69af7c427597132e30c5757402adf975e0c6983359`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2020 01:05:08 GMT
ADD file:e37c4728c0c89ac126542ac35e7e493425c021bfac751079c9b266821a1b4e99 in / 
# Thu, 16 Apr 2020 01:05:10 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 02:02:01 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 16 Apr 2020 02:02:54 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Thu, 16 Apr 2020 02:03:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 16 Apr 2020 02:03:26 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 16 Apr 2020 02:03:27 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 16 Apr 2020 02:03:28 GMT
EXPOSE 8888
# Thu, 16 Apr 2020 02:03:29 GMT
VOLUME [/var/lib/chronograf]
# Thu, 16 Apr 2020 02:03:30 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 16 Apr 2020 02:03:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 02:03:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f78d9963dfddc4747d6200353b50f6093a6e37ca82e1612fa397d64ff13e7299`  
		Last Modified: Thu, 16 Apr 2020 01:12:33 GMT  
		Size: 19.3 MB (19298546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a83ba0d6e415d0bb68db80a86f4023e0cac619036ce507dc505523c397d3975`  
		Last Modified: Thu, 16 Apr 2020 02:04:40 GMT  
		Size: 3.9 MB (3877396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5506d500f5aebcb5d1c8628305b1d4d6526a072813995c56b6fe10d4073a6e7d`  
		Last Modified: Thu, 16 Apr 2020 02:05:09 GMT  
		Size: 35.8 MB (35802723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914f8f57aa99afa7b946c065e71e2dad956f8e91cff10d0730d6bc1c9da663f7`  
		Last Modified: Thu, 16 Apr 2020 02:04:53 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a67d15af846b6df7e0c5abf433d571da53a63f12ff7a7b5975f9fc27dfae89e`  
		Last Modified: Thu, 16 Apr 2020 02:04:53 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3387407602baba71c2d2af369c844ed475b861091df8274a10282e550938f8b4`  
		Last Modified: Thu, 16 Apr 2020 02:04:53 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:df71381fd44afa99430afc26ec41db06b795afc63e853d962490aca7f73af1d9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60481064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2fd62fb75e7099efae09d61451284c4dae0be4b385fb99fa96347b8b52d08c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2020 02:45:19 GMT
ADD file:1588320d1c43714ec0353b7471f2ffd649045ca0f5f70dcb1eb064875fff9578 in / 
# Thu, 16 Apr 2020 02:45:21 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:33:04 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 16 Apr 2020 03:33:50 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Thu, 16 Apr 2020 03:34:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 16 Apr 2020 03:34:13 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 16 Apr 2020 03:34:14 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 16 Apr 2020 03:34:14 GMT
EXPOSE 8888
# Thu, 16 Apr 2020 03:34:15 GMT
VOLUME [/var/lib/chronograf]
# Thu, 16 Apr 2020 03:34:16 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 16 Apr 2020 03:34:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 03:34:18 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8978c87ff45d64d1663a585dcf1ed66d9e711c2e4048d83ef561da9514ef46e6`  
		Last Modified: Thu, 16 Apr 2020 02:51:32 GMT  
		Size: 20.4 MB (20370106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1f12b855cc63fdfabc47f79ca6cc4e5130d9eff6495b3185a5da6eeb8d2863`  
		Last Modified: Thu, 16 Apr 2020 03:35:11 GMT  
		Size: 4.1 MB (4080756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e7632f196b2490c6e153cfe44947774490d8a1e174ffd226a05dc6eee2f278e`  
		Last Modified: Thu, 16 Apr 2020 03:35:50 GMT  
		Size: 36.0 MB (36005818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ab8e2455db3a8941a270fb87bd2961d9924b55d7346e6e6a3c1a69c6a4dab6`  
		Last Modified: Thu, 16 Apr 2020 03:35:22 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1262d15f500c04fecc929ac9f4ec198aae2dc27d78318bd558cb9a8923660d9`  
		Last Modified: Thu, 16 Apr 2020 03:35:22 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea7971742fa16ea6b07e709b41d07cd4f929568d05e42d25ebe5cadfb7fb5a2`  
		Last Modified: Thu, 16 Apr 2020 03:35:22 GMT  
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
$ docker pull chronograf@sha256:cd06ab5b1d080d96b57c72bc9c37ce5b2fe036d52a828715e1e974cda2632c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8` - linux; amd64

```console
$ docker pull chronograf@sha256:a55c530d42cf36b1dd0d50589ede16fbf29807086b37e142b975e6c7726194e9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70123096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d3a298922095f82df717cb6635dfb956024853a8d779aed1a447d3162cf71c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:54:36 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 16 Apr 2020 03:55:33 GMT
ENV CHRONOGRAF_VERSION=1.8.2
# Thu, 16 Apr 2020 03:55:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 16 Apr 2020 03:55:51 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 16 Apr 2020 03:55:52 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 16 Apr 2020 03:55:52 GMT
EXPOSE 8888
# Thu, 16 Apr 2020 03:55:52 GMT
VOLUME [/var/lib/chronograf]
# Thu, 16 Apr 2020 03:55:53 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 16 Apr 2020 03:55:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 03:55:53 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44df9a0f20c0a9a55f33ce1ff19dbad64f53385c2d80e54cbae2095a8d4af02`  
		Last Modified: Thu, 16 Apr 2020 03:56:19 GMT  
		Size: 4.5 MB (4503605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03cb6cfbfe859b874306ae4930e04fb6f5126ef1c4868052cba5c87327c09af3`  
		Last Modified: Thu, 16 Apr 2020 03:56:53 GMT  
		Size: 43.1 MB (43081617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a4e39f707718b7d325f477dd5494de3859a4072d2cdc91859e59ff5f4eea12`  
		Last Modified: Thu, 16 Apr 2020 03:56:44 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69373310b905cc9fb8ff25b98daf958e0e14f75a71219ce82e8009308aace4ab`  
		Last Modified: Thu, 16 Apr 2020 03:56:43 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a8615afcc3335cdd446a318c5841f5d914bce72c7c6281cbe5fbb4829ea988`  
		Last Modified: Thu, 16 Apr 2020 03:56:44 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:6df64c9439758317fe998804398dc356c2072c2dc86aa1023a3f52657a787b68
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63543382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25bf9303adab528b50bd50799dc6ec73cdbd6cbe22d3ba8362e7f6191e86afb2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2020 01:05:08 GMT
ADD file:e37c4728c0c89ac126542ac35e7e493425c021bfac751079c9b266821a1b4e99 in / 
# Thu, 16 Apr 2020 01:05:10 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 02:02:01 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 16 Apr 2020 02:03:44 GMT
ENV CHRONOGRAF_VERSION=1.8.2
# Thu, 16 Apr 2020 02:04:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 16 Apr 2020 02:04:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 16 Apr 2020 02:04:17 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 16 Apr 2020 02:04:18 GMT
EXPOSE 8888
# Thu, 16 Apr 2020 02:04:19 GMT
VOLUME [/var/lib/chronograf]
# Thu, 16 Apr 2020 02:04:19 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 16 Apr 2020 02:04:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 02:04:22 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f78d9963dfddc4747d6200353b50f6093a6e37ca82e1612fa397d64ff13e7299`  
		Last Modified: Thu, 16 Apr 2020 01:12:33 GMT  
		Size: 19.3 MB (19298546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a83ba0d6e415d0bb68db80a86f4023e0cac619036ce507dc505523c397d3975`  
		Last Modified: Thu, 16 Apr 2020 02:04:40 GMT  
		Size: 3.9 MB (3877396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf4dc95e0852c9fced212c2f67659e706079ce008dfec7f6a95614019e94459`  
		Last Modified: Thu, 16 Apr 2020 02:05:26 GMT  
		Size: 40.3 MB (40343047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a750a7ae1be2d6095c6cacd1cbc4584782e12b59fc22b15048ffaa35d300a8`  
		Last Modified: Thu, 16 Apr 2020 02:05:16 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d563107fbf7fcbd2f215c764f8cc34d825ac3f0070b05df4df8900bfdb2a65ef`  
		Last Modified: Thu, 16 Apr 2020 02:05:16 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f7e5d70a08545c0c838e6628e25b91809844076c3b261a6854b793e8ca0fe58`  
		Last Modified: Thu, 16 Apr 2020 02:05:16 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:e585988f56e50a55821ac2e2b18988ca7e4adcf4b12388ebf47f15fe254d10fa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64663687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc21688dc157e88e6173411b2f6f6eb3dd837b831f084e537785b371995cab7d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2020 02:45:19 GMT
ADD file:1588320d1c43714ec0353b7471f2ffd649045ca0f5f70dcb1eb064875fff9578 in / 
# Thu, 16 Apr 2020 02:45:21 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:33:04 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 16 Apr 2020 03:34:26 GMT
ENV CHRONOGRAF_VERSION=1.8.2
# Thu, 16 Apr 2020 03:34:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 16 Apr 2020 03:34:49 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 16 Apr 2020 03:34:49 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 16 Apr 2020 03:34:50 GMT
EXPOSE 8888
# Thu, 16 Apr 2020 03:34:51 GMT
VOLUME [/var/lib/chronograf]
# Thu, 16 Apr 2020 03:34:51 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 16 Apr 2020 03:34:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 03:34:52 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8978c87ff45d64d1663a585dcf1ed66d9e711c2e4048d83ef561da9514ef46e6`  
		Last Modified: Thu, 16 Apr 2020 02:51:32 GMT  
		Size: 20.4 MB (20370106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1f12b855cc63fdfabc47f79ca6cc4e5130d9eff6495b3185a5da6eeb8d2863`  
		Last Modified: Thu, 16 Apr 2020 03:35:11 GMT  
		Size: 4.1 MB (4080756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d698eafefe800059a5deaa8403e80d80b847cac90468018ad793778a858f42d`  
		Last Modified: Thu, 16 Apr 2020 03:36:07 GMT  
		Size: 40.2 MB (40188435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76a8c8ed7b841a7efdb7d0e8ed3d48ebdf9f7ba5eafc06d34407124ca35bd19`  
		Last Modified: Thu, 16 Apr 2020 03:35:57 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a69d0fa2a0dd3ae32b0207b4837f96fb5b46c3058b728083631ddaf70d064be`  
		Last Modified: Thu, 16 Apr 2020 03:35:57 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882b9145451c434a1cf0cb271de8bba0dae489fd001410f1c9b7a85690b00cb8`  
		Last Modified: Thu, 16 Apr 2020 03:35:56 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.2`

```console
$ docker pull chronograf@sha256:cd06ab5b1d080d96b57c72bc9c37ce5b2fe036d52a828715e1e974cda2632c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8.2` - linux; amd64

```console
$ docker pull chronograf@sha256:a55c530d42cf36b1dd0d50589ede16fbf29807086b37e142b975e6c7726194e9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70123096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d3a298922095f82df717cb6635dfb956024853a8d779aed1a447d3162cf71c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:54:36 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 16 Apr 2020 03:55:33 GMT
ENV CHRONOGRAF_VERSION=1.8.2
# Thu, 16 Apr 2020 03:55:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 16 Apr 2020 03:55:51 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 16 Apr 2020 03:55:52 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 16 Apr 2020 03:55:52 GMT
EXPOSE 8888
# Thu, 16 Apr 2020 03:55:52 GMT
VOLUME [/var/lib/chronograf]
# Thu, 16 Apr 2020 03:55:53 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 16 Apr 2020 03:55:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 03:55:53 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44df9a0f20c0a9a55f33ce1ff19dbad64f53385c2d80e54cbae2095a8d4af02`  
		Last Modified: Thu, 16 Apr 2020 03:56:19 GMT  
		Size: 4.5 MB (4503605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03cb6cfbfe859b874306ae4930e04fb6f5126ef1c4868052cba5c87327c09af3`  
		Last Modified: Thu, 16 Apr 2020 03:56:53 GMT  
		Size: 43.1 MB (43081617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a4e39f707718b7d325f477dd5494de3859a4072d2cdc91859e59ff5f4eea12`  
		Last Modified: Thu, 16 Apr 2020 03:56:44 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69373310b905cc9fb8ff25b98daf958e0e14f75a71219ce82e8009308aace4ab`  
		Last Modified: Thu, 16 Apr 2020 03:56:43 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a8615afcc3335cdd446a318c5841f5d914bce72c7c6281cbe5fbb4829ea988`  
		Last Modified: Thu, 16 Apr 2020 03:56:44 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.2` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:6df64c9439758317fe998804398dc356c2072c2dc86aa1023a3f52657a787b68
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63543382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25bf9303adab528b50bd50799dc6ec73cdbd6cbe22d3ba8362e7f6191e86afb2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2020 01:05:08 GMT
ADD file:e37c4728c0c89ac126542ac35e7e493425c021bfac751079c9b266821a1b4e99 in / 
# Thu, 16 Apr 2020 01:05:10 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 02:02:01 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 16 Apr 2020 02:03:44 GMT
ENV CHRONOGRAF_VERSION=1.8.2
# Thu, 16 Apr 2020 02:04:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 16 Apr 2020 02:04:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 16 Apr 2020 02:04:17 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 16 Apr 2020 02:04:18 GMT
EXPOSE 8888
# Thu, 16 Apr 2020 02:04:19 GMT
VOLUME [/var/lib/chronograf]
# Thu, 16 Apr 2020 02:04:19 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 16 Apr 2020 02:04:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 02:04:22 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f78d9963dfddc4747d6200353b50f6093a6e37ca82e1612fa397d64ff13e7299`  
		Last Modified: Thu, 16 Apr 2020 01:12:33 GMT  
		Size: 19.3 MB (19298546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a83ba0d6e415d0bb68db80a86f4023e0cac619036ce507dc505523c397d3975`  
		Last Modified: Thu, 16 Apr 2020 02:04:40 GMT  
		Size: 3.9 MB (3877396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf4dc95e0852c9fced212c2f67659e706079ce008dfec7f6a95614019e94459`  
		Last Modified: Thu, 16 Apr 2020 02:05:26 GMT  
		Size: 40.3 MB (40343047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a750a7ae1be2d6095c6cacd1cbc4584782e12b59fc22b15048ffaa35d300a8`  
		Last Modified: Thu, 16 Apr 2020 02:05:16 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d563107fbf7fcbd2f215c764f8cc34d825ac3f0070b05df4df8900bfdb2a65ef`  
		Last Modified: Thu, 16 Apr 2020 02:05:16 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f7e5d70a08545c0c838e6628e25b91809844076c3b261a6854b793e8ca0fe58`  
		Last Modified: Thu, 16 Apr 2020 02:05:16 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.2` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:e585988f56e50a55821ac2e2b18988ca7e4adcf4b12388ebf47f15fe254d10fa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64663687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc21688dc157e88e6173411b2f6f6eb3dd837b831f084e537785b371995cab7d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2020 02:45:19 GMT
ADD file:1588320d1c43714ec0353b7471f2ffd649045ca0f5f70dcb1eb064875fff9578 in / 
# Thu, 16 Apr 2020 02:45:21 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:33:04 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 16 Apr 2020 03:34:26 GMT
ENV CHRONOGRAF_VERSION=1.8.2
# Thu, 16 Apr 2020 03:34:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 16 Apr 2020 03:34:49 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 16 Apr 2020 03:34:49 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 16 Apr 2020 03:34:50 GMT
EXPOSE 8888
# Thu, 16 Apr 2020 03:34:51 GMT
VOLUME [/var/lib/chronograf]
# Thu, 16 Apr 2020 03:34:51 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 16 Apr 2020 03:34:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 03:34:52 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8978c87ff45d64d1663a585dcf1ed66d9e711c2e4048d83ef561da9514ef46e6`  
		Last Modified: Thu, 16 Apr 2020 02:51:32 GMT  
		Size: 20.4 MB (20370106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1f12b855cc63fdfabc47f79ca6cc4e5130d9eff6495b3185a5da6eeb8d2863`  
		Last Modified: Thu, 16 Apr 2020 03:35:11 GMT  
		Size: 4.1 MB (4080756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d698eafefe800059a5deaa8403e80d80b847cac90468018ad793778a858f42d`  
		Last Modified: Thu, 16 Apr 2020 03:36:07 GMT  
		Size: 40.2 MB (40188435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76a8c8ed7b841a7efdb7d0e8ed3d48ebdf9f7ba5eafc06d34407124ca35bd19`  
		Last Modified: Thu, 16 Apr 2020 03:35:57 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a69d0fa2a0dd3ae32b0207b4837f96fb5b46c3058b728083631ddaf70d064be`  
		Last Modified: Thu, 16 Apr 2020 03:35:57 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882b9145451c434a1cf0cb271de8bba0dae489fd001410f1c9b7a85690b00cb8`  
		Last Modified: Thu, 16 Apr 2020 03:35:56 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.2-alpine`

```console
$ docker pull chronograf@sha256:fe96927d2c143cb3afeb8b6963a6bb7ef36ae931ba4d5edeaef1e3931e1082ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:1.8.2-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:01f411926861bcd593da03c858b43df18f3a5750ec01614233fa42208a7e5dbc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 MB (25287329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05446ac0ba565f34ae94c60b605709b2762f6d80e050be43cff8fbe8a19c290f`
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
# Wed, 15 Apr 2020 20:20:26 GMT
ENV CHRONOGRAF_VERSION=1.8.2
# Wed, 15 Apr 2020 20:20:30 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 15 Apr 2020 20:20:30 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 15 Apr 2020 20:20:30 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 15 Apr 2020 20:20:30 GMT
EXPOSE 8888
# Wed, 15 Apr 2020 20:20:30 GMT
VOLUME [/var/lib/chronograf]
# Wed, 15 Apr 2020 20:20:31 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 15 Apr 2020 20:20:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2020 20:20:31 GMT
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
	-	`sha256:fe934bc6fc7e3e9db6994bcb67c703748b4a7ed6b5762ffed79525aba3723b1c`  
		Last Modified: Wed, 15 Apr 2020 20:21:02 GMT  
		Size: 22.2 MB (22196749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd6f0d94304face3afa76b0a7fd134aef1a10deaa37724c598fdd83e255fc4e`  
		Last Modified: Wed, 15 Apr 2020 20:20:58 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f4a08a2e2a459e441c3e367cc2e2bf9e8366f9b2ea9b30c70fff8ce6f8a3cf`  
		Last Modified: Wed, 15 Apr 2020 20:20:58 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d294eaaba88989877f07dbce9a8d1b8cd0e37e2dd4e8fad75b74ab04368cfce`  
		Last Modified: Wed, 15 Apr 2020 20:20:58 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:fe96927d2c143cb3afeb8b6963a6bb7ef36ae931ba4d5edeaef1e3931e1082ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:01f411926861bcd593da03c858b43df18f3a5750ec01614233fa42208a7e5dbc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 MB (25287329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05446ac0ba565f34ae94c60b605709b2762f6d80e050be43cff8fbe8a19c290f`
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
# Wed, 15 Apr 2020 20:20:26 GMT
ENV CHRONOGRAF_VERSION=1.8.2
# Wed, 15 Apr 2020 20:20:30 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 15 Apr 2020 20:20:30 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 15 Apr 2020 20:20:30 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 15 Apr 2020 20:20:30 GMT
EXPOSE 8888
# Wed, 15 Apr 2020 20:20:30 GMT
VOLUME [/var/lib/chronograf]
# Wed, 15 Apr 2020 20:20:31 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 15 Apr 2020 20:20:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2020 20:20:31 GMT
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
	-	`sha256:fe934bc6fc7e3e9db6994bcb67c703748b4a7ed6b5762ffed79525aba3723b1c`  
		Last Modified: Wed, 15 Apr 2020 20:21:02 GMT  
		Size: 22.2 MB (22196749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd6f0d94304face3afa76b0a7fd134aef1a10deaa37724c598fdd83e255fc4e`  
		Last Modified: Wed, 15 Apr 2020 20:20:58 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f4a08a2e2a459e441c3e367cc2e2bf9e8366f9b2ea9b30c70fff8ce6f8a3cf`  
		Last Modified: Wed, 15 Apr 2020 20:20:58 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d294eaaba88989877f07dbce9a8d1b8cd0e37e2dd4e8fad75b74ab04368cfce`  
		Last Modified: Wed, 15 Apr 2020 20:20:58 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:fe96927d2c143cb3afeb8b6963a6bb7ef36ae931ba4d5edeaef1e3931e1082ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:01f411926861bcd593da03c858b43df18f3a5750ec01614233fa42208a7e5dbc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 MB (25287329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05446ac0ba565f34ae94c60b605709b2762f6d80e050be43cff8fbe8a19c290f`
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
# Wed, 15 Apr 2020 20:20:26 GMT
ENV CHRONOGRAF_VERSION=1.8.2
# Wed, 15 Apr 2020 20:20:30 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 15 Apr 2020 20:20:30 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 15 Apr 2020 20:20:30 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 15 Apr 2020 20:20:30 GMT
EXPOSE 8888
# Wed, 15 Apr 2020 20:20:30 GMT
VOLUME [/var/lib/chronograf]
# Wed, 15 Apr 2020 20:20:31 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 15 Apr 2020 20:20:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2020 20:20:31 GMT
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
	-	`sha256:fe934bc6fc7e3e9db6994bcb67c703748b4a7ed6b5762ffed79525aba3723b1c`  
		Last Modified: Wed, 15 Apr 2020 20:21:02 GMT  
		Size: 22.2 MB (22196749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd6f0d94304face3afa76b0a7fd134aef1a10deaa37724c598fdd83e255fc4e`  
		Last Modified: Wed, 15 Apr 2020 20:20:58 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f4a08a2e2a459e441c3e367cc2e2bf9e8366f9b2ea9b30c70fff8ce6f8a3cf`  
		Last Modified: Wed, 15 Apr 2020 20:20:58 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d294eaaba88989877f07dbce9a8d1b8cd0e37e2dd4e8fad75b74ab04368cfce`  
		Last Modified: Wed, 15 Apr 2020 20:20:58 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:cd06ab5b1d080d96b57c72bc9c37ce5b2fe036d52a828715e1e974cda2632c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:a55c530d42cf36b1dd0d50589ede16fbf29807086b37e142b975e6c7726194e9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70123096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d3a298922095f82df717cb6635dfb956024853a8d779aed1a447d3162cf71c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:54:36 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 16 Apr 2020 03:55:33 GMT
ENV CHRONOGRAF_VERSION=1.8.2
# Thu, 16 Apr 2020 03:55:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 16 Apr 2020 03:55:51 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 16 Apr 2020 03:55:52 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 16 Apr 2020 03:55:52 GMT
EXPOSE 8888
# Thu, 16 Apr 2020 03:55:52 GMT
VOLUME [/var/lib/chronograf]
# Thu, 16 Apr 2020 03:55:53 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 16 Apr 2020 03:55:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 03:55:53 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44df9a0f20c0a9a55f33ce1ff19dbad64f53385c2d80e54cbae2095a8d4af02`  
		Last Modified: Thu, 16 Apr 2020 03:56:19 GMT  
		Size: 4.5 MB (4503605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03cb6cfbfe859b874306ae4930e04fb6f5126ef1c4868052cba5c87327c09af3`  
		Last Modified: Thu, 16 Apr 2020 03:56:53 GMT  
		Size: 43.1 MB (43081617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a4e39f707718b7d325f477dd5494de3859a4072d2cdc91859e59ff5f4eea12`  
		Last Modified: Thu, 16 Apr 2020 03:56:44 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69373310b905cc9fb8ff25b98daf958e0e14f75a71219ce82e8009308aace4ab`  
		Last Modified: Thu, 16 Apr 2020 03:56:43 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a8615afcc3335cdd446a318c5841f5d914bce72c7c6281cbe5fbb4829ea988`  
		Last Modified: Thu, 16 Apr 2020 03:56:44 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:6df64c9439758317fe998804398dc356c2072c2dc86aa1023a3f52657a787b68
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63543382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25bf9303adab528b50bd50799dc6ec73cdbd6cbe22d3ba8362e7f6191e86afb2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2020 01:05:08 GMT
ADD file:e37c4728c0c89ac126542ac35e7e493425c021bfac751079c9b266821a1b4e99 in / 
# Thu, 16 Apr 2020 01:05:10 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 02:02:01 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 16 Apr 2020 02:03:44 GMT
ENV CHRONOGRAF_VERSION=1.8.2
# Thu, 16 Apr 2020 02:04:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 16 Apr 2020 02:04:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 16 Apr 2020 02:04:17 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 16 Apr 2020 02:04:18 GMT
EXPOSE 8888
# Thu, 16 Apr 2020 02:04:19 GMT
VOLUME [/var/lib/chronograf]
# Thu, 16 Apr 2020 02:04:19 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 16 Apr 2020 02:04:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 02:04:22 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f78d9963dfddc4747d6200353b50f6093a6e37ca82e1612fa397d64ff13e7299`  
		Last Modified: Thu, 16 Apr 2020 01:12:33 GMT  
		Size: 19.3 MB (19298546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a83ba0d6e415d0bb68db80a86f4023e0cac619036ce507dc505523c397d3975`  
		Last Modified: Thu, 16 Apr 2020 02:04:40 GMT  
		Size: 3.9 MB (3877396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf4dc95e0852c9fced212c2f67659e706079ce008dfec7f6a95614019e94459`  
		Last Modified: Thu, 16 Apr 2020 02:05:26 GMT  
		Size: 40.3 MB (40343047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a750a7ae1be2d6095c6cacd1cbc4584782e12b59fc22b15048ffaa35d300a8`  
		Last Modified: Thu, 16 Apr 2020 02:05:16 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d563107fbf7fcbd2f215c764f8cc34d825ac3f0070b05df4df8900bfdb2a65ef`  
		Last Modified: Thu, 16 Apr 2020 02:05:16 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f7e5d70a08545c0c838e6628e25b91809844076c3b261a6854b793e8ca0fe58`  
		Last Modified: Thu, 16 Apr 2020 02:05:16 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:e585988f56e50a55821ac2e2b18988ca7e4adcf4b12388ebf47f15fe254d10fa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64663687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc21688dc157e88e6173411b2f6f6eb3dd837b831f084e537785b371995cab7d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2020 02:45:19 GMT
ADD file:1588320d1c43714ec0353b7471f2ffd649045ca0f5f70dcb1eb064875fff9578 in / 
# Thu, 16 Apr 2020 02:45:21 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:33:04 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 16 Apr 2020 03:34:26 GMT
ENV CHRONOGRAF_VERSION=1.8.2
# Thu, 16 Apr 2020 03:34:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 16 Apr 2020 03:34:49 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 16 Apr 2020 03:34:49 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 16 Apr 2020 03:34:50 GMT
EXPOSE 8888
# Thu, 16 Apr 2020 03:34:51 GMT
VOLUME [/var/lib/chronograf]
# Thu, 16 Apr 2020 03:34:51 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 16 Apr 2020 03:34:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 03:34:52 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8978c87ff45d64d1663a585dcf1ed66d9e711c2e4048d83ef561da9514ef46e6`  
		Last Modified: Thu, 16 Apr 2020 02:51:32 GMT  
		Size: 20.4 MB (20370106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1f12b855cc63fdfabc47f79ca6cc4e5130d9eff6495b3185a5da6eeb8d2863`  
		Last Modified: Thu, 16 Apr 2020 03:35:11 GMT  
		Size: 4.1 MB (4080756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d698eafefe800059a5deaa8403e80d80b847cac90468018ad793778a858f42d`  
		Last Modified: Thu, 16 Apr 2020 03:36:07 GMT  
		Size: 40.2 MB (40188435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76a8c8ed7b841a7efdb7d0e8ed3d48ebdf9f7ba5eafc06d34407124ca35bd19`  
		Last Modified: Thu, 16 Apr 2020 03:35:57 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a69d0fa2a0dd3ae32b0207b4837f96fb5b46c3058b728083631ddaf70d064be`  
		Last Modified: Thu, 16 Apr 2020 03:35:57 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882b9145451c434a1cf0cb271de8bba0dae489fd001410f1c9b7a85690b00cb8`  
		Last Modified: Thu, 16 Apr 2020 03:35:56 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
