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
