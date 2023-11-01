<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.10`](#chronograf110)
-	[`chronograf:1.10-alpine`](#chronograf110-alpine)
-	[`chronograf:1.10.2`](#chronograf1102)
-	[`chronograf:1.10.2-alpine`](#chronograf1102-alpine)
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

## `chronograf:1.10`

```console
$ docker pull chronograf@sha256:3f3d7fe26384875f3da735a5cfecc96c4c0d987ee7d8fb9007393e60eec4fa96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.10` - linux; amd64

```console
$ docker pull chronograf@sha256:1a461fbe3edab762b1d59bcedb52e0f8e6b0970978aaea196f8d2cee12c7dcaa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84100967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e1dc006b87ef469329f2f30f1c8ccf4a91484765e4f522eb5635326d033295b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:49 GMT
ADD file:fbd8521c24ed758023728505c18d7a0d6d101bc77fd772a4af9b65049b943864 in / 
# Wed, 01 Nov 2023 00:20:49 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:08:34 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 01 Nov 2023 01:08:34 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Wed, 01 Nov 2023 01:08:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 01 Nov 2023 01:08:43 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 01 Nov 2023 01:08:43 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 01 Nov 2023 01:08:43 GMT
EXPOSE 8888
# Wed, 01 Nov 2023 01:08:43 GMT
VOLUME [/var/lib/chronograf]
# Wed, 01 Nov 2023 01:08:43 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 01 Nov 2023 01:08:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Nov 2023 01:08:43 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:578acb154839e9d0034432e8f53756d6f53ba62cf8c7ea5218a2476bf5b58fc9`  
		Last Modified: Wed, 01 Nov 2023 00:25:30 GMT  
		Size: 29.1 MB (29149836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74552c3cf744ecac6301ccde01a6a900a075b6c630a9f40b8abe29dde4a3e0b3`  
		Last Modified: Wed, 01 Nov 2023 01:09:51 GMT  
		Size: 7.9 MB (7873082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805fc64ace298a45ceda26ee328a12efc77ee97c4ffe0005b9d92adaabe8eb8c`  
		Last Modified: Wed, 01 Nov 2023 01:09:56 GMT  
		Size: 47.1 MB (47053662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe49558d81938f5c83cf0c2775ce79b575abaa938b3593a68598c62e4c18664`  
		Last Modified: Wed, 01 Nov 2023 01:09:50 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:869439d87344d0d0f75a8ae7cc5e6268384d88f988b4e6f4e549c978eb57a8b7`  
		Last Modified: Wed, 01 Nov 2023 01:09:50 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4a93857ae7d9c3a84b65e983d1c77071a23c7b74179bfcb3fd25b12faa9c16`  
		Last Modified: Wed, 01 Nov 2023 01:09:50 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:f561842ea3ac1c45f50ae0d511db8fade073f7135618a809e6d934e166eefcb9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75920594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95853d742a1a56e274165274664fe8b599273b187265f004ab759cbccbb436dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:11 GMT
ADD file:da08fed31a161a2210fd920a1b5e43aa3f4199985cdeaa0d5d24c0a0f19044aa in / 
# Wed, 11 Oct 2023 17:42:11 GMT
CMD ["bash"]
# Tue, 24 Oct 2023 00:57:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 24 Oct 2023 00:57:28 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 24 Oct 2023 00:57:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 24 Oct 2023 00:57:39 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 24 Oct 2023 00:57:39 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 24 Oct 2023 00:57:39 GMT
EXPOSE 8888
# Tue, 24 Oct 2023 00:57:39 GMT
VOLUME [/var/lib/chronograf]
# Tue, 24 Oct 2023 00:57:39 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 24 Oct 2023 00:57:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Oct 2023 00:57:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2f11c34abc7b59f09b58bb6e2cf54f260f4b4142ecf8023a114e281ea4b532d1`  
		Last Modified: Wed, 11 Oct 2023 17:46:22 GMT  
		Size: 24.7 MB (24748925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d373ef288c1016255f23880fa193ed8c7b16d4316eb58a30fcd570f718deccd4`  
		Last Modified: Tue, 24 Oct 2023 00:57:55 GMT  
		Size: 6.5 MB (6497689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2639aee512dab0e2fe78d1a515ae90b96cc3d89f675da7730898afb2cf7a18`  
		Last Modified: Tue, 24 Oct 2023 00:58:00 GMT  
		Size: 44.6 MB (44649590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed879c5c9cd7cc45825042bf0c9e2eb2933605e0d70f4f07af5f3b304114cac2`  
		Last Modified: Tue, 24 Oct 2023 00:57:54 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5b56f84fc2d127783ba14e5ded545ee284891285786a7e6a2ff86302561930`  
		Last Modified: Tue, 24 Oct 2023 00:57:54 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6392494cbb507a347e77034033f4d60c98c65638650c7b64bc988008353e0b3e`  
		Last Modified: Tue, 24 Oct 2023 00:57:53 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:c9fe4efbd1d71455a6fa4b661b4d78e670d34f082c3d8b554c73d7e981f8addf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81627643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5475822bc23d4a7a3706572d7590da773f63f34429209a46f4e6e787f9465543`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Tue, 24 Oct 2023 00:39:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 24 Oct 2023 00:39:33 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 24 Oct 2023 00:39:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 24 Oct 2023 00:39:42 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 24 Oct 2023 00:39:42 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 24 Oct 2023 00:39:42 GMT
EXPOSE 8888
# Tue, 24 Oct 2023 00:39:42 GMT
VOLUME [/var/lib/chronograf]
# Tue, 24 Oct 2023 00:39:42 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 24 Oct 2023 00:39:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Oct 2023 00:39:42 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4cdcc7908019036cf9c3d001ab98e52b489a56b0cf84628701cdd5171f58ba0`  
		Last Modified: Tue, 24 Oct 2023 00:39:59 GMT  
		Size: 7.7 MB (7650123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8aa51a450f2913c77d18e427d6d96164c2512d6049b5deb2a55ac285fdf54bb`  
		Last Modified: Tue, 24 Oct 2023 00:40:04 GMT  
		Size: 44.8 MB (44773847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf898ad709c1a0f6df7a3686c89f054fcc8c37cf07f5e6331b8fd90b996e3188`  
		Last Modified: Tue, 24 Oct 2023 00:39:58 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcae01731a3dc25c2550dbbb256be4612a6daf965ea1a0a9e2f07357f994a5a8`  
		Last Modified: Tue, 24 Oct 2023 00:39:58 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a71d77cfe25f61f27d00798befe3934cd764f9d0e4af6328e313b3a86dd77c0`  
		Last Modified: Tue, 24 Oct 2023 00:39:58 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:7530358bc4ca04eb208da945243c805590bf122d3261f8a97fabc0d8a89bf622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:fb43ec35ddd6e58cc2e78ef58f797cb6de9067c3932e3db1f85a4aea80fb6751
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31558951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55651823a683848ddd413718b400ba4b653ea7e671921241f5a3604a2cef16d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 01:30:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 02:34:58 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 24 Oct 2023 00:20:11 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 24 Oct 2023 00:20:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 24 Oct 2023 00:20:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 24 Oct 2023 00:20:16 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 24 Oct 2023 00:20:16 GMT
EXPOSE 8888
# Tue, 24 Oct 2023 00:20:16 GMT
VOLUME [/var/lib/chronograf]
# Tue, 24 Oct 2023 00:20:16 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 24 Oct 2023 00:20:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Oct 2023 00:20:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5352bf3aec614dde8ac36d38f28f5021eff4c2ff0226eb22dfa667f2b2add1`  
		Last Modified: Tue, 17 Oct 2023 01:33:20 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4048f49511dda4f4f68ff84317685f405a4090adcf74b1c9c7116e71ae80d30a`  
		Last Modified: Sat, 21 Oct 2023 02:35:44 GMT  
		Size: 284.7 KB (284698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6545ebb960dd3a534da359758d3fec7757e7866b3655ad8432156ab58b56bf56`  
		Last Modified: Tue, 24 Oct 2023 00:21:04 GMT  
		Size: 27.8 MB (27847599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28322186901948002f5674f518fd78626ce89862f988bcfbfe22b03a9868134`  
		Last Modified: Tue, 24 Oct 2023 00:20:58 GMT  
		Size: 12.3 KB (12268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d268d1b30ec9afb6cf8ac11fe77068afa5f6b2e2211c3e2861d51f122b8b5e07`  
		Last Modified: Tue, 24 Oct 2023 00:20:59 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c48929913d0bb1a8ca03b3dfcd0cfded77493e0142ff4fd446ca1f7bfbed9bd`  
		Last Modified: Tue, 24 Oct 2023 00:20:58 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.10.2`

```console
$ docker pull chronograf@sha256:3f3d7fe26384875f3da735a5cfecc96c4c0d987ee7d8fb9007393e60eec4fa96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.10.2` - linux; amd64

```console
$ docker pull chronograf@sha256:1a461fbe3edab762b1d59bcedb52e0f8e6b0970978aaea196f8d2cee12c7dcaa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84100967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e1dc006b87ef469329f2f30f1c8ccf4a91484765e4f522eb5635326d033295b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:49 GMT
ADD file:fbd8521c24ed758023728505c18d7a0d6d101bc77fd772a4af9b65049b943864 in / 
# Wed, 01 Nov 2023 00:20:49 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:08:34 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 01 Nov 2023 01:08:34 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Wed, 01 Nov 2023 01:08:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 01 Nov 2023 01:08:43 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 01 Nov 2023 01:08:43 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 01 Nov 2023 01:08:43 GMT
EXPOSE 8888
# Wed, 01 Nov 2023 01:08:43 GMT
VOLUME [/var/lib/chronograf]
# Wed, 01 Nov 2023 01:08:43 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 01 Nov 2023 01:08:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Nov 2023 01:08:43 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:578acb154839e9d0034432e8f53756d6f53ba62cf8c7ea5218a2476bf5b58fc9`  
		Last Modified: Wed, 01 Nov 2023 00:25:30 GMT  
		Size: 29.1 MB (29149836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74552c3cf744ecac6301ccde01a6a900a075b6c630a9f40b8abe29dde4a3e0b3`  
		Last Modified: Wed, 01 Nov 2023 01:09:51 GMT  
		Size: 7.9 MB (7873082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805fc64ace298a45ceda26ee328a12efc77ee97c4ffe0005b9d92adaabe8eb8c`  
		Last Modified: Wed, 01 Nov 2023 01:09:56 GMT  
		Size: 47.1 MB (47053662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe49558d81938f5c83cf0c2775ce79b575abaa938b3593a68598c62e4c18664`  
		Last Modified: Wed, 01 Nov 2023 01:09:50 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:869439d87344d0d0f75a8ae7cc5e6268384d88f988b4e6f4e549c978eb57a8b7`  
		Last Modified: Wed, 01 Nov 2023 01:09:50 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4a93857ae7d9c3a84b65e983d1c77071a23c7b74179bfcb3fd25b12faa9c16`  
		Last Modified: Wed, 01 Nov 2023 01:09:50 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10.2` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:f561842ea3ac1c45f50ae0d511db8fade073f7135618a809e6d934e166eefcb9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75920594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95853d742a1a56e274165274664fe8b599273b187265f004ab759cbccbb436dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:11 GMT
ADD file:da08fed31a161a2210fd920a1b5e43aa3f4199985cdeaa0d5d24c0a0f19044aa in / 
# Wed, 11 Oct 2023 17:42:11 GMT
CMD ["bash"]
# Tue, 24 Oct 2023 00:57:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 24 Oct 2023 00:57:28 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 24 Oct 2023 00:57:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 24 Oct 2023 00:57:39 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 24 Oct 2023 00:57:39 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 24 Oct 2023 00:57:39 GMT
EXPOSE 8888
# Tue, 24 Oct 2023 00:57:39 GMT
VOLUME [/var/lib/chronograf]
# Tue, 24 Oct 2023 00:57:39 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 24 Oct 2023 00:57:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Oct 2023 00:57:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2f11c34abc7b59f09b58bb6e2cf54f260f4b4142ecf8023a114e281ea4b532d1`  
		Last Modified: Wed, 11 Oct 2023 17:46:22 GMT  
		Size: 24.7 MB (24748925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d373ef288c1016255f23880fa193ed8c7b16d4316eb58a30fcd570f718deccd4`  
		Last Modified: Tue, 24 Oct 2023 00:57:55 GMT  
		Size: 6.5 MB (6497689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2639aee512dab0e2fe78d1a515ae90b96cc3d89f675da7730898afb2cf7a18`  
		Last Modified: Tue, 24 Oct 2023 00:58:00 GMT  
		Size: 44.6 MB (44649590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed879c5c9cd7cc45825042bf0c9e2eb2933605e0d70f4f07af5f3b304114cac2`  
		Last Modified: Tue, 24 Oct 2023 00:57:54 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5b56f84fc2d127783ba14e5ded545ee284891285786a7e6a2ff86302561930`  
		Last Modified: Tue, 24 Oct 2023 00:57:54 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6392494cbb507a347e77034033f4d60c98c65638650c7b64bc988008353e0b3e`  
		Last Modified: Tue, 24 Oct 2023 00:57:53 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10.2` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:c9fe4efbd1d71455a6fa4b661b4d78e670d34f082c3d8b554c73d7e981f8addf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81627643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5475822bc23d4a7a3706572d7590da773f63f34429209a46f4e6e787f9465543`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Tue, 24 Oct 2023 00:39:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 24 Oct 2023 00:39:33 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 24 Oct 2023 00:39:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 24 Oct 2023 00:39:42 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 24 Oct 2023 00:39:42 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 24 Oct 2023 00:39:42 GMT
EXPOSE 8888
# Tue, 24 Oct 2023 00:39:42 GMT
VOLUME [/var/lib/chronograf]
# Tue, 24 Oct 2023 00:39:42 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 24 Oct 2023 00:39:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Oct 2023 00:39:42 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4cdcc7908019036cf9c3d001ab98e52b489a56b0cf84628701cdd5171f58ba0`  
		Last Modified: Tue, 24 Oct 2023 00:39:59 GMT  
		Size: 7.7 MB (7650123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8aa51a450f2913c77d18e427d6d96164c2512d6049b5deb2a55ac285fdf54bb`  
		Last Modified: Tue, 24 Oct 2023 00:40:04 GMT  
		Size: 44.8 MB (44773847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf898ad709c1a0f6df7a3686c89f054fcc8c37cf07f5e6331b8fd90b996e3188`  
		Last Modified: Tue, 24 Oct 2023 00:39:58 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcae01731a3dc25c2550dbbb256be4612a6daf965ea1a0a9e2f07357f994a5a8`  
		Last Modified: Tue, 24 Oct 2023 00:39:58 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a71d77cfe25f61f27d00798befe3934cd764f9d0e4af6328e313b3a86dd77c0`  
		Last Modified: Tue, 24 Oct 2023 00:39:58 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.10.2-alpine`

```console
$ docker pull chronograf@sha256:7530358bc4ca04eb208da945243c805590bf122d3261f8a97fabc0d8a89bf622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.10.2-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:fb43ec35ddd6e58cc2e78ef58f797cb6de9067c3932e3db1f85a4aea80fb6751
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31558951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55651823a683848ddd413718b400ba4b653ea7e671921241f5a3604a2cef16d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 01:30:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 02:34:58 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 24 Oct 2023 00:20:11 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 24 Oct 2023 00:20:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 24 Oct 2023 00:20:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 24 Oct 2023 00:20:16 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 24 Oct 2023 00:20:16 GMT
EXPOSE 8888
# Tue, 24 Oct 2023 00:20:16 GMT
VOLUME [/var/lib/chronograf]
# Tue, 24 Oct 2023 00:20:16 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 24 Oct 2023 00:20:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Oct 2023 00:20:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5352bf3aec614dde8ac36d38f28f5021eff4c2ff0226eb22dfa667f2b2add1`  
		Last Modified: Tue, 17 Oct 2023 01:33:20 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4048f49511dda4f4f68ff84317685f405a4090adcf74b1c9c7116e71ae80d30a`  
		Last Modified: Sat, 21 Oct 2023 02:35:44 GMT  
		Size: 284.7 KB (284698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6545ebb960dd3a534da359758d3fec7757e7866b3655ad8432156ab58b56bf56`  
		Last Modified: Tue, 24 Oct 2023 00:21:04 GMT  
		Size: 27.8 MB (27847599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28322186901948002f5674f518fd78626ce89862f988bcfbfe22b03a9868134`  
		Last Modified: Tue, 24 Oct 2023 00:20:58 GMT  
		Size: 12.3 KB (12268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d268d1b30ec9afb6cf8ac11fe77068afa5f6b2e2211c3e2861d51f122b8b5e07`  
		Last Modified: Tue, 24 Oct 2023 00:20:59 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c48929913d0bb1a8ca03b3dfcd0cfded77493e0142ff4fd446ca1f7bfbed9bd`  
		Last Modified: Tue, 24 Oct 2023 00:20:58 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:e0bd028718a50fdb0ac7c85f277db67c03f9ba7f3734a8fe229ffcd452b8cb56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7` - linux; amd64

```console
$ docker pull chronograf@sha256:5c9b8ec096ec5ae82112884eaf1e6051c57e47ab47ddfa8497f9e16cd872e943
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70599012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb52087659b2da97d1aeeaf7c88c51b5c63dce727304a250a5b2167cde2a65f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:07:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 01 Nov 2023 01:07:36 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 01 Nov 2023 01:07:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 01 Nov 2023 01:07:44 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 01 Nov 2023 01:07:45 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 01 Nov 2023 01:07:45 GMT
EXPOSE 8888
# Wed, 01 Nov 2023 01:07:45 GMT
VOLUME [/var/lib/chronograf]
# Wed, 01 Nov 2023 01:07:45 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 01 Nov 2023 01:07:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Nov 2023 01:07:45 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35affda53775936efa474cb9aec8f4ec922ba2efa2a1c54c15d5a0521dcc4a4`  
		Last Modified: Wed, 01 Nov 2023 01:09:07 GMT  
		Size: 4.4 MB (4417362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6667baf4b984c11e75bb2a374db7604f4d12d99b419310303613c03509417241`  
		Last Modified: Wed, 01 Nov 2023 01:09:11 GMT  
		Size: 34.7 MB (34739345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617d828d3d940163b5334420b3dd4e63000d2bd4075402d44ab29c7cce00bc79`  
		Last Modified: Wed, 01 Nov 2023 01:09:07 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60048f906d91ebde1c064e3ebd2e3cb7b33596e3262d47b9d2e48a2c127096eb`  
		Last Modified: Wed, 01 Nov 2023 01:09:07 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d08aa9a956ba4f56d0a1bfb620d9459a0ec9f363f0a3fe1004f0825a0b3ae8`  
		Last Modified: Wed, 01 Nov 2023 01:09:07 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:e278faaa6a70c4414503d4d935a84bc4611e69121ded1d5a8e3c513ff801bd4c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63422665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829d42ad58a614d78757b478590d61c59e93b97ac394614cbac0be10f76f380a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:29 GMT
ADD file:0d1753bfedd7193184780166819d0407867a22d82804c0045274f1f13afecac0 in / 
# Wed, 11 Oct 2023 17:42:29 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:18:47 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 Oct 2023 18:18:47 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 11 Oct 2023 18:18:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 Oct 2023 18:18:57 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 Oct 2023 18:18:57 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 Oct 2023 18:18:57 GMT
EXPOSE 8888
# Wed, 11 Oct 2023 18:18:57 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 Oct 2023 18:18:57 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 Oct 2023 18:18:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Oct 2023 18:18:57 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bb9c59b28e9fb9c31ffdb002ca9a6656677eee093c8093fcbea8818e927df70a`  
		Last Modified: Wed, 11 Oct 2023 17:47:06 GMT  
		Size: 26.6 MB (26579008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b1d927d01dca9cb7a6bb783e36cace9cd8f5bac3a65d1d93af6336082169f7`  
		Last Modified: Wed, 11 Oct 2023 18:19:57 GMT  
		Size: 3.7 MB (3719890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142e5bafbc8ece06dd411e0e2a88e4834e87ccce2bab85d84c5dcbf82956d7f5`  
		Last Modified: Wed, 11 Oct 2023 18:20:01 GMT  
		Size: 33.1 MB (33099374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f1e379f64d26dc3fc57a3d0e40480d27394af49ebac6cdc4beb6106f037ea4`  
		Last Modified: Wed, 11 Oct 2023 18:19:56 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15091ab8f90eb6742de83da9442de1e61204bd02311957e8200ac1178061bd8f`  
		Last Modified: Wed, 11 Oct 2023 18:19:56 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c8762af1ea37ebdac079efb34864bf01333da66a264907b5fe0dd907454fdb`  
		Last Modified: Wed, 11 Oct 2023 18:19:56 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:389c74876512f03e023854e70553230c444008af1738a1fee36896c64b90f9be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67747147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91d89d56aaf500c64614c43342c9c3f3c89e577ed2386551996558f15caf000`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 19:59:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 Oct 2023 19:59:05 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 11 Oct 2023 19:59:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 Oct 2023 19:59:13 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 Oct 2023 19:59:13 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 Oct 2023 19:59:13 GMT
EXPOSE 8888
# Wed, 11 Oct 2023 19:59:13 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 Oct 2023 19:59:13 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 Oct 2023 19:59:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Oct 2023 19:59:13 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5726819688860c7f93aa6f1d45e20cdb98e56e717eccc9c74e4a8602ed8929`  
		Last Modified: Wed, 11 Oct 2023 20:00:10 GMT  
		Size: 4.4 MB (4418969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53bd84476afe6fd96dc7cd71031753d7892ea0ce78f7c9e3605d3cb16a62760f`  
		Last Modified: Wed, 11 Oct 2023 20:00:17 GMT  
		Size: 33.2 MB (33239692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce0d1452407272a49f6bf371b7a2c936fa5dffd31d98de67ff621b97dd4a26e`  
		Last Modified: Wed, 11 Oct 2023 20:00:10 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018a72239f48ec52a2faad1f6559f359763e46bfc6f2728bb37185f81cf24009`  
		Last Modified: Wed, 11 Oct 2023 20:00:10 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d515cfa9cd89177129fb9538629a3b9a9f0aec0bcaecc5be1f34bd56dcfcf21`  
		Last Modified: Wed, 11 Oct 2023 20:00:09 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:62301ed8dd488c82101db47255be49e9986d8a25dac6fb4d2adeafe007e89efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:24745c70055c5b34ce94a9f10ff0e038724bc65bc1299bdf1853086c5c99d150
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23245411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6757fd40e7a2442b1e9015bf7f4537bd61e551143b98599d0659018801dfcdb6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 01:29:21 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 00:12:27 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 21 Oct 2023 00:12:27 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Sat, 21 Oct 2023 00:12:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 21 Oct 2023 00:12:33 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 21 Oct 2023 00:12:33 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 21 Oct 2023 00:12:33 GMT
EXPOSE 8888
# Sat, 21 Oct 2023 00:12:33 GMT
VOLUME [/var/lib/chronograf]
# Sat, 21 Oct 2023 00:12:33 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 21 Oct 2023 00:12:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 00:12:33 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b161763ec9e11116a97547438c5541153248aba5eddc76475885813812367da`  
		Last Modified: Tue, 17 Oct 2023 01:31:50 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c036769ce42fe6069bea0e08abbf145ff40fb3519e68ec986c7aaf6b109ac7d5`  
		Last Modified: Sat, 21 Oct 2023 00:13:30 GMT  
		Size: 284.9 KB (284931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02062f55c3474493b57edcf76d3dfb180f6979574218338b17c7055e0dacdfb1`  
		Last Modified: Sat, 21 Oct 2023 00:13:33 GMT  
		Size: 19.6 MB (19557198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da33d48693c709e5812be997c1f8d1585b2038d8a3e9f07deae21538282754db`  
		Last Modified: Sat, 21 Oct 2023 00:13:30 GMT  
		Size: 12.3 KB (12262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caed337108b2c3a0c9bf35f3a66f7ed7a429550b4fbdd33ab5d231be9c2c89d9`  
		Last Modified: Sat, 21 Oct 2023 00:13:30 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a3663990537a0cc88299aff9b2651df091f1bbd4ee851fcf3787e25cacc8a0`  
		Last Modified: Sat, 21 Oct 2023 00:13:30 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:e0bd028718a50fdb0ac7c85f277db67c03f9ba7f3734a8fe229ffcd452b8cb56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7.17` - linux; amd64

```console
$ docker pull chronograf@sha256:5c9b8ec096ec5ae82112884eaf1e6051c57e47ab47ddfa8497f9e16cd872e943
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70599012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb52087659b2da97d1aeeaf7c88c51b5c63dce727304a250a5b2167cde2a65f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:07:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 01 Nov 2023 01:07:36 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 01 Nov 2023 01:07:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 01 Nov 2023 01:07:44 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 01 Nov 2023 01:07:45 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 01 Nov 2023 01:07:45 GMT
EXPOSE 8888
# Wed, 01 Nov 2023 01:07:45 GMT
VOLUME [/var/lib/chronograf]
# Wed, 01 Nov 2023 01:07:45 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 01 Nov 2023 01:07:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Nov 2023 01:07:45 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35affda53775936efa474cb9aec8f4ec922ba2efa2a1c54c15d5a0521dcc4a4`  
		Last Modified: Wed, 01 Nov 2023 01:09:07 GMT  
		Size: 4.4 MB (4417362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6667baf4b984c11e75bb2a374db7604f4d12d99b419310303613c03509417241`  
		Last Modified: Wed, 01 Nov 2023 01:09:11 GMT  
		Size: 34.7 MB (34739345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617d828d3d940163b5334420b3dd4e63000d2bd4075402d44ab29c7cce00bc79`  
		Last Modified: Wed, 01 Nov 2023 01:09:07 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60048f906d91ebde1c064e3ebd2e3cb7b33596e3262d47b9d2e48a2c127096eb`  
		Last Modified: Wed, 01 Nov 2023 01:09:07 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d08aa9a956ba4f56d0a1bfb620d9459a0ec9f363f0a3fe1004f0825a0b3ae8`  
		Last Modified: Wed, 01 Nov 2023 01:09:07 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:e278faaa6a70c4414503d4d935a84bc4611e69121ded1d5a8e3c513ff801bd4c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63422665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829d42ad58a614d78757b478590d61c59e93b97ac394614cbac0be10f76f380a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:29 GMT
ADD file:0d1753bfedd7193184780166819d0407867a22d82804c0045274f1f13afecac0 in / 
# Wed, 11 Oct 2023 17:42:29 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:18:47 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 Oct 2023 18:18:47 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 11 Oct 2023 18:18:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 Oct 2023 18:18:57 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 Oct 2023 18:18:57 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 Oct 2023 18:18:57 GMT
EXPOSE 8888
# Wed, 11 Oct 2023 18:18:57 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 Oct 2023 18:18:57 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 Oct 2023 18:18:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Oct 2023 18:18:57 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bb9c59b28e9fb9c31ffdb002ca9a6656677eee093c8093fcbea8818e927df70a`  
		Last Modified: Wed, 11 Oct 2023 17:47:06 GMT  
		Size: 26.6 MB (26579008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b1d927d01dca9cb7a6bb783e36cace9cd8f5bac3a65d1d93af6336082169f7`  
		Last Modified: Wed, 11 Oct 2023 18:19:57 GMT  
		Size: 3.7 MB (3719890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142e5bafbc8ece06dd411e0e2a88e4834e87ccce2bab85d84c5dcbf82956d7f5`  
		Last Modified: Wed, 11 Oct 2023 18:20:01 GMT  
		Size: 33.1 MB (33099374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f1e379f64d26dc3fc57a3d0e40480d27394af49ebac6cdc4beb6106f037ea4`  
		Last Modified: Wed, 11 Oct 2023 18:19:56 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15091ab8f90eb6742de83da9442de1e61204bd02311957e8200ac1178061bd8f`  
		Last Modified: Wed, 11 Oct 2023 18:19:56 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c8762af1ea37ebdac079efb34864bf01333da66a264907b5fe0dd907454fdb`  
		Last Modified: Wed, 11 Oct 2023 18:19:56 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:389c74876512f03e023854e70553230c444008af1738a1fee36896c64b90f9be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67747147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91d89d56aaf500c64614c43342c9c3f3c89e577ed2386551996558f15caf000`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 19:59:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 Oct 2023 19:59:05 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 11 Oct 2023 19:59:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 Oct 2023 19:59:13 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 Oct 2023 19:59:13 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 Oct 2023 19:59:13 GMT
EXPOSE 8888
# Wed, 11 Oct 2023 19:59:13 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 Oct 2023 19:59:13 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 Oct 2023 19:59:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Oct 2023 19:59:13 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5726819688860c7f93aa6f1d45e20cdb98e56e717eccc9c74e4a8602ed8929`  
		Last Modified: Wed, 11 Oct 2023 20:00:10 GMT  
		Size: 4.4 MB (4418969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53bd84476afe6fd96dc7cd71031753d7892ea0ce78f7c9e3605d3cb16a62760f`  
		Last Modified: Wed, 11 Oct 2023 20:00:17 GMT  
		Size: 33.2 MB (33239692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce0d1452407272a49f6bf371b7a2c936fa5dffd31d98de67ff621b97dd4a26e`  
		Last Modified: Wed, 11 Oct 2023 20:00:10 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018a72239f48ec52a2faad1f6559f359763e46bfc6f2728bb37185f81cf24009`  
		Last Modified: Wed, 11 Oct 2023 20:00:10 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d515cfa9cd89177129fb9538629a3b9a9f0aec0bcaecc5be1f34bd56dcfcf21`  
		Last Modified: Wed, 11 Oct 2023 20:00:09 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:62301ed8dd488c82101db47255be49e9986d8a25dac6fb4d2adeafe007e89efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:24745c70055c5b34ce94a9f10ff0e038724bc65bc1299bdf1853086c5c99d150
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23245411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6757fd40e7a2442b1e9015bf7f4537bd61e551143b98599d0659018801dfcdb6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 01:29:21 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 00:12:27 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 21 Oct 2023 00:12:27 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Sat, 21 Oct 2023 00:12:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 21 Oct 2023 00:12:33 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 21 Oct 2023 00:12:33 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 21 Oct 2023 00:12:33 GMT
EXPOSE 8888
# Sat, 21 Oct 2023 00:12:33 GMT
VOLUME [/var/lib/chronograf]
# Sat, 21 Oct 2023 00:12:33 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 21 Oct 2023 00:12:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 00:12:33 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b161763ec9e11116a97547438c5541153248aba5eddc76475885813812367da`  
		Last Modified: Tue, 17 Oct 2023 01:31:50 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c036769ce42fe6069bea0e08abbf145ff40fb3519e68ec986c7aaf6b109ac7d5`  
		Last Modified: Sat, 21 Oct 2023 00:13:30 GMT  
		Size: 284.9 KB (284931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02062f55c3474493b57edcf76d3dfb180f6979574218338b17c7055e0dacdfb1`  
		Last Modified: Sat, 21 Oct 2023 00:13:33 GMT  
		Size: 19.6 MB (19557198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da33d48693c709e5812be997c1f8d1585b2038d8a3e9f07deae21538282754db`  
		Last Modified: Sat, 21 Oct 2023 00:13:30 GMT  
		Size: 12.3 KB (12262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caed337108b2c3a0c9bf35f3a66f7ed7a429550b4fbdd33ab5d231be9c2c89d9`  
		Last Modified: Sat, 21 Oct 2023 00:13:30 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a3663990537a0cc88299aff9b2651df091f1bbd4ee851fcf3787e25cacc8a0`  
		Last Modified: Sat, 21 Oct 2023 00:13:30 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:619feeeb252f264c66619463530953052b510faeaaac35cc7d78dde380ce9f2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8` - linux; amd64

```console
$ docker pull chronograf@sha256:3d0b6ca8774f6a378a498989122a80a796d82658b12ba0997f7a5f78f36afac4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71250988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc841159405ead358abdc727a5f23bb91a0ac42bc479f0b0f5c1885083f3b52`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:07:59 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 01 Nov 2023 01:08:00 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 01 Nov 2023 01:08:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 01 Nov 2023 01:08:06 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 01 Nov 2023 01:08:06 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 01 Nov 2023 01:08:06 GMT
EXPOSE 8888
# Wed, 01 Nov 2023 01:08:06 GMT
VOLUME [/var/lib/chronograf]
# Wed, 01 Nov 2023 01:08:06 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 01 Nov 2023 01:08:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Nov 2023 01:08:07 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847941f89848cc57d1c0cea95a845974689e6b72d6b16bc086006c54c888d725`  
		Last Modified: Wed, 01 Nov 2023 01:09:22 GMT  
		Size: 5.2 MB (5228503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fce8ae35bb9a21864a7e30b1cb0581efa918c87a3910c2a54dee311bf4950ab`  
		Last Modified: Wed, 01 Nov 2023 01:09:25 GMT  
		Size: 34.6 MB (34580183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77adcca45f1bfd4c7688146a8c184cb0b7ef8115f821ce341aae35eea7092c4`  
		Last Modified: Wed, 01 Nov 2023 01:09:21 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266de969740f1c26a1b7efce3e48fabf7ab4b9755ecc627d540805f08fbcdff1`  
		Last Modified: Wed, 01 Nov 2023 01:09:21 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c106c84cb1910c5abb4b65787db7516a8b10681c662d0c8b846af0509dca5130`  
		Last Modified: Wed, 01 Nov 2023 01:09:21 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:6db29f45c067626c3aed58d554882530fb5a3a00985c4056c4b874065ebc83d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63848525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd537b51729c9005991ebee879bfc36732d22a4490c5c1444693dc77d41d4c6f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:29 GMT
ADD file:0d1753bfedd7193184780166819d0407867a22d82804c0045274f1f13afecac0 in / 
# Wed, 11 Oct 2023 17:42:29 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:19:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 Oct 2023 18:19:08 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 11 Oct 2023 18:19:16 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 Oct 2023 18:19:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 Oct 2023 18:19:16 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 Oct 2023 18:19:17 GMT
EXPOSE 8888
# Wed, 11 Oct 2023 18:19:17 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 Oct 2023 18:19:17 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 Oct 2023 18:19:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Oct 2023 18:19:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bb9c59b28e9fb9c31ffdb002ca9a6656677eee093c8093fcbea8818e927df70a`  
		Last Modified: Wed, 11 Oct 2023 17:47:06 GMT  
		Size: 26.6 MB (26579008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9796c0695f7c556cf6e46458a58316bc4e6ffab4671c0fa4471842995e378a`  
		Last Modified: Wed, 11 Oct 2023 18:20:12 GMT  
		Size: 4.5 MB (4493561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5f0e0be44fbc850734570b2d88fe881e3589617158faca0bf71d464d093286`  
		Last Modified: Wed, 11 Oct 2023 18:20:17 GMT  
		Size: 32.8 MB (32751558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63722eb8a739fa7459961de7f42b57977a0305867f5a4ac70b4ae2f7bd93343`  
		Last Modified: Wed, 11 Oct 2023 18:20:11 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0c8af953b49ffddfed5b3133b59b99d7b8f4056232ee54742904508d4e8559`  
		Last Modified: Wed, 11 Oct 2023 18:20:11 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598707cc254ec589a73e90d88c1b5da72e089626006cb16d4e4937f835ed5be9`  
		Last Modified: Wed, 11 Oct 2023 18:20:11 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:f0364c6d62a4eac81bf44d534a97ae90e6d4b862f71826ba2e3cfd9931f6a1bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67945046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8f34dbe5238b09af2b6d13fe96e4e735fb776295a9861889622f2379a076ec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 19:59:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 Oct 2023 19:59:25 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 11 Oct 2023 19:59:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 Oct 2023 19:59:31 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 Oct 2023 19:59:31 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 Oct 2023 19:59:31 GMT
EXPOSE 8888
# Wed, 11 Oct 2023 19:59:32 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 Oct 2023 19:59:32 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 Oct 2023 19:59:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Oct 2023 19:59:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df4fe693d9f3cceb1c1b06884788e739020d0f333835b047254ec0b586f9f24`  
		Last Modified: Wed, 11 Oct 2023 20:00:27 GMT  
		Size: 5.2 MB (5210827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b87e56e22fae62a6f2d2e05772db53d0d4130764402cdfe4e10345bb94a788d`  
		Last Modified: Wed, 11 Oct 2023 20:00:30 GMT  
		Size: 32.6 MB (32645734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5dedde53c034f276e80b746ff544cef9646146d9eda03355f3cc87e55a0b73b`  
		Last Modified: Wed, 11 Oct 2023 20:00:26 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e17c12000dee3c58684aad96a5e4b2d9a907f83dbf549bfd817a1bae05b2cf5`  
		Last Modified: Wed, 11 Oct 2023 20:00:26 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8896a9bc0eea2fc1ee7bf39f1fe081d035f5e918780e6a2e04c262504b0ceb00`  
		Last Modified: Wed, 11 Oct 2023 20:00:26 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:cc10fd7518969a4605d1889b1de5a95cd8979e9467f67096c73cf99fde781ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:1b6c05b6263c8b9cf0a11223b81084da036abaa979eef2364c5ea859b3e90285
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22892405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa8a9ef98bfb0bd734bcf02bc17a58a7b15f43352e7541211ffc4a0a86254a1a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 01:29:21 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 00:12:27 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 21 Oct 2023 00:12:39 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Sat, 21 Oct 2023 00:12:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 21 Oct 2023 00:12:45 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 21 Oct 2023 00:12:45 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 21 Oct 2023 00:12:45 GMT
EXPOSE 8888
# Sat, 21 Oct 2023 00:12:45 GMT
VOLUME [/var/lib/chronograf]
# Sat, 21 Oct 2023 00:12:45 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 21 Oct 2023 00:12:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 00:12:45 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b161763ec9e11116a97547438c5541153248aba5eddc76475885813812367da`  
		Last Modified: Tue, 17 Oct 2023 01:31:50 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c036769ce42fe6069bea0e08abbf145ff40fb3519e68ec986c7aaf6b109ac7d5`  
		Last Modified: Sat, 21 Oct 2023 00:13:30 GMT  
		Size: 284.9 KB (284931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0b1c874c38ce8395e2b0ad4419e183732836ff93c95dbaae6750e12adf83a3`  
		Last Modified: Sat, 21 Oct 2023 00:13:46 GMT  
		Size: 19.2 MB (19204176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6504027c845086daa6704d917065b1cdabec3a571eecd15c0261123fa5430d5c`  
		Last Modified: Sat, 21 Oct 2023 00:13:43 GMT  
		Size: 12.3 KB (12268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f52fd4eb9c1c6195d51e33d2f607a12bcabe5fc16704357cdb9a04c414f18d2`  
		Last Modified: Sat, 21 Oct 2023 00:13:43 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69feeb04bb774c2c87951159d9654b586336851212e9b75a41e4256e1aabb306`  
		Last Modified: Sat, 21 Oct 2023 00:13:43 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:619feeeb252f264c66619463530953052b510faeaaac35cc7d78dde380ce9f2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8.10` - linux; amd64

```console
$ docker pull chronograf@sha256:3d0b6ca8774f6a378a498989122a80a796d82658b12ba0997f7a5f78f36afac4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71250988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc841159405ead358abdc727a5f23bb91a0ac42bc479f0b0f5c1885083f3b52`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:07:59 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 01 Nov 2023 01:08:00 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 01 Nov 2023 01:08:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 01 Nov 2023 01:08:06 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 01 Nov 2023 01:08:06 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 01 Nov 2023 01:08:06 GMT
EXPOSE 8888
# Wed, 01 Nov 2023 01:08:06 GMT
VOLUME [/var/lib/chronograf]
# Wed, 01 Nov 2023 01:08:06 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 01 Nov 2023 01:08:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Nov 2023 01:08:07 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847941f89848cc57d1c0cea95a845974689e6b72d6b16bc086006c54c888d725`  
		Last Modified: Wed, 01 Nov 2023 01:09:22 GMT  
		Size: 5.2 MB (5228503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fce8ae35bb9a21864a7e30b1cb0581efa918c87a3910c2a54dee311bf4950ab`  
		Last Modified: Wed, 01 Nov 2023 01:09:25 GMT  
		Size: 34.6 MB (34580183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77adcca45f1bfd4c7688146a8c184cb0b7ef8115f821ce341aae35eea7092c4`  
		Last Modified: Wed, 01 Nov 2023 01:09:21 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266de969740f1c26a1b7efce3e48fabf7ab4b9755ecc627d540805f08fbcdff1`  
		Last Modified: Wed, 01 Nov 2023 01:09:21 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c106c84cb1910c5abb4b65787db7516a8b10681c662d0c8b846af0509dca5130`  
		Last Modified: Wed, 01 Nov 2023 01:09:21 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:6db29f45c067626c3aed58d554882530fb5a3a00985c4056c4b874065ebc83d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63848525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd537b51729c9005991ebee879bfc36732d22a4490c5c1444693dc77d41d4c6f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:29 GMT
ADD file:0d1753bfedd7193184780166819d0407867a22d82804c0045274f1f13afecac0 in / 
# Wed, 11 Oct 2023 17:42:29 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:19:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 Oct 2023 18:19:08 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 11 Oct 2023 18:19:16 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 Oct 2023 18:19:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 Oct 2023 18:19:16 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 Oct 2023 18:19:17 GMT
EXPOSE 8888
# Wed, 11 Oct 2023 18:19:17 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 Oct 2023 18:19:17 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 Oct 2023 18:19:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Oct 2023 18:19:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bb9c59b28e9fb9c31ffdb002ca9a6656677eee093c8093fcbea8818e927df70a`  
		Last Modified: Wed, 11 Oct 2023 17:47:06 GMT  
		Size: 26.6 MB (26579008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9796c0695f7c556cf6e46458a58316bc4e6ffab4671c0fa4471842995e378a`  
		Last Modified: Wed, 11 Oct 2023 18:20:12 GMT  
		Size: 4.5 MB (4493561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5f0e0be44fbc850734570b2d88fe881e3589617158faca0bf71d464d093286`  
		Last Modified: Wed, 11 Oct 2023 18:20:17 GMT  
		Size: 32.8 MB (32751558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63722eb8a739fa7459961de7f42b57977a0305867f5a4ac70b4ae2f7bd93343`  
		Last Modified: Wed, 11 Oct 2023 18:20:11 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0c8af953b49ffddfed5b3133b59b99d7b8f4056232ee54742904508d4e8559`  
		Last Modified: Wed, 11 Oct 2023 18:20:11 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598707cc254ec589a73e90d88c1b5da72e089626006cb16d4e4937f835ed5be9`  
		Last Modified: Wed, 11 Oct 2023 18:20:11 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:f0364c6d62a4eac81bf44d534a97ae90e6d4b862f71826ba2e3cfd9931f6a1bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67945046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8f34dbe5238b09af2b6d13fe96e4e735fb776295a9861889622f2379a076ec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 19:59:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 Oct 2023 19:59:25 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 11 Oct 2023 19:59:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 Oct 2023 19:59:31 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 Oct 2023 19:59:31 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 Oct 2023 19:59:31 GMT
EXPOSE 8888
# Wed, 11 Oct 2023 19:59:32 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 Oct 2023 19:59:32 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 Oct 2023 19:59:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Oct 2023 19:59:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df4fe693d9f3cceb1c1b06884788e739020d0f333835b047254ec0b586f9f24`  
		Last Modified: Wed, 11 Oct 2023 20:00:27 GMT  
		Size: 5.2 MB (5210827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b87e56e22fae62a6f2d2e05772db53d0d4130764402cdfe4e10345bb94a788d`  
		Last Modified: Wed, 11 Oct 2023 20:00:30 GMT  
		Size: 32.6 MB (32645734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5dedde53c034f276e80b746ff544cef9646146d9eda03355f3cc87e55a0b73b`  
		Last Modified: Wed, 11 Oct 2023 20:00:26 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e17c12000dee3c58684aad96a5e4b2d9a907f83dbf549bfd817a1bae05b2cf5`  
		Last Modified: Wed, 11 Oct 2023 20:00:26 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8896a9bc0eea2fc1ee7bf39f1fe081d035f5e918780e6a2e04c262504b0ceb00`  
		Last Modified: Wed, 11 Oct 2023 20:00:26 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:cc10fd7518969a4605d1889b1de5a95cd8979e9467f67096c73cf99fde781ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:1b6c05b6263c8b9cf0a11223b81084da036abaa979eef2364c5ea859b3e90285
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22892405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa8a9ef98bfb0bd734bcf02bc17a58a7b15f43352e7541211ffc4a0a86254a1a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 01:29:21 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 00:12:27 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 21 Oct 2023 00:12:39 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Sat, 21 Oct 2023 00:12:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 21 Oct 2023 00:12:45 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 21 Oct 2023 00:12:45 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 21 Oct 2023 00:12:45 GMT
EXPOSE 8888
# Sat, 21 Oct 2023 00:12:45 GMT
VOLUME [/var/lib/chronograf]
# Sat, 21 Oct 2023 00:12:45 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 21 Oct 2023 00:12:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 00:12:45 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b161763ec9e11116a97547438c5541153248aba5eddc76475885813812367da`  
		Last Modified: Tue, 17 Oct 2023 01:31:50 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c036769ce42fe6069bea0e08abbf145ff40fb3519e68ec986c7aaf6b109ac7d5`  
		Last Modified: Sat, 21 Oct 2023 00:13:30 GMT  
		Size: 284.9 KB (284931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0b1c874c38ce8395e2b0ad4419e183732836ff93c95dbaae6750e12adf83a3`  
		Last Modified: Sat, 21 Oct 2023 00:13:46 GMT  
		Size: 19.2 MB (19204176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6504027c845086daa6704d917065b1cdabec3a571eecd15c0261123fa5430d5c`  
		Last Modified: Sat, 21 Oct 2023 00:13:43 GMT  
		Size: 12.3 KB (12268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f52fd4eb9c1c6195d51e33d2f607a12bcabe5fc16704357cdb9a04c414f18d2`  
		Last Modified: Sat, 21 Oct 2023 00:13:43 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69feeb04bb774c2c87951159d9654b586336851212e9b75a41e4256e1aabb306`  
		Last Modified: Sat, 21 Oct 2023 00:13:43 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:93bb976678c4c4a68d72e5f24812545656df7c2f8232d6e2698bfcbd7f7b994e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9` - linux; amd64

```console
$ docker pull chronograf@sha256:541e28d5234f12a3ed4ab52751271e6b6347ac908ea737b4e499b57bb8ac96a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71898666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f8f5f30dc9c8a37b5426754b25b608fc3c4e6c01c8dc2432bc7cd350eac3b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:07:59 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 01 Nov 2023 01:08:12 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 01 Nov 2023 01:08:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 01 Nov 2023 01:08:19 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 01 Nov 2023 01:08:19 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 01 Nov 2023 01:08:19 GMT
EXPOSE 8888
# Wed, 01 Nov 2023 01:08:20 GMT
VOLUME [/var/lib/chronograf]
# Wed, 01 Nov 2023 01:08:20 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 01 Nov 2023 01:08:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Nov 2023 01:08:20 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847941f89848cc57d1c0cea95a845974689e6b72d6b16bc086006c54c888d725`  
		Last Modified: Wed, 01 Nov 2023 01:09:22 GMT  
		Size: 5.2 MB (5228503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60890cf1f314dadc1e9aa36af968ecb19366d1969d233f4d2f368cd146e617c4`  
		Last Modified: Wed, 01 Nov 2023 01:09:40 GMT  
		Size: 35.2 MB (35227850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c03514a0813ed0bd253c94ea690e936b81820e692e7cd1cd2633f8c295ad81`  
		Last Modified: Wed, 01 Nov 2023 01:09:35 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3809ec8d3203ec1657f212482bf6d00b7d0bbd34334550f6e43587b788a079b`  
		Last Modified: Wed, 01 Nov 2023 01:09:35 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51beb4ee79e4f23f66ebb49cecbf8da5854d8eb617a0902f8b611ed742e0701c`  
		Last Modified: Wed, 01 Nov 2023 01:09:35 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:b53660fe1af5575ccecc242cdccee2faddf4ceae58cbf3dcb1bffc88911661e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64624643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa8ed8137a424e633ab2bf4dc99963f79893c8996bb7617060e7a79bbc70fa2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:29 GMT
ADD file:0d1753bfedd7193184780166819d0407867a22d82804c0045274f1f13afecac0 in / 
# Wed, 11 Oct 2023 17:42:29 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:19:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 Oct 2023 18:19:21 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 11 Oct 2023 18:19:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 Oct 2023 18:19:29 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 Oct 2023 18:19:29 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 Oct 2023 18:19:29 GMT
EXPOSE 8888
# Wed, 11 Oct 2023 18:19:29 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 Oct 2023 18:19:29 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 Oct 2023 18:19:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Oct 2023 18:19:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bb9c59b28e9fb9c31ffdb002ca9a6656677eee093c8093fcbea8818e927df70a`  
		Last Modified: Wed, 11 Oct 2023 17:47:06 GMT  
		Size: 26.6 MB (26579008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9796c0695f7c556cf6e46458a58316bc4e6ffab4671c0fa4471842995e378a`  
		Last Modified: Wed, 11 Oct 2023 18:20:12 GMT  
		Size: 4.5 MB (4493561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7db89586125167b6f56f20b3a3586f9b109f66056caa6a96fd52348b2567cb3`  
		Last Modified: Wed, 11 Oct 2023 18:20:33 GMT  
		Size: 33.5 MB (33527682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba4892e757f21d30309834fc54d0702acfe82e7aa79959d2089e88aa1f6e8f0f`  
		Last Modified: Wed, 11 Oct 2023 18:20:29 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa84064bbf2ccabc0739bbbe5f0cfeec5003a1e9c8e7b02490413c1909e9303`  
		Last Modified: Wed, 11 Oct 2023 18:20:28 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81a941aaadab250a92e70202471310fa150e9c3c428261213c0fdaeff2d29e0`  
		Last Modified: Wed, 11 Oct 2023 18:20:28 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:60022e10803e59c6c11c7aa7b5cc3434e63ef4feb6a3a3c4b82f9ee20ded4729
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68697413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d171ec2d92df7dc01689b48d5d241ee1e465d6a38ec89b37a13da8b605ba42a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 19:59:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 Oct 2023 19:59:35 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 11 Oct 2023 19:59:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 Oct 2023 19:59:41 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 Oct 2023 19:59:41 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 Oct 2023 19:59:41 GMT
EXPOSE 8888
# Wed, 11 Oct 2023 19:59:41 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 Oct 2023 19:59:42 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 Oct 2023 19:59:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Oct 2023 19:59:42 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df4fe693d9f3cceb1c1b06884788e739020d0f333835b047254ec0b586f9f24`  
		Last Modified: Wed, 11 Oct 2023 20:00:27 GMT  
		Size: 5.2 MB (5210827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81e8c09a18736d758e13723a9a6dd284dde367a888feaff1ddb381446e216e1`  
		Last Modified: Wed, 11 Oct 2023 20:00:43 GMT  
		Size: 33.4 MB (33398100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3473bfae7a2ab8e066ddb29d80f31c1d600ddb6f6abf38d3d37b45f9696460ba`  
		Last Modified: Wed, 11 Oct 2023 20:00:40 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89e22b9d4377cc3ee2878d8b1169c4401bf4bbaa39a28db6783eec95801721d`  
		Last Modified: Wed, 11 Oct 2023 20:00:39 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366b3e065f656cb4699d68fbb0ce7f675180ecd8be57a02a835647a5dc2a5190`  
		Last Modified: Wed, 11 Oct 2023 20:00:39 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:81fd6739ec0866d54aeb57fe7f230d9fd67d1847994eb336380a5363e2c5b006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:9c596fdc931db5549ac6d4144cbda1d6d82d666444dcce5eab5f478c02170372
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23360449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d248f08cbf5085807b61e50c39cc60fddb02fa315bea8cc96309bcb543b1a3a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 01:29:21 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 00:12:27 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 21 Oct 2023 00:12:51 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Sat, 21 Oct 2023 00:12:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 21 Oct 2023 00:12:57 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 21 Oct 2023 00:12:57 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 21 Oct 2023 00:12:57 GMT
EXPOSE 8888
# Sat, 21 Oct 2023 00:12:57 GMT
VOLUME [/var/lib/chronograf]
# Sat, 21 Oct 2023 00:12:57 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 21 Oct 2023 00:12:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 00:12:57 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b161763ec9e11116a97547438c5541153248aba5eddc76475885813812367da`  
		Last Modified: Tue, 17 Oct 2023 01:31:50 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c036769ce42fe6069bea0e08abbf145ff40fb3519e68ec986c7aaf6b109ac7d5`  
		Last Modified: Sat, 21 Oct 2023 00:13:30 GMT  
		Size: 284.9 KB (284931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e6e2e7b6d89418bd1dbd9a733b2da1c5474358f22390f540a25006f543b033`  
		Last Modified: Sat, 21 Oct 2023 00:13:58 GMT  
		Size: 19.7 MB (19672231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9564077ee006017e729c2c63139fef09a7515d5147bfb50e5c726bdd6f34501`  
		Last Modified: Sat, 21 Oct 2023 00:13:55 GMT  
		Size: 12.3 KB (12265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e02ba258151fc19eb314b23a6d3a4d9fac29b7641e2ca5a7086b562eb82c1d1`  
		Last Modified: Sat, 21 Oct 2023 00:13:55 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa94676f65ae15a93443979dc006bc3e8ffc5343e1201c834b3ef6f42d8f7427`  
		Last Modified: Sat, 21 Oct 2023 00:13:55 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:93bb976678c4c4a68d72e5f24812545656df7c2f8232d6e2698bfcbd7f7b994e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9.4` - linux; amd64

```console
$ docker pull chronograf@sha256:541e28d5234f12a3ed4ab52751271e6b6347ac908ea737b4e499b57bb8ac96a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71898666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f8f5f30dc9c8a37b5426754b25b608fc3c4e6c01c8dc2432bc7cd350eac3b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:07:59 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 01 Nov 2023 01:08:12 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 01 Nov 2023 01:08:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 01 Nov 2023 01:08:19 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 01 Nov 2023 01:08:19 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 01 Nov 2023 01:08:19 GMT
EXPOSE 8888
# Wed, 01 Nov 2023 01:08:20 GMT
VOLUME [/var/lib/chronograf]
# Wed, 01 Nov 2023 01:08:20 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 01 Nov 2023 01:08:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Nov 2023 01:08:20 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847941f89848cc57d1c0cea95a845974689e6b72d6b16bc086006c54c888d725`  
		Last Modified: Wed, 01 Nov 2023 01:09:22 GMT  
		Size: 5.2 MB (5228503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60890cf1f314dadc1e9aa36af968ecb19366d1969d233f4d2f368cd146e617c4`  
		Last Modified: Wed, 01 Nov 2023 01:09:40 GMT  
		Size: 35.2 MB (35227850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c03514a0813ed0bd253c94ea690e936b81820e692e7cd1cd2633f8c295ad81`  
		Last Modified: Wed, 01 Nov 2023 01:09:35 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3809ec8d3203ec1657f212482bf6d00b7d0bbd34334550f6e43587b788a079b`  
		Last Modified: Wed, 01 Nov 2023 01:09:35 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51beb4ee79e4f23f66ebb49cecbf8da5854d8eb617a0902f8b611ed742e0701c`  
		Last Modified: Wed, 01 Nov 2023 01:09:35 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:b53660fe1af5575ccecc242cdccee2faddf4ceae58cbf3dcb1bffc88911661e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64624643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa8ed8137a424e633ab2bf4dc99963f79893c8996bb7617060e7a79bbc70fa2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:29 GMT
ADD file:0d1753bfedd7193184780166819d0407867a22d82804c0045274f1f13afecac0 in / 
# Wed, 11 Oct 2023 17:42:29 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:19:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 Oct 2023 18:19:21 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 11 Oct 2023 18:19:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 Oct 2023 18:19:29 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 Oct 2023 18:19:29 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 Oct 2023 18:19:29 GMT
EXPOSE 8888
# Wed, 11 Oct 2023 18:19:29 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 Oct 2023 18:19:29 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 Oct 2023 18:19:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Oct 2023 18:19:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bb9c59b28e9fb9c31ffdb002ca9a6656677eee093c8093fcbea8818e927df70a`  
		Last Modified: Wed, 11 Oct 2023 17:47:06 GMT  
		Size: 26.6 MB (26579008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9796c0695f7c556cf6e46458a58316bc4e6ffab4671c0fa4471842995e378a`  
		Last Modified: Wed, 11 Oct 2023 18:20:12 GMT  
		Size: 4.5 MB (4493561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7db89586125167b6f56f20b3a3586f9b109f66056caa6a96fd52348b2567cb3`  
		Last Modified: Wed, 11 Oct 2023 18:20:33 GMT  
		Size: 33.5 MB (33527682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba4892e757f21d30309834fc54d0702acfe82e7aa79959d2089e88aa1f6e8f0f`  
		Last Modified: Wed, 11 Oct 2023 18:20:29 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa84064bbf2ccabc0739bbbe5f0cfeec5003a1e9c8e7b02490413c1909e9303`  
		Last Modified: Wed, 11 Oct 2023 18:20:28 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81a941aaadab250a92e70202471310fa150e9c3c428261213c0fdaeff2d29e0`  
		Last Modified: Wed, 11 Oct 2023 18:20:28 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:60022e10803e59c6c11c7aa7b5cc3434e63ef4feb6a3a3c4b82f9ee20ded4729
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68697413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d171ec2d92df7dc01689b48d5d241ee1e465d6a38ec89b37a13da8b605ba42a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 19:59:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 Oct 2023 19:59:35 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 11 Oct 2023 19:59:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 Oct 2023 19:59:41 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 Oct 2023 19:59:41 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 Oct 2023 19:59:41 GMT
EXPOSE 8888
# Wed, 11 Oct 2023 19:59:41 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 Oct 2023 19:59:42 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 Oct 2023 19:59:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Oct 2023 19:59:42 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df4fe693d9f3cceb1c1b06884788e739020d0f333835b047254ec0b586f9f24`  
		Last Modified: Wed, 11 Oct 2023 20:00:27 GMT  
		Size: 5.2 MB (5210827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81e8c09a18736d758e13723a9a6dd284dde367a888feaff1ddb381446e216e1`  
		Last Modified: Wed, 11 Oct 2023 20:00:43 GMT  
		Size: 33.4 MB (33398100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3473bfae7a2ab8e066ddb29d80f31c1d600ddb6f6abf38d3d37b45f9696460ba`  
		Last Modified: Wed, 11 Oct 2023 20:00:40 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89e22b9d4377cc3ee2878d8b1169c4401bf4bbaa39a28db6783eec95801721d`  
		Last Modified: Wed, 11 Oct 2023 20:00:39 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366b3e065f656cb4699d68fbb0ce7f675180ecd8be57a02a835647a5dc2a5190`  
		Last Modified: Wed, 11 Oct 2023 20:00:39 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:81fd6739ec0866d54aeb57fe7f230d9fd67d1847994eb336380a5363e2c5b006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:9c596fdc931db5549ac6d4144cbda1d6d82d666444dcce5eab5f478c02170372
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23360449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d248f08cbf5085807b61e50c39cc60fddb02fa315bea8cc96309bcb543b1a3a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 01:29:21 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 00:12:27 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 21 Oct 2023 00:12:51 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Sat, 21 Oct 2023 00:12:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 21 Oct 2023 00:12:57 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 21 Oct 2023 00:12:57 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 21 Oct 2023 00:12:57 GMT
EXPOSE 8888
# Sat, 21 Oct 2023 00:12:57 GMT
VOLUME [/var/lib/chronograf]
# Sat, 21 Oct 2023 00:12:57 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 21 Oct 2023 00:12:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 00:12:57 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b161763ec9e11116a97547438c5541153248aba5eddc76475885813812367da`  
		Last Modified: Tue, 17 Oct 2023 01:31:50 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c036769ce42fe6069bea0e08abbf145ff40fb3519e68ec986c7aaf6b109ac7d5`  
		Last Modified: Sat, 21 Oct 2023 00:13:30 GMT  
		Size: 284.9 KB (284931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e6e2e7b6d89418bd1dbd9a733b2da1c5474358f22390f540a25006f543b033`  
		Last Modified: Sat, 21 Oct 2023 00:13:58 GMT  
		Size: 19.7 MB (19672231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9564077ee006017e729c2c63139fef09a7515d5147bfb50e5c726bdd6f34501`  
		Last Modified: Sat, 21 Oct 2023 00:13:55 GMT  
		Size: 12.3 KB (12265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e02ba258151fc19eb314b23a6d3a4d9fac29b7641e2ca5a7086b562eb82c1d1`  
		Last Modified: Sat, 21 Oct 2023 00:13:55 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa94676f65ae15a93443979dc006bc3e8ffc5343e1201c834b3ef6f42d8f7427`  
		Last Modified: Sat, 21 Oct 2023 00:13:55 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:7530358bc4ca04eb208da945243c805590bf122d3261f8a97fabc0d8a89bf622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:fb43ec35ddd6e58cc2e78ef58f797cb6de9067c3932e3db1f85a4aea80fb6751
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31558951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55651823a683848ddd413718b400ba4b653ea7e671921241f5a3604a2cef16d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 01:30:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 02:34:58 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 24 Oct 2023 00:20:11 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 24 Oct 2023 00:20:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 24 Oct 2023 00:20:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 24 Oct 2023 00:20:16 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 24 Oct 2023 00:20:16 GMT
EXPOSE 8888
# Tue, 24 Oct 2023 00:20:16 GMT
VOLUME [/var/lib/chronograf]
# Tue, 24 Oct 2023 00:20:16 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 24 Oct 2023 00:20:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Oct 2023 00:20:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5352bf3aec614dde8ac36d38f28f5021eff4c2ff0226eb22dfa667f2b2add1`  
		Last Modified: Tue, 17 Oct 2023 01:33:20 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4048f49511dda4f4f68ff84317685f405a4090adcf74b1c9c7116e71ae80d30a`  
		Last Modified: Sat, 21 Oct 2023 02:35:44 GMT  
		Size: 284.7 KB (284698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6545ebb960dd3a534da359758d3fec7757e7866b3655ad8432156ab58b56bf56`  
		Last Modified: Tue, 24 Oct 2023 00:21:04 GMT  
		Size: 27.8 MB (27847599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28322186901948002f5674f518fd78626ce89862f988bcfbfe22b03a9868134`  
		Last Modified: Tue, 24 Oct 2023 00:20:58 GMT  
		Size: 12.3 KB (12268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d268d1b30ec9afb6cf8ac11fe77068afa5f6b2e2211c3e2861d51f122b8b5e07`  
		Last Modified: Tue, 24 Oct 2023 00:20:59 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c48929913d0bb1a8ca03b3dfcd0cfded77493e0142ff4fd446ca1f7bfbed9bd`  
		Last Modified: Tue, 24 Oct 2023 00:20:58 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:3f3d7fe26384875f3da735a5cfecc96c4c0d987ee7d8fb9007393e60eec4fa96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:1a461fbe3edab762b1d59bcedb52e0f8e6b0970978aaea196f8d2cee12c7dcaa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84100967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e1dc006b87ef469329f2f30f1c8ccf4a91484765e4f522eb5635326d033295b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:49 GMT
ADD file:fbd8521c24ed758023728505c18d7a0d6d101bc77fd772a4af9b65049b943864 in / 
# Wed, 01 Nov 2023 00:20:49 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:08:34 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 01 Nov 2023 01:08:34 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Wed, 01 Nov 2023 01:08:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 01 Nov 2023 01:08:43 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 01 Nov 2023 01:08:43 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 01 Nov 2023 01:08:43 GMT
EXPOSE 8888
# Wed, 01 Nov 2023 01:08:43 GMT
VOLUME [/var/lib/chronograf]
# Wed, 01 Nov 2023 01:08:43 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 01 Nov 2023 01:08:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Nov 2023 01:08:43 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:578acb154839e9d0034432e8f53756d6f53ba62cf8c7ea5218a2476bf5b58fc9`  
		Last Modified: Wed, 01 Nov 2023 00:25:30 GMT  
		Size: 29.1 MB (29149836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74552c3cf744ecac6301ccde01a6a900a075b6c630a9f40b8abe29dde4a3e0b3`  
		Last Modified: Wed, 01 Nov 2023 01:09:51 GMT  
		Size: 7.9 MB (7873082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805fc64ace298a45ceda26ee328a12efc77ee97c4ffe0005b9d92adaabe8eb8c`  
		Last Modified: Wed, 01 Nov 2023 01:09:56 GMT  
		Size: 47.1 MB (47053662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe49558d81938f5c83cf0c2775ce79b575abaa938b3593a68598c62e4c18664`  
		Last Modified: Wed, 01 Nov 2023 01:09:50 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:869439d87344d0d0f75a8ae7cc5e6268384d88f988b4e6f4e549c978eb57a8b7`  
		Last Modified: Wed, 01 Nov 2023 01:09:50 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4a93857ae7d9c3a84b65e983d1c77071a23c7b74179bfcb3fd25b12faa9c16`  
		Last Modified: Wed, 01 Nov 2023 01:09:50 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:f561842ea3ac1c45f50ae0d511db8fade073f7135618a809e6d934e166eefcb9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75920594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95853d742a1a56e274165274664fe8b599273b187265f004ab759cbccbb436dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:11 GMT
ADD file:da08fed31a161a2210fd920a1b5e43aa3f4199985cdeaa0d5d24c0a0f19044aa in / 
# Wed, 11 Oct 2023 17:42:11 GMT
CMD ["bash"]
# Tue, 24 Oct 2023 00:57:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 24 Oct 2023 00:57:28 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 24 Oct 2023 00:57:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 24 Oct 2023 00:57:39 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 24 Oct 2023 00:57:39 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 24 Oct 2023 00:57:39 GMT
EXPOSE 8888
# Tue, 24 Oct 2023 00:57:39 GMT
VOLUME [/var/lib/chronograf]
# Tue, 24 Oct 2023 00:57:39 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 24 Oct 2023 00:57:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Oct 2023 00:57:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2f11c34abc7b59f09b58bb6e2cf54f260f4b4142ecf8023a114e281ea4b532d1`  
		Last Modified: Wed, 11 Oct 2023 17:46:22 GMT  
		Size: 24.7 MB (24748925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d373ef288c1016255f23880fa193ed8c7b16d4316eb58a30fcd570f718deccd4`  
		Last Modified: Tue, 24 Oct 2023 00:57:55 GMT  
		Size: 6.5 MB (6497689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2639aee512dab0e2fe78d1a515ae90b96cc3d89f675da7730898afb2cf7a18`  
		Last Modified: Tue, 24 Oct 2023 00:58:00 GMT  
		Size: 44.6 MB (44649590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed879c5c9cd7cc45825042bf0c9e2eb2933605e0d70f4f07af5f3b304114cac2`  
		Last Modified: Tue, 24 Oct 2023 00:57:54 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5b56f84fc2d127783ba14e5ded545ee284891285786a7e6a2ff86302561930`  
		Last Modified: Tue, 24 Oct 2023 00:57:54 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6392494cbb507a347e77034033f4d60c98c65638650c7b64bc988008353e0b3e`  
		Last Modified: Tue, 24 Oct 2023 00:57:53 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:c9fe4efbd1d71455a6fa4b661b4d78e670d34f082c3d8b554c73d7e981f8addf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81627643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5475822bc23d4a7a3706572d7590da773f63f34429209a46f4e6e787f9465543`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Tue, 24 Oct 2023 00:39:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 24 Oct 2023 00:39:33 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 24 Oct 2023 00:39:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 24 Oct 2023 00:39:42 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 24 Oct 2023 00:39:42 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 24 Oct 2023 00:39:42 GMT
EXPOSE 8888
# Tue, 24 Oct 2023 00:39:42 GMT
VOLUME [/var/lib/chronograf]
# Tue, 24 Oct 2023 00:39:42 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 24 Oct 2023 00:39:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Oct 2023 00:39:42 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4cdcc7908019036cf9c3d001ab98e52b489a56b0cf84628701cdd5171f58ba0`  
		Last Modified: Tue, 24 Oct 2023 00:39:59 GMT  
		Size: 7.7 MB (7650123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8aa51a450f2913c77d18e427d6d96164c2512d6049b5deb2a55ac285fdf54bb`  
		Last Modified: Tue, 24 Oct 2023 00:40:04 GMT  
		Size: 44.8 MB (44773847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf898ad709c1a0f6df7a3686c89f054fcc8c37cf07f5e6331b8fd90b996e3188`  
		Last Modified: Tue, 24 Oct 2023 00:39:58 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcae01731a3dc25c2550dbbb256be4612a6daf965ea1a0a9e2f07357f994a5a8`  
		Last Modified: Tue, 24 Oct 2023 00:39:58 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a71d77cfe25f61f27d00798befe3934cd764f9d0e4af6328e313b3a86dd77c0`  
		Last Modified: Tue, 24 Oct 2023 00:39:58 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
