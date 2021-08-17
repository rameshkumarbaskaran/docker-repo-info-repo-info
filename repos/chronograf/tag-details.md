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
-	[`chronograf:1.9.0`](#chronograf190)
-	[`chronograf:1.9.0-alpine`](#chronograf190-alpine)
-	[`chronograf:alpine`](#chronografalpine)
-	[`chronograf:latest`](#chronograflatest)

## `chronograf:1.6`

```console
$ docker pull chronograf@sha256:4889a8bf463e04ed41414c644f0f36e9407a5400db2c14dbf941cad96812b4c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6` - linux; amd64

```console
$ docker pull chronograf@sha256:3b4660a26f389836597fb2b820c1575a0f927f158fafdbbd75f5cfca03cf22ff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49357420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310cbe311dfb78e8644fc4e01b72c743add6339c31ddad257afcbcea04839dec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Aug 2021 01:26:09 GMT
ADD file:f6c4487fa1f7a4e17f5d88fd0c91031a6efc7fa210d363a1d43d8b0f3a8d1d03 in / 
# Tue, 17 Aug 2021 01:26:09 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:35:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 17 Aug 2021 09:35:18 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 17 Aug 2021 09:35:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 17 Aug 2021 09:35:29 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 17 Aug 2021 09:35:29 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 17 Aug 2021 09:35:29 GMT
EXPOSE 8888
# Tue, 17 Aug 2021 09:35:30 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Aug 2021 09:35:30 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 17 Aug 2021 09:35:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 09:35:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:33f99cea3b7da8c6e0143c9fd7590c6d56f7d310ddd59b11be4ad485ae4cab2a`  
		Last Modified: Tue, 17 Aug 2021 01:33:27 GMT  
		Size: 22.5 MB (22527748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ebf00cee8edb2723f73bb596dc02dac400fcd609c6288b968066e0333dc5cd`  
		Last Modified: Tue, 17 Aug 2021 09:37:00 GMT  
		Size: 6.8 MB (6760152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccda430674c7927de7007bb50f73dece289da6d73e105bff2ef5c92500989d69`  
		Last Modified: Tue, 17 Aug 2021 09:37:02 GMT  
		Size: 20.0 MB (20045128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5c8c3233de6e30d92f753e7ab5939410ec8ac407ff9f7a15ba73666c7caf82`  
		Last Modified: Tue, 17 Aug 2021 09:36:58 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f441ad12b885a481ebc2e5f518f52099cbc6ca3e6b1a60a4fa43a433038734`  
		Last Modified: Tue, 17 Aug 2021 09:36:58 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738a6d4707ebd96360080f6d9b73b271fb4ee1219cf558079a5655dd9f2f2ef2`  
		Last Modified: Tue, 17 Aug 2021 09:36:58 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:937f347d13b519066ca1ae2249c195c1299fc329a9ba8709436fb43e2ff81974
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43940050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed3e4e95860aad998ffa6095b118d4bcbe0933cc2c4c3b8879bb0a481d744a3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 22 Jul 2021 02:07:27 GMT
ADD file:86bd875241ca751f2f50a9c3504cfca4ce772411fed23fe6893299a271c275e3 in / 
# Thu, 22 Jul 2021 02:07:28 GMT
CMD ["bash"]
# Tue, 10 Aug 2021 23:00:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 10 Aug 2021 23:00:20 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 10 Aug 2021 23:00:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 10 Aug 2021 23:00:39 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 10 Aug 2021 23:00:39 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 10 Aug 2021 23:00:40 GMT
EXPOSE 8888
# Tue, 10 Aug 2021 23:00:40 GMT
VOLUME [/var/lib/chronograf]
# Tue, 10 Aug 2021 23:00:41 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 10 Aug 2021 23:00:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 10 Aug 2021 23:00:42 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:37325b08023150a9e16c0c8d98d10daa998ce21ec3b9226cc6f0148a245a8a57`  
		Last Modified: Thu, 22 Jul 2021 02:21:16 GMT  
		Size: 19.3 MB (19315955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84236a4145013894eb753d54367ba39e700f41448379d11fb8acf79e2100e630`  
		Last Modified: Tue, 10 Aug 2021 23:03:14 GMT  
		Size: 5.8 MB (5779562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a1dc89d74b7c5071acf919f530b85ed228e090e9cdccc9afea8caf0f30200f`  
		Last Modified: Tue, 10 Aug 2021 23:03:25 GMT  
		Size: 18.8 MB (18820143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99343d22bd6913d879353af2a2174afdea899e9dc0a06db34b78037c0ddccd45`  
		Last Modified: Tue, 10 Aug 2021 23:03:11 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ead756033b31ea26f45491b0a1053f06560360ab82603e4c36052a0a6cdd076`  
		Last Modified: Tue, 10 Aug 2021 23:03:12 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f774ca5cc026dd5d49d1d4894048be0935c16ddb91e0bed0fa054c7d2f4e317`  
		Last Modified: Tue, 10 Aug 2021 23:03:12 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:b3993f5a0342eb8518ecb45f32402b4826530ac265ee9895a0fceff87280b1f3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45423113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a0d2cce6e71edafe80039323e3f015795acf91d7028ea71b83f0a57c7e5c42`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Aug 2021 01:48:32 GMT
ADD file:5cd26935234cc0540158a144066c0341b46a0caeb0a80db0355eeb8cfaf4fc0d in / 
# Tue, 17 Aug 2021 01:48:32 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:06:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 17 Aug 2021 08:06:44 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 17 Aug 2021 08:06:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 17 Aug 2021 08:06:51 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 17 Aug 2021 08:06:51 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 17 Aug 2021 08:06:51 GMT
EXPOSE 8888
# Tue, 17 Aug 2021 08:06:51 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Aug 2021 08:06:52 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 17 Aug 2021 08:06:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 08:06:52 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f862659192cd149f96ede75854bd3ebf59937831d3e4103087ae62df34ef1a29`  
		Last Modified: Tue, 17 Aug 2021 01:58:00 GMT  
		Size: 20.4 MB (20389447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09101c696c7496dfd097387796cbe96c76aa138b186200c5879c0ab29f5a13f4`  
		Last Modified: Tue, 17 Aug 2021 08:08:19 GMT  
		Size: 6.0 MB (6047480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35a7bd7a24d14e7b972d73641567d9c535809bab448e644897b986e607352bf`  
		Last Modified: Tue, 17 Aug 2021 08:08:21 GMT  
		Size: 19.0 MB (18961797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffa82191109e148463f249f7ab2a56bcbe64c66f80df2f4de01b0df040bfca6`  
		Last Modified: Tue, 17 Aug 2021 08:08:18 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbe4df1b8d5a112e6eb342cca21bef851272f6f1fad782db24a6e6717463fef`  
		Last Modified: Tue, 17 Aug 2021 08:08:18 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84c8867c495c8baef876e2b57f77f5c856af2b43e06970f7ad6f6bb767a495ad`  
		Last Modified: Tue, 17 Aug 2021 08:08:18 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6-alpine`

```console
$ docker pull chronograf@sha256:ada0b282d21296c8d97068d0801d827e49d67792f2981e300538c4385990bc59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.6-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:28a7b9f2a681945dd89fc7865df21bcaa5216a16f7e79e87da33d316fda89910
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14842762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed5850f2dae8d0644d3496647550c4000636144456efedc97e9eda71a3d081c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:12:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:12:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 14 Apr 2021 20:12:40 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 10 Aug 2021 23:20:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 10 Aug 2021 23:20:02 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Tue, 10 Aug 2021 23:20:02 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 10 Aug 2021 23:20:03 GMT
EXPOSE 8888
# Tue, 10 Aug 2021 23:20:03 GMT
VOLUME [/var/lib/chronograf]
# Tue, 10 Aug 2021 23:20:03 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 10 Aug 2021 23:20:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 10 Aug 2021 23:20:03 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4496f95da0ff203c55ba4ff45e6cc518bfd24507a21516931244d25e8db7d14`  
		Last Modified: Wed, 14 Apr 2021 20:13:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9162e7666a3906b38fdfed2592cc2e4df967e365a3fcf17c8d6320caed7fd960`  
		Last Modified: Wed, 14 Apr 2021 20:13:33 GMT  
		Size: 280.9 KB (280875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfcd6b0882a537f8fe6b59585d29fa4d6d47e8cdb0e4262856bf896cf4764b15`  
		Last Modified: Tue, 10 Aug 2021 23:21:38 GMT  
		Size: 11.7 MB (11736757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081a63d1624e51ea2cd0c5ff9ad4d5cc13a47c2c5d6cd7de045353417b898fdb`  
		Last Modified: Tue, 10 Aug 2021 23:21:36 GMT  
		Size: 12.3 KB (12274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c635eea67029f9448825d79218907e17aa6c0b3e9b79fcaf6bd0e3b9844f9ea0`  
		Last Modified: Tue, 10 Aug 2021 23:21:36 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c52810ec67ccefae718979e0ee5a95dd3d15fbfbf934a7ffc1a49e5f38476e`  
		Last Modified: Tue, 10 Aug 2021 23:21:36 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6.2`

```console
$ docker pull chronograf@sha256:4889a8bf463e04ed41414c644f0f36e9407a5400db2c14dbf941cad96812b4c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6.2` - linux; amd64

```console
$ docker pull chronograf@sha256:3b4660a26f389836597fb2b820c1575a0f927f158fafdbbd75f5cfca03cf22ff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49357420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310cbe311dfb78e8644fc4e01b72c743add6339c31ddad257afcbcea04839dec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Aug 2021 01:26:09 GMT
ADD file:f6c4487fa1f7a4e17f5d88fd0c91031a6efc7fa210d363a1d43d8b0f3a8d1d03 in / 
# Tue, 17 Aug 2021 01:26:09 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:35:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 17 Aug 2021 09:35:18 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 17 Aug 2021 09:35:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 17 Aug 2021 09:35:29 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 17 Aug 2021 09:35:29 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 17 Aug 2021 09:35:29 GMT
EXPOSE 8888
# Tue, 17 Aug 2021 09:35:30 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Aug 2021 09:35:30 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 17 Aug 2021 09:35:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 09:35:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:33f99cea3b7da8c6e0143c9fd7590c6d56f7d310ddd59b11be4ad485ae4cab2a`  
		Last Modified: Tue, 17 Aug 2021 01:33:27 GMT  
		Size: 22.5 MB (22527748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ebf00cee8edb2723f73bb596dc02dac400fcd609c6288b968066e0333dc5cd`  
		Last Modified: Tue, 17 Aug 2021 09:37:00 GMT  
		Size: 6.8 MB (6760152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccda430674c7927de7007bb50f73dece289da6d73e105bff2ef5c92500989d69`  
		Last Modified: Tue, 17 Aug 2021 09:37:02 GMT  
		Size: 20.0 MB (20045128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5c8c3233de6e30d92f753e7ab5939410ec8ac407ff9f7a15ba73666c7caf82`  
		Last Modified: Tue, 17 Aug 2021 09:36:58 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f441ad12b885a481ebc2e5f518f52099cbc6ca3e6b1a60a4fa43a433038734`  
		Last Modified: Tue, 17 Aug 2021 09:36:58 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738a6d4707ebd96360080f6d9b73b271fb4ee1219cf558079a5655dd9f2f2ef2`  
		Last Modified: Tue, 17 Aug 2021 09:36:58 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:937f347d13b519066ca1ae2249c195c1299fc329a9ba8709436fb43e2ff81974
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43940050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed3e4e95860aad998ffa6095b118d4bcbe0933cc2c4c3b8879bb0a481d744a3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 22 Jul 2021 02:07:27 GMT
ADD file:86bd875241ca751f2f50a9c3504cfca4ce772411fed23fe6893299a271c275e3 in / 
# Thu, 22 Jul 2021 02:07:28 GMT
CMD ["bash"]
# Tue, 10 Aug 2021 23:00:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 10 Aug 2021 23:00:20 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 10 Aug 2021 23:00:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 10 Aug 2021 23:00:39 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 10 Aug 2021 23:00:39 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 10 Aug 2021 23:00:40 GMT
EXPOSE 8888
# Tue, 10 Aug 2021 23:00:40 GMT
VOLUME [/var/lib/chronograf]
# Tue, 10 Aug 2021 23:00:41 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 10 Aug 2021 23:00:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 10 Aug 2021 23:00:42 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:37325b08023150a9e16c0c8d98d10daa998ce21ec3b9226cc6f0148a245a8a57`  
		Last Modified: Thu, 22 Jul 2021 02:21:16 GMT  
		Size: 19.3 MB (19315955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84236a4145013894eb753d54367ba39e700f41448379d11fb8acf79e2100e630`  
		Last Modified: Tue, 10 Aug 2021 23:03:14 GMT  
		Size: 5.8 MB (5779562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a1dc89d74b7c5071acf919f530b85ed228e090e9cdccc9afea8caf0f30200f`  
		Last Modified: Tue, 10 Aug 2021 23:03:25 GMT  
		Size: 18.8 MB (18820143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99343d22bd6913d879353af2a2174afdea899e9dc0a06db34b78037c0ddccd45`  
		Last Modified: Tue, 10 Aug 2021 23:03:11 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ead756033b31ea26f45491b0a1053f06560360ab82603e4c36052a0a6cdd076`  
		Last Modified: Tue, 10 Aug 2021 23:03:12 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f774ca5cc026dd5d49d1d4894048be0935c16ddb91e0bed0fa054c7d2f4e317`  
		Last Modified: Tue, 10 Aug 2021 23:03:12 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:b3993f5a0342eb8518ecb45f32402b4826530ac265ee9895a0fceff87280b1f3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45423113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a0d2cce6e71edafe80039323e3f015795acf91d7028ea71b83f0a57c7e5c42`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Aug 2021 01:48:32 GMT
ADD file:5cd26935234cc0540158a144066c0341b46a0caeb0a80db0355eeb8cfaf4fc0d in / 
# Tue, 17 Aug 2021 01:48:32 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:06:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 17 Aug 2021 08:06:44 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 17 Aug 2021 08:06:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 17 Aug 2021 08:06:51 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 17 Aug 2021 08:06:51 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 17 Aug 2021 08:06:51 GMT
EXPOSE 8888
# Tue, 17 Aug 2021 08:06:51 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Aug 2021 08:06:52 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 17 Aug 2021 08:06:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 08:06:52 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f862659192cd149f96ede75854bd3ebf59937831d3e4103087ae62df34ef1a29`  
		Last Modified: Tue, 17 Aug 2021 01:58:00 GMT  
		Size: 20.4 MB (20389447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09101c696c7496dfd097387796cbe96c76aa138b186200c5879c0ab29f5a13f4`  
		Last Modified: Tue, 17 Aug 2021 08:08:19 GMT  
		Size: 6.0 MB (6047480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35a7bd7a24d14e7b972d73641567d9c535809bab448e644897b986e607352bf`  
		Last Modified: Tue, 17 Aug 2021 08:08:21 GMT  
		Size: 19.0 MB (18961797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffa82191109e148463f249f7ab2a56bcbe64c66f80df2f4de01b0df040bfca6`  
		Last Modified: Tue, 17 Aug 2021 08:08:18 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbe4df1b8d5a112e6eb342cca21bef851272f6f1fad782db24a6e6717463fef`  
		Last Modified: Tue, 17 Aug 2021 08:08:18 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84c8867c495c8baef876e2b57f77f5c856af2b43e06970f7ad6f6bb767a495ad`  
		Last Modified: Tue, 17 Aug 2021 08:08:18 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6.2-alpine`

```console
$ docker pull chronograf@sha256:ada0b282d21296c8d97068d0801d827e49d67792f2981e300538c4385990bc59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.6.2-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:28a7b9f2a681945dd89fc7865df21bcaa5216a16f7e79e87da33d316fda89910
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14842762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed5850f2dae8d0644d3496647550c4000636144456efedc97e9eda71a3d081c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:12:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:12:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 14 Apr 2021 20:12:40 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 10 Aug 2021 23:20:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 10 Aug 2021 23:20:02 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Tue, 10 Aug 2021 23:20:02 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 10 Aug 2021 23:20:03 GMT
EXPOSE 8888
# Tue, 10 Aug 2021 23:20:03 GMT
VOLUME [/var/lib/chronograf]
# Tue, 10 Aug 2021 23:20:03 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 10 Aug 2021 23:20:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 10 Aug 2021 23:20:03 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4496f95da0ff203c55ba4ff45e6cc518bfd24507a21516931244d25e8db7d14`  
		Last Modified: Wed, 14 Apr 2021 20:13:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9162e7666a3906b38fdfed2592cc2e4df967e365a3fcf17c8d6320caed7fd960`  
		Last Modified: Wed, 14 Apr 2021 20:13:33 GMT  
		Size: 280.9 KB (280875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfcd6b0882a537f8fe6b59585d29fa4d6d47e8cdb0e4262856bf896cf4764b15`  
		Last Modified: Tue, 10 Aug 2021 23:21:38 GMT  
		Size: 11.7 MB (11736757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081a63d1624e51ea2cd0c5ff9ad4d5cc13a47c2c5d6cd7de045353417b898fdb`  
		Last Modified: Tue, 10 Aug 2021 23:21:36 GMT  
		Size: 12.3 KB (12274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c635eea67029f9448825d79218907e17aa6c0b3e9b79fcaf6bd0e3b9844f9ea0`  
		Last Modified: Tue, 10 Aug 2021 23:21:36 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c52810ec67ccefae718979e0ee5a95dd3d15fbfbf934a7ffc1a49e5f38476e`  
		Last Modified: Tue, 10 Aug 2021 23:21:36 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:00074699e19dcbbe72168e3922afc82915fbbd9610998ce730594a6c5cea1b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7` - linux; amd64

```console
$ docker pull chronograf@sha256:a0bd7f9a7a6f41e1bff144f6705cbd765ad16522cd5c79f6e550d680b404c6c9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65385969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ec19aa91c9ffb33b4a9a9682dbb6c75d3b197f70a15fdfc2dd0a4e088425d23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Aug 2021 01:26:09 GMT
ADD file:f6c4487fa1f7a4e17f5d88fd0c91031a6efc7fa210d363a1d43d8b0f3a8d1d03 in / 
# Tue, 17 Aug 2021 01:26:09 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:35:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 17 Aug 2021 09:35:46 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 17 Aug 2021 09:35:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 17 Aug 2021 09:35:57 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 17 Aug 2021 09:35:58 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 17 Aug 2021 09:35:58 GMT
EXPOSE 8888
# Tue, 17 Aug 2021 09:35:58 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Aug 2021 09:35:58 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 17 Aug 2021 09:35:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 09:35:59 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:33f99cea3b7da8c6e0143c9fd7590c6d56f7d310ddd59b11be4ad485ae4cab2a`  
		Last Modified: Tue, 17 Aug 2021 01:33:27 GMT  
		Size: 22.5 MB (22527748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b30e58325c4aced5f8b1db67699808a32667aa9b4c6ce8f2bdfa2483c1fca5d`  
		Last Modified: Tue, 17 Aug 2021 09:37:14 GMT  
		Size: 4.5 MB (4506000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feaf4e133d20eb12180b56077702463f8b86964c0c436a6428ba22d49937aee9`  
		Last Modified: Tue, 17 Aug 2021 09:37:19 GMT  
		Size: 38.3 MB (38327828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9423787f4c740286bf12eb3babfa4d046ac80fe5a0df99011d36bc7157b5b58`  
		Last Modified: Tue, 17 Aug 2021 09:37:13 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327bac57cd40f7913cf4c837b08e39f503a2a96d4d741b7357a346936be0c4c6`  
		Last Modified: Tue, 17 Aug 2021 09:37:13 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc64a52a995cae676aef575882522843ca58890ae3dac6b44c5661dffcf7173`  
		Last Modified: Tue, 17 Aug 2021 09:37:13 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:1d6a2a47d1a53e5add56f3a4f85656b5bb195938af16da1267302f76d0a01c2c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59002287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4a884bbcf9a9acedb85ede6e9d279c7f056db4f991ce6eb96da82f1583cfdf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 22 Jul 2021 02:07:27 GMT
ADD file:86bd875241ca751f2f50a9c3504cfca4ce772411fed23fe6893299a271c275e3 in / 
# Thu, 22 Jul 2021 02:07:28 GMT
CMD ["bash"]
# Tue, 10 Aug 2021 23:01:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 10 Aug 2021 23:01:12 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 10 Aug 2021 23:01:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 10 Aug 2021 23:01:48 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 10 Aug 2021 23:01:48 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 10 Aug 2021 23:01:49 GMT
EXPOSE 8888
# Tue, 10 Aug 2021 23:01:49 GMT
VOLUME [/var/lib/chronograf]
# Tue, 10 Aug 2021 23:01:50 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 10 Aug 2021 23:01:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 10 Aug 2021 23:01:51 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:37325b08023150a9e16c0c8d98d10daa998ce21ec3b9226cc6f0148a245a8a57`  
		Last Modified: Thu, 22 Jul 2021 02:21:16 GMT  
		Size: 19.3 MB (19315955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed63205ee5bbe64765ff2ec58aad56001ae3eb0d545702e6c05108dd001961bf`  
		Last Modified: Tue, 10 Aug 2021 23:03:39 GMT  
		Size: 3.9 MB (3879523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bdd12b4164662e89f773859a94b34fd08b538d249f2bd05dccda3f989e69ac4`  
		Last Modified: Tue, 10 Aug 2021 23:03:57 GMT  
		Size: 35.8 MB (35782417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b74f5599148ea9c1fd6af2a42de0465c64fc60e12be00b443792137b69e7801`  
		Last Modified: Tue, 10 Aug 2021 23:03:37 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9c1c0540b45b54cfb793cc3bbfc8443ba363ffd2c0d5d009e3cc346566b622`  
		Last Modified: Tue, 10 Aug 2021 23:03:37 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a09074b078251844942abc895a5007d7db5ebcec7036ed6b056e0a636212f5a`  
		Last Modified: Tue, 10 Aug 2021 23:03:37 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:784ae2f5b10603b07a9469b6f024c2381eadba945c359aa00ff63815d49d2f07
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60482129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:addf16420eaf0c8efe1c3d1b592739421caa793126f877f4e221875ed395af62`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Aug 2021 01:48:32 GMT
ADD file:5cd26935234cc0540158a144066c0341b46a0caeb0a80db0355eeb8cfaf4fc0d in / 
# Tue, 17 Aug 2021 01:48:32 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:07:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 17 Aug 2021 08:07:08 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 17 Aug 2021 08:07:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 17 Aug 2021 08:07:18 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 17 Aug 2021 08:07:18 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 17 Aug 2021 08:07:18 GMT
EXPOSE 8888
# Tue, 17 Aug 2021 08:07:18 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Aug 2021 08:07:18 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 17 Aug 2021 08:07:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 08:07:19 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f862659192cd149f96ede75854bd3ebf59937831d3e4103087ae62df34ef1a29`  
		Last Modified: Tue, 17 Aug 2021 01:58:00 GMT  
		Size: 20.4 MB (20389447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a633450ca1e80832c0d9d386dc78f5a7b17e96988c46adfce9f7fb9df3080cc8`  
		Last Modified: Tue, 17 Aug 2021 08:08:33 GMT  
		Size: 4.1 MB (4082143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369d3b51668baff5b0af480d4afb8749ee0292e2bc1cda07ffb54f639a9bbf11`  
		Last Modified: Tue, 17 Aug 2021 08:08:37 GMT  
		Size: 36.0 MB (35986144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc24a9d100c2c1bddd8eb913e91e3ae5f1a7c73e8022cd1d9662b40460015b81`  
		Last Modified: Tue, 17 Aug 2021 08:08:32 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61d15ba426300c200c2f21e8a6d770db59bda2a4345a5f1f8e6c57b2b14215c`  
		Last Modified: Tue, 17 Aug 2021 08:08:32 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedb0a234ee76ab5785a3e9e6a79e908e8c003c24ac020d6ce8cbafd93df9774`  
		Last Modified: Tue, 17 Aug 2021 08:08:32 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:7f2c1b48dacf8cda891b9f3431190d98cb9f561242502165800e149fa4be82ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:7beaa6e432166805db8d2b34c8a82c9dec67d25ec5de5701442b8e96f2b71662
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22661219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9862dbed0dde486ca14af2cddd3120de4282ad0da44bdc0a1f49fafabf3dcfc2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:12:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:12:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 14 Apr 2021 20:12:52 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 10 Aug 2021 23:20:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 10 Aug 2021 23:20:37 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 10 Aug 2021 23:20:37 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 10 Aug 2021 23:20:38 GMT
EXPOSE 8888
# Tue, 10 Aug 2021 23:20:38 GMT
VOLUME [/var/lib/chronograf]
# Tue, 10 Aug 2021 23:20:38 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 10 Aug 2021 23:20:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 10 Aug 2021 23:20:38 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4496f95da0ff203c55ba4ff45e6cc518bfd24507a21516931244d25e8db7d14`  
		Last Modified: Wed, 14 Apr 2021 20:13:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9162e7666a3906b38fdfed2592cc2e4df967e365a3fcf17c8d6320caed7fd960`  
		Last Modified: Wed, 14 Apr 2021 20:13:33 GMT  
		Size: 280.9 KB (280875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec531746a92f98b90e9629bf1ce734e2a7f932a05425793711b30491820cafba`  
		Last Modified: Tue, 10 Aug 2021 23:22:07 GMT  
		Size: 19.6 MB (19555230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7909b7f7fe22c4b2666569e47acfbefa9e2c3e16a121904924eb490b48b990ea`  
		Last Modified: Tue, 10 Aug 2021 23:22:04 GMT  
		Size: 12.3 KB (12262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6234dfd52f3932667ba45cf52bece80bd66fe0d4cc74d054c98fab20ffa723d5`  
		Last Modified: Tue, 10 Aug 2021 23:22:04 GMT  
		Size: 11.9 KB (11894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2f09d05de27367023d73792d4d182455bde1b6601170833f524eb30f66869b7`  
		Last Modified: Tue, 10 Aug 2021 23:22:04 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:00074699e19dcbbe72168e3922afc82915fbbd9610998ce730594a6c5cea1b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7.17` - linux; amd64

```console
$ docker pull chronograf@sha256:a0bd7f9a7a6f41e1bff144f6705cbd765ad16522cd5c79f6e550d680b404c6c9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65385969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ec19aa91c9ffb33b4a9a9682dbb6c75d3b197f70a15fdfc2dd0a4e088425d23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Aug 2021 01:26:09 GMT
ADD file:f6c4487fa1f7a4e17f5d88fd0c91031a6efc7fa210d363a1d43d8b0f3a8d1d03 in / 
# Tue, 17 Aug 2021 01:26:09 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:35:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 17 Aug 2021 09:35:46 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 17 Aug 2021 09:35:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 17 Aug 2021 09:35:57 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 17 Aug 2021 09:35:58 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 17 Aug 2021 09:35:58 GMT
EXPOSE 8888
# Tue, 17 Aug 2021 09:35:58 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Aug 2021 09:35:58 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 17 Aug 2021 09:35:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 09:35:59 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:33f99cea3b7da8c6e0143c9fd7590c6d56f7d310ddd59b11be4ad485ae4cab2a`  
		Last Modified: Tue, 17 Aug 2021 01:33:27 GMT  
		Size: 22.5 MB (22527748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b30e58325c4aced5f8b1db67699808a32667aa9b4c6ce8f2bdfa2483c1fca5d`  
		Last Modified: Tue, 17 Aug 2021 09:37:14 GMT  
		Size: 4.5 MB (4506000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feaf4e133d20eb12180b56077702463f8b86964c0c436a6428ba22d49937aee9`  
		Last Modified: Tue, 17 Aug 2021 09:37:19 GMT  
		Size: 38.3 MB (38327828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9423787f4c740286bf12eb3babfa4d046ac80fe5a0df99011d36bc7157b5b58`  
		Last Modified: Tue, 17 Aug 2021 09:37:13 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327bac57cd40f7913cf4c837b08e39f503a2a96d4d741b7357a346936be0c4c6`  
		Last Modified: Tue, 17 Aug 2021 09:37:13 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc64a52a995cae676aef575882522843ca58890ae3dac6b44c5661dffcf7173`  
		Last Modified: Tue, 17 Aug 2021 09:37:13 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:1d6a2a47d1a53e5add56f3a4f85656b5bb195938af16da1267302f76d0a01c2c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59002287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4a884bbcf9a9acedb85ede6e9d279c7f056db4f991ce6eb96da82f1583cfdf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 22 Jul 2021 02:07:27 GMT
ADD file:86bd875241ca751f2f50a9c3504cfca4ce772411fed23fe6893299a271c275e3 in / 
# Thu, 22 Jul 2021 02:07:28 GMT
CMD ["bash"]
# Tue, 10 Aug 2021 23:01:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 10 Aug 2021 23:01:12 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 10 Aug 2021 23:01:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 10 Aug 2021 23:01:48 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 10 Aug 2021 23:01:48 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 10 Aug 2021 23:01:49 GMT
EXPOSE 8888
# Tue, 10 Aug 2021 23:01:49 GMT
VOLUME [/var/lib/chronograf]
# Tue, 10 Aug 2021 23:01:50 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 10 Aug 2021 23:01:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 10 Aug 2021 23:01:51 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:37325b08023150a9e16c0c8d98d10daa998ce21ec3b9226cc6f0148a245a8a57`  
		Last Modified: Thu, 22 Jul 2021 02:21:16 GMT  
		Size: 19.3 MB (19315955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed63205ee5bbe64765ff2ec58aad56001ae3eb0d545702e6c05108dd001961bf`  
		Last Modified: Tue, 10 Aug 2021 23:03:39 GMT  
		Size: 3.9 MB (3879523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bdd12b4164662e89f773859a94b34fd08b538d249f2bd05dccda3f989e69ac4`  
		Last Modified: Tue, 10 Aug 2021 23:03:57 GMT  
		Size: 35.8 MB (35782417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b74f5599148ea9c1fd6af2a42de0465c64fc60e12be00b443792137b69e7801`  
		Last Modified: Tue, 10 Aug 2021 23:03:37 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9c1c0540b45b54cfb793cc3bbfc8443ba363ffd2c0d5d009e3cc346566b622`  
		Last Modified: Tue, 10 Aug 2021 23:03:37 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a09074b078251844942abc895a5007d7db5ebcec7036ed6b056e0a636212f5a`  
		Last Modified: Tue, 10 Aug 2021 23:03:37 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:784ae2f5b10603b07a9469b6f024c2381eadba945c359aa00ff63815d49d2f07
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60482129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:addf16420eaf0c8efe1c3d1b592739421caa793126f877f4e221875ed395af62`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Aug 2021 01:48:32 GMT
ADD file:5cd26935234cc0540158a144066c0341b46a0caeb0a80db0355eeb8cfaf4fc0d in / 
# Tue, 17 Aug 2021 01:48:32 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:07:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 17 Aug 2021 08:07:08 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 17 Aug 2021 08:07:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 17 Aug 2021 08:07:18 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 17 Aug 2021 08:07:18 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 17 Aug 2021 08:07:18 GMT
EXPOSE 8888
# Tue, 17 Aug 2021 08:07:18 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Aug 2021 08:07:18 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 17 Aug 2021 08:07:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 08:07:19 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f862659192cd149f96ede75854bd3ebf59937831d3e4103087ae62df34ef1a29`  
		Last Modified: Tue, 17 Aug 2021 01:58:00 GMT  
		Size: 20.4 MB (20389447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a633450ca1e80832c0d9d386dc78f5a7b17e96988c46adfce9f7fb9df3080cc8`  
		Last Modified: Tue, 17 Aug 2021 08:08:33 GMT  
		Size: 4.1 MB (4082143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369d3b51668baff5b0af480d4afb8749ee0292e2bc1cda07ffb54f639a9bbf11`  
		Last Modified: Tue, 17 Aug 2021 08:08:37 GMT  
		Size: 36.0 MB (35986144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc24a9d100c2c1bddd8eb913e91e3ae5f1a7c73e8022cd1d9662b40460015b81`  
		Last Modified: Tue, 17 Aug 2021 08:08:32 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61d15ba426300c200c2f21e8a6d770db59bda2a4345a5f1f8e6c57b2b14215c`  
		Last Modified: Tue, 17 Aug 2021 08:08:32 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedb0a234ee76ab5785a3e9e6a79e908e8c003c24ac020d6ce8cbafd93df9774`  
		Last Modified: Tue, 17 Aug 2021 08:08:32 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:7f2c1b48dacf8cda891b9f3431190d98cb9f561242502165800e149fa4be82ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:7beaa6e432166805db8d2b34c8a82c9dec67d25ec5de5701442b8e96f2b71662
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22661219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9862dbed0dde486ca14af2cddd3120de4282ad0da44bdc0a1f49fafabf3dcfc2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:12:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:12:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 14 Apr 2021 20:12:52 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 10 Aug 2021 23:20:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 10 Aug 2021 23:20:37 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 10 Aug 2021 23:20:37 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 10 Aug 2021 23:20:38 GMT
EXPOSE 8888
# Tue, 10 Aug 2021 23:20:38 GMT
VOLUME [/var/lib/chronograf]
# Tue, 10 Aug 2021 23:20:38 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 10 Aug 2021 23:20:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 10 Aug 2021 23:20:38 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4496f95da0ff203c55ba4ff45e6cc518bfd24507a21516931244d25e8db7d14`  
		Last Modified: Wed, 14 Apr 2021 20:13:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9162e7666a3906b38fdfed2592cc2e4df967e365a3fcf17c8d6320caed7fd960`  
		Last Modified: Wed, 14 Apr 2021 20:13:33 GMT  
		Size: 280.9 KB (280875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec531746a92f98b90e9629bf1ce734e2a7f932a05425793711b30491820cafba`  
		Last Modified: Tue, 10 Aug 2021 23:22:07 GMT  
		Size: 19.6 MB (19555230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7909b7f7fe22c4b2666569e47acfbefa9e2c3e16a121904924eb490b48b990ea`  
		Last Modified: Tue, 10 Aug 2021 23:22:04 GMT  
		Size: 12.3 KB (12262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6234dfd52f3932667ba45cf52bece80bd66fe0d4cc74d054c98fab20ffa723d5`  
		Last Modified: Tue, 10 Aug 2021 23:22:04 GMT  
		Size: 11.9 KB (11894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2f09d05de27367023d73792d4d182455bde1b6601170833f524eb30f66869b7`  
		Last Modified: Tue, 10 Aug 2021 23:22:04 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:56315caa69444b79be293920cd145f719fab5df812db9b93235f8620ec2387a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8` - linux; amd64

```console
$ docker pull chronograf@sha256:02e7e7e461fefbdc8d151d4775b08f62e9eca611e1bc888f83a4c5a8730561d5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66238411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f735df9bd93956f4544c105a5ca505c769d1ee260ad75591e8661f64394155b6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Aug 2021 01:26:09 GMT
ADD file:f6c4487fa1f7a4e17f5d88fd0c91031a6efc7fa210d363a1d43d8b0f3a8d1d03 in / 
# Tue, 17 Aug 2021 01:26:09 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:35:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 17 Aug 2021 09:36:05 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 17 Aug 2021 09:36:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 17 Aug 2021 09:36:13 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 17 Aug 2021 09:36:13 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 17 Aug 2021 09:36:13 GMT
EXPOSE 8888
# Tue, 17 Aug 2021 09:36:13 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Aug 2021 09:36:14 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 17 Aug 2021 09:36:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 09:36:14 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:33f99cea3b7da8c6e0143c9fd7590c6d56f7d310ddd59b11be4ad485ae4cab2a`  
		Last Modified: Tue, 17 Aug 2021 01:33:27 GMT  
		Size: 22.5 MB (22527748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ebf00cee8edb2723f73bb596dc02dac400fcd609c6288b968066e0333dc5cd`  
		Last Modified: Tue, 17 Aug 2021 09:37:00 GMT  
		Size: 6.8 MB (6760152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d733329bb98a3c70530f4e78fbc26f2e104088f96861464937e43bf83cf5bc`  
		Last Modified: Tue, 17 Aug 2021 09:37:35 GMT  
		Size: 36.9 MB (36926121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6075bbba535a693eaae2e807d6035e58abde36009d60e74a72b3d4245bd92b`  
		Last Modified: Tue, 17 Aug 2021 09:37:30 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b744d95d8178283c366bf94fd33fbb9f2afdf33f607a43b5a44514b57b60f35d`  
		Last Modified: Tue, 17 Aug 2021 09:37:30 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49d310da5a1e0d6daac1fdcc68637b2efd0e73f879b8b1fad67dec4eac99591`  
		Last Modified: Tue, 17 Aug 2021 09:37:30 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:22d962b42bfd6cc98171029a05a340fdfaa48f23f3467945f72eb3903c7144ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59629723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3e34110a34484bb2b5fc92bb618d5407446d1bc3400e8d4f8b36f8993e40035`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 22 Jul 2021 02:07:27 GMT
ADD file:86bd875241ca751f2f50a9c3504cfca4ce772411fed23fe6893299a271c275e3 in / 
# Thu, 22 Jul 2021 02:07:28 GMT
CMD ["bash"]
# Tue, 10 Aug 2021 23:00:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 Aug 2021 17:57:54 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 11 Aug 2021 17:58:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 Aug 2021 17:58:15 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 Aug 2021 17:58:15 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 Aug 2021 17:58:16 GMT
EXPOSE 8888
# Wed, 11 Aug 2021 17:58:16 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 Aug 2021 17:58:17 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 Aug 2021 17:58:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Aug 2021 17:58:18 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:37325b08023150a9e16c0c8d98d10daa998ce21ec3b9226cc6f0148a245a8a57`  
		Last Modified: Thu, 22 Jul 2021 02:21:16 GMT  
		Size: 19.3 MB (19315955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84236a4145013894eb753d54367ba39e700f41448379d11fb8acf79e2100e630`  
		Last Modified: Tue, 10 Aug 2021 23:03:14 GMT  
		Size: 5.8 MB (5779562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c94e453b1526664141d2e656e2d459e6bdfe67c0125787e512a756b9ffd8d66`  
		Last Modified: Wed, 11 Aug 2021 17:59:24 GMT  
		Size: 34.5 MB (34509822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd08ad62061e36c850fea016d5e524bdd6e212a10f058ab27f66eafbf0f655ed`  
		Last Modified: Wed, 11 Aug 2021 17:59:07 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb0c19cb6001660e07df3fe79b9cf16cf6e70069f6ba63823f7ae328aecb1ac`  
		Last Modified: Wed, 11 Aug 2021 17:59:06 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79345035daad04e1a83f087e06fdc0ea2ed3cae344a24786d56721c803df31e4`  
		Last Modified: Wed, 11 Aug 2021 17:59:06 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:50bb95ad8e75c72c6c78f2adc41fa1e4e65c9ce606149939014765140436b714
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60893485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab2558c75bff2c996f9ab8ade4d2b02c8527c43f5217aaec182a7c2ef4bc3a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Aug 2021 01:48:32 GMT
ADD file:5cd26935234cc0540158a144066c0341b46a0caeb0a80db0355eeb8cfaf4fc0d in / 
# Tue, 17 Aug 2021 01:48:32 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:06:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 17 Aug 2021 08:07:26 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 17 Aug 2021 08:07:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 17 Aug 2021 08:07:34 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 17 Aug 2021 08:07:34 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 17 Aug 2021 08:07:34 GMT
EXPOSE 8888
# Tue, 17 Aug 2021 08:07:35 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Aug 2021 08:07:35 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 17 Aug 2021 08:07:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 08:07:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f862659192cd149f96ede75854bd3ebf59937831d3e4103087ae62df34ef1a29`  
		Last Modified: Tue, 17 Aug 2021 01:58:00 GMT  
		Size: 20.4 MB (20389447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09101c696c7496dfd097387796cbe96c76aa138b186200c5879c0ab29f5a13f4`  
		Last Modified: Tue, 17 Aug 2021 08:08:19 GMT  
		Size: 6.0 MB (6047480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dde8e33fe3c76bb15079dbf979e7a62649160f833f7b79c87e509274572b830`  
		Last Modified: Tue, 17 Aug 2021 08:08:54 GMT  
		Size: 34.4 MB (34432168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d5bfc7c7d8d7f65b1f51b16ceaecf855e71888a5698056ab8ec5637c6840df`  
		Last Modified: Tue, 17 Aug 2021 08:08:49 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5940fd5898023978d247df91489e6acb6c1faa54e057c808855af070b0ee5eb`  
		Last Modified: Tue, 17 Aug 2021 08:08:49 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed27ffdb1a1c2b0057c08793346e56e346582bc736e47db7707e2eb7c3c1846`  
		Last Modified: Tue, 17 Aug 2021 08:08:49 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:8f39edc24654fbd11f32e9e80229bbe27370cfa1f87d22cb39bb05d45f413594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:9a9ca1c1267bc671715843e0353e85bc10e7562e47924589893ea721baaecfe4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22309890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3802774693dc4a8d1ae2e3fc1443f2abc4fa439c8da2c33bc9631627cad1363`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:12:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:12:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 11 Aug 2021 18:19:56 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 11 Aug 2021 18:20:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 11 Aug 2021 18:20:03 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 Aug 2021 18:20:03 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 Aug 2021 18:20:03 GMT
EXPOSE 8888
# Wed, 11 Aug 2021 18:20:03 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 Aug 2021 18:20:03 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 11 Aug 2021 18:20:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Aug 2021 18:20:04 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4496f95da0ff203c55ba4ff45e6cc518bfd24507a21516931244d25e8db7d14`  
		Last Modified: Wed, 14 Apr 2021 20:13:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9162e7666a3906b38fdfed2592cc2e4df967e365a3fcf17c8d6320caed7fd960`  
		Last Modified: Wed, 14 Apr 2021 20:13:33 GMT  
		Size: 280.9 KB (280875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c29671357b22bf6c966f84c718c8cd16c7e8ce22e40cbdf87aceb248ad2206`  
		Last Modified: Wed, 11 Aug 2021 18:20:49 GMT  
		Size: 19.2 MB (19203896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef01851ecfdf47c32aefac2145603c02cb9aef56d95f3daaef616e6ed684a21`  
		Last Modified: Wed, 11 Aug 2021 18:20:46 GMT  
		Size: 12.3 KB (12264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d28858f637808b758c6047a197bd7e0e4e9fc975d9d7df3a67bcb3aaece355`  
		Last Modified: Wed, 11 Aug 2021 18:20:46 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8a411f207f7b3c2682ac77fdc8a28e9b3f645c46d53fdb3437c0ade731cb1a`  
		Last Modified: Wed, 11 Aug 2021 18:20:46 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:56315caa69444b79be293920cd145f719fab5df812db9b93235f8620ec2387a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8.10` - linux; amd64

```console
$ docker pull chronograf@sha256:02e7e7e461fefbdc8d151d4775b08f62e9eca611e1bc888f83a4c5a8730561d5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66238411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f735df9bd93956f4544c105a5ca505c769d1ee260ad75591e8661f64394155b6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Aug 2021 01:26:09 GMT
ADD file:f6c4487fa1f7a4e17f5d88fd0c91031a6efc7fa210d363a1d43d8b0f3a8d1d03 in / 
# Tue, 17 Aug 2021 01:26:09 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:35:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 17 Aug 2021 09:36:05 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 17 Aug 2021 09:36:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 17 Aug 2021 09:36:13 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 17 Aug 2021 09:36:13 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 17 Aug 2021 09:36:13 GMT
EXPOSE 8888
# Tue, 17 Aug 2021 09:36:13 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Aug 2021 09:36:14 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 17 Aug 2021 09:36:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 09:36:14 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:33f99cea3b7da8c6e0143c9fd7590c6d56f7d310ddd59b11be4ad485ae4cab2a`  
		Last Modified: Tue, 17 Aug 2021 01:33:27 GMT  
		Size: 22.5 MB (22527748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ebf00cee8edb2723f73bb596dc02dac400fcd609c6288b968066e0333dc5cd`  
		Last Modified: Tue, 17 Aug 2021 09:37:00 GMT  
		Size: 6.8 MB (6760152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d733329bb98a3c70530f4e78fbc26f2e104088f96861464937e43bf83cf5bc`  
		Last Modified: Tue, 17 Aug 2021 09:37:35 GMT  
		Size: 36.9 MB (36926121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6075bbba535a693eaae2e807d6035e58abde36009d60e74a72b3d4245bd92b`  
		Last Modified: Tue, 17 Aug 2021 09:37:30 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b744d95d8178283c366bf94fd33fbb9f2afdf33f607a43b5a44514b57b60f35d`  
		Last Modified: Tue, 17 Aug 2021 09:37:30 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49d310da5a1e0d6daac1fdcc68637b2efd0e73f879b8b1fad67dec4eac99591`  
		Last Modified: Tue, 17 Aug 2021 09:37:30 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:22d962b42bfd6cc98171029a05a340fdfaa48f23f3467945f72eb3903c7144ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59629723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3e34110a34484bb2b5fc92bb618d5407446d1bc3400e8d4f8b36f8993e40035`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 22 Jul 2021 02:07:27 GMT
ADD file:86bd875241ca751f2f50a9c3504cfca4ce772411fed23fe6893299a271c275e3 in / 
# Thu, 22 Jul 2021 02:07:28 GMT
CMD ["bash"]
# Tue, 10 Aug 2021 23:00:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 Aug 2021 17:57:54 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 11 Aug 2021 17:58:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 Aug 2021 17:58:15 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 Aug 2021 17:58:15 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 Aug 2021 17:58:16 GMT
EXPOSE 8888
# Wed, 11 Aug 2021 17:58:16 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 Aug 2021 17:58:17 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 Aug 2021 17:58:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Aug 2021 17:58:18 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:37325b08023150a9e16c0c8d98d10daa998ce21ec3b9226cc6f0148a245a8a57`  
		Last Modified: Thu, 22 Jul 2021 02:21:16 GMT  
		Size: 19.3 MB (19315955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84236a4145013894eb753d54367ba39e700f41448379d11fb8acf79e2100e630`  
		Last Modified: Tue, 10 Aug 2021 23:03:14 GMT  
		Size: 5.8 MB (5779562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c94e453b1526664141d2e656e2d459e6bdfe67c0125787e512a756b9ffd8d66`  
		Last Modified: Wed, 11 Aug 2021 17:59:24 GMT  
		Size: 34.5 MB (34509822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd08ad62061e36c850fea016d5e524bdd6e212a10f058ab27f66eafbf0f655ed`  
		Last Modified: Wed, 11 Aug 2021 17:59:07 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb0c19cb6001660e07df3fe79b9cf16cf6e70069f6ba63823f7ae328aecb1ac`  
		Last Modified: Wed, 11 Aug 2021 17:59:06 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79345035daad04e1a83f087e06fdc0ea2ed3cae344a24786d56721c803df31e4`  
		Last Modified: Wed, 11 Aug 2021 17:59:06 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:50bb95ad8e75c72c6c78f2adc41fa1e4e65c9ce606149939014765140436b714
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60893485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab2558c75bff2c996f9ab8ade4d2b02c8527c43f5217aaec182a7c2ef4bc3a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Aug 2021 01:48:32 GMT
ADD file:5cd26935234cc0540158a144066c0341b46a0caeb0a80db0355eeb8cfaf4fc0d in / 
# Tue, 17 Aug 2021 01:48:32 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:06:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 17 Aug 2021 08:07:26 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 17 Aug 2021 08:07:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 17 Aug 2021 08:07:34 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 17 Aug 2021 08:07:34 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 17 Aug 2021 08:07:34 GMT
EXPOSE 8888
# Tue, 17 Aug 2021 08:07:35 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Aug 2021 08:07:35 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 17 Aug 2021 08:07:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 08:07:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f862659192cd149f96ede75854bd3ebf59937831d3e4103087ae62df34ef1a29`  
		Last Modified: Tue, 17 Aug 2021 01:58:00 GMT  
		Size: 20.4 MB (20389447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09101c696c7496dfd097387796cbe96c76aa138b186200c5879c0ab29f5a13f4`  
		Last Modified: Tue, 17 Aug 2021 08:08:19 GMT  
		Size: 6.0 MB (6047480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dde8e33fe3c76bb15079dbf979e7a62649160f833f7b79c87e509274572b830`  
		Last Modified: Tue, 17 Aug 2021 08:08:54 GMT  
		Size: 34.4 MB (34432168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d5bfc7c7d8d7f65b1f51b16ceaecf855e71888a5698056ab8ec5637c6840df`  
		Last Modified: Tue, 17 Aug 2021 08:08:49 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5940fd5898023978d247df91489e6acb6c1faa54e057c808855af070b0ee5eb`  
		Last Modified: Tue, 17 Aug 2021 08:08:49 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed27ffdb1a1c2b0057c08793346e56e346582bc736e47db7707e2eb7c3c1846`  
		Last Modified: Tue, 17 Aug 2021 08:08:49 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:8f39edc24654fbd11f32e9e80229bbe27370cfa1f87d22cb39bb05d45f413594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:9a9ca1c1267bc671715843e0353e85bc10e7562e47924589893ea721baaecfe4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22309890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3802774693dc4a8d1ae2e3fc1443f2abc4fa439c8da2c33bc9631627cad1363`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:12:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:12:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 11 Aug 2021 18:19:56 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 11 Aug 2021 18:20:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 11 Aug 2021 18:20:03 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 Aug 2021 18:20:03 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 Aug 2021 18:20:03 GMT
EXPOSE 8888
# Wed, 11 Aug 2021 18:20:03 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 Aug 2021 18:20:03 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 11 Aug 2021 18:20:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Aug 2021 18:20:04 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4496f95da0ff203c55ba4ff45e6cc518bfd24507a21516931244d25e8db7d14`  
		Last Modified: Wed, 14 Apr 2021 20:13:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9162e7666a3906b38fdfed2592cc2e4df967e365a3fcf17c8d6320caed7fd960`  
		Last Modified: Wed, 14 Apr 2021 20:13:33 GMT  
		Size: 280.9 KB (280875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c29671357b22bf6c966f84c718c8cd16c7e8ce22e40cbdf87aceb248ad2206`  
		Last Modified: Wed, 11 Aug 2021 18:20:49 GMT  
		Size: 19.2 MB (19203896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef01851ecfdf47c32aefac2145603c02cb9aef56d95f3daaef616e6ed684a21`  
		Last Modified: Wed, 11 Aug 2021 18:20:46 GMT  
		Size: 12.3 KB (12264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d28858f637808b758c6047a197bd7e0e4e9fc975d9d7df3a67bcb3aaece355`  
		Last Modified: Wed, 11 Aug 2021 18:20:46 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8a411f207f7b3c2682ac77fdc8a28e9b3f645c46d53fdb3437c0ade731cb1a`  
		Last Modified: Wed, 11 Aug 2021 18:20:46 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:1e853b1238b1e0be115478df25e71decdef01bf186934f3a3cc85ecbd51b6e07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9` - linux; amd64

```console
$ docker pull chronograf@sha256:d30b8a1f515a1f68ac7675f55026ef00b5c9510dde3c84e552ceafbd8da84fd5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66757353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071d9a46cb06f25d04e299d93f99d10334cd8b43d697b016191c1f87004f0c27`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Aug 2021 01:26:09 GMT
ADD file:f6c4487fa1f7a4e17f5d88fd0c91031a6efc7fa210d363a1d43d8b0f3a8d1d03 in / 
# Tue, 17 Aug 2021 01:26:09 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:35:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 17 Aug 2021 09:36:21 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Tue, 17 Aug 2021 09:36:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 17 Aug 2021 09:36:30 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 17 Aug 2021 09:36:30 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 17 Aug 2021 09:36:31 GMT
EXPOSE 8888
# Tue, 17 Aug 2021 09:36:31 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Aug 2021 09:36:31 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 17 Aug 2021 09:36:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 09:36:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:33f99cea3b7da8c6e0143c9fd7590c6d56f7d310ddd59b11be4ad485ae4cab2a`  
		Last Modified: Tue, 17 Aug 2021 01:33:27 GMT  
		Size: 22.5 MB (22527748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ebf00cee8edb2723f73bb596dc02dac400fcd609c6288b968066e0333dc5cd`  
		Last Modified: Tue, 17 Aug 2021 09:37:00 GMT  
		Size: 6.8 MB (6760152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88d589540170378ab6422d641b642a6aa1e3fd063d84997f3d21de4c5f78981`  
		Last Modified: Tue, 17 Aug 2021 09:37:53 GMT  
		Size: 37.4 MB (37445059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e800a265cf9be534a8fe5b59b309a201c2663c6741f7c25aa4227364f32b4ba5`  
		Last Modified: Tue, 17 Aug 2021 09:37:46 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab0427bfc914c791fecbe16f14d108518b4438951f2dd347355fabc74377f53`  
		Last Modified: Tue, 17 Aug 2021 09:37:47 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded1c3ae33fb215a5bba57e059b94f9659e7950e44b102640e396f3bf7c72b01`  
		Last Modified: Tue, 17 Aug 2021 09:37:46 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:6b4d9dab676c63e970b0e8101bd9f17c9af30dadc55631be78288516e4ffa609
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60284073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf2a6a20b47c0aef2fa06438bde8605c3f435a9c57d66c726d023d2dccd09573`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 22 Jul 2021 02:07:27 GMT
ADD file:86bd875241ca751f2f50a9c3504cfca4ce772411fed23fe6893299a271c275e3 in / 
# Thu, 22 Jul 2021 02:07:28 GMT
CMD ["bash"]
# Tue, 10 Aug 2021 23:00:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 13 Aug 2021 06:28:57 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Fri, 13 Aug 2021 06:29:16 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 13 Aug 2021 06:29:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 13 Aug 2021 06:29:17 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 13 Aug 2021 06:29:17 GMT
EXPOSE 8888
# Fri, 13 Aug 2021 06:29:18 GMT
VOLUME [/var/lib/chronograf]
# Fri, 13 Aug 2021 06:29:18 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 13 Aug 2021 06:29:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Aug 2021 06:29:19 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:37325b08023150a9e16c0c8d98d10daa998ce21ec3b9226cc6f0148a245a8a57`  
		Last Modified: Thu, 22 Jul 2021 02:21:16 GMT  
		Size: 19.3 MB (19315955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84236a4145013894eb753d54367ba39e700f41448379d11fb8acf79e2100e630`  
		Last Modified: Tue, 10 Aug 2021 23:03:14 GMT  
		Size: 5.8 MB (5779562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37782ef560f704f577d6c716b1a84964308a1eda9f974593cb3f992eb436b1d3`  
		Last Modified: Fri, 13 Aug 2021 06:30:37 GMT  
		Size: 35.2 MB (35164164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4e5a09faa859d2865494cb8bef25a36860f7b8db37e1e426dcaeabfef50695`  
		Last Modified: Fri, 13 Aug 2021 06:30:20 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:475598b1dbd9c2d21faf7ca2681f77a5aeb9b3800c4736a16b03edf0e52e3715`  
		Last Modified: Fri, 13 Aug 2021 06:30:19 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0d85b0819b5afcc042ba75990fef9a0279e037da03505944d65154a7d662c9`  
		Last Modified: Fri, 13 Aug 2021 06:30:19 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:b2ebe33396b3deb42dbdc543bc92331a8a242813e8705f7d9cc0bbd5a84a048d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61522879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1378f77cfd03e8e67afd75650a3fbc1ac23364337d73d700d99a7d4693d19887`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Aug 2021 01:48:32 GMT
ADD file:5cd26935234cc0540158a144066c0341b46a0caeb0a80db0355eeb8cfaf4fc0d in / 
# Tue, 17 Aug 2021 01:48:32 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:06:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 17 Aug 2021 08:07:40 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Tue, 17 Aug 2021 08:07:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 17 Aug 2021 08:07:49 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 17 Aug 2021 08:07:49 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 17 Aug 2021 08:07:49 GMT
EXPOSE 8888
# Tue, 17 Aug 2021 08:07:49 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Aug 2021 08:07:49 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 17 Aug 2021 08:07:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 08:07:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f862659192cd149f96ede75854bd3ebf59937831d3e4103087ae62df34ef1a29`  
		Last Modified: Tue, 17 Aug 2021 01:58:00 GMT  
		Size: 20.4 MB (20389447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09101c696c7496dfd097387796cbe96c76aa138b186200c5879c0ab29f5a13f4`  
		Last Modified: Tue, 17 Aug 2021 08:08:19 GMT  
		Size: 6.0 MB (6047480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460f0536e20a65b2904cd15722337b7302f9c0dab6e10fb222940f49a6075215`  
		Last Modified: Tue, 17 Aug 2021 08:09:10 GMT  
		Size: 35.1 MB (35061557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010e9e427ef0ba79f667341edbabc8feb479b8c29c1c343bfc81e25b644480fb`  
		Last Modified: Tue, 17 Aug 2021 08:09:05 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ee27ad129e4bae5379fe5fe8edc5931a22031014148bc4d5b24e6e6c56421a`  
		Last Modified: Tue, 17 Aug 2021 08:09:05 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed64ace818385e3d03fa5b6dc95f4092a80eb5838be8fef6a05f07dd5162c74`  
		Last Modified: Tue, 17 Aug 2021 08:09:05 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:0e92cd8e5bffb3d7a2c0046654d344577e83857fa4cbeac05ea0cbd5cd1c9f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:980814eea80aee1882d0b5eaa435a7586c5031854e70fd4cf67c04d8ea9d76ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22688093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f0680cdef28aa807912648c6e2ed3390dee1ca5c488667b5358adf99f1cf3a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:12:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:12:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 12 Aug 2021 21:27:49 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Thu, 12 Aug 2021 21:27:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 12 Aug 2021 21:27:56 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 12 Aug 2021 21:27:56 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 12 Aug 2021 21:27:56 GMT
EXPOSE 8888
# Thu, 12 Aug 2021 21:27:57 GMT
VOLUME [/var/lib/chronograf]
# Thu, 12 Aug 2021 21:27:57 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Thu, 12 Aug 2021 21:27:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Aug 2021 21:27:57 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4496f95da0ff203c55ba4ff45e6cc518bfd24507a21516931244d25e8db7d14`  
		Last Modified: Wed, 14 Apr 2021 20:13:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9162e7666a3906b38fdfed2592cc2e4df967e365a3fcf17c8d6320caed7fd960`  
		Last Modified: Wed, 14 Apr 2021 20:13:33 GMT  
		Size: 280.9 KB (280875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42f7db3ff4561067195652cb6cf0d2ea143c3210b1632155a801b8913287643`  
		Last Modified: Thu, 12 Aug 2021 21:28:47 GMT  
		Size: 19.6 MB (19582094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ddf44064e05fc4424aba446e7b1e2bb9d1fa10a2eccd7e4fd88a62685fa903`  
		Last Modified: Thu, 12 Aug 2021 21:28:44 GMT  
		Size: 12.3 KB (12267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf51a4a07a8e17117691a200f92948affc6b8961d1ed2aa35884f13c99dd37e`  
		Last Modified: Thu, 12 Aug 2021 21:28:43 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ac1ca485101773e054a692975c2bf8b90327697782c4af134b99ffdea4600f`  
		Last Modified: Thu, 12 Aug 2021 21:28:43 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.0`

```console
$ docker pull chronograf@sha256:1e853b1238b1e0be115478df25e71decdef01bf186934f3a3cc85ecbd51b6e07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9.0` - linux; amd64

```console
$ docker pull chronograf@sha256:d30b8a1f515a1f68ac7675f55026ef00b5c9510dde3c84e552ceafbd8da84fd5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66757353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071d9a46cb06f25d04e299d93f99d10334cd8b43d697b016191c1f87004f0c27`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Aug 2021 01:26:09 GMT
ADD file:f6c4487fa1f7a4e17f5d88fd0c91031a6efc7fa210d363a1d43d8b0f3a8d1d03 in / 
# Tue, 17 Aug 2021 01:26:09 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:35:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 17 Aug 2021 09:36:21 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Tue, 17 Aug 2021 09:36:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 17 Aug 2021 09:36:30 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 17 Aug 2021 09:36:30 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 17 Aug 2021 09:36:31 GMT
EXPOSE 8888
# Tue, 17 Aug 2021 09:36:31 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Aug 2021 09:36:31 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 17 Aug 2021 09:36:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 09:36:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:33f99cea3b7da8c6e0143c9fd7590c6d56f7d310ddd59b11be4ad485ae4cab2a`  
		Last Modified: Tue, 17 Aug 2021 01:33:27 GMT  
		Size: 22.5 MB (22527748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ebf00cee8edb2723f73bb596dc02dac400fcd609c6288b968066e0333dc5cd`  
		Last Modified: Tue, 17 Aug 2021 09:37:00 GMT  
		Size: 6.8 MB (6760152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88d589540170378ab6422d641b642a6aa1e3fd063d84997f3d21de4c5f78981`  
		Last Modified: Tue, 17 Aug 2021 09:37:53 GMT  
		Size: 37.4 MB (37445059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e800a265cf9be534a8fe5b59b309a201c2663c6741f7c25aa4227364f32b4ba5`  
		Last Modified: Tue, 17 Aug 2021 09:37:46 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab0427bfc914c791fecbe16f14d108518b4438951f2dd347355fabc74377f53`  
		Last Modified: Tue, 17 Aug 2021 09:37:47 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded1c3ae33fb215a5bba57e059b94f9659e7950e44b102640e396f3bf7c72b01`  
		Last Modified: Tue, 17 Aug 2021 09:37:46 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.0` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:6b4d9dab676c63e970b0e8101bd9f17c9af30dadc55631be78288516e4ffa609
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60284073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf2a6a20b47c0aef2fa06438bde8605c3f435a9c57d66c726d023d2dccd09573`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 22 Jul 2021 02:07:27 GMT
ADD file:86bd875241ca751f2f50a9c3504cfca4ce772411fed23fe6893299a271c275e3 in / 
# Thu, 22 Jul 2021 02:07:28 GMT
CMD ["bash"]
# Tue, 10 Aug 2021 23:00:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 13 Aug 2021 06:28:57 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Fri, 13 Aug 2021 06:29:16 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 13 Aug 2021 06:29:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 13 Aug 2021 06:29:17 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 13 Aug 2021 06:29:17 GMT
EXPOSE 8888
# Fri, 13 Aug 2021 06:29:18 GMT
VOLUME [/var/lib/chronograf]
# Fri, 13 Aug 2021 06:29:18 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 13 Aug 2021 06:29:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Aug 2021 06:29:19 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:37325b08023150a9e16c0c8d98d10daa998ce21ec3b9226cc6f0148a245a8a57`  
		Last Modified: Thu, 22 Jul 2021 02:21:16 GMT  
		Size: 19.3 MB (19315955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84236a4145013894eb753d54367ba39e700f41448379d11fb8acf79e2100e630`  
		Last Modified: Tue, 10 Aug 2021 23:03:14 GMT  
		Size: 5.8 MB (5779562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37782ef560f704f577d6c716b1a84964308a1eda9f974593cb3f992eb436b1d3`  
		Last Modified: Fri, 13 Aug 2021 06:30:37 GMT  
		Size: 35.2 MB (35164164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4e5a09faa859d2865494cb8bef25a36860f7b8db37e1e426dcaeabfef50695`  
		Last Modified: Fri, 13 Aug 2021 06:30:20 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:475598b1dbd9c2d21faf7ca2681f77a5aeb9b3800c4736a16b03edf0e52e3715`  
		Last Modified: Fri, 13 Aug 2021 06:30:19 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0d85b0819b5afcc042ba75990fef9a0279e037da03505944d65154a7d662c9`  
		Last Modified: Fri, 13 Aug 2021 06:30:19 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.0` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:b2ebe33396b3deb42dbdc543bc92331a8a242813e8705f7d9cc0bbd5a84a048d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61522879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1378f77cfd03e8e67afd75650a3fbc1ac23364337d73d700d99a7d4693d19887`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Aug 2021 01:48:32 GMT
ADD file:5cd26935234cc0540158a144066c0341b46a0caeb0a80db0355eeb8cfaf4fc0d in / 
# Tue, 17 Aug 2021 01:48:32 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:06:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 17 Aug 2021 08:07:40 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Tue, 17 Aug 2021 08:07:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 17 Aug 2021 08:07:49 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 17 Aug 2021 08:07:49 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 17 Aug 2021 08:07:49 GMT
EXPOSE 8888
# Tue, 17 Aug 2021 08:07:49 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Aug 2021 08:07:49 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 17 Aug 2021 08:07:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 08:07:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f862659192cd149f96ede75854bd3ebf59937831d3e4103087ae62df34ef1a29`  
		Last Modified: Tue, 17 Aug 2021 01:58:00 GMT  
		Size: 20.4 MB (20389447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09101c696c7496dfd097387796cbe96c76aa138b186200c5879c0ab29f5a13f4`  
		Last Modified: Tue, 17 Aug 2021 08:08:19 GMT  
		Size: 6.0 MB (6047480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460f0536e20a65b2904cd15722337b7302f9c0dab6e10fb222940f49a6075215`  
		Last Modified: Tue, 17 Aug 2021 08:09:10 GMT  
		Size: 35.1 MB (35061557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010e9e427ef0ba79f667341edbabc8feb479b8c29c1c343bfc81e25b644480fb`  
		Last Modified: Tue, 17 Aug 2021 08:09:05 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ee27ad129e4bae5379fe5fe8edc5931a22031014148bc4d5b24e6e6c56421a`  
		Last Modified: Tue, 17 Aug 2021 08:09:05 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed64ace818385e3d03fa5b6dc95f4092a80eb5838be8fef6a05f07dd5162c74`  
		Last Modified: Tue, 17 Aug 2021 08:09:05 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.0-alpine`

```console
$ docker pull chronograf@sha256:0e92cd8e5bffb3d7a2c0046654d344577e83857fa4cbeac05ea0cbd5cd1c9f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9.0-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:980814eea80aee1882d0b5eaa435a7586c5031854e70fd4cf67c04d8ea9d76ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22688093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f0680cdef28aa807912648c6e2ed3390dee1ca5c488667b5358adf99f1cf3a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:12:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:12:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 12 Aug 2021 21:27:49 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Thu, 12 Aug 2021 21:27:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 12 Aug 2021 21:27:56 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 12 Aug 2021 21:27:56 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 12 Aug 2021 21:27:56 GMT
EXPOSE 8888
# Thu, 12 Aug 2021 21:27:57 GMT
VOLUME [/var/lib/chronograf]
# Thu, 12 Aug 2021 21:27:57 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Thu, 12 Aug 2021 21:27:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Aug 2021 21:27:57 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4496f95da0ff203c55ba4ff45e6cc518bfd24507a21516931244d25e8db7d14`  
		Last Modified: Wed, 14 Apr 2021 20:13:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9162e7666a3906b38fdfed2592cc2e4df967e365a3fcf17c8d6320caed7fd960`  
		Last Modified: Wed, 14 Apr 2021 20:13:33 GMT  
		Size: 280.9 KB (280875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42f7db3ff4561067195652cb6cf0d2ea143c3210b1632155a801b8913287643`  
		Last Modified: Thu, 12 Aug 2021 21:28:47 GMT  
		Size: 19.6 MB (19582094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ddf44064e05fc4424aba446e7b1e2bb9d1fa10a2eccd7e4fd88a62685fa903`  
		Last Modified: Thu, 12 Aug 2021 21:28:44 GMT  
		Size: 12.3 KB (12267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf51a4a07a8e17117691a200f92948affc6b8961d1ed2aa35884f13c99dd37e`  
		Last Modified: Thu, 12 Aug 2021 21:28:43 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ac1ca485101773e054a692975c2bf8b90327697782c4af134b99ffdea4600f`  
		Last Modified: Thu, 12 Aug 2021 21:28:43 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:0e92cd8e5bffb3d7a2c0046654d344577e83857fa4cbeac05ea0cbd5cd1c9f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:980814eea80aee1882d0b5eaa435a7586c5031854e70fd4cf67c04d8ea9d76ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22688093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f0680cdef28aa807912648c6e2ed3390dee1ca5c488667b5358adf99f1cf3a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:12:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:12:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 12 Aug 2021 21:27:49 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Thu, 12 Aug 2021 21:27:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 12 Aug 2021 21:27:56 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 12 Aug 2021 21:27:56 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 12 Aug 2021 21:27:56 GMT
EXPOSE 8888
# Thu, 12 Aug 2021 21:27:57 GMT
VOLUME [/var/lib/chronograf]
# Thu, 12 Aug 2021 21:27:57 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Thu, 12 Aug 2021 21:27:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Aug 2021 21:27:57 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4496f95da0ff203c55ba4ff45e6cc518bfd24507a21516931244d25e8db7d14`  
		Last Modified: Wed, 14 Apr 2021 20:13:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9162e7666a3906b38fdfed2592cc2e4df967e365a3fcf17c8d6320caed7fd960`  
		Last Modified: Wed, 14 Apr 2021 20:13:33 GMT  
		Size: 280.9 KB (280875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42f7db3ff4561067195652cb6cf0d2ea143c3210b1632155a801b8913287643`  
		Last Modified: Thu, 12 Aug 2021 21:28:47 GMT  
		Size: 19.6 MB (19582094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ddf44064e05fc4424aba446e7b1e2bb9d1fa10a2eccd7e4fd88a62685fa903`  
		Last Modified: Thu, 12 Aug 2021 21:28:44 GMT  
		Size: 12.3 KB (12267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf51a4a07a8e17117691a200f92948affc6b8961d1ed2aa35884f13c99dd37e`  
		Last Modified: Thu, 12 Aug 2021 21:28:43 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ac1ca485101773e054a692975c2bf8b90327697782c4af134b99ffdea4600f`  
		Last Modified: Thu, 12 Aug 2021 21:28:43 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:1e853b1238b1e0be115478df25e71decdef01bf186934f3a3cc85ecbd51b6e07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:d30b8a1f515a1f68ac7675f55026ef00b5c9510dde3c84e552ceafbd8da84fd5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66757353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071d9a46cb06f25d04e299d93f99d10334cd8b43d697b016191c1f87004f0c27`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Aug 2021 01:26:09 GMT
ADD file:f6c4487fa1f7a4e17f5d88fd0c91031a6efc7fa210d363a1d43d8b0f3a8d1d03 in / 
# Tue, 17 Aug 2021 01:26:09 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:35:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 17 Aug 2021 09:36:21 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Tue, 17 Aug 2021 09:36:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 17 Aug 2021 09:36:30 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 17 Aug 2021 09:36:30 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 17 Aug 2021 09:36:31 GMT
EXPOSE 8888
# Tue, 17 Aug 2021 09:36:31 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Aug 2021 09:36:31 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 17 Aug 2021 09:36:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 09:36:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:33f99cea3b7da8c6e0143c9fd7590c6d56f7d310ddd59b11be4ad485ae4cab2a`  
		Last Modified: Tue, 17 Aug 2021 01:33:27 GMT  
		Size: 22.5 MB (22527748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ebf00cee8edb2723f73bb596dc02dac400fcd609c6288b968066e0333dc5cd`  
		Last Modified: Tue, 17 Aug 2021 09:37:00 GMT  
		Size: 6.8 MB (6760152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88d589540170378ab6422d641b642a6aa1e3fd063d84997f3d21de4c5f78981`  
		Last Modified: Tue, 17 Aug 2021 09:37:53 GMT  
		Size: 37.4 MB (37445059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e800a265cf9be534a8fe5b59b309a201c2663c6741f7c25aa4227364f32b4ba5`  
		Last Modified: Tue, 17 Aug 2021 09:37:46 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab0427bfc914c791fecbe16f14d108518b4438951f2dd347355fabc74377f53`  
		Last Modified: Tue, 17 Aug 2021 09:37:47 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded1c3ae33fb215a5bba57e059b94f9659e7950e44b102640e396f3bf7c72b01`  
		Last Modified: Tue, 17 Aug 2021 09:37:46 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:6b4d9dab676c63e970b0e8101bd9f17c9af30dadc55631be78288516e4ffa609
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60284073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf2a6a20b47c0aef2fa06438bde8605c3f435a9c57d66c726d023d2dccd09573`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 22 Jul 2021 02:07:27 GMT
ADD file:86bd875241ca751f2f50a9c3504cfca4ce772411fed23fe6893299a271c275e3 in / 
# Thu, 22 Jul 2021 02:07:28 GMT
CMD ["bash"]
# Tue, 10 Aug 2021 23:00:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 13 Aug 2021 06:28:57 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Fri, 13 Aug 2021 06:29:16 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 13 Aug 2021 06:29:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 13 Aug 2021 06:29:17 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 13 Aug 2021 06:29:17 GMT
EXPOSE 8888
# Fri, 13 Aug 2021 06:29:18 GMT
VOLUME [/var/lib/chronograf]
# Fri, 13 Aug 2021 06:29:18 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 13 Aug 2021 06:29:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Aug 2021 06:29:19 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:37325b08023150a9e16c0c8d98d10daa998ce21ec3b9226cc6f0148a245a8a57`  
		Last Modified: Thu, 22 Jul 2021 02:21:16 GMT  
		Size: 19.3 MB (19315955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84236a4145013894eb753d54367ba39e700f41448379d11fb8acf79e2100e630`  
		Last Modified: Tue, 10 Aug 2021 23:03:14 GMT  
		Size: 5.8 MB (5779562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37782ef560f704f577d6c716b1a84964308a1eda9f974593cb3f992eb436b1d3`  
		Last Modified: Fri, 13 Aug 2021 06:30:37 GMT  
		Size: 35.2 MB (35164164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4e5a09faa859d2865494cb8bef25a36860f7b8db37e1e426dcaeabfef50695`  
		Last Modified: Fri, 13 Aug 2021 06:30:20 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:475598b1dbd9c2d21faf7ca2681f77a5aeb9b3800c4736a16b03edf0e52e3715`  
		Last Modified: Fri, 13 Aug 2021 06:30:19 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0d85b0819b5afcc042ba75990fef9a0279e037da03505944d65154a7d662c9`  
		Last Modified: Fri, 13 Aug 2021 06:30:19 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:b2ebe33396b3deb42dbdc543bc92331a8a242813e8705f7d9cc0bbd5a84a048d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61522879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1378f77cfd03e8e67afd75650a3fbc1ac23364337d73d700d99a7d4693d19887`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Aug 2021 01:48:32 GMT
ADD file:5cd26935234cc0540158a144066c0341b46a0caeb0a80db0355eeb8cfaf4fc0d in / 
# Tue, 17 Aug 2021 01:48:32 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:06:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 17 Aug 2021 08:07:40 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Tue, 17 Aug 2021 08:07:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 17 Aug 2021 08:07:49 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 17 Aug 2021 08:07:49 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 17 Aug 2021 08:07:49 GMT
EXPOSE 8888
# Tue, 17 Aug 2021 08:07:49 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Aug 2021 08:07:49 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 17 Aug 2021 08:07:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 08:07:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f862659192cd149f96ede75854bd3ebf59937831d3e4103087ae62df34ef1a29`  
		Last Modified: Tue, 17 Aug 2021 01:58:00 GMT  
		Size: 20.4 MB (20389447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09101c696c7496dfd097387796cbe96c76aa138b186200c5879c0ab29f5a13f4`  
		Last Modified: Tue, 17 Aug 2021 08:08:19 GMT  
		Size: 6.0 MB (6047480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460f0536e20a65b2904cd15722337b7302f9c0dab6e10fb222940f49a6075215`  
		Last Modified: Tue, 17 Aug 2021 08:09:10 GMT  
		Size: 35.1 MB (35061557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010e9e427ef0ba79f667341edbabc8feb479b8c29c1c343bfc81e25b644480fb`  
		Last Modified: Tue, 17 Aug 2021 08:09:05 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ee27ad129e4bae5379fe5fe8edc5931a22031014148bc4d5b24e6e6c56421a`  
		Last Modified: Tue, 17 Aug 2021 08:09:05 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed64ace818385e3d03fa5b6dc95f4092a80eb5838be8fef6a05f07dd5162c74`  
		Last Modified: Tue, 17 Aug 2021 08:09:05 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
