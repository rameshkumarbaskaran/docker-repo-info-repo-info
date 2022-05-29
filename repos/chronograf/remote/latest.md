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
