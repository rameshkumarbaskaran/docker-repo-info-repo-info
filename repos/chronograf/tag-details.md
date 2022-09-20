<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.10`](#chronograf110)
-	[`chronograf:1.10-alpine`](#chronograf110-alpine)
-	[`chronograf:1.10.0`](#chronograf1100)
-	[`chronograf:1.10.0-alpine`](#chronograf1100-alpine)
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
$ docker pull chronograf@sha256:a3dd2ea5f162b90eb91cc50bf553ea801d93f2492d3ea3aa8d76f7dff8f922fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.10` - linux; amd64

```console
$ docker pull chronograf@sha256:0131956c284642aa5046d24151f4c62239af3e7dbfba6b344647c7d883d68c21
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.2 MB (81242412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6c386352e5d3d8acedc1b7778f7016879414197db6bd43b691ba41db62e1c3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 20 Sep 2022 20:21:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Sep 2022 20:21:58 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Tue, 20 Sep 2022 20:22:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2022 20:22:05 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 20:22:05 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 20:22:05 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 20:22:05 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 20:22:05 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 20 Sep 2022 20:22:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 20:22:06 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9912bf5b6c0d0a8c9f83f63b25e9d2594eba49ae7977f589f65cb3c6db68ee`  
		Last Modified: Tue, 20 Sep 2022 20:22:53 GMT  
		Size: 5.2 MB (5226757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5465fc1b879a85d93348bfabdfcdefbb0690206998bead3c44f8d6c22cd0d42a`  
		Last Modified: Tue, 20 Sep 2022 20:23:29 GMT  
		Size: 44.6 MB (44587136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb13e1bf85984003fc04f672635ce3823c659d7a0256ecb8f4bf05818263c11`  
		Last Modified: Tue, 20 Sep 2022 20:23:22 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b396867a07f1e6c1663ed3f2f1fce140e3f25d0e1b220ec844910e28d75a7dc`  
		Last Modified: Tue, 20 Sep 2022 20:23:22 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bc49be513cee5763ad65b584f9dc6dda843bd132432ee82a4e99cf3af6a830`  
		Last Modified: Tue, 20 Sep 2022 20:23:22 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:79e4d12c8da2c80c1328792badf1807180df7dbef40720ea463da2fed777f8a7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73550015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ae5272dc31511ca7d9e9afe9c9564399d22e051a16ac6eefec2a04b706ad94`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Sep 2022 03:42:37 GMT
ADD file:04b0c48a2d326e2ac4255df4a6165508f0d29d8a32147fb8df6bf9504b8f6b09 in / 
# Tue, 13 Sep 2022 03:42:37 GMT
CMD ["bash"]
# Tue, 20 Sep 2022 19:58:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Sep 2022 19:58:30 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Tue, 20 Sep 2022 19:58:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2022 19:58:39 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 19:58:39 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 19:58:39 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 19:58:40 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 19:58:40 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 20 Sep 2022 19:58:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 19:58:40 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:43caeee1782255456dd3403ae8e6ba191802c3deb004ca68ce0420b30368995d`  
		Last Modified: Tue, 13 Sep 2022 03:49:46 GMT  
		Size: 26.6 MB (26567059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:371e8fe2f90e5f8d831cf3f7cbbc761654bac2e0078454288e46daa25ca92aa6`  
		Last Modified: Tue, 20 Sep 2022 19:59:29 GMT  
		Size: 4.5 MB (4493863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7655c5f70f62ed9844235f2139e13943ed47e2e18d3e6a57588794ff8469d608`  
		Last Modified: Tue, 20 Sep 2022 20:00:09 GMT  
		Size: 42.5 MB (42464705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797f5e419755f2972a7ea1b04533c75828cd0f0d6d0083e5d6fc1306b535ae7b`  
		Last Modified: Tue, 20 Sep 2022 20:00:00 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19af8ef6ad740ae7176c22212522177658a7a875eccfea0805b43a0b14519159`  
		Last Modified: Tue, 20 Sep 2022 20:00:00 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39fd7a5c09df81dba19d7d2d9053523f2b5336666a25dbcfb3c213f33038a407`  
		Last Modified: Tue, 20 Sep 2022 20:00:00 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:2d278a81bdce18c2e4856e98c43f18ef469615b525738941cda2b0c82e552571
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77688043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6218e80f8ed5be7d1c6494fbc10078f150696170e47bda497fed1c68e5488fbf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 20 Sep 2022 20:44:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Sep 2022 20:44:45 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Tue, 20 Sep 2022 20:44:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2022 20:44:56 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 20:44:57 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 20:44:57 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 20:44:58 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 20:45:00 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 20 Sep 2022 20:45:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 20:45:01 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2c9f840ab139e2eb5a0f134343fb6c9aee8c40ccb2c7359ee1412e99709bab`  
		Last Modified: Tue, 20 Sep 2022 20:45:42 GMT  
		Size: 5.2 MB (5208924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d628c5293d653bd4c9205ddfd8c98fc75b857deb038ef7d8e01a56c7f418c1`  
		Last Modified: Tue, 20 Sep 2022 20:46:22 GMT  
		Size: 42.4 MB (42400486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c4c343bf0713eee3dd2a8dfc3c39fc0a46d4db3ea0a20e15becb09dbaea4a89`  
		Last Modified: Tue, 20 Sep 2022 20:46:16 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8142f6c5218c655f3290043a32dcf2b8bb613b403a7f8edcd4cdb9d73510d8`  
		Last Modified: Tue, 20 Sep 2022 20:46:16 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c97fc46bd891af9e06e3fa2d3e7880d632e0fb64dca9d47f457efa8a08078116`  
		Last Modified: Tue, 20 Sep 2022 20:46:15 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:10db860523fe5eebdf4890773b3e7f2e03aaa709bc7728a5acf0444b06f26217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:716811ca8465a91cf9ee2ec75857611e7859c0fbb9a2569ebc840720317be46e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30311121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46e472a1f7b448779d264ff1d5a2d3e0711a25c41260fbf237eecb091cbd66b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:17:08 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 20 Sep 2022 20:22:08 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Tue, 20 Sep 2022 20:22:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 20 Sep 2022 20:22:14 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 20:22:14 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 20:22:14 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 20:22:14 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 20:22:15 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 20 Sep 2022 20:22:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 20:22:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86aedf0b86f2f672427bd99edb4d53285ee3f072fdd5e4ea92fd315f1f9d2bb8`  
		Last Modified: Tue, 09 Aug 2022 18:18:07 GMT  
		Size: 284.6 KB (284571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ea195aa67f5544afe9744fdcb50f8426f7c9e78f1d2852eedf8a4f25abe5f3`  
		Last Modified: Tue, 20 Sep 2022 20:23:46 GMT  
		Size: 27.2 MB (27174514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6442c946b6fb9dbfb0fade5a61bacb47071521acdb42ff9cfc3c786f281099de`  
		Last Modified: Tue, 20 Sep 2022 20:23:41 GMT  
		Size: 12.3 KB (12260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dcf32ffd08f927f5984bcd48dce204c61e8a41cb17c10bbebe8ab5fdb8b441a`  
		Last Modified: Tue, 20 Sep 2022 20:23:41 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac10f24f91124d09ad041e5953607fa76cb06490cf6412aecbf309a0ab9317d`  
		Last Modified: Tue, 20 Sep 2022 20:23:41 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.10.0`

```console
$ docker pull chronograf@sha256:a3dd2ea5f162b90eb91cc50bf553ea801d93f2492d3ea3aa8d76f7dff8f922fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.10.0` - linux; amd64

```console
$ docker pull chronograf@sha256:0131956c284642aa5046d24151f4c62239af3e7dbfba6b344647c7d883d68c21
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.2 MB (81242412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6c386352e5d3d8acedc1b7778f7016879414197db6bd43b691ba41db62e1c3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 20 Sep 2022 20:21:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Sep 2022 20:21:58 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Tue, 20 Sep 2022 20:22:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2022 20:22:05 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 20:22:05 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 20:22:05 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 20:22:05 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 20:22:05 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 20 Sep 2022 20:22:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 20:22:06 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9912bf5b6c0d0a8c9f83f63b25e9d2594eba49ae7977f589f65cb3c6db68ee`  
		Last Modified: Tue, 20 Sep 2022 20:22:53 GMT  
		Size: 5.2 MB (5226757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5465fc1b879a85d93348bfabdfcdefbb0690206998bead3c44f8d6c22cd0d42a`  
		Last Modified: Tue, 20 Sep 2022 20:23:29 GMT  
		Size: 44.6 MB (44587136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb13e1bf85984003fc04f672635ce3823c659d7a0256ecb8f4bf05818263c11`  
		Last Modified: Tue, 20 Sep 2022 20:23:22 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b396867a07f1e6c1663ed3f2f1fce140e3f25d0e1b220ec844910e28d75a7dc`  
		Last Modified: Tue, 20 Sep 2022 20:23:22 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bc49be513cee5763ad65b584f9dc6dda843bd132432ee82a4e99cf3af6a830`  
		Last Modified: Tue, 20 Sep 2022 20:23:22 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10.0` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:79e4d12c8da2c80c1328792badf1807180df7dbef40720ea463da2fed777f8a7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73550015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ae5272dc31511ca7d9e9afe9c9564399d22e051a16ac6eefec2a04b706ad94`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Sep 2022 03:42:37 GMT
ADD file:04b0c48a2d326e2ac4255df4a6165508f0d29d8a32147fb8df6bf9504b8f6b09 in / 
# Tue, 13 Sep 2022 03:42:37 GMT
CMD ["bash"]
# Tue, 20 Sep 2022 19:58:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Sep 2022 19:58:30 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Tue, 20 Sep 2022 19:58:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2022 19:58:39 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 19:58:39 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 19:58:39 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 19:58:40 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 19:58:40 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 20 Sep 2022 19:58:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 19:58:40 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:43caeee1782255456dd3403ae8e6ba191802c3deb004ca68ce0420b30368995d`  
		Last Modified: Tue, 13 Sep 2022 03:49:46 GMT  
		Size: 26.6 MB (26567059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:371e8fe2f90e5f8d831cf3f7cbbc761654bac2e0078454288e46daa25ca92aa6`  
		Last Modified: Tue, 20 Sep 2022 19:59:29 GMT  
		Size: 4.5 MB (4493863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7655c5f70f62ed9844235f2139e13943ed47e2e18d3e6a57588794ff8469d608`  
		Last Modified: Tue, 20 Sep 2022 20:00:09 GMT  
		Size: 42.5 MB (42464705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797f5e419755f2972a7ea1b04533c75828cd0f0d6d0083e5d6fc1306b535ae7b`  
		Last Modified: Tue, 20 Sep 2022 20:00:00 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19af8ef6ad740ae7176c22212522177658a7a875eccfea0805b43a0b14519159`  
		Last Modified: Tue, 20 Sep 2022 20:00:00 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39fd7a5c09df81dba19d7d2d9053523f2b5336666a25dbcfb3c213f33038a407`  
		Last Modified: Tue, 20 Sep 2022 20:00:00 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10.0` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:2d278a81bdce18c2e4856e98c43f18ef469615b525738941cda2b0c82e552571
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77688043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6218e80f8ed5be7d1c6494fbc10078f150696170e47bda497fed1c68e5488fbf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 20 Sep 2022 20:44:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Sep 2022 20:44:45 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Tue, 20 Sep 2022 20:44:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2022 20:44:56 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 20:44:57 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 20:44:57 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 20:44:58 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 20:45:00 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 20 Sep 2022 20:45:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 20:45:01 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2c9f840ab139e2eb5a0f134343fb6c9aee8c40ccb2c7359ee1412e99709bab`  
		Last Modified: Tue, 20 Sep 2022 20:45:42 GMT  
		Size: 5.2 MB (5208924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d628c5293d653bd4c9205ddfd8c98fc75b857deb038ef7d8e01a56c7f418c1`  
		Last Modified: Tue, 20 Sep 2022 20:46:22 GMT  
		Size: 42.4 MB (42400486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c4c343bf0713eee3dd2a8dfc3c39fc0a46d4db3ea0a20e15becb09dbaea4a89`  
		Last Modified: Tue, 20 Sep 2022 20:46:16 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8142f6c5218c655f3290043a32dcf2b8bb613b403a7f8edcd4cdb9d73510d8`  
		Last Modified: Tue, 20 Sep 2022 20:46:16 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c97fc46bd891af9e06e3fa2d3e7880d632e0fb64dca9d47f457efa8a08078116`  
		Last Modified: Tue, 20 Sep 2022 20:46:15 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.10.0-alpine`

```console
$ docker pull chronograf@sha256:10db860523fe5eebdf4890773b3e7f2e03aaa709bc7728a5acf0444b06f26217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.10.0-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:716811ca8465a91cf9ee2ec75857611e7859c0fbb9a2569ebc840720317be46e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30311121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46e472a1f7b448779d264ff1d5a2d3e0711a25c41260fbf237eecb091cbd66b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:17:08 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 20 Sep 2022 20:22:08 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Tue, 20 Sep 2022 20:22:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 20 Sep 2022 20:22:14 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 20:22:14 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 20:22:14 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 20:22:14 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 20:22:15 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 20 Sep 2022 20:22:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 20:22:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86aedf0b86f2f672427bd99edb4d53285ee3f072fdd5e4ea92fd315f1f9d2bb8`  
		Last Modified: Tue, 09 Aug 2022 18:18:07 GMT  
		Size: 284.6 KB (284571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ea195aa67f5544afe9744fdcb50f8426f7c9e78f1d2852eedf8a4f25abe5f3`  
		Last Modified: Tue, 20 Sep 2022 20:23:46 GMT  
		Size: 27.2 MB (27174514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6442c946b6fb9dbfb0fade5a61bacb47071521acdb42ff9cfc3c786f281099de`  
		Last Modified: Tue, 20 Sep 2022 20:23:41 GMT  
		Size: 12.3 KB (12260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dcf32ffd08f927f5984bcd48dce204c61e8a41cb17c10bbebe8ab5fdb8b441a`  
		Last Modified: Tue, 20 Sep 2022 20:23:41 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac10f24f91124d09ad041e5953607fa76cb06490cf6412aecbf309a0ab9317d`  
		Last Modified: Tue, 20 Sep 2022 20:23:41 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:22d529fa331be35eb210c5073642e5a7c0c1745867e9c930603e31c77494e392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7` - linux; amd64

```console
$ docker pull chronograf@sha256:d4fc995ab43dc980fde76e69903f1e7ff5bc878562ac72f0effb01c21970fc39
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70584232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b71a417eed3c6b8945f33c176113cdf78a76f8ca01ee83e54caead0e1325d4c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 20 Sep 2022 20:21:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Sep 2022 20:21:10 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 20 Sep 2022 20:21:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2022 20:21:19 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 20:21:19 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 20:21:19 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 20:21:19 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 20:21:19 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 20 Sep 2022 20:21:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 20:21:20 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fd61de5a1f4038cdacc54b6da13d30688f3110745089b278d74b40637374e9`  
		Last Modified: Tue, 20 Sep 2022 20:22:37 GMT  
		Size: 4.4 MB (4418266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d4b17ce7c02eeb425f2748e43546145eb3aa07d07d4285d7132738ea8460b89`  
		Last Modified: Tue, 20 Sep 2022 20:22:41 GMT  
		Size: 34.7 MB (34737452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ded8123f40f6e2139bdd178422d6cfec96a45042b0cb152a177067ddc479073`  
		Last Modified: Tue, 20 Sep 2022 20:22:37 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d796f65b4868b3a4c9b3e367b950ea3c05a297d718aec4fe8beb925ec69edc52`  
		Last Modified: Tue, 20 Sep 2022 20:22:37 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72071f4621e392cda688d9ecf9ea6eeb6ecb64a163d6c24327afa3203a1ad201`  
		Last Modified: Tue, 20 Sep 2022 20:22:37 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:1114a46928f61905e1249cebc29c782b341888186c83df0d6875ec882ec359ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63408404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08e7d6df76d72a374a5d51d44f89924730c03972af1c63e0ec88d8045b93bf1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Sep 2022 03:42:37 GMT
ADD file:04b0c48a2d326e2ac4255df4a6165508f0d29d8a32147fb8df6bf9504b8f6b09 in / 
# Tue, 13 Sep 2022 03:42:37 GMT
CMD ["bash"]
# Tue, 20 Sep 2022 19:57:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Sep 2022 19:57:34 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 20 Sep 2022 19:57:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2022 19:57:45 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 19:57:45 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 19:57:45 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 19:57:45 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 19:57:45 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 20 Sep 2022 19:57:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 19:57:46 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:43caeee1782255456dd3403ae8e6ba191802c3deb004ca68ce0420b30368995d`  
		Last Modified: Tue, 13 Sep 2022 03:49:46 GMT  
		Size: 26.6 MB (26567059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093d0806b1b00fed04f60ddae7ffb9f2875976771a9fdbbd29c3572045e0b70a`  
		Last Modified: Tue, 20 Sep 2022 19:59:11 GMT  
		Size: 3.7 MB (3719672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a7cb99ef901fea60bf8123428d997749e025f68db06d58b5407a9ff6108b7a`  
		Last Modified: Tue, 20 Sep 2022 19:59:17 GMT  
		Size: 33.1 MB (33097276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117a602903aefdb992da09cbc0c63f5542aa3150312a8934c7dc5672807767e7`  
		Last Modified: Tue, 20 Sep 2022 19:59:10 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6e8f61809053da18006863b7abd66f0bf38442ee29abcd4ee95e130d8983e2`  
		Last Modified: Tue, 20 Sep 2022 19:59:10 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c77cc1ab386fb9e84ce17d0e9ecf9530735d8c8da6c941980dd97b8d7be316`  
		Last Modified: Tue, 20 Sep 2022 19:59:10 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:915c88870e827f61e8f106a0fd37129909cc70ec83c666980bb29b3797bfe809
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67526059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89e4e6f18701641a9de3503ebf2042eb130d2190d520a7e4ec8cf92bffaa39d6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 20 Sep 2022 20:43:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Sep 2022 20:43:30 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 20 Sep 2022 20:43:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2022 20:43:41 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 20:43:42 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 20:43:42 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 20:43:43 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 20:43:45 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 20 Sep 2022 20:43:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 20:43:46 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0509b5418cb89f7fb0e8d138f56e1265b9b9c44d5ba7eb545023576ba1bb261d`  
		Last Modified: Tue, 20 Sep 2022 20:45:27 GMT  
		Size: 4.2 MB (4211191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc0000d7a1e768fc537d7dc6c16d64387e8c08cc95eae360610dabd1476b96c`  
		Last Modified: Tue, 20 Sep 2022 20:45:31 GMT  
		Size: 33.2 MB (33236231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466d8be1e5c283fa6d7968c8c11f9c8b1f588a5bff99570ccd76b55270824383`  
		Last Modified: Tue, 20 Sep 2022 20:45:27 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59143947e6c39f018bed9e73c6dbbabe5dbd6a6525dc6181dc8b0497c41171e9`  
		Last Modified: Tue, 20 Sep 2022 20:45:27 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51342a759293c7afd02bd86079a93b731376398854ca7cec4c90377d924761bc`  
		Last Modified: Tue, 20 Sep 2022 20:45:26 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:fea4948a9d212c423a391a04a0fa1a744bab2201b04f25d28a664324916f2166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:6e99be2a7bac5d79785429c530f776f1b9c4962f98ca89eba9da3accc2e0149b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22693411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613fc9f1aee33747b3623b95a2c4e433e694a02bf99b2603842cad9cd95350eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:17:08 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 09 Aug 2022 18:17:18 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 09 Aug 2022 18:17:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 09 Aug 2022 18:17:23 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 09 Aug 2022 18:17:23 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 09 Aug 2022 18:17:23 GMT
EXPOSE 8888
# Tue, 09 Aug 2022 18:17:23 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Aug 2022 18:17:23 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 09 Aug 2022 18:17:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Aug 2022 18:17:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86aedf0b86f2f672427bd99edb4d53285ee3f072fdd5e4ea92fd315f1f9d2bb8`  
		Last Modified: Tue, 09 Aug 2022 18:18:07 GMT  
		Size: 284.6 KB (284571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d588c7a740f6a0231b7e4eef9c215c7d86c3ee2c7629f86608c0da729d296b4`  
		Last Modified: Tue, 09 Aug 2022 18:18:23 GMT  
		Size: 19.6 MB (19556805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2285853c8534cea7724c2b4e7c863c0ca3077cea5440d2ab2a1057b3b2ae40`  
		Last Modified: Tue, 09 Aug 2022 18:18:20 GMT  
		Size: 12.3 KB (12261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5295b9363991edc0b91ca76c2202f61857fa2130afd1918b477a969afba18311`  
		Last Modified: Tue, 09 Aug 2022 18:18:20 GMT  
		Size: 11.9 KB (11894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961531905b194ca826eec578c91b790b266e5c429a5969e7afb0a17a674fee7c`  
		Last Modified: Tue, 09 Aug 2022 18:18:20 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:22d529fa331be35eb210c5073642e5a7c0c1745867e9c930603e31c77494e392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7.17` - linux; amd64

```console
$ docker pull chronograf@sha256:d4fc995ab43dc980fde76e69903f1e7ff5bc878562ac72f0effb01c21970fc39
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70584232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b71a417eed3c6b8945f33c176113cdf78a76f8ca01ee83e54caead0e1325d4c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 20 Sep 2022 20:21:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Sep 2022 20:21:10 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 20 Sep 2022 20:21:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2022 20:21:19 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 20:21:19 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 20:21:19 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 20:21:19 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 20:21:19 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 20 Sep 2022 20:21:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 20:21:20 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fd61de5a1f4038cdacc54b6da13d30688f3110745089b278d74b40637374e9`  
		Last Modified: Tue, 20 Sep 2022 20:22:37 GMT  
		Size: 4.4 MB (4418266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d4b17ce7c02eeb425f2748e43546145eb3aa07d07d4285d7132738ea8460b89`  
		Last Modified: Tue, 20 Sep 2022 20:22:41 GMT  
		Size: 34.7 MB (34737452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ded8123f40f6e2139bdd178422d6cfec96a45042b0cb152a177067ddc479073`  
		Last Modified: Tue, 20 Sep 2022 20:22:37 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d796f65b4868b3a4c9b3e367b950ea3c05a297d718aec4fe8beb925ec69edc52`  
		Last Modified: Tue, 20 Sep 2022 20:22:37 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72071f4621e392cda688d9ecf9ea6eeb6ecb64a163d6c24327afa3203a1ad201`  
		Last Modified: Tue, 20 Sep 2022 20:22:37 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:1114a46928f61905e1249cebc29c782b341888186c83df0d6875ec882ec359ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63408404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08e7d6df76d72a374a5d51d44f89924730c03972af1c63e0ec88d8045b93bf1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Sep 2022 03:42:37 GMT
ADD file:04b0c48a2d326e2ac4255df4a6165508f0d29d8a32147fb8df6bf9504b8f6b09 in / 
# Tue, 13 Sep 2022 03:42:37 GMT
CMD ["bash"]
# Tue, 20 Sep 2022 19:57:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Sep 2022 19:57:34 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 20 Sep 2022 19:57:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2022 19:57:45 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 19:57:45 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 19:57:45 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 19:57:45 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 19:57:45 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 20 Sep 2022 19:57:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 19:57:46 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:43caeee1782255456dd3403ae8e6ba191802c3deb004ca68ce0420b30368995d`  
		Last Modified: Tue, 13 Sep 2022 03:49:46 GMT  
		Size: 26.6 MB (26567059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093d0806b1b00fed04f60ddae7ffb9f2875976771a9fdbbd29c3572045e0b70a`  
		Last Modified: Tue, 20 Sep 2022 19:59:11 GMT  
		Size: 3.7 MB (3719672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a7cb99ef901fea60bf8123428d997749e025f68db06d58b5407a9ff6108b7a`  
		Last Modified: Tue, 20 Sep 2022 19:59:17 GMT  
		Size: 33.1 MB (33097276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117a602903aefdb992da09cbc0c63f5542aa3150312a8934c7dc5672807767e7`  
		Last Modified: Tue, 20 Sep 2022 19:59:10 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6e8f61809053da18006863b7abd66f0bf38442ee29abcd4ee95e130d8983e2`  
		Last Modified: Tue, 20 Sep 2022 19:59:10 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c77cc1ab386fb9e84ce17d0e9ecf9530735d8c8da6c941980dd97b8d7be316`  
		Last Modified: Tue, 20 Sep 2022 19:59:10 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:915c88870e827f61e8f106a0fd37129909cc70ec83c666980bb29b3797bfe809
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67526059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89e4e6f18701641a9de3503ebf2042eb130d2190d520a7e4ec8cf92bffaa39d6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 20 Sep 2022 20:43:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Sep 2022 20:43:30 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 20 Sep 2022 20:43:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2022 20:43:41 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 20:43:42 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 20:43:42 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 20:43:43 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 20:43:45 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 20 Sep 2022 20:43:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 20:43:46 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0509b5418cb89f7fb0e8d138f56e1265b9b9c44d5ba7eb545023576ba1bb261d`  
		Last Modified: Tue, 20 Sep 2022 20:45:27 GMT  
		Size: 4.2 MB (4211191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc0000d7a1e768fc537d7dc6c16d64387e8c08cc95eae360610dabd1476b96c`  
		Last Modified: Tue, 20 Sep 2022 20:45:31 GMT  
		Size: 33.2 MB (33236231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466d8be1e5c283fa6d7968c8c11f9c8b1f588a5bff99570ccd76b55270824383`  
		Last Modified: Tue, 20 Sep 2022 20:45:27 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59143947e6c39f018bed9e73c6dbbabe5dbd6a6525dc6181dc8b0497c41171e9`  
		Last Modified: Tue, 20 Sep 2022 20:45:27 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51342a759293c7afd02bd86079a93b731376398854ca7cec4c90377d924761bc`  
		Last Modified: Tue, 20 Sep 2022 20:45:26 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:fea4948a9d212c423a391a04a0fa1a744bab2201b04f25d28a664324916f2166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:6e99be2a7bac5d79785429c530f776f1b9c4962f98ca89eba9da3accc2e0149b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22693411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613fc9f1aee33747b3623b95a2c4e433e694a02bf99b2603842cad9cd95350eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:17:08 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 09 Aug 2022 18:17:18 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 09 Aug 2022 18:17:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 09 Aug 2022 18:17:23 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 09 Aug 2022 18:17:23 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 09 Aug 2022 18:17:23 GMT
EXPOSE 8888
# Tue, 09 Aug 2022 18:17:23 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Aug 2022 18:17:23 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 09 Aug 2022 18:17:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Aug 2022 18:17:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86aedf0b86f2f672427bd99edb4d53285ee3f072fdd5e4ea92fd315f1f9d2bb8`  
		Last Modified: Tue, 09 Aug 2022 18:18:07 GMT  
		Size: 284.6 KB (284571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d588c7a740f6a0231b7e4eef9c215c7d86c3ee2c7629f86608c0da729d296b4`  
		Last Modified: Tue, 09 Aug 2022 18:18:23 GMT  
		Size: 19.6 MB (19556805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2285853c8534cea7724c2b4e7c863c0ca3077cea5440d2ab2a1057b3b2ae40`  
		Last Modified: Tue, 09 Aug 2022 18:18:20 GMT  
		Size: 12.3 KB (12261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5295b9363991edc0b91ca76c2202f61857fa2130afd1918b477a969afba18311`  
		Last Modified: Tue, 09 Aug 2022 18:18:20 GMT  
		Size: 11.9 KB (11894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961531905b194ca826eec578c91b790b266e5c429a5969e7afb0a17a674fee7c`  
		Last Modified: Tue, 09 Aug 2022 18:18:20 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:5c16b82a4754e616e4de8a9fa06b26ff68ddb702bb9db3834c6ba66c5162bf8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8` - linux; amd64

```console
$ docker pull chronograf@sha256:2b3d294298fe9a8ee83c5e01a1817489aebd1188a227da1ffaa3516632216069
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71234152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f35393ef903f1ffd2ca4858a879e4734b2f24ac99d9fa3cdd8b038212517126`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 20 Sep 2022 20:21:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Sep 2022 20:21:33 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 20 Sep 2022 20:21:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2022 20:21:39 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 20:21:39 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 20:21:39 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 20:21:39 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 20:21:40 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 20 Sep 2022 20:21:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 20:21:40 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9912bf5b6c0d0a8c9f83f63b25e9d2594eba49ae7977f589f65cb3c6db68ee`  
		Last Modified: Tue, 20 Sep 2022 20:22:53 GMT  
		Size: 5.2 MB (5226757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee3ff3c6a1c52657ad4dde45705a73f429be88cc5b6db147420452c72f62df7`  
		Last Modified: Tue, 20 Sep 2022 20:22:57 GMT  
		Size: 34.6 MB (34578879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a73ee43124d2b0639702f98d659ae1eebb5c39681050a3d53d76373c67b390`  
		Last Modified: Tue, 20 Sep 2022 20:22:52 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de69ead3ae8eb920e459fbe639f0029c1d746145f8c5a569c8a034ded08a5d30`  
		Last Modified: Tue, 20 Sep 2022 20:22:52 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220ca2357529bb81f6a11ef219baf2813d5e05281c27d6887652ba267811a597`  
		Last Modified: Tue, 20 Sep 2022 20:22:52 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:c9419750a575e22b254a60c9a5b781ce24fb43d2133466c1ddef082ca3337e30
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63835736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e410f1d387370b7de7ad21e1bfa8e2ab5e224f8da79ae2d9d3ee86a2da497942`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Sep 2022 03:42:37 GMT
ADD file:04b0c48a2d326e2ac4255df4a6165508f0d29d8a32147fb8df6bf9504b8f6b09 in / 
# Tue, 13 Sep 2022 03:42:37 GMT
CMD ["bash"]
# Tue, 20 Sep 2022 19:58:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Sep 2022 19:58:01 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 20 Sep 2022 19:58:09 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2022 19:58:09 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 19:58:10 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 19:58:10 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 19:58:10 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 19:58:10 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 20 Sep 2022 19:58:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 19:58:10 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:43caeee1782255456dd3403ae8e6ba191802c3deb004ca68ce0420b30368995d`  
		Last Modified: Tue, 13 Sep 2022 03:49:46 GMT  
		Size: 26.6 MB (26567059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:371e8fe2f90e5f8d831cf3f7cbbc761654bac2e0078454288e46daa25ca92aa6`  
		Last Modified: Tue, 20 Sep 2022 19:59:29 GMT  
		Size: 4.5 MB (4493863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d88adf39df63a8b444562eb211b3fd3d22adf0e5366a247084b9d2bbfa682d9`  
		Last Modified: Tue, 20 Sep 2022 19:59:34 GMT  
		Size: 32.8 MB (32750413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04897827f95a6ea7c96c483b413df55f615ce4f84639ca839526fd351406291`  
		Last Modified: Tue, 20 Sep 2022 19:59:28 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2ba90f67c7c8dc09cf962b662d64a49f1eaf4935c56893bafcd0ea88e3bf0f`  
		Last Modified: Tue, 20 Sep 2022 19:59:28 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d14d4565258862598ded0a78dc3caf8a245ed2b7e8ebcea0454bc1c66091971`  
		Last Modified: Tue, 20 Sep 2022 19:59:28 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:cb272d5c2a85e403a317bd04f35a0ef6fd427dc81760d455c389f90b67987bd4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67715742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c091042c26231fe338baea23d28f863bd32ae971ca72d972ca89e4b749026f71`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 20 Sep 2022 20:44:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Sep 2022 20:44:03 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 20 Sep 2022 20:44:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2022 20:44:13 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 20:44:14 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 20:44:14 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 20:44:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 20:44:17 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 20 Sep 2022 20:44:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 20:44:18 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2c9f840ab139e2eb5a0f134343fb6c9aee8c40ccb2c7359ee1412e99709bab`  
		Last Modified: Tue, 20 Sep 2022 20:45:42 GMT  
		Size: 5.2 MB (5208924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:121226a9d1aa0b0f9798d0497c7219c0d2e3a67ceae63ace0f61551b7e986152`  
		Last Modified: Tue, 20 Sep 2022 20:45:46 GMT  
		Size: 32.4 MB (32428185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d65a56653c9a6aa234cba1100ccc15f8b5122fd1b66c154fa791ead30fe30d2`  
		Last Modified: Tue, 20 Sep 2022 20:45:41 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d30ba3db2ce0436c2a051e8ce36c6cd16fb811e028d054bf6fdb4b0209f607b`  
		Last Modified: Tue, 20 Sep 2022 20:45:41 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f1ad6500d4ae2126ac3fe00d19942a87f99be99d9bdf8c5fa758dec3725d84`  
		Last Modified: Tue, 20 Sep 2022 20:45:41 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:e21c2df83074058f591e400db598e2f2e0db991c065b382002f19a57036d65b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:4fbff7c953dd88ff517c74a639c8fab663fe9365b302d1e6414bea67cb3a79a0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22340814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e17e2be70c7462109bc2188a05c987ba18caac5fdbe12032d9b157b5e466809`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:17:08 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 09 Aug 2022 18:17:28 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 09 Aug 2022 18:17:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 09 Aug 2022 18:17:33 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 09 Aug 2022 18:17:33 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 09 Aug 2022 18:17:33 GMT
EXPOSE 8888
# Tue, 09 Aug 2022 18:17:33 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Aug 2022 18:17:33 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 09 Aug 2022 18:17:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Aug 2022 18:17:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86aedf0b86f2f672427bd99edb4d53285ee3f072fdd5e4ea92fd315f1f9d2bb8`  
		Last Modified: Tue, 09 Aug 2022 18:18:07 GMT  
		Size: 284.6 KB (284571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf91dd373292f741fe4469ec76e73a80420fbc2da4bdc8d4d3e2f14c4cca7607`  
		Last Modified: Tue, 09 Aug 2022 18:18:37 GMT  
		Size: 19.2 MB (19204195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686071ec84727f65defe0a32dc8401552bc4e3d88c84a6e35829f0da6fb5db30`  
		Last Modified: Tue, 09 Aug 2022 18:18:33 GMT  
		Size: 12.3 KB (12268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a1a0c949f66345474da08be2eb9ad15e11a935b421d5d4d52e509861a46bf7`  
		Last Modified: Tue, 09 Aug 2022 18:18:33 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae01956999004409f2013989dc7bc0d92b2ca8b9079486ad1eb081d55e5b6ae7`  
		Last Modified: Tue, 09 Aug 2022 18:18:33 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:5c16b82a4754e616e4de8a9fa06b26ff68ddb702bb9db3834c6ba66c5162bf8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8.10` - linux; amd64

```console
$ docker pull chronograf@sha256:2b3d294298fe9a8ee83c5e01a1817489aebd1188a227da1ffaa3516632216069
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71234152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f35393ef903f1ffd2ca4858a879e4734b2f24ac99d9fa3cdd8b038212517126`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 20 Sep 2022 20:21:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Sep 2022 20:21:33 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 20 Sep 2022 20:21:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2022 20:21:39 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 20:21:39 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 20:21:39 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 20:21:39 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 20:21:40 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 20 Sep 2022 20:21:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 20:21:40 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9912bf5b6c0d0a8c9f83f63b25e9d2594eba49ae7977f589f65cb3c6db68ee`  
		Last Modified: Tue, 20 Sep 2022 20:22:53 GMT  
		Size: 5.2 MB (5226757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee3ff3c6a1c52657ad4dde45705a73f429be88cc5b6db147420452c72f62df7`  
		Last Modified: Tue, 20 Sep 2022 20:22:57 GMT  
		Size: 34.6 MB (34578879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a73ee43124d2b0639702f98d659ae1eebb5c39681050a3d53d76373c67b390`  
		Last Modified: Tue, 20 Sep 2022 20:22:52 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de69ead3ae8eb920e459fbe639f0029c1d746145f8c5a569c8a034ded08a5d30`  
		Last Modified: Tue, 20 Sep 2022 20:22:52 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220ca2357529bb81f6a11ef219baf2813d5e05281c27d6887652ba267811a597`  
		Last Modified: Tue, 20 Sep 2022 20:22:52 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:c9419750a575e22b254a60c9a5b781ce24fb43d2133466c1ddef082ca3337e30
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63835736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e410f1d387370b7de7ad21e1bfa8e2ab5e224f8da79ae2d9d3ee86a2da497942`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Sep 2022 03:42:37 GMT
ADD file:04b0c48a2d326e2ac4255df4a6165508f0d29d8a32147fb8df6bf9504b8f6b09 in / 
# Tue, 13 Sep 2022 03:42:37 GMT
CMD ["bash"]
# Tue, 20 Sep 2022 19:58:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Sep 2022 19:58:01 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 20 Sep 2022 19:58:09 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2022 19:58:09 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 19:58:10 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 19:58:10 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 19:58:10 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 19:58:10 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 20 Sep 2022 19:58:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 19:58:10 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:43caeee1782255456dd3403ae8e6ba191802c3deb004ca68ce0420b30368995d`  
		Last Modified: Tue, 13 Sep 2022 03:49:46 GMT  
		Size: 26.6 MB (26567059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:371e8fe2f90e5f8d831cf3f7cbbc761654bac2e0078454288e46daa25ca92aa6`  
		Last Modified: Tue, 20 Sep 2022 19:59:29 GMT  
		Size: 4.5 MB (4493863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d88adf39df63a8b444562eb211b3fd3d22adf0e5366a247084b9d2bbfa682d9`  
		Last Modified: Tue, 20 Sep 2022 19:59:34 GMT  
		Size: 32.8 MB (32750413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04897827f95a6ea7c96c483b413df55f615ce4f84639ca839526fd351406291`  
		Last Modified: Tue, 20 Sep 2022 19:59:28 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2ba90f67c7c8dc09cf962b662d64a49f1eaf4935c56893bafcd0ea88e3bf0f`  
		Last Modified: Tue, 20 Sep 2022 19:59:28 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d14d4565258862598ded0a78dc3caf8a245ed2b7e8ebcea0454bc1c66091971`  
		Last Modified: Tue, 20 Sep 2022 19:59:28 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:cb272d5c2a85e403a317bd04f35a0ef6fd427dc81760d455c389f90b67987bd4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67715742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c091042c26231fe338baea23d28f863bd32ae971ca72d972ca89e4b749026f71`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 20 Sep 2022 20:44:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Sep 2022 20:44:03 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 20 Sep 2022 20:44:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2022 20:44:13 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 20:44:14 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 20:44:14 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 20:44:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 20:44:17 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 20 Sep 2022 20:44:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 20:44:18 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2c9f840ab139e2eb5a0f134343fb6c9aee8c40ccb2c7359ee1412e99709bab`  
		Last Modified: Tue, 20 Sep 2022 20:45:42 GMT  
		Size: 5.2 MB (5208924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:121226a9d1aa0b0f9798d0497c7219c0d2e3a67ceae63ace0f61551b7e986152`  
		Last Modified: Tue, 20 Sep 2022 20:45:46 GMT  
		Size: 32.4 MB (32428185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d65a56653c9a6aa234cba1100ccc15f8b5122fd1b66c154fa791ead30fe30d2`  
		Last Modified: Tue, 20 Sep 2022 20:45:41 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d30ba3db2ce0436c2a051e8ce36c6cd16fb811e028d054bf6fdb4b0209f607b`  
		Last Modified: Tue, 20 Sep 2022 20:45:41 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f1ad6500d4ae2126ac3fe00d19942a87f99be99d9bdf8c5fa758dec3725d84`  
		Last Modified: Tue, 20 Sep 2022 20:45:41 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:e21c2df83074058f591e400db598e2f2e0db991c065b382002f19a57036d65b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:4fbff7c953dd88ff517c74a639c8fab663fe9365b302d1e6414bea67cb3a79a0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22340814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e17e2be70c7462109bc2188a05c987ba18caac5fdbe12032d9b157b5e466809`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:17:08 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 09 Aug 2022 18:17:28 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 09 Aug 2022 18:17:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 09 Aug 2022 18:17:33 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 09 Aug 2022 18:17:33 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 09 Aug 2022 18:17:33 GMT
EXPOSE 8888
# Tue, 09 Aug 2022 18:17:33 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Aug 2022 18:17:33 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 09 Aug 2022 18:17:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Aug 2022 18:17:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86aedf0b86f2f672427bd99edb4d53285ee3f072fdd5e4ea92fd315f1f9d2bb8`  
		Last Modified: Tue, 09 Aug 2022 18:18:07 GMT  
		Size: 284.6 KB (284571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf91dd373292f741fe4469ec76e73a80420fbc2da4bdc8d4d3e2f14c4cca7607`  
		Last Modified: Tue, 09 Aug 2022 18:18:37 GMT  
		Size: 19.2 MB (19204195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686071ec84727f65defe0a32dc8401552bc4e3d88c84a6e35829f0da6fb5db30`  
		Last Modified: Tue, 09 Aug 2022 18:18:33 GMT  
		Size: 12.3 KB (12268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a1a0c949f66345474da08be2eb9ad15e11a935b421d5d4d52e509861a46bf7`  
		Last Modified: Tue, 09 Aug 2022 18:18:33 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae01956999004409f2013989dc7bc0d92b2ca8b9079486ad1eb081d55e5b6ae7`  
		Last Modified: Tue, 09 Aug 2022 18:18:33 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:6bcdd97ec79070cdc81bebfe9b516ca03d826a8efdd2c9ed6b56b0aa5746e67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9` - linux; amd64

```console
$ docker pull chronograf@sha256:694e8bab6ae3f4dd646af688f4c790cac097f7bfbebedc107036e276e9c12bec
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71881717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3ca8d13890b91f922f80a688845b9bdd913e1e6cdfb009e36cc8a7869eaa54`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 20 Sep 2022 20:21:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Sep 2022 20:21:44 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 20 Sep 2022 20:21:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2022 20:21:52 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 20:21:52 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 20:21:52 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 20:21:52 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 20:21:52 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 20 Sep 2022 20:21:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 20:21:52 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9912bf5b6c0d0a8c9f83f63b25e9d2594eba49ae7977f589f65cb3c6db68ee`  
		Last Modified: Tue, 20 Sep 2022 20:22:53 GMT  
		Size: 5.2 MB (5226757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f858f98c2fc7b84ac4e4e724df28aa1d1693d5ba7452b2101f450c2e1b1c8d`  
		Last Modified: Tue, 20 Sep 2022 20:23:12 GMT  
		Size: 35.2 MB (35226456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815a8049be7c95fbba36555b3d74548442f444aa4d031f194455721d8dbd735a`  
		Last Modified: Tue, 20 Sep 2022 20:23:07 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94818bc4ad21b22a74a469b5fd43191967deba02360d18d9dc4a3677e445db4b`  
		Last Modified: Tue, 20 Sep 2022 20:23:07 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34cc276b85549aa84243a3588344e5737bcea8a1cdd1c137e18f71f679ca0a1`  
		Last Modified: Tue, 20 Sep 2022 20:23:07 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:7146036f24aa9e1e166b756cda4e34568fcfb1e98a50bd362c4301886a9656fc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64611936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:728f159b2f0171718e9a66f3f63787e135caf15f3be015179446e3f16f367e09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Sep 2022 03:42:37 GMT
ADD file:04b0c48a2d326e2ac4255df4a6165508f0d29d8a32147fb8df6bf9504b8f6b09 in / 
# Tue, 13 Sep 2022 03:42:37 GMT
CMD ["bash"]
# Tue, 20 Sep 2022 19:58:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Sep 2022 19:58:16 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 20 Sep 2022 19:58:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2022 19:58:25 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 19:58:25 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 19:58:25 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 19:58:25 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 19:58:25 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 20 Sep 2022 19:58:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 19:58:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:43caeee1782255456dd3403ae8e6ba191802c3deb004ca68ce0420b30368995d`  
		Last Modified: Tue, 13 Sep 2022 03:49:46 GMT  
		Size: 26.6 MB (26567059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:371e8fe2f90e5f8d831cf3f7cbbc761654bac2e0078454288e46daa25ca92aa6`  
		Last Modified: Tue, 20 Sep 2022 19:59:29 GMT  
		Size: 4.5 MB (4493863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab1850643493bf25d0c68c29ad266c4f67f175f31e2515db85af18d2028d776`  
		Last Modified: Tue, 20 Sep 2022 19:59:49 GMT  
		Size: 33.5 MB (33526618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1988a81f8ae78d32966d6ef5cab36834912881b84ea48c3cfa698346cddc64`  
		Last Modified: Tue, 20 Sep 2022 19:59:44 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba51c69ab860b6578b1df65fe974baae531e4743a13c6626492ba066a0c9a2b`  
		Last Modified: Tue, 20 Sep 2022 19:59:44 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28447074d3a0939c65e75ba3630eab46594ba95b65c2514cefe5051f81d4f55a`  
		Last Modified: Tue, 20 Sep 2022 19:59:44 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:e29c8b01a0831127b1994934582089f2d801adfe4934b2f068e5711e4fd96e77
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68466898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91fea2f22cad79161668310578be729823ae84144d50a7c8605f3a39034283a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 20 Sep 2022 20:44:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Sep 2022 20:44:26 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 20 Sep 2022 20:44:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2022 20:44:34 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 20:44:35 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 20:44:35 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 20:44:36 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 20:44:38 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 20 Sep 2022 20:44:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 20:44:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2c9f840ab139e2eb5a0f134343fb6c9aee8c40ccb2c7359ee1412e99709bab`  
		Last Modified: Tue, 20 Sep 2022 20:45:42 GMT  
		Size: 5.2 MB (5208924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64aec835caa3d70608d551ce1b06bbb669a3cdbf6195116a274d5b1ec92cbc84`  
		Last Modified: Tue, 20 Sep 2022 20:46:02 GMT  
		Size: 33.2 MB (33179340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f201d733bb081122d97e8b575a7bb73a6ed70c43b09835889477c93fbbf5d7a`  
		Last Modified: Tue, 20 Sep 2022 20:45:57 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6079d751af0326f0081ae91b2d5a7f67c6f678e035b39d24f02577c87a7d3835`  
		Last Modified: Tue, 20 Sep 2022 20:45:57 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c67f0a76c180405d2d73a3ba5b7c9216b4cd49e559bee44cceca64fae5351ca`  
		Last Modified: Tue, 20 Sep 2022 20:45:57 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:cf92fc3cc4691bd74be8d509e1daca31c444deeda4f588d763a6dbf938b01403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:38373234e15d1c93f102793597e9bf12e862d1c6aa7585a0bcba9c07ebc77621
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22808785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced3757bcaca9904d45cc79b6978e0aa53759fa9d16a4fb13fa24be010091f25`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:17:08 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 09 Aug 2022 18:17:38 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 09 Aug 2022 18:17:43 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 09 Aug 2022 18:17:43 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 09 Aug 2022 18:17:43 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 09 Aug 2022 18:17:43 GMT
EXPOSE 8888
# Tue, 09 Aug 2022 18:17:43 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Aug 2022 18:17:43 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 09 Aug 2022 18:17:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Aug 2022 18:17:43 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86aedf0b86f2f672427bd99edb4d53285ee3f072fdd5e4ea92fd315f1f9d2bb8`  
		Last Modified: Tue, 09 Aug 2022 18:18:07 GMT  
		Size: 284.6 KB (284571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63ea984c81d9a176e87bff3e349d81ffb7375a5fbb71f461b755a13a4e2ab17`  
		Last Modified: Tue, 09 Aug 2022 18:18:51 GMT  
		Size: 19.7 MB (19672179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8828c26e16c48e93e2262d948136dc8b4f87b0a28d6a7b29b71e7a18844c1a34`  
		Last Modified: Tue, 09 Aug 2022 18:18:47 GMT  
		Size: 12.3 KB (12263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015194f0f71e31bae9c869e9a3a8d1ceca19267c54f9cc06ac3e2a9236a89f57`  
		Last Modified: Tue, 09 Aug 2022 18:18:47 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0585391111ba79d1f1c74c4c722494c1e3378ab7694b9df14300c55ff270fe0`  
		Last Modified: Tue, 09 Aug 2022 18:18:47 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:6bcdd97ec79070cdc81bebfe9b516ca03d826a8efdd2c9ed6b56b0aa5746e67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9.4` - linux; amd64

```console
$ docker pull chronograf@sha256:694e8bab6ae3f4dd646af688f4c790cac097f7bfbebedc107036e276e9c12bec
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71881717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3ca8d13890b91f922f80a688845b9bdd913e1e6cdfb009e36cc8a7869eaa54`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 20 Sep 2022 20:21:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Sep 2022 20:21:44 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 20 Sep 2022 20:21:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2022 20:21:52 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 20:21:52 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 20:21:52 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 20:21:52 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 20:21:52 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 20 Sep 2022 20:21:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 20:21:52 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9912bf5b6c0d0a8c9f83f63b25e9d2594eba49ae7977f589f65cb3c6db68ee`  
		Last Modified: Tue, 20 Sep 2022 20:22:53 GMT  
		Size: 5.2 MB (5226757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f858f98c2fc7b84ac4e4e724df28aa1d1693d5ba7452b2101f450c2e1b1c8d`  
		Last Modified: Tue, 20 Sep 2022 20:23:12 GMT  
		Size: 35.2 MB (35226456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815a8049be7c95fbba36555b3d74548442f444aa4d031f194455721d8dbd735a`  
		Last Modified: Tue, 20 Sep 2022 20:23:07 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94818bc4ad21b22a74a469b5fd43191967deba02360d18d9dc4a3677e445db4b`  
		Last Modified: Tue, 20 Sep 2022 20:23:07 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34cc276b85549aa84243a3588344e5737bcea8a1cdd1c137e18f71f679ca0a1`  
		Last Modified: Tue, 20 Sep 2022 20:23:07 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:7146036f24aa9e1e166b756cda4e34568fcfb1e98a50bd362c4301886a9656fc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64611936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:728f159b2f0171718e9a66f3f63787e135caf15f3be015179446e3f16f367e09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Sep 2022 03:42:37 GMT
ADD file:04b0c48a2d326e2ac4255df4a6165508f0d29d8a32147fb8df6bf9504b8f6b09 in / 
# Tue, 13 Sep 2022 03:42:37 GMT
CMD ["bash"]
# Tue, 20 Sep 2022 19:58:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Sep 2022 19:58:16 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 20 Sep 2022 19:58:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2022 19:58:25 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 19:58:25 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 19:58:25 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 19:58:25 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 19:58:25 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 20 Sep 2022 19:58:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 19:58:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:43caeee1782255456dd3403ae8e6ba191802c3deb004ca68ce0420b30368995d`  
		Last Modified: Tue, 13 Sep 2022 03:49:46 GMT  
		Size: 26.6 MB (26567059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:371e8fe2f90e5f8d831cf3f7cbbc761654bac2e0078454288e46daa25ca92aa6`  
		Last Modified: Tue, 20 Sep 2022 19:59:29 GMT  
		Size: 4.5 MB (4493863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab1850643493bf25d0c68c29ad266c4f67f175f31e2515db85af18d2028d776`  
		Last Modified: Tue, 20 Sep 2022 19:59:49 GMT  
		Size: 33.5 MB (33526618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1988a81f8ae78d32966d6ef5cab36834912881b84ea48c3cfa698346cddc64`  
		Last Modified: Tue, 20 Sep 2022 19:59:44 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba51c69ab860b6578b1df65fe974baae531e4743a13c6626492ba066a0c9a2b`  
		Last Modified: Tue, 20 Sep 2022 19:59:44 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28447074d3a0939c65e75ba3630eab46594ba95b65c2514cefe5051f81d4f55a`  
		Last Modified: Tue, 20 Sep 2022 19:59:44 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:e29c8b01a0831127b1994934582089f2d801adfe4934b2f068e5711e4fd96e77
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68466898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91fea2f22cad79161668310578be729823ae84144d50a7c8605f3a39034283a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 20 Sep 2022 20:44:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Sep 2022 20:44:26 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 20 Sep 2022 20:44:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2022 20:44:34 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 20:44:35 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 20:44:35 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 20:44:36 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 20:44:38 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 20 Sep 2022 20:44:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 20:44:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2c9f840ab139e2eb5a0f134343fb6c9aee8c40ccb2c7359ee1412e99709bab`  
		Last Modified: Tue, 20 Sep 2022 20:45:42 GMT  
		Size: 5.2 MB (5208924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64aec835caa3d70608d551ce1b06bbb669a3cdbf6195116a274d5b1ec92cbc84`  
		Last Modified: Tue, 20 Sep 2022 20:46:02 GMT  
		Size: 33.2 MB (33179340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f201d733bb081122d97e8b575a7bb73a6ed70c43b09835889477c93fbbf5d7a`  
		Last Modified: Tue, 20 Sep 2022 20:45:57 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6079d751af0326f0081ae91b2d5a7f67c6f678e035b39d24f02577c87a7d3835`  
		Last Modified: Tue, 20 Sep 2022 20:45:57 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c67f0a76c180405d2d73a3ba5b7c9216b4cd49e559bee44cceca64fae5351ca`  
		Last Modified: Tue, 20 Sep 2022 20:45:57 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:cf92fc3cc4691bd74be8d509e1daca31c444deeda4f588d763a6dbf938b01403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:38373234e15d1c93f102793597e9bf12e862d1c6aa7585a0bcba9c07ebc77621
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22808785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced3757bcaca9904d45cc79b6978e0aa53759fa9d16a4fb13fa24be010091f25`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:17:08 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 09 Aug 2022 18:17:38 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 09 Aug 2022 18:17:43 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 09 Aug 2022 18:17:43 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 09 Aug 2022 18:17:43 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 09 Aug 2022 18:17:43 GMT
EXPOSE 8888
# Tue, 09 Aug 2022 18:17:43 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Aug 2022 18:17:43 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 09 Aug 2022 18:17:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Aug 2022 18:17:43 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86aedf0b86f2f672427bd99edb4d53285ee3f072fdd5e4ea92fd315f1f9d2bb8`  
		Last Modified: Tue, 09 Aug 2022 18:18:07 GMT  
		Size: 284.6 KB (284571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63ea984c81d9a176e87bff3e349d81ffb7375a5fbb71f461b755a13a4e2ab17`  
		Last Modified: Tue, 09 Aug 2022 18:18:51 GMT  
		Size: 19.7 MB (19672179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8828c26e16c48e93e2262d948136dc8b4f87b0a28d6a7b29b71e7a18844c1a34`  
		Last Modified: Tue, 09 Aug 2022 18:18:47 GMT  
		Size: 12.3 KB (12263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015194f0f71e31bae9c869e9a3a8d1ceca19267c54f9cc06ac3e2a9236a89f57`  
		Last Modified: Tue, 09 Aug 2022 18:18:47 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0585391111ba79d1f1c74c4c722494c1e3378ab7694b9df14300c55ff270fe0`  
		Last Modified: Tue, 09 Aug 2022 18:18:47 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:10db860523fe5eebdf4890773b3e7f2e03aaa709bc7728a5acf0444b06f26217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:716811ca8465a91cf9ee2ec75857611e7859c0fbb9a2569ebc840720317be46e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30311121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46e472a1f7b448779d264ff1d5a2d3e0711a25c41260fbf237eecb091cbd66b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:17:08 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 20 Sep 2022 20:22:08 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Tue, 20 Sep 2022 20:22:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 20 Sep 2022 20:22:14 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 20:22:14 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 20:22:14 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 20:22:14 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 20:22:15 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 20 Sep 2022 20:22:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 20:22:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86aedf0b86f2f672427bd99edb4d53285ee3f072fdd5e4ea92fd315f1f9d2bb8`  
		Last Modified: Tue, 09 Aug 2022 18:18:07 GMT  
		Size: 284.6 KB (284571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ea195aa67f5544afe9744fdcb50f8426f7c9e78f1d2852eedf8a4f25abe5f3`  
		Last Modified: Tue, 20 Sep 2022 20:23:46 GMT  
		Size: 27.2 MB (27174514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6442c946b6fb9dbfb0fade5a61bacb47071521acdb42ff9cfc3c786f281099de`  
		Last Modified: Tue, 20 Sep 2022 20:23:41 GMT  
		Size: 12.3 KB (12260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dcf32ffd08f927f5984bcd48dce204c61e8a41cb17c10bbebe8ab5fdb8b441a`  
		Last Modified: Tue, 20 Sep 2022 20:23:41 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac10f24f91124d09ad041e5953607fa76cb06490cf6412aecbf309a0ab9317d`  
		Last Modified: Tue, 20 Sep 2022 20:23:41 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:a3dd2ea5f162b90eb91cc50bf553ea801d93f2492d3ea3aa8d76f7dff8f922fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:0131956c284642aa5046d24151f4c62239af3e7dbfba6b344647c7d883d68c21
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.2 MB (81242412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6c386352e5d3d8acedc1b7778f7016879414197db6bd43b691ba41db62e1c3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 20 Sep 2022 20:21:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Sep 2022 20:21:58 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Tue, 20 Sep 2022 20:22:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2022 20:22:05 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 20:22:05 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 20:22:05 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 20:22:05 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 20:22:05 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 20 Sep 2022 20:22:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 20:22:06 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9912bf5b6c0d0a8c9f83f63b25e9d2594eba49ae7977f589f65cb3c6db68ee`  
		Last Modified: Tue, 20 Sep 2022 20:22:53 GMT  
		Size: 5.2 MB (5226757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5465fc1b879a85d93348bfabdfcdefbb0690206998bead3c44f8d6c22cd0d42a`  
		Last Modified: Tue, 20 Sep 2022 20:23:29 GMT  
		Size: 44.6 MB (44587136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb13e1bf85984003fc04f672635ce3823c659d7a0256ecb8f4bf05818263c11`  
		Last Modified: Tue, 20 Sep 2022 20:23:22 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b396867a07f1e6c1663ed3f2f1fce140e3f25d0e1b220ec844910e28d75a7dc`  
		Last Modified: Tue, 20 Sep 2022 20:23:22 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bc49be513cee5763ad65b584f9dc6dda843bd132432ee82a4e99cf3af6a830`  
		Last Modified: Tue, 20 Sep 2022 20:23:22 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:79e4d12c8da2c80c1328792badf1807180df7dbef40720ea463da2fed777f8a7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73550015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ae5272dc31511ca7d9e9afe9c9564399d22e051a16ac6eefec2a04b706ad94`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Sep 2022 03:42:37 GMT
ADD file:04b0c48a2d326e2ac4255df4a6165508f0d29d8a32147fb8df6bf9504b8f6b09 in / 
# Tue, 13 Sep 2022 03:42:37 GMT
CMD ["bash"]
# Tue, 20 Sep 2022 19:58:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Sep 2022 19:58:30 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Tue, 20 Sep 2022 19:58:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2022 19:58:39 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 19:58:39 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 19:58:39 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 19:58:40 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 19:58:40 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 20 Sep 2022 19:58:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 19:58:40 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:43caeee1782255456dd3403ae8e6ba191802c3deb004ca68ce0420b30368995d`  
		Last Modified: Tue, 13 Sep 2022 03:49:46 GMT  
		Size: 26.6 MB (26567059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:371e8fe2f90e5f8d831cf3f7cbbc761654bac2e0078454288e46daa25ca92aa6`  
		Last Modified: Tue, 20 Sep 2022 19:59:29 GMT  
		Size: 4.5 MB (4493863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7655c5f70f62ed9844235f2139e13943ed47e2e18d3e6a57588794ff8469d608`  
		Last Modified: Tue, 20 Sep 2022 20:00:09 GMT  
		Size: 42.5 MB (42464705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797f5e419755f2972a7ea1b04533c75828cd0f0d6d0083e5d6fc1306b535ae7b`  
		Last Modified: Tue, 20 Sep 2022 20:00:00 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19af8ef6ad740ae7176c22212522177658a7a875eccfea0805b43a0b14519159`  
		Last Modified: Tue, 20 Sep 2022 20:00:00 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39fd7a5c09df81dba19d7d2d9053523f2b5336666a25dbcfb3c213f33038a407`  
		Last Modified: Tue, 20 Sep 2022 20:00:00 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:2d278a81bdce18c2e4856e98c43f18ef469615b525738941cda2b0c82e552571
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77688043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6218e80f8ed5be7d1c6494fbc10078f150696170e47bda497fed1c68e5488fbf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 20 Sep 2022 20:44:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Sep 2022 20:44:45 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Tue, 20 Sep 2022 20:44:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2022 20:44:56 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 20:44:57 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 20:44:57 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 20:44:58 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 20:45:00 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 20 Sep 2022 20:45:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 20:45:01 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2c9f840ab139e2eb5a0f134343fb6c9aee8c40ccb2c7359ee1412e99709bab`  
		Last Modified: Tue, 20 Sep 2022 20:45:42 GMT  
		Size: 5.2 MB (5208924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d628c5293d653bd4c9205ddfd8c98fc75b857deb038ef7d8e01a56c7f418c1`  
		Last Modified: Tue, 20 Sep 2022 20:46:22 GMT  
		Size: 42.4 MB (42400486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c4c343bf0713eee3dd2a8dfc3c39fc0a46d4db3ea0a20e15becb09dbaea4a89`  
		Last Modified: Tue, 20 Sep 2022 20:46:16 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8142f6c5218c655f3290043a32dcf2b8bb613b403a7f8edcd4cdb9d73510d8`  
		Last Modified: Tue, 20 Sep 2022 20:46:16 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c97fc46bd891af9e06e3fa2d3e7880d632e0fb64dca9d47f457efa8a08078116`  
		Last Modified: Tue, 20 Sep 2022 20:46:15 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
